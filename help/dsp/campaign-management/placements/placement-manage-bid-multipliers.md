---
title: Verwalten von Angebotsmultiplikatoren für Platzierungen
description: Erfahren Sie, wie Sie Angebotsmultiplikatoren für Ihre Platzierungsziele erstellen und bearbeiten.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Verwalten von Angebotsmultiplikatoren für Platzierungen

Sie können Angebotsmultiplikatoren erstellen und verwalten, mit denen ein algorithmisch berechnetes Angebot multipliziert wird, um das Angebot für Ihre vorhandenen Platzierungsziele (geeignete Zieltypen[ zu erhöhen oder zu ](#bid-multiplier-by-target). Sie können entweder die Werte des Angebotsmultiplikators für eine Platzierung manuell bearbeiten oder eine Tabelle mit Werten für eine oder mehrere Platzierungen hochladen.

Der Bid-Multiplikator für ein Ziel ist standardmäßig 1,00, was bedeutet, dass das Gebot nicht für dieses Ziel angepasst wird. Die Werte können zwischen 0,10 und 10,00 liegen. So verringert ein Gebotsmultiplikator von 0,5 ein Gebot von 6 USD auf 3 USD (0,5 x 6). Wenn sich eine Auktion für mehrere Angebotsmodifikatoren qualifiziert, werden alle entsprechenden Gebotsmultiplikatoren multipliziert. Wenn beispielsweise Kalifornien über einen Angebotsmultiplikator von 2 verfügt und San Francisco über einen Angebotsmultiplikator von 3, ist der letzte Angebotsmultiplikator für Anzeigen, die in San Francisco geschaltet werden, 6.

>[!NOTE]
>
>Angebotsmultiplikatoren erhöhen das Angebot nie auf mehr als das Höchstgebot.

Sie können Angebotsmultiplikatoren (mit Werten ungleich 1,00) für eine [begrenzte Anzahl von Zielen) ](#bid-multiplier-limits-by-target).

Diese Funktion funktioniert mit Ihren vorhandenen Platzierungszielen. Informationen zum Ändern der ausgewählten Ziele für Ihre Platzierungen finden Sie unter [Platzierungen bearbeiten](/help/dsp/campaign-management/placements/placement-edit.md).

## Verwalten der Angebotsmultiplikatoren für eine einzelne Platzierung

Sie können Werte entweder manuell bearbeiten oder eine Tabelle für eine einzelne Platzierung hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Edit]** > **[!UICONTROL Bid Multiplier]**.

1. Anpassen der Angebotsmultiplikatoren für geeignete Ziele:

   * Um die Werte des Angebotsmultiplikators manuell anzupassen, wechseln Sie zu jeder [zielspezifischen Registerkarte](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience] und [!UICONTROL Brand Safety]) und bearbeiten Sie die vorhandenen Werte für die Platzierungsziele.

     Die meisten Zielkategorien führen Unterkategorien auf der linken Seite auf. Klicken Sie auf eine Unterkategorie, um je nach Bedarf Angebotsmultiplikatoren für diese Unterkategorie zu verwalten.

   * So laden Sie eine CSV-Datei mit Bid-Multiplikatorwerten hoch, um alle vorhandenen Werte zu überschreiben:

      1. Klicken Sie oben rechts auf **[!UICONTROL CSV File Edit]** .

      1. Entweder a) auf **[!UICONTROL Download Template]** klicken und die Datei bearbeiten oder b) eine zuvor heruntergeladene Vorlage bearbeiten. Speichern Sie die bearbeitete Datei auf Ihrem Gerät oder Netzwerk.

         Heruntergeladene Arbeitsblätter enthalten ein Blatt für jeden Zieltyp (z. B. Land, Quellen und Site-Kategorie). Nur bestehende Gebotsmultiplikatoren mit Werten &lt; 1,0 oder > 1,0 werden einbezogen.

         * Um einen Angebotsmultiplikator für ein vorhandenes Ziel hinzuzufügen, geben Sie das Ziel mit derselben in der Benutzeroberfläche sichtbaren Syntax und dem entsprechenden Wert des Angebotsmultiplikators ein.

         * Um einen Angebotsmodifikator zu entfernen, setzen Sie den Wert des Angebotsmultiplikators auf 1,0 oder löschen Sie alle Informationen für die Zeile.

         ![Beispielzeile in einer Kalkulationstabellendatei mit Angebotsmultiplikator](/help/dsp/assets/bid-multiplier-spreadsheet.png "Beispielzeile in einer Kalkulationstabellendatei mit Angebotsmultiplikator")

      1. Klicken Sie auf **[!UICONTROL Next]** , um zum Abschnitt [!UICONTROL Upload File] zu wechseln, und entweder a) ziehen Sie die bearbeitete Datei per Drag-and-Drop in das Feld oder b) klicken Sie in das Feld, um die Datei auf Ihrem Gerät oder Netzwerk auszuwählen.

      1. Überprüfen Sie die hochgeladenen Daten im Abschnitt [!UICONTROL Review & Submit] und klicken Sie dann auf **[!UICONTROL Save]**.

## Hochladen von Angebotsmultiplikatoren für eine oder mehrere Platzierungen

Laden Sie eine Tabelle hoch, um dieselben Werte auf alle ausgewählten Platzierungen anzuwenden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Platzierung, deren Angebotsmultiplikatoren Sie verwalten möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. Laden Sie eine CSV-Datei mit Bid-Multiplikatorwerten hoch, um alle vorhandenen Werte für alle ausgewählten Platzierungen zu überschreiben.

   1. Entweder a) auf **[!UICONTROL Download Template]** klicken und die Datei bearbeiten oder b) eine zuvor heruntergeladene Vorlage bearbeiten. Speichern Sie die bearbeitete Datei auf Ihrem Gerät oder Netzwerk.

      Heruntergeladene Arbeitsblätter enthalten ein Blatt für jeden Zieltyp (z. B. Land, Quellen und Site-Kategorie). Nur bestehende Gebotsmultiplikatoren mit Werten &lt; 1,0 oder > 1,0 werden einbezogen.

      * Um einen Angebotsmultiplikator für ein vorhandenes Ziel hinzuzufügen, geben Sie das Ziel mit derselben in der Benutzeroberfläche sichtbaren Syntax und dem entsprechenden Wert des Angebotsmultiplikators ein.

      * Um einen Angebotsmodifikator zu entfernen, setzen Sie den Wert des Angebotsmultiplikators auf 1,0 oder löschen Sie alle Informationen für die Zeile.

      ![Beispielzeile in einer Kalkulationstabellendatei mit Angebotsmultiplikator](/help/dsp/assets/bid-multiplier-spreadsheet.png "Beispielzeile in einer Kalkulationstabellendatei mit Angebotsmultiplikator")

   1. Klicken Sie auf **[!UICONTROL Next]** , um zum Abschnitt [!UICONTROL Upload File] zu wechseln, und entweder a) ziehen Sie die bearbeitete Datei per Drag-and-Drop in das Feld oder b) klicken Sie in das Feld, um die Datei auf Ihrem Gerät oder Netzwerk auszuwählen.

   1. Überprüfen Sie die hochgeladenen Daten im Abschnitt [!UICONTROL Review & Submit] und klicken Sie dann auf **[!UICONTROL Save]**.

## Zieltypen, die für Angebotsmultiplikatoren geeignet sind {#bid-multiplier-by-target}

Angebotsmodifikatoren können nur für eingeschlossene, nicht für ausgeschlossene Ziele konfiguriert werden.

* **Geo-Ziele**: Geografie (Länder, Bundesstaaten und Städte), Postleitzahlen und DMAs

* **Inventarziele**: Quellen und Feeds für öffentliches Inventar und [!UICONTROL On Demand]

* **Site-Ziele:** zielgerichtete (aber nicht ausgeschlossene) Sites/Apps, Site-Kategorien

* **Zielgruppenziele:** Segmente, Dayparts und Themen

* **ads.txt-Ziele:** (Wenn Sie sich gegen ads.txt entscheiden, sodass Sie Inventar von allen Verkäufern kaufen können) ads.txt-Verkäufer, ads.txt-Direktverkäufer und ads.txt-Verkäufer plus Websites ohne ads.txt-<!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Maximale Anzahl an Angebotsmultiplikatoren nach Zieltyp {#bid-multiplier-limits-by-target}

Sie können für eine begrenzte Anzahl von Zielen Angebotsmultiplikatoren (mit Werten ungleich 1,00) festlegen. Beispielsweise können Sie Angebotsmultiplikatoren für bis zu 20 Länderziele festlegen. Die maximale Anzahl von Zielen für jeden Zieltyp, die Bid-Multiplikatoren haben können, ist unten aufgeführt.

| Kategorie | Parameter | Maximale Anzahl |
| -------- | --------- | ----- |
| Geo | Land | 20 |
| Geo | Bundesland | 100 |
| Geo | Stadt | 100 |
| Geo | U-Bahn | 100 |
| Geo | Postleitzahlen | 100 |
| Inventar | Quellen | 100 |
| Inventar | Feeds | 100 |
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
