---
title: Verwalten von Zielgruppen zur Kundenabstimmung mithilfe von Kundendatenlisten
description: Erfahren Sie, wie Sie in Ihren Kundendatenlisten  [!DNL Google Ads] und [!DNL Microsoft Advertising] Kundenabgleichs-Zielgruppen erstellen und bearbeiten.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Verwalten von [!DNL Google Ads] und [!DNL Microsoft Advertising] Kundenabgleich-Zielgruppen mithilfe von Kundendatenlisten

Sie können aus Ihren Kundendatenlisten [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Kundenabgleich-Zielgruppen erstellen. Sie können auch eine beliebige [!DNL Google Ads] - oder [!DNL Microsoft Advertising] Kundenabgleichs-Zielgruppe aktualisieren, mit Ausnahme von [!DNL Google Ads] Zielgruppen, die aus einer [!DNL Adobe] -Zielgruppe erstellt wurden.

## Erstellen einer Zielgruppe für die Kundenabstimmung aus einer Kundendatenliste

*[!DNL Google Ads]- und [!DNL Microsoft Advertising] -Konten, die nur für eine Kundenübereinstimmung infrage kommen*

Sie können eine auf Kundendaten basierende Liste mit dem Wert [!DNL Google Ads] oder [!DNL Microsoft Advertising] aus einer Datendatei erstellen, die Sie aus Ihrem CRM-System (Customer Relationship Management) generieren.

Bei [!DNL Microsoft Advertising] -Konten kann die Datei E-Mail-Adressen enthalten. Bei [!DNL Google Ads] -Konten kann die Datei E-Mail-Adressen, Postanschriften oder Telefonnummern, Benutzer-IDs oder Mobilgeräte-IDs aus Ihrem CRM-System enthalten.

>[!NOTE]
>
>In Search, Social und Commerce werden keine der von Ihnen hochgeladenen Kundendaten oder der [!DNL Adobe] Segmente gespeichert, die zum Erstellen oder Bearbeiten einer [!DNL Google Ads] - oder [!DNL Microsoft Advertising] -Zielgruppe verwendet werden.

1. Erstellen Sie eine Datei mit den Kundendaten im gewünschten Format.

   Vor- und Nachnamen, E-Mail-Adressen und Telefonnummern müssen mit dem SHA-256-Algorithmus gehasht werden. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Für [!DNL Google Ads] -Zielgruppen finden Sie in der [!DNL Google Ads] Dokumentation zu &quot;[Formatierungsrichtlinien für das Hochladen von Hash-Daten](https://support.google.com/google-ads/answer/7476159)&quot; eine Liste der zulässigen Kontaktdatenfelder und -anforderungen. Informationen zu [!DNL Microsoft Advertising] -Zielgruppen finden Sie in der [!DNL Microsoft Advertising] Dokumentation zu [ Vorbereitung von Kundenübereinstimmungslisten](https://help.ads.microsoft.com/#apex/ads/en/56921). Sie können optional eine [!DNL Microsoft Excel] -Vorlage für Kontaktinformationen herunterladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Wählen Sie im Menü [!UICONTROL Data Source] die Option **[!UICONTROL Customer List]** aus.

   1. Geben Sie den Wert **[!UICONTROL Audience Name]** ein.

   1. Laden Sie die Datei hoch:

      1. Wählen Sie die [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]* oder *[!UICONTROL Mobile Device IDs]* aus.

         Die Option Benutzer-IDs ist nur für [!DNL Google Ads] -Advertiser in den USA verfügbar, die sich für [Benutzer-ID-Segmente](https://support.google.com/google-ads/answer/9199250) entschieden haben

      1. (Nur Liste der Mobilgeräte-IDs) Wählen Sie den Wert **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* oder *[!UICONTROL iOS]*) und geben Sie den Wert **[!UICONTROL App ID]** ein.

         Die App-ID ist eine eindeutige Kennung, die das mobile Betriebssystem verwendet, damit Ihre Anwendung eine Verbindung zu Google Play oder Apple App Store herstellen kann:

         * ([!DNL Android™] apps) Der [!DNL Android™] Paketname innerhalb von [!DNL Google Play], identifiziert durch &quot;`id=<package_name>`&quot;.

           In https://play.google.com/store/apps/details?id=com.example.game lautet der Paketname beispielsweise com.example.game.

         * ([!DNL iOS] apps) Die Anwendungs-ID innerhalb des [!DNL iTunes App Store], identifiziert durch &quot;`<idNNNNNNNNN>`&quot;am Ende der URL. Sie ist auch im [!DNL iOS Developer Console] verfügbar.

           In https://itunes.apple.com/us/app/id284882215 lautet die ID beispielsweise id284882215.

         Ihr Entwicklungsteam hat Zugriff auf die [!UICONTROL App ID] für die jeweilige Plattform.

      1. Klicken Sie im Feld [!UICONTROL Select File] auf **[!UICONTROL Choose File]** und wählen Sie die Datei in Ihrem Netzwerk oder Gerät aus.

      1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie den Bedingungen der Datenschutzrichtlinien für [!DNL Adobe] und Werbenetzwerke zustimmen.

      1. (Werbetreibende, die [!DNL Google Ads] Zielgruppen erstellen, die im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK) geschäftlich tätig sind; optional) Wenn Sie die Zustimmung von EWR- und britischen Benutzern eingeholt haben, ihre Daten für Werbezwecke hochzuladen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignoriert alle Daten für Benutzer des EWR und des Vereinigten Königreichs mit einem nicht spezifizierten Genehmigungsstatus. Dies kann zu Datendiskrepanzen und Leistungsproblemen führen.

      1. Klicken Sie auf **[!UICONTROL Upload File]**.

   1. Geben Sie die Anzahl von **[!UICONTROL Membership Days]** an, also die Anzahl der Tage, in denen das Cookie eines Benutzers in der Zielgruppe verbleibt.

   Verwenden Sie die Zeitdauer, für die Sie erwarten, dass Ihre Anzeige für den Benutzer relevant ist. Kundenlisten laufen nur ab, wenn Sie einen Wert eingeben.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>* Die Verarbeitung der Datei im Werbenetzwerk kann bis zu 24 Stunden dauern.
>* Siehe die [[!DNL Google Ads] Dokumentation zur Funktionsweise der Kundenabgleich und zu Einschränkungen](https://support.google.com/displayvideo/answer/9539301).

## Bearbeiten einer Zielgruppe &quot;Kundenabgleich&quot;mithilfe einer Kundendatenliste

Mit Ausnahme von [!DNL Google Ads] Zielgruppen, die aus einer [!DNL Adobe] -Zielgruppe erstellt wurden, können Sie eine beliebige [!DNL Google Ads] - oder [!DNL Microsoft Advertising] Kundenübereinstimmungszielgruppe aktualisieren. Sie können Daten hochladen, um alle vorhandenen Daten für die Audience hinzuzufügen, zu löschen oder zu ersetzen.

Die Daten müssen vom ursprünglichen Typ der Kundenliste sein (E-Mail-Adressen, Postanschriften, Telefonnummern, Benutzer-IDs oder Mobilgeräte-IDs für eine bestimmte App unter einem bestimmten mobilen Betriebssystem).

1. Erstellen Sie eine Datei mit den Kundendaten im erforderlichen Format für den vorhandenen Datentyp.

Vor- und Nachnamen, E-Mail-Adressen und Telefonnummern müssen mit dem SHA-256-Algorithmus gehasht werden. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Für [!DNL Google Ads] -Zielgruppen finden Sie in der [!DNL Google Ads] Dokumentation zu &quot;[Formatierungsrichtlinien für das Hochladen von Hash-Daten](https://support.google.com/google-ads/answer/7476159)&quot; eine Liste der zulässigen Kontaktdatenfelder und -anforderungen. Informationen zu [!DNL Microsoft Advertising] -Zielgruppen finden Sie in der [!DNL Microsoft Advertising] Dokumentation zu [ Vorbereitung von Kundenübereinstimmungslisten](https://help.ads.microsoft.com/#apex/ads/en/56921). Sie können optional eine [!DNL Microsoft Excel] -Vorlage für Kontaktinformationen herunterladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Aktivieren Sie das Kontrollkästchen neben der zu bearbeitenden Audience.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png).

1. Wählen Sie die folgende Aktion aus: *[!UICONTROL Add]* (zum Hinzufügen der hochgeladenen Daten zu den vorhandenen Daten, sofern sie nicht bereits vorhanden sind), *[!UICONTROL Delete]* (zum Löschen der hochgeladenen Daten, falls sie bereits existieren) oder *[!UICONTROL Replace]* (zum Löschen aller vorhandenen Daten und zum Ersetzen durch die hochgeladenen Daten).

1. Laden Sie die Datei hoch:

   1. Klicken Sie im Feld [!UICONTROL Select File] auf **[!UICONTROL Choose File]** und wählen Sie die Datei in Ihrem Netzwerk oder Gerät aus.

   1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie den Bedingungen der Datenschutzrichtlinien für [!DNL Adobe] und Werbenetzwerke zustimmen.

   1. Klicken Sie auf **[!UICONTROL Upload File]**.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>Die Verarbeitung von Aktualisierungen an einer Audience im Werbenetzwerk kann einige Zeit dauern.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] von Kundenabgleichs-Zielgruppen aus  [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Erstellen einer [!DNL Google Ads] Kundenübereinstimmungs-Audience aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Dynamische Remarketing-Zielgruppen verwalten](audience-dynamic-remarketing-manage.md)
