---
title: Universelle Videoanzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für universelle Videoanzeigen.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Universelle Videoanzeigeneinstellungen

>[!NOTE]
>
>Universelle Videoanzeigen können nur an universelle Videoplatzierungen angehängt werden.

## [!UICONTROL Insert Ad Tag]

*Nur neue Anzeigen*

**[!UICONTROL URL]:** Die VAST-Tag-URL.

**[!UICONTROL Title]:** Ein Titel für die Datei, der sich in der Ansicht und den Berichten [!UICONTROL Ads] befindet.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]** -Taste. Wenn das Tag gültig ist, wird oben eine XML-Datei mit dem Wert `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der von Ihnen erstellte Anzeigentyp, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads]-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (wie z. B. Holiday Product Preview: 30 Sek. Universal Video&quot;).

**[!UICONTROL Show Controls]:** Wo Sie Videosteuerelemente für die Anzeige einbeziehen sollen: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oder *[!UICONTROL None]* (der Standard).

**[!UICONTROL Preserve Aspect Ratio]:** Gibt an, ob die Breite und Höhe des Videos (*[!UICONTROL Yes]*) beibehalten oder das Video gestreckt werden soll, um den verfügbaren Platz zu füllen (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als Anzeigenquelle eingegeben haben.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als Anzeigenquelle eingegeben haben, wobei gegebenenfalls die erforderlichen [Advertising DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md) eingefügt wurden.

**[!UICONTROL Wmode]:** Der Fenstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]* oder *[!UICONTROL opaque]*. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

**[!UICONTROL Video Format]:** Das Format des Anzeigenplayers für potenziellen Bestand: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* oder *[!UICONTROL VAST]*. Die Sichtbarkeit wird immer für [!UICONTROL VPAID] gemessen, aber [!UICONTROL VPAID & VAST] enthält Bestand, der keine Sichtbarkeitsmessung zulässt. Beachten Sie diese Unterscheidung, wenn Sichtbarkeitsmetriken für Ihre Kampagne wichtig sind.

Verwenden Sie &quot;[!UICONTROL VAST]&quot;, was keine Sichtbarkeitsmessung zulässt, wenn Sie angeschlossene Fernsehgeräte oder Inventare auswählen, für die ausschließlich das VAST-Format erforderlich ist (normalerweise aus Versorgungsquellen wie Google Ad Manager, Appnexus, SpotX und Freewheel). Verwenden Sie diese Option auch für das Inventar, das zuvor mit VAST-Platzierungen (Standard Pre-roll) oder Phone + Tablet Standard Pre-Roll (VAST)-Platzierungen/-Anzeigen kompatibel war.

**[!UICONTROL Clock Number]**: (Wird nur im Vereinigten Königreich verwendet; nur für Benutzer mit Berechtigung verfügbar) Eine eindeutige Kennung, mit der sichergestellt wird, dass die richtige Anzeige gesendet wird. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen für die einzelne Anzeige neue Pixel erstellen. **Tipp:** Informationen zum Bearbeiten der Tracking-Pixel von Drittanbietern für mehrere Anzeigen in einer Platzierung auf einmal mithilfe der [!UICONTROL Ad Tools]-Ansicht finden Sie unter &quot;[Verfolgungspixel von Drittanbietern an Anzeigen an eine Platzierung anhängen](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, durch das das Pixel ausgelöst wird. Verwenden Sie für diesen Anzeigentyp Pixel, die auf *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]* ausgelöst werden.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel eine *[!UICONTROL IMG URL]* (1x1-Pixelbilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [FAQs über universelle Videos](/help/dsp/campaign-management/faq-universal-video.md)
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Auflisten der mit einer Anzeige verknüpften Platzierungen](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP Makros](/help/dsp/campaign-management/macros.md)
