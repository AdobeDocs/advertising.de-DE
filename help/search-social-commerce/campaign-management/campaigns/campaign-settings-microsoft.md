---
title: '[!DNL Microsoft Advertising] Kampagneneinstellungen'
description: Referenzieren Sie die Einstellungen für [!DNL Microsoft Advertising] Kampagnen.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 096271a2e9daddc20f7f5f4e0063fda21974c8a1
workflow-type: tm+mt
source-wordcount: '2001'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Kampagneneinstellungen

## \[Bildschirm zur Kampagnenerstellung\]

**[!UICONTROL Campaign Type]:** (Nur bei Kampagnenerstellung verfügbar) Wo Anzeigen platziert werden und welche Anzeigentypen
die Kampagne kann Folgendes enthalten:

* *[!UICONTROL Search]:* Zeigt Textanzeigen im Suchnetzwerk an.

* *[!UICONTROL Shopping Network]:* Zeigt Produktanzeigen — für Ihre Produkte in Ihrem [!DNL Microsoft Merchant Center] Produktkatalog — im Warennetzwerk an.

* *[!UICONTROL Audience]:* Zeigt native/Display-Anzeigen auf dem [!DNL Microsoft Audience Network] an. Sie können entweder a) automatisch Feed-basierte Anzeigen generieren, indem Sie die Kampagne mit einem Merchant Center Store im Abschnitt [!UICONTROL Shopping Settings] verknüpfen oder b) responsive Anzeigen mit Text-Assets und hochgeladenen Bildern erstellen. Bei beiden Optionen müssen Sie Anzeigengruppen mit Benutzer-Targeting erstellen.

* *[!UICONTROL Shopping Campaigns for Brands]:* Bewerbt Ihre Produkte durch verlinkte Einzelhändler in den Such- und Zielgruppennetzwerken. Sie können untergeordnete Anzeigengruppen und Produktgruppen (Apps zur Werbung) sowie optionale Produktanzeigen für die Kampagne erstellen. [!DNL Microsoft Advertising] erstellt automatisch Anzeigen für die Produktgruppen. Verwenden Sie für Shopping-Kampagnen für Marken die Angebotsstrategie [!UICONTROL Manual CPC]. Verwenden Sie für Shopping-Promotions für Marken die Angebotsstrategie [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft Store Ads Campaign]:* Bewerbt eure Apps und Spiele, die in der [!DNL Microsoft Store] verfügbar sind. Sie können untergeordnete Anzeigengruppen, Produktgruppen und optionale Produktanzeigen für die Kampagne erstellen. [!DNL Microsoft Advertising] erstellt automatisch Anzeigen für die Produktgruppen.

* *[!UICONTROL Audience CTV Video]:* Zeigt verbundene TV-Videoanzeigen (CTV) im Zielgruppennetzwerk an.

* *[!UICONTROL Audience Video]:* Zeigt standardmäßige Videoanzeigen im Zielgruppennetzwerk an.

* *[!UICONTROL Performance Max]:* Zeigt mithilfe von [!DNL Microsoft Advertising] intelligentem Gebot mehrere Anzeigentypen in allen Netzwerken an. In den Kampagneneinstellungen müssen Sie eine oder mehrere Asset-Gruppen angeben, darunter Bilder, Logos, Überschriften, Beschreibungen, einen optionalen Aktionsaufruf und Zielgruppensignale. Das Werbenetzwerk kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der innerhalb des Kontos eindeutig ist. Die maximale Länge beträgt 128 Zeichen.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Werbekampagnen ist *aktiv*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Die Angebotsstrategie für die Kampagne:

* *[!UICONTROL Cost per Sale]:* (Nur Shopping-Kampagnen) Das Werbenetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote auf der Grundlage von [!UICONTROL Target CPS] (Kosten pro Verkauf). Sie zahlen nur, wenn ein Klick auf Ihre Produktanzeige innerhalb von 24 Stunden zu einem Verkauf führt. **Hinweis:** Schließen Sie keine Kampagnen mit dieser Angebotsstrategie in Portfolios ein. Die Optimierung von Suche, Social und Commerce steht nicht für Kampagnen mit dieser Angebotsstrategie zur Verfügung.

  Nachdem Sie eine Einkaufskampagne für Marken mit dieser Angebotsstrategie gespeichert haben, können Sie die Angebotsstrategie nicht mehr ändern. Bei anderen Kampagnentypen ist diese Strategie nur für neue Kampagnen verfügbar.

* *[!UICONTROL CPV]* (Nur Audience CTV-Videokampagnen) Verwendet das CPV-Modell (Cost-per-view). Search, Social und Commerce bieten keine Optimierung für Kampagnen mit dieser Angebotsstrategie, die in Portfolios enthalten sind.

* *[!UICONTROL Enhanced CPC]:* (Kampagnen in Zielgruppen-, Such- und Shopping-Netzwerken) Verwendet das erweiterte &quot;Cost-per-Click&quot;-Modell des Werbenetzwerks, mit dem das Werbenetzwerk das CPC-Angebot (Cost-per-Click) für jede Auktion automatisch ändern kann, um Konversionen zu maximieren, indem Konversionen verwendet werden, die im Anzeigennetzwerk angegeben sind (nicht in Search, Social und Commerce), während Sie versuchen, durchschnittliche CPC unterhalb Ihrer maximalen CPC.

  Wenn Sie eine Kampagne mit eCPC zu einem optimierten Portfolio von Search, Social und Commerce hinzufügen, optimiert Search, Social und Commerce die Basisangebote und - wenn die Option &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; aktiviert ist - das Kampagnenbudget. Das Werbenetzwerk optimiert alle Angebotsanpassungen und kann die von Search, Social und Commerce generierten Angebote zum Zeitpunkt der Benutzerabfrage basierend auf proprietären Daten und Einblicken ändern. **Vorsicht:** Verwenden Sie eCPC-Kampagnen in Portfolios nur, wenn die im Werbenetzwerk verfolgten Konversionen insgesamt mit dem Portfolioziel übereinstimmen.

* *[!UICONTROL Manual CPC]*: (Shopping-Kampagnen für Marken; [!DNL Microsoft Store Ads] Kampagnen; veraltet für andere Kampagnentypen) Verwendet das CPC-Modell (Cost-per-Click). Bei einigen Anzeigentypen können Sie optional zulassen, dass das Werbenetzwerk Angebote für die Kampagne ändert:

   * **[!UICONTROL Enable Enhanced CPC]** (standardmäßig deaktiviert): Diese Option entspricht der Verwendung der Option &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] Kampagnen) Verwendet das CPA-Modell (Cost per Akquise).

* *[!UICONTROL Manual CPM]* (Nur Zielgruppen-Kampagnen und Zielgruppen-Videokampagnen) Verwendet das CPM-Modell (Cost-per-Tausend-Impressions), für das Sie angeben, was Sie pro 1.000 angezeigten Impressionen ausgeben möchten. Kampagnen mit dieser Angebotsstrategie werden nicht optimiert, wenn sie in Portfolios enthalten sind.

* *[!UICONTROL Maximize Clicks]:* (Such- und Shopping-Kampagnen) Das Werbenetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote, um Klicks zu maximieren. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein, um sicherzustellen, dass das Werbenetzwerk nicht mehr als einen bestimmten Betrag für jeden Klick zahlt. **Vorsicht:** Wenn Sie eine Kampagne mit dieser Strategie zu einem Portfolio hinzufügen, sorgt die Klickgewichtung (nicht das Portfolioziel) für Gebote.

* *[!UICONTROL Maximize Conversion Value]:* (Such- und Shopping-/Smart-Shopping-Netzwerke, Performance-Max-Kampagnen) Das Anzeigennetzwerk — nicht &quot;Search, Social und Commerce&quot; — optimiert Gebote, um den Konversionswert zu maximieren. Geben Sie optional einen ROAS (0) als Prozentsatz ein. **[!UICONTROL Target Return on Ad Spend]** **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios.

* *[!UICONTROL Maximize Conversions]:* (Performance max campaigns and campaigns on the search network or audience network (but not audience videos or linked TV)) Das Werbenetzwerk — not Search, Social, &amp; Commerce — optimiert Gebote zur Maximierung von Konversionen. Geben Sie optional einen **[!UICONTROL Target CPC]** (Kosten pro Klick) ein. Für Zielgruppenkampagnen können Sie auch einen optionalen Wert **[!UICONTROL Target CPA]** (Kosten pro Akquise) eingeben. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios.

* *[!UICONTROL Target CPA]:* (Kampagnen im Suchnetzwerk) Das Werbenetzwerk — nicht &quot;Search, Social, &amp; Commerce&quot; — optimiert Gebote auf der Grundlage eines optionalen **[!UICONTROL Target CPA]** (Kosten pro Akquise), des 30-tägigen Durchschnittsbetrags, den Sie für eine Akquise (Konversion) bezahlen möchten. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target CPA].

  Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

* *[!UICONTROL Target Impression Share]:* (Kampagnen im Suchnetzwerk) Das Werbenetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote, um eine zielgerichtete Impressions-Freigabe und Anzeigenposition zu erzielen. Geben Sie optional einen **[!UICONTROL Target Impression Share]** als Prozentsatz, den **[!UICONTROL Target Ad Position]** und einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein. **Hinweis:** Diese Option wird in Hybridportfolios nicht unterstützt.

* *[!UICONTROL Target Return on Ad Spend]:* (Kampagnen in den Such- und Shopping-Netzwerken) Das Werbenetzwerk — nicht &quot;Search, Social, &amp; Commerce&quot; — optimiert Gebote auf Grundlage Ihrer **[!UICONTROL Target ROAS]** (Rendite aus Werbeausgaben), angegeben als Prozentsatz. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein, um sicherzustellen, dass das Werbenetzwerk nicht mehr als einen bestimmten Betrag für jeden Klick zahlt. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target ROAS].

  Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Nur Shopping-Kampagnen; schreibgeschützt für bestehende Kampagnen) Das Land, in dem
die Produkte der Kampagne werden verkauft. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (Nur Zielgruppenkampagnen; optional) Verknüpft die Kampagne mit einem bestimmten Merchant Center Store für automatisierte Feed-basierte Anzeigen und nicht mit responsiven Anzeigen. Wenn Sie diese Option auswählen, geben Sie die [!UICONTROL Merchant ID] und [!UICONTROL Products] an. Sie müssen Anzeigengruppen für die Kampagne erstellen, Sie müssen jedoch keine Anzeigen erstellen.

Nachdem Sie die Kampagne mit einem Store verknüpft und die Einstellungen gespeichert haben, können Sie diese Option nicht mehr ändern.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (Zielgruppenkampagnen, die nur mit einem Händler-Center-Store verknüpft sind) Die zu bewertenden Produkte. Standardmäßig ist *[!UICONTROL All products]* ausgewählt. Um nur Produkte mit bestimmten Attributen zu bewerben, wählen Sie &quot;*[!UICONTROL Filter products]*&quot;und geben Sie bis zu sieben Kombinationen aus Produktdimension und -attribut an, nach denen Ihre Produkte gefiltert werden sollen. Alle angegebenen Werte müssen gelten, damit Anzeigen für das Produkt angezeigt werden. Um beispielsweise Anzeigen für Acme-Heimtiervorräte anzuzeigen, können Sie die Filter `Custom Label 1=animals`, `Category=pet supplies` und `Brand=Acme Pet Supplies` erstellen.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Nur Performance max campaigns) Die Sprache der Anzeige, die mit der Sprache der Sites übereinstimmen sollte, auf denen Ihre Anzeige erscheinen kann. [!DNL Microsoft Advertising] bestimmt die Sprache eines Benutzers anhand verschiedener Signale, einschließlich der Abfrage des Benutzers, des Landes des Herausgebers und der Spracheinstellung des Benutzers.

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

Informationen zur Verfügbarkeit finden Sie in der Hilfe zu Microsoft Advertising , um zu verhindern, dass Anzeigen auf bestimmten Websites erscheinen.](https://help.ads.microsoft.com/#apex/bae/en/14061/0)[

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

**[!UICONTROL Track Product Group]:** (Nur für [!UICONTROL EF Redirect]) Nicht implementiert

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (pro Asset-Gruppe)

**[!UICONTROL Asset Group Name]:** Der Name des Asset-Ordners (Asset-Gruppe).

**[!UICONTROL Asset Group Status]:** Der Status der Asset-Gruppe: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Die endgültige URL für alle Anzeigen, die von der Asset-Gruppe erstellt wurden.

**[!UICONTROL Images]:** Bis zu 20 Bilder für die Anzeige, darunter mindestens ein quadratisches Bild und ein Landschaftsbild. Siehe [[!DNL Microsoft Advertising] Richtlinien für Bilder](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Sie können Bilder hochladen oder aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* So laden Sie Bilder hoch:

   1. Klicken Sie auf der Registerkarte [!UICONTROL Upload from Device] auf **[!UICONTROL +]** und wählen Sie Bilder von Ihrem Gerät oder Netzwerk aus.

   1. Für jedes Bild:

      1. Wählen Sie das Seitenverhältnis aus.

      1. Ziehen Sie das Zuschnittrahmen nach Bedarf an die gewünschte Position, um den sichtbaren Teil des Bildes auszuwählen und die Größe des sichtbaren Teils des Bildes nach Möglichkeit anzupassen.

      1. (Optional) Wählen Sie zusätzliche Seitenverhältnisse aus und positionieren Sie das Bild nach Bedarf für jedes ausgewählte Seitenverhältnis neu und ändern Sie die Größe.

         Für jedes ausgewählte Seitenverhältnis wird ein Asset erstellt.

      1. Klicken Sie auf **[!UICONTROL Proceed]**.

   1. Wenn Sie alle gewünschten Bilder angegeben haben, klicken Sie auf **[!UICONTROL Upload]**.

* Um Bilder aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Bilder aus.

**[!UICONTROL Logos]:** Mindestens ein Logo. Sie können bis zu fünf einbeziehen. Siehe [[!DNL Microsoft Advertising] Asset-Richtlinien](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Sie können Bilder hochladen oder aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* So laden Sie Bilder hoch:

   1. Klicken Sie auf der Registerkarte [!UICONTROL Upload from Device] auf **[!UICONTROL +]** und wählen Sie Bilder von Ihrem Gerät oder Netzwerk aus.

   1. Für jedes Bild:

      1. Wählen Sie das Seitenverhältnis aus.

      1. Ziehen Sie das Zuschnittrahmen nach Bedarf an die gewünschte Position, um den sichtbaren Teil des Bildes auszuwählen und die Größe des sichtbaren Teils des Bildes nach Möglichkeit anzupassen.

      1. (Optional) Wählen Sie zusätzliche Seitenverhältnisse aus und positionieren Sie das Bild nach Bedarf für jedes ausgewählte Seitenverhältnis neu und ändern Sie die Größe.

         Für jedes ausgewählte Seitenverhältnis wird ein Asset erstellt.

      1. Klicken Sie auf **[!UICONTROL Proceed]**.

   1. Wenn Sie alle gewünschten Bilder angegeben haben, klicken Sie auf **[!UICONTROL Upload]**.

* Um Bilder aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Bilder aus.

**[!UICONTROL Headlines]:** Mindestens drei und bis zu 15 kurze Überschriften mit jeweils maximal 30 Zeichen. Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* Texteingabe:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Long Headlines]:** Mindestens eine und bis zu fünf lange Überschriften mit jeweils maximal 90 Zeichen. Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* Texteingabe:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Descriptions]:** Mindestens zwei und bis zu fünf Beschreibungen mit jeweils maximal 90 Zeichen. Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* Texteingabe:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Call to Action]:** Der Aktionsaufruf, der in die Anzeige aufgenommen werden soll. Standardmäßig ist *[!UICONTROL Act Now]* ausgewählt.

**[!UICONTROL Business Name]:** Der Geschäftsname mit maximal 25 Zeichen. Es kann keine Skripte, HTML oder andere Markup-Sprachen enthalten.

**[!UICONTROL Audience Signal]:** (Optional) [!DNL Microsoft Advertising] Zielgruppen, die als Zielgruppensignale für die Kampagne verwendet werden. [!DNL Microsoft Advertising] Modelle für maschinelles Lernen verwenden die Zielgruppen, um ähnliche Websurfer zu finden wie Targeting, und zeigen möglicherweise auch Anzeigen für Zielgruppen an, die nicht als Signale angegeben sind, um Sie bei der Erreichung Ihrer Leistungsziele zu unterstützen. Wählen Sie Zielgruppen aus, die am ehesten konvertiert werden.

>[!NOTE]
>Zielgruppensignale unterscheiden sich von [Zielgruppenzielen auf Anzeigengruppenebene](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Ermöglicht die Angabe einer anderen Asset-Gruppe.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Gibt an, ob *[!UICONTROL Use account conversion goals for this campaign]* (der Standardwert) oder *[!UICONTROL Use campaign specific conversion goals]* verwendet werden soll. Wenn Sie Konversionsziele für die Kampagne festlegen, wählen Sie die Ziele aus der Liste aller verfügbaren Ziele aus. **Hinweis:** Ziele werden täglich synchronisiert, sodass in den letzten 24 Stunden erstellte Ziele möglicherweise nicht aufgeführt werden. Um die Liste zu aktualisieren, synchronisieren Sie die Anzeigennetzwerkdaten ](/help/search-social-commerce/campaign-management/campaigns/sync-network.md) manuell.[

>[!TIP]
>
>Wenn die Kampagne Teil eines hybriden Portfolios ist, empfiehlt es sich, kampagnenspezifische Ziele zu verwenden, die den Konversionszielen im Portfolio-Ziel entsprechen. Die Einbeziehung zusätzlicher Konversionsziele kann sich auf die Portfolioleistung auswirken.
>
> Führen Sie jedoch für Kampagnen in hybriden Portfolios, für die Sie [Ziele in das Werbenetzwerk hochladen](/help/search-social-commerce/tools/objective-upload-to-networks.md), im Editor des Anzeigennetzwerks anstelle von hier Folgendes aus: a) Fügen Sie die hochgeladene Portfoliozielmetrik &quot;Search, Social und Commerce&quot;(beginnend mit &quot;O_ACS_OBJ&quot;) als Konversionsziel für die Kampagne hinzu und b) fügen Sie alle Kampagnenziele hinzu, die Konversionen, die vom universellen verfolgt werden ), da von Anzeigen-Netzwerken getrackte Metriken nicht mit dem Ziel in das Werbenetzwerk hochgeladen werden.[!DNL Microsoft Advertising]

>[!MORELIKETHIS]
>
>* [Verwalten von Kampagnen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
