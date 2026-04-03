---
title: Audio-Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Audioanzeigen.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
TQID: https://experienceleague.adobe.com/rP0SJspXvqzivctnNqe7b35mbL-ARZlGzC3cLAS-uwA
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
source-wordcount: 277
ht-degree: 0%

---

# Audio-Anzeigeneinstellungen

## [!UICONTROL Insert Ad Tag]

*Nur neue Anzeigen*

**[!UICONTROL URL]**: Die VAST-Tag-URL.

**[!UICONTROL Title]**: Ein Name für die Datei, der in der [!UICONTROL Ads] und in Berichten verwendet wird.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]**. Wenn das Tag gültig ist, wird oben eine XML-Datei mit `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, dem die Anzeige angehängt werden kann. Standardwert ist *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Der Anzeigename. Der Asset-Titel wird standardmäßig verwendet, Sie können den Namen jedoch ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads] und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. „Holiday Product Preview: 30sec Audio„).

**[!UICONTROL Ad Duration]:** Die Länge der Audiodatei. Er wird je nach ausgewählter Werbeeinheit automatisch als [!UICONTROL 15] oder [!UICONTROL 30] festgelegt.

Dieses Feld kann je nach den Kontoberechtigungen angezeigt werden oder nicht.

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden) Eine URL für eine Werbequelle eines Drittanbieters. Stellen Sie sicher, dass das VAST-Tag nur Audio-Mediendateien enthält.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden) Die URL für die Werbequelle eines Drittanbieters mit den erforderlichen [Advertising DSP-Tracking-](/help/dsp/campaign-management/macros.md), falls zutreffend.

**[!UICONTROL Select Rate]:** (Nur Benutzer mit Genehmigung) Ein vorab ausgehandelter Tarif, der über Adobe in Rechnung gestellt wird, oder einer der Tarife, die Sie ausgehandelt haben und die vom Anbieter in Rechnung gestellt werden. Um einen Tarif hinzuzufügen, wenden Sie sich an Ihr Adobe Account Team.

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
