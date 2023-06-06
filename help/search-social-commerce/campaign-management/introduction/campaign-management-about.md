---
title: Über die Kampagnenverwaltung in Search, Social und Commerce
description: Erfahren Sie mehr über die Kampagnenverwaltungsfunktionen in Search, Social und Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Über die Kampagnenverwaltung in Search, Social und Commerce

Mit Search, Social und Commerce können Sie Ihre Such-, Anzeige-/Inhaltskampagnen, Social-Media-, Einkaufs-, Zielgruppen- und Performance-Max-Kampagnen an einem Ort verfolgen und/oder verwalten. Je nach Werbenetzwerk und Kampagnentyp können die verfügbaren Funktionen die Synchronisierung mit Ihren Werbenetzwerken, die Erstellung und Bearbeitung von Funktionen, die Nachverfolgung und Konversionszuordnung, die Berichterstellung sowie die Gebots- und Budgetoptimierung umfassen. Weitere Informationen zu den für jedes Anzeigennetzwerk verfügbaren Funktionen finden Sie unter[Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

Beim Hinzufügen und Bearbeiten von Kampagnendaten im [!UICONTROL Campaigns] -Ansichten, Suche, Social und Commerce überträgt die Datenänderungen sofort in das Werbenetzwerk. In Search, Social und Commerce werden auch Kampagnenstrukturdaten abgerufen und Klickdaten aus synchronisierten Anzeigen-Netzwerk-Konten einmal täglich (oder öfter, wenn neue Kampagnen erkannt werden) und nach Bedarf abgerufen.

## Zugriff auf Ihre Werbenetzwerkkonten einrichten

Um die Leistung von Anzeigen in einem Anzeigennetzwerkkonto eines Werbetreibenden zu verfolgen (und möglicherweise Angebote für die Anzeigen zu platzieren), muss das Adobe Account Team [erstellt einen entsprechenden Kontodatensatz](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) in Search, Social und Commerce. Der Kontodatensatz enthält Tracking-Optionen.

Bei Konten, die über die API des Anzeigennetzwerks synchronisiert werden, enthält der Kontodatensatz auch die Kontozugriffsberechtigungen. Sobald das Konto aktiviert ist, werden die Kontodaten mit dem Werbenetzwerk abgerufen. Anschließend können Sie die vorhandenen Kontodaten anzeigen sowie die Kampagnenstruktur und Anzeigendaten erstellen und bearbeiten.

## Klick-Tracking zum Verbinden von Klicks mit Konversionen

Wenn Sie den Adobe Advertising-Konversions-Tracking-Dienst verwenden, müssen Sie den Klick-Trackingcode für Suche, Social und Commerce in das Suffix der Landingpage, Tracking-Vorlagen und End-/Ziel-URLs für Anzeigen, Suchbegriffe, Platzierungen, Sitelinks und Produktlisten aufnehmen. Für [unterstützte Werbenetzwerke und Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) deren Kampagneneinstellungen Folgendes enthalten:[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot;&quot;Search, Social und Commerce hängt beim Speichern des Datensatzes automatisch seinen eigenen Umleitungs- und Trackingcode an, sodass Sie ihn nicht manuell hinzufügen müssen. Andernfalls müssen Sie den Code manuell zu Ihren Tracking-Vorlagen oder endgültigen URLs hinzufügen.

Weitere Informationen zum Tracking finden Sie im Kapitel &quot;Tracking&quot;.

## Automatisierung von Gebots- und Budgetverwaltung

Für [unterstützte Werbenetzwerke und Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md)können Sie Ihre Kampagnen in Portfolios gruppieren, jeweils mit einem bestimmten Geschäftsziel und einem spezifischen Budget- oder Leistungsziel. In Standard-Portfolios optimiert Search, Social und Commerce CPC-Suchbegriffangebote und Kampagnenbudgets. Hybrid-Portfolios kombinieren Optimierungstechnologien aus Search, Social, &amp; Commerce und Ihren Werbenetzwerken.

Weitere Informationen zu den verfügbaren Portfoliooptionen und zum Einrichten von Portfolios finden Sie im Kapitel &quot;Optimierungshandbuch&quot;zum &quot;Verwalten von Portfolios&quot;, das in &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

## Ansichten der Kampagnenverwaltung

Mit den Ansichten zur Kampagnenverwaltung können Sie Ihre Suchkonten überwachen und verwalten. Die folgenden Ansichten sind verfügbar:

* **[!UICONTROL Campaigns]** — Die [!UICONTROL Campaigns] -Ansichten zeigen Daten aus jedem verbundenen Anzeigennetzwerkkonto an. Sie können Kosten-, Klick-, Impressions- und Umsatzdaten für alle Anzeigennetzwerkkonten und über einzelne Konten, Kampagnen, Anzeigengruppen, Suchbegriffe, Anzeigen, Einkaufsproduktgruppen, Platzierungen, automatische Ziele (dynamische Suchziele), Zielgruppen und Anzeigenerweiterungsbibliotheken und die zugehörigen Kontoentitäten anzeigen. Für [unterstützte Kampagnentypen in unterstützten Werbenetzwerken](/help/search-social-commerce/introduction/supported-inventory.md)können Sie Daten für einzelne Kampagnen und Kampagnenkomponenten direkt in der Benutzeroberfläche erstellen und bearbeiten. Optional können Sie die Daten in den meisten Unteransichten in eine Tabellendatei exportieren.

   >[!NOTE]
   >
   >Daten auf Anzeigenebene stehen nicht zur Verfügung für [!DNL Google Ads] dynamische Suchanzeige (DSA), Leistungsmax, intelligentes Einkaufen und [!DNL YouTube] Kampagnen.

* **[!UICONTROL Products]** — Die [!UICONTROL Products] Ansichten zeigen Daten zu jedem [[!DNL Google] or [!DNL Microsoft] Konto des Händlers, das synchronisiert wird](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Die Standardeinstellung [!UICONTROL Accounts] Die Unteransicht listet alle synchronisierten Konten auf. Einige Benutzertypen können in dieser Ansicht neue Konten hinzufügen. Die [!UICONTROL Products] In der Unteransicht werden alle Produkte innerhalb des Kontos aufgelistet.

* **[!UICONTROL Advanced (ACM)]** — von der [!DNL Advanced] ([!DNL AMC]für die Ansicht &quot;Advanced Campaign Management&quot;(Erweiterter) können Sie automatisierte Prozesse einrichten, um [dynamische Anzeigen und Suchbegriffe, die auf jedes Element in Ihrem Bestand ausgerichtet sind](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) entsprechend einer von Ihnen erstellten Anzeigennetzwerkspezifischen Anzeigenvorlage und dem Inhalt von [!DNL Google Merchant Center] Konten oder Lagerbestandsdatendateien, die Sie an einen FTP-Speicherort hochladen. In Subansichten werden Details zu den einzelnen Feed-Vorlagen für den Advertiser und zu den einzelnen Kampagnen, Anzeigengruppen, Keywords und Anzeigen angezeigt, die in einem Feed enthalten sind, der über eine Feed-Vorlage propagiert, aber nicht im Werbenetzwerk veröffentlicht wurde.

* **[!UICONTROL Bulksheets]** — Verwenden Sie die [!UICONTROL Bulksheets] Ansicht zum Erstellen [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) mit so vielen Daten, wie Sie für ein Konto auf einem [unterstütztes Anzeigennetzwerk](/help/search-social-commerce/introduction/supported-inventory.md)und dann im Werbenetzwerk veröffentlichen.

* **[!UICONTROL Audiences]** — [Die [!UICONTROL Audiences] views](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) listet alle Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] aus verschiedenen Arten von Benutzerlisten generierte Zielgruppen. Sie können [!DNL Google Ads] Zielgruppen aus Ihren bestehenden Adobe Experience Cloud-Zielgruppen und Ihren Kunden-E-Mail-Listen. Sie können auch Zielgruppenziele und Ausschlüsse für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Anzeigen.

* **[!UICONTROL Label Classifications]** — Verwenden Sie diese Ansicht zum Erstellen und Löschen [Beschriftungsklassifizierungen](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), die Ihnen dabei helfen können, Ihre Bezeichnungen in aussagekräftige Sets zu gruppieren.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen](campaign-implemention-overview.md)
>* [Überwachen und verwalten Sie die Leistung Ihrer Werbenetzwerk-Kampagnen.](monitor-performance-campaigns.md)
>* [Google Ads-Konversionsdaten in Search, Social und Commerce](google-conversion-data.md)

