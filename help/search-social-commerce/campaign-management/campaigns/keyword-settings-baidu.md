---
title: '[!DNL Baidu] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für  [!DNL Baidu] -Keywords.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# [!DNL Baidu] Schlüsselworteinstellungen

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Schlüsselwörter. Die maximale Länge pro Keyword beträgt 30 Einzelbyte- oder 15 Doppelbyte-Zeichen

Sie können bis zu 2.000 Keywords eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein. Verwenden Sie die folgende Syntax:

* `keyword` für breite Übereinstimmung
* `"keyword"` für Phrasenübereinstimmung
* Für exakte Übereinstimmung `[keyword]`

>[!NOTE]
>
>* [!DNL Baidu] ist nur ein Übereinstimmungstyp pro Keyword pro Anzeigengruppe zulässig. Beispielsweise kann Anzeigengruppe 1 nicht sowohl `"keyword"` als auch `[keyword]` enthalten.
>* Negative Keywords können in der Ansicht [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie in den Anzeigengruppen- und Kampagneneinstellungen erstellt werden.
>* Wenn Sie ein [!DNL Baidu] Schlüsselwort ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues mit einer neuen Schlüsselwort-ID erstellt. Das Ändern des Übereinstimmungstyps löscht jedoch nicht das vorhandene Keyword.

**[!UICONTROL Status]:** Der Anzeigestatus des Keywords: *Aktiv* oder *Paused*. Der Standardwert für neue Keywords ist *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL-Optionen

**[!UICONTROL Base URL]:** (Nur Kampagnen mit Tracking auf Keyword-Ebene; optional) Die Landingpage-URL, zu der Benutzer geleitet werden, wenn sie auf Ihre Anzeige klicken. Sie kann Folgendes umfassen
Weiterleitungs- und Trackingcode von Drittanbietern. Wenn Sie einen Wert eingeben, überschreibt dieser die Basis-URL für die Anzeige.

Nachdem Sie den Datensatz gespeichert haben, enthält die Basis-URL alle für die Kampagne oder das Konto konfigurierten Anlagenparameter.

Wenn Sie den Adobe Advertising-Konversions-Tracking-Service verwenden und die Kampagneneinstellungen die Verwendung des [!UICONTROL EF Redirect] und das Hinzufügen des Trackings auf Keyword-Ebene beinhalten, fügt Search, Social und Commerce automatisch einen eigenen Klick-Tracking-Code hinzu.

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
