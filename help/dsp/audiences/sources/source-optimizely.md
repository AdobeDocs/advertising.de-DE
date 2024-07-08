---
title: Benutzer-IDs von [!DNL Optimizely] in universelle IDs konvertieren
description: Erfahren Sie, wie Sie DSP die Aufnahme Ihrer [!DNL Optimizely] Erstanbieter-Segmente aktivieren.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# Benutzer-IDs von [!DNL Optimizely] in universelle IDs konvertieren

*Beta Funktion*

Verwenden Sie die DSP Integration mit der [!DNL Optimizely] Kundendatenplattform, um die Erstanbieter-E-Mail-Adressen Ihres Unternehmens mit Hash in universelle IDs für Zielgruppengerechte Werbung zu konvertieren.

1. (Um E-Mail-Adressen konvertieren an [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Werbetreibende mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Festlegen bis zu Tracking, um die Messung](#analytics-tracking) zu ermöglichen [!DNL Analytics] .

1. [Erstellen eine Zielgruppe Quelle in DSP](#source-create).

1. [Bereiten Sie die Segment Daten](#push-data) vor und übertragen Sie sie.

1. [Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der E-Mail-Adressen](#compare-id-count) mit Hash.

## Schritt 1: Festlegen Tracking für [!DNL Analytics] die Messung {#analytics-tracking}

*Werbetreibende mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Gehen Sie folgendermaßen vor, um E-Mail-Adressen oder [!DNL ID5] IDs zu [!DNL RampIDs] konvertieren:

1. (Falls Sie dies noch nicht getan haben) Alle Applikationen alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und stellen Sie sicher, dass die AMO-ID und die [EF-ID](/help/integrations/analytics/ids.md) in Ihren Tracking-URLs ausgefüllt werden.

1. Registrieren Sie sich bei der Universal ID-Partner und stellen Sie universellen ID-spezifischen Code auf Ihren Webseiten bereit, um Conversions von den IDs in Desktop- und mobilen Webbrowsern (aber nicht in mobilen Apps) in Ansicht-Throughs abzugleichen:

   * **Für [!DNL RampIDs]:** Sie müssen ein zusätzliches JavaScript Tag auf Ihren Webseiten bereitstellen, um Konversionen von den IDs in Desktop- und mobilen Webbrowsern (aber nicht in mobilen Apps) in Ansicht-Throughs abzugleichen. Wenden Sie sich an Ihr Adobe Systems Account Team, das Ihnen Anweisungen gibt, wie Sie sich für eine [!DNL LiveRamp] [!DNL LaunchPad] Tag von [!DNL LiveRamp] Authentication Traffic Solutions registrieren können. Die Registrierung ist gratis, Sie müssen jedoch eine Vereinbarung unterzeichnen. Sobald Sie sich registriert haben, generiert Ihr Adobe Systems-Account-Team eine eindeutige Tag für Ihre Organisation, die Sie auf Ihren Webseiten implementieren können.

## Schritt 2: Erstellen einer Zielgruppe Quelle in DSP {#source-create}

1. [Erstellen eine Zielgruppe Quelle](source-manage.md) , um Zielgruppen in Ihre DSP Konto oder ein Advertiser Konto zu importieren. Sie können Ihre User-IDs in einem der [verfügbaren universellen ID-Formate](source-about.md) konvertieren.

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, mit dem Sie die Segment Daten übertragen.

1. Nachdem Sie die Zielgruppe Quelle erstellt haben, teilen Sie den Quellcodeschlüssel mit dem [!DNL Optimizely] User.

## Schritt 3: Bereiten Sie die Segment Daten vor und übertragen Sie sie {#push-data}

Der Advertiser muss die Daten mit Hilfe seines [!DNL Optimizely] Vertreters aufbereiten und übertragen.

1. Innerhalb [!DNL Optimizely Data Platform]von Hash die E-Mail-IDs für die Zielgruppe der Advertiser mithilfe des SHA-256-Algorithmus.

1. Befolgen Sie die Anweisungen [[!DNL Optimizely's] , um das Segment auf DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads) zu verschieben. Geben Sie die folgenden Informationen an, um die Integration zu aktivieren:

   * **Quelle Schlüssel:** Dies ist der in [Schritt 2](#source-create) erstellte Quellschlüssel.

   * **Konto Symbol:** Dies ist das alphanumerische DSP Konto Symbol, das Sie unter DSP unter [!UICONTROL Settings] > [!UICONTROL Account]finden.

Die Segmente sollten innerhalb von 24 Stunden in DSP verfügbar sein und werden entsprechend der Konfiguration für die Advertiser aktualisiert. Unabhängig davon, wie häufig die Segment aktualisiert wird, läuft die Aufnahme in eine Segment standardmäßig nach 30 Tagen oder nach einem vom Kunden angegebenen Gültigkeit Zeitraum ab. Aktualisieren Ihre Segmente, indem Sie sie vor [!DNL Optimizely] der Gültigkeit erneut verschieben. Wenden Sie sich an Ihr Adobe Systems Account-Team, um eine benutzerdefinierte Segment Gültigkeit zu Anfrage.

## Schritt 4: Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der gehashten E-Mail-Adressen {#compare-id-count}

Nachdem Sie alle Schritte ausgeführt haben, überprüfen Sie in Ihrem Zielgruppenbibliothek (das verfügbar ist, wenn Sie eine Zielgruppe in [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierung Einstellungen erstellen oder bearbeiten), ob die Segment verfügbar ist und innerhalb von 24 Stunden aufgefüllt wird. Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen E-Mail-Adressen mit Hash.

Die Übersetzungsrate von E-Mail-Adressen mit Hash in universelle IDs sollte über 90 % liegen. Wenn Sie beispielsweise 100 gehashte E-Mail-Adressen von Ihrer Kundendatenplattform senden, sollten diese in mehr als 90 universelle IDs übersetzt werden. Eine Übersetzungsrate von 90 % oder weniger ist ein Problem. Weitere Informationen darüber, wie die Anzahl der Segment variieren kann, finden Sie unter &quot;[Ursachen für Daten Abweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances)&quot;.

Wenn Sie Unterstützung bei der Fehlerbehebung benötigen, wenden Sie sich an das Adobe Systems Account-Team oder `adcloud-support@adobe.com`an .

>[!MORELIKETHIS]
>
>* [Informationen zu Erstanbieter-Audience Quellen](/help/dsp/audiences/sources/source-about.md)
>* [Audience Quellen verwalten, um universelle ID-Audiences zu aktivieren](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über Audience Management](/help/dsp/audiences/audience-about.md)
