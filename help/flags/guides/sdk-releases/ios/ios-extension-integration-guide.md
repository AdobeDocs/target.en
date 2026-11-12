---
title: Flags extension for iOS integration guide
description: Learn how to integrate the Flags extension with the Adobe Experience Platform Mobile SDK on iOS.
badge: label="Beta" type="Informative"
hide: true
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
---
# Flags extension for iOS {#ios-extension-integration-guide}

This guide describes how to integrate the Flags extension with the Adobe Experience Platform Mobile SDK on iOS. The source code is available in the [aepsdk-flags-ios](https://github.com/adobe/aepsdk-flags-ios) repository.

## Prerequisites {#prerequisites}

Before you start, make sure you have:

* iOS 12.0 or later, and Swift 5.7 or later
* A mobile property in [Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection)
* These extensions installed and configured in the mobile property:

  | Extension | Description | Minimum SDK version |
  |---|---|---|
  | [Mobile Core](https://developer.adobe.com/client-sdks/home/base/mobile-core/) | Configuration and event processing | AEPCore 5.8.0 |
  | [Lifecycle](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/) | Application lifecycle data | Same as AEPCore |
  | [Edge Network](https://developer.adobe.com/client-sdks/edge/edge-network/) | Communication with Adobe Experience Platform Edge Network. Requires a datastream. | AEPEdge 5.0.2 |
  | [Identity for Edge Network](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) | Identity management for Edge Network | AEPEdgeIdentity 5.0.0 |
  | [Flags](https://experienceleague.adobe.com/en/docs/target/flags/home) | Feature flag evaluation | See [Installation](#installation) |

## Configure Flags in Data Collection {#configure}

### Install the extension {#install-extension}

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection).

1. Select the **[!UICONTROL Tags]** menu and choose your mobile property.

1. Navigate to **[!UICONTROL Extensions]** > **[!UICONTROL Catalog]**.

1. Search for **[!DNL Adobe Flags]** and select **[!UICONTROL Install]**.

   ![](../assets/extension-install.png)

1. Configure the extension settings:

    * **[!UICONTROL Sandbox]**: The Adobe Experience Platform sandbox that contains your Flags configuration.
    * **[!UICONTROL Application ID]**: The identifier of your application in Flags.

1. Select **[!UICONTROL Save]**.

1. Follow the [publishing process](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) to update your configuration.

### Get the Environment File ID {#environment-file-id}

1. In your mobile property, navigate to **[!UICONTROL Environments]**.

1. Select the box icon in the **[!UICONTROL Install]** column of your selected environment.

   ![](../assets/extension-install-2.png)

1. In the **[!UICONTROL Mobile Install Instructions]** dialog, copy the **[!UICONTROL Environment File ID]**.

   ![](../assets/extension-install-3.png)

## Installation {#installation}

Add the extension with either Swift Package Manager or an XCFramework. Use one method per app target.

### Swift Package Manager {#swift-package-manager}

In Xcode:

1. Select **File** > **Add Package Dependencies**.

1. Enter the package URL: `https://github.com/adobe/aepsdk-flags-ios.git`

1. For the version rule, select **Exact Version** and enter the latest version from the [releases page](https://github.com/adobe/aepsdk-flags-ios/releases).

1. Add the `AEPFlags` library to your app target.

1. Add the Adobe packages that the extension depends on, and add their libraries to your app target:

   * `https://github.com/adobe/aepsdk-core-ios.git`: `AEPCore`, `AEPLifecycle`, and `AEPServices`
   * `https://github.com/adobe/aepsdk-edge-ios.git`: `AEPEdge`
   * `https://github.com/adobe/aepsdk-edgeidentity-ios.git`: `AEPEdgeIdentity`

If your project uses a `Package.swift` file, add the dependencies there instead. Replace `<latest-version>` with the latest version from the releases page.

```swift
dependencies: [
    .package(url: "https://github.com/adobe/aepsdk-flags-ios.git", exact: "<latest-version>"),
    .package(url: "https://github.com/adobe/aepsdk-core-ios.git", .upToNextMajor(from: "5.8.0")),
    .package(url: "https://github.com/adobe/aepsdk-edge-ios.git", .upToNextMajor(from: "5.0.2")),
    .package(url: "https://github.com/adobe/aepsdk-edgeidentity-ios.git", .upToNextMajor(from: "5.0.0"))
],
targets: [
    .target(
        name: "YourTarget",
        dependencies: [
            .product(name: "AEPFlags", package: "aepsdk-flags-ios"),
            .product(name: "AEPCore", package: "aepsdk-core-ios"),
            .product(name: "AEPLifecycle", package: "aepsdk-core-ios"),
            .product(name: "AEPServices", package: "aepsdk-core-ios"),
            .product(name: "AEPEdge", package: "aepsdk-edge-ios"),
            .product(name: "AEPEdgeIdentity", package: "aepsdk-edgeidentity-ios")
        ]
    )
]
```

### XCFramework {#xcframework}

1. From the [releases page](https://github.com/adobe/aepsdk-flags-ios/releases), download `AEPFlags-<version>.xcframework.zip` and unzip it.

1. Download the XCFrameworks that the extension depends on from each repository's releases page:

   * [aepsdk-core-ios releases](https://github.com/adobe/aepsdk-core-ios/releases): `AEPCore`, `AEPServices`, `AEPLifecycle`, and `AEPRulesEngine`
   * [aepsdk-edge-ios releases](https://github.com/adobe/aepsdk-edge-ios/releases): `AEPEdge`
   * [aepsdk-edgeidentity-ios releases](https://github.com/adobe/aepsdk-edgeidentity-ios/releases): `AEPEdgeIdentity`

1. In Xcode, select your app target, then open **General** > **Frameworks, Libraries, and Embedded Content**.

1. Add `AEPFlags.xcframework` and all the dependent XCFrameworks.

1. Set each framework to **Embed & Sign**.

## Initialize the SDK {#initialize-sdk}

Register the Flags extension, then initialize the SDK with the Environment File ID from your mobile property. `MobileCore.initialize` does not register the Flags extension for you, so register it first.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPCore
import AEPFlags
import UIKit

class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(
        _ application: UIApplication,
        didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
    ) -> Bool {
        MobileCore.registerExtensions([Flag.self])
        MobileCore.initialize(appId: "<your-environment-file-id>")
        return true
    }
}
```

>[!TAB Objective-C]

```objc
@import AEPCore;
@import AEPFlags;

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    [AEPMobileCore registerExtensions:@[AEPMobileFlag.class] completion:nil];
    [AEPMobileCore initializeWithAppId:@"<your-environment-file-id>" completion:nil];
    return YES;
}
```

>[!ENDTABS]

### Register extensions manually {#register-manually}

If you register extensions yourself, register all of them. Call `MobileCore.lifecycleStart` when the app enters the foreground and `MobileCore.lifecyclePause` when it enters the background.

If your app uses scenes, make these calls in `sceneWillEnterForeground(_:)` and `sceneDidEnterBackground(_:)` instead.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPCore
import AEPEdge
import AEPEdgeIdentity
import AEPFlags
import AEPLifecycle
import UIKit

class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(
        _ application: UIApplication,
        didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
    ) -> Bool {
        MobileCore.registerExtensions([
            Lifecycle.self,
            Edge.self,
            AEPEdgeIdentity.Identity.self,
            Flag.self
        ]) {
            MobileCore.configureWith(appId: "<your-environment-file-id>")
            DispatchQueue.main.async {
                if application.applicationState != .background {
                    MobileCore.lifecycleStart(additionalContextData: nil)
                }
            }
        }
        return true
    }

    func applicationWillEnterForeground(_ application: UIApplication) {
        MobileCore.lifecycleStart(additionalContextData: nil)
    }

    func applicationDidEnterBackground(_ application: UIApplication) {
        MobileCore.lifecyclePause()
    }
}
```

>[!TAB Objective-C]

```objc
@import AEPCore;
@import AEPEdge;
@import AEPEdgeIdentity;
@import AEPFlags;
@import AEPLifecycle;

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    [AEPMobileCore registerExtensions:@[
        AEPMobileLifecycle.class,
        AEPMobileEdge.class,
        AEPMobileEdgeIdentity.class,
        AEPMobileFlag.class
    ] completion:^{
        [AEPMobileCore configureWithAppId:@"<your-environment-file-id>"];
        dispatch_async(dispatch_get_main_queue(), ^{
            if (application.applicationState != UIApplicationStateBackground) {
                [AEPMobileCore lifecycleStart:nil];
            }
        });
    }];
    return YES;
}

- (void)applicationWillEnterForeground:(UIApplication *)application {
    [AEPMobileCore lifecycleStart:nil];
}

- (void)applicationDidEnterBackground:(UIApplication *)application {
    [AEPMobileCore lifecyclePause];
}
```

>[!ENDTABS]

## Evaluation context {#evaluation-context}

Every evaluation call takes a `FeatureEvaluationContext`. It holds the attributes that the targeting rules of your flags use.

| Parameter | Required | Description |
|---|---|---|
| `attributes` | No | `[String: [String]]`. Each key is an attribute name used by your flag targeting rules. Each value is the list of values for the current user. |

* Use attribute names and values that match the targeting rules you defined in Flags.
* Call `withAttributes` at most once per builder. A second call terminates the app.
* To evaluate without attributes, call `build()` without calling `withAttributes`.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPFlags

let context = FeatureEvaluationContext.builder()
    .withAttributes([
        "locale": ["en_US"],
        "appVersion": ["3.0.0"]
    ])
    .build()
```

>[!TAB Objective-C]

```objc
@import AEPFlags;

AEPFeatureEvaluationContext *context = [[[AEPFeatureEvaluationContext builder]
    withAttributes:@{
        @"locale": @[@"en_US"],
        @"appVersion": @[@"3.0.0"]
    }]
    build];
```

>[!ENDTABS]

## Custom identity {#custom-identity}

The Flags extension uses the Identity for Edge Network extension for identity resolution. A feature flag can be cohorted on a custom identity (for example, a CRM ID or a loyalty ID) so that variant splits and analytics are tied to the identity that matters to your application.

The custom identity namespace must be selected in the Flags UI when the feature flag is authored. To evaluate a flag against that identity, the same identity must be present in the Edge Identity `identityMap` on the device, using the matching namespace. Provide it at runtime with the Identity for Edge Network `updateIdentities` API.

### Add the custom identity to the Identity Map {#add-identity}

Add the identity under the same namespace configured on the feature flag.

Note the following behavior:

* The namespace must match the one configured on the flag exactly, including uppercase and lowercase letters.
* If there are several identities in the namespace, the one marked as primary is used. If none is marked as primary, the first one is used.
* If the identity is missing, the call does not fail. The user is assigned to a variant at random for the current app session only, and can be assigned to a different variant after the app restarts. Set the identity before you evaluate flags that use it.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPEdgeIdentity

let identityMap = IdentityMap()
identityMap.add(
    item: IdentityItem(id: "1111", authenticatedState: .authenticated, primary: true),
    withNamespace: "userCRMId" // must match the namespace configured on the feature flag
)
Identity.updateIdentities(with: identityMap)
```

>[!TAB Objective-C]

```objc
@import AEPEdgeIdentity;

AEPIdentityItem *item = [[AEPIdentityItem alloc] initWithId:@"1111"
                                         authenticatedState:AEPAuthenticatedStateAuthenticated
                                                    primary:YES];
AEPIdentityMap *identityMap = [[AEPIdentityMap alloc] init];
[identityMap addItem:item withNamespace:@"userCRMId"]; // must match the namespace configured on the feature flag
[AEPMobileEdgeIdentity updateIdentities:identityMap];
```

>[!ENDTABS]


## API reference {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

Check whether a feature is enabled for the current user. The result is `true` when the feature exists, the user matches its targeting rules, and the user is not in a control group. Otherwise, the result is `false`.

>[!BEGINTABS]

>[!TAB Swift]

```swift
static func isFeatureEnabled(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (Bool) -> Void,
    errorCallback: ((AEPError) -> Void)?
)
```

>[!TAB Objective-C]

```objc
+ (void)isFeatureEnabled:(NSString *)featureKey
       evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
              completion:(void (^)(BOOL))completion
           errorCallback:(void (^ _Nullable)(enum AEPError))errorCallback;
```

>[!ENDTABS]

**Parameters**

| Parameter | Type | Description |
|---|---|---|
| `featureKey` | String | Feature key to evaluate in Flags |
| `evaluationContext` | FeatureEvaluationContext | Include targeting attributes as needed; use `FeatureEvaluationContext.builder().build()` for an empty context. See [Evaluation context](#evaluation-context). |
| `completion` | `(Bool) -> Void` | Called with `true` if the feature is enabled, `false` otherwise. |
| `errorCallback` | `((AEPError) -> Void)?` | Optional. Called only for genuine failures, such as an empty key, missing configuration, a failed evaluation, or a timeout. |

**Examples**

>[!BEGINTABS]

>[!TAB Swift]

```swift
Flag.isFeatureEnabled("new-flag", evaluationContext: context) { isEnabled in
    DispatchQueue.main.async {
        if isEnabled {
            // Run the feature-specific behavior
        } else {
            // Run the default behavior
        }
    }
} errorCallback: { _ in
    DispatchQueue.main.async {
        // Run the default behavior
    }
}
```

>[!TAB Objective-C]

```objc
[AEPMobileFlag isFeatureEnabled:@"new-flag"
              evaluationContext:context
                     completion:^(BOOL isEnabled) {
    dispatch_async(dispatch_get_main_queue(), ^{
        if (isEnabled) {
            // Run the feature-specific behavior
        } else {
            // Run the default behavior
        }
    });
} errorCallback:^(enum AEPError error) {
    dispatch_async(dispatch_get_main_queue(), ^{
        // Run the default behavior
    });
}];
```

>[!ENDTABS]

### getFeature {#get-feature}

>[!IMPORTANT]
>
>Earlier versions called the error callback with `AEPError.unexpected` when a feature was not served. If your app treated that error as "feature missing", handle `nil` in the completion instead.

Returns the details of a feature for the current user, including its metadata and the variant the user is assigned to. Use it when you need more than enabled or disabled.

The completion is called with a result only when the feature is served to the user. If the feature is not served, the completion is called with `nil`. This is a normal outcome, not an error, and the error callback is not called. The completion is called with `nil` when:

* No feature has this key.
* The user does not match the targeting rules.
* The user is in a control group.

The error callback is called with `AEPError.unexpected` (or another `AEPError`) only when something goes wrong: the feature key is empty, a required configuration value is missing, the evaluation fails, the response cannot be read, or the request times out.

>[!BEGINTABS]

>[!TAB Swift]

```swift
static func getFeature(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (FeatureEvaluationResult?) -> Void,
    errorCallback: ((AEPError) -> Void)?
)
```

>[!TAB Objective-C]

```objc
+ (void)getFeature:(NSString *)featureKey
 evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
        completion:(void (^)(AEPFeatureEvaluationResult * _Nullable))completion
     errorCallback:(void (^ _Nullable)(enum AEPError))errorCallback;
```

>[!ENDTABS]

**Parameters**

| Parameter | Type | Description |
|---|---|---|
| `featureKey` | String | Feature key to evaluate in Flags |
| `evaluationContext` | FeatureEvaluationContext | Include targeting attributes as needed; use `FeatureEvaluationContext.builder().build()` for an empty context. See [Evaluation context](#evaluation-context). |
| `completion` | `(FeatureEvaluationResult?) -> Void` | Called with the evaluated feature payload. Called with `nil` when the feature is not served to the user (unknown key, targeting not matched, or control group). `nil` is not an error. |
| `errorCallback` | `((AEPError) -> Void)?` | Optional. Called only for genuine failures, such as an empty key, missing configuration, a failed evaluation, or a timeout. Not called when the feature is not served. |

**Response**

*FeatureEvaluationResult*

| Field | Type | Description |
|---|---|---|
| `id` | Int | The feature ID |
| `key` | String | The feature key |
| `featureGroupKey` | String? | The key of the feature group that contains the feature |
| `meta` | String? | The metadata configured for the feature, as text. If your metadata is JSON, decode it in your app. |
| `analyticsParam` | AnalyticsParam? | Identifiers of the feature and the user's variant |

**Examples**

>[!BEGINTABS]

>[!TAB Swift]

```swift
Flag.getFeature("new-flag", evaluationContext: context) { feature in
    DispatchQueue.main.async {
        guard let meta = feature?.meta, !meta.isEmpty else {
            // The feature is not served to this user (feature is nil), or it has no metadata.
            // Run the default behavior
            return
        }
        // Use the metadata to drive the feature behavior
    }
} errorCallback: { _ in
    DispatchQueue.main.async {
        // A genuine failure occurred. Run the default behavior
    }
}
```

>[!TAB Objective-C]

```objc
[AEPMobileFlag getFeature:@"new-flag"
        evaluationContext:context
               completion:^(AEPFeatureEvaluationResult * _Nullable feature) {
    dispatch_async(dispatch_get_main_queue(), ^{
        if (feature.meta.length > 0) {
            // Use the metadata to drive the feature behavior
        } else {
            // Run the default behavior
        }
    });
} errorCallback:^(enum AEPError error) {
    dispatch_async(dispatch_get_main_queue(), ^{
        // Run the default behavior
    });
}];
```

>[!ENDTABS]

### extensionVersion {#extension-version}

Returns the version of the Flags extension.

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
| `isFeatureEnabled(_:evaluationContext:completion:errorCallback:)` | Bool through the completion |
| `getFeature(_:evaluationContext:completion:errorCallback:)` | FeatureEvaluationResult? through the completion |
| `extensionVersion` | String |
