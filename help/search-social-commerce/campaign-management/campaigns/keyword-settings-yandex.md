---
title: '[!DNL Yandex] Suchbegriffeinstellungen'
description: Verweisen Sie auf die Einstellungen für  [!DNL Yandex] Keywords.
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Einstellungen für [!DNL Yandex] Keywords

Yandex-Keywords werden sowohl für Such- als auch für Display-Netzwerke (Inhalt) verwendet.

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Suchbegriffsausdrücke, einschließlich einer beliebigen Syntax vom Typ [Yandex-Übereinstimmung](https://yandex.com/support/direct/keywords/symbols-and-operators.html) für Suchbegriffe. Jeder Suchbegriff kann maximal sieben Wörter enthalten, wobei Stoppwörter ausgeschlossen sind.

Sie können bis zu 2000 Suchbegriffe eingeben oder einfügen. Trennen Sie mehrere Suchbegriffe durch Kommas oder geben Sie sie in separate Zeilen ein.

>[!NOTE]
>
>* Wenn Sie ein [!DNL Yandex] -Keyword oder einen Übereinstimmungstyp ändern, wird der vorhandene Suchbegriff gelöscht und ein neuer erstellt.
>* Jede Yandex-Anzeigengruppe kann maximal 200 Suchbegriffe enthalten.

**[!UICONTROL Status]:** Der Anzeigestatus des Suchbegriffs: *Aktiv* oder *Angehalten*. Der Standardwert für neue Suchbegriffe ist *aktiv*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** Der Wert der Ersetzungsvariablen `{param1}` und `{param2}`, die durch alle Instanzen von {param1} und {param2} in der Basis-URL für Anzeigen und Sitelinks ersetzt werden, wenn das Keyword zur Anzeige der Anzeige verwendet wird. Die maximale Länge beträgt 255 Byte.

Sonderzeichen werden automatisch in UTF-8 kodiert. Wenn die verknüpfte Anzeige beispielsweise über eine Basis-URL von &quot;http://www.example.com/{param1}&quot;verfügt und der Wert auf Suchbegriffebene von {param1} &quot;shoes/flats.html&quot;lautet, führt die Anzeige zu &quot;http://www.example.com/shoes%2Fflats.html&quot;.

>[!MORELIKETHIS]
>
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
