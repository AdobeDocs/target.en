---
title: Flags extension for Android integration guide
description: Learn how to integrate the Flags extension with the Adobe Experience Platform Mobile SDK on Android.
badge: label="Beta" type="Informative"
hide: true
exl-id: 683ef4d4-e637-4b7b-b694-689c7e65a99e
---
# Flags extension for Android {#android-extension-integration-guide}

This guide describes how to integrate the Flags extension with the Adobe Experience Platform Mobile SDK on Android.

## Prerequisites {#prerequisites}

Before implementing the Flags extension, ensure you have:

* A mobile property configured in [Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection)
* The Flags extension installed and configured in your mobile property
* An Adobe Experience Cloud Organization ID
* Minimum SDK: API 21 (Android 5.0 Lollipop)

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

#### Using Gradle with BOM (Recommended) {#gradle-bom}

Add the following dependencies to your app's `build.gradle.kts` file:

```kotlin
dependencies {
    // Adobe Experience Platform Mobile SDK BOM
    implementation(platform("com.adobe.marketing.mobile:sdkbom:3.+"))

    // Required extensions
    implementation("com.adobe.marketing.mobile:core")
    implementation("com.adobe.marketing.mobile:lifecycle")
    implementation("com.adobe.marketing.mobile:edge")
    implementation("com.adobe.marketing.mobile:edgeidentity")
}
```

#### Using Gradle (Groovy) {#gradle-groovy}

```groovy
dependencies {
    // Adobe Experience Platform Mobile SDK BOM
    implementation platform('com.adobe.marketing.mobile:sdkbom:3.+')

    // Required extensions
    implementation 'com.adobe.marketing.mobile:core'
    implementation 'com.adobe.marketing.mobile:lifecycle'
    implementation 'com.adobe.marketing.mobile:edge'
    implementation 'com.adobe.marketing.mobile:edgeidentity'
}
```

>[!IMPORTANT]
>
>For production applications, Adobe recommends using explicit version numbers instead of dynamic versions. See [Managing Gradle dependencies](https://docs.gradle.org/current/userguide/dependency_management.html) for more information.

### Add the Flags dependency {#add-flags-dependency}

#### Using the hosted Maven repository (Recommended) {#hosted-maven}

Add the Flags Maven repository to the `repositories` block in `settings.gradle.kts`:

```kotlin
maven {
    url = uri("<HTTPS Flags Maven repository URL>")
}
```

For a Groovy `settings.gradle` file:

```groovy
maven {
    url = uri('<HTTPS Flags Maven repository URL>')
}
```

Replace `<HTTPS Flags Maven repository URL>` with the secure repository URL provided for the Flags extension.

Then add the versioned Flags dependency to your app's `build.gradle.kts`:

```kotlin
implementation("com.adobe.marketing.mobile:flags:<version>")
```

For a Groovy `build.gradle` file:

```groovy
implementation 'com.adobe.marketing.mobile:flags:<version>'
```

Replace `<version>` with the exact Flags extension version provided for your release.

#### Using the Flags distribution package {#distribution-package}

The Flags extension distribution package includes:

* `flags-3.x.aar`
* `flags-3.x.module`
* `flags-3.x.pom`

Make the extension available to your Android project using one of the following methods:

* Publish all files from the distribution package to a local or private Maven repository, and configure your project to use that repository.
* Add `flags-3.x.aar` directly to your project and declare the transitive dependencies specified in `flags-3.x.pom`.

### Add permissions {#add-permissions}

Add the following permissions to your `AndroidManifest.xml` file:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

### Initialize the SDK {#initialize-sdk}

Initialize the Mobile SDK in your `Application` class before calling any Flags extension APIs. Use the Environment File ID from your mobile property with `MobileCore.initialize` so the app picks up the Flags settings you published in Data Collection.

#### Using MobileCore.initialize {#mobile-core-initialize}

Available starting from Android BOM version 3.8.0, this API initializes the SDK with your Data Collection environment file.

>[!IMPORTANT]
>
>For production apps, use `LoggingMode.ERROR` only; do not use `DEBUG` or `VERBOSE` in release builds.

**Kotlin**

```kotlin
import android.app.Application
import com.adobe.marketing.mobile.LoggingMode
import com.adobe.marketing.mobile.MobileCore

class MainApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        // Production: use LoggingMode.ERROR only. Do not use DEBUG or VERBOSE in release builds.
        MobileCore.setLogLevel(LoggingMode.ERROR)

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID")
    }
}
```

**Java**

```java
import android.app.Application;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;

public class MainApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();

        // Production: use LoggingMode.ERROR only. Do not use DEBUG or VERBOSE in release builds.
        MobileCore.setLogLevel(LoggingMode.ERROR);

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID", null);
    }
}
```

### Register the Application class {#register-application}

Register your `Application` class in `AndroidManifest.xml`:

```xml
<application
    android:name=".MainApplication"
    ... >
</application>
```

## Evaluation context {#evaluation-context}

`FeatureEvaluationContext` class includes targeting attributes (used for flag rule matching).

| Method | Required | Description |
|---|---|---|
| `withAttributes(map)` | No | `Map<String, List<String>>`. Key is the context attribute name used by your flag rules (for example `locale`, `platform`, `appVersion`, `deviceType`). Value is the list of candidate attribute values for that key for the current user/session (for example `["en_US"]` or `["phone"]`). |

**Kotlin**

```kotlin
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext

val attrs = mapOf(
    "locale" to listOf("en_US"),
    "platform" to listOf("ANDROID")
)

val ctx = FeatureEvaluationContext.builder()
    .withAttributes(attrs)
    .build()
```

**Java**

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

### Custom identity {#custom-identity}

The Flags extension uses the Identity for Edge Network extension for identity resolution. A feature flag can be cohorted on a custom identity (for example, a CRM ID or a loyalty ID) so that variant splits and analytics are tied to the identity that matters to your application.

The custom identity namespace must be selected in the Flags UI when the feature flag is authored. To evaluate a flag against that identity, the same identity must be present in the Edge Identity `identityMap` on the device, using the matching namespace. Provide it at runtime with the Identity for Edge Network `updateIdentities` API.

#### Add the custom identity to the Identity Map {#add-identity}

Add the identity under the same namespace configured on the feature flag.

**Kotlin**

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

**Java**

```java
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState;
import com.adobe.marketing.mobile.edge.identity.Identity;
import com.adobe.marketing.mobile.edge.identity.IdentityItem;
import com.adobe.marketing.mobile.edge.identity.IdentityMap;

final IdentityItem item = new IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true);
final IdentityMap identityMap = new IdentityMap();
identityMap.addItem(item, "userCRMId"); // must match the namespace configured on the feature flag
Identity.updateIdentities(identityMap);
```

## API reference {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled` returns whether a Flags feature is on or off for the given context. Pass `featureKey`, a `FeatureEvaluationContext` (optional targeting attributes), and a callback. See [Evaluation context](#evaluation-context).

**Signature**

*Kotlin*

```kotlin
Flag.isFeatureEnabled(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<Boolean>
)
```

*Java*

```java
Flag.isFeatureEnabled(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<Boolean> callback);
```

**Parameters**

| Parameter | Type | Description |
|---|---|---|
| `featureKey` | String | Feature key to evaluate in Flags |
| `evaluationContext` | FeatureEvaluationContext | Include targeting attributes as needed; use `FeatureEvaluationContext.builder().build()` for an empty context. See [Evaluation context](#evaluation-context). |
| `callback` | AdobeCallback&lt;Boolean&gt; | Invoked with `true` if the feature is enabled, `false` otherwise. You can also pass `AdobeCallbackWithError<Boolean>` to handle `fail(...)`. |

**Examples**

*Kotlin*

```kotlin
import com.adobe.marketing.mobile.AdobeCallback
import com.adobe.marketing.mobile.flags.Flag

Flag.isFeatureEnabled(
    "new-flag",
    ctx,
    object : AdobeCallback<Boolean> {
        override fun call(isEnabled: Boolean?) {
            if (isEnabled == true) {
                // run the feature-specific behavior
            } else {
                // fall back to the default behavior
            }
        }
    }
)
```

*Java*

```java
import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.flags.Flag;

Flag.isFeatureEnabled(
    "new-flag",
    ctx,
    new AdobeCallback<Boolean>() {
        @Override
        public void call(Boolean isEnabled) {
            if (Boolean.TRUE.equals(isEnabled)) {
                // run the feature-specific behavior
            } else {
                // fall back to the default behavior
            }
        }
    }
);
```

### getFeature {#get-feature}

`getFeature` returns the evaluated feature payload for the provided context. Use this API when you need more than enabled/disabled and want feature metadata or values.

**Signature**

*Kotlin*

```kotlin
Flag.getFeature(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<FeatureEvaluationResult>
)
```

*Java*

```java
Flag.getFeature(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<FeatureEvaluationResult> callback);
```

**Parameters**

| Parameter | Type | Description |
|---|---|---|
| `featureKey` | String | Feature key to evaluate in Flags |
| `evaluationContext` | FeatureEvaluationContext | Include targeting attributes as needed; use `FeatureEvaluationContext.builder().build()` for an empty context. See [Evaluation context](#evaluation-context). |
| `callback` | AdobeCallback&lt;FeatureEvaluationResult&gt; | Invoked with the evaluated feature payload; may be `null` when the feature is not found. You can also pass `AdobeCallbackWithError<FeatureEvaluationResult>` to handle `fail(...)`. |

**Response**

*FeatureEvaluationResult*

| Field | Type | Description |
|---|---|---|
| `id` | Int | Numeric feature identifier |
| `key` | String | Feature key |
| `featureGroupKey` | String? | Feature group key when available |
| `meta` | String? | Feature metadata as a JSON string when available |
| `analyticsParam` | AnalyticsParam? | Analytics details for the evaluated feature |

*AnalyticsParam*

| Field | Type | Description |
|---|---|---|
| `featureGroupId` | Int | Numeric feature group identifier |
| `featureId` | Int | Numeric feature identifier |
| `variantId` | String? | Variant identifier |

**Examples**

*Kotlin*

```kotlin
import com.adobe.marketing.mobile.AdobeCallback
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult
import com.adobe.marketing.mobile.flags.Flag

Flag.getFeature(
    "new-flag",
    ctx,
    object : AdobeCallback<FeatureEvaluationResult> {
        override fun call(feature: FeatureEvaluationResult?) {
            val meta = feature?.meta
            if (!meta.isNullOrEmpty()) {
                // Feature metadata is available: use it to drive the feature behavior
            } else {
                // No metadata available: fall back to the default behavior
            }
        }
    }
)
```

*Java*

```java
import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult;
import com.adobe.marketing.mobile.flags.Flag;

Flag.getFeature(
    "new-flag",
    ctx,
    new AdobeCallback<FeatureEvaluationResult>() {
        @Override
        public void call(FeatureEvaluationResult feature) {
            String meta = feature != null ? feature.getMeta() : null;
            if (meta != null && !meta.isEmpty()) {
                // Feature metadata is available: use it to drive the feature behavior
            } else {
                // No metadata available: fall back to the default behavior
            }
        }
    }
);
```

### extensionVersion {#extension-version}

Returns the version string of the Flags extension.

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
| `isFeatureEnabled(featureKey, evaluationContext, callback)`. `FeatureEvaluationContext` carries targeting attributes for rules. See [Feature evaluation](#is-feature-enabled). | Boolean via callback |
| `getFeature(featureKey, evaluationContext, callback)`. Returns the evaluated feature payload for the given context. See [getFeature](#get-feature). | FeatureEvaluationResult via callback |
| `extensionVersion()` | String |

## See also {#see-also}

* [Mobile applications](../../integrate/mobile-applications.md)
* [SDKs](../../integrate/sdks.md)

<!-- -->
