---
title: Einstellungen für Textanzeigen und responsive Suchanzeigenvorlagen für Inventar-Feeds
description: Referenzieren Sie die Einstellungen für Textanzeigen und Vorlagen für responsive Suchanzeigen für Inventar-Feeds.
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# Einstellungen für Textanzeigen und responsive Suchanzeigenvorlagen für Inventar-Feeds


*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

>[!NOTE]
>
>* Die folgenden Zeichen sind in der Vorlage für die Bezeichnung von Spaltennamen und Modifikatornamen reserviert und sind daher in allen Attributfeldern als Text verboten:  `[ ] < > `
>* In [!DNL Yandex templates], können Sie die dynamischen Parameter verwenden `{param1}` und `{param2}` nur in URLs verwenden, und Sie können die dynamische Preiseinfügung in Anzeigenbeschreibungen nicht verwenden.

## \[Über allen Registerkarten\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[linker Bereich\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (Optional) Ordnet alle neuen Anzeigengruppen zu (nicht verfügbar für [!DNL Yandex]), Suchbegriffen und Anzeigen zu bestehenden Kampagnen, anstatt Kampagnen zu erstellen. Wenn Sie diese Option aktivieren, wählen Sie die Zuordnungsmethode aus.

Verwenden [!UICONTROL Map Only] auf Kampagnenebene erfordert eine vorhandene Kontostruktur, die eng mit der Produkttaxonomie verknüpft ist und einfach dem Daten-Feed zugeordnet werden kann.

**[!UICONTROL Map Method]:** (When [!UICONTROL Map Only] wird für die Kampagne aktiviert) Die Methode, mit der neue Anzeigengruppen (nicht verfügbar für [!DNL Yandex]), Suchbegriffe und Anzeigen vorhandenen Kampagnen zugeordnet werden:

* *[!UICONTROL Contains Anywhere]:* Fügt Daten zu einer vorhandenen Kampagne hinzu, deren Name die angegebene Zeichenfolge enthält, sofern vorhanden.

* *[!UICONTROL Contains Exactly]:* Fügt Daten zu einer vorhandenen Kampagne hinzu, deren Name die angegebene Zeichenfolge enthält, sofern vorhanden.

* *[!UICONTROL Exactly Matches]* (Standardeinstellung): Fügt Daten zu einer bestehenden Kampagne mit demselben Namen hinzu, sofern vorhanden.

Wenn keine Übereinstimmung gefunden wird, werden alle Daten für die Kampagne ignoriert. Wenn mehrere Kampagnenübereinstimmungen gefunden werden, werden ihnen Suchbegriffe und Anzeigen zugeordnet.

**[!UICONTROL Campaign Tracking Template]:** (Nur Konten mit finalen/erweiterten URLs; optional) Die Tracking-Vorlage auf Kampagnenebene, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Dieser Wert überschreibt die Einstellung auf Kontoebene, aber Tracking-Vorlagen auf detaillierteren Ebenen (mit Keyword als granularster) überschreiben diesen Wert.

* Für Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot; Search, Social und Commerce hängt beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

* So betten Sie die endgültige URL ein:

   * ([!DNL Google Ads] und [!DNL Microsoft® Advertising] Nur) Eine Liste von Parametern zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie im Abschnitt ([!DNL Microsoft® Advertising] nur) [[!DNL Microsoft® Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799/2) oder ([!DNL Google Ads] nur) die Parameter &quot;Nur Tracking-Vorlage&quot; im Abschnitt &quot;Verfügbar&quot; [!DNL ValueTrack] Parameter&quot;im [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] nur) Verwenden Sie den Parameter . `!{unescapedurl}` um die Landingpage-URL anzugeben.

   * Sie können optional URL-Parameter und alle für die Kampagne definierten benutzerdefinierten Parameter einbeziehen, getrennt durch kaufmännische Und-Zeichen (&amp;), z. B. `{lpurl}?matchtype={matchtype}&device={device}`.

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

**[!UICONTROL Networks]:** (in [!DNL Google Ads] und [!DNL Yandex] Kampagneneinstellungen) Die Netzwerke, auf denen Anzeigen platziert werden:

* *[!UICONTROL Search]:* Platzieren von Angeboten für gesponserte Suchlisten.

  ([!DNL Google Ads] Kampagnen) So fügen Sie Angebote in Listen für [!DNL Google Ads] Suchpartner, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* So platzieren Sie Angebote für Platzierungen in Netzlisten für Inhalte (Display). **Hinweis:** Sie können Platzierungen nicht mit der Vorlage erstellen. Wenn Sie diese Option auswählen, erstellen Sie Platzierungen für jede Anzeigengruppe und geben Sie an, welche Seiten im Anzeigennetzwerk für jede Anzeigengruppe mit <!-- insert link --> Bulksheets oder <!-- insert links --> Anzeigengruppen- und Platzierungseinstellungen in [!UICONTROL Search] > [!UICONTROL Campaigns] Ansichten.

**[!UICONTROL Languages]:** ([!DNL Google Ads] Nur Such- und Display-Netzwerke) Eine oder mehrere Zielsprachen für Anzeigen in der Kampagne.

[!DNL Google Ads] bestimmt die Sprache eines Benutzers aus dem [!DNL Google] Spracheinstellung oder die Sprache der Suchabfrage, der aktuellen Seite oder der zuletzt angezeigten Seiten auf der [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Nur Konten mit finalen/erweiterten URLs) Die Tracking-Vorlage auf Anzeigengruppenebene, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet.

Für Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot; Search, Social und Commerce hängt beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein. So geben Sie die Landingpage-URL an:

* Für Yahoo! Japan Ads-Konten verwenden den Parameter {lpurl}.

* Die für Microsoft® Advertising- und Google Ads-Konten verfügbaren Parameter finden Sie im Abschnitt [[!DNL Microsoft® Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder die Parameter &quot;Nur Tracking-Vorlage&quot;im Abschnitt &quot;Verfügbar&quot; [!DNL ValueTrack] Parameter&quot;im [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

Dieser Wert setzt die Einstellungen auf Konto- und Kampagnenebene außer Kraft, aber Tracking-Vorlagen auf detaillierteren Ebenen (mit Keyword als dem granularsten) überschreiben diesen Wert.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Suchbegriffe für die angegebene Anzeigengruppe (oder Kampagne für [!DNL Yandex] -Konten), die aus einer beliebigen Kombination von statischem Text, Spalten in der angegebenen Datei und Modifikatoren bestehen können. Spaltennamen und -modifikatoren werden durch tatsächliche Daten ersetzt, wenn die angegebene Feed-Datei über die Vorlage propagiert wird.

Um einen Spaltennamen oder eine Modifikatorgruppe als dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und dann auf einen Spaltennamen in der Spaltenliste oder auf eine [Modifikatorname](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in der Liste Modifikatoren . Um mehrere Suchbegriffe oder mehrere Übereinstimmungstypen für denselben Suchbegriff anzugeben, geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Übereinstimmungstyp-Syntax für den Spaltennamen, um den Keyword-Übereinstimmungstyp anzugeben:

* Für [!DNL Google Ads], [!DNL Microsoft® Advertising], und [!DNL Yahoo! Japan Ads] templates:

   * Dynamische Parameter: Weit gefasste Übereinstimmung = `[keyword]`, Modifikator für breite Übereinstimmung für den ersten Begriff im [!UICONTROL Keyword] Spalte (z. B. +blaue Wildlederschuhe) = `+[keyword]`, Modifikator für breite Übereinstimmung für jeden Begriff in der Spalte Suchbegriff (z. B. +Blue +Wildleder +Schuhe) = `+[keyword]+`, Phrase Match = `"[keyword]"`, genaue Übereinstimmung = `[[keyword]]`

   * Für statische Suchbegriffe: Umfassende Übereinstimmung = `keyword`, Modifikator für breite Übereinstimmung = `+keyword`, oder Phrase-Übereinstimmung = `"keyword"`

     Sie können hier keine statischen Schlüsselwörter mit exakter Übereinstimmung und Standardübereinstimmungssyntax eingeben, da sie von Klammern (`[]`), genau wie dynamische Parameter.

* Für [!DNL Yandex] templates:

   * Für dynamische Parameter: Fügen Sie den Spaltennamen ein, z. B. `[keyword]`. Verwenden Sie zur Angabe des Übereinstimmungstyps die [[!DNL Yandex]-spezifische Syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Hinweis:** Verwenden Sie für weit gefasste Übereinstimmungsbegriffe die folgende Syntax: Modifikator für breite Übereinstimmung für den ersten Begriff in der Suchbegriffspalte (z. B. +blaue Wildlederschuhe) = `+[keyword]`, Modifikator für breite Übereinstimmung für jeden Begriff in der Spalte Suchbegriff (z. B. +Blue +Wildleder +Schuhe) = `+[keyword]+`

   * Für statische Suchbegriffe: Es werden nur Suchbegriffe unterstützt. Verwenden Sie die [[!DNL Yandex]-spezifische Syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html) für den Suchbegriff. Brackets (`[]`), um anzugeben, dass die Wortreihenfolge nicht unterstützt wird.

>[!NOTE]
>
>* Sie können mehrere Modifikatorwerte manuell in das Feld Keywords einfügen, indem Sie durch Kommas getrennte Werte in Klammern entweder vor oder nach einem Suchbegriffparameter einfügen (aber nicht an beiden Stellen). Beispiel: `(cheap, discount, affordable)[product]` produziert für jedes Produkt drei separate Anzeigen.
>* Wenn Sie keinen Übereinstimmungstyp angeben, wird der standardmäßige Übereinstimmungstyp &quot;broad&quot;verwendet.
>* Negative Übereinstimmungen werden nicht unterstützt.
>* Google-Modifikatoren für breite Übereinstimmung verhalten sich nun genauso wie Phrase-Übereinstimmungen für einige Sprachen, und Sie können keine neuen Keywords für Modifikatoren für breite Übereinstimmung erstellen. Siehe [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/10286719) für weitere Informationen.

**[!UICONTROL Map Only]:** Fügt neue Anzeigen zu Anzeigengruppen (oder zu Kampagnen für [!DNL Yandex] Konten), in denen die angegebenen Suchbegriffe gefunden werden, anstatt neue Suchbegriffe zu erstellen. Aktivieren Sie das Kontrollkästchen, um diese Option zu aktivieren. Wenn diese Option aktiviert ist, gelten alle Variablen von Param 1 und Param 2 in den angegebenen Keywords nicht, da die Keywords vorhanden sind.

**[!UICONTROL Keyword Final URL]:** (Konten mit finalen/erweiterten URLs; optional) Die Landingpage-URL, zu der die Anzeigennetzwerkbenutzer beim Klicken auf Ihre Anzeige gelangen. Sie muss dieselbe Domäne wie die Anzeigen-URL enthalten und alle Parameter in der endgültigen URL müssen mit den Parametern in der Landingpage-URL nach dem Anzeigenklick übereinstimmen. Sie kann Umleitungen innerhalb der Landingpage-Domäne oder -Subdomäne enthalten, jedoch keine Umleitungen außerhalb der Landingpage-Domäne.

Wenn Sie [!DNL Google Merchant Center] Feed hinzufügen und diesen Wert in die &quot;[!DNL Link]&quot;, und fügen Sie diese Spalte dann in dieses Feld ein.

>[!NOTE]
>
>* Wenn Sie Tracking-URLs generieren, wenn Sie Daten veröffentlichen, die über die Vorlage propagiert wurden, werden Tracking-Parameter basierend auf den Konto-Tracking-Einstellungen an diesen Wert angehängt.
>* ([!DNL Google Ads] -Konten) Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.

**[!UICONTROL Keyword Tracking Template]:** (Konten mit finalen/erweiterten URLs; optional) Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als granularsten) überschreibt Werte auf allen anderen Ebenen.

* Für Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot; Search, Social und Commerce hängt beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

* Sie können optional Umleitungen und Tracking von Drittanbietern eingeben.

* So geben Sie die Landingpage-URL an:

   * ([!DNL Google Ads] und [!DNL Microsoft® Advertising] Nur) Eine Liste von Parametern zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie im Abschnitt ([!DNL Microsoft® Advertising] nur) [[!DNL Microsoft® Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder ([!DNL Google Ads] nur) die Parameter &quot;Nur Tracking-Vorlage&quot; im Abschnitt &quot;Verfügbar&quot; [!DNL ValueTrack] Parameter&quot;im [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] nur) Verwenden Sie den Parameter . `!{lpurl}` um die Landingpage-URL anzugeben.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] templates\]:** ([!DNL Google Ads] Nur Vorlagen) Die Spalte in der angegebenen Datei, die die [!DNL Google Ads] `{param1}` oder `{param2}` -Variable, die Sie in die Anzeigenkopie oder die Anzeigen-URL für jede Anzeige einfügen können, die über die Vorlage erstellt wurde. Um den dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und dann auf einen Spaltennamen in der Spaltenliste. Der Spaltenname wird durch die tatsächlichen Daten ersetzt, wenn die Feed-Datei über die Vorlage propagiert wird.

Wenn Sie einen der beiden Parameter verwenden, haben Sie die Möglichkeit, den Parameter nur auf neue Suchbegriffe anzuwenden oder auch die Werte vorhandener Suchbegriffe zu aktualisieren, die nicht aus der Vorlage erstellt wurden:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (Standard): Hiermit wird einfach der Wert des Parameters für neue Suchbegriffe eingefügt, die mit der Vorlage erstellt werden.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Neben der Erstellung neuer Suchbegriffe aus dem Feed aktualisiert Search, Social und Commerce auch den Parameterwert für alle vorhandenen Suchbegriffe in der Anzeigengruppe, die nicht mit der Vorlage erstellt wurden. Geben Sie einen einzelnen numerischen Wert ein, der für alle diese Suchbegriffe verwendet wird. Die Vorlage muss mindestens einen Suchbegriff enthalten.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Neben der Erstellung neuer Suchbegriffe aus dem Feed aktualisiert Search, Social und Commerce auch den Parameterwert für alle vorhandenen Suchbegriffe in der Anzeigengruppe, die nicht mit der Vorlage erstellt wurden, sofern die Feed-Datei numerische Werte für den Parameter mit bis zu einem Dezimalpunkt ohne Kommas, Währungssymbole oder Codes oder andere Zeichen enthält. Der Mindestwert für den Parameter in der Feed-Datei wird für alle vorhandenen Suchbegriffe verwendet. Wenn die Feed-Datei beispielsweise [!UICONTROL Param1] Werte von 21500 und 22000, dann wird die [!UICONTROL Param1] -Werte für die vorhandenen Suchbegriffe auf 21500 geändert. Die Vorlage muss mindestens einen Suchbegriff enthalten. **Tipp:** Verwenden Sie diese Option nur, wenn Sie eng gefasste Anzeigengruppen verwenden, damit Suchbegriffe denselben Wert haben.

Die Datenfelder in der Feed-Datei dürfen maximal 25 Zeichen lang sein und nur aus numerischen Daten mit den folgenden nicht numerischen Zeichen bestehen:

* (Wenn Sie &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot;) Nur bis zu einem Dezimalpunkt.

* (Wenn Sie die[!UICONTROL Apply to Existing Keywords: Min]&quot; Parameter):

   * Dem Wert kann ein Währungssymbol oder ein Währungscode vorangestellt oder angehängt werden. Beispielsweise sind 2.000,00 £ und 2.000 GBP gültig.

   * Der Wert kann ein Komma (,) oder einen Punkt (.) enthalten. als Trennzeichen mit einem optionalen Punkt (.) oder Komma (,) für Bruchwerte. Beispielsweise sind 1.000.00 und 2.000,10 gültig.

   * Dem Wert kann ein Prozentzeichen (%), Pluszeichen (+) oder Minuszeichen (-) vorangestellt oder angehängt werden. Beispielsweise sind 20 %, 208+ und -42,32 gültig.

   * Zwei Zahlen können mit einem Schrägstrich eingebettet werden. Beispielsweise sind 4/1 und 0.95/0.45 gültig.

**[!UICONTROL Param 2]\[[!DNL Microsoft® Advertising] templates\]:** ([!DNL Microsoft® Advertising] Nur Vorlagen) Die Zeichenfolge, die als Ersatzwert für eine Anzeige verwendet werden soll, wenn der Titel, Text, die Anzeigen-URL oder die endgültige URL die Variable `{Param2}` dynamische Ersatzzeichenfolge. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Anzeigenelemente, in denen Sie sie verwenden (z. B. kann ein Anzeigentitel bis zu 25 Zeichen enthalten).

**[!UICONTROL Param 3]:** ([!DNL Microsoft® Advertising] Nur Vorlagen) Die Zeichenfolge, die als Ersatzwert für eine Anzeige verwendet werden soll, wenn der Titel, Text, die Anzeigen-URL oder die endgültige URL die Variable `{Param3}` dynamische Ersatzzeichenfolge. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Anzeigenelemente, in denen Sie sie verwenden (z. B. kann ein Anzeigentitel bis zu 25 Zeichen enthalten).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** Das anfängliche Gebot für jeden Suchbegriff mit dem angegebenen Übereinstimmungstyp oder Anzeigentyp.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] und [!DNL Microsoft® Advertising] nur Kampagnen) Der Typ der Anzeigen: *[!UICONTROL Expanded Search Ads]* oder *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Optional) Fügt alle alternativen Felder zum Kopieren von Anzeigen mit Text aus den Feldern zum Kopieren der ursprünglichen Anzeige vorab ein.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Nur responsive Suchanzeigen) Die Anzeigenposition, an der der Titel/die Überschrift enthalten sein muss (z. B.[!UICONTROL Pinned at position 1]&quot;). Der Standardwert ist [!UICONTROL Unpinned].

Für jede Position muss mindestens ein Titel verfügbar sein. Wenn Sie mehrere Titel an dieselbe Position veröffentlichen, enthält die endgültige Anzeige immer einen dieser Titel an der angegebenen Position. Titel, die an Position 3 gekoppelt sind, können nicht mit der Anzeige angezeigt werden.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (Nur responsive Suchanzeigen) Die Anzeigentitel (Überschriften). Jede Anzeigenvariante muss mindestens drei und bis zu 15 Anzeigentitel enthalten. Das Werbenetzwerk zeigt Anzeigen mit bis zu drei Überschriften an. Die maximale Länge für jeden Titel beträgt 30 Zeichen, einschließlich dynamischer Texte (wie die Werte von Suchbegriffen und Anzeigenanpassungen).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Vorhandene Microsoft® Advertising-Standardtextanzeigen; schreibgeschützt) Der Titel oder die erste Zeile einer Anzeige. Die Erstellung und Bearbeitung von Standardtextanzeigen wird von Microsoft® Advertising nicht mehr unterstützt.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] und [!DNL Yahoo! Japan Ads] nur erweiterte Textanzeigenvorlagen) Die Überschrift einer Anzeige. Die maximale Länge jeder Zeile (nach der Ersetzung dynamischer Parameter) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] Nur erweiterte Textanzeigenvorlagen; optional) Eine dritte Überschrift für eine Anzeige. Die maximale Länge (nach der Ersetzung dynamischer Parameter) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

**[!UICONTROL Title]:** ([!DNL Yandex] nur) Der Titel oder die erste Zeile einer Anzeige. Die maximale Länge beträgt 33 Zeichen.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (Nur Microsoft® Advertising erweiterte Textanzeigen) Die Überschrift einer Anzeige. Die maximale Länge jeder Zeile (nach der Ersetzung dynamischer Parameter) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Nur Microsoft® Advertising erweiterte Textanzeigen) Der Hauptteil einer Anzeige. Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 80 Zeichen oder 40 Doppelbyte-Zeichen (z. B. Chinesisch, Japanisch und Koreanisch).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** Der Hauptteil der Anzeige.

* (Google Fügt erweiterte Textanzeigenvorlagen hinzu) Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 90 Zeichen oder 45 Doppelbyte-Zeichen.

* (Yahoo! Japan Ads-Vorlagen) Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 80 Zeichen oder 40 Doppelbyte-Zeichen.

* (Yandex-Vorlagen) Die maximale Länge (nach der Ersetzung dynamischer Parameter) beträgt 75 Zeichen und ein einzelnes Wort darf nicht mehr als 22 Zeichen umfassen.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Nur responsive Suchanzeigen) Die Anzeigenposition, an der die Beschreibung eingefügt werden muss (z. B. &quot;[!UICONTROL Pinned at position 1]&quot;). Der Standardwert ist [!UICONTROL Unpinned]. Für jede Position muss mindestens eine Beschreibung verfügbar sein.

Wenn Sie mehrere Beschreibungen an derselben Position veröffentlichen, enthält die endgültige Anzeige immer eine dieser Beschreibungen an der angegebenen Position. In Position 2 enthaltene Beschreibungen werden möglicherweise nicht zusammen mit der Anzeige angezeigt.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (Nur responsive Suchanzeigen) Die Anzeigenbeschreibungen. Jede Anzeigenvariante muss mindestens zwei und bis zu vier Anzeigenbeschreibungen enthalten. Das Werbenetzwerk zeigt Anzeigen mit bis zu zwei Beschreibungen an. Geben Sie mindestens zwei ein. Die maximale Länge für jede Beschreibung beträgt 90 Zeichen, einschließlich dynamischer Texte (z. B. Suchbegriffe und Anzeigenanpassungen).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Nur erweiterte Textanzeigenvorlagen in Google; optional) Eine zweite Zeile der Anzeige. Die maximale Länge (nach der Ersetzung dynamischer Parameter) beträgt 90 Zeichen oder 45 Doppelbyte-Zeichen.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Nur erweiterte Text- und responsive Suchanzeigen; optional) Ein oder zwei URL-Pfade, die nacheinander nach der Basis-URL eingeschlossen werden. Sie sollten das Produkt oder die Dienstleistung in der Anzeige ausführlicher beschreiben. Wenn Sie beispielsweise eine [!UICONTROL Display Path 1] von &quot;Schuhen&quot;und [!UICONTROL Display Path 2] von &quot;Outdoor&quot;zur Basis-URL www.example.com, lautet die URL www.example.com/Shoes/Outdoor. Die maximale Länge (nach der Ersetzung dynamischer Parameter) für jedes Feld beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.

Fügen Sie für responsive Suchanzeigen einen Anzeigenanpasser mit den folgenden Formaten ein, wobei `Default text` ist ein optionaler Wert, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, beispielsweise `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft® Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, beispielsweise `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Bestehend [!DNL Microsoft® Advertising] und [!DNL Yahoo! Japan Ads] Nur Standardtextanzeigen; schreibgeschützt) Die in einer Anzeige angezeigte URL.

[!DNL Microsoft® Advertising] und [!DNL Yahoo! Japan Ads] die Erstellung und Bearbeitung von Standardtextanzeigen eingestellt haben.

**[!UICONTROL Base URL]:** (Nur Konten mit Ziel-URLs) Die Seite, auf die Benutzer geleitet werden. Sie kann Umleitung und Trackingcode von Drittanbietern enthalten. Wenn Sie den Adobe Advertising-Konversions-Tracking-Dienst verwenden und die Kampagneneinstellungen die Verwendung der [!UICONTROL EF Redirect] Fügen Sie Tracking auf Anzeigenebene hinzu, fügt Search, Social und Commerce der Anzeige automatisch einen eigenen Weiterleitungs- und Trackingcode hinzu.

Um einen Spaltennamen oder eine Modifikatorgruppe als dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und dann auf einen Spaltennamen in der Spaltenliste oder auf eine [Modifikatorname](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) im [!UICONTROL Modifiers] Liste.

**[!UICONTROL Final URL]:** (Konten mit finalen/erweiterten URLs) Die Landingpage-URL, zu der Benutzer beim Klicken auf Ihre Anzeige gelangen. Sie muss dieselbe Domäne wie die Anzeigen-URL enthalten und alle Parameter in der endgültigen URL müssen mit den Parametern in der Landingpage-URL nach dem Anzeigenklick übereinstimmen. Sie kann Umleitungen innerhalb der Landingpage-Domäne oder -Subdomäne enthalten, jedoch keine Umleitungen außerhalb der Landingpage-Domäne.

Wenn Sie [!DNL Google Merchant] Feed zentrieren und diesen Wert in die &quot;[!UICONTROL Link]&quot;, und fügen Sie diese Spalte dann in dieses Feld ein.

>[!NOTE]
>
>* Wenn Sie Tracking-URLs generieren, wenn Sie Daten veröffentlichen, die über die Vorlage propagiert wurden, werden basierend auf den Konto-Tracking-Einstellungen Tracking-Parameter an diesen Wert angehängt.
>* ([!DNL Google Ads] Konten ) Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.

**[!UICONTROL Tracking Template]:** (Konten mit finalen/erweiterten URLs; optional) Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als granularsten) überschreibt Werte auf allen anderen Ebenen.

Für Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot; Search, Social und Commerce hängt beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein. So geben Sie die Landingpage-URL an:

* Für Yahoo! Japan Ads-Konten verwenden den Parameter {lpurl}.

* Die für Microsoft® Advertising- und Google Ads-Konten verfügbaren Parameter finden Sie im Abschnitt [[!DNL Microsoft® Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder die Parameter &quot;Nur Tracking-Vorlage&quot;im Abschnitt &quot;Verfügbar&quot; [!DNL ValueTrack] Parameter&quot;im [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

**\[Alternative Anzeigenfelder unter den ursprünglichen Anzeigenfeldern\]:** (Optional) Ein alternativer Satz von Anzeigenkopien für eine Anzeige, der verwendet werden kann, wenn eine der Zeilen in der ursprünglichen Anzeigenkopie die maximal zulässige Länge überschreitet, sobald dynamische Parameter bei der Übertragung mit Daten gefüllt werden.

>[!NOTE]
>
>* Wenn die Variable [!UICONTROL Prefill] ausgewählt ist, werden die alternativen Felder mit den ursprünglichen Feldern vorausgefüllt und können nach Bedarf bearbeitet werden.
>* Nur die Werbetexte, die die maximale Länge überschreiten, werden durch den alternativen Wert ersetzt. Wenn beispielsweise nur eine ursprüngliche Überschrift oder ein Titel zu lang ist, verwendet die generierte Anzeigenvariante die alternative Überschrift oder den alternativen Titel und die Originalbeschreibungen. Stellen Sie daher sicher, dass die alternative Anzeigenkopie in Kombination mit der ursprünglichen Anzeigenkopie sinnvoll ist.
>* Wenn die ursprüngliche Anzeigenkopie die Längenanforderungen der Suchmaschine erfüllt, wird die alternative Anzeigenkopie verworfen.

**\[Komponente\] [!UICONTROL Ad Label Classifications] > \[Beschriftungsklassifizierung und Wert\]:** (Optional) Werte für bis zu fünf vorhandene Beschriftungsklassifizierungen, um sie den Anzeigenvarianten zuzuweisen, die mit der Vorlage erstellt oder bearbeitet werden. Für jede Kampagnenkomponente, der Sie Beschriftungsklassifizierungen zuweisen möchten:

1. Aktivieren Sie das Kontrollkästchen.

1. Konfigurieren Sie die Beschriftungs-Classification-Werte für die Anzeigenvariationsvorlage:

   * Führen Sie für jede Beschriftungsklassifizierung und jeden Wert, der der Komponente zugewiesen werden soll, folgende Schritte aus:

      1. Klicks **[!UICONTROL Add Label Classification]**.

      1. Wählen Sie die vorhandene Beschriftungs-Classification aus und wählen Sie dann entweder einen vorhandenen Wert aus oder geben Sie einen neuen Wert ein.

         Die maximale Länge pro Wert beträgt 100 Zeichen. Sie kann ASCII- und Nicht-ASCII-Zeichen enthalten.

         Um einen Spaltennamen als dynamischen Parameter für einen Beschriftungs-Classification-Wert einzufügen, klicken Sie in das Eingabefeld (das zweite Feld) und dann auf einen Spaltennamen in der Spaltenliste.

         Sie können pro Kampagnenkomponente nur einen Wert pro Classification einbeziehen. Eine Kampagne kann beispielsweise &quot;Color=Red&quot;haben, jedoch nicht &quot;Color=Red&quot;und &quot;Color=Blue&quot;.

         * Um einen vorhandenen Beschriftungs-Classification-Wert zu ändern, wählen Sie einen neuen Wert aus oder geben Sie einen neuen ein.

         * Um einen vorhandenen Beschriftungs-Classification-Wert zu entfernen, klicken Sie auf **[!UICONTROL X]** neben dem Wert.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds](../inventory-feeds-about.md)
>* [Verwalten von Modifikatoren](../modifiers-manage.md)
>* [Verwalten von Bestandsdaten-Feed-Dateien](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Feed-Daten über Vorlagen übertragen](../feed-data-propagate.md)
>* [Posten von Kampagnendaten aus Inventar-Feeds in Werbenetzwerke](../propagated-data-post.md)
