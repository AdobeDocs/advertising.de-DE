---
title: '''[!DNL Microsoft Advertising] Suchbegriffeinstellungen'
description: Verweisen Sie auf die Einstellungen für [!DNL Microsoft Advertising] Suchbegriffe.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Keyword-Einstellungen

Sie können Suchbegriffe für Kampagnen erstellen, die die Such- und Anzeigenetzwerke verwenden.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Suchbegriffe, einschließlich [!DNL Microsoft Advertising] Übereinstimmungssyntax und Platzhalter. Die maximale Länge pro Keyword beträgt 100 Zeichen.

Sie können bis zu 2000 Suchbegriffe eingeben oder einfügen. Trennen Sie mehrere Suchbegriffe durch Kommas oder geben Sie sie in separate Zeilen ein.

>[!NOTE]
>
>* Sie können negative Suchbegriffe aus dem [!UICONTROL Keywords] > [!UICONTROL Negatives] und in den Einstellungen für Anzeigengruppe und Kampagne anzeigen.
>* Ändern einer [!DNL Microsoft Advertising] löscht den vorhandenen Suchbegriff und erstellt einen neuen mit einer neuen Suchbegriff-ID. Beim Ändern des Übereinstimmungstyps wird jedoch der vorhandene Suchbegriff nicht gelöscht.

**[!UICONTROL Status]:** Der Anzeigestatus des Suchbegriffs: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Suchbegriffe ist *Aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL des Suchbegriffs oder der Titel, die Beschreibung oder die Basis-URL der Anzeige [die `{Param2}` dynamische Ersatzzeichenfolge](https://help.bingads.microsoft.com/#apex/3/en/53079/0). Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Anzeigenelemente, in denen Sie sie verwenden (Titel 1 und Titel 2 kombinieren können beispielsweise maximal 76 Zeichen lang sein).

**[!UICONTROL Param3]:** Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL des Suchbegriffs oder der Titel, die Beschreibung oder die Basis-URL der Anzeige [die `{Param3}` dynamische Ersatzzeichenfolge](https://help.bingads.microsoft.com/#apex/3/en/53079/0). Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Anzeigenelemente, in denen Sie sie verwenden (Titel 1 und Titel 2 kombinieren können beispielsweise maximal 76 Zeichen lang sein).

## URL-Optionen

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Dieses Feld kann optional die `{Param2}` und `{Param3}` dynamische Ersatzvariablen.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
