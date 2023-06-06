---
title: "[!DNL Microsoft Advertising] Kampagneneinstellungen"
description: Verweisen Sie auf die Einstellungen für [!DNL Microsoft Advertising] Kampagnen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Kampagneneinstellungen

## \[Bildschirm zur Kampagnenerstellung\]

**[!UICONTROL Campaign Type]:** (Nur bei der Kampagnenerstellung verfügbar) Wo Anzeigen platziert werden und welche Anzeigentypen die Kampagne enthalten kann:

* *[!UICONTROL Search and Display Network]:* Zeigt nur Textanzeigen im Suchnetzwerk an.

* *[!UICONTROL Shopping Network]:* Zeigt Produktanzeigen und Dashboards für Ihre Produkte in Ihrer [!DNL Microsoft Merchant Center] Produktkatalog — im Warenkorb

* *[!UICONTROL Audience]:* Zeigt native/Display-Anzeigen auf der [!DNL Microsoft Audience Network]. Sie können entweder a) automatisch Feed-basierte Anzeigen generieren, indem Sie die Kampagne mit einem Händler-Center-Store im [!UICONTROL Shopping Settings] oder b) erstellen Sie responsive Anzeigen mit Text-Assets und hochgeladenen Bildern. Bei beiden Optionen müssen Sie Anzeigengruppen mit Benutzer-Targeting erstellen.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der innerhalb des Kontos eindeutig ist. Die maximale Länge beträgt 128 Zeichen.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Werbekampagnen ist *Aktiv*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Angebotsstrategie für die Kampagne:

* *[!UICONTROL Enhanced CPC]:* (Kampagnen in Zielgruppen-, Such- und Shopping-Netzwerken) Verwendet das verbesserte &quot;Cost-per-Click&quot;-Modell des Werbenetzwerks, mit dem das Anzeigennetzwerk das Angebot &quot;Cost-per-Click&quot;(CPC) für jede Auktion automatisch ändern kann, um Konversionen zu maximieren, indem Konversionen verwendet werden, die im Anzeigennetzwerk (nicht in Search, Social und Commerce) angegeben sind, während versucht wird, Ihren durchschnittlichen CPC unterhalb zu belassen maximale CPC.

Wenn Sie eine Kampagne mit eCPC zu einem optimierten Portfolio für Suche, Social und Handel hinzufügen, optimiert Search, Social und Commerce die Basisangebote und - wenn die Variable[!UICONTROL Auto adjust campaign budget limits]Die Option ist aktiviert - das Kampagnenbudget. Das Werbenetzwerk optimiert alle Angebotsanpassungen und kann die von Search, Social und Commerce generierten Angebote zum Zeitpunkt der Benutzerabfrage basierend auf proprietären Daten und Einblicken ändern. **Vorsicht:** Verwenden Sie eCPC-Kampagnen in Portfolios nur, wenn die im Werbenetzwerk verfolgten Konversionen insgesamt mit dem Portfolioziel übereinstimmen.

* *[!UICONTROL Manual CPC]* (Standardeinstellung): (Veraltet von [!DNL Microsoft Advertising] 2021) Verwendet das CPC-Modell (Cost-per-Click). Sie können optional zulassen, dass das Werbenetzwerk Angebote für die Kampagne ändert:

   * **[!UICONTROL Enable Enhanced CPC]** (standardmäßig deaktiviert): Dies entspricht der Verwendung des[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPM]* (Nur Kampagnen im Zielgruppen-Netzwerk) Verwendet das CPM-Modell (Cost-per-Tausend-Impressions), für das Sie angeben, was Sie pro 1.000 angezeigten Impressionen ausgeben möchten. Kampagnen mit dieser Angebotsstrategie werden nicht optimiert, wenn sie in Portfolios enthalten sind.

* *[!UICONTROL Maximize Clicks]:* (Such- und Shopping-Kampagnen) Das Werbenetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote, um Klicks zu maximieren. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick), um sicherzustellen, dass das Werbenetzwerk nicht mehr als einen bestimmten Betrag für jeden Klick zahlt. **Vorsicht:** Wenn Sie eine Kampagne mit dieser Strategie zu einem Portfolio hinzufügen, werden die Angebote von der Klickgewichtung und nicht vom Portfolioziel bestimmt.

* *[!UICONTROL Maximize Conversion Value]:* (Such- und Shopping-/Smart-Shopping-Netzwerke) Das Werbenetzwerk — nicht &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;— optimiert Gebote, um den Konversionswert zu maximieren. Geben Sie optional eine **[!UICONTROL Target Return on Ad Spend]** (ROAS) in Prozent. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios.

* *[!UICONTROL Maximize Conversions]:* (Kampagnen im Suchnetzwerk) <!-- future: and audience network -->) Das Werbenetzwerk — nicht &quot;Search, Social, &amp; Commerce&quot; — optimiert Gebote, um Konversionen zu maximieren. Geben Sie optional eine **[!UICONTROL Target CPC]** (Kosten pro Klick)<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios.

* *[!UICONTROL Target CPA]:* (Kampagnen im Suchnetzwerk) Das Werbenetzwerk — nicht &quot;Search, Social, &amp; Commerce&quot; — optimiert Gebote auf der Grundlage eines optionalen **[!UICONTROL Target CPA]** (Kosten pro Akquise), der Durchschnittsbetrag von 30 Tagen, den Sie für eine Akquise (Konversion) bezahlen möchten. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer beliebigen Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target CPA].

   Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

* *[!UICONTROL Target Impression Share]:* (Kampagnen im Suchnetzwerk) Das Werbenetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote, um eine zielgerichtete Impressions-Freigabe und Anzeigenposition zu erreichen. Geben Sie optional einen **[!UICONTROL Target Impression Share]** als Prozentsatz die **[!UICONTROL Target Ad Position]** und **[!UICONTROL Max CPC]** (Kosten pro Klick). **Hinweis:** Diese Option wird in hybriden Portfolios nicht unterstützt.

* *[!UICONTROL Target Return on Ad Spend]:*  (Kampagnen in den Such- und Shopping-Netzwerken) Das Werbenetzwerk — nicht &quot;Search, Social, &amp; Commerce&quot; — optimiert Gebote basierend auf Ihrer **[!UICONTROL Target ROAS]** (Rendite auf Werbeausgaben), angegeben als Prozentsatz. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick), um sicherzustellen, dass das Werbenetzwerk nicht mehr als einen bestimmten Betrag für jeden Klick zahlt. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer beliebigen Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target ROAS].

   Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Nur Shopping-Kampagnen; schreibgeschützt für bestehende Kampagnen) Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (Nur Zielgruppenkampagnen; (optional) Verknüpft die Kampagne mit einem bestimmten Merchant Center Store für automatisierte Feed-basierte Anzeigen und nicht mit responsiven Anzeigen. Wenn Sie diese Option auswählen, geben Sie die [!UICONTROL Merchant ID] und [!UICONTROL Products]. Sie müssen Anzeigengruppen für die Kampagne erstellen, Sie müssen jedoch keine Anzeigen erstellen.

Nachdem Sie die Kampagne mit einem Store verknüpft und die Einstellungen gespeichert haben, können Sie diese Option nicht mehr ändern.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]:** (Nur Zielgruppenkampagnen, die mit einem Händler-Center-Store verknüpft sind) Die Produkte, die beworben werden sollen. Standardmäßig *[!UICONTROL All products]* ausgewählt ist. Um nur Produkte mit bestimmten Attributen zu bewerben, wählen Sie *[!UICONTROL Filter products]* und geben Sie bis zu sieben Produkt-Dimensions- und -Attributkombinationen an, nach denen Ihre Produkte gefiltert werden sollen. Alle angegebenen Werte müssen gelten, damit Anzeigen für das Produkt angezeigt werden. Wenn Sie beispielsweise Anzeigen für Acme-Heimtiervorräte anzeigen möchten, können Sie die Filter erstellen `Custom Label 1=animals`, `Category=pet supplies`und `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Nur Kampagnen im Display/nativen Netzwerk; optional) Sites im Display-Netzwerk, auf denen Ihre Anzeigen nicht angezeigt werden sollen. Geben Sie eine gültige URL ein, z. B. www.example.com. Um mehrere Zeichenfolgen anzugeben, trennen Sie sie durch Kommas oder geben Sie sie in separate Zeilen ein.

Informationen zur Verfügbarkeit finden Sie in der Microsoft Advertising-Hilfe zu &quot;[Verhindern der Anzeige von Anzeigen auf bestimmten Websites](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (Für [!UICONTROL EF Redirect] nur) Nicht implementiert

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

>[!MORELIKETHIS]
>
>* [Verwalten von Kampagnen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
