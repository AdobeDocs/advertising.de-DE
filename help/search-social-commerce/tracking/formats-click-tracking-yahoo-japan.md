---
title: Klick-Tracking-Formate für [!DNL Yahoo! Japan Ads]
description: Informationen zu den Klick-Tracking-Formaten für [!DNL Yahoo! Japan Ads] Konten.
exl-id: 4584f2c4-8090-4931-bd44-0df42f350755
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yahoo! Japan Ads]

Die folgenden grundlegenden Tracking-Vorlagenformate gelten für gesponserte Anzeigen:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

oder wenn die Option für das automatische Tagging für das Konto in [!DNL Yahoo! Japan Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Tokenübergabe deaktiviert ist, ersetzen Sie `cq?` after `<advertiser_ID>` mit `c?`.
>
>* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden.

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst](formats-click-tracking-about.md)
>* [Formate für den AMO-ID-Trackingcode](amo-id-tracking-parameter.md)
