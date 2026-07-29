---
title: Einstellungen für Anzeigengruppen [!DNL Microsoft Advertising]
description: Verweisen Sie auf die Einstellungen  [!DNL Microsoft Advertising]  Anzeigengruppen.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/f-mac9RGzF4qVr7P65-9AuhWKf22tdND5XSJ1YvLWyc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 0%

---

# Einstellungen für Anzeigengruppen [!DNL Microsoft Advertising]

## \[Seitenanfang]

**[!UICONTROL Ad Group Name]:** Ein innerhalb der Kampagne eindeutiger Anzeigengruppenname.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Paused*. Der Standardwert für neue Anzeigenkampagnen lautet *Aktiv*.

## Registerkarte [!UICONTROL Basic Settings]

*Nur neue Kampagnen*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne.

## Registerkarte [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Language]:** (Suchkampagnen) Die Zielsprache für Anzeigen.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## Registerkarte [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Suchanzeigen) Wie und wo Anzeigen innerhalb der Anzeigengruppe platziert werden:

* *[!UICONTROL Only Bing and Yahoo websites]* (Standard): Gebote für Anzeigen im Suchnetzwerk abgeben.

* *[!UICONTROL Only Bing and Yahoo syndicated search partners]:* Gebote für Anzeigen auf syndizierten Partnerseiten abzugeben.

* *[!UICONTROL Content Network]:* veraltet

## Registerkarte [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** veraltet

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Zielgruppen-Anzeigengruppen) Ob:

* *[!UICONTROL Bid Only]:* Anzeigen auch Personen anzuzeigen, die nicht mit Zielgruppen verknüpft sind, solange sie andere Zielgruppen auf Anzeigengruppenebene erfüllen. Sie können jedoch die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie höhere Gebote für diese Zielgruppen festlegen.

* *[!UICONTROL Target and Bid]:* Anzeigen nur Benutzern anzuzeigen, die mit Zielgruppen verknüpft sind und auch andere Ziele für die Anzeigengruppe erfüllen.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Für [!DNL Microsoft Advertising] Anzeigengruppen im Zielgruppennetzwerk werden Angebotsmodifikatoren für Standortziele in Standardportfolios mit der Einstellung &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot; nicht optimiert.

**[!UICONTROL Genre]:** (Anzeigengruppen in [!UICONTROL Audience CTV Video] Kampagnen; verfügbar in USA, CA, BR, MX, UK, DE, ES, FR, IT, AU, MY und TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) Die Zielgenres, die die Sendungen und Kanäle bestimmen, auf denen Ihre Anzeigen erscheinen:

* *[!UICONTROL All genres]:* (Standard) Targeting für alle Genres.

* *[!UICONTROL Select From Below List]:* Targeting ausgewählter Genres. Wählen Sie aus der Liste aller verfügbaren Genres.

Die Platzierung der Werbung für Connected TV (CTV) hängt von Ihrer Videoqualität und der Angebotsmenge ab. Siehe [Technische Anforderungen für CTV-Anzeigen](https://help.ads.microsoft.com/#apex/ads/en/60102/0/ #TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Optional) Bestimmte Geschlechter, die als Ziele ein- oder ausgeschlossen werden sollen: *[!UICONTROL Male]*, *[!UICONTROL Female]* und *[!UICONTROL Unknown]*. Standardmäßig werden alle Geschlechter als Zielgruppe ausgewählt. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote für jedes ausgewählte Geschlecht optional um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

**[!UICONTROL Age]:** (Optional) Bestimmte Altersklassen, die als Zielgruppen eingeschlossen oder ausgeschlossen werden sollen: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* und *[!UICONTROL Unknown]*. Standardmäßig werden alle Seiten als Ziel ausgewählt. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote für jedes Zielalter optional um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

**[!UICONTROL Company targets]:** (Optional) Bestimmte Unternehmen aus [!DNL LinkedIn], die als Ziele ein- oder ausgeschlossen werden sollen. Standardmäßig sind alle Unternehmen als Zielgruppe ausgewählt. Um die Zielgruppenbestimmung einzugrenzen, suchen und wählen Sie einzelne Unternehmen und mittlere Unternehmen aus. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote für jedes Zielunternehmen optional um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

**[!UICONTROL Industry]:** (Optional) Bestimmte Branchen aus [!DNL LinkedIn], die als Ziele ein- oder ausgeschlossen werden sollen. Standardmäßig sind alle Branchen angesprochen. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote für jede ausgewählte Branche optional um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

**[!UICONTROL Job Function Targets]:** (Optional) Spezifische Aufgabenfunktionen aus [!DNL LinkedIn], die als Ziele ein- oder ausgeschlossen werden sollen. Standardmäßig sind alle Auftragsfunktionen ausgewählt. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Werte auszuwählen, wählen Sie keine Werte aus.

* Um einen Wert einzuschließen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird. Sie können die Gebote optional für jede ausgewählte Funktion um einen bestimmten Prozentsatz erhöhen oder verringern.

* Um einen Wert auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

## Registerkarte [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## Registerkarte [!UICONTROL Additional Ad Group Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

### [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Nur Kampagnen auf der Anzeige/im nativen Netzwerk; optional) Websites auf dem Display-Netzwerk, auf denen Ihre Anzeigen nicht angezeigt werden sollen. Geben Sie eine gültige URL ein, z. B. www.example.com. Um mehrere Zeichenfolgen anzugeben, trennen Sie sie durch Kommas oder geben Sie sie in separaten Zeilen ein.

Informationen zur Verfügbarkeit finden Sie in [!DNL Microsoft Advertising] Hilfe zu &quot;[Verhindern, dass Anzeigen auf bestimmten Websites angezeigt werden](https://help.ads.microsoft.com/#apex/bae/en/14061/0).

### [!UICONTROL Ad Group Frequency Cap Settings]

(Optional) Die Häufigkeit, mit der eine Kundin oder ein Kunde Anzeigen aus der Anzeigengruppe erhalten kann. Geben Sie einen Wert ein und wählen Sie die Zeiteinheit (*[!UICONTROL Hour]*, *[!UICONTROL Day]*, *[!UICONTROL Week]*) oder *[!UICONTROL Month]*).

>[!MORELIKETHIS]
>
>* [Anzeigengruppen verwalten](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
