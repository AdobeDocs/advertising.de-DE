---
title: Häufig gestellte Fragen zu benutzerspezifischen Berichten
description: Erfahren Sie mehr über Antworten auf häufig gestellte Fragen zu Leistungsberichten, einschließlich der Fehlerbehebung bei Datenproblemen.
exl-id: 85707666-7c0f-4aa3-8c91-fb73ef6a5061
source-git-commit: 18d7ec2254dda9e5f94270e13476a521006ec686
workflow-type: tm+mt
source-wordcount: '3919'
ht-degree: 0%

---

# Häufig gestellte Fragen zu benutzerspezifischen Berichten

## Allgemeine Fragen

++ Was passiert, wenn der Datumsbereich für den Bericht beginnt, bevor Berichtsdaten verfügbar sind?
Der Bericht wird generiert, enthält jedoch nur Daten zu den Daten, für die Daten verfügbar sind. Weitere Informationen dazu, wann Daten für jeden Berichtstyp verfügbar sind, finden Sie unter[Die für Berichte verwendeten Daten](data-used-for-reports.md).&quot;
+++

+++ Was ist der Unterschied zwischen dem Klick- und dem Transaktionsdatum-basierten Berichten?
Wenn Sie Konversionen nach Transaktionsdatum melden, enthalten die Daten Transaktionen, deren Transaktionsdatum im angegebenen Zeitraum aufgetreten ist. Diese Option ist die Standardeinstellung in Basisberichten und erweiterten Berichten und zeigt an, wie viel Umsatz innerhalb des festgelegten Zeitraums erzielt wurde.

Wenn Sie Konversionen nach Klickdatum melden, enthalten die Daten Transaktionen, die aus einem Klick resultierten, der während des angegebenen Zeitraums aufgetreten ist. Wenn ein Portfolio erhebliche Verzögerungen zwischen Klicks und Transaktionen aufweist, zeigt diese Art der Berichterstellung den historischen Umsatz pro Klick für das Portfolio an, was Ihnen eine Vorstellung davon gibt, welches Umsatzverhalten im Laufe der Zeit zu erwarten ist.

![Bericht nach Klickdatum versus Bericht nach Transaktionsdatum](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Bericht nach Klickdatum versus Bericht nach Transaktionsdatum")
+++

+++ Was passiert, wenn ich das Klick-Lookback-Fenster oder das Impression-Lookback-Fenster ändere?
(Nur Advertiser mit dem pixelbasierten Konversions-Tracking-Dienst für Werbung) Daten zu Ereignissen, die aus dem ersten Klick resultieren, werden für einen längeren oder kürzeren Zeitraum erfasst.

Ein Advertiser [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) die Anzahl der Tage nach einem bezahlten Klick oder einer (bzw.) Anzeige-Impression bestimmen, in denen das Ereignis einer Konversion zugeordnet werden kann. Eine Änderung eines Werts in einen längeren oder kürzeren Zeitraum kann für Advertiser mit besonders kurzen oder langen Clickthrough-Umsatz- oder Anzeigen-Impressions-zu-Umsatz-Zeiträumen wichtig sein.

**Best Practice:** Stellen Sie sicher, dass die Lookback-Fenster länger sind als die Clickthrough- und Anzeigen-Impressions-zu-Umsatz-Zeiten für die meisten Ihrer Suchbegriffe oder Anzeigen. Wenn sie kürzer sind, werden einige Konversionen nicht mit dem ersten Klick oder der ersten Impression verknüpft.
+++

+++Woher weiß ich, welche Konversionen aus einer [!DNL Google Ads] Anzeigenerweiterung oder Produktliste?
Sie können sehen, welche Konversionen durch einen Klick auf eine [!DNL Google Ads] Anzeigenerweiterung (anstelle der Anzeige selbst) oder auf einer Produktliste durch Generieren einer [!UICONTROL Transaction Report]. Die [!UICONTROL Link Type] -Spaltenwert zeigt den Typ und Titel eines angeklickten Links an:

* Produktlisten werden als `pla:<product ID>`, z. B. `pla:8525822`.

* Sitelinks werden als `sl:<Sitelink text>`, z. B. `sl:See Current Offers`.

  Sie können auch einen Sitelink identifizieren, wenn Sie die [!UICONTROL Tracking URL] in den Bericht ein. Die [!UICONTROL Tracking URL] für einen Sitelink enthält das Attribut `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Konversionen aus [!DNL Google Ads] Standorte und Telefonerweiterungen sind in den Daten für die Anzeigen enthalten, die sie begleiten. Sie werden nicht separat gemeldet.

+++

++ + &quot;[!UICONTROL Keyword]&quot; enthält in meinem Bericht einen Wert &quot;(Inhalt der Gruppe adgroup) &lt;*Anzeigengruppenname*>.&quot;
Wenn die Zeile Daten für inhaltsfähige Suchkampagnen, Display-Kampagnen oder Social-Media-Kampagnen enthält, die keine Keywords enthalten, wird die [!UICONTROL Keyword] zeigt stattdessen den entsprechenden Anzeigengruppennamen an.
+++

+++ Aufgrund saisonaler oder marktrelevanter Veränderungen zeigen meine Berichte atypische Daten. Wird sich dies auf Angebote auswirken, sobald sich die Bedingungen ändern?
Die Optimierungsfunktion erstellt täglich ihre Umsatzmodelle für jede Angebotseinheit, um sicherzustellen, dass sie Trends identifiziert und sofort auf sie reagiert. Die Modelle enthalten langfristige historische Daten, um die saisonale Leistung vorherzusagen. Halbwertseinstellung des Umsatzmodells des Portfolios<!-- add link to glossary? --> bestimmt auch, wie stark aktuelle Umsatzdaten gewichtet werden. Die Best Practice ist, die Halbwertszeit in einem Zeitraum atypischer Performance zu reduzieren, aber nach Anpassung des Umsatzmodells zu erhöhen. Wenden Sie sich bei Fragen dazu, ob eine Anpassung der Halbwertszeit erforderlich ist, an Ihr Adobe Account Team.

Wenn Sie nicht möchten, dass sich die Daten für den Zeitraum auf künftige Angebote auswirken, können Sie diese Daten aus dem Modell ausschließen. Wenden Sie sich an Ihr Adobe Account Team, um die Daten auszuschließen.
+++

+++ Kann ich einen Bericht für eine bestimmte Eigenschaftsmetrik erstellen, z. B. [!UICONTROL Device] oder [!UICONTROL Objective Name]?
Für Kampagnenentitätsberichte ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report]und [!UICONTROL Product Group Report]), werden die Metrikdaten dynamisch durch die Eigenschaftsspalten aggregiert, die Sie in den Bericht einbeziehen. Optional können Sie die Schlüsselspalte für den Bericht entfernen und nur die Eigenschaftenspalten einschließen, für die Sie Daten aggregieren möchten.

Wenn Sie beispielsweise eine [!UICONTROL Keyword Report] , die Folgendes enthält: [!UICONTROL Ad Group] und  Gerätespalten, aggregiert der Bericht dann standardmäßig die Metriken für jeden Suchbegriff nach Anzeigengruppe und Gerätetyp. Wenn Sie jedoch die [!UICONTROL Keyword] vor der Berichterstellung, generiert der Bericht dynamisch Metriken für die angegebenen Anzeigengruppen nach Gerätetyp.

>[!NOTE]
>
>Sie können diese Funktion nicht verwenden, um Daten nach Beschriftungsklassifizierungen zu aggregieren. Alle Titel-Classification-Spalten im Bericht werden weggelassen. Verwenden Sie stattdessen die [Beschriftungsklassifizierungsbericht](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Allgemeine Datenfragen

+++Berichte, die mit verschiedenen Attributionsregeln erstellt wurden, zeigen unterschiedliche Summen an.
Wenn Sie einen Bericht mehrmals mit denselben Berichtsparametern, jedoch mit unterschiedlichen Attributionsregeln generieren, können die Daten aus einem der folgenden Gründe unterschiedlich sein:

* Klickdatumsbasierte Daten können außerhalb des angegebenen Datumsbereichs liegen.

  Wenn Sie den Berichtsparameter &quot;[!UICONTROL Conversions based on click date],&quot;wird der angegebene Datumsbereich auf das Datum des Klicks anstelle des Transaktionsdatums angewendet. Wenn der Bericht auch die Attributionsregel &quot;Erstes Ereignis&quot;oder &quot;Letztes Ereignis&quot;verwendet, kann das erste oder letzte Ereignis, das zur Konversion geführt hat, außerhalb des angegebenen Datumsbereichs liegen. Angenommen, ein Benutzer hat am 30. April auf Keyword_1 geklickt, am 20. Mai auf Keyword_2 geklickt und am 21. Mai konvertiert. Wenn der Bericht die Variable[!UICONTROL First Event]&quot; Attributionsregel und Datumsbereich vom 1. bis 21. Mai ist das erste Ereignis (ein Klick auf Keyword_1 am 30. April) nicht im Bericht enthalten. Wenn Sie den Bericht mit demselben Datumsbereich ausführen, aber die &quot;[!UICONTROL Last Event]&quot;, dann wird die Konversion in den Bericht aufgenommen, da der letzte Klick innerhalb des angegebenen Datumsbereichs erfolgte.

* Bei der Auswahl des Portfoliofilters werden einige der Ereignisse ausgeschlossen, die zur Konversion führten.

  Wenn Sie einen Bericht zu einer Untergruppe von Portfolios erstellen, schließen Sie möglicherweise nicht die Kampagnen ein, die das Ereignis enthielten, dem die Konversion unter einer der Attributionsregeln zugeordnet wurde. Angenommen, ein Benutzer klickt von Portfolio_1 auf Keyword_1, klickt auf Keyword_2 von Portfolio_2 und konvertiert dann. Wenn der Bericht die Variable[!UICONTROL First Event]&quot;. Dann muss Portfolio_1 angegeben werden, damit die Konversion in den Bericht aufgenommen wird. Wenn der Bericht jedoch die Attributionsregel &quot;Letztes Ereignis&quot;verwendet, muss Portfolio_2 einbezogen werden.

>[!TIP]
>
>Wenn Sie Konversionssummen unter verschiedenen Attributionsregeln vergleichen möchten, führen Sie Berichte mit dem Berichtsparameter aus.[!UICONTROL Conversions based on transaction date]und wählen Sie alle Anzeigennetze oder alle Portfolios aus. Wenn Sie keine anderen Filter festlegen, sollten die Konvertierungssummen übereinstimmen.

+++

Die Felder +++Individuelle Daten sind falsch, obwohl die Summen korrekt sind.
Diese Situation kann auftreten, wenn die Metrikformate Ganzzahlen verwenden:

* Wenn Sie eine [benutzerspezifische Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) mit dem Format *Anzahl mit Dezimalstellen* (die Daten als Ganzzahlen anzeigt) und sie in eine Ansicht oder einen Bericht mit einer gewichteten Konversionszuordnungsregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]oder [!UICONTROL Even Distribution]), wird die Ausgabe in Ganzzahlen und nicht in Dezimalstellen angezeigt. In diesem Fall sind die einzelnen Datenfelder möglicherweise falsch, obwohl die Summen korrekt sind. Wenn eine Bestellung beispielsweise gleichmäßig zwischen drei Ereignissen aufgeteilt ist, wird jedem der drei Ereignisse eine Bestellung (statt einer Reihenfolge von 0,33) zugeordnet. Um das Problem zu beheben, [Ändern des Metrikformats](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) nach *Anzahl bis 2 Dezimalstellen*.

* Wenn Sie eine Umsatzmetrik haben, die als Ganzzahl gesendet wird, tritt dasselbe Problem auf. (Das Umsatzformat wird durch das Konversions-Tag gesteuert, das die Daten sendet.) Um das Problem zu beheben, [Erstellen einer benutzerdefinierten Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) ausschließlich aus der Umsatzmetrik und dem Format besteht *Anzahl bis 2 Dezimalstellen*und sie in Ansichten und Berichte statt in die ursprüngliche Metrik aufnehmen.
+++

+++ Wenn Klick- oder Umsatzdaten fehlen, wie kann ich verhindern, dass sich dies auf zukünftige Angebote auswirkt?
Klickdatenprobleme treten auf, wenn Search, Social und Commerce nicht mit dem Anzeigennetzwerk synchronisiert sind. Wenden Sie sich an Ihr Adobe Account Team, um das Konto manuell zu synchronisieren. Wenn Klickdaten für einen ganzen Tag fehlen, bitten Sie Ihr Adobe Account Team, diesen Tag von den Kostenmodellen auszuschließen.

Umsatzdatenprobleme können aufgrund eines Tracking- oder Feed-Dateiproblems auftreten. Wenden Sie sich an Ihr Adobe Account Team, um das Problem zu untersuchen. Wenn Umsatzdaten einen ganzen Tag lang fehlen, bitten Sie Ihr Kundenbetreuungsteam, diesen Adobe von den Umsatzmodellen auszuschließen.
+++

+++Währungsdaten werden im falschen Format angezeigt.
Standardmäßig werden alle monetären Daten in Berichten im Format für US-Dollar angezeigt (z. B. 1.000,00). Um den Wert im korrekten Währungsformat anzuzeigen (jedoch ohne Währungssymbole in CSV- und TSV-Formaten), fügen Sie &quot;[!UICONTROL Currency]&quot;. Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, wird eine beliebige[!UICONTROL Total]&quot;Geldwerte sind einfach die Summe aller Zahlen in der Spalte, unabhängig von der Währung.
+++

+++ Warum sehe ich Dezimalwerte für eine Transaktionseigenschaft, die eine natürliche Zahl sein sollte (1, 2 usw.)?
In den folgenden Fällen können Dezimalwerte angezeigt werden:

* Wenn Sie den Bericht mit einem anderen Konversionsattributionsparameter als [!UICONTROL Last Event] oder [!UICONTROL First Event], kann der Umsatz auf mehrere Ereignisse im Konversionspfad aufgeteilt werden.

* Im [!UICONTROL Transaction Report], wenn mehrere [Bid-Einheiten](/help/search-social-commerce/glossary.md#a-b) mit verschiedenen Übereinstimmungstypen haben dieselbe Transaktions-ID, wird der Umsatz für die Tracking-ID entsprechend der Anzahl der Klicks auf das angegebene Klickdatum aufgeteilt.
+++

## Standardleistungsmetriken

+++Klick-Daten fehlen in Berichten.
Im Folgenden finden Sie häufige Gründe für das Fehlen von Klickdaten.

| Ursache | Erkennung/Analyse | Auflösung |
|---|---|---|
| Der Prozess, der Klickdaten aus dem Anzeigenkonto abruft, ist fehlgeschlagen. | Es gibt keine systematische Möglichkeit, dieses Problem zu erkennen. Sie können jedoch feststellen, dass eine Kampagne keine Kosten- oder Klickinformationen anzeigt, auch wenn das Anzeigenkonto Geld ausgegeben hat. | Kontaktieren Sie den Kundensupport unter &lt;*Ihr Benutzerkonto für Suche, Social und Commerce*>@support\.efrontier\.com.<!-- Escaped periods and using HTML code for angle brackets --><br><br>Wenn die Daten länger als 24 Stunden fehlen, schließen Sie diese Daten aus den Kostenvorausschätzungen aus, bis die Daten abgerufen werden. Ihr Adobe-Kontoteam kann die Daten ausschließen. |
| Ein Abrechnungsfehler zwischen dem Advertiser und dem Werbenetzwerk verhindert, dass das Werbekonto ausgegeben wird. | Es gibt keine systematische Möglichkeit, dieses Problem zu erkennen. Sie können jedoch feststellen, dass eine Kampagne keine Kosten- oder Klickinformationen anzeigt. | Wenn Sie wissen, dass ein Werbekonto aufgrund eines Abrechnungsproblems nicht ausgegeben werden konnte, schließen Sie diese Daten aus den Kostenprognosen aus. Ihr Adobe-Kontoteam kann die Daten ausschließen. |
+++

+++ Leistungsdaten unterscheiden sich von Daten im Werbenetzwerk-Editor.
Wenn das Werbenetzwerk Aktualisierungen an frühere Daten sendet (häufig weil sie Klickbetrug einigen Klicks zugeordnet haben), werden die Daten nur dann von Search, Social und Commerce aktualisiert, wenn mehr als 5 % Diskrepanz vorliegen und das Adobe Account Team eine Anfrage sendet.

Wenn Sie außerdem Daten von Impressions-Freigaben vergleichen, die über einen Datumsbereich aggregiert wurden, können die in den Berichten &quot;Search&quot;, &quot;Social&quot;und &quot;Commerce&quot;enthaltenen Daten von den Daten abweichen, die das Anzeigennetzwerk meldet. Dieser Unterschied liegt daran, wie die Daten von der API des Anzeigennetzwerks gemeldet werden, mit der Search, Social und Commerce Daten abrufen. Beispiel: für [!DNL Google Ads] data:

* Für die meisten Impressions-Share-Metriken: [!DNL Google Ads] Begrenzt entweder das untere oder das obere Ende der Werte, die für Werte angegeben werden, die kleiner als 10 % oder größer als 90 % sind. Die Daten werden als 0,0999 für &lt;10% und 0,9001 für >90% gemeldet.

* Wenn im Datumsbereich eine Mischung aus gecappten und nicht zugewiesenen Daten vorhanden ist, aggregiert Search, Social und Commerce Impressions-Share-Daten anhand der Werte, die im Istzustand in der API gesendet werden, wobei 0,0999 für Zeilen mit &lt;10 % und 0,9001 für Zeilen mit >90 % verwendet werden. Diese Aggregation kann zu einer Abweichung von der [!DNL Google Ads] voraggregierte Daten, weil [!DNL Google Ads] kann tatsächliche Prozentwerte verwenden, z. B. 7 % oder 97 %.
+++

+++ Leistungsdaten in Berichten unterscheiden sich von den Daten in [!DNL Google Analytics].
Die beiden Systeme messen unterschiedliche Daten, sodass Sie erwarten sollten, dass andere Daten angezeigt werden. Beispiel:

* Klicks werden in Search, Social und Commerce (und Google Ads) verfolgt, während Klicks in [!DNL Google Analytics] verfolgt Besuche pro 30-minütige Browser-Sitzung. Wenn ein Benutzer beispielsweise einmal auf Ihre Anzeige klickt, dann auf die Schaltfläche &quot;Zurück&quot;und dann erneut auf die Anzeige klickt, werden in Search, Social und Commerce zwei Klicks aufgezeichnet, aber [!DNL Google Analytics] erfasst einen Besuch.

* [!DNL Google Analytics] zeigt alle Traffic-Daten an, während &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;(und [!DNL Google Ads]) filtert ungültige Klicks (z. B. übermäßige, wiederholte Klicks).

* [!DNL Google Analytics] enthält Klick- und Umsatzdaten für alle Klicks. In Search, Social und Commerce können Klick- und Umsatzdaten für Anzeigen und Suchbegriffe mit falschen oder fehlenden Tracking-URLs nicht verfolgt werden.
+++

## Konversionsmetriken

+++ Mein Bericht zeigt keine Konversionsdaten an.
Der Bericht enthält möglicherweise keine Konversionsmetriken, für die Konversionen aufgetreten sind.
+++

+++Umsatz fehlt in Berichten.

**Advertiser, die Adobe Advertising-Konversions-Tags verwenden**

*Mögliche Ursachen:*

* Suchbegriffe oder Anzeigen wurden hinzugefügt, ohne den Tracking-Vorlagen oder Ziel-URLs das Klick-Tracking-Präfix &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;voranzustellen, oder das Tracking-Präfix ist falsch.

* Das Konversions-Tracking-Tag wurde nicht auf allen entsprechenden Webseiten korrekt implementiert oder bearbeitet.

* Die Transaktionseigenschaften, die von Search, Social und Commerce verfolgt werden, werden aus Berichten ausgeschlossen und sind daher nicht sichtbar.

* Der Umsatz-Parser für den Client wurde nicht implementiert.

*Mögliche Lösung oder Problemumgehung:*

1. Überprüfen Sie, ob die korrekten Spalten in den Berichten oder Datenansichten enthalten sind. Wenn die entsprechenden Spalten nicht hinzugefügt werden können, müssen Sie oder Ihr Adobe Account Team [Bereitstellen der Transaktionseigenschaften für Berichte](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. Stellen Sie sicher, dass die richtigen Konversions-Tracking-Tags auf allen entsprechenden Webseiten implementiert sind. Wenden Sie sich bei Bedarf an Ihr Kundenbetreuungsteam, um eine Testtransaktion für jedes zutreffende Konversions-Tracking-Tag zu erstellen und die Details der Transaktion zu erfassen, z. B. die `transactionid` und Details aus dem Cookie (z. B. der `trackingid`, `clickid`usw.).

1. Wenn die Variable [!UICONTROL Auto Upload] -Option für die Kampagne deaktiviert ist und Sie Suchbegriffe oder Anzeigen hinzugefügt haben, müssen Sie dann sicherstellen, dass Sie eine Tracking-Vorlage oder Ziel-URL generiert haben, die das Klick-Umleitungs-Tracking für Search, Social und Commerce enthält. Ihr Adobe-Kontoteam kann einen internen Bericht ausführen, um zu sehen, ob Klick-Tracking-URLs (Tracking-Vorlagen oder Ziel-URLs) fehlen oder fehlerhaft sind.

   Generieren Sie bei Bedarf ein Tracking, indem Sie eine Bulksheet-Datei mit den richtigen URLs erstellen und die Datei mithilfe der **Tracking-URLs generieren** -Option.

   Die Ziel-URL sollte mit &quot;http://pixel.everesttech.net&quot;oder &quot;https://pixel.everesttech.net&quot;beginnen.

1. Wenn keiner dieser Schritte das Problem behebt, dann [Kundenunterstützung kontaktieren](/help/search-social-commerce/get-help.md).

   Wenn der Client noch nicht gestartet wurde oder neu gestartet wurde, überprüft die Kundenunterstützung, ob ein Revenue Parser eingerichtet wurde. Wenn der Parser eingerichtet ist, überprüfen sie, ob Search, Social und Commerce Pixelkonvertierungen erhalten und beheben das Problem.

**Werbetreibende, die Konversionsdaten-Feeds senden**

*Mögliche Ursachen:*

* Die Feed-Datei wurde nicht bereitgestellt, sie wurde nicht vollständig analysiert oder der Feed enthielt verwaiste Transaktionen.

* Die relevanten Transaktionseigenschaften werden aus Berichten ausgeschlossen und sind daher nicht sichtbar.

>[!NOTE]
>
>Daten werden in der Benutzeroberfläche im Allgemeinen erst 2-4 Stunden nach Erhalt des Feeds angezeigt.

*Mögliche Lösung oder Problemumgehung:*

1. Überprüfen Sie, ob die korrekten Spalten in den Berichten oder Datenansichten enthalten sind. Wenn die entsprechenden Spalten nicht hinzugefügt werden können, müssen Sie oder Ihr Adobe Account Team [Bereitstellen der Transaktionseigenschaften für Berichte](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. Führen Sie die [!UICONTROL Portfolio Report]. Wenn es leer ist, führen Sie die [!UICONTROL Campaign Report] und [!UICONTROL Search Engine Report] um zu sehen, ob der Umsatz in diesen Berichten auftaucht. Ist dies der Fall, werden die Kampagnen möglicherweise nicht dem entsprechenden Portfolio zugewiesen.

1. Vergewissern Sie sich, dass die Datei an den Umsatzserver gesendet wurde und dass die Datei dasselbe Format und dieselbe Dateibenennungskonvention wie die vorherigen Dateien verwendet hat.

   Wenn das Format oder die Dateibenennungskonvention geändert wurden, korrigieren Sie die Datei und senden Sie sie erneut.

1. Wenn die Datei gesendet wurde, dann [Kundenunterstützung kontaktieren](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung prüft, ob die Datei empfangen und analysiert wurde. Wenn die Datei fehlerfrei verarbeitet wurde, wird geprüft, ob verwaiste Transaktionen vorliegen.
+++

+++ Einige erweiterte Berichte enthalten keine Konversionsdaten, die von einem Advertiser-Feed bereitgestellt werden.
Die [!UICONTROL Geo Distribution Report] und [!UICONTROL Domain Referral Report] Daten verwenden, die über den Adobe Advertising-Konversions-Tracking-Dienst erfasst wurden und nur für Advertiser mit dem Dienst generiert werden können. Die Berichte enthalten keine Konversionsdaten, die außerhalb des Adobe Advertising-Konversions-Tracking-Systems verfolgt werden.
+++

+++Umsatzdaten unterscheiden sich von den eigenen Umsatzdaten des Advertisers.

**Advertiser, die Adobe Advertising-Konversions-Tags verwenden**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abgelaufen oder gelöscht ist. Der Werbetreibende kann dies jedoch als gültigen Umsatz betrachten.

* Der Traffic zur Seite des Werbetreibenden stammt von einem Lesezeichen oder einer organischen Suche anstelle einer Anzeige.

* Das Konversions-Tracking-Tag wurde nicht auf allen entsprechenden Webseiten korrekt implementiert oder bearbeitet.

*Mögliche Lösung oder Problemumgehung:*

1. Navigieren Sie zu **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die von Search, Social und Commerce empfangenen Transaktionen mit den Daten des Advertisers.

1. Wenn einige Transaktionen falsch sind oder fehlen, stellen Sie sicher, dass das entsprechende Konversions-Tracking-Tag auf allen zutreffenden Webseiten implementiert ist und nicht bearbeitet wurde, es sei denn, Ihr Adobe-Kundenbetreuungsteam hat Sie dazu angewiesen. Wenn die Website kürzlich aktualisiert wurde, fehlt möglicherweise ein -Tag oder ändert es sich.

   Search, Social und Commerce erwarten wohlgeformte URLs (mit Parametern in Name/Wert-Paaren) innerhalb der Variablen `ef_transaction_properties` und innerhalb der Variablen `src` -Element `img` -Tag.

1. Wenn Sie das Problem nicht ermitteln und beheben können, dann [Kundenunterstützung kontaktieren](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung versucht, die fehlenden Transaktionen zu identifizieren und dann nach verwaisten Transaktionen und Transaktionen zu suchen, die nicht von einer Anzeige stammen (&quot;nicht korrelierte Konversionen&quot;).

**Advertiser mit Konversionsdaten-Feeds mit `ef_id` values**

Siehe mögliche Ursachen und Lösungen für Pixelimplementierungen oben.

**Advertiser mit Konversionsdaten-Feeds mithilfe von Transaktions-IDs**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abläuft oder gelöscht wird. Der Advertiser kann jedoch den Umsatz als gültig betrachten.

* Der Traffic zur Seite des Werbetreibenden stammt von einem Lesezeichen oder einer organischen Suche anstelle einer Anzeige.

* Eine Offline-Konversion wurde gemeldet, bevor eine Online-Transaktion mit derselben Transaktions-ID erfolgte. Die Online-Transaktion muss zuerst stattfinden.

*Mögliche Lösung oder Problemumgehung:*

1. Navigieren Sie zu **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die von Search, Social und Commerce empfangenen Transaktionen mit den Feed-Daten des Advertisers.

1. Wenn eine Transaktion in der Feed-Datei im Bericht fehlt, überprüfen Sie, ob vor der Offline-Konversion eine Online-Transaktion mit derselben Transaktions-ID (verfolgt über das Pixel) aufgetreten ist.

1. Wenn Sie das Problem nicht ermitteln und beheben können, dann [Kundenunterstützung kontaktieren](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung sucht nach Fehlern beim Analysieren von Daten und [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p).

**Advertiser mit anderen Arten von Konversionsdaten-Feeds**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abgelaufen oder gelöscht ist. Der Werbetreibende kann dies jedoch als gültigen Umsatz betrachten.

* Der Traffic zur Seite des Werbetreibenden stammt von einem Lesezeichen oder einer organischen Suche anstelle einer Anzeige.

* Es gibt [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p), also zählt Search, Social und Commerce nicht den gesamten Umsatz, den sie erzielen sollte.

* Der Advertiser validierte einen Bericht zu Search, Social und Commerce für einen anderen Datensatz als den im Feed gesendeten.

* Die Transaktions-IDs (`ev_transid` -Werte) nicht gesendet wurden, nicht eindeutig sind oder falsch sind.

* Die Feed-Datei enthält doppelte Tracking-IDs.

* Beim Analysieren der Datei sind Fehler aufgetreten.

* Die Deduplizierungslogik des Advertisers unterscheidet sich von der Logik von &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;.

*Mögliche Lösung oder Problemumgehung:*

1. Navigieren Sie zu **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die von Search, Social und Commerce empfangenen Transaktionen mit den Daten des Advertisers.

1. Wenn einige Transaktionen falsch sind oder fehlen, stellen Sie sicher, dass a) die Feed-Datei alle erforderlichen Transaktions-IDs und keine doppelten Tracking-IDs enthält und b) die Transaktions-IDs eindeutig und korrekt sind.

1. Wenn Sie das Problem nicht ermitteln und beheben können, dann [Kundenunterstützung kontaktieren](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung sucht nach Fehlern beim Analysieren von Daten und verwaisten Transaktionen.
+++

+++Umsatzdaten unterscheiden sich von den Daten in Adobe Analytics Siehe [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Spezifische Berichte

+++ Sollte die [!UICONTROL Portfolio Report] die gleichen Zahlen wie die [!UICONTROL Portfolios] Ansicht?
Die [!UICONTROL Portfolio Report] und [!UICONTROL Portfolios] -Ansicht zeigen dieselben Daten an, wenn alle Filter für die Ansicht, die Berichtsparameter und die Datenspalten für die Ansicht und den Bericht identisch sind. Wenn beispielsweise die Variable [!UICONTROL Portfolios] Ansicht zeigt Portfolios mit[!UICONTROL All but inactive]&quot; für den Datumsbereich &quot;[!UICONTROL Last 7 days]&quot;, wobei nur die Standarddatenspalten angezeigt werden, wird ein [!UICONTROL Portfolio Report] die Verwendung der Standardparameter zeigt identische Daten an. Wenn Sie einen der Berichtsparameter ändern oder andere Filter im [!UICONTROL Portfolios] anzeigen, können sich die Datenwerte unterscheiden.
+++

+++ Die Daten in der [!UICONTROL Portfolio Report] stimmt nicht mit den Daten in meiner [!UICONTROL Search Engine Report] oder [!UICONTROL Search Engine Account Report].
Die [!UICONTROL Portfolio Report] zeigt nur Daten für die Kampagnen an, die den angegebenen Portfolios zugewiesen sind, aber die [!UICONTROL Search Engine Report] und [!UICONTROL Search Engine Account Report] kann auch Daten für Kampagnen enthalten, die keinem Portfolio zugewiesen sind.
+++

+ + + Wie ist die [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] von der Portfolioebene abweichen [!UICONTROL Model Accuracy Report]?
(Nur Agentur-Kundenbetreuer, Adobe-Kundenbetreuer und Administratorbenutzer) Die [!UICONTROL Forecast Accuracy Report] verfügbar unter [!UICONTROL Reports] > [!UICONTROL Model Accuracy] liefert dieselben Daten wie die Portfolioebene [!UICONTROL Model Accuracy Report] Sie können sie jedoch über mehrere Portfolios hinweg ausführen und die Attributionsregel ändern. Sie können den Bericht auch mit benutzerdefinierten Parametern ausführen und planen und ihn zur Erstellung von Tabellenfeeds verwenden. Darüber hinaus wird die [!UICONTROL Forecast Accuracy Report] genauer als der alte Bericht auf Portfolioebene, da er die Genauigkeit der Einnahmen anhand der historischen Ziele für das Portfolio und nicht anhand des aktuellen Ziels bewertet und die Daten für die anwendbare Zeitzone genauer darstellt.
+++

+++Daten auf Anzeigenebene sind nicht verfügbar für [!DNL Google Ads] dynamische Suchanzeige (DSA), Leistungsmax, intelligentes Einkaufen und [!DNL YouTube] Kampagnen.
Die Werbenetzwerke stellen nicht die Kennung bereit, die erforderlich ist, um einer einzelnen Anzeige für diese Kampagnen Umsätze zuzuordnen. Folglich stehen für diese Kampagnentypen in der Variablen [!UICONTROL Ads] oder in der [!UICONTROL Ad Variation Report]. Erwarten Sie Diskrepanzen zwischen den Gesamtdaten der Anzeigenebene für eine Kampagne und den Gesamtdaten für die Kampagne.
+++

+++In der [!UICONTROL Transaction Report]Wie weiß ich, welche Transaktionseigenschaft von einem Daten-Feed stammt oder vom Adobe Advertising-Tracking-Pixel verfolgt wird?
In einem Transaktionsbericht können Sie feststellen, ob eine enthaltene Transaktionseigenschaft vom Adobe Advertising-Tracking-Pixel verfolgt wurde, wenn Sie die benutzerdefinierte Spalte &quot;[!UICONTROL Tracking URL].&quot; Tracking-URLs mit dem Adobe Advertising-Tracking-Pixel beginnen mit &quot;`http://pixel.everesttech.net`.&quot;
+++

+++ Die Daten in der [!UICONTROL Transaction Report] stimmt nicht mit den Daten in meiner [!UICONTROL Keyword Report].
Wenn Sie beide Berichte nach Portfolio generieren, unterscheiden sich die Daten, wenn Sie die [!UICONTROL Keyword Report] Verwendung historischer Daten (d. h. basierend auf der Portfoliokonfiguration während der angegebenen Datumsangaben) anstelle der Verwendung von Daten für die aktuellen Kampagnen. Wenn Sie die [!UICONTROL Transaction Report] nach Portfolio enthält sie Daten für die aktuellen Kampagnen im Portfolio.
+++

## Tabellen-Feeds

Die Ausgabe von +++ Berichten enthält eine Mischung aus Datumsbereichen.
Es können verschiedene Datumsbereiche angezeigt werden, wenn der Feed Daten mithilfe einer anderen Datenaggregationsebene als &quot;[!UICONTROL Daily].&quot;

Um das Problem zu beheben, aktualisieren Sie den Tabellenfeed, um täglich aggregierte Daten einzuschließen. Diese Aufgabe umfasst die Aktualisierung der Berichtsvorlage, die Erstellung eines Berichts mithilfe der Vorlage und die Erstellung eines benutzerdefinierten [!DNL Microsoft® Excel] Vorlage verwenden und dann die Feed-Einstellungen aktualisieren, um die neue Excel-Vorlage einzuschließen. Weitere Informationen finden Sie unter &quot;[Bearbeiten der Feed-Einstellungen für Tabellenberichte](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

++ + Ein Tabellenfeed führt zu einem internen Fehler.
Dieser Fehler kann auftreten, wenn Sie die Spalten in der Berichtsvorlage ändern, aber die [!DNL Microsoft® Excel] entsprechend.

Um das Problem zu beheben, aktualisieren Sie den Tabellenfeed, um die neuen Spalten einzuschließen. Diese Aufgabe umfasst die Aktualisierung der Berichtsvorlage, die Erstellung eines Berichts mithilfe der Vorlage und die Erstellung eines benutzerdefinierten [!DNL Excel] Vorlage verwenden und dann die Feed-Einstellungen aktualisieren, um die neue Excel-Vorlage einzuschließen. Weitere Informationen finden Sie unter &quot;[Bearbeiten der Feed-Einstellungen für Tabellenberichte](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++ Wenn ich versuche, einen Tabellenfeed in [!DNL Excel], [!DNL Excel] meldet den Fehler &quot;Unlesbarer Inhalt&quot;, und Daten werden aus dem wiederhergestellten Inhalt entfernt.
Wenn die [!DNL Microsoft® Excel] -Vorlage die Daten nicht nach Startdatum in aufsteigender Reihenfolge sortiert, kann der Tabellenfeed leere Zeilen enthalten. Insbesondere [!DNL Excel] meldet den Fehler &quot;Excel hat unlesbaren Inhalt in &#39;&lt;*Berichtsname*>.xlsx.&#39; Möchten Sie den Inhalt der Arbeitsmappe wiederherstellen? Wenn Sie der Quelle dieser Arbeitsmappe vertrauen, klicken Sie auf &quot;Ja&quot;. Wenn Sie auf &quot;Ja&quot;klicken, erhalten Sie die folgende Meldung: &quot;Entfernte Datensätze: Zellinformationen aus /xl/worksheets/sheet1.xml Teil&quot;, und der Arbeitsblatt-Feed enthält leere Zeilen.

Um das Problem zu beheben, bearbeiten Sie die [!DNL Excel] Vorlage, die mit dem Feed verknüpft ist, um Daten nach [!DNL Start date in Ascending (Oldest to Newest) order]und laden Sie dann die aktualisierte Vorlage über die Tabellen-Feed-Einstellungen hoch. Weitere Informationen finden Sie unter &quot;[Bearbeiten von Tabellenbericht-Feeds](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++
