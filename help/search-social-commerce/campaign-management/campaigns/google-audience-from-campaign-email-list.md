---
title: Erstellen Sie eine [!DNL Google Ads] Zielgruppe für Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste
description: Erfahren Sie, wie Sie eine [!DNL Google Ads] Kundenabgleich-Zielgruppe aus einer vorhandenen Adobe Campaign-E-Mail-Liste.
exl-id: 967580fc-52c3-42f5-8d60-18cb83bc714a
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Erstellen Sie eine [!DNL Google Ads] Zielgruppe für Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste

*[!DNL Google Ads]Konten, die nur für die Kundenübereinstimmung infrage kommen*

Sie können eine [!DNL Google Ads] Zielgruppe zum Kundenabgleich aus einer E-Mail-Liste in Adobe Campaign durch Einrichtung eines Kontolinks und eines Workflows in [!DNL Campaign].

Dazu benötigen Sie Zugriff auf Ihre [!DNL Campaign] -Instanz und einer XML-Datei, die den erforderlichen Workflow enthält, den Ihnen Ihr Adobe Account Team zur Verfügung stellt. Die Anweisungen können für verschiedene Versionen von [!DNL Campaign]. Bei Bedarf kann Ihr Adobe Account Team Sie bei der Einrichtung des Workflows in [!DNL Campaign].

1. Erhalten Sie Anmeldeinformationen für ein von Advertising Search, Social und Commerce bereitgestelltes SFTP-Konto.

1. In [!DNL Campaign], richten Sie den Versand der E-Mail-Liste an Advertising Search, Social und Commerce ein:

   1. Erstellen Sie eine [externes Konto](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) , um Ihr von Search, Social und Commerce bereitgestelltes SFTP-Konto zu verknüpfen:

      1. Gehen Sie im linken Menü zu **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Klicks ![Konto erstellen](/help/search-social-commerce/assets/campaign-create-account.png "Konto erstellen").

      1. Benennen Sie das Konto und wählen Sie **[!UICONTROL SFTP]** als Kontotyp.

      1. Geben Sie die URL und die Portnummer für die [!DNL Adobe] SFTP-Server und Ordnername, Benutzername und Kennwort des Advertisers.

      1. Klicken **[!UICONTROL Save]**.

   1. In [!DNL Campaign Client]installieren Sie das Datenpaket, das den für das Senden von E-Mail-Daten erforderlichen Workflow enthält:

      1. Navigieren Sie in der Menüleiste zu **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Auswählen **[!UICONTROL Install a package from a file]** und klicken Sie anschließend auf **[!UICONTROL Next]**.

      1. Suchen Sie die Datenpaketdatei (`AMO_Workflow.xml`) auf dem Gerät oder im Netzwerk und klicken Sie dann auf **[!UICONTROL Next]**.

      1. Klicks **[!UICONTROL Start]** und warten Sie, bis der Workflow installiert ist.

   1. Bearbeiten Sie den installierten Workflow, um optional die Filter für die Datenabfrage zu bearbeiten und den neuen Zielgruppennamen und das externe SFTP-Konto zu identifizieren:

      1. Navigieren Sie zu **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** und öffnen Sie das Paket.

      1. (Optional) Bearbeiten Sie einen der Filter für die Daten:

         * Doppelklicken Sie im Workflow auf die Abfrageaktivität (z. B. ForkTransition 1).

         * Bearbeiten Sie die Filterausdrücke.

         * Klicken **[!UICONTROL Finish]**.

      1. Benennen Sie das Segment:

         * Doppelklicken Sie im Workflow auf die Aktivität **[!UICONTROL Data extraction (File)]**.

         * Auf **[!UICONTROL Data extraction (File)]** in der **[!UICONTROL File name]** Geben Sie den Segmentnamen mit der Erweiterung ein.`.added`&quot;(z. B. PaidSubscribers.added).

           Der Segmentname darf nicht bereits vorhanden sein. Beim Segmentnamen wird zwischen Groß- und Kleinschreibung unterschieden. Er muss aus ASCII-Zeichen bestehen, darf jedoch keine Unterstriche (`_`).

           Wenn Sie das Segment jedoch zu einem bestimmten [!DNL Google Ad] -Konto ein, fügen Sie dann den Segmentnamen mit einem Unterstrich und dem [!UICONTROL User SE Account ID] (Suchen, Social und Commerce-ID für die [!DNL Google Ads] -Konto, nicht die Konto-ID des Netzwerks):

           `_<User SE Account ID>`

           Beispiel: Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >Dies ist eine Ausnahme von der Regel, die Unterstriche im Dateinamen verbietet.

           Andernfalls wird das Segment zu allen [!DNL Google Ads] Konten, die von Search, Social und Commerce für den Advertiser synchronisiert werden.

         * Belassen Sie die Option auf **[!UICONTROL Generate an outbound transition]** ausgewählt ist.

         * Klicken **[!UICONTROL Ok]**.

      1. Geben Sie das externe Konto an, an das die Daten gesendet werden sollen:

         * Doppelklicken Sie im Workflow auf die Aktivität **[!UICONTROL File Transfer]**.

         * Auf **[!UICONTROL File Transfer]** in der **[!UICONTROL Remote server]** -Abschnitt, wählen Sie die Option **[!UICONTROL Use an external account]**.

         * Im **[!UICONTROL External account]** den Titel für das externe Konto, das Sie in Schritt 2 erstellt haben.

         * Im **[!UICONTROL Server folder]** ein, wählen Sie den Wert für [!UICONTROL Account] für das externe Konto.

         * (Optional) Auf der Registerkarte **[!UICONTROL Schedule]** einen anderen Zeitplan für die Dateiübertragung festlegen.

           Standardmäßig wird der Workflow um 00:00 Uhr (Mitternacht) ausgeführt, wodurch sichergestellt wird, dass alle Datensätze verarbeitet werden. Um Latenzzeiten zu minimieren, planen Sie die Ausführung des Workflows bis spätestens 18:00 Uhr.

         * Klicken **[!UICONTROL Ok]**.

Search, Social und Commerce überprüft das Verzeichnis alle 30 Minuten (um NN:30 und NN:59 in der Zeitzone des Werbetreibenden) und verschiebt alle Dateien an einen anderen Speicherort. Anschließend erstellt er automatisch eine Zielgruppe aus den Daten und sendet sie um 22:00 Uhr (22:00 Uhr) an Google. Search, Social und Commerce suchen weiterhin alle 30 Minuten nach Aktualisierungen (Ergänzungen und Subtraktionen) der E-Mail-Liste und aktualisieren die Zielgruppe auf [!DNL Google Ads] entsprechend um 22:00 Uhr täglich.

>[!NOTE]
>
>* Wenn Sie zwischen den Verarbeitungszyklen mehr als eine Version einer Datei hochladen, wird die neueste Datei verwendet.
>
>* Search, Social und Commerce speichert keine Kundendaten aus Ihren E-Mail-Listen, die zum Erstellen oder Bearbeiten einer [!DNL Google Ads] Zielgruppe.
>
>* [!DNL Google Ads] kann eine Weile dauern, bis Aktualisierungen an einer Zielgruppe verarbeitet werden.
>
>* Siehe [[!DNL Google Ads] Dokumentation zur Funktionsweise und Einschränkungen von Kundenabgleich](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] Kundenabgleich-Zielgruppen aus [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Verwalten von Zielgruppen zur Kundenabstimmung mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
>* [Dynamische Remarketing-Zielgruppen verwalten](audience-dynamic-remarketing-manage.md)
