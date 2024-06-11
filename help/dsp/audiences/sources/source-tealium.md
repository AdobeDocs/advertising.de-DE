---
title: Konvertieren von Benutzer-IDs aus [!DNL Tealium] zu universellen IDs
description: Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL Tealium] Erstanbietersegmente.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 2d045640b5bdf8dfba70d0f7da3ac012fd86e82e
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Tealium] zu universellen IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL Tealium] Kundendatenplattform , um die Erstanbieter-Hash-E-Mail-Adressen Ihrer Organisation in universelle IDs für zielgerichtete Werbung zu konvertieren. Der Prozess verwendet die [!DNL Amazon Web Services] (AWS)-Feuerschlauch-Connector. Führen Sie die folgenden Schritte aus, um Daten aus Tealium für DSP freizugeben:

1. (Konvertieren von E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Tracking einrichten, um [!DNL Analytics] messen](#analytics-tracking).

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. [Vorbereiten und Freigeben von Daten zur Segmentzuordnung](#map-data).

1. [Erstellen von Connectoren in [!DNL Tealium] Freigeben von Segmentdaten](#tealium-connector).

1. [Duplizieren Sie den vorhandenen Connector in [!DNL Tealium] weiterhin Segmente freigeben](#duplicate-connector).

1. [Anzahl der universellen IDs mit der Anzahl der gehashten E-Mail-Adressen vergleichen](#compare-id-count).

## Schritt 1: Tracking einrichten für [!DNL Analytics] messen {#analytics-tracking}

*Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Konvertieren von E-Mail-Adressen in [!DNL RampIDs] oder [!DNL ID5] IDs verwenden, müssen Sie Folgendes tun:

1. (Wenn Sie dies noch nicht getan haben) Führen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und stellen Sie sicher, dass die Variable [AMO-ID und EF ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs aufgefüllt werden.

1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie universellen ID-spezifischen Code auf Ihren Webseiten bereit, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) für Durchsichten zuzuordnen:

   * **Für [!DNL RampIDs]:** Sie müssen auf Ihren Webseiten ein zusätzliches JavaScript-Tag bereitstellen, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (jedoch nicht mobilen Apps) zu ermöglichen, sodass Durchsichten möglich sind. Wenden Sie sich an Ihr Adobe Account-Team, das Ihnen Anweisungen zur Registrierung für eine [!DNL LiveRamp] [!DNL LaunchPad] Tag aus [!DNL LiveRamp] Authentifizierungs-Traffic-Lösungen. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nachdem Sie sich registriert haben, generiert Ihr Adobe Account-Team ein eindeutiges Tag, das Ihr Unternehmen für die Implementierung auf Ihren Webseiten bereitstellen kann.

## Schritt 2: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen einer Zielgruppenquelle](source-manage.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren. Sie können Ihre Benutzer-IDs beliebig in [Verfügbare universelle ID-Formate](source-about.md).

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, mit dem Sie die Daten für die Segmentzuordnung vorbereiten.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für die [!DNL Tealium] Benutzer.

## Schritt 3: Vorbereiten und Freigeben von Segmentzuordnungsdaten {#map-data}

Der Advertiser muss Daten zur Segmentzuordnung vorbereiten und freigeben.

1. Der Werbetreibende muss die Daten in [!DNL Tealium]:

   1. Hash der E-Mail-IDs für die Audience des Advertisers mithilfe des SHA-256-Algorithmus.

   1. Ordnen Sie die Spalte mit Hash-E-Mail-IDs dem Attribut des Typs der Besucher-ID zu.

   1. Erstellen Sie die Zielgruppe mit der `Tealium_visitor_id` -Attribut. Wenden Sie die richtige Anreicherung an, um die Audience Trigger. Siehe [[!DNL Tealium] Dokumentation zu Besucherkennungsattributen](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. Der Werbetreibende muss dem Adobe Account Team Daten zur Segmentzuordnung zur Verfügung stellen, damit die Segmente in DSP erstellt werden können. Verwenden Sie die folgenden Spaltennamen und -werte in einer Datei mit kommagetrennten Werten:

   * **Externer Segmentschlüssel:** Der externe Segmentschlüssel, den Sie später in den Aktionseinstellungen für den Connector in [!DNL Tealium]. Die empfohlene Benennungskonvention lautet &quot;`<DSP source key>_<Tealium segment name>`,&quot;z. B. &quot;57bf424dc10_ffee-drinkers&quot;. Verwenden Sie für den DSP Quellschlüssel die [!UICONTROL Source Key] aus den Quelleinstellungen der DSP Zielgruppe.

   * **Segmentname:** Der Segmentname.

   * **Segmentbeschreibung:** Der Zweck oder die Regel des Segments oder beides.

   * **Übergeordnete ID:** Leer lassen

   * **Video-CPM:** 0

   * **CPM anzeigen:** 0

   * **Segmentfenster:** Die Gültigkeitsdauer des Segments.

## Schritt 4: Erstellen von Connectoren in [!DNL Tealium] Freigeben von Segmentdaten {#tealium-connector}

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

            1. In der Option zum Erstellen eines benutzerdefinierten Felds finden Sie im [!DNL Source Key] und geben Sie die [!UICONTROL External Segment Key] , die in der [Segmentzuordnungsdaten](#map-data) im vorangegangenen Verfahren.

               DSP verwendet diesen Schlüssel zum Ausfüllen Ihres Segments.

            1. (Empfohlen) Erstellen Sie eine Aktualisierungsaktion, um das Segment zu aktualisieren.

## Schritt 5: Duplizieren Sie den vorhandenen Connector in [!DNL Tealium] weiterhin Segmente freigeben {#duplicate-connector}

Pro Segment können Sie nur einen Connector und pro Connector ein Segment haben.

1. In [!DNL Tealium], duplizieren Sie das Segment, für das Sie ein anderes Segment erstellen möchten, und benennen Sie das neue Segment um.

1. In [!DNL Tealium], Duplikat [Der von Ihnen erstellte Connector](#tealium-connector) und benennen Sie den neuen Connector aus`<original name>-copy`&quot; auf den neuen Segmentnamen.

## Schritt 6: Vergleich der Anzahl universeller IDs mit der Anzahl der gehashten E-Mail-Adressen {#compare-id-count}

Nachdem Sie alle Schritte ausgeführt haben, sollten die Segmente in DSP innerhalb von 24 Stunden verfügbar sein. Überprüfen Sie dies in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe aus [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierungseinstellungen), die das Segment innerhalb von 24 Stunden füllt. Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen.

Die Übersetzungsrate von Hash-E-Mail-Adressen in universelle IDs sollte über 90 % liegen. Wenn Sie beispielsweise 100 Hash-E-Mail-Adressen von Ihrer Kundendatenplattform senden, sollten diese in mehr als 90 universelle IDs übersetzt werden. Eine Übersetzungsrate von 90 % oder weniger ist ein Problem. Weitere Informationen dazu, wie die Segmentzählungen variieren können, finden Sie unter[Ursachen für Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).&quot;

Segmente werden alle 24 Stunden aktualisiert. Die Aufnahme in ein Segment läuft jedoch nach 30 Tagen ab, um die Einhaltung der Datenschutzbestimmungen sicherzustellen. Aktualisieren Sie daher die Zielgruppen, indem Sie sie erneut von [!DNL Tealium] alle 30 Tage oder weniger.

Wenden Sie sich zur Fehlerbehebung an Ihr Adobe-Account-Team oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
