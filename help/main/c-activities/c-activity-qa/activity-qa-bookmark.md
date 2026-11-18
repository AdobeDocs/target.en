---
keywords: qa;preview;bookmarklet;preview links
description: Learn how to use the Adobe [!DNL Target] QA bookmarklet to force [!DNL Target] to release you from QA mode.
title: How Do I use the Activity QA Bookmarklet?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
TQID: 'https://experienceleague.adobe.com/kOQcdF2WgiAGkOS3rrLWfDSFTvRJX8jb-IeaahWnM0c'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Activity QA bookmarklet {#activity-qa-bookmarklet}

>[!BEGINSHADEBOX]

**On this page:** Learn how to use the [!DNL Target] QA bookmarklet to exit **[!UICONTROL Activity QA]** mode and view your site like a typical visitor.

>[!ENDSHADEBOX]

After you browse a website in [QA mode](/help/main/c-activities/c-activity-qa/activity-qa.md), QA mode persists across pages until your [!DNL Target] session expires. A bookmarklet is a browser bookmark that runs JavaScript. The [!DNL Target] QA bookmarklet forces [!DNL Target] to release you from QA mode, so you do not have to wait for the session to expire. Use the version that matches the at.js version deployed on your site.

>[!NOTE]
>
>The process to create a bookmarklet varies by browser type and version. Consult the help of your browser or search on the Internet for specific directions.

## Activity QA bookmarklet for at.js 1.*x*

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to the Bookmarks Toolbar of your browser:

```javascript
javascript:(
    function () {
        if (window.location.href.indexOf('?') != -1) {
            var parts = window.location.href.split('at_preview_token',2);
            if (parts.length > 1) {
                window.location.href = parts[0].concat('at_preview_token=');
            } else {
                window.location.href = window.location.href.concat("&at_preview_token=")
            }
        } else {
            window.location.href = window.location.href.concat("?at_preview_token=")
        }
    }
)();
```

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter set to an empty value. For example:

`https://www.mysite.com/?at_preview_token=`

## Activity QA bookmarklet for at.js 2.*x*

In contrast to at.js 1.*x*, at.js 2.*x* does not support third-party cookies. QA mode persists only for the first-party domain, by means of a first-party cookie set by at.js. As a result, the QA mode session is managed only on the client side, and no QA mode cookies are sent to [!DNL Target].

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to the Bookmarks Toolbar of your browser:

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {            
            document.cookie = AT_QA_MODE + ';domain='+window.location.hostname+";Path=/; Max-Age=-0;";
            var token = window.location.href.indexOf("?at_preview_token")<0? "&at_preview_token" : "?at_preview_token";
            var url = window.location.href.split(token,2)[0];
            window.open(url, '_self', 'noreferrer');
        }
    })(); 
```

## Use the Activity QA bookmarklet

After you add the bookmarklet that matches your at.js version to your browser, use it whenever you want to leave QA mode:

1. Open any page of your site while you are in QA mode.
1. Click the bookmarklet in the Bookmarks Toolbar of your browser.
1. Load a page of your site. [!DNL Target] releases the session from QA mode, and the site displays as it does for a typical visitor.
