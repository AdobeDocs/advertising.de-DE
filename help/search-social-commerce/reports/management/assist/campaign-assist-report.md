---
title: '[!UICONTROL Campaign Assist Report]'
description: Erfahren Sie mehr über die [!UICONTROL Campaign Assist Report].
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
source-git-commit: 7a87d3c3827125adb97f50986823568c9aef8c24
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 1%

---

# Die [!UICONTROL Campaign Assist Report]

*Werbetreibende mit Klick-Tracking für Suche, Social und Commerce und mit Konversions-Tracking aus Adobe Advertising, Adobe Analytics (mit einer [!DNL Analytics]-Integration) oder bereitgestellt in -Feeds nur mit einem Token (`ef_id`)*

Die [!UICONTROL Campaign Assist Report] gibt an, welche Kampagnen den Konvertierungsprozess unterstützt haben. Der Bericht zeigt, wie jedes Kampagnenmuster, dessen Anzeigen zu einer oder mehreren Konversionen geführt haben, zu Ihren Gesamtkonversionen beigetragen hat. Sie können beispielsweise sehen, wie viele Konversionen stattgefunden haben, wenn Benutzende zum ersten Mal eine Anzeige aus Kampagne A gesehen, dann auf eine Anzeige aus Kampagne B geklickt und dann eine Bestellung aufgegeben haben. Auf ähnliche Weise können Sie sehen, wie viele Konversionen aufgetreten sind, nachdem Benutzende mit Anzeigen aus mehr als 10 Kampagnen interagiert haben.

Die Berichtsergebnisse enthalten aggregierte Daten für jedes Kampagnenmuster im Konversionspfad - bis hin zu den N frühesten Kampagnen - für Ereignisse, die im [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) des Werbetreibenden aufgetreten sind. Wenn Sie beispielsweise eine Pfadgröße von fünf (5) auswählen, enthält der Bericht Konversionspfade, die bis zu den fünf frühesten Kampagnen umfassten, wobei für jedes Muster von Kampagnen, deren Ereignisse verfolgt wurden, eine Zeile vorhanden ist. Jede Zeile zeigt ein Muster von Kampagnen an, einschließlich der ersten Kampagne im Pfad und der letzten Kampagne, die zu Konversionen geführt hat (auch wenn die letzte Kampagne außerhalb der angegebenen Pfadgröße liegt). Standardmäßig werden die Zeilen in aufsteigender Reihenfolge nach der Anzahl der Kampagnen im Pfad sortiert.

Optional können Sie für jede Zeile aggregierte Konversionsdaten einschließen, einschließlich Ihrer benutzerdefinierten Metriken. Wenn Sie die Spalten „Konversionen/Umsatz“ in den Bericht aufnehmen, wird jeder Konversionstyp in vier Spalten dargestellt und zeigt a) die Gesamtzahl der Konversionen, b) den Prozentsatz Ihrer Gesamtkonversionen, die diesem Kampagnenmuster zugeordnet wurden, c) die durchschnittliche Latenz in Tagen vom ersten Ereignis (in der ersten Kampagne) bis zu einer Konversion und d) die durchschnittliche Latenz in Tagen vom letzten Ereignis (in der letzten Kampagne) bis zu einer Konversion an. Wenn der Konversionspfad mehr Kampagnen als die angegebene Pfadgröße enthält, enthält der Bericht zusätzliche Zeilen, in denen Daten für Konversionen aggregiert werden, die aus der höheren Anzahl von Kampagnen resultieren (z. B. alle Muster, die sechs Kampagnen enthalten).

Optional können Sie auch das Werbenetzwerk und/oder den Ereignistyp nach dem Kampagnennamen einfügen, z. B. `<campaign name> (Google) click`.

Sie können Daten der vorherigen 18 Monate anzeigen.

>[!TIP]
>
>Wenn sich Ihre Markenschlüsselwörter in einer anderen Kampagne befinden als Ihre generischen Schlüsselwörter, gibt der Bericht an, ob Ihre Markenschlüsselwörter zu Konversionen beitragen.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus dem Abschnitt Spalten der Berichtseinstellungen hinzufügen.

| Spalte | Standard? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] zu [!UICONTROL 5th Campaign] | Standard | Die fünf frühesten Kampagnen im Konversionspfad, die innerhalb des (Klick[Lookback-Fensters des Advertisers und &#x200B;](/help/search-social-commerce/glossary.md#c-d)Impression-Lookback[Fensters aufgetreten &#x200B;](/help/search-social-commerce/glossary.md#i-j).<br><br>Wenn Sie eine der Berichtsoptionen einbezogen haben, um das Anzeigennetzwerk, den Kontonamen oder den Ereignistyp nach dem Entitätsnamen anzugeben, werden diese Informationen nach dem Kampagnennamen eingefügt (z. B. &quot;`"<"campaign name> [Google] [Account1] [impression]`„). |
| [!UICONTROL Path Size] | Standard | Die Anzahl der Kampagnen im Konversionspfad, die innerhalb des (Klick[Lookback-Fensters und &#x200B;](/help/search-social-commerce/glossary.md#c-d)Impression-Lookback[&#x200B; des Advertisers aufgetreten &#x200B;](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Standard | Die erste Kampagne im Konversionspfad. |
| [!UICONTROL Last Campaign] | Standard | Die letzte Kampagne, die zu Konversionen geführt hat (auch wenn das letzte Keyword außerhalb der angegebenen Pfadgröße liegt).<br><br>Wenn Sie eine der Berichtsoptionen einbezogen haben, um das Anzeigennetzwerk, den Kontonamen oder den Ereignistyp nach dem Entitätsnamen anzugeben, werden diese Informationen nach dem Kampagnennamen eingefügt (z. B. &quot;`"<"campaign name> [Google] [Account1] [impression]`„). |
| \[Advertiser-spezifische benutzerdefinierte (abgeleitete) Metriken\] | Benutzerdefiniert | Der Wert für eine von Ihnen erstellte benutzerdefinierte Metrik, die aus vorhandenen Metriken berechnet wird. |
| \[Advertiser-spezifische Konversionsmetriken\] | Benutzerdefiniert | Die Anzahl der Konversionen für eine bestimmte Konversionsmetrik oder Site-Interaktionsmetrik. |
| [!UICONTROL % of Total] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe für jede enthaltene Konversionsmetrik enthalten) Die Anzahl der Konversionen für eine angegebene Konversionsmetrik, die aus dem Kampagnenmuster resultierte. |
| [!UICONTROL 6th Campaign] zu [!UICONTROL 20th Campaign] | Benutzerdefiniert | Die sechste bis zwanzigste Kampagne im Konversionspfad, die innerhalb des (Klick[Lookback-Fensters des Advertisers &#x200B;](/help/search-social-commerce/glossary.md#c-d) (Impression[Lookback-Fenster) &#x200B;](/help/search-social-commerce/glossary.md#i-j).<br><br>Wenn Sie eine der Berichtsoptionen einbezogen haben, um das Anzeigennetzwerk, den Kontonamen oder den Ereignistyp nach dem Entitätsnamen anzugeben, werden diese Informationen nach dem Kampagnennamen eingefügt (z. B. &quot;`"<"campaign name> [Baidu] [Account1] [click]`„). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe für jede enthaltene Konversionsmetrik enthalten) Die durchschnittliche Latenz in Tagen vom ersten Ereignis (in der ersten Kampagne) bis zu einer Konversion. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe enthalten) Die durchschnittliche Latenz in Tagen vom letzten Ereignis (in der letzten Kampagne) bis zu einer Konversion. |
| [!UICONTROL EF Campaign ID] | Benutzerdefiniert | Die numerische ID, die Search, Social und Commerce der Kampagne zuweist. |
| [!UICONTROL EF Portfolio Group ID] | Benutzerdefiniert | Die numerische ID für die Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL EF Search Engine ID] | Benutzerdefiniert | Die numerische ID, die Search, Social und Commerce dem Anzeigennetzwerk zuweist: <i>[!UICONTROL 3]</i> für [!DNL Google Ads], <i>[!UICONTROL 10]</i> für [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> für [!DNL Meta], <i>[!UICONTROL 86]</i> für [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> für [!DNL Naver], <i>[!UICONTROL 88]</i> für [!DNL Baidu], <i>[!UICONTROL 90]</i> für [!DNL Yandex], <i>[!UICONTROL 94]</i> für [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> für [!DNL Yahoo Native] (veraltet) oder <i>[!UICONTROL 106]</i> für [!DNL Pinterest] (veraltet). |
| [!UICONTROL Portfolio ID] | Benutzerdefiniert | Die numerische Portfolio-ID. |
| [!UICONTROL User SE Account ID] | Benutzerdefiniert | Die numerische ID, die Search, Social und Commerce dem Anzeigennetzwerk zuweist. |

>[!MORELIKETHIS]
>
>* [Über Hilfsberichte](assist-report-about.md)
>* [Die [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Die [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Unterstützen von Berichteinstellungen](assist-report-settings.md)
>* [Erstellen eines Assist-Berichts](assist-report-generate.md)
