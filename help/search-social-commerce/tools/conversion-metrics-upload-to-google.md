---
title: Hochladen von Konversionsmetriken in [!DNL Google Ads]
description: Erfahren Sie, wie Sie die von Search, Social und Commerce verfolgten Konversionsmetriken in [!DNL Google Ads].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# Hochladen von Konversionsmetriken in [!DNL Google Ads]

*Advertiser mit [!DNL Google Ads] Nur Konten*

Suchen, Social und Commerce können optional in hochgeladen werden. [!DNL Google Ads] alle Konversionsmetriken, die für [!DNL Google Ads] Kampagnen, die den Adobe Adobe Advertising-Konversions-Tracking-Dienst und die von Adobe Analytics synchronisierten Konversionsmetriken verwenden. Mit dieser Option werden die Konversionen nicht für die Hybridoptimierung verfügbar. Wenn Sie Ihre Adobe-Konversionen für die Hybridoptimierung verwenden möchten, lesen Sie den Abschnitt[Aktivieren des Hochladens von Zielen in Werbenetzwerke](objective-upload-to-networks.md).&quot;

Tägliche Uploads beinhalten die getrackten `gclid` -Wert, der Konversionswert, der mithilfe des Attributionsmodells auf Advertiser-Ebene definiert wurde, und der Zeitstempel. Wenn das Attributionsmodell aktualisiert wird, verwendet der nächste Upload das neue Modell, aber vergangene Daten werden nicht für die Verwendung des neuen Modells aktualisiert.

>[!NOTE]
>
>Die Uploads enthalten keine Konversionsmetriken, die aus Feed-Dateien in Adobe Advertising hochgeladen wurden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Upload Conversions to Google Ads]**.

1. Klicken **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Hinzufügen von Anmeldeinformationen für Ihr Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Aktivieren des Hochladens von Zielen in Werbenetzwerke](objective-upload-to-networks.md)

