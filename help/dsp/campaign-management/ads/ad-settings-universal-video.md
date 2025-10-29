---
title: Einstellungen für universelle Videoanzeigen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für universelle Videoanzeigen.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Einstellungen für universelle Videoanzeigen

>[!NOTE]
>
>Universelle Videoanzeigen können nur an Platzierungen für universelle Videos angehängt werden.

## [!UICONTROL Insert Ad Tag]

*Nur neue Anzeigen*

**[!UICONTROL URL]:** Die VAST-Tag-URL.

**[!UICONTROL Title]:** Ein Titel für die Datei, der sich in der [!UICONTROL Ads] und in Berichten befindet.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]**. Wenn das Tag gültig ist, wird oben eine XML-Datei mit `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, dem die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigename. Der Asset-Titel wird standardmäßig verwendet, Sie können den Namen jedoch ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads] und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. „Holiday Product Preview: 30sec Universal Video„).

**[!UICONTROL Show Controls]:** Wohin sollen Videosteuerelemente für die Anzeige eingefügt werden: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oder *[!UICONTROL None]* (Standard).

**[!UICONTROL Preserve Aspect Ratio]:**, ob die Breiten- und Höhenverhältnisse des Videos beibehalten (*[!UICONTROL Yes]*) oder das Video gedehnt werden soll, um verfügbaren Platz auszufüllen (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag eines Drittanbieters, das Sie als Anzeigenquelle eingegeben haben.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag eines Drittanbieters, das Sie als Anzeigenquelle mit den erforderlichen [Advertising DSP-Tracking-Makros eingegeben haben](/help/dsp/campaign-management/macros.md) falls zutreffend.

**[!UICONTROL Wmode]:** Der Fenstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]* oder *[!UICONTROL opaque]*. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

**[!UICONTROL Video Format]:** Das Format des Anzeigen-Players für den potenziellen Bestand: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* oder *[!UICONTROL VAST]*. Die Sichtbarkeit wird immer für [!UICONTROL VPAID] gemessen, [!UICONTROL VPAID & VAST] umfasst jedoch ein Inventar, das keine Sichtbarkeitsmessung zulässt. Beachten Sie diese Unterscheidung, wenn Sichtbarkeitsmetriken für Ihre Kampagne wichtig sind.

Verwenden Sie [!UICONTROL VAST], was keine Sichtbarkeitsmessung zulässt, wenn Sie auf angeschlossene Fernsehgeräte oder Inventare abzielen, die ausschließlich das VAST-Format erfordern (in der Regel aus Bezugsquellen wie Google Ad Manager, Appnexus, SpotX und Freewheel). Verwenden Sie diese Option auch für Inventare, die zuvor mit VAST (Standard Pre-roll)- oder VAST (Phone + Tablet Standard Pre-roll)-Platzierungen/-Anzeigen kompatibel waren.

**[!UICONTROL Clock Number]**: (Wird nur im Vereinigten Königreich verwendet; steht nur Benutzenden mit Genehmigung zur Verfügung) Eine eindeutige Kennung, die verwendet wird, um sicherzustellen, dass die richtige Anzeige gesendet wird. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [FAQs zu Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Platzierungen auflisten, die mit einer Anzeige verbunden sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP-Makros](/help/dsp/campaign-management/macros.md)
