---
title: Konvertieren von Benutzer-IDs  [!DNL Amperity]  universellen IDs
description: Erfahren Sie, wie Sie DSP für die Aufnahme  [!DNL Amperity]  Erstanbietersegmenten aktivieren.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Amperity] in universelle IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL Amperity] Kundendatenplattform, um die gehashten First-Party-E-Mail-Adressen Ihres Unternehmens in universelle IDs für zielgerichtete Werbung zu konvertieren.

1. (So konvertieren Sie E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Richten Sie das Tracking ein, um  [!DNL Analytics]  Messung zu ](#analytics-tracking).

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. [Vorbereiten und Freigeben von Segmentzuordnungsdaten](#map-data).

1. [Anfordern eines Daten-Push von  [!DNL Amperity]  zur DSP](#push-data).

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

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quell-Code-Schlüssel für den [!DNL Amperity] Benutzer frei.

## Schritt 3: Vorbereiten und Freigeben von Segmentzuordnungsdaten {#map-data}

Der Advertiser muss Segmentzuordnungsdaten vorbereiten und freigeben.

1. Erstellen Sie in [!DNL Amperity] einen Hash-Wert für die E-Mail-IDs für die Zielgruppe mithilfe des SHA-256-Algorithmus.

1. Der Werbetreibende muss Segmentzuordnungsdaten an das Adobe-Konto-Team senden, um die Segmente in DSP zu erstellen. Verwenden Sie die folgenden Spaltennamen und -werte in einer durch Kommas getrennten Wertedatei:

   * **Externer Segmentschlüssel** Der mit dem Segment verknüpfte [!DNL Amperity] Segmentschlüssel.

   * **Segmentname:** Der Segmentname.

   * **Segmentbeschreibung:** Zweck oder Regel des Segments oder beides.

   * **Übergeordnete ID:** leer lassen

   * **Video CPM:** 0

   * **CPM anzeigen:** 0

   * **Segmentfenster** Die Lebensdauer des Segments.

## Schritt 4: Daten-Push von [!DNL Amperity] an DSP anfordern {#push-data}

1. Nachdem das Segment innerhalb von DSP zugeordnet wurde, muss der Advertiser mit seinem [!DNL Amperity] zusammenarbeiten, um die Segmentdaten an DSP zu verteilen.

1. Der Werbetreibende muss dann beim Adobe-Account-Team bestätigen, dass die Segmentdaten empfangen wurden.

Die Segmente sollten innerhalb von 24 Stunden in DSP verfügbar sein. Überprüfen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob das Segment verfügbar ist und aufgefüllt wird.

Die Segmente werden wie für den Advertiser in [!DNL Amperity] konfiguriert aktualisiert. Unabhängig davon, wie oft das Segment aktualisiert wird, läuft die Aufnahme in ein Segment standardmäßig nach 30 Tagen oder nach einem vom Kunden angegebenen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie vor dem Ablauf erneut aus [!DNL Amperity] pushen. Um eine benutzerdefinierte Segmentgültigkeit anzufordern, wenden Sie sich an Ihr Adobe-Account-Team.

## Schritt 5: Anzahl der universellen IDs mit der Anzahl der Hash-E-Mail-Adressen vergleichen {#compare-id-count}

Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein.

Vergleichen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten) die Anzahl der universellen IDs mit der Anzahl der ursprünglichen gehashten E-Mail-Adressen. Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentanzahl variieren kann, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Übersetzungsraten und Problemen mit der Benutzeranzahl finden Sie unter &quot;[ für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md).

Wenden Sie sich zur Fehlerbehebung bei Konvertierungsproblemen an Ihr Adobe-Kundenbetreuungsteam oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
