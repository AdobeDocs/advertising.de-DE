---
title: Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen
description: Erfahren Sie mehr über die Aufgaben beim Einrichten, Synchronisieren und Verwalten Ihrer Anzeigennetzwerkkonten.
exl-id: 401c5ebb-258c-4614-96e8-ca604fc698c0
feature: Search Campaign Management
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen

Adobe arbeitet mit jedem Advertiser zusammen, um seine Anzeigennetzwerkkonten und -kampagnen einzurichten. Dazu gehören die Konfiguration von Search, Social und Commerce zur Verbindung und Synchronisierung mit den Konten des Advertisers, die Erstellung neuer Kampagnen und Kampagnenkomponenten nach Bedarf, die Einrichtung des Trackings für die Komponentenanzeigen, optional das Hinzufügen der Kampagnen zu Portfolios, damit Search, Social und Commerce das Angebot für die Anzeigen optimieren können, und die Validierung der ursprünglichen Kosten-, Klick- und Umsatzdaten.

Nachdem eine Adobe aktiviert und optional einem Portfolio hinzugefügt wurde, muss das Kampagnenkontoverwaltungsteam, das Agenturteam oder der Werbetreibende (je nach den Bedingungen der Servicestufe-Vereinbarung) jede  überwachen und die relevanten Komponenten und Einstellungen entsprechend den Zielen des Werbetreibenden ändern.

Diese Seite enthält Informationen zu allen Kontotypen, einschließlich der Einrichtung der Kampagnenstruktur für synchronisierte Konten. Zusätzliche Anweisungen zum Einrichten von Nur-Tracking-Konten für [!DNL Naver], siehe[Implementierung [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

## Erste Einrichtungsaufgaben für Konten und Kampagnen

[!DNL Adobe] und/oder Ihre Agentur arbeitet mit Ihnen wie folgt zusammen:

1. (Neue Advertiser-Konten) Einrichten von Verwaltungskonten:

   1. Richten Sie das Konto des Werbetreibenden ein.

   1. (Bei Bedarf) Erstellen Sie Benutzerkonten für den Advertiser, um seine Kampagnendaten anzuzeigen und zu verwalten und Berichte zu erstellen.

1. (Einige Werbenetzwerke) Erhalten Sie eine Autorisierung für Search, Social und Commerce, um auf jedes Konto über die API des Anzeigennetzwerks und die Benutzeroberfläche für Suche, Social und Commerce zuzugreifen.

1. Für jedes Anzeigen-Netzwerk-Konto:

   1. (Bei Bedarf) Richten Sie das Konto im Werbenetzwerk ein.

   1. Integrieren Sie mit dem Konto von [Erstellen eines entsprechenden Kontodatensatzes](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) in &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;, die die Kontozugriffsberechtigungen und Tracking-Optionen enthalten, und legen Sie den Kontostatus auf aktiviert fest.

      Suchen, Social und Commerce synchronisiert dann mit dem Anzeigennetzwerk. Wenn das Konto bereits Kampagnendaten enthält, sind die Daten in etwa 24 Stunden verfügbar.

   1. ([Anzeigentypen, die Sie erstellen/bearbeiten können](/help/search-social-commerce/introduction/supported-inventory.md) in Search, Social, &amp; Commerce) Wenn das Konto noch keine Kampagnendaten enthält, erstellen Sie die Kampagnenstruktur und die Kampagnenkomponenten aus Search, Social und Commerce mit einer der folgenden Methoden, die für den Anzeigentyp verfügbar sind:

      * (Google Ads, Microsoft Advertising, Yahoo! Nur Anzeigen und Yandex-Konten) Richten Sie eine [automatisierter Prozess zum Erstellen dynamischer Anzeigen und Suchbegriffe, die auf jedes Element in Ihrem Bestand ausgerichtet sind](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) entsprechend einer von Ihnen erstellten Anzeigennetzwerkspezifischen Anzeigenvorlage und dem Inhalt der Lagerbestandsdatendateien, die Sie an einen FTP-Speicherort hochladen.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Nur Japan Ads- und Yandex-Konten) Hochladen [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) enthält so viele Daten wie Sie für ein Konto wünschen und sendet sie dann in die Werbenetzwerke.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads- und Yandex-Konten) Geben Sie Daten für einzelne Komponenten direkt in die Benutzeroberfläche ein. Für die meisten Kampagnen- und Anzeigentypen können Sie Daten auf Kampagnenebene, auf Anzeigengruppenebene sowie einzelne Suchbegriffe, Platzierungen und Anzeigenebenen erstellen.

      Einige Kampagnen- und Anzeigentypen erfordern jedoch eindeutige Workflows. Siehe Anweisungen zum Einrichten von [[!DNL Microsoft Advertising] Warenkorb](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md), [[!DNL Google Ads] dynamische Suchanzeigen](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md), [[!DNL Google Ads] Performance-Max-Kampagnen](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md), und [[!DNL Google Ads] Warenkorb](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] Nur Tracking-Konten) Hochladen [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) mit Daten zur Replikation der vorhandenen Kampagnen, Anzeigengruppen und Suchbegriffe in Search, Social und Commerce, ohne sie in posten zu müssen [!DNL Naver].

1. Richten Sie das Tracking für alle Anzeigen ein, für die der Adobe Advertising Konversionen verfolgt:

   1. (Advertiser mit dem Adobe Advertising-Konversions-Tracking-Dienst) Bei Bedarf, [Klick-Tracking einrichten](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) für Anzeigen und optional für Suchbegriffe, Platzierungen und Anzeigenerweiterungen durch Generieren und Hochladen von Such-, Social- und Commerce-Klick-Tracking-URLs.

      Für [!DNL Google Ads] Kampagnen mit maximaler Performance, Einrichten des gesamten Trackings im [Tracking-Einstellungen der Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Für reine Tracking-Kampagnen müssen Sie stattdessen Ziel-URLs mithilfe von Bulksheets generieren und dann die generierten Ziel-URLs mithilfe des nativen Editors des Werbenetzwerks zu den relevanten Entitäten hinzufügen.

   1. Einrichten des Konversions-Trackings. Abhängig von der Implementierung kann dies das Hinzufügen von Konversions-Tracking-Tags zu den Webseiten des Advertisers und/oder das Einrichten eines täglichen Feed-Drop für Konversionsdaten umfassen, die der Advertiser separat erfasst hat.

      Wenn Sie den Adobe Advertising-Konversions-Tracking-Dienst verwenden, können Sie Konversions-Tracking-Tags generieren [in Search, Social und Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md) oder [Verwenden von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. Validieren Sie die getrackten Daten.

   Weitere Informationen zum Einrichten des Trackings finden Sie im Kapitel &quot;Tracking&quot;.

1. (Werbetreibende mit Adobe Analytics) [Integration von Adobe Advertising und Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) damit sie Daten austauschen können.

1. (Damit Search, Social und Commerce Angebote und/oder Kampagnenbudgets optimieren können; [unterstützte Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) nur) [Zuweisen der Kampagne zu einem Portfolio](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Wenn das Portfolio noch nicht gestartet wurde (Optimierung von Angeboten und/oder Budgets), lassen Sie die Optimierungsfunktion genügend Daten sammeln, damit Kosten- und Umsatzmodelle erstellt werden können, damit Sie die Basisleistung für das Portfolio vor dem Start festlegen können.

   Wenn das Portfolio bereits gestartet ist, aktivieren Sie das Lernen für das Portfolio. Weitere Informationen finden Sie unter &quot;Anpassen der Portfoliostrategien&quot;. Sie sollten erwarten, dass das Portfolio nach dem Hinzufügen neuer Kampagnen schwankt, während die Optimierungsfunktion Daten zu den Gebotseinheiten der Kampagne erfasst. Das Angebot passt sich automatisch innerhalb von 1 bis 3 Wochen an.

   Weitere Informationen zu Portfolios finden Sie im Optimierungshandbuch, das in Search, Social und Commerce verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

1. (Wenn neue Konversionen für den Advertiser verfolgt werden) [Verfügbar machen von Konvertierungen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) für Berichte, Kampagnenverwaltungsansichten und Portfolioziele.

1. Stellen Sie für jede Kampagne sicher, dass Search, Social und Commerce Klicks- und Kostendaten aus dem Werbenetzwerk erhalten, und validieren Sie die in Search, Social und Commerce angezeigten Umsatzdaten mit den eigenen Umsatzdaten des Werbetreibenden.

1. (Optional) Automatisieren Sie die Berichterstellung, indem Sie Berichtsvorlagen, Tabellenfeeds und FTP-Bereitstellung geplanter Berichte einrichten.

   Anweisungen finden Sie im Kapitel &quot;Berichte&quot;.

>[!MORELIKETHIS]
>
>* [Über die Kampagnenverwaltung in Search, Social und Commerce](campaign-management-about.md)
>* [Überwachen und verwalten Sie die Leistung Ihrer Werbenetzwerk-Kampagnen.](monitor-performance-campaigns.md)
>* [Google Ads-Konversionsdaten in Search, Social und Commerce](google-conversion-data.md)
>* [Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)
