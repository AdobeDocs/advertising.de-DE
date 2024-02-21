---
title: Arten von Leistungsberichten in Campaign Management-Ansichten
description: Erfahren Sie mehr über die Berichtsdaten in den Kampagnenverwaltungsansichten.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: c7860d98edbf44b71d97c3800edf47a409606b74
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Arten von Leistungsberichten in Campaign Management-Ansichten

Die Ansichten der Kampagnenverwaltung beinhalten umfassende Berichtdaten. Die verfügbaren Berichte helfen Ihnen dabei, die Pakete und Platzierungen zu identifizieren, die eine gute Leistung erbringen, und jene, die Ihre Aufmerksamkeit benötigen. Schnellaktion-Schaltflächen machen Sie auch produktiver.

## Ansicht aller Kampagnen

Die [!UICONTROL Campaigns] -Ansicht öffnet sich eine Reihe von Leistungsdatendiagrammen und eine Liste aller Kampagnen in Ihrem Konto.

### Diagrammansicht {#chart-view}

Sie können [Trend-Diagramme für Zeitreihen anpassen](campaign-data-views-manage.md#data-visualizations-manage) über alle Kampagnen mit drei Metriken hinweg. Standardmäßig werden Daten für [!UICONTROL Net Spend], [!UICONTROL Impressions], und [!UICONTROL Net CPM] sind in separaten Diagrammen (Trellis-Diagrammen) enthalten. Sie können die Metriken optional ändern. Um stündliche Daten in Trend-Diagrammen für Zeitreihen zu aktivieren, ändern Sie Ihre Datumsauswahl auf einen einzelnen Tag ([!UICONTROL Today], [!UICONTROL Yesterday]oder einen bestimmten Tag).

![Trends für drei Metriken trennen](/help/dsp/assets/trend-chart-separate.png)

Sie können die drei Metriken optional auch überlagern, um Anomalien und Bereiche zu erkennen, in denen Skalierung oder Leistung verbessert werden können.

![Trenddiagramm mit Überlagerung](/help/dsp/assets/trend-chart.png)

### Tabellenansicht

![Kampagnenliste](/help/dsp/assets/campaigns-list.png)

Standardmäßig enthält jede Kampagnenzeile die Geschwindigkeit und Versandmetriken. Schrittmetriken beinhalten [!UICONTROL Gross Spend (Lifetime)], das eine Messung der tatsächlichen On-Target-Ausgaben im Vergleich zu den erwarteten On-Target-Ausgaben für alle Kampagnenkits enthält, sodass Sie leistungsschwache Kampagnen auf einen Blick erkennen können. Sie können optional [Spaltenansicht ändern](campaign-data-views-manage.md#column-view-change) oder sogar [Erstellen einer benutzerdefinierten Spaltenansicht](campaign-data-views-manage.md#column-view-create).

Sie können [Datentabellen anpassen](campaign-data-views-manage.md#data-tables-manage) auf zusätzliche Weise und [die sichtbaren Daten filtern](campaign-data-views-manage.md#filter-data-tables).

Um eine Kampagne detaillierter anzuzeigen, klicken Sie auf den Kampagnennamen.

#### Warnhinweise

*Beta-Funktion*

Ein &quot;[!UICONTROL Alerts]&quot; zeigt an, wenn eine Kampagne oder eine untergeordnete Entität darunter ein Problem hat. A [!UICONTROL Pulse Panel] rechts neben der Symbolleiste zeigt auch an, ob Warnhinweise für die aufgelisteten Entitäten verfügbar sind. Siehe &quot;[Warnhinweise anzeigen](campaign-alerts.md)&quot; für weitere Informationen.

## Berichterstellung für einzelne Kampagnen {#single-campaign-reporting}

Innerhalb einer Kampagne können Daten nach Kampagnenentität gefiltert werden: [!UICONTROL Packages], [!UICONTROL Placements], und [!UICONTROL Ads]. Sie können [die sichtbaren Daten filtern](campaign-data-views-manage.md#filter-data-tables) , um nur die Pakete, Platzierungen oder Anzeigen einzuschließen, die Sie sehen möchten.

![Tabs zur Kampagnenentität](/help/dsp/assets/campaign-subtabs.png)

### Diagrammansicht

Für jede Kampagne können Sie [Trend-Diagramme für Zeitreihen anpassen](campaign-data-views-manage.md#data-visualizations-manage) mit drei Metriken, die in jeder Entitätsansicht verfügbar sind. Dieselben Metriken bleiben für alle Trenddiagramme der Kampagne erhalten.

Siehe [Abschnitt &quot;Diagrammansicht&quot;zu kampagnenübergreifenden Metriken](#chart-view) für weitere Informationen.

### Tabellenansicht

In jeder Entitäts-Registerkarte enthält jede Zeile standardmäßig Pacing- und Versandmetriken. Sie können jedoch [Spaltenansicht ändern](campaign-data-views-manage.md#column-view-change) oder sogar [Erstellen einer benutzerdefinierten Spaltenansicht](campaign-data-views-manage.md#column-view-create) auf alle Unterregisterkarten der Kampagne anwenden. Sie können [Datentabellen anpassen](campaign-data-views-manage.md#data-tables-manage) auf zusätzliche Weise. Jede Datentabelle enthält eine [!UICONTROL Subtotals] -Zeile, die entweder die Summe oder den Durchschnittswert jeder Metrik über alle sichtbaren Zeilen hinweg anzeigt.

#### Warnhinweise

*Beta-Funktion*

Ein &quot;[!UICONTROL Alerts]&quot; gibt an, wann ein Paket, eine Platzierung oder eine Anzeige - oder eine untergeordnete Entität unter einem Paket oder einer Platzierung - ein Problem hat. Ein &quot;[!UICONTROL Alerts]&quot; zeigt an, wenn eine Kampagne oder eine untergeordnete Entität darunter ein Problem hat. A [!UICONTROL Pulse Panel] rechts neben der Symbolleiste zeigt auch an, ob Warnhinweise für die aufgelisteten Entitäten verfügbar sind. Siehe &quot;[Warnhinweise anzeigen](campaign-alerts.md)&quot; für weitere Informationen.

### Sonstige Berichtstypen auf Kampagnenebene

Für andere Datenaufschlüsselungen anzeigen [Berichtsseiten auf Kampagnenebene](/help/dsp/campaign-management/campaigns/campaign-view-report.md). Der Bericht enthält Abschnitte zu [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], und [!UICONTROL Audience Performance] Daten.

### Sonstige Berichtstypen auf Platzierungsebene

Für andere Datenaufschlüsselungen anzeigen [die Berichtsseiten auf Platzierungsebene](/help/dsp/campaign-management/placements/placement-view-report.md). Der Bericht enthält Abschnitte zu [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications], und [!UICONTROL Ads] Daten.

Darüber hinaus können Sie die folgenden Daten in den Platzierungseinstellungen anzeigen:

* [A (Detailansicht) [!UICONTROL Inspector])](placement-details-view.md), der alle zielgerichteten Sites, Anzeigen, Frequenzdaten und Angebote für eine Platzierung anzeigt.

* A [Platzierungsvorhersagebericht](/help/dsp/campaign-management/reports/placement-forecast.md)

* [Platzierungsdiagnoseberichte](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Sonstige Berichtstypen auf Anzeigenebene

Für andere Datenaufschlüsselungen anzeigen [Berichterstellungsseiten auf Anzeigenebene](/help/dsp/campaign-management/ads/ad-view-report.md). Der Bericht enthält [!UICONTROL Overview], [!UICONTROL Geography], und [!UICONTROL Viewability] Daten.

>[!MORELIKETHIS]
>
>* [Anzeigen von Sites, Anzeigen und Frequenzdetails für eine Platzierung](placement-details-view.md)
>* [Datenansichten Ihrer Kampagne verwalten](campaign-data-views-manage.md)
>* [Daten aus einer Campaign Management-Ansicht exportieren](campaign-export-data.md)
>* [Detaillierte Berichte für eine Kampagne anzeigen](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Warnhinweise anzeigen](campaign-alerts.md)
