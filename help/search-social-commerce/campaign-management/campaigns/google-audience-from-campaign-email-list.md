---
title: Erstellen einer  [!DNL Google Ads] -Zielgruppe aus einer Adobe Campaign-E-Mail-Liste
description: Erfahren Sie, wie Sie aus  [!DNL Google Ads]  bestehenden Adobe Campaign-E-Mail-Liste eine Zielgruppe für den Kundenabgleich erstellen.
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# Erstellen einer [!DNL Google Ads] Zielgruppe für den Kundenabgleich über eine Adobe Campaign-E-Mail-Liste

*[!DNL Google Ads]Konten, die nur für den Kundenabgleich infrage kommen*

Sie können in Adobe Campaign eine [!DNL Google Ads] Zielgruppe für den Kundenabgleich aus einer E-Mail-Liste erstellen, indem Sie in [!DNL Campaign] einen Konto-Link und einen Workflow einrichten.

Dazu benötigen Sie Zugriff auf Ihre [!DNL Campaign]-Instanz und eine XML-Datei mit dem erforderlichen Workflow, den Ihr Adobe-Account-Team Ihnen zur Verfügung stellt. Die Anweisungen können für verschiedene Versionen von [!DNL Campaign] variieren. Bei Bedarf kann Ihr Adobe-Account-Team Sie beim Einrichten des Workflows in [!DNL Campaign] unterstützen.

1. Erhalten Sie Anmeldedaten für ein von Advertising Search, Social und Commerce bereitgestelltes SFTP-Konto.

1. Richten Sie [!DNL Campaign] den Versand der E-Mail-Liste an Advertising Search, Social und Commerce ein:

   1. Erstellen Sie ein [externes Konto](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html?lang=de) um Ihr über Search, Social und Commerce bereitgestelltes SFTP-Konto zu verknüpfen:

      1. Navigieren Sie im linken Menü zu **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Klicken Sie ![Konto erstellen](/help/search-social-commerce/assets/campaign-create-account.png "Konto erstellen").

      1. Geben Sie einen Titel für das Konto ein und wählen Sie **[!UICONTROL SFTP]** als Kontotyp aus.

      1. Geben Sie die URL und Port-Nummer für den [!DNL Adobe] SFTP-Server sowie den Ordnernamen, den Benutzernamen und das Kennwort des Werbetreibenden ein.

      1. Klicken Sie auf **[!UICONTROL Save]**.

   1. Installieren Sie in [!DNL Campaign Client] das Datenpaket, das den zum Senden von E-Mail-Daten erforderlichen Workflow enthält:

      1. Wechseln Sie in der Menüleiste zu **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Wählen Sie **[!UICONTROL Install a package from a file]** aus und klicken Sie dann auf **[!UICONTROL Next]**.

      1. Suchen Sie die Datenpaketdatei (`AMO_Workflow.xml`) auf dem Gerät oder Netzwerk, und klicken Sie dann auf **[!UICONTROL Next]**.

      1. Klicken Sie auf **[!UICONTROL Start]** und warten Sie, bis der Workflow installiert ist.

   1. Bearbeiten Sie den installierten Workflow, um optional die Filter für die Datenabfrage zu bearbeiten und den neuen Zielgruppennamen und das externe SFTP-Konto zu identifizieren:

      1. Wechseln Sie zu **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** und öffnen Sie das Paket.

      1. (Optional) Bearbeiten Sie einen der Filter für die Daten:

         * Doppelklicken Sie im Workflow auf die Abfrageaktivität (z. B. ForkTransition 1).

         * Bearbeiten Sie die Filterausdrücke.

         * Klicken Sie auf **[!UICONTROL Finish]**.

      1. Segment benennen:

         * Doppelklicken Sie im Workflow auf die **[!UICONTROL Data extraction (File)]**.

         * Geben Sie auf der Registerkarte **[!UICONTROL Data extraction (File)]** im Feld **[!UICONTROL File name]** den Segmentnamen mit der Erweiterung &quot;`.added`&quot; ein (z. B. PaidSubscribers.added).

           Der Segmentname darf noch nicht vorhanden sein. Beim Segmentnamen wird zwischen Groß- und Kleinschreibung unterschieden. Er muss aus ASCII-Zeichen bestehen, darf jedoch keine Unterstriche (`_`) enthalten.

           Wenn Sie das Segment jedoch zu einem bestimmten [!DNL Google Ad]-Konto hinzufügen möchten, hängen Sie den Segmentnamen mit einem Unterstrich und der [!UICONTROL User SE Account ID] (die ID von Search, Social und Commerce für das [!DNL Google Ads]-Konto und nicht die Konto-ID des Netzwerks) an:

           `_<User SE Account ID>`

           Beispiel: Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >Dies ist eine Ausnahme von der Regel, die Unterstriche im Dateinamen verbietet.

           Andernfalls wird das Segment zu allen [!DNL Google Ads] hinzugefügt, die Search, Social und Commerce für den Advertiser synchronisieren.

         * Lassen Sie die Option ausgewählt **[!UICONTROL Generate an outbound transition]**.

         * Klicken Sie auf **[!UICONTROL Ok]**.

      1. Geben Sie das externe Konto an, an das die Daten gesendet werden sollen:

         * Doppelklicken Sie im Workflow auf die **[!UICONTROL File Transfer]**.

         * Wählen Sie auf der Registerkarte **[!UICONTROL File Transfer]** im Abschnitt **[!UICONTROL Remote server]** die zu **[!UICONTROL Use an external account]** Option aus.

         * Wählen Sie im Feld **[!UICONTROL External account]** den Titel für das externe Konto aus, das Sie in Schritt 2 erstellt haben.

         * Wählen Sie im Feld **[!UICONTROL Server folder]** den Wert für das Feld [!UICONTROL Account] für das externe Konto aus.

         * (Optional) Geben Sie auf der Registerkarte **[!UICONTROL Schedule]** einen anderen Zeitplan für die Dateiübertragung an.

           Standardmäßig wird der Workflow um 0:00 Uhr (Mitternacht) ausgeführt, wodurch sichergestellt wird, dass alle Datensätze verarbeitet werden. Um die Latenz zu minimieren, planen Sie die Ausführung des Workflows bis spätestens 18:00 Uhr.

         * Klicken Sie auf **[!UICONTROL Ok]**.

Search, Social und Commerce überprüft das Verzeichnis alle 30 Minuten (um NN:30 und NN:59 in der Zeitzone des Werbetreibenden) und verschiebt alle gefundenen Dateien an einen anderen Speicherort. Anschließend erstellt er automatisch eine Zielgruppe aus den Daten und pusht sie um 22:00 Uhr (22:00 Uhr) an Google. Search, Social und Commerce sucht weiterhin alle 30 Minuten nach Updates (Ergänzungen und Subtraktionen) in der E-Mail-Liste und aktualisiert die Audience auf [!DNL Google Ads] entsprechend täglich um 22:00 Uhr.

>[!NOTE]
>
>* Wenn Sie zwischen den Verarbeitungszyklen mehr als eine Version einer Datei hochladen, wird die neueste Datei verwendet.
>
>* Search, Social und Commerce speichert keine Kundendaten aus Ihren E-Mail-Listen, die zum Erstellen oder Bearbeiten einer [!DNL Google Ads] Zielgruppe verwendet werden.
>
>* [!DNL Google Ads] kann eine Weile dauern, bis Aktualisierungen für eine Zielgruppe verarbeitet sind.
>
>* Siehe [[!DNL Google Ads] Dokumentation zur Funktionsweise von Customer Match und zu Einschränkungen](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Info über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] Kundenabgleich von Zielgruppen aus [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Verwalten von Zielgruppen für den Kundenabgleich mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
>* [Dynamische Remarketing-Audiences verwalten](audience-dynamic-remarketing-manage.md)
