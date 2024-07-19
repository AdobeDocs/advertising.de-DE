---
title: '[!DNL Google Ads] Suchbegriffeinstellungen'
description: Verweisen Sie auf die Einstellungen für  [!DNL Google Ads] Keywords.
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Einstellungen für [!DNL Google Ads] Keywords

Sie können Suchbegriffe für Kampagnen erstellen, die die Such- und Anzeigenetzwerke verwenden.

Informationen zu den [Suchbegriffbeschränkungen pro Konto](https://support.google.com/google-ads/answer/6372658) finden Sie in der Hilfe zu Google Ads .

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Suchbegriffe, einschließlich aller [!DNL Google Ads] Übereinstimmungssyntax für Suchbegriffe und Platzhalter. [!DNL Google Ads] -Konten erfordern Suchbegriffe mit den folgenden Attributen:

* Die maximale Länge pro Keyword beträgt 80 Zeichen und höchstens 10 Wörter.
* Das Schlüsselwort darf nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: Leerzeichen `# $ & _ - " [] ' + . / :`

Sie können bis zu 2000 Suchbegriffe eingeben oder einfügen. Trennen Sie mehrere Suchbegriffe durch Kommas oder geben Sie sie in separate Zeilen ein.

>[!NOTE]
>
>* Sie können negative Suchbegriffe aus der Ansicht [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie aus den Anzeigengruppen- und Kampagneneinstellungen erstellen.
>* Wenn Sie ein [!DNL Google Ads] -Keyword oder einen Übereinstimmungstyp ändern, wird der vorhandene Suchbegriff gelöscht und ein neuer erstellt.

**[!UICONTROL Status]:** Der Anzeigestatus des Suchbegriffs: *Aktiv* oder *Angehalten*. Der Standardwert für neue Suchbegriffe ist *aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param1]:** Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL oder Tracking-Vorlage [die dynamische Ersatzzeichenfolge `{param1}`](https://support.google.com/google-ads/answer/6305348) enthält.

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL oder Tracking-Vorlage [die dynamische Ersatzzeichenfolge `{param2}`](https://support.google.com/google-ads/answer/6305348) enthält.

## URL-Optionen

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
