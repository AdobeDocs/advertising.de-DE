---
title: Erforderliche Bulksheet-Daten für [!DNL Microsoft Advertising] Konten
description: Referenzieren Sie die erforderlichen Kopfzeilenfelder und Datenfelder in Bulksheets für [!DNL Microsoft Advertising] Konten.
source-git-commit: 964ee8431d9f1d03b0c9eec8906ab5a0b7940222
workflow-type: tm+mt
source-wordcount: '7615'
ht-degree: 1%

---

# Anhang - Erforderliche Bulksheet-Daten für [!DNL Microsoft Advertising] Konten

So erstellen und aktualisieren Sie [!DNL Microsoft Advertising] Kampagnendaten stapelweise verwenden, können Sie Bulksheet-Dateien für Suche, Social und Commerce verwenden, die speziell für [!DNL Microsoft Advertising] Konten. Sie können entweder a) [Massenblatt-Dateien für bestehende Konten generieren](../bulksheet-download.md) im erforderlichen Dateiformat oder b) manuell erstellen (siehe[Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)&quot; allgemeine Informationen zu den unterstützten Dateiformaten).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## Alle verfügbaren Datenfelder

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Feld | Beschreibung |
|----|----|
| Plattform | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kontoname | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. Die maximale Länge beträgt 128 Zeichen. |
| Kampagnenbudget | Das tägliche oder monatliche Kampagnenbudget mit oder ohne monetäre Symbole und Satzzeichen. Es darf nicht weniger als 0,05 sein. |
| Kanaltyp | Der Typ des Kanals, auf den die Kampagne ausgerichtet ist: <i>Zielgruppe</i>, <i>DynamicSearchAds</i>, <i>Suche</i>oder <i>Shopping</i>. |
| Versandmethode | (Nur Kampagnen mit täglichem Budget) Wie schnell zeigen Sie Anzeigen für die Kampagne jeden Tag an:<ul><li><i>Standard (verteilt)</i> (Standardeinstellung für neue Kampagnen): So verbreiten Sie Ihre Anzeigenimpressionen über den Tag.</li><li><i>Accelerated:</i> Um Ihre Anzeigen so oft wie möglich anzuzeigen, bis Ihr Budget erreicht ist. Daher werden Ihre Anzeigen möglicherweise nicht später am Tag angezeigt.</li></ul> |
| Kampagnenpriorität | (Nur Shopping-Kampagnen) Die Priorität, mit der die Kampagne verwendet wird, wenn mehrere Kampagnen für dasselbe Produkt werben: <i>Niedrig</i> (Standardeinstellung für neue Kampagnen), <i>Mittel</i>oder <i>Hoch</i>.<br><br>Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Werbenetzwerk zuerst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und welches zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt. |
| Merchant-ID | (Nur Shopping-Kampagnen und Zielgruppenkampagnen, die mit einem Händler-Feed verknüpft sind) Die Kunden-ID des Händlers-Kontos, dessen Produkte für die Kampagne verwendet werden. |
| Vertriebsland | (Nur Shopping-Kampagnen; schreibgeschützt für bestehende Kampagnen) Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden. |
| Produktumfang-Filter | (Nur Kampagnen, die das Einkaufsnetzwerk verwenden) Die Produkte in Ihrem Händlerkonto, für die Produktanzeigen für die Kampagne erstellt werden können. Sie können bis zu sieben Produktdimensionen- und Attributkombinationen eingeben, nach denen Ihre Produkte gefiltert werden sollen. Verwenden Sie dazu das Attribut format dimension=attribute . Trennen Sie mehrere Filter mit einem &quot;>>&quot;-Trennzeichen. Eine Liste der verfügbaren Produktdimensionen finden Sie unter[Produktfilter für Shopping-Kampagnen](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Beispiel: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Um die vorhandenen Werte zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| DSA-Domänenname | (Kampagnen des Typs a) &quot;<i>DynamicSearchAds</i>&quot; oder b) &quot;<i>Suche</i>&quot;, wenn das Element ExperimentId nicht festgelegt ist) Der Domänenname der Website, auf die für dynamische Suchanzeigen abgezielt werden soll. Die maximale Länge beträgt 2.048 Zeichen. Wenn der Domänenname `www`, ist es abgeschnitten und nicht verwendet.<br><br>Bei vorhandenen Kampagnen können Sie die Domäne nicht bearbeiten, müssen sie jedoch einschließen, um andere Eigenschaften zu aktualisieren. |
| DSA-Domänensprache | (Kampagnen des Typs a) &quot;<i>DynamicSearchAds</i>&quot; oder b) &quot;<i>Suche</i>&quot;, wenn das Element ExperimentId nicht festgelegt ist) Die Sprache der Website-Seiten, die als Ziel für dynamische Suchanzeigen dienen sollen. Die unterstützten Domänennamen sind Niederländisch, Englisch, Französisch, Deutsch, Italienisch, Spanisch und Schwedisch.<br><br>Bei vorhandenen Kampagnen können Sie die Sprache nicht bearbeiten, müssen sie jedoch einbeziehen, um andere Eigenschaften zu aktualisieren. |
| Anzeigengruppenname | Der eindeutige Name, der eine Anzeigengruppe identifiziert. Die maximale Länge beträgt 128 Zeichen. Nachfolgende Leerzeichen werden nicht gespeichert (z. B. wird &quot;Anzeigengruppe 1&quot;als &quot;Anzeigengruppe 1&quot;gespeichert). |
| Anzeigengruppentyp | (Kampagnen im Suchnetz; schreibgeschützt für bestehende Anzeigengruppen) Der Anzeigengruppentyp: <i>Zielgruppe</i> (nur für Zielgruppenkampagnen), <i>Suchdynamik</i> (nur für dynamische Suchanzeigen) und <i>Search Standard</i> (nur für responsive Suchanzeigen und vorhandene erweiterte Textanzeigen). Einige Kampagnentypen können mehrere Anzeigengruppentypen umfassen. |
| Schlüsselwort | (Nur Kampagnen im Suchnetzwerk) Die Keyword-Zeichenfolge. Die maximale Länge beträgt 50 Zeichen.<br><br><b>Hinweise:</b><ul><li>Um einen Suchbegriff auf Anzeigengruppen- oder Kampagnenebene auszuschließen, setzen Sie den Übereinstimmungstyp auf `Negative`. Wenn die Zeile den Anzeigengruppennamen enthält, wird der Suchbegriff für die Anzeigengruppe ausgeschlossen. Wenn die Zeile nicht den Anzeigengruppennamen enthält, wird der Suchbegriff für die gesamte Kampagne ausgeschlossen.</li><li>Beim Ändern eines Microsoft Advertising-Suchbegriffs wird der vorhandene Suchbegriff gelöscht und ein neuer mit einer neuen Suchbegriff-ID erstellt. Beim Ändern des Übereinstimmungstyps wird jedoch der vorhandene Suchbegriff nicht gelöscht.</li></ul> |
| Platzierung | Veraltet |
| Zielgruppe | Die Remarketing-Liste für Suchanzeigen (RLSA)-Zielgruppe für die Kampagne oder Anzeigengruppe. |
| Zieltyp | (Nur RLSA) Der Zieltyp: <i>Einbindung</i> oder <i>Ausschluss</i>. |
| Ausdruck für automatisches Targeting | Dynamische Suchziele für die Anzeigengruppe. Verwenden Sie für alle Ziele &quot;Alle Webseiten&quot;.<br><br>Verwenden Sie das Format , um bis zu drei dynamische Suchkriterien als Ziel auszuwählen. `<category>=<target>`, wobei &lt;category> kann eine der folgenden Kategorien umfassen. Verknüpfen mehrerer Ziele für eine einzelne Kategorie mit &quot;`[blank space] and [blank space]`&quot; und fügen Sie mehrere Kategorien mit &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Kategorie:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit einer bestimmten Google-Inhaltskategorie an.</li><li><i>URL:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit einer bestimmten URL an, auf denen der Wert an einer beliebigen Stelle in der URL enthalten sein kann.</li><li><i>Seitentitel:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit spezifischem Text im Seitentitel an.</li><li><i>Seiteninhalt:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit bestimmten Inhalten an.</li></ul>Beispiel: url=shoes.example.com und page title=Schuhe<br>Beispiel: Alle Webseiten |
| Standort | Ein geografischer Ort, an dem Anzeigen für die Kampagne oder Anzeigengruppe platziert werden sollen; Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie keine Werte für die Kampagne oder Anzeigengruppe eingeben, werden alle Orte als Ziel ausgewählt. Um bestimmte Orte als Ziel festzulegen, geben Sie den Ort mithilfe der Codeformate für den Microsoft Advertising-Standort ein. Um eine Ortsliste herunterzuladen, melden Sie sich mit Ihren Anmeldedaten für das Microsoft Advertising-Werbekonto beim Entwicklerportal für Microsoft Advertising an. <b>Hinweis:</b> Um einen Ort auszuschließen, setzen Sie dem Ortscode ein Minuszeichen (`-`), z. B. `-United States`. |
| Location Type | Der Standorttyp, z. B. Stadt, Land, MetroArea, Postleitzahl und Bundesland. Um eine Ortsliste herunterzuladen, melden Sie sich mit Ihren Anmeldedaten für das Microsoft Advertising-Werbekonto beim Entwicklerportal für Microsoft Advertising an. |
| Übereinstimmungstyp | (Nur Kampagnen im Suchnetzwerk) Die Suchbegriffabgleichoption(en). Dies kann die Suchbegriffabgleichoption für ein dynamisches Suchziel oder eine Produktgruppe enthalten. Zu den Werten gehören: <i>Broad</i> (Standardeinstellung für neue Suchbegriffe), <i>Exakt</i>, <i>Satz</i>, <i>Inhalt</i> (Wird automatisch für Suchbegriffe festgelegt, wenn die Anzeigengruppe auf das Inhaltsnetzwerk ausgerichtet ist) <i>Negativ</i> (um einen Suchbegriff im Inhaltsnetzwerk auszuschließen), <i>Dynamic Ad Target</i> (Standardeinstellung für neue dynamische Suchziele), <i>Produktgruppe</i> (Standardeinstellung für neue Produktgruppen) oder <i>Negative Produktgruppe</i> (um eine Produktgruppe auszuschließen).  Zum Bearbeiten oder Löschen eines Suchbegriffs mit mehreren Übereinstimmungstypen ist ein Wert für den Übereinstimmungstyp oder die Keyword-ID erforderlich.<br><br>Wählen Sie für einen Modifikator für breite Übereinstimmung &quot;Weit gefasst&quot;und fügen Sie eine `+` vor einem beliebigen Wort innerhalb des erforderlichen Suchbegriffs (z. B. &quot;`+red +shoes`&quot;, um sowohl &quot;rot&quot; als auch &quot;Schuhe&quot; zu benötigen).<br><br>Wenn Sie den Übereinstimmungstyp für einen Microsoft Advertising-Suchbegriff ändern, wird der vorhandene Suchbegriff nicht gelöscht. |
| Max. CPC | (Kampagnen im Suchnetzwerk) Die maximalen Kosten pro Klick (CPC), d. h. der höchste zu zahlende Betrag für einen Klick auf eine Werbeanzeige basierend auf dem Suchbegriff, der Produktgruppe oder dem dynamischen Suchziel, mit oder ohne monetäre Symbole und Interpunktion.  Bei vorhandenen Suchbegriffen und Produktgruppen-Datensätzen in optimierten Portfolios sind Aktualisierungen nur für einen Tag wirksam und werden während des nächsten Optimierungszyklus überschrieben. <b>Hinweis:</b> Sie können keine Angebote für negative Suchbegriffe festlegen. |
| Max. Content-CPC | (Schreibgeschützt für CPC-Kampagnen, die vor der Einstellung des Inhaltsnetzwerks nur 2017 erstellt wurden) Die maximalen Inhaltskosten pro Klick (CPC), der höchste Betrag, der für einen Klick auf eine Display-Netzwerkseite mit oder ohne monetäre Symbole und Interpunktion zu zahlen ist. |
| Zielgruppenbestimmungsmethode | (Zielgruppen-Anzeigengruppen) Ob:<ul><li><i>Ziel und Angebot:</i> So zeigen Sie Anzeigen nur Benutzern an, die mit Zielgruppen verknüpft sind, die auch andere Ziele für die Anzeigengruppe erfüllen.</li><li><i>Nur Angebot:</i>Anzeigen auch für Personen anzeigen, die nicht mit Zielgruppen verbunden sind, solange sie andere Ziele auf Anzeigengruppenebene erfüllen.</li></ul> Sie können die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie jedoch höhere Angebote für diese Zielgruppen festlegen. |
| Übergeordnete Produktgruppen | Die Hierarchie der übergeordneten Produktgruppen.<br><br>Beispiel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| Produktgruppierung | Die Produktgruppe (z. B. &quot;brand=acme&quot;oder &quot;Alle Produkte&quot;).<br><br><b>Hinweise:</b><ul><li>Wenn eine bestimmte Produktgruppe nicht in der Hierarchie der übergeordneten Produktgruppen vorhanden ist, erstellt Search, Social und Commerce alle erforderlichen Teile der Hierarchie.</li><li>Search, Social und Commerce erstellt automatisch die Gruppe &quot;Alle Produkte&quot;, sobald Sie eine Anzeigengruppe in einer Google Shopping-Kampagne erstellen, deren Standardangebot auf das Standardgebot der Anzeigengruppe eingestellt ist. Search, Social und Commerce erstellt automatisch eine Gruppe &quot;Alles andere&quot;mit dem Standardangebot für Anzeigengruppen auf jeder Ebene der Produktgruppenhierarchie. Sie können diese Standardgruppen auch explizit erstellen und entweder ausschließen oder ihre Angebote ändern.</li><li>Jede Anzeigengruppe kann bis zu acht Stufen von Produktgruppen umfassen, darunter &quot;Alle Produkte&quot;und sieben weitere Stufen.</li></ul> |
| Partitionstyp | Der Partitionstyp für die Produktgruppe: <i>Unterteilung</i> (wenn es untergeordnete Produktgruppen hat) oder <i>Einheit</i> (wenn keine untergeordneten Produktgruppen vorhanden sind). |
| Anzeigentitel, Anzeigentitel 2-15 | (Nur erweiterte Textanzeigen, Multimedia-Anzeigen, responsive Anzeigen und responsive Suchanzeigen) Die Überschriften einer Anzeige. Die maximale Länge für jedes Feld mit Anzeigentitel beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen, einschließlich dynamischer Texte (z. B. die Werte von Keywords, `{Param2}` und `{Param3}` dynamische Ersatzvariablen und Anzeigenanpassungen).<br><br> Fügen Sie für responsive Suchanzeigen einen Anzeigenanpasser im folgenden Format ein, wobei &quot;Standardtext&quot;ein optionaler Wert ist, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Für erweiterte Textanzeigen sind Anzeigentitel und Anzeigentitel 2 erforderlich und Anzeigentitel 3 ist optional. Microsoft Advertising veraltete erweiterte Textanzeigen im August 2022. Sie können jetzt nur mehr Berichte zu diesen Werbeanzeigen erstellen und diese löschen.<br><br>Bei Multimedia-Anzeigen, responsiven Anzeigen und responsiven Suchanzeigen sind der Anzeigentitel, der Anzeigentitel 2 und der Anzeigentitel 3 erforderlich und alle anderen Felder für den Anzeigentitel sind optional.<br><br>Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).<br><br>Bei allen Anzeigentypen mit Ausnahme von erweiterten Textanzeigen löscht eine Änderung der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue Anzeige mit denselben Eigenschaften. |
| Position des Anzeigentitels 1-15 | (Nur responsive Suchanzeigen; optional) Eine Position, an der der entsprechende Anzeigentitel veröffentlicht werden soll: `[null]` (kein Wert, sodass der Anzeigentitel für alle Positionen infrage kommt), 1, 2 oder 3. Wenn beispielsweise die Anzeigentitelposition den Wert 1 hat, wird der Anzeigentitel nur in Position 1 angezeigt. Standardmäßig sind alle Anzeigentitel null (haben keine Werte). Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).<br><br><b>Hinweis:</b> Sie können mehrere Anzeigentitel an derselben Position veröffentlichen. Das Anzeigennetzwerk verwendet einen der Anzeigentitel, die an die Position gebunden sind. Titel, die an Position 3 gekoppelt sind, können nicht mit der Anzeige angezeigt werden. |
| Beschreibung Zeile 1-4 | (Nur Textanzeigen, dynamische Suchanzeigen, Multimedia-Anzeigen, responsive Suchanzeigen, responsive Suchanzeigen und erweiterte Sitelinks auf Kampagnenebene) Der Hauptteil einer Anzeige oder eines Sitelink.<br><br>Bei Sitelinks können Sie optional sowohl die Beschreibung Zeile 1 als auch die Beschreibung Zeile 2 verwenden, um zusätzlichen Text einzufügen, den das Werbenetzwerk unter dem Linktext anzeigen kann. Jedes Beschreibungsfeld kann bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.<br><br>Bei Anzeigen beträgt die maximale Länge für jedes Beschreibungsfeld 90 Zeichen oder 45 Doppelbyte-Zeichen, einschließlich dynamischer Texte (wie die Werte von Suchbegriffen und Anzeigenanpassungen).<br><br>Fügen Sie für responsive Suchanzeigen einen Anzeigenanpasser im folgenden Format ein, wobei Standardtext ein optionaler Wert ist, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Für Textanzeigen und dynamische Suchanzeigen ist die Beschreibung Zeile 1 erforderlich und die Beschreibung Zeile 2 ist optional.<br><br>Für Multimedia-Anzeigen, responsive Anzeigen und responsive Suchanzeigen sind Beschreibung Zeile 1 und Beschreibung Zeile 2 erforderlich und Beschreibung Zeile 3 und Beschreibung Zeile 4 sind optional.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).<br><br><b>Hinweise:</b><ul><li>(Standardtextanzeigen) Der kombinierte Titel und Text muss mindestens drei Wörter umfassen.</li><li>(Erweiterte Textanzeigen) Dieses Feld kann optional die {Param2} und {Param3} dynamische Ersatzvariablen. Ist dies der Fall, beträgt die maximale Länge des Anzeigentextes 300 Einzelbyte- oder 150 Doppelbyte-Zeichen. Microsoft Advertising veraltete erweiterte Textanzeigen im August 2022. Sie können jetzt nur mehr Berichte zu diesen Werbeanzeigen erstellen und diese löschen.</li><li>(Dynamische Suchanzeigen) Dynamischer Ersatztext ist nicht zulässig.</li><li>Bei allen Anzeigentypen außer erweiterten Textanzeigen löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue.</li></ul> |
| Beschreibung Zeile 1-4 Position | (Nur responsive Suchanzeigen; optional) Eine Position, an der die entsprechende Beschreibung veröffentlicht werden soll: `[null]` (kein Wert, sodass die Beschreibung für alle Positionen geeignet ist), 1, 2 oder 3. Wenn beispielsweise Beschreibung 1 Position den Wert 1 hat, wird Beschreibung 1 nur in Position 1 angezeigt. Standardmäßig werden keine Beschreibungen an eine Position veröffentlicht.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).<br><br><b>Hinweis:</b> Sie können mehrere Beschreibungen an derselben Position veröffentlichen. Das Werbenetzwerk verwendet eine der Beschreibungen, die an die Position gebunden sind. In Position 2 enthaltene Beschreibungen werden möglicherweise nicht zusammen mit der Anzeige angezeigt. |
| Geschäftsname | (Nur Multimedia-Anzeigen) Der Unternehmensname mit maximal 25 Zeichen. |
| Promotion Line | (Nur Produktlistenanzeigen) Eine eindeutige Promotion-Zeile, die in die Produktliste in den Suchergebnissen aufgenommen werden soll (z. B. &quot;Kostenloser Versand jetzt!&quot;). Die maximale Länge beträgt 45 Zeichen.<br><br>Die Promotion-Zeile kann an verschiedenen Stellen relativ zur Anzeige angezeigt werden (z. B. unter der Anzeige), je nachdem, wo die Anzeige auf der Seite erscheint. |
| URL anzeigen | Die in der Anzeige enthaltene URL.<br><br>Bei erweiterten dynamischen Suchanzeigen generiert das Werbenetzwerk diesen Wert dynamisch aus der Website-Domäne und Sie müssen keinen Wert eingeben.<br><br>Für erweiterte Textanzeigen und responsive Suchanzeigen müssen Sie keinen Wert eingeben. Die Anzeigen-URL wird automatisch aus der Domäne in der endgültigen URL extrahiert. Optional können Sie die URL mithilfe der Felder Pfad 1 und Pfad 2 anpassen.<br><br><b>Hinweise:</b><ul><li>(Konten mit finalen URLs) Die Domänennamen in der Anzeigen-URL und der endgültigen URL müssen übereinstimmen.</li><li>Microsoft Advertising veraltete erweiterte Textanzeigen im August 2022. Sie können jetzt nur mehr Berichte zu diesen Werbeanzeigen erstellen und diese löschen.</li></ul> |
| Anzeigepfad 1 | (Nur erweiterte Textanzeigen, dynamische Suchanzeigen und responsive Suchanzeigen) Text, der der Display-URL hinzugefügt wird, die automatisch aus der endgültigen URL extrahiert wird. Jeder Pfad wird in der URL durch einen Schrägstrich (/) vorangestellt. Ein Pfad darf keine Schrägstriche (/) oder Zeilenumbruchzeichen (\n) enthalten. Die maximale Länge für jeden Pfad beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.<br><br>Verwenden Sie zum Einfügen eines Anzeigenanpassers die folgenden Formate, wobei &quot;Standardtext&quot;ein optionaler Wert ist, der eingefügt werden kann, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`<br><br>Wenn der Anzeigepfad 1 beispielsweise &quot;Angebote&quot;lautet, lautet die Anzeigen-URL &lt;display url=&quot;&quot;>/transactions, z. B. www.example.com/deals.<br><br>Microsoft Advertising veraltete erweiterte Textanzeigen im August 2022. Sie können jetzt nur mehr Berichte zu diesen Werbeanzeigen erstellen und diese löschen. |
| Anzeigepfad 1 | (Nur erweiterte Textanzeigen, dynamische Suchanzeigen und responsive Suchanzeigen) Ein zusätzlicher Anzeigepfad; sehen Sie den Eintrag für Anzeigepfad 1.<br><br>Beispiel: Wenn der Anzeigepfad 1 &quot;Angebote&quot;und der Anzeigepfad 2 &quot;lokal&quot;ist, lautet die Anzeige-URL &lt;<i>Anzeigen-URL</i>>/transactions/local, z. B. www.example.com/deals/local. |
| Startdatum | (Nur erweiterte Sitelinks) Das erste Datum, an dem Angebote für den Sitelink in der Zeitzone des Werbetreibenden und in einem der folgenden Formate platziert werden können: m/d/yyy, m/d/yy, m-d-yyy oder m-d-yy. Die Standardeinstellung für neue erweiterte Sitelinks ist der aktuelle Tag. <b>Hinweis:</b> Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden. |
| Enddatum | Das letzte Datum, an dem der Sitelink mit Anzeigen in der Zeitzone des Advertisers und in einem der folgenden Formate angezeigt werden kann: m/d/yyy, m/d/yy, m-d-yyy oder m-d-yy. Bei einem neuen Sitelink ist die Standardeinstellung `[blank]` (d. h. kein Enddatum). |
| Aktionsaufruf | Der Aktionsaufruf, der in die Anzeige aufgenommen werden soll. Siehe [API-Referenz für eine Liste möglicher Werte](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), aber geben Sie Aktionsaufrufe mit mehreren Wörtern (z. B. &quot;Bet Now&quot;anstelle von &quot;BetNow&quot;) in Bulksheets ein. |
| Aktionssprache aufrufen | Die Sprache für die Aktionsoptionen. Siehe [API-Referenz für eine Liste möglicher Sprachen](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| Basis-URL/Endgültige URL | Die Landingpage-URL, auf die Suchmaschinenbenutzer beim Klicken auf Ihre Anzeige zugreifen, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter. Basis-/endgültige URLs auf Suchbegriffebene überschreiben diese auf Anzeigenebene und höher.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| Ziel-URL | (in generierten Bulksheets zu Informationszwecken enthalten; Bei Konten mit Ziel-URLs ist dies die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Advertisers verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Sie enthält alle für die Kampagne oder das Konto &quot;Search, Social und Commerce&quot;konfigurierten Anlagenparameter. Wenn Sie Tracking-URLs generiert haben, basiert dies auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie suchmaschinenspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Search, Social und Commerce ersetzt werden.<br><br>Bei Konten mit finalen URLs zeigt diese Spalte denselben Wert wie die Spalte Basis-URL/Endgültige URL an. |
| Benutzerdefinierter URL-Parameter | Zu ersetzende Daten `{custom_code}` dynamische Variable, wenn die Variable in den Tracking-Parametern für das Suchkonto oder die Kampagneneinstellungen enthalten ist. Um den benutzerdefinierten Wert in die Tracking-URL einzufügen, müssen Sie die Bulksheet-Datei mit der Option Tracking-URLs generieren hochladen. |
| Kreativer Typ | Das Anzeigenformat: <i>Dynamische Suchanzeige</i>, <i>Erweiterte Textanzeige</i>, <i>Erweiterte dynamische Suchanzeige</i>, <i>Multimedia-Anzeige</i>, <i>Produktanzeige</i> (Shopping-Anzeigen) oder <i>Responsive Suchanzeige</i>oder <i>Textanzeige</i>. Die Standardeinstellung für neue Anzeigen ist <i>Textanzeige</i>. |
| Startdatum der Anzeigengruppe | Das erste Datum, an dem Angebote für die Anzeigengruppe in der Zeitzone des Werbetreibenden und in einem der folgenden Formate platziert werden können: m/d/yyy, m/d/yy, m-d-yyy oder m-d-yy. Bei einer neuen Anzeigengruppe ist das aktuelle Datum der Standardwert. |
| Enddatum der Anzeigengruppe | Das letzte Datum, an dem Angebote für die Anzeigengruppe in der Zeitzone des Werbetreibenden und in einem der folgenden Formate platziert werden können: m/d/yyy, m/d/yy, m-d-yyy oder m-d-yy. Bei einer neuen Anzeigengruppe ist der Standardwert [blank] (d. h. kein Enddatum). |
| Tracking-Vorlage | (Optional) Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als granularsten) überschreibt die Werte auf allen höheren Ebenen.<br><br>Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;EF Redirect&quot;und &quot;Auto Upload&quot;enthalten, hängt Search, Social und Commerce beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.<br><br>Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.<br><br>Eine Liste der Parameter zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in der Microsoft Advertising-Dokumentation.<br><br> Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| Suffix der Einstiegsseite | Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen. Beispiel: `param2=value1&param3=value2`<br><br>Siehe[Klick-Tracking-Formate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Verwenden Sie den Microsoft Advertising Editor, um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren. |
| Netzwerkstatus durchsuchen | Ob Anzeigen für die Anzeigengruppe auf verschiedenen Elementen des Suchnetzwerks platziert werden sollen:<ul><li><i>Alle:</i> Zur Platzierung von Anzeigen in allen Bing-Suchnetzwerken und syndizierten Suchpartnern.</li><li><i>OwnedAndOperatedOnly:</i>So platzieren Sie Anzeigen nur auf Bing und Yahoo! Websites.</li><li><i>SyndicatedSearchOnly:</i> So platzieren Sie Anzeigen nur auf Bing und Yahoo! Syndizierte Suchpartner.</li><li><i>Aus:</i> So platzieren Sie Anzeigen nur im Inhaltsnetzwerk (nicht im Suchnetzwerk).</li></ul> Für neue Anzeigengruppen ist die Standardeinstellung &quot;An&quot;. |
| Inhaltsnetzwerkstatus | Veraltet |
| Sprachen | Die Zielsprache für Anzeigen in der Anzeigengruppe: Englisch, Französisch, Finnisch, Deutsch, Norwegisch, Spanisch oder Schwedisch. Die Standardeinstellung für neue Kampagnen ist Englisch.<br><br>Diese Einstellung bestimmt die Länder und Regionen, in denen Ihre Anzeige angezeigt werden kann. Achten Sie darauf, eine Sprache zu wählen, die mit den Standortzielen der Kampagne kompatibel ist. |
| Budgettyp | Ob das Budget <i>Täglich</i> (Standardeinstellung) oder <i>Monatlich</i>.<br><br>Hinweis: Wenn Sie die Kampagne einem optimierten Portfolio zuweisen, wird dieser Wert automatisch auf Täglich gesetzt. |
| Gerät | Ein Gerätetyp, für den Angebotsanpassungen auf Kampagnen- oder Anzeigengruppenebene vorgenommen werden: <i>Smartphone</i>, <i>Tablet</i>oder <i>Desktop</i>. |
| Angebotsanpassung | Die Angebotsanpassung für einen bestimmten Zieltyp. Wenn das Angebot auf Suchbegriffebene beispielsweise 1 USD und die Angebotsanpassung für Smartphones 50 % beträgt, beträgt das Gebot für Smartphones 1,50 USD. Standardmäßig beziehen sich alle Ziele auf das Angebot auf Suchbegriffebene. Gültige Prozentsätze können Folgendes umfassen:<ul><li>Smartphones und Tablets: -100 (kein Gebot für den Gerätetyp) und von -90 bis 900</li><li>Desktop: von 0 bis 900</li></ul> |
| Creative Preferred Devices | Die Gerätetypen, auf denen Sie die Anzeige oder den Sitelink bevorzugen: <i>Alle</i> (Standardeinstellung) oder <i>Mobile</i>. Wenn &quot;Mobile&quot;angegeben ist, versucht das Netzwerk, die Anzeige oder den Sitelink für Benutzer mobiler Geräte und nicht für Benutzer von Desktop- oder Tablet-Geräten anzuzeigen. Andernfalls zeigt das Netzwerk die Anzeige oder den Sitelink auf jedem Gerätetyp an. <b>Hinweis:</b> Das Netzwerk garantiert nicht, dass die Anzeige auf dem bevorzugten Gerätetyp angezeigt wird. |
| Param2 | Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL des Suchbegriffs oder der Titel, die Beschreibung oder die Basis-URL der Anzeige die Variable `{Param2}` dynamische Ersatzzeichenfolge. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge des Anzeigenelements, in dem Sie es verwenden werden (Titel 1 und Titel 2 zusammen können maximal 76 Zeichen lang sein). Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| Param3 | Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL des Suchbegriffs oder der Titel, die Beschreibung oder die Basis-URL der Anzeige die Variable `{Param3}` dynamische Ersatzzeichenfolge. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge des Anzeigenelements, in dem Sie es verwenden werden (Titel 1 und Titel 2 zusammen können maximal 76 Zeichen lang sein). Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| Linkname | Der Sitelink-Text. Sie muss innerhalb der Kampagne eindeutig sein. Wenn Sie &quot;Description1&quot;und &quot;Description2&quot;angeben, kann der Sitelink-Text bis zu 25 Einzelbyte- oder 12 Doppelbyte-Zeichen enthalten. Andernfalls kann der Sitelink-Text bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.<br><br>Microsoft Advertising kann zwei, vier oder sechs erweiterte Sitelinks mit Beschreibungen oder vier oder sechs Sitelinks in einer einzigen Zeile ohne Beschreibungen mit einer Anzeige anzeigen.<br><br>Sie können neue erweiterte Sitelinks nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellen. |
| Kampagnenstatus | Der Anzeigestatus der Kampagne: <i>Aktiv</i>, <i>Angehalten</i>oder <i>Gelöscht</i> (nur bestehende Kampagnen). Die Standardeinstellung für neue Kampagnen ist &quot;Aktiv&quot;. Um eine aktive oder ausgesetzte Kampagne zu löschen, geben Sie den Wert ein `Deleted`. |
| Anzeigengruppenstatus | Der Anzeigestatus der Anzeigengruppe: <i>Aktiv</i>, <i>Angehalten</i>oder <i>Gelöscht</i> (nur bestehende Anzeigengruppen). Die Standardeinstellung für neue Anzeigengruppen ist &quot;Aktiv&quot;. Um eine aktive oder ausgesetzte Anzeigengruppe zu löschen, geben Sie den Wert ein `Deleted`. |
| Suchbegriffstatus | Der Anzeigestatus des Suchbegriffs: <i>Aktiv</i>, <i>Angehalten</i>oder <i>Gelöscht</i> (nur vorhandene Suchbegriffe). Die Standardeinstellung für neue Suchbegriffe ist &quot;Aktiv&quot;. Um einen aktiven oder ausgesetzten Suchbegriff zu löschen, geben Sie den Wert ein `Deleted`. <b>Hinweis:</b> Wenn Sie Tracking-URLs für einen Suchbegriff mit mehreren Übereinstimmungstypen erstellen, muss der Suchbegriffstatus für jeden Übereinstimmungstyp identisch sein. |
| Platzierungsstatus | Veraltet |
| Anzeigenstatus | Der Anzeigestatus der Anzeige: <i>Aktiv</i>, <i>Gelöscht</i> (nur vorhandene Anzeigen), <i>Nicht genehmigt</i> (nicht bearbeitbar) oder <i>Angehalten</i>. Die Standardeinstellung für neue Anzeigen ist &quot;Aktiv&quot;. Um eine aktive oder ausgesetzte Anzeige zu löschen, geben Sie den Wert ein `Deleted`. |
| Zielstatus | Der Status eines dynamischen Suchziels: <i>Aktiv</i>, <i>Angehalten</i>oder <i>Gelöscht</i> (nur bestehende Ziele). Die Standardeinstellung für neue Ziele ist &quot;Aktiv&quot;. Um ein aktives oder ausgesetztes Ziel zu löschen, geben Sie den Wert ein `Deleted`. |
| Sitelink-Status | Der Anzeigestatus des Sitelink: <i>Aktiv</i> oder <i>Gelöscht</i> (nur bestehende Sitelinks). Die Standardeinstellung für neue Sitelinks ist &quot;Aktiv&quot;. Um einen aktiven Sitelink zu löschen, geben Sie den Wert ein `Deleted`. |
| Standort-Status | Der Status des Standort-Ziels: <i>Aktiv</i> oder <i>Gelöscht</i> (nur vorhandene Speicherorte). Die Standardeinstellung für neue Speicherorte ist &quot;Aktiv&quot;. Um eine aktive Position zu löschen, geben Sie den Wert ein `Deleted`. |
| Produktgruppenstatus | Der Anzeigestatus der Produktgruppe: <i>Aktiv</i> oder <i>Gelöscht</i> (nur bestehende Produktgruppen). Die Standardeinstellung für neue Produktgruppen ist &quot;Aktiv&quot;. Um eine aktive Produktgruppe zu löschen, geben Sie den Wert ein `Deleted`. |
| Gerätezielstatus | Der Status des Geräteziels auf Kampagnen- oder Anzeigengruppenebene: <i>Aktiv</i> oder <i>Gelöscht</i>. Für neue Kampagnen und Anzeigengruppen ist die Standardeinstellung &quot;Aktiv&quot;. |
| RLSA-Zielstatus | Der Status des RLSA-Ziels auf Kampagnen- oder Anzeigengruppenebene oder des Ausschlusses (nur Google Ads): <i>Aktiv</i> oder <i>Gelöscht</i> (nur bestehende Ziele). Die Standardeinstellung für neue Ziele oder Ausschlüsse ist &quot;Aktiv&quot;. Um eine aktive Zielgruppe oder einen Ausschluss zu löschen, geben Sie den Wert ein `Deleted`. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | (Benannt für eine Advertiser-spezifische Beschriftungs-Classification, z. B. &quot;Farbe&quot;für eine Beschriftungsklassifizierung namens &quot;Farbe&quot;) Ein Wert für die angegebene Classification, die mit der Entität verknüpft ist. Sie können pro Entität nur einen Wert angeben (z. B. &quot;rot&quot;für die Klassifizierung der Farbbeschriftung für Kampagne A). Die maximale Länge beträgt 100 Zeichen. Der Wert kann ASCII- und Nicht-ASCII-Zeichen enthalten.<br><br>Beschriftungsklassifizierungen und ihre Beschriftungswerte werden auf alle untergeordneten Komponenten angewendet. neue Komponenten, die später hinzugefügt werden, werden automatisch mit der Beschriftung verknüpft. Beschriftungsklassifizierungen für Produktgruppen werden auf die Einheitenebene (am detailliertesten) angewendet.<br><br>Weder der Classification-Name noch der Classification-Wert unterscheiden zwischen Groß- und Kleinschreibung. |
| Einschränkungen | Eine Beschränkung, die der Entität zugewiesen wird. Sie können pro Entität nur eine Begrenzung zuweisen.<br><b>>Einschränkungen werden von untergeordneten Entitäten übernommen. Sie müssen daher keine Werte für untergeordnete Entitäten eingeben, es sei denn, Sie möchten die vererbten Werte überschreiben. |
| Kampagnen-ID | Die eindeutige ID, die eine bestehende Kampagne identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält eine AMO-ID für die Kampagne. |
| Anzeigengruppen-ID | Die eindeutige ID, die eine bestehende Anzeigengruppe identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;für die Anzeigengruppe. |
| Platzierungs-ID | Veraltet |
| Schlüsselwort-ID | Die eindeutige ID, die einen vorhandenen Suchbegriff identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Suchbegriff ändern, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Suchbegriff zu identifizieren, oder b) eine &quot;AMO-ID&quot;. |
| Anzeigen-ID | <p>Die eindeutige ID, die eine vorhandene Anzeige identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Für responsive Suchanzeigen ist entweder die Anzeigen-ID oder die AMO-ID erforderlich, um Anzeigendaten zu bearbeiten oder zu löschen. Bei allen anderen Entitätstypen ist die AMO-ID nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;AMO-ID&quot;. Wenn Sie jedoch weder die Anzeigen-ID noch die AMO-ID angeben und die Spalten der Anzeigeneigenschaft mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen.</p><p><b>Hinweis:</b> Wenn Sie a) Anzeigeneigenschaftsspalten mit Ausnahme des Status für eine vorhandene Anzeige oder b) Daten für eine responsive Suchanzeige bearbeiten und weder die Anzeigen-ID noch die AMO-ID einschließen, wird eine neue Anzeige erstellt und die vorhandene Anzeige wird nicht geändert. </p> |
| Sitelink-ID | Die eindeutige ID, die einen vorhandenen Sitelink identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichende Eigenschaftsspalten, um den Sitelink zu identifizieren, oder b) eine &quot;AMO-ID&quot;. Wenn Sie jedoch weder die Sitelink-Anzeigen-ID noch die AMO-ID angeben und die Eigenschaftenspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status nur für einen der Sitelinks.</p><p><b>Hinweis:</b> Wenn Sie Sitelink-Eigenschaftenspalten mit Ausnahme des Status für einen vorhandenen Sitelink bearbeiten und weder die Sitelink-ID noch die AMO-ID einschließen, wird ein neuer Sitelink erstellt und der vorhandene Sitelink wird nicht geändert. |
| Produktgruppen-ID | Die eindeutige ID, die eine bestehende Produktgruppe identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichende Eigenschaftsspalten, um die Produktgruppe zu identifizieren, oder b) eine &quot;AMO-ID&quot;. |
| Standort-ID | Die eindeutige Microsoft Advertising-ID für das Standortziel. Um eine Ortsliste herunterzuladen, melden Sie sich mit Ihren Anmeldedaten für das Microsoft Advertising-Werbekonto beim Entwicklerportal für Microsoft Advertising an. Nur erforderlich, wenn Sie das Orts-Ziel ändern oder löschen, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;für das Ziel. |
| Target-ID | Die eindeutige ID, die ein vorhandenes automatisches Ziel identifiziert. Nur erforderlich, wenn Sie das automatische Ziel ändern oder löschen, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;für das Ziel. |
| RLSA Target-ID | Die eindeutige ID, die ein vorhandenes RLSA-Ziel auf Kampagnen- oder Anzeigengruppenebene identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie die Zielgruppe oder den Ausschluss ändern oder löschen, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;für die Zielgruppe. |
| AMO-ID | (In generierten Bulksheets) Eine von der Adobe generierte eindeutige Kennung für eine synchronisierte Entität. Bei responsiven Suchanzeigen ist die AMO-ID zum Bearbeiten oder Löschen von Anzeigen erforderlich, es sei denn, Sie enthalten die Anzeigen-ID. Um Daten für alle anderen Entitätstypen mit AMO-ID zu bearbeiten, muss die AMO-ID die Daten bearbeiten oder löschen, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |
| EF-Fehlermeldung | (Zu Informationszwecken in generierten Bulksheets enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Anzeigennetzwerk bezüglich Daten aus der Zeile; Fehlermeldungen sind in den EF-Fehlerdateien enthalten. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |
| SE-Fehlermeldung | (Zu Informationszwecken in generierten Bulksheets enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Anzeigennetzwerk bezüglich Daten aus der Zeile; Fehlermeldungen sind in den Dateien mit SE-Fehlern enthalten. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |
| Befreiungsantrag | (Enthalten in generierten Bulksheets für Informationszwecke) Platzhalter für die Anzeige der Namen und des Texts von Google-Werberichtlinien, gegen die eine Anzeige verstößt. |
| Einzelhandel-Hash | (Zu Informationszwecken in mit dem erweiterten Campaign Management generierten Bulksheets enthalten) Ein alphanumerischer Hash-Code (z. B. f9639f40cdf56524b541e5dacf55a991), der anzeigt, dass das Element mithilfe der Erweiterten (ACM) Ansicht generiert wurde. |

<table style="table-layout:auto">

[^1]: [!DNL Excel] konvertiert große Zahlen in wissenschaftliche Notation (z. B. 2.12E+09 für 2115585666), wenn die Datei geöffnet wird. Um Ziffern in der Standardnotation anzuzeigen, wählen Sie eine beliebige Zelle in der Spalte aus und klicken Sie in die Formelleiste.

## Felder, die zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente erforderlich sind

### Kampagnenfelder

| Feld | Erforderlich? |
| ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| Kampagnenbudget | Erforderlich zum Erstellen einer Kampagne. | Eine tägliche Ausgabenbegrenzung für die Kampagne mit oder ohne monetäre Symbole und Satzzeichen. Dieser Wert setzt das Kontobudget außer Kraft. |
| Kanaltyp | Erforderlich zum Erstellen einer Kampagne. |
| Versandmethode | Optional |
| Kampagnenpriorität | Erforderlich, um eine Warenkampagne zu erstellen. |
| Merchant-ID | Erforderlich, um eine Warenkampagne zu erstellen. |
| Vertriebsland | Erforderlich, um eine Warenkampagne zu erstellen. |
| Produktumfang-Filter | (Shopping-Kampagnen) Optional |
| DSA-Domänenname | Erforderlich, um eine Kampagne vom Typ a) &quot;DynamicSearchAds&quot;oder b) &quot;Search&quot;zu erstellen, wenn das Element ExperimentId nicht festgelegt ist.) |
| DSA-Domänensprache | Erforderlich, um eine Kampagne vom Typ a) &quot;DynamicSearchAds&quot;oder b) &quot;Search&quot;zu erstellen, wenn das Element ExperimentId nicht festgelegt ist.) |
| Tracking-Vorlage | Optional |
| Suffix der Einstiegsseite | <p>Optional |
| Budgettyp | Erforderlich zum Erstellen einer Kampagne. |
| Gerät | Optional |
| Angebotsanpassung | Optional |
| Kampagnenstatus | Nur zum Löschen einer Kampagne erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Einschränkungen | Optional |
| Kampagnen-ID | Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält eine AMO-ID für die Kampagne. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Anzeigengruppenfelder

| Feld | Erforderlich? |
| ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich |
| Anzeigengruppentyp | Erforderlich zum Erstellen einer Anzeigengruppe. |
| Zielgruppenbestimmungsmethode | Nur zum Erstellen von Zielgruppen-Anzeigengruppen erforderlich. |
| Startdatum der Anzeigengruppe | Optional |
| Enddatum der Anzeigengruppe | Optional |
| Tracking-Vorlage | Optional |
| Netzwerkstatus durchsuchen | (Nur Kampagnen im Suchnetzwerk) Optional |
| Sprachen | Optional |
| Gerät | Optional |
| Angebotsanpassung | Optional |
| Anzeigengruppenstatus | Nur zum Löschen einer Anzeigengruppe erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Einschränkungen | Optional |
| Anzeigengruppen-ID | Nur erforderlich, wenn Sie den Anzeigengruppennamen ändern, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;für die Anzeigengruppe. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Suchbegriffsfelder

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich |
| Schlüsselwort | Erforderlich |
| Übereinstimmungstyp | Zum Bearbeiten oder Löschen eines Suchbegriffs mit mehreren Übereinstimmungstypen ist ein Wert für den Übereinstimmungstyp oder die Keyword-ID erforderlich. |
| Max. CPC | Optional |
| Basis-URL/Endgültige URL | Optional |
| Benutzerdefinierter URL-Parameter | Optional |
| Tracking-Vorlage | Optional |
| Param1 | Optional |
| Param2 | Optional |
| Suchbegriffstatus | Nur zum Löschen eines Suchbegriffs erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Einschränkungen | Optional |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Optional |
| Schlüsselwort-ID | Nur erforderlich, wenn Sie den Suchbegriff bearbeiten oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Suchbegriff zu identifizieren, oder b) eine &quot;AMO-ID&quot;. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Dynamische Suchanzeigenfelder

>[!NOTE]
>
>Support erstellen ist nicht verfügbar.

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Creative (except RSA)]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich |
| Beschreibung Zeile 1-2 | Erforderlich, um die Beschreibung zu bearbeiten. <b>Hinweis:</b> Bei diesem Anzeigentyp löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue. |
| Anzeigepfad 1 | Erforderlich, um das Feld zu bearbeiten. |
| Anzeigepfad 2 | Erforderlich, um das Feld zu bearbeiten. |
| Kreativer Typ | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| Creative Preferred Devices | Optional |
| Anzeigenstatus | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Optional |
| Anzeigen-ID | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;AMO-ID&quot;. Wenn Sie jedoch weder die Anzeigen-ID noch die AMO-ID angeben und die Spalten der Anzeigeneigenschaft mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Produkt- (Einkaufs-)Anzeigenfelder

Weitere Informationen zum Erstellen von Shopping-Anzeigen finden Sie unter &quot;[Implementieren von Microsoft Advertising Shopping-Kampagnen](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).&quot;

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Creative (except RSA)]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich |
| Promotion Line | Optional |
| Basis-URL/Endgültige URL | Optional |
| Benutzerdefinierter URL-Parameter | Optional |
| Kreativer Typ | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| Tracking-Vorlage | Optional |
| Anzeigenstatus | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Einschränkungen | Optional |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Optional |
| Anzeigen-ID | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;AMO-ID&quot;. Wenn Sie jedoch weder die Anzeigen-ID noch die AMO-ID angeben und die Spalten der Anzeigeneigenschaft mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Responsive (Multimedia) Anzeigenfelder

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Creative (except RSA)]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich |
| Anzeigentitel, Anzeigentitel 2-15 | Für responsive Anzeigen sind der Anzeigentitel, der Anzeigentitel 2 und der Anzeigentitel 3 erforderlich, um Anzeigen zu erstellen. Alle anderen Felder für Anzeigentitel sind optional. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). <b>Hinweis:</b> Bei diesem Anzeigentyp löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue. |
| Beschreibung Zeile 1-4 | Beschreibung Zeile 1 und Beschreibung Zeile 2 sind erforderlich, um Anzeigen zu erstellen, und Beschreibung Zeile 3 und Beschreibung Zeile 4 sind optional. <b>Hinweis:</b> Bei diesem Anzeigentyp löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue. |
| Geschäftsname | Erforderlich zum Erstellen oder Löschen einer Anzeige. |
| Aktionsaufruf | Erforderlich zum Erstellen einer Anzeige. |
| Aktionssprache aufrufen | Erforderlich zum Erstellen einer Anzeige. |
| Basis-URL/Endgültige URL | Erforderlich zum Erstellen einer Anzeige. |
| Kreativer Typ | Optional. |
| Tracking-Vorlage | Optional |
| Anzeigenstatus | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Optional |
| Anzeigen-ID | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;AMO-ID&quot;. Wenn Sie jedoch weder die Anzeigen-ID noch die AMO-ID angeben und die Spalten der Anzeigeneigenschaft mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Responsive Suchanzeigenfelder

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Responsive Search Ad]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich | |
| Anzeigentitel, Anzeigentitel 2-15 | Für responsive Suchanzeigen müssen der Anzeigentitel, der Anzeigentitel 2 und der Anzeigentitel 3 eine Anzeige erstellen. Alle anderen Felder für den Anzeigentitel sind optional. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| Position des Anzeigentitels 1-15 | Optional |
| Beschreibung Zeile 1-4 | Für responsive Suchanzeigen sind Beschreibung Zeile 1 und Beschreibung Zeile 2 erforderlich, um eine Anzeige zu erstellen. Die Beschreibung Zeile 3 und Beschreibung Zeile 4 sind optional. Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| Beschreibung Zeile 1-4 Position | Optional |
| Anzeigepfad 1 | Optional |
| Anzeigepfad 2 | Optional |
| Basis-URL/Endgültige URL | Erforderlich zum Erstellen einer Anzeige. |
| Benutzerdefinierter URL-Parameter | Optional |
| Kreativer Typ | Optional |
| Tracking-Vorlage | Optional |
| Anzeigenstatus | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Optional |
| Anzeigen-ID | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, Sie enthalten die Anzeigen-ID. |

### Textanzeigenfelder

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Creative (except RSA)]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

>[!NOTE]
>
>Erweiterte Textanzeigen werden nicht mehr unterstützt. Sie können nur vorhandene Textanzeigen löschen.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich |
| Anzeigentitel, Anzeigentitel 2-3 | Schreibgeschützt |
| Beschreibung Zeile 1-2 | Schreibgeschützt |
| URL anzeigen | Schreibgeschützt |
| Anzeigepfad 1 | Schreibgeschützt |
| Anzeigepfad 2 | Schreibgeschützt |
| Basis-URL/Endgültige URL | Schreibgeschützt |
| Benutzerdefinierter URL-Parameter | Schreibgeschützt |
| Kreativer Typ | Optional |
| Tracking-Vorlage | Schreibgeschützt |
| Creative Preferred Devices | Schreibgeschützt |
| Anzeigenstatus | Erforderlich |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Optional |
| Anzeigen-ID | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Anzeigen-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Felder für dynamisches Suchziel (automatisches Targeting)

>[!NOTE]
>
>Support erstellen ist nicht verfügbar.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich |
| Ausdruck für automatisches Targeting | Erforderlich. |
| Übereinstimmungstyp | Optional |
| Max. CPC | Optional |
| Benutzerdefinierter URL-Parameter | Optional |
| Zielstatus | Löschen einer Zielgruppe erforderlich |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Einschränkungen | Optional |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Optional |
| Target-ID | Nur erforderlich, wenn Sie das automatische Ziel ändern oder löschen, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;für das Ziel. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Produktgruppenfelder kaufen

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich |
| Übereinstimmungstyp | Erforderlich zum Erstellen einer Produktgruppe. |
| Max. CPC | Erforderlich zum Erstellen einer Produktgruppe. |
| Übergeordnete Produktgruppen | Erforderlich |
| Produktgruppierung | Erforderlich |
| Partitionstyp | Erforderlich zum Erstellen einer Produktgruppe. |
| Basis-URL/Endgültige URL | Erforderlich |
| Tracking-Vorlage | Optional |
| Produktgruppenstatus | Nur zum Löschen einer Produktgruppe erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| Einschränkungen | Optional |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Optional |
| Produktgruppen-ID | Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichende Eigenschaftsspalten, um die Produktgruppe zu identifizieren, oder b) eine &quot;AMO-ID&quot;. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Sitelink-Felder auf Kampagnenebene

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Beschreibung Zeile 1 | Optional |
| Beschreibung Zeile 2 | Optional |
| Startdatum | Optional |
| Enddatum | Optional |
| Basis-URL/Endgültige URL | Erforderlich |
| Benutzerdefinierter URL-Parameter | Optional |
| Tracking-Vorlage | Optional |
| Creative Preferred Devices | Optional |
| Linkname | Erforderlich |
| Sitelink-Status | Nur zum Löschen eines Sitelink-Links erforderlich. |
| Kampagnen-ID | Optional |
| Sitelink-ID | Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichende Eigenschaftsspalten, um den Sitelink zu identifizieren, oder b) eine &quot;AMO-ID&quot;. Wenn Sie jedoch weder die Sitelink-Anzeigen-ID noch die AMO-ID angeben und die Eigenschaftenspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status nur für einen der Sitelinks.<br><br><b>Hinweis:</b> Wenn Sie Sitelink-Eigenschaftenspalten mit Ausnahme des Status für einen vorhandenen Sitelink bearbeiten und weder die Sitelink-ID noch die AMO-ID einschließen, wird ein neuer Sitelink erstellt und der vorhandene Sitelink wird nicht geändert. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Zielgruppenfelder der Position

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Standort | Erforderlich |
| Location Type | Erforderlich zum Erstellen einer Zielgruppe |
| Angebotsanpassung | Optional |
| Standort-Status | Nur zum Löschen eines Orts-Ziels erforderlich. |
| Kampagnen-ID | Optional |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Kampagnen-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Zielfelder auf Kampagnenebene und auf Anzeigengruppenebene

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Gerät | Erforderlich zum Löschen eines Geräteziels. |
| Angebotsanpassung | Optional |
| Anzeigengruppenname | Erforderlich für Geräteziele auf Anzeigengruppenebene. Gilt nicht für Geräteziele auf Kampagnenebene. |
| Gerätezielstatus | Nur zum Löschen eines Geräteziels erforderlich. |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Fakultativ; gilt nur für Geräteziele auf Anzeigengruppenebene. |
| AMO-ID | Erforderlich, um die Daten zu bearbeiten oder zu löschen, es sei denn, Sie enthalten die Geräteziel-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### RLSA-Zielfelder auf Kampagnenebene und Anzeigengruppenebene

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| Kontoname | Erforderlich, es sei denn, jede Zeile enthält eine &quot;AMO-ID&quot;für die Entität. |
| Kampagnenname | Erforderlich |
| Anzeigengruppenname | Erforderlich für Ziele auf Anzeigengruppenebene. Gilt nicht für Ziele auf Kampagnenebene. |
| Zielgruppe | Erforderlich, um ein neues Ziel zu erstellen. |
| Zieltyp | Optional |
| Angebotsanpassung | Optional |
| RLSA-Zielstatus | Erforderlich zum Löschen eines Ziels. |
| Kampagnen-ID | Optional |
| Anzeigengruppen-ID | Fakultativ; gilt nur für Ziele auf Anzeigengruppenebene. |
| RLSA Target-ID | Nur erforderlich, wenn Sie das Ziel ändern oder löschen, es sei denn, die Zeile enthält eine &quot;AMO-ID&quot;für das Ziel. |
| AMO-ID | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die RLSA-Target-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

>[!MORELIKETHIS]
>
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Vorgänge, die Sie in Bulksheets ausführen können](bulksheet-operations.md)
>* [Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
>* [Klick-Tracking-Formate für [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Hochladen einer Bulksheet-Datei oder einer korrigierten Fehlerdatei](../bulksheet-upload.md)
