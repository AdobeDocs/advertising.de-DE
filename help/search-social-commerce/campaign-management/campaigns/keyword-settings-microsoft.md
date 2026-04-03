---
title: '[!DNL Microsoft Advertising] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für  [!DNL Microsoft Advertising] -Keywords.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/fA0ZDCw5Ici0wOfpd1kXdjbQA6DtUFxOSBEtrlJl4Oo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Schlüsselworteinstellungen

Sie können Keywords für Kampagnen erstellen, die die Such- und Anzeigennetzwerke verwenden.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Schlüsselwörter, einschließlich aller [!DNL Microsoft Advertising], stimmen mit Syntax und Platzhaltern überein. Die maximale Länge pro Keyword beträgt 100 Zeichen.

Sie können bis zu 2.000 Keywords eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein.

>[!NOTE]
>
>* Negative Keywords können in der Ansicht [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie in den Anzeigengruppen- und Kampagneneinstellungen erstellt werden.
>* Wenn Sie ein [!DNL Microsoft Advertising] Schlüsselwort ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues mit einer neuen Schlüsselwort-ID erstellt. Das Ändern des Übereinstimmungstyps löscht jedoch nicht das vorhandene Keyword.

**[!UICONTROL Status]:** Der Anzeigestatus des Keywords: *Aktiv* oder *Paused*. Der Standardwert für neue Keywords ist *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Platzhalter

**[!UICONTROL Param2]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL des Schlüsselworts oder der Titel, die Beschreibung oder die Basis-URL der Anzeige [die `{Param2}` dynamische Ersatzzeichenfolge](https://help.bingads.microsoft.com/#apex/3/en/53079/0) enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Werbeelemente, in denen Sie sie verwenden (z. B. können Titel 1 und Titel 2 zusammen maximal 76 Zeichen lang sein).

**[!UICONTROL Param3]:** Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL des Schlüsselworts oder der Titel, die Beschreibung oder die Basis-URL der Anzeige [die `{Param3}` dynamische Ersatzzeichenfolge](https://help.bingads.microsoft.com/#apex/3/en/53079/0) enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Werbeelemente, in denen Sie sie verwenden (z. B. können Titel 1 und Titel 2 zusammen maximal 76 Zeichen lang sein).

## URL-Optionen

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Dieses Feld kann optional die `{Param2}` und `{Param3}` dynamische Substitutionsvariablen enthalten.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
