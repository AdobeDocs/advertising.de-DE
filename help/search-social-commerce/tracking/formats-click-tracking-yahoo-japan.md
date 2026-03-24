---
title: Klick-Tracking-Formate für [!DNL Yahoo! Japan Ads]
description: Erfahren Sie mehr über die Klick-Tracking-Formate für  [!DNL Yahoo! Japan Ads] .
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yahoo! Japan Ads]

Für gesponserte Anzeigen gelten die folgenden grundlegenden Tracking-Vorlagenformate:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

Oder wenn die Option für das automatische Tagging für das Konto in [!DNL Yahoo! Japan Ads] festgelegt ist:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

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
