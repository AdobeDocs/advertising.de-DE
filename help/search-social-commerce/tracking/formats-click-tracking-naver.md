---
title: Klick-Tracking-Formate für [!DNL Naver]
description: Informationen zu den Klick-Tracking-Formaten für [!DNL Naver] Konten.
exl-id: ff243eb5-d768-4e5c-b5b3-015fe22c9d5a
feature: Search Tracking
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Naver]

Das folgende Basis-Ziel-URL-Format gilt für gesponserte Anzeigen:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Tokenübergabe deaktiviert ist, ersetzen Sie `cq?` after `<advertiser_ID>` mit `c?`.
>
* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden.

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst](formats-click-tracking-about.md)
>* [AMO-ID-Formate](/help/integrations/analytics/ids.md#amo-id-formats)
