---
title: Klick-Tracking-Formate für [!DNL Baidu]
description: Erfahren Sie mehr über die Klick-Tracking-Formate für  [!DNL Baidu] .
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Baidu]

Das folgende Basis-Ziel-URL-Format gilt für gesponserte Anzeigen:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Werbetreibenden in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Token-Übergabe für die Kampagne aktiviert ist (Standard). Wenn die Token-Übergabe deaktiviert ist, ersetzen Sie `cq?` nach der `<advertiser_ID>` durch `c?`.
>
>* `<campaignID>` ist eine Variable für die numerische Kampagnen-ID.
>
>* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden.

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Konversionsverfolgungs-Service von Adobe Advertising](formats-click-tracking-about.md)
>* [AMO ID-Formate](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
