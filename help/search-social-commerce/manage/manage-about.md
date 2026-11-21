---
title: Über die Verwaltung von Kampagnen und Portfolios
description: Erfahren Sie, wie Werbenetzwerkkonten, Kampagnen, Tracking und Portfoliooptimierung zusammenarbeiten und wie Sie die Leistung überwachen und verbessern können.
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# Über die Verwaltung von Kampagnen und Portfolios

*Beta-Funktion*

Search, Social und Commerce bieten Kampagnenverwaltung, Leistungsberichte und Portfoliooptimierung in einer einzigen Oberfläche. Je nach Anzeigennetzwerk und Kampagnentyp können Sie Kampagnendaten synchronisieren, Kampagnenkomponenten erstellen und bearbeiten, Konversionen verfolgen und Gebote, Budgets oder Bid-Strategieziele optimieren. Unter [Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md) finden Sie die für jedes Werbenetzwerk verfügbaren Funktionen.

Das Menü [!UICONTROL Manage] bietet Zugriff auf Ihre Konten, Kampagnen, Anzeigengruppen, Anzeigen, Keywords, Produktgruppen und Portfolios. Ihre Berechtigungen bestimmen, welche Ansichten und Aktionen verfügbar sind. Die vollständige Menüorganisation finden Sie unter &quot;[&#x200B; der Benutzeroberfläche](/help/search-social-commerce/getting-started/user-interface.md).

## So passen Konten, Kampagnen und Portfolios zusammen

* **Anzeigen-**: Verbinden Sie die Daten Ihres Advertisers mit Search, Social und Commerce. [Kontotypen](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) beinhalten über eine API-Verbindung synchronisierte Konten, Konten, für die Sie Daten hochladen, und vorlagenbasierte Tracking-Konten. Der Kontotyp bestimmt, ob Sie Daten synchronisieren, Kampagnen verwalten oder die Portfoliooptimierung verwenden können.

* **Kampagnen** enthalten die Anzeigen und andere Komponenten, die für die Bereitstellung Ihrer Werbung verwendet werden. Für unterstützte Kampagnentypen können Sie [Erstellen und Verwalten von Kampagnen](/help/search-social-commerce/manage/campaigns/campaign-manage.md) und deren Komponenten über die [!UICONTROL Manage] Ansichten erstellen. Sie können auch [Bulksheets](/help/search-social-commerce/set-up/bulksheets/about.md) für unterstützte Massenvorgänge verwenden.

* **Portfolios** Gruppieren Sie geeignete Kampagnen, um sie auf ein gemeinsames Geschäftsziel und ein gemeinsames Budget oder Leistungsziel hin zu optimieren. Eine Kampagne kann nur zu einem Portfolio gehören und alle Kampagnen in einem Portfolio müssen dieselbe Währung verwenden. Siehe &quot;[&#x200B; Portfolios](/help/search-social-commerce/manage/portfolios/portfolio-about.md).

Die Zuweisung von Portfolio ist optional. Sie können Kampagnen verfolgen und Berichte dazu erstellen, ohne sie einem Portfolio zuzuweisen. Nicht alle Werbenetzwerke, Kampagnentypen oder Bid-Strategien unterstützen die Portfoliooptimierung.

## Kampagnendaten synchronisieren

Für -Konten, die über eine API verbunden sind, ruft Search, Social und Commerce unterstützte Kampagnenstruktur- und Leistungsdaten aus dem Werbenetzwerk ab. Änderungen, die Sie an unterstützten Kampagnenkomponenten in Search, Social und Commerce vornehmen, werden an das Werbenetzwerk gesendet.

Bei Bedarf können Sie [eine manuelle Synchronisierung anfordern](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md). Wenn ein Konto nicht mehr synchronisiert wird, überprüfen Sie [Authentifizierung und Zugriffsstatus](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status).

Daten-Upload-Konten und Nur-Tracking-Konten werden nicht mit dem Werbenetzwerk synchronisiert. Befolgen Sie den Workflow für den [Kontotyp](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) um Kampagnen- und Leistungsdaten bereitzustellen.

## Einrichten von Tracking und Optimierung

[Tracking](/help/search-social-commerce/tracking/tracking-about.md) verbindet Kampagnenaktivität mit den Konversionen, die für Ihr Unternehmen wichtig sind. Je nach Implementierung können Konversionsdaten aus Adobe Advertising-Tags, einer Adobe Analytics-Integration, dem Anzeigen-Netzwerk-Tracking oder Daten-Feeds stammen. Konfigurieren Sie das Klick-Tracking und das Konversions-Tracking nach Bedarf für Ihre Implementierung und validieren Sie die Daten, bevor Sie sie zur Optimierung verwenden.

In [!UICONTROL Goals] > [!UICONTROL Conversions] können Sie die Konversionsmetriken [, die für den Advertiser verfolgt werden, und ihre Sichtbarkeit &#x200B;](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md). Verwenden Sie die entsprechenden Metriken in Ihren [Zielen](/help/search-social-commerce/goals/objectives/objective-about.md).

Um die Portfoliooptimierung zu aktivieren[&#x200B; erstellen Sie ein Portfolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md) weisen Sie eine objektive und geeignete Kampagne zu und konfigurieren Sie deren Ausgaben- und Optimierungseinstellungen. Ein aktives Portfolio sammelt und modelliert Leistungsdaten. Wenn die Daten und Einstellungen fertig sind, [&#x200B; Sie den Portfoliostatus auf „Optimiert“, &#x200B;](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) mit der Optimierung zu beginnen. Die durchgeführten Aktionen hängen vom Portfoliotyp und den [Kampagnenangebotstrategien](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy) ab.

Eine detaillierte Einrichtungssequenz finden Sie unter &quot;[&#x200B; von Werbenetzwerkkonten und -kampagnen](/help/search-social-commerce/getting-started/campaign-implementation-overview.md).

## Überwachen der Kampagnen- und Portfolioleistung {#monitor-performance}

Das Account-Team, die Agentur oder der Advertiser ist für die Überwachung der Leistung und die Vornahme von Anpassungen gemäß den Bedingungen der Service-Vereinbarung verantwortlich. Routinemäßig:

* Überprüfen Sie die Kampagnen- und Kontoleistung in den [!UICONTROL Manage]. [Anpassen von Spalten, Filtern und Datumsbereichen](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) um den Fokus auf die wichtigen Metriken und Entitäten zu legen.

* Verwenden Sie [!UICONTROL Dashboard] > [!UICONTROL Overview], [&#x200B; Portfoliotrends und Leistungsänderungen zu &#x200B;](/help/search-social-commerce/dashboard/dashboard-overview.md).

* Prüfen Sie [benutzerdefinierte Warnhinweise](/help/search-social-commerce/common-tasks/alerts-manage.md) auf Bedingungen, die eine Untersuchung erfordern.

* [Berichte &#x200B;](/help/search-social-commerce/reports/management/report-manage.md) Kampagnen-, Keyword-, Anzeigen- und Portfolioleistung generieren. Überprüfen Sie für Portfolios [Leistungsdetails](/help/search-social-commerce/manage/portfolios/portfolio-details.md) einschließlich der tatsächlichen Leistung und Modellgenauigkeit.

* Verwenden [Simulationen](/help/search-social-commerce/plan/simulations/simulation-about.md) falls verfügbar, um die vorhergesagten Auswirkungen verschiedener Ausgabenniveaus zu bewerten.

* Untersuchen Sie die Unterschiede zwischen den gemeldeten Konversionen und den Quelldaten. Weitere Informationen finden Sie in der Anleitung zum [!DNL Google Ads] und [!DNL Microsoft Advertising] von Konversionsdaten unter den entsprechenden Links.

## Anpassen von Kampagnen und Portfolios

Je nach Leistung und Änderungen Ihrer Geschäftsziele müssen Sie möglicherweise Folgendes tun:

* Kampagneneinstellungen bearbeiten, Kampagnenkomponenten erstellen oder anhalten, Keyword-Sets verfeinern oder verschiedene Anzeigen testen. Die verfügbaren Aktionen hängen vom Anzeigennetzwerk und Kampagnentyp ab.

* Überprüfen Sie die geografische Ausrichtung, die Zielgruppe und die Platzierung mithilfe der entsprechenden Managementansichten und -berichte.

* [Ändern von Kampagnenzuweisungen](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) wenn eine Kampagne mit einem anderen Portfolio optimiert werden soll. Wenn Sie eine Kampagne einem anderen Portfolio zuweisen, wird sie aus dem vorherigen Portfolio entfernt.

* [Bearbeiten Sie &#x200B;](/help/search-social-commerce/manage/portfolios/portfolio-edit.md) Portfolioeinstellungen, einschließlich Ziel, Ausgabenstrategie, Einschränkungen oder Optimierungskontrollen, je nach Ihrem Produktprofil.

* Überprüfen Sie [Änderungsverlauf](/help/search-social-commerce/reports/history-logs.md), wenn Sie Leistungsänderungen untersuchen.

>[!MORELIKETHIS]
>
>* [Einrichten von Netzwerkkonten und Kampagnen für Werbeanzeigen](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)
>* [[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
