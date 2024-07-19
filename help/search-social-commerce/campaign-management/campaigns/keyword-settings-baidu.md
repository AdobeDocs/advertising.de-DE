---
title: '[!DNL Baidu] Suchbegriffeinstellungen'
description: Verweisen Sie auf die Einstellungen für  [!DNL Baidu] Keywords.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Einstellungen für [!DNL Baidu] Keywords

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Suchbegriffe. Die maximale Länge pro Keyword beträgt 30 Einzelbyte- oder 15 Doppelbyte-Zeichen

Sie können bis zu 2000 Suchbegriffe eingeben oder einfügen. Trennen Sie mehrere Suchbegriffe durch Kommas oder geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Syntax:

* `keyword` für breite Übereinstimmung
* `"keyword"` für Wortgruppenübereinstimmung
* `[keyword]` für genaue Übereinstimmung

>[!NOTE]
>
>* [!DNL Baidu] erlaubt nur einen Übereinstimmungstyp pro Suchbegriff pro Anzeigengruppe. Beispielsweise kann Anzeigengruppe 1 nicht sowohl `"keyword"` als auch `[keyword]` enthalten.
>* Sie können negative Suchbegriffe aus der Ansicht [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie aus den Anzeigengruppen- und Kampagneneinstellungen erstellen.
>* Wenn Sie einen [!DNL Baidu] -Suchbegriff ändern, wird der vorhandene Suchbegriff gelöscht und ein neuer mit einer neuen Suchbegriff-ID erstellt. Beim Ändern des Übereinstimmungstyps wird jedoch der vorhandene Suchbegriff nicht gelöscht.

**[!UICONTROL Status]:** Der Anzeigestatus des Suchbegriffs: *Aktiv* oder *Angehalten*. Der Standardwert für neue Suchbegriffe ist *aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL-Optionen

**[!UICONTROL Base URL]:** (Kampagnen nur mit Keyword-Level-Tracking; optional) Die Landingpage-URL, zu der Benutzer beim Klicken auf Ihre Anzeige gelangen. Sie kann Folgendes umfassen:
Umleitung und Trackingcode von Drittanbietern. Wenn Sie einen Wert eingeben, überschreibt er die Basis-URL für die Anzeige.

Nachdem Sie den Datensatz gespeichert haben, enthält die Basis-URL alle für die Kampagne oder das Konto konfigurierten Anlagenparameter.

Wenn Sie den Adobe Advertising-Konversions-Tracking-Dienst verwenden und die Kampagneneinstellungen die Verwendung von [!UICONTROL EF Redirect] und das Hinzufügen von Tracking auf Suchbegriffebene umfassen, fügt Search, Social und Commerce automatisch einen eigenen Klick-Tracking-Code hinzu.

>[!MORELIKETHIS]
>
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
