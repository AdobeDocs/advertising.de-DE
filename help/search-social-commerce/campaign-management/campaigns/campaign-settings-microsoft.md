---
title: '[!DNL Microsoft Advertising] Kampagneneinstellungen'
description: Verweisen Sie auf die Einstellungen für  [!DNL Microsoft Advertising] -Kampagnen.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: b8aa2461d261af50e1bf66c4ae29e4e453dfd182
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Kampagneneinstellungen

## \[Bildschirm zur Kampagnenerstellung\]

**[!UICONTROL Campaign Type]:** (nur während der Kampagnenerstellung verfügbar) Wo können Anzeigen geschaltet werden und welche Anzeigentypen
Die Kampagne kann Folgendes enthalten:

* *[!UICONTROL Search]:* Zeigt Textanzeigen im Suchnetzwerk an.

* *[!UICONTROL Shopping Network]:* Zeigt Produktanzeigen — für Ihre Produkte in Ihrem [!DNL Microsoft Merchant Center] Produktkatalog — im Shopping-Netzwerk an.

* *[!UICONTROL Audience]:* Zeigt native/angezeigte Anzeigen auf der [!DNL Microsoft Audience Network] an. Sie können entweder a) automatisch Feed-basierte Anzeigen generieren, indem Sie die Kampagne mit einem Händler-Center-Store im [!UICONTROL Shopping Settings] Abschnitt verknüpfen, oder b) responsive Anzeigen mit Text-Assets und hochgeladenen Bildern erstellen. Bei beiden Optionen müssen Anzeigengruppen mit Benutzer-Targeting erstellt werden.

* *[!UICONTROL Shopping Campaigns for Brands]:* Werbt für Ihre Produkte über verknüpfte Einzelhändler in den Such- und Zielgruppennetzwerken. Sie können untergeordnete Anzeigengruppen und Produktgruppen (zu bewerbende Apps) sowie optionale Produktanzeigen für die Kampagne erstellen. [!DNL Microsoft Advertising] erstellt automatisch Anzeigen für die Produktgruppen. Verwenden Sie für Shopping-Kampagnen für Marken die Bid-Strategie [!UICONTROL Manual CPC] für Shopping-Aktionen für Marken die Bid-Strategie [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft Store Ads Campaign]:* Werbt für Ihre Apps und Spiele, die im [!DNL Microsoft Store] verfügbar sind. Sie können untergeordnete Anzeigengruppen, Produktgruppen und optionale Produktanzeigen für die Kampagne erstellen. [!DNL Microsoft Advertising] erstellt automatisch Anzeigen für die Produktgruppen.

* *[!UICONTROL Audience CTV Video]:* Zeigt vernetzte TV- (CTV-) Videoanzeigen im Zielgruppennetzwerk an.

* *[!UICONTROL Audience Video]:* Zeigt Standard-Videoanzeigen im Zielgruppennetzwerk an.

* *[!UICONTROL Performance Max]:* Zeigt mehrere Anzeigentypen in allen Netzwerken mithilfe [!DNL Microsoft Advertising] intelligenten Gebots an. In den Kampagneneinstellungen müssen Sie eine oder mehrere Asset-Gruppen angeben, zu denen Bilder, Logos, Überschriften, Beschreibungen, ein optionaler Aktionsaufruf und Zielgruppensignale gehören. Das Werbenetzwerk kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der innerhalb des Kontos eindeutig ist. Die maximale Länge beträgt 128 Zeichen.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Paused*. Der Standardwert für neue Anzeigenkampagnen lautet *Aktiv*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Die Bid-Strategie für die Kampagne:

* *[!UICONTROL Cost per Sale]:* (nur Shopping-Kampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote auf der Grundlage der [!UICONTROL Target CPS] (Kosten pro Verkauf). Sie zahlen nur, wenn ein Klick auf Ihre Produktanzeige innerhalb von 24 Stunden zu einem Verkauf führt. **Hinweis** Schließen Sie Kampagnen mit dieser Bid-Strategie nicht in Portfolios ein. Die Optimierung von Suche, Social Media und Commerce ist für Kampagnen mit dieser Bid-Strategie nicht verfügbar.

  Nachdem Sie eine Shopping-Kampagne für Marken mit dieser Bid-Strategie gespeichert haben, können Sie die Bid-Strategie nicht mehr ändern. Für andere Shopping-Kampagnentypen ist diese Strategie nur für neue Kampagnen verfügbar.

* *[!UICONTROL CPV]* (Nur Zielgruppen-CTV-Videokampagnen) Verwendet das CPV-Modell (Cost-per-View) . Search, Social und Commerce bieten keine Optimierung für Kampagnen mit dieser Bid-Strategie, die in Portfolios enthalten sind.

* *[!UICONTROL Enhanced CPC]:* (Kampagnen in den Zielgruppen-, Such- und Einkaufsnetzwerken) Verwendet das erweiterte eCPC-Modell (Cost-Per-Click) des Werbenetzwerks, das es dem Werbenetzwerk ermöglicht, das Cost-Per-Click-Angebot (CPC) für jede Auktion automatisch zu ändern, um Konversionen zu maximieren, wobei die im Werbenetzwerk angegebenen Konversionen (nicht in Search, Social und Commerce) verwendet werden, während versucht wird, den durchschnittlichen CPC unter dem maximalen CPC zu halten.

  Wenn Sie eine Kampagne mit eCPC zu einem optimierten Search-, Social- und Commerce-Portfolio hinzufügen, optimiert Search, Social und Commerce die Basisgebote und - wenn die Option &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; aktiviert ist - das Kampagnenbudget. Das Werbenetzwerk optimiert alle Gebotsanpassungen und kann die von Search, Social und Commerce generierten Gebote zum Zeitpunkt der Benutzerabfrage auf der Grundlage proprietärer Daten und Erkenntnisse ändern. **Achtung:** Sie eCPC-Kampagnen nur dann in Portfolios, wenn die Gesamtzahl der im Werbenetzwerk nachverfolgten Konversionen mit dem Portfolioziel übereinstimmt.

* *[!UICONTROL Manual CPC]*: (Shopping-Kampagnen für Marken; [!DNL Microsoft Store Ads] Kampagnen; für andere Kampagnentypen nicht mehr unterstützt) Verwendet das Cost-Per-Click-Modell (CPC). Bei einigen Anzeigentypen können Sie dem Anzeigennetzwerk optional erlauben, Angebote für die Kampagne zu ändern:

   * **[!UICONTROL Enable Enhanced CPC]** (standardmäßig deaktiviert): Diese Option entspricht der Verwendung der Option &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] Kampagnen) Verwendet das CPA-Modell (Cost Per Acquisition) .

* *[!UICONTROL Manual CPM]* (Nur Zielgruppenkampagnen und Zielgruppen-Videokampagnen) Verwendet das Kosten-pro-Tausend-Impressionen-Modell (CPM), für das Sie angeben, was Sie pro 1.000 angezeigten Impressionen ausgeben möchten. Kampagnen mit dieser Bid-Strategie werden nicht optimiert, wenn sie in Portfolios enthalten sind.

* *[!UICONTROL Maximize Clicks]:* (Search- und Shopping-Kampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um Klicks zu maximieren. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein, um sicherzustellen, dass das Werbenetzwerk für jeden Klick nicht mehr als einen bestimmten Betrag zahlt. **Achtung:** Wenn Sie eine Kampagne mit dieser Strategie zu einem Portfolio hinzufügen, führt die Klickgewichtung (nicht das Portfolioziel) zu Angeboten.

* *[!UICONTROL Maximize Conversion Value]:* (Search and Shopping/Smart Shopping Networks, Performance Max Kampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um den Konversionswert zu maximieren. Geben Sie optional einen **[!UICONTROL Target Return on Ad Spend]** (ROAS) als Prozentsatz ein. **Hinweis** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in Standardportfolios. In Hybridportfolios optimieren Search, Social und Commerce die Target-ROAS.

* *[!UICONTROL Maximize Conversions]:* (Performance Max-Kampagnen und -Kampagnen im Suchnetzwerk oder Zielgruppennetzwerk (aber keine Zielgruppenvideos oder vernetztes Fernsehen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um Konversionen zu maximieren. Geben Sie optional einen **[!UICONTROL Target CPC]** ein (Kosten pro Klick). Für Audience-Kampagnen können Sie auch einen optionalen **[!UICONTROL Target CPA]** (Kosten pro Akquise) eingeben. **Hinweis** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in Standardportfolios. In hybriden Portfolios optimieren Search, Social und Commerce die Target-CPA.

* *[!UICONTROL Target CPA]:* (Kampagnen im Suchnetzwerk) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote auf der Grundlage einer optionalen **[!UICONTROL Target CPA]** (Kosten pro Akquise), die dem 30-Tage-Durchschnittsbetrag entspricht, den Sie für eine Akquise (Konversion) zahlen möchten. **Hinweis** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer beliebigen Ausgabenstrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target CPA]. In hybriden Portfolios optimieren Search, Social und Commerce die Target-CPA.

  Durchschnittliche Positionsdaten und CPC-Bid-Daten sind für Kampagnen mit dieser Bid-Strategie nicht verfügbar.

* *[!UICONTROL Target Impression Share]:* (Kampagnen im Suchnetzwerk) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um einen Ziel-Impression-Anteil und eine Anzeigenposition zu erreichen. Geben Sie optional einen **[!UICONTROL Target Impression Share]** als Prozentsatz, den **[!UICONTROL Target Ad Position]** und einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein. **Hinweis:** Diese Option wird in hybriden Portfolios nicht unterstützt.

* *[!UICONTROL Target Return on Ad Spend]:* (Kampagnen in den Such- und Shopping-Netzwerken) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote basierend auf Ihrer **[!UICONTROL Target ROAS]** (Rendite auf Werbeausgaben), angegeben als Prozentsatz. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein, um sicherzustellen, dass das Werbenetzwerk für jeden Klick nicht mehr als einen bestimmten Betrag zahlt. **Hinweis** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer beliebigen Ausgabenstrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target ROAS]. In Hybridportfolios optimieren Search, Social und Commerce die Target-ROAS.

  Durchschnittliche Positionsdaten und CPC-Bid-Daten sind für Kampagnen mit dieser Bid-Strategie nicht verfügbar.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Nur Einkaufskampagnen; nur für bestehende Kampagnen schreibgeschützt) Das Land, in dem
Die Kampagnenprodukte werden verkauft. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, für welche Produkte in der Kampagne geworben wird.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (Nur Zielgruppenkampagnen; optional) Verknüpft die Kampagne mit einem bestimmten Händler-Center-Store für automatisierte Feed-basierte Anzeigen anstelle von responsiven Anzeigen. Wenn Sie diese Option wählen, geben Sie die [!UICONTROL Merchant ID] und die [!UICONTROL Products] an. Sie müssen Anzeigengruppen für die Kampagne erstellen, aber Sie müssen keine Anzeigen erstellen.

Nachdem Sie die Kampagne mit einem Store verknüpft und die Einstellungen gespeichert haben, können Sie diese Option nicht mehr ändern.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (Zielgruppenkampagnen, die nur mit einem Händler-Center-Store verknüpft sind) Die zu bewerbenden Produkte. Standardmäßig ist *[!UICONTROL All products]* ausgewählt. Um nur Produkte mit bestimmten Attributen zu bewerben, wählen Sie *[!UICONTROL Filter products]* aus und geben Sie bis zu sieben Produkt-Dimension-Attribut-Kombinationen an, nach denen Ihre Produkte gefiltert werden sollen. Alle angegebenen Werte müssen für Anzeigen gelten, die für das Produkt angezeigt werden. Um beispielsweise Anzeigen für Acme-Haustierbedarf anzuzeigen, können Sie die Filter `Custom Label 1=animals`, `Category=pet supplies` und `Brand=Acme Pet Supplies` erstellen.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Nur Performance-Max-Kampagnen) Die Sprache der Anzeige, die mit der Sprache der Websites übereinstimmen sollte, auf denen Ihre Anzeige erscheinen kann. [!DNL Microsoft Advertising] bestimmt die Sprache eines Benutzers aus verschiedenen Signalen, einschließlich der Abfrage des Benutzers, des Landes des Herausgebers und der Spracheinstellung des Benutzers.

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

**[!UICONTROL Negative Websites]:** (Nur Kampagnen auf der Anzeige/im nativen Netzwerk; optional) Websites auf dem Display-Netzwerk, auf denen Ihre Anzeigen nicht angezeigt werden sollen. Geben Sie eine gültige URL ein, z. B. www.example.com. Um mehrere Zeichenfolgen anzugeben, trennen Sie sie durch Kommas oder geben Sie sie in separaten Zeilen ein.

Informationen zur Verfügbarkeit finden Sie in der Hilfe zu Microsoft Advertising [Verhindern von Anzeigen auf bestimmten Websites](https://help.ads.microsoft.com/#apex/bae/en/14061/0).

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

**[!UICONTROL Track Product Group]:** (nur für [!UICONTROL EF Redirect]) Nicht implementiert

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (pro Asset-Gruppe)

**[!UICONTROL Asset Group Name]:** Der Name des Asset-Ordners (Asset-Gruppe).

**[!UICONTROL Asset Group Status]:** Der Status der Asset-Gruppe: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Die endgültige URL für alle Anzeigen, die aus der Asset-Gruppe erstellt wurden.

**[!UICONTROL Images]:** Bis zu 20 Bilder für die Anzeige, darunter mindestens ein quadratisches Bild und ein Querformat. Siehe [[!DNL Microsoft Advertising] Bildrichtlinien](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Sie können entweder Bilder hochladen oder aus Ihren [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* So laden Sie Bilder hoch:

   1. Klicken Sie auf der Registerkarte [!UICONTROL Upload from Device] auf **[!UICONTROL +]** und wählen Sie Bilder von Ihrem Gerät oder Netzwerk aus.

   1. Für jedes Bild:

      1. Wahl des Seitenverhältnisses

      1. Ziehen Sie das Zuschnittsfeld nach Bedarf, um den sichtbaren Teil des Bildes auszuwählen, und ändern Sie die Größe des sichtbaren Teils des Bildes nach Bedarf.

      1. (Optional) Wählen Sie zusätzliche Seitenverhältnisse und positionieren Sie das Bild optional neu und ändern Sie die Größe für jedes ausgewählte Seitenverhältnis nach Bedarf.

         Für jedes ausgewählte Seitenverhältnis wird ein Asset erstellt.

      1. Klicken Sie auf **[!UICONTROL Proceed]**.

   1. Wenn Sie mit der Angabe der Bilder fertig sind, klicken Sie auf **[!UICONTROL Upload]**.

* Um Bilder aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Bilder aus.

**[!UICONTROL Logos]:** Mindestens ein Logo. Sie können bis zu fünf einbeziehen. Siehe [[!DNL Microsoft Advertising] Asset-Richtlinien](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Sie können entweder Bilder hochladen oder aus Ihren [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* So laden Sie Bilder hoch:

   1. Klicken Sie auf der Registerkarte [!UICONTROL Upload from Device] auf **[!UICONTROL +]** und wählen Sie Bilder von Ihrem Gerät oder Netzwerk aus.

   1. Für jedes Bild:

      1. Wahl des Seitenverhältnisses

      1. Ziehen Sie das Zuschnittsfeld nach Bedarf, um den sichtbaren Teil des Bildes auszuwählen, und ändern Sie die Größe des sichtbaren Teils des Bildes nach Bedarf.

      1. (Optional) Wählen Sie zusätzliche Seitenverhältnisse und positionieren Sie das Bild optional neu und ändern Sie die Größe für jedes ausgewählte Seitenverhältnis nach Bedarf.

         Für jedes ausgewählte Seitenverhältnis wird ein Asset erstellt.

      1. Klicken Sie auf **[!UICONTROL Proceed]**.

   1. Wenn Sie mit der Angabe der Bilder fertig sind, klicken Sie auf **[!UICONTROL Upload]**.

* Um Bilder aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Bilder aus.

**[!UICONTROL Headlines]:** Mindestens drei und bis zu 15 kurze Überschriften mit jeweils maximal 30 Zeichen. Sie können entweder Text eingeben oder Assets aus Ihrer [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* So geben Sie Text ein:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Long Headlines]:** Mindestens eine und bis zu fünf lange Überschriften mit jeweils maximal 90 Zeichen. Sie können entweder Text eingeben oder Assets aus Ihrer [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* So geben Sie Text ein:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Descriptions]:** Mindestens zwei und bis zu fünf Beschreibungen mit jeweils maximal 90 Zeichen. Sie können entweder Text eingeben oder Assets aus Ihrer [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* So geben Sie Text ein:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Call to Action]:** Der Aktionsaufruf, der in die Anzeige aufgenommen werden soll. Standardmäßig ist *[!UICONTROL Act Now]* ausgewählt.

**[!UICONTROL Business Name]:** Der Unternehmensname mit maximal 25 Zeichen. Es darf keine Skripte, HTML oder andere Markup-Sprache enthalten.

**[!UICONTROL Audience Signal]:** (Optional) [!DNL Microsoft Advertising] Zielgruppen, die als Zielgruppensignale für die Kampagne verwendet werden sollen. [!DNL Microsoft Advertising] Modelle für maschinelles Lernen verwenden die Zielgruppen, um ähnliche Websurfer zu finden, die als Ziel ausgewählt wurden, und können auch Anzeigen für Zielgruppen anzeigen, die nicht als Signale angegeben wurden, um Sie beim Erreichen Ihrer Leistungsziele zu unterstützen. Wählen Sie die Zielgruppen aus, die am ehesten konvertiert werden sollen.

>[!NOTE]
>Zielgruppensignale unterscheiden sich von Zielgruppenzielen auf [Anzeigengruppenebene](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Ermöglicht die Angabe einer anderen Asset-Gruppe.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Ob *[!UICONTROL Use account conversion goals for this campaign]* (Standard) oder *[!UICONTROL Use campaign specific conversion goals]* werden soll. Wenn Sie Konversionsziele für die Kampagne angeben möchten, wählen Sie die Ziele in der Liste aller verfügbaren Ziele aus. **Hinweis:** Ziele werden täglich synchronisiert, sodass in den letzten 24 Stunden erstellte Ziele möglicherweise nicht aufgeführt werden. Um die Liste zu aktualisieren, [manuell die Daten des Werbenetzwerks synchronisieren](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

>[!TIP]
>
>Wenn die Kampagne Teil eines hybriden Portfolios ist, empfiehlt es sich, Ziele auf Kampagnenebene zu verwenden, die den Konversionszielen im Portfolioziel entsprechen. Das Einschließen zusätzlicher Konversionsziele kann die Portfolioleistung beeinträchtigen.
>
> Gehen Sie bei Kampagnen in hybriden Portfolios, für die Sie [Ziele in das Anzeigennetzwerk hochladen](/help/search-social-commerce/tools/objective-upload-to-networks.md), wie folgt im Editor des Anzeigennetzwerks vor und nicht hier: a) Fügen Sie die hochgeladene Zielmetrik für das Zielportfolio für Suche, Social und Commerce (die mit „O_ACS_OBJ“ beginnt) als Konversionsziel für die Kampagne hinzu und b) fügen Sie alle Kampagnenziele hinzu, die Konversionen enthalten, die vom Tag [!DNL Microsoft Advertising] Universal Event Tracking (UET) verfolgt werden, da im Anzeigennetzwerk verfolgte Metriken nicht mit dem Ziel in das Anzeigennetzwerk hochgeladen werden.

>[!MORELIKETHIS]
>
>* [Kampagnen verwalten](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
