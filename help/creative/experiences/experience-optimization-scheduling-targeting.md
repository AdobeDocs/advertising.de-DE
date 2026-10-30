---
title: Anpassen der kreativen Optimierung und Planung für ein Erlebnis
description: Erfahren Sie, wie Sie die Optimierung und Anzeigenplanung für zielgerichtete Erlebnisse konfigurieren.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%
---
# Kreative Optimierung und Planung für ein Erlebnis mit Entscheidungsbaum-Targeting anpassen

*Targeting von Knoten nur mit vorhandenen Kreativen*

Standardmäßig wird die kreative Rotation für die gesamte Clickthrough-Rate in allen zugewiesenen Bundles optimiert. Sie können die Rotationseinstellungen anpassen oder bestimmte Pakete planen, die während sequenzieller Zeiträume ausgeführt werden sollen, mit separaten Rotationseinstellungen für jeden Zeitplan.

>[!NOTE]
>
>Diese Funktionen sind nicht für Knoten verfügbar, die die standardmäßigen Kreativen anstelle der zugewiesenen Kreativen verwenden.

Sie können diese Einstellungen direkt auf der Arbeitsfläche des KI-gesteuerten Editors (Beta) oder im Manualeditor konfigurieren. In beiden Editoren wird beim Speichern des Bundle-Dialogfelds die Arbeitsstruktur aktualisiert. Außerdem müssen Sie [das Erlebnis speichern](#save) aus der Kopfzeile der Baumstruktur entfernen.

## Rotationseinstellungen {#rotation-settings}

* **[!UICONTROL Weighted]:** Zeigt Anzeigenvarianten in den zugehörigen Kreativ-Bundles entsprechend der relativen Gewichtung an.

* **[!UICONTROL Algorithmic]:** Zeigt die effektivsten Anzeigenvarianten häufiger an, basierend auf einem angegebenen Optimierungsziel, wie z. B. Clickthrough-Rate oder einem benutzerdefinierten Advertising DSP-Ziel.

* **[!UICONTROL Sequence](KI-gesteuerter Editor) oder [!UICONTROL Sequencing] (manueller Editor):** Zeigt die zugehörigen Kreativ-Bundles in einer bestimmten Reihenfolge mit einer bestimmten Anzahl von Impressionen für jedes Bundle in der Sequenz an. Standardmäßig werden Bundles in der Reihenfolge sortiert, in der sie zum Erlebnis hinzugefügt wurden. Die Anzeigengrößen, die bereitgestellt werden, werden durch den verfügbaren Bestand bestimmt. Das endgültige Bundle kann unbegrenzt bereitstellen (Standard), oder die Sequenz kann zum ersten Bundle zurückkehren.

  Beispielsweise könnte eine Sequenz Anzeigenvarianten von Bundle 1 für drei Impressionen, Bundle 2 für eine Impression und Bundle 3 für zwei Impressionen bereitstellen und dann wiederholen. Ohne Schleife dient Bundle 3 weiterhin auf unbestimmte Zeit.

## Konfigurieren der kreativen Optimierung ohne Planung

Wenn die kreative Planung deaktiviert ist, gelten die Einstellungen für die kreative Optimierung für alle zugewiesenen Kreativen.

### Verwenden des KI-gesteuerten Editors (Beta) {#without-scheduling-ai}

1. Klicken Sie beim [ (Erstellen](experience-create-targeting.md#ai-editor) oder [Bearbeiten](experience-edit-targeting.md#ai-editor) des Erlebnisses auf **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** im kreativen Blattknoten.

   Klicken Sie für einen endgültigen Knoten ohne Bundles auf **[!UICONTROL Assign Bundles]** und [weisen Sie die Bundles ](experience-assign-creative-bundles.md#ai-editor).

1. Öffnen Sie die Registerkarte **[!UICONTROL Creative optimisation]** .

1. **[!UICONTROL Schedule]** deaktivieren.

1. Wählen Sie den Kreativ-Rotationstyp aus und konfigurieren Sie die Einstellungen:

   * **[!UICONTROL Weighted]:** Geben Sie die relative Gewichtung für jede Bundle-Zeile ein. Die Gewichtungen müssen insgesamt 100 betragen. Um die Gewichtungen gleichmäßig zu verteilen, klicken Sie auf **[!UICONTROL Apply equal weight]**.

   * **[!UICONTROL Algorithmic]:** Wählen Sie eine **[!UICONTROL Optimization goals]** Option aus. Wenn Sie ein benutzerdefiniertes Ziel auswählen, wählen Sie das vorhandene benutzerdefinierte Ziel [Advertising DSP](/help/dsp/optimization/custom-goal.md) in **[!UICONTROL Custom objective]** aus.

   * **[!UICONTROL Sequence]:** Ziehen Sie die Bundles in die gewünschte Reihenfolge und geben Sie die Anzahl der Impressionen für jede Sequenz ein. Aktivieren Sie **[!UICONTROL Keep in loop]**, um die Sequenz zu wiederholen, oder deaktivieren Sie sie, um die Impressions des letzten Bundles auf **[!UICONTROL Infinite]** zu setzen.

1. Klicken Sie im Dialogfeld auf **[!UICONTROL Save]** .

1. [Speichern Sie das Erlebnis](#save).

### Verwenden des manuellen Editors {#without-scheduling-manual}

[Öffnen Sie den manuellen Editor](experience-edit-targeting.md#experience-open) bevor Sie diese Schritte ausführen.

1. Öffnen Sie beim [ (Erstellen](experience-create-targeting.md) oder [Bearbeiten](experience-edit-targeting.md) des Erlebnisses die Einstellungen für die kreative Optimierung:

   1. Halten Sie den Cursor über den Creative Leaf-Knoten unter dem Zielknoten und führen Sie folgende Schritte aus:

      * Klicken Sie für vorhandene Bundles auf **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Klicken Sie bei neuen Bundles auf **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** und [weisen Sie die Bundles zu](experience-assign-creative-bundles.md).

   1. Klicken Sie auf die Registerkarte **[!UICONTROL Creative Optimization]** .

1. **[!UICONTROL Schedule]** deaktivieren.

1. Wählen Sie den Kreativ-Rotationstyp für Anzeigenvarianten in den zugehörigen Bundles aus:

   * *[!UICONTROL Weighted]:* Geben Sie die Gewichtung für jedes Bundle in Prozent ein. Um gleiche Gewichtungen auf alle zugehörigen Bundles anzuwenden, klicken Sie auf (![gleiche Gewichtung anwenden](/help/creative/assets/apply-equal-weight.png "gleiche Gewichtung anwenden")). Die Gewichtungen für alle ausgewählten Bundles müssen bis zu 100 addieren.

   * *[!UICONTROL Algorithmic]:* Wählen Sie für die **[!UICONTROL Optimization Goal]** *[!UICONTROL Click Through Rate]*, (Standard-Videoanzeigenerlebnisse) *[!UICONTROL Completion Rate]* oder *[!UICONTROL Custom Objective]* aus. Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes benutzerdefiniertes [Advertising DSP-Ziel ](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:*

     1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

     1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

     1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Konfigurieren der kreativen Optimierung mit kreativer Planung

Sie können optional die Ausführung bestimmter Kreativ-Bundles während bestimmter, sequenzieller Zeiträume zwischen dem Start- und dem Enddatum des Erlebnisses planen und benutzerdefinierte Kreativ-Rotationseinstellungen für jeden Zeitplan anwenden. Beispielsweise können Sie die Ausführung von Bundle 1 für die ersten beiden Wochen planen, um die Clickthrough-Rate zu optimieren, und Bundle 2 für die folgenden zwei Wochen, um für ein bestimmtes benutzerdefiniertes Ziel zu optimieren.

Wenn Sie die Planung verwenden, müssen Sie die Pakete für die Dauer des Erlebnisses planen.

### Verwenden des KI-gesteuerten Editors (Beta) {#with-scheduling-ai}

1. Klicken Sie beim [ (Erstellen](experience-create-targeting.md#ai-editor) oder [Bearbeiten](experience-edit-targeting.md#ai-editor) des Erlebnisses auf **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** im kreativen Blattknoten.

   Klicken Sie für einen endgültigen Knoten ohne Bundles auf **[!UICONTROL Assign Bundles]** und [weisen Sie die Bundles ](experience-assign-creative-bundles.md#ai-editor).

1. Öffnen Sie die Registerkarte **[!UICONTROL Creative optimisation]** und aktivieren Sie **[!UICONTROL Schedule]**.

1. Wählen Sie die **[!UICONTROL Timezone]** für den Zeitplan aus.

1. Für den ersten Zeitplan:

   1. Aktivieren Sie das Kontrollkästchen neben jedem Bundle, das in der linken Spalte enthalten sein soll.

   1. Geben Sie das Start- und Enddatum sowie die Uhrzeit an.

   1. Wählen Sie den Kreativ-Rotationstyp aus und konfigurieren Sie die Einstellungen:

      * **[!UICONTROL Weighted]:** Geben Sie die relative Gewichtung für jede Bundle-Zeile im Zeitplan ein. Die Gewichtungen müssen insgesamt 100 betragen. Um die Gewichtungen gleichmäßig zu verteilen, klicken Sie auf **[!UICONTROL Apply equal weight]**.

      * **[!UICONTROL Algorithmic]:** Wählen Sie eine **[!UICONTROL Optimization goals]** Option aus. Wenn Sie ein benutzerdefiniertes Ziel auswählen, wählen Sie das vorhandene benutzerdefinierte Ziel [Advertising DSP](/help/dsp/optimization/custom-goal.md) in **[!UICONTROL Custom objective]** aus.

      * **[!UICONTROL Sequence]:** Ziehen Sie die Bundles in die gewünschte Reihenfolge und geben Sie die Anzahl der Impressionen für jede Sequenz ein. Aktivieren Sie **[!UICONTROL Keep in loop]**, um die Sequenz zu wiederholen, oder deaktivieren Sie sie, um die Impressions des letzten Bundles auf **[!UICONTROL Infinite]** zu setzen.

1. Klicken Sie für jeden zusätzlichen Zeitplan auf **[!UICONTROL + Add Schedule]**, wählen Sie die Karte Zeitplan aus und konfigurieren Sie die Bundles, Daten und Uhrzeiten sowie die Rotationseinstellungen.

   Die Bundle-Kontrollkästchen gelten für den ausgewählten Zeitplan, nicht für alle Zeitpläne. Stellen Sie sicher, dass die Zeitpläne mit zugewiesenen Bundles die gesamte Erlebnisdauer abdecken.

1. Klicken Sie im Dialogfeld auf **[!UICONTROL Save]** .

1. [Speichern Sie das Erlebnis](#save).

### Verwenden des manuellen Editors {#with-scheduling-manual}

[Öffnen Sie den manuellen Editor](experience-edit-targeting.md#experience-open) bevor Sie diese Schritte ausführen.

1. Öffnen Sie beim [ (Erstellen](experience-create-targeting.md) oder [Bearbeiten](experience-edit-targeting.md) des Erlebnisses die Einstellungen für die kreative Optimierung:

   1. Halten Sie den Cursor über den Creative Leaf-Knoten unter dem Zielknoten und führen Sie folgende Schritte aus:

      * Klicken Sie für vorhandene Bundles auf **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Klicken Sie bei neuen Bundles auf **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** und [weisen Sie die Bundles zu](experience-assign-creative-bundles.md).

   1. Klicken Sie auf die Registerkarte **[!UICONTROL Creative Optimization]** .

1. **[!UICONTROL Schedule]** aktivieren.

1. Für den ersten Zeitplan:

   1. Aktivieren Sie in der linken Spalte das Kontrollkästchen neben jedem kreativen Bundle, das dem ersten Zeitplan hinzugefügt werden soll.

   1. Geben Sie das Startdatum und die Startzeit sowie das Enddatum und die Endzeit für den Zeitplan an.

   1. Wählen Sie den Kreativ-Rotationstyp aus:

      * *[!UICONTROL Weighted]:* Geben Sie die Gewichtung für jedes Bundle in Prozent ein. Um gleiche Gewichtungen auf alle Bundles im Zeitplan anzuwenden, klicken Sie auf (![gleiche Gewichtung anwenden](/help/creative/assets/apply-equal-weight.png "gleiche Gewichtung anwenden")). Die Gewichtungen für alle ausgewählten Bundles müssen bis zu 100 addieren.

      * *[!UICONTROL Algorithmic]:* Wählen Sie für die **[!UICONTROL Optimization Goal]** *[!UICONTROL Click Through Rate]*, (Standard-Videoanzeigenerlebnisse) *[!UICONTROL Completion Rate]* oder *[!UICONTROL Custom Objective]* aus. Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes benutzerdefiniertes [Advertising DSP-Ziel ](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:*

        1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

        1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

        1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Für jeden zusätzlichen Zeitplan:

   1. Klicken Sie auf **[!UICONTROL + Add Schedule]**.

   1. Aktivieren Sie in der linken Spalte das Kontrollkästchen neben jedem kreativen Bundle, das dem ersten Zeitplan hinzugefügt werden soll.

   1. Geben Sie das Start- und Enddatum für den Zeitplan an.

   1. Wählen Sie den Kreativ-Rotationstyp aus:

      * *[!UICONTROL Weighted]:* Geben Sie die Gewichtung für jedes Bundle in Prozent ein. Die Gewichtungen für alle ausgewählten Bundles müssen bis zu 100 addieren.

      * *[!UICONTROL Algorithmic]:* Wählen Sie für die **[!UICONTROL Optimization Goal]** entweder *[!UICONTROL Click Through Rate]* oder *[!UICONTROL Custom Objective]* aus. Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes benutzerdefiniertes [Advertising DSP-Ziel ](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:*

        1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

        1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

        1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Erlebnis speichern {#save}

Die folgenden Schritte gelten für beide Editoren.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Passen Sie die Tracking-URLs für Kreative an](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [Anzeigen des Änderungsprotokolls für ein Erlebnis](/help/creative/experiences/experience-view-change-log.md)
