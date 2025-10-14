---
title: Übersicht über die Implementierung von Werbenetzwerkkonten und -kampagnen
description: Erfahren Sie mehr über die Aufgaben beim Einrichten, Synchronisieren und Verwalten Ihrer Anzeigennetzwerkkonten.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Übersicht über die Implementierung von Werbenetzwerkkonten und -kampagnen

Adobe arbeitet mit jedem Advertiser zusammen, um seine Anzeigennetzwerkkonten und -kampagnen einzurichten. Dazu gehört die Konfiguration von Search, Social und Commerce für die Verbindung und Synchronisierung mit den Konten des Advertisers, die Erstellung neuer Kampagnen und Kampagnenkomponenten nach Bedarf, die Einrichtung des Trackings für die Komponentenanzeigen, das optionale Hinzufügen der Kampagnen zu Portfolios, damit Search, Social und Commerce die Gebote für die Anzeigen optimieren können, und die Validierung der anfänglichen Kosten-, Klick- und Umsatzdaten.

Nachdem eine Kampagne aktiviert und optional einem Portfolio hinzugefügt wurde, müssen das Adobe-Kundenbetreuungsteam, das Agenturteam oder der Werbetreibende (je nach den Bedingungen der service level agreement) jede Kampagne überwachen und die entsprechenden Komponenten und Einstellungen nach Bedarf ändern, um die Ziele des Werbetreibenden zu erreichen.

Diese Seite enthält Informationen zu allen Kontotypen, einschließlich der Einrichtung der Kampagnenstruktur für synchronisierte Konten. Weitere Anweisungen zum Einrichten von Nur-Tracking-Konten für [!DNL Naver] finden Sie unter [Implementieren [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).

## Ersteinrichtung von Aufgaben für Konten und Kampagnen

[!DNL Adobe] und/oder Ihre Agentur werden mit Ihnen zusammenarbeiten, um Folgendes zu tun:

1. (Neue Advertiser-Konten) Einrichten von administrativen Konten:

   1. Richten Sie das Konto des Werbetreibenden ein.

   1. (Falls erforderlich) Erstellen Sie Benutzerkonten für den Advertiser, um seine Kampagnendaten anzuzeigen und zu verwalten und Berichte zu generieren.

1. (Einige Werbenetzwerke) Erhalten Sie die Autorisierung für Search, Social und Commerce, um über die API des Werbenetzwerks und die Benutzeroberfläche für Search, Social und Commerce auf jedes Konto zuzugreifen.

1. Für jedes Anzeigennetzwerkkonto:

   1. (Falls erforderlich) Richten Sie das Konto im Werbenetzwerk ein.

   1. Integrieren Sie ihn mit dem Konto[&#x200B; indem Sie in Search, Social &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) Commerce einen entsprechenden Kontodatensatz erstellen, der die Anmeldedaten für den Kontozugriff und Tracking-Optionen enthält, und setzen Sie den Kontostatus auf „Aktiviert“.

      Search, Social und Commerce werden dann mit dem Werbenetzwerk synchronisiert. Wenn das Konto bereits Kampagnendaten enthält, stehen die Daten in etwa 24 Stunden zur Verfügung.

   1. ([Anzeigentypen, die Sie erstellen/bearbeiten können](/help/search-social-commerce/introduction/supported-inventory.md) in „Suche“, „Social“ und &quot;Commerce„) Wenn das Konto noch keine Kampagnendaten enthält, erstellen Sie die Kampagnenstruktur und die Kampagnenkomponenten aus „Suche“, „Social“ und &quot;Commerce&quot;, indem Sie eine der folgenden Methoden verwenden, die für den Anzeigentyp verfügbar sind:

      * (Google Ads, Microsoft Advertising, Yahoo! Nur Anzeigen und Yandex-Konten) Richten Sie einen [automatisierten Prozess ein, um dynamische Anzeigen und Keywords zu erstellen, die auf jedes Element in Ihrem Inventar ausgerichtet sind](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) entsprechend einer von Ihnen erstellten netzwerkspezifischen Anzeigenvorlage und dem Inhalt der Inventardatendateien, die Sie an einen FTP-Speicherort hochladen.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! (Nur japanische Anzeigen und Yandex-Konten) Hochladen [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) die so viele Daten enthalten, wie Sie für ein Konto benötigen, und diese dann in die Werbenetzwerke posten.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads, und nur Yandex-Konten) Geben Sie Daten für einzelne Komponenten direkt in die Benutzeroberfläche ein. Für die meisten Kampagnen- und Anzeigentypen können Daten auf Kampagnenebene, Anzeigengruppenebene sowie auf Ebene einzelner Keywords, Platzierungen und Anzeigen erstellt werden.

      Einige Kampagnen- und Anzeigetypen erfordern jedoch eindeutige Workflows. Siehe Anweisungen zum Einrichten [[!DNL Microsoft Advertising] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md), [[!DNL Google Ads] dynamische Suchanzeigen](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md), [[!DNL Google Ads] Performance Max-](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md) und [[!DNL Google Ads] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md).

   1. (Nur [!DNL Naver]-Tracking-Konten) Laden Sie [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) mit Daten hoch, um die bestehenden Kampagnen, Anzeigengruppen und Keywords in Search, Social und Commerce zu replizieren, ohne sie an [!DNL Naver] zu senden.

1. Richten Sie das Tracking für alle Anzeigen ein, für die Adobe Advertising Konversionen verfolgt:

   1. (Werbetreibende mit dem Adobe Advertising-Konversions-Tracking-Service) Richten Sie bei Bedarf [Klick-Tracking ein](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) für Anzeigen und optional für Keywords, Platzierungen und Anzeigenerweiterungen ein, indem Sie Klick-Tracking-URLs für Search, Social und Commerce generieren und hochladen.

      Richten Sie für Kampagnen mit dem [!DNL Google Ads] „Performance Max“ das gesamte Tracking in den [Tracking-Einstellungen der Kampagne) &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Für Kampagnen, die nur das Tracking betreffen, müssen Sie stattdessen Ziel-URLs mithilfe von Bulksheets generieren und dann die generierten Ziel-URLs mithilfe des nativen Editors des Anzeigennetzwerks zu den relevanten Entitäten hinzufügen.

   1. Konversionsverfolgung einrichten. Je nach Implementierung kann dies das Hinzufügen von Konversionsverfolgungs-Tags zu den Web-Seiten des Werbetreibenden und/oder die Einrichtung einer täglichen Feed-Drop für Konversionsdaten beinhalten, die der Werbetreibende separat erfasst hat.

      Wenn Sie den Konversionsverfolgungs-Service von Adobe Advertising verwenden, können Sie Konversionsverfolgungstags (in [, Social und Commerce) oder &#x200B;](/help/search-social-commerce/tools/conversion-tag-generate.md)mithilfe von [Adobe Experience Platform) &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html?lang=de).

   1. Validieren Sie die nachverfolgten Daten.

   Weitere Informationen zum Einrichten des Trackings finden Sie im Kapitel „Tracking“.

1. (Werbetreibende mit Adobe Analytics) [Integrieren von Adobe Advertising und &#x200B;](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=de), damit sie Daten austauschen können.

1. (Damit Search, Social und Commerce Angebote, Kampagnenbudgets und/oder Bid-Strategie-Ziele für Kampagnen optimieren können (nur [&#x200B; unterstützte Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md)) [Die Kampagne einem Portfolio zuweisen](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Wenn das Portfolio noch nicht gestartet wurde (Gebote und/oder Budgets optimieren), lassen Sie die Optimierungsfunktion genügend Daten sammeln, damit sie Kosten- und Umsatzmodelle erstellen kann, damit Sie die Grundleistung für das Portfolio vor dem Start ermitteln können.

   Wenn das Portfolio bereits gestartet wurde, aktivieren Sie das Lernprogramm für das Portfolio. Weitere Informationen finden Sie unter „Anpassung der Portfoliostrategien“. Nach dem Hinzufügen neuer Kampagnen sollte das Portfolio als volatil eingestuft werden, während die Optimierungsfunktion Daten zu den Bid-Einheiten der Kampagne erfasst. Gebote werden automatisch innerhalb von ein bis drei Wochen angepasst.

   Weitere Informationen zu Portfolios finden Sie im Optimierungshandbuch, das bei Search, Social und Commerce verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

1. (Wenn neue Konversionen für den Advertiser verfolgt werden) [Verfügbarmachen der Konversionen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) für Berichte, Kampagnenverwaltungsansichten und Portfolioziele.

1. Überprüfen Sie für jede Kampagne, ob Search, Social und Commerce Klick- und Kostendaten vom Anzeigennetzwerk erhält, und validieren Sie die in Search, Social und Commerce angezeigten Umsatzdaten mit den eigenen Umsatzdaten des Werbetreibenden.

1. (Optional) Automatisieren Sie das Reporting, indem Sie Berichtsvorlagen, Tabellen-Feeds und FTP-Bereitstellung geplanter Berichte einrichten.

   Anweisungen finden Sie im Kapitel „Berichte“.

>[!MORELIKETHIS]
>
>* [Über die Kampagnenverwaltung in Search, Social und Commerce](campaign-management-about.md)
>* [Überwachen und Verwalten der Leistung Ihrer Werbenetzwerk-Kampagnen](monitor-performance-campaigns.md)
>* [Google Ads-Konversionsdaten in Search, Social und Commerce](google-conversion-data.md)
>* [Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)
