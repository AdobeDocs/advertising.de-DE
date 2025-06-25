---
title: Verwalten von Zielgruppen für den Kundenabgleich mithilfe von Kundendatenlisten
description: Erfahren Sie, wie Sie Zielgruppen  [!DNL Google Ads]  Kundenabgleich und  [!DNL Microsoft Advertising]  in Ihren Kundendatenlisten erstellen und bearbeiten.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Verwalten von [!DNL Google Ads] und [!DNL Microsoft Advertising] von Zielgruppen für den Kundenabgleich mithilfe von Kundendatenlisten

Sie können aus Ihren Kundendatenlisten Zielgruppen für den Kundenabgleich erstellen [!DNL Google Ads] und [!DNL Microsoft Advertising]. Sie können auch alle [!DNL Google Ads] oder [!DNL Microsoft Advertising] Zielgruppen aktualisieren, mit Ausnahme [!DNL Google Ads] Zielgruppen, die aus einer [!DNL Adobe] Zielgruppe erstellt wurden.

## Erstellen einer Zielgruppe für den Kundenabgleich aus einer Kundendatenliste

*[!DNL Google Ads]- und [!DNL Microsoft Advertising], die nur für den Kundenabgleich infrage kommen*

Sie können eine [!DNL Google Ads] oder [!DNL Microsoft Advertising] kundendatenbasierte Liste aus einer Datendatei erstellen, die Sie aus Ihrem CRM-System (Customer Relationship Management) generieren.

Bei [!DNL Microsoft Advertising]-Konten kann die Datei E-Mail-Adressen enthalten. Bei [!DNL Google Ads]-Konten kann die Datei E-Mail-Adressen, Postanschriften oder Telefonnummern, Benutzer-IDs oder IDs von Mobilgeräten aus Ihrem CRM enthalten.

>[!NOTE]
>
>Search, Social und Commerce speichern keine Kundendaten, die Sie hochladen, oder aus den [!DNL Adobe] Segmenten, die zum Erstellen oder Bearbeiten einer [!DNL Google Ads] oder [!DNL Microsoft Advertising] Zielgruppe verwendet werden.

1. Generieren Sie eine Datei mit den Kundendaten im erforderlichen Format.

   Vor- und Nachnamen, E-Mail-Adressen und Telefonnummern müssen mit dem SHA-256-Algorithmus gehasht werden. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Eine Liste der zulässigen Felder und Anforderungen für Kontaktinformationen finden Sie [!DNL Google Ads] Zielgruppen in der [!DNL Google Ads]-Dokumentation unter [Formatierungsrichtlinien für ](https://support.google.com/google-ads/answer/7476159) Hochladen von Hash-Daten“. [!DNL Microsoft Advertising] Zielgruppen finden Sie in der [!DNL Microsoft Advertising] Dokumentation unter [Vorbereiten von Kundenabgleichlisten](https://help.ads.microsoft.com/#apex/ads/en/56921). Optional können Sie eine [!DNL Microsoft Excel] Vorlage für Kontaktinformationen herunterladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Anzeigennetzwerk und den Kontonamen aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Wählen Sie im [!UICONTROL Data Source] Menü **[!UICONTROL Customer List]** aus.

   1. Geben Sie die **[!UICONTROL Audience Name]** ein.

   1. Laden Sie die Datei hoch:

      1. Wählen Sie die [!UICONTROL Data Upload Type] aus: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]* oder *[!UICONTROL Mobile Device IDs]*.

         Die Option „Benutzer-IDs“ steht nur [!DNL Google Ads] Werbetreibenden in den USA zur Verfügung, die für „Benutzer-ID[Segmente“ ](https://support.google.com/google-ads/answer/9199250)

      1. (Nur ID-Listen für Mobilgeräte) Wählen Sie die **[!UICONTROL OS Type]** aus (*[!UICONTROL Android™]* oder *[!UICONTROL iOS]*) und geben Sie die **[!UICONTROL App ID]** ein.

         Die App-ID ist eine eindeutige Kennung, die vom Betriebssystem für Mobilgeräte verwendet wird, damit Ihre Anwendung eine Verbindung zu Google Play oder Apple App Store herstellen kann:

         * ([!DNL Android™] Apps) Der [!DNL Android™] Paketname in [!DNL Google Play], der durch &quot;`id=<package_name>`&quot; identifiziert wird.

           In `https://play.google.com/store/apps/details?id=com.example.game` lautet der Paketname beispielsweise com.example.game.

         * ([!DNL iOS] Apps) Die Anwendungs-ID innerhalb der [!DNL iTunes App Store], die durch &quot;`<idNNNNNNNNN>`&quot; am Ende der URL identifiziert wird. Es ist auch im [!DNL iOS Developer Console] erhältlich.

           In `https://itunes.apple.com/us/app/id284882215` ist die ID beispielsweise id284882215.

         Ihr Entwicklungs-Team hat Zugriff auf die [!UICONTROL App ID] für die entsprechende Plattform.

      1. Klicken Sie im Feld [!UICONTROL Select File] auf **[!UICONTROL Choose File]** und wählen Sie die Datei auf Ihrem Netzwerk oder Gerät aus.

      1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie mit den Bedingungen der Datenschutzrichtlinien für [!DNL Adobe] und Werbenetzwerke einverstanden sind.

      1. (Werbetreibende, die [!DNL Google Ads] Zielgruppen erstellen und im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (Vereinigtes Königreich) Geschäfte tätigen; optional) Wenn Sie die Zustimmung von EWR- und britischen Nutzern eingeholt haben, ihre Daten zu Werbezwecken hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignoriert alle Daten für Benutzer im EWR und im Vereinigten Königreich mit einem nicht spezifizierten Einverständnisstatus. Dies kann zu Datendiskrepanzen und Leistungsproblemen führen.

      1. Klicken Sie auf **[!UICONTROL Upload File]**.

   1. Geben Sie die Anzahl der **[!UICONTROL Membership Days]** an, d. h. die Anzahl der Tage, die das Cookie eines Benutzers in der Zielgruppe verbleibt.

   Verwenden Sie die Zeitspanne, für die Ihre Anzeige für den Benutzer relevant sein soll. Kundenlisten laufen nur ab, wenn Sie einen Wert eingeben.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>* Die Verarbeitung der Datei kann im Anzeigennetzwerk bis zu 24 Stunden dauern.
>* Siehe [[!DNL Google Ads] Dokumentation zur Funktionsweise von Customer Match und zu Einschränkungen](https://support.google.com/displayvideo/answer/9539301).

## Bearbeiten einer Zielgruppe vom Typ „Kundenabgleich“ mithilfe einer Kundendatenliste

Sie können jede [!DNL Google Ads] oder [!DNL Microsoft Advertising] Zielgruppe, die mit Kunden übereinstimmt, aktualisieren, mit Ausnahme [!DNL Google Ads] Zielgruppen, die aus einer [!DNL Adobe] Zielgruppe erstellt wurden. Sie können Daten hochladen, um sie hinzuzufügen, zu löschen oder alle vorhandenen Daten für die Zielgruppe zu ersetzen.

Die Daten müssen vom gleichen Typ wie die ursprüngliche Kundenliste sein (E-Mail-Adressen, Postanschriften, Telefonnummern, Benutzer-IDs oder IDs von Mobilgeräten für eine bestimmte Mobile App unter einem bestimmten mobilen Betriebssystem).

1. Generieren Sie eine Datei mit den Kundendaten im erforderlichen Format für den vorhandenen Datentyp.

Vor- und Nachnamen, E-Mail-Adressen und Telefonnummern müssen mit dem SHA-256-Algorithmus gehasht werden. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Eine Liste der zulässigen Felder und Anforderungen für Kontaktinformationen finden Sie [!DNL Google Ads] Zielgruppen in der [!DNL Google Ads]-Dokumentation unter [Formatierungsrichtlinien für ](https://support.google.com/google-ads/answer/7476159) Hochladen von Hash-Daten“. [!DNL Microsoft Advertising] Zielgruppen finden Sie in der [!DNL Microsoft Advertising] Dokumentation unter [Vorbereiten von Kundenabgleichlisten]&#x200B;(https://help.ads.microsoft.com/#apex/ads/en/56921. Optional können Sie eine [!DNL Microsoft Excel] Vorlage für Kontaktinformationen herunterladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Aktivieren Sie das Kontrollkästchen neben der Audience, die Sie bearbeiten möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png).

1. Wählen Sie die Aktion aus: *[!UICONTROL Add]* (um die hochgeladenen Daten zu den vorhandenen Daten hinzuzufügen, sofern sie noch nicht vorhanden sind), *[!UICONTROL Delete]* (um die hochgeladenen Daten aus den vorhandenen Daten zu löschen, sofern sie bereits vorhanden sind) oder *[!UICONTROL Replace]* (um alle vorhandenen Daten zu löschen und sie durch die hochgeladenen Daten zu ersetzen).

1. Laden Sie die Datei hoch:

   1. Klicken Sie im Feld [!UICONTROL Select File] auf **[!UICONTROL Choose File]** und wählen Sie die Datei auf Ihrem Netzwerk oder Gerät aus.

   1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie mit den Bedingungen der Datenschutzrichtlinien für [!DNL Adobe] und Werbenetzwerke einverstanden sind.

   1. Klicken Sie auf **[!UICONTROL Upload File]**.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>Es kann eine Weile dauern, bis das Werbenetzwerk Aktualisierungen für eine Zielgruppe verarbeitet.

>[!MORELIKETHIS]
>
>* [Info über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] Kundenabgleich von Zielgruppen aus [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Erstellen einer Zielgruppe  [!DNL Google Ads]  Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Dynamische Remarketing-Audiences verwalten](audience-dynamic-remarketing-manage.md)
