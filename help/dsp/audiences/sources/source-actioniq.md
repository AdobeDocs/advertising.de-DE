---
title: "Konvertieren von Benutzer-IDs aus [!DNL ActionIQ] zu universellen IDs"
description: "Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL ActionIQ] Erstanbietersegmente."
feature: DSP Audiences
source-git-commit: 4292083dac92860854dca30f7897e1b0279f68ec
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL ActionIQ] zu universellen IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL ActionIQ] Kundendatenplattform zur Konvertierung Ihrer Hash-E-Mail-Adressen in universelle IDs für zielgerichtete Werbung.

Es gibt <!-- NN --> Schritte zum Freigeben von Daten aus [!DNL ActionIQ] mit DSP:

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. ?

## Schritt 1: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen einer Zielgruppenquelle](source-manage.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren, wobei die [universelle ID-Formate](source-about.md) in die Sie Ihre Benutzer-IDs konvertieren möchten.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für die [!DNL ActionIQ] Benutzer.

1. 
   <!-- ActionIQ-specific step(s) -->

1. Überprüfen Sie dies in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe aus [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierungseinstellungen), die das Segment füllt, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen.

   Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein.

   Die Übersetzungsrate von Hash-E-Mail-Adressen auf universelle IDs sollte über 90 % liegen. Die Übersetzungsrate für [!DNL RampIDs] sollte insbesondere 95 % betragen, wenn alle Hash-E-Mail-Adressen eindeutig sind. Wenn Sie beispielsweise 100 Hash-E-Mail-Adressen von Ihrer Kundendatenplattform senden, sollten diese in mindestens 95 übersetzt werden. [!DNL RampIDs] oder mehr als 90 andere Typen universeller IDs. Eine niedrigere Übersetzungsrate ist ein Problem. Weitere Informationen dazu, wie die Segmentzählungen variieren können, finden Sie unter[Ursachen für Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).&quot;

   Wenden Sie sich zur Fehlerbehebung an Ihr Adobe-Account-Team oder `adcloud-support@adobe.com`.

Segmente werden alle 24 Stunden aktualisiert.

## Schritt 2:

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Konvertieren von Benutzer-IDs aus [!DNL Adobe Real-Time CDP] zu universellen IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs aus [!DNL Tealium] zu universellen IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
