---
title: Einstellungen für Anzeigengruppen [!DNL Microsoft Advertising]
description: Verweisen Sie auf die Einstellungen  [!DNL Microsoft Advertising]  Anzeigengruppen.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Einstellungen für Anzeigengruppen [!DNL Microsoft Advertising]

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ein Anzeigengruppenname, der innerhalb der Kampagne eindeutig ist. Die maximale Länge beträgt 128 Zeichen.

**[!UICONTROL Status]:** Der Anzeigestatus der Anzeigengruppe: *Aktiv* oder *Paused*. Der Standardwert für neue Anzeigengruppen lautet *Aktiv*.

**[!UICONTROL Ad Language]:** (Suchkampagnen) Die Zielsprache für Anzeigen.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Suchanzeigen) Wie und wo Anzeigen innerhalb der Anzeigengruppe platziert werden:

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (Standard): Gebote für Anzeigen im Suchnetzwerk abgeben.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* Gebote für Anzeigen auf syndizierten Partnerseiten abzugeben.

* *[!UICONTROL Content network]:* veraltet

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** veraltet

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Zielgruppen-Anzeigengruppen) Ob:

* *[!UICONTROL Target and Bid]:* Anzeigen nur Benutzern anzuzeigen, die mit Zielgruppen verknüpft sind und auch andere Ziele für die Anzeigengruppe erfüllen.

* *[!UICONTROL Bid Only]:* Anzeigen auch Personen anzuzeigen, die nicht mit Zielgruppen verknüpft sind, solange sie andere Zielgruppen auf Anzeigengruppenebene erfüllen. Sie können jedoch die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie höhere Gebote für diese Zielgruppen festlegen.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Für [!DNL Microsoft Advertising] Anzeigengruppen im Zielgruppennetzwerk werden Angebotsmodifikatoren für Standortziele in Standardportfolios mit der Einstellung &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot; nicht optimiert.

**[!UICONTROL Genre]:** (Anzeigengruppen in [!UICONTROL Audience CTV Video] Kampagnen; verfügbar in USA, CA, BR, MX, UK, DE, ES, FR, IT, AU, MY und TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) Die Zielgenres, die die Sendungen und Kanäle bestimmen, auf denen Ihre Anzeigen erscheinen:

* *[!UICONTROL All genres]:* (Standard) Targeting für alle Genres.

* *[!UICONTROL Select From Below List]:* Targeting ausgewählter Genres. Wählen Sie aus der Liste aller verfügbaren Genres.

Die Platzierung der Werbung für Connected TV (CTV) hängt von Ihrer Videoqualität und der Angebotsmenge ab. Siehe [Technische Anforderungen für CTV-Anzeigen](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Zielgruppen; optional) Spezifische Geschlechter, die als Zielgruppen ein- oder ausgeschlossen werden sollen: *[!UICONTROL Male]*, *[!UICONTROL Female]* und *[!UICONTROL Unknown]*. Standardmäßig werden alle Geschlechter als Zielgruppe ausgewählt. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote für jedes ausgewählte Geschlecht optional um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

**[!UICONTROL Age]:** (Zielgruppen-Anzeigengruppen; optional) Spezifische Alterskategorien, die als Zielgruppen ein- oder ausgeschlossen werden sollen: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* und *[!UICONTROL Unknown]*. Standardmäßig werden alle Seiten als Ziel ausgewählt. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote für jedes Zielalter optional um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

**[!UICONTROL Industry]:** (Zielgruppen-Anzeigengruppen; optional) Bestimmte Branchen, die als Ziele ein- oder ausgeschlossen werden sollen. Standardmäßig sind alle Branchen angesprochen. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote für jede ausgewählte Branche optional um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

**[!UICONTROL Job Function Targets]:** (Zielgruppen-Anzeigengruppen; optional) Spezifische Aufgabenfunktionen, die als Ziele ein- oder ausgeschlossen werden sollen. Standardmäßig sind alle Auftragsfunktionen ausgewählt. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote optional für jede ausgewählte Funktion um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Optional) Die Häufigkeit, mit der einem Kunden Anzeigen aus der Anzeigengruppe bereitgestellt werden können. Geben Sie einen Wert ein und wählen Sie die Zeiteinheit (*[!UICONTROL Hour]*, *[!UICONTROL Day]* oder *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Nur Kampagnen auf der Anzeige/im nativen Netzwerk; optional) Websites auf dem Display-Netzwerk, auf denen Ihre Anzeigen nicht angezeigt werden sollen. Geben Sie eine gültige URL ein, z. B. www.example.com. Um mehrere Zeichenfolgen anzugeben, trennen Sie sie durch Kommas oder geben Sie sie in separaten Zeilen ein.

Informationen zur Verfügbarkeit finden Sie in [!DNL Microsoft Advertising] Hilfe zu &quot;[Verhindern, dass Anzeigen auf bestimmten Websites angezeigt werden](https://help.ads.microsoft.com/#apex/bae/en/14061/0).

>[!MORELIKETHIS]
>
>* [Anzeigengruppen verwalten](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
