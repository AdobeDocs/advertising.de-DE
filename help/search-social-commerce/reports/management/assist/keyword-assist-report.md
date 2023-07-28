---
title: '[!UICONTROL Keyword Assist Report]'
description: Informationen zum [!UICONTROL Keyword Assist Report].
exl-id: 07de2880-111b-498f-9f7f-ec15f89230ae
feature: Search Reports, Search Assist Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Die [!UICONTROL Keyword Assist Report]

*Werbetreibende mit Klick-Tracking in Search, Social &amp; Commerce und Konversions-Tracking von Adobe Advertising, Adobe Analytics (mit einer [!DNL Analytics] -Integration) oder in Feeds mit einem Token (`ef_id`) nur*

Die [!UICONTROL Keyword Assist Report] gibt an, welche Suchbegriffe oder Platzierungen Klicks fördern. Der Bericht zeigt jedes Muster gebührenpflichtiger Suchbegriffe oder Platzierungen an, bei denen Klicks in einem Konversionspfad eingingen, und zeigt an, wie dieses Muster zu Ihren Gesamtkonversionen beigetragen hat. Sie würden beispielsweise sehen, wie viele Konversionen auftraten, wenn Benutzer zum ersten Mal auf eine Anzeige geklickt haben, die aus einer Suchbegriffsuche nach &quot;Lederschuhen&quot;resultierte, dann auf eine Anzeige nach einem Suchbegriff &quot;Wildlederschuhe&quot;geklickt und dann eine Bestellung aufgegeben haben. Andernfalls könnten Sie sehen, wie viele Konversionen auftraten, nachdem Benutzer auf Anzeigen geklickt hatten, die aus mehr als 10 Keywords stammten.

Die Berichtsergebnisse enthalten aggregierte Daten für den N frühesten gebührenpflichtigen Suchbegriff oder Platzierungsklicks im Konversionspfad, die innerhalb des Klick-Lookback- und Impression-Lookback-Fensters des Advertisers aufgetreten sind. Wenn Sie beispielsweise eine Pfadgröße von 5 (5) auswählen, besteht der Bericht aus Konversionspfaden, die bis zu den fünf frühesten Suchbegriffen oder Platzierungen mit Klicks enthielten, mit einer Zeile für jedes verfolgte Klickmuster. Jede Zeile enthält das erste Keyword oder die erste Platzierung im Pfad und das letzte Keyword bzw. die letzte Platzierung, das/die zu Konversionen geführt hat (auch wenn das letzte Keyword außerhalb der angegebenen Pfadgröße liegt). Standardmäßig werden die Zeilen nach der Anzahl der Ereignisse im Pfad in aufsteigender Reihenfolge angezeigt.

>[!NOTE]
>
>Wenn der Bericht Platzierungen aus inhaltsaktivierten Suchkampagnen enthält (die keine Keywords enthalten), wird die [!UICONTROL Keyword] zeigt die entsprechenden Anzeigengruppennamen an, z. B. &quot;(Anzeigengruppeninhalt) - Ihren Anzeigengruppennamen.&quot;

Sie können optional aggregierte Konversionsdaten für jede Zeile hinzufügen. Wenn Sie Konversions-/Umsatzspalten in den Bericht einbeziehen, wird jeder Konversionstyp in vier Spalten dargestellt: a) die Gesamtanzahl der Konversionen, b) der Prozentsatz Ihrer Konversionen insgesamt, die diesem Suchbegriffmuster zugeordnet wurden, c) die durchschnittliche Latenz in Tagen vom ersten Ereignis (im ersten Suchbegriff) bis zur Konversion und d) die durchschnittliche Latenz in Tagen vom letzten Ereignis (im letzten Suchbegriff) bis zur Konversion. Wenn der Konversionspfad mehr Suchbegriffe als die angegebene Pfadgröße enthält, enthält der Bericht zusätzliche Zeilen, die Daten für Konversionen aggregieren, die aus der höheren Anzahl von Suchbegriffen resultieren (z. B. alle Muster, die Klicks auf sechs Suchbegriffe enthielten).

Sie können Daten der letzten 18 Monate anzeigen.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus dem Bereich Spalten der Berichtseinstellungen hinzufügen.

| Spalte | Standard? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] nach [!UICONTROL 5th Keyword] | Standard | Die fünf frühesten Paid-Search-Suchkeywords oder Platzierungsklicks im Konversionspfad, die innerhalb der des Advertisers aufgetreten sind [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Hinweis:</b> Wenn der Bericht Platzierungen aus inhaltsaktivierten Suchkampagnen enthält (die keine Keywords enthalten), zeigen diese Spalten stattdessen die entsprechenden Anzeigengruppennamen an, z. B. &quot;(Anzeigengruppeninhalt) Ihr Anzeigengruppenname&quot;. |
| [!UICONTROL Path Size] | Standard | Die Anzahl der Suchbegriffe und/oder Platzierungen im Konversionspfad, die innerhalb der [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Standard | Das erste Keyword oder die erste Platzierung im Konversionspfad. |
| [!UICONTROL Last Keyword] | Standard | Das letzte Keyword oder die letzte Platzierung, das/die zu Konversionen führte (auch wenn das letzte Keyword außerhalb der angegebenen Pfadgröße liegt). |
| \[Advertiser-spezifische benutzerdefinierte (abgeleitete) Metriken\] | Benutzerdefiniert | Der Wert für eine von Ihnen erstellte benutzerspezifische Metrik, der aus vorhandenen Metriken berechnet wird. |
| \[Advertiser-spezifische Transaktionseigenschaften\] | Benutzerdefiniert | Die Anzahl der Konversionen für eine angegebene Transaktionseigenschaft oder Site-Interaktionsmetrik. |
| [!UICONTROL % of Total] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in die Berichtsausgabe für jede Transaktionseigenschaft eingeschlossen) Der Prozentsatz Ihrer Gesamtkonversionen in Portfolios, der dem Suchbegriff und/oder Platzierungsmuster zugeordnet wurde. |
| [!UICONTROL 6th Keyword] nach [!UICONTROL 10th Keyword] | Benutzerdefiniert | Der sechste bis zehnte Paid-Search-Suchbegriff oder die Platzierungsklicks im Konversionspfad, die innerhalb des vom Advertiser verwendeten [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Hinweis:</b> Wenn der Bericht Platzierungen aus inhaltsaktivierten Suchkampagnen enthält (die keine Keywords enthalten), zeigen diese Spalten stattdessen die entsprechenden Anzeigengruppennamen an, z. B. &quot;(Anzeigengruppeninhalt) Ihr Anzeigengruppenname&quot;. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in die Berichtsausgabe für jede Transaktionseigenschaft eingeschlossen) Die durchschnittliche Latenz in Tagen vom ersten Ereignis (im ersten Suchbegriff oder in der ersten Platzierung) bis hin zu einer Konversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[Transaktionseigenschaft\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe eingeschlossen) Die durchschnittliche Latenz in Tagen vom letzten Ereignis (am letzten Suchbegriff oder in der letzten Platzierung) bis hin zu einer Konversion. |
| [!UICONTROL Path Frequency] | Benutzerdefiniert | Die Häufigkeit, mit der der Pfad für diese Zeile vor der Konvertierung aufgetreten ist. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Über Hilfsberichte](assist-report-about.md)
>* [Die [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Die [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Berichtseinstellungen für Hilfe](assist-report-settings.md)
>* [Hilfsbericht erstellen](assist-report-generate.md)
