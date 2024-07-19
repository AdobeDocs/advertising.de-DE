---
title: Über die Synchronisierung von [!DNL Google Analytics] Konversionsmetriken
description: Erfahren Sie mehr über die Synchronisierung von [!DNL Google Analytics] Konversionsmetriken für die Optimierung und Berichterstellung.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Über die Synchronisierung der [!DNL Google Analytics] Konversionsmetriken

In Search, Social und Commerce können Konversionsmetriken für ein bestimmtes [!DNL Google Analytics] -Konto, eine bestimmte Eigenschaft und eine bestimmte Ansichtskombination synchronisiert werden, um sie zu optimieren und Berichte zu erstellen. [Seitenansichten](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sitzungen](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Absprungrate](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (berechnet als Absprünge/Sitzungen) und [Sitzungsdauer](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) werden automatisch einbezogen. Sie können bis zu 16 zusätzliche Metriken pro Datenquelle einbeziehen.

>[!NOTE]
>
>Advertising DSP-Benutzer können die Konversionsmetriken als benutzerdefinierte Ziele und in Berichten verwenden.

Die gesamte API-Nutzung für die Datenübertragungen wird an ein Projekt im entsprechenden [!DNL Google Analytics]-Konto gemessen. Sie können Ihre Quoten für dieses Projekt in [dem  [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas) anzeigen. Weitere Informationen zu [Kontingenten und Anrufbeschränkungen für Reporting-API-Anfragen finden Sie in der Dokumentation zu [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas) .

Die folgenden Schritte beschreiben den Prozess zum Synchronisieren von Konversionsdaten von [!DNL Google Analytics].

1. [Führen Sie die erforderlichen Aufgaben aus.](data-source-prerequisites.md)

   * Implementieren Sie ein Adobe Advertising-Token (`ef_id` Abfragezeichenfolgenparameter) in die URLs der Landingpage für alle zutreffenden Werbekonten.

   * Erfassen Sie das Adobe Advertising-Token (`ef_id` Abfragezeichenfolgenparameter) in einem [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Nur für Agenturkontoadministrator, Agenturkontomanager, [!DNL Adobe] Kontomanager und Administratorbenutzer) [Erstellen Sie eine Datenquelle pro [!DNL Google Analytics] Konto-, Eigenschafts- und Ansichtskombination](data-source-configure.md).

   Um Metriken für mehrere Eigenschaften oder für mehrere Ansichten für eine einzelne Eigenschaft zu integrieren, richten Sie für jede Eigenschaft eine separate Datenquelle ein.

   Sobald eine Datenquelle konfiguriert ist, ruft Search, Social und Commerce täglich Daten ab, beginnend um 05:00 Uhr in der Zeitzone des Advertisers. Sobald die Metriken verfügbar sind, können Sie sie in Kampagnen- und Portfoliomanagementansichten sowie in Berichten einbeziehen und sie bei Bedarf in Optimierungszielen verwenden.

>[!MORELIKETHIS]
>
>* [Voraussetzungen für die Konfiguration einer  [!DNL Google Analytics] Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren einer [!DNL Google Analytics] Ansicht als Datenquelle](data-source-configure.md)
>* [Bearbeiten einer [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren einer  [!DNL Google Analytics] Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbare [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
