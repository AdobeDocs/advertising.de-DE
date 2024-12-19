---
title: Klick-Tracking-Formate für [!DNL Yandex]
description: Erfahren Sie mehr über die Klick-Tracking-Formate für  [!DNL Yandex] .
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yandex]

Das folgende Basis-Ziel-URL-Format gilt für gesponserte Anzeigen:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Werbetreibenden auf Adobe Advertising.
>
>* Dieses Format gibt an, dass die Token-Übergabe für die Kampagne aktiviert ist (Standard). Wenn die Token-Übergabe deaktiviert ist, ersetzen Sie `cq?` nach der `<advertiser_ID>` durch `c?`.
>
>* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden.
>
>* `source_type` ist der Übereinstimmungstyp.
>
>* `source` ist, ob die Anzeige auf einer Suche oder einer inhaltsbasierten Website angezeigt wurde.
>
>* `position` ist die Positionsnummer für die Anzeige im Block. Für Nicht-Such-Traffic ist der Wert „0“.
>
>* `position_type` ist der Block, in dem die Anzeige auf [!DNL Yandex] angezeigt wurde. Mögliche Werte: „premium“ (oberster Block), „other“ (rechter Block) oder „none“ (Nicht-Such-Traffic).

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversionsverfolgungs-Service](formats-click-tracking-about.md)
>* [AMO ID-Formate](/help/integrations/analytics/ids.md#amo-id-formats)
