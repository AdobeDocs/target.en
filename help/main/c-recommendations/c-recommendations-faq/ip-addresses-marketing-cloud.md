---
keywords: IP address;IP addresses;whitelist;allowlist;firewall;recs;feed;servers;adobe marketing cloud;recommendations
description: View a list of IP addresses used in [!DNL Target] Recommendations feed-processing servers to help you configure your firewall to allow IP addresses originating from Adobe servers.
title: What IP Addresses Do Recommendations Feed-Processing Servers Use?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
---
# IP addresses used by [!DNL Recommendations] feed-processing servers

List of IP addresses used in [!DNL Adobe Target] [!DNL Recommendations] feed-processing servers to help you configure your firewall to allow IP addresses originating from [!DNL Adobe] servers.

>[!IMPORTANT]
>
>The [!DNL Target] team is currently updating the NAT gateway addresses for downloading [!DNL Recommendations] feeds. If you implement IP allowlisting, ensure that you allowlist the following new AWS hosts. The existing hosts are scheduled to be decommissioned on June 30, 2024. To ensure a smooth transition, allowlist all nine addresses. There is no urgency to remove the existing addresses.

[!DNL Target] [!UICONTROL Recommendations] activities use the following AWS hosts when accessing customers' FTP servers:

**New hosts**:

| Location | Host |
| --- | --- |
| Oregon | `52.40.124.129` |
| Oregon | `54.148.219.69` |
| Oregon | `54.189.208.212` |
| Oregon | `44.230.236.35` |
| Oregon | `54.190.78.243` |
| Oregon | `52.41.73.133` |

**Existing hosts**:

| Location | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations] APIs also use the same AWS hosts.
