---
title: Bearbeiten von Anzeigenplänen für Platzierungen
description: Erfahren Sie, wie Sie die Anzeigenzeitpläne für die an Platzierungen angehängten Anzeigen ändern.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Bearbeiten von Anzeigenplänen für Platzierungen

## Bearbeiten der Anzeigenzeitpläne für eine oder mehrere Platzierungen

Sie können die geplanten Flugdaten und die Anzeigenrotation für die Anzeigen, die an mehreren Platzierungen angehängt sind, mithilfe einer [!DNL Microsoft Excel] Tabelle ändern. Jede Anzeige kann während mehrerer Flüge aktiv sein.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Platzierung, deren Anzeigendaten Sie herunterladen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Wenn die Datei verfügbar ist, klicken Sie in der Benachrichtigung oben auf der Browser-Seite auf **[!UICONTROL Download]** , um eine Arbeitsblattdatei (im XLSX-Format) gemäß dem normalen Verfahren Ihres Browsers herunterzuladen.

   ![Fertige Benachrichtigung herunterladen](/help/dsp/assets/download-ready.png "Fertige Benachrichtigung herunterladen")

1. Öffnen Sie die heruntergeladene Datei, bearbeiten Sie die Fluginformationsfelder für jede Anzeigenzeile, die in den Flug aufgenommen werden soll, und speichern Sie die aktualisierte Datei:

   * **[!UICONTROL Flight N Start Date]**/**[!UICONTROL Flight N End Date]** (z. B. [!UICONTROL Flight 1 Start Date] und [!UICONTROL Flight 1 End Date]): Das erste und letzte Datum des Fluges. Verwenden Sie für jedes Datum das Format JJJJ-MM-TT. Alle Anzeigen mit leeren Flugdatumsfeldern werden als nicht teilnehmende Anzeigen behandelt.

   * **[!UICONTROL Flight N Weight]** (z. B. [!UICONTROL Flight 1 Weight]): Drehen der Anzeigen für einen Flug. Wert eingeben:

      * Um die Anzeigen für einen Flug gleichmäßig zu drehen, geben Sie `[!UICONTROL Even]` ein.

      * Um die Anzeigen für einen Flug ungleichmäßig zu drehen, geben Sie das relative Gewicht ein, um das jede Anzeige gedreht werden soll, als Prozentsatz (z. B. `40` für 40 %). Die Gesamtgewichte für den Flug müssen 100 betragen.

1. Laden Sie die bearbeitete Anzeigenplanvorlage hoch:

   1. Aktivieren Sie das Kontrollkästchen neben jeder entsprechenden Platzierung.

   1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]** und geben Sie die hochzuladende Datei an.

## Bearbeiten des Anzeigenplans für eine einzelne Platzierung

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

Sie können die geplanten Flugdaten und die Anzeigenrotation für die Anzeigen ändern, die einer Platzierung angehängt sind. Jede Anzeige kann während mehrerer Flüge aktiv sein.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Um einen Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]** und geben Sie dann das Start- und Enddatum an.

   * Um einen vorhandenen Flug zu einer Anzeige hinzuzufügen, klicken Sie in der Anzeigenzeile für die Spalte Flug auf **[!UICONTROL +]**.

   * Um einen vorhandenen Flug aus einer Anzeige zu entfernen, klicken Sie in der Anzeigenzeile für die Spalte Flug auf **[!UICONTROL x]**.

      * (Wenn mehrere Anzeigen denselben Flug haben) Um die Anzeigen ungleichmäßig zu drehen, klicken Sie in den Fluginformationen auf **[!UICONTROL Even Rotation]** und geben Sie dann das relative Gewicht, um das jede Anzeige gedreht werden soll, als Prozentsatz ein.

        Die Gesamtgewichte müssen 100 betragen.

1. Klicken Sie oben rechts auf **[!UICONTROL Continue]**.

1. Überprüfen Sie die Flugdetails und klicken Sie dann auf **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
