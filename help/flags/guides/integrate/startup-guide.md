---
title: Startup guide
description: Follow these steps to get your application integrated with Flags, from requesting access to creating your first feature flag.
hide: true
exl-id: 7aa09535-45fa-4ddf-9e3f-a23f8a8ee666
---
# Startup guide {#startup-guide}

Follow these steps to integrate Flags into your application.

## Step 1: Request access {#step-1-access}

Request access to the Flags console and join your team. See [Request access](../console/request-access.md) for step-by-step instructions.

## Step 2: Onboard your application {#step-2-onboard}

After gaining access, log in to the Flags console and verify that your application is listed under your team. If it is not, ask your team admin to add it. See [Onboard your application](../applications/onboard-your-application.md).

Before onboarding, prepare the following:

| Requirement | Details |
|---|---|
| **Application ID** | A unique client identifier used when calling the Flags APIs. Use your application's existing client ID where available. |

## Step 3: Get your Environment File ID {#step-3-credentials}

The Environment File ID you need depends on your integration path:

* **Web and mobile (tag-based):** Use the **environment file ID** from your published tag property. See Step 4a for how to get this.

## Step 4: Integrate using an SDK {#step-4-integrate}

Follow the integration guide for your application type. Choose the path that fits your stack:

* **Web and mobile apps** — see [Android](../sdk-releases/android/android-extension-integration-guide.md), [iOS](../sdk-releases/ios/ios-extension-integration-guide.md), and [Web](../sdk-releases/web/web-extension-integration-guide.md) guides in the integration guide section

## Step 4a: Set up Data Collection and publish your configuration {#step-4a-data-collection}

If you are integrating via a tag-based approach (web or mobile), configure your tag property before initializing the SDK:

1. In [Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection), open your mobile or web property.
1. Install the **Edge Network** extension, then the **Experience Rollout** extension (in that order).
1. Select your **data stream** (must include the Customer Journey Analytics dataset) and your edge domain.
1. Publish the configuration through **Dev → Staging → Production**.
1. Copy the **environment file ID** from the **Environments** tab — you will use this to initialize the SDK.

>[!IMPORTANT]
>
>In the **staging** environment, prefix the environment file ID with `staging/` — that is, use `staging/<environmentId>`. In **production**, use the environment file ID directly.

## Step 5: Create and test your first feature flag {#step-5-feature-flag}

Once integration is complete, create your first feature flag in the console and test it:

* [Create your first feature flag](../feature-flags/create-your-first-feature-flag.md)

## See also {#see-also}

* [Integrate Flags in your app](integrating-in-your-app.md)
* [SDKs](sdks.md)

<!-- -->
