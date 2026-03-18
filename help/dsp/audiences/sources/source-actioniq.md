---
title: Konvertieren von Benutzer-IDs  [!DNL ActionIQ]  universellen IDs
description: Erfahren Sie, wie Sie DSP die Aufnahme  [!DNL ActionIQ]  Erstanbietersegmenten ermöglichen.
feature: DSP Audiences
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL ActionIQ] in universelle IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit der [!DNL ActionIQ]-Kundendatenplattform, um Ihre gehashten E-Mail-Adressen für zielgerichtete Werbung in universelle IDs zu konvertieren.

Es gibt <!-- NN --> Schritte zum Freigeben von Daten aus [!DNL ActionIQ] mit DSP:

1. [Erstellen einer Zielgruppenquelle in DSP](#source-create).

1. ?

## Schritt 1: Erstellen einer Zielgruppenquelle in DSP {#source-create}

1. [Erstellen einer Zielgruppenquelle](source-manage.md) Um Zielgruppen in Ihr DSP-Konto oder ein Advertiser-Konto zu importieren, geben Sie die [universellen ID-Formate](source-about.md) an, in die Sie Ihre Benutzerkennungen konvertieren möchten.

1. Geben Sie nach dem Erstellen der Zielgruppenquelle den Quell-Code-Schlüssel für den [!DNL ActionIQ] Benutzer frei.

## Schritt 2:

## Schritt 3:

1. Überprüfen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob das Segment aufgefüllt ist, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen.

   Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppengröße innerhalb von neun (9) Stunden sichtbar sein. Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentanzahl variieren kann, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).

Segmente werden alle 24 Stunden aktualisiert.

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Übersetzungsraten und Problemen mit der Benutzeranzahl finden Sie unter &quot;[&#x200B; für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md).

Wenden Sie sich zur Fehlerbehebung bei Konvertierungsproblemen an Ihr Adobe-Account-Team oder an `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Adobe Real-Time CDP]  universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Tealium]  universelle IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
