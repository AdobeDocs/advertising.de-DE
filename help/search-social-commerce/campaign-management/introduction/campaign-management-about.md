---
title: Über die Kampagnenverwaltung in Search, Social und Commerce
description: Erfahren Sie mehr über die Funktionen zur Kampagnenverwaltung in Search, Social und Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Über die Kampagnenverwaltung in Search, Social und Commerce

Mit Search, Social und Commerce können Sie Ihre Kampagnen für Suche, Anzeige/Inhalt, Social Media, Shopping, Audience und Performance Max an einem Ort verfolgen und/oder verwalten. Je nach Anzeigennetzwerk und Kampagnentyp können die verfügbaren Funktionen eine Synchronisierung mit Ihren Anzeigennetzwerken, das Erstellen und Bearbeiten von Funktionen, Tracking und Konversionszuordnung, Berichte sowie die Angebots- und Budgetoptimierung umfassen. Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

Während Sie Kampagnendaten in den [!UICONTROL Campaigns] hinzufügen und bearbeiten, übertragen Search, Social und Commerce die Datenänderungen sofort an das Werbenetzwerk. Search, Social und Commerce ruft außerdem einmal täglich (oder öfter, wenn neue Kampagnen erkannt werden) und bei Bedarf Kampagnenstrukturdaten und Klickdaten aus synchronisierten Anzeigennetzwerkkonten ab.

## Einrichten des Zugriffs auf Ihre Werbenetzwerkkonten

Um die Performance von Anzeigen im Ad-Network-Konto eines Werbetreibenden zu verfolgen (und möglicherweise Gebote für die Anzeigen zu platzieren), erstellt das Adobe-Account-Team [einen entsprechenden Account-Eintrag](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) in Search, Social und Commerce. Der Kontodatensatz enthält Tracking-Optionen.

Bei Konten, die über die API des Anzeigennetzwerks synchronisiert werden, enthält der Kontodatensatz auch die Anmeldeinformationen für den Kontozugriff. Sobald das Konto aktiviert ist, werden die Kontodaten mit dem Werbenetzwerk abgerufen. Sie können dann die vorhandenen Kontodaten anzeigen sowie die Kampagnenstruktur und Anzeigendaten erstellen und bearbeiten.

## Klick-Tracking zum Verknüpfen von Klicks mit Konversionen

Wenn Sie den Konversionsverfolgungs-Service von Adobe Advertising verwenden, müssen Sie den Klick-Tracking-Code für Search, Social und Commerce in das Suffix der Landingpage, Tracking-Vorlagen und endgültige/Ziel-URLs für Anzeigen, Keywords und Platzierungen, Sitelinks und Produktlisten aufnehmen. Bei [unterstützten Werbenetzwerken und Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) deren Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, fügt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode an, sodass Sie ihn nicht manuell hinzufügen müssen. Andernfalls müssen Sie den Code manuell zu Ihren Tracking-Vorlagen oder endgültigen URLs hinzufügen.

Weitere Informationen zum Tracking finden Sie im Kapitel „Tracking“.

## Automatisieren von Gebots- und Budgetverwaltung

Für [unterstützte Werbenetzwerke und Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) können Sie Ihre Kampagnen in Portfolios mit jeweils einem bestimmten Geschäftsziel und einem bestimmten Budget oder Leistungsziel gruppieren. In Standardportfolios optimiert Search, Social und Commerce CPC-Keyword-Gebote und Kampagnenbudgets. Hybridportfolios kombinieren Optimierungstechnologien aus Search, Social und Commerce sowie Ihren Werbenetzwerken.

Weitere Informationen zu den verfügbaren Portfoliooptionen und zum Einrichten von Portfolios finden Sie im Kapitel Optimierungshandbuch unter &quot;Portfolios&quot;, das in Search, Social und Commerce verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

## Die Ansichten des Kampagnen-Managements

Mit den Ansichten für das Kampagnen-Management können Sie Ihre Suchkonten überwachen und verwalten. Die folgenden Ansichten sind verfügbar:

* **[!UICONTROL Campaigns]** - Die [!UICONTROL Campaigns] zeigen Daten von jedem verbundenen Anzeigennetzwerkkonto an. Sie können Kosten-, Klick-, Impressions- und Umsatzdaten über alle Anzeigennetzwerkkonten und über einzelne Konten, Kampagnen, Anzeigengruppen, Keywords, Anzeigen, Shopping-Produktgruppen, Platzierungen, automatische Ziele (dynamische Suchziele), Zielgruppen und Anzeigenerweiterungsbibliotheken und die zugehörigen Kontoentitäten hinweg anzeigen. Für [unterstützte Kampagnentypen in unterstützten Werbenetzwerken](/help/search-social-commerce/introduction/supported-inventory.md) können Sie Daten für einzelne Kampagnen und Kampagnenkomponenten direkt in der Benutzeroberfläche erstellen und bearbeiten. Optional können Sie die Daten in den meisten Unteransichten in eine Tabellendatei exportieren.

  >[!NOTE]
  >
  >Daten auf Anzeigenebene sind nicht verfügbar für [!DNL Google Ads] Dynamic Search Ad (DSA), Performance Max, Smart Shopping und [!DNL YouTube] Kampagnen.

* **[!UICONTROL Products]** - Die [!UICONTROL Products] zeigen Daten für jedes [[!DNL Google] - oder  [!DNL Microsoft] -Center-Konto an, das synchronisiert &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Die standardmäßige [!UICONTROL Accounts]-Unteransicht listet alle synchronisierten Konten auf. Einige Benutzertypen können neue Konten aus dieser Ansicht hinzufügen. Die [!UICONTROL Products] Unteransicht listet jedes Produkt im Konto auf.

* **[!UICONTROL Advanced (ACM)]** - In der Ansicht [!DNL Advanced] ([!DNL AMC], für Advanced Campaign Management) können Sie automatisierte Prozesse einrichten, um [dynamische Anzeigen und Keywords zu erstellen, die auf jedes Element in Ihrem Inventar ausgerichtet sind](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) entsprechend einer von Ihnen erstellten netzwerkspezifischen Anzeigenvorlage und dem Inhalt [!DNL Google Merchant Center] Konten oder Bestandsdatendateien, die Sie in einen FTP-Speicherort hochladen. Unteransichten zeigen Details zu jeder Feed-Vorlage für den Advertiser und zu jeder Kampagne, Anzeigengruppe, jedem Keyword und jeder Anzeige, die in einem Feed enthalten sind, der über eine Feed-Vorlage propagiert, aber nicht im Anzeigennetzwerk veröffentlicht wurde.

* **[!UICONTROL Bulksheets]** - Verwenden Sie die [!UICONTROL Bulksheets], um [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) zu erstellen, die beliebig viele Daten für ein Konto in einem [unterstützten Anzeigennetzwerk](/help/search-social-commerce/introduction/supported-inventory.md) enthalten, und sie dann im Anzeigennetzwerk zu veröffentlichen.

* **[!UICONTROL Audiences]** - [Die [!UICONTROL Audiences]-](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)) listet alle Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Zielgruppen auf, die aus verschiedenen Arten von Benutzerlisten generiert wurden. Sie können [!DNL Google Ads] Zielgruppen aus Ihren bestehenden Adobe Experience Cloud-Zielgruppen und Ihren Kunden-E-Mail-Listen erstellen. Sie können auch Zielgruppenziele und Ausschlüsse für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Anzeigen anzeigen und verwalten.

* **[!UICONTROL Label Classifications]** - Verwenden Sie diese Ansicht, um [Kennzeichnungsklassifizierungen](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) zu erstellen und zu löschen, damit Sie Ihre Kennzeichnungen in aussagekräftigen Sätzen gruppieren können.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Konten und Kampagnen des Werbenetzwerks](campaign-implemention-overview.md)
>* [Überwachen und Verwalten der Leistung Ihrer Werbenetzwerk-Kampagnen](monitor-performance-campaigns.md)
>* [Google Ads-Konversionsdaten in Search, Social und Commerce](google-conversion-data.md)
