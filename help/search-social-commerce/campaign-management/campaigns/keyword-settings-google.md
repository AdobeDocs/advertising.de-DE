---
title: '''[!DNL Google Ads] Suchbegriffeinstellungen'
description: Verweisen Sie auf die Einstellungen für [!DNL Google Ads] Suchbegriffe.
exl-id: 8834e852-214b-4b2c-9a95-4b1c802e800d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# [!DNL Google Ads] Keyword-Einstellungen

Sie können Suchbegriffe für Kampagnen erstellen, die die Such- und Anzeigenetzwerke verwenden.

Weitere Informationen finden Sie in der Hilfe zu Google Ads für [Suchbegriffbeschränkungen pro Konto](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Suchbegriffe, einschließlich [!DNL Google Ads] Übereinstimmungssyntax für Suchbegriffe und Platzhalter. [!DNL Google Ads] -Konten erfordern Suchbegriffe mit den folgenden Attributen:

* Die maximale Länge pro Keyword beträgt 80 Zeichen und höchstens 10 Wörter.
* Das Schlüsselwort darf nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: Leerzeichen `# $ & _ - " [] ' + . / :`

Sie können bis zu 2000 Suchbegriffe eingeben oder einfügen. Trennen Sie mehrere Suchbegriffe durch Kommas oder geben Sie sie in separate Zeilen ein.

>[!NOTE]
>
>* Sie können negative Suchbegriffe aus dem [!UICONTROL Keywords] > [!UICONTROL Negatives] und in den Einstellungen für Anzeigengruppe und Kampagne anzeigen.
>* Ändern einer [!DNL Google Ads] Suchbegriff oder Übereinstimmungstyp löscht den vorhandenen Suchbegriff und erstellt einen neuen.

**[!UICONTROL Status]:** Der Anzeigestatus des Suchbegriffs: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Suchbegriffe ist *Aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param1]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL oder die Tracking-Vorlage [die `{param1}`](https://support.google.com/google-ads/answer/6305348) dynamische Ersatzzeichenfolge.

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL oder die Tracking-Vorlage [die `{param2}`](https://support.google.com/google-ads/answer/6305348) dynamische Ersatzzeichenfolge.

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
