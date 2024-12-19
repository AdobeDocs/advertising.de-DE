---
title: 'Erforderliche Bulksheet-Daten für  [!DNL Microsoft Advertising] '
description: Referenzieren Sie die erforderlichen Kopfzeilenfelder und Datenfelder in Bulksheets für  [!DNL Microsoft Advertising]  Konten.
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '6928'
ht-degree: 0%

---

# Anhang - Erforderliche Bulksheet-Daten für [!DNL Microsoft Advertising]

Um [!DNL Microsoft Advertising] Kampagnendaten stapelweise zu erstellen und zu aktualisieren, können Sie Bulksheet-Dateien für Search, Social und Commerce verwenden, die speziell für [!DNL Microsoft Advertising]-Konten formatiert sind. Sie können entweder a) [Bulksheet-Dateien für bestehende Konten ](../bulksheet-download.md) dem erforderlichen Dateiformat generieren oder b) sie manuell erstellen (siehe &quot;[Unterstützte Bulksheet-](bulksheet-file-formats.md)&quot; für allgemeine Informationen über die unterstützten Dateiformate).

Jedes Bulksheet muss die Header-Felder und die entsprechenden Datenfelder enthalten, die für die [spezifischen Vorgänge, die Sie durchführen möchten, (](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md). B. das Erstellen einer Anzeige) erforderlich sind. Wenn ein Feld nicht erforderlich ist, können Sie es in der Kopfzeile und in den Datenzeilen auslassen. Alle benutzerdefinierten Spalten werden beim Hochladen der Bulk-Sheet-Datei gelöscht.

Im Folgenden finden Sie eine Tabelle mit allen verfügbaren Datenfeldern und zusätzlichen Tabellen, die angeben, welche Felder zum Hinzufügen, Bearbeiten oder Löschen von Daten für einzelne Entitäten (z. B. Kampagnen und Keywords) erforderlich sind.

## Alle verfügbaren Datenfelder {#bulksheet-fields-all-microsoft}

In der folgenden Tabelle werden alle verfügbaren Datenfelder beschrieben.

Die für Kontoentitäten relevanten Datenfelder finden Sie unter &quot;[Felder, die zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente erforderlich sind](#bulksheet-fields-per-component-microsoft)&quot;.

| Feld | Beschreibung |
|----|----|
| [!UICONTROL Platform] | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Acct Name] | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. Die maximale Länge beträgt 128 Zeichen. |
| [!UICONTROL Campaign Budget] | Das tägliche oder monatliche Kampagnenbudget, mit oder ohne Währungssymbole und Satzzeichen. Es kann nicht weniger als 0,05 sein. |
| [!UICONTROL Channel Type] | Der Kanaltyp, auf den die Kampagne abzielt: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i> oder <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Nur Kampagnen mit täglichen Budgets) Wie schnell Anzeigen für die Kampagne jeden Tag angezeigt werden:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (Standard für neue Kampagnen): Um Ihre Anzeigen-Impressions über den Tag zu verteilen.</li><li><i>[!UICONTROL Accelerated]:</i> Ihre Anzeigen so oft wie möglich anzuzeigen, bis Ihr Budget erreicht ist. Daher werden Ihre Anzeigen möglicherweise nicht zu einem späteren Zeitpunkt angezeigt.</li></ul> |
| [!UICONTROL Campaign Priority] | (Nur Einkaufskampagnen) Die Priorität, mit der die Kampagne verwendet wird, wenn mehrere Kampagnen für dasselbe Produkt werben: <i>[!UICONTROL Low]</i> (der Standard für neue Kampagnen), <i>[!UICONTROL Medium]</i> oder <i>[!UICONTROL High]</i>.<br><br>Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Anzeigennetzwerk zuerst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion geeignet ist. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot geeignet. |
| [!UICONTROL Merchant ID] | (Nur Shopping-Kampagnen und Audience-Kampagnen, die mit einem Händler-Feed verknüpft sind) Die Kunden-ID des Händler-Kontos, dessen Produkte für die Kampagne verwendet werden. |
| [!UICONTROL Sales Country] | (Nur Shopping-Kampagnen; bei bestehenden Kampagnen schreibgeschützt) Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, für welche Produkte in der Kampagne geworben wird. |
| [!UICONTROL Product Scope Filter] | (Nur Kampagnen, die das Shopping-Netzwerk verwenden) Die Produkte in Ihrem Händlerkonto, für die Produktanzeigen für die Kampagne erstellt werden können. Mit dem Format dimension=attribute können Sie bis zu sieben Produktdimensions- und Attributkombinationen eingeben, nach denen Ihre Produkte gefiltert werden sollen. Trennen Sie mehrere Filter durch ein Trennzeichen &quot;>>&quot;. Eine Liste der verfügbaren Produktdimensionen finden Sie unter &quot;[ von Kampagnenproduktfiltern](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).<br><br> Beispiel: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Um die vorhandenen Werte zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL DSA Domain Name] | (Kampagnen vom Typ a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; oder b) &quot;<i>[!UICONTROL Search]</i>&quot;, wenn das [!DNL ExperimentId] nicht festgelegt ist) Der Domain-Name der Website, die für dynamische Suchanzeigen ausgewählt werden soll. Die maximale Länge beträgt 2.048 Zeichen. Wenn der Domain-Name `www` enthält, wird er gekürzt und nicht verwendet.<br><br>Für bestehende Kampagnen können Sie die Domain nicht bearbeiten, müssen sie jedoch einbeziehen, um andere Eigenschaften zu aktualisieren. |
| [!UICONTROL DSA Domain Language] | (Kampagnen vom Typ a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; oder b) &quot;<i>[!UICONTROL Search]</i>&quot;, wenn das [!DNL ExperimentId] nicht festgelegt ist) Die Sprache der Website-Seiten, die für dynamische Suchanzeigen ausgewählt werden sollen. Die unterstützten Domänensprachen sind [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish] und [!UICONTROL Swedish].<br><br>Für bestehende Kampagnen können Sie die Sprache nicht bearbeiten, müssen sie jedoch einbeziehen, um andere Eigenschaften zu aktualisieren. |
| [!UICONTROL Ad Group Name] | Der eindeutige Name, der eine Anzeigengruppe identifiziert. Die maximale Länge beträgt 128 Zeichen. Nachfolgende leere Zeichen werden nicht gespeichert (z. B. wird „Anzeigengruppe 1 &quot; als „Anzeigengruppe 1 &quot; gespeichert). |
| [!UICONTROL Ad Group Type] | (Kampagnen im Suchnetzwerk; nur lesen für bestehende Anzeigengruppen) Der Anzeigengruppentyp: <i>[!UICONTROL Audience]</i> (nur für Zielgruppenkampagnen), <i>[!UICONTROL Search Dynamic]</i> (nur für dynamische Suchanzeigen) und <i>[!UICONTROL Search Standard]</i> (nur für responsive Suchanzeigen und vorhandene erweiterte Textanzeigen). Einige Kampagnentypen können mehrere Anzeigengruppentypen umfassen. |
| [!UICONTROL Keyword] | (Nur Kampagnen im Suchnetzwerk) Die Keyword-Zeichenfolge. Die maximale Länge beträgt 50 Zeichen.<br><br><b>Hinweise:</b><ul><li>Um ein Keyword auf Anzeigengruppen- oder Kampagnenebene auszuschließen, setzen Sie den [!UICONTROL Match Type] auf `Negative`. Wenn die Zeile den Namen der Anzeigengruppe enthält, wird das Keyword für die Anzeigengruppe ausgeschlossen. Wenn die Zeile nicht den Namen der Anzeigengruppe enthält, wird das Keyword für die gesamte Kampagne ausgeschlossen.</li><li>Wenn Sie ein [!DNL Microsoft Advertising] Schlüsselwort ändern, wird das vorhandene Schlüsselwort gelöscht und ein neues mit einer neuen Schlüsselwort-ID erstellt. Das Ändern des Übereinstimmungstyps löscht jedoch nicht das vorhandene Keyword.</li></ul> |
| Platzierung | Veraltet |
| [!UICONTROL Audience] | Die Remarketing-Liste für Suchanzeigen (RLSA) richtet sich an die Zielgruppe der Kampagne oder Anzeigengruppe. |
| [!UICONTROL Target Type] | (Nur RLSA-Ziele) Der Zieltyp: <i>[!UICONTROL Inclusion]</i> oder <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Dynamische Suchziele für die Anzeigengruppe. Verwenden Sie für alle Ziele &quot;[!UICONTROL All Web Pages]&quot;.<br><br>Um bis zu drei dynamische Suchkriterien auszuwählen, verwenden Sie die `<category>=<target>` Format , wobei &lt;category> jede der folgenden Kategorien enthalten kann. Mehrere Ziele für eine einzelne Kategorie mit &quot;`[blank space] and [blank space]`&quot; verbinden und mehrere Kategorien mit &quot;`[blank space] and [blank space]`&quot; verbinden.<br><ul><li><i>Kategorie:</i> So zeigen Sie dynamische Suchanzeigen für indizierte Seiten mit einer bestimmten Google-Inhaltskategorie an.</li><li><i>URL:</i> um dynamische Suchanzeigen für indizierte Seiten mit einer bestimmten URL anzuzeigen, wobei der Wert an einer beliebigen Stelle in der URL enthalten sein kann.</li><li><i>Seitentitel:</i> Anzeigen dynamischer Suchanzeigen für indizierte Seiten mit bestimmtem Text im Seitentitel.</li><li><i>Seiteninhalt:</i> Anzeigen dynamischer Suchanzeigen für indizierte Seiten mit bestimmtem Inhalt.</li></ul>Beispiel: url=shoes.example.com und page title=<br>-Beispiel: Alle Web-Seiten |
| [!UICONTROL Location] | Ein geografischer Ort, an dem Anzeigen für die Kampagne oder Anzeigengruppe geschaltet werden sollen. Die Werte unterscheiden nicht zwischen Groß- und Kleinschreibung. Wenn Sie keine Werte für die Kampagne oder Anzeigengruppe eingeben, werden alle Standorte als Zielgruppe ausgewählt. Um bestimmte Standorte auszuwählen, geben Sie den Standort mithilfe der [!DNL Microsoft Advertising]-Code-Formate ein. Um eine Standortliste herunterzuladen, melden Sie sich mit Ihren Anmeldedaten für das [!DNL Microsoft Advertising] Advertising-Konto beim [!DNL Microsoft Advertising]-Entwicklerportal an. <b>Hinweis:</b> Um einen Standort auszuschließen, stellen Sie dem Standort-Code ein Minuszeichen (`-`) voran, z. B. `-United States`. |
| [!UICONTROL Location Type] | Der Standorttyp, z. B. Stadt, Land, MetroArea, Postleitzahl und Bundesland. Um eine Standortliste herunterzuladen, melden Sie sich mit Ihren Anmeldedaten für das [!DNL Microsoft Advertising] Advertising-Konto beim [!DNL Microsoft Advertising]-Entwicklerportal an. |
| [!UICONTROL Match Type] | (Nur Kampagnen im Suchnetzwerk) Die Keyword-übereinstimmenden Optionen. Dies kann die Keyword-Matching-Option für eine dynamische Suchzielgruppe oder Produktgruppe enthalten. Zu den Werten gehören: <i>[!UICONTROL Broad]</i> (der Standard für neue Keywords), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (wird automatisch für Keywords festgelegt, wenn die Anzeigengruppe das Inhaltsnetzwerk anspricht), <i>[!UICONTROL Negative]</i> (um ein Keyword im Inhaltsnetzwerk auszuschließen), <i>[!UICONTROL Dynamic Ad Target]</i> (der Standard für neue dynamische Suchziele), <i>[!UICONTROL Product Group]</i> (der Standard für neue Produktgruppen) oder <i>[!UICONTROL Negative Product Group]</i> (um eine Produktgruppe auszuschließen).  Zum Bearbeiten oder Löschen eines Keywords mit mehreren Übereinstimmungstypen ist ein Wert für entweder den Übereinstimmungstyp oder die Keyword-ID erforderlich.<br><br>Wählen Sie für den Modifikator „Weite Übereinstimmung“ die Option „Weite Übereinstimmung“ und fügen Sie vor jedem Wort innerhalb des erforderlichen Keywords ein `+` ein (z. B. &quot;`+red +shoes`&quot;, um sowohl „Rot“ als auch „Schuhe“ zu erfordern).<br><br>Wenn Sie den Übereinstimmungstyp für ein [!DNL Microsoft Advertising] Schlüsselwort ändern, wird das vorhandene Schlüsselwort nicht gelöscht. |
| [!UICONTROL Max CPC] | (Kampagnen im Suchnetzwerk) Die maximalen Kosten pro Klick (CPC), die den höchsten Betrag darstellen, der für einen Anzeigenklick basierend auf dem Keyword, der Produktgruppe oder dem dynamischen Suchziel mit oder ohne Währungssymbole und Satzzeichen bezahlt werden muss.  Für bestehende Keywords und Produktgruppen-Datensätze in optimierten Portfolios sind Aktualisierungen nur für einen Tag wirksam und werden im nächsten Optimierungszyklus überschrieben. <b>Hinweis:</b> Sie können keine Angebote für negative Keywords festlegen. |
| [!UICONTROL Max Content CPC] | (Schreibgeschützt für CPC-Kampagnen, die erstellt wurden, bevor das Content Network im Jahr 2017 eingestellt wurde) Die maximalen Inhaltskosten pro Klick (CPC), die den höchsten Betrag darstellen, der für einen Anzeigenklick von einer Display-Netzwerk-Site mit oder ohne Währungssymbole und Satzzeichen bezahlt werden muss. |
| [!UICONTROL Audience Target Method] | (Zielgruppe und Gruppen) Ob:<ul><li><i>[!UICONTROL Target and Bid]:</i> Anzeigen nur Benutzern anzuzeigen, die mit Zielgruppen verknüpft sind und auch andere Ziele für die Anzeigengruppe erfüllen.</li><li><i>[!UICONTROL Bid Only]:</i>Anzeigen auch Personen anzuzeigen, die nicht mit Zielgruppen verknüpft sind, solange sie andere Zielgruppen auf Anzeigengruppenebene erfüllen.</li></ul> Sie können jedoch die Wahrscheinlichkeit erhöhen, dass Anzeigen bestimmten Zielgruppen angezeigt werden, indem Sie höhere Gebote für diese Zielgruppen festlegen. |
| [!UICONTROL Parent Product Groupings] | Die Hierarchie der übergeordneten Produktgruppen.<br><br>Beispiel: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | Die Produktgruppe (z. B. „brand=acme“ oder „Alle Produkte„).<br><br><b>Hinweise:</b><ul><li>Wenn eine bestimmte Produktgruppe nicht in der Hierarchie übergeordneter Produktgruppierungen vorhanden ist, erstellt Search, Social und Commerce die erforderlichen Teile der Hierarchie.</li><li>Search, Social und Commerce erstellt automatisch eine Gruppe &quot;[!UICONTROL All Products]&quot;, wenn Sie in einer Shopping-Kampagne eine Anzeigengruppe erstellen, deren Standardangebot auf das Standardangebot der Anzeigengruppe festgelegt ist. Search, Social und Commerce erstellt automatisch eine Gruppe &quot;[!UICONTROL Everything Else]&quot; mit dem Standardgebot der Anzeigengruppe auf jeder Ebene der Produktgruppenhierarchie. Sie können diese Standardgruppen weiterhin explizit erstellen und sie entweder ausschließen oder ihre Angebote ändern.</li><li>Jede Anzeigengruppe kann bis zu acht Ebenen von Produktgruppen enthalten, einschließlich &quot;[!UICONTROL All Products]&quot; und sieben weiteren Ebenen.</li></ul> |
| [!UICONTROL Partition Type] | Der Partitionstyp für die Produktgruppe: <i>[!UICONTROL subdivision]</i> (wenn untergeordnete Produktgruppen vorhanden sind) oder <i>[!UICONTROL unit]</i> (wenn keine untergeordneten Produktgruppen vorhanden sind). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Erweiterte Textanzeigen, Multimedia-Anzeigen, responsive Anzeigen und nur responsive Suchanzeigen) Die Überschriften einer Anzeige. Die maximale Länge für jedes Feld Anzeigentitel beträgt 30 Zeichen oder 15 Doppelbyte-Zeichen, einschließlich dynamischer Texte (wie die Werte von Schlüsselwörtern, `{Param2}` und `{Param3}` dynamischen Substitutionsvariablen und Anzeigenanpassungen).<br><br> Fügen Sie für responsive Suchanzeigen eine Anzeigenanpassung mit dem folgenden Format ein. Dabei ist „Standardtext“ ein optionaler Wert, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Für erweiterte Textanzeigen sind Anzeigentitel und Anzeigentitel 2 erforderlich, und [!UICONTROL Ad Title 3] ist optional. [!DNL Microsoft Advertising] veralteten erweiterten Textanzeigen im August 2022 können Sie jetzt nur noch Berichte dazu erstellen und sie löschen.<br><br>Für Multimedia-Anzeigen, responsive Anzeigen und responsive Suchanzeigen sind [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] und [!UICONTROL Ad Title 3] erforderlich. Alle anderen Felder für den Anzeigentitel sind optional.<br><br>Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie die `[delete]` Wert (einschließlich der Klammern).<br><br>Bei allen Anzeigentypen außer erweiterten Textanzeigen wird durch Ändern der Anzeigenkopie die vorhandene Anzeige gelöscht und eine neue Anzeige mit denselben Eigenschaften erstellt. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Nur responsive Suchanzeigen; optional) Eine Position, an der der entsprechende Anzeigentitel angeheftet werden kann: `[null]` (kein Wert, wodurch der Anzeigentitel für alle Positionen geeignet ist), 1, 2 oder 3. Wenn [!UICONTROL Ad Title Position] beispielsweise den Wert 1 hat, kann [!UICONTROL Ad Title] nur in Position 1 angezeigt werden. Standardmäßig sind alle Anzeigentitel null (ohne Werte). Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern).<br><br><b>Hinweis:</b> Sie können mehrere Anzeigentitel an derselben Position anheften. Das Werbenetzwerk verwendet einen der an die Position angehefteten Anzeigentitel. Titel, die an Position 3 angeheftet sind, werden in der Anzeige möglicherweise nicht angezeigt. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Nur Textanzeigen, dynamische Suchanzeigen, Multimedia-Anzeigen, responsive Anzeigen, responsive Suchanzeigen und erweiterte Sitelinks auf Kampagnenebene) Der Text einer Anzeige oder eines Sitelinks.<br><br>Bei Sitelinks können Sie optional sowohl [!UICONTROL Description Line 1] als auch [!UICONTROL Description Line 2] verwenden, um zusätzlichen Text einzuschließen, den das Werbenetzwerk unter dem Link-Text anzeigen kann. Jedes Beschreibungsfeld kann bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.<br><br>Bei Anzeigen beträgt die maximale Länge für jedes Beschreibungsfeld 90 Zeichen oder 45 Doppelbyte-Zeichen, einschließlich dynamischem Text (z. B. die Werte von Schlüsselwörtern und Anzeigenanpassungen).<br><br>Fügen Sie für responsive Suchanzeigen eine Anzeigenanpassung mit dem folgenden Format ein. Dabei ist Standardtext ein optionaler Wert, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Für Textanzeigen und dynamische Suchanzeigen ist die Beschreibungszeile 1 erforderlich und [!UICONTROL Description Line 2] optional.<br><br>Für Multimedia-Anzeigen, responsive Anzeigen und responsive Suchanzeigen sind [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] erforderlich. [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern).<br><br><b>Hinweise:</b><ul><li>(Standard-Textanzeigen) Der kombinierte Titel und Text müssen mindestens drei Wörter enthalten.</li><li>(Erweiterte Textanzeigen) Dieses Feld kann optional die {Param2} und {Param3} dynamische Substitutionsvariablen enthalten. Ist dies der Fall, beträgt die maximale Länge des Anzeigentextes 300 Einzelbyte- oder 150 Doppelbyte-Zeichen. [!DNL Microsoft Advertising] veralteten erweiterten Textanzeigen im August 2022 können Sie jetzt nur noch Berichte dazu erstellen und sie löschen.</li><li>(Dynamische Suchanzeigen) Dynamischer Ersatztext ist nicht zulässig.</li><li>Bei allen Anzeigentypen außer erweiterten Textanzeigen löscht das Ändern der Anzeigenkopie die vorhandene Anzeige und erstellt eine neue.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Nur responsive Suchanzeigen; optional) Eine Position, an der die entsprechende Beschreibung angeheftet werden kann: `[null]` (kein Wert, wodurch die Beschreibung für alle Positionen geeignet ist), 1, 2 oder 3. Wenn [!UICONTROL Description 1 Position] beispielsweise den Wert 1 hat, kann die Beschreibung 1 nur in Position 1 angezeigt werden. Standardmäßig werden keine Beschreibungen an eine Position angeheftet.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern).<br><br><b>Hinweis:</b> Sie können mehrere Beschreibungen an derselben Position anheften. Das Werbenetzwerk verwendet eine der an die Position angehefteten Beschreibungen. An Position 2 angeheftete Beschreibungen werden in der Anzeige möglicherweise nicht angezeigt. |
| [!UICONTROL Business Name] | (Nur Multimedia-Anzeigen) Der Unternehmensname mit maximal 25 Zeichen. |
| [!UICONTROL Promotion Line] | (Nur Produktlisten-Anzeigen) Eine eindeutige Promotion-Zeile, die in den Suchergebnissen in den Produktlisten enthalten sein soll (z. B. „Jetzt versandkostenfrei!„). Die maximale Länge beträgt 45 Zeichen.<br><br>Die Promotion-Zeile kann relativ zur Anzeige an verschiedenen Stellen angezeigt werden (z. B. unter der Anzeige), je nachdem, wo die Anzeige auf der Seite erscheint. |
| [!UICONTROL Display URL] | Die in der Anzeige enthaltene URL.<br><br>Bei erweiterten dynamischen Suchanzeigen generiert das Anzeigennetzwerk diesen Wert dynamisch aus der Website-Domain und Sie müssen keinen Wert eingeben.<br><br>Bei erweiterten Textanzeigen und responsiven Suchanzeigen müssen Sie keinen Wert eingeben. Die Anzeige-URL wird in der endgültigen URL automatisch aus der Domain extrahiert. Sie können die URL optional mit den Feldern Pfad 1 und Pfad 2 anpassen.<br><br><b>Hinweise:</b><ul><li>(Konten mit endgültigen URLs) Die Domain-Namen in der Anzeige-URL und der endgültigen URL müssen übereinstimmen.</li><li>[!DNL Microsoft Advertising] veralteten erweiterten Textanzeigen im August 2022 können Sie jetzt nur noch Berichte dazu erstellen und sie löschen.</li></ul> |
| [!UICONTROL Display Path 1] | (Nur erweiterte Textanzeigen, dynamische Suchanzeigen und responsive Suchanzeigen) Text, der zur Anzeige-URL hinzugefügt wird, die automatisch aus der endgültigen URL extrahiert wird. Jedem Pfad wird in der URL ein Schrägstrich (/) vorangestellt. Ein Pfad darf keine Schrägstriche (/) oder Zeilenumbrüche (\n) enthalten. Die maximale Länge für jeden Pfad beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.<br><br>Verwenden Sie zum Einfügen einer Anzeigenanpassung die folgenden Formate, wobei „Standardtext“ ein optionaler Wert ist, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält: `{CUSTOMIZER.Attribute name:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`<br><br>Wenn [!UICONTROL Display Path 1] beispielsweise „Angebote“ ist, wäre die Anzeige-URL &lt;display URL>/offers, z. B. www.example.com/deals.<br><br>[!DNL Microsoft Advertising] veralteten erweiterten Textanzeigen im August 2022 können Sie jetzt nur noch Berichte dazu erstellen und sie löschen. |
| [!UICONTROL Display Path 1] | (Nur erweiterte Textanzeigen, dynamische Suchanzeigen und responsive Suchanzeigen) Ein zusätzlicher Anzeigepfad; [!UICONTROL Display Path 1] finden Sie im Eintrag.<br><br>Beispiel: Wenn [!UICONTROL Display Path 1] „Angebote“ und [!UICONTROL Display Path 2] „lokal“ ist, dann würde die Anzeige-URL &lt;<i>Display URL>/</i>/local sein, z. B. www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Nur erweiterte Sitelinks) Das erste Datum, an dem Gebote für den Sitelink in der Zeitzone des Werbetreibenden in einem der folgenden Formate abgegeben werden können: M/D/JJJJ, M/D/JJJ, M-D-JJJJ oder M-D-JJJ. Der Standardwert für neue erweiterte Sitelinks ist der aktuelle Tag. <b>Hinweis</b> Neue erweiterte Sitelinks können nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellt werden. |
| [!UICONTROL End Date] | Das letzte Datum, an dem der Sitelink mit Anzeigen in der Zeitzone des Werbetreibenden und in einem der folgenden Formate angezeigt werden kann: M/D/JJJJ, M/D/JJJJ, M-D-JJJJ oder M-D-JJJ. Für einen neuen Sitelink ist der Standardwert `[blank]` (d. h. kein Enddatum). |
| [!UICONTROL Call To Action] | Der Aktionsaufruf, der in die Anzeige aufgenommen werden soll. Siehe die [API-Referenz für eine Liste möglicher Werte](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction) geben Sie jedoch mehrwortige Aktionsaufrufe als mehrere Wörter (z. B. „Bet Now“ anstelle von „BetNow„) in Bulksheets ein. |
| [!UICONTROL Call To Action Language] | Die Sprache für die Aktionsaufruf-Optionen. Eine Liste [ Sprachen finden Sie in der ](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | Die Landingpage-URL, zu der Suchmaschinenbenutzer beim Klicken auf Ihre Anzeige geleitet werden, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter. Basis-/endgültige URLs auf Keyword-Ebene überschreiben diese auf Anzeigenebene und höher.<br><br>Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Destination URL] | (Zu Informationszwecken in generierten Bulksheets enthalten; nicht an die Suchmaschine gepostet) Bei Konten mit Ziel-URLs handelt es sich um die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Werbetreibenden verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Sie enthält alle Anlagenparameter, die für die Kampagne oder das Konto „Suche“, „Social“ und &quot;Commerce&quot; konfiguriert wurden. Wenn Sie Tracking-URLs generiert haben, basiert dies auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie suchmaschinenspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Search, Social und Commerce ersetzt werden.<br><br>Bei Konten mit endgültigen URLs zeigt diese Spalte denselben Wert wie die Spalte „Basis-URL/Endgültige URL“ an. |
| [!UICONTROL Custom URL Param] | Daten, die durch die dynamische Variable `{custom_code}` ersetzt werden sollen, wenn die Variable in den Tracking-Parametern für das Suchkonto oder die Kampagneneinstellungen enthalten ist. Um den benutzerdefinierten Wert in die Tracking-URL einzufügen, müssen Sie die Bulksheet-Datei mit der Option Tracking-URLs generieren hochladen. |
| [!UICONTROL Creative Type] | Das Anzeigenformat: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (Shopping-Anzeigen) oder <i>[!UICONTROL Responsive Search Ad]</i> oder <i>[!UICONTROL Text ad]</i>. Der Standardwert für neue Anzeigen lautet <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | Das erste Datum, an dem Gebote für die Anzeigengruppe in der Zeitzone des Werbetreibenden in einem der folgenden Formate abgegeben werden können: M/D/JJJJ, M/D/JJJJ, M-D-JJJJ oder M-D-JJJ. Bei einer neuen Anzeigengruppe ist der Standardwert das aktuelle Datum. |
| [!UICONTROL Ad Group End Date] | Das letzte Datum, an dem Gebote für die Anzeigengruppe in der Zeitzone des Werbetreibenden in einem der folgenden Formate abgegeben werden können: M/D/JJJJ, M/D/JJJ, M-D-JJJJ oder M-D-JJJ. Für eine neue Anzeigengruppe lautet der Standardwert [leer] (d. h. kein Enddatum). |
| [!UICONTROL Tracking Template] | (Optional) Die Tracking-Vorlage, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Die Tracking-Vorlage auf der detailliertesten Ebene (mit dem Keyword als der detailliertesten) überschreibt die Werte auf allen höheren Ebenen.<br><br>Für das Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, fügt Search, Social und Commerce beim Speichern des Datensatzes automatisch Umleitungs- und Trackingcode an.<br><br>Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.<br><br>Eine Liste der Parameter zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in der [!DNL Microsoft Advertising].<br><br> Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Landing Page Suffix] | Alle Parameter, die an das Ende der endgültigen URLs angehängt werden müssen, um Informationen zu tracken. Beispiel: `param2=value1&param3=value2`<br><br>Siehe &quot;[Klick-Tracking-Formate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).“<br><br>Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Zur einfacheren Wartung verwenden Sie nur das Suffix auf Kontoebene, es sei denn, eine andere Nachverfolgung für einzelne Kontokomponenten ist erforderlich. Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den [!DNL Microsoft Advertising]. |
| Netzwerkstatus suchen | Gibt an, ob Anzeigen für die Anzeigengruppe in verschiedenen Elementen des Suchnetzwerks platziert werden sollen:<ul><li><i>Alle:</i> Platzieren von Anzeigen in allen Bing-Suchnetzen und syndizierten Suchpartnern.</li><li><i>OwnedAndOperatedOnly:</i>Platzieren von Anzeigen nur auf Bing und Yahoo! Websites.</li><li><i>SyndicatedSearchOnly:</i> Werbeanzeigen nur auf Bing und Yahoo schalten! Syndizierte Suchpartner.</li><li><i>Aus</i> Um Anzeigen nur im Content Network (nicht im Search Network) zu platzieren.</li></ul> Für neue Anzeigengruppen ist der Standardwert „Ein“. |
| [!UICONTROL Content Network Status] | Veraltet |
| [!UICONTROL Languages] | Die Zielsprache für Anzeigen in der Anzeigengruppe: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish] oder [!UICONTROL Swedish]. Der Standardwert für neue Kampagnen ist [!UICONTROL English].<br><br>Diese Einstellung legt die Länder und Regionen fest, in denen Ihre Anzeige angezeigt werden kann. Achten Sie darauf, eine Sprache auszuwählen, die mit den Standortzielen der Kampagne kompatibel ist. |
| [!UICONTROL Budget Type] | Ob das Budget <i>[!UICONTROL Daily]</i> (Standard) oder <i>[!UICONTROL Monthly]</i> ist.<br><br>Hinweis: Wenn Sie die Kampagne einem optimierten Portfolio zuweisen, wird dieser Wert automatisch auf [!UICONTROL Daily] gesetzt. |
| [!UICONTROL Device] | Ein Gerätetyp, für den Angebotsanpassungen auf Kampagnen- oder Anzeigengruppenebene vorgenommen werden: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> oder <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | Die Angebotsanpassung für einen bestimmten Zieltyp. Wenn beispielsweise das Gebot auf Keyword-Ebene 1 USD und die Gebotsanpassung für Smartphones 50 % beträgt, beträgt das Smartphone-Gebot 1,50 USD. Standardmäßig werden alle Ziele auf Keyword-Ebene geboten. Gültige Prozentsätze können Folgendes umfassen:<ul><li>Smartphones und Tablets: -100 (nicht zu bieten für den Gerätetyp) und von -90 bis 900</li><li>Desktop: von 0 bis 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | Die Gerätetypen, auf denen die Anzeige oder der Sitelink angezeigt werden soll: <i>[!UICONTROL All]</i> (Standard) oder <i>[!UICONTROL Mobile]</i>. Wenn „Mobil“ angegeben ist, versucht das Netzwerk, die Anzeige oder den Sitelink für Benutzer von Mobilgeräten anzuzeigen, anstatt für Desktop- oder Tablet-Benutzer. Andernfalls zeigt das Netzwerk die Anzeige oder den Sitelink auf jedem Gerätetyp an. <b>Hinweis:</b> Das Netzwerk garantiert nicht, dass es die Anzeige auf dem bevorzugten Gerätetyp anzeigt. |
| [!UICONTROL Param2] | Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL des Keywords oder der Titel, die Beschreibung oder die Basis-URL der Anzeige die `{Param2}` dynamische Ersatzzeichenfolge enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Werbeelemente, in denen Sie sie verwenden (z. B. können Titel 1 und Titel 2 zusammen maximal 76 Zeichen lang sein). Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Param3] | Die Zeichenfolge, die als Ersatzwert verwendet werden soll, wenn die Basis-URL des Keywords oder der Titel, die Beschreibung oder die Basis-URL der Anzeige die `{Param3}` dynamische Ersatzzeichenfolge enthält. Die maximale Länge beträgt 70 Zeichen. Beachten Sie jedoch die maximale Länge der Werbeelemente, in denen Sie sie verwenden (z. B. können Titel 1 und Titel 2 zusammen maximal 76 Zeichen lang sein). Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Link Name] | Der Sitelink-Text. Sie muss innerhalb der Kampagne eindeutig sein. Wenn Sie Description1 und Description2 angeben, kann der Sitelink-Text bis zu 25 Einzelbyte- oder 12 Doppelbyte-Zeichen enthalten. Andernfalls kann der Sitelink-Text bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.<br><br>[!DNL Microsoft Advertising] können zwei, vier oder sechs erweiterte Sitelinks mit Beschreibungen oder vier oder sechs Sitelinks in einer einzigen Zeile ohne Beschreibungen mit einer Anzeige anzeigen.<br><br>Sie können neue erweiterte Sitelinks nur in Kampagnen mit vorhandenen erweiterten Sitelinks oder ohne Sitelinks erstellen. |
| [!UICONTROL Campaign Status] | Der Anzeigestatus der Kampagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur für bestehende Kampagnen). Der Standardwert für neue Kampagnen ist [!UICONTROL Active]. Um eine aktive oder pausierte Kampagne zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Ad Group Status] | Der Anzeigestatus der Anzeigengruppe: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigengruppen). Der Standardwert für neue Anzeigengruppen ist [!UICONTROL Active]. Um eine aktive oder angehaltene Anzeigengruppe zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Keyword Status] | Der Anzeigestatus des Keywords: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Keywords). Die Standardeinstellung für neue Schlüsselwörter ist [!UICONTROL Active]. Um ein aktives oder angehaltenes Keyword zu löschen, geben Sie den Wert `Deleted` ein. <b>Hinweis</b> Wenn Sie Tracking-URLs für ein Keyword mit mehreren Übereinstimmungstypen erstellen, muss der Keyword-Status für jeden Übereinstimmungstyp gleich sein. |
| [!UICONTROL Placement Status] | Veraltet |
| [!UICONTROL Ad Status] | Der Anzeigestatus der Anzeige: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigen), <i>[!UICONTROL Disapproved]</i> (nicht bearbeitbar) oder <i>[!UICONTROL Paused]</i>. Der Standardwert für neue Anzeigen lautet [!UICONTROL Active]. Um eine aktive oder pausierte Anzeige zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Target Status] | Der Status eines dynamischen Suchziels: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Ziele). Der Standardwert für neue Ziele ist [!UICONTROL Active]. Um ein aktives oder angehaltenes Ziel zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Sitelink Status] | Der Anzeigestatus des Sitelinks: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Sitelinks). Der Standardwert für neue Sitelinks ist [!UICONTROL Active]. Um einen aktiven Sitelink zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Location Status] | Der Status des Standortziels: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Standorte). Der Standardwert für neue Speicherorte lautet [!UICONTROL Active]. Um einen aktiven Speicherort zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Product Group Status] | Der Anzeigestatus der Produktgruppe: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Produktgruppen). Der Standardwert für neue Produktgruppen ist [!UICONTROL Active]. Um eine aktive Produktgruppe zu löschen, geben Sie den Wert `Deleted` ein. |
| [!UICONTROL Device Target Status] | Der Status des Zielgeräts auf Kampagnen- oder Anzeigengruppenebene: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i>. Für neue Kampagnen und Anzeigengruppen ist der Standardwert [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | Der Status des RLSA-Ziels auf Kampagnen- oder Anzeigengruppenebene oder (nur Google Ads)-Ausschlusses: <i>[!UICONTROL Active]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Ziele). Der Standardwert für neue Ziele oder Ausschlüsse ist [!UICONTROL Active]. Um eine aktive Zielgruppe oder einen aktiven Ausschluss zu löschen, geben Sie den Wert `Deleted` ein. |
| \[Advertiser-spezifische Label-Klassifizierung\] | (Benannt nach einer Advertiser-spezifischen Kennzeichnungsklassifizierung, z. B. „Farbe“ für eine Kennzeichnungsklassifizierung namens „Farbe„) Ein Wert für die angegebene Klassifizierung, der mit der Entität verknüpft ist. Pro Entität kann nur ein Wert angegeben werden (z. B. „Rot“ für die Kennzeichnung „Farbe“ für Kampagne A). Die maximale Länge beträgt 100 Zeichen. Der Wert kann ASCII- und Nicht-ASCII-Zeichen enthalten.<br><br>Kennzeichnungsklassifizierungen und ihre Kennzeichnungswerte werden auf alle untergeordneten Komponenten angewendet; neue Komponenten, die später hinzugefügt werden, werden automatisch mit der Kennzeichnung verknüpft. Kennzeichnungsklassifizierungen für Produktgruppen werden auf die Ebene der Einheit (mit der höchsten Granularität) angewendet.<br><br>Weder beim Klassifizierungsnamen noch beim Klassifizierungswert wird zwischen Groß- und Kleinschreibung unterschieden. |
| [!UICONTROL Constraints] | Eine Begrenzung, die der Entität zugewiesen ist. Pro Entität kann nur eine Einschränkung zugewiesen werden.<br><b>>Abhängigkeiten werden von untergeordneten Entitäten übernommen. Daher müssen Sie keine Werte für untergeordnete Entitäten eingeben, es sei denn, Sie möchten die übernommenen Werte überschreiben. |
| [!UICONTROL Campaign ID] | Die eindeutige ID, die eine vorhandene Kampagne identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Kampagne. |
| [!UICONTROL Ad Group ID] | Die eindeutige ID, die eine vorhandene Anzeigengruppe identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Anzeigengruppe. |
| [!UICONTROL Placement ID] | Veraltet |
| [!UICONTROL Keyword ID] | Die eindeutige ID, die ein vorhandenes Keyword identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie das Keyword ändern, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung des Keywords oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Ad ID] | <p>Die eindeutige ID, die eine vorhandene Anzeige identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Für responsive Suchanzeigen ist zum Bearbeiten oder Löschen von Anzeigendaten entweder die Anzeigen-ID oder die AMO-ID erforderlich. Für alle anderen Entitätstypen ist die AMO-ID nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichend Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen.</p><p><b>Hinweis:</b> Wenn Sie a) Anzeigeneigenschaftsspalten mit Ausnahme des Status für eine vorhandene Anzeige oder b) Daten für eine responsive Suchanzeige bearbeiten und weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen, wird eine neue Anzeige erstellt und die vorhandene Anzeige wird nicht geändert. </p> |
| [!UICONTROL Sitelink ID] | Die eindeutige ID, die einen vorhandenen Sitelink identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten, um den Sitelink zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] einbeziehen und die Eigenschaftsspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status für nur einen der Sitelinks.</p><p><b>Hinweis:</b> Wenn Sie die Eigenschaftsspalten eines Sitelinks mit Ausnahme des Status für einen vorhandenen Sitelink bearbeiten und weder den [!UICONTROL Sitelink ID] noch den [!UICONTROL AMO ID] einbeziehen, wird ein neuer Sitelink erstellt und der vorhandene Sitelink wird nicht geändert. |
| [!UICONTROL Product Group ID] | Die eindeutige ID, die eine vorhandene Produktgruppe identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung der Produktgruppe oder b) ein &quot;[!UICONTROL AMO ID]&quot;.“ |
| Standort-ID | Die eindeutige [!DNL Microsoft Advertising] für den Zielspeicherort. Um eine Standortliste herunterzuladen, melden Sie sich mit Ihren Anmeldedaten für das [!DNL Microsoft Advertising] Advertising-Konto beim [!DNL Microsoft Advertising]-Entwicklerportal an. Nur erforderlich, wenn Sie den Zielspeicherort ändern oder löschen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL Target ID] | Die eindeutige ID, die ein vorhandenes automatisches Targeting identifiziert. Nur erforderlich, wenn Sie das automatische Targeting ändern oder löschen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Target. |
| [!UICONTROL RLSA Target ID] | Die eindeutige ID, die ein vorhandenes RLSA-Ziel auf Kampagnen- oder Anzeigengruppenebene identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie das Ziel oder den Ausschluss ändern oder löschen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Ziel. |
| [!UICONTROL AMO ID] | (In generierten Bulksheets) Eine von Adobe generierte eindeutige Kennung für eine synchronisierte Entität. Bei responsiven Suchanzeigen ist die AMO-ID erforderlich, um Anzeigen zu bearbeiten oder zu löschen, es sei denn, Sie beziehen die Anzeigen-ID ein. Um Daten für alle anderen Entitätstypen mit einer AMO-ID zu bearbeiten, muss die AMO-ID die Daten bearbeiten oder löschen, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |
| [!UICONTROL EF Error Message] | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Werbenetzwerk bezüglich Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL EF Errors] Dateien enthalten. Dieser Wert wird nicht an das Werbenetzwerk gesendet. |
| [!UICONTROL SE Error Message] | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Werbenetzwerk bezüglich Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL SE Errors] Dateien enthalten. Dieser Wert wird nicht an das Werbenetzwerk gesendet. |
| [!UICONTROL Exemption Request] | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige der Namen und des Texts aller Google-Werberichtlinien, die eine Anzeige verletzt. |
| [!UICONTROL Retail Hash] | (Zu Informationszwecken in Bulksheets enthalten, die mit Advanced Campaign Management generiert wurden) Ein alphanumerischer Hash-Code (z. B. f9639f40cdf56524b541e5dacf55a991), der angibt, dass das Element mithilfe der erweiterten (ACM) Ansicht generiert wurde. |

[^1]: [!DNL Excel] konvertiert große Zahlen in wissenschaftliche Notation (z. B. 2.12E+09 für 2115585666), wenn er die Datei öffnet. Um Ziffern in der Standardnotation anzuzeigen, wählen Sie eine beliebige Zelle in der Spalte aus und klicken Sie in die Leiste Formel .

## Erforderliche Felder zum Erstellen, Bearbeiten oder Löschen jeder Kontokomponente {#bulksheet-fields-per-component-microsoft}

Die folgenden Abschnitte enthalten die Felder, die für bestimmte Kontoentitäten relevant sind.

>[!NOTE]
>
>Wenn ein Feld nicht auf eine Aktion anwendbar ist, werden alle in das Feld eingegebenen Werte ignoriert.

### Kampagnenfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| [!UICONTROL Campaign Budget] | Erforderlich zum Erstellen einer Kampagne. | Eine tägliche Ausgabenbegrenzung für die Kampagne, mit oder ohne Währungssymbole und Satzzeichen. Dieser Wert überschreibt das Kontobudget, darf es jedoch nicht überschreiten. |
| [!UICONTROL Channel Type] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Delivery Method] | optional |
| [!UICONTROL Campaign Priority] | Erforderlich zum Erstellen einer Shopping-Kampagne. |
| [!UICONTROL Merchant ID] | Erforderlich zum Erstellen einer Shopping-Kampagne. |
| [!UICONTROL Sales Country] | Erforderlich zum Erstellen einer Shopping-Kampagne. |
| [!UICONTROL Product Scope Filter] | (Shopping-Kampagnen) Optional |
| [!UICONTROL DSA Domain Name] | Erforderlich zum Erstellen einer Kampagne vom Typ a) &quot;[!UICONTROL DynamicSearchAds]&quot; oder b) &quot;[!UICONTROL Search]&quot; (wenn das [!DNL ExperimentId] nicht festgelegt ist) |
| [!UICONTROL DSA Domain Language] | Erforderlich zum Erstellen einer Kampagne vom Typ a) &quot;[!UICONTROL DynamicSearchAds]&quot; oder b) &quot;[!UICONTROL Search]&quot; (wenn das [!DNL ExperimentId] nicht festgelegt ist) |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Landing Page Suffix] | <p>optional |
| [!UICONTROL Budget Type] | Erforderlich zum Erstellen einer Kampagne. |
| [!UICONTROL Device] | optional |
| [!UICONTROL Bid Adjustment] | optional |
| [!UICONTROL Campaign Status] | Nur zum Löschen einer Kampagne erforderlich. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Kampagne. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Anzeigengruppenfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Group Type] | Erforderlich zum Erstellen einer Anzeigengruppe. |
| [!UICONTROL Audience Target Method] | Nur erforderlich, um Zielgruppe und Gruppen zu erstellen. |
| [!UICONTROL Ad Group Start Date] | optional |
| [!UICONTROL Ad Group End Date] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Search Network Status] | (Nur Kampagnen im Suchnetzwerk) Optional |
| [!UICONTROL Languages] | optional |
| [!UICONTROL Device] | optional |
| [!UICONTROL Bid Adjustment] | optional |
| [!UICONTROL Ad Group Status] | Nur erforderlich, um eine Anzeigengruppe zu löschen. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Ad Group ID] | Nur erforderlich, wenn der Name der Anzeigengruppe geändert wird, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Anzeigengruppe. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Keyword-Felder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Keyword] | Erforderlich |
| [!UICONTROL Match Type] | Zum Bearbeiten oder Löschen eines Keywords mit mehreren Übereinstimmungstypen ist ein Wert für entweder den Übereinstimmungstyp oder die Keyword-ID erforderlich. |
| [!UICONTROL Max CPC] | optional |
| [!UICONTROL Base URL/Final URL] | optional |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Param1] | optional |
| [!UICONTROL Param2] | optional |
| [!UICONTROL Keyword Status] | Nur erforderlich, um ein Keyword zu löschen. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Keyword ID] | Nur erforderlich, wenn Sie das Keyword bearbeiten oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung des Keywords oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Dynamische Suche und Felder

>[!NOTE]
>
>Create-Support ist nicht verfügbar.

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot; im [!UICONTROL Download Bulksheet].

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Erforderlich zum Bearbeiten der Beschreibung. <b>Hinweis:</b> Bei diesem Anzeigentyp wird durch Ändern der Anzeigenkopie die vorhandene Anzeige gelöscht und eine neue erstellt. |
| [!UICONTROL Display Path 1] | Erforderlich zum Bearbeiten des Felds. |
| [!UICONTROL Display Path 2] | Erforderlich zum Bearbeiten des Felds. |
| [!UICONTROL Creative Type] | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Creative Preferred Devices] | optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichend Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Produkt (Einkaufen) und Felder

Weitere Informationen zum Erstellen von Shopping-Anzeigen finden Sie unter [Implementieren [!DNL Microsoft Advertising] Shopping-Kampagnen](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html).

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot; im [!UICONTROL Download Bulksheet].

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Promotion Line] | optional |
| [!UICONTROL Base URL/Final URL] | optional |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Creative Type] | Erforderlich zum Erstellen oder Bearbeiten des Status einer Produktanzeige. |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichend Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Responsive (Multimedia) Anzeigenfelder

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot; im [!UICONTROL Download Bulksheet].

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Für responsive Anzeigen sind [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] und [!UICONTROL Ad Title 3] erforderlich, um Anzeigen zu erstellen. Alle anderen Felder für Anzeigentitel sind optional. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). <b>Hinweis:</b> Bei diesem Anzeigentyp wird durch Ändern der Anzeigenkopie die vorhandene Anzeige gelöscht und eine neue erstellt. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] sind erforderlich, um Anzeigen zu erstellen, und [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional. <b>Hinweis:</b> Bei diesem Anzeigentyp wird durch Ändern der Anzeigenkopie die vorhandene Anzeige gelöscht und eine neue erstellt. |
| [!UICONTROL Business Name] | Erforderlich zum Erstellen oder Löschen einer Anzeige. |
| [!UICONTROL Call To Action] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Call To Action Language] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Base URL/Final URL] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Creative Type] | Optional. |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält a) ausreichend Anzeigeneigenschaftsspalten, um die Anzeige zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder die [!UICONTROL Ad ID] noch die [!UICONTROL AMO ID] einbeziehen und die Anzeigeneigenschaftsspalten mit mehreren Anzeigen übereinstimmen, ändert sich der Status nur für eine der Anzeigen. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Responsive Suchanzeigenfelder

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Responsive Search Ad]&quot; im [!UICONTROL Download Bulksheet].

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Für responsive Suchanzeigen sind [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] und [!UICONTROL Ad Title 3] erforderlich, um eine Anzeige zu erstellen. Alle anderen Felder für den Anzeigentitel sind optional. Um den vorhandenen Wert für ein nicht erforderliches Feld zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | optional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Für responsive Suchanzeigen sind [!UICONTROL Description Line 1] und [!UICONTROL Description Line 2] erforderlich, um eine Anzeige zu erstellen. [!UICONTROL Description Line 3] und [!UICONTROL Description Line 4] sind optional. Um den vorhandenen Wert zu löschen, verwenden Sie den `[delete]` (einschließlich der Klammern). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | optional |
| [!UICONTROL Display Path 1] | optional |
| [!UICONTROL Display Path 2] | optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich zum Erstellen einer Anzeige. |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Creative Type] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Ad Status] | Erforderlich zum Löschen einer Anzeige. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen von Anzeigen, es sei denn, Sie beziehen die Anzeigen-ID ein. |

### Text und Felder

Verwenden Sie für diesen Anzeigentyp die Zeile &quot;[!UICONTROL Creative (except RSA)]&quot; im [!UICONTROL Download Bulksheet].

>[!NOTE]
>
>Erweiterte Textanzeigen werden nicht mehr unterstützt. Sie können nur vorhandene Textanzeigen löschen.

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Schreibgeschützt |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Schreibgeschützt |
| [!UICONTROL Display URL] | Schreibgeschützt |
| [!UICONTROL Display Path 1] | Schreibgeschützt |
| [!UICONTROL Display Path 2] | Schreibgeschützt |
| [!UICONTROL Base URL/Final URL] | Schreibgeschützt |
| [!UICONTROL Custom URL Param] | Schreibgeschützt |
| [!UICONTROL Creative Type] | optional |
| [!UICONTROL Tracking Template] | Schreibgeschützt |
| [!UICONTROL Creative Preferred Devices] | Schreibgeschützt |
| [!UICONTROL Ad Status] | Erforderlich |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Ad ID] | Nur erforderlich, wenn Sie den Anzeigenstatus ändern, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Werbe-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Dynamische Target-Suche (automatisches Targeting)

>[!NOTE]
>
>Create-Support ist nicht verfügbar.

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Auto Target Expression] | Erforderlich. |
| [!UICONTROL Match Type] | optional |
| [!UICONTROL Max CPC] | optional |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Target Status] | Erforderlich zum Löschen einer Zielgruppe |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Target ID] | Nur erforderlich, wenn Sie das automatische Targeting ändern oder löschen, es sei denn, die Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für das Target. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Warenkorb-Produktgruppenfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich |
| [!UICONTROL Match Type] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Max CPC] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Parent Product Groupings] | Erforderlich |
| [!UICONTROL Product Grouping] | Erforderlich |
| [!UICONTROL Partition Type] | Erforderlich zum Erstellen einer Produktgruppe. |
| [!UICONTROL Base URL/Final URL] | Erforderlich |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Product Group Status] | Nur erforderlich, um eine Produktgruppe zu löschen. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional |
| [!UICONTROL Constraints] | optional |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | optional |
| [!UICONTROL Product Group ID] | Nur erforderlich, wenn Sie die Produktgruppe ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung der Produktgruppe oder b) ein &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Sitelink-Felder auf Kampagnenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| Beschreibungszeile 1 | optional |
| [!UICONTROL Description Line 2] | optional |
| [!UICONTROL Start Date] | optional |
| [!UICONTROL End Date] | optional |
| [!UICONTROL Base URL/Final URL] | Erforderlich |
| [!UICONTROL Custom URL Param] | optional |
| [!UICONTROL Tracking Template] | optional |
| [!UICONTROL Creative Preferred Devices] | optional |
| [!UICONTROL Link Name] | Erforderlich |
| [!UICONTROL Sitelink Status] | Nur zum Löschen eines Sitelinks erforderlich. |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Sitelink ID] | Nur erforderlich, wenn Sie den Sitelink ändern oder löschen, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten, um den Sitelink zu identifizieren, oder b) ein &quot;[!UICONTROL AMO ID]&quot;. Wenn Sie jedoch weder [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] einbeziehen und die Eigenschaftsspalten mit mehreren Sitelinks übereinstimmen, ändert sich der Status für nur einen der Sitelinks.<br><br><b>Hinweis:</b> Wenn Sie die Eigenschaftsspalten eines Sitelinks mit Ausnahme des Status für einen vorhandenen Sitelink bearbeiten und weder den [!UICONTROL Sitelink ID] noch den [!UICONTROL AMO ID] einbeziehen, wird ein neuer Sitelink erstellt und der vorhandene Sitelink wird nicht geändert. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Standort-Zielfelder

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Location] | Erforderlich |
| [!UICONTROL Location Type] | Erforderlich zum Erstellen einer Zielgruppe |
| [!UICONTROL Bid Adjustment] | optional |
| [!UICONTROL Location Status] | Nur erforderlich, um einen Zielspeicherort zu löschen. |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Kampagnen-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### Gerätezielfelder auf Kampagnenebene und Anzeigengruppenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Device] | Erforderlich zum Löschen eines Zielgeräts. |
| [!UICONTROL Bid Adjustment] | optional |
| [!UICONTROL Ad Group Name] | Erforderlich für Geräte-Ziele auf Anzeigengruppenebene. Gilt nicht für Geräte-Ziele auf Kampagnenebene. |
| [!UICONTROL Device Target Status] | Nur erforderlich, um ein Zielgerät zu löschen. |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | Optional; gilt nur für Geräte-Ziele auf Anzeigengruppenebene. |
| [!UICONTROL AMO ID] | Erforderlich zum Bearbeiten oder Löschen der Daten, es sei denn, Sie beziehen die Geräte-Ziel-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |

### RLSA-Zielfelder auf Kampagnenebene und Anzeigengruppenebene

Eine Beschreibung der einzelnen Datenfelder finden Sie unter &quot;[Alle verfügbaren Datenfelder](#bulksheet-fields-all-microsoft)&quot;.

| Feld | Erforderlich? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Erforderlich, es sei denn, jede Zeile enthält ein &quot;[!UICONTROL AMO ID]&quot; für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich |
| [!UICONTROL Ad Group Name] | Erforderlich für Ziele auf Anzeigengruppenebene. Gilt nicht für Zielgruppen auf Kampagnenebene. |
| [!UICONTROL Audience] | Erforderlich zum Erstellen einer neuen Zielgruppe. |
| [!UICONTROL Target Type] | optional |
| [!UICONTROL Bid Adjustment] | optional |
| [!UICONTROL RLSA Target Status] | Erforderlich zum Löschen einer Zielgruppe. |
| [!UICONTROL Campaign ID] | optional |
| [!UICONTROL Ad Group ID] | Optional; gilt nur für Zielgruppen auf Anzeigengruppenebene. |
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
