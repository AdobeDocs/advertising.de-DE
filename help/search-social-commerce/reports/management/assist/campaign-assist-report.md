---
title: "[!UICONTROL Campaign Assist Report]"
description: Erfahren Sie mehr über die [!UICONTROL Campaign Assist Report].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# Die [!UICONTROL Campaign Assist Report]

*Werbetreibende mit Klick-Tracking in Search, Social und Commerce und Konversions-Tracking aus Adobe Advertising, Adobe Analytics (mit einer [!DNL Analytics] -Integration) oder in Feeds mit einem Token (`ef_id`) nur*

Die [!UICONTROL Campaign Assist Report] gibt an, welche Kampagnen den Konvertierungsprozess unterstützt haben. Die Berichte zeigen, wie die einzelnen Muster von Kampagnen, deren Anzeigen zu einer oder mehreren Konversionen geführt haben, zu Ihren Gesamtkonversionen beigetragen haben. Sie können beispielsweise sehen, wie viele Konversionen stattgefunden haben, wenn Benutzer zum ersten Mal eine Anzeige aus Kampagne A gesehen, dann auf eine Anzeige aus Kampagne B geklickt und dann eine Bestellung aufgegeben haben. Auf ähnliche Weise können Sie sehen, wie viele Konversionen stattgefunden haben, nachdem Benutzer mit Anzeigen aus mehr als 10 Kampagnen interagiert haben.

Die Berichtsergebnisse enthalten aggregierte Daten für jedes Kampagnenmuster im Konversionspfad - bis zu den N frühesten Kampagnen - für Ereignisse, die innerhalb der des Advertisers aufgetreten sind [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). Wenn Sie beispielsweise eine Pfadgröße von 5 (5) auswählen, enthält der Bericht Konversionspfade, die bis zu den fünf frühesten Kampagnen umfassten, mit einer Zeile für jedes Muster von Kampagnen, deren Ereignisse verfolgt wurden. Jede Zeile zeigt ein Muster von Kampagnen, einschließlich der ersten Kampagne im Pfad und der letzten Kampagne, die zu Konversionen geführt hat (auch wenn die letzte Kampagne außerhalb der angegebenen Pfadgröße liegt). Standardmäßig sind die Zeilen nach der Anzahl der Kampagnen im Pfad in aufsteigender Reihenfolge angeordnet.

Optional können Sie für jede Zeile aggregierte Konversionsdaten einschließen, einschließlich Ihrer benutzerdefinierten Metriken. Wenn Sie Konversions-/Umsatzspalten in den Bericht einbeziehen, wird jeder Konversionstyp in vier Spalten dargestellt: a) die Gesamtanzahl der Konversionen, b) der Prozentsatz Ihrer Konversionen insgesamt, die diesem Kampagnenmuster zugeordnet wurden, c) die durchschnittliche Latenz in Tagen vom ersten Ereignis (in der ersten Kampagne) zu einer Konversion und d) die durchschnittliche Latenz in Tagen vom letzten Ereignis (in der letzten Kampagne) bis zur Konversion. Wenn der Konversionspfad mehr Kampagnen als die angegebene Pfadgröße enthält, enthält der Bericht zusätzliche Zeilen, in denen Daten für Konversionen aggregiert werden, die aus der höheren Anzahl von Kampagnen resultieren (z. B. alle Muster, die sechs Kampagnen enthielten).

Sie können optional auch das Anzeigennetzwerk und/oder den Ereignistyp nach dem Kampagnennamen einfügen, z. B. `<campaign name> (Google) click`.

Sie können Daten der letzten 18 Monate anzeigen.

>[!TIP]
>
>Wenn sich Ihre Markenkeywords in einer anderen Kampagne befinden als Ihre allgemeinen Suchbegriffe, zeigt der Bericht an, ob Ihre Markenkeywords zu Konversionen beitragen.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus dem Bereich Spalten der Berichtseinstellungen hinzufügen.

| Spalte | Standard? | Beschreibung |
|----|----|
| [!UICONTROL 1st Campaign] nach [!UICONTROL 5th Campaign] | Standard | Die fünf frühesten Kampagnen im Konversionspfad, die innerhalb der des Advertisers aufgetreten sind [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j).<br><br>Wenn Sie eine der Berichtsoptionen zur Angabe des Anzeigennetzwerks, des Kontonamens oder des Ereignistyps nach dem Entitätsnamen eingeschlossen haben, werden diese Informationen nach dem Kampagnennamen (z. B. `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| [!UICONTROL Path Size] | Standard | Die Anzahl der Kampagnen im Konversionspfad, die innerhalb der [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Standard | Die erste Kampagne im Konversionspfad. |
| [!UICONTROL Last Campaign] | Standard | Die letzte Kampagne, die zu Konversionen führte (auch wenn der letzte Suchbegriff außerhalb der angegebenen Pfadgröße liegt).<br><br>Wenn Sie eine der Berichtsoptionen zur Angabe des Anzeigennetzwerks, des Kontonamens oder des Ereignistyps nach dem Entitätsnamen eingeschlossen haben, werden diese Informationen nach dem Kampagnennamen (z. B. `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| \[Advertiser-spezifische benutzerdefinierte (abgeleitete) Metriken\] | Benutzerdefiniert | Der Wert für eine von Ihnen erstellte benutzerdefinierte Metrik, der aus vorhandenen Metriken berechnet wird. |
| \[Advertiser-spezifische Transaktionseigenschaften\] | Benutzerdefiniert | Die Anzahl der Konversionen für eine angegebene Transaktionseigenschaft oder Site-Interaktionsmetrik. |
| [!UICONTROL % of Total] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in die Berichtsausgabe für jede Transaktionseigenschaft eingeschlossen) Die Anzahl der Konversionen für eine bestimmte Transaktionseigenschaft, die aus dem Kampagnenmuster resultierte. |
| [!UICONTROL 6th Campaign] nach [!UICONTROL 20th Campaign] | Benutzerdefiniert | Die sechsten bis zwanzigsten Kampagnen im Konversionspfad, die innerhalb der vom Advertiser verwendeten [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j).<br><br>Wenn Sie eine der Berichtsoptionen zur Angabe des Anzeigennetzwerks, des Kontonamens oder des Ereignistyps nach dem Entitätsnamen eingeschlossen haben, werden diese Informationen nach dem Kampagnennamen (z. B. `"<"campaign name> [Baidu] [Account1] [click]`&quot;). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in die Berichtsausgabe für jede Transaktionseigenschaft eingeschlossen) Die durchschnittliche Latenz in Tagen vom ersten Ereignis (in der ersten Kampagne) bis hin zu einer Konversion. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe eingeschlossen) Die durchschnittliche Latenz in Tagen vom letzten Ereignis (in der letzten Kampagne) bis hin zu einer Konversion. |
| [!UICONTROL EF Campaign ID] | Benutzerdefiniert | Die numerische ID, die Search, Social und Commerce der Kampagne zuweisen. |
| [!UICONTROL EF Portfolio Group ID] | Benutzerdefiniert | Die numerische ID für die Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL EF Search Engine ID] | Benutzerdefiniert | Die numerische ID, die Search, Social und Commerce dem Werbenetzwerk zuweist: <i>[!UICONTROL 3]</i> für [!DNL Google Ads], <i>[!UICONTROL 10]</i> für [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> für [!DNL Meta], <i>[!UICONTROL 86]</i> für [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> für [!DNL Naver], <i>[!UICONTROL 88]</i> für [!DNL Baidu], <i>[!UICONTROL 90]</i> für [!DNL Yandex], <i>[!UICONTROL 94]</i> für [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> für [!DNL Yahoo Native] (veraltet) oder <i>[!UICONTROL 106]</i> für [!DNL Pinterest] (nicht mehr unterstützt). |
| [!UICONTROL Portfolio ID] | Die numerische Portfolio-ID. |
| [!UICONTROL User SE Account ID] | Die numerische ID, die Search, Social und Commerce dem Werbenetzwerk zuweist. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Über Hilfsberichte](assist-report-about.md)
>* [Die [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Die [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Berichtseinstellungen für Hilfe](assist-report-settings.md)
>* [Hilfsbericht erstellen](assist-report-generate.md)

