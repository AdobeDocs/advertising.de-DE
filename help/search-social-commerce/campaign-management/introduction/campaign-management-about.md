---
title: Über die Kampagnenverwaltung in Search, Social und Commerce
description: Erfahren Sie mehr über die Funktionen zur Kampagnenverwaltung in Search, Social und Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tgoMzw4DbEY5evC2s1f6mQHfJYYb7DJzMfFUnc-06Bk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 808
ht-degree: 0%

---

# Über die Kampagnenverwaltung in Search, Social und Commerce

Mit Search, Social und Commerce können Sie Ihre Kampagnen für Suche, Anzeige/Inhalt, Social Media, Shopping, Audience und Performance Max an einem Ort verfolgen und/oder verwalten. Je nach Anzeigennetzwerk und Kampagnentyp können die verfügbaren Funktionen eine Synchronisierung mit Ihren Anzeigennetzwerken, das Erstellen und Bearbeiten von Funktionen, Tracking und Konversionszuordnung, Berichte sowie die Angebots- und Budgetoptimierung umfassen. Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

Während Sie Kampagnendaten in den [!UICONTROL Campaigns] hinzufügen und bearbeiten, übertragen Search, Social und Commerce die Datenänderungen sofort an das Werbenetzwerk. Search, Social und Commerce ruft außerdem einmal täglich (oder öfter, wenn neue Kampagnen erkannt werden) und bei Bedarf Kampagnenstrukturdaten und Klickdaten aus synchronisierten Anzeigennetzwerkkonten ab.

## Einrichten des Zugriffs auf Ihre Werbenetzwerkkonten

Um die Performance von Anzeigen im Netzwerk-Konto eines Werbetreibenden zu verfolgen (und möglicherweise Angebote für die Anzeigen zu platzieren), erstellt das Adobe Account Team [einen entsprechenden Account-Datensatz](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) in Search, Social und Commerce. Der Kontodatensatz enthält Tracking-Optionen.

Bei Konten, die über die API des Anzeigennetzwerks synchronisiert werden, enthält der Kontodatensatz auch die Anmeldeinformationen für den Kontozugriff. Sobald das Konto aktiviert ist, werden die Kontodaten mit dem Werbenetzwerk abgerufen. Sie können dann die vorhandenen Kontodaten anzeigen sowie die Kampagnenstruktur und Anzeigendaten erstellen und bearbeiten.

## Klick-Tracking zum Verknüpfen von Klicks mit Konversionen

Wenn Sie den Konversionsverfolgungs-Service von Adobe Advertising verwenden, müssen Sie den Klick-Tracking-Code für Search, Social und Commerce in das Suffix der Landingpage, Tracking-Vorlagen und endgültige/Ziel-URLs für Anzeigen, Keywords und Platzierungen, Sitelinks und Produktlisten aufnehmen. Bei [unterstützten Werbenetzwerken und Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) deren Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, fügt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode an, sodass Sie ihn nicht manuell hinzufügen müssen. Andernfalls müssen Sie den Code manuell zu Ihren Tracking-Vorlagen oder endgültigen URLs hinzufügen.

Weitere Informationen zum Tracking finden Sie im Kapitel „Tracking“.

## Automatisieren von Gebots- und Budgetverwaltung

Für [unterstützte Werbenetzwerke und Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) können Sie Ihre Kampagnen in Portfolios mit jeweils einem bestimmten Geschäftsziel und einem bestimmten Budget oder Leistungsziel gruppieren. In Standardportfolios optimiert Search, Social und Commerce CPC-Keyword-Gebote und Kampagnenbudgets. Hybridportfolios kombinieren Optimierungstechnologien aus Search, Social und Commerce sowie Ihren Werbenetzwerken.

Weitere Informationen zu den verfügbaren Portfoliooptionen und zum Einrichten von Portfolios finden Sie im Kapitel Optimierungshandbuch zu „Portfolios“, das in Search, Social und Commerce verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

## Die Ansichten des Kampagnen-Managements

The campaign management views allow you to monitor and manage your search accounts. The following views are available:

* **[!UICONTROL Campaigns]** — The [!UICONTROL Campaigns] views show data from each connected ad network account. You can view cost, click, impression, and revenue data across all ad network accounts and across individual accounts, campaigns, ad groups, keywords, ads, shopping product groups, placements, auto targets (dynamic search targets), audiences, and ad extension libraries and their associated account entities. For [supported campaign types on supported ad networks](/help/search-social-commerce/introduction/supported-inventory.md), you can create and edit data for individual campaigns and campaign components directly in the interface. You can optionally export the data in most subviews to a spreadsheet file.

  >[!NOTE]
  >
  >Ad-level data isn&#39;t available for [!DNL Google Ads] dynamic search ad (DSA), performance max, smart shopping, and [!DNL YouTube] campaigns.

* **[!UICONTROL Products]** — The [!UICONTROL Products] views show data for each [[!DNL Google] or [!DNL Microsoft] merchant center account that&#39;s synced](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). The default [!UICONTROL Accounts] subview lists all synced accounts; some user types can add new accounts from this view. The [!UICONTROL Products] subview lists each product within the account.

* **[!UICONTROL Advanced (ACM)]** —  From the [!DNL Advanced] ([!DNL AMC], for Advanced Campaign Management) view, you can set up automated processes to create [dynamic ads and keywords targeted to each item in your inventory](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) according to an ad network-specific ad template you create and the contents of [!DNL Google Merchant Center] accounts or inventory data files you upload to an FTP location. Subviews show details about each feed template for the advertiser and each campaign, ad group, keyword, and ad included in a feed that was propagated through a feed template but not posted to the ad network.

* **[!UICONTROL Bulksheets]** — Use the [!UICONTROL Bulksheets] view to create [bulksheet files](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) containing as much data as you want for an account on a [supported ad network](/help/search-social-commerce/introduction/supported-inventory.md), and then post them to the ad network.

* **[!UICONTROL Audiences]** — [The [!UICONTROL Audiences] views](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) lists all of your [!DNL Google Ads] and [!DNL Microsoft Advertising] audiences generated from various types of user lists. You can create [!DNL Google Ads] audiences from your existing Adobe CX Enterprise audiences and your customer email lists. You can also view and manage audience targets and exclusions for your [!DNL Google Ads] and [!DNL Microsoft Advertising] ads.

* **[!UICONTROL Label Classifications]** — Use this view to create and delete [label classifications](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), which can help you group your labels into meaningful sets.

>[!MORELIKETHIS]
>
>* [Overview of implementing ad network accounts and campaigns](campaign-implemention-overview.md)
>* [Monitor and manage the performance of your ad network campaigns](monitor-performance-campaigns.md)
>* [Google Ads conversion data in Search, Social, &amp; Commerce](google-conversion-data.md)
