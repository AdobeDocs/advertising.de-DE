---
title: Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte
description: Erfahren Sie mehr über das Erstellen von Segmenten zur Verfolgung von IDs aus CCPA-Opt-out-Kaufanfragen und das Abrufen von Berichten über die IDs.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte

Sie können Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) verfolgen, indem Sie [ein CCPA-Opt-out-Kaufsegment erstellen und implementieren](ccpa-opt-out-segment-create.md). Benutzer bleiben unbegrenzt in CCPA-Opt-out-Segmenten.

Sobald das Segment-Pixel-Tag implementiert ist, beginnt Adobe Advertising, einen Pool von IDs im Namen des Advertisers zu sammeln.

## Verbraucherabmeldeberichte

Adobe Advertising generiert monatliche Berichte über IDs, die Kunden für Opt-out-Kaufanfragen für das Konto eingereicht haben. Die Daten konsolidieren Anforderungen, die mithilfe von CCPA-Opt-out-Kaufsegmenten erfasst wurden, die in DSP erstellt wurden, sowie alle über die Privacy Service-API durchgeführten Übermittlungen.  Die Berichte werden am ersten eines jeden Monats für den Vormonat erstellt. Beispielsweise ist die monatliche Benutzerliste für Juni am 1. Juli verfügbar.

Jeder Bericht ist als tabulatorgetrennte Textdatei verfügbar, die in das GZIP-Format komprimiert ist. In CCPA-Opt-out-Verkaufssegmenten erfasste Benutzer-IDs werden nach Segment und Advertiser identifiziert.

Sie können [ Links zu den monatlichen Berichten abrufen](ccpa-opt-out-segment-report-retrieve.md), die in den letzten drei Monaten erstellt wurden, entweder aus DSP heraus oder mithilfe des DSP [!DNL Trafficking API]. Jeder Link ist sieben Tage lang gültig, wird jedoch jedes Mal aktualisiert, wenn ein Kunde versucht, ihn abzurufen.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung für Verbraucher-Opt-out](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Abruf der Kundenabmeldeberichte](ccpa-opt-out-segment-report-retrieve.md)
>* [Über Zielgruppen-Management](audience-about.md)
