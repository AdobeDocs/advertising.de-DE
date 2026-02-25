---
title: (Neue Benutzeroberfläche) Manuelles Synchronisieren von Werbe- und Netzwerkdaten
description: Erfahren Sie, wie Sie die Synchronisierung Ihrer Kampagnenstruktur und Kampagnenentitäten für unterstützte Anzeigennetzwerke über die neue Benutzeroberfläche manuell mit Triggern durchführen.
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Manuelles Synchronisieren von Ad-Network-Daten über API-Verbindung

<!-- EDIT ALL -- FROM LEGACY UI -->

Nur *[!DNL Google Ads], [!DNL Microsoft Advertising] (früher [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] und bestehende [!DNL Baidu] Konten*

Synchronisierung ist der Prozess, mit dem Search, Social und Commerce aktualisierte Informationen für die Konten der verbundenen Werbenetzwerke jedes Werbetreibenden in [unterstützten Werbenetzwerken](/help/search-social-commerce/introduction/supported-inventory.md) erfassen. Diese Daten umfassen die Kampagnenstruktur und Kampagnenentitäten des Advertisers, einschließlich der meisten seiner Attribute, die in Search, Social und Commerce verwaltet oder gemeldet werden. Es enthält keine Klickdaten und auch keine Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben und separat erfasst wurden.

Search, Social und Commerce synchronisiert (synchronisiert) automatisch einmal täglich mit Ihren Anzeigennetzwerkkonten und auch dann, wenn eine neue Kampagne in einem Ihrer Anzeigennetzwerke erkannt wird. Darüber hinaus sendet es sofort alle Änderungen an Kampagnendaten, die innerhalb von Search, Social und Commerce vorgenommen wurden, an das Werbenetzwerk.

Sie können die Synchronisierung aller aktiven und pausierten Kampagnen in bestimmten Konten manuell <!--Not available as of 2/23:  or in specific active and paused campaigns -->. Diese Aufgabe sammelt Entitäten im Anzeigennetzwerk, die neu oder geändert sind.

Für Kampagnen mit der Option &quot;[!UICONTROL Auto Update]&quot; generiert und veröffentlicht der Synchronisierungsvorgang auch Trackingcodes, die in den Tracking-Vorlagen oder Ziel-URLs fehlen oder geändert werden müssen. Die URLs werden entsprechend den Parametern in den Tracking-Einstellungen für die Kontoeinstellungen oder die Kampagne generiert. Wenn für die entsprechenden Elemente Tracking-URLs vorhanden sind, werden sie nicht neu generiert, es sei denn, neue werden benötigt (z. B. wenn der Schlüsselwortübereinstimmungstyp, der Kreativtext oder die Tracking-Parameter des Kontos geändert wurden).

>[!NOTE]
>
>Jedes Mal, [&#x200B; Sie eine Bulksheet erstellen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) können Sie optional mit dem Werbenetzwerk synchronisieren, bevor die Bulksheet erstellt wird.

## Synchronisieren von Kampagnen in einem Anzeigennetzwerkkonto

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Kontonamen.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**.

   * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

In der [!UICONTROL Workspace] können Sie den Status des Synchronisierungsauftrags verfolgen. Der Vorgang kann dauern
Eine Stunde oder mehr, um angezeigt zu werden.

>[!MORELIKETHIS]
>
>* [Bulksheet-Datei herunterladen/erstellen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
