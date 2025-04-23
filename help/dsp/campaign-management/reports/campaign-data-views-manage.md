---
title: Campaign-Datenansichten verwalten
description: Erfahren Sie, wie Sie Ihre Datenansichten für Kampagnen, Pakete, Platzierungen und Anzeigen anpassen können.
feature: DSP Campaign Data Views
exl-id: a22da10b-104d-4860-a23f-f2a6e59b637c
source-git-commit: 40cfd72c0f295ab1b6b7743828dded4032d435d4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Campaign-Datenansichten verwalten

Sie können die Daten anpassen, die in Ihren Ansichten zur Kampagnenverwaltung angezeigt werden ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] und [!UICONTROL Ads]).

## Verwalten von Datenvisualisierungen {#data-visualizations-manage}

Sie können die Metriken und den Diagrammmodus für alle Datenvisualisierungen in Kampagnen oder für eine einzelne Kampagne ändern. Änderungen an einer einzelnen Kampagne werden auf alle Datenvisualisierungen für die Kampagne angewendet, einschließlich der [!UICONTROL Packages]-, [!UICONTROL Placements]- und [!UICONTROL Ads].

### Ändern von Metriken für eine Datenvisualisierung

1. Klicken Sie oben rechts in der Datenvisualisierung auf ![Einstellungen](/help/dsp/assets/settings-chart.png).

1. Auswählen der Metriken.

   Sie können dieselbe Metrik nicht zweimal auswählen.

1. Klicken Sie auf **[!UICONTROL Apply]**.

### Ändern des Anzeigemodus für eine Datenvisualisierung

* Klicken Sie oben rechts in der Datenvisualisierung auf den [!UICONTROL Overlay] (![Überlagerungsschalter](/help/dsp/assets/overlay.png)), um zwischen dem Überlagerungsmodus (alle Diagramme überlagert) und dem Gitterdiagrammmodus (drei separate Diagramme) zu wechseln.

## Verwalten von Datentabellen {#data-tables-manage}

In allen Ansichten für das Kampagnen-Management ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] und [!UICONTROL Ads]) können Sie die Daten anpassen, die in der Datentabelle angezeigt werden.

### Spaltenansichten verwalten {#column-views-manage}

Jede Kampagnenverwaltungsebene ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] und [!UICONTROL Ads]) enthält integrierte [!UICONTROL Pacing] und [!UICONTROL Performance], die relevante Metriken für diese Entität enthalten. Standardmäßig wird die [!UICONTROL Pacing] angezeigt, damit Sie leistungsschwache Kampagnen und Kampagnenkomponenten auf einen Blick erkennen können. Optional können Sie benutzerdefinierte Spaltensätze erstellen und bearbeiten.

![Spaltenansichtsauswahl](/help/dsp/assets/column-view-selector.png)

DSP speichert Ihre letzte Ansicht als Standardansicht, sodass Sie immer dann, wenn Sie zur Seite zurückkehren, die für Sie relevanten Metriken anzeigen.

#### Spaltenansicht ändern {#column-view-change}

* Klicken Sie in der Ansichtsauswahl auf ![Abwärtspfeil](/help/dsp/assets/chevron-down.png) und klicken Sie dann auf den Namen der gewünschten Spaltenansicht.

#### Erstellen einer benutzerdefinierten Spaltenansicht {#column-view-create}

1. Klicken Sie in der Ansichtsauswahl auf ![Abwärtspfeil](/help/dsp/assets/chevron-down.png) und dann auf **[!UICONTROL Create View]**.

1. Geben Sie die Metriken an, die in die Ansicht aufgenommen werden sollen:

   1. Aktivieren Sie in der Liste der verfügbaren Metriken das Kontrollkästchen neben den einzelnen einzuschließenden Metriken.

      Alle Metriken sind alphabetisch nach Kategorie geordnet: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (Standardmetriken, die DSP verfolgt), [!UICONTROL Viewability] und [!UICONTROL Conversions]. Mit „([!UICONTROL Lifetime])“ angehängte Metriken geben Werte vom Beginn der Kampagne zurück, unabhängig vom auf der Seite ausgewählten Datumsbereich.

   1. Bearbeiten Sie die Spaltenreihenfolge nach Bedarf, indem Sie im rechten Bedienfeld auf Spaltennamen klicken und sie an die gewünschten Positionen ziehen.

   Einige Spalten haben feste Positionen und können nicht verschoben oder entfernt werden.

1. Anwenden oder Speichern der Einstellungen:

   * Um die Einstellungen vorübergehend anzuwenden, ohne sie in der Ansicht zu speichern, klicken Sie auf **[!UICONTROL Apply].**

   * Um die Einstellungen in einer neuen, benutzerdefinierten Spaltenansicht zu speichern, klicken Sie auf **[!UICONTROL Save As]**. Geben Sie im [!UICONTROL Save View] den Namen der neuen Ansicht ein, und klicken Sie dann auf **[!UICONTROL Save]**.

#### Spaltenansicht bearbeiten {#column-view-edit}

>[!NOTE]
>
>Sie können Änderungen nicht in einer standardmäßigen (vordefinierten) Spaltenansicht speichern, sondern können Ihre Änderungen vorübergehend anwenden oder in einer neuen benutzerdefinierten Ansicht speichern.

1. Klicken Sie in der Ansichtsauswahl auf ![Abwärtspfeil](/help/dsp/assets/chevron-down.png) und klicken Sie dann auf den Namen der vorhandenen Spaltenansicht.

1. Klicken Sie in der Ansichtsauswahl auf ![Abwärtspfeil](/help/dsp/assets/chevron-down.png) und dann auf **[!UICONTROL Edit View]**.

1. Bearbeiten Sie die Metriken, die in die Ansicht aufgenommen werden sollen:

   1. Aktivieren Sie in der Liste der verfügbaren Metriken das Kontrollkästchen neben jeder einzuschließenden Metrik und deaktivieren Sie das Kontrollkästchen neben jeder auszuschließenden Metrik.

      Alle Metriken sind alphabetisch nach Kategorie geordnet: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (Standardmetriken, die DSP verfolgt), [!UICONTROL Viewability] und [!UICONTROL Conversions]. Mit „([!UICONTROL Lifetime])“ angehängte Metriken geben Werte vom Beginn der Kampagne zurück, unabhängig vom auf der Seite ausgewählten Datumsbereich.

   1. Bearbeiten Sie die Spaltenreihenfolge nach Bedarf, indem Sie im rechten Bedienfeld auf Spaltennamen klicken und sie an die gewünschten Positionen ziehen.

   Einige Spalten haben feste Positionen und können nicht verschoben oder entfernt werden.

1. Anwenden oder Speichern der Einstellungen:

   * (Nur benutzerdefinierte Ansichten) Klicken Sie auf &quot;**[!UICONTROL Save]**&quot;, um die Einstellungen zu speichern.

   * Um die Einstellungen vorübergehend anzuwenden, ohne sie in der Ansicht zu speichern, klicken Sie auf **[!UICONTROL Apply].**

   * Um die Einstellungen in einer neuen, benutzerdefinierten Spaltenansicht zu speichern, klicken Sie auf **[!UICONTROL Save As]**. Geben Sie im [!UICONTROL Save View] den Namen der neuen Ansicht ein, und klicken Sie dann auf **[!UICONTROL Save]**.

### Kampagnendaten filtern {#filter-data-tables}

Filter ändern die Daten, die auf der aktuellen Registerkarte angezeigt werden. Die verfügbaren Filter variieren je nach Entitätstyp, können jedoch Entitätsnamen, Status und zusätzliche Eigenschaftsspalten enthalten.

1. Klicken Sie in der Hauptsymbolleiste auf ![Filterschaltfläche](/help/dsp/assets/filter.png).
1. Klicken Sie für jeden Filter, den Sie anwenden möchten, auf den Filternamen in der linken Spalte und geben Sie dann die Filterwerte an.
1. Klicken Sie auf **[!UICONTROL Apply]**.

#### Verfügbare Filter

Die folgenden Filter sind für Ihre [!UICONTROL Campaigns]-, [!UICONTROL Packages]- und [!UICONTROL Placements] verfügbar:

* Filter für die [!UICONTROL Campaigns]:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* Filter für die [!UICONTROL Packages]:
   * [!UICONTROL Custom flights] (ob sie existieren oder nicht)
   * [!UICONTROL Custom goal] (falls anwendbar)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* Filter für die [!UICONTROL Placements]:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (falls anwendbar)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than] oder [!UICONTROL equal to] eines angegebenen Werts)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] oder [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* Filter für die [!UICONTROL Ads]:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### Ändern des Datumsbereichs

Ändern Sie den in allen Standard- und benutzerdefinierten Ansichten verwendeten Datumsbereich, indem Sie die Datumsbereichsauswahl über einer beliebigen Datentabelle verwenden.

![Datumsbereichsauswahl](/help/dsp/assets/date-range-selector.png "Datumsbereichsauswahl")

* Für einen voreingestellten Bereich: Wählen Sie aus der Liste der gängigen Zeitinkremente. Der Standardwert lautet [!UICONTROL Last 30 days]*.

* Führen Sie für einen bestimmten Bereich einen der folgenden Schritte aus:

   * Klicken Sie ![Kalender](/help/dsp/assets/calendar.png "Kalender") und klicken Sie dann im Kalender auf das Anfangs- und Enddatum.

   * Klicken Sie in den Datumsbereich und geben Sie dann entweder ein Anfangs- und ein Enddatum ein oder wählen Sie diese im Kalender aus.

     Sie können numerische Werte (von M-D-YY bis MM-TT-YYYY) und/oder Monatsnamen oder Abkürzungen (z. B. Januar oder Januar) eingeben.

### Sortieren einer Datenspalte

Sie können jede Datenspalte in aufsteigender Reihenfolge (A bis Z oder 1 bis 10) oder in absteigender Reihenfolge (Z bis A oder 10 bis 1) sortieren.

* Klicken Sie auf die Spaltenüberschrift, um zwischen auf- und absteigender Reihenfolge zu wechseln.


### Anzahl der Datenzeilen angeben

Wählen Sie unten rechts auf einer beliebigen Seite neben **[!UICONTROL Items per page]** die Option *[!UICONTROL 25]*, *[!UICONTROL 50]* oder *[!UICONTROL 100]* aus.

>[!MORELIKETHIS]
>
>* [Typen von Leistungsberichten in Ansichten des Kampagnen-Managements](campaign-reports-about.md)
>* [Anzeigen, Sites und Häufigkeitsdetails für eine Platzierung anzeigen](placement-details-view.md)
>* [Anzeigen des Berichts für Platzierungs-Forecasts](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Anzeigen der Platzierungs-Diagnoseberichte](placement-diagnostics.md)
>* [Exportieren von Daten aus einer Kampagnenverwaltungsansicht](campaign-export-data.md)
>* [Video: DSP-Kontostruktur und Benutzeroberfläche](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
