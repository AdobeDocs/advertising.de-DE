---
title: Manuelles Synchronisieren von Anzeigennetzwerkdaten
description: Erfahren Sie, wie Sie die Synchronisierung Ihrer Kampagnenstruktur und Kampagnenentitäten für unterstützte Werbenetzwerke manuell durchführen können.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Manuelles Synchronisieren von Anzeigennetzwerkdaten

*[!DNL Google Ads], [!DNL Microsoft Advertising] (früher [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] und vorhandene [!DNL Baidu] Konten nur*

Bei der Synchronisierung sammeln Search, Social und Commerce aktualisierte Informationen für die vernetzten Anzeigennetzwerkkonten jedes Advertisers in [unterstützten Anzeigennetzwerken](/help/search-social-commerce/introduction/supported-inventory.md). Diese Daten umfassen die Kampagnenstruktur und Kampagnenentitäten des Advertisers, einschließlich der meisten ihrer Attribute, die in Search, Social und Commerce verwaltet oder in Berichten aufgeführt werden. Er enthält keine Klickdaten sowie Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben werden und separat gesammelt werden.

Search, Social und Commerce synchronisieren (synchronisieren) automatisch mit Ihren Anzeigennetzwerkkonten einmal täglich und immer dann, wenn eine neue Kampagne in einem Ihrer Werbenetzwerke erkannt wird. Darüber hinaus werden alle in Search, Social und Commerce vorgenommenen Änderungen an Kampagnendaten sofort an das Werbenetzwerk gesendet.

Sie können die Synchronisierung aller aktiven und ausgesetzten Kampagnen in bestimmten Konten oder in bestimmten aktiven und ausgesetzten Kampagnen manuell anfordern. Diese Aufgabe erfasst Entitäten im Werbenetzwerk, die neu oder geändert sind.

Bei Kampagnen mit der Option &quot;[!UICONTROL Auto Upload]&quot; generiert und sendet der Synchronisierungsvorgang auch Trackingcodes, die fehlen oder in den Tracking-Vorlagen oder Ziel-URLs geändert werden müssen. Die URLs werden entsprechend den Parametern in den Tracking-Einstellungen für die Kontoeinstellungen oder die Kampagne generiert. Wenn Tracking-URLs für die relevanten Elemente vorhanden sind, werden sie nur dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Keyword-Übereinstimmungstyp, der kreative Text oder die Tracking-Parameter des Kontos geändert haben).

>[!NOTE]
>
>Jedes Mal, wenn Sie [ein Bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) erstellen, können Sie optional mit dem Werbenetzwerk synchronisieren, bevor das Bulksheet erstellt wird.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]>[!UICONTROL Campaigns]**. Wählen Sie im Untermenü entweder **[!UICONTROL Accounts]** zur Synchronisierung aller Kampagnen in bestimmten Konten oder **[!UICONTROL Campaigns]** zur Synchronisierung bestimmter Kampagnen aus.

1. (Optional) Filtern Sie die Liste, um bestimmte Konten oder Kampagnen einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben jedem Konto oder jeder Kampagne, das/die Sie synchronisieren möchten. Sie können bis zu 50 Kampagnen gleichzeitig synchronisieren. Wenn Sie mehr als fünf Konten gleichzeitig synchronisieren, wird der Auftrag in Batches mit jeweils bis zu fünf Konten aufgeteilt.

1. Klicken Sie in der Symbolleiste auf **![Mehr](/help/search-social-commerce/assets/more.png "Mehr")** und wählen Sie dann **[!UICONTROL Sync]** aus.

Sie können den Status des Synchronisierungsauftrags in der Ansicht [!UICONTROL Workspace] verfolgen. Die Arbeit kann dauern
eine Stunde oder mehr, die angezeigt werden sollen.

>[!MORELIKETHIS]
>
>* [Herunterladen/Erstellen einer Bulksheet-Datei](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
