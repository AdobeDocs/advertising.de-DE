---
title: Angeben von Platzierungen und Anzeigen für ein privates Angebot
description: Erfahren Sie, wie Sie einen privaten Deal mit zusätzlichen Platzierungen und Anzeigen verwenden.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Angeben von Platzierungen und Anzeigen für ein privates Angebot

Bei nicht garantierten Angeboten können Sie den Abschluss als Lagerziel für neue Platzierungen in der [!UICONTROL Placements] angeben.

Bei programmgesteuert garantierten (PG) Angeboten können Sie Platzierungen mit bestimmten Anzeigen aus der [!UICONTROL Deals] erstellen.

Sie können auch [Anzeigen an Platzierungen anhängen](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) die mit PG- und nicht garantierten Angeboten verknüpft sind.

## Geben Sie einen nicht garantierten Abschluss als Lagerziel für eine Platzierung an

* [Platzierung über die [!UICONTROL Placements] erstellen](/help/dsp/campaign-management/placements/placement-create.md). Wählen Sie in den [!UICONTROL Inventory Targeting] Einstellungen den privaten Deal aus.

## Platzierungen und Anzeigen an einen PG-Abschluss anhängen

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
>* [Über den privaten Bestand](private-inventory-about.md)
>* [Platzierungen und Anzeigen für ein privates Angebot auflisten](/help/dsp/inventory/private-deal-view-placements.md)
>* [Details zur Angebots-ID manuell erstellen](deal-id-create.md)
>* [Manuelle Deal ID-Einstellungen](deal-id-settings.md)
>* [Richten Sie einen programmgesteuerten garantierten Abschluss ein](programmatic-guaranteed-set-up.md)
