---
title: Adobe Advertising von Metriken in Analysis Workspace
description: Adobe Advertising von Metriken in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Adobe Advertising von Metriken in Analysis Workspace

*Advertiser mit nur Adobe Advertising-Adobe Analytics-Integration*

>[!NOTE]
>
>* Adobe Advertising übergibt Traffic-Metriken und -Dimensionen an [!DNL Analytics] täglich.
>* [!DNL Analytics] erfasst Adobe Advertising-Clickthroughs und Durchsichten in Echtzeit.
>* Für [!DNL Search, Social, & Commerce]festgelegt ist, wird diese Funktion für die meisten Anzeigennetzwerke und Kampagnentypen unterstützt. Siehe &quot;[Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)&quot; in der [!DNL Search, Social, & Commerce] Handbuch für weitere Informationen.

## Traffic-Metriken von Adobe Advertising

Adobe Advertising von Traffic-Metriken in [!DNL Analytics] beginnen normalerweise mit &quot;Adobe Advertising&quot;, mit Ausnahme von &quot;[!UICONTROL AMO ID Instances].&quot; Bei langfristigen Kunden, die zum Erstellen von Metriken für Klicks, Kosten und Impressionen ein benutzerspezifisches Ereignis (statt eines reservierten Ereignisses) verwendet haben, beginnen diese Metriken jedoch weiterhin mit &quot;AMO&quot;.

| Traffic-Metrik | Beschreibung |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] oder (einige ältere Kunden) [!UICONTROL AMO Clicks] | Die Anzahl der Adobe Advertising-Klicks insgesamt. |
| [!UICONTROL Adobe Advertising Cost] oder (einige ältere Kunden) [!UICONTROL AMO Cost] | Die Adobe Advertising gibt in der Währung der Report Suite aus. |
| [!UICONTROL Adobe Advertising Impressions] oder (einige ältere Kunden) [!UICONTROL AMO Impressions] | Die Anzahl der Adobe Advertising-Impressionen. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Die Anzahl der Impressionen, für die die Sichtbarkeitsinstrumentierung erfolgreich initialisiert wurde. Dieser Wert wird berechnet als (instrumentierte Impressionen - die Anzahl nicht messbarer Impressionen). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Die Anzahl der Minuten, in denen ein Adobe Advertising-Video angesehen wurde. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Die Anzahl der Impressionen, die als nicht sichtbar identifiziert wurden. Dieser Wert wird als ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Die Anzahl der Impressionen, die gemäß der Platzierungskonfiguration als sichtbar gemessen wurden. |
| [!UICONTROL Adobe Advertising Views] | Die Anzahl der Ansichten auf einer Anzeige. Eine Ansicht wird gezählt, wenn der Viewer das Adobe Advertising-Video initiiert. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Die Anzahl der Ansichten, bei denen mindestens 25 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Die Anzahl der Ansichten, bei denen mindestens 50 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Die Anzahl der Ansichten, bei denen mindestens 75 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Die Anzahl der Ansichten, bei denen 100 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO ID Instances] | Die Häufigkeit der [!UICONTROL AMO ID] festgelegt ist. |

## Adobe Advertising-Dimensionen

>[!NOTE]
>
>Alle Adobe Advertising-Dimensionen in [!DNL Analytics] gefolgt von &quot;[!DNL (AMO ID)].&quot;

| Dimension | Anwendbare Adobe Advertising-Daten | Beschreibung |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Advertising DSP oder der Name der Suchmaschine |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Der Kontoname. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) oder dem Namen des Werbenetzwerks ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Der Kampagnenname. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Das Paket ([!DNL DSP]) oder Portfolio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Der Platzierungsname. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | Der Anzeigengruppenname. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | Das Keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Der Suchübereinstimmungstyp. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Keyword und Übereinstimmungstyp. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Der Anzeigentyp, z. B. `text`, `video`, `display`oder `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Der Anzeigentyp ([!DNL DSP]) oder Anzeigentitel ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Die Anzeigenbeschreibung ([!DNL DSP]) oder Anzeigenkörper ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | Die in der Anzeige angezeigte URL. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | Die Ziel-URL für die Anzeige. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Ob der Einstieg in die Landingpage eine Durchsicht oder ein Clickthrough war. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | Das Produktziel für eine Produktlistenanzeige. |

## Nützliche benutzerspezifische berechnete Metriken zum Adobe Advertising

Erwägen Sie die Erstellung der folgenden Metriken für Ihre Adobe Advertising-Daten.

* Klicks zur Landingpage-Instanz ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): Dies ist der Prozentsatz der Personen, die auf die Anzeige geklickt und sie zur Landingpage weitergeleitet haben.
* Messrate ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Sichtbare Impressionsrate ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Kosten pro Ansicht ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Kosten pro Klick ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
