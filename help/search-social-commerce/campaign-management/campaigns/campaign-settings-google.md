---
title: '[!DNL Google Ads] Kampagneneinstellungen'
description: Referenzieren Sie die Einstellungen für [!DNL Google Ads] Kampagnen.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: ae98579b6b2edb54de5753e84891987a88184515
workflow-type: tm+mt
source-wordcount: '2576'
ht-degree: 0%

---

# [!DNL Google Ads] Kampagneneinstellungen

## \[Bildschirm zur Kampagnenerstellung\]

**[!UICONTROL Campaign Type]:** (Nur bei Kampagnenerstellung verfügbar) Wo Anzeigen platziert werden und welche Anzeigentypen die Kampagne enthalten kann:

* *[!UICONTROL Search Network Only]:* Zeigt Anzeigen im Suchnetzwerk an, die [!DNL Google] Suchergebnisse und optional Suchpartner-Sites enthalten. Sie müssen Suchbegriffe für jede Anzeigengruppe angeben.

* *[!UICONTROL Search with Display Select]:* Zeigt Anzeigen im Suchnetzwerk (einschließlich [!DNL Google] Suchergebnissen und optional Suchpartner-Sites) und zeigt möglicherweise Anzeigen auf Display-Netzwerkseiten an. Im Display-Netzwerk zeigt [!DNL Google Ads] Ihre Anzeigen selektiv mithilfe automatisierter Angebote an, unabhängig von der Angebotsstrategie der Kampagne. Geben Sie für Suchanzeigen Suchbegriffe für jede Anzeigengruppe an. Geben Sie für Display-Anzeigen Platzierungen an und geben Sie optional Suchbegriffe für jede Anzeigengruppe an.

* *[!UICONTROL Shopping Network]:* Zeigt Produktanzeigen an, die [!DNL Google] automatisch basierend auf Ihren Produkten in [!DNL Google Merchant Center] auf [!DNL Google Shopping] generiert, den Bereich neben [!DNL Google] Suchergebnissen (getrennt von Textanzeigen) und (optional) Suchpartner-Websites. Für jede Anzeigengruppe in der Kampagne können Sie Produktgruppen für die Werbung angeben.

* *[!UICONTROL Display Network Only]:* Zeigt Anzeigen im Display-Netzwerk an. Für jede Anzeigengruppe müssen Sie Platzierungen angeben und können optional Suchbegriffe angeben.

* *[!UICONTROL Performance Max]:* Zeigt Konversionen für Ihre Anzeigen über verschiedene Kanäle hinweg mithilfe von [!DNL Google Ads] intelligentem Gebot an und optimiert diese. In den Kampagneneinstellungen müssen Sie eine oder mehrere Asset-Gruppen angeben, zu denen Bilder, Logos, Überschriften, Beschreibungen, optionale Videos und Zielgruppensignale gehören. [!DNL Google Ads] kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen (wie [!DNL YouTube], [!DNL Gmail] oder [!DNL Search]).

  **Notizen:**

   * Es sind nur erforderliche Einstellungen verfügbar. Für optionale Einstellungen melden Sie sich beim [!DNL Google Ads]-Editor an.

   * Links zu [!DNL Google Merchant Center] -Produkt-Feeds werden nicht unterstützt.

   * Unterstützung für die Auflistung von Gruppen ist nicht verfügbar. Um Daten für die Auflistung von Gruppen zu verwalten und anzuzeigen, melden Sie sich beim [!DNL Google Ads]-Editor an.

   * Die Hybrid-Optimierung wird unterstützt. Angebotsstrategieziele und Kampagnenbudgets werden auf Kampagnenebene festgelegt.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der innerhalb des Kontos eindeutig ist.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Vorhandene schreibgeschützte Gmail-Kampagnen) Ob:

* *[!UICONTROL Target and Bid]* So zeigen Sie Anzeigen nur Benutzern an, die mit Zielgruppen verknüpft sind, die auch andere Ziele für die Anzeigengruppe erfüllen.

* *[!UICONTROL Bid Only]:* So zeigen Sie Anzeigen auch für Personen an, die nicht mit Zielgruppen verbunden sind, solange sie andere Ziele auf Anzeigengruppenebene erfüllen. Sie können die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie jedoch höhere Angebote für diese Zielgruppen festlegen.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Werbekampagnen ist *aktiv*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Kampagnen, die nur auf das Suchnetzwerk abzielen, einschließlich Einkaufskampagnen) Zeigt
Ihre Anzeigen in den Suchpartnernetzwerken des Werbenetzwerks. Standardmäßig ist diese Option *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Die Angebotsstrategie für die Kampagne:

* *[!UICONTROL Enhanced CPC]:* (Nicht verfügbar für maximale Leistung oder vorhandene schreibgeschützte [!DNL Gmail] Kampagnen) Verwendet das erweiterte Cost-per-Click-Modell (eCPC) des Werbenetzwerks, mit dem das Anzeigennetzwerk das CPC-Angebot (Cost-per-Click) für jede Auktion automatisch ändern kann, um Konversionen zu maximieren, indem Konversionen verwendet werden, die im Werbenetzwerk angegeben sind (nicht in Search, Social und Commerce), während versuchen, Ihre durchschnittliche CPC unter der maximalen CPC zu halten.

Wenn Sie eine Kampagne mit eCPC zu einem optimierten Portfolio von Search, Social und Commerce hinzufügen, optimiert Search, Social und Commerce die Basisangebote und - wenn die Option &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; aktiviert ist - das Kampagnenbudget. Das Werbenetzwerk optimiert alle Angebotsanpassungen und kann die von Search, Social und Commerce generierten Angebote zum Zeitpunkt der Benutzerabfrage basierend auf proprietären Daten und Einblicken ändern. **Vorsicht:** Verwenden Sie eCPC-Kampagnen in Portfolios nur, wenn die im Werbenetzwerk verfolgten Konversionen insgesamt mit dem Portfolioziel übereinstimmen. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (Standardeinstellung): (Nicht verfügbar für Kampagnen mit der maximalen Performance) Verwendet das CPC-Modell (Cost-per-Click). Sie können optional zulassen, dass das Werbenetzwerk Angebote für die Kampagne ändert:

   * **[!UICONTROL Enable Enhanced CPC]** (standardmäßig deaktiviert): Dies entspricht der Verwendung der Option &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Such-, Anzeige- und Einkaufskampagnen) Das Werbenetzwerk (nicht &quot;Search, Social, &amp; Commerce&quot;) optimiert Gebote, um Klicks zu maximieren. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein, um sicherzustellen, dass das Werbenetzwerk nicht mehr als einen bestimmten Betrag für jeden Klick zahlt. **Vorsicht:** Wenn Sie eine Kampagne mit dieser Strategie zu einem Portfolio hinzufügen, werden die Angebote von der Klickgewichtung und nicht vom Portfolioziel bestimmt.

* *[!UICONTROL Maximize Conversion Value]:* (Such-, Performance-Max- und Smart-Shopping-Kampagnen) Das Anzeigennetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote, um den Konversionswert zu maximieren. Geben Sie optional einen ROAS-Wert (**[!UICONTROL Target Return on Ad Spend]**) als Prozentsatz ein. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios. In hybriden Portfolios optimiert Search, Social und Commerce die Target-ROAS auf Kampagnenebene oder (falls verfügbar) auf Anzeigengruppenebene.

* *[!UICONTROL Maximize Conversions]:* (Search, display, performance max campaigns) Das Anzeigennetzwerk — nicht Search, Social, &amp; Commerce — optimiert Gebote zur Maximierung von Konversionen. Geben Sie optional einen **[!UICONTROL Target CPA]** (Kosten pro Akquise) ein. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios. In hybriden Portfolios optimiert Search, Social und Commerce die Target-CPA auf Kampagnenebene oder (falls verfügbar) auf Anzeigengruppenebene.

* *[!UICONTROL Target CPA]:* (Display campaigns) Das Werbenetzwerk — nicht &quot;Search, Social, &amp; Commerce&quot; — optimiert Gebote auf der Grundlage eines optionalen **[!UICONTROL Target CPA]** (Kosten pro Akquise), d. h. des Durchschnittsbetrags von 30 Tagen, den Sie für eine Akquise (Konversion) bezahlen möchten. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target CPA]. In hybriden Portfolios optimiert Search, Social und Commerce die Target-CPA auf Kampagnenebene oder (falls verfügbar) auf Anzeigengruppenebene.

  Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

* *[!UICONTROL Target Impression Share]:* (Suchkampagnen) Das Werbenetzwerk - nicht &quot;Search, Social und Commerce&quot; - optimiert Gebote, um eine zielgerichtete Impressions-Freigabe und Anzeigenposition zu erzielen. Geben Sie optional eine **[!UICONTROL Target Impression Share]** als Prozentsatz, die **[!UICONTROL Target Ad Position]** und eine **[!UICONTROL Max CPC]** (Kosten pro Klick) ein. **Hinweis:** Diese Option wird in Portfolios nicht unterstützt.

* *[!UICONTROL Target Return on Ad Spend]:* (Display- und Shopping-Kampagnen) Das Anzeigennetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote auf der Grundlage eines festgelegten **[!UICONTROL Target ROAS]** (Rendite aus Werbeausgaben), angegeben als Prozentsatz. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target ROAS]. In hybriden Portfolios optimiert Search, Social und Commerce die Target-ROAS auf Kampagnenebene oder (falls verfügbar) auf Anzeigengruppenebene.

  Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

* *[!UICONTROL Viewable CPM]:* (Vorhandene, schreibgeschützte [!DNL Gmail] Kampagnen) Das Werbenetzwerk — nicht &quot;Search&quot;, &quot;Social&quot;und &quot;Commerce&quot;— bietet nur Angebote für Anzeigen, die als sichtbar gemessen werden. **Hinweis:** Die Optimierung dieser Strategie wird in keinem Portfolio unterstützt.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Nur Shopping-Kampagnen; schreibgeschützt für bestehende Kampagnen) Das Land, in dem
die Produkte der Kampagne werden verkauft. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Nur Shopping-Kampagnen; Werbetreibende, die bereits am lokalen Shopping-Programm mit [!DNL Google Merchant Center] Geschäften in den USA, Großbritannien, DE, FR, JP und AU teilnehmen; optional) Ermöglicht [!DNL Google Ads] das automatische Hinzufügen Ihrer lokalen Inventarinformationen zu Ihren Shopping-Anzeigen auf Google.com.

**Tipp:** Wenn Sie diese Einstellung verwenden, schließen Sie lokale Anzeigen nicht in der Einstellung [!UICONTROL Inventory Filter] aus.

**Hinweis:** Lokale Lagerbestandsanzeigen erfordern zwei zusätzliche Feeds zu [!DNL Google Merchant Center] - einen mit Ihren lokalen Produktdaten und einen weiteren mit Ihrem lokalen Produktbestand. Weitere Informationen zu [lokalen Shopping-Anzeigen](https://www.google.com/retail/local-inventory-ads/) finden Sie in der Dokumentation zu [!DNL Google Ads] .

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Nur Such- und Display-Netzwerke) Eine oder mehrere Zielsprachen für Anzeigen in der Kampagne.

[!DNL Google Ads] bestimmt die Sprache eines Benutzers anhand der Spracheinstellung [!DNL Google] des Benutzers oder der Sprache der Suchabfrage, der aktuellen Seite oder der zuletzt angezeigten Seiten im [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Bestimmte geografische Benutzerstandorte, die als Ziele ein- oder ausgeschlossen werden sollen. Standardmäßig werden alle Orte als Ziel ausgewählt. Sie können Benutzer in einer beliebigen Kombination von Standorten ein- und ausschließen. Ausnahmen überschreiben Einschlüsse immer.

* Wählen Sie keine Orte aus, um alle Orte als Ziel auszuwählen.

* So schließen Sie bestimmte Orte ein oder aus:

   * (Länder, Bundesländer, Ballungsgebiete oder Städte) Klicken Sie auf &quot;**[!UICONTROL Location Target]**&quot;(![Standortziel](/help/search-social-commerce/assets/location-target.png "Standortziel")) und suchen Sie nach den Orten, die ein- und ausgeschlossen werden sollen:

      * Um einen Ort und seine untergeordneten Positionen einzubeziehen, klicken Sie einmal auf den benachbarten Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird.

      * Um eine Position auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

      * Um einen Ort in seine Unterkomponenten (z. B. die Bundesstaaten, Metropolregionen oder Städte in den USA) einzuteilen, klicken Sie auf den Standortnamen.

      * Um nach einer Position zu suchen, geben Sie mindestens die ersten drei Zeichen der Position in das Eingabefeld ein oder fügen Sie sie ein. Klicken Sie in den Suchergebnissen auf **[!UICONTROL Include]** neben einer Position, die eingeschlossen werden soll, oder auf **[!UICONTROL Exclude]** neben einer Position, die ausgeschlossen werden soll.

   * (Orte in der Nähe einer Adresse; nur eingeschlossene Ziele) Klicken Sie auf **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) und klicken Sie dann auf **[!UICONTROL Address]**. Geben Sie die Adresse und den Radius in Meilen oder Kilometern um die Zieladresse ein und klicken Sie dann auf **[!UICONTROL Add]**.

   * (Standorte in der Nähe geografischer Koordinaten; nur eingeschlossene Ziele) Klicken Sie auf **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) und klicken Sie dann auf **[!UICONTROL Coordinate]**. Geben Sie den Breiten- und Längengrad sowie den Radius in Meilen oder Kilometern um den Zielort ein und klicken Sie dann auf **[!UICONTROL Add]**.

* (Um eine Angebotsanpassung für einen eingeschlossenen Zielort hinzuzufügen) Geben Sie einen Angebotsanpassungswert ein:

* 0 %: Um keine Angebote für Anzeigen an diesem Ort anzupassen.

* \[Andere Werte von -90 % bis 300 %\]: Um das Angebot für Anzeigen an diesem Ort zu erhöhen oder zu verringern.

**Hinweis:**

* Search, Social und Commerce bieten keine automatisch angepassten Angebotsanpassungen für die folgenden Standortziele aufgrund von Einschränkungen in den Daten, die [!DNL Google Ads] für die Zuordnung von Surfer-Orten zu Standortzielen bereitstellt:

   * Radius-Ziele.

   * Einige Standorte unterhalb der Ebene von Bundesstaat/Provinz/Region/Bezirk/Präfektur, für die [!DNL Google Ads] keinen übergeordneten Standort in der URL des Surfers sendet, einschließlich Flughäfen und Kongressvierteln der USA.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Nur Netzwerk anzeigen) Spezifische Mobilnetzbetreiber, die als Ziel ausgewählt werden sollen; die Netzbetreiber werden sortiert.
nach Ländern. Wenn Sie keine auswählen, werden alle Zielgruppen ausgewählt.

**[!UICONTROL Mobile Carriers]:** (Nur Netzwerk anzeigen) Spezifische Betriebssysteme für das Targeting. Wenn Sie keine auswählen, werden alle Zielgruppen ausgewählt.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Customer Acquisition Goals]

**[!UICONTROL Customer Acquisition]:** (Nur Leistungsmax und Suchkampagnen) Zuweisen von Angeboten für neue Kunden und bestehende Kunden:

* *[!UICONTROL Bid equally for new and existing customers]*

* *[!UICONTROL Bid higher for new customers than for existing customers]*

  **Hinweis:** Um diese Einstellung zu verwenden, müssen Sie zunächst das neue Kundenakquise-Ziel für das [!DNL Google Ads] -Konto oder, falls zutreffend, für das Managerkonto aktivieren. Das Ziel definiert die zulässigen vorhandenen Kundenlisten und den zusätzlichen Konversionswert für neue Kunden in den Konvertierungseinstellungen. Siehe Schritte 1 bis 2 in der [!DNL Google Ads] Hilfe &quot;[Aktivieren des neuen Kundenakquise-Ziels](https://support.google.com/google-ads/answer/14007601)&quot;.

* *[!UICONTROL Only bid for new customers]*

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

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

**[!UICONTROL Asset Group Name]:** Der Name der Asset-Gruppe. Links zu [!DNL Google Merchant Center] -Produkt-Feeds werden nicht unterstützt.

**[!UICONTROL Asset Group Status]:** Der Status der Asset-Gruppe: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Die endgültige URL für alle Anzeigen, die von der Asset-Gruppe erstellt wurden. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Bis zu 15 Bilder für die Anzeige, einschließlich der folgenden Größen: 1) mindestens drei quadratische Bilder, 2) mindestens drei Querformat-Bilder und 3) mindestens ein Hochformat-Bild. Siehe [[!DNL Google Ads] Bildspezifikationen](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Sie können Bilder hochladen oder aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

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

**[!UICONTROL Logos]:** Mindestens ein quadratisches (1:1) Logo und ein Querformatlogo (4:1). Sie können bis zu fünf von jeder Größe einbeziehen. Siehe [[!DNL Google Ads] Logospezifikationen](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Sie können Bilder hochladen oder aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

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

**[!UICONTROL Videos]:** (Optional) Mindestens ein und bis zu fünf [!DNL YouTube] Videos, die mindestens 10 Sekunden lang sind. Sie können entweder URLs eingeben oder aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* So geben Sie URLs ein:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Video Url] eine URL ein.

   1. (Optional) Um eine weitere URL hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die URL ein.

* Um Videos aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Videos aus.

**[!UICONTROL Headlines]:** Mindestens drei und bis zu fünf kurze Überschriften mit maximal 30 Zeichen pro Kopf. Mindestens eine Überschrift darf maximal 15 Zeichen lang sein. Wenn die Option auf Kampagnenebene zum Aktivieren der endgültigen URL-Erweiterung auf [!DNL Google Ads] eingestellt ist, ersetzt [!DNL Google Ads] diesen Wert durch eine benutzerdefinierte Überschrift, die auf dem Inhalt der Landingpage basiert.

Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* Texteingabe:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Long Headlines]:** Mindestens eine und bis zu fünf lange Überschriften mit jeweils maximal 90 Zeichen. Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* Texteingabe:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Descriptions]:** Mindestens zwei und bis zu vier Beschreibungen mit jeweils maximal 90 Zeichen. Mindestens eine Beschreibung muss mindestens 30 Zeichen lang sein. Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] auswählen, aber nicht beide im selben Vorgang.

* Texteingabe:

   1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrem [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Call to Action]:** Der Aktionsaufruf, der in die Anzeige aufgenommen werden soll. Standardmäßig ist *[!UICONTROL Automated]* ausgewählt und [!DNL Google Ads] wählt den Aktionsaufruf aus. Sie können optional eine andere Aktion auswählen.

**[!UICONTROL Business Name]:** Der Geschäftsname mit maximal 25 Zeichen.

**[!UICONTROL Audience Signal]:** (Optional) [!DNL Google Ads] Zielgruppen, die als Zielgruppensignale für die Kampagne verwendet werden. [!DNL Google Ads] Modelle für maschinelles Lernen verwenden die Zielgruppen, um ähnliche Websurfer zu finden wie Targeting, und zeigen möglicherweise auch Anzeigen für Zielgruppen an, die nicht als Signale angegeben sind, um Ihnen bei der Erreichung Ihrer Leistungsziele zu helfen. Wählen Sie Zielgruppen aus, die am ehesten konvertiert werden.

>[!NOTE]
>Zielgruppensignale unterscheiden sich von [Zielgruppen-Zielen auf Kampagnenebene und Anzeigengruppenebene](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Primary Status]:** (Schreibgeschütztes Feld für vorhandene Asset-Gruppen in Kampagnen zur Leistungssteigerung) Warum die Asset-Gruppe nicht mit voller Kapazität bereitgestellt wird oder nicht. Dabei werden der Asset-Gruppenstatus sowie andere Signale wie Richtlinien- und Qualitätsgenehmigungen berücksichtigt. Die Werte können *ELIGIBLE,* *LIMITED,* *NOT_ELIGIBLE,* *PAUSED,* *PENDING,* *REMOVED,* *UNBEKANNT,* oder *UNSPECIFIIFIY enthalten. ED.*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]:** (Schreibgeschütztes Feld für vorhandene Asset-Gruppen in Kampagnen zur Leistungssteigerung) Zusätzliche Details zum primären Status der Asset-Gruppe. Die Werte können *ASSET_GROUP_DISAPPROVED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,* *ASSET_GROUP_UNDER_REVIEW,* *CAMPAIGN umfassen._ENDED,* *CAMPAIGN_PAUSED,* *CAMPAIGN_PENDING,* *CAMPAIGN_REMOVED,* *UNBEKANNT,* oder *UNSPECIFIED*. 1}

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Gibt an, ob *[!UICONTROL Use account conversion goals for this campaign]* (der Standardwert) oder *[!UICONTROL Use campaign specific conversion goals]* verwendet werden soll. Wenn Sie sich dafür entscheiden, Konversionsziele für die Kampagne festzulegen, wählen Sie Standardziele aus und/oder erstellen Sie ein benutzerdefiniertes Ziel für die Kampagne.

Ziele werden täglich synchronisiert, sodass vorhandene Ziele, die in den letzten 24 Stunden erstellt wurden, möglicherweise nicht aufgelistet werden. Um die Liste zu aktualisieren, synchronisieren Sie die Anzeigennetzwerkdaten ](/help/search-social-commerce/campaign-management/campaigns/sync-network.md) manuell.[

Um ein benutzerdefiniertes Konversionsziel zu erstellen, klicken Sie auf &quot;**[!UICONTROL + Add custom goal]**&quot;, geben Sie den Namen des benutzerdefinierten Ziels ein, wählen Sie die [Konversionsaktionen](https://support.google.com/google-ads/answer/6032150) aus, die in das benutzerdefinierte Ziel aufgenommen werden sollen, und klicken Sie dann auf &quot;**[!UICONTROL Save]**&quot;. **Hinweis:** Jede Kampagne kann nur ein benutzerdefiniertes Ziel haben.

>[!TIP]
>
>Wenn die Kampagne Teil eines hybriden Portfolios ist, empfiehlt es sich, kampagnenspezifische Ziele zu verwenden, die den Konversionszielen im Portfolio-Ziel entsprechen. Die Einbeziehung zusätzlicher Konversionsziele kann sich auf die Portfolioleistung auswirken.
>
>Führen Sie jedoch für Kampagnen in hybriden Portfolios, für die Sie Ziele [in das Anzeigennetzwerk hochladen](/help/search-social-commerce/tools/objective-upload-to-networks.md), im Editor des Anzeigennetzwerks anstelle von hier Folgendes aus: a) Fügen Sie die hochgeladene Portfoliozielmetrik &quot;Search, Social und Commerce&quot;als Konversionsaktion für die Kampagne hinzu und b) fügen Sie alle Kampagnenziele hinzu, die [!DNL Google]-verfolgte Konversionen enthalten, da Anzeigen-Netzwerk-Metriken werden mit dem Ziel nicht in das Werbenetzwerk hochgeladen.

>[!MORELIKETHIS]
>
>* [Verwalten von Kampagnen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
