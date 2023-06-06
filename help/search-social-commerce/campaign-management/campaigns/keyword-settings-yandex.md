---
title: "[!DNL Yandex] Suchbegriffeinstellungen"
description: Verweisen Sie auf die Einstellungen für [!DNL Yandex] Suchbegriffe.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] Keyword-Einstellungen

Yandex-Keywords werden sowohl für Such- als auch für Display-Netzwerke (Inhalt) verwendet.

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Suchbegriffe, einschließlich [Yandex-Übereinstimmungstyp-Syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html) für Suchbegriffe. Jeder Suchbegriff kann maximal sieben Wörter enthalten, wobei Stoppwörter ausgeschlossen sind.

Sie können bis zu 2000 Suchbegriffe eingeben oder einfügen. Trennen Sie mehrere Suchbegriffe durch Kommas oder geben Sie sie in separate Zeilen ein.

>[!NOTE]
>
>* Ändern einer [!DNL Yandex] Suchbegriff oder Übereinstimmungstyp löscht den vorhandenen Suchbegriff und erstellt einen neuen.
>* Jede Yandex-Anzeigengruppe kann maximal 200 Suchbegriffe enthalten.


**[!UICONTROL Status]:** Der Anzeigestatus des Suchbegriffs: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Suchbegriffe ist *Aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** Der Wert der `{param1}` und `{param2}` Ersatzvariablen, die für alle Instanzen von {param1} und {param2} in der Basis-URL für Anzeigen und Sitelinks ersetzt werden, wenn das Keyword zur Anzeige der Anzeige verwendet wird. Die maximale Länge beträgt 255 Byte.

Sonderzeichen werden automatisch in UTF-8 kodiert. Wenn die verknüpfte Anzeige beispielsweise die Basis-URL &quot;http://www.example.com/{param1}&quot;hat und der Wert auf Suchbegriffebene von {param1} &quot;shoes/flats.html&quot;lautet, führt die Anzeige zu &quot;http://www.example.com/shoes%2Fflats.html&quot;.

>[!MORELIKETHIS]
>
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

