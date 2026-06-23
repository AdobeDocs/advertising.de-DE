---
title: Manuelles Synchronisieren von Werbenetzwerkdaten
description: Erfahren Sie, wie Sie die Synchronisierung Ihrer Kampagnenstruktur und Kampagnenentitäten für unterstützte Anzeigennetzwerke manuell mit Triggern durchführen.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/3X49sKMCu3P0X1CUUEpkmTXv4fdoeKk0sBAty5MBd8Y
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3111796b54e2e633ca734c7141efbc2d82f3087d
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 0%

---

# Manuelles Synchronisieren von Werbenetzwerkdaten

*[!DNL Google Ads], [!DNL LY Ads] (früher [!DNL Yahoo! Japan Ads]), [!DNL Microsoft Advertising] (früher [!DNL Bing Ads]), [!DNL Yandex] und nur vorhandene [!DNL Baidu] Konten*

Synchronisierung ist der Prozess, mit dem Search, Social und Commerce aktualisierte Informationen für die Konten der verbundenen Werbenetzwerke jedes Werbetreibenden in [unterstützten Werbenetzwerken](/help/search-social-commerce/introduction/supported-inventory.md) erfassen. Diese Daten umfassen die Kampagnenstruktur und Kampagnenentitäten des Advertisers, einschließlich der meisten seiner Attribute, die in Search, Social und Commerce verwaltet oder gemeldet werden. Es enthält keine Klickdaten und auch keine Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben und separat erfasst wurden.

Search, Social und Commerce synchronisiert (synchronisiert) automatisch täglich mit Ihren Anzeigennetzwerkkonten und auch dann, wenn eine neue Kampagne in einem Ihrer Anzeigennetzwerke erkannt wird. Darüber hinaus sendet es sofort alle Änderungen an Kampagnendaten, die innerhalb von Search, Social und Commerce vorgenommen wurden, an das Werbenetzwerk.

Sie können die Synchronisierung aller aktiven und pausierten Kampagnen in bestimmten Konten oder in bestimmten aktiven und pausierten Kampagnen manuell anfordern. Diese Aufgabe sammelt Entitäten im Anzeigennetzwerk, die neu oder geändert sind.

Für Kampagnen mit der Option &quot;[!UICONTROL Auto Upload]&quot; generiert und veröffentlicht der Synchronisierungsvorgang auch Trackingcodes, die in den Tracking-Vorlagen oder Ziel-URLs fehlen oder geändert werden müssen. Die URLs werden entsprechend den Parametern in den Tracking-Einstellungen für die Kontoeinstellungen oder die Kampagne generiert. Wenn für die entsprechenden Elemente Tracking-URLs vorhanden sind, werden sie nicht neu generiert, es sei denn, neue werden benötigt (z. B. wenn der Schlüsselwortübereinstimmungstyp, der Kreativtext oder die Tracking-Parameter des Kontos geändert wurden).

>[!NOTE]
>
>Jedes Mal, [ Sie eine Bulksheet erstellen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) können Sie optional mit dem Werbenetzwerk synchronisieren, bevor die Bulksheet erstellt wird.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]>[!UICONTROL Campaigns]**. Wählen Sie im Untermenü entweder **[!UICONTROL Accounts]** aus, um alle Kampagnen in bestimmten Konten zu synchronisieren, oder **[!UICONTROL Campaigns]**, um bestimmte Kampagnen zu synchronisieren.

1. (Optional) Filtern Sie die Liste, um bestimmte Konten oder Kampagnen einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben jedem Konto oder jeder Kampagne, das bzw. die Sie synchronisieren möchten. Sie können bis zu 50 Kampagnen gleichzeitig synchronisieren. Wenn Sie mehr als fünf Konten gleichzeitig synchronisieren, wird der Vorgang in Batches von jeweils bis zu fünf Konten unterteilt.

1. Klicken Sie auf ![**Mehr**](/help/search-social-commerce/assets/more.png " Mehr") in der Symbolleiste und wählen Sie dann **[!UICONTROL Sync]** aus.

In der [!UICONTROL Workspace] können Sie den Status des Synchronisierungsauftrags verfolgen. Der Vorgang kann dauern
Eine Stunde oder mehr, um angezeigt zu werden.

>[!MORELIKETHIS]
>
>* [Bulksheet-Datei herunterladen/erstellen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
