---
title: Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte
description: Erfahren Sie, wie Sie Segmente erstellen, um IDs aus CCPA-Opt-out-Anfragen zu verfolgen, und wie Sie Berichte zu den IDs abrufen können.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
TQID: https://experienceleague.adobe.com/Bp8Fj0z7lqSXmHd-aJQa6ocQyj6FVQuydArNBucpJp4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 0%

---

# Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte

Sie können Benutzer-IDs aus Verbraucher-Opt-out-Kaufanfragen auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) verfolgen, indem Sie [ein Segment für das CCPA-Opt-out-Verkauf erstellen und implementieren](ccpa-opt-out-segment-create.md). Benutzende bleiben auf unbestimmte Zeit in CCPA-Opt-out-of-Sale-Segmenten.

Sobald das Segment-Pixel-Tag implementiert ist, beginnt Adobe Advertising mit der Erfassung eines Pools von IDs im Namen des Werbetreibenden.

## Berichte zum Verbraucher-Opt-out vom Verkauf

Adobe Advertising generiert monatliche Berichte zu IDs, die Kunden für Opt-out-Kaufanfragen für das Konto gesendet haben. Die Daten konsolidieren Anfragen, die mithilfe von in DSP erstellten CCPA-Opt-out-of-Sale-Segmenten erfasst wurden, sowie alle Übermittlungen, die über die Privacy Service-API erfolgen.  Berichte werden am ersten eines jeden Monats für den vorherigen Monat generiert. Beispielsweise ist die monatliche Benutzerliste für Juni am 1. Juli verfügbar.

Jeder Bericht ist als tabulatorgetrennte Textdatei verfügbar, die im GZIP-Format komprimiert ist. In CCPA-Opt-out-of-Sale-Segmenten erfasste Benutzer-IDs werden nach Segment und Advertiser identifiziert.

Sie können [Links zu den monatlichen Berichten](ccpa-opt-out-segment-report-retrieve.md) abrufen, die in den letzten drei Monaten erstellt wurden, entweder aus DSP oder mithilfe der DSP-[!DNL Trafficking API]. Jeder Link ist sieben Tage lang gültig, wird jedoch jedes Mal aktualisiert, wenn ein Kunde versucht, einen abzurufen.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung für Verbraucher-Opt-out vom Verkauf](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Abrufen von Opt-out-Verkaufsberichten von Kundinnen und Kunden](ccpa-opt-out-segment-report-retrieve.md)
>* [Über die Zielgruppenverwaltung](audience-about.md)
