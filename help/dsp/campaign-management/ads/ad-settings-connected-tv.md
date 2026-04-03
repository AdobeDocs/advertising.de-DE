---
title: Einstellungen für verbundene TV-Werbeanzeigen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für verbundene TV-Anzeigen.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
TQID: https://experienceleague.adobe.com/EY3BI7GFcDtR9SmA-N9VY3pwEMPTA99GApcuReaLBeQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 393
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

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung in Advertising DSP](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Platzierungen auflisten, die mit einer Anzeige verbunden sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP-Makros](/help/dsp/campaign-management/macros.md)
