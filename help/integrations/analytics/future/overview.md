---
title: Adobe Advertising integrations with Adobe Analytics
description: Learn about how Adobe Advertising can exchange data with Adobe Analytics and how you can use the data within Search, Social, & Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Adobe Advertising integrations with Adobe Analytics

You can integrate Adobe Advertising with Analytics in the following ways.

## Exchange data between [!DNL Analytics] and Adobe Advertising

### Pull [!DNL Analytics] data into Adobe Advertising

With [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] and DSP pull in:

* **[!DNL Analytics]segments:**  Metadata, hierarchy data, and unique audience data for all of an advertiser&#39;s or agency&#39;s segments created in [!DNL Analytics] and published to Adobe CX Enterprise.

* **[!DNL Analytics]site engagement metrics**

* **[!DNL Analytics]standard, custom, and reserved metrics**

### Send Adobe Advertising data to [!DNL Analytics]

* **Traffic metrics from Adobe Advertising**

* **Dimensions from Adobe Advertising**

>[!NOTE]
>
>For [!DNL Search, Social, & Commerce], this feature is supported for most ad networks and campaign types. See &quot;Supported Inventory&quot; in the [!DNL Search, Social, & Commerce] Guide for more information.<!-- add link when that's published in ExL -->

### Use [!DNL Analytics] segments to create [!DNL Google Ads] audiences {#audience-manager-google-audiences}

*Opted-in advertisers with [!DNL Advertising Search, Social, & Commerce] only*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], you can create [!DNL Google Ads] Google customer match audiences from user IDs using your existing [!DNL Analytics] segments. This includes Adobe Analytics segments that are published to Adobe CX Enterprise and segments that are created using the Adobe CX Enterprise [!DNL Audience Library]. For more information, see &quot;[Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Customer match audiences from user IDs](https://support.google.com/google-ads/answer/9199250) work like website tag-based audiences, but a non-PII ID is assigned to unique audience members for distinct benefits over standard customer match and website tag-based audiences.

To create the necessary user IDs, you must use an Adobe Advertising JavaScript tag <!-- with a user ID parameter -->on your websites. Contact your Adobe Account Team for more information.

![segment creation process](/help/integrations/assets/ad_search_user_id_pic.png)

Nach der Erstellung können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen oder Ausschlüsse [ Kampagnen oder Anzeigengruppen ](#audience-manager-targets).

### Verwenden [!DNL Analytics] Segmente zum Targeting oder Ausschließen von Anzeigen {#analytics-targets}

* (Opt-in-Werbetreibende mit [!DNL Search, Social, & Commerce]) Sie können in Ihren [!DNL Google Ads]-Kampagnen beliebige [!DNL Google Ads]-Zielgruppen [erstellt mit [!DNL Analytics] Segmenten](#audience-manager-google-audiences) als Zielgruppen oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene verwenden.

* (Advertisers mit DSP) Sie können Ihre vorhandenen [!DNL Analytics] als Ziele für Ihre Anzeigenplatzierungen verwenden. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Advertisers mit Advertising Creative) Sie können Ihre vorhandenen [!DNL Analytics] als Ziele für bestimmte Kreative in Ihren Anzeigenerlebnissen verwenden.
