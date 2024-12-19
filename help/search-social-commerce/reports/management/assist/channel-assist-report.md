---
title: '[!UICONTROL Channel Assist Report]'
description: Erfahren Sie mehr über die [!UICONTROL Channel Assist Report].
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
source-git-commit: 45920c6ea9d2953c963ddf6472966b3fc3a91395
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# Die [!UICONTROL Channel Assist Report]

*Werbetreibende mit Klick-Tracking für Search, Social und Commerce und mit Konversions-Tracking von Adobe Advertising, Adobe Analytics (mit einer [!DNL Analytics]-Integration) oder bereitgestellt in -Feeds nur mit einem Token (`ef_id`)*

Die [!UICONTROL Channel Assist Report] geben an, wie verschiedene Marketing-Kanäle (Suche oder Social Media aus Search, Social und Commerce; oder Display oder Video aus Advertising DSP) den Konvertierungsprozess unterstützt haben. Der Bericht zeigt, wie jedes Muster von Ereignistypen, das zu einer oder mehreren Konversionen geführt hat, zu Ihren Gesamtkonversionen beigetragen hat. Sie können beispielsweise sehen, wie viele Konversionen stattgefunden haben, wenn Benutzer zum ersten Mal eine Display-Anzeigenimpression gesehen und dann auf eine Suchanzeige geklickt und eine Bestellung aufgegeben haben, oder Sie können sehen, wie viele Konversionen aufgetreten sind, nachdem Benutzer mit mehr als 10 Anzeigen interagiert haben. Zu den Ereignistypen gehören Such-Klicks, Display-Impressionen und -Klicks, Video-Impressionen und -Klicks und andere Impressionen und andere Klicks. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

Die Berichtsergebnisse enthalten aggregierte Daten für jedes Muster von Ereignistypen im Konversionspfad - bis hin zu den N frühesten Ereignistypen -, die innerhalb des [Klick-Lookback-Fensters](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fensters](/help/search-social-commerce/glossary.md#i-j) des Werbetreibenden aufgetreten sind. Wenn Sie beispielsweise eine Pfadgröße von fünf (5) auswählen, enthält der Bericht Konversionspfade, die bis zu den fünf frühesten Ereignissen enthalten, wobei für jedes Muster der verfolgten Ereignistypen eine Zeile vorhanden ist (z. B. „Suchklick“ und dann „Display-Impression„). Jede Zeile zeigt ein Ereignismuster, einschließlich des ersten Ereignisses im Pfad und des letzten Ereignisses, das zu Konversionen geführt hat (auch wenn das letzte Ereignis außerhalb der angegebenen Pfadgröße liegt). Standardmäßig werden die Zeilen in aufsteigender Reihenfolge nach der Anzahl der Ereignisse im Pfad sortiert.

Optional können Sie aggregierte Konversionsdaten für jede Zeile einbeziehen. Wenn Sie Konversionen/Umsatz -Spalten in den Bericht einbeziehen, wird jeder Konversionstyp in vier Spalten dargestellt, die a) die Gesamtzahl der Konversionen, b) den Prozentsatz Ihrer gesamten Konversionen, die diesem Ereignismuster zugeordnet wurden, c) die durchschnittliche Latenz in Tagen vom ersten Ereignis bis zu einer Konversion und d) die durchschnittliche Latenz in Tagen vom letzten Ereignis bis zu einer Konversion anzeigen. Wenn der Konvertierungspfad mehr Ereignisse als die angegebene Pfadgröße enthält, enthält der Bericht zusätzliche Zeilen, in denen Daten für Konversionen aggregiert werden, die aus der höheren Anzahl von Ereignissen resultieren (z. B. alle Muster, die sechs Ereignistypen enthalten).

Sie können Daten der vorherigen 18 Monate anzeigen.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus dem Abschnitt Spalten der Berichtseinstellungen hinzufügen.

| Spalte | Standard? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] zu [!UICONTROL 5th Event] | Standard | Die fünf frühesten Ereignistypen im Konversionspfad, die innerhalb des (Klick[Lookback-Fensters des Advertisers und ](/help/search-social-commerce/glossary.md#c-d)Impression-Lookback[Fensters aufgetreten ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Standard | Die Anzahl der Ereignistypen im Konversionspfad, die innerhalb des (Klick[Lookback-Fensters und ](/help/search-social-commerce/glossary.md#c-d)Impression-Lookback[ des Advertisers aufgetreten ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | Standard | Der Ereignistyp des ersten (frühesten) Ereignisses im Konversionspfad. |
| [!UICONTROL Last Event Type] | Standard | Der Ereignistyp des letzten Ereignisses, das zu Konversionen geführt hat (auch wenn das letzte Ereignis außerhalb der angegebenen Pfadgröße liegt). |
| \[Advertiser-spezifische benutzerdefinierte (abgeleitete) Metriken\] | Benutzerdefiniert | Der Wert für eine von Ihnen erstellte benutzerdefinierte Metrik, die aus vorhandenen Metriken berechnet wird. |
| \[Advertiser-spezifische Konversionsmetriken\] | Benutzerdefiniert | Die Anzahl der Konversionen für eine bestimmte Konversionsmetrik oder Site-Interaktionsmetrik. |
| [!UICONTROL % of Total] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe für jede enthaltene Konversionsmetrik enthalten) Der Prozentsatz der Gesamtkonversionen in den Portfolios, die dem Ereignismuster zugeordnet wurden. |
| [!UICONTROL 6th Event] zu [!UICONTROL 30th Event] | Benutzerdefiniert | Der sechste bis 30. Ereignistyp im Konversionspfad, der innerhalb des (Klick[Lookback-Fensters des Advertisers ](/help/search-social-commerce/glossary.md#c-d) (Impression[Lookback-Fenster) ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe für jede eingeschlossene Konversionsmetrik enthalten) Die durchschnittliche Latenz in Tagen vom ersten Ereignis bis zu einer Konversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe enthalten) Die durchschnittliche Latenz in Tagen vom letzten Ereignis bis zu einer Konversion. |
| [!UICONTROL Path Frequency] | Benutzerdefiniert | Die Häufigkeit, mit der der Pfad für diese Zeile vor der Konvertierung aufgetreten ist. |

>[!MORELIKETHIS]
>
>* [Über Hilfsberichte](assist-report-about.md)
>* [Die [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Die [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Unterstützen von Berichteinstellungen](assist-report-settings.md)
>* [Erstellen eines Assist-Berichts](assist-report-generate.md)
