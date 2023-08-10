---
title: Klick-Tracking-Formate für [!DNL Yandex]
description: Informationen zu den Klick-Tracking-Formaten für [!DNL Yandex] Konten.
exl-id: cf1d6c4b-9bcd-4b82-919f-c14dbaff9a76
feature: Search Tracking
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yandex]

Das folgende Basis-Ziel-URL-Format gilt für gesponserte Anzeigen:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Tokenübergabe deaktiviert ist, ersetzen Sie `cq?` after `<advertiser_ID>` mit `c?`.
>
>* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden.
>
>* `source_type`  ist der Übereinstimmungstyp.
>
>* `source` ist, ob die Anzeige auf einer Such- oder inhaltsbasierten Site angezeigt wurde.
>
>* `position` ist die Positionsnummer der Anzeige im Block. Bei Traffic ohne Suchvorgänge ist der Wert &quot;0&quot;.
>
>* `position_type` ist der Block, in dem die Anzeige auf [!DNL Yandex]. Mögliche Werte: &quot;Premium&quot;(oberster Block), &quot;other&quot;(rechter Block) oder &quot;none&quot;(nicht suchbasierter Traffic).

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst](formats-click-tracking-about.md)
>* [Formate für den AMO-ID-Trackingcode](skwcid-tracking-parameter.md)
