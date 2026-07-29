---
title: '[!DNL Yandex] Kampagneneinstellungen'
description: Verweisen Sie auf die Einstellungen für  [!DNL Yandex] -Kampagnen.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# [!DNL Yandex] Kampagneneinstellungen

## \[Seitenanfang]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der innerhalb des Kontos eindeutig ist.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Paused*. Der Standardwert für neue Anzeigenkampagnen lautet *Aktiv*.

## Registerkarte [!UICONTROL Basic Settings]

*Nur neue Kampagnen*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign Type]:** Ort, an dem Anzeigen geschaltet werden:

* *[!UICONTROL Search Network Only]:* Zeigt Textanzeigen im Suchnetzwerk an. Für jede Anzeigengruppe müssen Schlüsselwörter angegeben werden.

* *[!UICONTROL Search and Display Network]:* Zeigt Textanzeigen im Suchnetzwerk und im [!DNL Yandex Advertising Network] an. Für Suchanzeigen müssen Sie für jede Anzeigengruppe Suchbegriffe angeben. Für Display-Anzeigen müssen Sie für jede Anzeigengruppe Schlüsselwörter für die Websites angeben, auf denen Sie werben möchten.

* *[!UICONTROL Display Network Only]:* Zeigt Textanzeigen auf der [!DNL Yandex Advertising Network] an. Für jede Anzeigengruppe müssen Sie Schlüsselwörter für die Websites angeben, auf denen Sie werben möchten.

## Registerkarte [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

## Registerkarte [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** Das Budget, das den Betrag darstellt, den Sie täglich (im Durchschnitt) oder während der Lebensdauer der Kampagne ausgeben möchten, je nach Budgettyp des Kontos. Das Mindestbudget beträgt Py6 300, EUR 10 oder USD 10.

**Hinweise:**

* Neue Kampagnen haben die Angebotsverwaltungsstrategie „Höchste verfügbare Position“.

* Wenn Sie diese Kampagne je nach Suchbedingungen einem Portfolio zuweisen, das so konfiguriert ist, dass die Kampagnenbudgetgrenzen automatisch angepasst werden können, können die Ausgaben für einen bestimmten Tag, Monat oder eine bestimmte Lebensdauer mehr oder weniger als das angegebene Budget betragen.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## Registerkarte [!UICONTROL Additional Campaign Information]

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (Nur für [!UICONTROL EF Redirect]; schreibgeschützt) Die Ebene, auf der Klicks und Umsatz verfolgt werden sollen. Nur *[!UICONTROL Creative]* ist für [!DNL Yandex] verfügbar - Daten werden nur auf Anzeigenebene (kreativ) verfolgt.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [Kampagnen verwalten](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
