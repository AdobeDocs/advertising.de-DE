---
title: '[!DNL Baidu] Schlüsselworteinstellungen'
description: Referenzieren Sie die Einstellungen für  [!DNL Baidu] -Keywords.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/uMU0oAkL8rmsOIMXYR8qgp9-upe2qWIK-ev1YtPQUb4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 230
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

Wenn Sie den Konversionsverfolgungs-Service von Adobe Advertising verwenden und die Kampagneneinstellungen die Verwendung der [!UICONTROL EF Redirect] und das Hinzufügen von Verfolgungen auf Keyword-Ebene einschließen, fügt Search, Social und Commerce automatisch einen eigenen Klick-Verfolgungs-Code hinzu.

>[!MORELIKETHIS]
>
>* [Schlüsselwörter verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
