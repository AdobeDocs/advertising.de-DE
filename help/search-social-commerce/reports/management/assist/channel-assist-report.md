---
title: '[!UICONTROL Channel Assist Report]'
description: Erfahren Sie mehr über die [!UICONTROL Channel Assist Report].
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# Der [!UICONTROL Channel Assist Report]

*Werbetreibende mit Such-, Social- und Commerce-Klick-Tracking und Konversions-Tracking von Adobe Advertising, Adobe Analytics (mit einer [!DNL Analytics] -Integration) oder , die in Feeds mit einem Token (`ef_id`) bereitgestellt werden,*

Die [!UICONTROL Channel Assist Report] geben an, wie verschiedene Marketing-Kanäle (Suche oder Social aus Search, Social &amp; Commerce oder Anzeige oder Video aus Advertising DSP) den Konvertierungsprozess unterstützt haben. Der Bericht zeigt an, wie jedes Muster von Ereignistypen, das zu einer oder mehreren Konversionen führte, zu Ihren Gesamtkonversionen beigetragen hat. Sie würden beispielsweise sehen, wie viele Konversionen auftraten, wenn Benutzer zum ersten Mal eine Anzeige-Impression sahen, dann auf eine Suchanzeige klickten und dann
eine Bestellung aufgegeben hat oder Sie sehen, wie viele Konversionen auftraten, nachdem Benutzer mit mehr als 10 Anzeigen interagiert hatten. Zu Ereignistypen gehören Suchklicks, Impressionen und Klicks auf die Anzeige, Videoimpressionen und -klicks sowie andere Impressionen und andere Klicks. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

Die Berichtsergebnisse enthalten aggregierte Daten für jedes Muster von Ereignistypen im Konversionspfad - bis zu den N frühesten Ereignistypen -, die im [Klick-Lookback-Fenster des Advertisers](/help/search-social-commerce/glossary.md#c-d) und im [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) aufgetreten sind. Wenn Sie beispielsweise eine Pfadgröße von 5 (5) auswählen, enthält der Bericht Konversionspfade, die bis zu den fünf frühesten Ereignissen enthielten, wobei für jedes getrackte Muster von Ereignistypen eine Zeile vorhanden ist (z. B. &quot;Suchklick&quot;und dann &quot;Impression anzeigen&quot;). Jede Zeile zeigt ein Ereignismuster, einschließlich des ersten Ereignisses im Pfad und des letzten Ereignisses, das zu Konversionen führte (auch wenn das letzte Ereignis außerhalb der angegebenen Pfadgröße liegt). Standardmäßig werden die Zeilen nach der Anzahl der Ereignisse im Pfad in aufsteigender Reihenfolge angezeigt.

Sie können optional aggregierte Konversionsdaten für jede Zeile hinzufügen. Wenn Sie Konversions-/Umsatzspalten in den Bericht einbeziehen, wird jeder Konversionstyp in vier Spalten dargestellt: a) die Gesamtanzahl der Konversionen, b) der Prozentsatz Ihrer Konversionen insgesamt, die diesem Ereignismuster zugeordnet wurden, c) die durchschnittliche Latenz am Tag vom ersten Ereignis zu einer Konversion und d) die durchschnittliche Latenz in Tagen vom letzten Ereignis zu einer Konversion. Wenn der Konversionspfad mehr Ereignisse als die angegebene Pfadgröße enthält, enthält der Bericht zusätzliche Zeilen, die Daten für Konversionen aggregieren, die aus der höheren Anzahl von Ereignissen resultieren (z. B. alle Muster, die sechs Ereignistypen enthielten).

Sie können Daten der letzten 18 Monate anzeigen.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus dem Bereich Spalten der Berichtseinstellungen hinzufügen.

| Spalte | Standard? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] bis [!UICONTROL 5th Event] | Standard | Die fünf frühesten Ereignistypen im Konversionspfad, die im [Klick-Lookback-Fenster des Werbetreibenden](/help/search-social-commerce/glossary.md#c-d) und im [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) aufgetreten sind. |
| [!UICONTROL Path Size] | Standard | Die Anzahl der Ereignistypen im Konversionspfad, die im [Klick-Lookback-Fenster des Werbetreibenden](/help/search-social-commerce/glossary.md#c-d) und im [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) aufgetreten sind. |
| [!UICONTROL First Event Type] | Standard | Der Ereignistyp des ersten (frühesten) Ereignisses im Konversionspfad. |
| [!UICONTROL Last Event Type] | Standard | Der Ereignistyp des letzten Ereignisses, das zu Konversionen führte (auch wenn das letzte Ereignis außerhalb der angegebenen Pfadgröße liegt). |
| \[Advertiser-spezifische benutzerdefinierte (abgeleitete) Metriken\] | Benutzerdefiniert | Der Wert für eine von Ihnen erstellte benutzerspezifische Metrik, der aus vorhandenen Metriken berechnet wird. |
| \[Advertiser-spezifische Konversionsmetriken\] | Benutzerdefiniert | Die Anzahl der Konversionen für eine bestimmte Konversionsmetrik oder Site-Interaktionsmetrik. |
| [!UICONTROL % of Total] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in die Berichtsausgabe für jede Konversionsmetrik eingeschlossen) Der Prozentsatz Ihrer Gesamtkonversionen über Portfolios hinweg, der dem Ereignismuster zugeordnet wurde. |
| [!UICONTROL 6th Event] bis [!UICONTROL 30th Event] | Benutzerdefiniert | Die sechsten bis 30. Ereignistypen im Konversionspfad, die im [Klick-Lookback-Fenster des Werbetreibenden](/help/search-social-commerce/glossary.md#c-d) und im [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) aufgetreten sind. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in die Berichtsausgabe für jede Konversionsmetrik eingeschlossen) Die durchschnittliche Latenz in Tagen vom ersten Ereignis zu einer Konversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe eingeschlossen) Die durchschnittliche Latenz in Tagen vom letzten Ereignis zu einer Konversion. |
| [!UICONTROL Path Frequency] | Benutzerdefiniert | Die Häufigkeit, mit der der Pfad für diese Zeile vor der Konvertierung aufgetreten ist. |

>[!MORELIKETHIS]
>
>* [Über Hilfsberichte](assist-report-about.md)
>* [Der [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Der [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Bereiten Sie die Berichtseinstellungen vor](assist-report-settings.md)
>* [ Hilfsbericht erzeugen](assist-report-generate.md)
