---
title: Hochladen von Offline-Kontodaten für Berichte und Simulationen
description: Erfahren Sie, wie Sie Offline-Kontodaten manuell oder in einen [!DNL Amazon] [!DNL S3]-Bucket hochladen können, um Reporting- und Simulationsunterstützung zu erhalten. Protokolldateien verfolgen den Fortschritt von Upload-Aufträgen.
source-git-commit: 8ba0f8fa6050a3e6ec93bcf08df2c0204191fc02
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Hochladen von Offline-Kontodaten für Berichte und Simulationen

*Werbetreibende, die für das Hochladen von Kontodaten aktiviert sind*

Hochladen von Kampagneninhalten und Offline-Kosten-, Klick- und Konversionsdaten für ein Konto ohne API-Unterstützung für Reporting- und Leistungssimulationen.

Sie können den Fortschritt Ihrer Upload-Aufträge mithilfe der [!UICONTROL Upload Logs]-Funktion verfolgen:

* Zeigt eine Liste aller für das Konto hochgeladenen Dateien an. Zu den Informationen über jeden Datei-Upload-Auftrag gehören der Dateiname, der Upload-Kanal (*[!UICONTROL Cloud Storage]* oder *[!UICONTROL Drag & Drop]*), das Synchronisierungsdatum und der Status sowie die Gründe für unvollständige Uploads.

* Laden Sie eine Datei mit den Kontoentitäten und zugehörigen Metriken herunter, die für einen beliebigen Auftrag hochgeladen wurden. Die Dateien befinden sich im CSV-Format (Kommagetrennte Werte).

## Kontodaten manuell hochladen

Sie können ein Konto mit Kampagneninhalten und Kosten-, Klick- und Konversionsdaten füllen, indem Sie die Daten manuell in eine Datei hochladen.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Aus der [!UICONTROL Accounts]):

      1. Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Upload]** .

      1. Ziehen Sie entweder eine Datei in das Feld oder klicken Sie auf **[!UICONTROL Browse Files]** und wählen Sie eine Datei von Ihrem Gerät oder Netzwerk aus.

      1. Klicken Sie auf **[!UICONTROL Upload Files]**.

   * (Aus den Kontoeinstellungen):

      1. Wählen Sie das Konto auf eine der folgenden Arten aus:

         * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

         * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

      1. Klicken Sie auf die Registerkarte **[!UICONTROL Upload File]** .

      1. Ziehen Sie entweder eine Datei in das Feld oder klicken Sie auf **[!UICONTROL Browse Files]** und wählen Sie eine Datei von Ihrem Gerät oder Netzwerk aus.

      1. Klicken Sie auf **[!UICONTROL Save]**.

## Hochladen von Kontodaten in einen [!DNL Amazon] [!DNL S3] Bucket {#data-upload-s3}

Sie können ein Konto mit Kampagneninhalten und Kosten-, Klick- und Konversionsdaten füllen, indem Sie die Daten in einen Ordner „Suche“, „Social“ und &quot;Commerce&quot; in einem [!DNL Amazon Web Services] ([!DNL Simple Storage Service]) des Typs [!DNL S3] (AWS) hochladen.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Wenden Sie sich an Ihr Adobe-Accountteam , um das Hochladen von Account-Daten für Ihr Search-, Social- und Commerce Advertiser-Konto zu aktivieren. Das Team erleichtert die Erstellung eines organisationsspezifischen Ordners in einem [!DNL S3] Behälter und teilt Ihnen mit, wann er abgeschlossen ist.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* Rufen Sie den [!DNL S3] Cloud-Speicherpfad, die Zugriffsschlüssel-ID und den geheimen Zugriffsschlüssel für Ihr Konto ab. Für alle Datenupload-<!-- naming convention?-->-Konten des Unternehmens werden dieselbe Zugriffsschlüssel-ID und derselbe geheime Zugriffsschlüssel verwendet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Aus der [!UICONTROL Accounts]):

      1. Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Upload]** .

      1. Klicken Sie im [!UICONTROL Cloud Storage Link] auf **[!UICONTROL Go to the Link]**.

      1. Klicken Sie auf **[!UICONTROL Show Access Key and Secret]**.

      1. Klicken Sie neben dem Feld [!UICONTROL Storage Link] auf **[!UICONTROL Copy]** , um den Link in die Zwischenablage zu kopieren und an einem sicheren Ort zu speichern.

      1. Kopieren Sie auf ähnliche Weise die [!UICONTROL Access Key] und die [!UICONTROL Secret Key] Werte und speichern Sie sie sicher.

      1. Klicken Sie auf **[!UICONTROL Done]**.

   * (Aus den Kontoeinstellungen):

      1. Wählen Sie das Konto auf eine der folgenden Arten aus:

         * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

         * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

      1. Klicken Sie auf die Registerkarte **[!UICONTROL Upload File]** .

      1. Klicken Sie im [!UICONTROL Cloud Storage Link] auf **[!UICONTROL Go to the Link]**.

      1. Klicken Sie auf **[!UICONTROL Show Access Key and Secret]**.

      1. Klicken Sie neben dem Feld [!UICONTROL Storage Link] auf **[!UICONTROL Copy]** , um den Link in die Zwischenablage zu kopieren und an einem sicheren Ort zu speichern.

      1. Kopieren Sie auf ähnliche Weise die [!UICONTROL Access Key] und die [!UICONTROL Secret Key] Werte und speichern Sie sie sicher.

      1. Klicken Sie auf **[!UICONTROL Done]**.

      1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Einmal pro Organisation) Richten Sie Ihre lokale AWS-Umgebung ein:

   1. Laden Sie [!DNL AWS Command Line Interface] (AWS CLI) vom folgenden Speicherort herunter und installieren Sie es: [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Konfigurieren Sie Ihre AWS-Anmeldedaten:

      1. Erstellen Sie eine Nur-Text-Datei und benennen Sie sie `~/.aws/credentials` (ohne Dateierweiterung).

      1. Öffnen Sie die Datei in einem Texteditor und geben Sie die Zugriffsschlüssel-ID und den geheimen Zugriffsschlüssel des Unternehmens wie folgt ein:

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Laden Sie Ihren Kontodatenbericht aus dem Anzeigennetzwerk herunter und speichern Sie ihn.

1. Führen Sie in der AWS-CLI den folgenden Befehl aus, um Ihre Kontodaten in Ihren [!DNL S3] Cloud-Speicherort hochzuladen.

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Beispiel: `aws s3 cp filename.txt s3://cloud-location/`

## Protokoll der hochgeladenen Kontodatendateien anzeigen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Upload Logs]**.

1. (Optional) Um die Daten für eine hochgeladene Datei herunterzuladen, klicken Sie in der ![&#x200B; Spalte auf &#x200B;](/help/search-social-commerce/assets/download.png "Herunterladen")Herunterladen[!UICONTROL Download] und laden Sie die Datei entsprechend dem normalen Verfahren Ihres Browsers herunter.

## Erforderliche Daten

Die Daten müssen den Datenanforderungen für das Werbenetzwerk entsprechen. Die Datenfelder für jede Entität können je nach Anzeigennetzwerk variieren.
