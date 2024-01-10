---
title: Bearbeiten von Anzeigenplänen für Platzierungen
description: Erfahren Sie, wie Sie die Anzeigenzeitpläne für die Anzeigen ändern, die an Platzierungen angehängt sind.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: d993ffe4a7dceed36ecbae85642e82de271432cd
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Bearbeiten von Anzeigenplänen für Platzierungen

## Bearbeiten von Anzeigenplänen für eine oder mehrere Platzierungen

Sie können die geplanten Flugdaten und die Anzeigenrotation für die Anzeigen ändern, die an mehrere Platzierungen angehängt sind, indem Sie eine [!DNL Microsoft Excel] Tabelle. Jede Anzeige kann während mehrerer Flüge aktiv sein.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Platzierung, deren Anzeigendaten Sie herunterladen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Wenn die Datei verfügbar ist, klicken Sie auf **[!UICONTROL Download]** in der Benachrichtigung oben auf der Browser-Seite, um eine Arbeitsblattdatei (im XLSX-Format) gemäß der üblichen Vorgehensweise Ihres Browsers herunterzuladen.

   ![Herunterladen von vorbereitenden Benachrichtigungen](/help/dsp/assets/download-ready.png "Herunterladen von vorbereitenden Benachrichtigungen")

1. Öffnen Sie die heruntergeladene Datei, bearbeiten Sie die Fluginformationen nach Bedarf und speichern Sie die aktualisierte Datei:

   * Um einen Flug hinzuzufügen, geben Sie mithilfe der **[!UICONTROL Flight N Start Date]** und **[!UICONTROL Flight N End Date]** Spalten. Verwenden Sie für jedes Datum das Format JJJJ-MM-TT .

     Geben Sie beispielsweise für Anzeigen im ersten Flug Werte in die [!UICONTROL Flight 1 Start Date] und [!UICONTROL Flight 1 End Date] -Felder. Wenn die Anzeigenzeilen nicht bereits in der Datei enthalten sind, geben Sie die erforderlichen Anzeigeninformationen in neue Zeilen ein.

     Alle Anzeigen mit leeren Flugdatumsfeldern werden als nicht teilnehmende Anzeigen behandelt.

   * Um die Anzeigen für einen Flug gleichmäßig zu drehen, geben Sie &quot;**[!UICONTROL Even]**&quot; in den einschlägigen **[!UICONTROL Flight N Weight]** -Felder (z. B. [!UICONTROL Flight 1 Weight]).

   * Um die Anzeigen für einen Flug ungleichmäßig zu drehen, geben Sie das relative Gewicht, um das jede Anzeige gedreht werden soll, in Prozent in die entsprechende **[!UICONTROL Flight N Weight]** -Felder (z. B. [!UICONTROL Flight 1 Weight]).

     Die Gesamtgewichte für jeden Flug müssen 100 betragen.

1. Laden Sie die bearbeitete Anzeigenplanvorlage hoch:

   1. Aktivieren Sie das Kontrollkästchen neben jeder entsprechenden Platzierung.

   1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]** und geben Sie die hochzuladende Datei an.

## Bearbeiten des Anzeigenzeitplans für eine einzelne Platzierung

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

Sie können die geplanten Flugdaten und die Anzeigenrotation für die Anzeigen ändern, die mit einer Platzierung verbunden sind. Jede Anzeige kann während mehrerer Flüge aktiv sein.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

   1. Führen Sie einen der folgenden Schritte aus:

      * Um einen Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]** und geben Sie dann das Start- und Enddatum an.

      * Um einen vorhandenen Flug zu einer Anzeige hinzuzufügen, klicken Sie auf **[!UICONTROL +]** in der Anzeigenzeile für die Flugspalte.

      * Um einen vorhandenen Flug aus einer Anzeige zu entfernen, klicken Sie auf **[!UICONTROL x]** in der Anzeigenzeile für die Flugspalte.

      * (Wenn mehrere Anzeigen denselben Flug haben) Um die Anzeigen ungleichmäßig zu drehen, klicken Sie auf **[!UICONTROL Even Rotation]** in den Fluginformationen und geben Sie dann die relative Gewichtung der einzelnen Anzeigen in Prozent an.

        Die Gesamtgewichte müssen 100 betragen.

   1. Klicken Sie oben rechts auf **[!UICONTROL Continue]**.

   1. Überprüfen Sie die Flugdetails und klicken Sie dann auf **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Eine Platzierung bearbeiten](placement-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
