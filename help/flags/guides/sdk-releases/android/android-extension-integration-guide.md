---
title: Flags extension for Android integration guide
description: Learn how to integrate the Flags extension with the Adobe Experience Platform Mobile SDK on Android.
badge: label="Beta" type="Informative"
hide: true
exl-id: 683ef4d4-e637-4b7b-b694-689c7e65a99e
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
---
# Flags extension for Android {#android-extension-integration-guide}

This guide describes how to integrate the Flags extension with the Adobe Experience Platform Mobile SDK on Android.

## Prerequisites {#prerequisites}

Before implementing the Flags extension, ensure you have:

* A mobile property configured in [Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection)
* The Adobe Flags extension installed and configured in your mobile property
* An Adobe Experience Cloud Organization ID
* An Edge Network datastream configured in your mobile property, to receive exposure analytics
* Android API 21 (Android 5.0 Lollipop) or later
* Mobile Core 3.6.0 or later (included in `sdk-bom` 3.17.0 and later)

## Extension dependencies {#extension-dependencies}

The Flags extension requires the following Adobe Experience Platform extensions:

| Extension | Description | Required |
|---|---|---|
| [Mobile Core](https://developer.adobe.com/client-sdks/home/base/mobile-core/) | Provides configuration, event processing, and SDK initialization | Yes |
| [Lifecycle](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/) | Reports when the app moves to the foreground or background | Yes |
| [Edge Network](https://developer.adobe.com/client-sdks/edge/edge-network/) | Sends exposure analytics to Adobe Experience Platform | Yes |
| [Identity for Edge Network](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) | Provides the identities used to assign users to variants | Yes |

Ensure these extensions are installed in your Data Collection mobile property and included in your app dependencies.

## Configure Flags extension in Data Collection {#configure}

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

## Add Flags extension to your app {#add-to-app}

### Add dependencies {#add-dependencies}

>[!IMPORTANT]
>
>The Flags extension is not part of the Mobile SDK BOM. Replace `<latest-version>` with the latest version from Maven Central. Without a version, Gradle cannot resolve the dependency.
>
></br>
>For production applications, Adobe recommends using explicit version numbers instead of dynamic versions such as `3.+`. See [Managing Gradle dependencies](https://docs.gradle.org/current/userguide/dependency_management.html) for more information.

Add the following dependencies to your app's `build.gradle.kts` (Kotlin) or `build.gradle` (Groovy) file:

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
dependencies {
    // Adobe Experience Platform Mobile SDK BOM (3.17.0 or later)
    implementation(platform("com.adobe.marketing.mobile:sdk-bom:3.+"))

    // Required extensions (versions managed by the BOM)
    implementation("com.adobe.marketing.mobile:core")
    implementation("com.adobe.marketing.mobile:lifecycle")
    implementation("com.adobe.marketing.mobile:edge")
    implementation("com.adobe.marketing.mobile:edgeidentity")

    // Flags extension (not managed by the BOM; specify the version)
    implementation("com.adobe.marketing.mobile:flags:<latest-version>")
}
```

>[!TAB Groovy]

```groovy
dependencies {
    // Adobe Experience Platform Mobile SDK BOM (3.17.0 or later)
    implementation platform('com.adobe.marketing.mobile:sdk-bom:3.+')

    // Required extensions (versions managed by the BOM)
    implementation 'com.adobe.marketing.mobile:core'
    implementation 'com.adobe.marketing.mobile:lifecycle'
    implementation 'com.adobe.marketing.mobile:edge'
    implementation 'com.adobe.marketing.mobile:edgeidentity'

    // Flags extension (not managed by the BOM; specify the version)
    implementation 'com.adobe.marketing.mobile:flags:<latest-version>'
}
```

>[!ENDTABS]

### Initialize the SDK {#initialize-sdk}

>[!IMPORTANT]
>
>For production apps, use `LoggingMode.ERROR` only. Do not use `DEBUG` or `VERBOSE` in release builds.

Initialize the Mobile SDK in your `Application` class before calling any Flags extension APIs. Use the Environment File ID from your mobile property so the app picks up the Flags settings you published in Data Collection.

`MobileCore.initialize` registers every Adobe extension included in your Gradle dependencies, including the Flags extension.

Note that when you use `MobileCore.initialize`, do not also call `MobileCore.registerExtensions`, `MobileCore.lifecycleStart`, or `MobileCore.lifecyclePause`. These are handled for you.

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import android.app.Application
import com.adobe.marketing.mobile.LoggingMode
import com.adobe.marketing.mobile.MobileCore

class MainApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        MobileCore.setLogLevel(LoggingMode.ERROR)

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID")
    }
}
```

>[!TAB Java]

```java
import android.app.Application;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;

public class MainApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();

        MobileCore.setLogLevel(LoggingMode.ERROR);

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID");
    }
}
```

>[!ENDTABS]

### Register the Application class {#register-application}

Register your `Application` class in `AndroidManifest.xml`:

```xml
<application
    android:name=".MainApplication"
    ... >
</application>
```

### If you register extensions manually {#register-manually}

If your app cannot use `MobileCore.initialize` and registers extensions with `MobileCore.registerExtensions`, add `Flag.EXTENSION` to the list. Use the Identity for Edge Network class, `com.adobe.marketing.mobile.edge.identity.Identity`, not the legacy `com.adobe.marketing.mobile.Identity`.

```kotlin
import com.adobe.marketing.mobile.Edge
import com.adobe.marketing.mobile.Lifecycle
import com.adobe.marketing.mobile.MobileCore
import com.adobe.marketing.mobile.edge.identity.Identity
import com.adobe.marketing.mobile.flags.Flag

MobileCore.setApplication(this)
MobileCore.configureWithAppID("YOUR_ENVIRONMENT_FILE_ID")
MobileCore.registerExtensions(
    listOf(Lifecycle.EXTENSION, Identity.EXTENSION, Edge.EXTENSION, Flag.EXTENSION)
) { }
```

In this setup, lifecycle is not tracked automatically. Call `MobileCore.lifecycleStart(null)` in every Activity's `onResume` and `MobileCore.lifecyclePause()` in its `onPause`. Without these calls, the extension keeps refreshing flags while the app is in the background, and exposure analytics are sent later.

## Evaluation context {#evaluation-context}

`FeatureEvaluationContext` holds the targeting attributes that your flag rules use. You do not pass an identity: the extension reads it from Identity for Edge Network on every evaluation. See [Custom identity](#custom-identity).

| Method | Required | Description |
|---|---|---|
| `withAttributes(map)` | No | `Map<String, List<String>>`. Each key is an attribute name used by your flag rules (for example, `locale` or `appVersion`). Each value is the list of values for the current user (for example, `["en_US"]`). |

* A context is required for every evaluation. If you have no attributes, pass `FeatureEvaluationContext.builder().build()`.
* Call `withAttributes` at most once per builder.
* A built context cannot be changed, so you can reuse it across evaluations.

### Usage {#evaluation-context-usage}

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext

val ctx = FeatureEvaluationContext.builder()
    .withAttributes(
        mapOf(
            "locale" to listOf("en_US"),
            "platform" to listOf("ANDROID")
        )
    )
    .build()
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext;
import java.util.Arrays;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

Map<String, List<String>> attrs = new HashMap<>();
attrs.put("locale", Arrays.asList("en_US"));
attrs.put("platform", Arrays.asList("ANDROID"));

FeatureEvaluationContext ctx = FeatureEvaluationContext.builder()
        .withAttributes(attrs)
        .build();
```

>[!ENDTABS]

### Sample targeting attributes {#sample-attributes}

| Attribute | Description | Example values |
|---|---|---|
| `locale` | User's locale | `["en_US"]`, `["fr_FR"]` |
| `platform` | Platform | `["ANDROID"]` |
| `appVersion` | App version | `["3.0.0"]` |
| `deviceType` | Device type | `["phone"]`, `["tablet"]` |

Attribute names and values must match the ones used in your flag rules.

## Custom identity {#custom-identity}

The Flags extension uses the Identity for [Edge Network extension](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) for identity resolution. A feature flag can be cohorted on a custom identity, for example, a CRM ID or a loyalty ID, so that variant splits and analytics are tied to the identity that matters to your application.

The custom identity namespace must be selected in the Flags UI when the feature flag is authored. To evaluate a flag against that identity, the same identity must be present in the Edge Identity `identityMap` on the device, using the matching namespace. Provide it at runtime with the Identity for Edge Network `updateIdentities` API.

### Add the custom identity to the identity map {#add-identity}

Add the identity under the same namespace configured on the feature flag, before you evaluate the flag.

Note the following when you add the identity:

* The namespace must match exactly, including case.
* If the namespace has more than one identity, the one marked as primary is used. Otherwise, the first one is used.
* If the identity is missing when the flag is evaluated, the user is assigned by a temporary ID that changes every time the app starts. The user's variant can then change between app launches. Always set the identity before you evaluate flags that use it.

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState
import com.adobe.marketing.mobile.edge.identity.Identity
import com.adobe.marketing.mobile.edge.identity.IdentityItem
import com.adobe.marketing.mobile.edge.identity.IdentityMap

val identityMap = IdentityMap()
identityMap.addItem(
    IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true),
    "userCRMId" // must match the namespace configured on the feature flag
)
Identity.updateIdentities(identityMap)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState;
import com.adobe.marketing.mobile.edge.identity.Identity;
import com.adobe.marketing.mobile.edge.identity.IdentityItem;
import com.adobe.marketing.mobile.edge.identity.IdentityMap;

IdentityMap identityMap = new IdentityMap();
identityMap.addItem(
        new IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true),
        "userCRMId"); // must match the namespace configured on the feature flag
Identity.updateIdentities(identityMap);
```

>[!ENDTABS]

## API reference {#api-reference}

### Callbacks and error handling {#callbacks-errors}

These rules apply to `isFeatureEnabled` and `getFeature`:

* Always provide a default experience. Pass an `AdobeCallbackWithError` and show your default experience in `fail`. With a plain `AdobeCallback`, nothing is called when an error occurs.

* The extension preloads flag definitions when the app starts. After that, flags are evaluated on the device.

* Other errors: `fail` is called with `AdobeError.UNEXPECTED_ERROR` when:

  * the feature key is empty,
  * the Flags settings or the Experience Cloud Organization ID are missing from the published configuration, or
  * flag definitions could not be downloaded when the app started (for example, the device was offline). The extension tries again on the next configuration update, usually the next app launch.

### isFeatureEnabled {#is-feature-enabled}

Returns whether a feature is enabled for the current user.

**Signature**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
Flag.isFeatureEnabled(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<Boolean>
)
```

>[!TAB Java]

```java
Flag.isFeatureEnabled(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<Boolean> callback);
```

>[!ENDTABS]

**Parameters**

| Parameter | Type | Description |
|---|---|---|
| `featureKey` | String | Key of the feature to evaluate |
| `evaluationContext` | FeatureEvaluationContext | Targeting attributes. Use `FeatureEvaluationContext.builder().build()` if you have none. See [Evaluation context](#evaluation-context). |
| `callback` | AdobeCallback&lt;Boolean&gt; | Called with `true` if the feature is enabled for the user. Called with `false` if the feature is not found, the targeting rules do not match, or the user is in the control group. Pass an `AdobeCallbackWithError<Boolean>` to also receive errors. |

**Examples**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.AdobeCallbackWithError
import com.adobe.marketing.mobile.AdobeError
import com.adobe.marketing.mobile.flags.Flag

Flag.isFeatureEnabled(
    "new-checkout",
    ctx,
    object : AdobeCallbackWithError<Boolean> {
        override fun call(isEnabled: Boolean?) {
            runOnUiThread {
                if (isEnabled == true) showNewCheckout() else showDefaultCheckout()
            }
        }

        override fun fail(error: AdobeError?) {
            runOnUiThread { showDefaultCheckout() }
        }
    }
)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.AdobeCallbackWithError;
import com.adobe.marketing.mobile.AdobeError;
import com.adobe.marketing.mobile.flags.Flag;

Flag.isFeatureEnabled(
    "new-checkout",
    ctx,
    new AdobeCallbackWithError<Boolean>() {
        @Override
        public void call(Boolean isEnabled) {
            runOnUiThread(() -> {
                if (Boolean.TRUE.equals(isEnabled)) {
                    showNewCheckout();
                } else {
                    showDefaultCheckout();
                }
            });
        }

        @Override
        public void fail(AdobeError error) {
            runOnUiThread(() -> showDefaultCheckout());
        }
    }
);
```

>[!ENDTABS]

### getFeature {#get-feature}

Returns the evaluated feature for the current user, including its metadata. Use this API when you need more than enabled or disabled.

**Signature**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
Flag.getFeature(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<FeatureEvaluationResult>
)
```

>[!TAB Java]

```java
Flag.getFeature(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<FeatureEvaluationResult> callback);
```

>[!ENDTABS]

**Parameters**

| Parameter | Type | Description |
|---|---|---|
| `featureKey` | String | Key of the feature to evaluate |
| `evaluationContext` | FeatureEvaluationContext | Targeting attributes. Use `FeatureEvaluationContext.builder().build()` if you have none. See [Evaluation context](#evaluation-context). |
| `callback` | AdobeCallback&lt;FeatureEvaluationResult&gt; | Called with the evaluated feature, or with `null` when the feature is not served to the user: the key is unknown, the targeting criteria are not met, or the user is in a control cohort. `null` is a normal outcome, not an error. Control cohort exposures are still reported to analytics. Pass an `AdobeCallbackWithError<FeatureEvaluationResult>` to receive `fail(...)` for genuine failures such as timeouts. |

Treat a `null` result as "feature off" and show your default experience. Also show the default experience when `fail` is called, which only happens on genuine failures such as timeouts.

**Response**

*FeatureEvaluationResult*

| Field | Type | Description |
|---|---|---|
| `id` | Int | Feature ID |
| `key` | String | Feature key |
| `featureGroupKey` | String? | Feature group key, if the feature belongs to a group |
| `meta` | String? | Metadata configured for the feature, as plain text, or `null` if none is set. If you stored JSON, parse the string in your app. |
| `analyticsParam` | AnalyticsParam? | Analytics details for the evaluation |

*AnalyticsParam*

| Field | Type | Description |
|---|---|---|
| `featureGroupId` | Int | Feature group ID |
| `featureId` | Int | Feature ID |
| `variantId` | String? | ID of the variant the user was assigned to |

**Examples**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.AdobeCallbackWithError
import com.adobe.marketing.mobile.AdobeError
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult
import com.adobe.marketing.mobile.flags.Flag

Flag.getFeature(
    "new-checkout",
    ctx,
    object : AdobeCallbackWithError<FeatureEvaluationResult> {
        override fun call(feature: FeatureEvaluationResult?) {
            val meta = feature?.meta
            runOnUiThread {
                if (!meta.isNullOrEmpty()) applyExperience(meta) else showDefaultExperience()
            }
        }

        override fun fail(error: AdobeError?) {
            runOnUiThread { showDefaultExperience() }
        }
    }
)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.AdobeCallbackWithError;
import com.adobe.marketing.mobile.AdobeError;
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult;
import com.adobe.marketing.mobile.flags.Flag;

Flag.getFeature(
    "new-checkout",
    ctx,
    new AdobeCallbackWithError<FeatureEvaluationResult>() {
        @Override
        public void call(FeatureEvaluationResult feature) {
            final String meta = feature != null ? feature.getMeta() : null;
            runOnUiThread(() -> {
                if (meta != null && !meta.isEmpty()) {
                    applyExperience(meta);
                } else {
                    showDefaultExperience();
                }
            });
        }

        @Override
        public void fail(AdobeError error) {
            runOnUiThread(() -> showDefaultExperience());
        }
    }
);
```

>[!ENDTABS]

### extensionVersion {#extension-version}

Returns the version of the Flags extension.

**Syntax**

```kotlin
Flag.extensionVersion(): String
```

**Example**

*Kotlin*

```kotlin
val version = Flag.extensionVersion()
```

*Java*

```java
String version = Flag.extensionVersion();
```

## API summary {#api-summary}

| API | Returns |
|---|---|
| `isFeatureEnabled(featureKey, evaluationContext, callback)`. See [isFeatureEnabled](#is-feature-enabled). | Boolean via callback |
| `getFeature(featureKey, evaluationContext, callback)`. See [getFeature](#get-feature). | FeatureEvaluationResult via callback |
| `extensionVersion()` | String |

## Debugging {#debugging}

To debug, set `MobileCore.setLogLevel(LoggingMode.DEBUG)` in a debug build and filter Logcat by `Flags`. You should see a `Discovered extension` message from MobileCore for `com.adobe.marketing.mobile.flags.FlagExtension`.


