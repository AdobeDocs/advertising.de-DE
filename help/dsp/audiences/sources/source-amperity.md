---
title: Konvertieren von Benutzer-IDs aus [!DNL Amperity] zu universellen IDs
description: Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL Amperity] Erstanbietersegmente.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Amperity] zu universellen IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL Amperity] Kundendatenplattform , um die Erstanbieter-Hash-E-Mail-Adressen Ihrer Organisation in universelle IDs für zielgerichtete Werbung zu konvertieren.

1. (Konvertieren von E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Tracking einrichten, um [!DNL Analytics] messen](#analytics-tracking).

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. [Vorbereiten und Freigeben von Daten zur Segmentzuordnung](#map-data).

1. [Daten-Push-Benachrichtigung anfordern von [!DNL Amperity] DSP](#push-data).

1. [Anzahl der universellen IDs mit der Anzahl der gehashten E-Mail-Adressen vergleichen](#compare-id-count).

## Schritt 1: Tracking einrichten für [!DNL Analytics] messen {#analytics-tracking}

*Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Konvertieren von E-Mail-Adressen in [!DNL RampIDs] oder [!DNL ID5] IDs verwenden, müssen Sie Folgendes tun:

1. (Wenn Sie dies noch nicht getan haben) Führen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und stellen Sie sicher, dass die Variable [AMO-ID und EF ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs aufgefüllt werden.

1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie universellen ID-spezifischen Code auf Ihren Webseiten bereit, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) für Durchsichten zuzuordnen:

   * **Für [!DNL RampIDs]:** Sie müssen auf Ihren Webseiten ein zusätzliches JavaScript-Tag bereitstellen, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) zu ermöglichen, Durchsichten anzuzeigen. Wenden Sie sich an Ihr Adobe Account-Team, das Ihnen Anweisungen zur Registrierung für eine [!DNL LiveRamp] [!DNL LaunchPad] Tag aus [!DNL LiveRamp] Authentifizierungs-Traffic-Lösungen. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nachdem Sie sich registriert haben, generiert Ihr Adobe Account-Team ein eindeutiges Tag, das Ihr Unternehmen für die Implementierung auf Ihren Webseiten bereitstellen kann.

## Schritt 2: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen einer Zielgruppenquelle](source-manage.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren. Sie können Ihre Benutzer-IDs beliebig in [Verfügbare universelle ID-Formate](source-about.md).

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, den Sie zum Pushen der Segmentdaten verwenden.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für die [!DNL Amperity] Benutzer.

## Schritt 3: Vorbereiten und Freigeben von Segmentzuordnungsdaten {#map-data}

Der Advertiser muss Daten zur Segmentzuordnung vorbereiten und freigeben.

1. Within [!DNL Amperity], Hash die E-Mail-IDs für die Zielgruppe mithilfe des SHA-256-Algorithmus.

1. Der Werbetreibende muss dem Adobe Account Team Daten zur Segmentzuordnung zur Verfügung stellen, damit die Segmente in DSP erstellt werden können. Verwenden Sie die folgenden Spaltennamen und -werte in einer Datei mit kommagetrennten Werten:

   * **Externer Segmentschlüssel:** Die [!DNL Amperity] Segmentschlüssel, der mit dem Segment verknüpft ist.

   * **Segmentname:** Der Segmentname.

   * **Segmentbeschreibung:** Der Zweck oder die Regel des Segments oder beides.

   * **Übergeordnete ID:** Leer lassen

   * **Video-CPM:** 0

   * **CPM anzeigen:** 0

   * **Segmentfenster:** Die Gültigkeitsdauer des Segments.

## Schritt 4: Daten-Push-Benachrichtigung anfordern von [!DNL Amperity] DSP {#push-data}

1. Nachdem das Segment in DSP zugeordnet wurde, muss der Advertiser mit seiner [!DNL Amperity] repräsentativ sein, um die Segmentdaten an DSP zu verteilen.

1. Der Werbetreibende muss dann mit dem Adobe Account Team bestätigen, dass die Segmentdaten empfangen wurden.

Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Überprüfen Sie dies in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe aus [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierungseinstellungen), dass das Segment verfügbar ist und gefüllt wird.

Die Segmente werden entsprechend der Konfiguration für den Advertiser in [!DNL Amperity]. Unabhängig davon, wie häufig das Segment aktualisiert wird, läuft die Aufnahme in ein Segment standardmäßig nach 30 Tagen oder nach einem kundenspezifischen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie erneut aus [!DNL Amperity] vor Ablauf. Wenden Sie sich an Ihr Adobe-Account-Team, um einen benutzerdefinierten Segmentablauf anzufordern.

## Schritt 5: Vergleich der Anzahl universeller IDs mit der Anzahl der gehashten E-Mail-Adressen {#compare-id-count}

Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein. In Ihrer Zielgruppenbibliothek (verfügbar, wenn Sie eine Zielgruppe aus [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierungseinstellungen) die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen vergleichen.

Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentzählungen variieren können, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).&quot;

Wenden Sie sich zur Fehlerbehebung an Ihr Adobe-Account-Team oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
