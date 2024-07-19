---
title: Einstellungen für Textanzeigen und responsive Suchanzeigenvorlagen für Inventar-Feeds
description: Referenzieren Sie die Einstellungen für Textanzeigen und Vorlagen für responsive Suchanzeigen für Inventar-Feeds.
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# Einstellungen für Textanzeigen und responsive Suchanzeigenvorlagen für Inventar-Feeds


*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

>[!NOTE]
>
>* Die folgenden Zeichen sind in der Vorlage für die Bezeichnung von Spaltennamen und Modifikatornamen reserviert und sind daher als Text in allen Attributfeldern verboten: `[ ] < > `
>* In [!DNL Yandex templates] können Sie die dynamischen Parameter `{param1}` und `{param2}` nur in URLs verwenden und keine dynamische Preiseinfügung in Anzeigenbeschreibungen verwenden.

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

**[!UICONTROL Map Only]:** (Optional) Ordnet alle neuen Anzeigengruppen (nicht verfügbar für [!DNL Yandex]), Suchbegriffe und Anzeigen vorhandenen Kampagnen zu, anstatt Kampagnen zu erstellen. Wenn Sie diese Option aktivieren, wählen Sie die Zuordnungsmethode aus.

Die Verwendung von [!UICONTROL Map Only] auf Kampagnenebene erfordert eine vorhandene Kontostruktur, die eng mit der Produkttaxonomie verknüpft ist und einfach dem Daten-Feed zugeordnet werden kann.

**[!UICONTROL Map Method]:** (Wenn [!UICONTROL Map Only] für die Kampagne aktiviert ist) Die Methode, mit der neue Anzeigengruppen (nicht verfügbar für [!DNL Yandex]), Suchbegriffe und Anzeigen vorhandenen Kampagnen zugeordnet werden:

* *[!UICONTROL Contains Anywhere]:* Fügt Daten zu einer vorhandenen Kampagne hinzu, deren Name die angegebene Zeichenfolge enthält, sofern vorhanden.

* *[!UICONTROL Contains Exactly]:* Fügt Daten zu einer vorhandenen Kampagne hinzu, deren Name die angegebene Zeichenfolge enthält, sofern vorhanden.

* *[!UICONTROL Exactly Matches]* (Standard): Fügt Daten zu einer vorhandenen Kampagne mit demselben Namen hinzu, sofern vorhanden.

Wenn keine Übereinstimmung gefunden wird, werden alle Daten für die Kampagne ignoriert. Wenn mehrere Kampagnenübereinstimmungen gefunden werden, werden ihnen Suchbegriffe und Anzeigen zugeordnet.

**[!UICONTROL Campaign Tracking Template]:** (Nur Konten mit finalen/erweiterten URLs; optional) Die Tracking-Vorlage auf Kampagnenebene, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Dieser Wert überschreibt die Einstellung auf Kontoebene, aber Tracking-Vorlagen auf detaillierteren Ebenen (mit Keyword als granularster) überschreiben diesen Wert.

* Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, hängt die Such-, Social- und Commerce-Funktion beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

* So betten Sie die endgültige URL ein:

   * ([!DNL Google Ads] und [!DNL Microsoft Advertising] only) Eine Liste von Parametern, die endgültige URLs in Tracking-Vorlagen angeben sollen, finden Sie in der ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799/2) oder ([!DNL Google Ads] only) den Parametern &quot;Nur Tracking-Vorlage&quot;im Abschnitt &quot;Verfügbare [!DNL ValueTrack] Parameter&quot;in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] only) Verwenden Sie den Parameter `!{unescapedurl}`, um die URL der Landingpage anzugeben.

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

**[!UICONTROL Networks]:** (In den Kampagneneinstellungen [!DNL Google Ads] und [!DNL Yandex]) Die Netzwerke, auf denen Anzeigen platziert werden sollen:

* *[!UICONTROL Search]:* Platzieren von Angeboten für gesponserte Suchlisten.

  ([!DNL Google Ads] Kampagnen) Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Search partners]**, um Angebote für [!DNL Google Ads] Suchpartner in Listen aufzunehmen.

* *[!UICONTROL Content]:* So platzieren Sie Angebote für Platzierungen auf Inhalts- (Anzeige-)Netzwerklisten. **Hinweis:** Sie können keine Platzierungen mit der Vorlage erstellen. Wenn Sie diese Option auswählen, erstellen Sie Platzierungen für jede Anzeigengruppe und geben Sie an, welche Seiten im Anzeigennetzwerk für jede Anzeigengruppe mit <!-- insert link --> Bulksheets oder der <!-- insert links --> Anzeigengruppe und Platzierungseinstellungen in den Ansichten [!UICONTROL Search] > [!UICONTROL Campaigns] als Ziel ausgewählt werden sollen.

**[!UICONTROL Languages]:** ([!DNL Google Ads] Nur Such- und Display-Netzwerke) Eine oder mehrere Zielsprachen für Anzeigen in der Kampagne.

[!DNL Google Ads] bestimmt die Sprache eines Benutzers anhand der Spracheinstellung [!DNL Google] des Benutzers oder der Sprache der Suchabfrage, der aktuellen Seite oder der zuletzt angezeigten Seiten im [!DNL Google Display Network].

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

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, hängt die Such-, Social- und Commerce-Funktion beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein. So geben Sie die Landingpage-URL an:

* Für Yahoo! Japan Ads-Konten verwenden den Parameter {lpurl}.

* Informationen zu Parametern, die für Microsoft Advertising- und Google Ads-Konten verfügbar sind, finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348) in der Dokumentation unter &quot;Verfügbare [!DNL ValueTrack] Parameter&quot;oder in den Parametern &quot;Nur Tracking-Vorlage&quot;.[[!DNL Microsoft Advertising] ](https://help.ads.microsoft.com/#apex/3/en/56799)

Dieser Wert setzt die Einstellungen auf Konto- und Kampagnenebene außer Kraft, aber Tracking-Vorlagen auf detaillierteren Ebenen (mit Keyword als dem granularsten) überschreiben diesen Wert.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Suchbegriffe für die angegebene Anzeigengruppe (oder Kampagne für [!DNL Yandex]-Konten), die aus einer beliebigen Kombination aus statischem Text, Spalten in der angegebenen Datei und Modifikatoren bestehen können. Spaltennamen und -modifikatoren werden durch tatsächliche Daten ersetzt, wenn die angegebene Feed-Datei über die Vorlage propagiert wird.

Um einen Spaltennamen oder eine Modifikatorgruppe als dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und klicken Sie dann in der Spaltenliste auf einen Spaltennamen oder in der Modifikatorliste auf einen [Modifikatornamen](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) . Um mehrere Suchbegriffe oder mehrere Übereinstimmungstypen für denselben Suchbegriff anzugeben, geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Übereinstimmungstyp-Syntax für den Spaltennamen, um den Keyword-Übereinstimmungstyp anzugeben:

* Für die Vorlagen [!DNL Google Ads], [!DNL Microsoft Advertising] und [!DNL Yahoo! Japan Ads]:

   * Für dynamische Parameter: Gesamtübereinstimmung = `[keyword]`, Modifizierer für breite Übereinstimmung für den ersten Begriff in der Spalte [!UICONTROL Keyword] (z. B. +blaue Wildlederschuhe) = `+[keyword]`, Modifikator für breite Übereinstimmung für jeden Begriff in der Spalte &quot;Suchbegriff&quot;(z. B. +blaue +Wildlederschuhe) = `+[keyword]+`, Phrase-Übereinstimmung = `"[keyword]"`, genaue Übereinstimmung = `[[keyword]]`

   * Für statische Suchbegriffe: Gesamtübereinstimmung = `keyword`, Modifikator der breiten Übereinstimmung = `+keyword` oder Satz-Übereinstimmung = `"keyword"`

     Sie können hier keine statischen Suchbegriffe mit exakter Übereinstimmung und Standardübereinstimmungssyntax eingeben, da sie von Klammern (`[]`) umgeben sind, wie dies bei dynamischen Parametern der Fall ist.

* Für [!DNL Yandex] Vorlagen:

   * Für dynamische Parameter: Fügen Sie den Spaltennamen ein, z. B. `[keyword]`. Verwenden Sie die [[!DNL Yandex]-spezifische Syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html), um den Übereinstimmungstyp anzugeben. **Hinweis:** Verwenden Sie für weit gefasste Übereinstimmungsbegriffe die folgende Syntax: Modifikator für breite Übereinstimmung für den ersten Begriff in der Suchbegriffspalte (z. B. +blaue Wildlederschuhe) = `+[keyword]`, Modifikator für breite Übereinstimmung für jeden Begriff in der Suchbegriffspalte (z. B. +blaue +Wildlederschuhe) = `+[keyword]+`

   * Für statische Suchbegriffe: Es werden nur Suchbegriffe unterstützt. Verwenden Sie die [[!DNL Yandex]-spezifische Syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html) für den Suchbegriff. Klammern (`[]`) zur Angabe der Wortreihenfolge werden nicht unterstützt.

>[!NOTE]
>
>* Sie können mehrere Modifikatorwerte manuell in das Feld Keywords einfügen, indem Sie durch Kommas getrennte Werte in Klammern entweder vor oder nach einem Suchbegriffparameter einfügen (aber nicht an beiden Stellen). Beispielsweise erzeugt `(cheap, discount, affordable)[product]` drei separate Anzeigen für jedes Produkt.
>* Wenn Sie keinen Übereinstimmungstyp angeben, wird der standardmäßige Übereinstimmungstyp &quot;broad&quot;verwendet.
>* Negative Übereinstimmungen werden nicht unterstützt.
>* Google-Modifikatoren für breite Übereinstimmung verhalten sich nun genauso wie Phrase-Übereinstimmungen für einige Sprachen, und Sie können keine neuen Keywords für Modifikatoren für breite Übereinstimmung erstellen. Weitere Informationen finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/10286719) .

**[!UICONTROL Map Only]:** Fügt neue Anzeigen zu Anzeigengruppen (oder zu Kampagnen für [!DNL Yandex]-Konten) hinzu, in denen die angegebenen Suchbegriffe gefunden werden, anstatt neue Suchbegriffe zu erstellen. Aktivieren Sie das Kontrollkästchen, um diese Option zu aktivieren. Wenn diese Option aktiviert ist, gelten alle Variablen von Param 1 und Param 2 in den angegebenen Keywords nicht, da die Keywords vorhanden sind.

**[!UICONTROL Keyword Final URL]:** (Konten mit finalen/erweiterten URLs; optional) Die Landingpage-URL, zu der Benutzer des Anzeigennetzwerks beim Klicken auf Ihre Anzeige gelangen. Sie muss dieselbe Domäne wie die Anzeigen-URL enthalten und alle Parameter in der endgültigen URL müssen mit den Parametern in der Landingpage-URL nach dem Anzeigenklick übereinstimmen. Sie kann Umleitungen innerhalb der Landingpage-Domäne oder -Subdomäne enthalten, jedoch keine Umleitungen außerhalb der Landingpage-Domäne.

Wenn Sie einen [!DNL Google Merchant Center] -Feed verwenden und diesen Wert in die Spalte &quot;[!DNL Link]&quot; aufnehmen, fügen Sie diese Spalte in dieses Feld ein.

>[!NOTE]
>
>* Wenn Sie Tracking-URLs generieren, wenn Sie Daten veröffentlichen, die über die Vorlage propagiert wurden, werden Tracking-Parameter basierend auf den Konto-Tracking-Einstellungen an diesen Wert angehängt.
>* ([!DNL Google Ads] -Konten) Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.

**[!UICONTROL Keyword Tracking Template]:** (Konten mit finalen/erweiterten URLs; optional) Die Tracking-Vorlage, die alle Off-Landingpage-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als granularsten) überschreibt Werte auf allen anderen Ebenen.

* Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, hängt die Such-, Social- und Commerce-Funktion beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

* Sie können optional Umleitungen und Tracking von Drittanbietern eingeben.

* So geben Sie die Landingpage-URL an:

   * ([!DNL Google Ads] und [!DNL Microsoft Advertising] only) Eine Liste von Parametern, die endgültige URLs in Tracking-Vorlagen angeben sollen, finden Sie in der ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder ([!DNL Google Ads] only) den Parametern &quot;Nur Tracking-Vorlage&quot;im Abschnitt &quot;Verfügbare [!DNL ValueTrack] Parameter&quot;in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] only) Verwenden Sie den Parameter `!{lpurl}`, um die URL der Landingpage anzugeben.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] templates\]:** ([!DNL Google Ads] templates) Die Spalte in der angegebenen Datei, die die Variable [!DNL Google Ads] `{param1}` oder `{param2}` darstellt, die Sie in die Anzeigen-Copy- oder Anzeigen-URL für jede Anzeige einfügen können, die aus der Vorlage erstellt wurde. Um den dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und dann auf einen Spaltennamen in der Spaltenliste. Der Spaltenname wird durch die tatsächlichen Daten ersetzt, wenn die Feed-Datei über die Vorlage propagiert wird.

Wenn Sie einen der beiden Parameter verwenden, haben Sie die Möglichkeit, den Parameter nur auf neue Suchbegriffe anzuwenden oder auch die Werte vorhandener Suchbegriffe zu aktualisieren, die nicht aus der Vorlage erstellt wurden:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (Standard): Hiermit wird einfach der Wert des Parameters für neue Suchbegriffe eingefügt, die mit der Vorlage erstellt werden.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Neben der Erstellung neuer Suchbegriffe aus dem Feed aktualisiert Search, Social und Commerce auch den Parameterwert für alle vorhandenen Suchbegriffe in der Anzeigengruppe, die nicht mit der Vorlage erstellt wurden. Geben Sie einen einzelnen numerischen Wert ein, der für alle diese Suchbegriffe verwendet wird. Die Vorlage muss mindestens einen Suchbegriff enthalten.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Neben der Erstellung neuer Suchbegriffe aus dem Feed aktualisiert Search, Social und Commerce auch den Parameterwert für alle vorhandenen Suchbegriffe in der Anzeigengruppe, die nicht mit der Vorlage erstellt wurden, solange die Feed-Datei numerische Werte für den Parameter mit bis zu einem Dezimalpunkt ohne Kommas, Währungssymbole oder Codes oder andere Zeichen enthält. Der Mindestwert für den Parameter in der Feed-Datei wird für alle vorhandenen Suchbegriffe verwendet. Wenn die Feed-Datei beispielsweise die Werte &quot;[!UICONTROL Param1]&quot;von 21500 und 22000 aufweist, werden die Werte &quot;[!UICONTROL Param1]&quot;für die vorhandenen Suchbegriffe in &quot;21500&quot;geändert. Die Vorlage muss mindestens einen Suchbegriff enthalten. **Tipp:** Verwenden Sie diese Option nur, wenn Sie eng gefasste Anzeigengruppen mit Themen haben, sodass es sinnvoll ist, dass Suchbegriffe denselben Wert haben.

Die Datenfelder in der Feed-Datei dürfen maximal 25 Zeichen lang sein und nur aus numerischen Daten mit den folgenden nicht numerischen Zeichen bestehen:

* (Wenn Sie den Parameter &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; verwenden) Nur bis zu einem Dezimalpunkt.

* (Wenn Sie den Parameter &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; nicht verwenden):

   * Dem Wert kann ein Währungssymbol oder ein Währungscode vorangestellt oder angehängt werden. Beispielsweise sind 2.000,00 £ und 2.000 GBP gültig.

   * Der Wert kann ein Komma (,) oder einen Punkt (.) enthalten. als Trennzeichen mit einem optionalen Punkt (.) oder Komma (,) für Bruchwerte. Beispielsweise sind 1.000.00 und 2.000,10 gültig.

   * Dem Wert kann ein Prozentzeichen (%), Pluszeichen (+) oder Minuszeichen (-) vorangestellt oder angehängt werden. Beispielsweise sind 20 %, 208+ und -42,32 gültig.

   * Zwei Zahlen können mit einem Schrägstrich eingebettet werden. Beispielsweise sind 4/1 und 0.95/0.45 gültig.

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising] templates\]:** ([!DNL Microsoft Advertising] templates only) Die Zeichenfolge, die als Ersatzwert für eine Anzeige verwendet werden soll, wenn der Titel, Text, die Anzeigen-URL oder die endgültige URL die dynamische Ersetzungszeichenfolge `{Param2}` enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Anzeigenelemente, in denen Sie sie verwenden (z. B. kann ein Anzeigentitel bis zu 25 Zeichen enthalten).

**[!UICONTROL Param 3]:** ([!DNL Microsoft Advertising] nur Vorlagen) Die Zeichenfolge, die als Substitutionswert für eine Anzeige verwendet wird, wenn der Titel, Text, die Anzeigen-URL oder die endgültige URL die dynamische Ersetzungszeichenfolge `{Param3}` enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Anzeigenelemente, in denen Sie sie verwenden (z. B. kann ein Anzeigentitel bis zu 25 Zeichen enthalten).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** Das anfängliche Gebot für jeden Suchbegriff mit dem angegebenen Übereinstimmungstyp oder Anzeigentyp.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] und [!DNL Microsoft Advertising] Kampagnen only) Der Typ der Anzeigen: *[!UICONTROL Expanded Search Ads]* oder *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Optional) Fügt alle alternativen Anzeigenkopie-Felder mit Text aus den ursprünglichen Werbeanzeigenkopie-Feldern vorab ein.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Nur responsive Suchanzeigen) Die Anzeigenposition, an der der Titel/die Überschrift enthalten sein muss (z. B. &quot;[!UICONTROL Pinned at position 1]&quot;). Der Standardwert ist [!UICONTROL Unpinned].

Für jede Position muss mindestens ein Titel verfügbar sein. Wenn Sie mehrere Titel an dieselbe Position veröffentlichen, enthält die endgültige Anzeige immer einen dieser Titel an der angegebenen Position. Titel, die an Position 3 gekoppelt sind, können nicht mit der Anzeige angezeigt werden.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (Nur responsive Suchanzeigen) Die Anzeigentitel (Überschriften). Jede Anzeigenvariante muss mindestens drei und bis zu 15 Anzeigentitel enthalten. Das Werbenetzwerk zeigt Anzeigen mit bis zu drei Überschriften an. Die maximale Länge für jeden Titel beträgt 30 Zeichen, einschließlich dynamischer Texte (wie die Werte von Suchbegriffen und Anzeigenanpassungen).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Vorhandene Microsoft Advertising-Standardtextanzeigen; schreibgeschützt) Der Titel oder die erste Zeile einer Anzeige. Microsoft Advertising hat die Erstellung und Bearbeitung von Standardtextanzeigen eingestellt.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] und [!DNL Yahoo! Japan Ads] nur erweiterte/erweiterte Textanzeigenvorlagen) Die Überschrift einer Anzeige. Die maximale Länge jeder Zeile (nach der Ersetzung dynamischer Parameter) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] nur erweiterte Textanzeigenvorlagen; optional) Eine dritte Überschrift für eine Anzeige. Die maximale Länge (nach der Ersetzung dynamischer Parameter) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

**[!UICONTROL Title]:** ([!DNL Yandex] Nur) Der Titel oder die erste Zeile einer Anzeige. Die maximale Länge beträgt 33 Zeichen.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (Nur erweiterte Textanzeigen von Microsoft Advertising) Die Überschrift einer Anzeige. Die maximale Länge jeder Zeile (nach der Ersetzung dynamischer Parameter) beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Nur erweiterte Microsoft Advertising-Textanzeigen) Der Hauptteil einer Anzeige. Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 80 Zeichen oder 40 Doppelbyte-Zeichen (z. B. Chinesisch, Japanisch und Koreanisch).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** Der Hauptteil der Anzeige.

* (Google Fügt erweiterte Textanzeigenvorlagen hinzu) Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 90 Zeichen oder 45 Doppelbyte-Zeichen.

* (Yahoo! Japan Ads-Vorlagen) Die maximale Länge (nachdem dynamische Parameter ersetzt wurden) beträgt 80 Zeichen oder 40 Doppelbyte-Zeichen.

* (Yandex-Vorlagen) Die maximale Länge (nach der Ersetzung dynamischer Parameter) beträgt 75 Zeichen und ein einzelnes Wort darf nicht mehr als 22 Zeichen umfassen.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Nur responsive Suchanzeigen) Die Anzeigenposition, an der die Beschreibung enthalten sein muss (z. B. &quot;[!UICONTROL Pinned at position 1]&quot;). Der Standardwert ist [!UICONTROL Unpinned]. Für jede Position muss mindestens eine Beschreibung verfügbar sein.

Wenn Sie mehrere Beschreibungen an derselben Position veröffentlichen, enthält die endgültige Anzeige immer eine dieser Beschreibungen an der angegebenen Position. In Position 2 enthaltene Beschreibungen werden möglicherweise nicht zusammen mit der Anzeige angezeigt.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (Nur responsive Suchanzeigen) Die Anzeigenbeschreibungen. Jede Anzeigenvariante muss mindestens zwei und bis zu vier Anzeigenbeschreibungen enthalten. Das Werbenetzwerk zeigt Anzeigen mit bis zu zwei Beschreibungen an. Geben Sie mindestens zwei ein. Die maximale Länge für jede Beschreibung beträgt 90 Zeichen, einschließlich dynamischer Texte (z. B. Suchbegriffe und Anzeigenanpassungen).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Nur erweiterte Textanzeigenvorlagen von Google; optional) Eine zweite Zeile der Anzeige. Die maximale Länge (nach der Ersetzung dynamischer Parameter) beträgt 90 Zeichen oder 45 Doppelbyte-Zeichen.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Nur erweiterte Text- und responsive Suchanzeigen; optional) Ein oder zwei URL-Pfade, die nacheinander nach der Basis-URL eingeschlossen werden. Sie sollten das Produkt oder die Dienstleistung in der Anzeige ausführlicher beschreiben. Wenn Sie beispielsweise der Basis-URL www.example.com den Wert [!UICONTROL Display Path 1] von &quot;Schuhe&quot;und den Wert [!UICONTROL Display Path 2] von &quot;Outdoor&quot;hinzufügen, lautet die URL www.example.com/Shoes/Outdoor. Die maximale Länge (nach der Ersetzung dynamischer Parameter) für jedes Feld beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.

Fügen Sie für responsive Suchanzeigen einen Anzeigenanpasser mit den folgenden Formaten ein, wobei `Default text` ein optionaler Wert ist, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Nur vorhandene Standardtextanzeigen [!DNL Microsoft Advertising] und [!DNL Yahoo! Japan Ads]; schreibgeschützt) Die in einer Anzeige angezeigte URL.

[!DNL Microsoft Advertising] und [!DNL Yahoo! Japan Ads] haben die Erstellung und Bearbeitung von Standardtextanzeigen eingestellt.

**[!UICONTROL Base URL]:** (Nur Konten mit Ziel-URLs) Die Seite, auf die Benutzer geleitet werden. Sie kann Umleitung und Trackingcode von Drittanbietern enthalten. Wenn Sie den Adobe Advertising-Konversions-Tracking-Dienst verwenden und die Kampagneneinstellungen die Verwendung von [!UICONTROL EF Redirect] und das Hinzufügen von Tracking auf Anzeigenebene umfassen, fügt Search, Social und Commerce der Anzeige automatisch einen eigenen Weiterleitungs- und Trackingcode hinzu.

Um einen Spaltennamen oder eine Modifikatorgruppe als dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und klicken Sie dann in der Spaltenliste auf einen Spaltennamen oder in der Liste [!UICONTROL Modifiers] auf einen [Modifikatornamen](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) .

**[!UICONTROL Final URL]:** (Konten mit finalen/erweiterten URLs) Die Landingpage-URL, zu der Benutzer beim Klicken auf Ihre Anzeige gelangen. Sie muss dieselbe Domäne wie die Anzeigen-URL enthalten und alle Parameter in der endgültigen URL müssen mit den Parametern in der Landingpage-URL nach dem Anzeigenklick übereinstimmen. Sie kann Umleitungen innerhalb der Landingpage-Domäne oder -Subdomäne enthalten, jedoch keine Umleitungen außerhalb der Landingpage-Domäne.

Wenn Sie einen &quot;[!DNL Google Merchant] Center&quot;-Feed verwenden und diesen Wert in die &quot;[!UICONTROL Link]&quot;-Spalte aufnehmen, fügen Sie diese Spalte in dieses Feld ein.

>[!NOTE]
>
>* Wenn Sie Tracking-URLs generieren, wenn Sie Daten veröffentlichen, die über die Vorlage propagiert wurden, werden basierend auf den Konto-Tracking-Einstellungen Tracking-Parameter an diesen Wert angehängt.
>* ([!DNL Google Ads] -Konten ) Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.

**[!UICONTROL Tracking Template]:** (Konten mit finalen/erweiterten URLs; optional) Die Tracking-Vorlage, die alle Off-Landingpage-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als granularsten) überschreibt Werte auf allen anderen Ebenen.

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, hängt die Such-, Social- und Commerce-Funktion beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein. So geben Sie die Landingpage-URL an:

* Für Yahoo! Japan Ads-Konten verwenden den Parameter {lpurl}.

* Informationen zu Parametern, die für Microsoft Advertising- und Google Ads-Konten verfügbar sind, finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348) in der Dokumentation unter &quot;Verfügbare [!DNL ValueTrack] Parameter&quot;oder in den Parametern &quot;Nur Tracking-Vorlage&quot;.[[!DNL Microsoft Advertising] ](https://help.ads.microsoft.com/#apex/3/en/56799)

**\[Alternative Anzeigenfelder unter den ursprünglichen Anzeigenfeldern\]:** (Optional) Ein alternativer Satz von Anzeigenkopien für eine Anzeige, der verwendet werden kann, wenn eine der Zeilen in der ursprünglichen Anzeigenkopie die maximal zulässige Länge überschreitet, sobald dynamische Parameter bei der Propagierung mit Daten gefüllt werden.

>[!NOTE]
>
>* Wenn die Option [!UICONTROL Prefill] ausgewählt ist, werden die alternativen Felder mit den ursprünglichen Feldern vorausgefüllt und können nach Bedarf bearbeitet werden.
>* Nur die Werbetexte, die die maximale Länge überschreiten, werden durch den alternativen Wert ersetzt. Wenn beispielsweise nur eine ursprüngliche Überschrift oder ein Titel zu lang ist, verwendet die generierte Anzeigenvariante die alternative Überschrift oder den alternativen Titel und die Originalbeschreibungen. Stellen Sie daher sicher, dass die alternative Anzeigenkopie in Kombination mit der ursprünglichen Anzeigenkopie sinnvoll ist.
>* Wenn die ursprüngliche Anzeigenkopie die Längenanforderungen der Suchmaschine erfüllt, wird die alternative Anzeigenkopie verworfen.

**\[Komponente\] [!UICONTROL Ad Label Classifications] > \[Beschriftungsklassifizierung und Wert\]:** (Optional) Werte für bis zu fünf vorhandene Beschriftungsklassifizierungen, um sie den Anzeigenvarianten zuzuweisen, die mit der Vorlage erstellt oder bearbeitet werden. Für jede Kampagnenkomponente, der Sie Beschriftungsklassifizierungen zuweisen möchten:

1. Aktivieren Sie das Kontrollkästchen.

1. Konfigurieren Sie die Beschriftungs-Classification-Werte für die Anzeigenvariationsvorlage:

   * Führen Sie für jede Beschriftungsklassifizierung und jeden Wert, der der Komponente zugewiesen werden soll, folgende Schritte aus:

      1. Klicken Sie auf **[!UICONTROL Add Label Classification]**.

      1. Wählen Sie die vorhandene Beschriftungs-Classification aus und wählen Sie dann entweder einen vorhandenen Wert aus oder geben Sie einen neuen Wert ein.

         Die maximale Länge pro Wert beträgt 100 Zeichen. Sie kann ASCII- und Nicht-ASCII-Zeichen enthalten.

         Um einen Spaltennamen als dynamischen Parameter für einen Beschriftungs-Classification-Wert einzufügen, klicken Sie in das Eingabefeld (das zweite Feld) und dann auf einen Spaltennamen in der Spaltenliste.

         Sie können pro Kampagnenkomponente nur einen Wert pro Classification einbeziehen. Eine Kampagne kann beispielsweise &quot;Color=Red&quot;haben, jedoch nicht &quot;Color=Red&quot;und &quot;Color=Blue&quot;.

         * Um einen vorhandenen Beschriftungs-Classification-Wert zu ändern, wählen Sie einen neuen Wert aus oder geben Sie einen neuen ein.

         * Um einen vorhandenen Beschriftungs-Classification-Wert zu entfernen, klicken Sie neben dem Wert auf **[!UICONTROL X]** .

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
>* [Verwalten von Bestandsdaten-Feed-Dateien](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Übertragen von Feed-Daten über Vorlagen](../feed-data-propagate.md)
>* [Veröffentlichen von Kampagnendaten aus Inventar-Feeds in Werbenetzwerke](../propagated-data-post.md)
