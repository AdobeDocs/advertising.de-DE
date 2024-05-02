---
title: Pre-Roll-Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Pre-Roll-Anzeigen.
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Pre-Roll-Anzeigeneinstellungen

## [!UICONTROL Insert Ad Tag]

*Nur neue Anzeigen*

**[!UICONTROL URL]:** Die VAST-Tag-URL.

**[!UICONTROL Title]:** Ein Titel für die Datei, der sich im [!UICONTROL Ads] anzeigen und Berichte anzeigen.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]** Schlüssel. Wenn das Tag gültig ist, wird eine XML-Datei angezeigt, die Folgendes enthält: `<VAST>` oben.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen. Er entspricht dem Platzierungstyp, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung anhängen, in der [!UICONTROL Ads] und in Berichten anzeigen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. Holiday Product Preview: 30 Sek. Preroll&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Nur standardmäßige und übersprungene Pre-Roll-Anzeigen) Die Breite der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Nur standardmäßige und übersprungene Pre-Roll-Anzeigen) Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Player X]:** Die X-Koordinate für die Anzeigeneinheit. Behalten Sie die Standardeinstellung bei.

**[!UICONTROL Player Y]:** Die Y-Koordinate für die Anzeigeneinheit. Behalten Sie die Standardeinstellung bei.

**[!UICONTROL Player Width]:** Die Breite der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

Dieses Feld entspricht dem **[!UICONTROL Width]** -Feld.

**[!UICONTROL Player Height]:** Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

Dies entspricht dem **[!UICONTROL Height]** -Feld.

**[!UICONTROL Show Controls]:** Wo Sie Videosteuerelemente für die Anzeige einbeziehen: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oder *[!UICONTROL None]* (Standardeinstellung).

**[!UICONTROL Preserve Aspect Ratio]:** Gibt an, ob die Breite und Höhe des Videos (*[!UICONTROL Yes]*) oder das Video zu dehnen, um den verfügbaren Platz (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag eines Drittanbieters, das Sie als Anzeigenquelle eingegeben haben.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag eines Drittanbieters, das Sie als Anzeigenquelle mit dem erforderlichen [Anzeigen DSP Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

**[!UICONTROL Wmode]:** (Nur interaktive Pre-Roll) Der Fenstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]* oder *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Nur interaktive Pre-Roll) Das Format des Anzeigen-Players für potenzielle Bestände: *[!UICONTROL VPAID]* oder *[!UICONTROL VPAID & VAST]*. Die Sichtbarkeit wird immer für VPAID gemessen, VPAID und VAST enthalten jedoch Bestände, die keine Sichtbarkeitsmessung zulassen. Beachten Sie diese Unterscheidung, wenn Sichtbarkeitsmetriken für Ihre Kampagne wichtig sind.

**[!UICONTROL Clock Number]**: (Nur interaktive Pre-Roll-Daten; nur im Vereinigten Königreich verwendet; nur für Benutzer mit Berechtigung verfügbar) Eine eindeutige Kennung, mit der sichergestellt wird, dass die richtige Anzeige gesendet wird. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen für die einzelne Anzeige neue Pixel erstellen.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel zum Auslösen Trigger wird. Verwenden Sie für diesen Anzeigentyp Pixel, die auf dem *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (1x1-Pixel-Bilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds in dem für die [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Einzelne Anzeige erstellen](ad-create.md)
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP Makros](/help/dsp/campaign-management/macros.md)
