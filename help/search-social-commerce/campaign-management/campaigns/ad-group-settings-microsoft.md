---
title: "[!DNL Microsoft Advertising] Anzeigengruppeneinstellungen"
description: Verweisen Sie auf die Einstellungen für [!DNL Microsoft Advertising] Anzeigengruppen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Anzeigengruppeneinstellungen

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ein Anzeigengruppenname, der innerhalb der Kampagne eindeutig ist. Die maximale Länge beträgt 128 Zeichen.

**[!UICONTROL Status]:** Der Anzeigestatus der Anzeigengruppe: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Anzeigengruppen ist *Aktiv*.

**[!UICONTROL Ad Language]:** Die Zielsprache für Anzeigen.<!-- Which campaign types? Not there for audience image-based ad groups. -->

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** Wie und wo innerhalb der Anzeigengruppe Anzeigen platziert werden:

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (Standardeinstellung): Platzieren von Angeboten für Anzeigen im Suchnetzwerk.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* So platzieren Sie Gebote für Anzeigen auf Syndizierte Partner-Sites.

* *[!UICONTROL Content network]:* Veraltet

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Veraltet

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Zielgruppen-Anzeigengruppen) Ob:

* *[!UICONTROL Target and Bid]:* So zeigen Sie Anzeigen nur Benutzern an, die mit Zielgruppen verknüpft sind, die auch andere Ziele für die Anzeigengruppe erfüllen.

* *[!UICONTROL Bid Only]:* Anzeigen auch für Personen anzeigen, die nicht mit Zielgruppen verbunden sind, solange sie andere Ziele auf Anzeigengruppenebene erfüllen. Sie können die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie jedoch höhere Angebote für diese Zielgruppen festlegen.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Für [!DNL Microsoft Advertising] Anzeigengruppen im Zielgruppennetzwerk werden Gebotsmodifikatoren für Standortziele nicht in Standard-Portfolios mit dem Wert[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Zielgruppe und Gruppen; (optional) Spezifische Geschlechter, die als Ziele ein- oder ausgeschlossen werden sollen: *[!UICONTROL Male]*, *[!UICONTROL Female]* und *[!UICONTROL Unknown]*. Standardmäßig werden alle Geschlechter angesprochen. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte als Ziel auszuwählen, dürfen Sie keine Werte auswählen.

* Um einen Wert einzuschließen, klicken Sie einmal auf den Kreis neben ihm, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt. Optional können Sie Angebote für jedes ausgewählte Geschlecht um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den Kreis neben dem Wert, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt.

**[!UICONTROL Age]:** (Zielgruppe und Gruppen; (optional) Spezifische Alterskategorien, die als Zielgruppen ein- oder ausgeschlossen werden sollen: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* und *[!UICONTROL Unknown]*. Standardmäßig werden alle Altersgruppen angesprochen. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte als Ziel auszuwählen, dürfen Sie keine Werte auswählen.

* Um einen Wert einzuschließen, klicken Sie einmal auf den Kreis neben ihm, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt. Optional können Sie die Angebote für jede Zielseite um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den Kreis neben dem Wert, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt.

**[!UICONTROL Industry]:** (Zielgruppe und Gruppen; (optional) Bestimmte Wirtschaftszweige, die als Zielgruppen ein- oder ausgeschlossen werden sollen. Standardmäßig werden alle Branchen angesprochen. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte als Ziel auszuwählen, dürfen Sie keine Werte auswählen.

* Um einen Wert einzuschließen, klicken Sie einmal auf den Kreis neben ihm, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt. Optional können Sie die Angebote um einen bestimmten Prozentsatz für jede Branche erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den Kreis neben dem Wert, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt.

**[!UICONTROL Job Function Targets]:** (Zielgruppe und Gruppen; (optional) Spezifische Auftragsfunktionen, die als Ziele ein- oder ausgeschlossen werden. Standardmäßig werden alle Auftragsfunktionen angesprochen. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte als Ziel auszuwählen, dürfen Sie keine Werte auswählen.

* Um einen Wert einzuschließen, klicken Sie einmal auf den Kreis neben ihm, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt. Optional können Sie die Angebote um einen bestimmten Prozentsatz für jede ausgewählte Auftragsfunktion erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den Kreis neben dem Wert, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Nur Kampagnen im Display/nativen Netzwerk; optional) Sites im Display-Netzwerk, auf denen Ihre Anzeigen nicht angezeigt werden sollen. Geben Sie eine gültige URL ein, z. B. www.example.com. Um mehrere Zeichenfolgen anzugeben, trennen Sie sie durch Kommas oder geben Sie sie in separate Zeilen ein.

Informationen zur Verfügbarkeit finden Sie in der Microsoft Advertising-Hilfe unter[Verhindern der Anzeige von Anzeigen auf bestimmten Websites](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigengruppen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)

