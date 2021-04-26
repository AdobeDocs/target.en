---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Work with Adobe Client Care to implement CNAME (Canonical Name) support in Adobe [!DNL Target] to handle ad-blocking issues or ITP-related cookie policies.
title: How Do I Use CNAME in Target?
feature: Privacy & Security
role: Developer
exl-id: bf533771-6d46-48ba-964c-3ad9ce9f7352
---
# CNAME and Adobe Target

Instructions for working with [!DNL Adobe] Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Use CNAME to handle ad blocking issues or ITP-related (Intelligent Tracking Prevention) cookie policies. With CNAME, calls are made to a domain owned by the customer rather than a domain owned by [!DNL Adobe].

## Request CNAME support in Target

1. Determine the list of hostnames you need for your SSL certificate (see FAQ below).

1. For each hostname, create a CNAME record in your DNS pointing to your regular [!DNL Target] hostname `clientcode.tt.omtrdc.net`. 

   For example, if your client code is "cnamecustomer" and your proposed hostname is `target.example.com`, your DNS CNAME record looks similar to:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >Adobe's certificate authority, DigiCert, cannot issue a certificate until this step is complete. Therefore, [!DNL Adobe] cannot fulfill your request for a CNAME implementation until this step is complete.

1. [Fill out this form](/help/assets/FPC_Request_Form.xlsx) and include it when you [open an Adobe Client Care ticket requesting CNAME support](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C):

   * Adobe [!DNL Target] client code:
   * SSL certificate hostnames (example: `target.example.com target.example.org`):
   * SSL certificate purchaser (Adobe is highly recommended, see FAQ): Adobe/customer
   * If the customer is purchasing the certificate, also known as "Bring Your Own Certificate" (BYOC), fill out these additional details:
      * Certificate organization (example: Example Company Inc):
      * Certificate organizational unit (optional, example: Marketing):
      * Certificate country (example: US):
      * Certificate state/region (example: California):
      * Certificate city (example: San Jose):

1. If [!DNL Adobe] is purchasing the certificate, [!DNL Adobe] works with DigiCert to purchase and deploy your certificate on Adobe's production servers.

   If the customer is purchasing the certificate (BYOC), [!DNL Adobe] Client Care sends you the certificate signing request (CSR). Use the CSR when purchasing the certificate through your certificate authority of choice. After the certificate is issued, send a copy of the certificate and any intermediate certificates to [!DNL Adobe] Client Care for deployment.

   [!DNL Adobe] Client Care notifies you when your implementation is ready.

1. Update the `serverDomain` to the new CNAME in at.js.

## Frequently Asked Questions

The following information answers frequently asked questions about requesting and implementing CNAME support in [!DNL Target]:

### Can I provide my own certificate (Bring Your Own Certificate or BYOC)?

You can provide your own certificate. However, [!DNL Adobe] does not recommend this practice. Management of the SSL certificate lifecycle is easier for both [!DNL Adobe] and you if [!DNL Adobe] purchases and controls the certificate. SSL certificates must be renewed every year. Therefore, [!DNL Adobe] Client Care must contact you every year to obtain a new certificate in a timely manner. Some customers can have difficulty producing a renewed certificate in a timely manner. Your [!DNL Target] implementation is jeopardized when the certificate expires because browsers refuse connections.

>[!IMPORTANT]
>
>If you request a [!DNL Target] bring-your-own-certificate CNAME implementation, you are responsible for providing renewed certificates to [!DNL Adobe] Client Care every year. Allowing your CNAME certificate to expire before [!DNL Adobe] can deploy a renewed certificate results in an outage for your specific [!DNL Target] implementation.

### How long until my new SSL certificate expires?

Certificates issued before September 1, 2020 are two-year certificates. Certificates issued on or after September 1, 2020 are one-year certificates. You can read more about the move to one-year certificates [here](https://www.digicert.com/position-on-1-year-certificates).

### What hostnames should I choose? How many hostnames per domain should I choose?

[!DNL Target] CNAME implementations require only one hostname per domain on the SSL certificate and in the customer's DNS. Adobe recommends one hostname. Some customers require more hostnames per domain for their own purposes (testing in staging, for example), which is supported.

Most customers choose a hostname like `target.example.com`. Adobe recommends following this practice, but the choice is ultimately yours. Do not request a hostname of an existing DNS record. Doing so causes a conflict and delays time to resolution of your [!DNL Target] CNAME request.

### I already have a CNAME implementation for [!DNL Adobe Analytics], can we use the same certificate or hostname?

No, [!DNL Target] requires a separate hostname and certificate.

### Is my current implementation of [!DNL Target] impacted by ITP 2.x?

In a Safari browser, navigate to your website on which you have a [!DNL Target] JavaScript library. If you see a [!DNL Target] cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

ITP issues can be resolved for [!DNL Target] with just an [!DNL Analytics] CNAME. You need a separate [!DNL Target] CNAME only in ad-blocking scenarios where [!DNL Target] is blocked.

For more information about ITP, see [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### What kind of service disruptions can I expect when my CNAME implementation is deployed?

There is no service disruption when the certificate is deployed (including certificate renewals). 

However, after you change the hostname in your [!DNL Target] implementation code (`serverDomain` in at.js) to the new CNAME hostname (`target.example.com`), web browsers treat returning visitors as new visitors. Returning visitors' profile data is lost because the previous cookie is inaccessible under the old hostname (`clientcode.tt.omtrdc.net`). The previous cookie is inaccessible due to browser security models. This disruption occurs only on the initial cut-over to the new CNAME. Certificate renewals do not have the same effect because the hostname doesn't change.

### What key type and certificate signature algorithm is used for my CNAME implementation?

All certificates are RSA SHA-256 and keys are RSA 2048-bit, by default. Key sizes larger than 2048-bit are not currently supported.

### How can I validate that my CNAME implementation is ready for traffic?

Use the following set of commands (in the macOS or Linux command-line terminal, using bash and curl 7.49+):

1. Paste this bash function into your terminal:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Paste this command (replacing `target.example.com` with your hostname):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   If the implementation is ready, you see output like below. The important part is that all lines include `CN=target.example.com`, which matches the desired hostname. If any lines include `CN=*.tt.omtrdc.net`, the implementation is **not** ready.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge36.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Validate your new DNS CNAME with another curl request, which should also show `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >If this command fails but the `validateEdgeFpsslSni` command above succeeds, wait for your DNS updates to fully propagate. DNS records have an associated [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) that dictates cache expiration time for DNS replies of those records. As a result, you might need to wait at least as long as your TTLs. You can use the `dig target.example.com` command or [the G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) to look up your specific TTLs.

## Known limitations

* QA mode is not sticky when you have CNAME and at.js 1.x because it is based on a third-party cookie. The workaround is to add the preview parameters to each URL you navigate to. QA mode is sticky when you have CNAME and at.js 2.x.
* Currently the `overrideMboxEdgeServer` setting doesn't work properly with CNAME when using at.js versions before at.js 1.8.2 and at.js 2.3.1. If you are using an older version of at.js, this setting should be set as `false` in order to avoid failing requests. Alternatively, you should consider [updating at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) to a newer, supported version.
* When using CNAME, it becomes more likely that the size of the cookie header for [!DNL Target] calls increase. [!DNL Adobe] recommends keeping the cookie size under 8 KB.
