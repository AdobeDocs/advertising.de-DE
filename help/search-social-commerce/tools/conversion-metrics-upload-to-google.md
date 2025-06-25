---
title: Upload-Konversionsmetriken für Suche, Social und Commerce [!DNL Google Ads]
description: Erfahren Sie, wie Sie Konversionsmetriken für Suche, Social und Commerce-Tracking in hochladen [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Search-, Social- und Commerce-Tracking-Konversionsmetriken in [!DNL Google Ads] hochladen

*Nur Werbetreibende mit [!DNL Google Ads]-Konten und Adobe Advertising-Konversionsverfolgung*

[!DNL Google Ads] Search, Social und Commerce können optional alle Konversionsmetriken hochladen, die für [!DNL Google Ads] Kampagnen verfolgt werden, die den Konversionsverfolgungs-Service von Adobe Advertising verwenden. Diese Option stellt die Konvertierungen nicht für die Hybridoptimierung zur Verfügung. Wenn Sie Ihre Adobe-Konversionen für die Hybridoptimierung verwenden möchten, lesen Sie den Abschnitt [Hochladen von Zielen in Werbenetzwerke aktivieren](objective-upload-to-networks.md).

Tägliche Uploads umfassen den getrackten `gclid`, den Konversionswert, der mithilfe des Attributionsmodells auf Advertiser-Ebene definiert wurde, und den Zeitstempel. Wenn das Attributionsmodell aktualisiert wird, wird beim nächsten Upload das neue Modell verwendet, aber die früheren Daten werden nicht aktualisiert, um das neue Modell zu verwenden.

>[!NOTE]
>
>Die Uploads enthalten keine Konversionsmetriken, die aus Feed-Dateien in Adobe Advertising hochgeladen wurden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Werbetreibende, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) Geschäfte machen; optional) Wenn Sie die Zustimmung von EWR- und britischen Nutzern eingeholt haben, ihre Daten zu Werbezwecken hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Anmeldeinformationen für Ihr Manager-Konto hinzufügen](/help/search-social-commerce/admin/manager-accounts.md) unter **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Hochladen von Zielen in Werbenetzwerke aktivieren](objective-upload-to-networks.md)
