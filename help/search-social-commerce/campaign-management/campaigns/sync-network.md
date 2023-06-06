---
title: Manuelles Synchronisieren von Anzeigennetzwerkdaten
description: Erfahren Sie, wie Sie die Synchronisierung Ihrer Kampagnenstruktur und Kampagnenentitäten für unterstützte Werbenetzwerke manuell durchführen können.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Manuelles Synchronisieren von Anzeigennetzwerkdaten

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising] (früher [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads]und [!DNL Yandex] Nur Konten*

Bei der Synchronisierung werden von Search, Social und Commerce aktualisierte Informationen zu den Anzeigennetzwerkkonten jedes Advertisers erfasst [unterstützte Werbenetzwerke](/help/search-social-commerce/introduction/supported-inventory.md). Diese Daten umfassen die Kampagnenstruktur und Kampagnenentitäten des Advertisers, einschließlich der meisten ihrer Attribute, die in Search, Social und Commerce verwaltet oder in Berichten aufgeführt werden. Er enthält keine Klickdaten sowie Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben werden und separat gesammelt werden.

Search, Social und Commerce synchronisieren einmal täglich automatisch mit Ihren Anzeigennetzwerkkonten und immer dann, wenn eine neue Kampagne in einem Ihrer Werbenetzwerke erkannt wird. Darüber hinaus werden sofort alle Änderungen an Kampagnendaten aus Search, Social und Commerce an das Werbenetzwerk gesendet.

Sie können die Synchronisierung aller aktiven und ausgesetzten Kampagnen in bestimmten Konten oder in bestimmten aktiven und ausgesetzten Kampagnen manuell anfordern. Diese Aufgabe erfasst Entitäten im Werbenetzwerk, die neu oder geändert sind.

Für Kampagnen mit dem Wert &quot;[!UICONTROL Auto Upload]&quot;, generiert und sendet der Synchronisierungsvorgang auch Trackingcodes, die fehlen oder in den Tracking-Vorlagen oder Ziel-URLs geändert werden müssen. Die URLs werden entsprechend den Parametern in den Tracking-Einstellungen für die Kontoeinstellungen oder die Kampagne generiert. Wenn Tracking-URLs für die relevanten Elemente vorhanden sind, werden sie nur dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Keyword-Übereinstimmungstyp, der kreative Text oder die Tracking-Parameter des Kontos geändert haben).

>[!NOTE]
>
>Immer [Bulksheet erstellen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)können Sie optional mit dem Anzeigennetzwerk synchronisieren, bevor das Bulksheet erstellt wird.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]>[!UICONTROL Campaigns]**. Wählen Sie im Untermenü entweder **[!UICONTROL Accounts]** Synchronisieren aller Kampagnen in bestimmten Konten oder **[!UICONTROL Campaigns]** zum Synchronisieren bestimmter Kampagnen.

1. (Optional) Filtern Sie die Liste, um bestimmte Konten oder Kampagnen einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben jedem Konto oder jeder Kampagne, das/die Sie synchronisieren möchten. Sie können bis zu 50 Kampagnen gleichzeitig synchronisieren. Wenn Sie mehr als fünf Konten gleichzeitig synchronisieren, wird der Auftrag in Batches mit jeweils bis zu fünf Konten aufgeteilt.

1. Klicken **![Mehr](/help/search-social-commerce/assets/more.png "Mehr")** in der Symbolleiste und wählen Sie **[!UICONTROL Sync]**.

Sie können den Status des Synchronisierungsauftrags im [!UICONTROL Workspace] anzeigen. Der Auftrag kann eine Stunde oder länger dauern.

>[!MORELIKETHIS]
>
>* [Bulksheet-Datei herunterladen/erstellen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)

