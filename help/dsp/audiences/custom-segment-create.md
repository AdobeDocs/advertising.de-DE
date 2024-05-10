---
title: Erstellen und Implementieren eines benutzerdefinierten Segments
description: Erfahren Sie, wie Sie ein benutzerdefiniertes Segment erstellen und implementieren, um Benutzer zu verfolgen, die Anzeigen oder Benutzern ausgesetzt sind, die Ihre Webseiten besuchen.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Erstellen und Implementieren eines benutzerdefinierten Segments

Sie können Ihre eigenen Erstanbieter-Zielgruppendaten erfassen, indem Sie ein benutzerdefiniertes DSP erstellen und implementieren. Sie können das Segment verwenden, um a) Benutzer zu verfolgen, die Anzeigen von Desktop- und Mobilgeräten erhalten, und b) Benutzer, die bestimmte Webseiten besuchen. Sie können später Benutzer im Segment mit zusätzlichen Anzeigen erneut ansprechen oder verhindern, dass Benutzer im Segment zusätzliche Anzeigen erhalten.

>[!NOTE]
>
>Um Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website zu verfolgen, erstellen Sie gemäß dem California Consumer Privacy Act (CCPA) eine [CCPA-Ausschluss vom Verkaufssegment](ccpa-opt-out-segment-create.md).

## Voraussetzungen für die Verfolgung von ID5-IDs durch Segmente

*Beta-Funktion*

* Bevor Sie ein Segment generieren, um Benutzer zu verfolgen, die mit ID5-IDs verknüpft sind, müssen Sie eine Vereinbarung mit [!DNL ID5] und rufen Sie die Partner-ID Ihres Unternehmens ab. Wenden Sie sich für weitere Informationen an Ihr Adobe Account-Team.

* Für die Messung in Adobe Analytics müssen Sie:

   1. Alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und [AMO-ID und EF-ID in Ihren Tracking-URLs](/help/integrations/analytics/ids.md).

   1. Fügen Sie Ihren Webseiten den folgenden Parameter vor oder innerhalb der [JavaScript-Code erforderlich für [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) - an einer beliebigen Stelle, bevor der letzte Ereignisdienst initialisiert wird.

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

## Erstellen und Implementieren eines benutzerdefinierten Segments

1. Erstellen Sie das Segment:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

   1. Eindeutige Eingabe **[!UICONTROL Segment Name]**.

   1. Für **[!UICONTROL Segment Type]** auswählen *[!UICONTROL Custom]*.

   1. Geben Sie die **[!UICONTROL Lookback Window]**: die Anzahl der Tage, in denen das Cookie eines Benutzers im Segment verbleibt.

      Das Standardfenster beträgt 45 Tage. Geben Sie einen Wert von 1 (1) bis 365 ein.

   1. Klicks **[!UICONTROL Advanced]** , um die erweiterten Einstellungen zu erweitern, und wählen Sie dann die Typen von Benutzer-IDs aus, die das Segment-Tag verfolgt:

      * *[!UICONTROL Cookies]:* (Standard) Das Segment-Tag verfolgt Cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* Das Segment-Tag verfolgt [!DNL ID5] IDs. Für Impressionen, die an universelle IDs gesendet werden, fallen keine Gebühren an.

        **[!UICONTROL Terms of Service]:** Die Nutzungsbedingungen für die Verwendung von universellen IDs. Sie oder ein anderer Benutzer im DSP müssen die Bedingungen einmal akzeptieren, bevor Sie universelle IDs für einen neuen ID-Typ verwenden können. Für Kunden mit verwalteten Serviceverträgen erhält Ihr Adobe Account Team Ihre Einwilligung und akzeptiert die Bedingungen im Namen Ihres Unternehmens. Um die Begriffe zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum unteren Rand der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

   1. Klicks **[!UICONTROL Save]**.

1. Kopieren Sie nach Bedarf Tags und implementieren Sie diese, um das Segment zu verfolgen:

   1. Zurück zu **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Halten Sie den Cursor über die Segmentzeile und klicken Sie auf **[!UICONTROL Get Pixel]**.

      * So verfolgen Sie Desktop- und Mobilbesucher einer Webseite:

         1. Kopieren Sie das Tracking-Tag für Seitenansichten mit der Bezeichnung &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Stellen Sie das Tag dem Advertiser oder Website-Kontakt zur Bereitstellung bereit.

            Möglicherweise muss die IT-Abteilung des Werbetreibenden oder eine andere Gruppe die Tag-Bereitstellung planen oder darüber informiert werden.

      * So verfolgen Sie Benutzer, die einer Anzeigeneinheit auf Desktop- oder Mobilgeräten ausgesetzt sind:

         1. Kopieren Sie das Impression-Tracking-Tag mit der Bezeichnung &quot;[!UICONTROL Desktop or mobile ads].&quot;

   1. (Tags für Segmente, die [!DNL ID5] IDs für Desktop- und mobile Besucher einer Webseite) Ersetzen Sie im kopierten Tag `ID5_PARTNER_ID` mit der Partner-ID, die [!DNL ID5] Ihrer Organisation zugewiesen wurde.

   Wenn Ihre ID5-Partner-ID beispielsweise `abcde` und das generierte Segment-Tag

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   then replace `ID5_PARTNER_ID` mit `abcde` innerhalb des -Tags, um Folgendes zu erhalten:

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   Ihre Organisation hat die Partner-ID erhalten, als sie eine Vereinbarung mit [!DNL ID5]. Wenn Sie Ihre Partner-ID nicht kennen, wenden Sie sich an Ihr Adobe-Account-Team.

   Dieser Schritt ist nicht erforderlich, damit Tags verfolgt werden können. [!DNL ID5] IDs für Benutzer, die einer Anzeigeneinheit auf Desktop- oder Mobilgeräten ausgesetzt sind.

1. Fügen Sie das Tag entweder zum [!UICONTROL Pixel] für jede relevante Anzeige oder für die [!UICONTROL Event Pixels] Abschnitt [[!UICONTROL Tracking] Einstellungen für jede relevante Platzierung](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Sobald ein Tracking-Tag implementiert ist, können Sie das Segment in den Zielgruppen-Zielen oder Ausschlüssen für jede Platzierung verwenden.

>[!TIP]
>
>Verfolgen Sie die Segmentgröße, während Benutzer verfolgt werden.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen-Management](audience-about.md)
>* [Segmentinformationen bearbeiten](segment-edit.md)
>* [Segment löschen](segment-delete.md)
>* [Anzeigen von Tracking-Pixeln für ein Segment](segment-view-pixels.md)
>* [Freigeben oder Beenden der Freigabe eines Segments](segment-share.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Wiederverwendbare Zielgruppe erstellen](reusable-audience-create.md)
>* [Verfügbare Drittanbieter von Daten](third-party-data-providers.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
