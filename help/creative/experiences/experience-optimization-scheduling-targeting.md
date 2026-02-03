---
title: Anpassen der kreativen Optimierung und Planung für ein Erlebnis
description: Erfahren Sie, wie Sie die Optimierung und Anzeigenplanung für zielgerichtete Erlebnisse konfigurieren.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 0%

---

# Kreative Optimierung und Planung für ein Erlebnis mit Entscheidungsbaum-Targeting anpassen

*Targeting von Knoten nur mit vorhandenen Kreativen*

Standardmäßig wird die kreative Rotation für ein Erlebnis algorithmisch bestimmt, um die gesamte Clickthrough-Rate zu optimieren. Die Einstellungen für die kreative Optimierung gelten für alle zugewiesenen Bundles. Sie können Bundles alternativ algorithmisch für ein bestimmtes benutzerdefiniertes Advertising DSP-Ziel optimieren, gemäß einer bestimmten Bundle-Sequenz mit einer bestimmten Anzahl von Impressionen über jede Bundle-Sequenz hinweg drehen oder entsprechend der relativen Gewichtung. Sie können auch bestimmte kreative Bundles für bestimmte, sequenzielle Zeiträume planen und benutzerdefinierte kreative Rotationseinstellungen für jeden Zeitplan anwenden.

>[!NOTE]
>
>Diese Funktionen sind nicht für Knoten verfügbar, die die standardmäßigen Kreativen anstelle der zugewiesenen Kreativen verwenden.

## Konfigurieren der kreativen Optimierung ohne Planung

Wenn die kreative Planung deaktiviert ist, gelten die Einstellungen für die kreative Optimierung für alle zugewiesenen Kreativen.

1. Halten Sie den Cursor über den Creative Leaf-Knoten unter dem Zielknoten und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. **[!UICONTROL Schedule]** deaktivieren.

1. Wählen Sie den Kreativ-Rotationstyp für Anzeigenvarianten in den zugehörigen Bundles aus:

   * *[!UICONTROL Weighted]:* Zeigt Anzeigenvarianten in den zugehörigen Kreativ-Bundles entsprechend der relativen Gewichtung an. Geben Sie die Gewichtung für jedes Bundle als Prozentsatz ein. Die Gewichtungen für alle ausgewählten Bundles müssen bis zu 100,<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. --> addieren

   * *[!UICONTROL Algorithmic]:* Zeigt die effektivsten Anzeigenvarianten häufiger an, basierend auf einem bestimmten Ziel.

      * Wählen Sie für die **[!UICONTROL Optimization Goal]** *[!UICONTROL Click Through Rate]*, (Standard-Videoanzeigenerlebnisse) *[!UICONTROL Completion Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes benutzerdefiniertes [Advertising DSP-Ziel &#x200B;](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:* Zeigt die zugehörigen Kreativ-Bundles in einer bestimmten Reihenfolge an (wobei Bundle 1 zuerst bereitgestellt wird, Bundle 2 als zweites bereitgestellt wird usw.), mit einer angegebenen Gesamtanzahl von Impressions für jede Bundle-Sequenz. Die Anzeigengrößen, die bereitgestellt werden, werden durch den verfügbaren Bestand bestimmt. Sie können das endgültige Bundle in der Sequenz so konfigurieren, dass a\) auf unbestimmte Zeit angezeigt wird (Standard) oder b\) zum ersten Bundle zurückkehrt. Sie können beispielsweise jede der Anzeigenvarianten in Bundle 1 für drei (3) Impressionen anzeigen, dann jede Anzeigenvariante in Bundle 2 für eine (1) Impression anzeigen, dann jede der Anzeigenvarianten in Bundle 3 für zwei (2) Impressionen anzeigen und dann die Schleife erneut starten. Alternativ können Sie, sobald die Anzeigenvarianten in Bundle 3 angezeigt werden, die Anzeigenvarianten in Bundle 3 weiterhin unbegrenzt anzeigen, anstatt eine Schleife zu erstellen. Beim Aktivieren der Sequenzierung:

      1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

     Standardmäßig werden die zugewiesenen Bundles in der Reihenfolge sortiert, in der sie zum Erlebnis hinzugefügt wurden.

      1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

      1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Konfigurieren der kreativen Optimierung mit kreativer Planung

Sie können optional die Ausführung bestimmter Kreativ-Bundles während bestimmter, sequenzieller Zeiträume zwischen dem Start- und dem Enddatum des Erlebnisses planen und benutzerdefinierte Kreativ-Rotationseinstellungen für jeden Zeitplan anwenden. Beispielsweise können Sie die Ausführung von Bundle 1 für die ersten beiden Wochen planen, um die Clickthrough-Rate zu optimieren, und Bundle 2 für die folgenden zwei Wochen, um für ein bestimmtes benutzerdefiniertes Ziel zu optimieren.

Wenn Sie die Planung verwenden, müssen Sie die Pakete für die Dauer des Erlebnisses planen.

1. Halten Sie den Cursor über den Creative Leaf-Knoten unter dem Zielknoten und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. **[!UICONTROL Schedule]** aktivieren.

1. Für den ersten Zeitplan:

   1. Aktivieren Sie in der linken Spalte das Kontrollkästchen neben jedem kreativen Bundle, das dem ersten Zeitplan hinzugefügt werden soll.

   1. Geben Sie das Start- und Enddatum für den Zeitplan an.

   1. Wählen Sie den Kreativ-Rotationstyp aus:

      * *[!UICONTROL Weighted]:* Dreht die Kreativen in jedem Paket manuell entsprechend der relativen Gewichtung. Geben Sie die Gewichtung für jedes Bundle als Prozentsatz ein. Die Gewichtungen für alle ausgewählten Bundles müssen bis zu 100 addieren.

      * *[!UICONTROL Algorithmic]:* Dreht die Kreativen in jedem Bundle algorithmisch nach einem bestimmten Optimierungsziel.

         * Wählen Sie für die **[!UICONTROL Optimization Goal]** *[!UICONTROL Click Through Rate]*, (Standard-Videoanzeigenerlebnisse) *[!UICONTROL Completion Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes benutzerdefiniertes [Advertising DSP-Ziel &#x200B;](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* Dreht die zugehörigen kreativen Bundles in einer bestimmten Reihenfolge (wobei Bundle 1 zuerst bereitgestellt wird, Bundle 2 erst bereitgestellt wird usw.) mit einer bestimmten Gesamtzahl von Impressions für jede Bundle-Sequenz. Die Anzeigengrößen, die bereitgestellt werden, werden durch den verfügbaren Bestand bestimmt. Sie können das endgültige Bundle in der Sequenz so konfigurieren, dass a\) auf unbestimmte Zeit angezeigt wird (Standard) oder b\) zum ersten Bundle zurückkehrt. Sie können beispielsweise eines der Kreativen in Bundle 1 für drei (3) Impressions anzeigen, dann ein Kreatives in Bundle 2 für eine (1) Impression anzeigen, dann eines der Kreativen in Bundle 3 für zwei (2) Impressionen anzeigen und dann die Schleife erneut starten. Alternativ können Sie, sobald die Kreativen in Bundle 3 angezeigt werden, die Kreativen in Bundle 3 weiterhin auf unbestimmte Zeit anzeigen, anstatt eine Schleife zu erstellen. Beim Aktivieren der Sequenzierung:

         1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

            Standardmäßig werden die zugewiesenen Bundles in der Reihenfolge sortiert, in der sie zum Erlebnis hinzugefügt wurden.

         1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

         1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Für jeden zusätzlichen Zeitplan:

   1. Klicken Sie auf **[!UICONTROL + Add Schedule]**.

   1. Aktivieren Sie in der linken Spalte das Kontrollkästchen neben jedem kreativen Bundle, das dem ersten Zeitplan hinzugefügt werden soll.

   1. Geben Sie das Start- und Enddatum für den Zeitplan an.

   1. Wählen Sie den Kreativ-Rotationstyp aus:

      * *[!UICONTROL Weighted]:* Dreht die Kreativen in jedem Paket manuell entsprechend der relativen Gewichtung. Geben Sie die Gewichtung für jedes Bundle als Prozentsatz ein. Die Gewichtungen für alle ausgewählten Bundles müssen bis zu 100 addieren.

      * *[!UICONTROL Algorithmic]:* Dreht die Kreativen in jedem Bundle algorithmisch nach einem bestimmten Optimierungsziel.

         * Wählen Sie für die **[!UICONTROL Optimization Goal]** entweder *[!UICONTROL Click Through Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes benutzerdefiniertes [Advertising DSP-Ziel &#x200B;](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* Dreht die zugehörigen Kreativ-Bundles in einer bestimmten Reihenfolge mit einer angegebenen Gesamtzahl von Impressionen über jede Bundle-Sequenz hinweg. Beim Aktivieren der Sequenzierung:

         1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

            Standardmäßig werden die zugewiesenen Bundles in der Reihenfolge sortiert, in der sie zum Erlebnis hinzugefügt wurden.

         1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

         1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Passen Sie die Tracking-URLs für Kreative an](/help/creative/experiences/experience-tracking-urls-targeting.md)
