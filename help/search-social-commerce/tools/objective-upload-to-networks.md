---
title: Hochladen von Zielen in Werbenetzwerke aktivieren
description: Erfahren Sie, wie Sie Ziele für Ihre hybriden Portfolios in  [!DNL Google Ads] / [!DNL Microsoft Advertising] hochladen.
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 464fd13de476f2710536bea6540e0b9be4684395
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Hochladen von Zielen in Werbenetzwerke aktivieren

*Werbetreibende nur mit [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten*

*Werbetreibende nur für die Hybridoptimierung aktiviert*

Search, Social und Commerce können die Ziele für die Portfolios eines Advertiser-Kontos in [!DNL Google Ads] und [!DNL Microsoft Advertising] hochladen, damit Sie sie für die Hybridoptimierung verwenden können. Die hochgeladenen Ziele sind als Konversionsaktionen für benutzerdefinierte Konversionsziele auf Konto- und Kampagnenebene verfügbar.

Durch Aktivierung dieser Option wird automatisch ein Upload von Zielen in Portfolios mit Kampagnen mit intelligenten Angebotsstrategien Trigger. Search, Social und Commerce erstellen für jedes anwendbare Ziel eine Konversion im Anzeigennetzwerk. Die Konversion stellt alle gewichteten Konversionsmetriken im -Ziel auf EF-ID-(Klick-ID-)Ebene dar. Bei [!DNL Google Ads] Klicks ist die EF ID der [!DNL Google Ads] `gclid`; bei [!DNL Microsoft Advertising] Klicks ist die EF ID der [!DNL Microsoft Advertising] der `msclkid`. Aufgrund dieser Klick-ID können Konversionsdaten dem jeweiligen Keyword und der Klickzeit zugeordnet werden.

Jede hochgeladene Konversion hat den folgenden Namen:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

Dabei ist `<network_ID>` die numerische ID, die Search, Social und Commerce für das Werbenetzwerk verwendet, `<objective_id>` die numerische Ziel-ID und `<network_account_ID>` die numerische ID für das Werbenetzwerkkonto oder das Managerkonto.

Uploads auf [!DNL Google Ads] und [!DNL Microsoft Advertising] erfolgen über den ganzen Tag, manchmal sogar stündlich. Bei Werbetreibenden mit großen Konten oder benutzerdefinierten Konfigurationen werden Uploads mindestens dreimal täglich durchgeführt.

>[!IMPORTANT]
>
>Konversionen, die von Google Ads und vom UET-Tag (Universal Event Tracking) von Microsoft Advertising verfolgt werden, werden nicht erneut in die Werbenetzwerke hochgeladen. Wenn Sie sie in ein Ziel einbeziehen, müssen Sie sie im Editor des Anzeigennetzwerks zu den Kampagnenzielen hinzufügen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Enable Objective Upload]**.

1. (Werbetreibende mit [!DNL Google Ads], die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) Geschäfte tätigen; optional) Wenn Sie die Zustimmung von EWR- und britischen Nutzern eingeholt haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Wenn Ihre Konversionen auf Manager-Kontoebene verfolgt werden) [Anmeldeinformationen für Ihr Manager-Konto hinzufügen](/help/search-social-commerce/admin/manager-accounts.md) unter **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Stellen Sie sicher, dass jedes Ziel — namens `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — innerhalb von zwei Tagen im Werbenetzwerk angezeigt wird.

   Suchen Sie im [!DNL Google Ads]-Editor nach Ihren [Konversionsaktionen](https://support.google.com/google-ads/answer/11461796). Suchen Sie im [!DNL Microsoft Advertising]-Editor nach Ihren [Konversionszielen](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Aktualisieren Sie bei Bedarf den Datumsbereich, um das Upload-Datum einzuschließen.

## Berechnen des gewichteten Ziels

Das gewichtete Ziel, das an das Werbenetzwerk übergeben wird, ist die Summe aller erfassten Metrikwerte, mit Ausnahme der Konversionen, die von [!DNL Google Ads] oder vom [!DNL Microsoft Advertising] UET-Tag (Universal Event Tracking) verfolgt werden. Der Wert wird mithilfe der Attributionsmethode berechnet, die für das Konto „Suche“, „Social“ und &quot;Commerce&quot; des Werbetreibenden eingerichtet wurde.

Angenommen, die Zielmetrik des Ziels lautet beispielsweise „Warenkorbhinzufügungen“ mit einer Gewichtung von 25. Ihre Hilfsmetriken umfassen „GGL_Lead“ und „Umsatz“ mit einer Gewichtung von 1 und „Downloads“ mit einer Gewichtung von 0,5.

![Beispiel eines gewichteten Ziels](/help/search-social-commerce/assets/objective-example.png "Beispiel eines gewichteten Ziels")

Angenommen, ein Keyword führt zu den folgenden Aktionen für das Portfolio:

* 10 Zusatz zum Warenkorb
* 500 USD Umsatz
* 50 Downloads
* 5 GGL_Lead

GGL_Lead ist nicht in der Berechnung/dem Upload enthalten, da es sich um eine von Google Ads verfolgte Metrik handelt. Daher wird der gewichtete Zielwert berechnet als ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>Sie können Daten zum gewichteten Umsatz von Adobe Advertising in den Berichten des Werbenetzwerks anzeigen. Vergleichen Sie als Best Practice den gewichteten Umsatz mit dem [!DNL Google Ads] „Alle Konversionen“. (durch Konv. die Metrik „time“ oder die [!DNL Microsoft Advertising] Metrik „All conv. Umsatz,“ segmentiert in die Metrik O_ACS_OBJ*.<!--clarify -->

## Fehlerbehebung bei fehlenden Zielen

Wenn das Ziel - namens `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` - für eines Ihrer Portfolios nicht im Werbenetzwerk angezeigt wird, überprüfen Sie Folgendes:

* ([!DNL Google Ads]) Überprüfen Sie, ob die Konversionen auf Konto- oder Managerebene hochgeladen werden sollen. Wenn sie auf Managerebene hochgeladen werden sollen:

   * Überprüfen Sie, ob die Anmeldeinformationen für das [!DNL Google Ads] Manager-Konto unter **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** angegeben sind. Fügen Sie bei Bedarf [Anmeldeinformationen für das Manager-Konto hinzu](/help/search-social-commerce/admin/manager-accounts.md).

   * Überprüfen Sie, ob das Anzeigennetzwerkkonto bereits denselben Metriknamen enthält. Benennen Sie in diesem Fall die Metrik um, damit die richtige Eigenschaft auf Managerebene erstellt werden kann.

* Vergewissern Sie sich, dass die Option „Hybrid“ des Portfolios ausgewählt ist und dass das Ziel einen gültigen Umsatz hat.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung der Konversionsmetriken eines Werbetreibenden](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Konversionsmetriken für Suche, Social Media und Commerce-Tracking hochladen nach [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
