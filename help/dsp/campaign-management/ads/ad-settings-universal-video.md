---
title: Einstellungen für universelle Videoanzeigen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für universelle Videoanzeigen.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '511'
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

Alle vorhandenen Pixel der Ereignisverfolgung für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und bei Bedarf neue Pixel erstellen, basierend auf Ihren Tracking-Anforderungen für die einzelne Anzeige. **Tipp** Informationen zum gleichzeitigen Bearbeiten der Tracking-Pixel von Drittanbietern für mehrere Anzeigen in einer Platzierung mithilfe der [!UICONTROL Ad Tools] finden Sie unter &quot;[Anhängen von Tracking-Pixeln von Drittanbietern an Anzeigen in einer Platzierung](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, durch das das Pixel zum Auslösen Trigger wird. Verwenden Sie für diesen Anzeigentyp Pixel, die auf dem *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]* ausgelöst werden.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (Bilddatei mit 1 x 1 Pixel), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für die angegebene [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, der Ihnen die Identifizierung des Pixels erleichtert.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [FAQs zu Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Platzierungen auflisten, die mit einer Anzeige verbunden sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP-Makros](/help/dsp/campaign-management/macros.md)
