---
title: Konvertieren von Benutzer-IDs  [!DNL Optimizely]  universellen IDs
description: Erfahren Sie, wie Sie DSP für die Aufnahme  [!DNL Optimizely]  Erstanbietersegmenten aktivieren.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Optimizely] in universelle IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL Optimizely] Kundendatenplattform, um die gehashten First-Party-E-Mail-Adressen Ihres Unternehmens in universelle IDs für zielgerichtete Werbung zu konvertieren.

1. (So konvertieren Sie E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Richten Sie das Tracking ein, um  [!DNL Analytics]  Messung zu ](#analytics-tracking).

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. [Vorbereiten und Übertragen der Segmentdaten](#push-data).

1. [Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der Hash-E-Mail-Adressen](#compare-id-count).

## Schritt 1: Einrichten des Trackings für die [!DNL Analytics] {#analytics-tracking}

*Werbetreibende mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Gehen Sie wie folgt vor, um E-Mail-Adressen in [!DNL RampIDs]- oder [!DNL ID5]-IDs zu konvertieren:

1. (Falls noch nicht geschehen) Vervollständigen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und stellen Sie sicher, dass [AMO-ID und EF-ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs angegeben sind.

1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie auf Ihren Web-Seiten einen universellen ID-spezifischen Code bereit, um Konversionen aus den IDs in Desktop-Browsern und mobilen Webbrowsern (aber nicht in mobilen Apps) abzugleichen und Anleitungen zu erhalten:

   * **[!DNL RampIDs]:** Sie müssen ein zusätzliches JavaScript-Tag auf Ihren Web-Seiten bereitstellen, damit die Konversionen der IDs in Desktop- und mobilen Webbrowsern (aber nicht in mobilen Apps) für die Viewthroughs übereinstimmen. Wenden Sie sich an Ihr Adobe-Konto-Team, das Ihnen Anweisungen zur Registrierung für ein [!DNL LiveRamp] [!DNL LaunchPad]-Tag von [!DNL LiveRamp] Authentication Traffic Solutions gibt. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nach der Registrierung generiert Ihr Adobe-Account-Team ein eindeutiges Tag, das Ihr Unternehmen auf Ihren Web-Seiten implementieren kann.

## Schritt 2: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen einer Zielgruppenquelle](source-manage.md) um Zielgruppen in Ihr DSP-Konto oder ein Advertiser-Konto zu importieren. Sie können Ihre Benutzerkennungen in eines der ([ universellen ID-Formate) ](source-about.md).

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, mit dem Sie die Segmentdaten pushen.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quell-Code-Schlüssel für den [!DNL Optimizely] Benutzer frei.

## Schritt 3: Vorbereiten und Übertragen der Segmentdaten {#push-data}

Der Werbetreibende muss die Daten mithilfe der [!DNL Optimizely Data Platform] vorbereiten und pushen. Wenden Sie sich bei Fragen zum Prozess an Ihren [!DNL Optimizely].

1. Erstellen Sie in [!DNL Optimizely Data Platform] einen Hash-Wert für die E-Mail-IDs für die Zielgruppe mithilfe des SHA-256-Algorithmus.

1. Befolgen Sie die [[!DNL Optimizely's] Anweisungen von , um das Segment auf DSP zu ](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Fügen Sie die folgenden Informationen hinzu, um die Integration zu aktivieren:

   * **Source-Schlüssel:** Dies ist der in Schritt 2[ erstellte ](#source-create).

   * **Kontocode:** Dies ist der alphanumerische DSP-Kontocode, den Sie in DSP unter [!UICONTROL Settings] > [!UICONTROL Account] finden.

Die Segmente werden wie für den Advertiser konfiguriert aktualisiert. Unabhängig davon, wie oft das Segment aktualisiert wird, läuft die Aufnahme in ein Segment standardmäßig nach 30 Tagen oder nach einem vom Kunden angegebenen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie vor dem Ablauf erneut aus [!DNL Optimizely] pushen. Um eine benutzerdefinierte Segmentgültigkeit anzufordern, wenden Sie sich an Ihr Adobe-Account-Team.

## Schritt 4: Anzahl der universellen IDs mit der Anzahl der Hash-E-Mail-Adressen vergleichen {#compare-id-count}

Die Segmente sollten innerhalb von 24 Stunden in DSP verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein.

Überprüfen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob das Segment verfügbar ist und aufgefüllt wird, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen. Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentanzahl variieren kann, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Übersetzungsraten und Problemen mit der Benutzeranzahl finden Sie unter &quot;[ für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md).

Wenden Sie sich zur Fehlerbehebung bei Konvertierungsproblemen an Ihr Adobe-Kundenbetreuungsteam oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
