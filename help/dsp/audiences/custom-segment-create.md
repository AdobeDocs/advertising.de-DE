---
title: Erstellen und Implementieren eines benutzerdefinierten Segments
description: Erfahren Sie, wie Sie ein benutzerdefiniertes Segment erstellen und implementieren, um Benutzer zu verfolgen, die Anzeigen oder Benutzern ausgesetzt sind, die Ihre Web-Seiten besuchen.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: dda4ff8e7538bc742caa50862575cb4e46a1371d
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Erstellen und Implementieren eines benutzerdefinierten Segments

Sie können Ihre eigenen First-Party-Zielgruppendaten erfassen, indem Sie ein benutzerdefiniertes DSP-Segment erstellen und implementieren. Sie können das Segment verwenden, um a) Benutzende zu verfolgen, die Anzeigen von Desktop- und Mobilgeräten ausgesetzt sind, und b) Benutzende, die bestimmte Web-Seiten besuchen. Sie können später Benutzende im Segment erneut mit zusätzlichen Anzeigen ansprechen oder verhindern, dass Benutzende im Segment zusätzliche Anzeigen erhalten.

>[!NOTE]
>
>Um Benutzer-IDs aus Verbraucher-Opt-out-Kaufanfragen auf Ihrer Website zu verfolgen, erstellen Sie gemäß dem California Consumer Privacy Act (CCPA) ein [CCPA-Opt-out-Kaufsegment](ccpa-opt-out-segment-create.md).

## Voraussetzungen für Segmente zum Tracking von ID5-IDs

*Beta-Funktion*

* Bevor Sie ein Segment zum Tracking von Benutzern generieren, die mit ID5-IDs verknüpft sind, unterzeichnen Sie eine Vereinbarung mit [!DNL ID5] und erhalten Sie die Partner-ID Ihres Unternehmens. Wenden Sie sich an Ihr Adobe-Account-Team.

* Für Messungen in Adobe Analytics ist Folgendes erforderlich:

   1. Schließen Sie alle [Voraussetzungen für die Implementierung von  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) ab und stellen Sie sicher, dass die [AMO-ID und EF](/help/integrations/analytics/ids.md)ID in Ihren Tracking-URLs angegeben sind.

   1. Fügen Sie den folgenden Parameter Ihren Web-Seiten vor oder innerhalb des [JavaScript-Codes hinzu, der für erforderlich ist [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) - an einer beliebigen Stelle, bevor der letzte Ereignisdienst initialisiert wird.

      ```window.id5PartnerId=ID5_PartnerID;```

      Beispiel:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

      Siehe &quot;[Format von JavaScript-Konversionsverfolgungstags Version &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)&quot; und &quot;[Format von JavaScript-Konversionsverfolgungstags Version &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)&quot; für das vollständige Tag-Format.

   1. Verwenden Sie ein beliebiges Browser-Debugging-Tool, um zu überprüfen, ob jeder Aufruf an die Domain-`lasteventf-tm.everesttech.net` initiiert wird und den Parameter `_les_id5` mit einer verschlüsselten ID5-ID als Wert enthält.

## Erstellen und Implementieren eines benutzerdefinierten Segments

1. Erstellen Sie das Segment:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

   1. Eindeutige **[!UICONTROL Segment Name]** eingeben.

   1. Wählen Sie für die **[!UICONTROL Segment Type]** *[!UICONTROL Custom]* aus.

   1. Geben Sie die **[!UICONTROL Lookback Window]** ein, d. h. die Anzahl der Tage, die das Cookie eines Benutzers im Segment verbleibt.

      Das Standardfenster beträgt 45 Tage. Geben Sie einen Wert zwischen 1 und 365 ein.

   1. Klicken Sie auf **[!UICONTROL Advanced]** , um die erweiterten Einstellungen zu erweitern, und wählen Sie dann die Typen von Benutzerkennung aus, die das Segment-Tag nachverfolgt:

      * *[!UICONTROL Cookies]:* (Standard) Das Segment-Tag verfolgt Cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* Das Segment-Tag verfolgt [!DNL ID5] IDs. Für Impressionen, die an universelle IDs gesendet werden, fallen keine Gebühren an.

        **[!UICONTROL Terms of Service]:** Die Nutzungsbedingungen für die Verwendung universeller IDs. Sie oder ein anderer Benutzer im DSP-Konto muss die Bedingungen nur einmal akzeptieren, bevor Sie universelle IDs für einen neuen ID-Typ verwenden können. Für Kunden mit verwalteten Service-Verträgen wird Ihr Adobe-Account-Team Ihre Zustimmung einholen und die Bedingungen im Namen Ihres Unternehmens akzeptieren. Um die Bedingungen zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum Ende der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

   1. Klicken Sie auf **[!UICONTROL Save]**.

1. Kopieren Sie Tags und implementieren Sie sie nach Bedarf, um das Segment zu verfolgen:

   1. Kehren Sie zu **[!UICONTROL Audiences]** > **[!UICONTROL Segments]** zurück.

   1. Halten Sie den Cursor über die Segmentzeile und klicken Sie auf **[!UICONTROL Get Pixel]**.

      * So verfolgen Sie Desktop- und Mobile-Besucher einer Web-Seite:

         1. Kopieren Sie das Tracking-Tag der Seitenansicht mit der Beschriftung &quot;[!UICONTROL Desktop or mobile websites]&quot;.

         1. (Tags für Segmente, die [!DNL ID5]-IDs verfolgen) Ersetzen Sie im kopierten Tag `ID5_PARTNER_ID` durch die Partner-ID, die Ihrer Organisation zugewiesen [!DNL ID5].

            Wenn beispielsweise Ihre ID5-Partner-ID `abcde` ist und das generierte Segment-Tag lautet

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Ersetzen Sie dann `ID5_PARTNER_ID` durch `abcde` innerhalb des -Tags, um Folgendes zu erhalten:

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Ihre Organisation hat die Partner-ID erhalten, als sie eine Vereinbarung mit [!DNL ID5] unterzeichnet hat. Wenn Sie Ihre Partner-ID nicht kennen, wenden Sie sich an Ihr Adobe-Account-Team.

            Dieser Schritt ist für Tags nicht erforderlich, um [!DNL ID5] IDs für Benutzende zu verfolgen, die einer Werbeeinheit auf Desktop- oder Mobilgeräten bereitgestellt werden.

         1. Geben Sie das Tag dem Advertiser oder dem Website-Kontakt für die Bereitstellung.

            Möglicherweise muss die IT-Abteilung oder andere Gruppe des Werbetreibenden die Tag-Bereitstellung planen oder darüber informiert werden.

      * So verfolgen Sie Benutzer, die einer Werbeeinheit auf Desktop- oder Mobilgeräten ausgesetzt sind:

         1. Kopieren Sie das Impression-Tracking-Tag mit der Bezeichnung &quot;[!UICONTROL Desktop or mobile ads]&quot;.

         1. Fügen Sie das Tag entweder der Registerkarte [!UICONTROL Pixel] für jede relevante Anzeige oder dem Abschnitt [!UICONTROL Event Pixels] der [[!UICONTROL Tracking] für jede relevante Platzierung &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Sobald ein Tracking-Tag implementiert ist, können Sie das Segment in den Zielgruppen-Zielen oder -Ausschlüssen für jede Platzierung verwenden.

>[!TIP]
>
>Die Segmentgröße im Auge behalten, während Benutzende verfolgt werden.

>[!MORELIKETHIS]
>
>* [Über die Zielgruppenverwaltung](audience-about.md)
>* [Segmentinformationen bearbeiten](segment-edit.md)
>* [Segment löschen](segment-delete.md)
>* [Tracking-Pixel für ein Segment anzeigen](segment-view-pixels.md)
>* [Freigeben oder Beenden der Segmentfreigabe](segment-share.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Erstellen einer wiederverwendbaren Zielgruppe](reusable-audience-create.md)
>* [Verfügbare Datenanbieter von Drittanbietern](third-party-data-providers.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
