---
title: "Konvertieren von Benutzer-IDs von  [!DNL ActionIQ] in universelle IDs"
description: '"Erfahren Sie, wie Sie DSP aktivieren, um Ihre Erstanbietersegmente zu erfassen." [!DNL ActionIQ] '
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs von [!DNL ActionIQ] in universelle IDs

*Beta-Funktion*

Verwenden Sie die DSP Integration mit der [!DNL ActionIQ]-Kundendatenplattform, um Ihre Hash-E-Mail-Adressen in universelle IDs für zielgerichtete Werbung zu konvertieren.

Es gibt <!-- NN --> Schritte zum Freigeben von Daten aus [!DNL ActionIQ] für DSP:

1. [Erstellen Sie eine Zielgruppenquelle in DSP](#source-create).

1. ?

## Schritt 1: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen Sie eine Zielgruppenquelle](source-manage.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren. Geben Sie dabei die [universellen ID-Formate](source-about.md) an, in die Sie Ihre Benutzerkennung konvertieren möchten.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für den Benutzer [!DNL ActionIQ] frei.

## Schritt 2:

## Schritt 3:

1. Überprüfen Sie in Ihrer Zielgruppenbibliothek (die beim Erstellen oder Bearbeiten einer Zielgruppe über &quot;[!UICONTROL Audiences] > [!UICONTROL All Audiences]&quot;oder in den Platzierungseinstellungen verfügbar ist), ob das Segment gefüllt wird, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen.

   Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein. Weitere Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentzahlen variieren können, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances)&quot;.

Segmente werden alle 24 Stunden aktualisiert.

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Problemen mit der Übersetzungsrate und der Benutzeranzahl finden Sie unter &quot;[Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md)&quot;.

Wenden Sie sich zur Fehlerbehebung bei Problemen mit dem Konvertierungsverfahren an Ihr Adobe Account-Team oder an `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Adobe Real-Time CDP] in universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Tealium] in universelle IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
