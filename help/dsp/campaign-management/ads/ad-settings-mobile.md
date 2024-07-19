---
title: Einstellungen für mobile Anzeigen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für mobile Anzeigen.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# Einstellungen für mobile Anzeigen

## [!UICONTROL Insert Ad Tag]

*Nur neue mobile Videoanzeigenformate*

**[!UICONTROL URL]** oder **[!UICONTROL Ad Tag]**: Ein VAST-Anzeigen-Tag oder Anzeigen-Tag eines Drittanbieters, das kreative Assets und Tracking-Pixel enthält

**[!UICONTROL Ad Title]** oder **[!UICONTROL Title]**: Ein Name für die Anzeige, der in der [!UICONTROL Ads]-Ansicht und den Berichten verwendet wird.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]** -Taste. Wenn das Tag gültig ist, wird oben eine XML-Datei mit dem Wert `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Display-Anzeigen für Mobilgeräte

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der von Ihnen erstellte Anzeigentyp, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der Anzeigen-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (wie z. B. Holiday Product Preview: 300x250 Gamer&quot;).

**\[Ad Source\]**: (schreibgeschützt) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** Die URL des kreativen Drittanbieter-Assets. Alle Parameter [timestamp] und [[timestamp]] werden durch tatsächliche Werte ersetzt.

**[!UICONTROL Final Display Code]:** Die URL für das kreative Asset eines Drittanbieters mit den erforderlichen [Advertising DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md), sofern zutreffend.

### [!UICONTROL Basic]: Videoanzeigen

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der von Ihnen erstellte Anzeigentyp, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der Anzeigen-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Gerätetyp und einige wichtige Attribute (z. B. Holiday Product Preview: 30 Sek. Phone Preroll).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Die Breite der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Player X]:** Die X-Koordinate für die Anzeigeneinheit. Behalten Sie die Standardeinstellung bei.

**[!UICONTROL Player Y]:** Die Y-Koordinate für die Anzeigeneinheit. Behalten Sie die Standardeinstellung bei.

**[!UICONTROL Player Width]:** Die Breite der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

Dies entspricht dem Feld **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

Dies entspricht dem Feld **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** Wo Sie Videosteuerelemente für die Anzeige einbeziehen sollen: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oder *[!UICONTROL None]* (der Standard).

**[!UICONTROL Preserve Aspect Ratio]:** Gibt an, ob die Breite und Höhe des Videos (*[!UICONTROL Yes]*) beibehalten oder das Video gestreckt werden soll, um den verfügbaren Platz zu füllen (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Einige Anzeigentypen) Die Anzahl der Sekunden, um die Anzeige der Schließen-Schaltfläche zu verzögern.

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als kreatives Asset eingegeben haben.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als kreatives Asset eingegeben haben, wobei gegebenenfalls die erforderlichen [Advertising DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md) eingefügt wurden.

**[!UICONTROL Wmode]:** (Einige Anzeigentypen) Der Fenstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]* oder *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen für die einzelne Anzeige neue Pixel erstellen. **Tipp:** Informationen zum Bearbeiten der Tracking-Pixel von Drittanbietern für mehrere Anzeigen in einer Platzierung auf einmal mithilfe der [!UICONTROL Ad Tools]-Ansicht finden Sie unter &quot;[Verfolgungspixel von Drittanbietern an Anzeigen an eine Platzierung anhängen](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, durch das das Pixel ausgelöst wird. Verwenden Sie für diesen Anzeigentyp Pixel, die auf *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]* ausgelöst werden.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel eine *[!UICONTROL IMG URL]* (1x1-Pixelbilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

### [!UICONTROL Sharing]

Veraltet

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Auflisten der mit einer Anzeige verknüpften Platzierungen](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP Makros](/help/dsp/campaign-management/macros.md)
