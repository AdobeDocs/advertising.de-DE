---
title: Erforderliche Bulksheet-Daten für [!DNL Microsoft Advertising] Konten
description: Referenzieren Sie die erforderlichen Kopfzeilenfelder und Datenfelder in Bulksheets für [!DNL Microsoft Advertising] Konten.
exl-id: a3090962-49df-46b0-89f8-98b633c3ea7a
source-git-commit: e4901c1ac6e73f27886e315136c3fe9b865cdd48
workflow-type: tm+mt
source-wordcount: '6721'
ht-degree: 1%

---

# Anhang - Erforderliche Bulksheet-Daten für [!DNL Microsoft Advertising] Konten

So erstellen und aktualisieren Sie [!DNL Microsoft Advertising] Kampagnendaten stapelweise verwenden, können Sie Bulksheet-Dateien für Suche, Social und Commerce verwenden, die speziell für [!DNL Microsoft Advertising] Konten. Sie können entweder a) [Massenblatt-Dateien für bestehende Konten generieren](../bulksheet-download.md) im erforderlichen Dateiformat oder b) manuell erstellen (siehe[Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)&quot; allgemeine Informationen zu den unterstützten Dateiformaten).

Jedes Bulksheet muss die Kopfzeilenfelder und die entsprechenden Datenfelder enthalten, die für die [bestimmte Vorgänge, die Sie ausführen möchten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (z. B. Erstellen einer Anzeige). Wenn ein Feld nicht erforderlich ist, können Sie es aus der Kopfzeile und den Datenzeilen auslassen. Alle benutzerdefinierten Spalten werden beim Hochladen der Bulk-Sheet-Datei gelöscht.

Im Folgenden finden Sie eine Tabelle aller verfügbaren Datenfelder und zusätzliche Tabellen, die angeben, welche Felder zum Hinzufügen, Bearbeiten oder Löschen von Daten für einzelne Entitäten (z. B. Kampagnen und Suchbegriffe) erforderlich sind.

## Alle verfügbaren Datenfelder

Die folgende Tabelle zeigt alle verfügbaren Datenfelder.

Informationen zu den für Kontoentitäten relevanten Datenfeldern finden Sie unter[Felder, die zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente erforderlich sind](#bulksheet-fields-per-component-microsoft).

| Feld | Beschreibung |
|----|----|
| [!UICONTROL Platform] | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Acct Name] | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. Die maximale Länge beträgt 128 Zeichen. |
| [!UICONTROL Campaign Budget] | Das tägliche oder monatliche Kampagnenbudget mit oder ohne monetäre Symbole und Satzzeichen. Es darf nicht weniger als 0,05 sein. |
| [!UICONTROL Channel Type] | Der Typ des Kanals, auf den die Kampagne ausgerichtet ist: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i>oder <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Nur Kampagnen mit täglichem Budget) Wie schnell zeigen Sie Anzeigen für die Kampagne jeden Tag an:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (Standardeinstellung für neue Kampagnen): So verbreiten Sie Ihre Anzeigenimpressionen über den Tag.</li><li><i>[!UICONTROL Accelerated]:</i> Um Ihre Anzeigen so oft wie möglich anzuzeigen, bis Ihr Budget erreicht ist. Daher werden Ihre Anzeigen möglicherweise nicht später am Tag angezeigt.</li></ul> |
| [!UICONTROL Campaign Priority] | (Nur Shopping-Kampagnen) Die Priorität, mit der die Kampagne verwendet wird, wenn mehrere Kampagnen für dasselbe Produkt werben: <i>[!UICONTROL Low]</i> (Standardeinstellung für neue Kampagnen), <i>[!UICONTROL Medium]</i>oder <i>[!UICONTROL High]</i>.<br><br>Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Werbenetzwerk zuerst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und welches zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt. |
| [!UICONTROL Merchant ID] | (Nur Shopping-Kampagnen und Zielgruppenkampagnen, die mit einem Händler-Feed verknüpft sind) Die Kunden-ID des Händlers-Kontos, dessen Produkte für die Kampagne verwendet werden. |
| [!UICONTROL Sales Country] | (Nur Shopping-Kampagnen; schreibgeschützt für bestehende Kampagnen) Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden. |
| [!UICONTROL Product Scope Filter] | (Nur Kampagnen, die das Einkaufsnetzwerk verwenden) Die Produkte in Ihrem Händlerkonto, für die Produktanzeigen für die Kampagne erstellt werden können. Sie können bis zu sieben Produktdimensionen- und Attributkombinationen eingeben, nach denen Ihre Produkte gefiltert werden sollen. Verwenden Sie dazu das Attribut format dimension=attribute . Trennen Sie mehrere Filter mit einem &quot;>>&quot;-Trennzeichen. Eine Liste der verfügbaren Produktdimensionen finden Sie unter[Produktfilter für Shopping-Kampagnen](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Beispiel: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Um die vorhandenen Werte zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL DSA Domain Name] | (Kampagnen des Typs a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; oder b) &quot;<i>[!UICONTROL Search]</i>&quot;, wenn die [!DNL ExperimentId] -Element nicht festgelegt ist) Der Domänenname der Website, auf die für dynamische Suchanzeigen abgezielt werden soll. Die maximale Länge beträgt 2.048 Zeichen. Wenn der Domänenname `www`, ist es abgeschnitten und nicht verwendet.<br><br>Bei vorhandenen Kampagnen können Sie die Domäne nicht bearbeiten, müssen sie jedoch einschließen, um andere Eigenschaften zu aktualisieren. |
| [!UICONTROL DSA Domain Language] | (Kampagnen des Typs a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; oder b) &quot;<i>[!UICONTROL Search]</i>&quot;, wenn die [!DNL ExperimentId] -Element nicht festgelegt ist) Die Sprache der Website-Seiten, die als Ziel für dynamische Suchanzeigen dienen sollen. Die unterstützten Domänensprachen sind [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish]und [!UICONTROL Swedish].<br><br>Bei vorhandenen Kampagnen können Sie die Sprache nicht bearbeiten, müssen sie jedoch einbeziehen, um andere Eigenschaften zu aktualisieren. |
| [!UICONTROL Ad Group Name] | Der eindeutige Name, der eine Anzeigengruppe identifiziert. Die maximale Länge beträgt 128 Zeichen. Nachfolgende Leerzeichen werden nicht gespeichert (z. B. wird &quot;Anzeigengruppe 1&quot;als &quot;Anzeigengruppe 1&quot;gespeichert). |
| [!UICONTROL Ad Group Type] | (Kampagnen im Suchnetz; schreibgeschützt für bestehende Anzeigengruppen) Der Anzeigengruppentyp: <i>[!UICONTROL Audience]</i> (nur für Zielgruppenkampagnen), <i>[!UICONTROL Search Dynamic]</i> (nur für dynamische Suchanzeigen) und <i>[!UICONTROL Search Standard]</i> (nur für responsive Suchanzeigen und vorhandene erweiterte Textanzeigen). Einige Kampagnentypen können mehrere Anzeigengruppentypen umfassen. |
| [!UICONTROL Keyword] | (Nur Kampagnen im Suchnetzwerk) Die Keyword-Zeichenfolge. Die maximale Länge beträgt 50 Zeichen.<br><br><b>Hinweise:</b><ul><li>Um einen Suchbegriff auf Anzeigengruppen- oder Kampagnenebene auszuschließen, legen Sie die [!UICONTROL Match Type] nach `Negative`. Wenn die Zeile den Anzeigengruppennamen enthält, wird der Suchbegriff für die Anzeigengruppe ausgeschlossen. Wenn die Zeile nicht den Anzeigengruppennamen enthält, wird der Suchbegriff für die gesamte Kampagne ausgeschlossen.</li><li>Ändern einer [!DNL Microsoft Advertising] löscht den vorhandenen Suchbegriff und erstellt einen neuen mit einer neuen Suchbegriff-ID. Beim Ändern des Übereinstimmungstyps wird jedoch der vorhandene Suchbegriff nicht gelöscht.</li></ul> |
| Platzierung | Veraltet |
| [!UICONTROL Audience] | Die Remarketing-Liste für Suchanzeigen (RLSA)-Zielgruppe für die Kampagne oder Anzeigengruppe. |
| [!UICONTROL Target Type] | (Nur RLSA) Der Zieltyp: <i>[!UICONTROL Inclusion]</i> oder <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Dynamische Suchziele für die Anzeigengruppe. Verwenden Sie für alle Ziele &quot;[!UICONTROL All Web Pages].&quot;<br><br>Verwenden Sie das Format , um bis zu drei dynamische Suchkriterien als Ziel auszuwählen. `<category>=<target>`, wobei &lt;category> kann eine der folgenden Kategorien umfassen. Verknüpfen mehrerer Ziele für eine einzelne Kategorie mit &quot;`[blank space] and [blank space]`&quot; und fügen Sie mehrere Kategorien mit &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Kategorie:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit einer bestimmten Google-Inhaltskategorie an.</li><li><i>URL:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit einer bestimmten URL an, auf denen der Wert an einer beliebigen Stelle in der URL enthalten sein kann.</li><li><i>Seitentitel:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit spezifischem Text im Seitentitel an.</li><li><i>Seiteninhalt:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit bestimmten Inhalten an.</li></ul>Beispiel: url=shoes.example.com und page title=Schuhe<br>Beispiel: Alle Webseiten |
| [!UICONTROL Location] | Ein geografischer Ort, an dem Anzeigen für die Kampagne oder Anzeigengruppe platziert werden sollen; Bei den Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie keine Werte für die Kampagne oder Anzeigengruppe eingeben, werden alle Orte als Ziel ausgewählt. Geben Sie den Standort mithilfe der [!DNL Microsoft Advertising] Speicherort-Codeformate. Um eine Standortliste herunterzuladen, melden Sie sich bei der [!DNL Microsoft Advertising] Entwicklerportal mit [!DNL Microsoft Advertising] Anmeldedaten für Werbekonten. <b>Hinweis:</b> Um einen Ort auszuschließen, setzen Sie dem Ortscode ein Minuszeichen (`-`), z. B. `-United States`. |
| [!UICONTROL Location Type] | Der Standorttyp, z. B. Stadt, Land, MetroArea, Postleitzahl und Bundesland. Um eine Standortliste herunterzuladen, melden Sie sich bei der [!DNL Microsoft Advertising] Entwicklerportal mit [!DNL Microsoft Advertising] Anmeldedaten für Werbekonten. |
| [!UICONTROL Match Type] | (Nur Kampagnen im Suchnetzwerk) Die Suchbegriffabgleichoption(en). Dies kann die Suchbegriffabgleichoption für ein dynamisches Suchziel oder eine Produktgruppe enthalten. Zu den Werten gehören: <i>[!UICONTROL Broad]</i> (Standardeinstellung für neue Suchbegriffe), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (Wird automatisch für Suchbegriffe festgelegt, wenn die Anzeigengruppe auf das Inhaltsnetzwerk ausgerichtet ist) <i>[!UICONTROL Negative]</i> (um einen Suchbegriff im Inhaltsnetzwerk auszuschließen), <i>[!UICONTROL Dynamic Ad Target]</i> (Standardeinstellung für neue dynamische Suchziele), <i>[!UICONTROL Product Group]</i> (Standardeinstellung für neue Produktgruppen) oder <i>[!UICONTROL Negative Product Group]</i> (um eine Produktgruppe auszuschließen).  Zum Bearbeiten oder Löschen eines Suchbegriffs mit mehreren Übereinstimmungstypen ist ein Wert für den Übereinstimmungstyp oder die Keyword-ID erforderlich.<br><br>Wählen Sie für einen Modifikator für breite Übereinstimmung &quot;Weit gefasst&quot;und fügen Sie eine `+` vor einem beliebigen Wort innerhalb des erforderlichen Suchbegriffs (z. B. &quot;`+red +shoes`&quot;, um sowohl &quot;rot&quot; als auch &quot;Schuhe&quot; zu benötigen).<br><br>Ändern des Übereinstimmungstyps für eine [!DNL Microsoft Advertising] den vorhandenen Suchbegriff nicht löscht. |
| [!UICONTROL Max CPC] | (Kampagnen im Suchnetzwerk) Die maximalen Kosten pro Klick (CPC), d. h. der höchste zu zahlende Betrag für einen Klick auf eine Werbeanzeige basierend auf dem Suchbegriff, der Produktgruppe oder dem dynamischen Suchziel, mit oder ohne monetäre Symbole und Interpunktion.  Bei vorhandenen Suchbegriffen und Produktgruppen-Datensätzen in optimierten Portfolios sind Aktualisierungen nur für einen Tag wirksam und werden während des nächsten Optimierungszyklus überschrieben. <b>Hinweis:</b> Sie können keine Angebote für negative Suchbegriffe festlegen. |
| [!UICONTROL Max Content CPC] | (Schreibgeschützt für CPC-Kampagnen, die vor der Einstellung des Inhaltsnetzwerks nur 2017 erstellt wurden) Die maximalen Inhaltskosten pro Klick (CPC), der höchste Betrag, der für einen Klick auf eine Display-Netzwerkseite mit oder ohne monetäre Symbole und Interpunktion zu zahlen ist. |
| [!UICONTROL Audience Target Method] | (Zielgruppen-Anzeigengruppen) Ob:<ul><li><i>[!UICONTROL Target and Bid]:</i> So zeigen Sie Anzeigen nur Benutzern an, die mit Zielgruppen verknüpft sind, die auch andere Ziele für die Anzeigengruppe erfüllen.</li><li><i>[!UICONTROL Bid Only]:</i>Anzeigen auch für Personen anzeigen, die nicht mit Zielgruppen verbunden sind, solange sie andere Ziele auf Anzeigengruppenebene erfüllen.</li></ul> Sie können die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie jedoch höhere Angebote für diese Zielgruppen festlegen. |
| [!UICONTROL Parent Product Groupings] | Die Hierarchie der übergeordneten Produktgruppen.<br><br>Beispiel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | Die Produktgruppe (z. B. &quot;brand=acme&quot;oder &quot;Alle Produkte&quot;).<br><br><b>Hinweise:</b><ul><li>Wenn eine bestimmte Produktgruppe nicht in der Hierarchie der übergeordneten Produktgruppen vorhanden ist, erstellt Search, Social und Commerce alle erforderlichen Teile der Hierarchie.</li><li>Search, Social &amp; Commerce erstellt automatisch ein &quot;[!UICONTROL All Products]&quot; immer dann gruppieren, wenn Sie eine Anzeigengruppe in einer Einkaufskampagne erstellen, bei der ein Standardangebot für die Anzeigengruppe auf das Standardgebot eingestellt ist. Search, Social &amp; Commerce erstellt automatisch ein &quot;[!UICONTROL Everything Else]&quot; mit dem Standardangebot für Anzeigengruppen auf jeder Ebene der Produktgruppenhierarchie. Sie können diese Standardgruppen auch explizit erstellen und entweder ausschließen oder ihre Angebote ändern.</li><li>Jede Anzeigengruppe kann bis zu acht Stufen von Produktgruppen umfassen, darunter[!UICONTROL All Products]&quot; und sieben weitere Ebenen.</li></ul> |
| [!UICONTROL Partition Type] | Der Partitionstyp für die Produktgruppe: <i>[!UICONTROL subdivision]</i> (wenn es untergeordnete Produktgruppen hat) oder <i>[!UICONTROL unit]</i> (wenn keine untergeordneten Produktgruppen vorhanden sind). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Nur erweiterte Textanzeigen, Multimedia-Anzeigen, responsive Anzeigen und responsive Suchanzeigen) Die Überschriften einer Anzeige. Die maximale Länge für jedes Feld mit Anzeigentitel beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen, einschließlich dynamischer Texte (z. B. die Werte von Keywords, `{Param2}` und `{Param3}` dynamische Ersatzvariablen und Anzeigenanpassungen).<br><br> Fügen Sie für responsive Suchanzeigen einen Anzeigenanpasser im folgenden Format ein, wobei &quot;Standardtext&quot;ein optionaler Wert ist, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Für erweiterte Textanzeigen sind Anzeigentitel und Anzeigentitel 2 erforderlich und [!UICONTROL Ad Title 3] ist optional. [!DNL Microsoft Advertising] veraltete erweiterte Textanzeigen im August 2022. Sie können jetzt nur noch Berichte zu diesen Werbeanzeigen erstellen und diese löschen.<br><br>Für Multimedia-Anzeigen, responsive Anzeigen und responsive Suchanzeigen, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]und [!UICONTROL Ad Title 3] sind erforderlich und alle anderen Felder für den Anzeigentitel sind optional.<br><br>Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).<br><br>Bei allen Anzeigentypen mit Ausnahme von erweiterten Textanzeigen löscht eine Änderung der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue Anzeige mit denselben Eigenschaften. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Nur responsive Suchanzeigen; optional) Eine Position, an der der entsprechende Anzeigentitel veröffentlicht werden soll: `[null]` (kein Wert, sodass der Anzeigentitel für alle Positionen infrage kommt), 1, 2 oder 3. Wenn beispielsweise [!UICONTROL Ad Title Position] den Wert 1 hat, dann [!UICONTROL Ad Title] wird nur in Position 1 angezeigt. Standardmäßig sind alle Anzeigentitel null (haben keine Werte). Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).<br><br><b>Hinweis:</b> Sie können mehrere Anzeigentitel an derselben Position veröffentlichen. Das Anzeigennetzwerk verwendet einen der Anzeigentitel, die an die Position gebunden sind. Titel, die an Position 3 gekoppelt sind, können nicht mit der Anzeige angezeigt werden. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Nur Textanzeigen, dynamische Suchanzeigen, Multimedia-Anzeigen, responsive Suchanzeigen, responsive Suchanzeigen und erweiterte Sitelinks auf Kampagnenebene) Der Hauptteil einer Anzeige oder eines Sitelink.<br><br>Für Sitelinks optional beide [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] um zusätzlichen Text einzufügen, den das Werbenetzwerk unter dem Link-Text anzeigen kann. Jedes Beschreibungsfeld kann bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.<br><br>Bei Anzeigen beträgt die maximale Länge für jedes Beschreibungsfeld 90 Zeichen oder 45 Doppelbyte-Zeichen, einschließlich dynamischer Texte (wie die Werte von Suchbegriffen und Anzeigenanpassungen).<br><br>Fügen Sie für responsive Suchanzeigen einen Anzeigenanpasser im folgenden Format ein, wobei Standardtext ein optionaler Wert ist, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Für Textanzeigen und dynamische Suchanzeigen ist eine Beschreibung Zeile 1 erforderlich und [!UICONTROL Description Line 2] ist optional.<br><br>Für Multimedia-Anzeigen, responsive Anzeigen und responsive Suchanzeigen, [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] erforderlich sind und [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).<br><br><b>Hinweise:</b><ul><li>(Standardtextanzeigen) Der kombinierte Titel und Text muss mindestens drei Wörter umfassen.</li><li>(Erweiterte Textanzeigen) Dieses Feld kann optional die {Param2} und {Param3} dynamische Ersatzvariablen. Ist dies der Fall, beträgt die maximale Länge des Anzeigentextes 300 Einzelbyte- oder 150 Doppelbyte-Zeichen. [!DNL Microsoft Advertising] veraltete erweiterte Textanzeigen im August 2022. Sie können jetzt nur noch Berichte zu diesen Werbeanzeigen erstellen und diese löschen.</li><li>(Dynamische Suchanzeigen) Dynamischer Ersatztext ist nicht zulässig.</li><li>Bei allen Anzeigentypen außer erweiterten Textanzeigen löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Nur responsive Suchanzeigen; optional) Eine Position, an der die entsprechende Beschreibung veröffentlicht werden soll: `[null]` (kein Wert, sodass die Beschreibung für alle Positionen geeignet ist), 1, 2 oder 3. Wenn beispielsweise [!UICONTROL Description 1 Position] den Wert 1 hat, wird die Beschreibung 1 nur in Position 1 angezeigt. Standardmäßig werden keine Beschreibungen an eine Position veröffentlicht.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern).<br><br><b>Hinweis:</b> Sie können mehrere Beschreibungen an derselben Position veröffentlichen. Das Werbenetzwerk verwendet eine der Beschreibungen, die an die Position gebunden sind. In Position 2 enthaltene Beschreibungen werden möglicherweise nicht zusammen mit der Anzeige angezeigt. |
| [!UICONTROL Business Name] | (Nur Multimedia-Anzeigen) Der Unternehmensname mit maximal 25 Zeichen. |
| [!UICONTROL Promotion Line] | (Nur Produktlistenanzeigen) Eine eindeutige Promotion-Zeile, die in die Produktliste in den Suchergebnissen aufgenommen werden soll (z. B. &quot;Kostenloser Versand jetzt!&quot;). Die maximale Länge beträgt 45 Zeichen.<br><br>Die Promotion-Zeile kann an verschiedenen Stellen relativ zur Anzeige angezeigt werden (z. B. unter der Anzeige), je nachdem, wo die Anzeige auf der Seite erscheint. |
| [!UICONTROL Display URL] | Die in der Anzeige enthaltene URL.<br><br>Bei erweiterten dynamischen Suchanzeigen generiert das Werbenetzwerk diesen Wert dynamisch aus der Website-Domäne und Sie müssen keinen Wert eingeben.<br><br>Für erweiterte Textanzeigen und responsive Suchanzeigen müssen Sie keinen Wert eingeben. Die Anzeigen-URL wird automatisch aus der Domäne in der endgültigen URL extrahiert. Optional können Sie die URL mithilfe der Felder Pfad 1 und Pfad 2 anpassen.<br><br><b>Hinweise:</b><ul><li>(Konten mit finalen URLs) Die Domänennamen in der Anzeigen-URL und der endgültigen URL müssen übereinstimmen.</li><li>[!DNL Microsoft Advertising] veraltete erweiterte Textanzeigen im August 2022. Sie können jetzt nur noch Berichte zu diesen Werbeanzeigen erstellen und diese löschen.</li></ul> |
| [!UICONTROL Display Path 1] | (Nur erweiterte Textanzeigen, dynamische Suchanzeigen und responsive Suchanzeigen) Text, der der Display-URL hinzugefügt wird, die automatisch aus der endgültigen URL extrahiert wird. Jeder Pfad wird in der URL durch einen Schrägstrich (/) vorangestellt. Ein Pfad darf keine Schrägstriche (/) oder Zeilenumbruchzeichen (\n) enthalten. Die maximale Länge für jeden Pfad beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.<br><br>Verwenden Sie zum Einfügen eines Anzeigenanpassers die folgenden Formate, wobei &quot;Standardtext&quot;ein optionaler Wert ist, der eingefügt werden kann, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`<br><br>Wenn beispielsweise [!UICONTROL Display Path 1] auf &quot;Angebote&quot;gesetzt ist, lautet die Anzeigen-URL &lt;display url=&quot;&quot;>/transactions, z. B. www.example.com/deals.<br><br>[!DNL Microsoft Advertising] veraltete erweiterte Textanzeigen im August 2022. Sie können jetzt nur noch Berichte zu diesen Werbeanzeigen erstellen und diese löschen. |
| [!UICONTROL Display Path 1] | (Nur erweiterte Textanzeigen, dynamische Suchanzeigen und responsive Suchanzeigen) Ein zusätzlicher Anzeigepfad; siehe Eintrag für [!UICONTROL Display Path 1].<br><br>Beispiel: Wenn [!UICONTROL Display Path 1] auf &quot;Angebote&quot;gesetzt ist und [!UICONTROL Display Path 2] den Wert &quot;lokal&quot;hat, wäre die Anzeige-URL &lt;<i>Anzeigen-URL</i>>/transactions/local, z. B. www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Nur erweiterte Sitelinks) Das erste Datum, an dem Angebote für den Sitelink in der Zeitzone des Werbetreibenden und in einem der folgenden Formate platziert werden können: m/d/yyy, m/d/yy, m-d-yyy oder m-d-yy. Die Standardeinstellung für neue erweiterte Sitelinks ist der aktuelle Tag. <b>Hinweis:</b> Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden. |
| [!UICONTROL End Date] | Das letzte Datum, an dem der Sitelink mit Anzeigen in der Zeitzone des Advertisers und in einem der folgenden Formate angezeigt werden kann: m/d/yyy, m/d/yy, m-d-yyy oder m-d-yy. Bei einem neuen Sitelink ist die Standardeinstellung `[blank]` (d. h. kein Enddatum). |
| [!UICONTROL Call To Action] | Der Aktionsaufruf, der in die Anzeige aufgenommen werden soll. Siehe [API-Referenz für eine Liste möglicher Werte](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), aber geben Sie Aktionsaufrufe mit mehreren Wörtern (z. B. &quot;Bet Now&quot;anstelle von &quot;BetNow&quot;) in Bulksheets ein. |
| [!UICONTROL Call To Action Language] | Die Sprache für die Aktionsoptionen. Siehe [API-Referenz für eine Liste möglicher Sprachen](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | Die Landingpage-URL, auf die Suchmaschinenbenutzer beim Klicken auf Ihre Anzeige zugreifen, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter. Basis-/endgültige URLs auf Suchbegriffebene überschreiben diese auf Anzeigenebene und höher.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Destination URL] | (in generierten Bulksheets zu Informationszwecken enthalten; Bei Konten mit Ziel-URLs ist dies die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Advertisers verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Sie enthält alle für die Kampagne oder das Konto &quot;Search, Social und Commerce&quot;konfigurierten Anlagenparameter. Wenn Sie Tracking-URLs generiert haben, basiert dies auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie suchmaschinenspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Search, Social und Commerce ersetzt werden.<br><br>Bei Konten mit finalen URLs zeigt diese Spalte denselben Wert wie die Spalte Basis-URL/Endgültige URL an. |
| [!UICONTROL Custom URL Param] | Zu ersetzende Daten `{custom_code}` dynamische Variable, wenn die Variable in den Tracking-Parametern für das Suchkonto oder die Kampagneneinstellungen enthalten ist. Um den benutzerdefinierten Wert in die Tracking-URL einzufügen, müssen Sie die Bulksheet-Datei mit der Option Tracking-URLs generieren hochladen. |
| [!UICONTROL Creative Type] | Das Anzeigenformat: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (Shopping-Anzeigen) oder <i>[!UICONTROL Responsive Search Ad]</i>oder <i>[!UICONTROL Text ad]</i>. Die Standardeinstellung für neue Anzeigen ist <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | Das erste Datum, an dem Angebote für die Anzeigengruppe in der Zeitzone des Werbetreibenden und in einem der folgenden Formate platziert werden können: m/d/yyy, m/d/yy, m-d-yyy oder m-d-yy. Bei einer neuen Anzeigengruppe ist das aktuelle Datum der Standardwert. |
| [!UICONTROL Ad Group End Date] | Das letzte Datum, an dem Angebote für die Anzeigengruppe in der Zeitzone des Werbetreibenden und in einem der folgenden Formate platziert werden können: m/d/yyy, m/d/yy, m-d-yyy oder m-d-yy. Bei einer neuen Anzeigengruppe ist der Standardwert [blank] (d. h. kein Enddatum). |
| [!UICONTROL Tracking Template] | (Optional) Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als granularsten) überschreibt die Werte auf allen höheren Ebenen.<br><br>Für das Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot; Search, Social und Commerce hängt beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.<br><br>Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.<br><br>Eine Liste der Parameter zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in der [!DNL Microsoft Advertising] Dokumentation.<br><br> Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Landing Page Suffix] | Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen. Beispiel: `param2=value1&param3=value2`<br><br>Siehe[Klick-Tracking-Formate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren, verwenden Sie die [!DNL Microsoft Advertising] Editor. |
| Netzwerkstatus durchsuchen | Ob Anzeigen für die Anzeigengruppe auf verschiedenen Elementen des Suchnetzwerks platziert werden sollen:<ul><li><i>Alle:</i> Zur Platzierung von Anzeigen in allen Bing-Suchnetzwerken und syndizierten Suchpartnern.</li><li><i>OwnedAndOperatedOnly:</i>So platzieren Sie Anzeigen nur auf Bing und Yahoo! Websites.</li><li><i>SyndicatedSearchOnly:</i> So platzieren Sie Anzeigen nur auf Bing und Yahoo! Syndizierte Suchpartner.</li><li><i>Aus:</i> So platzieren Sie Anzeigen nur im Inhaltsnetzwerk (nicht im Suchnetzwerk).</li></ul> Für neue Anzeigengruppen ist die Standardeinstellung &quot;An&quot;. |
| [!UICONTROL Content Network Status] | Veraltet |
| [!UICONTROL Languages] | Die Zielsprache für Anzeigen in der Anzeigengruppe: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish]oder [!UICONTROL Swedish]. Die Standardeinstellung für neue Kampagnen ist [!UICONTROL English].<br><br>Diese Einstellung bestimmt die Länder und Regionen, in denen Ihre Anzeige angezeigt werden kann. Achten Sie darauf, eine Sprache zu wählen, die mit den Standortzielen der Kampagne kompatibel ist. |
| [!UICONTROL Budget Type] | Ob das Budget <i>[!UICONTROL Daily]</i> (Standardeinstellung) oder <i>[!UICONTROL Monthly]</i>.<br><br>Hinweis: Wenn Sie die Kampagne einem optimierten Portfolio zuweisen, wird dieser Wert automatisch auf [!UICONTROL Daily]. |
| [!UICONTROL Device] | Ein Gerätetyp, für den Angebotsanpassungen auf Kampagnen- oder Anzeigengruppenebene vorgenommen werden: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>oder <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | Die Angebotsanpassung für einen bestimmten Zieltyp. Wenn das Angebot auf Suchbegriffebene beispielsweise 1 USD und die Angebotsanpassung für Smartphones 50 % beträgt, beträgt das Gebot für Smartphones 1,50 USD. Standardmäßig beziehen sich alle Ziele auf das Angebot auf Suchbegriffebene. Gültige Prozentsätze können Folgendes umfassen:<ul><li>Smartphones und Tablets: -100 (kein Gebot für den Gerätetyp) und von -90 bis 900</li><li>Desktop: von 0 bis 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | Die Gerätetypen, auf denen Sie die Anzeige oder den Sitelink bevorzugen: <i>[!UICONTROL All]</i> (Standardeinstellung) oder <i>[!UICONTROL Mobile]</i>. Wenn &quot;Mobile&quot;angegeben ist, versucht das Netzwerk, die Anzeige oder den Sitelink für Benutzer mobiler Geräte und nicht für Benutzer von Desktop- oder Tablet-Geräten anzuzeigen. Andernfalls zeigt das Netzwerk die Anzeige oder den Sitelink auf jedem Gerätetyp an. <b>Hinweis:</b> Das Netzwerk garantiert nicht, dass die Anzeige auf dem bevorzugten Gerätetyp angezeigt wird. |
| [!UICONTROL Param2] | Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL des Suchbegriffs oder der Titel, die Beschreibung oder die Basis-URL der Anzeige die Variable `{Param2}` dynamische Ersatzzeichenfolge. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge des Anzeigenelements, in dem Sie es verwenden werden (Titel 1 und Titel 2 zusammen können maximal 76 Zeichen lang sein). Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Param3] | Die Zeichenfolge, die als Ersatzwert verwendet wird, wenn die Basis-URL des Suchbegriffs oder der Titel, die Beschreibung oder die Basis-URL der Anzeige die Variable `{Param3}` dynamische Ersatzzeichenfolge. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge des Anzeigenelements, in dem Sie es verwenden werden (Titel 1 und Titel 2 zusammen können maximal 76 Zeichen lang sein). Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Link Name] | Der Sitelink-Text. Sie muss innerhalb der Kampagne eindeutig sein. Wenn Sie &quot;Description1&quot;und &quot;Description2&quot;angeben, kann der Sitelink-Text bis zu 25 Einzelbyte- oder 12 Doppelbyte-Zeichen enthalten. Andernfalls kann der Sitelink-Text bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.<br><br>[!DNL Microsoft Advertising] kann zwei, vier oder sechs erweiterte Sitelinks mit Beschreibungen oder vier oder sechs Sitelinks ohne Beschreibungen in einer Zeile mit einer Anzeige anzeigen.<br><br>Sie können neue erweiterte Sitelinks nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellen. |
| [!UICONTROL Campaign Status] | Der Anzeigestatus der Kampagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i> (nur bestehende Kampagnen). Die Standardeinstellung für neue Kampagnen ist [!UICONTROL Active]. Um eine aktive oder ausgesetzte Kampagne zu löschen, geben Sie den Wert ein `Deleted`. |
| [!UICONTROL Ad Group Status] | Der Anzeigestatus der Anzeigengruppe: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i> (nur bestehende Anzeigengruppen). Die Standardeinstellung für neue Anzeigengruppen ist [!UICONTROL Active]. Um eine aktive oder ausgesetzte Anzeigengruppe zu löschen, geben Sie den Wert ein `Deleted`. |
| [!UICONTROL Keyword Status] | Der Anzeigestatus des Suchbegriffs: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Suchbegriffe). Die Standardeinstellung für neue Suchbegriffe ist [!UICONTROL Active]. Um einen aktiven oder ausgesetzten Suchbegriff zu löschen, geben Sie den Wert ein `Deleted`. <b>Hinweis:</b> Wenn Sie Tracking-URLs für einen Suchbegriff mit mehreren Übereinstimmungstypen erstellen, muss der Suchbegriffstatus für jeden Übereinstimmungstyp identisch sein. |
| [!UICONTROL Placement Status] | Veraltet |
| [!UICONTROL Ad Status] | Der Anzeigestatus der Anzeige: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigen), <i>[!UICONTROL Disapproved]</i> (nicht bearbeitbar) oder <i>[!UICONTROL Paused]</i>. Die Standardeinstellung für neue Anzeigen ist [!UICONTROL Active]. Um eine aktive oder ausgesetzte Anzeige zu löschen, geben Sie den Wert ein `Deleted`. |
| [!UICONTROL Target Status] | Der Status eines dynamischen Suchziels: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i> (nur bestehende Ziele). Die Standardeinstellung für neue Ziele ist [!UICONTROL Active]. Um ein aktives oder ausgesetztes Ziel zu löschen, geben Sie den Wert ein `Deleted`. |
| [!UICONTROL Sitelink Status] | Der Anzeigestatus des Sitelink: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur bestehende Sitelinks). Die Standardeinstellung für neue Sitelinks ist [!UICONTROL Active]. Um einen aktiven Sitelink zu löschen, geben Sie den Wert ein `Deleted`. |
| [!UICONTROL Location Status] | Der Status des Standort-Ziels: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Speicherorte). Die Standardeinstellung für neue Speicherorte ist [!UICONTROL Active]. Um eine aktive Position zu löschen, geben Sie den Wert ein `Deleted`. |
| [!UICONTROL Product Group Status] | Der Anzeigestatus der Produktgruppe: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur bestehende Produktgruppen). Die Standardeinstellung für neue Produktgruppen ist [!UICONTROL Active]. Um eine aktive Produktgruppe zu löschen, geben Sie den Wert ein `Deleted`. |
| [!UICONTROL Device Target Status] | Der Status des Geräteziels auf Kampagnen- oder Anzeigengruppenebene: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i>. Für neue Kampagnen und Anzeigengruppen ist die Standardeinstellung [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | Der Status des RLSA-Ziels auf Kampagnen- oder Anzeigengruppenebene oder des Ausschlusses (nur Google Ads): <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur bestehende Ziele). Die Standardeinstellung für neue Ziele oder Ausschlüsse ist [!UICONTROL Active]. Um eine aktive Zielgruppe oder einen Ausschluss zu löschen, geben Sie den Wert ein `Deleted`. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | (Benannt für eine Advertiser-spezifische Beschriftungs-Classification, z. B. &quot;Farbe&quot;für eine Beschriftungsklassifizierung namens &quot;Farbe&quot;) Ein Wert für die angegebene Classification, die mit der Entität verknüpft ist. Sie können pro Entität nur einen Wert angeben (z. B. &quot;rot&quot;für die Klassifizierung der Farbbeschriftung für Kampagne A). Die maximale Länge beträgt 100 Zeichen. Der Wert kann ASCII- und Nicht-ASCII-Zeichen enthalten.<br><br>Beschriftungsklassifizierungen und ihre Beschriftungswerte werden auf alle untergeordneten Komponenten angewendet. neue Komponenten, die später hinzugefügt werden, werden automatisch mit der Beschriftung verknüpft. Beschriftungsklassifizierungen für Produktgruppen werden auf die Einheitenebene (am detailliertesten) angewendet.<br><br>Weder der Classification-Name noch der Classification-Wert unterscheiden zwischen Groß- und Kleinschreibung. |
| [!UICONTROL Constraints] | Eine Beschränkung, die der Entität zugewiesen wird. Sie können pro Entität nur eine Begrenzung zuweisen.<br><b>>Einschränkungen werden von untergeordneten Entitäten übernommen. Sie müssen daher keine Werte für untergeordnete Entitäten eingeben, es sei denn, Sie möchten die vererbten Werte überschreiben. |
| [!UICONTROL Campaign ID] | Die eindeutige ID, die eine bestehende Kampagne identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält eine[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Ad Group ID] | Die eindeutige ID, die eine bestehende Anzeigengruppe identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält eine[!UICONTROL AMO ID]&quot;für die Anzeigengruppe. |
| [!UICONTROL Placement ID] | Veraltet |
| [!UICONTROL Keyword ID] | Die eindeutige ID, die einen vorhandenen Suchbegriff identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Suchbegriff ändern, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Suchbegriff zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>Die eindeutige ID, die eine vorhandene Anzeige identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Für responsive Suchanzeigen ist entweder die Anzeigen-ID oder die AMO-ID erforderlich, um Anzeigendaten zu bearbeiten oder zu löschen. Bei allen anderen Entitätstypen ist die AMO-ID nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID]&quot;.&quot; Wenn Sie jedoch weder die [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen.</p><p><b>Hinweis:</b> Wenn Sie a) Anzeigeneigenschaftsspalten bearbeiten, außer Status für eine vorhandene Anzeige oder b) alle Daten für eine responsive Suchanzeige und Sie weder die [!UICONTROL Ad ID] nor [!UICONTROL AMO ID], wird eine neue Anzeige erstellt und die vorhandene Anzeige wird nicht geändert. </p> |
| [!UICONTROL Sitelink ID] | Die eindeutige ID, die einen vorhandenen Sitelink identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Sitelink zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID]&quot;.&quot; Wenn Sie jedoch [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]und die Eigenschaftsspalten mit mehreren Sitelinks übereinstimmen, ändert sich nur der Status für eine der Sitelinks.</p><p><b>Hinweis:</b> Wenn Sie die Sitelink-Eigenschaftsspalten bearbeiten, mit Ausnahme des Status für einen vorhandenen Sitelink und Sie weder die [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID], wird ein neuer Sitelink erstellt und die bestehende Sitelink wird nicht geändert. |
| [!UICONTROL Product Group ID] | Die eindeutige ID, die eine bestehende Produktgruppe identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um die Produktgruppe zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| Standort-ID | Die eindeutige [!DNL Microsoft Advertising] Kennung für das Ortsziel. Um eine Standortliste herunterzuladen, melden Sie sich bei der [!DNL Microsoft Advertising] Entwicklerportal mit [!DNL Microsoft Advertising] Anmeldedaten für Werbekonten. Nur erforderlich, wenn Sie das Ortsziel ändern oder löschen, es sei denn, die Zeile enthält eine[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Target ID] | Die eindeutige ID, die ein vorhandenes automatisches Ziel identifiziert. Nur erforderlich, wenn Sie das automatische Ziel ändern oder löschen, es sei denn, die Zeile enthält eine[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL RLSA Target ID] | Die eindeutige ID, die ein vorhandenes RLSA-Ziel auf Kampagnen- oder Anzeigengruppenebene identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie die Zielgruppe oder den Ausschluss ändern oder löschen, es sei denn, die Zeile enthält eine[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | (In generierten Bulksheets) Eine von der Adobe generierte eindeutige Kennung für eine synchronisierte Entität. Bei responsiven Suchanzeigen ist die AMO-ID zum Bearbeiten oder Löschen von Anzeigen erforderlich, es sei denn, Sie enthalten die Anzeigen-ID. Um Daten für alle anderen Entitätstypen mit AMO-ID zu bearbeiten, muss die AMO-ID die Daten bearbeiten oder löschen, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |
| [!UICONTROL EF Error Message] | (Zu Informationszwecken in generierten Bulksheets enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Anzeigennetzwerk bezüglich Daten aus der Zeile; Fehlermeldungen sind in [!UICONTROL EF Errors] Dateien. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |
| [!UICONTROL SE Error Message] | (Zu Informationszwecken in generierten Bulksheets enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Anzeigennetzwerk bezüglich Daten aus der Zeile; Fehlermeldungen sind in [!UICONTROL SE Errors] Dateien. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |
| [!UICONTROL Exemption Request] | (Enthalten in generierten Bulksheets für Informationszwecke) Platzhalter für die Anzeige der Namen und des Texts von Google-Werberichtlinien, gegen die eine Anzeige verstößt. |
| [!UICONTROL Retail Hash] | (Zu Informationszwecken in mit dem erweiterten Campaign Management generierten Bulksheets enthalten) Ein alphanumerischer Hash-Code (z. B. f9639f40cdf56524b541e5dacf55a991), der anzeigt, dass das Element mithilfe der Erweiterten (ACM) Ansicht generiert wurde. |

<table style="table-layout:auto">

[^1]: [!DNL Excel] konvertiert große Zahlen in wissenschaftliche Notation (z. B. 2.12E+09 für 2115585666), wenn die Datei geöffnet wird. Um Ziffern in der Standardnotation anzuzeigen, wählen Sie eine beliebige Zelle in der Spalte aus und klicken Sie in die Formelleiste.

## Felder, die zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente erforderlich sind {#bulksheet-fields-per-component-microsoft}

>[!NOTE]
>
>Wenn ein Feld nicht auf eine Aktion anwendbar ist, werden alle im Feld eingegebenen Werte ignoriert.

### Kampagnenfelder

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| [!UICONTROL Campaign Budget] | Erforderlich zum Erstellen einer Kampagne. | Eine tägliche Ausgabenbegrenzung für die Kampagne mit oder ohne monetäre Symbole und Satzzeichen. Dieser Wert setzt das Kontobudget außer Kraft. |
| [!UICONTROL Channel Type] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Delivery Method] | Optional |
| [!UICONTROL Campaign Priority] | Erforderlich, um eine Warenkampagne zu erstellen. |
| [!UICONTROL Merchant ID] | Erforderlich, um eine Warenkampagne zu erstellen. |
| [!UICONTROL Sales Country] | Erforderlich, um eine Warenkampagne zu erstellen. |
| [!UICONTROL Product Scope Filter] | (Shopping-Kampagnen) Optional |
| [!UICONTROL DSA Domain Name] | Erforderlich für die Erstellung einer Kampagne des Typs a) &quot;[!UICONTROL DynamicSearchAds]&quot; oder b) &quot;[!UICONTROL Search]&quot;, wenn die [!DNL ExperimentId] -Element nicht festgelegt ist) |
| [!UICONTROL DSA Domain Language] | Erforderlich für die Erstellung einer Kampagne des Typs a) &quot;[!UICONTROL DynamicSearchAds]&quot; oder b) &quot;[!UICONTROL Search]&quot;, wenn die [!DNL ExperimentId] -Element nicht festgelegt ist) |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Landing Page Suffix] | <p>Optional |
| [!UICONTROL Budget Type] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Device] | Optional |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Campaign Status] | Nur zum Löschen einer Kampagne erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält eine[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Anzeigengruppenfelder

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Group Type] | Erforderlich zum Erstellen einer Anzeigengruppe. |
| [!UICONTROL Audience Target Method] | Nur zum Erstellen von Zielgruppen-Anzeigengruppen erforderlich. |
| [!UICONTROL Ad Group Start Date] | Optional |
| [!UICONTROL Ad Group End Date] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Search Network Status] | (Nur Kampagnen im Suchnetzwerk) Optional |
| [!UICONTROL Languages] | Optional |
| [!UICONTROL Device] | Optional |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Ad Group Status] | Nur zum Löschen einer Anzeigengruppe erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Ad Group ID] | Nur erforderlich, wenn Sie den Anzeigengruppennamen ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Anzeigengruppe. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Suchbegriffsfelder

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Keyword] | Erforderlich |
| [!UICONTROL Match Type] | Zum Bearbeiten oder Löschen eines Suchbegriffs mit mehreren Übereinstimmungstypen ist ein Wert für den Übereinstimmungstyp oder die Keyword-ID erforderlich. |
| [!UICONTROL Max CPC] | Optional |
| [!UICONTROL Base URL/Final URL] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Param1] | Optional |
| [!UICONTROL Param2] | Optional |
| [!UICONTROL Keyword Status] | Nur zum Löschen eines Suchbegriffs erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Keyword ID] | Nur erforderlich, wenn Sie den Suchbegriff bearbeiten oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Suchbegriff zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Dynamische Suchanzeigenfelder

>[!NOTE]
>
>Support erstellen ist nicht verfügbar.

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Creative (except RSA)]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Erforderlich, um die Beschreibung zu bearbeiten. <b>Hinweis:</b> Bei diesem Anzeigentyp löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue. |
| [!UICONTROL Display Path 1] | Erforderlich, um das Feld zu bearbeiten. |
| [!UICONTROL Display Path 2] | Erforderlich, um das Feld zu bearbeiten. |
| [!UICONTROL Creative Type] | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Creative Preferred Devices] | Optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID].&quot; Wenn Sie jedoch weder die [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich dann der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Produkt- (Einkaufs-)Anzeigenfelder

Weitere Informationen zum Erstellen von Shopping-Anzeigen finden Sie unter &quot;[Implementierung [!DNL Microsoft Advertising] Warenkorb](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).&quot;

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Creative (except RSA)]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Promotion Line] | Optional |
| [!UICONTROL Base URL/Final URL] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Creative Type] | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID].&quot; Wenn Sie jedoch weder die [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich dann der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Responsive (Multimedia) Anzeigenfelder

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Creative (except RSA)]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Für responsive Anzeigen [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]und [!UICONTROL Ad Title 3] sind erforderlich, um Anzeigen zu erstellen, und alle anderen Felder für Anzeigentitel sind optional. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). <b>Hinweis:</b> Bei diesem Anzeigentyp löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] zum Erstellen von Anzeigen erforderlich sind und [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional. <b>Hinweis:</b> Bei diesem Anzeigentyp löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue. |
| [!UICONTROL Business Name] | Erforderlich zum Erstellen oder Löschen einer Anzeige. |
| [!UICONTROL Call To Action] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Call To Action Language] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Base URL/Final URL] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Creative Type] | Optional. |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichende Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID].&quot; Wenn Sie jedoch weder die [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich dann der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Responsive Suchanzeigenfelder

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Responsive Search Ad]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Für responsive Suchanzeigen, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]und [!UICONTROL Ad Title 3] zum Erstellen einer Anzeige erforderlich sind und alle anderen Felder für den Anzeigentitel optional sind. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Optional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Für responsive Suchanzeigen, [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] zum Erstellen einer Anzeige erforderlich sind und [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional. Um den vorhandenen Wert zu löschen, verwenden Sie den Wert `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Optional |
| [!UICONTROL Display Path 1] | Optional |
| [!UICONTROL Display Path 2] | Optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Creative Type] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, Sie enthalten die Anzeigen-ID. |

### Textanzeigenfelder

Verwenden Sie für diesen Anzeigentyp den[!UICONTROL Creative (except RSA)]&quot; in der [!UICONTROL Download Bulksheet] angezeigt.

>[!NOTE]
>
>Erweiterte Textanzeigen werden nicht mehr unterstützt. Sie können nur vorhandene Textanzeigen löschen.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Schreibgeschützt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Schreibgeschützt |
| [!UICONTROL Display URL] | Schreibgeschützt |
| [!UICONTROL Display Path 1] | Schreibgeschützt |
| [!UICONTROL Display Path 2] | Schreibgeschützt |
| [!UICONTROL Base URL/Final URL] | Schreibgeschützt |
| [!UICONTROL Custom URL Param] | Schreibgeschützt |
| [!UICONTROL Creative Type] | Optional |
| [!UICONTROL Tracking Template] | Schreibgeschützt |
| [!UICONTROL Creative Preferred Devices] | Schreibgeschützt |
| [!UICONTROL Ad Status] | Erforderlich |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Anzeigen-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Felder für dynamisches Suchziel (automatisches Targeting)

>[!NOTE]
>
>Support erstellen ist nicht verfügbar.

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Auto Target Expression] | Erforderlich. |
| [!UICONTROL Match Type] | Optional |
| [!UICONTROL Max CPC] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Target Status] | Löschen einer Zielgruppe erforderlich |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Target ID] | Nur erforderlich, wenn Sie das automatische Ziel ändern oder löschen, es sei denn, die Zeile enthält eine[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Produktgruppenfelder kaufen

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Match Type] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Max CPC] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Parent Product Groupings] | Erforderlich |
| [!UICONTROL Product Grouping] | Erforderlich |
| [!UICONTROL Partition Type] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Base URL/Final URL] | Erforderlich |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Product Group Status] | Nur zum Löschen einer Produktgruppe erforderlich. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Product Group ID] | Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um die Produktgruppe zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Sitelink-Felder auf Kampagnenebene

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| Beschreibung Zeile 1 | Optional |
| [!UICONTROL Description Line 2] | Optional |
| [!UICONTROL Start Date] | Optional |
| [!UICONTROL End Date] | Optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Creative Preferred Devices] | Optional |
| [!UICONTROL Link Name] | Erforderlich |
| [!UICONTROL Sitelink Status] | Nur zum Löschen eines Sitelink-Links erforderlich. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Sitelink ID] | Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Sitelink zu identifizieren, oder b) eine &quot;[!UICONTROL AMO ID].&quot; Wenn Sie jedoch [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]  und die Eigenschaftsspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status nur für eine der Sitelinks.<br><br><b>Hinweis:</b> Wenn Sie die Sitelink-Eigenschaftsspalten bearbeiten, mit Ausnahme des Status für einen vorhandenen Sitelink, und Sie [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID], wird ein neuer Sitelink erstellt und die bestehende Sitelink wird nicht geändert. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Zielgruppenfelder der Position

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Location] | Erforderlich |
| [!UICONTROL Location Type] | Erforderlich zum Erstellen einer Zielgruppe |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Location Status] | Nur zum Löschen eines Orts-Ziels erforderlich. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die Kampagnen-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### Zielfelder auf Kampagnenebene und auf Anzeigengruppenebene

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Device] | Erforderlich zum Löschen eines Geräteziels. |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Ad Group Name] | Erforderlich für Geräteziele auf Anzeigengruppenebene. Gilt nicht für Geräteziele auf Kampagnenebene. |
| [!UICONTROL Device Target Status] | Nur zum Löschen eines Geräteziels erforderlich. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Fakultativ; gilt nur für Geräteziele auf Anzeigengruppenebene. |
| [!UICONTROL AMO ID] | Erforderlich, um die Daten zu bearbeiten oder zu löschen, es sei denn, Sie enthalten die Geräteziel-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

### RLSA-Zielfelder auf Kampagnenebene und Anzeigengruppenebene

| Feld | Erforderlich? | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich für Ziele auf Anzeigengruppenebene. Gilt nicht für Ziele auf Kampagnenebene. |
| [!UICONTROL Audience] | Erforderlich, um ein neues Ziel zu erstellen. |
| [!UICONTROL Target Type] | Optional |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL RLSA Target Status] | Erforderlich zum Löschen eines Ziels. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Fakultativ; gilt nur für Ziele auf Anzeigengruppenebene. |
| [!UICONTROL RLSA Target ID] | Nur erforderlich, wenn Sie die Zielgruppe ändern oder löschen, es sei denn, die Zeile enthält eine[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie enthalten die RLSA-Target-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |

>[!MORELIKETHIS]
>
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Vorgänge, die Sie in Bulksheets ausführen können](bulksheet-operations.md)
>* [Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
>* [Klick-Tracking-Formate für [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Hochladen einer Bulksheet-Datei oder einer korrigierten Fehlerdatei](../bulksheet-upload.md)
