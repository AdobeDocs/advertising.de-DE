---
title: Einstellungen für Anzeigengruppen [!DNL Google Ads]
description: Verweisen Sie auf die Einstellungen  [!DNL Google Ads]  Anzeigengruppen.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: 345c2af5363ca10412f3809700e281af5b06897f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Einstellungen für Anzeigengruppen [!DNL Google Ads]

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ein Anzeigengruppenname, der innerhalb der Kampagne eindeutig ist. Die maximale Länge beträgt 255 Doppelbyte-Zeichen.

**[!UICONTROL Status]:** Der Anzeigestatus der Anzeigengruppe: *Aktiv* oder *Paused*. Der Standardwert für neue Anzeigengruppen lautet *Aktiv*.

**[!UICONTROL Ad Group Type]:** (Nur erweiterte dynamische Suchanzeigen-Kampagnen) Der Typ der Anzeigengruppe:

* *[!UICONTROL Search Standard]* (Standard): Für Standardanzeigen.

* *[!UICONTROL Search Dynamic]:* für dynamische Suchanzeigen.

**[!UICONTROL Ad Rotation Mode]:** Wie oft [!DNL Google Ads] Ihre aktiven Anzeigen in Bezug zueinander innerhalb der Anzeigengruppe bereitstellt:

* *[!UICONTROL Optimize]:* Google Ads bevorzugt Anzeigen, deren Leistung besser als die anderer Anzeigen in der Anzeigengruppe ist. Diese Anzeigen treten häufiger in die Werbeanzeigenauktion ein, und im Laufe der Zeit wird eine einzelne Anzeige bevorzugt. Dies kann im Widerspruch zu Ihren Geschäfts- und Optimierungszielen stehen.

* *[!UICONTROL Rotate forever]:*   Jede Ihrer Anzeigen tritt noch gerader in die Auktion ein, sodass Search, Social und Commerce Ihre Anzeigen nicht nur nach Clickthrough-Rate, sondern auch nach Konversionen bewerten können.

* *[!UICONTROL Use campaign setting]*(Standard für neue Anzeigengruppen): Verwendet die vorhandene Einstellung für die Anzeigenrotation auf Kampagnenebene. **Hinweis:** Die Einstellung auf Kampagnenebene ist in Search, Social und Commerce nicht sichtbar.

Wenn die Kampagne eine intelligente Gebotsstrategie verwendet (z. B. [!UICONTROL Target CPA], [!UICONTROL Target ROAS]), setzt [!DNL Google Ads] die Option automatisch auf &quot;[!UICONTROL Optimize]&quot;.

**[!UICONTROL Custom Bid Level]:** (Kampagnen, die nur auf das Anzeigennetzwerk abzielen) Anleitung: nach *[!UICONTROL Ad Group]* (Standard), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Interessen und Remarketing in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (Website), *[!UICONTROL Unknown]* oder *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Erstellen Sie Tracking-Vorlagen auf Keyword-Ebene, wenn Sie Gebote nach Keyword erstellen. Erstellen Sie auf ähnliche Weise Tracking-Vorlagen auf Platzierungsebene, wenn Sie nach Platzierung bieten. Erstellen Sie für alle anderen Dimensionen Tracking-Vorlagen auf Anzeigenebene.
>* Wenn Sie nach Alter, Geschlecht, Interesse und Liste oder vertikal für Kampagnen in Portfolios bieten, optimiert die Optimierungsfunktion keine Angebote für die Dimension. Außerdem wird die gesamte Attribution auf die Anzeigengruppe angewendet.
>* Werbeanzeigen im Suchnetzwerk verwenden immer Keyword-Gebote.

**[!UICONTROL AI Max Search Term Matching]:** (Kampagnen, die auf das Suchnetzwerk abzielen und für die die [KI-Max-Funktion](https://support.google.com/google-ads/answer/15910366) und die Suchbegriffabgleichfunktion auf Kampagnenebene aktiviert sind; schreibgeschützt) Ob die Abgleichung von Suchbegriffen auf Anzeigengruppenebene aktiviert ist: *[!UICONTROL Disabled]* oder *[!UICONTROL Enabled]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Kampagnen mit [!UICONTROL Target CPA] Gebot; optional) Die Zielkosten pro Akquise (CPA) für die Anzeigengruppe. Dieser Wert überschreibt das Ziel auf Kampagnenebene.

**[!UICONTROL Target ROAS]:** (Kampagnen mit [!UICONTROL Target ROAS] Gebot; optional) Der Zielertrag auf Werbeausgaben (ROAS) für die Anzeigengruppe in Prozent. Dieser Wert überschreibt das Ziel auf Kampagnenebene.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Kampagnen, die nur im Suchnetzwerk laufen, und vorhandene, schreibgeschützte [!DNL Gmail] Kampagnen im Display-Netzwerk) Ob:

* *[!UICONTROL Target and Bid]:* Anzeigen nur Benutzern anzuzeigen, die mit Zielgruppen verknüpft sind und auch andere Ziele für die Anzeigengruppe erfüllen.

* *[!UICONTROL Bid Only]:* Anzeigen auch Personen anzuzeigen, die nicht mit Zielgruppen verknüpft sind, solange sie andere Zielgruppen auf Anzeigengruppenebene erfüllen. Sie können jedoch die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie höhere Gebote für diese Zielgruppen festlegen.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Anzeigengruppen verwalten](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
