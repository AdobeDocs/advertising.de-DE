---
title: Einstellungen für Sonderberichte
description: Erfahren Sie mehr über die erforderlichen und optionalen Einstellungen für spezielle Berichte.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '2995'
ht-degree: 0%

---

# Einstellungen für Sonderberichte

| Registerkarte | Parameter | Beschreibung |
|----|----|----|
| Nicht zutreffend | [!UICONTROL Name] | (Optional) Ein Name für den Bericht und die Vorlage (wenn Sie den Bericht als Vorlage speichern). Wenn Sie eine vorhandene Vorlage anwenden, wird der Vorlagenname standardmäßig ausgefüllt. Wenn Sie keine Vorlage anwenden oder einen Namen eingeben, erhält der Bericht den Namen `<client name>-<date and time>-<report type>` (z. B. &quot;acme - 3. April 2009 11&quot;:25:19 Uhr PDT - Keyword&quot;) standardmäßig eingestellt.<br><br>Sie können optional einen benutzerdefinierten Namen eingeben, aber keine Dateierweiterung verwenden.<br><br>Wenn Sie eine Vorlage erstellen, um [Senden von Berichten an ein FTP-Verzeichnis](/help/search-social-commerce/reports/automation/ftp-reports.md), können Sie optional &quot;CSV&quot;(in Großbuchstaben) an einer beliebigen Stelle im Dateinamen einfügen, um Dateien im CSV-Format und nicht im standardmäßigen TSV-Format zu erstellen. Siehe [Dateinamenanforderungen für Berichte, die an ein FTP-Verzeichnis gesendet werden](/help/search-social-commerce/reports/automation/ftp-reports.md). |
|  | [!UICONTROL Save as template] | (Optional, es sei denn, Sie möchten den Bericht gemäß einem Zeitplan ausführen.) Speichert die Berichtseinstellungen als Vorlage, die im [!UICONTROL Reports] > [!UICONTROL Report Templates] anzeigen und können wiederverwendet werden, um neue Berichte zu erstellen. Um den Bericht als Vorlage zu speichern, aktivieren Sie das Kontrollkästchen.<br><br>Um den Bericht planmäßig auszuführen, müssen Sie die Einstellungen als Vorlage speichern.<br><br><b>Hinweis:</b> Sie können den aktuellen Parametersatz als neue Vorlage speichern, selbst wenn er auf einer vorhandenen Vorlage basiert. |
|  | [!UICONTROL Type] | Der zu erzeugende Berichtstyp. |
| [!UICONTROL Basic  Settings] | [!UICONTROL Template] | (Optional) Eine anzuwendende Berichtsvorlage, mit der die Berichtsoptionen entsprechend der Vorlage vorausgefüllt werden. Alle Vorlagen, die für den Berichtstyp gespeichert und für Sie verfügbar sind, werden aufgelistet.<br><br>Wenn Sie eine Vorlage auswählen, können Sie die Berichtsoptionen weiterhin ändern und den Bericht sogar als neue Vorlage speichern. |
|  | [!UICONTROL Data Aggregation] | ([!UICONTROL Forecast Accuracy Report only]) Die Zeiteinheit, die in jeder Berichtszeile dargestellt werden soll: <i>[!UICONTROL Summary (the default)]</i>, <i>[!UICONTROL Daily]</i>, <i>[!UICONTROL Weekly]</i> (und geben Sie dann den ersten Wochentag an), <i>[!UICONTROL Monthly]</i>, <i>[!UICONTROL Quarterly]</i>, <i>[!UICONTROL Yearly]</i>oder <i>[!UICONTROL Day of Week]</i> (nur Basisberichte).<br><br>Der Bericht zeigt eine Zeile für jeden Suchbegriff oder jedes andere Element für jede Zeiteinheit im angegebenen Datumsbereich an. Wenn Sie beispielsweise <i>[!UICONTROL Summary]</i> und einen Datumsbereich <i>[!UICONTROL Last 7 Days]</i> für einen Suchbegriffbericht enthält der Bericht eine Zeile für jeden Suchbegriff, in der die Summen und Durchschnittswerte der sieben Tage zusammengefasst werden. Derselbe Bericht mit <i>[!UICONTROL Daily]</i> Datenaggregation umfasst eine Zeile für jeden Suchbegriff für jeden der letzten sieben Tage (sieben Zeilen pro Suchbegriff).<br><br><b>Hinweise:</b><ul><li>Wenn Sie Daten stündlich aggregieren, verwenden Sie entweder das[!UICONTROL Hourly]&quot; oder &quot;[!UICONTROL Day of Week (Hourly)]&quot; aggregation:</li><ul><li>Sie können Daten aus den letzten 14 Tagen anzeigen. Der Bericht zeigt Daten stündlich nach 24-Stunden-Zeit an. &quot;[!UICONTROL 0]&quot; enthält 00:01-00:59 (12):01-12:59.00 Uhr) und &quot;[!UICONTROL 23]&quot; enthält 23:01-23:59 (11):01-11:17.00 Uhr) in der Zeitzone des Werbetreibenden.</li><li>Die &quot;[!UICONTROL Device]&quot;-Spalte wird nicht unterstützt.</li><li>Für [!UICONTROL Ad Group Report], wird[!UICONTROL Data Based On]&quot; option &quot;[!UICONTROL Portfolio Configuration During the Specified Dates]&quot; wird nicht unterstützt.</li><li>Für [!UICONTROL Ad Group Report]können Sie stündliche Daten nur auf der aktuellen Portfoliokonfiguration basieren (mithilfe der[!UICONTROL Data Based On]&quot; option &quot;[!UICONTROL Current Portfolio Configuration]&quot;), nicht die Portfoliokonfiguration zu bestimmten Zeitpunkten.</li></ul></ul> |
|  | [!UICONTROL Conversions Based on] | ([!UICONTROL AdWords Shopping Performance Report], [!UICONTROL Campaign Daily Impression Share Report]und [!UICONTROL Keyword Daily Impression Share Report] nur) So melden Sie Konversionsdaten:<ul><li><i>[!UICONTROL Transaction date]</i> (Standardeinstellung): Um Transaktionen anzuzeigen, deren Transaktionsdatum im angegebenen Zeitraum aufgetreten ist. Diese Option zeigt an, wie viel Umsatz innerhalb des festgelegten Zeitraums erzielt wurde.</li><li><i>[!UICONTROL Click date]:</i> Um Transaktionen anzuzeigen, die durch einen Klick entstanden sind, der während des angegebenen Zeitraums erfolgte. Wenn ein Portfolio erhebliche Verzögerungen zwischen Klicks und Transaktionen aufweist, ist diese Option für die Berechnung des historischen Umsatzes pro Klick für das Portfolio nützlich, was das zu erwartende Umsatzwuster im Laufe der Zeit anzeigt.</li></ul> |
|  | [!UICONTROL Date Range] | Der Datumsbereich, für den Daten generiert werden sollen:<ul><li><i>[Vorgabenbereich]:</i> Eine Liste der gängigen Zeitabstände, von <i>[!UICONTROL Today]</i> nach <i>[!UICONTROL Last 180 Days]</i>. Der Standardwert ist <i>[!UICONTROL Last 7 Days]</i>, der die letzten sieben Tage angibt, für die Daten verfügbar sind. <b>Hinweis:</b> <i>[!UICONTROL Last Month]</i>, <i>[!UICONTROL Last 3 Months]</i>und <i>[!UICONTROL Last 6 Months]</i> Daten der vorherigen Kalendermonate anzeigen.</li><li><i>[!UICONTROL Custom Date Range]:</i> Geben Sie das Anfangsdatum und das Enddatum an. Geben Sie Datumsangaben in das Format MM/TT/JJJJ oder M/D/JJJJ ein oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") neben einem Feld und wählen Sie ein Datum aus.</li></ul> |
|  | [!UICONTROL Compare With] | Vergleicht Daten für den angegebenen Datumsbereich mit Daten für einen zweiten Datumsbereich. Wenn Sie diese Option auswählen, werden für jede reguläre Datenspalte zwei zusätzliche Spalten hinzugefügt. Anstatt beispielsweise nur eine Spalte für &quot;Impressionen&quot;einzuschließen, enthält der Bericht Spalten für[!UICONTROL Impressions Range 1], &quot;[!UICONTROL Impressions Range 2],&quot; und &quot;[!UICONTROL Impressions Difference].&quot;<br><br><b>Hinweise:</b><ul><li>Die Differenzspalte wird für benutzerdefinierte/abgeleitete Metriken nicht angezeigt.</li><li>Berichte, die große Datumsbereiche vergleichen, brauchen länger zu generieren.</li></ul> |
|  | [!UICONTROL Show Comparison Data as] | (Wenn[!UICONTROL Compare With]&quot;(ist ausgewählt) Wie wird der Unterschied zwischen den Daten in den beiden ausgewählten Datumsbereichen in der &quot;[Datenfeld] [!UICONTROL Difference]&quot; column:<ul><li><i>[!UICONTROL Variance]</i> (Standardeinstellung): Zeigt die Differenz als numerischen Wert an.</li><li><i>[!UICONTROL % Change]:</i> Zeigt die Differenz in Prozent an.</li></ul> |
|  | [!UICONTROL Filter By] | ([!UICONTROL RSA Asset Report], [!UICONTROL Campaign Daily Impression Share Report]und [!UICONTROL Keyword Daily Impression Share Report] nur) Ob Berichte zu Daten für bestimmte Portfolios oder für bestimmte Werbenetzwerke erstellt werden:<ul><li><i>[!UICONTROL Portfolio]</i> (Standardeinstellung): So schließen Sie Daten für Kampagnen in ein oder mehrere Portfolios ein.</li><li><i>[!UICONTROL Search Engine]:</i> So fügen Sie Daten für Kampagnen in einem oder mehreren Werbenetzwerken hinzu (je nach Berichtstyp). |
|  | \[Primäre Filter\] | Die einzuschließenden Datenkomponenten. Wenn Sie keine Auswahl treffen, werden Daten für alle Portfolios (falls zutreffend) oder für alle anwendbaren Werbenetzwerke und deren Unterkomponenten in den Bericht aufgenommen. Optional können Sie die zu meldenden Daten einschränken, indem Sie einzelne Komponenten und Unterkomponenten angeben. Geben Sie je nach Berichtstyp und (falls zutreffend) nach Portfolio oder Anzeigennetzwerk filtern Sie die einzuschließenden Komponenten an:<ul><li><i>[!UICONTROL Portfolio]:</i> Ein oder mehrere Portfolios oder deren Unterkomponenten (Kampagnen oder Anzeigengruppen). Um eine Komponente und alle zugehörigen Unterkomponenten auszuwählen, aktivieren Sie das Kontrollkästchen neben dem Komponentennamen. Um eine Unterkomponente auszuwählen, aktivieren Sie das Kontrollkästchen neben dem Namen der Unterkomponente und klicken Sie dann auf >> , um sie in die [!UICONTROL Selected Filters] Spalte. Um beispielsweise Daten für Portfolio 1 und alle Kampagnen und Anzeigengruppen abzurufen, aktivieren Sie das Kontrollkästchen neben Portfolio 1. Um Daten zu erhalten, wenn in Campaign 1 in Portfolio 1 mindestens ein Ereignis aufgetreten ist, erweitern Sie Portfolio 1 und aktivieren Sie dann nur das Kontrollkästchen neben Campaign 1.</li><li><i>[!UICONTROL Search Engine]:</i> Ein oder mehrere Werbenetzwerke oder ihre Unterkomponenten (Konten, Kampagnen oder Anzeigengruppen). Um eine Komponente und alle zugehörigen Unterkomponenten auszuwählen, aktivieren Sie das Kontrollkästchen neben dem Komponentennamen und klicken Sie dann auf >> , um sie in die [!UICONTROL Selected Filters] Spalte. Um eine Unterkomponente auszuwählen, aktivieren Sie das Kontrollkästchen neben dem Namen der Unterkomponente und klicken Sie dann auf >> , um sie in die [!UICONTROL Selected Filters] Spalte. Um beispielsweise Daten abzurufen, wenn mindestens ein Ereignis in einem [!DNL Google Ads] Konto, Kampagne und Anzeigengruppe, aktivieren Sie das Kontrollkästchen neben [!DNL Google AdWords]. So rufen Sie nur Daten für Campaign 1 ab: [!DNL Google Ads] Konto 1, erweitern [!DNL Google Ads] und dann Konto 1, und aktivieren Sie dann nur das Kontrollkästchen neben Kampagne 1.</li></ul><b>Hinweise:</b><ul><li>Um eine Komponente in der Liste zu erweitern (z. B. die Konten in einem Werbenetzwerk aufzulisten), klicken Sie auf ![Symbol mit dem Rechtspfeil](/help/search-social-commerce/assets/compressed-item.png "Symbol mit dem Rechtspfeil") neben der Komponente.</li><li>Um zu sehen, welcher Komponententyp ein Element ist, halten Sie den Cursor darüber.</li><li>Standardmäßig werden nur a) aktive und optimierte Portfolios und ihre aktiven Komponenten oder b) aktive und aktivierte Anzeigennetzwerkkonten, Kampagnen und ihre aktiven Komponenten aufgelistet. Um ausgesetzte und gelöschte Komponenten anzuzeigen, klicken Sie auf ![Abwärtspfeil](/help/search-social-commerce/assets/arrow-down-expand.png "Abwärtspfeil") neben **[!UICONTROL Show]** und wählen Sie **[!UICONTROL All]**.</li><li>Wenn Sie einen erweiterten Bericht nach Portfolio generieren, werden die resultierenden Daten für Kampagnen verwendet, die derzeit den angegebenen Portfolios zugeordnet sind. Der Bericht enthält keine Daten zu Kampagnen, die sich im Datumsbereich in den Portfolios befanden, aber noch nicht dort sind.</li></ul> |
| [!UICONTROL Columns] | \[Berichtsspalten\] | Die im Bericht angezeigten Datenspalten und ihre Reihenfolge:<ul><li>Um eine Spalte hinzuzufügen, klicken Sie auf den Metriknamen in der linken Spalte und dann auf ![Rechter Pfeil](/help/search-social-commerce/assets/arrow-right-customize.png "Rechter Pfeil").</li><li>Um eine Spalte zu entfernen, klicken Sie auf den Metriknamen in der rechten Spalte und dann auf ![Linker Pfeil](/help/search-social-commerce/assets/arrow-left-customize.png "Linker Pfeil").</li><li>Um eine Spalte innerhalb des Berichts nach links zu verschieben, klicken Sie auf den Metriknamen in der rechten Spalte und dann auf ![Nach oben](/help/search-social-commerce/assets/arrow-up-customize.png "Nach oben").</li><li>Um eine Spalte innerhalb des Berichts nach rechts zu verschieben, klicken Sie auf den Metriknamen in der rechten Spalte und dann auf ![Abwärtspfeil](/help/search-social-commerce/assets/arrow-down-customize.png "Abwärtspfeil").</li></ul><b>Hinweise:</b><ul><li>Um nur einen bestimmten Datentyp aufzulisten, klicken Sie auf eines der Symbole oberhalb der Liste:<ul><li>![Eigenschaften](/help/search-social-commerce/assets/property-columns.png "Eigenschaften") für Eigenschaftsnamen und IDs für Anzeigennetzwerkkonten oder Portfoliokomponenten, z. B. [!UICONTROL Campaign Status]&lt;.li<li>![Traffic-Metriken](/help/search-social-commerce/assets//traffic-metric-columns.png "Traffic-Metriken") für standardmäßige Traffic-Metriken wie Impressionen und Klicks</li><li>![Umsatzmetriken](/help/search-social-commerce/assets/revenue-metric-columns.png "Umsatzmetriken") für Umsatzmetriken/Transaktionseigenschaften, die für den Advertiser verfolgt werden, einschließlich der von Adobe Analytics synchronisierten Konversions- und Site-Interaktionsmetriken</li><li>![Abgeleitete Metriken](/help/search-social-commerce/assets/derived-metric-columns.png "Abgeleitete Metriken") für benutzerdefinierte abgeleitete Metriken, die vom Advertiser erstellt wurden</li><li>![Beschriftungsklassifizierungen](/help/search-social-commerce/assets/label-classification-columns.png "Beschriftungsklassifizierungen") nur für Beschriftungsklassifizierungen in den Berichten &quot;Kampagne&quot;, &quot;Anzeigengruppe&quot;, &quot;Anzeigenvariante&quot;, &quot;Keyword&quot;und &quot;Produktgruppe&quot;</li></ul></li></li><li>Standardmäßig werden alle monetären Daten in Berichten im Format für US-Dollar angezeigt (z. B. 1.000,00). Um den Wert im korrekten Währungsformat anzuzeigen (jedoch ohne Währungssymbole in CSV- und TSV-Formaten), fügen Sie &quot;[!UICONTROL Currency]&quot;. Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, wird eine beliebige[!UICONTROL Total]&quot;Geldwerte sind einfach die Summe aller Zahlen in der Spalte, unabhängig von der Währung.</li><li>Berichte, die viele Transaktionseigenschaften oder benutzerdefinierte abgeleitete Metriken enthalten, die viele Transaktionseigenschaften enthalten, können länger dauern, bis sie generiert werden.</li><li>Informationen zum Hinzufügen, Erstellen oder Bearbeiten neuer Metriken finden Sie unter[Benutzerdefinierte Metrik erstellen](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md), &quot;[Benutzerdefinierte Metrik bearbeiten](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md),&quot; und &quot;[Benutzerdefinierte Metrik löschen](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md).&quot;</li><li>Beschreibungen aller verfügbaren Spalten finden Sie unter[Grundlegende und erweiterte Berichtsspalten](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md).&quot;</li></ul> |
|  | [!UICONTROL Order Results/Limit Rows by] | Sortiert den Bericht nach bis zu zwei Spalten, die im Bericht enthalten sind. Die Standardwerte unterscheiden sich für jeden Berichtstyp. Um die Sortierreihenfolge anzupassen, wählen Sie eine Berichtsspalte und dann <i>[!UICONTROL Ascending]</i> (um Ergebnisse von A bis Z oder von 1 bis 100 anzuzeigen) oder <i>[!UICONTROL Descending]</i> (um Ergebnisse von Z bis A oder von 100 bis 1 anzuzeigen). Geben Sie mindestens eine Spalte an, nach der sortiert werden soll. Wenn Sie nach zwei Spalten sortieren, wird der Bericht zunächst nach der ersten angegebenen Spalte und dann nach der zweiten Spalte sortiert. |
|  | [!UICONTROL Include assets with no performance data, except for assets with zero lifetime data] | ([!UICONTROL RSA Asset Report only]) Umfasst Zeilen, für die für die angegebenen Daten keine Leistungsdaten verfügbar sind, wobei Werte von null (0) für die fehlenden Daten eingefügt werden. Standardmäßig ist diese Option nicht ausgewählt und Zeilen werden nur angezeigt, wenn Daten (unabhängig vom Wert) verfügbar sind.<br><br>Wenn diese Option aktiviert ist, enthalten Berichte Leistungsdaten für Anzeigennetzwerkkonten ohne Kampagnen und Kampagnen ohne aktive Suchbegriffe sowie für Komponenten, die im gesamten Datenbereich deaktiviert, ausgesetzt und gelöscht wurden. Darüber hinaus zeigt der RSA Asset-Bericht Zeilen für alle Assets an, mit Ausnahme von Assets mit Nulllebenszeitdaten.<br><br><b>Warnung:</b> Wenn Sie diese Option auswählen und einen Bericht für einen großen Datumsbereich für viele Unterkomponenten erstellen, die keine Daten haben, kann die Erstellung des Berichts lange dauern. |
|  | [!UICONTROL Share with others] | Ermöglicht anderen Benutzern mit Zugriff auf die Daten desselben Advertisers die Anzeige der generierten Berichte und - wenn Sie den Bericht als Vorlage speichern - die Verwendung der Vorlage, aber nicht deren Bearbeitung oder Löschung. Standardmäßig ist diese Option nicht aktiviert. <b>Hinweis:</b> Unabhängig von dieser Einstellung sind Ihre Berichte und Vorlagen für alle Benutzer mit höheren (Administrator-) Benutzerrollen und für alle zugewiesenen Adobe Account Team-Mitglieder sichtbar. |
| [!UICONTROL Advanced Filters] | \[Erweiterte Filter\] | Gibt Zeilen nur zurück, wenn der Wert für eine Metrik bestimmte Kriterien erfüllt; Die Metrik muss nicht als Spalte im Bericht enthalten sein. Die Liste der verfügbaren Metriken variiert je nach Berichtstyp, kann jedoch benutzerdefinierte abgeleitete Metriken für den Advertiser, die IDs und Eigenschaftsnamen für jede Werbenetzwerk- und Portfoliokomponente (z. B. [!UICONTROL Campaign ID] und [!UICONTROL Campaign Status]), Umsatzmetriken (Transaktionseigenschaften) für den Advertiser und klickbezogene Metriken aus den Werbenetzwerken. Verfügbare Operatoren umfassen <i>[!UICONTROL contains]</i>, <i>[!UICONTROL starts with]</i>, <i>[!UICONTROL equals]</i>, <i>[!UICONTROL is greater than]</i>, <i>[!UICONTROL is greater than or equal to]</i>, <i>[!UICONTROL is less than]</i>, <i>[!UICONTROL is less than or equal to]</i>oder <i>[!UICONTROL isn't equal to]</i>.<br><br>Gehen Sie wie folgt vor, um einen oder mehrere Filter anzuwenden:<ul><li>Wählen Sie eine Metrik und einen Operator aus und geben Sie dann den entsprechenden Wert ein. Wenn Sie beispielsweise nur Suchbegriffe mit mehr als 100 Klicks zurückgeben möchten, wählen Sie [!UICONTROL Clicks]auswählen [!UICONTROL >]und geben Sie dann 100 in das Eingabefeld ein.</li><li>(Um weitere Filter anzuwenden) Klicken Sie für jeden zusätzlichen Filter auf **[!UICONTROL +Add Filter]** auswählen **[!UICONTROL AND]** oder **[!UICONTROL OR]**, wählen Sie eine Metrik und einen Operator und geben Sie dann den entsprechenden Wert ein.</li></ul> |
| [!UICONTROL Attribution] | [!UICONTROL Rule] | (Advertiser mit dem pixelbasierten Konversions-Tracking-Dienst für Adobe Advertising; [!UICONTROL AdWords Shopping Performance Report], [!UICONTROL Campaign Daily Impression Share Report]und [!UICONTROL Keyword Daily Impression Share Report] nur) )) Wie werden im Bericht Konversionsdaten zugeordnet? potenziell über mehrere Anzeigenkanäle und Portfolios hinweg in einer Reihe von Ereignissen, die zu einer Konversion führen:<ul><li><i>[!UICONTROL First Event]:</i> Ordnet die Konversion dem ersten gebührenpflichtigen Klick in der Reihe innerhalb des Advertisers zu [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) oder, wenn keine gebührenpflichtigen Klicks aufgetreten sind, zum letzten Impression innerhalb der [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j).</li><li><i>[!UICONTROL Weight First Event More]:</i> Ordnet die Konversion allen Ereignissen in der Reihe zu, die innerhalb der [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j), gibt jedoch dem ersten Ereignis die höchste Gewichtung und den folgenden Ereignissen schrittweise eine geringere Gewichtung. Wenn der Konversion sowohl gebührenpflichtige Klicks als auch Impressionen vorangehen, wird die angegebene Impressionsüberschreibungsgewichtung weiter auf die Impressionen angewendet. Wenn der Konversion nur Impressionen vorangehen, werden die Impressionen nach der Viewthrough-Gewichtung des Werbetreibenden und nicht nach der Impressions-Überschreibung gewichtet.</li><li><i>[!UICONTROL Even Distribution]:</li> Weist die Konversion zu jedem Ereignis in der Reihe gleichermaßen der Viewthrough-Gewichtung des Werbetreibenden zu und nicht der Impressions-Überschreibung.</li><li><i>[!UICONTROL Weight Last Event More]:</i> Ordnet die Konversion allen Ereignissen in der Reihe zu, die innerhalb der [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j), gibt jedoch dem letzten Ereignis die höchste Gewichtung und den vorhergehenden Ereignissen schrittweise eine geringere Gewichtung. Wenn der Konversion sowohl gebührenpflichtige Klicks als auch Impressionen vorangehen, wird die angegebene Impressionsüberschreibungsgewichtung weiter auf die Impressionen angewendet. Wenn der Konversion nur Impressionen vorangehen, werden die Impressionen nach der Viewthrough-Gewichtung des Werbetreibenden und nicht nach der Impressions-Überschreibung gewichtet.</li><li><i>[!UICONTROL Last Event]</i> (Standardeinstellung): Ordnet die Konversion dem letzten gebührenpflichtigen Klick in der Serie im Advertiser zu. [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) oder, wenn keine gebührenpflichtigen Klicks aufgetreten sind, zum letzten Impression innerhalb der [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j).</li><li><i>U-förmig:</i> Ordnet die Konversion allen Ereignissen in der Reihe zu, die innerhalb der [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j), gibt jedoch das erste Ereignis und das letzte Ereignis mit der höchsten Gewichtung an, wobei die Ereignisse in der Mitte des Konversionspfads nach und nach weniger berücksichtigt werden. Wenn der Konversion sowohl gebührenpflichtige Klicks als auch Impressionen vorangehen, wird die angegebene Impressionsüberschreibungsgewichtung weiter auf die Impressionen angewendet. Wenn der Konversion nur Impressionen vorangehen, werden die Impressionen nach der Viewthrough-Gewichtung des Werbetreibenden und nicht nach der Impressions-Überschreibung gewichtet.</li></ul><b>Hinweise:</b><ul><li>Alle Attributionsregeln, außer für [!UICONTROL Last Event] sind nur für Advertiser mit Adobe Advertising-Klick-Tracking und Konversions-Tracking von Adobe Advertising oder Adobe Analytics (mit einer Adobe Analytics-Integration) verfügbar.</li><li>Attributionsregeln gelten für Impressionen auf Display-Anzeigen und für Klicks auf gebührenpflichtige Anzeigen in beliebigen Kanälen. Sie gelten nicht für Impressionen bei Paid Search oder Social-Media-Anzeigen, die nicht auf Ereignisebene verfolgt werden können.</li><li>Wenn Sie Konversionsdaten mit einer beliebigen Attributionsregel melden, mit Ausnahme einer der[!UICONTROL Last Event]&quot;, können die Ereignisse, die zur Konversion führen, über mehrere Portfolios hinweg auftreten. Wenn die Ereignisse in mehreren Portfolios auftreten, enthält der Bericht nur Daten für die Konversion, wenn die Anzeigen oder Suchbegriffe in diesen Portfolios in den Bericht aufgenommen werden.</li><li>([!UICONTROL Transaction Report]) Wenn Sie Transaktionen mit einer beliebigen Attributionsregel melden, mit Ausnahme von &quot;[!UICONTROL Last Event]&quot; oder &quot;[!UICONTROL First Event],&quot;enthält der Bericht eine Zeile für jedes Ereignis im Transaktionspfad.</li></ul> |
|  | [!UICONTROL Impression Override Weight] | (Für alle Attributionsregeln außer [!UICONTROL Last Event] oder [!UICONTROL First Event]) Wenn der Konversion sowohl gebührenpflichtige Klicks als auch Impressionen vorangestellt werden, ordnet den angegebenen Prozentsatz eines Konversionswerts Impressionen zu, die innerhalb der [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). Standardmäßig beträgt dieser Wert 10 %. Sie können den Wert von 0 bis 100 in eine beliebige Zahl ändern. Dieser Wert wird nur innerhalb des Berichts verwendet.<br><br>Wenn einer Konversion nur Impressionen vorangestellt werden, wird die [Viewthrough-Gewichtung](/help/search-social-commerce/glossary.md#u-v)anstelle der Impressionsüberschreibungsgewichtung auf die Impressionen angewendet. |
|  | [!UICONTROL Conversion Attribution] | (Gilt nur für Display-Kampagnen; [!UICONTROL AdWords Shopping Performance Report] nur) Welche Konversionstypen zu melden sind, wenn vorherige Ereignisse aufgetreten sind:<ul><li><i>[!UICONTROL Clicks]:</i> So melden Sie nur Konversionen, die durch Klicks verursacht wurden. Jeder Konversionsname wird mit &quot;[!UICONTROL (CT)].&quot;</li><li><i>[!UICONTROL View-throughs Only]:</i> So melden Sie nur Konversionen, die aus Durchsichten resultierten. Jeder Konversionsname wird mit &quot;[!UICONTROL (VT)].&quot; Wenn Sie diese Option auswählen, wählen Sie den Wert aus, den die Konvertierung erhalten soll. Wählen Sie im Feld View-through-Bewertungsmethode eine Option aus:<ul><li><i>[!UICONTROL Raw]:</i> So melden Sie Konversionen ohne Anwendung einer Gewichtung.</li>li><i>[!UICONTROL Weighted]</i> (Standardeinstellung): So gewichten Sie jede Konversion entsprechend der für den Advertiser festgelegten Viewthrough-Gewichtung.</li></ul></li><li><i>[!UICONTROL Clicks + View-throughs]:</i> So melden Sie alle Konversionen. Standardmäßig wird jeder Konversionsname an &quot;[!UICONTROL (CT+VT)].&quot; Dieser Konversionsattributtyp umfasst zwei zusätzliche Optionen:<ul><li>[!UICONTROL Discreet columns for click & view-through conversions] — Enthält drei separate Spalten für jeden Konvertierungstyp, den Sie einschließen: jeweils eine für 1) Clickthrough-Konversionen, angehängt an &quot;[!UICONTROL (CT)]&quot;, 2) Durchsichtskonvertierungen, angehängt an &quot;[!UICONTROL (VT)]&quot;, 3) und allen Konversionen, die mit &quot;[!UICONTROL (CT+VT)].&quot; Wenn Sie diese Option auswählen, wählen Sie aus den drei Spalten, die Sie zum Filtern und Sortieren verwenden möchten, die[!UICONTROL Filter & sort using]&quot; list: <i>[!UICONTROL click]</i> (Standardeinstellung), <i>[!UICONTROL view-through]</i>oder <i>[!UICONTROL click + view-through]</i>.<br><br><b>Hinweis:</b> Konversionen für Suchkampagnen werden in den Spalten für Clickthroughs angezeigt, nicht aber in der Spalte für Durchsichtskonversionen.</li><li>[!UICONTROL View-through valuation method]: Welchen Wert für jede Konversion angibt, die aus einer Durchsicht resultiert:</li><ul><i>[!UICONTROL Weighted]</i> (Standardeinstellung): So gewichten Sie jede Konversion entsprechend der für den Advertiser festgelegten Viewthrough-Gewichtung.</li><li><i>[!UICONTROL Raw]:</i> So melden Sie Konversionen ohne Anwendung einer Gewichtung.</li></ul></li></ul> |
|  | [!UICONTROL Conversion Attribution] > [!UICONTROL Discrete columns for cross device conversions] | Obsolete |  |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Report Schedule] | (Optional) nur verfügbar, wenn &quot;[!UICONTROL Save as template]&quot;&quot;ausgewählt ist) Wann der Bericht ausgeführt werden soll: <i>[!UICONTROL Now]</i> (den Bericht einmal auszuführen; Standard), <i>[!UICONTROL Daily]</i>, <i>[!UICONTROL Weekly on] [Wochentag]</i>oder <i>[!UICONTROL Every Month] [Tag des Monats]</i>. Alle Zeiträume außer <i>[!UICONTROL Now]</i>, wählen Sie die Stunde in der Zeitzone des Advertisers aus, beginnend mit 09:00 Uhr. |
|  | [!UICONTROL Email Recipients] | <b>Hinweis:</b>  Diese Einstellung wird nur verwendet, wenn E-Mail-Benachrichtigungen für [!UICONTROL Reports] are [aktiviert in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-edit.md).<br><br>E-Mail-Adressen registrierter Search-, Social- und Commerce-Benutzer, an die Benachrichtigungen gesendet werden sollen, wenn der Bericht abgeschlossen ist oder aufgrund von Fehlern abgebrochen wird. Standardmäßig wird die Adresse für Ihr Benutzerkonto angegeben. Um mehrere Adressen anzugeben, trennen Sie sie durch Kommas, Leerzeichen oder neue Zeilen. Wenn die wiederholte Ausführung des Berichts geplant ist, wird bei jedem Abschluss eines Berichts eine Benachrichtigung gesendet. |
|  | [!UICONTROL Email Notification] | <b>Hinweis:</b>  Diese Einstellung wird nur verwendet, wenn E-Mail-Benachrichtigungen für [!UICONTROL Reports] are [aktiviert in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-edit.md).<br><br>(When [!UICONTROL Email Recipients] festgelegt sind) Was in E-Mail-Benachrichtigungen an bestimmte Adressen eingeschlossen werden soll:<ul><li><i>[!UICONTROL Notification Only]</i> (Standardeinstellung): So senden Sie nur eine Benachrichtigung über den Berichtabschluss oder -fehler ohne Anlagen. Die Benachrichtigung enthält temporäre Download-Links für alle Berichtsformate.</li><li><i>[!UICONTROL XLS Attachment]:</i> So fügen Sie eine Kopie des abgeschlossenen Berichts im XLS-Format ein, wenn die Datei kleiner als etwa 10 MB ist. Dateien über 1 MB werden komprimiert.</li><li><i>[!UICONTROL TSV Attachment]:</i> Um eine Kopie des abgeschlossenen Berichts im TSV-Format einzufügen, wenn die Datei kleiner als etwa 10 MB ist. Dateien über 1 MB werden komprimiert.</li><li><i>[!UICONTROL CSV Attachment]:</i> So fügen Sie eine Kopie des abgeschlossenen Berichts im CSV-Format ein, wenn die Datei kleiner als etwa 10 MB ist. Dateien über 1 MB werden komprimiert. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Über Sonderberichte](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md)
>* [Einen Spezialbericht erstellen](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Einstellungen für Sonderberichte](/help/search-social-commerce/reports/management/specialty/specialty-report-settings.md)
>* [Berichtsspalten für Sonderberichte](/help/search-social-commerce/reports/management/specialty/specialty-report-columns.md)
