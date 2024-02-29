---
title: Hochladen von Konversionsmetriken in [!DNL Google Ads]
description: Erfahren Sie, wie Sie die von Search, Social und Commerce verfolgten Konversionsmetriken in [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: a004f5025ee94c6a40c24124a9cb134a4e1668ce
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Hochladen von Konversionsmetriken in [!DNL Google Ads]

*Advertiser mit [!DNL Google Ads] Nur Konten*

Suchen, Social und Commerce können optional in hochgeladen werden. [!DNL Google Ads] alle Konversionsmetriken, die für [!DNL Google Ads] Kampagnen, die den Adobe Advertising-Konversions-Tracking-Dienst verwenden. Mit dieser Option werden die Konversionen nicht für die Hybridoptimierung verfügbar. Wenn Sie Ihre Adobe-Konvertierungen für die Hybridoptimierung verwenden möchten, lesen Sie den Abschnitt &quot;[Aktivieren des Hochladens von Zielen in Werbenetzwerke](objective-upload-to-networks.md).&quot;

Tägliche Uploads beinhalten die verfolgten `gclid` -Wert, der Konversionswert, der mithilfe des Attributionsmodells auf Advertiser-Ebene definiert wurde, und der Zeitstempel. Wenn das Attributionsmodell aktualisiert wird, verwendet der nächste Upload das neue Modell, aber vergangene Daten werden nicht für die Verwendung des neuen Modells aktualisiert.

>[!NOTE]
>
>Die Uploads enthalten keine Konversionsmetriken, die aus Feed-Dateien auf Adobe Advertising hochgeladen wurden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Werbetreibende, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) tätig sind; optional) Wenn Sie die Zustimmung von EWR- und britischen Benutzern erhalten haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicks **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Hinzufügen von Anmeldeinformationen für Ihr Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Aktivieren des Hochladens von Zielen in Werbenetzwerke](objective-upload-to-networks.md)
