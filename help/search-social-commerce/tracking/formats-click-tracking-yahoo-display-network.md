---
title: Klick-Tracking-Formate für [!DNL Yahoo DSP]
description: Erfahren Sie mehr über die Klick-Tracking-Formate für  [!DNL Yahoo DSP] .
exl-id: ee6642b3-fb84-4604-91cc-da1213835be8
feature: Search Tracking
TQID: https://experienceleague.adobe.com/sQo6hr3UHQwN9GgazCKv2ba-m4ZXf2ZrhdemCpbVYvU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yahoo DSP]

Das folgende Basis-Ziel-URL-Format gilt für gesponserte Anzeigen:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

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
