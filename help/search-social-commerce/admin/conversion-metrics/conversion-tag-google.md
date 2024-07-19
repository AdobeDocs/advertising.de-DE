---
title: Konversions-Tag für  [!DNL Google Ads] erstellen
description: Erfahren Sie, wie Sie ein [!DNL Google Ads] Konversions-Tag erstellen.
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Konversions-Tag für [!DNL Google Ads] erstellen

Sie können Konversions-Tags für neue Konversionen erstellen, die für einzelne [!DNL Google Ads]-Konten verfolgt werden sollen, die nicht auf Manager-Kontoebene verfolgt werden.

Verwenden Sie zum Generieren von Konversions-Tags für vorhandene Konversionen den Editor des Anzeigennetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Geben Sie die [Konversions-Tag-Einstellungen](#conversion-tag-settings-google) an.

   1. Wählen Sie das Konto und dann den Konvertierungstyp aus.

   1. Klicken Sie auf **[!UICONTROL Next]**.

   1. Geben Sie die Konvertierungsoptionen an.

   1. Klicken Sie auf **[!UICONTROL Generate]**.

1. Kopieren Sie das Konversions-Tag und implementieren Sie es auf den Websites, von denen Sie die Konversionsmetrik verfolgen möchten.

   Siehe &quot;Installieren des [!DNL Google]-Tags&quot;in der [!DNL Google Ads]-Hilfe zu &quot;[2. Richten Sie das Google-Tag](https://support.google.com/google-ads/answer/12215519) ein.&quot;

1. Klicken Sie auf **[!UICONTROL Done].**

Nachdem Sie die Tags zu Ihrer Website hinzugefügt haben und sie ausgelöst werden, zeichnet [!DNL Google Ads] Konversionen auf der Website auf. In Search, Social und Commerce werden die Konversionen täglich synchronisiert. Weitere Informationen zu den synchronisierten Daten finden Sie unter &quot;[[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot;.

## Konversions-Tag-Einstellungen {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** Das entsprechende Google Ads-Konto.

**[!UICONTROL Type of Conversion]:** Der Typ der zu verfolgenden Konvertierung: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* oder *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Ein eindeutiger Name für die Konversionsmetrik.

**\[Konversionskategorie\]:** Die Konversionskategorie. Die verfügbaren Kategorien variieren je nach Konversionstyp. Für *[!UICONTROL Calls to a phone number on your website]* und *[!UICONTROL Clicks to your number on your mobile website]* ist standardmäßig &quot;[!UICONTROL Phone Call Lead]&quot;ausgewählt.

**\[Aktionstyp\]:** Ob das Ziel ein *[!UICONTROL Primary action used for bidding optimization]* oder ein *[!UICONTROL Secondary action not used for bidding optimization]* ist.

**[!UICONTROL Value]:** So messen Sie den [Wert jeder Konversion](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* ; dies erfordert, dass Sie eine Währung auswählen und den Wert für jede Konversion eingeben.

* *[!UICONTROL Use a different value for each conversion],* ; dies erfordert, dass Sie eine Währung auswählen und einen Standardwert für jede Konversion eingeben. Sie können den Standardwert im Tag mit einem transaktionsspezifischen Wert ändern, wenn Sie das Tag auf einer bestimmten Webseite implementieren.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Wie viele Konversionen pro Klick oder Interaktion gezählt werden sollen](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* oder *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Die maximale Anzahl von Tagen nach einer Anzeigeninteraktion, für die Konversionen aufgezeichnet werden. Für Such-, Anzeige- und Einkaufskampagnen kann das Fenster zwischen 1 und 90 Tagen betragen. Wählen Sie eine Zahl aus oder wählen Sie **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL View Through Conversion Window]:** Die maximale Anzahl von Tagen, nach denen ein Benutzer Ihre Anzeigen anzeigt, für die Durchsichtskonversionen aufgezeichnet werden. Für Such-, Anzeige- und Einkaufskampagnen kann das Fenster zwischen 1 und 90 Tagen betragen. Wählen Sie eine Zahl aus oder wählen Sie **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL Attribution Model]:** [Wie viel Gewichtung jede Anzeigeninteraktion erhält](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* oder *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
