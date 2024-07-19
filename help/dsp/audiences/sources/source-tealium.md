---
title: Konvertieren von Benutzer-IDs von  [!DNL Tealium]  in universelle IDs
description: Erfahren Sie, wie Sie DSP aktivieren, um Ihre Erstanbietersegmente zu erfassen. [!DNL Tealium]
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs von [!DNL Tealium] in universelle IDs

*Beta-Funktion*

Verwenden Sie die DSP Integration mit der [!DNL Tealium]-Kundendatenplattform, um die Erstanbieter-Hash-E-Mail-Adressen Ihrer Organisation in universelle IDs für zielgerichtete Werbung zu konvertieren. Der Prozess verwendet den Feuerschlauch-Connector [!DNL Amazon Web Services] (AWS). Führen Sie die folgenden Schritte aus, um Daten aus Tealium für DSP freizugeben:

1. (So konvertieren Sie E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Werbetreibende mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Richten Sie das Tracking ein, um die  [!DNL Analytics] Messung](#analytics-tracking) zu aktivieren.

1. [Erstellen Sie eine Zielgruppenquelle in DSP](#source-create).

1. [ Vorbereitung und Freigabe von Daten zur Segmentzuordnung](#map-data).

1. [Erstellen Sie Connectoren in  [!DNL Tealium] , um Segmentdaten freizugeben](#tealium-connector).

1. [Duplizieren Sie den vorhandenen Connector in [!DNL Tealium] , um weiterhin Segmente freizugeben](#duplicate-connector).

1. [Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der gehashten E-Mail-Adressen](#compare-id-count).

## Schritt 1: Tracking für [!DNL Analytics]-Messung einrichten {#analytics-tracking}

*Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Um E-Mail-Adressen in [!DNL RampIDs] oder [!DNL ID5] IDs zu konvertieren, müssen Sie Folgendes tun:

1. (Wenn Sie dies noch nicht getan haben) Füllen Sie alle [Voraussetzungen für die Implementierung von [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) aus und stellen Sie sicher, dass die [AMO ID und EF ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs eingetragen sind.

1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie universellen ID-spezifischen Code auf Ihren Webseiten bereit, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) für Durchsichten zuzuordnen:

   * **Für [!DNL RampIDs]:** Sie müssen auf Ihren Webseiten ein zusätzliches JavaScript-Tag bereitstellen, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) zu ermöglichen, Durchsichten anzuzeigen. Wenden Sie sich an Ihr Adobe Account-Team, das Ihnen Anweisungen zur Registrierung für ein [!DNL LiveRamp] [!DNL LaunchPad] -Tag von [!DNL LiveRamp] Authentication Traffic Solutions gibt. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nachdem Sie sich registriert haben, generiert Ihr Adobe Account-Team ein eindeutiges Tag, das Ihr Unternehmen für die Implementierung auf Ihren Webseiten bereitstellen kann.

## Schritt 2: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen Sie eine Zielgruppenquelle](source-manage.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren. Sie können Ihre Benutzer-IDs in eines der [verfügbaren universellen ID-Formate](source-about.md) konvertieren.

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, mit dem Sie die Daten für die Segmentzuordnung vorbereiten.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für den Benutzer [!DNL Tealium] frei.

## Schritt 3: Vorbereiten und Freigeben von Segmentzuordnungsdaten {#map-data}

Der Advertiser muss Daten zur Segmentzuordnung vorbereiten und freigeben.

1. Der Werbetreibende muss die Daten innerhalb von [!DNL Tealium] vorbereiten:

   1. Hash der E-Mail-IDs für die Audience des Advertisers mithilfe des SHA-256-Algorithmus.

   1. Ordnen Sie die Spalte mit Hash-E-Mail-IDs dem Attribut des Typs der Besucher-ID zu.

   1. Erstellen Sie die Zielgruppe mit dem Attribut `Tealium_visitor_id` . Wenden Sie die richtige Anreicherung an, um die Audience Trigger. Weitere Informationen finden Sie in der [[!DNL Tealium] Dokumentation zu Besucherkennungsattributen](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. Der Werbetreibende muss dem Adobe Account Team Daten zur Segmentzuordnung zur Verfügung stellen, damit die Segmente in DSP erstellt werden können. Verwenden Sie die folgenden Spaltennamen und -werte in einer Datei mit kommagetrennten Werten:

   * **Externer Segmentschlüssel:** Der externe Segmentschlüssel, den Sie später in den Aktionseinstellungen für den Connector in [!DNL Tealium] angeben. Die empfohlene Benennungskonvention ist &quot;`<DSP source key>_<Tealium segment name>`&quot;, z. B. &quot;57bf424dc10_ffee-drinkers&quot;. Verwenden Sie für den DSP Quellschlüssel die [!UICONTROL Source Key] aus den Einstellungen der DSP Zielgruppenquelle.

   * **Segmentname:** Der Segmentname.

   * **Segmentbeschreibung:** Der Zweck oder die Regel des Segments oder beides.

   * **Übergeordnete ID:** Leer lassen

   * **Video CPM:** 0

   * **CPM anzeigen:** 0

   * **Segmentfenster:** Die Live-Zeit des Segments.

## Schritt 4: Erstellen Sie Connectoren in [!DNL Tealium], um Segmentdaten freizugeben. {#tealium-connector}

Erstellen Sie für jedes Segment, das Sie freigeben möchten, einen separaten Connector für jede Aktion, bei der sich die Daten von Trigger ändern. Um beispielsweise zwei Segmente mit jeweils zwei Triggern freizugeben, erstellen Sie vier Connectoren.

1. Das Adobe Account-Team stellt dem Advertiser die Anmeldeinformationen des AWS-Feuerschlauch-Connectors zur Verfügung.

1. Fügen Sie in [!DNL Tealium] [einen Connector](https://docs.tealium.com/server-side/connectors/add/) mit den folgenden Optionen hinzu:

   1. Wählen Sie den Connector [!DNL AWS Firehose] aus.

   1. In den Quelleinstellungen:

      1. Wählen Sie das freizugebende Zielgruppensegment aus.

      1. Richten Sie einen Trigger ein:

         * Wählen Sie für den ersten Connector für das Segment den Trigger `Joined Audience` aus. Dadurch wird sichergestellt, dass Daten für DSP freigegeben werden, sobald ein Benutzer einem Segment beitritt.

         * Wählen Sie für den zweiten Connector für das Segment den Trigger `Left Audience` aus. Dieser Connector wird verwendet, um alle Opt-outs und Benutzer zu verarbeiten, die das Segment in DSP verlassen.

   1. Geben Sie in den Konfigurationseinstellungen den AWS-Feuerschlauch-Connector an. Wenn Sie den Feuerlöschschlauch-Connector noch nicht für DSP hinzugefügt haben, fügen Sie mithilfe der folgenden Informationen einen Feuerlöschschlauch-Connector hinzu:

      * **Name:** Der Name des Connectors.

      * **Zugriffsschlüssel:** Der vom Adobe Account Team bereitgestellte Zugriffsschlüssel.

      * **Geheimer Schlüssel:** Der vom Adobe-Account-Team bereitgestellte geheime Schlüssel.

      * **Region:** US East North Virginia (us-east-1)

   1. Führen Sie in den Aktionseinstellungen die folgenden Schritte aus:

      1. Erstellen Sie die Aktion &quot;Senden von Kundendaten an Bereitstellungs-Stream (Erweitert)&quot;, um dem Segment Daten hinzuzufügen. Verwenden Sie dazu die folgenden Informationen:

         * **Aktionsname:** Der Name der Aktion.

         * **Aktionstyp:** Senden von Kundendaten an den Bereitstellungs-Stream (erweitert)

         * **Bereitstellungsstream:** tealium_CDP_Connector

         * **Nachrichtendaten:** Gehen Sie wie folgt vor:

            1. Wählen Sie ein Attribut für das Segment aus:

               * Nennen Sie für das Attribut Hashed_Email die benutzerdefinierte Nachricht &quot;`hashed_email`&quot;.

               * Nennen Sie für das Attribut Cookies die benutzerdefinierte Meldung `cookies`.

            1. Geben Sie in der Option zum Erstellen eines benutzerdefinierten Felds im Feld [!DNL Source Key] den Wert [!UICONTROL External Segment Key] ein, der im vorherigen Verfahren in den [Daten der Segmentzuordnung](#map-data) enthalten war.

               DSP verwendet diesen Schlüssel zum Ausfüllen Ihres Segments.

            1. (Empfohlen) Erstellen Sie eine Aktualisierungsaktion, um das Segment zu aktualisieren.

## Schritt 5: Duplizieren Sie den vorhandenen Connector in [!DNL Tealium], um weiterhin Segmente freizugeben. {#duplicate-connector}

Pro Segment können Sie nur einen Connector und pro Connector ein Segment haben.

1. Duplizieren Sie in [!DNL Tealium] das Segment, für das Sie ein weiteres Segment erstellen möchten, und benennen Sie das neue Segment um.

1. Duplizieren Sie in &quot;[!DNL Tealium]&quot;den Connector, den Sie im vorherigen Verfahren erstellt haben, und benennen Sie den neuen Connector von &quot;`<original name>-copy`&quot;in den neuen Segmentnamen um.[](#tealium-connector)

## Schritt 6: Vergleich der Anzahl universeller IDs mit der Anzahl der gehashten E-Mail-Adressen {#compare-id-count}

Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein.

Überprüfen Sie in Ihrer Zielgruppenbibliothek (die beim Erstellen oder Bearbeiten einer Zielgruppe über &quot;[!UICONTROL Audiences] > [!UICONTROL All Audiences]&quot;oder in den Platzierungseinstellungen verfügbar ist), ob das Segment gefüllt wird, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen. Weitere Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentzahlen variieren können, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances)&quot;.

Segmente werden alle 24 Stunden aktualisiert. Die Aufnahme in ein Segment läuft jedoch standardmäßig nach 30 Tagen oder nach einem kundenspezifischen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie vor Ablauf von [!DNL Tealium] erneut aus dem Diagramm verschieben. Wenden Sie sich an Ihr Adobe-Account-Team, um einen benutzerdefinierten Segmentablauf anzufordern.

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Problemen mit der Übersetzungsrate und der Benutzeranzahl finden Sie unter &quot;[Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md)&quot;.

Wenden Sie sich zur Fehlerbehebung bei Problemen mit dem Konvertierungsverfahren an Ihr Adobe Account-Team oder an `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
