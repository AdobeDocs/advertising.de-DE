---
title: '[!DNL Microsoft Advertising] Produktgruppeneinstellungen'
description: Referenzieren Sie die Einstellungen für  [!DNL Microsoft Advertising] Einkaufsproduktgruppen.
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Produktgruppeneinstellungen

## Produktgruppen &quot;Alle Produkte&quot;

**[!UICONTROL Condition]:** (schreibgeschützt) Alle Produkte

**[!UICONTROL Bid]:** (Nur inklusive Produktgruppen) Die maximalen Kosten pro Klick (CPC), der höchste Betrag, der für einen Klick auf die Anzeige bezahlt wird. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Wertes auf Anzeigengruppenebene verwendet.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

## Alle anderen Produktgruppen

**[!UICONTROL Condition/Value]:** (Schreibgeschützt für vorhandene Produktgruppen) Die Produktdimensionen, die als Ziel dienen sollen. Geben Sie für neue Produktgruppen die Dimension an, mit der Produkte angesprochen werden sollen, und das qualifizierende Attribut für die ausgewählte Informationskategorie (z. B. &quot;Acme&quot;, wenn Sie ein Targeting nach Marke durchführen, oder &quot;Neu&quot;, wenn Sie ein Targeting nach Bedingung durchführen).

Nachdem Sie eine Produktgruppe für bestimmte Produktdimensionen erstellt haben (d. h. nicht &quot;Alle Produkte&quot;), erstellt Search, Social und Commerce automatisch eine Produktgruppe für &quot;Alles andere&quot;.

Eine Liste der verfügbaren Produktdimensionen finden Sie unter &quot;[Produktfilter für Shopping-Kampagnen](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;. Die Liste der Dimensionen kann je nach der Einstellung [!UICONTROL Inventory Filter] der Kampagne begrenzt sein.

**[!UICONTROL Excluded]:** (Optional für neue Produktgruppen; schreibgeschützt für bestehende Produktgruppen) Schließt Gebote auf Anzeigen für übereinstimmende Produkte aus.

**[!UICONTROL Bid]:** (Nur inklusive Produktgruppen) Die maximalen Kosten pro Klick (CPC), der höchste Betrag, der für einen Klick auf die Anzeige bezahlt wird. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Wertes auf Anzeigengruppenebene verwendet.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

>[!MORELIKETHIS]
>
>* [Über Einkaufsproduktgruppen](product-group-about.md)
>* [Verwalten von Einkaufsproduktgruppen](product-group-manage.md)
>* [Produktfilter für Kampagnenkampagnen](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementieren von [!DNL Microsoft Advertising] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
