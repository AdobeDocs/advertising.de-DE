---
title: Aktivieren des Hochladens von Zielen in Werbenetzwerke
description: Erfahren Sie, wie Sie Ziele für Ihre hybriden Portfolios in [!DNL Google Ads] und [!DNL Microsoft® Advertising].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Aktivieren des Hochladens von Zielen in Werbenetzwerke

*Advertiser mit [!DNL Google Ads] und [!DNL Microsoft® Advertising] Nur Konten*

*Advertiser, die nur für die Hybridoptimierung aktiviert wurden*

Wenn Ihr Advertiser-Konto für die Verwendung der Hybridoptimierung konfiguriert ist, kann Adobe Advertising optional die Zielvorgaben für die Kontoportfolios in [!DNL Google Ads] und [!DNL Microsoft® Advertising] als Konversionen, damit Sie sie zur Hybridoptimierung verwenden können.

Durch Aktivierung dieser Option wird automatisch ein Upload für Portfolios mit Kampagnen mit Smart-Gebotsstrategien Trigger. Search, Social und Commerce erstellen eine Konversion im Anzeigennetzwerk für jede zutreffende Kombination aus Portfolio und Ziel. Jede Konversion hat den Namen `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, wobei `<portfolio_id>` ist die numerische Portfolio-ID und `<se_acctid/conversion_manager_se_acctid>` ist die numerische ID für das Anzeigen-Netzwerk-Konto oder Manager-Konto. Die Konversion stellt alle gewichteten Transaktionseigenschaften im Ziel dar.

Hochladen in [!DNL Google Ads] treten täglich um 6:00 Uhr in der Zeitzone des Werbetreibenden auf. Hochladen in [!DNL Microsoft® Advertising] treten täglich um 9:00 Uhr in der Zeitzone des Werbetreibenden auf.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Enable Objective Upload]**.

   Diese Option ist nur verfügbar, wenn Ihr Advertiser-Konto für die Verwendung der Hybridoptimierung konfiguriert ist. Wenden Sie sich zur Aktivierung der Hybridoptimierung an Ihr Adobe Account Team.

1. Klicken **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Hinzufügen von Anmeldeinformationen für Ihr Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung der Transaktionseigenschaften eines Advertisers](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
>* [Hochladen von Konversionsmetriken in [!DNL Google Ads]](conversion-metrics-upload-to-google.md)

