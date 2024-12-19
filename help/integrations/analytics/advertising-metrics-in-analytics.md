---
title: Adobe Advertising-Metriken in Analysis Workspace
description: Adobe Advertising-Metriken in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Adobe Advertising-Metriken in Analysis Workspace

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

>[!NOTE]
>
>* Adobe Advertising leitet Traffic-Metriken und -Dimensionen täglich an [!DNL Analytics] weiter.
>* [!DNL Analytics] erfasst Adobe Advertising-Clickthroughs und Viewthroughs in Echtzeit.
>* [!DNL Search, Social, & Commerce] wird diese Funktion für die meisten Werbenetzwerke und Kampagnentypen unterstützt. Weitere Informationen finden Sie [ „Unterstütztes ](/help/search-social-commerce/introduction/supported-inventory.md)&quot; im [!DNL Search, Social, & Commerce].

## Traffic-Metriken von Adobe Advertising

Adobe Advertising-Traffic-Metriken in [!DNL Analytics] beginnen normalerweise mit &quot;Adobe Advertising&quot;, mit Ausnahme von &quot;[!UICONTROL AMO ID Instances]&quot;. Für Langzeitkunden, die ein benutzerdefiniertes Ereignis (anstelle eines reservierten Ereignisses) verwendet haben, um ursprünglich Metriken für Klicks, Kosten und Impressionen zu erstellen, beginnen diese Metriken jedoch weiterhin mit „AMO“.

| Traffic-Metrik | Beschreibung |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] oder (einige ältere Kunden) [!UICONTROL AMO Clicks] | Die Gesamtzahl der Adobe Advertising-Klicks. |
| [!UICONTROL Adobe Advertising Cost] oder (einige ältere Kunden) [!UICONTROL AMO Cost] | Die Adobe Advertising-Ausgaben in der Währung der Report Suite. |
| [!UICONTROL Adobe Advertising Impressions] oder (einige ältere Kunden) [!UICONTROL AMO Impressions] | Die Anzahl der Adobe Advertising-Impressionen. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Die Anzahl der bereitgestellten Impressionen, für die die Sichtbarkeitsinstrumentierung erfolgreich initialisiert wurde. Dieser Wert wird als (instrumentierte Impressions - die Anzahl der nicht messbaren Impressions) berechnet. |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Die Anzahl der Minuten, die ein Adobe Advertising-Video angesehen wurde. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Die Anzahl der Impressionen, die als nicht sichtbar eingestuft wurden. Dieser Wert wird berechnet als ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Die Anzahl der Impressionen, die gemessen wurden, um gemäß der Platzierungskonfiguration sichtbar zu sein. |
| [!UICONTROL Adobe Advertising Views] | Die Anzahl der Ansichten einer Anzeige. Eine Ansicht wird gezählt, wenn der Viewer das Adobe Advertising-Video initiiert. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Die Anzahl der Aufrufe, für die mindestens 25 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Die Anzahl der Ansichten, für die mindestens 50 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Die Anzahl der Aufrufe, für die mindestens 75 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Die Anzahl der Ansichten, für die 100 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO ID Instances] | Die Häufigkeit, mit der die [!UICONTROL AMO ID] festgelegt wird. |

## Adobe Advertising-Dimensionen

>[!NOTE]
>
>Auf alle Adobe Advertising-Dimensionen in [!DNL Analytics] folgt &quot;[!DNL (AMO ID)]&quot;.

| Dimension | Anwendbare Adobe Advertising-Daten | Beschreibung |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | Advertising DSP oder der Name der Suchmaschine |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | Der Kontoname. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | RTB ([!DNL DSP]) oder der Anzeigennetzwerkname ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | Der Kampagnenname. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | Der Package- ([!DNL DSP]) oder Portfolio- ([!DNL Search, Social, & Commerce]) Name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] | Der Name der Platzierung. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] | Der Name der Anzeigengruppe. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] | Das Keyword . |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] | Der Suchtyp. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] | Das Keyword und der Übereinstimmungstyp. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | Der Anzeigentyp, z. B. `text`, `video`, `display` oder `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | Der Anzeigentyp ([!DNL DSP]) oder Anzeigentitel ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | Die Anzeigenbeschreibung ([!DNL DSP]) oder der Anzeigenhauptteil ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] | Die in der Anzeige angezeigte URL. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] | Die Ziel-URL für die Anzeige. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] | Ob es sich bei dem Einstiegsseiteneintrag um eine Durchsicht oder einen Clickthrough handelte. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] | Die Produktzielgruppe für eine Produktlistenanzeige. |

## Nützliche benutzerdefinierte berechnete Metriken für das Adobe Advertising

Erwägen Sie, die folgenden Metriken für Ihre Adobe Advertising-Daten zu erstellen.

* Klicks auf die Landingpage-Instanz ([!UICONTROL AMO ID Instances]/[!UICONTROL Adobe Advertising Clicks]): Dies ist der Prozentsatz der Personen, die auf die Anzeige geklickt und sie zur Landingpage weitergeleitet haben.
* Messbare Rate ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Sichtbare Impressionsrate ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Kosten pro Ansicht ([!UICONTROL Adobe Advertising Cost]/[!UICONTROL Adobe Advertising Views])
* Kosten pro Klick ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
