---
title: Über das Synchronisieren [!DNL Google Analytics] Konversionsmetriken
description: Erfahren Sie mehr über das Synchronisieren [!DNL Google Analytics] Konversionsmetriken für Optimierung und Reporting.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
TQID: 'https://experienceleague.adobe.com/dN7AVijGEiKM1o2iu3Fcb2D61pFkTguFOOu0qIe-mZk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 1003789d-7feb-5a2f-a02d-3182fd0ceb8a
    internal-label: Search Admin
  - id: 9bd4e165-792f-5324-bcaa-eee38dc8b8e9
    internal-label: Search Data Sources
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
    internal-label: Data sources
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: Admin
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: faa6de4fca9b018a704740bbdc3aa5369ee11721
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%
---
# Über das Synchronisieren [!DNL Google Analytics] Konversionsmetriken

Search, Social und Commerce können Konversionsmetriken für ein bestimmtes [!DNL Google Analytics] Konto, eine bestimmte Eigenschaft und eine bestimmte Ansichtskombination synchronisieren, um Optimierungen und Berichte zu ermöglichen. [Seitenansichten](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=page_tracking&jump=ga_pageviews), [Sitzungen](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessions), [Absprungrate](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_bouncerate) (berechnet als Absprünge/Sitzungen) und [Sitzungsdauer](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessionduration) werden automatisch einbezogen. Sie können bis zu 16 zusätzliche Metriken pro Datenquelle einbeziehen.

>[!NOTE]
>
>Advertising DSP-Benutzer können die Konversionsmetriken als benutzerdefinierte Ziele und in Berichten verwenden.

Die gesamte API-Nutzung für die Datenübertragungen wird zu einem Projekt im entsprechenden [!DNL Google Analytics]-Konto bewertet. Sie können Ihre Kontingente für dieses Projekt in [der [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas) anzeigen. Weitere Informationen zu ([ und Aufrufbeschränkungen für Reporting-API-Anfragen](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas) finden Sie in [!DNL Google Analytics] Dokumentation.

Die folgenden Schritte beschreiben den Prozess zum Synchronisieren von Konvertierungsdaten aus [!DNL Google Analytics].

1. [Ausführen der erforderlichen Aufgaben](data-source-prerequisites.md)

   * Implementieren Sie ein Adobe Advertising-Token (`ef_id` Abfragezeichenfolgenparameter) für alle anwendbaren Werbekonten in den Landingpage-URLs.

   * Erfassen Sie das Adobe Advertising-Token (`ef_id` Abfragezeichenfolgenparameter) in einem [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Nur für Agenturkonto-Administrator, Agenturkonto-Manager, [!DNL Adobe]-Konto-Manager und Admin-Benutzer) [Erstellen Sie eine Datenquelle pro  [!DNL Google Analytics] , Eigenschaft und Ansichtskombination](data-source-configure.md).

   Um Metriken für mehrere Eigenschaften oder für mehrere Ansichten für eine einzelne Eigenschaft zu integrieren, richten Sie für jede Eigenschaft eine separate Datenquelle ein.

   Sobald eine Datenquelle konfiguriert ist, ruft Search, Social und Commerce täglich ab 05:00 Uhr in der Zeitzone des Werbetreibenden Daten ab. Sobald die Metriken verfügbar sind, können Sie sie in Kampagnen- und Portfolio-Management-Ansichten und in Berichte einbeziehen und bei Bedarf für Optimierungsziele verwenden.

>[!MORELIKETHIS]
>
>* [Voraussetzungen für die Konfiguration  [!DNL Google Analytics]  Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren einer  [!DNL Google Analytics] -Ansicht als Datenquelle](data-source-configure.md)
>* [Datenquelle  [!DNL Google Analytics] bearbeiten](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren  [!DNL Google Analytics]  Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbare  [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
