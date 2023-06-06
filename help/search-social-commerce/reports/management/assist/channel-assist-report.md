---
title: "[!UICONTROL Channel Assist Report]"
description: Erfahren Sie mehr über die [!UICONTROL Channel Assist Report].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Die [!UICONTROL Channel Assist Report]

*Werbetreibende mit Klick-Tracking in Search, Social und Commerce und Konversions-Tracking aus Adobe Advertising, Adobe Analytics (mit einer [!DNL Analytics] -Integration) oder in Feeds mit einem Token (`ef_id`) nur*

Die [!UICONTROL Channel Assist Report] Geben Sie an, wie viele Marketing-Kanäle (Suche oder Social Media aus Search, Social und Commerce) verwendet werden; oder Anzeigen oder Videos aus Advertising DSP) den Konvertierungsprozess unterstützt haben. Der Bericht zeigt an, wie jedes Muster von Ereignistypen, das zu einer oder mehreren Konversionen führte, zu Ihren Gesamtkonversionen beigetragen hat. Sie würden beispielsweise sehen, wie viele Konversionen stattgefunden haben, wenn Benutzer zum ersten Mal eine Anzeige-Impression gesehen, dann auf eine Suchanzeige geklickt und dann eine Bestellung aufgegeben haben. oder Sie können sehen, wie viele Konversionen aufgetreten sind, nachdem Benutzer mit mehr als 10 Anzeigen interagiert haben. Zu Ereignistypen gehören Suchklicks, Impressionen und Klicks auf die Anzeige, Videoimpressionen und -klicks sowie andere Impressionen und andere Klicks. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

Die Berichtsergebnisse enthalten aggregierte Daten für jedes Muster von Ereignistypen im Konversionspfad - bis zu den N frühesten Ereignistypen -, die innerhalb der des Advertisers aufgetreten sind [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). Wenn Sie beispielsweise eine Pfadgröße von 5 (5) auswählen, enthält der Bericht Konversionspfade, die bis zu den fünf frühesten Ereignissen enthielten, wobei für jedes getrackte Muster von Ereignistypen eine Zeile vorhanden ist (z. B. &quot;Suchklick&quot;und dann &quot;Impression anzeigen&quot;). Jede Zeile zeigt ein Ereignismuster, einschließlich des ersten Ereignisses im Pfad und des letzten Ereignisses, das zu Konversionen führte (auch wenn das letzte Ereignis außerhalb der angegebenen Pfadgröße liegt). Standardmäßig werden die Zeilen nach der Anzahl der Ereignisse im Pfad in aufsteigender Reihenfolge angezeigt.

Sie können optional aggregierte Konversionsdaten für jede Zeile hinzufügen. Wenn Sie Konversions-/Umsatzspalten in den Bericht einbeziehen, wird jeder Konversionstyp in vier Spalten dargestellt: a) die Gesamtanzahl der Konversionen, b) der Prozentsatz Ihrer Konversionen insgesamt, die diesem Ereignismuster zugeordnet wurden, c) die durchschnittliche Latenz am Tag vom ersten Ereignis zu einer Konversion und d) die durchschnittliche Latenz in Tagen vom letzten Ereignis zu einer Konversion. Wenn der Konversionspfad mehr Ereignisse als die angegebene Pfadgröße enthält, enthält der Bericht zusätzliche Zeilen, die Daten für Konversionen aggregieren, die aus der höheren Anzahl von Ereignissen resultieren (z. B. alle Muster, die sechs Ereignistypen enthielten).

Sie können Daten der letzten 18 Monate anzeigen.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus dem Bereich Spalten der Berichtseinstellungen hinzufügen.

| Spalte | Standard? | Beschreibung |
|----|----|
| [!UICONTROL 1st Event] nach [!UICONTROL 5th Event] | Standard | Die fünf frühesten Ereignistypen im Konversionspfad, die innerhalb der des Advertisers aufgetreten sind [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Standard | Die Anzahl der Ereignistypen im Konversionspfad, die innerhalb der [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | Standard | Der Ereignistyp des ersten (frühesten) Ereignisses im Konversionspfad. |
| [!UICONTROL Last Event Type] | Standard | Der Ereignistyp des letzten Ereignisses, das zu Konversionen führte (auch wenn das letzte Ereignis außerhalb der angegebenen Pfadgröße liegt). |
| \[Advertiser-spezifische benutzerdefinierte (abgeleitete) Metriken\] | Benutzerdefiniert | Der Wert für eine von Ihnen erstellte benutzerdefinierte Metrik, der aus vorhandenen Metriken berechnet wird. |
| \[Advertiser-spezifische Transaktionseigenschaften\] | Benutzerdefiniert | Die Anzahl der Konversionen für eine angegebene Transaktionseigenschaft oder Site-Interaktionsmetrik. |
| [!UICONTROL % of Total] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in die Berichtsausgabe für jede Transaktionseigenschaft eingeschlossen) Der Prozentsatz Ihrer Gesamtkonversionen über Portfolios, die dem Ereignismuster zugeordnet wurden. |
| [!UICONTROL 6th Event] nach [!UICONTROL 30th Event] | Benutzerdefiniert | Die sechsten bis 30. Ereignistypen im Konversionspfad, die innerhalb des vom Advertiser verwendeten [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in die Berichtsausgabe für jede Transaktionseigenschaft eingeschlossen) Die durchschnittliche Latenz in Tagen vom ersten Ereignis zu einer Konversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe eingeschlossen) Die durchschnittliche Latenz in Tagen vom letzten Ereignis zu einer Konversion. |
| [!UICONTROL Path Frequency] | Benutzerdefiniert | Die Häufigkeit, mit der der Pfad für diese Zeile vor der Konvertierung aufgetreten ist. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Über Hilfsberichte](assist-report-about.md)
>* [Die [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Die [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Berichtseinstellungen für Hilfe](assist-report-settings.md)
>* [Hilfsbericht erstellen](assist-report-generate.md)

