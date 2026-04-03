---
title: Angeben von Platzierungen und Anzeigen für ein privates Angebot
description: Erfahren Sie, wie Sie einen privaten Deal mit zusätzlichen Platzierungen und Anzeigen verwenden.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
TQID: https://experienceleague.adobe.com/ZCFqnc6cQLEqahDoElttE7DzeZCR3IRx2lkyyb3BPMs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 278
ht-degree: 0%

---

# Angeben von Platzierungen und Anzeigen für ein privates Angebot

Bei nicht garantierten Angeboten können Sie den Abschluss als Lagerziel für neue Platzierungen in der [!UICONTROL Placements] angeben.

Bei programmgesteuert garantierten (PG) Angeboten können Sie Platzierungen mit bestimmten Anzeigen aus der [!UICONTROL Deals] erstellen.

Sie können auch [Anzeigen an Platzierungen anhängen](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) die mit PG- und nicht garantierten Angeboten verknüpft sind.

## Geben Sie einen nicht garantierten Abschluss als Lagerziel für eine Platzierung an

* [Platzierung über die [!UICONTROL Placements] erstellen](/help/dsp/campaign-management/placements/placement-create.md). Wählen Sie in den [!UICONTROL Inventory Targeting] Einstellungen den privaten Deal aus.

## Platzierungen und Anzeigen an einen PG-Deal anhängen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Klicken Sie in der Angebotszeile auf **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. Wählen Sie in den [!UICONTROL Ad & Campaign Selection] die Anzeigen aus, die für die Platzierung verwendet werden sollen:

       1. Wählen Sie den Advertiser, die Kampagne und den Anzeigentyp aus. Wählen Sie optional einen Anzeigenstatus aus, nach dem die Anzeigen gefiltert werden sollen.
       
       1. Aktivieren Sie in der Liste der verfügbaren Anzeigen das Kontrollkästchen neben jeder Anzeige, die für das Angebot verwendet werden soll.
       
       1. Klicken Sie auf **[!UICONTROL Apply]**.
   
   1. Im Bildschirm mit den Platzierungseinstellungen :

      1. Geben Sie den Platzierungsnamen ein.

      1. (Optional) Bearbeiten Sie die [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md) einschließlich des Überschreibens des Standardangebots, das automatisch mit dem CPM-Wert aus dem Angebot gefüllt wird. Ändern Sie den Datumsbereich oder fügen Sie weitere Anzeigen hinzu.

      Der Abschluss wird automatisch im Abschnitt Inventarziele ausgewählt. Alle anderen Targeting-Optionen sind nicht anwendbar.

      1. Klicken Sie auf **[!UICONTROL Create placement]**.

Die Platzierung beginnt zu laufen, nachdem der Publisher Ihre PG-Angebots-ID aktiviert hat.

>[!NOTE]
>
> Sie müssen das Angebots-Tag nicht zur Verifizierung an den Publisher senden.

>[!MORELIKETHIS]
>
>* [Über die private Bestandsaufnahme](private-inventory-about.md)
>* [Platzierungen und Anzeigen für ein privates Angebot auflisten](/help/dsp/inventory/private-deal-view-placements.md)
>* [Details zur Angebots-ID manuell erstellen](deal-id-create.md)
>* [Manuelle Deal ID-Einstellungen](deal-id-settings.md)
>* [Richten Sie einen programmgesteuerten garantierten Abschluss ein](programmatic-guaranteed-set-up.md)
