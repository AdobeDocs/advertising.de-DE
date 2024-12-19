---
title: Häufig gestellte Fragen zum universellen Video
description: Erfahren Sie mehr über universelle Videoanzeigen.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Häufig gestellte Fragen zum universellen Video

[Universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-about.md#ad-types) ermöglichen es Ihnen, den Videobestand aus Desktop-, Mobile- und verbundenen TV-Umgebungen für VPAID- und VAST-Inventar mithilfe einer einzigen Videoplatzierung anzusprechen.

## Wie erstelle ich universelle Video-Platzierungen und Anzeigen?

Universelle Videoplatzierungen können nur universelle Videoanzeigen enthalten, und universelle Videoanzeigen können nur an universelle Videoplatzierungen angehängt werden.

Erstellen Sie universelle Video-Platzierungen und -Anzeigen ähnlich wie Sie andere Arten von Platzierungen und Videos erstellen:

1. Erstellen Sie innerhalb der gewünschten Kampagne [eine universelle Videoplatzierung](/help/dsp/campaign-management/placements/placement-create.md) und wählen Sie die [!UICONTROL Placement Type] **[!UICONTROL Universal Video]** aus.

   Es muss mindestens eine Zielumgebung (Desktop, Mobile, Connected TV) angegeben werden.

1. Erstellen Sie in derselben Kampagne wie bei der Platzierung des universellen Videos [eine einzelne universelle Videoanzeige](/help/dsp/campaign-management/ads/ad-create.md) oder [mehrere universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Wenn Sie mehrere Anzeigen erstellen, stellen Sie sicher, dass Sie &quot;[!UICONTROL Universal Video]&quot; als [!UICONTROL Ad Type] angeben:

   * Für [!DNL Google] oder [!DNL Flashtalking] Anzeigen: Klicken Sie im Schritt &quot;[!UICONTROL Review ad types]&quot; nach dem Hochladen der Datei auf das **[!UICONTROL Ad Type]** Feld und wählen Sie **[!UICONTROL Universal Video]** aus.

   * Für andere Arten von Anzeigen-Tags: Geben Sie in der Tabellendatei, die Sie hochladen, das Feld Anzeigentyp für jede Anzeige wie **[!UICONTROL Universal Video]** an.

1. [Öffnen Sie die Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-edit.md) für jede neue Anzeige und wählen Sie das entsprechende Videoformat aus:

   * **[!UICONTROL VPAID]:** Sichtbarkeit wird immer gemessen.
   * **[!UICONTROL VPAID & VAST (Default)]:** Enthält ein Inventar, das keine Sichtbarkeitsmessung zulässt.
   * **[!UICONTROL VAST]** - Geeignet für vernetzten TV-Bestand.

   Weitere Informationen finden Sie [ „Einstellungen für universelle ](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot;.

1. [Fügen Sie die neuen universellen Videoanzeigen ](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) der Platzierung „Universelles Video“ hinzu.

## Warum sind einige Optimierungsziele und -pakete nicht verfügbar, wenn die Connected TV-Umgebung für eine universelle Videoplatzierung ausgewählt wird?

Ziele, die mit standardmäßigen Platzierungen für angeschlossene Fernsehgeräte inkompatibel sind, wie z. B. niedrigste Kosten pro Klick, werden für die angeschlossene TV-Umgebung in universellen Videoplatzierungen nicht unterstützt. Ebenso sind Pakete mit inkompatiblen Optimierungszielen ebenfalls nicht zur Auswahl verfügbar.

## Wann sollte das **[!UICONTROL VAST]** Videoformat für universelle Videoanzeigen verwendet werden?

Verwenden Sie **[!UICONTROL VAST]** in einem der folgenden Szenarien:

* Die Platzierung zielt auf das verbundene TV-Inventar ab.
* Die Platzierung zielt auf das Videoinventar aus Google Ad Manager, Appnexus, SpotX oder Freewheel ab. Diese SSPs unterstützen nicht das Videoformat VPAID &amp; VAST.

## Ist es möglich, mehrere universelle Videoanzeigen an dieselbe universelle Videoplatzierung anzuhängen?

Ja.
