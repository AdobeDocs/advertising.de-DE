---
title: Einrichten eines programmgesteuerten "garantierten Angebots"
description: Erfahren Sie, wie Sie einen programmgesteuerten garantierten (PG) Deal einrichten, den Sie mit einem Publisher ausgehandelt haben.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Einrichten eines programmgesteuerten &quot;garantierten Angebots&quot;

*[Nur unterstützte angebotsseitige Plattformen](programmatic-guaranteed-about.md)*

Nachdem Sie mit einem unterstützten Herausgeber einen programmgesteuerten garantierten (PG) Vertrag ausgehandelt haben, können Sie den Deal in DSP einrichten, indem Sie entweder das [!DNL Deal ID inbox] verwenden oder die Details des Deals manuell eingeben.

>[!NOTE]
>
> Bei PG-Angeboten verarbeitet der Herausgeber alle Budgetkürzungen, Budgetbegrenzungen und Targeting. Alle SSPs, die PG durch zulassen, DSP bestätigen, dass der Herausgeber eine Budgetbegrenzung einrichten kann.
>
> Das Einrichten programmgesteuerter garantierter Angebote für Herausgeber unter [!DNL FreeWheel] erfordert zusätzliche Berechtigungen und Schritte. Weitere Informationen finden Sie unter &quot;[Übersicht über das Einrichten programmgesteuerter garantierter Angebote in [!DNL FreeWheel]](freewheel-overview.md)&quot;.

## Einrichten eines programmgesteuerten garantierten Deals mit dem [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Die folgende Methode wird für [!DNL FreeWheel], [!DNL Google Authorized Buyers] und [!DNL Magnite DV+] bevorzugt.

1. [Akzeptieren Sie den Deal](deal-id-inbox-accept.md).

1. Nachdem Sie den Deal gespeichert haben, wählen Sie die Anzeigen (oder das 1x1-Tracking-Pixel für von Herausgebern verwaltete Anzeigen) aus, die für den Deal verwendet werden sollen, und erstellen Sie nach Aufforderung eine programmgesteuerte, garantierte (PG) Standardplatzierung.

   Die Erstellung einer standardmäßigen PG-Platzierung für den Deal ist obligatorisch, um 100 % Ihres Kaufs bereitzustellen. Dieser Platzierungstyp hat kein Targeting, sodass DSP jedem Angebotsantrag des Herausgebers ein Angebot zurückgeben kann.

   * Wenn Sie eine einzelne Transaktion akzeptieren, werden Sie automatisch zum Arbeitsablauf für die Erstellung der Platzierung mit PG-Standard weitergeleitet.

     Alle [!DNL FreeWheel]-Angebote werden als ein einziges Angebot vorgeschlagen.

   * Wenn Sie einen Vorschlag mit mehreren PG-Deal-IDs akzeptieren, identifizieren Sie jede PG-Standardplatzierung, die Sie erstellen müssen. Nachdem Sie alle erforderlichen Platzierungen erstellt haben, ist die Schaltfläche Weiter aktiviert.

1. (Optional) Richten Sie die PG-Transaktion in zusätzlichen PG- oder Nicht-PG-Platzierungen ein, indem Sie auf ![Menü &quot;Optionen&quot;](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]** klicken.

   Ein Deal kann mehrere Platzierungen ansprechen, die eine beliebige Kombination von Medientypen unterstützen (z. B. vernetztes Fernsehen, Desktop und Audio).

## Manuelles Einrichten eines programmatischen Garantiedeals

Verwenden Sie diese Methode für alle anderen SSPs.

1. [Richten Sie die Details der Deal-ID manuell ein](deal-id-create.md).

1. Nachdem Sie den Deal gespeichert haben, wählen Sie die Anzeigen (oder 1x1-Tracking-Pixel für von Publisher verwaltete Anzeigen) aus, die für den Deal verwendet werden sollen, und erstellen Sie nach Aufforderung eine PG-Standardplatzierung.

   Die Erstellung einer PG-Standardplatzierung für den Kauf ist obligatorisch, um 100 % Ihres Kaufs bereitzustellen. Dieser Platzierungstyp hat kein Targeting, sodass DSP jedem Angebotsantrag des Herausgebers ein Angebot zurückgeben kann.

1. (Optional) Richten Sie die PG-Transaktion in zusätzlichen PG- oder Nicht-PG-Platzierungen ein, indem Sie auf ![Menü &quot;Optionen&quot;](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]** klicken.

   Ein Deal kann mehrere Platzierungen ansprechen, die eine beliebige Kombination von Medientypen unterstützen (z. B. vernetztes Fernsehen, Desktop und Audio).

>[!MORELIKETHIS]
>
>* [Über programmgesteuerte garantierte Deals](programmatic-guaranteed-about.md)
>* [Tipps für die Aushandlung eines programmatischen Garantierten Angebots](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Senden einer Anzeige für einen programmgesteuerten garantierten Deal mit  [!DNL FreeWheel]](freewheel-submit.md)
>* [Akzeptieren eines Angebots im Posteingang der Angebots-ID](deal-id-inbox-accept.md)
>* [Manuelles Erstellen von Details zur Angebots-ID](deal-id-create.md)
>* [SSP-Partner](ssp-partners.md)
>* [Überblick über die Inventarfunktionen](inventory-overview.md)
