---
title: 'Erforderliche Bulksheet-Daten für  [!DNL Google Ads] '
description: Referenzieren Sie die erforderlichen Kopfzeilenfelder und Datenfelder in Bulksheets für  [!DNL Google Ads]  Konten.
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '7898'
ht-degree: 0%

---

# Anhang - Erforderliche Bulksheet-Daten für [!DNL Google Ads]

Um [!DNL Google Ads] Kampagnendaten stapelweise zu erstellen und zu aktualisieren, können Sie Bulksheet-Dateien für Search, Social und Commerce verwenden, die speziell für [!DNL Google Ads]-Konten formatiert sind. Sie können entweder a) [Bulksheet-Dateien für bestehende Konten &#x200B;](../bulksheet-download.md) dem erforderlichen Dateiformat generieren oder b) sie manuell erstellen (siehe &quot;[Unterstützte Bulksheet-](bulksheet-file-formats.md)&quot; für allgemeine Informationen über die unterstützten Dateiformate).

Jedes Bulksheet muss die Header-Felder und die entsprechenden Datenfelder enthalten, die für die [spezifischen Vorgänge, die Sie durchführen möchten, (](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md). B. das Erstellen einer Anzeige) erforderlich sind. Wenn ein Feld nicht erforderlich ist, können Sie es in der Kopfzeile und in den Datenzeilen auslassen. Alle benutzerdefinierten Spalten werden beim Hochladen der Bulk-Sheet-Datei gelöscht.

Im Folgenden finden Sie eine Tabelle mit allen verfügbaren Datenfeldern und zusätzlichen Tabellen, die angeben, welche Felder zum Hinzufügen, Bearbeiten oder Löschen von Daten für einzelne Entitäten (z. B. Kampagnen und Keywords) erforderlich sind.

## Alle verfügbaren Datenfelder {#bulksheet-fields-all-google}

In der folgenden Tabelle werden alle verfügbaren Datenfelder beschrieben.

Die für Kontoentitäten relevanten Datenfelder finden Sie unter &quot;[Felder, die zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente erforderlich sind](#bulksheet-fields-per-component-google)&quot;.

>[!NOTE]
>
>* Bei den Werten in allen Textspalten wird zwischen Groß- und Kleinschreibung unterschieden.
>* Wenn Sie einen neuen Datensatz erstellen und keine Werte für alle erforderlichen Datenfelder einschließen, werden einigen dieser Felder die angegebenen Standardwerte zugewiesen.
>* Für Felder, die unten nicht angegeben werden, wird der Standardwert für das Werbenetzwerk verwendet.
>* Eine Liste der verfügbaren Bulksheet-Zeilen im [!UICONTROL Download Bulksheet]-Dialogfeld finden Sie unter [Bulksheet-Zeilen nach Anzeigennetzwerk](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network).

| Feld | Beschreibung |
| ---- | ---- |
| [!UICONTROL Platform] | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Acct Name] | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| [!UICONTROL Campaign Budget] | Eine tägliche Ausgabenbegrenzung für die Kampagne, mit oder ohne Währungssymbole und Satzzeichen. Dieser Wert überschreibt das Kontobudget, darf es jedoch nicht überschreiten. |
| [!UICONTROL Delivery Method] | <p>Wie schnell Anzeigen für die Kampagne jeden Tag angezeigt werden:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (Standard für neue Kampagnen): Um Ihre Anzeigen-Impressions über den Tag zu verteilen.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (im Oktober 2019 nicht mehr unterstützt), um Ihre Anzeigen so oft wie möglich anzuzeigen, bis Ihr Budget erreicht ist. Daher werden Ihre Anzeigen möglicherweise nicht zu einem späteren Zeitpunkt angezeigt.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>Die Kanäle, auf denen Anzeigen geschaltet werden. Geben Sie eine oder mehrere Optionen an:</p><ul><li><p><i>[!UICONTROL Search]</i> (Standard für neue Kampagnen): Platzieren von Anzeigen im [!DNL Google Ads]-Suchnetzwerk (einschließlich Websites von [!DNL Google Ads] Such- und Suchpartnern) und optional auch im [!DNL Google Ads]-Display-Netzwerk. <b>Hinweis</b> Kampagnen, die sowohl auf das Suchnetzwerk als auch auf das Anzeigennetzwerk abzielen, können nicht zur Angebotsoptimierung zu einem Portfolio hinzugefügt werden.</p></li><li><p><i>[!UICONTROL Display]</i>: Platzieren von Anzeigen nur im [!DNL Google Ads] Anzeigennetzwerk.</p></li><li><p><i>[!UICONTROL Shopping]</i>: Platzieren von Shopping-Anzeigen in [!DNL Google Ads] Shopping-Netzwerk (in ausgewählten Ländern) und dem [!DNL Google Ads]-Suchnetzwerk (einschließlich Websites [!DNL Google Ads] Such- und Suchpartner). Um Shopping-Anzeigen zu erstellen, müssen Sie Produkte in einem [!DNL Google Merchant Center]-Konto haben und [Search, Social und Commerce dürfen keine Daten aus dem Konto herunterladen](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Siehe &quot;[Implementieren [!DNL Google Ads] Shopping-](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; für weitere Informationen zum Erstellen von Shopping-Anzeigen.</p></li></ul> |
| [!UICONTROL Networks] | <p>Wo Anzeigen geschaltet werden können. Geben Sie eine oder mehrere Optionen an:</p><ul><li><p><i>[!UICONTROL Google Search]</i>: Nur gesponserte Suchlisten im Google Search Network.</p></li><li><p><i>[!UICONTROL Search Partners]</i>: Gesponserte Suchlisten zu den Suchpartnern von Google.</p></li><li><p><i>[!UICONTROL Content]</i>: Gebote für die Anzeige von Netzwerklisten abgeben.</p></li><li><p><i>[!UICONTROL All]</i> (Standard für neue Kampagnen): Targeting von Google-Suche, Suchpartnern und Inhalten.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Nur Suchnetzwerk; nur anwendbar auf erweiterte dynamische Suchanzeigen) Die Stammdomäne (z. B. example.com) oder Subdomäne (z. B. shoes.example.com) der Website, deren Inhalt das Anzeigennetzwerk zum Targeting Ihrer dynamischen Suchanzeigen verwendet.<br><br><b>Hinweise:</b></p><ul><li><p>Erweiterte dynamische Suchanzeigen zielen auf Website-Inhalte statt auf Keywords ab.</p></li><li><p>Ihre Domain muss vom organischen Suchindex des Anzeigennetzwerks indiziert sein, damit sie als Ziel ausgewählt werden kann.</p></li><li><p>Wenn Sie keine Domain angeben, müssen Sie für jede Anzeigengruppe dynamische Suchziele erstellen, die entweder alle Ihre Website-Seiten oder eine Untergruppe davon ansprechen.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Nur Netzwerk durchsuchen; gilt nur für erweiterte dynamische Suchanzeigen) Die Sprache für die angegebene Website-Domain. <b>Hinweis:</b> Wenn die Domain Seiten in mehreren Sprachen enthält und Sie alle ansprechen möchten, erstellen Sie für jede Sprache eine separate Kampagne. |
| [!UICONTROL GDN Custom Bid Level] | (Nur für das Anzeigennetzwerk bestimmte Kampagnen) Gebotsweise: <i>[!UICONTROL Ad Group]</i> (Standard), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (Website) oder <i>[!UICONTROL None]</i> (zum Zurücksetzen des vorhandenen Werts). Andere Dimensionen (<i>Alter</i>, <i>Geschlecht</i>, <i>Interesse und Liste</i>, <i>Thema</i> und <i>Vertikal</i>) sind in der [!DNL Google Ads] verfügbar. Wenn Sie die [!DNL Google Ads]-Schnittstelle zum Konfigurieren von Geboten nach einer anderen Dimension verwendet haben, wird dieser Wert angezeigt, Sie können diese Dimensionen jedoch hier nicht auswählen oder eingeben.</p><p><b>Hinweis:</b></p><ul><li><p>Erstellen Sie Tracking-Vorlagen auf Keyword-Ebene, wenn Sie Gebote nach Keyword erstellen. Erstellen Sie auf ähnliche Weise Tracking-Vorlagen auf Platzierungsebene, wenn Sie nach Platzierung bieten. Erstellen Sie für alle anderen Dimensionen Tracking-Vorlagen auf Anzeigenebene.</p></li><li><p>Wenn Sie nach einer nicht unterstützten Dimension (Alter, Geschlecht, Interesse und Liste oder Thema) bieten, optimiert Search, Social und Commerce keine Angebote für die Dimension und die gesamte Attribution wird auf die Anzeigengruppe angewendet.</p></li><li><p>Werbeanzeigen im Suchnetzwerk verwenden immer Keyword-Gebote.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Nur Einkaufskampagnen) Die Priorität, mit der die Kampagne verwendet wird, wenn mehrere Kampagnen für dasselbe Produkt werben: <i>[!UICONTROL Low]</i> (der Standard für neue Kampagnen), <i>[!UICONTROL Medium]</i> oder <i>[!UICONTROL High]</i>.</p><p>Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Anzeigennetzwerk zuerst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion geeignet ist. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot geeignet. |
| [!UICONTROL Has EU Political Ads] | (Gilt für Kampagnen, die auf Zielgruppen in der Europäischen Union (EU) abzielen) Gibt an, ob die Kampagne politische Werbung gemäß den Anforderungen für in der Europäischen Union gemäß der EU-Verordnung 2024/90 geschaltete Anzeigen enthält: <i>[!UICONTROL Yes]</i> oder <i>[!UICONTROL No]</i>. |
| [!UICONTROL Merchant ID] | (Nur Shopping-Kampagnen und Audience-Kampagnen, die mit einem Händler-Feed verknüpft sind) Die Kunden-ID des Händler-Kontos, dessen Produkte für die Kampagne verwendet werden. |
| [!UICONTROL Sales Country] | (Nur Shopping-Kampagnen; bei bestehenden Kampagnen schreibgeschützt) Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, für welche Produkte in der Kampagne geworben wird. |
| [!UICONTROL Product Scope Filter] | (Nur Kampagnen, die das [!DNL Google Ads] Shopping-Netzwerk verwenden) Die Produkte in Ihrem [!DNL Google Merchant Center]-Konto, für die Shopping-Anzeigen für die Kampagne erstellt werden können. Mit dem Format dimension=attribute können Sie bis zu sieben Produktdimensions- und Attributkombinationen eingeben, nach denen Ihre Produkte gefiltert werden sollen. Trennen Sie mehrere Filter durch ein Trennzeichen &quot;>>&quot;. Eine Liste der verfügbaren Produktdimensionen finden Sie unter &quot;[&#x200B; von Kampagnenproduktfiltern](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).</p><p>Beispiel: „KategorieL1=Tiere„KategorieL2=Haustierbedarf„Marke=Acme Haustierbedarf“</p><p>Verwenden Sie zum Löschen der vorhandenen Werte den Wert <code>[delete]</code> (einschließlich der Klammern).</p> |
| [!UICONTROL Languages] | <p>(Nur Netzwerke suchen und anzeigen) Die Zielsprachen für Anzeigen in der Kampagne.</p><p>Wenn Sie weder für dieses Feld noch für das Feld [!UICONTROL Geo Targeting] einen Wert für eine neue Kampagne eingeben, bestimmt die für das Konto angegebene Währung die Standardsprachen. Der Unterschied besteht darin, dass Kampagnen mit Währungen, die nicht bestimmten Sprachen zugeordnet sind (z. B. EUR), auf alle Sprachen ausgerichtet sind. Wenn Sie keinen Wert für dieses Feld eingeben, sondern einen Wert in das [!UICONTROL Geo Targeting] Feld für eine neue Kampagne eingeben, ist dies standardmäßig <i>[!UICONTROL All]</i>. Wenn Sie dieses Feld für eine vorhandene Kampagne leer lassen, wird der vorhandene Wert beibehalten.</p><p>Um alle Sprachen auszuwählen, geben Sie <span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span> ein. Um bestimmte Sprachen auszuwählen, geben Sie Werte ein, die durch Semikolons getrennt sind, und zwar entweder <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] Sprachnamen (</a>. B. <i>Englisch;Japanisch</i>, die durch die richtigen numerischen Codes ersetzt werden) oder numerische Codes (<i>1000;1005</i>). Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.</p> |
| [!UICONTROL Location] | Ein geografischer Ort, an dem Anzeigen für die Kampagne geschaltet werden sollen oder für den Anzeigen ausgeschlossen werden sollen. Wenn Sie für eine neue Kampagne keine Werte für dieses Feld oder das Feld Sprachen eingeben, bestimmt die für das Konto angegebene Währung die Standardspeicherorte. Der Unterschied besteht darin, dass Kampagnen mit Währungen, die nicht bestimmten Speicherorten zugeordnet sind (z. B. EUR), auf alle Speicherorte ausgerichtet sind. Wenn Sie keinen Wert für dieses Feld eingeben, sondern einen Wert in das [!UICONTROL Languages] Feld für eine neue Kampagne eingeben, ist dies standardmäßig <i>[!UICONTROL All]</i>. Wenn Sie dieses Feld für eine vorhandene Kampagne leer lassen, wird der vorhandene Wert beibehalten.</p><p>Verwenden Sie einen der [[!DNL Google Ads] Ortsnamen“ (die durch den richtigen numerischen Code ersetzt werden](https://developers.google.com/adwords/api/docs/appendix/geotargeting) oder Standortcodes, um einen bestimmten Standort auszuwählen:</p><ul><li><p>Länder/Gebiete: Geben Sie die Namen der Länder/Gebiete (<i>.USA;Japan</i>) oder die numerischen Codes (<i>.2840;2392</i>) ein.</p></li><li><p>Bundesstaaten/Provinzen/Regionen: Geben Sie die Namen der Bundesstaaten/Provinzen/Regionen mit den entsprechenden Abkürzungen für Länder/Regionen (z. B. <i>Tokyo, JP; New York, USA</i>) oder die numerischen Codes (z. B. <i>20636;21167</i>) ein.</p></li><li><p>Städte außerhalb der USA: Geben Sie den Stadtnamen, den Bundesstaat/Provinz/Regionsnamen und die Abkürzungen für Land/Gebiet (z. B. <i>Adachi, Tokyo, JP; Kita, Tokyo, JP</i>) oder die numerischen Codes (z. B. <i>1028850;1009293</i>) ein</p></li><li><p>U-Bahn-Gebiete in den USA: Geben Sie die Namen der Städte, Bundesstaaten und Länderkürzel (z. B. <i>Buffalo NY, US;New York NY, US</i>) oder die numerischen Codes (z. B. <i>514;501</i>) ein.</p></li></ul><p>Um einen Standort auszuschließen, stellen Sie dem Standortnamen oder -code ein Minuszeichen (`-`) voran, z. B. <i>-Japan</i>.</p><p><b>Hinweis:</b> Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.</p> |
| [!UICONTROL Location Type] | (Wenn Sie einen Speicherort einschließen) Der [Standorttyp](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Ein Gerätetyp, für den Angebotsanpassungen auf Kampagnen- oder Anzeigengruppenebene vorgenommen werden: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> oder <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(Wenn Sie ein [!UICONTROL Location], einen [!UICONTROL Device] oder eine Zielgruppe [!UICONTROL RLSA]) Ob die Angebote für Anzeigen an einem bestimmten Ort, auf einem bestimmten Gerätetyp oder mit einer bestimmten Zielgruppe angepasst werden sollen:</p><ul><li><p>Um das Gebot auf Keyword-Ebene zu verwenden (0 % Differenz), geben Sie 0 ein. Bei neuen Zielgruppen können Sie dieses Feld auch leer lassen.</p></li><li><p>Um ein anderes Angebot für diese Zielgruppe zu verwenden, geben Sie den Prozentsatz ein, um den die Gebote erhöht oder verringert werden sollen.</p></li><ul><li><p>Gültige Prozentsätze für Standort- und RLSA-Ziele sind -90 bis 900.</p></li><li><p>Gültige Prozentsätze für Geräteangebotsanpassungen sind:</p></li><ul><li><p>(Kampagnen)-100 (kein Gebot für Anzeigen auf dem Gerätetyp) oder von -90 bis 900.</p></li><li><p>(Anzeigengruppen) -100 für Smartphones und Tablets (um kein Gebot für den Gerätetyp abzugeben) und -90 bis 900 für alle Gerätetypen.</p></li></ul></ul><li><p>(Bestehende Kampagnen und Anzeigengruppen) Lassen Sie dieses Feld leer, um die vorhandene Angebotsanpassung zu verwenden.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (In generierten Bulksheets zu Informationszwecken enthalten) Die schreibgeschützte Angebotsanpassung, die Adobe für ein Standortziel auf Kampagnenebene oder ein RLSA empfiehlt. Sie wird nur berechnet, wenn sich die Kampagne in einem Portfolio mit einem Ziel befindet, das gewichtete Konversionsmetriken verwendet (nicht das [!UICONTROL Maximize Clicks] Ziel), und die Kampagne mindestens zwei Standort-Ziele oder RLSAs mit mindestens fünf Klicks oder 5 USD an Kosten in den letzten 90 Tagen enthält.</p><p>Wenn Sie ein Standortziel oder RLSA manuell bearbeiten möchten, um den empfohlenen Wert zu verwenden, warten Sie nach der Erstellung des Standortziels oder RLSA mindestens zwei Wochen, um eine ausreichende Datenerfassung zu ermöglichen, und ändern Sie den Wert nicht öfter als einmal pro Woche. |
| [!UICONTROL Device Targets] | <p>(Nur ältere Kampagnentypen) Die Geräte, auf denen die Anzeige angezeigt werden kann: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> oder <i>[!UICONTROL Tablets]</i>. Für neue Kampagnen lautet der Standardwert <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Nur ältere Kampagnentypen; anwendbar, wenn die Geräteziele „Smartphones“ oder „Tablets“ umfassen) Die Betriebssysteme, auf denen die Anzeige angezeigt werden kann: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> oder <i>[!UICONTROL Palm]</i>. Für neue Kampagnen lautet der Standardwert <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Nur veraltete Kampagnentypen; anwendbar, wenn die [!UICONTROL Device Targets] &quot;[!UICONTROL All]&quot; oder &quot;[!UICONTROL Smartphones]&quot; enthalten) Mobilfunknetzbetreiber, mit denen die Smartphones verbunden sein können: <i>[!UICONTROL All]</i> oder ein oder mehrere durch &lt;c<i>Netzbetreiber-Code</i>>,&lt;<i>Länder-Code</i>> (z. B. T-Mobile,US) angegebene Netzbetreiber unter Verwendung der Liste <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">verfügbaren Netzbetreiber und Codes für [!DNL Google Ads]</a>. Trennen Sie mehrere Träger mit Semikolons (z. B. T-Mobile,US;T-Mobile,GB). Für neue Kampagnen lautet der Standardwert <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>Der eindeutige Name, der eine Anzeigengruppe identifiziert. Die maximale Länge beträgt 255 Zeichen. Nachfolgende leere Zeichen werden nicht gespeichert (beispielsweise wird „Anzeigengruppe 1 &quot; als „Anzeigengruppe 1 &quot; gespeichert). Dieses Feld gilt nicht für Sitelinks auf Kampagnenebene oder Geräte-Ziele auf Kampagnenebene.</p> |
| [!UICONTROL Ad Group Type] | <p>Der Anzeigengruppentyp: <i>[!UICONTROL Demand Gen]</i> (nur für Demand Gen-Kampagnen), <i>[!UICONTROL Display]</i> (für Display-Kampagnen), <i>[!UICONTROL Search Dynamic]</i> (für erweiterte dynamische Suchanzeigen), <i>[!UICONTROL Search Standard]</i> (für Suchanzeigen), <i>[!UICONTROL Shopping Product]</i> (für Shopping-Produktanzeigen), <i>[!UICONTROL Shopping Showcase]</i> (Erstellung und Bearbeitung wird nicht unterstützt) oder <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Nur CPC-Kampagnen) Die maximalen Kosten pro Klick (CPC), d. h. der höchste Betrag, der für einen Anzeigenklick im Werbenetzwerk bezahlt werden muss, mit oder ohne Währungssymbole und Satzzeichen. Sie können Werte für Anzeigengruppen und Keywords, Produktgruppen und dynamische Suchziele festlegen. Der Standardwert für ein neues Keyword wird von der Anzeigengruppenebene übernommen. Für Produktgruppen können Sie Werte für die niedrigste Produktgruppenebene festlegen. Der Standard für eine neue Ebene wird von der übergeordneten Ebene übernommen.</p><p>Für bestehende Produktgruppen und dynamische Suchziele in optimierten Portfolios sind Aktualisierungen nur für einen Tag wirksam und werden im nächsten Optimierungszyklus überschrieben.</p> |
| [!UICONTROL Max Content CPC] | <p>(Nur CPC-Kampagnen) Die maximalen Inhaltskosten pro Klick (CPC), d. h. der höchste Betrag, der für einen Anzeigenklick auf einer Display-Netzwerk-Website bezahlt werden muss, mit oder ohne Währungssymbole und Satzzeichen. Sie können Werte in Kampagnen, die nicht auf Platzierungen ausgerichtet sind, auf Anzeigengruppenebene festlegen und bearbeiten.</p> |
| [!UICONTROL Audience Target Method] | <p>(Kampagnen, die nur im Suchnetzwerk laufen, und vorhandene, schreibgeschützte [!DNL Gmail] Kampagnen im Display-Netzwerk) Ob:</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>: Anzeigen nur Benutzern anzeigen, die mit Zielgruppen verknüpft sind und auch andere Ziele für die Anzeigengruppe erfüllen.</p></li><li><p><i>[!UICONTROL Bid Only]</i>: Anzeigen auch Personen anzuzeigen, die nicht mit Zielgruppen verknüpft sind, solange sie andere Zielgruppen auf Anzeigengruppenebene erfüllen.</p><p>Sie können jedoch die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie höhere Gebote für diese Zielgruppen festlegen.</p></li></ul> |
| [!UICONTROL Keyword] | Die Keyword-Zeichenfolge. Die maximale Länge beträgt 80 Zeichen und maximal 10 Wörter. Sie darf nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: Leerzeichen `# $ & _ - " [ ] ' + . / :`</p><p><b>Hinweis:</b></p><ul><li><p>Um ein Keyword auf Anzeigengruppen- oder Kampagnenebene auszuschließen, setzen Sie den [!UICONTROL Match Type] auf <i>[!UICONTROL Negative]</i>. Wenn die Zeile den Namen der Anzeigengruppe enthält, wird das Keyword für die Anzeigengruppe ausgeschlossen. Wenn die Zeile nicht den Namen der Anzeigengruppe enthält, wird das Keyword für die gesamte Kampagne ausgeschlossen.</p></li><li><p>Wenn Sie ein [!DNL Google Ads] Schlüsselwort oder einen Übereinstimmungstyp ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues erstellt.</p></li></ul> |
| [!UICONTROL Placement] | (Kampagnen, bei denen nur Inhalte übereinstimmen) Eine Platzierung im Display-Netzwerk, auf der Ihre Anzeigen angezeigt werden können. Geben Sie eine der folgenden Optionen an:</p><ul><li><p>Website: Geben Sie eine gültige URL ein. Dabei kann es sich um eine Domain auf oberster Ebene, eine Subdomain auf oberster Ebene oder eine Domain mit einem einzelnen Verzeichnisnamen handeln. Die URL darf kein Fragezeichen (?) enthalten. Beispiele:<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>Eine Anzeigenposition auf einer bestimmten Seite: Verwenden Sie den `<URL> >> <location,sublocation>` Format (z. B. `finance.google.com >> Company pages,Top right`).</p></li><li><p>Eine Themenkategorie: Verwenden der Syntax `<category::<category> > <subcategory>` usw. (z. B. `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Hinweis:</b> Um eine Platzierung auf der Anzeigengruppen- oder Kampagnenebene auszuschließen, setzen Sie die [!UICONTROL Match Type] auf <i>[!UICONTROL Negative]</i>. Wenn die Zeile den Namen der Anzeigengruppe enthält, wird die Platzierung für die Anzeigengruppe ausgeschlossen. Wenn die Zeile nicht den Namen der Anzeigengruppe enthält, wird die Platzierung für die gesamte Kampagne ausgeschlossen.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Erforderlich, wenn die Kampagneneinstellung &quot;[!UICONTROL Use my website contents to target my ads]&quot; nicht aktiviert ist; andernfalls optional) Dynamische Suchziele für die Anzeigengruppe.</p><p>Verwenden Sie für alle Ziele ein Sternchen (*).</p><p>Verwenden Sie für die Auswahl von bis zu drei dynamischen Suchkriterien das Format `<category>=<target>` , wobei `<category>` jede der folgenden Kategorien einschließen können. Mehrere Ziele für eine einzelne Kategorie mit &quot;\[Leerraum\] und \[Leerraum\]&quot; verbinden und mehrere Kategorien mit &quot;[Leerraum] und [Leerraum] verbinden.</p><ul><li><p><i>[!UICONTROL Category]</i>: Anzeigen erweiterter dynamischer Suchanzeigen für indizierte Seiten mit einer bestimmten [!DNL Google Ads] Inhaltskategorie.</p></li><li><p><i>[!UICONTROL URL]</i>: Anzeigen erweiterter dynamischer Suchanzeigen für indizierte Seiten mit einer bestimmten URL, wobei der Wert an einer beliebigen Stelle in der URL enthalten sein kann.</p></li><li><p><i>[!UICONTROL Page Title]</i>: Zum Anzeigen erweiterter dynamischer Suchanzeigen für indizierte Seiten mit bestimmtem Text im Seitentitel.</p></li><li><p><i>[!UICONTROL Page Content]</i>: Anzeigen erweiterter dynamischer Suchanzeigen für indizierte Seiten mit bestimmtem Inhalt.</p></li></ul><p>Beispiel: url=shoes.example.com und page title=Footwear</p> |
| [!UICONTROL Parent Product Groupings] | Die Hierarchie der übergeordneten Produktgruppen.<br><br>Beispiel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>Die Produktgruppe (z. B. „brand=acme“ oder „Alle Produkte„).</p><p><b>Hinweis:</b></p><ul><li><p>Wenn eine bestimmte Produktgruppe nicht in der [!UICONTROL Parent Product Groupings] vorhanden ist, erstellt Search, Social und Commerce die erforderlichen Teile der Hierarchie.</p></li><li><p>Search, Social und Commerce erstellt automatisch eine Gruppe &quot;[!UICONTROL All Products]&quot;, wenn Sie eine Anzeigengruppe in einer [!DNL Google Ads] Shopping-Kampagne erstellen und das Standardangebot auf das Standardangebot der Anzeigengruppe festgelegt ist. Search, Social und Commerce erstellen automatisch eine Gruppe &quot;[!UICONTROL Everything Else]&quot; mit dem Standardgebot der Anzeigengruppe auf jeder Ebene der Produktgruppenhierarchie. Sie können diese Standardgruppen weiterhin explizit erstellen und sie entweder ausschließen oder ihre Angebote ändern.</p></li><li><p>Jede Anzeigengruppe kann bis zu acht Ebenen von Produktgruppen enthalten, einschließlich &quot;[!UICONTROL All Products]&quot; und sieben weiteren Ebenen.</p></li></ul> |
| [!UICONTROL Partition Type] | Der Partitionstyp für die Produktgruppe: <i>Unterteilung</i> (wenn untergeordnete Produktgruppen vorhanden sind) oder <i>Einheit</i> (wenn keine untergeordneten Produktgruppen vorhanden sind). |
| [!UICONTROL Match Type] | <p>Für dynamische Suchziele oder -produktgruppen: Die Suchbegriffabgleichoption für die dynamische Suchzielgruppe oder -produktgruppe: <i>[!UICONTROL Dynamic Ad Target]</i> (der Standard für neue dynamische Suchziele), <i>[!UICONTROL Product Group]</i> (der Standard für neue Produktgruppen) oder <i>[!UICONTROL Negative Product Group]</i> (zum Ausschließen einer Produktgruppe).</p><p>Bei Schlüsselwörtern: Die Option zum Abgleichen von Schlüsselwörtern für das Schlüsselwort: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> oder <i>[!UICONTROL Negative]</i> (um ein Schlüsselwort oder eine Platzierung im Display-Netzwerk auszuschließen); Produktgruppen, die mit Shopping-Anzeigen verwendet werden, haben den Typ „Übereinstimmung“ von <i>[!UICONTROL Product Group]</i>. Wenn Sie <i>[!UICONTROL Negative]</i> verwenden, müssen Sie auch den Übereinstimmungstyp angeben, der ausgeschlossen werden soll (z. B. „Negativsatz„).</p><p>Für neue Schlüsselwörter ist der Standardwert <i>[!UICONTROL Broad]</i>. Ein Wert für entweder den Übereinstimmungstyp oder die Keyword-ID ist nur erforderlich, um ein Keyword mit mehreren Übereinstimmungstypen zu bearbeiten.</p><p><b>Hinweis:</b></p><ul><li><p>Übereinstimmungstypen können nicht auf erweiterte dynamische Suchanzeigen angewendet werden, die keine Keywords verwenden.</p></li><li><p>Wenn Sie den Übereinstimmungstyp für ein [!DNL Google Ads] Schlüsselwort ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues erstellt.</p></li><li><p>Wählen Sie für den Modifikator „Weit“ und fügen Sie ein + vor einem Wort innerhalb des Keywords ein, für das enge Varianten erforderlich sind (z. B. &quot;+Rot+Schuhe“, um enge Varianten sowohl von „Rot“ als auch von „Schuhe“ zu erfordern). <b>Hinweis:</b> Modifikatoren für breite Übereinstimmungen weisen jetzt dasselbe Übereinstimmungsverhalten wie Phrasenübereinstimmung für einige Sprachen auf, und seit Juli 2021 konnten keine neuen Keywords für breite Übereinstimmungsmodifikatoren erstellt werden. Weitere Informationen finden [[!DNL Google Ads]  unter &#x200B;](https://support.google.com/google-ads/answer/7042511)Dokumentation).</p> |
| [!UICONTROL First Page Bid] | (Zu Informationszwecken in generierten Bulksheets enthalten) Das Angebot, das erforderlich ist, um eine Anzeige auf der ersten Seite der Suchergebnisse zu platzieren. Dieser Wert wird nicht an das Werbenetzwerk gesendet. |
| [!UICONTROL Quality Score] | (In generierten Bulksheets zu Informationszwecken enthalten) Der aktuelle Qualitätswert, den die Suchmaschine dem Keyword zugewiesen hat. Dieser Wert wird nicht an das Werbenetzwerk gesendet.) |
| [!UICONTROL Creative Preferred Devices] | (Textanzeigen, erweiterte dynamische Suchanzeigen und erweiterte Sitelinks; optional) Die Gerätetypen, für die Sie die Anzeige lieber anzeigen möchten: <i>[!UICONTROL All]</i> (Standard) oder <i>[!UICONTROL Mobile]</i>. Wenn <i>[!UICONTROL Mobile]</i> angegeben ist, versucht das Netzwerk, die Anzeige für Benutzende von Mobilgeräten und nicht für Desktop- oder Tablet-Benutzende anzuzeigen. Andernfalls zeigt das Netzwerk die Anzeige auf jedem Gerätetyp an.</p><p><b>Hinweis:</b></p><ul><li><p>Diese Einstellung kann nur von Benutzern des Admins und des [!DNL Adobe] Account Managers bearbeitet werden.</p></li><li><p>Das Netzwerk garantiert nicht, dass es die Anzeige auf dem bevorzugten Gerätetyp anzeigt.</p></li><li><p>Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Nur erweiterte Textanzeigen und responsive Suchanzeigen) Die Überschriften einer Anzeige, jeweils getrennt durch einen vertikalen senkrechten Strich (&vert;). Die maximale Länge für jedes Feld Anzeigentitel beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen, einschließlich dynamischem Text (z. B. die Werte von Schlüsselwörtern und Anzeigenanpassungen).</p><p>Für responsive Suchanzeigen sind [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] und [!UICONTROL Ad Title 3] erforderlich. Alle anderen Felder für den Anzeigentitel sind optional. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den Wert <code>[delete]</code> (einschließlich der Klammern).</p><p>Fügen Sie für responsive Suchanzeigen eine Anzeigenanpassung im folgenden Format ein: <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, z. B. <code>{CUSTOMIZER.Discount:10%}</code></p><p>Sie können keine erweiterten Textanzeigen erstellen oder bearbeiten, aber Sie können sie löschen, die im Juni 2022 eingestellt [!DNL Google Ads]. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Nur responsive Suchanzeigen; optional) Eine Position, an der der entsprechende Anzeigentitel angeheftet werden kann: `[null]` (kein Wert, wodurch der Anzeigentitel für alle Positionen geeignet ist), <i>1</i>, <i>2</i> oder <i>3</i>. Wenn [!UICONTROL Ad Title Position] beispielsweise den Wert 1 hat, wird der Anzeigentitel nur in Position 1 angezeigt. Standardmäßig sind alle Anzeigentitel null (ohne Werte).</p><p>Verwenden Sie zum Löschen des vorhandenen Werts den Wert <code>[delete]</code> (einschließlich der Klammern).</p><p><b>Hinweis:</b> Sie können mehrere Anzeigentitel an derselben Position anheften. Das Werbenetzwerk verwendet einen der an die Position angehefteten Anzeigentitel. Titel, die an Position 3 angeheftet sind, werden in der Anzeige möglicherweise nicht angezeigt.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Nur erweiterte dynamische Suchanzeigen, erweiterte Textanzeigen und responsive Suchanzeigen) Der Hauptteil einer Anzeige. Die maximale Länge für jedes Beschreibungsfeld beträgt 90 Zeichen oder 45 Doppelbyte-Zeichen, einschließlich dynamischer Texte (wie Werte von Schlüsselwörtern und Anzeigenanpassungen).</p><p>Fügen Sie für responsive Suchanzeigen eine Anzeigenanpassung ein, die das folgende Format verwendet: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, z. B. `{CUSTOMIZER.Discount:10%}`</p><p>Verwenden Sie für erweiterte dynamische Suchanzeigen nur [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2]. <b>Hinweis:</b> Bei diesem Anzeigentyp wird durch Ändern der Anzeigenkopie die vorhandene Anzeige gelöscht und eine neue erstellt.</p><p>Sie können keine erweiterten Textanzeigen erstellen oder bearbeiten, aber Sie können sie löschen, die im Juni 2022 eingestellt [!DNL Google Ads].</p><p>Für responsive Suchanzeigen sind [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] erforderlich. [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional. Verwenden Sie zum Löschen des vorhandenen Werts den Wert <code>[delete]</code> (einschließlich der Klammern).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Nur responsive Suchanzeigen; optional) Eine Position, an der die entsprechende Beschreibung angeheftet werden kann: `[null]` (kein Wert, wodurch die Beschreibung für alle Positionen geeignet ist), <i>1</i>, <i>2</i> oder <i>3</i>. Wenn [!UICONTROL Description 1 Position] beispielsweise den Wert 1 hat, wird [!UICONTROL Description 1] nur in Position 1 angezeigt. Standardmäßig werden keine Beschreibungen an eine Position angeheftet.</p><p>Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern).</p><p><b>Hinweis:</b> Sie können mehrere Beschreibungen an derselben Position anheften. Das Werbenetzwerk verwendet eine der an die Position angehefteten Beschreibungen. An Position 2 angeheftete Beschreibungen werden in der Anzeige möglicherweise nicht angezeigt. |
| [!UICONTROL Display URL] | Die in der Anzeige enthaltene URL.<br><br>Bei erweiterten dynamischen Suchanzeigen generiert [!DNL Google Ads] diesen Wert dynamisch aus der Website-Domain und Sie müssen keinen Wert eingeben.<br><br>Für responsive Suchanzeigen müssen Sie keinen Wert eingeben. Die Anzeige-URL wird in der endgültigen URL automatisch aus der Domain extrahiert. Sie können die URL optional mit den Feldern Pfad 1 und Pfad 2 anpassen.<br><br>Sie können keine erweiterten Textanzeigen erstellen oder bearbeiten, aber Sie können sie löschen, die im Juni 2022 eingestellt [!DNL Google Ads].<br><br><b>Hinweis:</b> (Konten mit endgültigen URLs) Die Domain-Namen in der Anzeige-URL und der endgültigen URL müssen übereinstimmen.</p> |
| [!UICONTROL Display Path 1] | <p>(Nur erweiterte Textanzeigen <span> responsive Suchanzeigen</span>)</p><p>(Optional) Text, der zur Anzeige-URL hinzugefügt wird, die automatisch aus der endgültigen URL extrahiert wird. In der URL wird ihm ein Schrägstrich (/) vorangestellt. Ein Pfad darf keine Schrägstriche (/) oder Zeilenumbrüche (\n) enthalten. Die maximale Länge beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.</p><p>Verwenden Sie zum Einfügen einer Anzeigenanpassung die folgenden Formate, wobei `Default text` ein optionaler Wert ist, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält:&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`</p><p>Wenn [!UICONTROL Display Path 1] beispielsweise „Angebote“ lautet, dann lautet die Anzeige-URL &lt;<i>Display URL</i>//Angebote, z. B. www.example.com/deals.</p><p>Sie können keine erweiterten Textanzeigen erstellen oder bearbeiten, aber Sie können sie löschen, die im Juni 2022 eingestellt [!DNL Google Ads].</p> |
| [!UICONTROL Display Path 2] | Ein zweiter Anzeigepfad. Siehe den Eintrag für [!UICONTROL Display Path 1].<br><br>Beispiel: Wenn [!UICONTROL Display Path 1] „Angebote“ und [!UICONTROL Display Path 2] „lokal“ ist, dann lautet die Anzeige-URL &lt;<i>Display URL</i>>/offers/local, z. B. www.example.com/deals/local.</p><p>Sie können keine erweiterten Textanzeigen erstellen oder bearbeiten, aber Sie können sie löschen, die im Juni 2022 eingestellt [!DNL Google Ads].</p> |
| [!UICONTROL Promotion Line] | (Nur Produktlisten-Anzeigen) Eine optionale Promotion-Zeile, die in den Suchergebnissen in den Produktlisten enthalten sein soll. Die maximale Länge beträgt 45 Zeichen.</p><p>Die Promotion-Zeile kann relativ zur Anzeige an verschiedenen Stellen angezeigt werden (z. B. unter der Anzeige), je nachdem, wo die Anzeige auf der Seite erscheint. |
| [!UICONTROL Link Name] | <p>Der Sitelink-Text. Sie kann bis zu 25 Zeichen lang sein.</p><p>Bei neuen Sitelinks müssen Sie den Kampagnennamen in die Zeile „Sitelink“ aufnehmen. Bei Sitelinks auf Anzeigengruppenebene müssen Sie auch den Anzeigengruppennamen angeben.</p><p><b>Hinweis:</b> Vorhandener Text von 35 Zeichen wird weiterhin in Anzeigen auf Desktops und Tablets angezeigt, jedoch nicht auf Mobilgeräten.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Nur vorhandene App-Installationsanzeigen) Das Betriebssystem, auf dem die Mobile App ausgeführt wird: <i>Android™</i> oder <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Nur vorhandene App-Installationsanzeigen) <p>Die Anwendungs-ID oder der Paketname. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Nur vorhandene App-Installationsanzeigen) Der Name des Programms. |
| [!UICONTROL Start Date] | <p>(Nur erweiterte Sitelinks) Das erste Datum, an dem Gebote für den Sitelink in der Zeitzone des Werbetreibenden und in einem der folgenden Formate abgegeben werden können: <i>m/d/jjjj</i>, <i>m/d/jjj</i>, <i>m-d-jjjj</i> oder <i>m-d-jjj</i>. Der Standardwert für neue erweiterte Sitelinks ist der aktuelle Tag.</p><p><b>Hinweis</b> Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden.</p> |
| [!UICONTROL End Date] | <p>(Nur erweiterte Sitelinks) Das letzte Datum, an dem Gebote für den Sitelink in der Zeitzone des Werbetreibenden und in einem der folgenden Formate abgegeben werden können:  <i>m/d/jjjj</i>, <i>m/d/jjjj</i>, <i>m-d-jjjj</i> oder <i>m-d-jjj</i>. Der Standardwert ist „Ohne“ (kein Enddatum).</p><p><b>Hinweis</b> Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Nur vorhandene App-Installationsanzeigen)</p><p>(Optional) Verhindert, dass [!DNL Google Ads] die Anzeige für Tablet-Benutzer anzeigen. Werte können &quot;<i>&quot; </i> &quot;<i>&quot; </i>. |
| [!UICONTROL Landing Page Suffix] | Alle Parameter, die an das Ende der endgültigen URLs angehängt werden müssen, um Informationen zu tracken. Beispiel: `param2=value1&param3=value2`<br><br>Siehe &quot;[Klick-Tracking-Formate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).“<br><br>Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Zur einfacheren Wartung verwenden Sie nur das Suffix auf Kontoebene, es sei denn, eine andere Nachverfolgung für einzelne Kontokomponenten ist erforderlich. Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den [!DNL Google Ads]. |
| [!UICONTROL Tracking Template] | Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen [!DNL ValueTrack] einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als der detailliertesten) überschreibt die Werte auf allen höheren Ebenen.<br><br>Für das Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, fügt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode an.<br><br>Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein. Eine Liste der [!DNL ValueTrack] zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie unter den Parametern „Nur Tracking-Vorlage“ im Abschnitt „Verfügbare [!DNL ValueTrack]&quot; in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/2375447).<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Base URL/Final URL] | Die Landingpage-URL, zu der Suchmaschinenbenutzer beim Klicken auf Ihre Anzeige geleitet werden, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter. Basis-/endgültige URLs auf Keyword-Ebene überschreiben diese auf Anzeigenebene und höher.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Destination URL] | (Zu Informationszwecken in generierten Bulksheets enthalten; nicht an die Suchmaschine gepostet) Bei Konten mit Ziel-URLs handelt es sich um die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Werbetreibenden verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Sie enthält alle Anlagenparameter, die für die Kampagne oder das Konto „Suche“, „Social“ und &quot;Commerce&quot; konfiguriert wurden. Wenn Sie Tracking-URLs generiert haben, basiert dies auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie suchmaschinenspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Search, Social und Commerce ersetzt werden.<br><br>Bei Konten mit endgültigen URLs zeigt diese Spalte denselben Wert wie die Spalte „Basis-URL/Endgültige URL“ an. |
| [!UICONTROL Custom URL Param] | Daten, die durch die dynamische Variable `{custom_code}` ersetzt werden sollen, wenn die Variable in den Tracking-Parametern für das Suchkonto oder die Kampagneneinstellungen enthalten ist. Um den benutzerdefinierten Wert in die Tracking-URL einzufügen, müssen Sie die Bulksheet-Datei mit der Option Tracking-URLs generieren hochladen. |
| [!UICONTROL Creative Type] | Das Anzeigenformat: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Demand Gen Carousel Ad]</i> (Karussell-Anzeigen mit mehreren Bildern), <i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>, <i>[!UICONTROL Demand Gen Product Ad]</i> und <i>[!UICONTROL Demand Gen Video Ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (veralteter Anzeigentyp), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (veraltet), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (Shopping-Anzeigen) oder <i>[!UICONTROL Responsive search ad]</i>. Der Standardwert für neue Anzeigen lautet <i>[!UICONTROL Text ad]</i>.<br><br>Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Param1] | <p>Der numerische Wert des `{param1}` Anzeigenparameters, der bei jeder Anzeige in der Bulksheet-Datei in die Anzeigenkopie oder die Anzeige-URL aufgenommen werden kann. Die maximale Länge beträgt 25 Zeichen und Sie können die folgenden nicht numerischen Zeichen einbeziehen:</p><ul><li><p>Dem Wert kann ein Währungssymbol oder ein Währungscode vorangestellt oder angehängt werden. Beispielsweise sind `£2.000,00` und `2000GBP` gültig.</p></li><li><p>Der Wert kann ein Komma (`,`) oder einen Punkt (`.`) als Trennzeichen enthalten, mit einem optionalen Punkt (`.`) oder Komma (`,`) für Teilwerte. Beispielsweise sind `1,000.00` und `2.000,10` gültig.</p></li><li><p>Dem Wert kann ein Prozentzeichen (`%`), ein Pluszeichen (`+`) oder ein Minuszeichen (`- `) vorangestellt oder angehängt werden. Beispielsweise sind `20%`, `208+` und `-42.32` gültig.</p></li><li><p>Zwei Zahlen können mit einem Schrägstrich eingebettet werden. Beispielsweise sind `4/1` und `0.95/0.45` gültig.</p></li></ul><p>Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern).</p> |
| [!UICONTROL Param2] | Der numerische Wert des `{param2}` Anzeigenparameters, der bei jeder Anzeige in der Bulksheet-Datei in die Anzeigenkopie oder die Anzeige-URL aufgenommen werden kann. Weitere Informationen finden Sie im Eintrag für Param1 . |
| [!UICONTROL Audience] | Die Remarketing-Liste für Suchanzeigen (RLSA) richtet sich an die Zielgruppe oder die ausgeschlossene Zielgruppe für die Kampagne oder Anzeigengruppe. Geben Sie im Feld „Zieltyp“ an, ob es sich um eine Zielgruppe oder einen Ausschluss handelt. |
| [!UICONTROL Target Type] | (Wenn eine Zielgruppe angegeben wird) Gibt an, ob es sich bei der angegebenen Zielgruppe um <i>Einschluss</i> (Ziel) oder <i>Ausschluss</i> handelt. |
| [!UICONTROL Campaign Status] | Der Anzeigestatus der Kampagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (nicht bearbeitbar) oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Kampagnen). Der Standardwert für neue Kampagnen ist <i>[!UICONTROL Active]</i>. Um eine aktive oder pausierte Kampagne zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Ad Group Status] | Der Anzeigestatus der Anzeigengruppe: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigengruppen). Der Standardwert für neue Anzeigengruppen ist [!UICONTROL Active]. Um eine aktive oder angehaltene Anzeigengruppe zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Keyword Status] | Der Anzeigestatus des Keywords: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Keywords). Die Standardeinstellung für neue Schlüsselwörter ist [!UICONTROL Active]. Um ein aktives oder angehaltenes Keyword zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Ad Status] | Der Anzeigestatus der Anzeige: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigen), <i>[!UICONTROL Disapproved]</i> (nicht bearbeitbar) oder <i>[!UICONTROL Paused]</i>. Der Standardwert für neue Anzeigen lautet [!UICONTROL Active]. Um eine aktive oder pausierte Anzeige zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Placement Status] | Der Status der Website-Platzierung: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigen). Der Standardwert für neue Websites lautet <i>Aktiv.</i> Um eine aktive oder angehaltene Platzierung zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Target Status] | Der Status eines dynamischen Suchziels: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Ziele). Der Standardwert für neue Ziele ist <i>Aktiv.</i> Um ein aktives oder angehaltenes Ziel zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Product Group Status] | Der Anzeigestatus der Produktgruppe: <i>[!UICONTROL Active]</i> <span>oder</span> <i>[!UICONTROL Deleted]</i> (nur bestehende Produktgruppen). Der Standardwert für neue Produktgruppen ist <i>[!UICONTROL Active]</i>. Um eine aktive Produktgruppe zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Sitelink Status] | Der Anzeigestatus des Sitelinks: <i>Aktiv oder Gelöscht</i> (nur vorhandene Sitelinks). Der Standardwert für neue Sitelinks ist <i>[!UICONTROL Active]</i>. Um einen aktiven Sitelink zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Location Status] | Der Status des Standortziels: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Standorte). Der Standardwert für neue Speicherorte lautet [!UICONTROL Active]. Um einen aktiven Speicherort zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL RLSA Target Status] | Der Status des RLSA-Ziels oder Ausschlusses auf Kampagnen- oder Anzeigengruppenebene: <i>[!UICONTROL Active]</i> oder [!UICONTROL Deleted]</i> (nur vorhandene Ziele). Der Standardwert für neue Ziele oder Ausschlüsse ist <i>[!UICONTROL Active]</i>. Um eine aktive Zielgruppe oder einen aktiven Ausschluss zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Device Target Status] | <p>Der Status des Zielgeräts auf Kampagnen- oder Anzeigengruppenebene: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i>. Für neue Kampagnen und Anzeigengruppen ist der Standardwert <i>[!UICONTROL Active]</i>.</p> |
| \[Advertiser-spezifische Label-Klassifizierung\] | (Benannt nach einer Advertiser-spezifischen Kennzeichnungsklassifizierung, z. B. „Farbe“ für eine Kennzeichnungsklassifizierung namens „Farbe„) Ein Wert für die angegebene Klassifizierung, der mit der Entität verknüpft ist. Pro Entität kann nur ein Wert angegeben werden (z. B. „Rot“ für die Kennzeichnung „Farbe“ für Kampagne A). Die maximale Länge beträgt 100 Zeichen. Der Wert kann ASCII- und Nicht-ASCII-Zeichen enthalten.<br><br>Kennzeichnungsklassifizierungen und ihre Kennzeichnungswerte werden auf alle untergeordneten Komponenten angewendet; neue Komponenten, die später hinzugefügt werden, werden automatisch mit der Kennzeichnung verknüpft. Kennzeichnungsklassifizierungen für Produktgruppen werden auf die Ebene der Einheit (mit der höchsten Granularität) angewendet.<br><br>Weder beim Klassifizierungsnamen noch beim Klassifizierungswert wird zwischen Groß- und Kleinschreibung unterschieden. |
| [!UICONTROL Constraints] | Eine Begrenzung, die der Entität zugewiesen ist. Pro Entität kann nur eine Einschränkung zugewiesen werden.<br><b>>Abhängigkeiten werden von untergeordneten Entitäten übernommen. Daher müssen Sie keine Werte für untergeordnete Entitäten eingeben, es sei denn, Sie möchten die übernommenen Werte überschreiben. |
| [!UICONTROL Campaign ID] | Die eindeutige ID, die eine vorhandene Kampagne identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Kampagne. |
| [!UICONTROL Ad Group ID] | Die eindeutige ID, die eine vorhandene Anzeigengruppe identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Anzeigengruppe. |
| [!UICONTROL Keyword ID] | Die eindeutige ID, die ein vorhandenes Keyword identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie das Keyword ändern, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung des Keywords oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Ad ID] | <p>Die eindeutige ID, die eine vorhandene Anzeige identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Für responsive Suchanzeigen ist zum Bearbeiten oder Löschen von Anzeigendaten entweder die Anzeigen-ID oder die AMO-ID erforderlich. Für alle anderen Entitätstypen ist die Anzeigen-ID nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichend Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen.</p><p><b>Hinweis:</b> Wenn Sie a) Anzeigeneigenschaftsspalten mit Ausnahme des Status für eine vorhandene Anzeige oder b) Daten für eine responsive Suchanzeige bearbeiten und weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen, wird eine neue Anzeige erstellt und die vorhandene Anzeige wird nicht geändert.</p> |
| [!UICONTROL Placement ID] | Die eindeutige ID, die eine Website-Platzierung identifiziert. Nur erforderlich, wenn Sie die Platzierung ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung der Platzierung oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Target ID] | Die eindeutige ID, die ein vorhandenes automatisches Targeting identifiziert. Nur erforderlich, wenn Sie das automatische Targeting ändern oder löschen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Target. |
| [!UICONTROL Product Group ID] | Die eindeutige ID, die eine vorhandene Produktgruppe identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung der Produktgruppe oder b) ein &quot;[!UICONTROL AMO ID]&quot;.“ |
| [!UICONTROL Sitelink ID] | Die eindeutige ID, die einen vorhandenen Sitelink identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten, um den Sitelink zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] einbeziehen und die Eigenschaftsspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status für nur einen der Sitelinks.</p><p><b>Hinweis:</b> Wenn Sie die Eigenschaftsspalten eines Sitelinks mit Ausnahme des Status für einen vorhandenen Sitelink bearbeiten und weder den [!UICONTROL Sitelink ID] noch den [!UICONTROL AMO ID] einbeziehen, wird ein neuer Sitelink erstellt und der vorhandene Sitelink wird nicht geändert. |
| [!UICONTROL RLSA Target ID] | Die eindeutige ID, die ein vorhandenes RLSA-Ziel oder einen Ausschluss auf Kampagnen- oder Anzeigengruppenebene identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie das Ziel oder den Ausschluss ändern oder löschen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL Device Target ID] | <p>Die eindeutige ID, die ein vorhandenes Ziel oder einen Ausschluss eines Geräts auf Kampagnenebene oder Anzeigengruppenebene identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie die Zielgruppe ändern oder löschen, es sei denn, die Zeile enthält eine &quot;[!UICONTROL AMO ID]&quot; für die Zielgruppe.</p> |
| [!UICONTROL AMO ID] | (In generierten Bulksheets) Eine von Adobe generierte eindeutige Kennung für eine synchronisierte Entität. Bei responsiven Suchanzeigen ist die AMO-ID erforderlich, um Anzeigen zu bearbeiten oder zu löschen, es sei denn, Sie beziehen die Anzeigen-ID ein. Um Daten für alle anderen Entitätstypen mit einer AMO-ID zu bearbeiten, muss die AMO-ID die Daten bearbeiten oder löschen, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |
| [!UICONTROL EF Error Message] | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Werbenetzwerk bezüglich Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL EF Errors] Dateien enthalten. Dieser Wert wird nicht an das Werbenetzwerk gesendet. |
| [!UICONTROL SE Error Message] | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Werbenetzwerk bezüglich Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL SE Errors] Dateien enthalten. Dieser Wert wird nicht an das Werbenetzwerk gesendet. |
| [!UICONTROL Exemption Request] | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige der Namen und des Textes aller [!DNL Google Ads] Werberichtlinien, gegen die eine Anzeige verstößt. |
| [!UICONTROL Retail Hash] | (Zu Informationszwecken in Bulksheets enthalten, die mit der erweiterten Kampagnenverwaltung generiert wurden) Ein alphanumerischer Hash-Code (wie z. B. f9639f40cdf56524b541e5dacf55a991), der angibt, dass das Element mit der erweiterten (ACM) Ansicht generiert wurde. |

[^1]: [!DNL Excel] konvertiert große Zahlen in wissenschaftliche Notation (z. B. 2.12E+09 für 2115585666), wenn er die Datei öffnet. Um Ziffern in der Standardnotation anzuzeigen, wählen Sie eine beliebige Zelle in der Spalte aus und klicken Sie in die Leiste Formel .

## Erforderliche Felder zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente {#bulksheet-fields-per-component-google}

Die folgenden Abschnitte enthalten die Felder, die für bestimmte Kontoentitäten relevant sind.

>[!NOTE]
>
>Wenn ein Feld nicht auf eine Aktion anwendbar ist, werden alle in das Feld eingegebenen Werte ignoriert.

### Kampagnenfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Campaign Budget] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Delivery Method] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Channel Type] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Networks] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL DSA Domain Name] | Erforderlich zum Erstellen einer Kampagne mit dynamischen Suchanzeigen im Suchnetzwerk. |
| [!UICONTROL DSA Domain Language] | Erforderlich zum Erstellen einer Kampagne mit dynamischen Suchanzeigen im Suchnetzwerk. |
| [!UICONTROL Campaign Priority] | Erforderlich zum Erstellen einer Shopping-Kampagne. |
| [!UICONTROL Has EU Political Ads] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Merchant ID] | Erforderlich zum Erstellen einer Shopping-Kampagne. |
| [!UICONTROL Sales Country] | Erforderlich zum Erstellen einer Shopping-Kampagne. |
| [!UICONTROL Product Scope Filter] | (Shopping-Kampagnen) Optional |
| [!UICONTROL Languages] | optional |
| [!UICONTROL Device Targets] | optional |
| [!UICONTROL Device Targets (Google Adwords)] | optional |
| [!UICONTROL Mobile Carriers (Google Adwords)] | optional |
| [!UICONTROL Audience Target Method] | Nicht zutreffend |
| [!UICONTROL Landing Page Suffix] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Campaign Status] | Nur zum Löschen einer Kampagne erforderlich. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Kampagne. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Anzeigengruppenfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Networks] | Nicht zutreffend |
| [!UICONTROL GDN Custom Bid Level] | optional |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Group Type] | Erforderlich zum Erstellen einer Anzeigengruppe. |
| [!UICONTROL Max CPC] | optional |
| [!UICONTROL Max Content CPC] | optional |
| [!UICONTROL Audience Target Method] | Erforderlich |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Ad Group Status] | Nur erforderlich, um eine Anzeigengruppe zu löschen. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Ad Group ID] | Nur erforderlich, wenn der Name der Anzeigengruppe geändert wird, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Anzeigengruppe. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Keyword-Felder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Max CPC] | optional |
| [!UICONTROL Keyword] | Erforderlich |
| [!UICONTROL Match Type] | Zum Bearbeiten oder Löschen eines Keywords mit mehreren Übereinstimmungstypen ist ein Wert für entweder den Übereinstimmungstyp oder die Keyword-ID erforderlich. |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Base URL/Final URL] | optional |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Param1] | optional |
| [!UICONTROL Param2] | optional |
| [!UICONTROL Keyword Status] | Nur erforderlich, um ein Keyword zu löschen. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Keyword ID] | Nur erforderlich, wenn Sie das Keyword bearbeiten oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung des Keywords oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Platzierungsfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Max Placement CPC (Google Adwords)] | optional |
| [!UICONTROL Max Placement CPM (Google Adwords)] | optional |
| [!UICONTROL Placement] | Erforderlich |
| [!UICONTROL Match Type] | Erforderlich |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Base URL/Final URL] | optional |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Placement Status] | Nur erforderlich, um eine Platzierung zu löschen. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Placement ID] | Nur erforderlich, wenn Sie die Platzierung bearbeiten oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung der Platzierung oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Erweiterte dynamische Suchanzeige

Dieser Anzeigentyp wird in [!DNL Google Ads] jetzt als „dynamische Suchanzeige“ bezeichnet. Weitere Informationen zum Erstellen dynamischer Suchanzeigen finden Sie unter &quot;[Implementieren [!DNL Google Ads] dynamischer Suchanzeigen](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html).

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot; im [!UICONTROL Download Bulksheet].

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Creative Preferred Devices] | optional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Erforderlich zum Erstellen einer Anzeige oder Bearbeiten der Beschreibung. <b>Hinweis:</b> Bei diesem Anzeigentyp wird durch Ändern der Anzeigenkopie die vorhandene Anzeige gelöscht und eine neue erstellt. |
| [!UICONTROL Display URL] | Erforderlich |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Creative Type] | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichend Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Produktlisten-/Shopping-Anzeigenfelder

Weitere Informationen zum Erstellen von Shopping-Anzeigen finden Sie unter [Implementieren [!DNL Google Ads] Shopping-Kampagnen](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html).

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot; im [!UICONTROL Download Bulksheet].

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Promotion Line] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Base URL/Final URL] | optional |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Creative Type] | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichend Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Responsive Suchanzeigenfelder

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Responsive Search Ad]&quot; im [!UICONTROL Download Bulksheet].

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | Für responsive Suchanzeigen sind [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] und [!UICONTROL Ad Title 3] erforderlich, um eine Anzeige zu erstellen. Alle anderen Felder für den Anzeigentitel sind optional. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | optional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Für responsive Suchanzeigen sind [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] erforderlich, um eine Anzeige zu erstellen. [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional. Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | optional |
| [!UICONTROL Display Path 1] | optional |
| [!UICONTROL Display Path 2] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Creative Type] | optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, Sie beziehen die Anzeigen-ID ein. |

### Text und Felder

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot; im [!UICONTROL Download Bulksheet].

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

>[!NOTE]
>
>Erweiterte Textanzeigen werden seit Juni 2022 nicht mehr unterstützt. Sie können nur vorhandene Textanzeigen löschen.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Creative Preferred Devices] | Schreibgeschützt |
| [!UICONTROL Ad Title], Anzeigentitel 2-3 | Schreibgeschützt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Schreibgeschützt |
| [!UICONTROL Display URL] | Schreibgeschützt |
| [!UICONTROL Display Path 1] | Schreibgeschützt |
| [!UICONTROL Display Path 2] | Schreibgeschützt |
| [!UICONTROL Tracking Template] | Schreibgeschützt |
| [!UICONTROL Base URL/Final URL] | Schreibgeschützt |
| [!UICONTROL Custom URL Param] | Schreibgeschützt |
| [!UICONTROL Creative Type] | optional |
| [!UICONTROL Ad Status] | Erforderlich |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a&rpar; genügend Anzeigeneigenschaftsspalten, um die Anzeige oder b&rpar; ein &quot;[!UICONTROL AMO ID]&quot; zu identifizieren. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Dynamische Target-Suche (automatisches Targeting)

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Max CPC] | optional |
| [!UICONTROL Auto Target Expression] | Nur erforderlich, wenn die Kampagneneinstellung auf [!UICONTROL Use my website contents to target my ads] nicht aktiviert ist. |
| [!UICONTROL Match Type] | optional |
| [!UICONTROL Target Status] | Erforderlich zum Löschen einer Zielgruppe |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Target ID] | Nur erforderlich, wenn Sie das automatische Targeting ändern oder löschen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Target. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Warenkorb-Produktgruppenfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Max CPC] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Parent Product Groupings] | Erforderlich |
| [!UICONTROL Product Grouping] | Erforderlich |
| [!UICONTROL Partition Type] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Match Type] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich |
| [!UICONTROL Product Group Status] | Nur erforderlich, um eine Produktgruppe zu löschen. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Product Group ID] | Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung der Produktgruppe oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Sitelink-Felder auf Kampagnenebene und Anzeigengruppenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich für Sitelinks auf Anzeigengruppenebene. Gilt nicht für Sitelinks auf Kampagnenebene. |
| [!UICONTROL Creative Preferred Devices] | optional |
| [!UICONTROL Link Name] | Erforderlich |
| [!UICONTROL Start Date] | optional |
| [!UICONTROL End Date] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich |
| [!UICONTROL Sitelink Status] | Nur zum Löschen eines Sitelinks erforderlich. |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Sitelink ID] | Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten, um den Sitelink zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] einbeziehen und die Eigenschaftsspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status für nur einen der Sitelinks.<br><br><b>Hinweis:</b> Wenn Sie die Eigenschaftsspalten eines Sitelinks mit Ausnahme [!UICONTROL Status] für einen vorhandenen Sitelink bearbeiten und weder den [!UICONTROL Sitelink ID] noch den [!UICONTROL AMO ID] einbeziehen, wird ein neuer Sitelink erstellt und der vorhandene Sitelink wird nicht geändert. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Ziel des Speicherorts

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Location] | Erforderlich |
| [!UICONTROL Location Type] | optional |
| [!UICONTROL Bid Adjustment] | optional |
| [!UICONTROL Location Status] | Nur erforderlich, um einen Zielspeicherort zu löschen. |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie schließen die [!UICONTROL Campaign ID] ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Gerätezielfelder auf Kampagnenebene und Anzeigengruppenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Device] | Erforderlich zum Erstellen oder Bearbeiten eines Zielgeräts. |
| [!UICONTROL Bid Adjustment] | optional |
| [!UICONTROL Ad Group Name] | Erforderlich für Geräte-Ziele auf Anzeigengruppenebene. Gilt nicht für Geräte-Ziele auf Kampagnenebene. |
| [!UICONTROL Device Target Status] | Nur erforderlich, um ein Zielgerät zu löschen. |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | Optional; gilt nur für Geräte-Ziele auf Anzeigengruppenebene. |
| [!UICONTROL Device Target ID] | Nur erforderlich, wenn das Ziel geändert oder gelöscht wird, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Geräte-Ziel-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### RLSA-Ziel-/Ausschlussfelder auf Kampagnenebene und Anzeigengruppenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Bid Adjustment] | optional |
| [!UICONTROL Ad Group Name] | Erforderlich für Ziele und Ausschlüsse auf Anzeigengruppenebene. Gilt nicht für Zielgruppen und Ausschlüsse auf Kampagnenebene. |
| [!UICONTROL Audience] | Erforderlich zum Erstellen einer neuen Zielgruppe oder eines neuen Ausschlusses. |
| [!UICONTROL Target Type] | Erforderlich zum Erstellen einer neuen Zielgruppe oder eines neuen Ausschlusses. |
| [!UICONTROL RLSA Target Status] | Nur erforderlich, um eine Zielgruppe oder einen Ausschluss zu löschen. |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | Optional; gilt nur für Ziele und Ausschlüsse auf Anzeigengruppenebene. |
| [!UICONTROL RLSA Target ID] | Nur erforderlich, wenn das Ziel geändert oder gelöscht wird, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die RLSA-Ziel-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

>[!MORELIKETHIS]
>
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Vorgänge, die Sie in Bulksheets ausführen können](bulksheet-operations.md)
>* [Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
>* [Klick-Tracking-Formate für [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Hochladen einer Bulksheet-Datei oder einer korrigierten Fehlerdatei](../bulksheet-upload.md)
