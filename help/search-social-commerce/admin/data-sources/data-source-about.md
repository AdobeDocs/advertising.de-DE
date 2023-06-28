---
title: Über die Synchronisierung [!DNL Google Analytics] Konversionsmetriken
description: Informationen zur Synchronisierung [!DNL Google Analytics] Konversionsmetriken zur Optimierung und Berichterstellung.
role: User, Admin
exl-id: 0c263ced-3774-4d4b-9d61-65289cd74027
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Über die Synchronisierung [!DNL Google Analytics] Konversionsmetriken

Search, Social und Commerce können Konversionsmetriken für eine bestimmte [!DNL Google Analytics] Kombination aus Konto, Eigenschaft und Ansicht zur Optimierung und Berichterstellung. [Seitenansichten](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sitzungen](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Absprungrate](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (berechnet als Absprünge/Sitzungen) und [Sitzungsdauer](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) automatisch einbezogen werden. Sie können bis zu 16 zusätzliche Metriken pro Datenquelle einbeziehen.

>[!NOTE]
>
>Benutzer von Advertising DSP können die Konversionsmetriken als benutzerdefinierte Ziele und in Berichten verwenden.

Die gesamte API-Nutzung für Datenübertragungen wird an ein Projekt in den entsprechenden [!DNL Google Analytics] -Konto. Ihre Quoten für dieses Projekt finden Sie unter [die [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Siehe [!DNL Google Analytics] Dokumentation für weitere Informationen zu [Quoten und Anrufbeschränkungen für API-Anfragen zur Berichterstellung](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

Die folgenden Schritte beschreiben den Prozess der Synchronisierung von Konversionsdaten aus [!DNL Google Analytics].

1. [Führen Sie die erforderlichen Aufgaben aus.](data-source-prerequisites.md)

   * Implementieren eines Adobe Advertising-Tokens (`ef_id` -Abfragezeichenfolgen-Parameter) in den Landingpage-URLs für alle zutreffenden Werbekonten.

   * Erfassen Sie das Adobe Advertising-Token (`ef_id` Abfragezeichenfolgenparameter) in einer [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Kontoverwalter der Agentur, Kontoverwalter der Agentur, [!DNL Adobe] Kundenbetreuer und nur Administrator-Benutzer) [Erstellen einer Datenquelle pro [!DNL Google Analytics] Kombination aus Konto, Eigenschaft und Ansicht](data-source-configure.md).

   Um Metriken für mehrere Eigenschaften oder für mehrere Ansichten für eine einzelne Eigenschaft zu integrieren, richten Sie für jede Eigenschaft eine separate Datenquelle ein.

   Sobald eine Datenquelle konfiguriert ist, ruft Search, Social und Commerce täglich Daten ab, beginnend um 5:00 Uhr in der Zeitzone des Advertisers. Sobald die Metriken verfügbar sind, können Sie sie in Kampagnen- und Portfoliomanagementansichten sowie in Berichten einbeziehen und sie bei Bedarf in Optimierungszielen verwenden.

>[!MORELIKETHIS]
>
>* [Voraussetzungen für die Konfiguration einer [!DNL Google Analytics] Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren Sie eine [!DNL Google Analytics] als Datenquelle anzeigen](data-source-configure.md)
>* [Bearbeiten von [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren eines [!DNL Google Analytics] Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbar [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
