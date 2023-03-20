---
title: Häufig gestellte Fragen zu universellen Videos
description: Erfahren Sie mehr über universelle Videoanzeigen.
feature: DSP Placements, DSP Ads
source-git-commit: fe5340cbf495eb9498d89c18080307464d4067d9
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Häufig gestellte Fragen zu universellen Videos

## Wie werden universelle Videoplatzierungen und -anzeigen erstellt?

Universelle Videoplatzierungen können nur universelle Videoanzeigen enthalten und universelle Videoanzeigen können nur an universelle Videoplatzierungen angehängt werden.

Erstellen Sie sie ähnlich wie andere Platzierungs- und Videotypen:

1. Innerhalb der gewünschten Kampagne, [Erstellen einer universellen Videoplatzierung](/help/dsp/campaign-management/placements/placement-create.md), die [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Sie müssen mindestens eine Umgebung (Desktop, Mobil, vernetztes TV) angeben, um das Ziel zu erreichen.

1. In derselben Kampagne wie der Platzierung für universelle Videos [einzelne universelle Videoanzeige erstellen](/help/dsp/campaign-management/ads/ad-create.md) oder [Erstellen mehrerer universeller Videoanzeigen](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Wenn Sie mehrere Anzeigen erstellen, geben Sie &quot;[!UICONTROL Universal Video]&quot; als [!UICONTROL Ad Type]:

   * Für [!DNL Google] oder [!DNL Flashtalking] Anzeigen: Im[!UICONTROL Review ad types]&quot; Schritt nach dem Hochladen der Datei klicken Sie auf das **[!UICONTROL Ad Type]** Feld und wählen Sie **[!UICONTROL Universal Video]**.

   * Für andere Arten von Anzeigen-Tags: Geben Sie in der hochgeladenen Tabellendatei für jede Anzeige das Feld Anzeigentyp als **[!UICONTROL Universal Video]**.

1. [Öffnen Sie die Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-edit.md) für jede neue Anzeige und wählen Sie das entsprechende Videoformat aus:

   * **[!UICONTROL VPAID]:** Die Sichtbarkeit wird immer gemessen.
   * **[!UICONTROL VPAID & VAST (Default)]:** Umfasst Inventar, das keine Sichtbarkeitsmessung zulässt.
   * **[!UICONTROL VAST]** - geeignet für angeschlossene TV-Inventare.

   Siehe[Universelle Videoanzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot;.

1. [Neue universelle Videoanzeigen anhängen](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) zur universellen Videoplatzierung.

## Warum sind einige Optimierungsziele und -pakete nicht verfügbar, wenn die Umgebung &quot;Connected TV&quot;für eine universelle Videoplatzierung ausgewählt ist?

Ziele, die mit standardmäßigen vernetzten TV-Platzierungen inkompatibel sind, z. B. niedrigste Kosten pro Klick, werden für die vernetzte TV-Umgebung bei universellen Videoplatzierungen nicht unterstützt. Ebenso sind Pakete mit inkompatiblen Optimierungszielen nicht zur Auswahl verfügbar.

## Wann sollte die **[!UICONTROL VAST]** Videoformat für universelle Videoanzeigen?

Verwendung **[!UICONTROL VAST]** in einem der folgenden Szenarien:

* Die Platzierung zielt auf angeschlossene TV-Inventare ab.
* Die Platzierung richtet sich an die Videoinventarisierung aus Google Ad Manager, Appnexus, SpotX oder Freewheel. Diese SSPs unterstützen das VPAID- und VAST-Videoformat nicht.

## Ist es möglich, mehrere universelle Videoanzeigen an dieselbe universelle Videoplatzierung anzuhängen?

Ja.
