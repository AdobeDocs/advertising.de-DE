---
title: Erstellen Sie eine Konversionsaktion für eine [!DNL Google Ads] erweiterte Konversion für Leads.
description: Erfahren Sie, wie Sie eine [!DNL Google Ads] Konversionsaktion für eine erweiterte Konversion für Leads erstellen.
feature: Conversions
source-git-commit: 5eb6ed5b42e74f424fc8499f6df0dbe3f2430ab2
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Erstellen Sie eine Konversionsaktion für eine [!DNL Google Ads] erweiterte Konversion für Leads.

*[!DNL Google Ads]nur Konten*

Sie können Konversionsaktionen für [!DNL Google Ads] erweiterte Konversionen erstellen, damit Leads für einzelne [!DNL Google Ads]-Konten verfolgt werden, nicht aber für Konversionen, die auf Manager-Kontoebene verfolgt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** , um die Registerkarte **[!UICONTROL Summary]** zu öffnen.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Geben Sie die Einstellungen für die Konvertierungsaktion [ an.](#conversion-action-settings-google)

   1. Wählen Sie das Konto aus und wählen Sie dann den Konvertierungstyp aus: *[!UICONTROL Import conversion]*.

   1. Klicken Sie auf **[!UICONTROL Next]**.

   1. Geben Sie die Konvertierungsaktionsoptionen an.

   1. Klicken Sie auf **[!UICONTROL Generate]**.

1. Lesen Sie Informationen darüber, wie Sie ein Tracking-Tag für die erweiterte Konversion für Leads erstellen, und klicken Sie dann auf **[!UICONTROL Next]**.

   Erstellen Sie das Konversions-Tag und implementieren Sie es nach Bedarf auf den Websites, von denen Sie die Konversionsmetrik verfolgen möchten. Anweisungen finden Sie in den folgenden Abschnitten:

   * Informationen zum Verwenden des Tags [!DNL Google] finden Sie in den Anweisungen zum Konfigurieren der Tag-Einstellungen für [!DNL Google] in &quot;[Einrichten verbesserter Konversionen für Leads mit dem Tag [!DNL Google] Tag](https://support.google.com/google-ads/answer/11347292)&quot;.[!DNL Google Ads]

   * Informationen zur Verwendung von [!DNL Google Tag Manager] finden Sie in den [!DNL Google Ads] Anweisungen zum Konfigurieren der Tag-Einstellungen für [!DNL Google] und &quot;Überprüfen Sie Ihr Setup und veröffentlichen Sie den Container&quot; in &quot;[Einrichten verbesserter Konvertierungen für Leads mit  [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure)&quot;.

1. Klicken Sie auf **[!UICONTROL Done].**

Nachdem Sie die Konversionsaktion erstellt und ein Konversions-Tracking-Tag implementiert haben, können Sie die Offline-Konversionsdaten hochladen, die Ihr Unternehmen erfasst und der Konversionsaktion zuordnet. Siehe &quot;[Hochladen von Offline-Konversionsdaten für erweiterte Konversionen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)&quot;.

## Einstellungen für Konvertierungsaktionen {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** Das entsprechende Google Ads-Konto.

**[!UICONTROL Type of Conversion]:** Der Typ der zu verfolgenden Konvertierung: Wählen Sie *[!UICONTROL Import conversion]* aus. Alle anderen Typen werden verwendet, um Konversions-Tracking-Tags (nicht Konversionsaktionen) für andere Konversionstypen zu erstellen.

**[!UICONTROL Conversion Name]:** Ein eindeutiger Name für die Konversionsaktion.

**\[Konversionskategorie\]:** Die Konversionskategorie, z. B. *Qualifizierter Lead* oder *Anmelden*.

**\[Aktionstyp\]:** Ob das Ziel ein *[!UICONTROL Primary action used for bidding optimization]* oder ein *[!UICONTROL Secondary action not used for bidding optimization]* ist.

**[!UICONTROL Value]:** So messen Sie den [Wert jeder Konversion](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],* ; dies erfordert, dass Sie eine Währung auswählen und den Wert für jede Konversion eingeben.

* *[!UICONTROL Use a different value for each conversion],* ; dies erfordert, dass Sie eine Währung auswählen und einen Standardwert für jede Konversion eingeben. Sie können den Standardwert im Tag mit einem transaktionsspezifischen Wert ändern, wenn Sie das Tag auf einer bestimmten Webseite implementieren.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Wie viele Konversionen pro Klick oder Interaktion gezählt werden sollen](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* oder *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Die maximale Anzahl von Tagen nach einer Anzeigeninteraktion, für die Konversionen aufgezeichnet werden. Für Such-, Anzeige- und Einkaufskampagnen kann das Fenster zwischen 1 und 90 Tagen betragen. Wählen Sie eine Zahl aus oder wählen Sie **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL View Through Conversion Window]:** Die maximale Anzahl von Tagen, nach denen ein Benutzer Ihre Anzeigen anzeigt, für die Durchsichtskonversionen aufgezeichnet werden. Für Such-, Anzeige- und Einkaufskampagnen kann das Fenster zwischen 1 und 90 Tagen betragen. Wählen Sie eine Zahl aus oder wählen Sie **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL Attribution Model]:** [Wie viel Gewichtung jede Anzeigeninteraktion erhält](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* oder *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konvertierungen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementieren [!DNL Google Ads] verbesserter Konvertierungen für Leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
