---
title: Anpassen der kreativen Optimierung und Planung für ein Erlebnis
description: Weitere Informationen zu
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Kreative Optimierung und Planung für ein Erlebnis mit Entscheidungsbaum-Targeting anpassen

*Targeting von Knoten nur mit vorhandenen Kreativen*
*Geschlossene Beta-Version*

Standardmäßig wird die kreative Rotation für ein Erlebnis algorithmisch bestimmt, um die gesamte Clickthrough-Rate zu optimieren. Die Einstellungen für die kreative Optimierung gelten für alle zugewiesenen Bundles. Sie können die Kreativrotation so anpassen, dass die Kreativen in jedem Bundle entsprechend der relativen Gewichtung manuell ausgeführt oder für ein bestimmtes benutzerdefiniertes Advertising DSP-Ziel algorithmisch optimiert werden. <!-- verify --> Sie können auch bestimmte kreative Bundles für bestimmte, sequenzielle Zeiträume planen und benutzerdefinierte kreative Rotationseinstellungen für jeden Zeitplan anwenden.

>[!NOTE]
>
>Diese Funktionen sind nicht für Knoten verfügbar, die die standardmäßigen Bildkreativen anstelle der zugewiesenen Kreativen verwenden.

## Konfigurieren der kreativen Optimierung ohne Planung

Wenn die kreative Planung deaktiviert ist, gelten die Einstellungen für die kreative Optimierung für alle zugewiesenen Kreativen.

1. Halten Sie den Cursor über den Creative Leaf-Knoten unter dem Zielknoten und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. **[!UICONTROL Schedule]** deaktivieren.

1. Wählen Sie den Kreativ-Rotationstyp aus:

   * ** *Gewichtete* ** - Dreht die Kreativen in jedem Paket manuell entsprechend der relativen Gewichtung. Geben Sie die Gewichtung für jedes Bundle als Prozentsatz ein. Die Gewichtungen für alle Bundles müssen bis zu 100 addieren.

   * ** *Algorithmisch* ** - Dreht die Kreativen in jedem Bundle algorithmisch entsprechend einem angegebenen Optimierungsziel.

   * Wählen Sie für die **[!UICONTROL Optimization Goal]** entweder *[!UICONTROL Click Through Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes [benutzerdefiniertes Advertising DSP-Ziel aus](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. Klicken Sie auf **[!UICONTROL Save]**.

## Konfigurieren der kreativen Optimierung mit kreativer Planung

Sie können optional die Ausführung bestimmter Kreativ-Bundles während bestimmter, sequenzieller Zeiträume zwischen dem Start- und dem Enddatum des Erlebnisses planen und benutzerdefinierte Kreativ-Rotationseinstellungen für jeden Zeitplan anwenden. Beispielsweise können Sie die Ausführung von Bundle 1 für die ersten beiden Wochen planen, um die Clickthrough-Rate zu optimieren, und Bundle 2 für die folgenden zwei Wochen, um für ein bestimmtes benutzerdefiniertes Ziel zu optimieren.

Wenn Sie die Planung verwenden, müssen Sie die Pakete für die Dauer des Erlebnisses planen.

1. Halten Sie den Cursor über den Creative Leaf-Knoten unter dem Zielknoten und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. **[!UICONTROL Schedule]** aktivieren.

1. Für den ersten Zeitplan:

   1. Aktivieren Sie in der linken Spalte das Kontrollkästchen neben jedem kreativen Bundle, das dem ersten Zeitplan hinzugefügt werden soll.

   1. Geben Sie das Start- und Enddatum für den Zeitplan an.

   1. Wählen Sie den Kreativ-Rotationstyp aus:

      * ** *Gewichtete* ** - Dreht die Kreativen in jedem Paket manuell entsprechend der relativen Gewichtung. Geben Sie die Gewichtung für jedes Bundle als Prozentsatz ein. Die Gewichtungen für alle ausgewählten Bundles müssen bis zu 100 addieren.

      * ** *Algorithmisch* ** - Dreht die Kreativen in jedem Bundle algorithmisch entsprechend einem angegebenen Optimierungsziel.

      * Wählen Sie für die **[!UICONTROL Optimization Goal]** entweder *[!UICONTROL Click Through Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes [benutzerdefiniertes Advertising DSP-Ziel aus](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. Für jeden zusätzlichen Zeitplan:

   1. Klicken Sie auf **[!UICONTROL + Add Schedule]**.

   1. Aktivieren Sie in der linken Spalte das Kontrollkästchen neben jedem kreativen Bundle, das dem ersten Zeitplan hinzugefügt werden soll.

   1. Geben Sie das Start- und Enddatum für den Zeitplan an.

   1. Wählen Sie den Kreativ-Rotationstyp aus:

      * ** *Gewichtete* ** - Dreht die Kreativen in jedem Paket manuell entsprechend der relativen Gewichtung. Geben Sie die Gewichtung für jedes Bundle als Prozentsatz ein. Die Gewichtungen für alle ausgewählten Bundles müssen bis zu 100 addieren.

      * ** *Algorithmisch* ** - Dreht die Kreativen in jedem Bundle algorithmisch entsprechend einem angegebenen Optimierungsziel.

      * Wählen Sie für die **[!UICONTROL Optimization Goal]** entweder *[!UICONTROL Click Through Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes [benutzerdefiniertes Advertising DSP-Ziel aus](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Passen Sie die Tracking-URLs für Kreative an](/help/creative/experiences/experience-tracking-urls-targeting.md)
