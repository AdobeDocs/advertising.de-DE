---
title: Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen
description: Erfahren Sie mehr über die Aufgaben beim Einrichten, Synchronisieren und Verwalten Ihrer Anzeigennetzwerkkonten.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen

Adobe arbeitet mit jedem Advertiser zusammen, um seine Anzeigennetzwerkkonten und -kampagnen einzurichten. Dazu gehören die Konfiguration von Search, Social und Commerce für die Verbindung und Synchronisierung mit den Konten des Advertisers, die Erstellung neuer Kampagnen und Kampagnenkomponenten nach Bedarf, die Einrichtung des Trackings für die Komponentenanzeigen, optional das Hinzufügen der Kampagnen zu Portfolios, damit Search, Social und Commerce das Angebot für die Anzeigen optimieren können, und die Validierung der ursprünglichen Kosten-, Klick- und Umsatzdaten.

Nachdem eine Kampagne aktiviert und optional einem Portfolio hinzugefügt wurde, muss das Adobe Account Management Team, das Agenturteam oder der Advertiser (je nach den Bedingungen der Service-Level-Vereinbarung) jede-Kampagne überwachen und die relevanten Komponenten und Einstellungen entsprechend den Zielen des Advertisers ändern.

Diese Seite enthält Informationen zu allen Kontotypen, einschließlich der Einrichtung der Kampagnenstruktur für synchronisierte Konten. Weitere Anweisungen zum Einrichten von Nur-Tracking-Konten für [!DNL Naver] finden Sie unter &quot;[Implementieren [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)&quot;.

## Erste Einrichtungsaufgaben für Konten und Kampagnen

[!DNL Adobe] und/oder Ihre Agentur arbeitet mit Ihnen Folgendes:

1. (Neue Advertiser-Konten) Einrichten von Verwaltungskonten:

   1. Richten Sie das Konto des Werbetreibenden ein.

   1. (Bei Bedarf) Erstellen Sie Benutzerkonten für den Advertiser, um seine Kampagnendaten anzuzeigen und zu verwalten und Berichte zu erstellen.

1. (Einige Werbenetzwerke) Erhalten Sie eine Autorisierung für Search, Social und Commerce, um über die API des Anzeigennetzwerks und die Benutzeroberfläche von Search, Social und Commerce auf jedes Konto zuzugreifen.

1. Für jedes Anzeigen-Netzwerk-Konto:

   1. (Bei Bedarf) Richten Sie das Konto im Werbenetzwerk ein.

   1. Integrieren Sie in das Konto, indem Sie [einen entsprechenden Kontodatensatz erstellen](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) in Search, Social und Commerce, der die Kontozugriffsberechtigungen und Tracking-Optionen enthält, und legen Sie den Kontostatus auf &quot;Aktiviert&quot;fest.

      Suchen, Social und Commerce synchronisiert sich dann mit dem Anzeigennetzwerk. Wenn das Konto bereits Kampagnendaten enthält, sind die Daten in etwa 24 Stunden verfügbar.

   1. ([Anzeigentypen, die Sie in Search, Social und Commerce erstellen/bearbeiten können](/help/search-social-commerce/introduction/supported-inventory.md)) Wenn das Konto noch keine Kampagnendaten enthält, erstellen Sie die Kampagnenstruktur und Kampagnenkomponenten aus Search, Social und Commerce mit einer der folgenden für den Anzeigentyp verfügbaren Methoden:

      * (Google Ads, Microsoft Advertising, Yahoo! Nur Anzeigen und Yandex-Konten) Richten Sie einen [automatisierten Prozess ein, um dynamische Anzeigen und Suchbegriffe zu erstellen, die auf jedes Element in Ihrem Bestand abzielen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md), entsprechend einer von Ihnen erstellten Anzeigennetzwerkspezifischen Anzeigenvorlage und dem Inhalt der Lagerbestandsdatendateien, die Sie an einen FTP-Speicherort hochladen.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads- und Yandex-Konten) Laden Sie [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) hoch, die so viele Daten enthalten, wie Sie für ein Konto benötigen, und veröffentlichen Sie sie dann in den Werbenetzwerken.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads- und Yandex-Konten) Geben Sie Daten für einzelne Komponenten direkt in die Benutzeroberfläche ein. Für die meisten Kampagnen- und Anzeigentypen können Sie Daten auf Kampagnenebene, auf Anzeigengruppenebene sowie einzelne Suchbegriffe, Platzierungen und Anzeigenebenen erstellen.

      Einige Kampagnen- und Anzeigentypen erfordern jedoch eindeutige Workflows. Siehe Anweisungen zum Einrichten von [[!DNL Microsoft Advertising] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md), [[!DNL Google Ads] dynamischen Suchanzeigen](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md), [[!DNL Google Ads] Leistungsmax-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md) und [[!DNL Google Ads] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md).

   1. ([!DNL Naver] Nur-Tracking-Konten) Laden Sie [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) mit Daten hoch, um die vorhandenen Kampagnen, Anzeigengruppen und Suchbegriffe in Search, Social und Commerce zu replizieren, ohne sie in [!DNL Naver] zu veröffentlichen.

1. Richten Sie das Tracking für alle Anzeigen ein, für die Adobe Advertising Konversionen verfolgt:

   1. (Werbetreibende mit dem Adobe Advertising-Konversions-Tracking-Dienst) Richten Sie bei Bedarf [Klick-Tracking](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) für Anzeigen und optional für Suchbegriffe, Platzierungen und Anzeigenerweiterungen ein, indem Sie Such-, Social- und Commerce-Klick-Tracking-URLs generieren und hochladen.

      Richten Sie für Kampagnen mit der maximalen Leistung von [!DNL Google Ads] das gesamte Tracking in den Tracking-Einstellungen der [Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) ein.

1. Für reine Tracking-Kampagnen müssen Sie stattdessen Ziel-URLs mithilfe von Bulksheets generieren und dann die generierten Ziel-URLs mithilfe des nativen Editors des Werbenetzwerks zu den relevanten Entitäten hinzufügen.

   1. Einrichten des Konversions-Trackings. Abhängig von der Implementierung kann dies das Hinzufügen von Konversions-Tracking-Tags zu den Webseiten des Advertisers und/oder das Einrichten eines täglichen Feed-Drop für Konversionsdaten umfassen, die der Advertiser separat erfasst hat.

      Wenn Sie den Adobe Advertising-Konversions-Tracking-Dienst verwenden, können Sie Konversions-Tracking-Tags [in Search, Social und Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md) oder [mit Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html) generieren.

   1. Validieren Sie die getrackten Daten.

   Weitere Informationen zum Einrichten des Trackings finden Sie im Kapitel &quot;Tracking&quot;.

1. (Werbetreibende mit Adobe Analytics) [Integrieren Sie Adobe Advertising und Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html), damit sie Daten austauschen können.

1. (Damit Search, Social und Commerce Angebote, Kampagnenbudgets und/oder Kampagnenangebotsstrategieziele optimieren können; [Nur unterstützte Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md)) [Weisen Sie die Kampagne einem Portfolio zu](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Wenn das Portfolio noch nicht gestartet wurde (Optimierung von Angeboten und/oder Budgets), lassen Sie die Optimierungsfunktion genügend Daten sammeln, damit Kosten- und Umsatzmodelle erstellt werden können, damit Sie die Basisleistung für das Portfolio vor dem Start festlegen können.

   Wenn das Portfolio bereits gestartet ist, aktivieren Sie das Lernen für das Portfolio. Weitere Informationen finden Sie unter &quot;Anpassen der Portfoliostrategien&quot;. Sie sollten erwarten, dass das Portfolio nach dem Hinzufügen neuer Kampagnen schwankt, während die Optimierungsfunktion Daten zu den Gebotseinheiten der Kampagne erfasst. Das Angebot passt sich automatisch innerhalb von 1 bis 3 Wochen an.

   Weitere Informationen zu Portfolios finden Sie im Optimierungshandbuch, das in Search, Social und Commerce verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

1. (Wenn neue Konversionen für den Advertiser verfolgt werden) [Stellen Sie die Konversionen für Berichte, Kampagnenverwaltungsansichten und Portfolioziele zur Verfügung](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md).

1. Überprüfen Sie für jede Kampagne, ob Search, Social und Commerce Klick- und Kostendaten aus dem Werbenetzwerk erhalten, und validieren Sie die in Search, Social und Commerce angezeigten Umsatzdaten mit den eigenen Umsatzdaten des Werbetreibenden.

1. (Optional) Automatisieren Sie die Berichterstellung, indem Sie Berichtsvorlagen, Tabellenfeeds und FTP-Bereitstellung geplanter Berichte einrichten.

   Anweisungen finden Sie im Kapitel &quot;Berichte&quot;.

>[!MORELIKETHIS]
>
>* [Über die Kampagnenverwaltung in Search, Social und Commerce](campaign-management-about.md)
>* [Überwachen und Verwalten der Leistung Ihrer Werbenetzwerk-Kampagnen](monitor-performance-campaigns.md)
>* [Google Ads-Konversionsdaten in Search, Social und Commerce](google-conversion-data.md)
>* [Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)
