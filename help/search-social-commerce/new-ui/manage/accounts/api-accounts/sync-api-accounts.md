---
title: (Neue Benutzeroberfläche) Manuelles Synchronisieren von Werbe- und Netzwerkdaten
description: Erfahren Sie, wie Sie die Synchronisierung Ihrer Kampagnenstruktur und Kampagnenentitäten für unterstützte Anzeigennetzwerke über die neue Benutzeroberfläche manuell mit Triggern durchführen.
feature: Search Campaign Management
exl-id: 5e857713-53f0-4d90-8b7a-18a3675d320e
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%
---
# (Neue Benutzeroberfläche) Manuelles Synchronisieren von Ad-Network-Daten über API-Verbindung

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads], [!DNL LY Ads] (früher [!DNL Yahoo! Japan Ads]), [!DNL Microsoft Advertising] (früher [!DNL Bing Ads]), [!DNL Yandex] und nur vorhandene [!DNL Baidu] Konten*

Synchronisierung ist der Prozess, mit dem Search, Social und Commerce aktualisierte Informationen für die Konten der verbundenen Werbenetzwerke jedes Werbetreibenden in [unterstützten Werbenetzwerken](/help/search-social-commerce/introduction/supported-inventory.md) erfassen. Diese Daten umfassen die Kampagnenstruktur und Kampagnenentitäten des Advertisers, einschließlich der meisten seiner Attribute, die in Search, Social und Commerce verwaltet oder gemeldet werden. Es enthält keine Klickdaten und auch keine Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben und separat erfasst wurden.

Search, Social und Commerce synchronisiert (synchronisiert) automatisch einmal täglich mit Ihren Anzeigennetzwerkkonten und auch dann, wenn eine neue Kampagne in einem Ihrer Anzeigennetzwerke erkannt wird. Darüber hinaus sendet es sofort alle Änderungen an Kampagnendaten, die innerhalb von Search, Social und Commerce vorgenommen wurden, an das Werbenetzwerk.

Sie können die Synchronisierung aller aktiven und pausierten Kampagnen in bestimmten Konten manuell <!--Not available as of 2/23:  or in specific active and paused campaigns -->. Diese Aufgabe sammelt Entitäten im Anzeigennetzwerk, die neu oder geändert sind.

Für Kampagnen mit der Option &quot;[!UICONTROL Auto Update]&quot; generiert und veröffentlicht der Synchronisierungsvorgang auch Trackingcodes, die in den Tracking-Vorlagen oder Ziel-URLs fehlen oder geändert werden müssen. Die URLs werden entsprechend den Parametern in den Tracking-Einstellungen für die Kontoeinstellungen oder die Kampagne generiert. Wenn für die entsprechenden Elemente Tracking-URLs vorhanden sind, werden sie nicht neu generiert, es sei denn, neue werden benötigt (z. B. wenn der Schlüsselwortübereinstimmungstyp, der Kreativtext oder die Tracking-Parameter des Kontos geändert wurden).

>[!NOTE]
>
>Jedes Mal, [&#x200B; Sie eine Bulksheet erstellen](/help/search-social-commerce/new-ui/set-up/bulksheets/download.md) können Sie optional mit dem Werbenetzwerk synchronisieren, bevor die Bulksheet erstellt wird.

## Alle Kampagnen in Anzeigennetzwerkkonten synchronisieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Namen jedes zu synchronisierenden Kontos.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Sync]**.

Es kann eine Stunde oder länger dauern, bis der Vorgang abgeschlossen ist.

## Synchronisieren Sie Kampagnen über die [!UICONTROL Campaigns].

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Namen jeder zu synchronisierenden Kampagne.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**.

Es kann eine Stunde oder länger dauern, bis der Vorgang abgeschlossen ist.

>[!MORELIKETHIS]
>
>* [Bulksheet-Datei herunterladen/erstellen](/help/search-social-commerce/new-ui/set-up/bulksheets/download.md)
