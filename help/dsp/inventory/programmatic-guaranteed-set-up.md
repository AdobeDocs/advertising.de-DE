---
title: Programmgesteuerte garantierte Vereinbarung einrichten
description: Erfahren Sie, wie Sie einen programmgesteuert garantierten (PG) Deal einrichten, den Sie mit einem Publisher ausgehandelt haben.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Programmgesteuerte garantierte Vereinbarung einrichten

*[Nur unterstützte Plattformen auf der Angebotsseite](programmatic-guaranteed-about.md)*

Nachdem Sie einen programmgesteuert garantierten (PG) Deal mit einem unterstützten Herausgeber ausgehandelt haben, können Sie den Deal in DSP einrichten, indem Sie entweder die [!DNL Deal ID inbox] verwenden oder die Deal-Details manuell eingeben.

>[!NOTE]
>
> Bei PG-Angeboten übernimmt der Herausgeber das gesamte Budget, die Budgetbegrenzung und die Zielgruppenbestimmung. Alle SSPs, die PG über DSP zulassen, bestätigen, dass der Herausgeber eine Budgetbegrenzung einrichten kann.
>
> Das Einrichten programmgesteuerter garantierter Abschlüsse mit Herausgebern auf [!DNL FreeWheel] erfordert zusätzliche Berechtigungen und Schritte. Weitere Informationen finden [&#x200B; unter „Überblick über das Einrichten programmgesteuerter garantierter  [!DNL FreeWheel]](freewheel-overview.md) in“.

## Erstellen eines programmgesteuerten garantierten Angebots mithilfe des [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Die folgende Methode ist das bevorzugte Verfahren für [!DNL FreeWheel], [!DNL Google Authorized Buyers] und [!DNL Magnite DV+].

1. [Akzeptiere den Deal](deal-id-inbox-accept.md).

1. Nachdem Sie den Deal gespeichert haben, wählen Sie die Anzeigen (oder 1x1 Tracking-Pixel für Publisher-verwaltete Anzeigen) aus, die für den Deal verwendet werden sollen, und erstellen Sie nach Aufforderung eine programmgesteuerte garantierte (PG) Standardplatzierung.

   Die Erstellung einer standardmäßigen PG-Platzierung für den Abschluss ist obligatorisch, um 100 % Ihres Kaufs zu liefern. Diese Platzierung hat keine Zielgruppenbestimmung, sodass DSP an jede Bid-Anfrage des Publishers ein Angebot zurückgeben kann.

   * Wenn Sie einen einzelnen Deal akzeptieren, werden Sie automatisch zum Workflow für die Erstellung von PG-Standardplatzierungen weitergeleitet.

     Alle [!DNL FreeWheel] Angebote werden als ein einziges Angebot unterbreitet.

   * Wenn Sie ein Angebot mit mehreren PG-Angebots-IDs akzeptieren, identifizieren Sie jede PG-Standardplatzierung, die Sie erstellen müssen. Nachdem Sie alle erforderlichen Platzierungen erstellt haben, ist die Schaltfläche „Weiter“ aktiviert.

1. (Optional) Targeting des PG-Angebots in zusätzlichen PG- oder Nicht-PG-Platzierungen durch Klicken auf ![Optionsmenü](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Ein Angebot kann mehrere Platzierungen ansprechen, die eine beliebige Kombination von Medientypen unterstützen (z. B. vernetztes TV, Desktop und Audio).

## Manuelles Einrichten eines programmgesteuerten garantierten Angebots

Verwenden Sie diese Methode für alle anderen SSPs.

1. [Richten Sie die Details der Angebots-ID manuell &#x200B;](deal-id-create.md).

1. Nachdem Sie den Deal gespeichert haben, wählen Sie die Anzeigen (oder 1x1 Tracking-Pixel für Publisher-verwaltete Anzeigen) aus, die für den Deal verwendet werden sollen, und erstellen Sie eine PG-Standardplatzierung, wie Sie dazu aufgefordert werden.

   Die Erstellung einer PG-Standardplatzierung für den Abschluss ist obligatorisch, um 100 % Ihres Kaufs zu liefern. Diese Platzierung hat keine Zielgruppenbestimmung, sodass DSP an jede Bid-Anfrage des Publishers ein Angebot zurückgeben kann.

1. (Optional) Targeting des PG-Angebots in zusätzlichen PG- oder Nicht-PG-Platzierungen durch Klicken auf ![Optionsmenü](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Ein Angebot kann mehrere Platzierungen ansprechen, die eine beliebige Kombination von Medientypen unterstützen (z. B. vernetztes TV, Desktop und Audio).

>[!MORELIKETHIS]
>
>* [Über programmgesteuerte garantierte -Angebote](programmatic-guaranteed-about.md)
>* [Tipps für die Aushandlung eines programmgesteuerten garantierten Deals](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Senden einer Anzeige für einen programmgesteuerten garantierten Deal mit [!DNL FreeWheel]](freewheel-submit.md)
>* [Akzeptieren eines Angebots im Angebots-ID-Posteingang](deal-id-inbox-accept.md)
>* [Details zur Angebots-ID manuell erstellen](deal-id-create.md)
>* [SSP-Partner](ssp-partners.md)
>* [Übersicht über die Inventar-Funktionen](inventory-overview.md)
