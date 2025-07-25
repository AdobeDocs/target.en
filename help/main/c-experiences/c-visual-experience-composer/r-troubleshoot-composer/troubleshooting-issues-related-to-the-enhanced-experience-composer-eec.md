---
keywords: Targeting;eec;visual experience composer;troubleshoot enhanced experience composer;troubleshooting
description: Learn how to troubleshoot problems that sometimes occur in the [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEC) under certain conditions.
title: How Do I Troubleshoot Issues Related to the [!UICONTROL Enhanced Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
---
# Troubleshooting issues related to the [!UICONTROL Enhanced Experience Composer] 

Display problems sometimes occur in the [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEC) under certain conditions.

## The EEC won't load an internal QA URL that is not accessible on public IP. {#section_D29E96911D5C401889B5EACE267F13CF}


+++Details
This issue can be resolved by allowlisting the following IP addresses. These IP addresses are for the [!DNL Adobe] server used for the EEC proxy. These IP addresses are only required for activity editing. Visitors to your site do not need these IP addresses allowlisted.

Ask your IT team to allowlist the following IP addresses:

### US (va7)

40.70.154.136/29
52.254.106.240/28
52.254.106.160/28
52.254.107.16/28
20.186.185.181
20.22.83.112
20.186.185.227
52.254.106.192/28
52.254.106.0/28
52.254.107.128/28
52.254.107.80/28
52.254.106.176/28
52.254.107.32/28
52.254.105.192/28
52.254.107.64/28
52.254.106.208/28
52.254.107.0/28
52.254.106.224/28
20.14.241.153
20.186.185.239
4.152.211.251
52.254.107.144/28
52.254.106.144/28

### EMEA (nld2)

51.138.17.16/28
51.138.17.48/28
51.138.16.128/28
51.138.17.32/28
51.138.16.240/28
51.138.17.112/28
51.138.16.160/28
51.138.16.208/28
51.138.17.80/28
51.138.17.0/28
51.138.17.96/28
51.138.16.144/28
20.31.145.248
20.126.189.248
51.138.16.224/28
51.138.16.192/28
51.138.12.94
51.138.12.11
51.138.16.176/28
51.138.12.100
51.138.17.64/28
51.138.12.160/28

### APAC (aus)

20.43.104.160/28
20.227.35.177
20.40.188.227
20.43.104.112/28
20.43.104.128/28
20.43.104.144/28
20.40.188.166
20.53.206.128
20.43.104.80/28
20.43.104.16/28
20.43.105.48/28
20.43.104.96/28
20.43.104.48/28
20.40.188.194
20.43.104.32/28
20.40.191.224/28
20.43.105.16/28
20.40.191.96/28
20.43.104.176/28
20.40.191.240/28
20.43.104.64/28
20.43.105.32/28
20.43.104.192/28
20.43.105.0/28
20.43.104.0/28

### Legacy IP addresses

The following legacy IP addresses should continue to be allowlisted until further notice.

34.254.77.200
54.73.207.147
54.229.152.123
3.224.194.242
54.90.51.39
34.228.136.112
54.150.116.11
18.178.142.8
54.199.107.77
99.80.139.221
54.78.56.224
54.247.179.246
54.80.219.243
34.201.235.54
54.196.224.236
35.75.212.45
52.199.184.130
18.180.161.176

You might see the following error message in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![EEC_error image](assets/EEC_error.png)

The following are reasons that you might see this error message and remedies to fix the situation:

* **Issue:** Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer].

  **Remedy:** Allowlist the IP addresses listed above. 

* **Issue:** The IP addresses are allowlisted but your website does not support TLS version 1.2. [!DNL Target] currently uses the default configuration of 1.2. Prior to the [!DNL Target] 18.4.1 (April 25, 2018), the default configuration supported TLS 1.0. For more information, see [TLS (Transport Layer Security) Encryption Changes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

  **Solution:** See the following question (The [!UICONTROL Enhanced Visual Experience Composer] won't load on secure pages on my site that use TLS 1.2).

+++

## The EEC won't load on secure pages on my site that use TLS 1.0. (EEC only) {#section_C5B31E3D32A844F68E5A8153BD17551F}

+++Details
You might see the error message described above in "The [!UICONTROL Enhanced Visual Experience Composer] won't load on secure pages on my site." if the above IP addresses are allowlisted but your website does not support TLS version 1.2. [!DNL Target] currently uses the default configuration of 1.2. Prior to the [!DNL Target] 18.4.1 (April 25, 2018), the default configuration supported TLS 1.0. For more information, see [TLS (Transport Layer Security) Encryption Changes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

To check the TLS version on your website using Firefox (other browsers have similar steps):

1. Open the affected website in Firefox. 
1. Click the **[!UICONTROL Show Site Information]** icon on the browser's address bar.

   ![firefox_more_info image](assets/firefox_more_info.png)

1. Click **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![firefox_more_info_2 image](assets/firefox_more_info_2.png)

1. Examine the TLS version information under Technical Details:

   ![firefox_more_info_3 image](assets/firefox_more_info_3.png)

1. If you find that your website is showing TLS 1.0, see [TLS (Transport Layer Security) Encryption Changes](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank} for information about Target's TLS support policy. To remedy the situation for now (valid until September 12, 2018){target=_blank}, reach out to [Customer Care](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) for configuration with your TLS version and the domain.

+++

## I'm seeing timeouts or "access denied" errors when loading sites with proxy enabled. (EEC only) {#section_60CBB9022DC449F593606C0E6252302D}

+++Details
Make sure proxy IPs are not blocked in your environment.

+++
