---
title: '''[!DNL Google Ads] Anzeigengruppeneinstellungen'
description: Verweisen Sie auf die Einstellungen für [!DNL Google Ads] Anzeigengruppen.
exl-id: 00aaa936-796f-4e22-9bee-4bb5121cd887
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] Anzeigengruppeneinstellungen

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Ein Anzeigengruppenname, der innerhalb der Kampagne eindeutig ist. Die maximale Länge beträgt 255 Doppelbyte-Zeichen.

**[!UICONTROL Status]:** Der Anzeigestatus der Anzeigengruppe: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Anzeigengruppen ist *Aktiv*.

**[!UICONTROL Ad Group Type]:** (Nur erweiterte dynamische Suchanzeigekampagnen) Der Typ der Anzeigengruppe:

* *[!UICONTROL Search Standard]* (Standard): Für Standardanzeigen.

* *[!UICONTROL Search Dynamic]:* Für dynamische Suchanzeigen.

**[!UICONTROL Ad Rotation Mode]:** Wie oft [!DNL Google Ads] stellt Ihre aktiven Anzeigen im Verhältnis zueinander innerhalb der Anzeigengruppe bereit:

* *[!UICONTROL Optimize]:* Google Ads bevorzugt Anzeigen, von denen erwartet wird, dass sie eine bessere Leistung erzielen als andere Anzeigen in der Anzeigengruppe. Diese Anzeigen treten häufiger in die Anzeigenauktion ein und im Laufe der Zeit wird eine einzelne Anzeige bevorzugt. Dies entspricht möglicherweise nicht Ihren Unternehmens- und Optimierungszielen.

* *[!UICONTROL Rotate forever]:*   Jede Ihrer Anzeigen tritt in die Anzeigenauktion ein, was es Search, Social und Commerce ermöglicht, Ihre Anzeigen nicht nur mit der Clickthrough-Rate, sondern auch mit Konversionen zu bewerten.

* *[!UICONTROL Use campaign setting]*(Standardeinstellung für neue Anzeigengruppen): Verwendet die Einstellung für die Anzeigenrotation auf Kampagnenebene. **Hinweis:** Die Einstellung auf Kampagnenebene ist in &quot;Suchen&quot;, &quot;Sozial&quot;und &quot;Commerce&quot;nicht sichtbar.

Wenn die Kampagne eine Smart Bidding-Angebotsstrategie verwendet (z. B. [!UICONTROL Target CPA], [!UICONTROL Target ROAS]oder [!UICONTROL Enhanced CPC]), dann [!DNL Google Ads] setzt die Option automatisch auf &quot;[!UICONTROL Optimize].&quot;

**[!UICONTROL Custom Bid Level]:** (Kampagnen, die nur auf das Display-Netzwerk abzielen) Anleitung zum Angebot: von *[!UICONTROL Ad Group]* (Standardeinstellung), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Interest &amp; Remarketing in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (Website), *[!UICONTROL Unknown]* oder *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Erstellen Sie beim Gebot nach Keyword Tracking-Vorlagen auf Suchbegriffebene. Erstellen Sie auf ähnliche Weise Tracking-Vorlagen, wenn Sie ein Angebot nach Platzierung unterbreiten. Erstellen Sie für alle anderen Dimensionen Tracking-Vorlagen auf Anzeigenebene.
>* Wenn Sie für Kampagnen in Portfolios ein Angebot nach Alter, Geschlecht, Interessen und Liste oder Vertikal erstellen, optimiert die Optimierungsfunktion keine Angebote für die Dimension. Außerdem wird die gesamte Attribution auf die Anzeigengruppe angewendet.
>* Anzeigen im Suchnetzwerk verwenden immer Suchbegriffangebote.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Kampagnen mit [!UICONTROL Target CPA] Gebote; optional) Die Zielkosten pro Akquise (CPA) für die Anzeigengruppe. Dieser Wert überschreibt das Ziel auf Kampagnenebene.

**[!UICONTROL Target ROAS]:** (Kampagnen mit [!UICONTROL Target ROAS] Gebote; optional) Die Zielrendite aus Werbeausgaben (ROAS) für die Anzeigengruppe in Prozent. Dieser Wert überschreibt das Ziel auf Kampagnenebene.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Kampagnen, die sich nur auf das Suchnetzwerk beziehen, sowie bestehende, schreibgeschützte [!DNL Gmail] Kampagnen im Display-Netzwerk) Ob:

* *[!UICONTROL Target and Bid]:* So zeigen Sie Anzeigen nur Benutzern an, die mit Zielgruppen verknüpft sind, die auch andere Ziele für die Anzeigengruppe erfüllen.

* *[!UICONTROL Bid Only]:* Anzeigen auch für Personen anzeigen, die nicht mit Zielgruppen verbunden sind, solange sie andere Ziele auf Anzeigengruppenebene erfüllen. Sie können die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie jedoch höhere Angebote für diese Zielgruppen festlegen.

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
>* [Verwalten von Anzeigengruppen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
