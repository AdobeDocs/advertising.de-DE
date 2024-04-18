---
title: Verwalten von Angebotsmultiplikatoren für Platzierungen
description: Erfahren Sie, wie Sie Angebotsmultiplikatoren für bestimmte Platzierungsziele erstellen und bearbeiten.
feature: DSP Placements
source-git-commit: b3932c066e0ecd29e57152f0654ee4b0d9e0dda1
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 3%

---

# Verwalten von Angebotsmultiplikatoren für Platzierungen

Mit dieser Funktion können Sie die Angebotsmultiplikatoren für Ihre vorhandenen Platzierungsziele ändern. Sie können die Angebotsmultiplikatoren für jeweils eine Platzierung verwalten.<!-- remove that line once we can edit multiple -->

Informationen zum Ändern der ausgewählten Ziele für Ihre Platzierungen finden Sie unter[Eine Platzierung bearbeiten](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Verschieben nach [Zielgruppenspezifischer Tab](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], und [!UICONTROL Brand Safety]) und bearbeiten Sie die vorhandenen Werte für die Platzierungsziele. Die meisten Zielkategorien listen links Unterkategorien auf. Klicken Sie auf eine Unterkategorie, um Angebotsmultiplikatoren für diese Unterkategorie zu verwalten, sofern zutreffend.

   Standardmäßig beträgt der Angebotsmultiplikator für eine Zielgruppe 1,00, was bedeutet, dass das Angebot nicht an diese Zielgruppe angepasst wird. Die Werte können zwischen 0,10 und 10,00 liegen. Beispielsweise reduziert ein Angebotsmodifikator von 0,5 ein Angebot von 6 USD auf 3 USD (0,5 x 6). Angebotsmodifikatoren erhöhen das Angebot nie auf mehr als das Höchstangebot.

   Wenn eine Auktion für mehrere Angebotsmodifikatoren qualifiziert ist, werden alle anwendbaren Angebotsmodifikatoren multipliziert.

   Sie können Angebotsmultiplikatoren (mit anderen Werten als 1,00) für eine [begrenzte Anzahl von Zielen](#bid-multiplier-limits-by-target).

1. Klicken Sie oben rechts auf **[!UICONTROL Save]**.

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
>* [Eine Platzierung bearbeiten](placement-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
