---
title: Hochladen von Konversionsmetriken in  [!DNL Google Ads]
description: Erfahren Sie, wie Sie Konversionsmetriken mit Such-, Social- und Commerce-Verfolgung in  [!DNL Google Ads] hochladen.
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: e8eabf7e4aa7c9201cd8198aae32d325b2858f2b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Hochladen von Konversionsmetriken in [!DNL Google Ads]

*Advertiser mit [!DNL Google Ads] Konten nur*

Search, Social und Commerce können optional alle von ihr verfolgten Konversionsmetriken für [!DNL Google Ads] Kampagnen, die den Adobe Advertising-Konversions-Tracking-Dienst verwenden, in [!DNL Google Ads] hochladen. Mit dieser Option werden die Konversionen nicht für die Hybridoptimierung verfügbar. Wenn Sie Ihre Adobe-Konversionen für die Hybridoptimierung verwenden möchten, finden Sie weitere Informationen unter &quot;[Aktivieren des Hochladens von Zielgruppen in Werbenetzwerke](objective-upload-to-networks.md)&quot;.

Tägliche Uploads umfassen den verfolgten `gclid` -Wert, den mithilfe des Attributionsmodells auf Advertiser-Ebene definierten Konversionswert und den Zeitstempel. Wenn das Attributionsmodell aktualisiert wird, verwendet der nächste Upload das neue Modell, aber vergangene Daten werden nicht für die Verwendung des neuen Modells aktualisiert.

>[!NOTE]
>
>Die Uploads enthalten keine Konversionsmetriken, die aus Feed-Dateien auf Adobe Advertising hochgeladen wurden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Werbetreibende, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) tätig sind; optional) Wenn Sie die Zustimmung von EWR- und britischen Benutzern eingeholt haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Fügen Sie Anmeldedaten für Ihr Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) unter **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** hinzu.

>[!MORELIKETHIS]
>
>* [Aktivieren des Hochladens von Zielen in Anzeigennetzwerke](objective-upload-to-networks.md)
