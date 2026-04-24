---
title: Integration with Adobe CX Enterprise solutions and services
description: Erfahren Sie mehr über die Integration von Search, Social und Commerce mit Adobe CX Enterprise-Lösungen und -Services.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
TQID: https://experienceleague.adobe.com/vIjCxWutfGn8H9-TqxLvztNazb9RWq7ECeoOQXLfyEw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: f2860a4b-f905-4545-bead-1bbc92564592
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 619
ht-degree: 0%

---

# Integration with Adobe CX Enterprise solutions and services

Advertising Search, Social, &amp; Commerce is integrated with the following [!DNL Adobe] products.

* [Tags from Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — You can use the [Adobe Advertising Cloud Extension](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) for Adobe Experience Platform to [create Adobe Advertising conversion tracking tags](/help/search-social-commerce/tools/conversion-tag-generate.md), as well as third-party tracking tags, for your ad landing pages. If your organization doesn&#39;t have an Experience Platform account, then you can still install the extension directly in the [user interface for Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection/), which is available for free to Adobe CX Enterprise customers.

  To install the required extension, contact your organization administrator for access to Data Collection features in the UI and ask them to grant you the `manage_properties` permission.

  **Note:** You can also [create conversion tracking tags directly within Search, Social, &amp; Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — (Opt-in feature) Adobe Advertising and [!DNL Analytics] are integrated in the following ways:

   * Adobe Advertising and [!DNL Analytics] seamlessly share data. [!DNL Analytics] can send site engagement and conversion data daily to Search, Social, &amp; Commerce, where the data is available for ad optimization and for reporting. Also, Adobe Advertising can send ad traffic data — including impressions, clicks, and cost — from your ad networks daily to [!DNL Analytics], where the data is available in all reporting tools.

     See &quot;[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)&quot; for more information about [!DNL Analytics] support for each ad network and ad type. See also &quot;[Overview of [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; for more information about the data exchange.

     To exchange data, both Adobe Advertising and [!DNL Analytics] must be initially configured. Contact your Adobe Account Team for more information about the initial setup.

     >[!NOTE]
     >
     >By default, the [!DNL Analytics] metrics aren&#39;t visible in Search, Social, &amp; Commerce screens. You must explicitly [make the metrics available in campaign management views, portfolios, and reports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) after the [!DNL Adobe] implementation team has configured selected standard or custom events to pass into Adobe Advertising. Sie können optional die angezeigten Metriknamen ändern (ohne sie in [!DNL Analytics] zu ändern). Sie können Metriken in der Benutzeroberfläche anzeigen lassen und Metriken unter [!UICONTROL Admin] > [!UICONTROL Conversions] umbenennen.

   * Werbetreibende mit [!DNL Analytics], aber nicht mit Audience Manager können [Zielgruppen  [!DNL Google Ads]  Kundenabgleich erstellen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) aus [!DNL Analytics] Segmenten erstellen, die mit Adobe CX Enterprise geteilt werden. Um berechtigt zu sein, muss ein Advertiser den [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) implementieren und ein Tag auf seinen Websites bereitstellen. Anschließend können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen (Zielgruppen) oder Ausschlüsse (Ausschlüsse) auf Kampagnenebene [ ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) [ Anzeigengruppe ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager-Segmente - (Opt-in-Funktion) Sie können [Zielgruppen erstellen [!DNL Google Ads] Kundenabgleich durchführen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) aus Audience Manager-Segmenten, die „Search“, „Social“ und Commerce als Ziel haben. Dies kann [!DNL Analytics] Segmente umfassen, die in Adobe CX Enterprise veröffentlicht werden, sowie Segmente, die mithilfe der Adobe CX Enterprise-Zielgruppenbibliothek erstellt wurden. Anschließend können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen (Zielgruppen) oder Ausschlüsse (Ausschlüsse) auf Kampagnenebene [ ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) [ Anzeigengruppe ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Weitere Informationen finden Sie unter &quot;[Adobe Advertising-Integrationen ](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html) Adobe Audience Manager&quot;.

* Adobe Target - Sie können die Clickthrough-Signalfreigabe zwischen Search, Social, Commerce und [!DNL Target] implementieren, eine A/B-Testaktivität in [!DNL Target] für Ihre Anzeigen einrichten und dann [!DNL Analytics] Analysis Workspace verwenden, um die Testdaten anzuzeigen.

* Adobe Campaign - Sie können [eine Zielgruppe für den Kundenabgleich erstellen  [!DNL Google Ads]  aktualisieren, indem Sie eine E-Mail-Liste in  [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe CX Enterprise-Benachrichtigungen - (Wenn Sie über Adobe CX Enterprise angemeldet sind) Über den Benachrichtigungslink ([Warnhinweise](/help/search-social-commerce/assets/notifications-panel.png "Alert Notifications")) oben auf jeder Seite können Sie alle Adobe CX Enterprise-Systemaktualisierungen, -Beiträge, -Erwähnungen und freigegebenen Assets anzeigen. Wenden Sie sich an Ihr Adobe-Accountteam , um Informationen zum Zugriff auf Adobe CX Enterprise zu erhalten.
