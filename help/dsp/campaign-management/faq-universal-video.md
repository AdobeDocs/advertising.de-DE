---
title: Häufig gestellte Fragen zum universellen Video
description: Erfahren Sie mehr über universelle Videoanzeigen.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
TQID: https://experienceleague.adobe.com/LAzSivup-EVuDgtWN1T58lfRjzgrchIiFF9-lMJAVlw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 348
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

## Warum sind einige Optimierungsziele und -pakete nicht verfügbar, wenn die verbundene TV-Umgebung für eine universelle Videoplatzierung ausgewählt wird?

Ziele, die mit standardmäßigen Platzierungen für angeschlossene Fernsehgeräte inkompatibel sind, wie z. B. niedrigste Kosten pro Klick, werden für die angeschlossene TV-Umgebung in universellen Videoplatzierungen nicht unterstützt. Ebenso sind Pakete mit inkompatiblen Optimierungszielen ebenfalls nicht zur Auswahl verfügbar.

## Wann sollte das **[!UICONTROL VAST]** Videoformat für universelle Videoanzeigen verwendet werden?

Verwenden Sie **[!UICONTROL VAST]** in einem der folgenden Szenarien:

* Die Platzierung zielt auf das verbundene TV-Inventar ab.
* Die Platzierung zielt auf das Videoinventar aus Google Ad Manager, Appnexus, SpotX oder FreeWheel ab. Diese SSPs unterstützen nicht das Videoformat VPAID &amp; VAST.

## Ist es möglich, mehrere universelle Videoanzeigen an dieselbe universelle Videoplatzierung anzuhängen?

Ja.
