---
title: Erstellen und Implementieren eines benutzerdefinierten Segments
description: Erfahren Sie, wie Sie ein benutzerdefiniertes Segment erstellen und implementieren, um Benutzer zu verfolgen, die Anzeigen oder Benutzern ausgesetzt sind, die Ihre Webseiten besuchen.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 67b59f4f066d25f323620b83b5a0cb49beb3ee04
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Erstellen und Implementieren eines benutzerdefinierten Segments

Sie können Ihre eigenen Erstanbieter-Zielgruppendaten erfassen, indem Sie ein benutzerdefiniertes DSP erstellen und implementieren. Sie können das Segment verwenden, um a) Benutzer zu verfolgen, die Anzeigen von Desktop- und Mobilgeräten erhalten, und b) Benutzer, die bestimmte Webseiten besuchen. Sie können später Benutzer im Segment mit zusätzlichen Anzeigen erneut ansprechen oder verhindern, dass Benutzer im Segment zusätzliche Anzeigen erhalten.

>[!NOTE]
>
>Um Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website zu verfolgen, erstellen Sie gemäß dem California Consumer Privacy Act (CCPA) eine [CCPA-Ausschluss vom Verkaufssegment](ccpa-opt-out-segment-create.md).

1. Erstellen Sie das Segment:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

   1. Eindeutige Eingabe **[!UICONTROL Segment Name]**.

   1. Für **[!UICONTROL Segment Type]** auswählen *[!UICONTROL Custom]*.

   1. Geben Sie die **[!UICONTROL Segment Window]**: die Anzahl der Tage, in denen das Cookie eines Benutzers im Segment verbleibt.

      Das Standardfenster beträgt 45 Tage. Geben Sie einen Wert von 1 (1) bis 365 ein.

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
