---
title: Flags extension for iOS integration guide
description: Learn how to integrate the Flags extension with the Adobe Experience Platform Mobile SDK on iOS.
hide: true
---
# Flags extension for iOS {#ios-extension-integration-guide}

This guide describes how to integrate the Flags extension with the Adobe Experience Platform Mobile SDK on iOS.

## Prerequisites {#prerequisites}

Before implementing the Flags extension, ensure you have:

* A mobile property configured in [Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection)
* The Flags extension installed and configured in your mobile property
* An Adobe Experience Cloud Organization ID
* Minimum deployment target: iOS 12.0

## Extension dependencies {#extension-dependencies}

The Flags extension requires the following Adobe Experience Platform extensions:

| Extension | Description | Required |
|---|---|---|
| Mobile Core | Provides core functionality including configuration and event processing | Yes |
| Lifecycle | Collects application lifecycle and session data for the Mobile SDK | Yes |
| Edge Network | Enables communication with Adobe Experience Platform Edge Network | Yes |
| Edge Identity | Enables identity management from a mobile app when using the Edge Network extension | Yes |

Ensure these extensions are installed in your Data Collection mobile property and included in your app dependencies.

## Configure Flags extension in Data Collection {#configure}

### Install the extension {#install-extension}

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection).
1. Select the **Tags** tab and choose your mobile property.
1. Navigate to **Extensions** > **Catalog**.
1. Search for **Flags extension** and select **Install**.
1. Configure the extension settings:

   | Setting | Description |
   |---|---|
   | Application ID | A unique identifier for your application in Flags |

1. Select **Save**.
1. Follow the [publishing process](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) to update your configuration.

### Get the Environment File ID {#environment-file-id}

1. In your mobile property, navigate to **Environments**.
1. Select the box icon under the **Install** column for your environment.
1. In the **Mobile Install Instructions** dialog, copy the **Environment File ID**.

## Add Flags extension to your app {#add-to-app}

### Add dependencies {#add-dependencies}

Add the Mobile SDK dependencies to your project. The Flags extension requires Mobile Core and the Edge-related extensions listed below.

#### Using Swift Package Manager {#swift-package-manager}

In Xcode, select **File** > **Add Packages** and add the following Adobe Experience Platform Mobile SDK package URLs:

| Package | URL |
|---|---|
| AEPCore | `https://github.com/adobe/aepsdk-core-ios.git` |
| AEPEdge | `https://github.com/adobe/aepsdk-edge-ios.git` |
| AEPEdgeIdentity | `https://github.com/adobe/aepsdk-edgeidentity-ios.git` |

When prompted, select the following libraries to add to your target:

* `AEPCore`, `AEPLifecycle` (from `aepsdk-core-ios`)
* `AEPEdge` (from `aepsdk-edge-ios`)
* `AEPEdgeIdentity` (from `aepsdk-edgeidentity-ios`)

Use AEPCore 5.8.0 or later.

>[!NOTE]
>
>When adding a package in Xcode, choose a dependency rule for each package (for example **Up to Next Major Version**), which picks up new minor and patch releases automatically while excluding the next major version. For the latest released versions, check each extension's releases page on GitHub.

### Add the Flags package {#add-flags-package}

Use either the Swift package or the XCFramework integration method for an app target, not both.

#### For an Xcode project without a Package.swift file {#xcode-project}

1. In Xcode, select **File** > **Add Packages**.
1. Select **Add Local**.
1. Select the supplied `Packages/AEPFlags` directory that contains `Package.swift`.
1. Add the `AEPFlags` library to your application target.

Xcode stores the local package reference in the project, so your application does not need its own `Package.swift` file.

#### For a project with a Package.swift file {#package-swift-project}

In your existing manifest, add `AEPFlags` to your application target dependencies and add the binary target using the URL and checksum from the supplied manifest:

```swift
targets: [
    .target(
        name: "YourApp",
        dependencies: [
            "AEPFlags"
        ]
    ),
    .binaryTarget(
        name: "AEPFlags",
        url: "<AEPFlags binary URL>",
        checksum: "<AEPFlags binary checksum>"
    )
]
```

Swift Package Manager resolves the binary target for local Xcode, CI, and archive builds.

#### Add the XCFramework directly {#xcframework}

Alternatively, drag the supplied `AEPFlags.xcframework` into the Xcode project navigator and add it to your application target. Under **General** > **Frameworks, Libraries, and Embedded Content**, set the framework to **Embed & Sign**.

### Initialize the SDK {#initialize-sdk}

Register the Mobile SDK extensions in your `AppDelegate` before calling any Flags APIs. Register `Flag` after Identity, Edge, and Lifecycle, then configure the SDK using the Environment File ID from your mobile property.

#### Register and configure extensions {#register-configure}

>[!IMPORTANT]
>
>For production apps, use `.error` log level only; do not use `.debug` or `.trace` in release builds.

**Swift**

```swift
// AppDelegate.swift
import AEPCore
import AEPLifecycle
import AEPEdge
import AEPEdgeIdentity
import AEPFlags
import UIKit

final class AppDelegate: NSObject, UIApplicationDelegate {

    func application(_: UIApplication,
                      didFinishLaunchingWithOptions _: [UIApplication.LaunchOptionsKey: Any]? = nil) -> Bool {
        // Production: use .error only. Do not use .debug or .trace in release builds.
        MobileCore.setLogLevel(.error)

        MobileCore.registerExtensions([
            Identity.self,
            Edge.self,
            Lifecycle.self,
            Flag.self
        ]) {
            MobileCore.configureWith(appId: "YOUR_ENVIRONMENT_FILE_ID")
            MobileCore.lifecycleStart(additionalContextData: nil)
        }

        return true
    }
}
```

**Objective-C**

```objc
// AppDelegate.m
#import "AppDelegate.h"
@import AEPCore;
@import AEPLifecycle;
@import AEPEdge;
@import AEPEdgeIdentity;
@import AEPFlags;

@implementation AppDelegate

- (BOOL)application:(UIApplication *)application
    didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {

    // Production: use AEPLogLevelError only. Do not use Debug or Trace in release builds.
    [AEPMobileCore setLogLevel:AEPLogLevelError];

    [AEPMobileCore registerExtensions:@[
        AEPMobileEdgeIdentity.class,
        AEPMobileEdge.class,
        AEPMobileLifecycle.class,
        AEPMobileFlag.class
    ] completion:^{
        [AEPMobileCore configureWithAppId:@"YOUR_ENVIRONMENT_FILE_ID"];
        [AEPMobileCore lifecycleStart:nil];
    }];

    return YES;
}

@end
```

## Evaluation context {#evaluation-context}

`FeatureEvaluationContext` includes targeting attributes (used for flag rule matching).

| Parameter | Required | Description |
|---|---|---|
| `attributes` | No | `[String: [String]]`. Key is the context attribute name used by your flag rules (for example `locale`, `platform`, `appVersion`, `deviceType`). Value is the list of candidate attribute values for that key for the current user/session (for example `["en_US"]` or `["phone"]`). |

**Swift**

```swift
import AEPFlags

let attrs: [String: [String]] = [
    "locale": ["en_US"],
    "platform": ["IOS"],
    "appVersion": ["3.0.0"]
]

let ctx = FeatureEvaluationContext.builder()
    .withAttributes(attrs)
    .build()
```

**Objective-C**

```objc
@import AEPFlags;

NSDictionary<NSString *, NSArray<NSString *> *> *attrs = @{
    @"locale": @[@"en_US"],
    @"platform": @[@"IOS"],
    @"appVersion": @[@"3.0.0"]
};

AEPFeatureEvaluationContextBuilder *builder = [AEPFeatureEvaluationContext builder];
AEPFeatureEvaluationContext *ctx = [[builder withAttributes:attrs] build];
```

### Sample targeting attributes {#sample-attributes}

| Attribute | Description | Example values |
|---|---|---|
| `locale` | User's locale/language | `["en_US"]`, `["fr_FR"]` |
| `platform` | Platform identifier | `["IOS"]` |
| `appVersion` | Application version | `["3.0.0"]` |
| `deviceType` | Device type | `["phone"]`, `["tablet"]` |

### Custom identity {#custom-identity}

The Flags extension uses the Identity for Edge Network extension for identity resolution. A feature flag can be cohorted on a custom identity (for example, a CRM ID or a loyalty ID) so that variant splits and analytics are tied to the identity that matters to your application.

The custom identity namespace must be selected in the Flags UI when the feature flag is authored. To evaluate a flag against that identity, the same identity must be present in the Edge Identity `identityMap` on the device, using the matching namespace. Provide it at runtime with the Identity for Edge Network `updateIdentities` API.

#### Add the custom identity to the Identity Map {#add-identity}

Add the identity under the same namespace configured on the feature flag.

**Swift**

```swift
import AEPEdgeIdentity

let identityMap = IdentityMap()
identityMap.add(item: IdentityItem(id: "1111", authenticatedState: .authenticated, primary: true),
                 withNamespace: "userCRMId") // must match the namespace configured on the feature flag
Identity.updateIdentities(with: identityMap)
```

**Objective-C**

```objc
@import AEPEdgeIdentity;

AEPIdentityItem *item = [[AEPIdentityItem alloc]
    initWithId:@"1111"
    authenticatedState:AEPAuthenticatedStateAuthenticated
    primary:YES];
AEPIdentityMap *identityMap = [[AEPIdentityMap alloc] init];
[identityMap addItem:item withNamespace:@"userCRMId"]; // must match the namespace configured on the feature flag
[AEPMobileEdgeIdentity updateIdentities:identityMap];
```

## API reference {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled` returns whether a Flags feature is on or off for the given context. Pass `featureKey`, a `FeatureEvaluationContext` (optional targeting attributes), and a completion closure. See [Evaluation context](#evaluation-context).

**Signature**

*Swift*

```swift
static func isFeatureEnabled(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (Bool) -> Void
)
```

*Objective-C*

```objc
+ (void)isFeatureEnabled:(NSString *)featureKey
       evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
               completion:(void (^)(BOOL))completion;
```

**Parameters**

| Parameter | Type | Description |
|---|---|---|
| `featureKey` | String | Feature key to evaluate in Flags |
| `evaluationContext` | FeatureEvaluationContext | Include targeting attributes as needed; use `FeatureEvaluationContext.builder().build()` for an empty context. See [Evaluation context](#evaluation-context). |
| `completion` | `(Bool) -> Void` | Called with `true` if the feature is enabled, `false` otherwise. |

**Examples**

*Swift*

```swift
import AEPFlags

Flag.isFeatureEnabled(
    "new-flag",
    evaluationContext: ctx
) { isEnabled in
    if isEnabled {
        // Feature is enabled: run the feature-specific behavior
    } else {
        // Feature is disabled: fall back to the default behavior
    }
}
```

*Objective-C*

```objc
@import AEPFlags;

[AEPMobileFlag isFeatureEnabled:@"new-flag"
              evaluationContext:ctx
                      completion:^(BOOL isEnabled) {
    if (isEnabled) {
        // Feature is enabled: run the feature-specific behavior
    } else {
        // Feature is disabled: fall back to the default behavior
    }
}];
```

### getFeature {#get-feature}

`getFeature` returns the evaluated feature payload for the provided context. Use this API when you need more than enabled/disabled and want feature metadata or values.

**Signature**

*Swift*

```swift
static func getFeature(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (FeatureEvaluationResult?) -> Void
)
```

*Objective-C*

```objc
+ (void)getFeature:(NSString *)featureKey
 evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
        completion:(void (^)(AEPFeatureEvaluationResult * _Nullable))completion;
```

**Parameters**

| Parameter | Type | Description |
|---|---|---|
| `featureKey` | String | Feature key to evaluate in Flags |
| `evaluationContext` | FeatureEvaluationContext | Include targeting attributes as needed; use `FeatureEvaluationContext.builder().build()` for an empty context. See [Evaluation context](#evaluation-context). |
| `completion` | `(FeatureEvaluationResult?) -> Void` | Called with the evaluated feature payload; `nil` when the feature is not found. |

**Response**

*FeatureEvaluationResult*

| Field | Type | Description |
|---|---|---|
| `id` | Int | Numeric feature identifier |
| `key` | String | Feature key |
| `featureGroupKey` | String? | Feature group key when available |
| `meta` | String? | Opaque feature metadata when available |
| `analyticsParam` | AnalyticsParam? | Analytics details for the evaluated feature |

*AnalyticsParam*

| Field | Type | Description |
|---|---|---|
| `featureGroupId` | Int | Numeric feature group identifier |
| `featureId` | Int | Numeric feature identifier |
| `variantId` | String? | Variant identifier |

**Examples**

*Swift*

```swift
import AEPFlags

Flag.getFeature(
    "new-flag",
    evaluationContext: ctx
) { feature in
    guard let meta = feature?.meta, !meta.isEmpty else {
        // No metadata available: fall back to the default behavior
        return
    }
    // Feature metadata is available: use it to drive the feature behavior
}
```

*Objective-C*

```objc
@import AEPFlags;

[AEPMobileFlag getFeature:@"new-flag"
        evaluationContext:ctx
                completion:^(AEPFeatureEvaluationResult * _Nullable feature) {
    NSString *meta = feature.meta;
    if (meta.length > 0) {
        // Feature metadata is available: use it to drive the feature behavior
    } else {
        // No metadata available: fall back to the default behavior
    }
}];
```

### extensionVersion {#extension-version}

Returns the version string of the Flags extension.

**Syntax**

*Swift*

```swift
static var extensionVersion: String
```

*Objective-C*

```objc
+ (nonnull NSString *)flagExtensionVersion;
```

**Example**

*Swift*

```swift
let version = Flag.extensionVersion
```

*Objective-C*

```objc
NSString *version = [AEPMobileFlag flagExtensionVersion];
```

## API summary {#api-summary}

| API | Returns |
|---|---|
| `isFeatureEnabled(_:evaluationContext:completion:)`. `FeatureEvaluationContext` carries targeting attributes for rules. See [isFeatureEnabled](#is-feature-enabled). | Bool via completion closure |
| `getFeature(_:evaluationContext:completion:)`. Returns the evaluated feature payload for the given context. See [getFeature](#get-feature). | FeatureEvaluationResult? via closure |
| `extensionVersion` | String |

## See also {#see-also}

* [Mobile applications](../../integrate/mobile-applications.md)
* [SDKs](../../integrate/sdks.md)
* [Android extension integration guide](../android/android-extension-integration-guide.md)

<!-- -->
