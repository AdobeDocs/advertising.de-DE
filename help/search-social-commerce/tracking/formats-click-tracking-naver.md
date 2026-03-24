---
title: Klick-Tracking-Formate für [!DNL Naver]
description: Erfahren Sie mehr über die Klick-Tracking-Formate für  [!DNL Naver] .
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Naver]

Das folgende Basis-Ziel-URL-Format gilt für gesponserte Anzeigen:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Werbetreibenden in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Token-Übergabe für die Kampagne aktiviert ist (Standard). Wenn die Token-Übergabe deaktiviert ist, ersetzen Sie `cq?` nach der `<advertiser_ID>` durch `c?`.
>
>* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden.

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Konversionsverfolgungs-Service von Adobe Advertising](formats-click-tracking-about.md)
>* [AMO ID-Formate](https://experienceleague.adobe.com/de/docs/analytics/components/dimensions/amo-id#dimension-items)
