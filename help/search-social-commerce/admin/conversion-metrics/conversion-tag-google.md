---
title: Erstellen Sie ein Konvertierungs-Tag für [!DNL Google Ads]
description: Erfahren Sie, wie Sie ein Konversions [!DNL Google Ads] Tag erstellen.
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Erstellen eines Konvertierungs-Tags für [!DNL Google Ads]

Sie können Konversions-Tags für neue Konversionen erstellen, die für einzelne [!DNL Google Ads] und nicht auf Manager-Kontoebene verfolgt werden sollen.

Verwenden Sie den Editor des Anzeigennetzwerks, um Konvertierungs-Tags für vorhandene Konvertierungen zu generieren.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, wodurch die Registerkarte **[!UICONTROL Summary]** geöffnet wird.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Geben Sie die [Konvertierungs-Tag-Einstellungen](#conversion-tag-settings-google) an.

   1. Wählen Sie das Konto und dann den Konvertierungstyp aus.

   1. Klicken Sie auf **[!UICONTROL Next]**.

   1. Geben Sie die Konvertierungsoptionen an.

   1. Klicken Sie auf **[!UICONTROL Generate]**.

1. Kopieren Sie das Konversions-Tag und implementieren Sie es auf den Websites, von denen Sie die Konversionsmetrik verfolgen möchten.

   Siehe „Installieren des [!DNL Google]-Tags“ in der [!DNL Google Ads] Hilfe zu &quot;[2. Richten Sie Ihr Google-Tag ein](https://support.google.com/google-ads/answer/12215519)&quot;

1. Klicken Sie auf **[!UICONTROL Done].**

Nachdem Sie die Tags zu Ihrer Website hinzugefügt haben und sie ausgelöst werden, zeichnet [!DNL Google Ads] Konversionen auf der Website auf. Search, Social und Commerce synchronisieren die Konversionen täglich. Weitere Informationen zu den synchronisierten Daten finden Sie unter &quot;[[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Konvertierungs-Tag-Einstellungen {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** Das entsprechende Google Ads-Konto.

**[!UICONTROL Type of Conversion]:** Der Typ der zu verfolgenden Konvertierung: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* oder *[!UICONTROL Clicks to your number on your mobile website]*. **Hinweis:** *[!UICONTROL Import conversion]* wird für einen anderen Zweck verwendet; siehe &quot;[Erstellen einer Konversionsaktion für eine  [!DNL Google Ads] -Konversion für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)&quot;

**[!UICONTROL Conversion Name]:** Ein eindeutiger Name für die Konversionsmetrik.

**\[Konversionskategorie\]:** Die Konversionskategorie. Die verfügbaren Kategorien variieren je nach Konversionstyp. Für *[!UICONTROL Calls to a phone number on your website]* und *[!UICONTROL Clicks to your number on your mobile website]* ist standardmäßig &quot;[!UICONTROL Phone Call Lead]&quot; ausgewählt.

**\[Aktionstyp\]:**, ob das Ziel ein *[!UICONTROL Primary action used for bidding optimization]* oder ein *[!UICONTROL Secondary action not used for bidding optimization]* ist.

**[!UICONTROL Value]:** Messen des [Werts jeder Konversion](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],*. Dazu müssen Sie eine Währung auswählen und den Wert für jede Konvertierung eingeben.

* *[!UICONTROL Use a different value for each conversion],*. Dazu müssen Sie eine Währung auswählen und für jede Konvertierung einen Standardwert eingeben. Sie können den Standardwert im -Tag in einen transaktionsspezifischen Wert ändern, wenn Sie das Tag auf einer bestimmten Web-Seite implementieren.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Anzahl der pro Klick oder Interaktion zu zählenden Konversionen](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* oder *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Die maximale Anzahl von Tagen nach einer Anzeigeninteraktion, für die Konversionen aufgezeichnet werden. Für Kampagnen zum Suchen, Anzeigen und Einkaufen kann das Fenster 1 bis 90 Tage lang sein. Wählen Sie eine Zahl aus oder klicken Sie auf **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL View Through Conversion Window]:** Die maximale Anzahl von Tagen, nachdem ein Benutzer Ihre Anzeigen angesehen hat, für die View-Through-Konversionen aufgezeichnet werden. Für Kampagnen zum Suchen, Anzeigen und Einkaufen kann das Fenster 1 bis 90 Tage lang sein. Wählen Sie eine Zahl aus oder klicken Sie auf **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL Attribution Model]:** [Wie viel Credits erhält jede Anzeigeninteraktion](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* oder *[!UICONTROL Last click]*. **Hinweis:** Konvertierungsaktionen, die zuvor die jetzt nicht unterstützten *[!UICONTROL First click]*-, *[!UICONTROL Linear]*-, *[!UICONTROL Time decay]*- oder *[!UICONTROL Position based]*-Modelle verwendet haben, verwenden jetzt das *[!UICONTROL Data driven]*.

>[!MORELIKETHIS]
>
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konversionen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
