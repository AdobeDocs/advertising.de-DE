---
title: '[!DNL Google Ads] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für  [!DNL Google Ads] -Keywords.
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/XwutnbHVQrg8mfimzVjv-Px6OeUsOWzT7-347-ff2C0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b2ff290c2cee19c8acdc8001433189ea9bdbf83f
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 0%

---

# [!DNL Google Ads] Schlüsselworteinstellungen

Sie können Keywords für Kampagnen erstellen, die die Such- und Anzeigennetzwerke verwenden.

Siehe die [!DNL Google Ads]-Hilfe für [Keyword-Limits pro Konto](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Schlüsselwörter, einschließlich aller [!DNL Google Ads], stimmen mit der Syntax für Schlüsselwörter und Platzhalter überein. [!DNL Google Ads]-Konten erfordern Schlüsselwörter mit den folgenden Attributen:

* Die maximale Länge pro Keyword beträgt 80 Zeichen und maximal 10 Wörter.
* Das Keyword darf nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: `# $ & _ - " [] ' + . / :`

Sie können bis zu 2.000 Keywords eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein.

>[!NOTE]
>
>* Negative Keywords können in der Ansicht [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie in den Anzeigengruppen- und Kampagneneinstellungen erstellt werden.
>* Wenn Sie ein [!DNL Google Ads] Schlüsselwort oder einen Übereinstimmungstyp ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues erstellt.

**[!UICONTROL Status]:** Der Anzeigestatus des Keywords: *Aktiv* oder *Paused*. Der Standardwert für neue Keywords ist *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param1]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL oder Tracking-Vorlage [die dynamische `{param1}`](https://support.google.com/google-ads/answer/6305348)-Ersatzzeichenfolge“ enthält.

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL oder Tracking-Vorlage [die dynamische `{param2}`](https://support.google.com/google-ads/answer/6305348)-Ersatzzeichenfolge“ enthält.

## URL-Optionen

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
