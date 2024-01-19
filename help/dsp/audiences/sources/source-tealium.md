---
title: Workflow für die Verwendung der DSP Integration mit [!DNL Tealium]
description: Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL Tealium] Erstanbietersegmente.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Workflow für die Verwendung der DSP Integration mit [!DNL Tealium]

Sie können die Erstanbieterdaten Ihrer Organisation über die [!DNL Tealium] Kundendatenplattform mit [!DNL Amazon Web Services] (AWS)-Feuerschlauch-Connector. Es gibt vier Schritte zum Freigeben von Daten aus Tealium für DSP:

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. [Vorbereiten und Freigeben von Daten zur Segmentzuordnung](#map-data).

1. [Erstellen von Connectoren in [!DNL Tealium] Freigeben von Segmentdaten](#tealium-connector).

1. [Duplizieren Sie den vorhandenen Connector in [!DNL Tealium] weiterhin Segmente freigeben](#duplicate-connector).

## Schritt 1: Erstellen einer Zielgruppenquelle in DSP {#source-create}

* [Erstellen einer Zielgruppenquelle](source-create.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren und den Quell-Code-Schlüssel für die [!DNL Tealium] Benutzer.

## Schritt 2: Vorbereiten und Freigeben von Segmentzuordnungsdaten {#map-data}

1. Der Advertiser muss Daten zur Segmentzuordnung vorbereiten und freigeben:

   1. Der Werbetreibende muss die Daten in [!DNL Tealium]:

      1. Die E-Mail-IDs für die Audience des Advertisers müssen mit dem SHA-256-Algorithmus gehasht werden.

      1. Die Spalte mit Hash-E-Mail-IDs muss dem Attribut des Typs Besucher-ID zugeordnet sein.

      1. Die Audience muss mit der `Tealium_visitor_id` -Attribut. Die richtige Anreicherung muss auf den Trigger der Audience angewendet werden. Siehe [[!DNL Tealium] Dokumentation zu Besucherkennungsattributen](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. Der Werbetreibende muss dem Adobe Account Team Daten zur Segmentzuordnung zur Verfügung stellen, damit die Segmente in DSP erstellt werden können. Verwenden Sie die folgenden Spaltennamen und -werte in einer Datei mit kommagetrennten Werten:

      * **Externer Segmentschlüssel:** Der externe Segmentschlüssel, den Sie später in den Aktionseinstellungen für den Connector in [!DNL Tealium]. Die empfohlene Benennungskonvention lautet &quot;`<DSP source key>_<Tealium segment name>`,&quot;z. B. &quot;57bf424dc10_ffee-drinkers&quot;.

      * **Segmentname:** Der Segmentname.

      * **Segmentbeschreibung:** Der Zweck oder die Regel des Segments oder beides.

      * **Übergeordnete ID:** Leer lassen

      * **Video-CPM:** 0

      * **CPM anzeigen:** 0

      * **Segmentfenster:** Die Gültigkeitsdauer des Segments.

## Schritt 3: Erstellen von Connectoren in [!DNL Tealium] Freigeben von Segmentdaten {#tealium-connector}

Erstellen Sie für jedes Segment, das Sie freigeben möchten, einen separaten Connector für jede Aktion, bei der sich die Daten von Trigger ändern. Um beispielsweise zwei Segmente mit jeweils zwei Triggern freizugeben, erstellen Sie vier Connectoren.

1. Das Adobe Account-Team stellt dem Advertiser die Anmeldeinformationen des AWS-Feuerschlauch-Connectors zur Verfügung.

1. In [!DNL Tealium], [Connector hinzufügen](https://docs.tealium.com/server-side/connectors/add/), unter Verwendung der folgenden Optionen:

   1. Wählen Sie die [!DNL AWS Firehose] Connector.

   1. In den Quelleinstellungen:

      1. Wählen Sie das freizugebende Zielgruppensegment aus.

      1. Richten Sie einen Trigger ein:

         * Wählen Sie für den ersten Connector für das Segment den Trigger aus. `Joined Audience`. Dadurch wird sichergestellt, dass Daten für DSP freigegeben werden, sobald ein Benutzer einem Segment beitritt.

         * Wählen Sie für den zweiten Connector für das Segment den Trigger aus. `Left Audience`. Dieser Connector wird verwendet, um alle Opt-outs und Benutzer zu verarbeiten, die das Segment in DSP verlassen.

   1. Geben Sie in den Konfigurationseinstellungen den AWS-Feuerschlauch-Connector an. Wenn Sie den Feuerlöschschlauch-Connector noch nicht für DSP hinzugefügt haben, fügen Sie mithilfe der folgenden Informationen einen Feuerlöschschlauch-Connector hinzu:

      * **Name:** Der Name des Connectors.

      * **Zugriffsschlüssel:** Der vom Adobe Account Team bereitgestellte Zugriffsschlüssel.

      * **Geheimer Schlüssel:** Der vom Adobe Account Team bereitgestellte geheime Schlüssel.

      * **Region:** USA, Nordvirginia (us-east-1)

   1. Führen Sie in den Aktionseinstellungen die folgenden Schritte aus:

      1. Erstellen Sie die Aktion &quot;Senden von Kundendaten an Bereitstellungs-Stream (Erweitert)&quot;, um dem Segment Daten hinzuzufügen. Verwenden Sie dazu die folgenden Informationen:

         * **Aktionsname:** Der Name der Aktion.

         * **Aktionstyp:** Senden von Kundendaten an Bereitstellungs-Stream (erweitert)

         * **Versandstream:** Tealium_CDP_Connector

         * **Nachrichtendaten:**  Gehen Sie wie folgt vor:

            1. Wählen Sie ein Attribut für das Segment aus:

               * Nennen Sie die benutzerdefinierte Nachricht für das Attribut Hashed_Email . `hashed_email`.

               * Geben Sie für das Attribut Cookies einen Namen für die benutzerdefinierte Nachricht ein. `cookies`.

            1. In der Option zum Erstellen eines benutzerdefinierten Felds finden Sie im [!DNL Source Key] und geben Sie die [!UICONTROL External Segment Key] , die in den Segmentzuordnungsdaten in [Schritt 2](#map-data).

               DSP verwendet diesen Schlüssel zum Ausfüllen Ihres Segments.

            1. (Empfohlen) Erstellen Sie eine Aktualisierungsaktion, um das Segment zu aktualisieren.

## Schritt 4: Duplizieren Sie den vorhandenen Connector in [!DNL Tealium] weiterhin Segmente freigeben {#duplicate-connector}

Pro Segment können Sie nur einen Connector und pro Connector ein Segment haben.

1. In [!DNL Tealium], duplizieren Sie das Segment, für das Sie ein anderes Segment erstellen möchten, und benennen Sie das neue Segment um.

1. In [!DNL Tealium], duplizieren Sie den Connector, den Sie in erstellt haben. [Schritt 3](#tealium-connector)und benennen Sie den neuen Connector aus um.`<original name>-copy`&quot; auf den neuen Segmentnamen.

>[!MORELIKETHIS]
>
>* [Informationen zum Aktivieren authentifizierter Segmente aus Zielgruppen-Quellen](/help/dsp/audiences/sources/source-about.md)
>* [Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen](source-create.md)
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Workflow für die Verwendung der DSP Integration mit [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
