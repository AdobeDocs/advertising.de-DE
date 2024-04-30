---
title: Aktivieren des Hochladens von Zielen in Werbenetzwerke
description: Erfahren Sie, wie Sie Ziele für Ihre hybriden Portfolios in [!DNL Google Ads] und [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 1f2ffd65f9341db4492a2796bc82ed0bb42f13ed
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Aktivieren des Hochladens von Zielen in Werbenetzwerke

*Advertiser mit [!DNL Google Ads] und [!DNL Microsoft® Advertising] Nur Konten*

*Advertiser, die nur für die Hybridoptimierung aktiviert wurden*

Search, Social und Commerce können die Ziele für die Portfolios eines Advertiser-Kontos in [!DNL Google Ads] und [!DNL Microsoft® Advertising] , damit Sie sie zur Hybridoptimierung verwenden können. Ihre hochgeladenen Ziele stehen als Konversionsaktionen für benutzerdefinierte Konversionsziele auf Kontoebene und Kampagnenebene zur Verfügung.

Durch Aktivierung dieser Option wird automatisch ein Upload für Ziele in Portfolios mit Kampagnen mit Smart-Gebotsstrategien Trigger. Search, Social und Commerce erstellen für jedes anwendbare Ziel eine Konversion im Anzeigennetzwerk. Die Konversion stellt alle gewichteten Konversionsmetriken im Ziel dar. Jede Konversion hat einen der folgenden Namen:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  where `<network_ID>` die numerische ID, die Search, Social und Commerce für das Anzeigennetzwerk verwenden, `<objective_id>` ist die numerische Ziel-ID und `<network_account_ID>` ist die numerische ID für das Anzeigen-Netzwerk-Konto oder Manager-Konto.

* (Altes Format, das in Zukunft nicht mehr unterstützt wird) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  where `<portfolio_id>` ist die numerische Portfolio-ID und `<se_acctid/conversion_manager_se_acctid>` ist die numerische ID für das Anzeigen-Netzwerk-Konto oder Manager-Konto.

  Ihr Adobe Account-Team wird mit Ihnen zusammenarbeiten, um Ihre bestehenden Konvertierungsaktionsnamen innerhalb des Werbenetzwerks zu migrieren, bevor das alte Format nicht mehr unterstützt wird. Während des Migrationszeitraums werden sowohl die Uploads im alten als auch im neuen Format parallel ausgeführt. Modellierung und Optimierung sind nicht betroffen, da die neuen Konversionsaktionen zunächst mit dem Status &quot;sekundär&quot;(nicht optimiert) und mit Daten zum Aufstocken von 90 Tagen angezeigt werden.

Hochladen in [!DNL Google Ads] treten täglich um 6:00 Uhr in der Zeitzone des Werbetreibenden auf. Hochladen in [!DNL Microsoft® Advertising] treten täglich um 9:00 Uhr in der Zeitzone des Werbetreibenden auf.

>[!IMPORTANT]
>
>Konversionen, die von Google Ads und dem Microsoft Advertising Universal Event Tracking (UET)-Tag verfolgt werden, werden nicht erneut in die Werbenetzwerke hochgeladen. Wenn Sie sie in ein Ziel einbeziehen, fügen Sie sie den Kampagnenzielen im Editor des Werbenetzwerks hinzu.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Enable Objective Upload]**.

1. (Werbetreibende mit [!DNL Google Ads] Konten, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) geschäftlich tätig sind (optional) Wenn Sie die Zustimmung von EWR- und britischen Benutzern eingeholt haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicks **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Hinzufügen von Anmeldeinformationen für Ihr Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

Nach Abschluss des täglichen Uploads können Sie überprüfen, ob die Konversionsaktionen im Werbenetzwerk angezeigt werden.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung der Konversionsmetriken eines Advertisers](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Hochladen von Konversionsmetriken in [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
