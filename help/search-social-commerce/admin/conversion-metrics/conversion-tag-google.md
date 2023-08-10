---
title: Erstellen Sie ein Konversions-Tag für [!DNL Google Ads]
description: Erfahren Sie, wie Sie eine [!DNL Google Ads] Konversions-Tag.
feature: Conversions
source-git-commit: 395421c69214c3b0370523909047a924af23ea55
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Erstellen Sie ein Konversions-Tag für [!DNL Google Ads]

Sie können Konversions-Tags für neue Konversionen erstellen, die für einzelne [!DNL Google Ads] -Konten, die nicht auf der Ebene eines Manager-Kontos verfolgt werden.

Verwenden Sie zum Generieren von Konversions-Tags für vorhandene Konversionen den Editor des Anzeigennetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Geben Sie die [Konversions-Tag-Einstellungen](#conversion-tag-settings-google).

   1. Wählen Sie das Konto und dann den Konvertierungstyp aus.

   1. Klicken **[!UICONTROL Next]**.

   1. Geben Sie die Konvertierungsoptionen an.

   1. Klicken **[!UICONTROL Generate]**.

1. Kopieren Sie das Konversions-Tag und implementieren Sie es auf den Websites, von denen Sie die Konversionsmetrik verfolgen möchten.

   Siehe &quot;Installieren der [!DNL Google] Tag&quot;in der [!DNL Google Ads] &quot;[2. Google-Tag einrichten](https://support.google.com/google-ads/answer/12215519).&quot;

1. Klicken **[!UICONTROL Done].**

Nachdem Sie die Tags zu Ihrer Website hinzugefügt haben und sie ausgelöst werden, [!DNL Google Ads] erfasst Konversionen auf der Website. In Search, Social und Commerce werden die Konversionen täglich synchronisiert. Weitere Informationen zu den synchronisierten Daten finden Sie unter[[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Konversions-Tag-Einstellungen {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** Das entsprechende Google Ads-Konto.

**[!UICONTROL Type of Conversion]:** Der Typ der zu verfolgenden Konvertierung: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* oder *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Ein eindeutiger Name für die Konversionsmetrik.

**\[Konversionskategorie\]:** Die Konversionskategorie. Die verfügbaren Kategorien variieren je nach Konversionstyp. Für *[!UICONTROL Calls to a phone number on your website]* und *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]ist standardmäßig ausgewählt.

**\[Aktionstyp\]:** Ob das Ziel eine *[!UICONTROL Primary action used for bidding optimization]* oder *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Messen der [Wert jeder Konversion](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* müssen Sie eine Währung auswählen und den Wert für jede Konversion eingeben.

* *[!UICONTROL Use a different value for each conversion],* müssen Sie eine Währung auswählen und einen Standardwert für jede Konversion eingeben. Sie können den Standardwert im Tag mit einem transaktionsspezifischen Wert ändern, wenn Sie das Tag auf einer bestimmten Webseite implementieren.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Anzahl der Konversionen pro Klick oder Interaktion](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* oder *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Die maximale Anzahl von Tagen nach einer Anzeigeninteraktion, für die Konversionen aufgezeichnet werden. Für Such-, Anzeige- und Einkaufskampagnen kann das Fenster zwischen 1 und 90 Tagen betragen. Auswählen einer Zahl oder Auswählen **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL View Through Conversion Window]:** Die maximale Anzahl von Tagen, nach denen ein Benutzer Ihre Anzeigen aufruft, für die Durchsichtskonversionen aufgezeichnet werden. Für Such-, Anzeige- und Einkaufskampagnen kann das Fenster zwischen 1 und 90 Tagen betragen. Auswählen einer Zahl oder Auswählen **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL Attribution Model]:** [Wie viel Gewichtung jede Anzeigeninteraktion erhält](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* oder *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
