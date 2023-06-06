---
title: "[!DNL Google Ads] Kampagneneinstellungen"
description: Verweisen Sie auf die Einstellungen für [!DNL Google Ads] Kampagnen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1958'
ht-degree: 0%

---

# [!DNL Google Ads] Kampagneneinstellungen

## \[Bildschirm zur Kampagnenerstellung\]

**[!UICONTROL Campaign Type]:** (Nur bei der Kampagnenerstellung verfügbar) Wo Anzeigen platziert werden und welche Anzeigentypen die Kampagne enthalten kann:

* *[!UICONTROL Search Network Only]:* Zeigt Anzeigen im Suchnetzwerk an, einschließlich [!DNL Google] Suchergebnisse und, optional, Suchpartner-Sites. Sie müssen Suchbegriffe für jede Anzeigengruppe angeben.

* *[!UICONTROL Search with Display Select]:* Zeigt Anzeigen im Suchnetzwerk an (einschließlich [!DNL Google] Suchergebnisse und optional Suchpartner-Sites) anzeigen und möglicherweise Anzeigen auf Display-Netzwerkseiten anzeigen. im Display-Netzwerk, [!DNL Google Ads] zeigt Ihre Anzeigen selektiv mithilfe automatisierter Angebote an, unabhängig von der Angebotsstrategie der Kampagne. Für Suchanzeigen müssen Sie Suchbegriffe für jede Anzeigengruppe angeben. für Display-Anzeigen müssen Sie Platzierungen angeben und optional Suchbegriffe für jede Anzeigengruppe angeben.

* *[!UICONTROL Shopping Network]:* Zeigt Produktanzeigen an, die [!DNL Google] generiert automatisch basierend auf Ihren Produkten in [!DNL Google Merchant Center] on [!DNL Google Shopping], den Bereich neben [!DNL Google] Suchergebnisse (getrennt von Textanzeigen) und (optional) Suchpartner-Websites. Für jede Anzeigengruppe in der Kampagne können Sie Produktgruppen für die Werbung angeben.

* *[!UICONTROL Display Network Only]:* Zeigt Anzeigen im Display-Netzwerk an. Für jede Anzeigengruppe müssen Sie Platzierungen angeben und optional Suchbegriffe angeben.

* *[!UICONTROL Performance Max]:* (Beta-Funktion) Zeigt Konversionen für Ihre Anzeigen kanalübergreifend an und optimiert sie mithilfe von [!DNL Google Ads] intelligentes Bidding. In den Kampagneneinstellungen müssen Sie eine oder mehrere Asset-Gruppen angeben, zu denen Bilder, Logos, Überschriften, Beschreibungen, optionale Videos und Zielgruppensignale gehören. [!DNL Google Ads] kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen (z. B. [!DNL YouTube], [!DNL Gmail]oder [!DNL Search]).

   **Hinweise:**

   * Es sind nur erforderliche Einstellungen verfügbar. Für optionale Einstellungen melden Sie sich bei der [!DNL Google Ads] Editor.

   * Links zu [!DNL Google Merchant Center] -Produkt-Feeds werden nicht unterstützt.

   * Unterstützung für die Auflistung von Gruppen ist nicht verfügbar. Um Daten für Auflistungsgruppen zu verwalten und anzuzeigen, melden Sie sich bei der [!DNL Google Ads] Editor.

   * Die Hybrid-Optimierung wird unterstützt. Angebotsstrategieziele und Kampagnenbudgets werden auf Kampagnenebene festgelegt.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der innerhalb des Kontos eindeutig ist.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Nur vorhandene schreibgeschützte Gmail-Kampagnen) Ob:

* *[!UICONTROL Target and Bid]* So zeigen Sie Anzeigen nur Benutzern an, die mit Zielgruppen verknüpft sind, die auch andere Ziele für die Anzeigengruppe erfüllen.

* *[!UICONTROL Bid Only]:*  Anzeigen auch für Personen anzeigen, die nicht mit Zielgruppen verbunden sind, solange sie andere Ziele auf Anzeigengruppenebene erfüllen. Sie können die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie jedoch höhere Angebote für diese Zielgruppen festlegen.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Angehalten*. Die Standardeinstellung für neue Werbekampagnen ist *Aktiv*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Kampagnen, die nur auf das Suchnetzwerk abzielen, einschließlich Einkaufskampagnen) Zeigt Ihre Anzeigen in den Suchpartnernetzwerken des Werbenetzwerks an. Standardmäßig ist diese Option *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Angebotsstrategie für die Kampagne:

* *[!UICONTROL Enhanced CPC]:* (Nicht verfügbar für maximale Leistung oder vorhandene, schreibgeschützte [!DNL Gmail] Kampagnen) Verwendet das erweiterte Modell &quot;Cost-per-Click&quot;(eCPC) des Werbenetzwerks, mit dem das Werbenetzwerk das Angebot &quot;Cost-per-Click&quot;(CPC) für jede Auktion automatisch ändern kann, um Konversionen zu maximieren, indem Konversionen verwendet werden, die im Werbenetzwerk (nicht in Search, Social und Commerce) angegeben sind, während versucht wird, den durchschnittlichen CPC unter Ihrem maximalen CPC zu halten.

Wenn Sie eine Kampagne mit eCPC zu einem optimierten Portfolio für Suche, Social und Handel hinzufügen, optimiert Search, Social und Commerce die Basisangebote und - wenn die Variable[!UICONTROL Auto adjust campaign budget limits]Die Option ist aktiviert - das Kampagnenbudget. Das Werbenetzwerk optimiert alle Angebotsanpassungen und kann die von Search, Social und Commerce generierten Angebote zum Zeitpunkt der Benutzerabfrage basierend auf proprietären Daten und Einblicken ändern. **Vorsicht:** Verwenden Sie eCPC-Kampagnen in Portfolios nur, wenn die im Werbenetzwerk verfolgten Konversionen insgesamt mit dem Portfolioziel übereinstimmen. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (Standardeinstellung): (Nicht verfügbar für Kampagnen mit der maximalen Leistung) Verwendet das CPC-Modell (Cost-per-Click). Sie können optional zulassen, dass das Werbenetzwerk Angebote für die Kampagne ändert:

   * **[!UICONTROL Enable Enhanced CPC]** (standardmäßig deaktiviert): Dies entspricht der Verwendung des[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Such-, Anzeige- und Einkaufskampagnen) Das Werbenetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote, um Klicks zu maximieren. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick), um sicherzustellen, dass das Werbenetzwerk nicht mehr als einen bestimmten Betrag für jeden Klick zahlt. **Vorsicht:** Wenn Sie eine Kampagne mit dieser Strategie zu einem Portfolio hinzufügen, werden die Angebote von der Klickgewichtung und nicht vom Portfolioziel bestimmt.

* *[!UICONTROL Maximize Conversion Value]:* (Such-, Leistungs- und Smart-Shopping-Kampagnen) Das Werbenetzwerk - nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;- optimiert Gebote, um den Konversionswert zu maximieren. Geben Sie optional eine **[!UICONTROL Target Return on Ad Spend]** (ROAS) als Prozentsatz. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios.

* *[!UICONTROL Maximize Conversions]:* (Kampagnen für Suche, Anzeige und Performance-Maximalwerte) Das Anzeigennetzwerk - nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;- optimiert Gebote, um Konversionen zu maximieren. Geben Sie optional eine **[!UICONTROL Target CPA]** (Kosten pro Akquise). **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios.

* *[!UICONTROL Target CPA]:* (Display-Kampagnen; vorhandene Suchkampagnen) Das Werbenetzwerk - nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;- optimiert Gebote auf der Grundlage eines optionalen **[!UICONTROL Target CPA]** (Kosten pro Akquise), der Durchschnittsbetrag von 30 Tagen, den Sie für eine Akquise (Konversion) bezahlen möchten. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer beliebigen Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target CPA].

   Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

   Für neue Suchkampagnen: [!DNL Google Ads] hat diese Angebotsstrategie durch die Variable [!UICONTROL Maximize Conversions] -Strategie mithilfe einer [!UICONTROL Target CPA] -Wert. Bei vorhandenen Suchkampagnen mit dieser Strategie können Sie nur den Zielwert bearbeiten. Dadurch wird die Strategie in die [!UICONTROL Maximize Conversions] -Strategie unter Verwendung der angegebenen [!UICONTROL Target CPA] -Wert.

* *[!UICONTROL Target Impression Share]:* (Suchkampagnen) Das Werbenetzwerk - nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;- optimiert Gebote, um eine zielgerichtete Impressions-Freigabe und Anzeigenposition zu erreichen. Geben Sie optional einen **[!UICONTROL Target Impression Share]** als Prozentsatz die **[!UICONTROL Target Ad Position]** und **[!UICONTROL Max CPC]** (Kosten pro Klick). **Hinweis:** Diese Option wird in Portfolios nicht unterstützt.

* *[!UICONTROL Target Return on Ad Spend]:*  (Display- und Shopping-Kampagnen; vorhandene Suchkampagnen) Das Werbenetzwerk — nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;- optimiert Gebote auf der Grundlage einer festgelegten **[!UICONTROL Target ROAS]** (Rendite auf Werbeausgaben), angegeben als Prozentsatz. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer beliebigen Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target ROAS].

   Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

   Für neue Suchkampagnen: [!DNL Google Ads] hat diese Angebotsstrategie durch die Variable [!UICONTROL Maximize Conversion Value] -Strategie mithilfe einer [!UICONTROL Target Return on Ad Spend value]. Bei vorhandenen Suchkampagnen mit dieser Strategie können Sie nur den Zielwert bearbeiten. Dadurch wird die Strategie in die [!UICONTROL Maximize Conversion Value] -Strategie unter Verwendung der angegebenen [!UICONTROL Target Return on Ad Spend] -Wert.

* *[!UICONTROL Viewable CPM]:* (Vorhanden, schreibgeschützt [!DNL Gmail] nur Kampagnen) Das Werbenetzwerk — nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;— bietet nur Angebote für Anzeigen, die als sichtbar gemessen werden. **Hinweis:** Die Optimierung dieser Strategie wird in keinem Portfolio unterstützt.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Nur Shopping-Kampagnen; schreibgeschützt für bestehende Kampagnen) Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Nur Shopping-Kampagnen; Advertiser, die bereits am lokalen Einkaufsprogramm mit [!DNL Google Merchant Center] Geschäfte in den USA, Großbritannien, DE, FR, JP und AU; optional) Ermöglicht [!DNL Google Ads] , um Ihre lokalen Inventarinformationen automatisch zu Ihren Shopping-Anzeigen auf Google.com hinzuzufügen.

**Tipp:** Wenn Sie diese Einstellung verwenden, schließen Sie lokale Anzeigen nicht im [!UICONTROL Inventory Filter] -Einstellung.

**Hinweis:** Lokale Lagerbestandsanzeigen erfordern zwei zusätzliche Feeds für [!DNL Google Merchant Center] - eine mit Ihren lokalen Produktdaten und eine andere mit Ihrem lokalen Produktbestand. Siehe [!DNL Google Ads] Dokumentation für weitere Informationen zu [lokale Einkaufsmöglichkeiten](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Nur Such- und Display-Netzwerke) Eine oder mehrere Zielsprachen für Anzeigen in der Kampagne.

[!DNL Google Ads] bestimmt die Sprache eines Benutzers aus dem [!DNL Google] Spracheinstellung oder die Sprache der Suchabfrage, der aktuellen Seite oder der zuletzt angezeigten Seiten auf der [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Bestimmte geografische Standorte des Benutzers, die als Ziele ein- oder ausgeschlossen werden sollen. Standardmäßig werden alle Orte als Ziel ausgewählt. Sie können Benutzer in einer beliebigen Kombination von Standorten ein- und ausschließen. Ausnahmen überschreiben Einschlüsse immer.

* Wählen Sie keine Orte aus, um alle Orte als Ziel auszuwählen.

* So schließen Sie bestimmte Orte ein oder aus:

   * (Länder, Bundesstaaten, Metropolregionen oder Städte) Klicken Sie auf **[!UICONTROL Location Target]** (![Standort-Ziel](/help/search-social-commerce/assets/location-target.png "Standort-Ziel")) und suchen Sie die Speicherorte, die ein- und ausgeschlossen werden sollen:

      * Um einen Ort und seine untergeordneten Positionen einzuschließen, klicken Sie einmal auf den Kreis daneben, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt.

      * Um eine Position auszuschließen, klicken Sie zweimal auf den Kreis neben ihr, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt.

      * Um einen Ort in seine Unterkomponenten (z. B. die Bundesstaaten, Metropolregionen oder Städte in den USA) einzuteilen, klicken Sie auf den Standortnamen.

      * Um nach einer Position zu suchen, geben Sie mindestens die ersten drei Zeichen der Position in das Eingabefeld ein oder fügen Sie sie ein. Klicken Sie in den Suchergebnissen auf **[!UICONTROL Include]** neben einem Speicherort, der eingeschlossen werden soll, oder **[!UICONTROL Exclude]** neben einem Standort, der ausgeschlossen werden soll.
   * (Standorte in der Nähe einer Adresse; Nur enthaltene Ziele) Klicken Sie auf **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) und klicken Sie dann auf **[!UICONTROL Address]**. Geben Sie die Adresse und den Radius in Meilen oder Kilometern um die Zieladresse ein und klicken Sie dann auf **[!UICONTROL Add]**.

   * (Standorte in der Nähe geografischer Koordinaten; Nur enthaltene Ziele) Klicken Sie auf **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) und klicken Sie dann auf **[!UICONTROL Coordinate]**. Geben Sie den Breiten- und Längengrad sowie den Radius in Meilen oder Kilometern um den Zielort ein und klicken Sie dann auf **[!UICONTROL Add]**.

   * (Standorte in der Nähe Ihrer [!DNL My Business] Orte, die als Positionserweiterungen verfügbar sind; Nur enthaltene Ziele) Klicken Sie auf **[!UICONTROL Location Group Target]** (![Standortgruppe](/help/search-social-commerce/assets/location-group.png "Standortgruppe")); Geben Sie optional ein Land, einen Bundesstaat, eine Metropolregion oder eine Stadt ein, um die Liste der verfügbaren Orte nach unten zu verschieben. und wählen Sie dann einen oder mehrere Orte aus der Liste der [!DNL Google My Business] Standorte. Geben Sie den Radius in Meilen oder Kilometern um die Zielorte an und klicken Sie dann auf **[!UICONTROL Add]**.


* (Um eine Angebotsanpassung für einen eingeschlossenen Zielort hinzuzufügen) Geben Sie einen Angebotsanpassungswert ein:

* 0 %: So passen Sie keine Angebote für Anzeigen an dieser Position an.

* \[Andere Werte von -90 % bis 300 %\]: Erhöhen oder Verringern des Angebots für Anzeigen an diesem Ort.

**Hinweis:**

* Search, Social und Commerce bietet keine automatisch angepassten Angebotsanpassungen für die folgenden Standortziele aufgrund von Einschränkungen in den Daten, die [!DNL Google Ads] stellt die Zuordnung von Surfer-Standorten zu Standortzielen bereit:

   * Radius-Ziele.

   * Einige Standorte unterhalb der Ebene von Bundesland/Provinz/Region/Bezirk/Präfektur, für die [!DNL Google Ads] sendet keinen übergeordneten Ort in der URL des Surfers, einschließlich Flughäfen und Kongressvierteln der USA.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Nur Display-Netz) Spezifische Mobilnetzbetreiber für die Zielgruppenbestimmung; die Luftfahrtunternehmen sind nach Land sortiert. Wenn Sie keine auswählen, werden alle Zielgruppen ausgewählt.

**[!UICONTROL Mobile Carriers]:** (Nur Netzwerk anzeigen) Spezifische Betriebssysteme für die Zielgruppenbestimmung. Wenn Sie keine auswählen, werden alle Zielgruppen ausgewählt.

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

**[!UICONTROL Track Product Group]:** (Für [!UICONTROL EF Redirect] nur) Nicht implementiert

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (pro Asset-Gruppe)

**[!UICONTROL Asset Group Name]:** Der Name der Asset-Gruppe. Links zu [!DNL Google Merchant Center] -Produkt-Feeds werden nicht unterstützt.

**[!UICONTROL Asset Group Status]:** Der Status der Asset-Gruppe: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Die endgültige URL für alle Anzeigen, die aus der Asset-Gruppe erstellt wurden. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Bis zu fünfzehn Bilder für die Anzeige, einschließlich der folgenden Größen: 1) mindestens drei quadratische Bilder, 2) mindestens drei Querformatbilder und 3) mindestens ein Hochformat. Siehe [[!DNL Google Ads] Bildspezifikationen](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). So laden Sie Bilder hoch:

1. Für jedes Bild:

   1. Klicken **[!UICONTROL +]** und wählen Sie ein Bild von Ihrem Gerät oder Netzwerk aus.

   1. Wählen Sie das Seitenverhältnis aus.

   1. Ziehen Sie das Zuschnittsfeld nach Bedarf an die gewünschte Position, um den sichtbaren Teil des Bildes auszuwählen, und klicken Sie dann auf **[!UICONTROL Proceed]**.

1. Wenn Sie mit der Angabe von Bildern fertig sind, klicken Sie auf **[!UICONTROL Upload]**.

**[!UICONTROL Logos]:** Mindestens ein quadratisches (1:1) Logo und ein Querformatlogo (4:1). Sie können bis zu fünf von jeder Größe einbeziehen. Siehe [[!DNL Google Ads] Logo-Spezifikationen](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). So laden Sie Bilder hoch:

1. Für jedes Bild:

   1. Klicken **[!UICONTROL +]** und wählen Sie ein Bild von Ihrem Gerät oder Netzwerk aus.

   1. Ziehen Sie das Zuschnittsfeld nach Bedarf an die gewünschte Position, um den sichtbaren Teil des Bildes auszuwählen, und klicken Sie dann auf **[!UICONTROL Proceed]**.

1. Wenn Sie mit der Angabe von Bildern fertig sind, klicken Sie auf **[!UICONTROL Upload]**.

**[!UICONTROL Videos]:** (Optional) Die URL für mindestens eine und bis zu fünf, [!DNL YouTube] Videos mit einer Länge von mehr als 10 Sekunden.

**[!UICONTROL Headlines]:** Mindestens drei und bis zu fünf kurze Überschriften mit jeweils maximal 30 Zeichen. Mindestens eine Überschrift darf maximal 15 Zeichen lang sein. Wenn die Option auf Kampagnenebene zur Aktivierung der endgültigen URL-Erweiterung in [!DNL Google Ads], dann [!DNL Google Ads] ersetzt diesen Wert durch eine benutzerdefinierte Überschrift, die auf dem Inhalt der Landingpage basiert.

**[!UICONTROL Long Headlines]:** Mindestens eine und bis zu fünf lange Überschriften mit maximal 90 Zeichen pro Kopf.

**[!UICONTROL Descriptions]:** Mindestens zwei bis vier Beschreibungen mit jeweils maximal 90 Zeichen. Mindestens eine Beschreibung muss mindestens 30 Zeichen lang sein.

**[!UICONTROL Call to Action]:** Der Aktionsaufruf, der in die Anzeige aufgenommen werden soll. Standardmäßig *[!UICONTROL Automated]* ausgewählt ist und [!DNL Google Ads] wählt den Aktionsaufruf aus. Sie können optional eine andere Aktion auswählen.

**[!UICONTROL Business Name]:** Der Unternehmensname mit maximal 25 Zeichen.

**[!UICONTROL Add new asset group]:** Ermöglicht die Angabe einer zusätzlichen Asset-Gruppe.

>[!MORELIKETHIS]
>
>* [Verwalten von Kampagnen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
