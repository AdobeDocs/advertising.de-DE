---
title: Konvertieren von Benutzer-IDs  [!DNL Tealium]  universellen IDs
description: Erfahren Sie, wie Sie DSP für die Aufnahme  [!DNL Tealium]  Erstanbietersegmenten aktivieren.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Tealium] in universelle IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL Tealium] Kundendatenplattform, um die gehashten First-Party-E-Mail-Adressen Ihres Unternehmens in universelle IDs für zielgerichtete Werbung zu konvertieren. Der Prozess verwendet den Firehose-Connector von [!DNL Amazon Web Services] (AWS). Führen Sie die folgenden Schritte aus, um Daten von Tealium für DSP freizugeben:

1. (So konvertieren Sie E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Richten Sie das Tracking ein, um  [!DNL Analytics]  Messung zu &#x200B;](#analytics-tracking).

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. [Vorbereiten und Freigeben von Segmentzuordnungsdaten](#map-data).

1. [Erstellen von Connectoren in [!DNL Tealium] , um Segmentdaten freizugeben](#tealium-connector).

1. [Duplizieren Sie den vorhandenen Connector in [!DNL Tealium] , um weiterhin Segmente freizugeben](#duplicate-connector).

1. [Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der Hash-E-Mail-Adressen](#compare-id-count).

## Schritt 1: Einrichten des Trackings für die [!DNL Analytics] {#analytics-tracking}

*Werbetreibende mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Gehen Sie wie folgt vor, um E-Mail-Adressen in [!DNL RampIDs]- oder [!DNL ID5]-IDs zu konvertieren:

1. (Falls noch nicht geschehen) Vervollständigen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und stellen Sie sicher, dass [AMO-ID und EF-ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs angegeben sind.

1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie auf Ihren Web-Seiten einen universellen ID-spezifischen Code bereit, um Konversionen aus den IDs in Desktop-Browsern und mobilen Webbrowsern (aber nicht in mobilen Apps) abzugleichen und Anleitungen zu erhalten:

   * **[!DNL RampIDs]:** Sie müssen ein zusätzliches JavaScript-Tag auf Ihren Web-Seiten bereitstellen, damit die Konversionen der IDs in Desktop- und mobilen Webbrowsern (aber nicht in mobilen Apps) für die Viewthroughs übereinstimmen. Wenden Sie sich an Ihr Adobe-Konto-Team, das Ihnen Anweisungen zur Registrierung für ein [!DNL LiveRamp] [!DNL LaunchPad]-Tag von [!DNL LiveRamp] Authentication Traffic Solutions gibt. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nach der Registrierung generiert Ihr Adobe-Account-Team ein eindeutiges Tag, das Ihr Unternehmen auf Ihren Web-Seiten implementieren kann.

## Schritt 2: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen einer Zielgruppenquelle](source-manage.md) um Zielgruppen in Ihr DSP-Konto oder ein Advertiser-Konto zu importieren. Sie können Ihre Benutzerkennungen in eines der ([&#x200B; universellen ID-Formate) &#x200B;](source-about.md).

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, mit dem Sie die Segmentzuordnungsdaten vorbereiten.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quell-Code-Schlüssel für den [!DNL Tealium] Benutzer frei.

## Schritt 3: Vorbereiten und Freigeben von Segmentzuordnungsdaten {#map-data}

Der Advertiser muss Segmentzuordnungsdaten vorbereiten und freigeben.

1. Der Werbetreibende muss die Daten in [!DNL Tealium] vorbereiten:

   1. Hashing der E-Mail-IDs für die Zielgruppe des Werbetreibenden mithilfe des SHA-256-Algorithmus durchführen.

   1. Ordnen Sie die Spalte mit den Hash-E-Mail-IDs dem Attribut des Typs der Besucher-ID zu.

   1. Erstellen Sie die Zielgruppe mit dem Attribut `Tealium_visitor_id` . Wenden Sie die richtige Anreicherung auf die Zielgruppe an, um sie mit Triggern zu versehen. Siehe die [[!DNL Tealium] Dokumentation zu Besucher-ID-Attributen](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. Der Werbetreibende muss Segmentzuordnungsdaten an das Adobe-Konto-Team senden, um die Segmente in DSP zu erstellen. Verwenden Sie die folgenden Spaltennamen und -werte in einer durch Kommas getrennten Wertedatei:

   * **Externer Segmentschlüssel** Der Schlüssel des externen Segments, den Sie später in den Aktionseinstellungen für den Connector in [!DNL Tealium] angeben. Die empfohlene Namenskonvention lautet &quot;`<DSP source key>_<Tealium segment name>`&quot;, z. B. „57bf424dc10_Coffee-Drinkers“. Verwenden Sie für den DSP-Quellschlüssel die [!UICONTROL Source Key] aus den Einstellungen für die DSP-Zielgruppenquelle.

   * **Segmentname:** Der Segmentname.

   * **Segmentbeschreibung:** Zweck oder Regel des Segments oder beides.

   * **Übergeordnete ID:** leer lassen

   * **Video CPM:** 0

   * **CPM anzeigen:** 0

   * **Segmentfenster** Die Lebensdauer des Segments.

## Schritt 4: Erstellen Sie Connectoren in [!DNL Tealium], um Segmentdaten freizugeben {#tealium-connector}

Erstellen Sie für jedes Segment, das Sie freigeben möchten, einen separaten Connector für jede Aktion, die Datenänderungen Trigger. Um beispielsweise zwei Segmente mit jeweils zwei Triggern gemeinsam zu nutzen, erstellen Sie vier Connectoren.

1. Das Adobe-Konto-Team stellt dem Werbetreibenden Anmeldeinformationen für den AWS-Firehose-Connector zur Verfügung.

1. Fügen Sie [!DNL Tealium] [einen Connector hinzu](https://docs.tealium.com/server-side/connectors/add/) indem Sie die folgenden Optionen verwenden:

   1. Wählen Sie den [!DNL AWS Firehose] Connector aus.

   1. In den Quelleinstellungen:

      1. Zielgruppensegment zur Freigabe auswählen.

      1. Einrichten eines Triggers:

         * Wählen Sie als ersten Connector für das Segment die `Joined Audience` Trigger aus. Dadurch wird sichergestellt, dass Daten für DSP freigegeben werden, sobald ein Benutzer einem Segment beitritt.

         * Wählen Sie als zweiten Connector für das Segment die `Left Audience` Trigger aus. Dieser Connector wird verwendet, um alle Opt-outs und Benutzende zu verarbeiten, die das Segment in DSP verlassen.

   1. Geben Sie in den Konfigurationseinstellungen den AWS-Firehose-Connector an. Wenn Sie noch keinen Feuerschlauch-Connector für DSP hinzugefügt haben, fügen Sie einen Feuerschlauch-Connector mit den folgenden Informationen hinzu:

      * **Name:** Der Name des Connectors.

      * **Zugriffsschlüssel:** Der vom Adobe-Konto-Team bereitgestellte Zugriffsschlüssel.

      * **Geheimer Schlüssel:** Der geheime Schlüssel, der vom Adobe-Konto-Team bereitgestellt wird.

      * **Region:** US East North Virginia (US-East-1)

   1. Gehen Sie in den Aktionseinstellungen wie folgt vor:

      1. Erstellen Sie die Aktion „Kundendaten an Versand-Stream (Erweitert) senden“, um dem Segment Daten hinzuzufügen, und verwenden Sie dabei die folgenden Informationen:

         * **Aktionsname:** Der Name der Aktion.

         * **Aktionstyp** Kundendaten an Versand-Stream senden (Erweitert)

         * **Versand-Stream:** Tealium_CDP_connector

         * **Nachrichtendaten:** Sie Folgendes aus:

            1. Wählen Sie ein Attribut für das Segment:

               * Benennen Sie für das Attribut hashed_email die benutzerdefinierte `hashed_email`.

               * Benennen Sie für das Cookies -Attribut die benutzerdefinierte `cookies`.

            1. Geben Sie in der Option zum Erstellen eines benutzerdefinierten Felds im Feld [!DNL Source Key] die [!UICONTROL External Segment Key] ein, die in den [Segmentzuordnungsdaten“ &#x200B;](#map-data) vorherigen Verfahren enthalten waren.

               DSP verwendet diesen Schlüssel zum Ausfüllen Ihres Segments.

            1. (Empfohlen) Erstellen Sie eine Aktualisierungsaktion, um das Segment aktuell zu halten.

## Schritt 5: Duplizieren Sie den vorhandenen Connector in [!DNL Tealium], um weiterhin Segmente freizugeben {#duplicate-connector}

Pro Segment und Segment kann nur ein Connector verwendet werden.

1. Duplizieren Sie [!DNL Tealium] das Segment, für das Sie ein weiteres Segment erstellen möchten, und benennen Sie das neue Segment um.

1. Duplizieren Sie [!DNL Tealium] [den von Ihnen &#x200B;](#tealium-connector) vorherigen Vorgang erstellten Connector) und benennen Sie den neuen Connector von &quot;`<original name>-copy`&quot; in den neuen Segmentnamen um.

## Schritt 6: Anzahl der universellen IDs mit der Anzahl der Hash-E-Mail-Adressen vergleichen {#compare-id-count}

Die Segmente sollten innerhalb von 24 Stunden in DSP verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein.

Überprüfen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob das Segment aufgefüllt ist, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen. Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentanzahl variieren kann, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).

Segmente werden alle 24 Stunden aktualisiert. Die Aufnahme in ein Segment läuft jedoch standardmäßig nach 30 Tagen oder nach einem vom Kunden angegebenen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie vor dem Ablauf erneut aus [!DNL Tealium] pushen. Um eine benutzerdefinierte Segmentgültigkeit anzufordern, wenden Sie sich an Ihr Adobe-Account-Team.

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Übersetzungsraten und Problemen mit der Benutzeranzahl finden Sie unter &quot;[&#x200B; für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md).

Wenden Sie sich zur Fehlerbehebung bei Konvertierungsproblemen an Ihr Adobe-Kundenbetreuungsteam oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
