---
title: Erstellen einer [!DNL Google Ads] Kundenabgleichzielgruppe aus einer Adobe Campaign-E-Mail-Liste
description: Erfahren Sie, wie Sie aus einer vorhandenen Adobe Campaign-E-Mail-Liste eine Audience für die Übereinstimmung von Kunden erstellen. [!DNL Google Ads]
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# Erstellen einer [!DNL Google Ads]-Kundenabgleichzielgruppe aus einer Adobe Campaign-E-Mail-Liste

*[!DNL Google Ads]Konten, die nur für eine Kundenübereinstimmung infrage kommen*

Sie können aus einer E-Mail-Liste in Adobe Campaign eine Zielgruppe für die Übereinstimmung mit [!DNL Google Ads] Kunden erstellen, indem Sie einen Kontolink und einen Workflow in [!DNL Campaign] einrichten.

Dazu benötigen Sie Zugriff auf Ihre [!DNL Campaign] -Instanz und eine XML-Datei, die den erforderlichen Workflow enthält, den Ihnen Ihr Adobe Account-Team zur Verfügung stellt. Die Anweisungen können für verschiedene Versionen von [!DNL Campaign] variieren. Bei Bedarf kann Ihr Adobe Account Team Ihnen bei der Einrichtung des Workflows in [!DNL Campaign] helfen.

1. Erhalten Sie Anmeldeinformationen für ein von Advertising Search, Social und Commerce bereitgestelltes SFTP-Konto.

1. Richten Sie in [!DNL Campaign] den Versand der E-Mail-Liste an Advertising Search, Social und Commerce ein:

   1. Erstellen Sie ein [externes Konto](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html), um Ihr von Search, Social und Commerce bereitgestelltes SFTP-Konto zu verknüpfen:

      1. Gehen Sie im linken Menü zu **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Klicken Sie auf ![Konto erstellen](/help/search-social-commerce/assets/campaign-create-account.png "Konto erstellen").

      1. Geben Sie einen Titel für das Konto ein und wählen Sie **[!UICONTROL SFTP]** als Kontotyp aus.

      1. Geben Sie die URL und Portnummer für den SFTP-Server [!DNL Adobe] sowie den Ordnernamen, den Benutzernamen und das Kennwort des Advertisers ein.

      1. Klicken Sie auf **[!UICONTROL Save]**.

   1. Installieren Sie in [!DNL Campaign Client] das Datenpaket, das den zum Senden von E-Mail-Daten erforderlichen Workflow enthält:

      1. Gehen Sie in der Menüleiste zu **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Wählen Sie **[!UICONTROL Install a package from a file]** und klicken Sie dann auf **[!UICONTROL Next]**.

      1. Suchen Sie die Datenpaketdatei (`AMO_Workflow.xml`) auf dem Gerät oder im Netzwerk und klicken Sie auf **[!UICONTROL Next]**.

      1. Klicken Sie auf **[!UICONTROL Start]** und warten Sie, bis der Workflow installiert ist.

   1. Bearbeiten Sie den installierten Workflow, um optional die Filter für die Datenabfrage zu bearbeiten und den neuen Zielgruppennamen und das externe SFTP-Konto zu identifizieren:

      1. Gehen Sie zu **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** und öffnen Sie das Paket.

      1. (Optional) Bearbeiten Sie einen der Filter für die Daten:

         * Doppelklicken Sie im Workflow auf die Abfrageaktivität (z. B. ForkTransition 1).

         * Bearbeiten Sie die Filterausdrücke.

         * Klicken Sie auf **[!UICONTROL Finish]**.

      1. Benennen Sie das Segment:

         * Doppelklicken Sie im Workflow auf die Aktivität **[!UICONTROL Data extraction (File)]**.

         * Geben Sie auf der Registerkarte **[!UICONTROL Data extraction (File)]** im Feld **[!UICONTROL File name]** den Segmentnamen mit der Erweiterung &quot;`.added`&quot; ein (z. B. PaidSubscribers.added).

           Der Segmentname darf nicht bereits vorhanden sein. Beim Segmentnamen wird zwischen Groß- und Kleinschreibung unterschieden. Er muss aus ASCII-Zeichen bestehen, darf jedoch keine Unterstriche (`_`) enthalten.

           Wenn Sie das Segment jedoch einem bestimmten [!DNL Google Ad] -Konto hinzufügen möchten, hängen Sie den Segmentnamen mit einem Unterstrich und die [!UICONTROL User SE Account ID] an (Such-, Social- und Commerce-ID für das [!DNL Google Ads] -Konto, nicht die Konto-ID des Netzwerks):

           `_<User SE Account ID>`

           Beispiel: Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >Dies ist eine Ausnahme von der Regel, die Unterstriche im Dateinamen verbietet.

           Andernfalls wird das Segment zu allen [!DNL Google Ads] -Konten hinzugefügt, die von Search, Social und Commerce für den Advertiser synchronisiert werden.

         * Belassen Sie die Option auf &quot;**[!UICONTROL Generate an outbound transition]**&quot;.

         * Klicken Sie auf **[!UICONTROL Ok]**.

      1. Geben Sie das externe Konto an, an das die Daten gesendet werden sollen:

         * Doppelklicken Sie im Workflow auf die Aktivität **[!UICONTROL File Transfer]**.

         * Wählen Sie auf der Registerkarte **[!UICONTROL File Transfer]** im Abschnitt **[!UICONTROL Remote server]** die Option zu **[!UICONTROL Use an external account]** aus.

         * Wählen Sie im Feld **[!UICONTROL External account]** die Bezeichnung für das externe Konto aus, das Sie in Schritt 2 erstellt haben.

         * Wählen Sie im Feld **[!UICONTROL Server folder]** den Wert für das Feld [!UICONTROL Account] für das externe Konto aus.

         * (Optional) Geben Sie auf der Registerkarte **[!UICONTROL Schedule]** einen anderen Zeitplan für die Dateiübertragung an.

           Standardmäßig wird der Workflow um 00:00 Uhr (Mitternacht) ausgeführt, wodurch sichergestellt wird, dass alle Datensätze verarbeitet werden. Um Latenzzeiten zu minimieren, planen Sie die Ausführung des Workflows bis spätestens 18:00 Uhr.

         * Klicken Sie auf **[!UICONTROL Ok]**.

Search, Social und Commerce überprüfen das Verzeichnis alle 30 Minuten (um NN:30 und NN:59 in der Zeitzone des Advertisers) und verschieben alle Dateien an einen anderen Speicherort. Anschließend erstellt sie automatisch eine Zielgruppe aus den Daten und sendet sie um 22:00 Uhr (22:00 Uhr) an Google. Search, Social und Commerce suchen weiterhin alle 30 Minuten nach Aktualisierungen (Ergänzungen und Abzüge) der E-Mail-Liste und aktualisieren die Zielgruppe auf [!DNL Google Ads] um 22:00 Uhr.

>[!NOTE]
>
>* Wenn Sie zwischen den Verarbeitungszyklen mehr als eine Version einer Datei hochladen, wird die neueste Datei verwendet.
>
>* In Search, Social und Commerce werden keine Kundendaten aus Ihren E-Mail-Listen gespeichert, die zum Erstellen oder Bearbeiten einer [!DNL Google Ads] -Zielgruppe verwendet werden.
>
>* [!DNL Google Ads] kann eine Weile dauern, bis Aktualisierungen an einer Zielgruppe verarbeitet werden.
>
>* Siehe die [[!DNL Google Ads] Dokumentation zur Funktionsweise der Kundenabgleich und zu Einschränkungen](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] von Kundenabgleichs-Zielgruppen aus  [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Verwalten von Zielgruppen zur Kundenabstimmung mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
>* [Dynamische Remarketing-Zielgruppen verwalten](audience-dynamic-remarketing-manage.md)
