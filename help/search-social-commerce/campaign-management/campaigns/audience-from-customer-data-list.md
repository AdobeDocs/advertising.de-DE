---
title: Verwalten von Zielgruppen zur Kundenabstimmung mithilfe von Kundendatenlisten
description: Erfahren Sie, wie Sie [!DNL Google Ads] und [!DNL Microsoft® Advertising] Kundenabgleich-Zielgruppen aus Ihren Kundendatenlisten.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 588b6b5887903e5912fc68a18ef142d908026870
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Verwalten [!DNL Google Ads] und [!DNL Microsoft® Advertising] Kundenabgleich von Zielgruppen mithilfe von Kundendatenlisten

Sie können [!DNL Google Ads] und [!DNL Microsoft® Advertising] Kundenabgleich-Zielgruppen aus Ihren Kundendatenlisten. Sie können auch jede [!DNL Google Ads] oder [!DNL Microsoft® Advertising] Zielgruppe für Kundenabgleich mit Ausnahme von [!DNL Google Ads] Zielgruppen, die aus einer [!DNL Adobe] Zielgruppe.

## Erstellen einer Zielgruppe für die Kundenabstimmung aus einer Kundendatenliste

*[!DNL Google Ads]und [!DNL Microsoft® Advertising] Konten, die nur für die Kundenübereinstimmung infrage kommen*

Sie können eine [!DNL Google Ads] oder [!DNL Microsoft® Advertising] kundendatenbasierte Liste aus einer Datendatei, die Sie aus Ihrem CRM-System (Customer Relationship Management) generieren.

Für [!DNL Microsoft® Advertising] Konten, kann die Datei E-Mail-Adressen enthalten. Für [!DNL Google Ads] -Konten, kann die Datei E-Mail-Adressen, Postanschriften oder Telefonnummern, Benutzer-IDs oder Mobilgeräte-IDs aus Ihrem CRM-System enthalten.

>[!NOTE]
>
>&quot;Search&quot;, &quot;Social&quot;und &quot;Commerce&quot;speichern keine der Kundendaten, die Sie hochladen, oder die aus dem [!DNL Adobe] Segmente zum Erstellen oder Bearbeiten von [!DNL Google Ads] oder [!DNL Microsoft® Advertising] Zielgruppe.

1. Erstellen Sie eine Datei mit den Kundendaten im gewünschten Format.

   Vor- und Nachnamen, E-Mail-Adressen und Telefonnummern müssen mit dem SHA-256-Algorithmus gehasht werden. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Für [!DNL Google Ads] Zielgruppen, siehe [!DNL Google Ads] Dokumentation zu &quot;[Formatierungsrichtlinien für das Hochladen von Hash-Daten](https://support.google.com/google-ads/answer/7476159)&quot; für eine Liste der zulässigen Kontaktdatenfelder und Anforderungen. Für [!DNL Microsoft® Advertising] Zielgruppen, siehe [!DNL Microsoft® Advertising] Dokumentation zu [Anpassen der Kundenübereinstimmungslisten](https://help.ads.microsoft.com/#apex/ads/en/56921. Sie können optional eine [!DNL Microsoft® Excel] Vorlage für Kontaktinformationen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Im [!UICONTROL Data Source] Menü auswählen **[!UICONTROL Customer List]**.

   1. Geben Sie die **[!UICONTROL Audience Name]**.

   1. Laden Sie die Datei hoch:

      1. Wählen Sie die [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]* oder *[!UICONTROL Mobile Device IDs]*.

         Die Option Benutzer-IDs ist nur für [!DNL Google Ads] Advertiser in den USA, die sich für [Benutzer-ID-Segmente](https://support.google.com/google-ads/answer/9199250)

      1. (Nur Liste der Mobilgeräte-IDs) Wählen Sie die **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* oder *[!UICONTROL iOS]*) und geben Sie die **[!UICONTROL App ID]**.

         Die App-ID ist eine eindeutige Kennung, die das mobile Betriebssystem verwendet, damit Ihre Anwendung eine Verbindung zu Google Play oder Apple App Store herstellen kann:

         * ([!DNL Android™] apps) Die [!DNL Android™] Paketname in [!DNL Google Play]durch &quot;`id=<package_name>`.&quot;

           In https://play.google.com/store/apps/details?id=com.example.game lautet der Paketname beispielsweise com.example.game.

         * ([!DNL iOS] apps) Die Anwendungs-ID innerhalb der [!DNL iTunes App Store]durch &quot;`<idNNNNNNNNN>`&quot; am Ende der URL. Es ist auch im [!DNL iOS Developer Console].

           In https://itunes.apple.com/us/app/id284882215 lautet die ID beispielsweise id284882215.

         Ihr Entwicklungsteam hat Zugriff auf die [!UICONTROL App ID] für die jeweilige Plattform.

      1. Im [!UICONTROL Select File] Feld, klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie die Datei in Ihrem Netzwerk oder Gerät aus.

      1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie den Bedingungen der [!DNL Adobe] Datenschutzrichtlinien für Werbenetzwerke.

      1. (Erstellen von Advertisern [!DNL Google Ads] Zielgruppen, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) geschäftlich tätig sind (optional) Wenn Sie die Zustimmung von EWR- und britischen Benutzern erhalten haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignoriert alle Daten für Benutzer des EWR und des Vereinigten Königreichs mit einem nicht festgelegten Genehmigungsstatus. Dies kann zu Datendiskrepanzen und Leistungsproblemen führen.

      1. Klicks **[!UICONTROL Upload File]**.

   1. Geben Sie die Anzahl der **[!UICONTROL Membership Days]**: die Anzahl der Tage, in denen das Cookie eines Benutzers in der Zielgruppe verbleibt.

   Verwenden Sie die Zeitdauer, für die Sie erwarten, dass Ihre Anzeige für den Benutzer relevant ist. Kundenlisten laufen nur ab, wenn Sie einen Wert eingeben.

1. Klicks **[!UICONTROL Post]**.

>[!NOTE]
>
>* Die Verarbeitung der Datei im Werbenetzwerk kann bis zu 24 Stunden dauern.
>* Siehe [[!DNL Google Ads] Dokumentation zur Funktionsweise und Einschränkungen von Kundenabgleich](https://support.google.com/displayvideo/answer/9539301).

## Bearbeiten einer Zielgruppe &quot;Kundenabgleich&quot;mithilfe einer Kundendatenliste

Sie können jede [!DNL Google Ads] oder [!DNL Microsoft® Advertising] Zielgruppe für Kundenabgleich mit Ausnahme von [!DNL Google Ads] Zielgruppen, die aus einer [!DNL Adobe] Zielgruppe. Sie können Daten hochladen, um alle vorhandenen Daten für die Audience hinzuzufügen, zu löschen oder zu ersetzen.

Die Daten müssen vom ursprünglichen Typ der Kundenliste sein (E-Mail-Adressen, Postanschriften, Telefonnummern, Benutzer-IDs oder Mobilgeräte-IDs für eine bestimmte App unter einem bestimmten mobilen Betriebssystem).

1. Erstellen Sie eine Datei mit den Kundendaten im erforderlichen Format für den vorhandenen Datentyp.

Vor- und Nachnamen, E-Mail-Adressen und Telefonnummern müssen mit dem SHA-256-Algorithmus gehasht werden. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Für [!DNL Google Ads] Zielgruppen, siehe [!DNL Google Ads] Dokumentation zu &quot;[Formatierungsrichtlinien für das Hochladen von Hash-Daten](https://support.google.com/google-ads/answer/7476159)&quot; für eine Liste der zulässigen Kontaktdatenfelder und Anforderungen. Für [!DNL Microsoft® Advertising] Zielgruppen, siehe [!DNL Microsoft® Advertising] Dokumentation zu [Anpassen der Kundenübereinstimmungslisten](https://help.ads.microsoft.com/#apex/ads/en/56921. Sie können optional eine [!DNL Microsoft® Excel] Vorlage für Kontaktinformationen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Aktivieren Sie das Kontrollkästchen neben der zu bearbeitenden Audience.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png).

1. Wählen Sie die Aktion aus: *[!UICONTROL Add]* (um die hochgeladenen Daten den vorhandenen Daten hinzuzufügen, sofern sie nicht bereits existieren), *[!UICONTROL Delete]* (zum Löschen der hochgeladenen Daten aus den vorhandenen Daten, sofern diese bereits vorhanden sind) oder *[!UICONTROL Replace]* (um alle vorhandenen Daten zu löschen und sie durch die hochgeladenen Daten zu ersetzen).

1. Laden Sie die Datei hoch:

   1. Im [!UICONTROL Select File] Feld, klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie die Datei in Ihrem Netzwerk oder Gerät aus.

   1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie den Bedingungen der [!DNL Adobe] Datenschutzrichtlinien für Werbenetzwerke.

   1. Klicks **[!UICONTROL Upload File]**.

1. Klicks **[!UICONTROL Post]**.

>[!NOTE]
>
>Die Verarbeitung von Aktualisierungen an einer Audience im Werbenetzwerk kann einige Zeit dauern.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] Kundenabgleich-Zielgruppen aus [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Erstellen Sie eine [!DNL Google Ads] Zielgruppe für Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Dynamische Remarketing-Zielgruppen verwalten](audience-dynamic-remarketing-manage.md)
