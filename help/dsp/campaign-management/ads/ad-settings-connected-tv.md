---
title: Einstellungen für verbundene TV-Werbeanzeigen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für verbundene TV-Anzeigen.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Einstellungen für verbundene TV-Werbeanzeigen

## [!UICONTROL Insert Ad Tag]

*Nur neue Anzeigen*

**[!UICONTROL URL]**: Die VAST-Tag-URL.

**[!UICONTROL Title]**: Ein Name für die Datei, der in der Ansicht Anzeigen und in Berichten verwendet wird.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]**. Wenn das Tag gültig ist, wird oben eine XML-Datei mit `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, dem die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigename. Der Asset-Titel wird standardmäßig verwendet, Sie können den Namen jedoch ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads] und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. „Holiday Product Preview: 30sec CTV„).

**[!UICONTROL Width | Ad Unit Width]:** Die Breite der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigenkomponententyp gesperrt werden.

**[!UICONTROL Height | Ad Unit Height]:** Die Höhe der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigenkomponententyp gesperrt werden.

**[!UICONTROL Player X]:** Die X-Koordinate für die Werbeeinheit. Standardeinstellung beibehalten.

**[!UICONTROL Player Y]:** Die Y-Koordinate für die Werbeeinheit. Standardeinstellung beibehalten.

**[!UICONTROL Player Width]:** Die Breite der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigenkomponententyp gesperrt werden.

Dies ist dasselbe wie das Feld **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** Die Höhe der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigenkomponententyp gesperrt werden.

Dies ist dasselbe wie das Feld **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** Wohin sollen Videosteuerelemente für die Anzeige eingefügt werden: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oder *[!UICONTROL None]* (Standard).

**[!UICONTROL Preserve Aspect Ratio]:** Soll das Breiten- und Höhenverhältnis des Videos beibehalten (*[!UICONTROL Yes]*) oder das Video so gedehnt werden, dass es den verfügbaren Platz ausfüllt (*[!UICONTROL No]*)?

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag eines Drittanbieters, das Sie als Anzeigenquelle eingegeben haben.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag eines Drittanbieters, das Sie als Anzeigenquelle mit den erforderlichen [Advertising DSP-Tracking-Makros eingegeben haben](/help/dsp/campaign-management/macros.md) falls zutreffend.

**[!UICONTROL Clock Number]**: (Wird nur im Vereinigten Königreich verwendet; steht nur Benutzenden mit Genehmigung zur Verfügung) Eine eindeutige Kennung, die verwendet wird, um sicherzustellen, dass die richtige Anzeige gesendet wird. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

### [!UICONTROL Pixel]

Alle vorhandenen Pixel der Ereignisverfolgung für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und bei Bedarf neue Pixel erstellen, basierend auf Ihren Tracking-Anforderungen für die einzelne Anzeige. **Tipp** Informationen zum gleichzeitigen Bearbeiten der Tracking-Pixel von Drittanbietern für mehrere Anzeigen in einer Platzierung mithilfe der [!UICONTROL Ad Tools] finden Sie unter &quot;[Anhängen von Tracking-Pixeln von Drittanbietern an Anzeigen in einer Platzierung](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)&quot;.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, durch das das Pixel zum Auslösen Trigger wird. Verwenden Sie für diesen Anzeigentyp Pixel, die auf dem *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]* ausgelöst werden.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (Bilddatei mit 1 x 1 Pixel), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen Pixeltyp.

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, der Ihnen die Identifizierung des Pixels erleichtert.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Platzierungen auflisten, die mit einer Anzeige verbunden sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP-Makros](/help/dsp/campaign-management/macros.md)
