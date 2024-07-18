---
title: Aktivieren des Hochladens von Zielen in Werbenetzwerke
description: Erfahren Sie, wie Sie Ziele für Ihre hybriden Portfolios in [!DNL Google Ads] und [!DNL Microsoft Advertising] hochladen.
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: f491537c2dd56716abe0ab4fa8c26b8558dca664
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# Aktivieren des Hochladens von Zielen in Werbenetzwerke

*Advertiser mit [!DNL Google Ads] - und [!DNL Microsoft Advertising] -Konten nur*

*Nur für Hybridoptimierung aktivierte Advertiser*

Search, Social und Commerce können die Ziele für die Portfolios eines Advertiser-Kontos in [!DNL Google Ads] und [!DNL Microsoft Advertising] hochladen, damit Sie sie zur Hybridoptimierung verwenden können. Ihre hochgeladenen Ziele stehen als Konversionsaktionen für benutzerdefinierte Konversionsziele auf Kontoebene und Kampagnenebene zur Verfügung.

Durch Aktivierung dieser Option wird automatisch ein Upload für Ziele in Portfolios mit Kampagnen mit Smart-Gebotsstrategien Trigger. Search, Social und Commerce erstellen für jedes anwendbare Ziel eine Konversion im Anzeigennetzwerk. Die Konversion stellt alle gewichteten Konversionsmetriken im Ziel auf EF ID-Ebene (Klick-ID) dar. Bei [!DNL Google Ads] Klicks ist die EF ID der [!DNL Google Ads] `gclid`; bei [!DNL Microsoft Advertising] Klicks ist die EF ID der [!DNL Microsoft Advertising] `msclkid`. Aufgrund dieser Klick-ID können Konversionsdaten dem jeweiligen Suchbegriff und der Klickzeit zugeordnet werden.

Jede hochgeladene Konvertierung hat den folgenden Namen:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

wobei `<network_ID>` die numerische ID ist, die von Search, Social und Commerce für das Anzeigennetzwerk verwendet wird, `<objective_id>` die numerische Ziel-ID und `<network_account_ID>` die numerische ID für das Anzeigennetzwerkkonto oder -managerkonto.

Uploads auf [!DNL Google Ads] erfolgen täglich um 06:00 Uhr in der Zeitzone des Werbetreibenden. Uploads auf [!DNL Microsoft Advertising] erfolgen täglich um 9:00 Uhr in der Zeitzone des Werbetreibenden.

>[!IMPORTANT]
>
>Konversionen, die von Google Ads und dem Microsoft Advertising Universal Event Tracking (UET)-Tag verfolgt werden, werden nicht erneut in die Werbenetzwerke hochgeladen. Wenn Sie sie in ein Ziel einbeziehen, müssen Sie sie den Kampagnenzielen im Editor des Werbenetzwerks hinzufügen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Enable Objective Upload]**.

1. (Werbetreibende mit [!DNL Google Ads] Konten, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) geschäftlich tätig sind (optional) Wenn Sie die Zustimmung von EWR- und britischen Benutzern eingeholt haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Fügen Sie Anmeldedaten für Ihr Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md) unter **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** hinzu.

1. Stellen Sie sicher, dass jedes Ziel mit dem Namen `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` innerhalb von zwei Tagen im Werbenetzwerk angezeigt wird.

   Suchen Sie im [!DNL Google Ads] -Editor Ihre [Konversionsaktionen](https://support.google.com/google-ads/answer/11461796). Suchen Sie im [!DNL Microsoft Advertising]-Editor nach Ihren [Konvertierungszielen](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Aktualisieren Sie bei Bedarf den Datumsbereich, um das Upload-Datum einzuschließen.

## Berechnung des gewichteten Ziels

Das gewichtete Ziel, das an das Werbenetzwerk übergeben wird, ist die Summe aller erfassten Metrikwerte, mit Ausnahme der Konversionen, die durch [!DNL Google Ads] oder das [!DNL Microsoft Advertising] Universal Event Tracking (UET)-Tag verfolgt werden. Der Wert wird anhand der Attributionsmethode berechnet, die für das Search-, Social- und Commerce-Konto des Advertisers eingerichtet wurde.

Nehmen wir beispielsweise an, die Zielmetrik des Ziels ist &quot;Zusatz zum Warenkorb mit einer Gewichtung von 25&quot;und Ihre Hilfmetriken sind GGL_Lead und Umsatz mit einer Gewichtung von 1 und Downloads mit einer Gewichtung von 0,5.

![Beispiel eines gewichteten Ziels](/help/search-social-commerce/assets/objective-example.png "Beispiel eines gewichteten Ziels")

Angenommen, ein Keyword führte zu den folgenden Aktionen für das Portfolio:

* 10 Zusatz zum Warenkorb
* Umsatz von 500 $
* 50 Downloads
* 5 GGL_Lead

GGL_Lead ist nicht in die Berechnung/den Upload eingeschlossen, da es sich um eine von Google Ads getrackte Metrik handelt. Daher wird der gewichtete Zielwert berechnet als ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>Sie können Daten zu Adobe Advertising gewichteten Umsätzen in den Berichten des Werbenetzwerks anzeigen. Als Best Practice wird empfohlen, den gewichteten Umsatz mit dem Wert [!DNL Google Ads] &quot;Alle&quot; zu vergleichen. (durch conv. Zeit)&quot;oder die Metrik [!DNL Microsoft Advertising] &quot;Alle Konversionsmetriken&quot;. Umsatz&quot;, segmentiert nach der Metrik O_ACS_OBJ*.<!--clarify -->

## Fehlerbehebung bei fehlenden Zielen

Wenn das Ziel mit dem Namen `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` für eines Ihrer Portfolios nicht im Werbenetzwerk angezeigt wird, überprüfen Sie Folgendes:

* ([!DNL Google Ads]) Überprüfen Sie, ob die Konversionen auf Konto- oder Managerebene hochgeladen werden sollen. Wenn sie auf Manager-Ebene hochgeladen werden sollen:

   * Überprüfen Sie, ob die Anmeldeinformationen für das Manager-Konto [!DNL Google Ads] unter **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** angegeben sind. Fügen Sie bei Bedarf [die Anmeldeinformationen für das Managerkonto hinzu](/help/search-social-commerce/admin/manager-accounts.md).

   * Überprüfen Sie, ob das Anzeigennetzwerkkonto bereits denselben Metriknamen enthält. Ist dies der Fall, benennen Sie die Metrik so um, dass die richtige Eigenschaft auf Manager-Ebene erstellt werden kann.

* Überprüfen Sie, ob die &quot;Hybrid&quot;-Option des Portfolios ausgewählt ist und ob das Ziel über einen gültigen Umsatz verfügt.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung der Konversionsmetriken eines Advertisers](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Hochladen von Konversionsmetriken in  [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
