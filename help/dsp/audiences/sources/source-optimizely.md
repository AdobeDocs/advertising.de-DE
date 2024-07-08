---
title: Konvertieren von Benutzer-IDs aus [!DNL Optimizely] zu universellen IDs
description: Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL Optimizely] Erstanbietersegmente.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 31713da81bbb1eb840de0f8e0d40013b42cd3140
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Optimizely] zu universellen IDs

*Beta-Funktion*

Verwenden Sie die DSP Integration mit der [!DNL Optimizely] Kundendatenplattform, um die Erstanbieter-E-Mail-Adressen Ihres Unternehmens mit Hash in universelle IDs für Zielgruppengerechte Werbung zu konvertieren.

1. (Um E-Mail-Adressen konvertieren an [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Werbetreibende mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Festlegen bis zu Tracking, um die Messung](#analytics-tracking) zu ermöglichen [!DNL Analytics] .

1. [Erstellen eine Zielgruppe Quelle in DSP](#source-create).

1. [Bereiten Sie die Segment Daten](#push-data) vor und übertragen Sie sie.

1. [Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der E-Mail-Adressen](#compare-id-count) mit Hash.

## Schritt 1: Festlegen Tracking für [!DNL Analytics] die Messung {#analytics-tracking}

*Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Konvertieren von E-Mail-Adressen in [!DNL RampIDs] oder [!DNL ID5] IDs verwenden, müssen Sie Folgendes tun:

1. (Wenn Sie dies noch nicht getan haben) Führen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und stellen Sie sicher, dass die Variable [AMO-ID und EF ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs aufgefüllt werden.

1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie universellen ID-spezifischen Code auf Ihren Webseiten bereit, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) für Durchsichten zuzuordnen:

   * **Für [!DNL RampIDs]:** Sie müssen auf Ihren Webseiten ein zusätzliches JavaScript-Tag bereitstellen, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) zu ermöglichen, Durchsichten anzuzeigen. Wenden Sie sich an Ihr Adobe Systems Account Team, das Ihnen Anweisungen gibt, wie Sie sich für eine [!DNL LiveRamp] [!DNL LaunchPad] Tag von [!DNL LiveRamp] Authentication Traffic Solutions registrieren können. Die Registrierung ist gratis, Sie müssen jedoch eine Vereinbarung unterzeichnen. Sobald Sie sich registriert haben, generiert Ihr Adobe Systems-Account-Team eine eindeutige Tag für Ihre Organisation, die Sie auf Ihren Webseiten implementieren können.

## Schritt 2: Erstellen einer Zielgruppe Quelle in DSP {#source-create}

1. [Erstellen eine Zielgruppe Quelle](source-manage.md) , um Zielgruppen in Ihre DSP Konto oder ein Advertiser Konto zu importieren. Sie können Ihre User-IDs in einem der [verfügbaren universellen ID-Formate](source-about.md) konvertieren.

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, mit dem Sie die Segment Daten übertragen.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für die [!DNL Optimizely] Benutzer.

## Schritt 3: Segmentdaten vorbereiten und pushen {#push-data}

Der Werbetreibende muss die Daten mithilfe der [!DNL Optimizely Data Platform]. Wenden Sie sich bei Fragen zum Prozess an Ihren [!DNL Optimizely] Vertreter.

1. Within [!DNL Optimizely Data Platform], Hash die E-Mail-IDs für die Zielgruppe mithilfe des SHA-256-Algorithmus.

1. Folgen [[!DNL Optimizely's] Anweisungen zum Senden des Segments an DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Fügen Sie die folgenden Informationen hinzu, um die Integration zu aktivieren:

   * **Quelle Schlüssel:** Dies ist der in [Schritt 2](#source-create) erstellte Quellschlüssel.

   * **Konto Symbol:** Dies ist das alphanumerische DSP Konto Symbol, das Sie unter DSP unter [!UICONTROL Settings] > [!UICONTROL Account]finden.

Die Segmente sollten innerhalb von 24 Stunden in DSP verfügbar sein und werden entsprechend der Konfiguration für die Advertiser aktualisiert. Unabhängig davon, wie häufig die Segment aktualisiert wird, läuft die Aufnahme in eine Segment standardmäßig nach 30 Tagen oder nach einem vom Kunden angegebenen Gültigkeit Zeitraum ab. Aktualisieren Ihre Segmente, indem Sie sie vor [!DNL Optimizely] der Gültigkeit erneut verschieben. Wenden Sie sich an Ihr Adobe Systems Account-Team, um eine benutzerdefinierte Segment Gültigkeit zu Anfrage.

## Schritt 4: Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der gehashten E-Mail-Adressen {#compare-id-count}

Nachdem Sie alle Schritte ausgeführt haben, überprüfen Sie in Ihrem Zielgruppenbibliothek (das verfügbar ist, wenn Sie eine Zielgruppe in [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierung Einstellungen erstellen oder bearbeiten), ob die Segment verfügbar ist und innerhalb von 24 Stunden aufgefüllt wird. Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen.

Die Übersetzungsrate von Hash-E-Mail-Adressen in universelle IDs sollte über 90 % liegen. Wenn Sie beispielsweise 100 Hash-E-Mail-Adressen von Ihrer Kundendatenplattform senden, sollten diese in mehr als 90 universelle IDs übersetzt werden. Eine Übersetzungsrate von 90 % oder weniger ist ein Problem. Weitere Informationen dazu, wie die Segmentzählungen variieren können, finden Sie unter[Ursachen für Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).&quot;

Wenden Sie sich zur Fehlerbehebung an Ihr Adobe-Account-Team oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informationen zu Erstanbieter-Audience Quellen](/help/dsp/audiences/sources/source-about.md)
>* [Audience Quellen verwalten, um universelle ID-Audiences zu aktivieren](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über Audience Management](/help/dsp/audiences/audience-about.md)
