---
title: Konvertieren von Benutzer-IDs aus [!DNL Optimizely] zu universellen IDs
description: Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL Optimizely] Erstanbietersegmente.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Optimizely] zu universellen IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL Optimizely] Kundendatenplattform , um die Erstanbieter-Hash-E-Mail-Adressen Ihrer Organisation in universelle IDs für zielgerichtete Werbung zu konvertieren.

1. (Konvertieren von E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Tracking einrichten, um [!DNL Analytics] messen](#analytics-tracking).

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. [Segmentdaten vorbereiten und pushen](#push-data).

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

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für die [!DNL Optimizely] Benutzer.

## Schritt 3: Segmentdaten vorbereiten und pushen {#push-data}

Der Werbetreibende muss die Daten mithilfe der [!DNL Optimizely Data Platform]. Wenden Sie sich bei Fragen zum Prozess an Ihren [!DNL Optimizely] Vertreter.

1. Within [!DNL Optimizely Data Platform], Hash die E-Mail-IDs für die Zielgruppe mithilfe des SHA-256-Algorithmus.

1. Folgen [[!DNL Optimizely's] Anweisungen zum Senden des Segments an DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Fügen Sie die folgenden Informationen hinzu, um die Integration zu aktivieren:

   * **Source-Schlüssel:** Dies ist der in [Schritt 2](#source-create).

   * **Kontocode:** Dies ist der alphanumerische DSP-Kontocode, den Sie in DSP finden unter [!UICONTROL Settings] > [!UICONTROL Account].

Die Segmente werden entsprechend der Konfiguration für den Advertiser aktualisiert. Unabhängig davon, wie häufig das Segment aktualisiert wird, läuft die Aufnahme in ein Segment standardmäßig nach 30 Tagen oder nach einem kundenspezifischen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie erneut aus [!DNL Optimizely] vor Ablauf. Wenden Sie sich an Ihr Adobe-Account-Team, um einen benutzerdefinierten Segmentablauf anzufordern.

## Schritt 4: Vergleich der Anzahl universeller IDs mit der Anzahl der gehashten E-Mail-Adressen {#compare-id-count}

Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein.

Überprüfen Sie dies in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe aus [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierungseinstellungen), dass das Segment verfügbar ist und ausgefüllt wird, und die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen vergleichen. Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentzählungen variieren können, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).&quot;

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Problemen mit der Übersetzungsrate und der Benutzeranzahl finden Sie unter &quot;[Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md).&quot;

Wenden Sie sich zur Fehlerbehebung bei Problemen mit dem Konvertierungsverfahren an Ihr Adobe-Account-Team oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
