---
title: Aktivieren Sie das Hochladen von Zielen in Anzeige Netzwerke
description: Erfahren Sie, wie Sie Ziele für Ihre hybriden Portfolios an und [!DNL Microsoft Advertising] Upload [!DNL Google Ads] .
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Aktivieren Sie das Hochladen von Zielen in Anzeige Netzwerke

*Werbetreibende mit [!DNL Google Ads] und [!DNL Microsoft Advertising] nur Konten*

*Nur für die Hybridoptimierung aktivierte Advertiser*

Search, Social &amp; Commerce können die Ziele für die Portfolios eines Advertiser Konto Upload, sodass [!DNL Google Ads] [!DNL Microsoft Advertising] Sie sie für die hybride Optimierung verwenden können. Ihre hochgeladenen Ziele sind als Konversion Aktionen für benutzerdefinierte Konversion-Ziele auf Konto und Kampagne-Ebene verfügbar.

Wenn Sie diese Option aktivieren, wird automatisch eine Upload für Ziele in Portfolios ausgelöst, die Kampagnen mit intelligenten Gebotsstrategien enthalten. Search, Social, &amp; Commerce erstellt auf der Anzeigennetzwerk für jedes zutreffende Ziel eine Konversion. Die Konversion stellt alle gewichteten Konversion Metriken in der Zielsetzung dar. Jede Konversion hat einen der folgenden Namen:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  Dabei `<network_ID>` handelt es sich um die numerisch-ID, die Search, Social &amp; Commerce für die Anzeigennetzwerk verwendet, `<objective_id>` um die numerisch objektive ID und `<network_account_ID>` um die numerisch-ID für den Anzeigennetzwerk Konto oder Manager Konto.

* (Altes Format, das in Zukunft nicht mehr unterstützt wird) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  , wobei `<portfolio_id>` die numerisch Portfolio-ID und `<se_acctid/conversion_manager_se_acctid>` die numerisch-ID für den Anzeigennetzwerk Konto- oder Manager-Konto ist.

  Ihr Adobe Systems Account-Team wird mit Ihnen zusammenarbeiten, um Ihre vorhandenen Konversion Aktionsnamen innerhalb der Anzeigennetzwerk zu migrieren, bevor das alte Format veraltet ist. Während des Migrationszeitraums werden Uploads im alten und im neuen Format parallel ausgeführt. Modellierung und Optimierung sind nicht betroffen, da die neuen Konversion-Aktionen zunächst mit dem Status &quot;sekundär&quot; (nicht optimiert) und mit Daten von Aufstockung für 90 Tage angezeigt werden.

Uploads müssen [!DNL Google Ads] täglich um 06:00 Uhr in der Zeitzone des Advertiser erfolgen. Uploads erfolgen [!DNL Microsoft Advertising] täglich um 09:00 Uhr in der Zeitzone der Advertiser.

>[!IMPORTANT]
>
>Abschlüsse, die von Google Ads und dem Microsoft Advertising Universal Ereignis Tracking (UET)-Tag nachverfolgt werden, werden nicht erneut in die Anzeige Netzwerke hochgeladen. Wenn du sie in eine Vorgabe einbindest, füge sie den Kampagne Zielen im Bearbeiter der Anzeigennetzwerk hinzu.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Enable Objective Upload]**.

1. (Werbetreibende mit [!DNL Google Ads] Konten, die im Europäischen Wirtschaftsraum (EEA) oder im Vereinigten Königreich (UK) geschäftlich tätig sind; optional) Wenn Sie die Einwilligung von Nutzern aus EEA und dem Vereinigten Königreich zur Upload ihrer Daten für Werbezwecke eingeholt haben, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Managerebene Konto nachverfolgt werden) [hinzufügen Anmeldeinformationen für Ihren Vorgesetzten Konto](/help/search-social-commerce/admin/manager-accounts.md) Sie unter **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Stellen Sie sicher, dass jedes Ziel (benannt) `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` innerhalb von zwei Tagen auf der Anzeigennetzwerk angezeigt wird.

   [!DNL Google Ads] Suchen Sie im Bearbeiter nach Ihren [Konversion Aktionen](https://support.google.com/google-ads/answer/11461796). [!DNL Microsoft Advertising] Suchen Sie im Bearbeiter nach Ihren [Konversion Zielen](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Aktualisieren Sie gegebenenfalls die Datumsbereich, sodass sie das Upload Datum enthält.

## Fehlerbehebung fehlender Ziele

Wenn das Ziel – benannt `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` – für eines Ihrer Portfolios nicht in der Anzeigennetzwerk angezeigt wird, überprüfen Sie Folgendes:

* ([!DNL Google Ads]) Prüfen Sie, ob die Konvertierungen auf die Konto- oder Managerebene hochgeladen werden sollen. Falls sie auf Manager-Ebene hochgeladen werden sollen:

   * Überprüfen Sie, ob die Anmeldeinformationen für den [!DNL Google Ads] Manager-Konto unter **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** bereitgestellt wurden. Fügen Sie, falls erforderlich, [die Anmeldeinformationen für die Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) hinzu.

   * Überprüfen Sie, ob die Anzeigennetzwerk Konto bereits denselben Kennzahl Namen enthält. Ist dies der Fall, benennen Sie die Kennzahl um, damit die richtigen Eigenschaft auf Managerebene erstellt werden können.

* Vergewissern Sie sich, dass die Option &quot;Hybrid&quot; des Portfolio ausgewählt ist und dass das Ziel gültige Umsatz hat.

>[!MORELIKETHIS]
>
>* [Verwaltung der Konversion Metriken eines Advertiser](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Hochladen Konversion Metriken in [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
