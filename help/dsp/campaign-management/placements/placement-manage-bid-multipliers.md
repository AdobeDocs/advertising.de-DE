---
title: Verwalten von Angebotsmultiplikatoren für Platzierungen
description: Erfahren Sie, wie Sie Angebotsmultiplikatoren für Ihre Platzierungsziele erstellen und bearbeiten.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 28f1b799daaa4e511abab1102a639e72b3a32d18
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Verwalten von Angebotsmultiplikatoren für Platzierungen

Sie können Angebotsmultiplikatoren erstellen und verwalten, mit denen ein algorithmisch berechnetes Angebot multipliziert wird, um das Angebot zu erhöhen oder zu verringern, und zwar für Ihre vorhandenen Platzierungsziele von [geeigneten Zieltypen](#bid-multiplier-by-target). Sie können entweder Angebotsmultiplikatorwerte für eine Platzierung manuell bearbeiten oder eine Tabelle mit Werten für eine oder mehrere Platzierungen hochladen.

Standardmäßig beträgt der Angebotsmultiplikator für eine Zielgruppe 1,00, was bedeutet, dass das Angebot nicht an diese Zielgruppe angepasst wird. Die Werte können zwischen 0,10 und 10,00 liegen. Beispielsweise senkt ein Angebotsmultiplikator von 0,5 ein Angebot von 6 USD auf 3 USD (0,5 x 6). Wenn eine Auktion für mehrere Angebotsmodifikatoren qualifiziert ist, werden alle anwendbaren Angebotsmultiplikatoren multipliziert. Wenn beispielsweise Kalifornien einen Angebotsmultiplikator von 2 hat und San Francisco einen Angebotsmultiplikator von 3 hat, dann ist der letzte Angebotsmultiplikator für Anzeigen, die in San Francisco ausgeführt werden, 6.

>[!NOTE]
>
>Angebotsmultiplikatoren erhöhen das Angebot nie auf mehr als das Höchstangebot.

Sie können Angebotsmultiplikatoren (mit anderen Werten als 1,00) für eine [begrenzte Anzahl von Zielen](#bid-multiplier-limits-by-target) festlegen.

Diese Funktion funktioniert mit Ihren vorhandenen Platzierungszielen. Informationen zum Ändern der ausgewählten Ziele für Ihre Platzierungen finden Sie unter &quot;[Platzierungen bearbeiten](/help/dsp/campaign-management/placements/placement-edit.md)&quot;.

## Verwalten der Angebotsmultiplikatoren für eine einzelne Platzierung

Sie können Werte entweder manuell bearbeiten oder eine Tabelle für eine einzelne Platzierung hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Passen Sie die Angebotsmultiplikatoren für die förderfähigen Ziele an:

   * Um die Werte des Angebotsmultiplikators manuell anzupassen, wechseln Sie zu jedem [zielspezifischen Tab](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience] und [!UICONTROL Brand Safety]) und bearbeiten Sie die vorhandenen Werte für die Platzierungsziele.

     Die meisten Zielkategorien listen links Unterkategorien auf. Klicken Sie auf eine Unterkategorie, um Angebotsmultiplikatoren für diese Unterkategorie zu verwalten.

   * So laden Sie eine CSV-Datei mit Angebotsmultiplikatorwerten hoch, um alle vorhandenen Werte zu überschreiben:

      1. Klicken Sie oben rechts auf &quot;**[!UICONTROL CSV File Edit]**&quot;.

      1. a) Klicken Sie auf &quot;**[!UICONTROL Download Template]**&quot;und bearbeiten Sie die Datei oder b) bearbeiten Sie eine zuvor heruntergeladene Vorlage. Speichern Sie die bearbeitete Datei auf Ihrem Gerät oder Netzwerk.

         Die heruntergeladenen Tabellen enthalten ein Blatt für jeden Zieltyp (z. B. Land, Quellen und Site-Kategorie). Es werden nur bestehende Angebotsmultiplikatoren mit Werten &lt; 1,0 oder > 1,0 einbezogen.

         * Um einen Angebotsmultiplikator für eine vorhandene Zielgruppe hinzuzufügen, geben Sie die Zielgruppe unter Verwendung der gleichen Syntax ein, die in der Benutzeroberfläche sichtbar ist, und des entsprechenden Angebotsmultiplikatorwerts.

         * Um einen Angebotsmodifikator zu entfernen, setzen Sie den Angebotsmultiplikatorwert auf 1,0 oder löschen Sie alle Informationen für die Zeile.

         ![Beispielzeile in einer Tabellendatei mit Angebotsmultiplikator](/help/dsp/assets/bid-multiplier-spreadsheet.png "Beispielzeile in einer Tabellendatei mit Angebotsmultiplikator")

      1. Klicken Sie auf &quot;**[!UICONTROL Next]**&quot;, um zum Abschnitt &quot;[!UICONTROL Upload File]&quot; zu wechseln. Ziehen Sie die bearbeitete Datei per Drag-and-Drop in das Feld oder klicken Sie in das Feld, um die Datei von Ihrem Gerät oder Netzwerk auszuwählen.

      1. Überprüfen Sie die hochgeladenen Daten im Abschnitt [!UICONTROL Review & Submit] und klicken Sie dann auf **[!UICONTROL Save]**.

## Hochladen von Angebotsmultiplikatoren für eine oder mehrere Platzierungen

Laden Sie eine Tabelle hoch, um dieselben Werte auf alle ausgewählten Platzierungen anzuwenden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Platzierung, deren Angebotsmultiplikatoren Sie verwalten möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. Laden Sie eine CSV-Datei mit Angebotsmultiplikatorwerten hoch, um alle vorhandenen Werte für alle ausgewählten Platzierungen zu überschreiben.

   1. a) Klicken Sie auf &quot;**[!UICONTROL Download Template]**&quot;und bearbeiten Sie die Datei oder b) bearbeiten Sie eine zuvor heruntergeladene Vorlage. Speichern Sie die bearbeitete Datei auf Ihrem Gerät oder Netzwerk.

      Die heruntergeladenen Tabellen enthalten ein Blatt für jeden Zieltyp (z. B. Land, Quellen und Site-Kategorie). Es werden nur bestehende Angebotsmultiplikatoren mit Werten &lt; 1,0 oder > 1,0 einbezogen.

      * Um einen Angebotsmultiplikator für eine vorhandene Zielgruppe hinzuzufügen, geben Sie die Zielgruppe unter Verwendung der gleichen Syntax ein, die in der Benutzeroberfläche sichtbar ist, und des entsprechenden Angebotsmultiplikatorwerts.

      * Um einen Angebotsmodifikator zu entfernen, setzen Sie den Angebotsmultiplikatorwert auf 1,0 oder löschen Sie alle Informationen für die Zeile.

      ![Beispielzeile in einer Tabellendatei mit Angebotsmultiplikator](/help/dsp/assets/bid-multiplier-spreadsheet.png "Beispielzeile in einer Tabellendatei mit Angebotsmultiplikator")

   1. Klicken Sie auf &quot;**[!UICONTROL Next]**&quot;, um zum Abschnitt &quot;[!UICONTROL Upload File]&quot; zu wechseln. Ziehen Sie die bearbeitete Datei per Drag-and-Drop in das Feld oder klicken Sie in das Feld, um die Datei von Ihrem Gerät oder Netzwerk auszuwählen.

   1. Überprüfen Sie die hochgeladenen Daten im Abschnitt [!UICONTROL Review & Submit] und klicken Sie dann auf **[!UICONTROL Save]**.

## Für Angebotsmultiplikatoren geeignete Zieltypen {#bid-multiplier-by-target}

Sie können Angebotsmodifikatoren nur für enthaltene Ziele, nicht für ausgeschlossene Ziele konfigurieren.

* **Geoziele**: Geografie (Länder, Bundesländer und Städte), Postleitzahlen und DMAs

* **Inventarziele**: Quellen und Feeds für den öffentlichen Bestand und [!UICONTROL On Demand] Inventar

* **Site-Ziele:** zielgerichtete (aber nicht ausgeschlossene) Sites/Apps, Site-Kategorien

* **Zielgruppenziele:** Segmente, Dayparts und Themen

* **ads.txt-Ziele:** (Wenn Sie ads.txt abwählen, was es Ihnen ermöglicht, Inventar von allen Verkäufern zu kaufen) Nur ads.txt sellers, ads.txt direct sellers und ads.txt sellers plus sites ohne ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Maximale Anzahl der Angebotsmultiplikatoren nach Zieltyp {#bid-multiplier-limits-by-target}

Sie können Angebotsmultiplikatoren (mit anderen Werten als 1,00) für eine begrenzte Anzahl von Zielen festlegen. Sie können beispielsweise Angebotsmultiplikatoren für bis zu 20 Länderziele festlegen. Die maximale Anzahl von Zielen für jeden Zieltyp, der über Gebotsmultiplikatoren verfügen kann, ist unten aufgeführt.

| Kategorie | Parameter | Höchstzahl |
| -------- | --------- | ----- |
| Geo | Land | 20 |
| Geo | Bundesland | 100 |
| Geo | Ort | 100 |
| Geo | Metro | 100 |
| Geo | Postleitzahlen | 100 |
| Bestand | Quellen | 100 |
| Bestand | Feeds | 100 |
| Sites | Site-Kategorie | 100 |
| Sites | Sites/Apps | 100 |
| Zielgruppe | Segmente | 500 |
| Zielgruppe | Themen | 100 |
| Markensicherheit | Ads.txt | Nicht zutreffend |

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
