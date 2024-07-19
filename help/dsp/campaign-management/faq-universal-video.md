---
title: Häufig gestellte Fragen zu universellen Videos
description: Erfahren Sie mehr über universelle Videoanzeigen.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Häufig gestellte Fragen zu universellen Videos

[Universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-about.md#ad-types) ermöglichen es Ihnen, den Videobasis aus Desktop-, Mobil- und vernetzten TV-Umgebungen für VPAID- und VAST-Bestände mithilfe einer einzigen Videoplatzierung gezielt anzusprechen.

## Wie werden universelle Videoplatzierungen und -anzeigen erstellt?

Universelle Videoplatzierungen können nur universelle Videoanzeigen enthalten und universelle Videoanzeigen können nur an universelle Videoplatzierungen angehängt werden.

Erstellen Sie universelle Videoplatzierungen und -anzeigen ähnlich wie bei der Erstellung anderer Platzierungs- und Videotypen:

1. Erstellen Sie innerhalb der gewünschten Kampagne [eine universelle Videoplatzierung](/help/dsp/campaign-management/placements/placement-create.md) und wählen Sie die Option [!UICONTROL Placement Type] **[!UICONTROL Universal Video]** aus.

   Sie müssen mindestens eine Umgebung (Desktop, Mobile, Connected TV) für die Zielgruppenbestimmung angeben.

1. Erstellen Sie in derselben Kampagne wie die Platzierung für universelle Videos [ eine einzelne universelle Videoanzeige](/help/dsp/campaign-management/ads/ad-create.md) oder [ mehrere universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Wenn Sie mehrere Anzeigen erstellen, geben Sie &quot;[!UICONTROL Universal Video]&quot;als [!UICONTROL Ad Type] an:

   * Für Anzeigen des Typs [!DNL Google] oder [!DNL Flashtalking]: Klicken Sie im Schritt &quot;[!UICONTROL Review ad types]&quot; nach dem Hochladen der Datei auf das Feld **[!UICONTROL Ad Type]** und wählen Sie **[!UICONTROL Universal Video]** aus.

   * Für andere Arten von Anzeigen-Tags: Geben Sie in der hochgeladenen Tabellendatei für jede Anzeige das Feld Anzeigentyp als **[!UICONTROL Universal Video]** an.

1. [Öffnen Sie die Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-edit.md) für jede neue Anzeige und wählen Sie das entsprechende Videoformat aus:

   * **[!UICONTROL VPAID]:** Die Sichtbarkeit wird immer gemessen.
   * **[!UICONTROL VPAID & VAST (Default)]:** Umfasst Inventar, das keine Sichtbarkeitsmessung zulässt.
   * **[!UICONTROL VAST]** - Geeignet für angeschlossene TV-Bestände.

   Weitere Informationen finden Sie unter &quot;[Einstellungen für universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot;.

1. [Hängen Sie die neuen universellen Videoanzeigen](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) an die universelle Videoplatzierung an.

## Warum sind einige Optimierungsziele und -pakete nicht verfügbar, wenn die Umgebung &quot;Connected TV&quot;für eine universelle Videoplatzierung ausgewählt ist?

Ziele, die mit standardmäßigen vernetzten TV-Platzierungen inkompatibel sind, z. B. niedrigste Kosten pro Klick, werden für die vernetzte TV-Umgebung bei universellen Videoplatzierungen nicht unterstützt. Ebenso sind Pakete mit inkompatiblen Optimierungszielen nicht zur Auswahl verfügbar.

## Wann sollte das **[!UICONTROL VAST]**-Videoformat für universelle Videoanzeigen verwendet werden?

Verwenden Sie **[!UICONTROL VAST]** in einem der folgenden Szenarien:

* Die Platzierung zielt auf angeschlossene TV-Inventare ab.
* Die Platzierung dient der Bestimmung des Videoinventars von Google Ad Manager, Appnexus, SpotX oder Freewheel. Diese SSPs unterstützen das VPAID- und VAST-Videoformat nicht.

## Ist es möglich, mehrere universelle Videoanzeigen an dieselbe universelle Videoplatzierung anzuhängen?

Ja.
