---
title: Erstellen und Implementieren eines benutzerdefinierten Segments
description: Erfahren Sie, wie Sie ein benutzerdefiniertes Segment erstellen und implementieren, um Benutzer zu verfolgen, die Anzeigen oder Benutzern ausgesetzt sind, die Ihre Webseiten besuchen.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 3774da55139fd9f70162c931dd7708e8e258ad83
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Erstellen und Implementieren eines benutzerdefinierten Segments

Sie können Ihre eigenen Erstanbieter-Zielgruppendaten erfassen, indem Sie ein benutzerdefiniertes DSP erstellen und implementieren. Sie können das Segment verwenden, um a) Benutzer zu verfolgen, die Anzeigen von Desktop- und Mobilgeräten erhalten, und b) Benutzer, die bestimmte Webseiten besuchen. Sie können später Benutzer im Segment mit zusätzlichen Anzeigen erneut ansprechen oder verhindern, dass Benutzer im Segment zusätzliche Anzeigen erhalten.

>[!NOTE]
>
>Um Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website zu verfolgen, erstellen Sie gemäß dem California Consumer Privacy Act (CCPA) ein Segment für die Opt-out-Kaufentscheidung mit dem CCPA-Wert [CCPA.](ccpa-opt-out-segment-create.md)

## Voraussetzungen für die Verfolgung von ID5-IDs durch Segmente

*Beta-Funktion*

* Bevor Sie ein Segment generieren, um Benutzer zu verfolgen, die mit ID5-IDs verknüpft sind, unterzeichnen Sie eine Vereinbarung mit [!DNL ID5] und erhalten Sie die Partner-ID Ihres Unternehmens. Wenden Sie sich für weitere Informationen an Ihr Adobe Account-Team.

* Für die Messung in Adobe Analytics müssen Sie:

   1. Füllen Sie alle [Voraussetzungen für die Implementierung von [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) aus und stellen Sie sicher, dass die [AMO-ID und die EF ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs eingetragen sind.

   1. Fügen Sie den folgenden Parameter vor oder innerhalb des für  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) erforderlichen [JavaScript-Codes zu Ihren Webseiten hinzu - und zwar an einer beliebigen Stelle, bevor der letzte Ereignisdienst initialisiert wird.

      ```window.id5PartnerId=Your_ID5_PartnerID;```

      Beispiel:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

      Siehe &quot;[Format der JavaScript-Konversions-Tracking-Tags Version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)&quot;und &quot;[Format der JavaScript-Konversions-Tracking-Tags Version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)&quot; für das vollständige Tag-Format.

   1. Verwenden Sie ein Browser-Debugging-Tool, um sicherzustellen, dass jeder Aufruf an die Domäne `lasteventf-tm.everesttech.net` initiiert wird und den Parameter `_les_id5` mit einer verschlüsselten ID5-ID als Wert enthält.

## Erstellen und Implementieren eines benutzerdefinierten Segments

1. Erstellen Sie das Segment:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

   1. Geben Sie eine eindeutige **[!UICONTROL Segment Name]** ein.

   1. Wählen Sie für den Wert **[!UICONTROL Segment Type]** *[!UICONTROL Custom]* aus.

   1. Geben Sie den Wert **[!UICONTROL Lookback Window]** ein, d. h. die Anzahl der Tage, in denen das Cookie eines Benutzers im Segment verbleibt.

      Das Standardfenster beträgt 45 Tage. Geben Sie einen Wert von 1 (1) bis 365 ein.

   1. Klicken Sie auf &quot;**[!UICONTROL Advanced]**&quot;, um die erweiterten Einstellungen zu erweitern, und wählen Sie dann die vom Segment-Tag verfolgten Typen von Benutzerkennung aus:

      * *[!UICONTROL Cookies]:* (Standard) Das Segment-Tag verfolgt Cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* Das Segment-Tag verfolgt [!DNL ID5] IDs. Für Impressionen, die an universelle IDs gesendet werden, fallen keine Gebühren an.

        **[!UICONTROL Terms of Service]:** Die Nutzungsbedingungen für die Verwendung von universellen IDs. Sie oder ein anderer Benutzer im DSP müssen die Bedingungen einmal akzeptieren, bevor Sie universelle IDs für einen neuen ID-Typ verwenden können. Für Kunden mit verwalteten Serviceverträgen erhält Ihr Adobe Account Team Ihre Einwilligung und akzeptiert die Bedingungen im Namen Ihres Unternehmens. Um die Begriffe zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum unteren Rand der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

   1. Klicken Sie auf **[!UICONTROL Save]**.

1. Kopieren Sie nach Bedarf Tags und implementieren Sie diese, um das Segment zu verfolgen:

   1. Kehren Sie zu **[!UICONTROL Audiences]** > **[!UICONTROL Segments]** zurück.

   1. Halten Sie den Cursor über die Segmentzeile und klicken Sie auf **[!UICONTROL Get Pixel]**.

      * So verfolgen Sie Desktop- und Mobilbesucher einer Webseite:

         1. Kopieren Sie das Tracking-Tag für Seitenansichten mit der Bezeichnung &quot;[!UICONTROL Desktop or mobile websites]&quot;.

         1. (Tags für Segmente, die [!DNL ID5] IDs verfolgen) Ersetzen Sie im kopierten Tag `ID5_PARTNER_ID` durch die Partner-ID, die [!DNL ID5] Ihrer Organisation zugewiesen ist.

            Wenn Ihre ID5-Partner-ID beispielsweise `abcde` lautet und das generierte Segment-Tag

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Ersetzen Sie dann `ID5_PARTNER_ID` durch `abcde` innerhalb des -Tags, um Folgendes zu erhalten:

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Ihre Organisation hat die Partner-ID erhalten, als sie eine Vereinbarung mit [!DNL ID5] unterzeichnete. Wenn Sie Ihre Partner-ID nicht kennen, wenden Sie sich an Ihr Adobe-Account-Team.

            Dieser Schritt ist nicht erforderlich, damit Tags [!DNL ID5] IDs für Benutzer verfolgen können, die einer Anzeigeneinheit auf Desktop- oder Mobilgeräten ausgesetzt sind.

         1. Stellen Sie das Tag dem Advertiser oder Website-Kontakt zur Bereitstellung bereit.

            Möglicherweise muss die IT-Abteilung des Werbetreibenden oder eine andere Gruppe die Tag-Bereitstellung planen oder darüber informiert werden.

      * So verfolgen Sie Benutzer, die einer Anzeigeneinheit auf Desktop- oder Mobilgeräten ausgesetzt sind:

         1. Kopieren Sie das Impression-Tracking-Tag mit der Bezeichnung &quot;[!UICONTROL Desktop or mobile ads]&quot;.

         1. Fügen Sie das Tag entweder der Registerkarte [!UICONTROL Pixel] für jede relevante Anzeige oder dem Abschnitt [!UICONTROL Event Pixels] der [[!UICONTROL Tracking]-Einstellungen für jede relevante Platzierung hinzu.](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking)

Sobald ein Tracking-Tag implementiert ist, können Sie das Segment in den Zielgruppen-Zielen oder Ausschlüssen für jede Platzierung verwenden.

>[!TIP]
>
>Verfolgen Sie die Segmentgröße, während Benutzer verfolgt werden.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen-Management](audience-about.md)
>* [Bearbeiten von Segmentinformationen](segment-edit.md)
>* [Löschen eines Segments](segment-delete.md)
>* [Tracking-Pixel für ein Segment anzeigen](segment-view-pixels.md)
>* [Freigeben oder Beenden der Segmentfreigabe](segment-share.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Erstellen einer wiederverwendbaren Zielgruppe](reusable-audience-create.md)
>* [Verfügbare Drittanbieter-Datenanbieter](third-party-data-providers.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
