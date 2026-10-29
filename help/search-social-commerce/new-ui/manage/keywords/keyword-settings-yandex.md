---
title: '[!DNL Yandex] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für [!DNL Yandex] Schlüsselwörter.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%
---
# [!DNL Yandex] Schlüsselworteinstellungen

[!DNL Yandex] Keywords werden sowohl für Such- als auch für Display-Netzwerke (Content-Netzwerke) verwendet.

## [!UICONTROL Basic Settings]

*Nur neue Keywords*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne.

**[!UICONTROL Ad Group]:** Die Anzeigengruppe.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Keyword-Phrasen, einschließlich [[!DNL Yandex]  (Syntax vom Typ Übereinstimmung](https://yandex.com/support/direct/keywords/symbols-and-operators.html) für Keywords. Jedes Keyword kann maximal sieben Wörter enthalten, wobei Stoppwörter ausgeschlossen sind.

Sie können bis zu 2.000 Keywords eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein.

>[!NOTE]
>
>* Wenn Sie ein [!DNL Yandex] Schlüsselwort oder einen Übereinstimmungstyp ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues erstellt.
>* Jede [!DNL Yandex] Anzeigengruppe kann maximal 200 Keywords enthalten.

**[!UICONTROL Status]:** Der Anzeigestatus des Keywords: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*. Die Standardeinstellung für neue Schlüsselwörter ist *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>Sonderzeichen werden automatisch in UTF-8 kodiert. Wenn beispielsweise die zugehörige Anzeige eine Basis-URL von `http://www.example.com/{param1}` hat und der Wert auf Schlüsselwortebene von `{param1}` `shoes/flats.html` ist, führt die Anzeige zu `http://www.example.com/shoes%2Fflats.html`.

**[!UICONTROL Param1]:** Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL die `{param1}` dynamische Ersatzzeichenfolge für Anzeigen und Sitelinks enthält, wenn das Schlüsselwort zur Anzeige der Anzeige verwendet wird. Die maximale Länge beträgt 255 Byte.

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL die `{param2}` dynamische Ersatzzeichenfolge für Anzeigen und Sitelinks enthält, wenn das Schlüsselwort zur Anzeige der Anzeige verwendet wird. Die maximale Länge beträgt 255 Byte.

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](keyword-manage.md)
