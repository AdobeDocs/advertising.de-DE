---
title: Erforderliche Bulksheet-Daten für [!DNL Google Ads] Konten
description: Referenzieren Sie die erforderlichen Kopfzeilenfelder und Datenfelder in Bulksheets für [!DNL Google Ads] Konten.
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '7855'
ht-degree: 0%

---

# Anhang - Erforderliche Bulksheet-Daten für [!DNL Google Ads]-Konten

Um [!DNL Google Ads] -Kampagnendaten stapelweise zu erstellen und zu aktualisieren, können Sie die Bulksheet-Dateien &quot;Search&quot;, &quot;Social&quot;und &quot;Commerce&quot;verwenden, die speziell für [!DNL Google Ads] -Konten formatiert sind. Sie können entweder a) [Massenblattdateien für vorhandene Konten generieren](../bulksheet-download.md) im erforderlichen Dateiformat oder b) sie manuell erstellen (allgemeine Informationen zu den unterstützten Dateiformaten finden Sie unter &quot;[Unterstützte Massendateiformate für Massenblätter](bulksheet-file-formats.md)&quot;).

Jedes Bulksheet muss die Kopfzeilenfelder und die entsprechenden Datenfelder enthalten, die für die [spezifischen Vorgänge, die Sie ausführen möchten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (z. B. das Erstellen einer Anzeige) erforderlich sind. Wenn ein Feld nicht erforderlich ist, können Sie es aus der Kopfzeile und den Datenzeilen auslassen. Alle benutzerdefinierten Spalten werden beim Hochladen der Bulk-Sheet-Datei gelöscht.

Im Folgenden finden Sie eine Tabelle aller verfügbaren Datenfelder und zusätzliche Tabellen, die angeben, welche Felder zum Hinzufügen, Bearbeiten oder Löschen von Daten für einzelne Entitäten (z. B. Kampagnen und Suchbegriffe) erforderlich sind.

## Alle verfügbaren Datenfelder {#bulksheet-fields-all-google}

In der folgenden Tabelle werden alle verfügbaren Datenfelder beschrieben.

Informationen zu den Datenfeldern, die für Kontoentitäten relevant sind, finden Sie unter &quot;[Felder, die zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente erforderlich sind](#bulksheet-fields-per-component-google)&quot;.

>[!NOTE]
>
>* Bei den Werten in allen Textspalten wird zwischen Groß- und Kleinschreibung unterschieden.
>* Wenn Sie einen neuen Datensatz erstellen und keine Werte für alle erforderlichen Datenfelder einschließen, werden einigen dieser Felder die angegebenen Standardwerte zugewiesen.
>* Für Felder, die unten nicht angegeben sind, wird der Standardwert für das Werbenetzwerk verwendet.
>* Eine Liste der verfügbaren Bulksheet-Zeilen im Dialogfeld [!UICONTROL Download Bulksheet] finden Sie unter &quot;[Bulksheet-Zeilen nach Anzeigennetzwerk](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network)&quot;.

| Feld | Beschreibung |
| ---- | ---- |
| [!UICONTROL Platform] | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Acct Name] | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| [!UICONTROL Campaign Budget] | Eine tägliche Ausgabenbegrenzung für die Kampagne mit oder ohne monetäre Symbole und Satzzeichen. Dieser Wert setzt das Kontobudget außer Kraft. |
| [!UICONTROL Delivery Method] | <p>Wie schnell zeigen Sie Anzeigen für die Kampagne jeden Tag an:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (Standard für neue Kampagnen): Um Ihre Anzeigenimpressionen über den Tag zu verteilen.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (Veraltet im Oktober 2019) So zeigen Sie Ihre Anzeigen so oft wie möglich an, bis Ihr Budget erreicht ist. Daher werden Ihre Anzeigen möglicherweise nicht später am Tag angezeigt.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>Die Kanäle, auf denen Anzeigen platziert werden sollen. Legen Sie eine oder mehrere Optionen fest:</p><ul><li><p><i>[!UICONTROL Search]</i> (Standardeinstellung für neue Kampagnen): Zum Platzieren von Anzeigen im [!DNL Google Ads] Suchnetzwerk (einschließlich [!DNL Google Ads] Such- und Suchpartner-Websites) und optional auch im [!DNL Google Ads] Display-Netzwerk. <b>Hinweis:</b> Kampagnen, die sowohl auf das Suchnetzwerk als auch auf das Display-Netzwerk abzielen, können nicht zu einem Portfolio zur Angebotsoptimierung hinzugefügt werden.</p></li><li><p><i>[!UICONTROL Display]</i>: Um Anzeigen nur im Anzeigenetzwerk [!DNL Google Ads] zu platzieren.</p></li><li><p><i>[!UICONTROL Shopping]</i>: Zum Platzieren von Shopping-Anzeigen im [!DNL Google Ads] -Einkaufsnetzwerk (in ausgewählten Ländern) und im [!DNL Google Ads] Suchnetzwerk (einschließlich [!DNL Google Ads] Such- und Suchpartner-Websites). Um Shopping-Anzeigen zu erstellen, müssen Sie über Produkte in einem [!DNL Google Merchant Center] -Konto verfügen und [erlauben Sie Search, Social und Commerce, Daten aus dem Konto herunterzuladen](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Weitere Informationen zum Erstellen von Shopping-Anzeigen finden Sie unter &quot;[Implementieren [!DNL Google Ads] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot;.</p></li></ul> |
| [!UICONTROL Networks] | <p>Ort, an dem Anzeigen platziert werden. Legen Sie eine oder mehrere Optionen fest:</p><ul><li><p><i>[!UICONTROL Google Search]</i>: Sponsored Search listings nur im Google Search Network.</p></li><li><p><i>[!UICONTROL Search Partners]</i>: Sponsored Search listings auf Googles Suchpartnern.</p></li><li><p><i>[!UICONTROL Content]</i>: Zum Platzieren von Angeboten für Display-Netzwerklisten.</p></li><li><p><i>[!UICONTROL All]</i> (Standardeinstellung für neue Kampagnen): Targets Google Search, Search Partners und Content.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Nur Suchnetzwerk; nur für erweiterte dynamische Suchanzeigen verfügbar) Die Stammdomäne (z. B. example.com) oder Subdomäne (z. B. shoes.example.com) der Website, deren Inhalt das Werbenetzwerk verwendet, um Ihre dynamischen Suchanzeigen auszuwählen.<br><br><b>Notizen:</b></p><ul><li><p>Erweiterte dynamische Suchanzeigen zielen auf den Inhalt der Website und nicht auf Suchbegriffe ab.</p></li><li><p>Ihre Domäne muss durch den organischen Suchindex des Werbenetzwerks indiziert sein, damit Targeting erfolgt.</p></li><li><p>Wenn Sie keine Domäne angeben, müssen Sie dynamische Suchziele erstellen, die für jede Anzeigengruppe entweder alle Seiten Ihrer Website oder eine Untergruppe davon abrufen.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Nur Suchnetzwerk; nur für erweiterte dynamische Suchanzeigen verfügbar) Die Sprache für die angegebene Website-Domäne. <b>Hinweis:</b> Wenn die Domäne Seiten in mehreren Sprachen enthält und Sie alle Zielgruppen auswählen möchten, erstellen Sie für jede Sprache eine separate Kampagne. |
| [!UICONTROL GDN Custom Bid Level] | (Kampagnen, die nur auf das Display-Netzwerk abzielen) Angebotsmethode: von <i>[!UICONTROL Ad Group]</i> (Standard), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (Website) oder <i>[!UICONTROL None]</i> (um den vorhandenen Wert zurückzusetzen). Andere Dimensionen (<i>Alter</i>, <i>Geschlecht</i>, <i>Interesse und Liste</i>, <i>Thema</i> und <i>Vertikal</i>) sind über die Benutzeroberfläche [!DNL Google Ads] verfügbar. Wenn Sie die Oberfläche [!DNL Google Ads] verwendet haben, um Gebote durch eine andere Dimension zu konfigurieren, wird dieser Wert angezeigt, aber Sie können diese Dimensionen hier nicht auswählen oder eingeben.</p><p><b>Hinweis:</b></p><ul><li><p>Erstellen Sie beim Gebot nach Keyword Tracking-Vorlagen auf Suchbegriffebene. Erstellen Sie auf ähnliche Weise Tracking-Vorlagen, wenn Sie ein Angebot nach Platzierung unterbreiten. Erstellen Sie für alle anderen Dimensionen Tracking-Vorlagen auf Anzeigenebene.</p></li><li><p>Wenn Sie ein Gebot nach einer nicht unterstützten Dimension (Alter, Geschlecht, Interessen und Liste oder Thema) senden, optimiert Search, Social und Commerce keine Gebote für die Dimension und alle Zuordnungen werden auf die Anzeigengruppe angewendet.</p></li><li><p>Anzeigen im Suchnetzwerk verwenden immer Suchbegriffangebote.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Nur Shopping-Kampagnen) Die Priorität, mit der die Kampagne verwendet wird, wenn mehrere Kampagnen für dasselbe Produkt werben: <i>[!UICONTROL Low]</i> (Standard für neue Kampagnen), <i>[!UICONTROL Medium]</i> oder <i>[!UICONTROL High]</i>.</p><p>Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Werbenetzwerk zuerst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und welches zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt. |
| [!UICONTROL Merchant ID] | (Nur Shopping-Kampagnen und Zielgruppenkampagnen, die mit einem Händler-Feed verknüpft sind) Die Kunden-ID des Händlers-Kontos, dessen Produkte für die Kampagne verwendet werden. |  |
| [!UICONTROL Sales Country] | (Nur Shopping-Kampagnen; schreibgeschützt für bestehende Kampagnen) Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden. |
| [!UICONTROL Product Scope Filter] | (Nur Kampagnen, die das [!DNL Google Ads] -Einkaufsnetzwerk verwenden) Die Produkte in Ihrem [!DNL Google Merchant Center]-Konto, für die für die Kampagne Shopping-Anzeigen erstellt werden können. Sie können bis zu sieben Produktdimensionen- und Attributkombinationen eingeben, nach denen Ihre Produkte gefiltert werden sollen. Verwenden Sie dazu das Attribut format dimension=attribute . Trennen Sie mehrere Filter mit einem &quot;>>&quot;-Trennzeichen. Eine Liste der verfügbaren Produktdimensionen finden Sie unter &quot;[Produktfilter für Shopping-Kampagnen](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;.</p><p>Beispiel: &quot;CategoryL1=animal>>CategoryL2=pet materials>>Brand=Acme Pet Supplies&quot;</p><p>Löschen Sie die vorhandenen Werte mit dem Wert <code>[delete]</code> (einschließlich der Klammern).</p> |
| [!UICONTROL Languages] | <p>(Nur Such- und Display-Netzwerke) Die Zielsprachen für Anzeigen in der Kampagne.</p><p>Wenn Sie keinen Wert für dieses Feld oder für das Feld [!UICONTROL Geo Targeting] für eine neue Kampagne eingeben, bestimmt die für das Konto angegebene Währung die Standardsprachen. Der Unterschied besteht darin, dass Kampagnen mit Währungen, die nicht bestimmten Sprachen zugeordnet sind (z. B. EUR), auf alle Sprachen ausgerichtet sind. Wenn Sie für dieses Feld keinen Wert eingeben, aber im Feld [!UICONTROL Geo Targeting] für eine neue Kampagne einen Wert eingeben, wird standardmäßig <i>[!UICONTROL All]</i> verwendet. Wenn Sie dieses Feld für eine bestehende Kampagne leer lassen, wird der vorhandene Wert beibehalten.</p><p>Geben Sie <span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span> ein, um alle Sprachen als Ziel festzulegen. Geben Sie für bestimmte Sprachen durch Semikolons getrennte Werte entweder mit <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] Sprachnamen</a> (z. B. <i>Englisch;Japanisch</i>, die durch die richtigen numerischen Codes ersetzt werden) oder mit numerischen Codes (z. B. <i>1000;1005</i>) ein. Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.</p> |
| [!UICONTROL Location] | Ein geografischer Ort, an dem Anzeigen für die Kampagne platziert oder für den Anzeigen ausgeschlossen werden sollen. Wenn Sie bei einer neuen Kampagne weder Werte für dieses Feld noch für das Feld Sprachen eingeben, bestimmt die für das Konto angegebene Währung die Standardspeicherorte. Der Unterschied besteht darin, dass Kampagnen mit Währungen, die nicht bestimmten Positionen zugeordnet sind (z. B. EUR), auf alle Standorte ausgerichtet sind. Wenn Sie für dieses Feld keinen Wert eingeben, aber für eine neue Kampagne im Feld [!UICONTROL Languages] einen Wert eingeben, wird standardmäßig <i>[!UICONTROL All]</i> verwendet. Wenn Sie dieses Feld für eine bestehende Kampagne leer lassen, wird der vorhandene Wert beibehalten.</p><p>Verwenden Sie einen der folgenden [[!DNL Google Ads] Ortsnamen](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (die durch den richtigen numerischen Code ersetzt werden) oder Ortungscodes, um einen bestimmten Ort als Ziel auszuwählen:</p><ul><li><p>Länder/Gebiete: Geben Sie die Namen des Landes/Gebiets (z. B. <i>Vereinigte Staaten;Japan</i>) oder die numerischen Codes (z. B. <i>2840;2392</i>) ein.</p></li><li><p>Bundesländer/Provinzen/Regionen: Geben Sie die Namen des Bundeslandes/der Provinz/Region mit den entsprechenden Abkürzungen für Land/Gebiet (z. B. <i>Tokyo, JP;New York, US</i>) oder die numerischen Codes (z. B. <i>20636;21167</i>) ein.</p></li><li><p>Nicht-amerikanische Städte: Geben Sie den Namen der Stadt, des Bundeslandes/der Region sowie die Abkürzungen für Land/Gebiet (z. B. <i>Adachi, Tokyo, JP;Kita, Tokyo, JP</i>) oder die numerischen Codes (z. B. <i>1028850;1009293</i>) ein.</p></li><li><p>U-Bahnbereiche in den USA: Geben Sie die Namen der Städte, Bundesländer und Landesabkürzungen (z. B. <i>Buffalo NY, US;New York NY, US</i>) oder die numerischen Codes (z. B. <i>514;501</i>) ein.</p></li></ul><p>Um einen Ort auszuschließen, müssen Sie dem Ortsnamen oder dem Code ein Minuszeichen (`-`) voranstellen, z. B. <i>-Japan</i>.</p><p><b>Hinweis:</b> Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.</p> |
| [!UICONTROL Location Type] | (Wenn Sie einen Ort einschließen) Der [Positionstyp](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Ein Gerätetyp, für den Angebotsanpassungen auf Kampagnen- oder Anzeigengruppenebene vorgenommen werden: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> oder <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(Wenn Sie ein Ziel [!UICONTROL Location], [!UICONTROL Device] oder [!UICONTROL RLSA] einschließen) Gibt an, ob Angebote für Anzeigen an einem bestimmten Ort, auf einem bestimmten Gerätetyp oder mit einem bestimmten Zielgruppen-Ziel angepasst werden sollen:</p><ul><li><p>Geben Sie 0 ein, um das Angebot auf Suchbegriffebene (0 % Differenz) zu verwenden. Bei neuen Zielgruppen können Sie dies auch leer lassen.</p></li><li><p>Um ein anderes Angebot für diese Zielgruppe zu verwenden, geben Sie den Prozentsatz ein, um den die Angebote erhöht oder reduziert werden sollen.</p></li><ul><li><p>Für Standort- und RLSA-Ziele sind gültige Prozentsätze zwischen -90 und 900.</p></li><li><p>Für Gerätegebotsanpassungen umfassen gültige Prozentsätze Folgendes:</p></li><ul><li><p>(Kampagnen)-100 (kein Gebot für Anzeigen des Gerätetyps) oder von -90 bis 900.</p></li><li><p>(Anzeigengruppen) -100 für Smartphones und Tablets (um kein Gebot für den Gerätetyp zu erhalten) und von -90 bis 900 für alle Gerätetypen.</p></li></ul></ul><li><p>(Vorhandene Kampagnen und Anzeigengruppen) Lassen Sie diese leer, um die vorhandene Angebotsanpassung zu verwenden.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (In generierten Bulksheets für Informationszwecke enthalten) Die schreibgeschützte Angebotsanpassung, die von Adobe für das Standortziel auf Kampagnenebene oder eine RLSA empfohlen wird. Sie wird nur berechnet, wenn sich die Kampagne in einem Portfolio mit einem Ziel befindet, das gewichtete Konversionsmetriken verwendet (nicht das Ziel [!UICONTROL Maximize Clicks] ), und die Kampagne mindestens zwei Standortziele oder RLSAs mit mindestens fünf Klicks oder Kosten von 5 USD in den letzten 90 Tagen enthält.</p><p>Wenn Sie ein Standortziel oder RLSA zur Verwendung des empfohlenen Werts manuell bearbeiten möchten, warten Sie mindestens zwei Wochen nach der Erstellung des Standortziels oder RLSA, um eine ausreichende Datenerfassung zu ermöglichen, und ändern Sie den Wert nicht öfter als einmal pro Woche. |
| [!UICONTROL Device Targets] | <p>(Nur ältere Kampagnentypen) Die Geräte, auf denen die Anzeige angezeigt werden kann: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> oder <i>[!UICONTROL Tablets]</i>. Für neue Kampagnen ist der Standardwert <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Nur ältere Kampagnentypen; anwendbar, wenn die Geräteziele &quot;Smartphones&quot;oder &quot;Tablets&quot;enthalten) Die Betriebssysteme, unter denen die Anzeige angezeigt werden kann: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> oder <i>[!UICONTROL Palm]</i>. Für neue Kampagnen ist der Standardwert <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Nur ältere Kampagnentypen; anwendbar, wenn [!UICONTROL Device Targets] &quot;[!UICONTROL All]&quot; oder &quot;[!UICONTROL Smartphones]&quot; enthält) Mobilnetzbetreiber, mit denen die Smartphones verbunden sein können: <i>[!UICONTROL All]</i> oder ein oder mehrere Netzbetreiber, angegeben durch &lt;c<i>Betreibercode</i>>,&lt;<i>Ländercode</i>> (z. B. T-Mobile,US), wobei die Liste mit <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">verfügbaren Netzbetreibern und Codes für [!DNL Google Ads]</a> verwendet wird. Trennen Sie mehrere Netzbetreiber mit Semikolons (z. B. T-Mobile,US;T-Mobile,GB). Für neue Kampagnen ist der Standardwert <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>Der eindeutige Name, der eine Anzeigengruppe identifiziert. Die maximale Länge beträgt 255 Zeichen. Nachfolgende leere Zeichen werden nicht gespeichert (z. B. wird &quot;Anzeigengruppe 1 &quot;als &quot;Anzeigengruppe 1&quot;gespeichert). Dieses Feld gilt nicht für Sitelinks auf Kampagnenebene oder Geräteziele auf Kampagnenebene.</p> |
| [!UICONTROL Ad Group Type] | <p>Der Anzeigengruppentyp: <i>[!UICONTROL Discovery]</i> (nur für Erkennungskampagnen), <i>[!UICONTROL Display]</i> (für Display-Kampagnen), <i>[!UICONTROL Search Dynamic]</i> (für erweiterte dynamische Suchanzeigen), <i>[!UICONTROL Search Standard]</i> (für Suchanzeigen), <i>[!UICONTROL Shopping Product]</i> (für Shopping-Produktanzeigen), <i>[!UICONTROL Shopping Showcase]</i> (Erstellung und Bearbeitung werden nicht unterstützt) oder <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Nur CPC-Kampagnen) Die maximalen Kosten pro Klick (CPC), wobei es sich um den höchsten Betrag handelt, der für einen Klick auf die Werbeanzeige im Werbenetzwerk mit oder ohne monetäre Symbole und Interpunktion bezahlt wird. Sie können Werte für Anzeigengruppen und Suchbegriffe, Produktgruppen und dynamische Suchziele festlegen. Die Standardeinstellung für einen neuen Suchbegriff wird von der Anzeigengruppenebene übernommen. Für Produktgruppen können Sie Werte für die niedrigste Produktgruppenebene festlegen. Der Standardwert für eine neue Ebene wird von der übergeordneten Ebene übernommen.</p><p>Für bestehende Produktgruppen und dynamische Suchziele in optimierten Portfolios sind Aktualisierungen nur für einen Tag wirksam und werden während des nächsten Optimierungszyklus überschrieben.</p> |
| [!UICONTROL Max Content CPC] | <p>(Nur CPC-Kampagnen) Die maximalen Inhaltskosten pro Klick (CPC), der höchste Betrag, der für einen Klick auf eine Display-Netzwerkseite mit oder ohne monetäre Symbole und Interpunktion bezahlt wird. Sie können Werte auf Anzeigengruppenebene in Kampagnen festlegen und bearbeiten, die nicht platzierungszielgerichtet sind.</p> |
| [!UICONTROL Audience Target Method] | <p>(Kampagnen, die sich nur auf das Suchnetzwerk beziehen, sowie bestehende schreibgeschützte [!DNL Gmail] Kampagnen im Anzeigenetzwerk) Ob:</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>: So zeigen Sie Anzeigen nur Benutzern an, die mit Zielgruppen verknüpft sind, die auch andere Ziele für die Anzeigengruppe erfüllen.</p></li><li><p><i>[!UICONTROL Bid Only]</i>: So zeigen Sie Anzeigen auch Personen an, die nicht mit Zielgruppen verbunden sind, solange sie andere Ziele auf Anzeigengruppenebene erfüllen.</p><p>Sie können die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie jedoch höhere Angebote für diese Zielgruppen festlegen.</p></li></ul> |
| [!UICONTROL Keyword] | Die Suchbegriff-Zeichenfolge. Die maximale Länge beträgt 80 Zeichen und höchstens 10 Wörter. Sie darf nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: Leerzeichen `# $ & _ - " [ ] ' + . / :`</p><p><b>Hinweis:</b></p><ul><li><p>Um einen Suchbegriff auf Anzeigengruppen- oder Kampagnenebene auszuschließen, setzen Sie [!UICONTROL Match Type] auf <i>[!UICONTROL Negative]</i>. Wenn die Zeile den Anzeigengruppennamen enthält, wird der Suchbegriff für die Anzeigengruppe ausgeschlossen. Wenn die Zeile nicht den Anzeigengruppennamen enthält, wird der Suchbegriff für die gesamte Kampagne ausgeschlossen.</p></li><li><p>Wenn Sie ein [!DNL Google Ads] -Keyword oder einen Übereinstimmungstyp ändern, wird der vorhandene Suchbegriff gelöscht und ein neuer erstellt.</p></li></ul> |
| [!UICONTROL Placement] | (Nur Kampagnen, die Inhalte verwenden, stimmen überein) Eine Platzierung im Display-Netzwerk, in der Ihre Anzeigen angezeigt werden können. Geben Sie eine der folgenden Optionen an:</p><ul><li><p>Website: Geben Sie eine gültige URL ein. Es kann sich um eine Domäne der obersten Ebene, eine Subdomäne der ersten Ebene oder eine Domäne mit einem einzigen Ordnernamen handeln. Die URL darf kein Fragezeichen (?) enthalten. Beispiele:<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>Eine Anzeigenposition auf einer bestimmten Seite: Verwenden Sie das Format `<URL> >> <location,sublocation>` (z. B. `finance.google.com >> Company pages,Top right`).</p></li><li><p>Eine Themenkategorie: Verwenden Sie die Syntax `<category::<category> > <subcategory>` usw. (z. B. `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Hinweis:</b> Setzen Sie die [!UICONTROL Match Type] auf <i>[!UICONTROL Negative]</i>, um eine Platzierung auf Anzeigengruppen- oder Kampagnenebene auszuschließen. Wenn die Zeile den Anzeigengruppennamen enthält, wird die Platzierung für die Anzeigengruppe ausgeschlossen. Wenn die Zeile nicht den Anzeigengruppennamen enthält, wird die Platzierung für die gesamte Kampagne ausgeschlossen.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Erforderlich, wenn die Kampagneneinstellung auf &quot;[!UICONTROL Use my website contents to target my ads]&quot; nicht aktiviert ist; andernfalls optional) Dynamische Suchziele für die Anzeigengruppe.</p><p>Verwenden Sie für alle Ziele ein Sternchen (*).</p><p>Um bis zu drei dynamische Suchkriterien als Ziel festzulegen, verwenden Sie das Format `<category>=<target>`, wobei `<category>` eine der folgenden Kategorien enthalten kann. Verknüpfen Sie mehrere Ziele für eine einzelne Kategorie mit &quot;\[Leerraum\] und \[Leerraum\]&quot;und fügen Sie mehrere Kategorien mit &quot;[Leerraum]&quot;und &quot;[Leerraum]&quot;ein.</p><ul><li><p><i>[!UICONTROL Category]</i>: So zeigen Sie erweiterte dynamische Suchanzeigen für indizierte Seiten mit einer bestimmten [!DNL Google Ads] Inhaltskategorie an.</p></li><li><p><i>[!UICONTROL URL]</i>: So zeigen Sie erweiterte dynamische Suchanzeigen für indizierte Seiten mit einer bestimmten URL an, wo der Wert an einer beliebigen Stelle in der URL enthalten sein kann.</p></li><li><p><i>[!UICONTROL Page Title]</i>: So zeigen Sie erweiterte dynamische Suchanzeigen für indizierte Seiten mit spezifischem Text im Seitentitel an.</p></li><li><p><i>[!UICONTROL Page Content]</i>: So zeigen Sie erweiterte dynamische Suchanzeigen für indizierte Seiten mit bestimmten Inhalten an.</p></li></ul><p>Beispiel: url=shoes.example.com und page title=Schuhe</p> |
| [!UICONTROL Parent Product Groupings] | Die Hierarchie der übergeordneten Produktgruppen.<br><br>Beispiel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>Die Produktgruppe (z. B. &quot;brand=acme&quot;oder &quot;Alle Produkte&quot;).</p><p><b>Hinweis:</b></p><ul><li><p>Wenn eine bestimmte Produktgruppe nicht in der [!UICONTROL Parent Product Groupings]-Hierarchie vorhanden ist, erstellt Search, Social und Commerce alle erforderlichen Teile der Hierarchie.</p></li><li><p>Search, Social und Commerce erstellen automatisch eine &quot;[!UICONTROL All Products]&quot;-Gruppe, wenn Sie eine Anzeigengruppe in einer [!DNL Google Ads] Shopping-Kampagne erstellen, deren Standardangebot auf das Standardgebot der Anzeigengruppe eingestellt ist. Search, Social und Commerce erstellen automatisch eine &quot;[!UICONTROL Everything Else]&quot;-Gruppe mit dem Standardangebot für Anzeigengruppen auf jeder Ebene der Produktgruppenhierarchie. Sie können diese Standardgruppen auch explizit erstellen und entweder ausschließen oder ihre Angebote ändern.</p></li><li><p>Jede Anzeigengruppe kann bis zu acht Stufen von Produktgruppen enthalten, darunter &quot;[!UICONTROL All Products]&quot;und sieben weitere Stufen.</p></li></ul> |
| [!UICONTROL Partition Type] | Der Partitionstyp für die Produktgruppe: <i>Unterteilung</i> (wenn sie untergeordnete Produktgruppen hat) oder <i>Einheit</i> (wenn sie keine untergeordneten Produktgruppen hat). |
| [!UICONTROL Match Type] | <p>Für dynamische Suchzielgruppen oder Produktgruppen: Die Suchbegriffabgleichoption für das dynamische Suchziel oder die dynamische Produktgruppe: <i>[!UICONTROL Dynamic Ad Target]</i> (Standard für neue dynamische Suchziele), <i>[!UICONTROL Product Group]</i> (Standard für neue Produktgruppen) oder <i>[!UICONTROL Negative Product Group]</i> (Ausschluss einer Produktgruppe).</p><p>Für Suchbegriffe: Die Suchbegriffabgleichoption für den Suchbegriff: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> oder <i>[!UICONTROL Negative]</i> (um einen Suchbegriff oder eine Platzierung im Display-Netzwerk auszuschließen); Produktgruppen, die mit Shopping-Anzeigen verwendet werden, haben den Übereinstimmungstyp <i>[!UICONTROL Product Group]</i>. Wenn Sie <i>[!UICONTROL Negative]</i> verwenden, müssen Sie auch den Übereinstimmungstyp einbeziehen, der ausgeschlossen werden soll (z. B. &quot;Negative Wortgruppe&quot;).</p><p>Bei neuen Suchbegriffen ist der Standardwert <i>[!UICONTROL Broad]</i>. Ein Wert für den Übereinstimmungstyp oder die Keyword-ID ist nur erforderlich, um einen Suchbegriff mit mehreren Übereinstimmungstypen zu bearbeiten.</p><p><b>Hinweis:</b></p><ul><li><p>Übereinstimmungstypen gelten nicht für erweiterte dynamische Suchanzeigen, die keine Suchbegriffe verwenden.</p></li><li><p>Wenn Sie den Übereinstimmungstyp für ein [!DNL Google Ads] -Keyword ändern, wird der vorhandene Keyword gelöscht und ein neuer erstellt.</p></li><li><p>Wählen Sie für Modifikator für breite Übereinstimmung &quot;Weit gefasst&quot;aus und fügen Sie ein &quot;+&quot;vor einem beliebigen Wort innerhalb des Suchbegriffs ein, für das enge Varianten erforderlich sind (z. B. &quot;+red +shoes&quot;, um enge Varianten von &quot;red&quot;und &quot;shoes&quot;zu erfordern). <b>Hinweis:</b> Weit gefasste Modifikatoren für Übereinstimmungen weisen jetzt dasselbe Verhalten auf wie eine Wortgruppenübereinstimmung für einige Sprachen, und Sie können seit Juli 2021 keine neuen Suchbegriffe für Modifikatoren für breite Übereinstimmung erstellen. Weitere Informationen finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/7042511) .</p> |
| [!UICONTROL First Page Bid] | (In generierten Bulksheets für Informationszwecke enthalten) Das Gebot, das erforderlich ist, um eine Anzeige auf der ersten Seite der Suchergebnisse zu platzieren. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |
| [!UICONTROL Quality Score] | (Zu Informationszwecken in generierten Bulksheets enthalten) Der aktuelle Qualitätswert, den die Suchmaschine dem Suchbegriff zugewiesen hat. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht.) |
| [!UICONTROL Creative Preferred Devices] | (Textanzeigen, erweiterte dynamische Suchanzeigen und erweiterte Sitelinks; optional) Die Gerätetypen, auf denen die Anzeige angezeigt werden soll: <i>[!UICONTROL All]</i> (Standard) oder <i>[!UICONTROL Mobile]</i>. Wenn <i>[!UICONTROL Mobile]</i> angegeben ist, versucht das Netzwerk, die Anzeige für Benutzer mobiler Geräte und nicht für Desktop- oder Tablet-Benutzer anzuzeigen. Andernfalls zeigt das Netzwerk die Anzeige auf einem beliebigen Gerätetyp an.</p><p><b>Hinweis:</b></p><ul><li><p>Diese Einstellung kann nur von Administratoren und Benutzern des [!DNL Adobe] -Kontomanagers bearbeitet werden.</p></li><li><p>Das Netzwerk garantiert nicht, dass die Anzeige auf dem bevorzugten Gerätetyp angezeigt wird.</p></li><li><p>Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Nur erweiterte Textanzeigen und responsive Suchanzeigen) Die Überschriften einer Anzeige, jeweils durch einen senkrechten Strich (&amp;vert;) getrennt. Die maximale Länge für jedes Feld mit Anzeigentitel beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen, einschließlich dynamischer Texte (wie die Werte von Suchbegriffen und Anzeigenanpassungen).</p><p>Für responsive Suchanzeigen sind [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] und [!UICONTROL Ad Title 3] erforderlich und alle anderen Felder für den Anzeigentitel sind optional. Verwenden Sie zum Löschen des vorhandenen Werts für ein nicht erforderliches Feld den Wert <code>[delete]</code> (einschließlich der Klammern).</p><p>Fügen Sie für responsive Suchanzeigen einen Anzeigenanpasser im folgenden Format ein: <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, z. B. <code>{CUSTOMIZER.discount:10%}</code></p><p>Sie können keine Textanzeigen erstellen oder bearbeiten, aber Sie können erweiterte Textanzeigen löschen, die im Juni 2022 von [!DNL Google Ads] eingestellt wurden. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Nur responsive Suchanzeigen; optional) Eine Position, an der der entsprechende Anzeigentitel veröffentlicht werden soll: `[null]` (kein Wert, der den Anzeigentitel für alle Positionen infrage stellt), <i>1</i>, <i>2</i> oder <i>3</i>. Wenn beispielsweise [!UICONTROL Ad Title Position] den Wert 1 hat, wird der Anzeigentitel nur in Position 1 angezeigt. Standardmäßig sind alle Anzeigentitel null (haben keine Werte).</p><p>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert <code>[delete]</code> (einschließlich der Klammern).</p><p><b>Hinweis:</b> Sie können mehrere Anzeigentitel an derselben Position veröffentlichen. Das Anzeigennetzwerk verwendet einen der Anzeigentitel, die an die Position veröffentlicht sind. Titel, die an Position 3 gekoppelt sind, können nicht mit der Anzeige angezeigt werden.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Nur erweiterte dynamische Suchanzeigen, erweiterte Textanzeigen und responsive Suchanzeigen) Der Hauptteil einer Anzeige. Die maximale Länge für jedes Beschreibungsfeld beträgt 90 Zeichen oder 45 Doppelbyte-Zeichen, einschließlich dynamischer Texte (wie die Werte von Keywords und Anzeigenanpassungen).</p><p>Fügen Sie für responsive Suchanzeigen einen Anzeigenanpasser im folgenden Format ein: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, z. B. `{CUSTOMIZER.Discount:10%}`</p><p>Verwenden Sie für erweiterte dynamische Suchanzeigen nur [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2]. <b>Hinweis:</b> Bei diesem Anzeigentyp wird durch Ändern der Anzeigenkopie die vorhandene Anzeige gelöscht und eine neue erstellt.</p><p>Sie können keine Textanzeigen erstellen oder bearbeiten, aber Sie können erweiterte Textanzeigen löschen, die im Juni 2022 von [!DNL Google Ads] eingestellt wurden.</p><p>Für responsive Suchanzeigen sind [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] erforderlich und [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] optional. Um den vorhandenen Wert zu löschen, verwenden Sie den Wert <code>[delete]</code> (einschließlich der Klammern).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Nur responsive Suchanzeigen; optional) Eine Position, an der die entsprechende Beschreibung veröffentlicht werden soll: `[null]` (kein Wert, der die Beschreibung für alle Positionen infrage stellt), <i>1</i>, <i>2</i> oder <i>3</i>. Wenn beispielsweise [!UICONTROL Description 1 Position] den Wert 1 hat, wird [!UICONTROL Description 1] nur in Position 1 angezeigt. Standardmäßig werden keine Beschreibungen an eine Position veröffentlicht.</p><p>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).</p><p><b>Hinweis:</b> Sie können mehrere Beschreibungen an derselben Position veröffentlichen. Das Anzeigennetzwerk verwendet eine der Beschreibungen, die an die Position gebunden sind. In Position 2 enthaltene Beschreibungen werden möglicherweise nicht zusammen mit der Anzeige angezeigt. |
| [!UICONTROL Display URL] | Die in der Anzeige enthaltene URL.<br><br>Für erweiterte dynamische Suchanzeigen generiert [!DNL Google Ads] diesen Wert dynamisch aus der Website-Domäne und Sie müssen keinen Wert eingeben.<br><br>Für responsive Suchanzeigen müssen Sie keinen Wert eingeben. Die Anzeigen-URL wird automatisch aus der Domäne in der endgültigen URL extrahiert. Optional können Sie die URL mithilfe der Felder Pfad 1 und Pfad 2 anpassen.<br><br>Sie können keine Textanzeigen erstellen oder bearbeiten, aber Sie können erweiterte Textanzeigen löschen, die im Juni 2022 von [!DNL Google Ads] nicht mehr unterstützt wurden.<br><br><b>Hinweis:</b> (Konten mit finalen URLs) Die Domänennamen in der Anzeigen-URL und der endgültigen URL müssen übereinstimmen.</p> |
| [!UICONTROL Display Path 1] | <p>(Nur erweiterte Textanzeigen<span> und responsive Suchanzeigen</span>)</p><p>(Optional) Text, der der Anzeigen-URL hinzugefügt wird, die automatisch aus der endgültigen URL extrahiert wird. Der URL wird ein Schrägstrich (/) vorangestellt. Ein Pfad darf keine Schrägstriche (/) oder Zeilenumbruchzeichen (\n) enthalten. Die maximale Länge beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.</p><p>Verwenden Sie zum Einfügen eines Anzeigenanpassers die folgenden Formate, wobei `Default text` ein optionaler Wert ist, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält:&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`</p><p>Wenn beispielsweise [!UICONTROL Display Path 1] &quot;Angebote&quot;ist, ist die Anzeige-URL &lt;<i>Anzeigen-URL</i>>/Angebote, z. B. www.example.com/deals.</p><p>Sie können keine Textanzeigen erstellen oder bearbeiten, aber Sie können erweiterte Textanzeigen löschen, die im Juni 2022 von [!DNL Google Ads] eingestellt wurden.</p> |
| [!UICONTROL Display Path 2] | Ein zweiter Anzeigepfad; siehe den Eintrag für [!UICONTROL Display Path 1].<br><br>Beispiel: Wenn [!UICONTROL Display Path 1] &quot;Angebote&quot;und [!UICONTROL Display Path 2] &quot;lokal&quot;ist, ist die Anzeige-URL &lt;<i>Anzeigen-URL</i>>/Angebote/lokal, z. B. www.example.com/deals/local.</p><p>Sie können keine Textanzeigen erstellen oder bearbeiten, aber Sie können erweiterte Textanzeigen löschen, die im Juni 2022 von [!DNL Google Ads] eingestellt wurden.</p> |
| [!UICONTROL Promotion Line] | (Nur Produktanzeigen) Eine optionale Promotion-Zeile, die in die Produktliste in den Suchergebnissen aufgenommen werden soll. Die maximale Länge beträgt 45 Zeichen.</p><p>Die Promotion-Zeile kann an verschiedenen Stellen relativ zur Anzeige angezeigt werden (z. B. unter der Anzeige), je nachdem, wo die Anzeige auf der Seite erscheint. |
| [!UICONTROL Link Name] | <p>Der Sitelink-Text. Er kann bis zu 25 Zeichen enthalten.</p><p>Bei neuen Sitelinks müssen Sie den Kampagnennamen in die Sitelink-Zeile aufnehmen. Bei Sitelinks auf Anzeigengruppenebene müssen Sie auch den Anzeigengruppennamen angeben.</p><p><b>Hinweis:</b> Der vorhandene Text von 35 Zeichen wird weiterhin in Anzeigen auf Desktops und Tablets angezeigt, jedoch nicht auf Mobilgeräten.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Nur vorhandene Anzeigen zur App-Installation) Das Betriebssystem, auf dem die Mobile App ausgeführt wird: <i>Android™</i> oder <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Nur vorhandene App-Installationsanzeigen) <p>Die Anwendungs-ID oder der Paketname. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Nur vorhandene App-Installationsanzeigen) Der Name der Anwendung. |
| [!UICONTROL Start Date] | <p>(Nur erweiterte Sitelinks) Das erste Datum, an dem Gebote für den Sitelink in der Zeitzone des Werbetreibenden und in einem der folgenden Formate platziert werden können: <i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i> oder <i>m-d-yy</i>. Die Standardeinstellung für neue erweiterte Sitelinks ist der aktuelle Tag.</p><p><b>Hinweis:</b> Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden.</p> |
| [!UICONTROL End Date] | <p>(Nur erweiterte Sitelinks) Das letzte Datum, an dem Angebote für den Sitelink in der Zeitzone des Werbetreibenden und in einem der folgenden Formate platziert werden können:  <i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i> oder <i>m-d-yy</i>. Der Standardwert ist &quot;none&quot;(kein Enddatum).</p><p><b>Hinweis:</b> Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Nur vorhandene App-Installationsanzeigen)</p><p>(Optional) Verhindert, dass [!DNL Google Ads] die Anzeige für Tablet-Benutzer anzeigt. Die Werte können <i>yes</i> und <i>no</i> enthalten. |
| [!UICONTROL Landing Page Suffix] | Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen. Beispiel: `param2=value1&param3=value2`<br><br>Siehe &quot;[Klick-Tracking-Formate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)&quot;.<br><br>Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Verwenden Sie den Editor [!DNL Google Ads] , um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren. |
| [!UICONTROL Tracking Template] | Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen [!DNL ValueTrack] -Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als granularsten) überschreibt die Werte auf allen höheren Ebenen.<br><br>Für das Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, hängt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode an.<br><br>Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein. Eine Liste der Parameter [!DNL ValueTrack] zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in den Parametern &quot;Nur Tracking-Vorlage&quot;im Abschnitt &quot;Verfügbare [!DNL ValueTrack] Parameter&quot;in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/2375447).<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Base URL/Final URL] | Die Landingpage-URL, auf die Suchmaschinenbenutzer beim Klicken auf Ihre Anzeige zugreifen, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter. Basis-/endgültige URLs auf Suchbegriffebene überschreiben diese auf Anzeigenebene und höher.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Destination URL] | (In generierten Bulksheets zu Informationszwecken enthalten; nicht bei der Suchmaschine veröffentlicht) Bei Konten mit Ziel-URLs ist dies die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Advertisers verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Er enthält alle für die Kampagne oder das Konto &quot;Search, Social und Commerce&quot;konfigurierten Anlagenparameter. Wenn Sie Tracking-URLs generiert haben, basiert dies auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie suchmaschinenspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Search, Social und Commerce ersetzt werden.<br><br>Bei Konten mit finalen URLs zeigt diese Spalte denselben Wert wie die Spalte Basis-URL/Endgültige URL an. |
| [!UICONTROL Custom URL Param] | Daten, die die dynamische Variable `{custom_code}` ersetzen sollen, wenn die Variable in den Tracking-Parametern für das Suchkonto oder die Kampagneneinstellungen enthalten ist. Um den benutzerdefinierten Wert in die Tracking-URL einzufügen, müssen Sie die Bulksheet-Datei mit der Option Tracking-URLs generieren hochladen. |
| [!UICONTROL Creative Type] | Das Anzeigenformat: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (nicht mehr unterstützt), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (nicht mehr unterstützt), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (Shopping-Anzeigen) oder <i>[!UICONTROL Responsive search ad]</i>. Der Standardwert für neue Anzeigen ist <i>[!UICONTROL Text ad]</i>.<br><br>Erforderlich, um den Status einer Produktanzeige zu erstellen oder zu bearbeiten. |
| [!UICONTROL Param1] | <p>Der numerische Wert des Anzeigenparameters `{param1}` , der in die Anzeigen-Copy- oder Anzeigen-URL für jede Anzeige in der Bulksheet-Datei aufgenommen werden kann. Die maximale Länge beträgt 25 Zeichen. Folgende nicht numerische Zeichen sind zulässig:</p><ul><li><p>Dem Wert kann ein Währungssymbol oder ein Währungscode vorangestellt oder angehängt werden. Beispielsweise sind `£2.000,00` und `2000GBP` gültig.</p></li><li><p>Der Wert kann ein Komma (`,`) oder einen Punkt (`.`) als Trennzeichen mit einem optionalen Punkt (`.`) oder ein Komma (`,`) für Bruchwerte enthalten. Beispielsweise sind `1,000.00` und `2.000,10` gültig.</p></li><li><p>Dem Wert kann ein Prozentzeichen (`%`), ein Pluszeichen (`+`) oder ein Minuszeichen (`- `) vorangestellt oder angehängt werden. Beispielsweise sind `20%`, `208+` und `-42.32` gültig.</p></li><li><p>Zwei Zahlen können mit einem Schrägstrich eingebettet werden. Beispielsweise sind `4/1` und `0.95/0.45` gültig.</p></li></ul><p>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).</p> |
| [!UICONTROL Param2] | Der numerische Wert des Anzeigenparameters `{param2}` , der in die Anzeigen-Copy- oder Anzeigen-URL für jede Anzeige in der Bulksheet-Datei aufgenommen werden kann. Weitere Informationen finden Sie im Eintrag für Param1 . |
| [!UICONTROL Audience] | Die Remarketing-Liste für Suchanzeigen (RLSA) dient der Zielgruppe oder der ausgeschlossenen Zielgruppe für die Kampagne oder Anzeigengruppe. Geben Sie im Feld &quot;Zieltyp&quot;an, ob es sich um eine Zielgruppe oder einen Ausschluss handelt. |
| [!UICONTROL Target Type] | (Wenn eine Zielgruppe angegeben wird) Gibt an, ob die angegebene Zielgruppe eine <i>Aufnahme</i> (Ziel) oder ein <i>Ausschluss</i> ist. |
| [!UICONTROL Campaign Status] | Der Anzeigestatus der Kampagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (nicht bearbeitbar) oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Kampagnen). Der Standardwert für neue Kampagnen ist <i>[!UICONTROL Active]</i>. Um eine aktive oder ausgesetzte Kampagne zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Ad Group Status] | Der Anzeigestatus der Anzeigengruppe: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur bestehende Anzeigengruppen). Der Standardwert für neue Anzeigengruppen ist [!UICONTROL Active]. Um eine aktive oder ausgesetzte Anzeigengruppe zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Keyword Status] | Der Anzeigestatus des Keywords: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Keywords). Der Standardwert für neue Suchbegriffe ist [!UICONTROL Active]. Um einen aktiven oder ausgesetzten Suchbegriff zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Ad Status] | Der Anzeigestatus der Anzeige: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigen), <i>[!UICONTROL Disapproved]</i> (nicht bearbeitbar) oder <i>[!UICONTROL Paused]</i>. Der Standardwert für neue Anzeigen ist [!UICONTROL Active]. Um eine aktive oder ausgesetzte Anzeige zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Placement Status] | Der Status der Website-Platzierung: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigen). Die Standardeinstellung für neue Websites ist <i>Aktiv.</i> Um eine aktive oder angehaltene Platzierung zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Target Status] | Der Status eines dynamischen Suchziels: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Ziele). Der Standardwert für neue Ziele ist <i>Aktiv.</i> Um ein aktives oder ausgesetztes Ziel zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Product Group Status] | Der Anzeigestatus der Produktgruppe: <i>[!UICONTROL Active]</i> <span>oder</span> <i>[!UICONTROL Deleted]</i> (nur bestehende Produktgruppen). Der Standardwert für neue Produktgruppen ist <i>[!UICONTROL Active]</i>. Um eine aktive Produktgruppe zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Sitelink Status] | Der Anzeigestatus des Sitelinks: <i>Aktiv oder Gelöscht</i> (nur vorhandene Sitelinks). Die Standardeinstellung für neue Sitelinks ist <i>[!UICONTROL Active]</i>. Um einen aktiven Sitelink zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Location Status] | Der Status des Ortungsziels: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Orte). Der Standardwert für neue Speicherorte ist [!UICONTROL Active]. Um einen aktiven Ort zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL RLSA Target Status] | Der Status des RLSA-Ziels oder Ausschlusses auf Kampagnen- oder Anzeigengruppenebene: <i>[!UICONTROL Active]</i> oder [!UICONTROL Deleted]</i> (nur vorhandene Ziele). Der Standardwert für neue Ziele oder Ausschlüsse ist <i>[!UICONTROL Active]</i>. Um eine aktive Zielgruppe oder einen Ausschluss zu löschen, geben Sie den Wert <i>[!UICONTROL Deleted]</i> ein. |
| [!UICONTROL Device Target Status] | <p>Der Status des Geräteziels auf Kampagnen- oder Anzeigengruppenebene: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i>. Für neue Kampagnen und Anzeigengruppen ist der Standardwert <i>[!UICONTROL Active]</i>.</p> |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | (Benannt für eine Advertiser-spezifische Beschriftungs-Classification, z. B. &quot;Farbe&quot;für eine Beschriftungsklassifizierung namens &quot;Farbe&quot;) Ein Wert für die angegebene Classification, die mit der Entität verknüpft ist. Sie können pro Entität nur einen Wert angeben (z. B. &quot;rot&quot;für die Klassifizierung der Farbbeschriftung für Kampagne A). Die maximale Länge beträgt 100 Zeichen. Der Wert kann ASCII- und Nicht-ASCII-Zeichen enthalten.<br><br>Beschriftungsklassifizierungen und ihre Beschriftungswerte werden auf alle untergeordneten Komponenten angewendet. Neue Komponenten, die später hinzugefügt werden, werden automatisch mit der Beschriftung verknüpft. Beschriftungsklassifizierungen für Produktgruppen werden auf die Einheitenebene (am detailliertesten) angewendet.<br><br>Weder der Classification-Name noch der Classification-Wert unterscheiden zwischen Groß- und Kleinschreibung. |
| [!UICONTROL Constraints] | Eine Beschränkung, die der Entität zugewiesen wird. Sie können pro Entität nur eine Begrenzung zuweisen.<br><b>>Begrenzungen werden von untergeordneten Entitäten übernommen, sodass Sie keine Werte für untergeordnete Entitäten eingeben müssen, es sei denn, Sie möchten die vererbten Werte überschreiben. |
| [!UICONTROL Campaign ID] | Die eindeutige ID, die eine bestehende Kampagne identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Kampagne. |
| [!UICONTROL Ad Group ID] | Die eindeutige ID, die eine bestehende Anzeigengruppe identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Anzeigengruppe. |
| [!UICONTROL Keyword ID] | Die eindeutige ID, die einen vorhandenen Suchbegriff identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Suchbegriff ändern, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Suchbegriff zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Ad ID] | <p>Die eindeutige ID, die eine vorhandene Anzeige identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Für responsive Suchanzeigen ist entweder die Anzeigen-ID oder die AMO-ID erforderlich, um Anzeigendaten zu bearbeiten oder zu löschen. Bei allen anderen Entitätstypen ist die Anzeigen-ID nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einschließen und die Spalten der Anzeigeneigenschaft mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen.</p><p><b>Hinweis:</b> Wenn Sie a) Anzeigeneigenschaftsspalten bearbeiten, außer Status für eine vorhandene Anzeige oder b) Daten für eine responsive Suchanzeige, und Sie weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einschließen, wird eine neue Anzeige erstellt und die vorhandene Anzeige wird nicht geändert.</p> |
| [!UICONTROL Placement ID] | Die eindeutige ID, die die Platzierung einer Website identifiziert. Erforderlich nur, wenn Sie die Platzierung ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um die Platzierung zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Target ID] | Die eindeutige ID, die ein vorhandenes automatisches Ziel identifiziert. Nur erforderlich, wenn Sie das automatische Ziel ändern oder löschen, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL Product Group ID] | Die eindeutige ID, die eine bestehende Produktgruppe identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichende Eigenschaftsspalten, um die Produktgruppe zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Sitelink ID] | Die eindeutige ID, die einen vorhandenen Sitelink identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichende Eigenschaftsspalten, um den Sitelink zu identifizieren, oder b) einen &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] einschließen und die Eigenschaftenspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status nur für einen der Sitelinks.</p><p><b>Hinweis: </b> Wenn Sie die Sitelink-Eigenschaftsspalten bearbeiten, mit Ausnahme des Status für einen vorhandenen Sitelink, und Sie weder den [!UICONTROL Sitelink ID] noch den [!UICONTROL AMO ID] einschließen, wird ein neuer Sitelink erstellt und der vorhandene Sitelink wird nicht geändert. |
| [!UICONTROL RLSA Target ID] | Die eindeutige ID, die ein vorhandenes RLSA-Ziel oder einen Ausschluss auf Kampagnen- oder Anzeigengruppenebene identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie das Ziel oder den Ausschluss ändern oder löschen, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL Device Target ID] | <p>Die eindeutige ID, die ein vorhandenes Geräteziel oder -ausschluss auf Kampagnen- oder Anzeigengruppenebene identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie das Ziel ändern oder löschen, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für das Ziel.</p> |
| [!UICONTROL AMO ID] | (In generierten Bulksheets) Eine von Adobe generierte eindeutige Kennung für eine synchronisierte Entität. Bei responsiven Suchanzeigen ist die AMO-ID zum Bearbeiten oder Löschen von Anzeigen erforderlich, es sei denn, Sie enthalten die Anzeigen-ID. Um Daten für alle anderen Entitätstypen mit AMO-ID zu bearbeiten, muss die AMO-ID die Daten bearbeiten oder löschen, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |
| [!UICONTROL EF Error Message] | (In generierten Bulksheets für Informationszwecke enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Anzeigennetzwerk bezüglich Daten in der Zeile; Fehlermeldungen werden in [!UICONTROL EF Errors] -Dateien eingeschlossen. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |
| [!UICONTROL SE Error Message] | (In generierten Bulksheets für Informationszwecke enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Anzeigennetzwerk bezüglich Daten in der Zeile; Fehlermeldungen werden in [!UICONTROL SE Errors] -Dateien eingeschlossen. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |
| [!UICONTROL Exemption Request] | (Einschließlich in generierten Bulksheets für Informationszwecke) Platzhalter für die Anzeige der Namen und des Texts von [!DNL Google Ads] Werberichtlinien, die eine Anzeige verletzt. |
| [!UICONTROL Retail Hash] | (Zu Informationszwecken in mit dem erweiterten Campaign Management generierten Bulksheets enthalten) Ein alphanumerischer Hash-Code (z. B. f9639f40cdf56524b541e5dacf55a991), der anzeigt, dass das Element mithilfe der Erweiterten (ACM) Ansicht generiert wurde. |

[^1]: [!DNL Excel] konvertiert große Zahlen in wissenschaftliche Notation (z. B. 2.12E+09 für 2115585666), wenn die Datei geöffnet wird. Um Ziffern in der Standardnotation anzuzeigen, wählen Sie eine beliebige Zelle in der Spalte aus und klicken Sie in die Formelleiste.

## Felder, die zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente erforderlich sind {#bulksheet-fields-per-component-google}

Die folgenden Abschnitte enthalten die Felder, die für bestimmte Kontoentitäten relevant sind.

>[!NOTE]
>
>Wenn ein Feld nicht auf eine Aktion anwendbar ist, werden alle im Feld eingegebenen Werte ignoriert.

### Kampagnenfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Campaign Budget] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Delivery Method] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Channel Type] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Networks] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL DSA Domain Name] | Erforderlich, um eine Kampagne mit dynamischen Suchanzeigen im Suchnetzwerk zu erstellen. |
| [!UICONTROL DSA Domain Language] | Erforderlich, um eine Kampagne mit dynamischen Suchanzeigen im Suchnetzwerk zu erstellen. |
| [!UICONTROL Campaign Priority] | Erforderlich zum Erstellen einer Warenkampagne. |
| [!UICONTROL Merchant ID] | Erforderlich zum Erstellen einer Warenkampagne. |
| [!UICONTROL Sales Country] | Erforderlich zum Erstellen einer Warenkampagne. |
| [!UICONTROL Product Scope Filter] | (Shopping-Kampagnen) Optional |
| [!UICONTROL Languages] | Optional |
| [!UICONTROL Device Targets] | Optional |
| [!UICONTROL Device Targets (Google Adwords)] | Optional |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Optional |
| [!UICONTROL Audience Target Method] | Nicht zutreffend |
| [!UICONTROL Landing Page Suffix] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Campaign Status] | Nur zum Löschen einer Kampagne erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Kampagne. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Anzeigengruppenfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Networks] | Nicht zutreffend |
| [!UICONTROL GDN Custom Bid Level] | Optional |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Group Type] | Erforderlich zum Erstellen einer Anzeigengruppe. |
| [!UICONTROL Max CPC] | Optional |
| [!UICONTROL Max Content CPC] | Optional |
| [!UICONTROL Audience Target Method] | Erforderlich |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Ad Group Status] | Nur zum Löschen einer Anzeigengruppe erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Ad Group ID] | Nur erforderlich, wenn Sie den Anzeigengruppennamen ändern, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Anzeigengruppe. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Suchbegriffsfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Max CPC] | Optional |
| [!UICONTROL Keyword] | Erforderlich |
| [!UICONTROL Match Type] | Zum Bearbeiten oder Löschen eines Suchbegriffs mit mehreren Übereinstimmungstypen ist ein Wert für den Übereinstimmungstyp oder die Keyword-ID erforderlich. |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Param1] | Optional |
| [!UICONTROL Param2] | Optional |
| [!UICONTROL Keyword Status] | Nur zum Löschen eines Suchbegriffs erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Keyword ID] | Nur erforderlich, wenn Sie den Suchbegriff bearbeiten oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Suchbegriff zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Platzierungsfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Max Placement CPC (Google Adwords)] | Optional |
| [!UICONTROL Max Placement CPM (Google Adwords)] | Optional |
| [!UICONTROL Placement] | Erforderlich |
| [!UICONTROL Match Type] | Erforderlich |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Placement Status] | Nur zum Löschen einer Platzierung erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Placement ID] | Erforderlich nur, wenn Sie die Platzierung bearbeiten oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um die Platzierung zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Erweiterte dynamische Suchanzeige

Dieser Anzeigentyp wird jetzt in [!DNL Google Ads] als &quot;dynamische Suchanzeige&quot;bezeichnet. Weitere Informationen zum Erstellen dynamischer Suchanzeigen finden Sie unter &quot;[Implementieren [!DNL Google Ads] dynamischer Suchanzeigen](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-dynamic-search-ads.html)&quot;.

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot;im Dialogfeld &quot;[!UICONTROL Download Bulksheet]&quot;.

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Creative Preferred Devices] | Optional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Erforderlich zum Erstellen einer Anzeige oder Bearbeiten der Beschreibung. <b>Hinweis:</b> Bei diesem Anzeigentyp wird durch Ändern der Anzeigenkopie die vorhandene Anzeige gelöscht und eine neue erstellt. |
| [!UICONTROL Display URL] | Erforderlich |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Creative Type] | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einschließen und die Spalten der Anzeigeneigenschaft mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Felder für Produktliste/Shopping-Anzeige

Weitere Informationen zum Erstellen von Shopping-Anzeigen finden Sie unter &quot;[Implementieren [!DNL Google Ads] Shopping-Kampagnen](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-shopping-campaigns.html)&quot;.

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot;im Dialogfeld &quot;[!UICONTROL Download Bulksheet]&quot;.

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Promotion Line] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Creative Type] | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einschließen und die Spalten der Anzeigeneigenschaft mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Responsive Suchanzeigenfelder

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Responsive Search Ad]&quot;im Dialogfeld &quot;[!UICONTROL Download Bulksheet]&quot;.

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | Für responsive Suchanzeigen sind [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] und [!UICONTROL Ad Title 3] erforderlich, um eine Anzeige zu erstellen, und alle anderen Felder für den Anzeigentitel sind optional. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Optional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Für responsive Suchanzeigen sind [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] erforderlich, um eine Anzeige zu erstellen, und [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional. Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Optional |
| [!UICONTROL Display Path 1] | Optional |
| [!UICONTROL Display Path 2] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Creative Type] | Optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, Sie enthalten die Anzeigen-ID. |

### Textanzeigenfelder

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot;im Dialogfeld &quot;[!UICONTROL Download Bulksheet]&quot;.

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

>[!NOTE]
>
>Erweiterte Textanzeigen wurden im Juni 2022 eingestellt. Sie können nur vorhandene Textanzeigen löschen.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Creative Preferred Devices] | Schreibgeschützt |
| [!UICONTROL Ad Title], Anzeigentitel 2-3 | Schreibgeschützt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Schreibgeschützt |
| [!UICONTROL Display URL] | Schreibgeschützt |
| [!UICONTROL Display Path 1] | Schreibgeschützt |
| [!UICONTROL Display Path 2] | Schreibgeschützt |
| [!UICONTROL Tracking Template] | Schreibgeschützt |
| [!UICONTROL Base URL/Final URL] | Schreibgeschützt |
| [!UICONTROL Custom URL Param] | Schreibgeschützt |
| [!UICONTROL Creative Type] | Optional |
| [!UICONTROL Ad Status] | Erforderlich |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einschließen und die Spalten der Anzeigeneigenschaft mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Felder für dynamisches Suchziel (automatisches Targeting)

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Max CPC] | Optional |
| [!UICONTROL Auto Target Expression] | Nur erforderlich, wenn die Kampagneneinstellung &quot;[!UICONTROL Use my website contents to target my ads]&quot; nicht aktiviert ist. |
| [!UICONTROL Match Type] | Optional |
| [!UICONTROL Target Status] | Löschen einer Zielgruppe erforderlich |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Target ID] | Nur erforderlich, wenn Sie das automatische Ziel ändern oder löschen, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Produktgruppenfelder kaufen

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Max CPC] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Parent Product Groupings] | Erforderlich |
| [!UICONTROL Product Grouping] | Erforderlich |
| [!UICONTROL Partition Type] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Match Type] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich |
| [!UICONTROL Product Group Status] | Nur zum Löschen einer Produktgruppe erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Product Group ID] | Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichende Eigenschaftsspalten, um die Produktgruppe zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Sitelink-Felder auf Kampagnenebene und Anzeigengruppenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich für Sitelinks auf Anzeigengruppenebene. Gilt nicht für Sitelinks auf Kampagnenebene. |
| [!UICONTROL Creative Preferred Devices] | Optional |
| [!UICONTROL Link Name] | Erforderlich |
| [!UICONTROL Start Date] | Optional |
| [!UICONTROL End Date] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich |
| [!UICONTROL Sitelink Status] | Nur zum Löschen eines Sitelink erforderlich. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Sitelink ID] | Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichende Eigenschaftsspalten, um den Sitelink zu identifizieren, oder b) einen &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] einschließen und die Eigenschaftsspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status nur für einen der Sitelinks.<br><br><b>Hinweis: </b> Wenn Sie die Sitelink-Eigenschaftsspalten mit Ausnahme von [!UICONTROL Status] für einen vorhandenen Sitelink bearbeiten und weder den [!UICONTROL Sitelink ID] noch den [!UICONTROL AMO ID] einschließen, wird ein neuer Sitelink erstellt und der vorhandene Sitelink wird nicht geändert. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Standort-Ziel

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Location] | Erforderlich |
| [!UICONTROL Location Type] | Optional |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Location Status] | Nur zum Löschen eines Orts-Ziels erforderlich. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL AMO ID] | Erforderlich, um die Daten zu bearbeiten oder zu löschen, es sei denn, Sie enthalten die [!UICONTROL Campaign ID].<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Zielfelder auf Kampagnenebene und auf Anzeigengruppenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Device] | Erforderlich zum Erstellen oder Bearbeiten eines Geräteziels. |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Ad Group Name] | Erforderlich für Geräteziele auf Anzeigengruppenebene. Gilt nicht für Geräteziele auf Kampagnenebene. |
| [!UICONTROL Device Target Status] | Nur zum Löschen eines Geräteziels erforderlich. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional. Gilt nur für Geräteziele auf Anzeigengruppenebene. |
| [!UICONTROL Device Target ID] | Nur erforderlich, wenn Sie das Ziel ändern oder löschen, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL AMO ID] | Erforderlich, um die Daten zu bearbeiten oder zu löschen, es sei denn, Sie enthalten die Geräteziel-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### RLSA-Zielgruppen-/Ausschlussfelder auf Kampagnenebene und Anzeigengruppenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-google)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Ad Group Name] | Erforderlich für Ziele und Ausschlüsse auf Anzeigengruppenebene. Gilt nicht für Ziele und Ausschlüsse auf Kampagnenebene. |
| [!UICONTROL Audience] | Erforderlich zum Erstellen einer neuen Zielgruppe oder eines neuen Ausschlusses. |
| [!UICONTROL Target Type] | Erforderlich zum Erstellen einer neuen Zielgruppe oder eines neuen Ausschlusses. |
| [!UICONTROL RLSA Target Status] | Nur zum Löschen einer Zielgruppe oder eines Ausschlusses erforderlich. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional. Gilt nur für Ziele und Ausschlüsse auf Anzeigengruppenebene. |
| [!UICONTROL RLSA Target ID] | Nur erforderlich, wenn Sie das Ziel ändern oder löschen, es sei denn, die Zeile enthält einen &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die RLSA-Target-ID.<br><br>Suche, Social und Commerce verwenden den Wert, um die richtige Identität zu bestimmen, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

>[!MORELIKETHIS]
>
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Vorgänge, die Sie in Bulksheets ausführen können](bulksheet-operations.md)
>* [Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)
>* [Herunterladen/Erstellen einer Bulksheet-Datei](../bulksheet-download.md)
>* [Klick-Tracking-Formate für  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Laden Sie eine Bulksheet-Datei oder eine korrigierte Fehlerdatei hoch](../bulksheet-upload.md)
