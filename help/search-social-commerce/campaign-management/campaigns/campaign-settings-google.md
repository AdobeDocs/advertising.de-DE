---
title: '''[!DNL Google Ads] Kampagneneinstellungen'
description: Verweisen Sie auf die Einstellungen für [!DNL Google Ads] Kampagnen.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: 7b4818260fad61a773fb7261cbcdfd84bee84d42
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---

# [!DNL Google Ads] Kampagneneinstellungen

## \[Bildschirm zur Kampagnenerstellung\]

**[!UICONTROL Campaign Type]:** (Nur bei der Kampagnenerstellung verfügbar) Wo Anzeigen platziert werden und welche Anzeigentypen die Kampagne enthalten kann:

* *[!UICONTROL Search Network Only]:* Zeigt Anzeigen im Suchnetzwerk an, einschließlich [!DNL Google] Suchergebnisse und, optional, Suchpartner-Sites. Sie müssen Suchbegriffe für jede Anzeigengruppe angeben.

* *[!UICONTROL Search with Display Select]:* Zeigt Anzeigen im Suchnetzwerk an (einschließlich [!DNL Google] Suchergebnisse und optional Suchpartner-Sites) anzeigen und möglicherweise Anzeigen auf Display-Netzwerkseiten anzeigen. im Display-Netzwerk, [!DNL Google Ads] zeigt Ihre Anzeigen selektiv mithilfe automatisierter Angebote an, unabhängig von der Angebotsstrategie der Kampagne. Geben Sie für Suchanzeigen Suchbegriffe für jede Anzeigengruppe an. Geben Sie für Display-Anzeigen Platzierungen an und geben Sie optional Suchbegriffe für jede Anzeigengruppe an.

* *[!UICONTROL Shopping Network]:* Zeigt Produktanzeigen an, die [!DNL Google] generiert automatisch basierend auf Ihren Produkten in [!DNL Google Merchant Center] on [!DNL Google Shopping], den Bereich neben [!DNL Google] Suchergebnisse (getrennt von Textanzeigen) und (optional) Suchpartner-Websites. Für jede Anzeigengruppe in der Kampagne können Sie Produktgruppen für die Werbung angeben.

* *[!UICONTROL Display Network Only]:* Zeigt Anzeigen im Display-Netzwerk an. Für jede Anzeigengruppe müssen Sie Platzierungen angeben und können optional Suchbegriffe angeben.

* *[!UICONTROL Performance Max]:* (Beta-Funktion) Zeigt Konversionen für Ihre Anzeigen kanalübergreifend an und optimiert sie mithilfe von [!DNL Google Ads] intelligentes Bidding. In den Kampagneneinstellungen müssen Sie eine oder mehrere Asset-Gruppen angeben, zu denen Bilder, Logos, Überschriften, Beschreibungen, optionale Videos und Zielgruppensignale gehören. [!DNL Google Ads] kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen (z. B. [!DNL YouTube], [!DNL Gmail]oder [!DNL Search]).

  **Hinweise:**

   * Es sind nur erforderliche Einstellungen verfügbar. Für optionale Einstellungen melden Sie sich bei der [!DNL Google Ads] Editor.

   * Links zu [!DNL Google Merchant Center] -Produkt-Feeds werden nicht unterstützt.

   * Unterstützung für die Auflistung von Gruppen ist nicht verfügbar. Um Daten für die Auflistung von Gruppen zu verwalten und anzuzeigen, melden Sie sich bei der [!DNL Google Ads] Editor.

   * Die Hybrid-Optimierung wird unterstützt. Angebotsstrategieziele und Kampagnenbudgets werden auf Kampagnenebene festgelegt.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der im Konto eindeutig ist.

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

* *[!UICONTROL Enhanced CPC]:* (Nicht verfügbar für maximale Leistung oder vorhandene, schreibgeschützte [!DNL Gmail] Kampagnen) Verwendet das erweiterte &quot;Cost-per-Click&quot;-Modell des Werbenetzwerks, das es dem Werbenetzwerk ermöglicht, das Angebot pro Klick (Cost-per-Click) für jede Auktion automatisch zu ändern, um Konversionen zu maximieren, indem Konversionen verwendet werden, die im Werbenetzwerk (nicht in Search, Social und Commerce) angegeben sind, während versucht wird, den durchschnittlichen CPC unter Ihrem maximalen CPC zu halten.

Wenn Sie eine Kampagne mit eCPC zu einem optimierten Portfolio für Suche, Social und Handel hinzufügen, optimiert Search, Social und Commerce die Basisangebote und - wenn die Variable[!UICONTROL Auto adjust campaign budget limits]Die Option ist aktiviert - das Kampagnenbudget. Das Werbenetzwerk optimiert alle Angebotsanpassungen und kann die von Search, Social und Commerce generierten Angebote zum Zeitpunkt der Benutzerabfrage basierend auf proprietären Daten und Einblicken ändern. **Vorsicht:** Verwenden Sie eCPC-Kampagnen in Portfolios nur, wenn die im Werbenetzwerk verfolgten Konversionen insgesamt mit dem Portfolioziel übereinstimmen. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (Standard): (Nicht verfügbar für Kampagnen mit maximaler Leistung) Verwendet das CPC-Modell (Cost-per-Click). Sie können optional zulassen, dass das Werbenetzwerk Angebote für die Kampagne ändert:

   * **[!UICONTROL Enable Enhanced CPC]** (standardmäßig deaktiviert): Dies entspricht der Verwendung des[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Such-, Anzeige- und Einkaufskampagnen) Das Werbenetzwerk - nicht &quot;Search, Social, &amp; Commerce&quot; - optimiert Gebote zur Maximierung von Klicks. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick), um sicherzustellen, dass das Werbenetzwerk nicht mehr als einen bestimmten Betrag für jeden Klick zahlt. **Vorsicht:** Wenn Sie eine Kampagne mit dieser Strategie zu einem Portfolio hinzufügen, werden die Angebote von der Klickgewichtung und nicht vom Portfolioziel bestimmt.

* *[!UICONTROL Maximize Conversion Value]:* (Such-, Leistungs- und Smart-Shopping-Kampagnen) Das Anzeigennetzwerk - nicht &quot;Search, Social&quot;und &quot;Commerce&quot;- optimiert Gebote zur Maximierung des Konversionswerts. Geben Sie optional eine **[!UICONTROL Target Return on Ad Spend]** (ROAS) als Prozentsatz. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios.

* *[!UICONTROL Maximize Conversions]:* (Kampagnen für Suche, Anzeige und Performance-Maximalwerte) Das Werbenetzwerk - nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;- optimiert Gebote zur Maximierung von Konversionen. Geben Sie optional eine **[!UICONTROL Target CPA]** (Kosten pro Akquise). **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios, jedoch nicht in standardmäßigen Portfolios.

* *[!UICONTROL Target CPA]:* (Display-Kampagnen; vorhandene Suchkampagnen) Das Werbenetzwerk — nicht &quot;Search, Social, &amp; Commerce&quot; — optimiert Gebote auf der Grundlage eines optionalen **[!UICONTROL Target CPA]** (Kosten pro Akquise), der Durchschnittsbetrag von 30 Tagen, den Sie für eine Akquise (Konversion) bezahlen möchten. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer beliebigen Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target CPA].

  Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

  Für neue Suchkampagnen: [!DNL Google Ads] hat diese Angebotsstrategie durch die Variable [!UICONTROL Maximize Conversions] -Strategie mithilfe einer [!UICONTROL Target CPA] -Wert. Bei vorhandenen Suchkampagnen mit dieser Strategie können Sie nur den Zielwert bearbeiten. Dadurch wird die Strategie in die [!UICONTROL Maximize Conversions] -Strategie unter Verwendung der angegebenen [!UICONTROL Target CPA] -Wert.

* *[!UICONTROL Target Impression Share]:* (Suchkampagnen) Das Werbenetzwerk - nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;- optimiert Gebote, um eine zielgerichtete Impressions-Freigabe und Anzeigenposition zu erzielen. Geben Sie optional einen **[!UICONTROL Target Impression Share]** als Prozentsatz die **[!UICONTROL Target Ad Position]** und ein **[!UICONTROL Max CPC]** (Kosten pro Klick). **Hinweis:** Diese Option wird in Portfolios nicht unterstützt.

* *[!UICONTROL Target Return on Ad Spend]:*  (Display- und Shopping-Kampagnen; vorhandene Suchkampagnen) Das Werbenetzwerk — nicht &quot;Search, Social, &amp; Commerce&quot; — optimiert Gebote auf der Basis eines angegebenen **[!UICONTROL Target ROAS]** (Rendite auf Werbeausgaben), angegeben als Prozentsatz. **Hinweis:** Verwenden Sie diese Option für Kampagnen in hybriden Portfolios (aber nicht in Standard-Portfolios) mit einer beliebigen Ausgabestrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target ROAS].

  Durchschnittliche Position und CPC-Angebotsdaten sind nicht für Kampagnen mit dieser Angebotsstrategie verfügbar.

  Für neue Suchkampagnen: [!DNL Google Ads] hat diese Angebotsstrategie durch die Variable [!UICONTROL Maximize Conversion Value] -Strategie mithilfe einer [!UICONTROL Target Return on Ad Spend value]. Bei vorhandenen Suchkampagnen mit dieser Strategie können Sie nur den Zielwert bearbeiten. Dadurch wird die Strategie in die [!UICONTROL Maximize Conversion Value] -Strategie unter Verwendung der angegebenen [!UICONTROL Target Return on Ad Spend] -Wert.

* *[!UICONTROL Viewable CPM]:* (Vorhanden, schreibgeschützt [!DNL Gmail] nur Kampagnen) Das Werbenetzwerk — nicht &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;— bietet nur Angebote für Anzeigen, die als sichtbar gemessen werden. **Hinweis:** Die Optimierung dieser Strategie wird in keinem Portfolio unterstützt.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Nur Shopping-Kampagnen; schreibgeschützt für bestehende Kampagnen) Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Nur Shopping-Kampagnen; Advertiser, die bereits am lokalen Shopping-Programm mit [!DNL Google Merchant Center] Geschäfte in den USA, Großbritannien, DE, FR, JP und AU; optional) Erlaubt [!DNL Google Ads] um Ihre lokalen Lagerbestandsdaten automatisch zu Ihren Shopping-Anzeigen auf Google.com hinzuzufügen.

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

      * Um nach einer Position zu suchen, geben Sie mindestens die ersten drei Zeichen der Position in das Eingabefeld ein oder fügen Sie sie ein. Klicken Sie im Suchergebnis auf **[!UICONTROL Include]** neben einem Speicherort, der eingeschlossen werden soll, oder **[!UICONTROL Exclude]** neben einem Standort, der ausgeschlossen werden soll.

   * (Standorte in der Nähe einer Adresse; nur enthaltene Ziele) Klicken Sie auf **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) und klicken Sie dann auf **[!UICONTROL Address]**. Geben Sie die Adresse und den Radius in Meilen oder Kilometern um die Zieladresse ein und klicken Sie dann auf **[!UICONTROL Add]**.

   * (Standorte in der Nähe geografischer Koordinaten; nur eingeschlossene Ziele) Klicken Sie auf **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) und klicken Sie dann auf **[!UICONTROL Coordinate]**. Geben Sie den Breiten- und Längengrad sowie den Radius in Meilen oder Kilometern um den Zielort ein und klicken Sie dann auf **[!UICONTROL Add]**.

* (Um eine Angebotsanpassung für einen eingeschlossenen Zielort hinzuzufügen) Geben Sie einen Angebotsanpassungswert ein:

* 0 %: Um keine Angebote für Anzeigen an diesem Ort anzupassen.

* \[Andere Werte von -90 % bis 300 %\]: Um das Angebot für Anzeigen an diesem Ort zu erhöhen oder zu verringern.

**Hinweis:**

* Search, Social und Commerce bietet keine automatisch angepassten Angebotsanpassungen für die folgenden Standortziele aufgrund von Einschränkungen in den Daten, [!DNL Google Ads] stellt die Zuordnung von Surfer-Standorten zu Standortzielen bereit:

   * Radius-Ziele.

   * Einige Standorte unterhalb der Ebene von Bundesland/Provinz/Region/Bezirk/Präfektur, für die [!DNL Google Ads] sendet keinen übergeordneten Ort in der URL des Surfers, einschließlich Flughäfen und Kongressvierteln der USA.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Nur Netzwerkanzeige) Spezifische Mobilnetzbetreiber für die Zielgruppenbestimmung; die Netzbetreiber werden nach Land sortiert. Wenn Sie keine auswählen, werden alle Zielgruppen ausgewählt.

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

**[!UICONTROL Images]:** Bis zu 15 Bilder für die Anzeige, darunter die folgenden Größen: 1) mindestens drei quadratische Bilder, 2) mindestens drei Landschaftsbilder und 3) mindestens ein Hochformat-Bild. Siehe [[!DNL Google Ads] Bildspezifikationen](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Sie können entweder Bilder hochladen oder aus Ihrem [!UICONTROL Asset Library] — aber nicht beide im selben Betrieb.

* So laden Sie Bilder hoch:

   1. Im [!UICONTROL Upload from Device] Registerkarte, klicken **[!UICONTROL +]** und wählen Sie Bilder von Ihrem Gerät oder Netzwerk aus.

   1. Für jedes Bild:

      1. Wählen Sie das Seitenverhältnis aus.

      1. Ziehen Sie das Zuschnittrahmen nach Bedarf an die gewünschte Position, um den sichtbaren Teil des Bildes auszuwählen und die Größe des sichtbaren Teils des Bildes nach Möglichkeit anzupassen.

      1. (Optional) Wählen Sie zusätzliche Seitenverhältnisse aus und positionieren Sie das Bild nach Bedarf für jedes ausgewählte Seitenverhältnis neu und ändern Sie die Größe.

         Für jedes ausgewählte Seitenverhältnis wird ein Asset erstellt.

      1. Klicken **[!UICONTROL Proceed]**.

   1. Wenn Sie mit der Angabe von Bildern fertig sind, klicken Sie auf **[!UICONTROL Upload]**.

* So wählen Sie Bilder aus [!UICONTROL Asset Library]klicken **[!UICONTROL Asset Library]** und wählen Sie die Bilder aus.

**[!UICONTROL Logos]:** Mindestens ein quadratisches (1:1) Logo und ein Querformatlogo (4:1). Sie können bis zu fünf von jeder Größe einbeziehen. Siehe [[!DNL Google Ads] Logo-Spezifikationen](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Sie können entweder Bilder hochladen oder aus Ihrem [!UICONTROL Asset Library] — aber nicht beide im selben Betrieb.

* So laden Sie Bilder hoch:

   1. Im [!UICONTROL Upload from Device] Registerkarte, klicken **[!UICONTROL +]** und wählen Sie Bilder von Ihrem Gerät oder Netzwerk aus.

   1. Für jedes Bild:

      1. Wählen Sie das Seitenverhältnis aus.

      1. Ziehen Sie das Zuschnittrahmen nach Bedarf an die gewünschte Position, um den sichtbaren Teil des Bildes auszuwählen und die Größe des sichtbaren Teils des Bildes nach Möglichkeit anzupassen.

      1. (Optional) Wählen Sie zusätzliche Seitenverhältnisse aus und positionieren Sie das Bild nach Bedarf für jedes ausgewählte Seitenverhältnis neu und ändern Sie die Größe.

         Für jedes ausgewählte Seitenverhältnis wird ein Asset erstellt.

      1. Klicken **[!UICONTROL Proceed]**.

   1. Wenn Sie mit der Angabe von Bildern fertig sind, klicken Sie auf **[!UICONTROL Upload]**.

* So wählen Sie Bilder aus [!UICONTROL Asset Library]klicken **[!UICONTROL Asset Library]** und wählen Sie die Bilder aus.

**[!UICONTROL Videos]:** (Optional) Mindestens ein und bis zu fünf, [!DNL YouTube] Videos mit einer Länge von mindestens 10 Sekunden. Sie können entweder URLs eingeben oder aus Ihrem [!UICONTROL Asset Library] — aber nicht beide im selben Betrieb.

* So geben Sie URLs ein:

   1. Im [!UICONTROL Enter Video Url] Registerkarte eine URL eingeben.

   1. (Optional) Um eine weitere URL hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die URL ein.

* So wählen Sie Videos aus [!UICONTROL Asset Library]klicken **[!UICONTROL Asset Library]** und wählen Sie die Videos aus.

**[!UICONTROL Headlines]:** Mindestens drei bis fünf kurze Überschriften mit maximal 30 Zeichen pro Kopf. Mindestens eine Überschrift darf maximal 15 Zeichen lang sein. Wenn die Option auf Kampagnenebene zur Aktivierung der endgültigen URL-Erweiterung in [!DNL Google Ads], dann [!DNL Google Ads] ersetzt diesen Wert durch eine benutzerdefinierte Überschrift, die auf dem Inhalt der Landingpage basiert.

Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] — aber nicht beide im selben Betrieb.

* Texteingabe:

   1. Im [!UICONTROL Enter Text] eingeben.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* So wählen Sie Assets aus Ihrem [!UICONTROL Asset Library]klicken **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Long Headlines]:** Mindestens eine und bis zu fünf lange Überschriften mit maximal 90 Zeichen pro Kopf. Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] — aber nicht beide im selben Betrieb.

* Texteingabe:

   1. Im [!UICONTROL Enter Text] eingeben.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* So wählen Sie Assets aus Ihrem [!UICONTROL Asset Library]klicken **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Descriptions]:** Mindestens zwei bis vier Beschreibungen mit jeweils maximal 90 Zeichen. Mindestens eine Beschreibung muss mindestens 30 Zeichen lang sein. Sie können entweder Text eingeben oder Assets aus Ihrem [!UICONTROL Asset Library] — aber nicht beide im selben Betrieb.

* Texteingabe:

   1. Im [!UICONTROL Enter Text] eingeben.

   1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* So wählen Sie Assets aus Ihrem [!UICONTROL Asset Library]klicken **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Call to Action]:** Der Aktionsaufruf, der in die Anzeige aufgenommen werden soll. Standardmäßig ist *[!UICONTROL Automated]* ausgewählt ist und [!DNL Google Ads] markiert den Aktionsaufruf. Sie können optional eine andere Aktion auswählen.

**[!UICONTROL Business Name]:** Der Unternehmensname mit maximal 25 Zeichen.

**[!UICONTROL Audience Signal]:** (Optional) [!DNL Google Ads] Zielgruppen, die als Zielgruppensignale für die Kampagne verwendet werden. [!DNL Google Ads] Modelle für maschinelles Lernen verwenden die Zielgruppen, um ähnliche Websurfer für das Targeting zu finden, und zeigen möglicherweise auch Anzeigen für Zielgruppen an, die nicht als Signale angegeben sind, um Sie bei der Erreichung Ihrer Leistungsziele zu unterstützen. Wählen Sie Zielgruppen aus, die am ehesten konvertiert werden.

>[!NOTE]
>Zielgruppensignale unterscheiden sich von [Zielgruppenziele auf Kampagnenebene und Anzeigengruppenebene](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Ermöglicht die Angabe einer anderen Asset-Gruppe.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Ob *[!UICONTROL Use account conversion goals for this campaign]* (Standardeinstellung) oder *[!UICONTROL Use campaign specific conversion goals]*. Wenn Sie sich dafür entscheiden, Konversionsziele für die Kampagne festzulegen, wählen Sie Standardziele aus und/oder erstellen Sie ein benutzerdefiniertes Ziel für die Kampagne.

Ziele werden täglich synchronisiert, sodass vorhandene Ziele, die in den letzten 24 Stunden erstellt wurden, möglicherweise nicht aufgelistet werden. So aktualisieren Sie die Liste: [Manuelles Synchronisieren der Daten des Anzeigennetzwerks](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Um ein benutzerdefiniertes Konversionsziel zu erstellen, klicken Sie auf **[!UICONTROL + Add custom goal]**, geben Sie den benutzerdefinierten Zielnamen ein, wählen Sie die [Konversionsaktionen](https://support.google.com/google-ads/answer/6032150) , um sie in das benutzerdefinierte Ziel einzubeziehen, und klicken Sie dann auf **[!UICONTROL Save]**. **Hinweis:** Jede Kampagne kann nur ein einziges benutzerdefiniertes Ziel haben.

>[!TIP]
>
>Wenn die Kampagne Teil eines Portfolios ist, verwenden Sie dieselben Konversionsziele wie das Ziel des Portfolios. Die Verwendung verschiedener Konversionsziele kann sich auf die Portfolioleistung auswirken.

>[!MORELIKETHIS]
>
>* [Verwalten von Kampagnen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
