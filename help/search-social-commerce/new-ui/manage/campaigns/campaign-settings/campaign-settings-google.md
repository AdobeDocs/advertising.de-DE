---
title: '[!DNL Google Ads] Kampagneneinstellungen'
description: Verweisen Sie auf die Einstellungen für  [!DNL Google Ads] -Kampagnen.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: cec8bc6b2b092a7c9a0ffec2da79acceab91b98b
workflow-type: tm+mt
source-wordcount: 3057
ht-degree: 0%

---

# [!DNL Google Ads] Kampagneneinstellungen

## \[Seitenanfang]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der innerhalb des Kontos eindeutig ist.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Paused*. Der Standardwert für neue Anzeigenkampagnen lautet *Aktiv*.

## Registerkarte [!UICONTROL Basic Settings]

*Nur neue Kampagnen*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign Type]:** Wo werden Anzeigen geschaltet und welche Anzeigentypen kann die Kampagne enthalten:

* *[!UICONTROL Search Network Only]:* Zeigt Anzeigen im Suchnetzwerk an, das [!DNL Google] Suchergebnisse und optional Partner-Sites umfasst. Für jede Anzeigengruppe müssen Schlüsselwörter angegeben werden.

* *[!UICONTROL Search with Display Select]:* Zeigt Anzeigen im Suchnetzwerk an (das [!DNL Google] Suchergebnisse und optional Suchpartnersites umfasst) und zeigt möglicherweise Anzeigen auf Display-Netzwerksites an. Im Display-Netzwerk zeigt [!DNL Google Ads] Ihre Anzeigen selektiv mithilfe automatisierter Gebote an, unabhängig von der Bid-Strategie der Kampagne. Geben Sie für Suchanzeigen Schlüsselwörter für jede Anzeigengruppe an, geben Sie für Display-Anzeigen Platzierungen an und geben Sie optional Schlüsselwörter für jede Anzeigengruppe an.

* *[!UICONTROL Shopping Network]:* Zeigt Produktanzeigen an, die [!DNL Google] automatisch basierend auf Ihren Produkten in [!DNL Google Merchant Center] auf [!DNL Google Shopping], dem Bereich neben [!DNL Google] Suchergebnissen (getrennt von Textanzeigen) und (optional) Partner-Websites für die Suche generiert. Für jede Anzeigengruppe in der Kampagne können Sie Produktgruppen angeben, die beworben werden sollen.

* *[!UICONTROL Display Network Only]:* Zeigt Anzeigen im Anzeigennetzwerk an. Für jede Anzeigengruppe müssen Sie Platzierungen angeben und können optional Schlüsselwörter angeben.

* *[!UICONTROL Performance Max]:* Zeigt Konversionen für Ihre Anzeigen kanalübergreifend mit [!DNL Google Ads] Smart Bidding an und optimiert sie. In den Kampagneneinstellungen müssen Sie eine oder mehrere Asset-Gruppen angeben, zu denen Bilder, Logos, Überschriften, Beschreibungen, optionale Videos und Zielgruppensignale gehören. [!DNL Google Ads] kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen (z. B. [!DNL YouTube], [!DNL Gmail] oder [!DNL Search]).

  **Hinweise:**

  * Es sind nur erforderliche Einstellungen verfügbar. Für optionale Einstellungen melden Sie sich beim [!DNL Google Ads] an.

  * Links zu [!DNL Google Merchant Center] Produkt-Feeds werden nicht unterstützt.

  * Die Auflistung von Gruppen wird nicht unterstützt. Um Daten für die Auflistung von Gruppen zu verwalten und anzuzeigen, melden Sie sich beim [!DNL Google Ads] an.

## Registerkarte [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Kampagnen, die nur auf das Suchnetzwerk abzielen, einschließlich Shopping-Kampagnen) Zeigt Ihre Anzeigen in den Suchpartnernetzwerken des Anzeigennetzwerks an. Standardmäßig ist diese Option *[!UICONTROL Off]*.

**[!UICONTROL Audience Target Method]:**(Bestehende, schreibgeschützte Gmail-Kampagnen) Ob:

* *[!UICONTROL Bid Only]:* Anzeigen auch Personen anzuzeigen, die nicht mit Zielgruppen verknüpft sind, solange sie andere Zielgruppen auf Anzeigengruppenebene erfüllen. Sie können jedoch die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie höhere Gebote für diese Zielgruppen festlegen.

* *[!UICONTROL Target and Bid]* Anzeigen nur Benutzern anzuzeigen, die mit Zielgruppen verknüpft sind und auch alle anderen Ziele für die Anzeigengruppe erfüllen.

**[!UICONTROL Contains EU Political Ads]:**(Gilt für Kampagnen, die sich an Zielgruppen in der Europäischen Union (EU) richten) Gibt an, ob die Kampagne politische Werbung gemäß den Anforderungen für in der Europäischen Union gemäß der EU-Verordnung 2024/90 geschaltete Anzeigen enthält: *[!UICONTROL No]* oder *[!UICONTROL Yes]*.

## Registerkarte [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

**[!UICONTROL Google Recommended Budget]:** (Optional; gilt für Kampagnen zur Leistungsmaximierung und Suche mit allen erforderlichen Einstellungen, die nur Anzeigengruppen enthalten) Klicken Sie auf **[!UICONTROL Show Recommendation]**, um das von [!DNL Google Ads] empfohlene Budget anzuzeigen. Derzeit sind nur Kampagnen mit weniger als 40.000 Keywords zulässig.

Für Kampagnen mit dem Typ „Performance Max“ und „Search“ sind die folgenden Einstellungen für Empfehlungen erforderlich:

* Bid-Strategietyp
* Endgültige URL
* Asset-Gruppen

Für Suchkampagnen sind außerdem die folgenden zusätzlichen Einstellungen für Recommendations erforderlich:

* Bid-Strategie-Ziel
* Land
* Sprache
* Ein eingeschlossener oder ausgeschlossener Speicherort
* Schlüsselwörter

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Die Bid-Strategie für die Kampagne:

* *[!UICONTROL Enhanced CPC]:* veraltet. [!DNL Google Ads] begann im Jahr 2025 automatisch mit [&#x200B; Änderung bestehender (verbesserter CPC](https://support.google.com/google-ads/answer/2464964)Angebotsstrategien) auf manuelle CPCs.

* *[!UICONTROL Manual CPC]* (Standard): (Für Kampagnen mit dem Typ „Performance Max“ nicht verfügbar) Verwendet das CPC-Modell (Cost Per Click) . Optional können Sie dem Werbenetzwerk erlauben, Gebote für die Kampagne zu ändern:

  * **[!UICONTROL Enable Enhanced CPC]** (standardmäßig deaktiviert): Dies entspricht der Verwendung der Option &quot;[!UICONTROL Enhanced CPC]&quot;, die nicht mehr unterstützt wird. [!DNL Google Ads] begann im Jahr 2025 automatisch mit [&#x200B; Änderung bestehender (verbesserter CPC](https://support.google.com/google-ads/answer/2464964)Angebotsstrategien) auf manuelle CPCs.

* *[!UICONTROL Maximize Clicks]:* (Search-, Display- und Shopping-Kampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um Klicks zu maximieren. Geben Sie optional einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein, um sicherzustellen, dass das Werbenetzwerk für jeden Klick nicht mehr als einen bestimmten Betrag zahlt. **Achtung:** Wenn Sie eine Kampagne mit dieser Strategie zu einem Portfolio hinzufügen, werden Gebote durch die Klickgewichtung gesteuert und nicht durch das Portfolioziel.

* *[!UICONTROL Maximize Conversion Value]:* (Search, Performance Max und Smart Shopping-Kampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um den Konversionswert zu maximieren. Geben Sie optional einen **[!UICONTROL Target Return on Ad Spend]** (ROAS) als Prozentsatz ein. **Hinweis** Verwenden Sie diese Option für Kampagnen in Portfolios mit Optimierung auf Kampagnen- oder Anzeigengruppenebene, nicht aber für Portfolios mit Optimierung auf Schlüsselwortebene. In Portfolios mit Optimierung auf Kampagnen- oder Anzeigengruppenebene optimiert Search, Social und Commerce die Target-ROAS auf Kampagnenebene oder (falls verfügbar) auf Anzeigengruppenebene.

* *[!UICONTROL Maximize Conversions]:* (Search-, Display- und Performance Max-Kampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um Konversionen zu maximieren. Geben Sie optional eine **[!UICONTROL Target CPA]** (Kosten pro Akquise) und die entsprechende **[!UICONTROL Portfolio]** ein. **Hinweis** Verwenden Sie diese Option für Kampagnen in Portfolios mit Optimierung auf Kampagnen- oder Anzeigengruppenebene, nicht aber für Portfolios mit Optimierung auf Schlüsselwortebene. In Portfolios mit Optimierung auf Kampagnen- oder Anzeigengruppenebene optimiert Search, Social und Commerce die Target-CPA auf Kampagnenebene oder (falls verfügbar) auf Anzeigengruppenebene.

* *[!UICONTROL Target CPA]:* (Nur-Anzeige-Kampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote auf der Grundlage einer optionalen **[!UICONTROL Target CPA]** (Kosten pro Akquise), die dem 30-Tage-Durchschnittsbetrag entspricht, den Sie für eine Akquise (Konversion) zahlen möchten. **Hinweis:** Kampagnen in Portfolios mit Optimierung auf Kampagnen- oder Anzeigengruppenebene (aber keine Portfolios mit Optimierung auf Schlüsselwortebene) mit einer beliebigen Ausgabenstrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target CPA]. In Portfolios mit Optimierung auf Kampagnen- oder Anzeigengruppenebene optimiert Search, Social und Commerce die Target-CPA auf Kampagnenebene oder (falls verfügbar) auf Anzeigengruppenebene.

  Durchschnittliche Positionsdaten und CPC-Bid-Daten sind für Kampagnen mit dieser Bid-Strategie nicht verfügbar.

* *[!UICONTROL Target Impression Share]:* (Suchkampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um einen Ziel-Impression-Anteil und eine Anzeigenposition zu erreichen. Geben Sie optional einen **[!UICONTROL Target Impression Share]** als Prozentsatz, den **[!UICONTROL Target Ad Position]** und einen **[!UICONTROL Max CPC]** (Kosten pro Klick) ein. **Hinweis:** Diese Option wird in Portfolios nicht unterstützt.

* *[!UICONTROL Target Return on Ad Spend]:* (Shopping-Kampagnen) Das Anzeigennetzwerk - nicht Search, Social und Commerce - optimiert Angebote auf der Grundlage eines bestimmten **[!UICONTROL Target ROAS]** (Rendite auf Werbeausgaben), angegeben als Prozentsatz. **Hinweis:** Verwenden Sie diese Option für Kampagnen in Portfolios mit Optimierung auf Kampagnen- oder Anzeigengruppenebene (aber nicht für Portfolios mit Optimierung auf Keyword-Ebene) mit einer beliebigen Ausgabenstrategie außer [!UICONTROL Weekly] oder [!UICONTROL Google Target ROAS]. In Portfolios mit Optimierung auf Kampagnen- oder Anzeigengruppenebene optimiert Search, Social und Commerce die Target-ROAS auf Kampagnenebene oder (falls verfügbar) auf Anzeigengruppenebene.

  Durchschnittliche Positionsdaten und CPC-Bid-Daten sind für Kampagnen mit dieser Bid-Strategie nicht verfügbar.

* *[!UICONTROL Viewable CPM]:* (Nur bestehende, schreibgeschützte [!DNL Gmail]) Das Anzeigennetzwerk - nicht Search, Social und Commerce - bietet nur für Anzeigen, die als sichtbar gemessen werden. **Hinweis** Die Optimierung für diese Strategie wird in keinem Portfolio unterstützt.

## Registerkarte [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Nur Einkaufskampagnen; nur für bestehende Kampagnen schreibgeschützt) Das Land, in dem
Die Kampagnenprodukte werden verkauft. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, für welche Produkte in der Kampagne geworben wird.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Nur Shopping-Kampagnen; Werbetreibende, die bereits am lokalen Shopping-Programm mit [!DNL Google Merchant Center] Geschäften in den USA, Großbritannien, DE, FR, JP und AU teilnehmen; optional) Ermöglicht es [!DNL Google Ads], Ihre lokalen Inventarinformationen automatisch zu Ihren Shopping-Anzeigen auf Google.com hinzuzufügen.

**Tipp:** Wenn Sie diese Einstellung verwenden, schließen Sie lokale Anzeigen in der [!UICONTROL Inventory Filter] nicht aus.

**Hinweis:** [!DNL Google Merchant Center] Für lokale Inventaranzeigen sind zwei zusätzliche Feeds erforderlich, eine für Ihre lokalen Produktdaten und eine weitere für Ihr lokales Produktinventar. Weitere Informationen zu (lokalen [) finden Sie in der [!DNL Google Ads]-](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## Registerkarte [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Nur Netzwerke zum Suchen und Anzeigen) Eine oder mehrere Zielsprachen für Anzeigen in der Kampagne.

[!DNL Google Ads] bestimmt die Sprache eines Benutzers anhand der [!DNL Google] Spracheinstellung des Benutzers oder der Sprache der Suchanfrage, der aktuellen Seite oder der kürzlich angezeigten Seiten im [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Bestimmte geografische Benutzerstandorte, die als Ziele ein- oder ausgeschlossen werden sollen. Standardmäßig sind alle Standorte als Ziel festgelegt. Sie können Benutzer in jeder beliebigen Kombination von Speicherorten ein- oder ausschließen. Ausnahmen überschreiben Einschlüsse immer.

* Um alle Standorte auszuwählen, wählen Sie keine Standorte aus.

* So zielen Sie auf bestimmte Standorte ab oder schließen sie aus:

  * (Länder, Bundesstaaten, Metropolregionen oder Städte) Klicken Sie auf **[!UICONTROL Location Target]** (![Standortziel](/help/search-social-commerce/assets/location-target.png "Standortziel")) und suchen Sie die Standorte, die ein- und ausgeschlossen werden sollen:

    * Um eine Position und ihre untergeordneten Positionen einzubeziehen, klicken Sie einmal auf den angrenzenden Kreis, sodass ein blaues Häkchen (![Einschließen](/help/search-social-commerce/assets/include.png "Einschließen")) angezeigt wird.

    * Um eine Position auszuschließen, klicken Sie zweimal auf den angrenzenden Kreis, sodass ein rotes Häkchen (![Ausschließen](/help/search-social-commerce/assets/exclude.png "Ausschließen")) angezeigt wird.

    * Um einen Standort in seine Unterkomponenten (z. B. Bundesstaaten, Metropolregionen oder Städte in den USA) zu erweitern, klicken Sie auf den Standortnamen.

    * Um nach einem Speicherort zu suchen, geben Sie mindestens die ersten drei Zeichen des Speicherorts in das Eingabefeld ein oder fügen Sie sie ein. Klicken Sie in den Suchergebnissen auf **[!UICONTROL Include]** neben einem einzuschließenden Speicherort oder auf **[!UICONTROL Exclude]** neben einem auszuschließenden Speicherort.

  * (Standorte in der Nähe einer Adresse; nur eingeschlossene Ziele) Klicken Sie auf **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")) und klicken Sie dann auf **[!UICONTROL Address]**. Geben Sie die Adresse und den Radius in Meilen oder Kilometern um die Adresse ein, die Sie ansprechen möchten, und klicken Sie dann auf **[!UICONTROL Add]**.

  * (Orte in der Nähe von geografischen Koordinaten; nur eingeschlossene Ziele) Klicken Sie auf **[!UICONTROL Radius Target]** (![Radius-Ziel](/help/search-social-commerce/assets/radius-target.png "Radius-Ziel")) und klicken Sie dann auf **[!UICONTROL Coordinate]**. Geben Sie den Breiten- und Längengrad sowie den Radius in Meilen oder Kilometern um den Zielort ein und klicken Sie dann auf **[!UICONTROL Add]**.

* (Um eine Gebotsanpassung für einen eingeschlossenen Zielspeicherort hinzuzufügen) Geben Sie einen Gebotsanpassungswert ein:

* 0 %: Keine Anpassung der Angebote für Anzeigen an diesem Ort.

* \[Andere Werte von -90% bis 300%\]: Erhöhen oder Verringern des Angebots für Anzeigen an diesem Ort.

**Hinweis:**

* Search, Social und Commerce bietet keine automatisch angepassten Angebotsanpassungen für die folgenden Standortziele, da die Daten, die [!DNL Google Ads] für die Zuordnung von Surfer-Standorten zu Standortzielen bereitstellt, Beschränkungen aufweisen:

  * Radius-Ziele.

  * Einige Orte unterhalb der Ebene Bundesland/Provinz/Region/Kreis/Präfektur, für die [!DNL Google Ads] keinen übergeordneten Ort in der URL des Surfers sendet, einschließlich Flughäfen und US-Kongresswahlbezirken.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## Registerkarte [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Nur Display-Netzwerk) Bestimmte Mobilnetzbetreiber, die angesprochen werden sollen. Die Anbieter werden sortiert.
Nach Land. Wenn Sie keine auswählen, werden alle als Ziel ausgewählt.

**[!UICONTROL Mobile Carriers]:** (Nur Netzwerk anzeigen) Spezifische Betriebssysteme für das Targeting. Wenn Sie keine auswählen, werden alle als Ziel ausgewählt.

## Registerkarte [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## Registerkarte [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## Registerkarte [!UICONTROL AI Max]

*Kampagnen, die nur auf das Suchnetzwerk abzielen*

**[!UICONTROL AI Max]:** Ob [[!UICONTROL AI Max]](https://support.google.com/google-ads/answer/15910366) - KI-gesteuerter Suchbegriffabgleich, Textanpassung und endgültige URL-Erweiterung - für die Kampagne aktiviert werden soll. Nach der Aktivierung von **[!UICONTROL AI Max]** stehen zwei zusätzliche Einstellungen zur Verfügung:

* **[!UICONTROL Text customization]:** Ob [!DNL Google Ads] die Verwendung generativer KI zulassen sollen, um Anzeigenkopien, Überschriften und Beschreibungen basierend auf den vorhandenen Anzeigen und der Landingpage-Kopie anzupassen.

* **[!UICONTROL Final URL expansion]:** Gibt an, ob [!DNL Google Ads] Traffic basierend auf seiner Suchabsicht an die relevanteste Landingpage auf Ihrer Website weiterleiten soll. Diese Einstellung ist nur verfügbar, wenn **[!UICONTROL Text customization]** aktiviert ist.

<!-- Clarify why this is "Unspecified" and read-only for me as of 7/23. Also, shouldn't we reword this? -->

**[!UICONTROL Bundling required]:** (Bestehende Kampagnen, für die die [!UICONTROL AI Max]-Funktion aktiviert ist; schreibgeschützt) Ob [!UICONTROL AI Max] aktiviert sein müssen, um die Textanpassung und die Steuerung der Markenliste für die Kampagne zu berücksichtigen oder zu ändern: *[!UICONTROL Required]*, *[!UICONTROL Not required]* oder *[!UICONTROL Unspecified]*.

<!-- Is this based on the advanced location options set elsewhere in Google Ads editor? -->

**[!UICONTROL Geo Targeting Type]:** (Bestehende Kampagnen, bei denen die [!UICONTROL AI Max]-Funktion aktiviert ist; schreibgeschützt) Wenn eine der Anzeigengruppen der Kampagne [!UICONTROL Locations of Interest] Zielgruppen enthält, werden die Typen der Benutzerinteressen angegeben, die angesprochen werden: *[!UICONTROL Search Interest]* (Benutzer, die an einem bestimmten Ort interessiert sind), *[!UICONTROL Presence]* (Benutzer, die an einem bestimmten Ort sind oder sich regelmäßig an einem bestimmten Ort befinden) oder *[!UICONTROL Presence or Interest]* (Benutzer, die an einem bestimmten Ort sind, regelmäßig daran teilnehmen oder daran interessiert sind).

## Registerkarte [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

### [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (Nur für [!UICONTROL EF Redirect]) Die Ebene, auf der Klicks und Umsatz verfolgt werden sollen, indem eine Umleitung hinzugefügt wird (falls relevant) und Parameter an die entsprechenden URLs angehängt werden:

* *[!UICONTROL Keyword]:* Zum Nachverfolgen von Daten nur auf Keyword-Ebene.

* *[!UICONTROL Creative]:* Zum Nachverfolgen von Daten nur auf Anzeigenebene (kreativ).

* *[!UICONTROL Creative and Keyword]:* Verfolgen Sie Daten sowohl auf Anzeigenebene (kreativ) als auch auf Schlüsselwortebene.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** Fügt den Anzeigen im Konto oder in der Kampagne einen URL-Parameter für das Konversions-Tracking hinzu.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

**[!UICONTROL Track Product Group]:** (nur für [!UICONTROL EF Redirect]) Nicht implementiert

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

### [!UICONTROL Asset Groups] (pro Asset-Gruppe)

*Nur Performance Max-Kampagnen*

**[!UICONTROL Asset Group Name]:** Der Name der Asset-Gruppe. Links zu [!DNL Google Merchant Center] Produkt-Feeds werden nicht unterstützt.

**[!UICONTROL Asset Group Status]:** Der Status der Asset-Gruppe: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Die endgültige URL für alle Anzeigen, die aus der Asset-Gruppe erstellt wurden. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and [!DNL Google Ads] replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Bis zu 15 Bilder für die Anzeige, darunter mindestens ein Querformat (1,91:1, mindestens 600 x 314 Pixel) und mindestens ein Quadrat (1:1, mindestens 300 x 300 Pixel). Optional können Sie ein Hochformat (4:5, mindestens 480 x 600 Pixel) einbeziehen. Siehe [[!DNL Google Ads] Bildspezifikationen](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Sie können entweder Bilder hochladen oder aus Ihren [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

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

**[!UICONTROL Logos]:** Mindestens ein quadratisches (1:1, mindestens 128 x 128 Pixel) Logo. Optional können Sie ein Querformat (4:1, mindestens 512 x 218 Pixel) einfügen. Sie können insgesamt bis zu fünf Logos hinzufügen. Siehe &quot;[[!DNL Google Ads] &quot; &#x200B;](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Sie können entweder Bilder hochladen oder aus Ihren [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

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

**[!UICONTROL Videos]:** (Optional) Mindestens ein und bis zu fünf [!DNL YouTube] Videos, die mindestens 10 Sekunden lang sind. Sie können URLs entweder eingeben oder aus Ihrer [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* URLs eingeben:

  1. Geben Sie auf der Registerkarte [!UICONTROL Enter Video Url] eine URL ein.

  1. (Optional) Um eine weitere URL hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die URL ein.

* Um Videos aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Videos aus.

**[!UICONTROL Headlines]:** Mindestens drei und bis zu fünf kurze Überschriften mit jeweils maximal 30 Zeichen. Mindestens eine Überschrift muss mindestens 15 Zeichen lang sein. Wenn die Option auf Kampagnenebene zur Aktivierung der endgültigen URL-Erweiterung in [!DNL Google Ads] festgelegt ist, ersetzt [!DNL Google Ads] diesen Wert durch eine benutzerdefinierte Überschrift, die auf dem Inhalt der Landingpage basiert.

Sie können entweder Text eingeben oder Assets aus Ihrer [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* So geben Sie Text ein:

  1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

  1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Long Headlines]:** Mindestens eine und bis zu fünf lange Überschriften mit jeweils maximal 90 Zeichen. Sie können entweder Text eingeben oder Assets aus Ihrer [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* So geben Sie Text ein:

  1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

  1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Descriptions]:** Mindestens zwei und bis zu vier Beschreibungen mit jeweils maximal 90 Zeichen. Mindestens eine Beschreibung muss mindestens 30 Zeichen lang sein. Sie können entweder Text eingeben oder Assets aus Ihrer [!UICONTROL Asset Library] auswählen - aber nicht beide im selben Vorgang.

* So geben Sie Text ein:

  1. Geben Sie auf der Registerkarte [!UICONTROL Enter Text] den Text ein.

  1. (Optional) Um eine weitere Textzeichenfolge hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]** und geben Sie die Zeichenfolge ein.

* Um Assets aus Ihrer [!UICONTROL Asset Library] auszuwählen, klicken Sie auf **[!UICONTROL Asset Library]** und wählen Sie die Assets aus.

**[!UICONTROL Call to Action]:** Die call to action, die in die Anzeige aufgenommen werden soll. Standardmäßig ist *[!UICONTROL Automated]* ausgewählt, und [!DNL Google Ads] wählt die call to action aus. Sie können optional eine andere Aktion auswählen.

**[!UICONTROL Business Name]:** Der Unternehmensname mit maximal 25 Zeichen.

**[!UICONTROL Audience Signal]:** (Optional) [!DNL Google Ads] Zielgruppen, die als Zielgruppensignale für die Kampagne verwendet werden sollen. [!DNL Google Ads] Modelle für maschinelles Lernen verwenden die Zielgruppen, um ähnliche Websurfer zu finden, die als Ziel ausgewählt wurden, und können auch Anzeigen für Zielgruppen anzeigen, die nicht als Signale angegeben wurden, um Sie beim Erreichen Ihrer Leistungsziele zu unterstützen. Wählen Sie die Zielgruppen aus, die am ehesten konvertiert werden sollen.

>[!NOTE]
>
>Zielgruppensignale unterscheiden sich von Zielgruppenzielen [auf Kampagnenebene und Anzeigengruppenebene](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Primary Status]:** (schreibgeschütztes Feld für vorhandene Asset-Gruppen in Kampagnen zur Leistungsmaximierung) Warum die Asset-Gruppe die volle Kapazität aufweist oder nicht. Sie berücksichtigt den Asset-Gruppenstatus sowie andere Signale wie Richtlinien- und Qualitätsgenehmigungen. Werte können Folgendes umfassen *ELIGIBLE,* *LIMITED,* *NOT_ELIGIBLE,* *PAUSED,* **&#x200B; PENDING,** REMOVED,*UNKNOWN,* oder *UNSPECIFIED.*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]:** (schreibgeschütztes Feld für vorhandene Asset-Gruppen in -Kampagnen mit dem Wert „Performance Max„) Zusätzliche Details zum primären Status der Asset-Gruppe. Zu den Werten gehören *ASSET_GROUP_DISAPPROVED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,*** ASSET_GROUP_UNDER_REVIEW,*CAMPAIGN_ENDED,**&#x200B;CAMPAIGN_PAUSED,* CAMPAIGN_PENDING,*CAMPAIGN_REMOVED,* UNKNOWN,**&#x200B; *oder**&#x200B;UNSPECIFIED.*

### [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Ob *[!UICONTROL Use account conversion goals for this campaign]* (Standard) oder *[!UICONTROL Use campaign specific conversion goals]* werden soll. Wenn Sie Konversionsziele für die Kampagne angeben möchten, wählen Sie Standardziele aus und/oder erstellen Sie ein benutzerdefiniertes Ziel für die Kampagne.

Ziele werden täglich synchronisiert, sodass vorhandene Ziele, die in den letzten 24 Stunden erstellt wurden, möglicherweise nicht aufgeführt werden. Um die Liste zu aktualisieren, [manuell die Daten des Werbenetzwerks synchronisieren](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Um ein benutzerdefiniertes Konversionsziel zu erstellen, klicken Sie auf **[!UICONTROL + Add custom goal]**, geben Sie den benutzerdefinierten Zielnamen ein, wählen Sie die [Konversionsaktionen](https://support.google.com/google-ads/answer/6032150) aus, die in das benutzerdefinierte Ziel aufgenommen werden sollen, und klicken Sie dann auf **[!UICONTROL Save]**. **Hinweis:** Jede Kampagne kann nur ein benutzerdefiniertes Ziel haben.

>[!TIP]
>
>Wenn die Kampagne Teil eines hybriden Portfolios ist, empfiehlt es sich, Ziele auf Kampagnenebene zu verwenden, die den Konversionszielen im Portfolioziel entsprechen. Das Einschließen zusätzlicher Konversionsziele kann die Portfolioleistung beeinträchtigen.
>
>Für Kampagnen in hybriden Portfolios, für die Sie [Ziele in das Anzeigennetzwerk hochladen](/help/search-social-commerce/tools/objective-upload-to-networks.md), gehen Sie jedoch wie folgt innerhalb des Editors des Anzeigennetzwerks anstelle von hier vor: a) fügen Sie die hochgeladene Zielmetrik für das Such-, Social- und Commerce-Portfolio (die mit „O_ACS_OBJ“ beginnt) als Konversionsaktion für die Kampagne hinzu und b) fügen Sie alle Kampagnenziele hinzu, die [!DNL Google] verfolgte Konversionen enthalten, da im Anzeigennetzwerk verfolgte Metriken nicht mit dem Ziel in das Anzeigennetzwerk hochgeladen werden.

### [!UICONTROL Set Customer Acquisition Goal]

Optimieren Sie Ihre Kampagne für neue Kunden, Bestandskunden oder beides. Um diese Einstellung verwenden zu können, müssen Sie zunächst das Ziel der Kundenakquise für das [!DNL Google Ads]-Konto oder ggf. das Manager-Konto aktivieren. Das Ziel definiert die Listen der zulässigen Bestandskunden und den zusätzlichen Konversionswert für neue Kunden in den Konvertierungseinstellungen. Siehe Schritte 1-2 in der [!DNL Google Ads]-Hilfe [Aktivieren des Ziels für die Kundenakquise](https://support.google.com/google-ads/answer/14007601).

**[!UICONTROL Customer Goal]:** Der Zieltyp für die Kundenakquise:

* *[!UICONTROL All Customers]* (Standard): Für neue und bestehende Kundinnen und Kunden gleichermaßen optimieren.

* *[!UICONTROL New Customers]:* Akquise neuer Kunden priorisieren. Durch Auswahl dieser Option wird die **[!UICONTROL New Customer Bid Adjustment]** angezeigt.

* *[!UICONTROL Existing Customers]:* Priorisieren Sie die Kundenbindung.

**[!UICONTROL New Customer Bid Adjustment]:** (**[!UICONTROL Customer Goal]** nur auf **[!UICONTROL New Customers]** festgelegt) Ein Multiplikator, der auf Angebote von 0,1 bis 10,0 angewendet wird, wenn neue Kunden angesprochen werden. Der Standardwert ist 1.0 (keine Anpassung). So erhöht beispielsweise 1,5 die Gebote für neue Kunden um 50 %, 2,0-fach die Gebote für neue Kunden um das Doppelte und 0,5-fach die Gebote für neue Kunden um 50 %.

>[!MORELIKETHIS]
>
>* [Kampagnen verwalten](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
