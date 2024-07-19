---
title: Adobe Advertising von Metriken in Analysis Workspace
description: Adobe Advertising von Metriken in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Adobe Advertising von Metriken in Analysis Workspace

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

>[!NOTE]
>
>* Adobe Advertising übergibt Traffic-Metriken und -Dimensionen an [!DNL Analytics] täglich.
>* [!DNL Analytics] erfasst Adobe Advertising-Clickthroughs und Durchsichten in Echtzeit.
>* Für [!DNL Search, Social, & Commerce] wird diese Funktion für die meisten Anzeigennetzwerke und Kampagnentypen unterstützt. Weitere Informationen finden Sie unter &quot;[Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)&quot;im [!DNL Search, Social, & Commerce]-Handbuch.

## Traffic-Metriken von Adobe Advertising

Adobe Advertising-Traffic-Metriken in [!DNL Analytics] beginnen normalerweise mit &quot;Adobe Advertising&quot;, außer &quot;[!UICONTROL AMO ID Instances]&quot;. Bei langfristigen Kunden, die zum Erstellen von Metriken für Klicks, Kosten und Impressionen ein benutzerspezifisches Ereignis (statt eines reservierten Ereignisses) verwendet haben, beginnen diese Metriken jedoch weiterhin mit &quot;AMO&quot;.

| Traffic-Metrik | Beschreibung |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] oder (einige ältere Kunden) [!UICONTROL AMO Clicks] | Die Anzahl der Adobe Advertising-Klicks insgesamt. |
| [!UICONTROL Adobe Advertising Cost] oder (einige ältere Kunden) [!UICONTROL AMO Cost] | Die Adobe Advertising gibt in der Währung der Report Suite aus. |
| [!UICONTROL Adobe Advertising Impressions] oder (einige ältere Kunden) [!UICONTROL AMO Impressions] | Die Anzahl der Adobe Advertising-Impressionen. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Die Anzahl der Impressionen, für die die Sichtbarkeitsinstrumentierung erfolgreich initialisiert wurde. Dieser Wert wird berechnet als (instrumentierte Impressionen - die Anzahl nicht messbarer Impressionen). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Die Anzahl der Minuten, in denen ein Adobe Advertising-Video angesehen wurde. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Die Anzahl der Impressionen, die als nicht sichtbar identifiziert wurden. Dieser Wert wird als ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]) berechnet. |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Die Anzahl der Impressionen, die gemäß der Platzierungskonfiguration als sichtbar gemessen wurden. |
| [!UICONTROL Adobe Advertising Views] | Die Anzahl der Ansichten auf einer Anzeige. Eine Ansicht wird gezählt, wenn der Viewer das Adobe Advertising-Video initiiert. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Die Anzahl der Ansichten, bei denen mindestens 25 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Die Anzahl der Ansichten, bei denen mindestens 50 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Die Anzahl der Ansichten, bei denen mindestens 75 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Die Anzahl der Ansichten, bei denen 100 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO ID Instances] | Die Häufigkeit, mit der der [!UICONTROL AMO ID] eingestellt wird. |

## Adobe Advertising-Dimensionen

>[!NOTE]
>
>Auf alle Adobe Advertising-Dimensionen in [!DNL Analytics] folgt &quot;[!DNL (AMO ID)]&quot;.

| Dimension | Anwendbare Adobe Advertising-Daten | Beschreibung |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | Advertising DSP oder der Name der Suchmaschine |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | Der Kontoname. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | RTB ([!DNL DSP]) oder der Name des Anzeigennetzwerks ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | Der Kampagnenname. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | Der Name des Pakets ([!DNL DSP]) oder Portfolios ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] Daten | Der Platzierungsname. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] Daten | Der Anzeigengruppenname. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] Daten | Das Keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] Daten | Der Suchübereinstimmungstyp. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] Daten | Keyword und Übereinstimmungstyp. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | Der Anzeigentyp, z. B. `text`, `video`, `display` oder `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | Der Anzeigentyp ([!DNL DSP]) oder der Anzeigentitel ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | Die Anzeigenbeschreibung ([!DNL DSP]) oder der Anzeigetext ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] Daten | Die in der Anzeige angezeigte URL. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] Daten | Die Ziel-URL für die Anzeige. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] - und [!DNL Search, Social, & Commerce] -Daten | Ob der Einstieg in die Landingpage eine Durchsicht oder ein Clickthrough war. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] Daten | Das Produktziel für eine Produktlistenanzeige. |

## Nützliche benutzerspezifische berechnete Metriken zum Adobe Advertising

Erwägen Sie die Erstellung der folgenden Metriken für Ihre Adobe Advertising-Daten.

* Klicks zur Landingpage-Instanz ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): Dies ist der Prozentsatz der Personen, die auf die Anzeige geklickt und sie zur Landingpage weitergeleitet haben.
* Messbare Rate ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Sichtbare Impressionsrate ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Kosten pro Ansicht ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Kosten pro Klick ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
