---
title: Datenansichten der Kampagne verwalten
description: Erfahren Sie, wie Sie die Datenansichten für Kampagnen, Pakete, Platzierungen und Anzeigen anpassen können.
feature: DSP Campaign Data Views
source-git-commit: 14da2c26a6a6c3820f691cd752c22c982278314d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# Datenansichten der Kampagne verwalten

## Datenvisualisierungen verwalten

Sie können die Metriken und den Diagrammmodus für alle Datenvisualisierungen in Kampagnen oder für eine einzelne Kampagne ändern. Änderungen an einer einzelnen Kampagne werden für alle Datenvisualisierungen der Kampagne angewendet, einschließlich der Variablen [!UICONTROL Packages], [!UICONTROL Placements], und [!UICONTROL Ads] Registerkarten.

### Metriken für eine Datenvisualisierung ändern

1. Klicken Sie oben rechts in der Datenvisualisierung auf ![Einstellungen](/help/dsp/assets/settings-chart.png).
1. Wählen Sie die Metriken aus.
Dieselbe Metrik kann nicht zweimal ausgewählt werden.
1. Klicks **[!UICONTROL Apply]**.

### Anzeigemodus für eine Datenvisualisierung ändern

* Klicken Sie oben rechts in der Datenvisualisierung auf das [!UICONTROL Overlay] switch (![Überlagerungsschalter](/help/dsp/assets/overlay.png)), um zwischen dem Überlagerungsmodus (alle Diagramme werden zusammen überlagert) und dem Trellis-Diagrammmodus (drei separate Diagramme) zu wechseln.

## Datentabellen verwalten

In allen Kampagnenverwaltungsansichten ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], und [!UICONTROL Ads]), können Sie die in der Datentabelle angezeigten Daten anpassen.

### Spaltenansicht ändern

* Klicken Sie in der Ansicht-Auswahl auf ![Nach unten](/help/dsp/assets/chevron-down.png)und klicken Sie dann auf den Namen der gewünschten Spaltenansicht.

### Benutzerdefinierte Spaltenansicht erstellen

1. Klicken Sie in der Ansicht-Auswahl auf ![Nach unten](/help/dsp/assets/chevron-down.png)und klicken Sie anschließend auf **[!UICONTROL Create View]**.

1. Geben Sie die Metriken an, die in die Ansicht aufgenommen werden sollen:

   1. Aktivieren Sie in der Liste der verfügbaren Metriken das Kontrollkästchen neben den einzelnen Metriken, die einbezogen werden sollen.

   1. Bearbeiten Sie die Spaltenreihenfolge nach Bedarf, indem Sie im rechten Bereich auf Spaltennamen klicken und sie an die gewünschten Positionen ziehen.

   Einige Spalten haben feste Positionen und können nicht verschoben oder entfernt werden.

1. Wenden Sie die Einstellungen an oder speichern Sie sie:

   * Um die Einstellungen vorübergehend anzuwenden, ohne sie in der Ansicht zu speichern, klicken Sie auf **[!UICONTROL Apply].**

   * Um die Einstellungen in einer neuen, benutzerdefinierten Spaltenansicht zu speichern, klicken Sie auf **[!UICONTROL Save As]**. Im [!UICONTROL Save View] , geben Sie den Namen der neuen Ansicht ein und klicken Sie auf **[!UICONTROL Save]**.

### Bearbeiten einer benutzerdefinierten Spaltenansicht

>[!NOTE]
>
>Eine standardmäßige (vordefinierte) Spaltenansicht kann nicht bearbeitet werden.

1. Klicken Sie in der Ansicht-Auswahl auf ![Nach unten](/help/dsp/assets/chevron-down.png)und klicken Sie dann auf den Namen der vorhandenen Spaltenansicht.

1. Klicken Sie in der Ansicht-Auswahl auf ![Nach unten](/help/dsp/assets/chevron-down.png)und klicken Sie anschließend auf **[!UICONTROL Edit View]**.

1. Bearbeiten Sie die Metriken, die in die Ansicht aufgenommen werden sollen:

   1. Aktivieren Sie in der Liste der verfügbaren Metriken das Kontrollkästchen neben den einzelnen einzuschließenden Metriken und deaktivieren Sie das Kontrollkästchen neben den einzelnen Metriken, die ausgeschlossen werden sollen.

   1. Bearbeiten Sie die Spaltenreihenfolge nach Bedarf, indem Sie im rechten Bereich auf Spaltennamen klicken und sie an die gewünschten Positionen ziehen.

   Einige Spalten haben feste Positionen und können nicht verschoben oder entfernt werden.

1. Wenden Sie die Einstellungen an oder speichern Sie sie:

   * Um die Einstellungen vorübergehend anzuwenden, ohne sie in der Ansicht zu speichern, klicken Sie auf **[!UICONTROL Apply].**

   * Um die Einstellungen in einer neuen, benutzerdefinierten Spaltenansicht zu speichern, klicken Sie auf **[!UICONTROL Save As]**. Im [!UICONTROL Save View] , geben Sie den Namen der neuen Ansicht ein und klicken Sie auf **[!UICONTROL Save]**.

### Filtern von Kampagnendaten

1. Klicken Sie in der Symbolleiste auf ![Filterschaltfläche](/help/dsp/assets/filter.png).
1. Klicken Sie für jeden anzuwendenden Filter in der linken Spalte auf den Namen des Filters und geben Sie die Filterwerte an.
1. Klicks **[!UICONTROL Apply]**.

#### Verfügbare Filter

Die folgenden Filter stehen für Ihre [!UICONTROL Campaigns], [!UICONTROL Packages], und [!UICONTROL Placements] Ansichten:

* [!UICONTROL Campaigns] Ansichtsfilter:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] Ansichtsfilter:
   * [!UICONTROL Custom flights] (unabhängig davon, ob sie existieren oder nicht)
   * [!UICONTROL Custom goal] (falls zutreffend)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] Ansichtsfilter:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (falls zutreffend)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than]oder [!UICONTROL equal to] einen angegebenen Wert)
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
* [!UICONTROL Ads] Ansichtsfilter:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### Sortieren einer Datenspalte

Sie können jede Datenspalte in aufsteigender Reihenfolge (A bis Z oder 1 bis 10) oder in absteigender Reihenfolge (Z bis A oder 10 bis 1) sortieren.

* Klicken Sie auf die Spaltenüberschrift, um zwischen auf- und absteigender Reihenfolge zu wechseln.

<!-- add more links-->

>[!MORELIKETHIS]
>
>* [Über In-Platform-Berichte](campaign-reports-about.md)
>* [Datenvisualisierungen verwalten](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [Spaltenansicht ändern](column-view-change.md)
>* [Benutzerdefinierte Spaltenansicht erstellen](column-view-create.md)
>* [Bearbeiten einer benutzerdefinierten Spaltenansicht](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [Filtern von Kampagnendaten](campaign-data-filter.md)
>* [Sortieren einer Datenspalte](campaign-data-sort.md)
>* [Anzeigen von Sites, Anzeigen und Frequenzdetails für eine Platzierung](placement-details-view.md)
>* [Anzeigen des Berichts zur Platzierungsvorschau](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Anzeigen der platzierungsdiagnostischen Berichte](placement-diagnostics.md)
>* [Daten aus einer Campaign Management-Ansicht exportieren](campaign-export-data.md)
>* [Video: DSP Kontostruktur und Benutzeroberfläche](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
