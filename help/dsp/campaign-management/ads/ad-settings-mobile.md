---
title: Mobile-Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Mobile-Anzeigen.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Mobile-Anzeigeneinstellungen

## [!UICONTROL Insert Ad Tag]

*Nur neue Mobile-Video-Werbeformate*

**[!UICONTROL URL]** oder **[!UICONTROL Ad Tag]**: Ein VAST-Anzeigen-Tag oder Anzeigen-Tag eines Drittanbieters, das Kreativ-Assets und Tracking-Pixel enthält

**[!UICONTROL Ad Title]** oder **[!UICONTROL Title]**: Ein Name für die Anzeige, die in der [!UICONTROL Ads] und in Berichten verwendet wird.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]**. Wenn das Tag gültig ist, wird oben eine XML-Datei mit `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Anzeigen für Mobilgeräte

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, dem die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigename. Der Asset-Titel wird standardmäßig verwendet, Sie können den Namen jedoch ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der Anzeigen-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. „Holiday Product Preview: 300x250 Gamer„).

**\[Ad Source\]**: (Schreibgeschützt) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** Die URL des Kreativ-Assets eines Drittanbieters. Alle [Zeitstempel] und [[Zeitstempel]]-Parameter werden durch die tatsächlichen Werte ersetzt.

**[!UICONTROL Final Display Code]:** Die URL für das Kreativ-Asset eines Drittanbieters, mit den erforderlichen [Advertising DSP-](/help/dsp/campaign-management/macros.md), falls zutreffend.

### [!UICONTROL Basic]: Videoanzeigen

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, dem die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigename. Der Asset-Titel wird standardmäßig verwendet, Sie können den Namen jedoch ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der Anzeigen-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. „Holiday Product Preview: 30sec Phone Preroll„).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Die Breite der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigenkomponententyp gesperrt werden.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Die Höhe der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigenkomponententyp gesperrt werden.

**[!UICONTROL Player X]:** Die X-Koordinate für die Werbeeinheit. Standardeinstellung beibehalten.

**[!UICONTROL Player Y]:** Die Y-Koordinate für die Werbeeinheit. Standardeinstellung beibehalten.

**[!UICONTROL Player Width]:** Die Breite der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigenkomponententyp gesperrt werden.

Dies ist dasselbe wie das Feld **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** Die Höhe der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigenkomponententyp gesperrt werden.

Dies ist dasselbe wie das Feld **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** Wohin sollen Videosteuerelemente für die Anzeige eingefügt werden: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oder *[!UICONTROL None]* (Standard).

**[!UICONTROL Preserve Aspect Ratio]:** Soll das Breiten- und Höhenverhältnis des Videos beibehalten (*[!UICONTROL Yes]*) oder das Video so gedehnt werden, dass es den verfügbaren Platz ausfüllt (*[!UICONTROL No]*)?

**[!UICONTROL Close Button Delay]:** (Einige Anzeigentypen) Die Anzahl der Sekunden, um die das Erscheinen der Schaltfläche Schließen verzögert wird.

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag eines Drittanbieters, das Sie als Kreativ-Asset eingegeben haben.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag eines Drittanbieters, das Sie als Kreativ-Asset eingegeben haben, mit den erforderlichen [Advertising DSP-Tracking-](/help/dsp/campaign-management/macros.md).

**[!UICONTROL Wmode]:** (Einige Anzeigentypen) Der Fenstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]* oder *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

### [!UICONTROL Sharing]

Veraltet

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Platzierungen auflisten, die mit einer Anzeige verbunden sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP-Makros](/help/dsp/campaign-management/macros.md)
