---
title: '[!UICONTROL Keyword Assist Report]'
description: Erfahren Sie mehr über die [!UICONTROL Keyword Assist Report].
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# Die [!UICONTROL Keyword Assist Report]

*Werbetreibende mit Klick-Tracking für Search, Social und Commerce und mit Konversions-Tracking von Adobe Advertising, Adobe Analytics (mit einer [!DNL Analytics]-Integration) oder bereitgestellt in -Feeds nur mit einem Token (`ef_id`)*

Die [!UICONTROL Keyword Assist Report] gibt an, welche Keywords oder Platzierungen Klicks fördern. Der Bericht zeigt jedes Muster von Paid Search-Keywords oder Platzierungen, die Klicks in einem Konversionspfad erhalten haben, und zeigt an, wie dieses Muster zu Ihren Gesamtkonversionen beigetragen hat. Sie können beispielsweise sehen, wie viele Konversionen aufgetreten sind, wenn Benutzer zuerst auf eine Anzeige geklickt haben, die aus der Keyword-Suche nach „Lederschuhe“ resultiert, dann auf eine Anzeige geklickt haben, nachdem ein Keyword nach „Wildlederschuhe“ gesucht und dann eine Bestellung aufgegeben hat, oder Sie können sehen, wie viele Konversionen stattgefunden haben, nachdem Benutzer auf Anzeigen geklickt haben, die aus mehr als 10 Keywords hervorgegangen sind.

Die Berichtsergebnisse enthalten aggregierte Daten für bis zum N frühesten Paid-Search-Keyword oder Platzierungsklicks im Konversionspfad, die in den
Klicken Sie auf Lookback- und Impression-Lookback-Fenster. Wenn Sie beispielsweise eine Pfadgröße von fünf (5) auswählen, besteht der Bericht aus Konversionspfaden, die bis zu den fünf frühesten Keywords oder Platzierungen enthalten, die Klicks erhalten haben, wobei für jedes Klickmuster eine Zeile angegeben wird. Jede Zeile enthält das erste Keyword oder die erste Platzierung im Pfad und das letzte Keyword oder die letzte Platzierung, die zu Konversionen geführt hat (auch wenn das letzte Keyword außerhalb der angegebenen Pfadgröße liegt). Standardmäßig werden die Zeilen in aufsteigender Reihenfolge nach der Anzahl der Ereignisse im Pfad sortiert.

>[!NOTE]
>
>Wenn der Bericht Platzierungen aus inhaltsaktivierten Suchkampagnen enthält (die keine Keywords enthalten), zeigt die Spalte [!UICONTROL Keyword] die entsprechenden Anzeigengruppennamen an, wie z. B. „Anzeigengruppeninhalt: Ihr Anzeigengruppenname“.

Optional können Sie aggregierte Konversionsdaten für jede Zeile einbeziehen. Wenn Sie Konversionen/Umsatz -Spalten in den Bericht einbeziehen, wird jeder Konversionstyp in vier Spalten dargestellt, die a) die Gesamtzahl der Konversionen, b) den Prozentsatz Ihrer Gesamtkonversionen, die diesem Keyword-Muster zugeordnet wurden, c) die durchschnittliche Latenz in Tagen vom ersten Ereignis (beim ersten Keyword) bis zu einer Konversion und d) die durchschnittliche Latenz in Tagen vom letzten Ereignis (beim letzten Keyword) bis zu einer Konversion anzeigen. Wenn der Konvertierungspfad mehr Keywords als die angegebene Pfadgröße enthält, enthält der Bericht zusätzliche Zeilen, in denen Daten für Konversionen aggregiert werden, die aus der höheren Anzahl von Keywords resultieren (z. B. allen Mustern, die Klicks auf sechs Keywords enthalten).

Sie können Daten der vorherigen 18 Monate anzeigen.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus dem Abschnitt Spalten der Berichtseinstellungen hinzufügen.

| Spalte | Standard? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] zu [!UICONTROL 5th Keyword] | Standard | Die fünf frühesten Paid Search-Keywords oder Platzierungs-Klicks im Konversionspfad, die im [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster des Werbetreibenden aufgetreten ](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Hinweis:</b> Wenn der Bericht Platzierungen aus inhaltsaktivierten Suchkampagnen (die keine Keywords enthalten) enthält, zeigen diese Spalten stattdessen die entsprechenden Anzeigengruppennamen an, z. B. „Ihr Anzeigengruppenname (AdGroup-Inhalt)“. |
| [!UICONTROL Path Size] | Standard | Die Anzahl der Keywords und/oder Platzierungen im Konversionspfad, die innerhalb des (Klick[Lookback-Fensters des Advertisers ](/help/search-social-commerce/glossary.md#c-d) (Impression[Lookback-Fenster) ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Standard | Das erste Keyword oder die erste Platzierung im Konversionspfad. |
| [!UICONTROL Last Keyword] | Standard | Das letzte Keyword oder die letzte Platzierung, die zu Konversionen geführt hat (selbst wenn das letzte Keyword außerhalb der angegebenen Pfadgröße liegt). |
| \[Advertiser-spezifische benutzerdefinierte (abgeleitete) Metriken\] | Benutzerdefiniert | Der Wert für eine von Ihnen erstellte benutzerdefinierte Metrik, die aus vorhandenen Metriken berechnet wird. |
| \[Advertiser-spezifische Konversionsmetriken\] | Benutzerdefiniert | Die Anzahl der Konversionen für eine bestimmte Konversionsmetrik oder Site-Interaktionsmetrik. |
| [!UICONTROL % of Total] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe für jede eingeschlossene Konversionsmetrik enthalten) Der Prozentsatz der Gesamtkonversionen in den Portfolios, die dem Keyword und/oder dem Platzierungsmuster zugeordnet wurden. |
| [!UICONTROL 6th Keyword] zu [!UICONTROL 10th Keyword] | Benutzerdefiniert | Das sechste bis zehnte Paid-Search-Keyword oder die Platzierungsklicks im Konversionspfad, die innerhalb des „Klick-Lookback[-Fensters ](/help/search-social-commerce/glossary.md#c-d) Impression-Lookback-[ des Werbetreibenden aufgetreten ](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Hinweis:</b> Wenn der Bericht Platzierungen aus inhaltsaktivierten Suchkampagnen (die keine Keywords enthalten) enthält, zeigen diese Spalten stattdessen die entsprechenden Anzeigengruppennamen an, z. B. „Ihr Anzeigengruppenname (AdGroup-Inhalt)“. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe für jede eingeschlossene Konversionsmetrik enthalten) Die durchschnittliche Latenz in Tagen vom ersten Ereignis (beim ersten Keyword oder der ersten Platzierung) bis zu einer Konversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[Konversionsmetrik\] | Automatisch | (Nicht in den Berichtseinstellungen verfügbar, aber automatisch in der Berichtsausgabe enthalten) Die durchschnittliche Latenz in Tagen vom letzten Ereignis (beim letzten Keyword oder der letzten Platzierung) bis zu einer Konversion. |
| [!UICONTROL Path Frequency] | Benutzerdefiniert | Die Häufigkeit, mit der der Pfad für diese Zeile vor der Konvertierung aufgetreten ist. |

>[!MORELIKETHIS]
>
>* [Über Hilfsberichte](assist-report-about.md)
>* [Die [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Die [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Unterstützen von Berichteinstellungen](assist-report-settings.md)
>* [Erstellen eines Assist-Berichts](assist-report-generate.md)
