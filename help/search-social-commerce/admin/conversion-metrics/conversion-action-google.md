---
title: Erstellen einer Konvertierungsaktion für eine  [!DNL Google Ads]  Konversion für Leads
description: Erfahren Sie, wie Sie eine  [!DNL Google Ads]  für eine erweiterte Konversion für Leads erstellen.
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
source-git-commit: f29d5173547a48ea818a93a0b931d5fb27e10044
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Erstellen einer Konvertierungsaktion für eine [!DNL Google Ads] erweiterte Konversion für Leads

Nur *[!DNL Google Ads]Konten*

Sie können Konversionsaktionen für [!DNL Google Ads] erweiterten Konversionen für Leads erstellen, die für einzelne [!DNL Google Ads] verfolgt werden sollen, und nicht für Konversionen, die auf der Ebene eines Manager-Kontos verfolgt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**. Dadurch wird die Registerkarte **[!UICONTROL Summary]** geöffnet.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Geben Sie die [Einstellungen für Konversionsaktionen](#conversion-action-settings-google) an.

   1. Wählen Sie das Konto und dann den Konvertierungstyp aus: *[!UICONTROL Import conversion]*.

   1. Klicken Sie auf **[!UICONTROL Next]**.

   1. Geben Sie die Optionen für die Konvertierungsaktion an.

   1. Klicken Sie auf **[!UICONTROL Generate]**.

1. Lesen Sie die Informationen zum Erstellen eines Tracking-Tags für die erweiterte Konversion für Leads, und klicken Sie dann auf **[!UICONTROL Next]**.

   Erstellen Sie das Konversions-Tag und implementieren Sie es nach Bedarf auf den Websites, von denen Sie die Konversionsmetrik verfolgen möchten. Anweisungen finden Sie unter:

   * Informationen zur Verwendung des [!DNL Google]-Tags finden Sie in den [!DNL Google Ads] zu „Konfigurieren [!DNL Google] Tag-Einstellungen“ unter &quot;[Einrichten erweiterter Konversionen für Leads mit dem  [!DNL Google] -Tag](https://support.google.com/google-ads/answer/11347292)&quot;.

   * Informationen zur Verwendung von [!DNL Google Tag Manager] finden Sie in den [!DNL Google Ads] zu „Konfigurieren [!DNL Google] Tag-Einstellungen“ und „Überprüfen Sie Ihr Setup und veröffentlichen Sie den Container“ unter &quot;[Einrichten erweiterter Konversionen für Leads mit [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure).

1. Klicken Sie auf **[!UICONTROL Done].**

Nachdem Sie die Konversionsaktion erstellt und ein Konversionsverfolgungs-Tag implementiert haben, können Sie die von Ihrem Unternehmen erfassten Offline-Konversionsdaten hochladen und der Konversionsaktion zuordnen. Siehe [Hochladen von Offline-Konversionsdaten für erweiterte Konversionen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md).

## Einstellungen für Konversionsaktionen {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** Das entsprechende Google Ads-Konto.

**[!UICONTROL Type of Conversion]:** Der Typ der nachzuverfolgenden Konversion: *[!UICONTROL Import conversion]* auswählen. Alle anderen Typen werden verwendet, um Konversionsverfolgungstags (keine Konversionsaktionen) für andere Konversionstypen zu erstellen.

**[!UICONTROL Conversion Name]:** Ein eindeutiger Name für die Konvertierungsaktion.

**\[Konversionskategorie\]:** Die Konversionskategorie, z. B *„Qualifizierter Lead* oder *Anmeldung*.

**\[Aktionstyp\]:**, ob das Ziel ein *[!UICONTROL Primary action used for bidding optimization]* oder ein *[!UICONTROL Secondary action not used for bidding optimization]* ist.

**[!UICONTROL Value]:** Messen des [Werts jeder Konversion](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],*. Dazu müssen Sie eine Währung auswählen und den Wert für jede Konvertierung eingeben.

* *[!UICONTROL Use a different value for each conversion],*. Dazu müssen Sie eine Währung auswählen und für jede Konvertierung einen Standardwert eingeben. Sie können den Standardwert im -Tag in einen transaktionsspezifischen Wert ändern, wenn Sie das Tag auf einer bestimmten Web-Seite implementieren.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Anzahl der pro Klick oder Interaktion zu zählenden Konversionen](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* oder *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Die maximale Anzahl von Tagen nach einer Anzeigeninteraktion, für die Konversionen aufgezeichnet werden. Für Kampagnen zum Suchen, Anzeigen und Einkaufen kann das Fenster 1 bis 90 Tage lang sein. Wählen Sie eine Zahl aus oder klicken Sie auf **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL View Through Conversion Window]:** Die maximale Anzahl von Tagen, nachdem ein Benutzer Ihre Anzeigen angesehen hat, für die View-Through-Konversionen aufgezeichnet werden. Für Kampagnen zum Suchen, Anzeigen und Einkaufen kann das Fenster 1 bis 90 Tage lang sein. Wählen Sie eine Zahl aus oder klicken Sie auf **[!UICONTROL Custom]** und geben Sie eine Zahl ein.

**[!UICONTROL Attribution Model]:** [Wie viel Credits erhält jede Anzeigeninteraktion](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* oder *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konversionen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementieren [!DNL Google Ads] verbesserter Konversionen für Leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
