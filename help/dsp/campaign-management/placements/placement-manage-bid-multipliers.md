---
title: Verwalten von Angebotsmultiplikatoren für Platzierungen
description: Erfahren Sie, wie Sie Angebotsmultiplikatoren für Ihre Platzierungsziele erstellen und bearbeiten.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 2c6e21dd63c5d0c8e0d0c82bcacd0851c56c6084
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 2%

---

# Verwalten von Angebotsmultiplikatoren für Platzierungen

Sie können Angebotsmultiplikatoren erstellen und verwalten, mit denen ein Angebot multipliziert wird, um das Angebot zu erhöhen oder zu verringern, und zwar für Ihre vorhandenen Platzierungsziele von [förderfähige Zieltypen](#bid-multiplier-by-target). Sie können entweder Angebotsmultiplikatorwerte manuell bearbeiten oder eine Tabelle mit Werten hochladen.

Standardmäßig beträgt der Angebotsmultiplikator für eine Zielgruppe 1,00, was bedeutet, dass das Angebot nicht an diese Zielgruppe angepasst wird. Die Werte können zwischen 0,10 und 10,00 liegen. Beispielsweise reduziert ein Angebotsmodifikator von 0,5 ein Angebot von 6 USD auf 3 USD (0,5 x 6). Wenn eine Auktion für mehrere Angebotsmodifikatoren qualifiziert ist, werden alle anwendbaren Angebotsmodifikatoren multipliziert. Angebotsmodifikatoren erhöhen das Angebot nie auf mehr als das Höchstangebot.

Sie können Angebotsmultiplikatoren (mit anderen Werten als 1,00) für eine [begrenzte Anzahl von Zielen](#bid-multiplier-limits-by-target).

Diese Funktion funktioniert mit Ihren vorhandenen Platzierungszielen. Informationen zum Ändern der ausgewählten Ziele für Ihre Platzierungen finden Sie unter[Platzierungen bearbeiten](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Passen Sie die Angebotsmultiplikatoren für die förderfähigen Ziele an:

   * Um die Werte des Angebotsmultiplikators manuell anzupassen, wechseln Sie zu jedem [Zielgruppenspezifischer Tab](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], und [!UICONTROL Brand Safety]) und bearbeiten Sie die vorhandenen Werte für die Platzierungsziele.

     Die meisten Zielkategorien listen links Unterkategorien auf. Klicken Sie auf eine Unterkategorie, um Angebotsmultiplikatoren für diese Unterkategorie zu verwalten.

   * So laden Sie eine CSV-Datei mit Angebotsmultiplikatorwerten hoch, um alle vorhandenen Werte zu überschreiben:

      1. Klicks **[!UICONTROL CSV File Edit]** oben rechts.

      1. Klicken Sie entweder a) **[!UICONTROL Download Template]** und bearbeiten Sie die Datei oder b) bearbeiten Sie eine zuvor heruntergeladene Vorlage. Speichern Sie die bearbeitete Datei auf Ihrem Gerät oder Netzwerk.

         Heruntergeladene Vorlagen enthalten für jeden Zieltyp (z. B. Land, Quellen und Site-Kategorie) eine Tabelle. Es werden nur bestehende Angebotsmultiplikatoren mit anderen Werten als 1.0 einbezogen.

         * Um einen Angebotsmultiplikator für eine vorhandene Zielgruppe hinzuzufügen, geben Sie die Zielgruppe unter Verwendung der gleichen Syntax ein, die in der Benutzeroberfläche sichtbar ist, und des entsprechenden Angebotsmultiplikatorwerts.

         * Um einen Angebotsmodifikator zu entfernen, setzen Sie den Angebotsmultiplikatorwert auf 1,0 oder löschen Sie alle Informationen für die Zeile.

         ![Beispielzeile in einer Tabelle mit Angebotsmultiplikatoren](/help/dsp/assets/bid-multiplier-spreadsheet.png "Beispielzeile in einer Tabelle mit Angebotsmultiplikatoren")

      1. Klicks **[!UICONTROL Next]** , um zum [!UICONTROL Upload File] und entweder a) ziehen Sie die bearbeitete Datei in das Feld oder b) klicken Sie in das Feld, um die Datei von Ihrem Gerät oder Netzwerk auszuwählen.

      1. Überprüfen Sie die hochgeladenen Daten im [!UICONTROL Review & Submit] und klicken Sie anschließend auf **[!UICONTROL Save]**.

## Für Angebotsmultiplikatoren geeignete Zieltypen {#bid-multiplier-by-target}

Sie können Angebotsmodifikatoren nur für enthaltene Ziele, nicht für ausgeschlossene Ziele konfigurieren.

* **Geo-Ziele**: Geografie (Länder, Bundesländer und Städte), Postleitzahlen und DMAs

* **Inventarziele**: Quellen und Feeds für das öffentliche Inventar und [!UICONTROL On Demand] inventory

* **Site-Ziele:** zielgerichtete (aber nicht ausgeschlossene) Sites/Apps, Site-Kategorien

* **Zielgruppenziele:** Segmente, Dayparting und Themen

* **ads.txt-Ziele:** (Wenn Sie sich von ads.txt abmelden, was es Ihnen ermöglicht, Inventar von allen Verkäufern zu kaufen), nur ads.txt sellers, ads.txt direct sellers und ads.txt sellers plus sites ohne ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

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
