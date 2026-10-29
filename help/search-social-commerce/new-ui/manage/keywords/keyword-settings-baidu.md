---
title: '[!DNL Baidu] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für [!DNL Baidu] Schlüsselwörter.
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
source-wordcount: '245'
ht-degree: 0%
---
# [!DNL Baidu] Schlüsselworteinstellungen

## [!UICONTROL Basic Settings]

*Nur neue Keywords*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne.

**[!UICONTROL Ad Group]:** Die Anzeigengruppe.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Die Schlüsselwörter. Die maximale Länge pro Keyword beträgt 30 Einzelbyte- oder 15 Doppelbyte-Zeichen.

Sie können bis zu 2.000 Keywords eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein. Verwenden Sie die folgende Syntax:

* `keyword` für breite Übereinstimmung
* `"keyword"` für Phrasenübereinstimmung
* Für exakte Übereinstimmung `[keyword]`

>[!NOTE]
>
>* [!DNL Baidu] ist nur ein Übereinstimmungstyp pro Keyword pro Anzeigengruppe zulässig. Beispielsweise kann Anzeigengruppe 1 nicht sowohl `"keyword"` als auch `[keyword]` enthalten.
>* Negative Keywords können Sie auf der Registerkarte [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] sowie in den Anzeigengruppen- und Kampagneneinstellungen erstellen.
>* Wenn Sie ein [!DNL Baidu] Schlüsselwort ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues mit einer neuen Schlüsselwort-ID erstellt. Das Ändern des Übereinstimmungstyps löscht jedoch nicht das vorhandene Keyword.

**[!UICONTROL Status]:** Der Anzeigestatus des Keywords: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*. Die Standardeinstellung für neue Schlüsselwörter ist *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL URL Options]

**[!UICONTROL Base URL]:** (Nur Kampagnen mit Tracking auf Keyword-Ebene; optional) Die Landingpage-URL, zu der Benutzer geleitet werden, wenn sie auf Ihre Anzeige klicken. Es kann Umleitungs- und Trackingcode von Drittanbietern enthalten. Wenn Sie einen Wert eingeben, überschreibt dieser die Basis-URL für die Anzeige.

Nachdem Sie den Datensatz gespeichert haben, enthält die Basis-URL alle für die Kampagne oder das Konto konfigurierten Anlagenparameter.

Wenn Sie den Konversionsverfolgungs-Service von Adobe Advertising verwenden und die Kampagneneinstellungen die Verwendung der [!UICONTROL EF Redirect] und das Hinzufügen von Verfolgungen auf Keyword-Ebene einschließen, fügt Search, Social und Commerce automatisch einen eigenen Klick-Verfolgungs-Code hinzu.

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](keyword-manage.md)
