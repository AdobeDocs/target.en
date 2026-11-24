---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;sftp;upload csv
description: Learn how to upload a CSV file to customize recommendations in Adobe [!DNL Target] Recommendations.
title: Upload custom criteria
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
TQID: 'https://experienceleague.adobe.com/8gSKOQxHGB5TPe6vdhjgy5sAFxN8O7dodITo7wgrR50'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Upload custom criteria {#upload-custom-criteria}

>[!BEGINSHADEBOX]

**On this page:** Learn how to upload a CSV file of recommendations to create custom criteria in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

Custom criteria use a CSV file of recommendations that is uploaded to [!DNL Target]. This allows recommendations that are computed outside [!DNL Target] to be delivered in [!DNL Recommendations] activities. For more information about how custom criteria work, see [The science behind Target's recommendations algorithms](/help/main/c-recommendations/c-algorithms/recommendations-algorithms.md).

Custom criteria are created from the **[!UICONTROL Create New Criteria]** screen. For the ways to reach this screen, see [Access the Create New Criteria screen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#access-create-criteria). The following steps start from the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen.

1. Click **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

    ![Criteria page with the Create criteria menu open, showing Create Criteria and Create Criteria Sequence](../assets/criteria_create_1.png)

1. Fill in the information in the [Basic Information](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) section.

1. From the **[!UICONTROL Select Algorithm Type]** drop-down list, select **[!UICONTROL Custom Criteria]**. From the **[!UICONTROL Algorithm]** drop-down list, select **[!UICONTROL Custom Algorithm]**.

    ![Recommendations Algorithm section with Custom Criteria as the Algorithm Type and Custom Algorithm as the Algorithm](../assets/criteria_create_9.png)

1. (Conditional) Fill in the information in the [Backup Content](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) and [Inclusion Rules](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) sections.

1. In the **[!UICONTROL Upload CSV]** section, select the **[!UICONTROL Location]** of the CSV file.

   The CSV file must be formatted correctly to upload successfully. To get a correctly formatted CSV file, click **[!UICONTROL Download the CSV template]**.

   The following location options are available:

   * **FTP**: To upload the CSV file from an FTP server, select **[!UICONTROL FTP]**, then enter the required information. SSL can be used, which uses the FTPS protocol to transfer the CSV file securely.

   * **SFTP**: To upload the CSV file from an SFTP server, select **[!UICONTROL SFTP]**, then enter the host name or IP address, port (default 22), username, a password and/or SSH private key, directory, and filename. For details, see [Supported SFTP server settings](/help/main/c-recommendations/c-products/feeds.md#steps).

     SFTP does not change the custom-criteria CSV format. Use the `# Key,Recommendation_1,...` format. A CSV file in the format of a different feed type causes the import to fail.

   * **URL**: To upload the CSV file from a URL, select **[!UICONTROL URL]**, then enter a feed URL.

      ![Upload CSV section with the Location options FTP, SFTP, and URL highlighted and SFTP selected](../assets/criteria_create_10.png)

1. Click **[!UICONTROL Create]**.

## Considerations

* Custom criteria entities (rows) can contain up to 1,000 recommended items (columns).

* Custom criteria updates are "cumulative" by default. New key-value pairs in the CSV upload file overwrite existing key-value pairs. Existing key-value pairs whose keys are not in the CSV upload remain available for delivery and expire 31 days after they were last uploaded as part of the CSV file.

  To discard the existing results that are not included in the next CSV upload, contact Client Care to enable the corresponding setting. When this setting is enabled, only the keys present in the custom CSV feed file are available for delivery. This setting applies to all custom criteria.

* Custom criteria feeds update once every 24 hours.

  The upload and sync status of each custom criteria upload is displayed on the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** page. The status is also displayed in the **[!UICONTROL Edit]** dialog box when custom criteria are edited.

* The flow for an error-free upload is **[!UICONTROL Scheduled]** > **[!UICONTROL Downloading Feed File]** > **[!UICONTROL Importing]** > **[!UICONTROL Successful]**.

* If [!DNL Target] encounters a problem with the upload, the following error messages are possible:

  | Error Message | Details |
  |--- |--- |
  |Unknown Error|Indicates an internal technical error.|
  |Parsing Error|There is likely an issue with the feed file format. Correct the file format and re-save the algorithm, which restarts the file download process.|
  |Server Not Found|Provide an IP or host name that is visible on the internet.|
  |Credentials Error|Provide a valid user and password for an active account on the server.|
  |Directory Not Found|Provide a directory that exists on the server.|
  |File Not Found|Provide the name of a file that exists on the server in the specified directory.|
