---
title: "Konvertieren von Benutzer-IDs aus [!DNL ActionIQ] zu universellen IDs"
description: "Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL ActionIQ] Erstanbietersegmente."
feature: DSP Audiences
source-git-commit: ecab6e81575128718156bb0bde1a5ea33a21d5f0
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL ActionIQ] zu universellen IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL ActionIQ] Kundendatenplattform zur Konvertierung Ihrer Hash-E-Mail-Adressen in universelle IDs für zielgerichtete Werbung.

Es gibt <!-- NN --> Schritte zum Freigeben von Daten aus [!DNL ActionIQ] mit DSP:

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. ?

## Schritt 1: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen einer Zielgruppenquelle](source-create.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren, wobei die [universelle ID-Formate](source-about.md) in die Sie Ihre Benutzer-IDs konvertieren möchten.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quellcode-Schlüssel für die [!DNL ActionIQ] Benutzer.

1. Nachdem Sie alle Schritte ausgeführt haben, überprüfen Sie diese in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe aus [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierungseinstellungen), die das Segment innerhalb von 24 Stunden füllt. Vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen.

   Die Übersetzungsrate von Hash-E-Mail-Adressen in universelle IDs sollte über 90 % liegen. Wenn Sie beispielsweise 100 Hash-E-Mail-Adressen von Ihrer Kundendatenplattform senden, sollten diese in mehr als 90 universelle IDs übersetzt werden. Eine Übersetzungsrate von 90 % oder weniger ist ein Problem. Weitere Informationen dazu, wie die Segmentzählungen variieren können, finden Sie unter[Ursachen für Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).&quot;

   Wenden Sie sich zur Fehlerbehebung an Ihr Adobe-Account-Team oder `adcloud-support@adobe.com`.

Segmente werden alle 24 Stunden aktualisiert.

## Schritt 2:

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Erstellen einer Zielgruppenquelle zur Aktivierung von universellen ID-Zielgruppen](source-create.md)
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Konvertieren von Benutzer-IDs aus [!DNL Adobe Real-Time CDP] zu universellen IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs aus [!DNL Tealium] zu universellen IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
