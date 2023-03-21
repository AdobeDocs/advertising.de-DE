---
title: Adobe Advertising-Metriken in Analysis Workspace
description: Adobe Advertising-Metriken in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 5dd3772de945660e76321dac935de5ebcab5979a
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Adobe Advertising-Metriken in Analysis Workspace

*Werbetreibende mit nur einer Adobe Advertising-Adobe Analytics-Integration*

>[!NOTE]
>
>* Adobe Advertising übergibt Traffic-Metriken und -Dimensionen an [!DNL Analytics] täglich.
>* [!DNL Analytics] erfasst Adobe Advertising-Clickthroughs und Durchsichten in Echtzeit.
   > Für [!DNL Search, Social, & Commerce]festgelegt ist, wird diese Funktion für die meisten Anzeigennetzwerke und Kampagnentypen unterstützt. Siehe &quot;Unterstütztes Inventar&quot;im [!DNL Search, Social, & Commerce] Handbuch für weitere Informationen.<!-- add link when that's published in ExL -->


## Traffic-Metriken aus Adobe Advertising

>[!NOTE]
>
>Alle Adobe Advertising-Traffic-Metriken in [!DNL Analytics] Beginnen Sie mit &quot;AMO&quot;.

| Traffic-Metrik | Beschreibung |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Die Anzahl der Adobe Advertising-Impressionen. |
| [!UICONTROL AMO Clicks] | Die Anzahl der Adobe-Werbe-Klicks insgesamt. |
| [!UICONTROL AMO Cost] | Die Werbeausgaben für Adoben in der Währung der Report Suite. |
| [!UICONTROL AMO ID Instance] | Die Häufigkeit, mit der die Adobe Advertising ID festgelegt wurde. |
| [!UICONTROL AMO Minutes Viewed] | Die Anzahl der Minuten, in denen ein Adobe Advertising-Video angesehen wurde. |
| [!UICONTROL AMO Views] | Die Anzahl der Ansichten auf einer Anzeige. Eine Ansicht wird gezählt, wenn der Viewer das Adobe Advertising-Video startet. |
| [!UICONTROL AMO Views 25% Complete] | Die Anzahl der Ansichten, bei denen mindestens 25 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO Views 50% Complete] | Die Anzahl der Ansichten, bei denen mindestens 50 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO Views 75% Complete] | Die Anzahl der Ansichten, bei denen mindestens 75 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO Views 100% Complete] | Die Anzahl der Ansichten, bei denen 100 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO Viewable Impressions] | Die Anzahl der Impressionen, die gemäß der Platzierungskonfiguration als sichtbar gemessen wurden. |
| [!UICONTROL AMO Not Viewable Impressions] | Die Anzahl der Impressionen, die als nicht sichtbar identifiziert wurden. Dieser Wert wird als ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable]). |
| [!UICONTROL AMO Measurable Impressions] | Die Anzahl der Impressionen, für die die Sichtbarkeitsinstrumentierung erfolgreich initialisiert wurde. Dieser Wert wird berechnet als (instrumentierte Impressionen - die Anzahl nicht messbarer Impressionen). |

## Adobe Advertising-Dimensionen

>[!NOTE]
>
>Alle Adobe Advertising-Dimensionen in [!DNL Analytics] gefolgt von &quot;(AMO-ID).&quot;

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
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Der Übereinstimmungstyp für die Suche. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Keyword und Übereinstimmungstyp. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Der Anzeigentyp, z. B. `text`, `video`, `display`oder `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Der Anzeigentyp ([!DNL DSP]) oder Anzeigentitel ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Die Anzeigenbeschreibung ([!DNL DSP]) oder Anzeigenkörper ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | Die in der Anzeige angezeigte URL. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | Die Ziel-URL für die Anzeige. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] und [!DNL Search, Social, & Commerce] data | Ob der Einstieg in die Landingpage eine Durchsicht oder ein Clickthrough war. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | Das Produktziel für eine Produktlistenanzeige. |

## Nützliche benutzerspezifische berechnete Metriken für Adobe Advertising

Erwägen Sie die Erstellung der folgenden Metriken für Ihre Adobe Advertising-Daten.

* Klicks zur Landingpage-Instanz ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Dies ist der Prozentsatz der Personen, die auf die Anzeige geklickt und sie zur Landingpage weitergeleitet haben.
* Messrate ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Sichtbare Impressionsrate ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Kosten pro Ansicht ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Kosten pro Klick ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)

