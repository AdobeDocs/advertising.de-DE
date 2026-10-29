---
title: '[!DNL Google Ads] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für [!DNL Google Ads] Schlüsselwörter.
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%
---
# [!DNL Google Ads] Schlüsselworteinstellungen

Sie können Keywords für Kampagnen erstellen, die die Such- und Anzeigennetzwerke verwenden.

Siehe die [!DNL Google Ads]-Hilfe für [Keyword-Limits pro Konto](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Basic Settings]

*Nur neue Keywords*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne.

**[!UICONTROL Ad Group]:** Die Anzeigengruppe.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Schlüsselwörter, einschließlich aller [!DNL Google Ads], stimmen mit der Syntax für Schlüsselwörter und Platzhalter überein. [!DNL Google Ads]-Konten erfordern Schlüsselwörter mit den folgenden Attributen:

* Die maximale Länge pro Keyword beträgt 80 Zeichen und maximal 10 Wörter.

* Das Keyword darf nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: `# $ & _ - " [] ' + . / :`

Sie können bis zu 2.000 Keywords eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein.

>[!NOTE]
>
>* Negative Keywords können Sie auf der Registerkarte [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie in den Anzeigengruppen- und Kampagneneinstellungen erstellen.
>* Wenn Sie ein [!DNL Google Ads] Schlüsselwort oder einen Übereinstimmungstyp ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues erstellt.

**[!UICONTROL Status]:** Der Anzeigestatus des Keywords: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*. Die Standardeinstellung für neue Schlüsselwörter ist *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL oder Tracking-Vorlage [die dynamische `{param1}`](https://support.google.com/google-ads/answer/6305348)-Ersatzzeichenfolge“ enthält.

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL oder Tracking-Vorlage [die dynamische `{param2}`](https://support.google.com/google-ads/answer/6305348)-Ersatzzeichenfolge“ enthält.

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](keyword-manage.md)
