---
keywords: visual experience composer;visual experience composer best practices;visual experience composer limitations;visual experience composer caveats;vec best practices;vec
description: Learn best practices to make your experiences work as expected when using the [!UICONTROL Visual Experience Composer] (VEC).
title: What Are [!UICONTROL Visual Experience Composer] Best Practices and Limitations?
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
---
# [!UICONTROL Visual Experience Composer] best practices and limitations

To ensure your experiences function as intended, follow best practices when using the [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC). Be aware of key tips and limitations to maximize performance and avoid common issues. 

## Best Practices {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}

The following are best practices when using the VEC:

### Place the at.js reference at the top of the `<head>` section of your page.

+++See details
If you also use the [!UICONTROL Visitor API Service], place the visitor API script above at.js.

+++

### You can enable the [!UICONTROL Enhanced Experience Composer] at the account level (enabled for all activities created in the account) or at the individual activity level.

+++See details
To enable the [!UICONTROL Enhanced Experience Composer] at the account level, click [!UICONTROL [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer]], then toggle the [!UICONTROL Enable Enhanced Experience Composer] switch to the On position.

To enable the [!UICONTROL Enhanced Experience Composer] at the activity level while creating an activity in the [!UICONTROL Visual Experience Composer], click [!UICONTROL Configure > [!UICONTROL Page Delivery]], then toggle the [!UICONTROL Enable Enhanced Experience Composer] switch to the On position.

+++

### You can allowlist certain IP addresses if the [!UICONTROL Enhanced Experience Composer] won't load on secure pages on your site.

+++See details
Problems loading the [!UICONTROL Enhanced Experience Composer] can be resolved by allowlisting the following IP addresses. These IP addresses are for [!DNL Adobe] servers used for the [!UICONTROL Enhanced Experience Composer] proxy. They are only required for activity editing. Visitors to your site do not need these IP addresses allowlisted.

For more information, see [The EEC won't load an internal QA URL that is not accessible on public IP](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) in *Troubleshooting issues related to the Enhanced Experience Composer*.

+++

### Use unique IDs for top-level elements and any other elements that could be good testing/targeting candidates.

+++Details
Anything immediately inside the body element should have a unique ID. If new elements are injected into the body and code moves around, at least the parent elements have an easier way to be recognized.

[!DNL Target] does not require IDs, but using IDs increases the reliability of experiences created with the experience composer. [!DNL Target] uses CSS selectors to modify your content when the experience is delivered. When you edit an experience, the [!UICONTROL Visual Experience Composer] anchors the selector to the closest ancestor with a non-null ID attribute to the HTML element being modified. It is, therefore, not advisable to use any mechanism, including JavaScript libraries, that sets or modifies HTML ID attributes. Although those IDs might be available to the [!DNL Target] experience composer for activity creation, if JavaScript modifies IDs, the ID that was used when the experience was created might not be available when the experience runs. If an ID is not available, the selector anchored to the ID fails.

+++

### Name CSS classes so they are easily identifiable.

+++Details
When editing CSS classes in the [!DNL Visual Experience Composer], it is helpful to make the classes easy to identify by using descriptive class names. This helps to ensure that you edit the right CSS classes, and your pages appear as expected.

Don't use the `!important` CSS property when hiding or removing elements.

If the `!important` CSS property is present, changes made by `target.js` during delivery is overridden by the site's CSS rules.

+++

### Avoid using HTML tables for page layouts.

+++Details
[!DNL Target] uses JavaScript to format a page. It is difficult to modify table-based layouts with JavaScript. Also, table-based layouts might not display the same way in all browsers. For best results, use CSS to create page layouts.

+++

### Minimize the use of iFrames.

+++Details
It is a good practice to minimize the use of iFrames, to simplify page and test management. The Visual Experience Composer can apply some actions within an iFrame, but some actions, such as resizing, do not work properly. It is difficult to manage and resize pages that use multiple iFrames. As a result, testing iFrame-heavy pages can create problems.

+++

### Attempt to arrange all dynamic DOM modifications as soon after DOM ready as possible.

+++Details
If your modifications fail to apply before the experience application by `target.js`, content delivery could be broken. This happens only when there is a DOM change in the hierarchy of a targeted element.

+++

### Use only plain text or an image tag in your anchor elements.

+++Details
`<a>Anchor Text</a>`

OR

`<a href=""> <img src=""> </img> </a>`

+++

### Avoid block-level elements inside an inline element.

+++Details
Block-level elements should not be used inside inline elements, such as anchor, span, and so on. Doing so causes inline elements to lose their height and width, so the overlay tool in the [!UICONTROL Visual Experience Composer] might not work as expected.

+++

### Don't use the base tag in your website to resolve URLs and links.

+++Details
The VEC manipulates the website behind the scenes, using a proxy server that updates the links. If you add a base tag, the URLs used by the proxy server are resolved again by the browser and appear broken.

+++

### Using EDIT HTML to manipulate DOM structure can break selectors.

+++Details
For example, if you have taken two actions:

* Added a class to Element 1
* Edited the HTML for Element 1

Each change creates a new element in the VEC. Because the second action modifies Element 1, if you delete Element 1, the second action no longer has anything to modify, so the change no longer works.

In other words, if you add an element with text, then in a separate action you edit that element with different text, the code editor shows both actions as separate elements. When you edited the element, you created a new element that modifies the original one you created, containing the edited text. If you then delete the original element, the edited text won't be able to find the element that was edited, and will not display. The second element remains in the list of elements, but it does not affect the page because the element it changes no longer exists.

See [Element Selectors Used in the [!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337).

+++

### Use `<b>` and `<i>` tags when styling text elements with the rich-text editor.

+++Details
* For bold text, use `<b>` rather than `<strong>`.
* For italic text, use `<i>` rather than `<em>`.

`<strong>` and `<em>` tags might cause unexpected results.

+++

### Be careful when removing form fields.

+++Details
Certain form fields might be mandatory for submission. Removing those form fields could impact submissions.

+++

### Do not include `mboxCreate` inside scripts.

+++Details
Because `mboxCreate` uses `document.write`, it is not recommended to include `mboxCreate` in scripts. Instead, use `mboxDefine` and `mboxUpdate` for the same purpose.

+++

### Don't update an HTML snippet using [!DNL Target] if it requires JavaScript code for its initialization.


+++Details
When an action (Edit HTML) is performed on page components (such as sliders, carousels, and so on), delivery might appear broken. The VEC performs the action after the page component has been instantiated by JavaScript.

However, when the content of the page is delivered to visitors, the action is applied before instantiation of the component. Because of this, this component's functionality may or may not break at the time of delivery. Functionality depends on the nature of the script used on his page to define the component.

If you test for delivery and it works the first time, it is not guaranteed that it will continue working. There may (or may not) be a race condition.

* If there is a race condition, delivery works intermittently.
* If there is no race condition, delivery always works.

Test your page multiple times to make sure delivery works as expected.

+++

### Don't use a base tag in your website to resolve URLs and links.

+++Details
When you use the [!UICONTROL Enhanced Experience Composer], the website is manipulated behind the scenes by a proxy server that updates all link URLs to make them work in the proxy. If you add a base tag, all these URLs are resolved by the browser, so they appear broken.

+++

### Important text on the site that might be used for targeting should be kept in HTML code within an element.

+++Details
For example, you cannot target Shopping Cart text in the VEC if your code is like the following:

```html
<a href="https://www.botanicchoice.com/shop.axd/Cart"> 
   <img alt="Shopping Cart"src="/images/ico-cart.gif"></img> 
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

### Don't use `top` or `self` variables in JavaScript code.

+++Details
When the [!UICONTROL Enhanced Experience Composer] is enabled, the value of the top and self variables are updated to disable iframe busting. Use an X-frame-options header to add iframe busting instead of custom JavaScript codes.

+++

### Always test your website if parameters are added when loading the page.

+++Details
For example, to open `www.abc.com`, the following URL parameters are used:

`www.abc.com?mboxEdit=1&mboxDisable=1`

These parameters enable editing in an iframe.

Make sure your website loads as expected after adding parameters like these.

+++

### Make sure your page opens as expected in an iframe.

+++Details
Turn OFF iframe busting techniques on your website and check whether the website opens as expected within an iframe on a dummy page. For example:

```html
<!DOCTYPE 
<html> 
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

## Caveats {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

Consider the following caveats when using the [!UICONTROL Visual Experience Composer] to design your activity.

### The [!UICONTROL Move] feature does not support z-index.

+++Details
Because there is no z-index functionality, the moved element can't be moved on top of another element. See [Limitations](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721) for more details.

+++

### Rearranging elements affects click tracking.

+++Details
If an element marked for click tracking is rearranged, the paths of the rearranged elements are changed. As a result, the element in the location where the original element was before it was rearranged is the one whose clicks are tracked.

This occurs because both the code to deliver the activity content and the code to track clicks is included in one piece of code that is delivered to the page. If you browse to a different page and set up click tracking, then the activity content code and the click tracking code are delivered to that page. If the click-tracking page has a similar page structure to the page where the test is run, then the test content might also appear on the click-tracking page.

+++

### Inserting an element might not work in a `<div>` that is an mbox.

+++Details
If an mbox contains an offer, inserting an element may appear as `insertBefore` and not `insertAfter`, if the mbox is implemented incorrectly.

+++

### When editing both a parent and child element, edit the parent first.

+++Details
If you swap an image action on an element, then edit the text or HTML on its parent element, delivery issues can occur. The best workflow is to edit the parent element before swapping the image on the child element.

+++

### Cannot select page element that includes an mbox as a child element.

+++Details
For example, if your page contains:

```html
<div> 
  <div class="mboxDefault" > 
  </div>
  <script>mboxCreate('myMbox'); 
</div>`
```

The outer div should not be selected in an experience because the mbox hardcoded in the page still makes a call to [!DNL Target] and receives a response. This response interferes with the response intended for the larger page element.

+++

### Proxy IPs might be blocked in customers environment.

+++Details
If you are using [!UICONTROL Enhanced Experienced Composer] on a non-live site, such as a staging environment, you might see timeouts and access denied errors if your site blocks RIPs.

+++

## Limitations {#section_F33C2EA27F2E417AA036BC199DD6C721}

Consider the following limitations when working with the VEC:

### Handling VEC compatibility with [!DNL Chrome] extension policy changes. {#ext}

+++Details
Due to updated [V3 Manifest policies in Google Chrome](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank}, extensions can no longer modify the original DOM before it is parsed by the browser. As a result, certain security scripts&mdash;such as iframe-busting implementations&mdash;might block pages from loading in the VEC.

To ensure compatibility, these scripts should be conditionally disabled when the page is loaded inside the [!DNL Target] iframe. This process can be safely done by checking for the presence of the `window.adobeVecExtension` object, which is injected by [!DNL Target] during VEC loading.

The following code snippets are examples of iframe-busting code that can lead to web page not loading in the VEC:

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

A simple check can be used to verify when a web page is embedded inside [!DNL Target]. A code snippet should look like this:

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

### You cannot move an element outside a container followed by a CSS property.

+++Details
An element cannot be moved outside a container that is followed by a CSS property.

+++

### You cannot select the [!UICONTROL Button] element for rearranging.

+++Details
[!UICONTROL Button] elements cannot be directly selected for rearranging. To enable rearrangement, place buttons inside a larger container.

+++

### Only swap offers are available on mboxes.

+++Details
Actions such as [!UICONTROL Edit Class] and [!UICONTROL Rearrange] are not allowed inside an mbox.

+++

### You should not rearrange and move the same element.

+++Details
If an element has been moved to another location, and you select the parent container and try to rearrange the child elements, the moved element is not affected and remains where it is. The rearrangement might not appear as desired.

+++

### The [!UICONTROL Change Image] action does not work on an image in a carousel.

+++Details
If, for example, your page contains a carousel with six images and you want to swap an image with the second image of the carousel, the [!UICONTROL Change Image] action does not work.

The workaround is to select the parent container and use the [!UICONTROL Edit HTML] action to edit the HTML of the carousel to update the image source of the desired image.

+++

### Images cannot be resized in an mbox.

+++Details
If you swap an image in an mbox element, then try to resize that image according to the mbox element size, the resizing is not permitted.

+++

### After you swap an image, you cannot select the [!UICONTROL Edit] action.

+++Details
After you swap the image, you cannot edit the Scene7 URL.

+++

### HTML elements with an external source cannot be edited.

+++Details
For example: Video, audio tags, embed, iFrames, frames.

+++

### Click tracking does not work for anchor elements that contain anything other than plain text or image tags.

+++Details
For example, click tracking does not work if the element contains JavaScript.

+++

### Pages must accept URL parameters for the VEC to work.

+++Details
Some sites strip any URL parameters for their pages. However, the VEC requires those parameters.

+++

### While using a script as part of HTML, any variables and functions that are accessed from outside should be declared under the window namespace.

+++Details
The script is executed within the scope of `target.js` after the page loads. Therefore, any variable or function that is declared locally is not accessible from outside the script block.

*Incorrect:*

```html
<script> 
  var myVar = 123; 
  function myFunc() { 
    // 
  } 
</script>`
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

### Inserting an image from the [!UICONTROL Content] library (Scene7) and editing the HTML breaks the image URL.

+++Details
Add an anchor element inside the 'customHeaderMessage' div with some dummy text:

```html
<a href="#"> 
<span> Dummy text </span>
</a>
```

Select this div using the [!UICONTROL Insert Element] action to insert a image as a sibling of this dummy text div. 

After image insertion, it looks like:

```html
<a href="#">  
<span> Dummy text </span> 
<img src=""> This is inserted Image. </img> 
</a>
```

Remove the dummy text span.

+++

### The `customCode` action in the VEC does not work with [!DNL Internet Explorer] 8.

+++Details
Due to IE8 limitations when handling script content, `target.js` does not support this in IE8. As a workaround, if the page contains jQuery and is exposed on the window object globally, `target.js` can use deliver the `customCode` action. Ensure that `window.jQuery` and `window.jQuery.fn.prepend` are defined.

+++

### Click tracking is supported only on the page on which experiences are created or on the redirected page.

+++Details
Although [!UICONTROL Browse] mode is available for click tracking in the VEC, [!UICONTROL Browse] mode can't be used to add click tracking on a page.

+++
