---
title: Einstellungen für Anzeigengruppen [!DNL Google Ads]
description: Verweisen Sie auf die Einstellungen  [!DNL Google Ads]  Anzeigengruppen.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/pDFheVIM62XNCh2-7jbCscIqOrcTep7qnNg5S1tHYF8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 549
ht-degree: 0%

---

# Einstellungen für Anzeigengruppen [!DNL Google Ads]

## \[Seitenanfang]

**[!UICONTROL Ad Group Name]:** Ein innerhalb der Kampagne eindeutiger Anzeigengruppenname.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Paused*. Der Standardwert für neue Anzeigenkampagnen lautet *Aktiv*.

## Registerkarte [!UICONTROL Basic Settings]

*Nur neue Kampagnen*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne.

## Registerkarte [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Group Type]:** (Nur erweiterte dynamische Suchanzeigen-Kampagnen) Der Typ der Anzeigengruppe:

* *[!UICONTROL Search Standard]* (Standard): Für Standardanzeigen.

* *[!UICONTROL Search Dynamic]:* für dynamische Suchanzeigen.

**[!UICONTROL Ad Rotation Mode]:** Wie oft [!DNL Google Ads] Ihre aktiven Anzeigen in Bezug zueinander innerhalb der Anzeigengruppe bereitstellt:

* *[!UICONTROL Optimize]:* [!DNL Google Ads] bevorzugt Anzeigen, von denen eine bessere Leistung erwartet wird als von anderen Anzeigen in der Anzeigengruppe. Diese Anzeigen treten häufiger in die Werbeanzeigenauktion ein, und im Laufe der Zeit wird eine einzelne Anzeige bevorzugt. Dies kann im Widerspruch zu Ihren Geschäfts- und Optimierungszielen stehen.

* *[!UICONTROL Rotate forever]:* Jede Ihrer Anzeigen tritt noch gerader in die Auktion ein, sodass Search, Social und Commerce Ihre Anzeigen nicht nur nach Clickthrough-Rate, sondern auch nach Konversionen bewerten können.

* *[!UICONTROL Use campaign setting]*(Standard für neue Anzeigengruppen): Verwendet die vorhandene Einstellung für die Anzeigenrotation auf Kampagnenebene. **Hinweis:** Die Einstellung auf Kampagnenebene ist in Search, Social und Commerce nicht sichtbar.

Wenn die Kampagne eine intelligente Gebotsstrategie verwendet (z. B. [!UICONTROL Target CPA], [!UICONTROL Target ROAS]), setzt [!DNL Google Ads] die Option automatisch auf &quot;[!UICONTROL Optimize]&quot;.

**[!UICONTROL Custom Bid Level]:** (Kampagnen, die nur auf das Anzeigennetzwerk abzielen) Anleitung: nach *[!UICONTROL Ad Group]* (Standard), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Interessen und Remarketing in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (Website), *[!UICONTROL Unknown]* oder *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Erstellen Sie Tracking-Vorlagen auf Keyword-Ebene, wenn Sie Gebote nach Keyword erstellen. Erstellen Sie auf ähnliche Weise Tracking-Vorlagen auf Platzierungsebene, wenn Sie nach Platzierung bieten. Erstellen Sie für alle anderen Dimensionen Tracking-Vorlagen auf Anzeigenebene.
>* Wenn Sie nach Alter, Geschlecht, Interesse und Liste oder vertikal für Kampagnen in Portfolios bieten, optimiert die Optimierungsfunktion keine Angebote für die Dimension. Außerdem wird die gesamte Attribution auf die Anzeigengruppe angewendet.
>* Werbeanzeigen im Suchnetzwerk verwenden immer Keyword-Gebote.

**[!UICONTROL AI Max Search Term Matching]:** (Kampagnen, die auf das Suchnetzwerk abzielen und für die die [KI-Max-Funktion](https://support.google.com/google-ads/answer/15910366) und die Suchbegriffabgleichfunktion auf Kampagnenebene aktiviert sind; schreibgeschützt) Ob die Abgleichung von Suchbegriffen auf Anzeigengruppenebene aktiviert ist: *[!UICONTROL Disabled]* oder *[!UICONTROL Enabled]*.

## Registerkarte [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Kampagnen mit [!UICONTROL Target CPA] Gebot; optional) Die Zielkosten pro Akquise (CPA) für die Anzeigengruppe. Dieser Wert überschreibt das Ziel auf Kampagnenebene.

**[!UICONTROL Target ROAS]:** (Kampagnen mit [!UICONTROL Target ROAS] Gebot; optional) Der Zielertrag auf Werbeausgaben (ROAS) für die Anzeigengruppe in Prozent. Dieser Wert überschreibt das Ziel auf Kampagnenebene.

## Registerkarte [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Kampagnen, die nur im Suchnetzwerk laufen, und vorhandene, schreibgeschützte [!DNL Gmail] Kampagnen im Display-Netzwerk) Ob:

* *[!UICONTROL Target and Bid]:* Anzeigen nur Benutzern anzuzeigen, die mit Zielgruppen verknüpft sind und auch andere Ziele für die Anzeigengruppe erfüllen.

* *[!UICONTROL Bid Only]:* Anzeigen auch Personen anzuzeigen, die nicht mit Zielgruppen verknüpft sind, solange sie andere Zielgruppen auf Anzeigengruppenebene erfüllen. Sie können jedoch die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie höhere Gebote für diese Zielgruppen festlegen.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## Registerkarte [!UICONTROL AI Max]

*Kampagnen, die nur auf das Suchnetzwerk abzielen*

## Registerkarte [!UICONTROL AI Max]

**[!UICONTROL AI Search Term Matching]:** (Nur Kampagnen mit aktiviertem [!DNL AI Max]) Ob die KI-gestützte, schlüsselwortlose Suchbegriffübereinstimmung verwendet werden soll, um Reichweite und Optimierung zu verbessern.<!--SUPPOSEDLY, BUT THIS IS OFF FOR ME:  It's enabled by default for campaigns with [!DNL AI Max], but you can disable it at the ad group level. -->

**[!UICONTROL Locations of Interest]:** (Nur Kampagnen mit aktiviertem [!DNL AI Max]) Bestimmte Orte mit geografischer Absicht, die angesprochen (aber nicht ausgeschlossen) werden sollen. Die Benutzer müssen auch die geografische Zielgruppe der Kampagne erfüllen. Standardmäßig werden Benutzende in allen geografischen Standorten angesprochen, die sich regelmäßig dort aufhalten oder an ihnen interessiert sind. Um die Ziele einzugrenzen, wählen Sie jeden Zielort aus.

## Registerkarte [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## Registerkarte [!UICONTROL Additional Ad Group Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

### [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Anzeigengruppen verwalten](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
