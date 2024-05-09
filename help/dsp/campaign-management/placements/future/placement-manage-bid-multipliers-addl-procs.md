---
title: Verwalten von Angebotsmultiplikatoren für Platzierungen
description: Erfahren Sie, wie Sie Angebotsmultiplikatoren für bestimmte Platzierungsziele erstellen und bearbeiten.
feature: DSP Placements
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Verwalten von Angebotsmultiplikatoren für Platzierungen


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

Mit dieser Funktion können Sie die Angebotsmultiplikatoren für Ihre vorhandenen Platzierungsziele ändern.

Informationen zum Ändern der ausgewählten Ziele für Ihre Platzierungen finden Sie unter[Platzierungen bearbeiten](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Verwalten der Angebotsmultiplikatoren für eine oder mehrere Platzierungen

Bei allen ausgewählten Platzierungen können Sie entweder Werte manuell bearbeiten oder eine Tabelle mit Werten hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Platzierung, deren Angebotsmultiplikatoren Sie verwalten möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Passen Sie die Angebotsmultiplikatoren für die geeignete Zielgruppe manuell an oder indem Sie eine CSV-Datei mit Zielwerten hochladen:

   * Um die Werte des Angebotsmultiplikators manuell anzupassen, wechseln Sie zu jedem zielspezifischen Tab ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], und[!UICONTROL Brand Safety]) und bearbeiten Sie die vorhandenen Werte für die Platzierungsziele.

   Die gleichen Änderungen gelten für alle ausgewählten Platzierungen.

   * So laden Sie eine CSV-Datei mit Angebotsmultiplikatorwerten hoch, die die vorhandenen Werte überschreiben:

     >[!NOTE]
     >
     >Wenn Sie ein Feld leer lassen, werden alle Werte für diesen Zieltyp gelöscht.<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there will be only one data row applicable for all. -->

      1. Klicks **[!UICONTROL CSV Edit]** oben rechts.

      1. Klicken Sie entweder a) **[!UICONTROL Download Template]** und bearbeiten Sie die Angebotsmultiplikatorwerte oder b) bearbeiten Sie eine zuvor heruntergeladene Vorlage. Speichern Sie die bearbeitete Datei auf Ihrem Gerät oder Netzwerk.

      1. a) Ziehen Sie die bearbeitete Datei in das Feld oder b) klicken Sie in das Feld, um die Datei von Ihrem Gerät oder Netzwerk auszuwählen.

   1. Klicks **[!UICONTROL Upload]**.

   Standardmäßig beträgt der Angebotsmultiplikator für eine Zielgruppe 1,00, was bedeutet, dass das Angebot nicht an diese Zielgruppe angepasst wird. Die Werte können zwischen 0,10 und 10,00 liegen. Beispielsweise reduziert ein Angebotsmodifikator von 0,5 ein Angebot von 6 USD auf 3 USD (0,5 x 6). Sie können Angebotsmultiplikatoren (mit anderen Werten als 1,00) für eine [begrenzte Anzahl von Zielen](#bid-multiplier-limits-by-target).

   Wenn eine Auktion für mehrere Angebotsmodifikatoren qualifiziert ist, werden alle anwendbaren Angebotsmodifikatoren multipliziert.

   Angebotsmodifikatoren erhöhen das Angebot nie auf mehr als das Höchstangebot.

1. Klicks **[!UICONTROL Save]**.

-->

## Hochladen einer Tabelle zur Verwaltung der Angebotsmultiplikatoren für eine einzelne Platzierung<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

Änderungen in der hochgeladenen Datei überschreiben die vorhandenen Gebotsmultiplikatorwerte.<!-- what if you delete a row? -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. Klicken Sie entweder a) **[!UICONTROL Download Template]** und bearbeiten Sie die Angebotsmultiplikatorwerte oder b) bearbeiten Sie eine zuvor heruntergeladene Vorlage. Speichern Sie die bearbeitete Datei auf Ihrem Gerät oder Netzwerk.

   Standardmäßig beträgt der Angebotsmultiplikator für eine Zielgruppe 1,00, was bedeutet, dass das Angebot nicht an diese Zielgruppe angepasst wird. Die Werte können zwischen 0,10 und 10,00 liegen. Beispielsweise reduziert ein Angebotsmodifikator von 0,5 ein Angebot von 6 USD auf 3 USD (0,5 x 6). Sie können Angebotsmultiplikatoren (mit anderen Werten als 1,00) für eine [begrenzte Anzahl von Zielen](#bid-multiplier-limits-by-target).

   Wenn eine Auktion für mehrere Angebotsmodifikatoren qualifiziert ist, werden alle anwendbaren Angebotsmodifikatoren multipliziert.

   Angebotsmodifikatoren erhöhen das Angebot nie auf mehr als das Höchstangebot.

1. a) Ziehen Sie die bearbeitete Datei in das Feld oder b) klicken Sie in das Feld, um die Datei von Ihrem Gerät oder Netzwerk auszuwählen.

1. Klicks **[!UICONTROL Upload]**.

1. Klicks **[!UICONTROL Save]**.

## Für Angebotsmultiplikatoren geeignete Zieltypen {#bid-multiplier-by-target}

nicht hier auskippen

## Maximale Anzahl der Angebotsmultiplikatoren nach Zieltyp {#bid-multiplier-limits-by-target}

nicht hier auskippen

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
