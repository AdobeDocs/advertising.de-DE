---
title: Einstellungen für Textanzeigen und responsive Suchanzeigen-Vorlagen für Inventar-Feeds
description: Verweisen Sie auf die Einstellungen für Textanzeigen und Vorlagen für responsive Suchanzeigen für Inventar-Feeds.
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '3360'
ht-degree: 0%

---

# Einstellungen für Textanzeigen und responsive Suchanzeigen-Vorlagen für Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

>[!NOTE]
>
>* Die folgenden Zeichen sind für die Bezeichnung von Spaltennamen und Modifikatornamen in der Vorlage reserviert und dürfen daher nicht als Text in allen Attributfeldern verwendet werden: `[ ] < > `
>* In [!DNL Yandex templates] können Sie die dynamischen Parameter `{param1}` und `{param2}` nur in URLs verwenden und keine dynamische Preiseinfügung in Anzeigenbeschreibungen verwenden.

## \[Vor allen Registerkarten\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Linker Bereich\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (Optional) Ordnet alle neuen Anzeigengruppen (nicht verfügbar für [!DNL Yandex]), Keywords und Anzeigen vorhandenen Kampagnen zu, anstatt Kampagnen zu erstellen. Wenn Sie diese Option aktivieren, wählen Sie die Zuordnungsmethode aus.

Die Verwendung von [!UICONTROL Map Only] auf Kampagnenebene erfordert eine vorhandene Kontostruktur, die eng mit der Produkttaxonomie verknüpft ist und einfach dem Daten-Feed zugeordnet werden kann.

**[!UICONTROL Map Method]:** (wenn [!UICONTROL Map Only] für die Kampagne aktiviert ist) Die Methode, mit der neue Anzeigengruppen (für [!DNL Yandex] nicht verfügbar), Schlüsselwörter und Anzeigen vorhandenen Kampagnen zugeordnet werden:

* *[!UICONTROL Contains Anywhere]:* Fügt Daten zu einer vorhandenen Kampagne hinzu, deren Name die angegebene Zeichenfolge enthält, sofern vorhanden.

* *[!UICONTROL Contains Exactly]:* Fügt Daten zu einer vorhandenen Kampagne hinzu, deren Name die angegebene Zeichenfolge enthält, sofern vorhanden.

* *[!UICONTROL Exactly Matches]* (Standard): Fügt Daten zu einer vorhandenen Kampagne mit demselben Namen hinzu, sofern vorhanden.

Wenn keine Übereinstimmung gefunden wird, werden alle Daten für die Kampagne ignoriert. Wenn mehrere Kampagnenübereinstimmungen gefunden werden, werden die Schlüsselwörter und Anzeigen allen zugeordnet.

**[!UICONTROL Campaign Tracking Template]:** (Nur Konten mit endgültigen/erweiterten URLs; optional) Die Tracking-Vorlage auf Kampagnenebene, die alle Umleitungs- und Tracking-Parameter für ausgelagerte Domains angibt und die endgültige URL in einen Parameter einbettet. Dieser Wert überschreibt die Einstellung auf Kontoebene, aber Tracking-Vorlagen auf detaillierteren Ebenen (mit Keyword als am detailliertesten) überschreiben diesen Wert.

* Bei Adobe Advertising-Konversionsverfolgung, die angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, fügt Search, Social und Commerce beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

* Einbetten der endgültigen URL:

   * (Nur [!DNL Google Ads] und [!DNL Microsoft Advertising]) Eine Liste der Parameter zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in den Parametern (nur [!DNL Microsoft Advertising]) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799/2) oder (nur [!DNL Google Ads]) den Parametern „Tracking-Vorlage nur“ im Abschnitt „Verfügbare [!DNL ValueTrack]&quot; in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

   * (Nur [!DNL Yahoo! Japan Ads]) Verwenden Sie den Parameter `!{unescapedurl}` , um die Landingpage-URL anzugeben.

   * Sie können optional URL-Parameter und beliebige benutzerdefinierte Parameter einbeziehen, die für die Kampagne definiert wurden und durch kaufmännische Und-Zeichen (&amp;) getrennt sind, z. B. `{lpurl}?matchtype={matchtype}&device={device}`.

* Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** (In [!DNL Google Ads]- und [!DNL Yandex]-Kampagneneinstellungen) Die Netzwerke, in denen Anzeigen geschaltet werden sollen:

* *[!UICONTROL Search]:* Gebote für gesponserte Suchlisten abgeben.

  ([!DNL Google Ads]-Kampagnen) Um Angebote für [!DNL Google Ads] Suchpartner in Listen aufzunehmen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* Platzieren von Geboten für Platzierungen in Inhalts- (Anzeige-) Netzwerklisten. **Hinweis:** Platzierungen können nicht mit der Vorlage erstellt werden. Wenn Sie diese Option wählen, erstellen Sie Platzierungen für jede Anzeigengruppe und geben Sie an, welche Seiten im Anzeigennetzwerk für jede Anzeigengruppe mithilfe <!-- insert link --> Bulksheets oder der <!-- insert links --> Anzeigengruppen- und Platzierungseinstellungen in [!UICONTROL Search] > [!UICONTROL Campaigns] ausgewählt werden sollen.

**[!UICONTROL Languages]:** (nur [!DNL Google Ads] Such- und Anzeigennetzwerke) Eine oder mehrere Zielsprachen für Anzeigen in der Kampagne.

[!DNL Google Ads] bestimmt die Sprache eines Benutzers anhand der [!DNL Google] Spracheinstellung des Benutzers oder der Sprache der Suchanfrage, der aktuellen Seite oder der kürzlich angezeigten Seiten im [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]:**(Nur [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Kampagnen; anwendbar auf Kampagnen, die sich an Zielgruppen in der Europäischen Union (EU) richten Unabhängig davon, ob die Kampagne politische Werbung gemäß den Anforderungen für in der Europäischen Union gemäß der EU-Verordnung 2024/90 geschaltete Anzeigen enthält: *[!UICONTROL Yes]* oder *[!UICONTROL No]*.

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Nur Konten mit endgültigen/erweiterten URLs) Die Tracking-Vorlage auf Anzeigengruppen-Ebene, die alle off-landing-domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet.

Bei Adobe Advertising-Konversionsverfolgung, die angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, fügt Search, Social und Commerce beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein. So geben Sie die Landingpage-URL an:

* Für Yahoo! Japan Ads-Konten, verwenden Sie den Parameter {lpurl}.

* Informationen zu den für Microsoft Advertising- und Google Ads-Konten verfügbaren Parametern finden Sie unter [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder den Parametern „Nur Tracking-Vorlage“ im Abschnitt „Verfügbare [!DNL ValueTrack]&quot; in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

Dieser Wert überschreibt die Einstellungen auf Konto- und Kampagnenebene, aber Tracking-Vorlagen auf detaillierteren Ebenen (mit Keyword als am detailliertesten) überschreiben diesen Wert.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Schlüsselwörter für die angegebene Anzeigengruppe (oder Kampagne für [!DNL Yandex]), die aus einer beliebigen Kombination von statischem Text, Spalten in der angegebenen Datei und Modifikatoren bestehen kann. Spaltennamen und Modifikatoren werden durch tatsächliche Daten ersetzt, wenn die angegebene Feed-Datei durch die Vorlage übertragen wird.

Um einen Spaltennamen oder eine Modifikatorgruppe als dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld, und klicken Sie dann auf einen Spaltennamen in der Spaltenliste oder auf einen [Modifikatornamen](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in der Modifikatorliste. Um mehrere Keywords oder mehrere Übereinstimmungstypen für dasselbe Keyword anzugeben, geben Sie sie in separaten Zeilen ein. Um den Übereinstimmungstyp des Keywords anzugeben, verwenden Sie die folgende Syntax für den Übereinstimmungstyp um den Spaltennamen:

* Für [!DNL Google Ads]-, [!DNL Microsoft Advertising]- und [!DNL Yahoo! Japan Ads]:

   * Für dynamische Parameter: Breite Übereinstimmung = `[keyword]`, Breite Übereinstimmung Modifikator für den ersten Begriff in der [!UICONTROL Keyword] Spalte (z. B. +blaue Wildlederschuhe) = `+[keyword]`, Breite Übereinstimmung Modifikator für jeden Begriff in der Schlüsselwortspalte (z. B. +blau +Wildleder +Schuhe) = `+[keyword]+`, Phrase Übereinstimmung = `"[keyword]"`, genaue Übereinstimmung = `[[keyword]]`

   * Für statische Schlüsselwörter: Grobe Übereinstimmung = `keyword`, Grobe Übereinstimmung Modifikator = `+keyword` oder Phrase Übereinstimmung = `"keyword"`

     Sie können hier keine statischen Keywords mit exakter Übereinstimmung und standardmäßiger Übereinstimmungssyntax eingeben, da sie wie dynamische Parameter von Klammern (`[]`) umgeben sind.

* Für [!DNL Yandex] Vorlagen:

   * Für dynamische Parameter: Fügen Sie den Spaltennamen ein, z. B. `[keyword]`. Um den Übereinstimmungstyp anzugeben, verwenden Sie die [[!DNL Yandex] Syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Hinweis:** Verwenden Sie für allgemeine Übereinstimmungsbegriffe die folgende Syntax: Broad Match Modifier für den ersten Begriff in der Keyword-Spalte (z. B. +blaue Wildlederschuhe) = `+[keyword]`, Broad Match Modifier für jeden Begriff in der Keyword-Spalte (z. B. +blau +Wildleder +Schuhe) = `+[keyword]+`

   * Für statische Keywords werden nur Suchbegriffe unterstützt. Verwenden Sie die [[!DNL Yandex] Syntax für ](https://yandex.com/support/direct/keywords/symbols-and-operators.html) Schlüsselwort . Klammern (`[]`), um anzugeben, dass die Wortreihenfolge nicht unterstützt wird.

>[!NOTE]
>
>* Sie können mehrere Modifikatorwerte manuell in das Keywords-Feld einschließen, indem Sie kommagetrennte Werte entweder vor oder nach einem Keyword-Parameter in Klammern einschließen (aber nicht an beiden Stellen). Beispielsweise produziert `(cheap, discount, affordable)[product]` drei separate Anzeigen für jedes Produkt.
>* Wenn Sie keinen Übereinstimmungstyp angeben, wird der standardmäßige Übereinstimmungstyp „Broad“ verwendet.
>* Negative Übereinstimmungen werden nicht unterstützt.
>* Google-Modifikatoren für breite Übereinstimmungen weisen jetzt für einige Sprachen dasselbe Übereinstimmungsverhalten wie Phrasenübereinstimmung auf, und Sie können keine neuen Keywords für breite Übereinstimmungen erstellen. Weitere Informationen finden [[!DNL Google Ads]  in der ](https://support.google.com/google-ads/answer/10286719).

**[!UICONTROL Map Only]:** Fügt alle neuen Anzeigen zu Anzeigengruppen (oder zu Kampagnen für [!DNL Yandex] Konten) hinzu, in denen die angegebenen Schlüsselwörter gefunden werden, anstatt neue Schlüsselwörter zu erstellen. Um diese Option zu aktivieren, aktivieren Sie das Kontrollkästchen. Wenn diese Option aktiviert ist, werden alle Parameter 1 und Parameter 2 Variablen in den angegebenen Keywords nicht angewendet, da die Keywords vorhanden sind.

**[!UICONTROL Keyword Final URL]:** (Konten mit endgültigen/erweiterten URLs; optional) Die Landingpage-URL, zu der Anzeigennetzwerkbenutzer geleitet werden, wenn sie auf Ihre Anzeige klicken. Sie muss dieselbe Domain wie die Anzeige-URL enthalten und alle Parameter in der endgültigen URL müssen mit den Parametern in der Landingpage-URL nach dem Anzeigenklick übereinstimmen. Es kann Weiterleitungen innerhalb der Landingpage-Domain oder Subdomain enthalten, jedoch keine Weiterleitungen außerhalb der Landingpage-Domain.

Wenn Sie einen [!DNL Google Merchant Center] Feed verwenden und diesen Wert in die Spalte &quot;[!DNL Link]&quot; aufnehmen, fügen Sie diese Spalte in dieses Feld ein.

>[!NOTE]
>
>* Wenn Sie Tracking-URLs generieren, während Sie über die Vorlage verteilte Daten posten, werden Tracking-Parameter basierend auf den Tracking-Einstellungen des Kontos an diesen Wert angehängt.
>* ([!DNL Google Ads] Konten) Verwenden Sie keine Makros, die nicht durch Klicks aus Quellen ersetzt werden, die paralleles Tracking ermöglichen. Wenn der Werbetreibende Makros verwenden muss, sollte das Adobe-Account-Team den Kunden-Support oder das Implementierungsteam kontaktieren, um diese hinzuzufügen.

**[!UICONTROL Keyword Tracking Template]:** (Konten mit endgültigen/erweiterten URLs; optional) Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als der detailliertesten) überschreibt Werte auf allen anderen Ebenen.

* Bei Adobe Advertising-Konversionsverfolgung, die angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, fügt Search, Social und Commerce beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

* Sie können optional Umleitungen und Tracking von Drittanbietern eingeben.

* So geben Sie die Landingpage-URL an:

   * (Nur [!DNL Google Ads] und [!DNL Microsoft Advertising]) Eine Liste der Parameter zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in den Parametern (nur [!DNL Microsoft Advertising]) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder (nur [!DNL Google Ads]) den Parametern „Tracking-Vorlage nur“ im Abschnitt „Verfügbare [!DNL ValueTrack]&quot; in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

   * (Nur [!DNL Yahoo! Japan Ads]) Verwenden Sie den Parameter `!{lpurl}` , um die Landingpage-URL anzugeben.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] templates\]:** (nur [!DNL Google Ads] templates) Die Spalte in der angegebenen Datei, die die [!DNL Google Ads] `{param1}` oder `{param2}` Variable darstellt, die Sie in die Anzeigenkopie oder die Anzeige-URL einer aus der Vorlage erstellten Anzeige einbeziehen können. Um den dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und klicken Sie dann auf einen Spaltennamen in der Spaltenliste. Der Spaltenname wird durch die tatsächlichen Daten ersetzt, wenn die Feed-Datei durch die Vorlage übertragen wird.

Wenn Sie einen der Parameter verwenden, haben Sie die Möglichkeit, den Parameter nur auf neue Keywords anzuwenden oder auch die Werte vorhandener Keywords zu aktualisieren, die nicht aus der Vorlage erstellt wurden:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (Standard): Hiermit wird einfach der Wert des Parameters für neue Keywords eingefügt, die mithilfe der Vorlage erstellt werden.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Zusätzlich zur Erstellung neuer Keywords aus dem Feed aktualisiert Search, Social und Commerce auch den Wert des Parameters für alle vorhandenen Keywords in der Anzeigengruppe, die nicht mithilfe der Vorlage erstellt wurden. Geben Sie einen einzelnen numerischen Wert ein, der für alle diese Keywords verwendet wird. Die Vorlage muss mindestens ein Keyword enthalten.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Zusätzlich zur Erstellung neuer Keywords aus dem Feed aktualisiert Search, Social und Commerce auch den Wert des Parameters für alle vorhandenen Keywords in der Anzeigengruppe, die nicht mithilfe der Vorlage erstellt wurden, solange die Feed-Datei numerische Werte für den Parameter enthält, mit bis zu einem Dezimalpunkt, aber ohne Kommas, Währungssymbole oder Codes oder andere Zeichen. Der Mindestwert für den Parameter in der Feed-Datei wird für alle vorhandenen Keywords verwendet. Wenn die Feed-Datei beispielsweise [!UICONTROL Param1] Werte 21500 und 22000 hat, werden die [!UICONTROL Param1] Werte für die vorhandenen Keywords in 21500 geändert. Die Vorlage muss mindestens ein Keyword enthalten. **Tipp:** Verwenden Sie diese Option nur, wenn Sie über streng designbezogene Anzeigengruppen verfügen, sodass es sinnvoll ist, wenn Schlüsselwörter denselben Wert aufweisen.

Die Datenfelder in der Feed-Datei dürfen maximal 25 Zeichen lang sein und nur aus numerischen Daten mit den folgenden nicht numerischen Zeichen bestehen:

* (Bei Verwendung des Parameters &quot;[!UICONTROL Apply to Existing Keywords: Min]„) Nur bis zu einem Dezimalpunkt.

* (Wenn Sie den Parameter &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; nicht verwenden):

   * Dem Wert kann ein Währungssymbol oder ein Währungscode vorangestellt oder angehängt werden. Beispielsweise sind 2.000,00 £ und 2.000 GBP gültig.

   * Der Wert kann ein Komma (,) oder einen Punkt (.) als Trennzeichen enthalten, mit einem optionalen Punkt (.) oder einem Komma (,) für Teilwerte. Beispielsweise sind 1.000.00 und 2.000.10 gültig.

   * Dem Wert kann ein Prozentzeichen (%), ein Pluszeichen (+) oder ein Minuszeichen (-) vorangestellt oder angehängt werden. Beispielsweise sind 20 %, 208+ und -42,32 gültig.

   * Zwei Zahlen können mit einem Schrägstrich eingebettet werden. Beispielsweise sind 4/1 und 0,95/0,45 gültig.

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising] Vorlagen\]:** (nur [!DNL Microsoft Advertising] Vorlagen) Die Zeichenfolge, die als Ersatzwert in einer Anzeige verwendet werden soll, wenn der Titel, der Text, die Anzeige-URL oder die endgültige URL die `{Param2}` dynamische Ersatzzeichenfolge enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Werbeelemente, in denen Sie sie verwenden (ein Anzeigentitel kann beispielsweise bis zu 25 Zeichen enthalten).

**[!UICONTROL Param 3]:** (nur [!DNL Microsoft Advertising]) Die Zeichenfolge, die als Ersatzwert in einer Anzeige verwendet werden soll, wenn Titel, Text, Anzeige-URL oder endgültige URL die `{Param3}` dynamische Ersatzzeichenfolge enthalten. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Werbeelemente, in denen Sie sie verwenden (ein Anzeigentitel kann beispielsweise bis zu 25 Zeichen enthalten).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** Das Anfangsgebot für jedes Keyword mit dem angegebenen Übereinstimmungstyp oder Anzeigetyp.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** (nur [!DNL Google Ads] und [!DNL Microsoft Advertising] Kampagnen) Der Typ der Anzeigen: *[!UICONTROL Expanded Search Ads]* oder *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Optional) Befüllt alle alternativen Anzeigenkopie-Felder vorab mit Text aus den ursprünglichen Anzeigenkopie-Feldern.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (nur responsive Suchanzeigen) Die Anzeigenposition, an der der Titel/die Überschrift eingefügt werden muss (z. B. &quot;[!UICONTROL Pinned at position 1]„). Der Standardwert lautet [!UICONTROL Unpinned].

Für jede Position muss mindestens ein Titel verfügbar sein. Wenn Sie mehrere Titel an derselben Position anheften, enthält die endgültige Anzeige immer einen dieser Titel an der angegebenen Position. Titel, die an Position 3 angeheftet sind, werden in der Anzeige möglicherweise nicht angezeigt.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (nur responsive Suchanzeigen) Die Anzeigentitel (Überschriften). Jede Anzeigenvariante muss mindestens drei und bis zu 15 Anzeigentitel enthalten. Das Anzeigennetzwerk zeigt Anzeigen mit bis zu drei Überschriften an. Die maximale Länge für jeden Titel beträgt 30 Zeichen, einschließlich dynamischer Texte (wie die Werte von Keywords und Anzeigenanpassungen).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Vorhandene standardmäßige Microsoft Advertising-Textanzeigen; schreibgeschützt) Der Titel oder die erste Zeile einer Anzeige. Microsoft Advertising hat die Erstellung und Bearbeitung von standardmäßigen Textanzeigen verworfen.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** (Nur [!DNL Google Ads] und [!DNL Yahoo! Japan Ads] erweiterte/erweiterte Text-Anzeigenvorlagen) Die Überschrift einer Anzeige. Die maximale Länge für jede Zeile (nachdem dynamische Parameter ersetzt wurden) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** (nur [!DNL Google Ads] erweiterte Text-Anzeigenvorlagen; optional) Eine dritte Überschrift für eine Anzeige. Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

**[!UICONTROL Title]:** (nur [!DNL Yandex]) Der Titel oder die erste Zeile einer Anzeige. Der Maximalwert beträgt 33 Zeichen.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (nur erweiterte Textanzeigen von Microsoft Advertising) Die Überschrift einer Anzeige. Die maximale Länge für jede Zeile (nachdem dynamische Parameter ersetzt wurden) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (nur Microsoft Advertising-erweiterte Textanzeigen) Der Hauptteil einer Anzeige. Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 80 Zeichen oder 40 Doppelbyte-Zeichen (z. B. Chinesisch, Japanisch und Koreanisch).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** Der Hauptteil der Anzeige.

* (Erweiterte Text-Anzeigenvorlagen von Google Ads) Die maximale Länge (nach dem Ersetzen dynamischer Parameter) beträgt 90 Zeichen oder 45 Doppelbyte-Zeichen.

* (Yahoo! Japan Ads-Vorlagen) Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 80 Zeichen oder 40 Doppelbyte-Zeichen.

* (Yandex-Vorlagen) Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 75 Zeichen, und ein einzelnes Wort darf nicht mehr als 22 Zeichen lang sein.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Nur responsive Suchanzeigen) Die Anzeigenposition, an der die Beschreibung enthalten sein muss (z. B. &quot;[!UICONTROL Pinned at position 1]„). Der Standardwert lautet [!UICONTROL Unpinned]. Für jede Position muss mindestens eine Beschreibung verfügbar sein.

Wenn Sie mehrere Beschreibungen an derselben Position anheften, enthält die endgültige Anzeige immer eine dieser Beschreibungen an der angegebenen Position. An Position 2 angeheftete Beschreibungen werden in der Anzeige möglicherweise nicht angezeigt.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (nur responsive Suchanzeigen) Die Anzeigenbeschreibungen. Jede Anzeigenvariante muss mindestens zwei und bis zu vier Anzeigenbeschreibungen enthalten. Das Anzeigennetzwerk zeigt Anzeigen mit bis zu zwei Beschreibungen an. Geben Sie mindestens zwei ein. Die maximale Länge für jede Beschreibung beträgt 90 Zeichen, einschließlich dynamischer Texte (z. B. Werte von Schlüsselwörtern und Anzeigenanpassungen).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Nur erweiterte Text-Anzeigenvorlagen in Google; optional) Eine zweite Zeile der Anzeige. Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 90 Zeichen oder 45 Doppelbyte-Zeichen.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Nur erweiterte Text- und responsive Suchanzeigen; optional) Ein oder zwei URL-Pfade, die nach der Basis-URL nacheinander eingeschlossen werden. Sie sollten das Produkt oder die Dienstleistung in der Anzeige detaillierter beschreiben. Wenn Sie beispielsweise der Basis-URL www.example.com die [!UICONTROL Display Path 1] „Schuhe“ und [!UICONTROL Display Path 2] „Outdoor“ hinzufügen, lautet die URL www.example.com/Shoes/Outdoor. Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) für jedes Feld beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.

Fügen Sie für responsive Suchanzeigen eine Anzeigenanpassung mit den folgenden Formaten ein. Dabei ist `Default text` ein optionaler Wert, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Nur vorhandene [!DNL Microsoft Advertising] und [!DNL Yahoo! Japan Ads] Standardtextanzeigen; schreibgeschützt) Die in einer Anzeige angezeigte URL.

[!DNL Microsoft Advertising] und [!DNL Yahoo! Japan Ads] haben die Erstellung und Bearbeitung von Standard-Textanzeigen eingestellt.

**[!UICONTROL Base URL]:** (Nur Konten mit Ziel-URLs) Die Seite, zu der Benutzer weitergeleitet werden. Es kann Umleitungs- und Trackingcode von Drittanbietern enthalten. Wenn Sie den Konversionsverfolgungs-Service von Adobe Advertising verwenden und die Kampagneneinstellungen die Verwendung des [!UICONTROL EF Redirect] und das Hinzufügen des Trackings auf Anzeigenebene beinhalten, fügt Search, Social und Commerce der Anzeige automatisch einen eigenen Umleitungs- und Trackingcode hinzu.

Um einen Spaltennamen oder eine Modifikatorgruppe als dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und klicken Sie dann auf einen Spaltennamen in der Spaltenliste oder auf einen [Modifikatornamen](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in der [!UICONTROL Modifiers].

**[!UICONTROL Final URL]:** (Konten mit endgültigen/erweiterten URLs) Die Landingpage-URL, zu der Benutzer geleitet werden, wenn sie auf Ihre Anzeige klicken. Sie muss dieselbe Domain wie die Anzeige-URL enthalten und alle Parameter in der endgültigen URL müssen mit den Parametern in der Landingpage-URL nach dem Anzeigenklick übereinstimmen. Es kann Weiterleitungen innerhalb der Landingpage-Domain oder Subdomain enthalten, jedoch keine Weiterleitungen außerhalb der Landingpage-Domain.

Wenn Sie einen [!DNL Google Merchant] Center-Feed verwenden und diesen Wert in die Spalte &quot;[!UICONTROL Link]&quot; aufnehmen, fügen Sie diese Spalte in dieses Feld ein.

>[!NOTE]
>
>* Wenn Sie Tracking-URLs generieren, während Sie über die Vorlage übertragene Daten posten, werden Tracking-Parameter basierend auf den Tracking-Einstellungen des Kontos an diesen Wert angehängt.
>* ([!DNL Google Ads]-Konten ) Verwenden Sie keine Makros, die keine Klicks aus Quellen ersetzen, die paralleles Tracking ermöglichen. Wenn der Werbetreibende Makros verwenden muss, sollte das Adobe-Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um diese hinzuzufügen.

**[!UICONTROL Tracking Template]:** (Konten mit endgültigen/erweiterten URLs; optional) Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als der detailliertesten) überschreibt Werte auf allen anderen Ebenen.

Bei Adobe Advertising-Konversionsverfolgung, die angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, fügt Search, Social und Commerce beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein. So geben Sie die Landingpage-URL an:

* Für Yahoo! Japan Ads-Konten, verwenden Sie den Parameter {lpurl}.

* Informationen zu den für Microsoft Advertising- und Google Ads-Konten verfügbaren Parametern finden Sie unter [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder den Parametern „Nur Tracking-Vorlage“ im Abschnitt „Verfügbare [!DNL ValueTrack]&quot; in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

**\[Alternative Anzeigenfelder unter den ursprünglichen Anzeigenfeldern\]:** (Optional) Ein alternativer Satz von Anzeigenkopien für eine Anzeige, der verwendet werden kann, wenn eine der Zeilen in der ursprünglichen Anzeigenkopie die maximal zulässige Länge überschreitet, sobald dynamische Parameter während der Verbreitung mit Daten gefüllt werden.

>[!NOTE]
>
>* Wenn die Option [!UICONTROL Prefill] ausgewählt ist, werden die alternativen Felder mit den ursprünglichen Feldern vorausgefüllt und Sie können sie nach Bedarf bearbeiten.
>* Nur die Anzeigenkopie-Felder, die die maximale Länge überschreiten, werden durch den alternativen Wert ersetzt. Wenn beispielsweise nur eine ursprüngliche Überschrift oder ein Titel zu lang ist, verwendet die generierte Anzeigenvariante die alternative Überschrift oder den Titel und die ursprünglichen Beschreibungen. Achten Sie daher darauf, dass die alternative Anzeigenkopie in Kombination mit der ursprünglichen Anzeigenkopie sinnvoll ist.
>* Wenn die ursprüngliche Anzeigenkopie die Längenanforderungen der Suchmaschine erfüllt, wird die alternative Anzeigenkopie verworfen.

**\[Komponente\] [!UICONTROL Ad Label Classifications] > \[Kennzeichnungsklassifizierung und -wert\]:** (Optional) Werte für bis zu fünf vorhandene Kennzeichnungsklassifizierungen, die den Anzeigenvarianten zugewiesen werden sollen, die mithilfe der Vorlage erstellt oder bearbeitet werden. Für jede Kampagnenkomponente, der Sie Kennzeichnungsklassifizierungen zuweisen möchten:

1. Aktivieren Sie das Kontrollkästchen.

1. Konfigurieren Sie die Klassifizierungswerte der Kennzeichnung für die Anzeigenvariantenvorlage:

   * Gehen Sie für jede Kennzeichnungsklassifizierung und jeden Wert, der der Komponente zugewiesen werden soll, wie folgt vor:

      1. Klicken Sie auf **[!UICONTROL Add Label Classification]**.

      1. Wählen Sie die vorhandene Kennzeichnungsklassifizierung aus und wählen Sie dann entweder einen vorhandenen Wert aus oder geben Sie einen neuen Wert ein.

         Die maximale Länge für jeden Wert beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

         Um einen Spaltennamen als dynamischen Parameter für einen Beschriftungsklassifizierungswert einzufügen, klicken Sie auf das Eingabefeld (das zweite Feld) und dann auf einen Spaltennamen in der Spaltenliste.

         Pro Kampagnenkomponente kann nur ein Wert enthalten sein. Beispielsweise kann eine Kampagne „Farbe=Rot“, aber nicht „Farbe=Rot“ und „Farbe=Blau“ haben.

         * Um einen vorhandenen Kennzeichnungswert zu ändern, wählen Sie einen neuen Wert aus oder geben Sie ihn ein.

         * Um einen vorhandenen Kennzeichnungswert zu entfernen, klicken Sie auf **[!UICONTROL X]** neben dem Wert.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Über die Automatisierung der Anzeigenverwaltung mithilfe von Inventar-Feeds](../inventory-feeds-about.md)
>* [Verwalten von Modifikatoren](../modifiers-manage.md)
>* [Verwalten von Inventardaten-Feed-Dateien](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Verbreiten von Feed-Daten über Vorlagen](../feed-data-propagate.md)
>* [Kampagnendaten aus Inventar-Feeds in Werbenetzwerke posten](../propagated-data-post.md)
