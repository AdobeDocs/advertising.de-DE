---
title: Über die Kampagnenverwaltung in Search, Social und Commerce
description: Erfahren Sie mehr über die Kampagnenverwaltungsfunktionen in Search, Social und Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Über die Kampagnenverwaltung in Search, Social und Commerce

Mit Search, Social und Commerce können Sie Ihre Such-, Anzeige-/Inhaltskampagnen, Social-Media-, Einkaufs-, Zielgruppen- und Performance-Max-Kampagnen an einem Ort verfolgen und/oder verwalten. Je nach Werbenetzwerk und Kampagnentyp können die verfügbaren Funktionen die Synchronisierung mit Ihren Werbenetzwerken, die Erstellung und Bearbeitung von Funktionen, die Nachverfolgung und Konversionszuordnung, die Berichterstellung sowie die Gebots- und Budgetoptimierung umfassen. Weitere Informationen zu den für jedes Anzeigennetzwerk verfügbaren Funktionen finden Sie unter &quot;[Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

Beim Hinzufügen und Bearbeiten von Kampagnendaten in den [!UICONTROL Campaigns] -Ansichten überträgt Search, Social und Commerce die Datenänderungen sofort an das Werbenetzwerk. In Search, Social und Commerce werden auch Kampagnenstrukturdaten abgerufen und Klickdaten aus synchronisierten Anzeigen-Netzwerk-Konten einmal täglich (oder häufiger, wenn neue Kampagnen erkannt werden) und nach Bedarf abgerufen.

## Zugriff auf Ihre Werbenetzwerkkonten einrichten

Um die Leistung von Anzeigen im Anzeigennetzwerkkonto eines Advertisers zu verfolgen (und möglicherweise Angebote für die Anzeigen zu platzieren), erstellt das Adobe Account-Team [einen entsprechenden Kontodatensatz](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) in Search, Social und Commerce. Der Kontodatensatz enthält Tracking-Optionen.

Bei Konten, die über die API des Anzeigennetzwerks synchronisiert werden, enthält der Kontodatensatz auch die Kontozugriffsberechtigungen. Sobald das Konto aktiviert ist, werden die Kontodaten mit dem Werbenetzwerk abgerufen. Anschließend können Sie die vorhandenen Kontodaten anzeigen sowie die Kampagnenstruktur und Anzeigendaten erstellen und bearbeiten.

## Klick-Tracking zum Verbinden von Klicks mit Konversionen

Wenn Sie den Adobe Advertising-Konversions-Tracking-Dienst verwenden, müssen Sie den Klick-Trackingcode für Search, Social und Commerce in das Suffix der Landingpage, Tracking-Vorlagen und endgültige/Ziel-URLs für Anzeigen, Suchbegriffe und Platzierungen, Sitelinks und Produktlisten aufnehmen. Bei [unterstützten Werbenetzwerken und Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md), deren Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;beinhalten, hängt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Weiterleitungs- und Trackingcode an, sodass Sie ihn nicht manuell hinzufügen müssen. Andernfalls müssen Sie den Code manuell zu Ihren Tracking-Vorlagen oder endgültigen URLs hinzufügen.

Weitere Informationen zum Tracking finden Sie im Kapitel &quot;Tracking&quot;.

## Automatisierung von Gebots- und Budgetverwaltung

Für [unterstützte Werbenetzwerke und Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) können Sie Ihre Kampagnen in Portfolios gruppieren, von denen jede ein bestimmtes Geschäftsziel sowie ein bestimmtes Budget oder Leistungsziel aufweist. In Standard-Portfolios optimiert Search, Social und Commerce CPC-Suchbegriffangebote und Kampagnenbudgets. Hybrid-Portfolios kombinieren Optimierungstechnologien aus Search, Social und Commerce und Ihren Werbenetzwerken.

Weitere Informationen zu den verfügbaren Portfoliooptionen und zum Einrichten von Portfolios finden Sie im Kapitel &quot;Optimierungshandbuch&quot;zu &quot;Portfolio&quot;, das in Search, Social und Commerce verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

## Ansichten der Kampagnenverwaltung

Die Kampagnenverwaltungsansichten ermöglichen die Überwachung und Verwaltung Ihrer Suchkonten. Die folgenden Ansichten sind verfügbar:

* **[!UICONTROL Campaigns]** - Die [!UICONTROL Campaigns] -Ansichten zeigen Daten aus jedem verbundenen Anzeigen-Netzwerkkonto an. Sie können Kosten-, Klick-, Impressions- und Umsatzdaten für alle Anzeigennetzwerkkonten und über einzelne Konten, Kampagnen, Anzeigengruppen, Suchbegriffe, Anzeigen, Einkaufsproduktgruppen, Platzierungen, automatische Ziele (dynamische Suchziele), Zielgruppen und Anzeigenerweiterungsbibliotheken und die zugehörigen Kontoentitäten anzeigen. Für [unterstützte Kampagnentypen in unterstützten Werbenetzwerken](/help/search-social-commerce/introduction/supported-inventory.md) können Sie Daten für einzelne Kampagnen und Kampagnenkomponenten direkt in der Benutzeroberfläche erstellen und bearbeiten. Optional können Sie die Daten in den meisten Unteransichten in eine Tabellendatei exportieren.

  >[!NOTE]
  >
  >Daten auf Anzeigenebene stehen nicht für [!DNL Google Ads] dynamische Suchanzeige (DSA), Performance-Max, Smart-Shopping und [!DNL YouTube]-Kampagnen zur Verfügung.

* **[!UICONTROL Products]** - Die [!UICONTROL Products] -Ansichten zeigen Daten für jedes [[!DNL Google] oder [!DNL Microsoft] Handelscenter-Konto an, das synchronisiert wird](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Die Standardunteransicht &quot;[!UICONTROL Accounts]&quot; listet alle synchronisierten Konten auf. Einige Benutzertypen können von dieser Ansicht aus neue Konten hinzufügen. In der Unteransicht &quot;[!UICONTROL Products]&quot;werden die einzelnen Produkte innerhalb des Kontos aufgelistet.

* **[!UICONTROL Advanced (ACM)]** - Aus der Ansicht [!DNL Advanced] ([!DNL AMC], für erweiterte Campaign Management) können Sie automatisierte Prozesse einrichten, um [dynamische Anzeigen und Suchbegriffe für jedes Element in Ihrem Bestand zu erstellen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md), je nach einer von Ihnen erstellten Anzeigennetzwerkspezifischen Anzeigenvorlage und dem Inhalt von [!DNL Google Merchant Center]-Konten oder Bestandsdatendateien, die Sie an einen FTP-Speicherort hochladen. In Subviews werden Details zu den einzelnen Feed-Vorlagen für den Advertiser und zu den einzelnen Kampagnen, Anzeigengruppen, Keywords und Anzeigen angezeigt, die in einem Feed enthalten sind, der über eine Feed-Vorlage propagiert, aber nicht im Werbenetzwerk veröffentlicht wurde.

* **[!UICONTROL Bulksheets]** - Verwenden Sie die Ansicht [!UICONTROL Bulksheets] , um [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) zu erstellen, die so viele Daten enthalten, wie Sie für ein Konto in einem [unterstützten Anzeigennetzwerk](/help/search-social-commerce/introduction/supported-inventory.md) benötigen, und diese dann im Werbenetzwerk zu veröffentlichen.

* **[!UICONTROL Audiences]** - [ Die [!UICONTROL Audiences] Ansichten](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) listen alle Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Zielgruppen auf, die aus verschiedenen Arten von Benutzerlisten generiert wurden. Sie können [!DNL Google Ads] -Zielgruppen aus Ihren bestehenden Adobe Experience Cloud-Zielgruppen und Ihren Kunden-E-Mail-Listen erstellen. Sie können auch Zielgruppenziele und Ausschlüsse für Ihre [!DNL Google Ads] - und [!DNL Microsoft Advertising] -Anzeigen anzeigen und verwalten.

* **[!UICONTROL Label Classifications]** - Verwenden Sie diese Ansicht, um [Beschriftungsklassifizierungen](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) zu erstellen und zu löschen. So können Sie Ihre Bezeichnungen in aussagekräftige Sätze gruppieren.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen](campaign-implemention-overview.md)
>* [Überwachen und Verwalten der Leistung Ihrer Werbenetzwerk-Kampagnen](monitor-performance-campaigns.md)
>* [Google Ads-Konversionsdaten in Search, Social und Commerce](google-conversion-data.md)
