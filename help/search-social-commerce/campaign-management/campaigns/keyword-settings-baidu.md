---
title: "[!DNL Baidu] Suchbegriffeinstellungen"
description: Verweisen Sie auf die Einstellungen für [!DNL Baidu] Suchbegriffe.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] Keyword-Einstellungen

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Suchbegriffe. Die maximale Länge pro Keyword beträgt 30 Einzelbyte- oder 15 Doppelbyte-Zeichen

Sie können bis zu 2000 Suchbegriffe eingeben oder einfügen. Trennen Sie mehrere Suchbegriffe durch Kommas oder geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Syntax:

* `keyword` für breite Übereinstimmung
* `"keyword"` für Wortgruppenübereinstimmung
* `[keyword]` für exakte Übereinstimmung

>[!NOTE]
>
>* [!DNL Baidu] erlaubt nur einen Übereinstimmungstyp pro Suchbegriff pro Anzeigengruppe. Beispielsweise kann Anzeigengruppe 1 nicht beide `"keyword"` und `[keyword]`.
>* Sie können negative Suchbegriffe aus dem [!UICONTROL Keywords] > [!UICONTROL Negatives] und in den Einstellungen für Anzeigengruppe und Kampagne anzeigen.
>* Ändern einer [!DNL Baidu] löscht den vorhandenen Suchbegriff und erstellt einen neuen mit einer neuen Suchbegriff-ID. Beim Ändern des Übereinstimmungstyps wird jedoch der vorhandene Suchbegriff nicht gelöscht.


**[!UICONTROL Status]:** Der Anzeigestatus des Suchbegriffs: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Suchbegriffe ist *Aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL-Optionen

**[!UICONTROL Base URL]:** (Kampagnen, die nur auf Keyword-Ebene verfolgt werden; optional) Die Landingpage-URL, zu der Benutzer beim Klicken auf Ihre Anzeige weitergeleitet werden. Sie kann Umleitung und Trackingcode von Drittanbietern enthalten. Wenn Sie einen Wert eingeben, überschreibt er die Basis-URL für die Anzeige.

Nachdem Sie den Datensatz gespeichert haben, enthält die Basis-URL alle für die Kampagne oder das Konto konfigurierten Anlagenparameter.

Wenn Sie den Adobe Advertising Conversion Tracking-Dienst verwenden und die Kampagneneinstellungen die Verwendung der [!UICONTROL EF Redirect] und das Hinzufügen von Tracking auf Suchbegriffebene, fügt dann Search, Social und Commerce automatisch einen eigenen Klick-Tracking-Code hinzu.

>[!MORELIKETHIS]
>
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

