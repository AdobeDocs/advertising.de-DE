---
title: Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte
description: Erfahren Sie, wie Sie Segmente erstellen, um IDs aus CCPA-Opt-out-Anfragen zu verfolgen, und wie Sie Berichte zu den IDs abrufen können.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte

Sie können Benutzer-IDs aus Verbraucher-Opt-out-Kaufanfragen auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) verfolgen, indem Sie [ein Segment für das CCPA-Opt-out-Verkauf erstellen und implementieren](ccpa-opt-out-segment-create.md). Benutzende bleiben auf unbestimmte Zeit in CCPA-Opt-out-of-Sale-Segmenten.

Sobald das Segment-Pixel-Tag implementiert ist, beginnt Adobe Advertising im Namen des Werbetreibenden mit der Erfassung eines Pools von IDs.

## Berichte zum Verbraucher-Opt-out vom Verkauf

Adobe Advertising generiert monatliche Berichte zu IDs, die Kunden für Opt-out-Kaufanfragen für das Konto gesendet haben. Die Daten konsolidieren Anfragen, die mit CCPA-Opt-out-of-Sale-Segmenten erfasst wurden, die in DSP erstellt wurden, sowie alle Übermittlungen, die über die Privacy Service-API vorgenommen wurden.  Berichte werden am ersten eines jeden Monats für den vorherigen Monat generiert. Beispielsweise ist die monatliche Benutzerliste für Juni am 1. Juli verfügbar.

Jeder Bericht ist als tabulatorgetrennte Textdatei verfügbar, die im GZIP-Format komprimiert ist. In CCPA-Opt-out-of-Sale-Segmenten erfasste Benutzer-IDs werden nach Segment und Advertiser identifiziert.

Sie können [Links zu den monatlichen Berichten](ccpa-opt-out-segment-report-retrieve.md) abrufen, die in den letzten drei Monaten erstellt wurden, entweder über die DSP oder mithilfe der DSP-[!DNL Trafficking API]. Jeder Link ist sieben Tage lang gültig, wird jedoch jedes Mal aktualisiert, wenn ein Kunde versucht, einen abzurufen.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Verbraucher-Opt-out-Unterstützung](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Abrufen von Berichten zum Verbraucher-Opt-out vom Verkauf](ccpa-opt-out-segment-report-retrieve.md)
>* [Über die Zielgruppenverwaltung](audience-about.md)
