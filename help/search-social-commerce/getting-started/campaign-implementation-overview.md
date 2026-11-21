---
title: Einrichten von Werbenetzwerkkonten und -kampagnen
description: Befolgen Sie den Einrichtungs-Workflow für Anzeigennetzwerkverbindungen, Kampagnen, Tracking, Konversionsmetriken und optionale Portfoliooptimierung.
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%
---
# Einrichten von Werbenetzwerkkonten und -kampagnen

*Beta-Funktion*

[!DNL Adobe] und Ihre Agentur arbeiten mit Ihnen zusammen, um Ihre Werbenetzwerkkonten zu verbinden, Kampagnen vorzubereiten, das Tracking zu konfigurieren und Leistungsdaten zu validieren. Wenn Sie möchten, dass Search, Social und Commerce geeignete Kampagnen optimieren, umfasst der Workflow auch die Portfolioeinrichtung.

Diese Checkliste enthält die Konto- und Kampagnendetails für den größeren [-Workflow](implemention-overview.md). Die Aufgaben, die Sie ausführen können, hängen von Ihren Berechtigungen und der [Funktionalität ab, die für jedes Werbenetzwerk und jeden Kampagnentyp unterstützt wird](/help/search-social-commerce/introduction/supported-inventory.md).

## Workflow einrichten

1. **Bestätigen der Zugriffs- und Kontoanforderungen.**

   Arbeiten Sie mit Ihrem Administrator zusammen, um den Zugriff auf den entsprechenden Advertiser und die für Ihre Aufgaben erforderlichen Berechtigungen zu bestätigen. Siehe &quot;[Benutzerverwaltung für Suche, Social und Commerce](/help/search-social-commerce/user-administration.md)&quot;

   Erstellen Sie bei Bedarf das tatsächliche Konto im Werbenetzwerk auf der Website des Werbenetzwerks. Beim Erstellen eines Kontodatensatzes in Search, Social und Commerce wird kein Konto im Werbenetzwerk erstellt.

1. **Verbinden oder registrieren Sie jedes Anzeigennetzwerkkonto.**

   Verwenden Sie in [!UICONTROL Manage] > [!UICONTROL Accounts] den Workflow für den [Kontotyp](/help/search-social-commerce/manage/accounts/ad-network-account-about.md):

   * **API-Verbindung** [Kontodetails erstellen](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account), Netzwerkspezifische Authentifizierung abschließen, Tracking-Optionen konfigurieren und das Konto aktivieren. Überprüfen Sie [Authentifizierungs- und Zugriffsstatus](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status). Eine erfolgreiche Authentifizierung bedeutet nicht unbedingt, dass alle erforderlichen Berechtigungen erteilt wurden.

   * **Daten-Upload** [Kontodetails erstellen und Kampagnen- und Leistungsdaten hochladen](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md). Diese Konten werden nicht mit dem Anzeigennetzwerk synchronisiert und unterstützen keine Portfoliooptimierung.

   * Nur-Tracking **[!DNL Naver]:** Sie den [Tracking-Only-Konto-Workflow](/help/search-social-commerce/manage/accounts/template-account-manage.md). Verwenden Sie Bulksheets, um Tracking-URLs zu generieren und im Editor des Anzeigennetzwerks anzuwenden. Das Konto wird nicht synchronisiert oder unterstützt die Portfoliooptimierung.

1. **Kampagnenstruktur überprüfen oder erstellen.**

   Überprüfen Sie für Konten mit API-Verbindung die synchronisierten Kampagnen und ihre Komponenten. [Fordern Sie bei &#x200B;](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md) eine manuelle Synchronisierung an.

   Verwenden Sie für unterstützte Kampagnentypen [!UICONTROL Manage] > [!UICONTROL Campaigns] , um [Kampagnen zu erstellen oder zu bearbeiten](/help/search-social-commerce/manage/campaigns/campaign-manage.md). Erstellen Sie die erforderlichen [Anzeigengruppen](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md), [Anzeigen](/help/search-social-commerce/manage/ads/ad-manage.md) und andere unterstützte Komponenten. Sie können auch [Bulksheets](/help/search-social-commerce/set-up/bulksheets/about.md) für unterstützte Massenvorgänge verwenden.

   Schließen Sie vor der Aktivierung der Kampagnen alle erforderlichen netzwerkspezifischen Setups ab. Verwalten Sie nicht unterstützte Komponenten in der Benutzeroberfläche des Anzeigennetzwerks.

1. **Konfigurieren und Validieren des Trackings vor dem Start.**

   Wählen Sie die [Konversionsverfolgungsmethode](/help/search-social-commerce/tracking/conversion-tracking-about.md) aus, die Ihrer Implementierung entspricht. Falls erforderlich, [Generieren und Anwenden von Klick-Tracking](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)URLs und [Generieren von Konversionsverfolgungstags](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md).

   Konfigurieren Sie alle erforderlichen [Integrationen](/help/integrations/home.md) oder [Konversions-Feeds](/help/search-social-commerce/tracking/tracking-about.md) und überprüfen Sie, ob Konversionen erwartungsgemäß zugeordnet werden können. Wenden Sie bei Kampagnen, die nur das Tracking betreffen, die generierten Tracking-URLs im Editor des Werbenetzwerks an.

1. **Konversionsmetriken überprüfen.**

   Überprüfen Sie unter [!UICONTROL Goals] > [!UICONTROL Conversions] [die verfolgten Metriken und machen Sie die erforderlichen Metriken &#x200B;](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available) Verwaltungsansichten, Berichte und Ziele sichtbar. Ändern Sie bei Bedarf Anzeigenamen, um Metriken zu unterscheiden.

1. **(Optional) Portfoliooptimierung vorbereiten.**

   Vergewissern Sie sich, dass die Kampagnen und ihre Bid-Strategien [für die Portfoliooptimierung geeignet](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

   [Erstellen oder wählen Sie ein Ziel aus](/help/search-social-commerce/goals/objectives/objective-about.md) das die entsprechenden Konversionsmetriken verwendet. Erstellen Sie unter [!UICONTROL Manage] > [!UICONTROL Portfolios] [Portfolio erstellen](/help/search-social-commerce/manage/portfolios/portfolio-create.md) oder [bearbeiten Sie ein vorhandenes Portfolio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md) mit dem erforderlichen Ziel, der erforderlichen Ausgabenstrategie und den erforderlichen Optimierungseinstellungen.

   [Zuweisen der Kampagnen zum Portfolio](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). Jede Kampagne kann nur zu einem Portfolio gehören und alle Kampagnen in einem Portfolio müssen dieselbe Währung verwenden.

1. **Validieren von Kampagnendaten und Festlegen einer Leistungsgrundlinie.**

   Vergewissern Sie sich, dass für jede Kampagne Kosten-, Klick- und Konversionsdaten verfügbar sind. Konversionsdaten mit der entsprechenden Quelle, einschließlich [!DNL Google Ads] und ggf. [!DNL Microsoft Advertising], vergleichen. Verwenden Sie beim Vergleichen von Berichten konsistente Datumsbereiche und Attributionseinstellungen.

   Für ein neues Portfolio [&#x200B; Sie es &#x200B;](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), um Daten zu erfassen und zu modellieren. Überprüfen Sie die Daten- und Portfolioeinstellungen, bevor Sie die Optimierung aktivieren.

1. **(Optional) Portfoliooptimierung starten.**

   Wenn das Portfolio fertig ist, [ändern Sie seinen Status in optimiert](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) und überprüfen Sie die Voraussetzungen und Bestätigungsmeldungen. Search, Social und Commerce optimieren dann das Portfolio entsprechend den Einstellungen und den unterstützten Kampagnen-Bid-Strategien.

1. **Konfigurieren der fortlaufenden Überwachung und Berichterstellung.**

   [Datenansichten anpassen](/help/search-social-commerce/common-tasks/data-views/data-views-about.md), [benutzerdefinierte Warnhinweise einrichten](/help/search-social-commerce/common-tasks/alerts-manage.md) und [terminierte Berichte erstellen](/help/search-social-commerce/reports/management/report-manage.md). Automatisieren Sie bei Bedarf das Reporting mithilfe [Berichtsvorlagen](/help/search-social-commerce/reports/report-templates-manage.md) und [Tabellen-Feeds](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Fortsetzung der [Überwachung und Anpassung von Kampagnen und Portfolios](/help/search-social-commerce/manage/manage-about.md#monitor-performance) nach dem Start.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Search, Social und Commerce](implemention-overview.md)
>* [Über die Verwaltung von Kampagnen und Portfolios](/help/search-social-commerce/manage/manage-about.md)
>* [[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
