---
title: Aktivieren des Hochladens von Zielen in Werbenetzwerke
description: Erfahren Sie, wie Sie Ziele für Ihre hybriden Portfolios in [!DNL Google Ads] und [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 39936c6834012432447d3216d8463937996b0017
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Aktivieren des Hochladens von Zielen in Werbenetzwerke

*Advertiser mit [!DNL Google Ads] und [!DNL Microsoft Advertising] Nur Konten*

*Advertiser, die nur für die Hybridoptimierung aktiviert wurden*

Search, Social und Commerce können die Ziele für die Portfolios eines Advertiser-Kontos in [!DNL Google Ads] und [!DNL Microsoft Advertising] , damit Sie sie zur Hybridoptimierung verwenden können. Ihre hochgeladenen Ziele stehen als Konversionsaktionen für benutzerdefinierte Konversionsziele auf Kontoebene und Kampagnenebene zur Verfügung.

Durch Aktivierung dieser Option wird automatisch ein Upload für Ziele in Portfolios mit Kampagnen mit Smart-Gebotsstrategien Trigger. Search, Social und Commerce erstellen für jedes anwendbare Ziel eine Konversion im Anzeigennetzwerk. Die Konversion stellt alle gewichteten Konversionsmetriken im Ziel auf EF ID-Ebene (Klick-ID) dar. Für [!DNL Google Ads] Klicks, die EF ID ist die [!DNL Google Ads] `gclid`; [!DNL Microsoft Advertising] Klicks, die EF ID ist die [!DNL Microsoft Advertising] `msclkid`. Aufgrund dieser Klick-ID können Konversionsdaten dem jeweiligen Suchbegriff und der Klickzeit zugeordnet werden.

Jede hochgeladene Konversion hat einen der folgenden Namen:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  where `<network_ID>` die numerische ID, die Search, Social und Commerce für das Anzeigennetzwerk verwenden, `<objective_id>` ist die numerische Ziel-ID und `<network_account_ID>` ist die numerische ID für das Anzeigen-Netzwerk-Konto oder Manager-Konto.

* (Altes Format, das in Zukunft nicht mehr unterstützt wird) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  where `<portfolio_id>` ist die numerische Portfolio-ID und `<se_acctid/conversion_manager_se_acctid>` ist die numerische ID für das Anzeigen-Netzwerk-Konto oder Manager-Konto.

  Ihr Adobe Account-Team wird mit Ihnen zusammenarbeiten, um Ihre bestehenden Konvertierungsaktionsnamen innerhalb des Werbenetzwerks zu migrieren, bevor das alte Format nicht mehr unterstützt wird. Während des Migrationszeitraums werden sowohl die Uploads im alten als auch im neuen Format parallel ausgeführt. Modellierung und Optimierung sind nicht betroffen, da die neuen Konversionsaktionen zunächst mit dem Status &quot;sekundär&quot;(nicht optimiert) und mit Daten zum Aufstocken von 90 Tagen angezeigt werden.

Hochladen in [!DNL Google Ads] treten täglich um 6:00 Uhr in der Zeitzone des Werbetreibenden auf. Hochladen in [!DNL Microsoft Advertising] treten täglich um 9:00 Uhr in der Zeitzone des Werbetreibenden auf.

>[!IMPORTANT]
>
>Konversionen, die von Google Ads und dem Microsoft Advertising Universal Event Tracking (UET)-Tag verfolgt werden, werden nicht erneut in die Werbenetzwerke hochgeladen. Wenn Sie sie in ein Ziel einbeziehen, müssen Sie sie den Kampagnenzielen im Editor des Werbenetzwerks hinzufügen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Enable Objective Upload]**.

1. (Werbetreibende mit [!DNL Google Ads] Konten, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) geschäftlich tätig sind (optional) Wenn Sie die Zustimmung von EWR- und britischen Benutzern eingeholt haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicks **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Hinzufügen von Anmeldeinformationen für Ihr Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Vergewissern Sie sich, dass jedes Ziel `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` - innerhalb von zwei Tagen im Werbenetzwerk angezeigt.

   Im [!DNL Google Ads] Editor, suchen Sie Ihre [Konversionsaktionen](https://support.google.com/google-ads/answer/11461796). Im [!DNL Microsoft Advertising] Editor, suchen Sie Ihre [Konversionsziele](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Aktualisieren Sie bei Bedarf den Datumsbereich, um das Upload-Datum einzuschließen.

## Berechnung des gewichteten Ziels

Das gewichtete Ziel, das an das Werbenetzwerk übergeben wird, ist die Summe aller erfassten Metrikwerte, mit Ausnahme der Konversionen, die von [!DNL Google Ads] oder [!DNL Microsoft Advertising] Universal Event Tracking (UET)-Tag.

Nehmen wir beispielsweise an, die Zielmetrik des Ziels ist &quot;Zusatz zum Warenkorb mit einer Gewichtung von 25&quot;und Ihre Hilfmetriken sind GGL_Lead und Umsatz mit einer Gewichtung von 1 und Downloads mit einer Gewichtung von 0,5.

![Beispiel eines gewichteten Ziels](/help/search-social-commerce/assets/objective-example.png "Beispiel eines gewichteten Ziels")

Angenommen, ein Keyword führte zu den folgenden Aktionen für das Portfolio:

* 10 Zusatz zum Warenkorb
* Umsatz von 500 $
* 50 Downloads
* 5 GGL_Lead

GGL_Lead ist nicht in die Berechnung/den Upload eingeschlossen, da es sich um eine von Google Ads getrackte Metrik handelt. Daher wird der gewichtete Zielwert berechnet als ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

## Fehlerbehebung bei fehlenden Zielen

Wenn das Ziel `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — für eines Ihrer Portfolios nicht im Werbenetzwerk angezeigt wird, überprüfen Sie Folgendes:

* ([!DNL Google Ads]) Überprüfen Sie, ob die Konversionen auf Konto- oder Managerebene hochgeladen werden sollen. Wenn sie auf Manager-Ebene hochgeladen werden sollen:

   * Überprüfen Sie, ob die Anmeldeinformationen für die [!DNL Google Ads] Manager-Konto bereitgestellt unter **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Falls erforderlich, [die Anmeldeinformationen für das Managerkonto hinzufügen](/help/search-social-commerce/admin/manager-accounts.md).

   * Überprüfen Sie, ob das Anzeigennetzwerkkonto bereits denselben Metriknamen enthält. Ist dies der Fall, benennen Sie die Metrik so um, dass die richtige Eigenschaft auf Manager-Ebene erstellt werden kann.

* Überprüfen Sie, ob die &quot;Hybrid&quot;-Option des Portfolios ausgewählt ist und ob das Ziel über einen gültigen Umsatz verfügt.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung der Konversionsmetriken eines Advertisers](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Hochladen von Konversionsmetriken in [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
