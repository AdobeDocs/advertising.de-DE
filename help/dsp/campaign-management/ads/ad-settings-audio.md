---
title: Audio-Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Audioanzeigen.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Audio-Anzeigeneinstellungen

## [!UICONTROL Insert Ad Tag]

*Nur neue Anzeigen*

**[!UICONTROL URL]**: Die VAST-Tag-URL.

**[!UICONTROL Title]**: Ein Name für die Datei, der im [!UICONTROL Ads] anzeigen und Berichte anzeigen.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]** Schlüssel. Wenn das Tag gültig ist, wird eine XML-Datei angezeigt, die Folgendes enthält: `<VAST>` oben.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen. Er entspricht dem Platzierungstyp, an den die Anzeige angehängt werden kann. Die Standardeinstellung ist *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung anhängen, in der [!UICONTROL Ads] und in Berichten anzeigen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (wie z. B. Holiday Product Preview: 30sec Audio&quot;).

**[!UICONTROL Ad Duration]:** Die Länge der Audiodatei. Sie wird automatisch als [!UICONTROL 15] oder [!UICONTROL 30], abhängig von der ausgewählten Anzeigeneinheit.

Je nach den Kontoberechtigungen kann dieses Feld angezeigt werden.

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden) Eine URL für eine Anzeigenquelle eines Drittanbieters. Stellen Sie sicher, dass das VAST-Tag nur Audiomediendateien enthält.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden) Die URL für die Anzeigenquelle eines Drittanbieters mit den erforderlichen [Anzeigen DSP Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

**[!UICONTROL Select Rate]:** (Nur Benutzer mit Berechtigung) Ein vorab ausgehandelter Preis, der über Adobe in Rechnung gestellt wird, oder einer der Tarife, die Sie ausgehandelt haben und für die Sie vom Anbieter in Rechnung gestellt werden. Wenden Sie sich zum Hinzufügen einer Gebühr an Ihr Adobe-Account-Team.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen für die einzelne Anzeige neue Pixel erstellen. **Tipp:** So bearbeiten Sie die Verfolgungspixel von Drittanbietern für mehrere Anzeigen in einer Platzierung gleichzeitig mit der [!UICONTROL Ad Tools] Ansicht, siehe[Anhängen von Tracking-Pixeln von Drittanbietern an Anzeigen an einer Platzierung](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel zum Auslösen Trigger wird. Verwenden Sie für diesen Anzeigentyp Pixel, die auf dem *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (1x1-Pixel-Bilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen Pixeltyp.

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter:*[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Einzelne Anzeige erstellen](ad-create.md)
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP Makros](/help/dsp/campaign-management/macros.md)
