---
title: '[!DNL Microsoft Advertising] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für [!DNL Microsoft Advertising] Schlüsselwörter.
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
source-wordcount: '281'
ht-degree: 0%
---
# [!DNL Microsoft Advertising] Schlüsselworteinstellungen

Sie können Keywords für Kampagnen erstellen, die die Such- und Anzeigennetzwerke verwenden.

## [!UICONTROL Basic Settings]

*Nur neue Keywords*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne.

**[!UICONTROL Ad Group]:** Die Anzeigengruppe.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Schlüsselwörter, einschließlich aller [!DNL Microsoft Advertising], stimmen mit Syntax und Platzhaltern überein. Die maximale Länge pro Keyword beträgt 100 Zeichen.

Sie können bis zu 2.000 Keywords eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein.

>[!NOTE]
>
>* Negative Keywords können Sie auf der Registerkarte [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie in den Anzeigengruppen- und Kampagneneinstellungen erstellen.
>* Wenn Sie ein [!DNL Microsoft Advertising] Schlüsselwort ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues mit einer neuen Schlüsselwort-ID erstellt. Das Ändern des Übereinstimmungstyps löscht jedoch nicht das vorhandene Keyword.

**[!UICONTROL Status]:** Der Anzeigestatus des Keywords: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*. Die Standardeinstellung für neue Schlüsselwörter ist *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL des Schlüsselworts oder der Titel, die Beschreibung oder die Basis-URL der Anzeige [die `{Param1}` dynamische Ersatzzeichenfolge](https://help.bingads.microsoft.com/#apex/3/en/53079/0) enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Werbeelemente, in denen Sie sie verwenden (z. B. können Titel 1 und Titel 2 zusammen maximal 76 Zeichen lang sein).

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL des Schlüsselworts oder der Titel, die Beschreibung oder die Basis-URL der Anzeige [die `{Param2}` dynamische Ersatzzeichenfolge](https://help.bingads.microsoft.com/#apex/3/en/53079/0) enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Werbeelemente, in denen Sie sie verwenden (z. B. können Titel 1 und Titel 2 zusammen maximal 76 Zeichen lang sein).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Dieses Feld kann optional die `{Param1}` und `{Param2}` dynamische Substitutionsvariablen enthalten.

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](keyword-manage.md)
