---
title: '[!DNL Yandex] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für  [!DNL Yandex] -Keywords.
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# [!DNL Yandex] Schlüsselworteinstellungen

Yandex Schlüsselwörter werden sowohl für Such- als auch für Display (Inhalts) Netzwerke verwendet.

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Keyword-Phrasen, einschließlich [Yandex-Match-Typ-Syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html) für Keywords. Jedes Keyword kann maximal sieben Wörter enthalten, wobei Stoppwörter ausgeschlossen sind.

Sie können bis zu 2.000 Keywords eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein.

>[!NOTE]
>
>* Wenn Sie ein [!DNL Yandex] Schlüsselwort oder einen Übereinstimmungstyp ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues erstellt.
>* Jede Yandex Werbegruppe kann maximal 200 Keywords enthalten.

**[!UICONTROL Status]:** Der Anzeigestatus des Keywords: *Aktiv* oder *Paused*. Der Standardwert für neue Keywords ist *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** Der Wert der `{param1}`- und `{param2}`-Substitutionsvariablen, die alle Instanzen von {param1} und {param2} in der Basis-URL für Anzeigen und Sitelinks ersetzen, wenn das Keyword zur Anzeige der Anzeige verwendet wird. Die maximale Länge beträgt 255 Byte.

Sonderzeichen werden automatisch in UTF-8 kodiert. Wenn beispielsweise die zugehörige Anzeige eine Basis-URL von &quot;http://www.example.com/&quot; {param1} und der Wert auf Schlüsselwortebene von &quot;{param1}&quot; shoes/flats.html lautet, führt die Anzeige zu http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
