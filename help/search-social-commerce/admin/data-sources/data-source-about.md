---
title: Über Synchronisierungs [!DNL Google Analytics] Konversionsmetriken
description: Erfahren Sie mehr über  [!DNL Google Analytics] -/Konversionsmetriken für Optimierung und Reporting.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Über das Synchronisieren [!DNL Google Analytics] Konversionsmetriken

Search, Social und Commerce können Konversionsmetriken für ein bestimmtes [!DNL Google Analytics] Konto, eine bestimmte Eigenschaft und eine bestimmte Ansichtskombination synchronisieren, um Optimierungen und Berichte zu ermöglichen. [Seitenansichten](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sitzungen](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Absprungrate](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (berechnet als Absprünge/Sitzungen) und [Sitzungsdauer](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) werden automatisch einbezogen. Sie können bis zu 16 zusätzliche Metriken pro Datenquelle einbeziehen.

>[!NOTE]
>
>Advertising DSP-Benutzer können die Konversionsmetriken als benutzerdefinierte Ziele und in Berichten verwenden.

Die gesamte API-Nutzung für die Datenübertragungen wird zu einem Projekt im entsprechenden [!DNL Google Analytics]-Konto bewertet. Sie können Ihre Kontingente für dieses Projekt in [der [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas) anzeigen. Weitere Informationen zu ([&#x200B; und Aufrufbeschränkungen für Reporting-API-Anfragen](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas) finden Sie in [!DNL Google Analytics] Dokumentation.

Die folgenden Schritte beschreiben den Prozess zum Synchronisieren von Konvertierungsdaten aus [!DNL Google Analytics].

1. [Ausführen der erforderlichen Aufgaben](data-source-prerequisites.md)

   * Implementieren Sie ein Adobe Advertising-Token (`ef_id` Abfragezeichenfolgenparameter) in den Landingpage-URLs für alle anwendbaren Werbekonten.

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
