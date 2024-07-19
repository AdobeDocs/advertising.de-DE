---
title: Konvertieren von Benutzer-IDs von  [!DNL Amperity]  in universelle IDs
description: Erfahren Sie, wie Sie DSP aktivieren, um Ihre Erstanbietersegmente zu erfassen. [!DNL Amperity]
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs von [!DNL Amperity] in universelle IDs

*Beta-Funktion*

Verwenden Sie die DSP Integration mit der [!DNL Amperity]-Kundendatenplattform, um die Erstanbieter-Hash-E-Mail-Adressen Ihrer Organisation in universelle IDs für zielgerichtete Werbung zu konvertieren.

1. (So konvertieren Sie E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Werbetreibende mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Richten Sie das Tracking ein, um die  [!DNL Analytics] Messung](#analytics-tracking) zu aktivieren.

1. [Erstellen Sie eine Zielgruppenquelle in DSP](#source-create).

1. [ Vorbereitung und Freigabe von Daten zur Segmentzuordnung](#map-data).

1. [Fordern Sie einen Daten-Push von  [!DNL Amperity] an DSP](#push-data) an.

1. [Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der gehashten E-Mail-Adressen](#compare-id-count).

## Schritt 1: Tracking für [!DNL Analytics]-Messung einrichten {#analytics-tracking}

*Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Um E-Mail-Adressen in [!DNL RampIDs] oder [!DNL ID5] IDs zu konvertieren, müssen Sie Folgendes tun:

1. (Wenn Sie dies noch nicht getan haben) Füllen Sie alle [Voraussetzungen für die Implementierung von [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) aus und stellen Sie sicher, dass die [AMO ID und EF ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs eingetragen sind.

1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie universellen ID-spezifischen Code auf Ihren Webseiten bereit, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) für Durchsichten zuzuordnen:

   * **Für [!DNL RampIDs]:** Sie müssen auf Ihren Webseiten ein zusätzliches JavaScript-Tag bereitstellen, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) zu ermöglichen, Durchsichten anzuzeigen. Wenden Sie sich an Ihr Adobe Account-Team, das Ihnen Anweisungen zur Registrierung für ein [!DNL LiveRamp] [!DNL LaunchPad] -Tag von [!DNL LiveRamp] Authentication Traffic Solutions gibt. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nachdem Sie sich registriert haben, generiert Ihr Adobe Account-Team ein eindeutiges Tag, das Ihr Unternehmen für die Implementierung auf Ihren Webseiten bereitstellen kann.

## Schritt 2: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen Sie eine Zielgruppenquelle](source-manage.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren. Sie können Ihre Benutzer-IDs in eines der [verfügbaren universellen ID-Formate](source-about.md) konvertieren.

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, den Sie zum Pushen der Segmentdaten verwenden.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für den Benutzer [!DNL Amperity] frei.

## Schritt 3: Vorbereiten und Freigeben von Segmentzuordnungsdaten {#map-data}

Der Advertiser muss Daten zur Segmentzuordnung vorbereiten und freigeben.

1. Hash Sie innerhalb von [!DNL Amperity] die E-Mail-IDs für die Zielgruppe mithilfe des SHA-256-Algorithmus.

1. Der Werbetreibende muss dem Adobe Account Team Daten zur Segmentzuordnung zur Verfügung stellen, damit die Segmente in DSP erstellt werden können. Verwenden Sie die folgenden Spaltennamen und -werte in einer Datei mit kommagetrennten Werten:

   * **Externer Segmentschlüssel:** Der mit dem Segment verknüpfte [!DNL Amperity] Segmentschlüssel.

   * **Segmentname:** Der Segmentname.

   * **Segmentbeschreibung:** Der Zweck oder die Regel des Segments oder beides.

   * **Übergeordnete ID:** Leer lassen

   * **Video CPM:** 0

   * **CPM anzeigen:** 0

   * **Segmentfenster:** Die Live-Zeit des Segments.

## Schritt 4: Daten-Push-Benachrichtigung von [!DNL Amperity] an DSP anfordern {#push-data}

1. Nachdem das Segment in DSP zugeordnet wurde, muss der Werbetreibende mit seinem [!DNL Amperity] -Vertreter zusammenarbeiten, um die Segmentdaten an DSP zu verteilen.

1. Der Werbetreibende muss dann mit dem Adobe Account Team bestätigen, dass die Segmentdaten empfangen wurden.

Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Überprüfen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe über [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob das Segment verfügbar ist und ausgefüllt wird.

Die Segmente werden wie für den Advertiser in [!DNL Amperity] konfiguriert aktualisiert. Unabhängig davon, wie häufig das Segment aktualisiert wird, läuft die Aufnahme in ein Segment standardmäßig nach 30 Tagen oder nach einem kundenspezifischen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie vor Ablauf von [!DNL Amperity] erneut aus dem Diagramm verschieben. Wenden Sie sich an Ihr Adobe-Account-Team, um einen benutzerdefinierten Segmentablauf anzufordern.

## Schritt 5: Vergleich der Anzahl universeller IDs mit der Anzahl der gehashten E-Mail-Adressen {#compare-id-count}

Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein.

In Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe über &quot;[!UICONTROL Audiences] > [!UICONTROL All Audiences]&quot;oder in den Platzierungseinstellungen erstellen oder bearbeiten) wird die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen verglichen. Weitere Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentzahlen variieren können, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances)&quot;.

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Problemen mit der Übersetzungsrate und der Benutzeranzahl finden Sie unter &quot;[Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md)&quot;.

Wenden Sie sich zur Fehlerbehebung bei Problemen mit dem Konvertierungsverfahren an Ihr Adobe Account-Team oder an `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
