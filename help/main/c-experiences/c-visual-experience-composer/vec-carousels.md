---
keywords: Visual Experience Composer;VEC;carousel
description: Learn how to create a carousel that can be edited in the Adobe [!DNL Target] Visual Experience Composer (VEC).
title: How Do I Create Carousels in the Visual Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
TQID: 'https://experienceleague.adobe.com/RN04MJgC49BI2-h2e-i-kgSRTejpLHzKACm-hOv2VCE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Creating carousels that work in the [!UICONTROL Visual Experience Composer] {#vec-carousels}

>[!BEGINSHADEBOX]

**On this page:** Learn how to build a carousel that can be edited in the **[!UICONTROL Visual Experience Composer]** (VEC).

>[!ENDSHADEBOX]

A carousel built with the following structure can be edited in the [!DNL Adobe Target] **[!UICONTROL Visual Experience Composer]** (VEC). The structure keeps the selector of each slide valid, so [!DNL Target] always identifies the correct slide, even when the displayed slide changes a few seconds after the page loads in the VEC.

1. Create the slides as static HTML placeholders, with one visible slide and the other slides hidden by class.

   ```html
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. Design the look and feel with CSS only. Do not use JavaScript for this.

   >[!NOTE]
   >
   >The **[!UICONTROL Render Using JavaScript]** option is currently not supported when it is used together with custom code in the **[!UICONTROL Visual Experience Composer]**.

1. Show the next slide by updating only the class names: hide the other slides and show the next one with a timer or an animation. Never update the DOM structure with JavaScript.
