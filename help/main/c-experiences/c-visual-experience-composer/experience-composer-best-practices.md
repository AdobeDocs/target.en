---
keywords: visual experience composer;visual experience composer best practices;visual experience composer limitations;visual experience composer caveats;vec best practices;vec
description: Learn best practices to make your experiences work as expected when using the [!UICONTROL Visual Experience Composer] (VEC).
title: What Are [!UICONTROL Visual Experience Composer] Best Practices and Limitations?
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
TQID: 'https://experienceleague.adobe.com/upZDSyuS9VqUmYskNXrlYazhwRHmZGBpSR-cR-qliRs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!UICONTROL Visual Experience Composer] best practices and limitations {#vec-best-practices}

>[!BEGINSHADEBOX]

**On this page:** Learn the best practices, caveats, and limitations to be aware of when creating experiences in the **[!UICONTROL Visual Experience Composer]** (VEC).

>[!ENDSHADEBOX]

Following these practices helps experiences created in the [!DNL Adobe Target] **[!UICONTROL Visual Experience Composer]** (VEC) function as intended. The caveats and limitations describe behaviors that can cause common issues, so knowing them helps avoid problems and maintain performance.

## Best practices {#best-practices}

The following practices apply when using the VEC.

### Enable the [!UICONTROL Enhanced Experience Composer] {#enable-eec}

The **[!UICONTROL Enhanced Experience Composer]** can be enabled at the account level, which enables it for all activities created in the account, or at the individual activity level.

* **Account level:** Click **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**, then toggle the **[!UICONTROL Enable Enhanced Experience Composer]** switch to the On position.
* **Activity level:** While creating an activity in the **[!UICONTROL Visual Experience Composer]**, click **[!UICONTROL Configure]** > **[!UICONTROL Page Delivery]**, then toggle the **[!UICONTROL Enable Enhanced Experience Composer]** switch to the On position.

### Page setup and loading

+++ Place the at.js reference at the top of the `<head>` section of the page.

If the **[!UICONTROL Visitor API Service]** is also used, place the Visitor API script above at.js.

+++

+++ Allowlist IP addresses if the [!UICONTROL Enhanced Experience Composer] does not load on secure pages of the site.

Allowlisting the IP addresses of the [!DNL Adobe] servers used for the **[!UICONTROL Enhanced Experience Composer]** proxy resolves loading problems. These IP addresses are required only for activity editing. Visitors to the site do not need them allowlisted. The IP addresses are listed in [The EEC will not load an internal QA URL that is not accessible on public IP](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md#eec-ip-addresses) in *Troubleshooting issues related to the Enhanced Experience Composer*.

+++

+++ Do not use the base tag in the website to resolve URLs and links.

The VEC, including the **[!UICONTROL Enhanced Experience Composer]**, manipulates the website behind the scenes through a proxy server that updates all link URLs to make them work in the proxy. If a base tag is added, the browser resolves these URLs again, so they appear broken.

+++

+++ Do not use the `top` or `self` variables in JavaScript code.

When the **[!UICONTROL Enhanced Experience Composer]** is enabled, the values of the `top` and `self` variables are updated to disable iframe busting. Use an X-Frame-Options header to add iframe busting instead of custom JavaScript code.

+++

+++ Always test the website if parameters are added when the page loads.

For example, the following URL parameters are used to open `www.abc.com` for editing in an iframe:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Make sure that the website loads as expected after adding parameters like these.

+++

+++ Make sure that the page opens as expected in an iframe.

Turn off iframe busting techniques on the website and check whether the website opens as expected in an iframe on a dummy page. For example:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>
  <iframe src="https://www.homedepot.com"</iframe>
</body>
</html>
```

+++

### Page markup

+++ Use unique IDs for top-level elements and for any other elements that are good testing or targeting candidates.

Anything immediately inside the body element should have a unique ID, so that at least the parent elements are easy to recognize when new elements are injected into the body and the code moves around.

[!DNL Target] does not require IDs, but IDs increase the reliability of experiences created with the experience composer. [!DNL Target] uses CSS selectors to modify content when the experience is delivered. When an experience is edited, the **[!UICONTROL Visual Experience Composer]** anchors the selector to the closest ancestor of the modified HTML element that has a non-null ID attribute. It is therefore not advisable to use any mechanism, including JavaScript libraries, that sets or modifies HTML ID attributes. Those IDs might be available to the experience composer when the activity is created, but if JavaScript modifies them, the ID used at creation might not be available when the experience runs. If an ID is not available, the selector anchored to that ID fails.

+++

+++ Use descriptive CSS class names.

Descriptive class names make the classes easy to identify when CSS classes are edited in the **[!UICONTROL Visual Experience Composer]**. This helps ensure that the right CSS classes are edited and that the pages appear as expected.

+++

+++ Do not use the `!important` CSS property when hiding or removing elements.

If the `!important` CSS property is present, the CSS rules of the site override the changes that `target.js` makes during delivery.

+++

+++ Avoid HTML tables for page layouts.

[!DNL Target] uses JavaScript to format a page, and table-based layouts are difficult to modify with JavaScript. Table-based layouts might also not display the same way in all browsers. For best results, use CSS to create page layouts.

+++

+++ Minimize the use of iFrames.

Minimizing iFrames simplifies page and test management. The **[!UICONTROL Visual Experience Composer]** can apply some actions within an iFrame, but some actions, such as resizing, do not work properly. Pages that use multiple iFrames are difficult to manage and resize, so testing iFrame-heavy pages can create problems.

+++

+++ Use only plain text or an image tag in anchor elements.

An anchor element contains either plain text:

`<a>Anchor Text</a>`

or an image tag:

`<a href=""> <img src=""> </img> </a>`

+++

+++ Avoid block-level elements inside an inline element.

Block-level elements should not be used inside inline elements, such as anchor and span elements. Doing so causes the inline elements to lose their height and width, so the overlay tool in the **[!UICONTROL Visual Experience Composer]** might not work as expected.

+++

+++ Be careful when removing form fields.

Certain form fields might be mandatory for submission, so removing them could affect submissions.

+++

+++ Keep important text that might be used for targeting in the HTML code within an element.

For example, the Shopping Cart text cannot be targeted in the VEC if the code is like the following:

```html
<a href="https://www.botanicchoice.com/shop.axd/Cart">
   <img alt="Shopping Cart" src="/images/ico-cart.gif"></img>
   Shopping Cart:
   <span id="HeaderCartQtyTotal">
      0
  </span>
  Items
  <span id="HeaderCartPriceTotal"></span>
</a>
```

In this example, the entire anchor element is selected in the VEC, which adversely affects other elements if targeting is performed.

+++

### Editing and delivery

+++ Arrange all dynamic DOM modifications as soon after DOM ready as possible.

If the modifications fail to apply before `target.js` applies the experience, content delivery could be broken. This happens only when there is a DOM change in the hierarchy of a targeted element.

+++

+++ Using Edit HTML to manipulate the DOM structure can break selectors.

For example, two actions are taken:

* A class is added to Element 1.
* The HTML of Element 1 is edited.

Each change creates a new element in the VEC. The second action modifies Element 1, so if Element 1 is deleted, the second action no longer has anything to modify and the change no longer works.

In the same way, if an element is added with text and a separate action then edits that element with different text, the code editor shows both actions as separate elements. The edit creates a new element that modifies the original one and contains the edited text. If the original element is then deleted, the edited text cannot find the element to modify and does not display. The second element remains in the list of elements, but it has no effect on the page because the element it changes no longer exists.

See [Element Selectors Used in the **[!UICONTROL Visual Experience Composer]**](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#vec-selectors).

+++

+++ Use `<b>` and `<i>` tags when styling text elements with the rich-text editor.

* For bold text, use `<b>` rather than `<strong>`.
* For italic text, use `<i>` rather than `<em>`.

The `<strong>` and `<em>` tags might cause unexpected results.

+++

+++ Do not include `mboxCreate` inside scripts.

`mboxCreate` uses `document.write`, so including it in scripts is not recommended. Use `mboxDefine` and `mboxUpdate` for the same purpose.

+++

+++ Do not update an HTML snippet with [!DNL Target] if the snippet requires JavaScript code for its initialization.

When an action (Edit HTML) is performed on page components such as sliders and carousels, delivery might appear broken. The VEC performs the action after JavaScript has instantiated the page component. When the page content is delivered to visitors, however, the action is applied before the component is instantiated. As a result, the functionality of the component might or might not break at delivery, depending on the script that defines the component on the page.

A delivery test that works the first time does not guarantee that delivery continues to work, because a race condition might exist:

* If there is a race condition, delivery works intermittently.
* If there is no race condition, delivery always works.

Test the page multiple times to make sure that delivery works as expected.

+++

## Caveats {#caveats}

The following caveats apply when using the **[!UICONTROL Visual Experience Composer]** to design an activity.

+++ The [!UICONTROL Move] feature does not support z-index.

Without z-index functionality, a moved element cannot be placed on top of another element. See [Limitations](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721) for more details.

+++

+++ Rearranging elements affects click tracking.

If an element marked for click tracking is rearranged, the paths of the rearranged elements change. As a result, clicks are tracked on the element in the location where the original element was before it was rearranged.

This occurs because the code that delivers the activity content and the code that tracks clicks are included in one piece of code that is delivered to the page. If a different page is browsed to and click tracking is set up there, both pieces of code are delivered to that page. If the click-tracking page has a page structure similar to that of the page where the test runs, the test content might also appear on the click-tracking page.

+++

+++ Inserting an element might not work in a `<div>` that is an mbox.

If an mbox contains an offer and the mbox is implemented incorrectly, an inserted element might appear as `insertBefore` and not as `insertAfter`.

+++

+++ When editing both a parent element and a child element, edit the parent first.

If an image action is swapped on an element and the text or HTML of its parent element is then edited, delivery issues can occur. The best workflow is to edit the parent element before swapping the image on the child element.

+++

+++ Do not select a page element that includes an mbox as a child element.

For example, if the page contains the following code:

```html
<div>
  <div class="mboxDefault" >
  </div>
  <script>mboxCreate('myMbox');
</script>
</div>
```

The outer div should not be selected in an experience, because the mbox hardcoded in the page still makes a call to [!DNL Target] and receives a response. This response interferes with the response intended for the larger page element.

+++

+++ Proxy IP addresses might be blocked in the environment of the customer.

If the **[!UICONTROL Enhanced Experience Composer]** is used on a non-live site, such as a staging environment, timeouts and access denied errors might occur if the site blocks the proxy IP addresses.

+++

## Limitations {#section_F33C2EA27F2E417AA036BC199DD6C721}

The following limitations apply when working with the VEC.

### Page requirements

+++ Handle VEC compatibility with [!DNL Chrome] extension policy changes.

Under the updated [V3 Manifest policies in Google Chrome](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank}, extensions can no longer modify the original DOM before the browser parses it. As a result, certain security scripts, such as iframe-busting implementations, might block pages from loading in the VEC.

To ensure compatibility, conditionally disable these scripts when the page is loaded inside the [!DNL Target] iframe. This can be done safely by checking for the presence of the `window.adobeVecExtension` object, which [!DNL Target] injects while the VEC loads.

The following code snippets are examples of iframe-busting code that can prevent a web page from loading in the VEC:

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

A simple check can verify when a web page is embedded inside [!DNL Target]. The code snippet looks like this:

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

+++ Pages must accept URL parameters for the VEC to work.

Some sites strip any URL parameters from their pages, but the VEC requires those parameters.

+++

+++ When a script is used as part of HTML, declare any variables and functions that are accessed from outside under the window namespace.

The script is executed within the scope of `target.js` after the page loads, so any variable or function that is declared locally is not accessible from outside the script block.

*Incorrect:*

```html
<script>
  var myVar = 123;
  function myFunc() {
    //
  }
</script>
```

*Correct:*

```html
<script>
  window.myVar = 123;
  window.myFunc = function() {
    //
  };
</script>
```

+++

+++ The `customCode` action in the VEC does not work with [!DNL Internet Explorer] 8.

`target.js` does not support this action in IE8 because of IE8 limitations when handling script content. As a workaround, if the page contains jQuery and jQuery is exposed globally on the window object, `target.js` can deliver the `customCode` action. Make sure that `window.jQuery` and `window.jQuery.fn.prepend` are defined.

+++

### Rearranging and mboxes

**An element cannot be moved outside a container that is followed by a CSS property.**

+++ The [!UICONTROL Button] element cannot be selected for rearranging.

**[!UICONTROL Button]** elements cannot be selected directly for rearranging. To enable rearrangement, place the buttons inside a larger container.

+++

+++ Do not rearrange and move the same element.

If an element has been moved to another location, and the parent container is then selected to rearrange the child elements, the moved element is not affected and remains where it is. The rearrangement might not appear as desired.

+++

+++ Only swap offers are available on mboxes.

Actions such as **[!UICONTROL Edit Class]** and **[!UICONTROL Rearrange]** are not allowed inside an mbox.

+++

### Images

+++ The [!UICONTROL Change Image] action does not work on an image in a carousel.

For example, if the page contains a carousel with six images and an image is to be swapped with the second image of the carousel, the **[!UICONTROL Change Image]** action does not work.

As a workaround, select the parent container and use the **[!UICONTROL Edit HTML]** action to edit the HTML of the carousel and update the image source of the desired image.

+++

+++ Images cannot be resized in an mbox.

If an image is swapped in an mbox element and then resized according to the size of the mbox element, the resizing is not permitted.

+++

+++ After an image is swapped, the [!UICONTROL Edit] action cannot be selected.

After the image is swapped, the Scene7 URL cannot be edited.

+++

+++ Inserting an image from the [!UICONTROL Content] library (Scene7) and editing the HTML breaks the image URL.

Add an anchor element inside the `customHeaderMessage` div with some dummy text:

```html
<a href="#">
<span> Dummy text </span>
</a>
```

Select this div using the **[!UICONTROL Insert Element]** action to insert an image as a sibling of the dummy text.

After the image is inserted, the code looks like this:

```html
<a href="#">
<span> Dummy text </span>
<img src=""> This is inserted Image. </img>
</a>
```

Remove the dummy text span.

+++

### Click tracking and external content

+++ Click tracking does not work for anchor elements that contain anything other than plain text or image tags.

For example, click tracking does not work if the element contains JavaScript.

+++

+++ Click tracking is supported only on the page on which experiences are created or on the redirected page.

Although **[!UICONTROL Browse]** mode is available for click tracking in the VEC, **[!UICONTROL Browse]** mode cannot be used to add click tracking on a page.

+++

+++ HTML elements with an external source cannot be edited.

For example: video, audio tags, embed, iFrames, and frames. 

+++
