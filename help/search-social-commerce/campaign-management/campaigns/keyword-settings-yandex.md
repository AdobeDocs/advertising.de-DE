---
title: '''[!DNL Yandex] Suchbegriffeinstellungen'
description: Verweisen Sie auf die Einstellungen für [!DNL Yandex] Suchbegriffe.
exl-id: 276f991b-f604-445c-8dd0-481b6eaee3d2
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
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

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** Der Wert der `{param1}` und `{param2}` Ersatzvariablen, die für alle Instanzen von {param1} und {param2} in der Basis-URL für Anzeigen und Sitelinks, wenn das Keyword zur Anzeige der Anzeige verwendet wird. Die maximale Länge beträgt 255 Byte.

Sonderzeichen werden automatisch in UTF-8 kodiert. Beispiel: Die verknüpfte Anzeige hat die Basis-URL &quot;http://www.example.com/&quot;{param1} und dem Wert auf Keyword-Ebene von {param1} auf &quot;shoes/flats.html&quot;gesetzt ist, führt die Anzeige zu &quot;http://www.example.com/shoes%2Fflats.html&quot;.

>[!MORELIKETHIS]
>
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
