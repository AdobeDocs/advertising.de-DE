---
title: Anzeigen der Tracking-Pixel für ein Segment
description: Erfahren Sie, wie Sie die Tracking-Pixel für ein benutzerdefiniertes oder CCPA-Opt-out vom Verkauf -Segment anzeigen.
feature: DSP Segments
exl-id: 3b67ab72-d7bb-45a0-b5ba-e4b811b7d2b3
TQID: 'https://experienceleague.adobe.com/jWneyyCriQcP299jQg-6Ggue0AObOfyehJwPvemYSfY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 2b670c6e-542a-5afe-b96b-d9ce7818cd55
    internal-label: DSP Segments
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
    internal-label: Segments
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%
---
# Anzeigen der Tracking-Pixel für ein Segment

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

1. Halten Sie den Cursor über die Segmentzeile und klicken Sie auf **[!UICONTROL Get Pixel]**.

   * Das Seitenansichts-Tracking-Tag, mit dem Besucher auf Desktop- und Mobilgeräten auf einer Web-Seite verfolgt werden, trägt die Bezeichnung &quot;[!UICONTROL Desktop or mobile websites]&quot;. Ersetzen Sie bei Segmenten, die [!DNL ID5]-IDs verfolgen, `ID5_PARTNER_ID` im kopierten Tag durch die Partner-ID, die Ihrer Organisation zugewiesen [!DNL ID5], als sie eine Vereinbarung mit [!DNL ID5] unterzeichnet hat. Wenn Sie Ihre Partner-ID nicht kennen, wenden Sie sich an Ihr Adobe Account Team.

     Fügen Sie das Tag den Seiten hinzu, deren Ansichten Sie verfolgen möchten.

   * (Nur benutzerdefinierte Segmente) Das Impression-Tracking-Tag, mit dem Benutzende verfolgt werden, die einer Werbeeinheit auf Desktop-, Mobil- oder CTV-Geräten ausgesetzt sind, erhält die Bezeichnung &quot;[!UICONTROL Desktop or mobile ads]&quot;. Fügen Sie das Tag zu den Anzeigen hinzu, deren Ansichten Sie verfolgen möchten. Optional können Sie das Tag zu einer Platzierung hinzufügen, um es standardmäßig allen mit der Platzierung verbundenen Anzeigen zuzuordnen.

Sobald ein Tracking-Tag implementiert ist, können Sie das Segment in den Zielgruppen-Zielen oder -Ausschlüssen für jede Platzierung verwenden.

>[!MORELIKETHIS]
>
>* [Über die Zielgruppenverwaltung](audience-about.md)
>* [Benutzerdefiniertes Segment erstellen](custom-segment-create.md)
>* [Segmentinformationen bearbeiten](segment-edit.md)
>* [Segment löschen](segment-delete.md)
>* [Freigeben oder Beenden der Segmentfreigabe](segment-share.md)
