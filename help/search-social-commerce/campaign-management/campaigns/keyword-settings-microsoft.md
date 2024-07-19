---
title: '[!DNL Microsoft Advertising] Suchbegriffeinstellungen'
description: Verweisen Sie auf die Einstellungen für  [!DNL Microsoft Advertising] Keywords.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Einstellungen für [!DNL Microsoft Advertising] Keywords

Sie können Suchbegriffe für Kampagnen erstellen, die die Such- und Anzeigenetzwerke verwenden.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Suchbegriffe, einschließlich aller [!DNL Microsoft Advertising], stimmen mit der Syntax und den Platzhaltern überein. Die maximale Länge pro Keyword beträgt 100 Zeichen.

Sie können bis zu 2000 Suchbegriffe eingeben oder einfügen. Trennen Sie mehrere Suchbegriffe durch Kommas oder geben Sie sie in separate Zeilen ein.

>[!NOTE]
>
>* Sie können negative Suchbegriffe aus der Ansicht [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie aus den Anzeigengruppen- und Kampagneneinstellungen erstellen.
>* Wenn Sie einen [!DNL Microsoft Advertising] -Suchbegriff ändern, wird der vorhandene Suchbegriff gelöscht und ein neuer mit einer neuen Suchbegriff-ID erstellt. Beim Ändern des Übereinstimmungstyps wird jedoch der vorhandene Suchbegriff nicht gelöscht.

**[!UICONTROL Status]:** Der Anzeigestatus des Suchbegriffs: *Aktiv* oder *Angehalten*. Der Standardwert für neue Suchbegriffe ist *aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL des Suchbegriffs oder der Titel, die Beschreibung oder die Basis-URL der Anzeige [die dynamische Ersetzungszeichenfolge `{Param2}` enthält. ](https://help.bingads.microsoft.com/#apex/3/en/53079/0) Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Anzeigenelemente, in denen Sie sie verwenden (Titel 1 und Titel 2 kombinieren können beispielsweise maximal 76 Zeichen lang sein).

**[!UICONTROL Param3]:** Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL des Suchbegriffs oder der Titel, die Beschreibung oder die Basis-URL der Anzeige [die dynamische Ersetzungszeichenfolge `{Param3}` enthält. ](https://help.bingads.microsoft.com/#apex/3/en/53079/0) Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Anzeigenelemente, in denen Sie sie verwenden (Titel 1 und Titel 2 kombinieren können beispielsweise maximal 76 Zeichen lang sein).

## URL-Optionen

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Dieses Feld kann optional die dynamischen Ersatzvariablen `{Param2}` und `{Param3}` enthalten.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
