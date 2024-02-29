---
title: Aktivieren des Hochladens von Zielen in Werbenetzwerke
description: Erfahren Sie, wie Sie Ziele für Ihre hybriden Portfolios in [!DNL Google Ads] und [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 0fb03410e67be28d24496c948b52399c8465e041
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Aktivieren des Hochladens von Zielen in Werbenetzwerke

*Advertiser mit [!DNL Google Ads] und [!DNL Microsoft® Advertising] Nur Konten*

*Advertiser, die nur für die Hybridoptimierung aktiviert wurden*

Wenn Ihr Advertiser-Konto für die Verwendung der Hybridoptimierung konfiguriert ist, kann Adobe Advertising optional die Ziele für die Kontoportfolios in [!DNL Google Ads] und [!DNL Microsoft® Advertising] als Konversionen verwenden, damit Sie sie zur Hybridoptimierung verwenden können.

Durch Aktivierung dieser Option wird automatisch ein Upload für Portfolios mit Kampagnen mit Smart-Gebotsstrategien Trigger. Search, Social und Commerce erstellen eine Konversion im Anzeigennetzwerk für jede zutreffende Kombination aus Portfolio und Ziel. Jede Konversion hat den Namen `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, wobei `<portfolio_id>` ist die numerische Portfolio-ID und `<se_acctid/conversion_manager_se_acctid>` ist die numerische ID für das Anzeigen-Netzwerk-Konto oder Manager-Konto. Die Konversion stellt alle gewichteten Konversionsmetriken im Ziel dar.

Hochladen in [!DNL Google Ads] treten täglich um 6:00 Uhr in der Zeitzone des Werbetreibenden auf. Hochladen in [!DNL Microsoft® Advertising] treten täglich um 9:00 Uhr in der Zeitzone des Werbetreibenden auf.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Enable Objective Upload]**.

   Diese Option ist nur verfügbar, wenn Ihr Advertiser-Konto für die Verwendung der Hybridoptimierung konfiguriert ist. Wenden Sie sich zur Aktivierung der Hybridoptimierung an Ihr Adobe Account-Team.

1. (Werbetreibende mit [!DNL Google Ads] Konten, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) geschäftlich tätig sind (optional) Wenn Sie die Zustimmung von EWR- und britischen Benutzern erhalten haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicks **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Hinzufügen von Anmeldeinformationen für Ihr Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung der Konversionsmetriken eines Advertisers](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Hochladen von Konversionsmetriken in [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
