---
title: Anpassen der kreativen Optimierung und Planung für ein Erlebnis
description: Weitere Informationen zu
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 0%

---

# Anpassen der kreativen Optimierung und Planung für ein Erlebnis ohne Targeting mit Entscheidungsbaum

*Erlebnisse nur mit vorhandenen Kreativen*

Standardmäßig wird die kreative Rotation für ein Anzeigen-Erlebnis-Tag algorithmisch bestimmt, um die Gesamtklickrate zu optimieren, und die Einstellungen für die kreative Optimierung gelten für alle zugewiesenen Kreativen. Sie können die Kreativrotation so anpassen, dass die Kreativen manuell entsprechend der relativen Gewichtung ausgeführt oder algorithmisch für ein bestimmtes benutzerdefiniertes Advertising DSP-Ziel optimiert werden. Sie können auch festlegen, dass bestimmte Kreative während bestimmter, sequenzieller Zeiträume ausgeführt werden, und benutzerdefinierte Kreativ-Rotationseinstellungen für jeden Zeitplan anwenden.

## Konfigurieren der kreativen Optimierung ohne Planung

Wenn die kreative Planung deaktiviert ist, gelten die Einstellungen für die kreative Optimierung für alle zugewiesenen Kreativen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Tag Manager]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Tag Manager]**.

1. Halten Sie den Cursor über die Zeile für das entsprechende Anzeigen-Tag und klicken Sie auf ![Anzeigenzeitplan](/help/creative/assets/edit-gray.png "Tracking-URLs bearbeiten") **[!UICONTROL Creative Optimization]**.&lt;!— Tag Manager hat ab 2/2 nur eine Listenansicht, aber keine Kartenansicht. >

1. **[!UICONTROL Schedule]** deaktivieren.

1. Wählen Sie den Kreativ-Rotationstyp aus:

   * *[!UICONTROL Weighted]:* Dreht die Kreativen manuell entsprechend der relativen Gewichtung. Geben Sie die Gewichtung für jeden Kreativen in Prozent ein. Die Gewichtungen aller ausgewählten Kreativen müssen bis zu 100 betragen.

   * *[!UICONTROL Algorithmic]:* Dreht die Kreativen algorithmisch entsprechend einem angegebenen Optimierungsziel.

      * Wählen Sie für die **[!UICONTROL Optimization Goal]** *[!UICONTROL Click Through Rate]*, (Standard-Videoanzeigenerlebnisse) *[!UICONTROL Completion Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes [benutzerdefiniertes Advertising DSP-Ziel aus](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

   * *[!UICONTROL Sequencing]:* Dreht die zugehörigen kreativen Bundles in einer bestimmten Reihenfolge (wobei Bundle 1 zuerst bereitgestellt wird, Bundle 2 erst bereitgestellt wird usw.) mit einer bestimmten Gesamtzahl von Impressions für jede Bundle-Sequenz. Die Anzeigengrößen, die bereitgestellt werden, werden durch den verfügbaren Bestand bestimmt. Sie können das endgültige Bundle in der Sequenz so konfigurieren, dass a\) auf unbestimmte Zeit angezeigt wird (Standard) oder b\) zum ersten Bundle zurückkehrt. Sie können beispielsweise eines der Kreativen in Bundle 1 für drei (3) Impressions anzeigen, dann ein Kreatives in Bundle 2 für eine (1) Impression anzeigen, dann eines der Kreativen in Bundle 3 für zwei (2) Impressionen anzeigen und dann die Schleife erneut starten. Alternativ können Sie, sobald die Kreativen in Bundle 3 angezeigt werden, die Kreativen in Bundle 3 weiterhin auf unbestimmte Zeit anzeigen, anstatt eine Schleife zu erstellen. Beim Aktivieren der Sequenzierung:

      1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

     Standardmäßig werden die zugewiesenen Bundles in der Reihenfolge sortiert, in der sie zum Erlebnis hinzugefügt wurden.

      1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

      1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Konfigurieren der kreativen Optimierung mit kreativer Planung

Sie können optional bestimmte Kreative planen, die für ein Anzeigen-Erlebnis-Tag verwendet werden, um sie in bestimmten, sequenziellen Zeiträumen zwischen dem Start- und dem Enddatum des Erlebnisses auszuführen, und benutzerdefinierte Einstellungen für die kreative Rotation auf jeden Zeitplan anwenden. Beispielsweise können Sie die Ausführung von Creative 1 für die ersten beiden Wochen planen, um die Clickthrough-Rate zu optimieren, und Creative 2 für die folgenden zwei Wochen, um für ein bestimmtes benutzerdefiniertes Ziel zu optimieren.

Wenn Sie die Planung verwenden, müssen Sie die Dauer des Erlebnisses für die Kreativen planen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Tag Manager]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Tag Manager]**.

1. Halten Sie den Cursor über die Zeile für das entsprechende Anzeigen-Tag und klicken Sie auf ![Anzeigenzeitplan](/help/creative/assets/edit-gray.png "Tracking-URLs bearbeiten") **[!UICONTROL Creative Optimization]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— Tag Manager hat ab 2/2 nur eine Listenansicht, aber keine Kartenansicht. >

1. **[!UICONTROL Schedule]** aktivieren.

1. Für den ersten Zeitplan:

   1. Aktivieren Sie in der linken Spalte das Kontrollkästchen neben jedem Kreativen, der dem ersten Zeitplan hinzugefügt werden soll.

   1. Geben Sie das Start- und Enddatum für den Zeitplan an.

   1. Wählen Sie den Kreativ-Rotationstyp aus:

      * *[!UICONTROL Weighted]:* Dreht die Kreativen manuell entsprechend der relativen Gewichtung. Geben Sie die Gewichtung für jeden Kreativen in Prozent ein. Die Gewichtungen aller ausgewählten Kreativen müssen bis zu 100 betragen.

      * *[!UICONTROL Algorithmic]:* Dreht die Kreativen algorithmisch entsprechend einem angegebenen Optimierungsziel.

         * Wählen Sie für die **[!UICONTROL Optimization Goal]** *[!UICONTROL Click Through Rate]*, (Standard-Videoanzeigenerlebnisse) *[!UICONTROL Completion Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes [benutzerdefiniertes Advertising DSP-Ziel aus](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

      * *[!UICONTROL Sequencing]:* Dreht die zugehörigen kreativen Bundles in einer bestimmten Reihenfolge (wobei Bundle 1 zuerst bereitgestellt wird, Bundle 2 erst bereitgestellt wird usw.) mit einer bestimmten Gesamtzahl von Impressions für jede Bundle-Sequenz. Die Anzeigengrößen, die bereitgestellt werden, werden durch den verfügbaren Bestand bestimmt. Sie können das endgültige Bundle in der Sequenz so konfigurieren, dass a\) auf unbestimmte Zeit angezeigt wird (Standard) oder b\) zum ersten Bundle zurückkehrt. Sie können beispielsweise eines der Kreativen in Bundle 1 für drei (3) Impressions anzeigen, dann ein Kreatives in Bundle 2 für eine (1) Impression anzeigen, dann eines der Kreativen in Bundle 3 für zwei (2) Impressionen anzeigen und dann die Schleife erneut starten. Alternativ können Sie, sobald die Kreativen in Bundle 3 angezeigt werden, die Kreativen in Bundle 3 weiterhin auf unbestimmte Zeit anzeigen, anstatt eine Schleife zu erstellen. Beim Aktivieren der Sequenzierung:

         1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

            Standardmäßig werden die zugewiesenen Bundles in der Reihenfolge sortiert, in der sie zum Erlebnis hinzugefügt wurden.

         1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

         1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Für jeden zusätzlichen Zeitplan:

   1. Klicken Sie auf **[!UICONTROL + Add Schedule]**.

   1. Aktivieren Sie in der linken Spalte das Kontrollkästchen neben jedem Kreativen, der dem ersten Zeitplan hinzugefügt werden soll.

   1. Geben Sie das Start- und Enddatum für den Zeitplan an.

   1. Wählen Sie den Kreativ-Rotationstyp aus:

      * *[!UICONTROL Weighted]:* Dreht die Kreativen manuell entsprechend der relativen Gewichtung. Geben Sie die Gewichtung für jeden Kreativen in Prozent ein. Die Gewichtungen aller ausgewählten Kreativen müssen bis zu 100 betragen.

      * *[!UICONTROL Algorithmic]:* Dreht die Kreativen algorithmisch entsprechend einem angegebenen Optimierungsziel.

         * Wählen Sie für die **[!UICONTROL Optimization Goal]** entweder *[!UICONTROL Click Through Rate]* oder *[!UICONTROL Custom Objective]* aus.  Wenn Sie *[!UICONTROL Custom Objective]* auswählen, wählen Sie ein vorhandenes [benutzerdefiniertes Advertising DSP-Ziel aus](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

      * *[!UICONTROL Sequencing]:* Dreht die zugehörigen Kreativ-Bundles in einer bestimmten Reihenfolge mit einer angegebenen Gesamtzahl von Impressionen über jede Bundle-Sequenz hinweg. Beim Aktivieren der Sequenzierung:

         1. Ziehen Sie die zugewiesenen Bundles in die gewünschte Reihenfolge.

            Standardmäßig werden die zugewiesenen Bundles in der Reihenfolge sortiert, in der sie zum Erlebnis hinzugefügt wurden.

         1. Geben Sie die Anzahl der Impressionen für jede Sequenz ein.

         1. Ändern Sie für die letzte Sequenz, ob Sie a\) das letzte Bundle in der Sequenz auf unbestimmte Zeit anzeigen möchten (*[!UICONTROL Infinite]* (Standard) oder b\), bevor Sie zum ersten Bundle zurückkehren, nachdem das letzte Bundle angezeigt wurde (*[!UICONTROL Keep in Loop]*).

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Manuelles Erstellen eines Anzeigen-Tags für eine entsprechende Kreativgröße](/help/creative/experiences/experience-tag-create-manually.md)
>* [Zuweisen von Kreativen zu einem Anzeigen-Tag für Erlebnisse ohne Targeting](experience-tag-assign-creatives.md)
>* [Anpassen der Tracking-URLs für ein Erlebnis ohne Targeting mit Entscheidungsbaum](experience-tracking-urls-no-targeting.md)
