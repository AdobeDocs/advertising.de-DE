---
title: Häufig gestellte Fragen zu benutzerspezifischen Berichten
description: Hier erhalten Sie Antworten auf häufig gestellte Fragen zu Leistungsberichten, einschließlich der Fehlerbehebung bei Datenproblemen.
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# Häufig gestellte Fragen zu benutzerspezifischen Berichten

## Allgemeine Fragen

++ Was passiert, wenn der Datumsbereich für den Bericht beginnt, bevor Berichtsdaten verfügbar sind?
Der Bericht wird generiert, enthält jedoch nur Daten zu den Daten, für die Daten verfügbar sind. Weitere Informationen dazu, wann für jeden Berichtstyp Daten verfügbar sind, finden Sie unter &quot;[Für Berichte verwendete Daten](data-used-for-reports.md)&quot;.
+++

+++ Was ist der Unterschied zwischen dem Klick- und dem Transaktionsdatum-basierten Berichten?
Wenn Sie Konversionen nach Transaktionsdatum melden, enthalten die Daten Transaktionen, deren Transaktionsdatum im angegebenen Zeitraum aufgetreten ist. Diese Option ist die Standardeinstellung in Basisberichten und erweiterten Berichten und zeigt an, wie viel Umsatz innerhalb des festgelegten Zeitraums erzielt wurde.

Wenn Sie Konversionen nach Klickdatum melden, enthalten die Daten Transaktionen, die aus einem Klick resultierten, der während des angegebenen Zeitraums aufgetreten ist. Wenn ein Portfolio erhebliche Verzögerungen zwischen Klicks und Transaktionen aufweist, zeigt diese Art der Berichterstellung den historischen Umsatz pro Klick für das Portfolio an, was Ihnen eine Vorstellung davon gibt, welches Umsatzverhalten im Laufe der Zeit zu erwarten ist.

![Bericht nach Klickdatum versus Bericht nach Transaktionsdatum](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Bericht nach Klickdatum versus Bericht nach Transaktionsdatum")
+++

+++ Was passiert, wenn ich das Klick-Lookback-Fenster oder das Impression-Lookback-Fenster ändere?
(Nur Advertiser mit pixelbasiertem Konversions-Tracking-Dienst von Advertising) Daten zu Ereignissen, die aus dem ersten Klick resultieren, werden für einen längeren oder kürzeren Zeitraum erfasst.

Das [Klick-Lookback-Fenster eines Werbetreibenden](/help/search-social-commerce/glossary.md#c-d) und das [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) bestimmen die Anzahl der Tage, nach denen ein gebührenpflichtiger Klick oder eine Display-Impression (bzw. eine Anzeige-Impression) auftritt, in denen das Ereignis einer Konversion zugeordnet werden kann. Eine Änderung eines Werts in einen längeren oder kürzeren Zeitraum kann für Advertiser mit besonders kurzen oder langen Clickthrough-Umsatz- oder Anzeigen-Impressions-zu-Umsatz-Zeiträumen wichtig sein.

**Best Practice:** Stellen Sie sicher, dass die Lookback-Fenster für die meisten Ihrer Suchbegriffe oder Anzeigen länger sind als die Clickthrough-Umsatz- und Impression-to-Umsatz-Zeiten. Wenn sie kürzer sind, werden einige Konversionen nicht mit dem ersten Klick oder der ersten Impression verknüpft.
+++

+++ Wie weiß ich, welche Konversionen aus einer [!DNL Google Ads] Anzeigenerweiterung oder Produktliste resultierten?
Sie können sehen, welche Konversionen durch einen Klick auf eine [!DNL Google Ads] -Anzeigenerweiterung (statt auf die Anzeige selbst) oder auf eine Produktliste durch Generieren von [!UICONTROL Transaction Report] entstanden sind. Der Spaltenwert [!UICONTROL Link Type] zeigt den Typ und Titel eines angeklickten Links an:

* Produktlisten werden als `pla:<product ID>` aufgeführt, z. B. `pla:8525822`.

* Sitelinks werden als `sl:<Sitelink text>` aufgeführt, z. B. `sl:See Current Offers`.

  Sie können auch einen Sitelink identifizieren, wenn Sie die Spalte [!UICONTROL Tracking URL] in den Bericht einbeziehen. Die [!UICONTROL Tracking URL] für einen Sitelink enthält das Attribut `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Konversionen von [!DNL Google Ads] Standorten und Telefonerweiterungen sind in den Daten für die Anzeigen enthalten, die sie begleiten. Sie werden nicht separat gemeldet.

+++

+++ Die Spalte &quot;[!UICONTROL Keyword]&quot; in meinem Bericht enthält den Wert &quot;(Adgroup content) &lt;*Anzeigengruppenname*>&quot;.
Wenn die Zeile Daten für inhaltsfähige Suchkampagnen, Display-Kampagnen oder Social-Media-Kampagnen enthält, die keine Suchbegriffe enthalten, zeigt die Spalte &quot;[!UICONTROL Keyword]&quot;stattdessen den entsprechenden Anzeigengruppennamen an.
+++

+++ Aufgrund saisonaler oder marktrelevanter Veränderungen zeigen meine Berichte atypische Daten. Hat dies Auswirkungen auf Gebote, sobald sich die Bedingungen ändern?
Die Optimierungsfunktion erstellt täglich ihre Umsatzmodelle für jede Angebotseinheit, um sicherzustellen, dass sie Trends identifiziert und sofort auf sie reagiert. Die Modelle enthalten langfristige historische Daten, um die saisonale Leistung vorherzusagen. Die Einstellung der Halbwertszeit des Umsatzmodells des Portfolios<!-- add link to glossary? --> bestimmt auch, wie stark aktuelle Umsatzdaten gewichtet werden. Die Best Practice ist, die Halbwertszeit in einem Zeitraum atypischer Performance zu reduzieren, aber nach Anpassung des Umsatzmodells zu erhöhen. Wenden Sie sich bei Fragen dazu, ob eine Anpassung der Halbwertszeit erforderlich ist, an Ihr Adobe Account Team.

Wenn Sie nicht möchten, dass sich die Daten für den Zeitraum auf künftige Angebote auswirken, können Sie diese Daten aus dem Modell ausschließen. Wenden Sie sich an Ihr Adobe Account Team, um die Daten auszuschließen.
+++

+++ Kann ich einen Bericht für eine bestimmte Metrik der Kontoeigenschaft erstellen, z. B. [!UICONTROL Device] oder [!UICONTROL Objective Name]?
Bei Kampagnenentitätsberichten ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] und [!UICONTROL Product Group Report]) werden die Metrikdaten dynamisch durch die Eigenschaftsspalten aggregiert, die Sie in den Bericht aufnehmen. Optional können Sie die Schlüsselspalte für den Bericht entfernen und nur die Eigenschaftenspalten einschließen, für die Sie Daten aggregieren möchten.

Wenn Sie beispielsweise eine &quot;[!UICONTROL Keyword Report]&quot;-Variable generieren, die die Spalten [!UICONTROL Ad Group] und  Gerät enthält, aggregiert der Bericht standardmäßig die Metriken für jeden Suchbegriff nach Anzeigengruppe und Gerätetyp. Wenn Sie jedoch die Spalte [!UICONTROL Keyword] entfernen, bevor Sie den Bericht generieren, generiert der Bericht dynamisch Metriken für die angegebenen Anzeigengruppen nach Gerätetyp.

>[!NOTE]
>
>Sie können diese Funktion nicht verwenden, um Daten nach Beschriftungsklassifizierungen zu aggregieren. Alle Titel-Classification-Spalten im Bericht werden weggelassen. Verwenden Sie stattdessen den [Beschriftungsklassifizierungsbericht](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Allgemeine Datenfragen

+++Berichte, die mit verschiedenen Attributionsregeln erstellt wurden, zeigen unterschiedliche Summen an.
Wenn Sie einen Bericht mehrmals mit denselben Berichtsparametern, jedoch mit unterschiedlichen Attributionsregeln generieren, können die Daten aus einem der folgenden Gründe unterschiedlich sein:

* Klickdatumsbasierte Daten können außerhalb des angegebenen Datumsbereichs liegen.

  Wenn Sie den Berichtsparameter &quot;[!UICONTROL Conversions based on click date]&quot;verwenden, gilt der angegebene Datumsbereich für das Klickdatum anstelle des Transaktionsdatums. Wenn der Bericht auch die Attributionsregel &quot;Erstes Ereignis&quot;oder &quot;Letztes Ereignis&quot;verwendet, kann das erste oder letzte Ereignis, das zur Konversion geführt hat, außerhalb des angegebenen Datumsbereichs liegen. Angenommen, ein Benutzer hat am 30. April auf Keyword_1 geklickt, am 20. Mai auf Keyword_2 geklickt und am 21. Mai konvertiert. Wenn der Bericht die &quot;[!UICONTROL First Event]&quot;-Attributionsregel und einen Datumsbereich vom 1. bis 21. Mai verwendet, ist das erste Ereignis (ein Klick auf Keyword_1 am 30. April) nicht im Bericht enthalten. Wenn Sie den Bericht mit demselben Datumsbereich ausführen, aber die &quot;[!UICONTROL Last Event]&quot;-Attributionsregel verwenden, wird die Konversion in den Bericht aufgenommen, da der letzte Klick innerhalb des angegebenen Datumsbereichs erfolgte.

* Bei der Auswahl des Portfoliofilters werden einige der Ereignisse ausgeschlossen, die zur Konversion führten.

  Wenn Sie einen Bericht zu einer Untergruppe von Portfolios erstellen, schließen Sie möglicherweise nicht die Kampagnen ein, die das Ereignis enthielten, dem die Konversion unter einer der Attributionsregeln zugeordnet wurde. Angenommen, ein Benutzer klickt von Portfolio_1 auf Keyword_1, klickt auf Keyword_2 von Portfolio_2 und konvertiert dann. Wenn der Bericht die &quot;[!UICONTROL First Event]&quot;-Attributionsregel verwendet, muss Portfolio_1 enthalten sein, damit die Konversion in den Bericht aufgenommen werden kann. Wenn der Bericht jedoch die Attributionsregel &quot;Letztes Ereignis&quot;verwendet, muss Portfolio_2 einbezogen werden.

>[!TIP]
>
>Wenn Sie Konversionssummen unter verschiedenen Attributionsregeln vergleichen möchten, führen Sie Berichte mit dem Berichtsparameter &quot;[!UICONTROL Conversions based on transaction date]&quot;aus und wählen Sie alle Anzeigennetzwerke oder alle Portfolios aus. Wenn Sie keine anderen Filter festlegen, sollten die Konvertierungssummen übereinstimmen.

+++

Die Felder +++Individuelle Daten sind falsch, obwohl die Summen korrekt sind.
Diese Situation kann auftreten, wenn die Metrikformate Ganzzahlen verwenden:

* Wenn Sie eine [benutzerspezifische Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) mit dem Format *Zahl ohne Dezimalstellen* erstellen (das Daten als Ganzzahlen anzeigt) und sie in eine Ansicht oder einen Bericht einschließen, der eine gewichtete Konversionsattributionsregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] oder [!UICONTROL Even Distribution]) verwendet, wird die Ausgabe in Ganzzahlen und nicht in Dezimalzahlen angezeigt. In diesem Fall sind die einzelnen Datenfelder möglicherweise falsch, obwohl die Summen korrekt sind. Wenn eine Bestellung beispielsweise gleichmäßig zwischen drei Ereignissen aufgeteilt ist, wird jedem der drei Ereignisse eine Bestellung (statt einer Reihenfolge von 0,33) zugeordnet. Um das Problem zu beheben, ändern [das Metrikformat](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) in *Zahl auf 2 Dezimalstellen*.

* Wenn Sie eine Umsatzmetrik haben, die als Ganzzahl gesendet wird, tritt dasselbe Problem auf. (Das Umsatzformat wird durch das Konversions-Tag gesteuert, das die Daten sendet.) Um das Problem zu beheben, erstellen Sie [eine benutzerdefinierte Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md), die ausschließlich aus der Umsatzmetrik und mit dem Format *Zahl bis 2 Dezimalstellen* besteht, und fügen Sie sie in Ansichten und Berichten anstelle der ursprünglichen Metrik ein.
+++

+++ Wenn Klick- oder Umsatzdaten fehlen, wie kann ich verhindern, dass sich dies auf zukünftige Angebote auswirkt?
Klickdatenprobleme treten auf, wenn Search, Social und Commerce nicht mit dem Anzeigennetzwerk synchronisiert sind. Wenden Sie sich an Ihr Adobe Account-Team, um das Konto manuell zu synchronisieren. Wenn Klickdaten für einen ganzen Tag fehlen, bitten Sie Ihr Adobe Account-Team, diesen Tag von den Kostenmodellen auszuschließen.

Umsatzdatenprobleme können aufgrund eines Tracking- oder Feed-Dateiproblems auftreten. Wenden Sie sich an Ihr Adobe Account Team, um das Problem zu untersuchen. Wenn Umsatzdaten für einen ganzen Tag fehlen, bitten Sie Ihr Adobe Account-Team, diesen Tag aus den Umsatzmodellen auszuschließen.
+++

+++Währungsdaten werden im falschen Format angezeigt.
Standardmäßig werden alle monetären Daten in Berichten im Format für US-Dollar angezeigt (z. B. 1.000,00). Um den Wert im richtigen Währungsformat anzuzeigen (jedoch ohne Währungssymbole im CSV- und TSV-Format), fügen Sie die Spalte &quot;[!UICONTROL Currency]&quot; zum Bericht hinzu. Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, sind beliebige &quot;[!UICONTROL Total]&quot;-Geldwerte einfach die Summe aller Zahlen in der Spalte, unabhängig von der Währung.
+++

+++ Warum sehe ich Dezimalwerte für eine Konversionsmetrik, die eine natürliche Zahl sein sollte (1, 2 usw.)?
In den folgenden Fällen können Dezimalwerte angezeigt werden:

* Wenn Sie den Bericht mit einem anderen Konversionsattributionsparameter als [!UICONTROL Last Event] oder [!UICONTROL First Event] ausgeführt haben, kann der Umsatz auf mehrere Ereignisse im Konversionspfad aufgeteilt werden.

* Wenn im [!UICONTROL Transaction Report] mehrere [Angebotseinheiten](/help/search-social-commerce/glossary.md#a-b) mit unterschiedlichen Übereinstimmungstypen dieselbe Transaktions-ID aufweisen, wird der Umsatz für die Tracking-ID nach der Anzahl der Klicks am angegebenen Klickdatum aufgeteilt.
+++

## Standardleistungsmetriken

+++Klick-Daten fehlen in Berichten.
Im Folgenden finden Sie häufige Gründe für das Fehlen von Klickdaten.

| Ursache | Erkennung/Analyse | Auflösung |
|---|---|---|
| Der Prozess, der Klickdaten aus dem Anzeigenkonto abruft, ist fehlgeschlagen. | Es gibt keine systematische Möglichkeit, dieses Problem zu erkennen. Sie können jedoch feststellen, dass eine Kampagne keine Kosten- oder Klickinformationen anzeigt, auch wenn das Anzeigenkonto Geld ausgegeben hat. | Wenden Sie sich an Ihr Adobe-Account-Team.<br><br>Wenn die Daten länger als 24 Stunden fehlen, schließen Sie diese Daten aus den Kostenvorausschätzungen aus, bis die Daten abgerufen werden. Ihr Adobe-Account-Team kann die Daten ausschließen. |
| Ein Abrechnungsfehler zwischen dem Advertiser und dem Werbenetzwerk verhindert, dass das Werbekonto ausgegeben wird. | Es gibt keine systematische Möglichkeit, dieses Problem zu erkennen. Sie können jedoch feststellen, dass eine Kampagne keine Kosten- oder Klickinformationen anzeigt. | Wenn Sie wissen, dass ein Werbekonto aufgrund eines Abrechnungsproblems nicht ausgegeben werden konnte, schließen Sie diese Daten aus den Kostenprognosen aus. Ihr Adobe-Account-Team kann die Daten ausschließen. |
+++

+++ Leistungsdaten unterscheiden sich von Daten im Werbenetzwerk-Editor.
Wenn das Werbenetzwerk Aktualisierungen an frühere Daten sendet (häufig weil sie Klickbetrug einigen Klicks zugeordnet haben), aktualisiert Search, Social und Commerce die Daten nur, wenn mehr als eine 5-%-Diskrepanz vorliegt und das Adobe Account Team eine Anfrage sendet.

Wenn Sie außerdem Daten von Impressions-Freigaben vergleichen, die über einen Datumsbereich aggregiert wurden, unterscheiden sich die in den Berichten von Search, Social und Commerce enthaltenen Daten möglicherweise von den Daten, die das Anzeigennetzwerk meldet. Dieser Unterschied liegt daran, wie die Daten von der API des Anzeigennetzwerks gemeldet werden, mit der Search, Social und Commerce Daten abrufen. Beispiel für [!DNL Google Ads] -Daten:

* Bei den meisten Impressions-Share-Metriken ist [!DNL Google Ads] entweder auf das untere oder das obere Ende der Werte begrenzt, die für Werte gemeldet werden, die kleiner als 10 % oder größer als 90 % sind. Die Daten werden als 0,0999 für &lt;10% und 0,9001 für >90% gemeldet.

* Wenn im Datumsbereich eine Mischung aus gecappten und nicht zugewiesenen Daten vorhanden ist, aggregiert Search, Social und Commerce Impressions-Share-Daten anhand der Werte, die im Istzustand in der API gesendet werden, wobei 0,0999 für Zeilen mit &lt;10 % und 0,9001 für Zeilen mit >90 % verwendet werden. Diese Aggregation kann zu einer Abweichung von den voraggregierten [!DNL Google Ads] -Daten führen, da [!DNL Google Ads] tatsächliche Prozentwerte wie 7 % oder 97 % verwenden kann.
+++

+++ Leistungsdaten in Berichten unterscheiden sich von Daten in [!DNL Google Analytics].
Die beiden Systeme messen unterschiedliche Daten, sodass Sie erwarten sollten, dass andere Daten angezeigt werden. Beispiel:

* Klicks werden in Search, Social und Commerce (und Google Ads) verfolgt, während [!DNL Google Analytics] Besuche pro 30-minütiger Browsersitzung verfolgt. Wenn ein Benutzer beispielsweise einmal auf Ihre Anzeige klickt, dann auf die Schaltfläche &quot;Zurück&quot;und dann erneut auf die Anzeige klickt, zeichnet Search, Social und Commerce zwei Klicks auf, wobei [!DNL Google Analytics] jedoch einen Besuch erfasst.

* [!DNL Google Analytics] zeigt alle Traffic-Daten an, während Search, Social und Commerce (und [!DNL Google Ads]) ungültige Klicks filtern (z. B. übermäßige, wiederholte Klicks).

* [!DNL Google Analytics] enthält Klick- und Umsatzdaten für alle Klicks. In Search, Social und Commerce können Klick- und Umsatzdaten für Anzeigen und Suchbegriffe mit falschen oder fehlenden Tracking-URLs nicht verfolgt werden.
+++

## Konversionsmetriken

+++ Mein Bericht zeigt keine Konversionsdaten an.
Der Bericht enthält möglicherweise keine Konversionsmetriken, für die Konversionen aufgetreten sind.
+++

+++Umsatz fehlt in Berichten.

**Advertiser, die Adobe Advertising-Konversions-Tags verwenden**

*Mögliche Ursachen:*

* Suchbegriffe oder Anzeigen wurden hinzugefügt, ohne den Tracking-Vorlagen oder Ziel-URLs das Klick-Tracking-Präfix &quot;Search&quot;, &quot;Social&quot;und &quot;Commerce&quot;voranzustellen. Andernfalls ist das Tracking-Präfix falsch.

* Das Konversions-Tracking-Tag wurde nicht auf allen entsprechenden Webseiten korrekt implementiert oder bearbeitet.

* Die Konversionsmetriken, die von Search, Social und Commerce verfolgt werden, werden aus Berichten ausgeschlossen und sind daher nicht sichtbar.

* Der Umsatz-Parser für den Client wurde nicht implementiert.

*Mögliche Lösung oder Problemumgehung:*

1. Überprüfen Sie, ob die korrekten Spalten in den Berichten oder Datenansichten enthalten sind. Wenn die richtigen Spalten nicht hinzugefügt werden können, müssen Sie oder Ihr Adobe Account-Team [die Konversionsmetriken für Berichte verfügbar machen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Stellen Sie sicher, dass die richtigen Konversions-Tracking-Tags auf allen entsprechenden Webseiten implementiert sind. Bitten Sie bei Bedarf Ihr Adobe Account-Team, eine Testtransaktion für jedes zutreffende Konversions-Tracking-Tag zu erstellen und die Details der Transaktion zu erfassen, z. B. `transactionid` und Details aus dem Cookie (z. B. `trackingid`, `clickid` usw.).

1. Wenn die Option [!UICONTROL Auto Upload] für die Kampagne deaktiviert ist und Sie Suchbegriffe oder Anzeigen hinzugefügt haben, stellen Sie sicher, dass Sie eine Tracking-Vorlage oder Ziel-URL generiert haben, die das Klick-Umleitungs-Tracking in Search, Social und Commerce enthält. Ihr Adobe Account-Team kann einen internen Bericht ausführen, um zu sehen, ob Klick-Tracking-URLs (Tracking-Vorlagen oder Ziel-URLs) fehlen oder fehlerhaft sind.

   Generieren Sie bei Bedarf ein Tracking, indem Sie eine Bulksheet-Datei mit den richtigen URLs erstellen und die Datei mithilfe der Option **Tracking-URLs generieren** an das entsprechende Konto posten.

   Die Ziel-URL sollte mit &quot;http://pixel.everesttech.net&quot;oder &quot;https://pixel.everesttech.net&quot;beginnen.

1. Wenn keiner dieser Schritte das Problem behebt, kontaktieren Sie [die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Wenn der Client noch nicht gestartet wurde oder neu gestartet wurde, überprüft die Kundenunterstützung, ob ein Revenue Parser eingerichtet wurde. Wenn der Parser eingerichtet ist, überprüfen sie, ob Search, Social und Commerce Pixelkonvertierungen erhalten und beheben das Problem.

**Advertiser, die Konversionsdaten-Feeds senden**

*Mögliche Ursachen:*

* Die Feed-Datei wurde nicht bereitgestellt, sie wurde nicht vollständig analysiert oder der Feed enthielt verwaiste Transaktionen.

* Die relevanten Konversionsmetriken werden aus Berichten ausgeschlossen und sind daher nicht sichtbar.

>[!NOTE]
>
>Daten werden in der Benutzeroberfläche im Allgemeinen erst 2-4 Stunden nach Erhalt des Feeds angezeigt.

*Mögliche Lösung oder Problemumgehung:*

1. Überprüfen Sie, ob die korrekten Spalten in den Berichten oder Datenansichten enthalten sind. Wenn die richtigen Spalten nicht hinzugefügt werden können, müssen Sie oder Ihr Adobe Account-Team [die Konversionsmetriken für Berichte verfügbar machen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Führen Sie die [!UICONTROL Portfolio Report] aus. Wenn es leer ist, führen Sie die Schritte [!UICONTROL Campaign Report] und [!UICONTROL Search Engine Report] aus, um zu sehen, ob der Umsatz in diesen Berichten angezeigt wird. Ist dies der Fall, werden die Kampagnen möglicherweise nicht dem entsprechenden Portfolio zugewiesen.

1. Vergewissern Sie sich, dass die Datei an den Umsatzserver gesendet wurde und dass die Datei dasselbe Format und dieselbe Dateibenennungskonvention wie die vorherigen Dateien verwendet hat.

   Wenn das Format oder die Dateibenennungskonvention geändert wurden, korrigieren Sie die Datei und senden Sie sie erneut.

1. Wenn die Datei gesendet wurde, kontaktieren Sie [die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung prüft, ob die Datei empfangen und analysiert wurde. Wenn die Datei fehlerfrei verarbeitet wurde, wird auf verwaiste Transaktionen überprüft.
+++

+++ Einige erweiterte Berichte enthalten keine Konversionsdaten, die von einem Advertiser-Feed bereitgestellt werden.
Die [!UICONTROL Geo Distribution Report] und [!UICONTROL Domain Referral Report] verwenden Daten, die über den Adobe Advertising-Konversions-Tracking-Dienst erfasst werden und nur für Advertiser mit dem Dienst generiert werden können. Die Berichte enthalten keine Konversionsdaten, die außerhalb des Adobe Advertising-Konversions-Tracking-Systems verfolgt werden.
+++

+++Umsatzdaten unterscheiden sich von den eigenen Umsatzdaten des Advertisers.

**Advertiser, die Adobe Advertising-Konversions-Tags verwenden**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abgelaufen oder gelöscht ist. Der Advertiser kann jedoch davon ausgehen, dass der Umsatz gültig ist.

* Der Traffic zur Seite des Werbetreibenden stammt von einem Lesezeichen oder einer organischen Suche anstelle einer Anzeige.

* Das Konversions-Tracking-Tag wurde nicht auf allen entsprechenden Webseiten korrekt implementiert oder bearbeitet.

*Mögliche Lösung oder Problemumgehung:*

1. Gehen Sie zu **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die von Search, Social und Commerce empfangenen Transaktionen mit den Daten des Advertisers.

1. Wenn einige Transaktionen falsch sind oder fehlen, stellen Sie sicher, dass das entsprechende Konversions-Tracking-Tag auf allen zutreffenden Webseiten implementiert ist und nicht bearbeitet wurde, es sei denn, Ihr Adobe Account-Team hat Sie dazu angewiesen. Wenn die Website kürzlich aktualisiert wurde, fehlt möglicherweise ein -Tag oder ändert es sich.

   Search, Social und Commerce erwarten wohlgeformte URLs (mit Parametern in Name/Wert-Paaren) innerhalb der Variable `ef_transaction_properties` und innerhalb des Elements `src` des Tags `img`.

1. Wenn Sie das Problem nicht ermitteln und beheben können, wenden Sie sich an [die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung versucht, die fehlenden Transaktionen zu identifizieren und dann nach verwaisten Transaktionen und Transaktionen zu suchen, die nicht von einer Anzeige stammen (&quot;nicht korrelierte Konversionen&quot;).

**Advertiser mit Konversionsdaten-Feeds mit `ef_id` Werten**

Siehe mögliche Ursachen und Lösungen für Pixelimplementierungen oben.

**Advertiser mit Konversionsdaten-Feeds, die Transaktions-IDs verwenden**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abläuft oder gelöscht wird. Der Advertiser kann jedoch davon ausgehen, dass der Umsatz gültig ist.

* Der Traffic zur Seite des Werbetreibenden stammt von einem Lesezeichen oder einer organischen Suche anstelle einer Anzeige.

* Eine Offline-Konversion wurde gemeldet, bevor eine Online-Transaktion mit derselben Transaktions-ID erfolgte. Die Online-Transaktion muss zuerst stattfinden.

*Mögliche Lösung oder Problemumgehung:*

1. Gehen Sie zu **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die von Search, Social und Commerce empfangenen Transaktionen mit den Feed-Daten des Advertisers.

1. Wenn eine Transaktion in der Feed-Datei im Bericht fehlt, überprüfen Sie, ob vor der Offline-Konversion eine Online-Transaktion mit derselben Transaktions-ID (verfolgt über das Pixel) aufgetreten ist.

1. Wenn Sie das Problem nicht ermitteln und beheben können, wenden Sie sich an [die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung sucht nach Fehlern beim Analysieren von Daten und [verwaisten Transaktionen](/help/search-social-commerce/glossary.md#o-p).

**Advertiser mit anderen Arten von Konversionsdaten-Feeds**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abgelaufen oder gelöscht ist. Der Advertiser kann jedoch davon ausgehen, dass der Umsatz gültig ist.

* Der Traffic zur Seite des Werbetreibenden stammt von einem Lesezeichen oder einer organischen Suche anstelle einer Anzeige.

* Es gibt [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p), daher zählen Search, Social und Commerce nicht den gesamten Umsatz, den sie erzielen sollten.

* Der Advertiser validierte einen Bericht zu Search, Social und Commerce für einen anderen Datensatz als den im Feed gesendeten.

* Die Transaktions-IDs (`ev_transid` -Werte) wurden nicht gesendet, sind nicht eindeutig oder sind falsch.

* Die Feed-Datei enthält doppelte Tracking-IDs.

* Beim Analysieren der Datei sind Fehler aufgetreten.

* Die Deduplizierungslogik des Advertisers unterscheidet sich von der Logik &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;.

*Mögliche Lösung oder Problemumgehung:*

1. Gehen Sie zu **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die von Search, Social und Commerce empfangenen Transaktionen mit den Daten des Advertisers.

1. Wenn einige Transaktionen falsch sind oder fehlen, stellen Sie sicher, dass a) die Feed-Datei alle erforderlichen Transaktions-IDs und keine doppelten Tracking-IDs enthält und b) die Transaktions-IDs eindeutig und korrekt sind.

1. Wenn Sie das Problem nicht ermitteln und beheben können, wenden Sie sich an [die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung sucht nach Fehlern beim Analysieren von Daten und verwaisten Transaktionen.
+++

+++Umsatzdaten unterscheiden sich von den Daten in Adobe Analytics
Siehe [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Spezifische Berichte

+++ Sollte die [!UICONTROL Portfolio Report]-Ansicht dieselben Zahlen wie die [!UICONTROL Portfolios]-Ansicht aufweisen?
Die Ansicht [!UICONTROL Portfolio Report] und [!UICONTROL Portfolios] zeigen dieselben Daten, wenn alle Filter für die Ansicht, die Berichtsparameter und die Datenspalten für Ansicht und Bericht identisch sind. Wenn die Ansicht &quot;[!UICONTROL Portfolios]&quot;beispielsweise Portfolios mit &quot;[!UICONTROL All but inactive]&quot;für den Datumsbereich &quot;[!UICONTROL Last 7 days]&quot;anzeigt und nur die Standarddatenspalten angezeigt werden, zeigt ein [!UICONTROL Portfolio Report] mit den Standardparametern identische Daten an. Wenn Sie einen der Berichtsparameter ändern oder in der [!UICONTROL Portfolios]-Ansicht andere Filter verwenden, können die Datenwerte unterschiedlich sein.
+++

+++ Die Daten in meinem [!UICONTROL Portfolio Report] stimmen nicht mit den Daten in meinem [!UICONTROL Search Engine Report] oder meinem [!UICONTROL Search Engine Account Report] überein.
Die [!UICONTROL Portfolio Report] zeigt nur Daten für die Kampagnen an, die den angegebenen Portfolios zugewiesen sind, die [!UICONTROL Search Engine Report] und die [!UICONTROL Search Engine Account Report] können jedoch auch Daten für Kampagnen enthalten, die keinem Portfolio zugewiesen sind.
+++

+++Wie unterscheidet sich die [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] von der Portfolioebene [!UICONTROL Model Accuracy Report]?
(Nur Agentur-Kundenbetreuer, Adobe-Kundenbetreuer und Administratorbenutzer) Das unter [!UICONTROL Reports] > [!UICONTROL Model Accuracy] verfügbare [!UICONTROL Forecast Accuracy Report] liefert dieselben Daten wie das Portfolio-Level [!UICONTROL Model Accuracy Report], mit dem Unterschied, dass Sie es über mehrere Portfolios hinweg ausführen können und Sie die Zuordnungsregel ändern können. Sie können den Bericht auch mit benutzerdefinierten Parametern ausführen und planen und ihn zur Erstellung von Tabellenfeeds verwenden. Darüber hinaus ist der [!UICONTROL Forecast Accuracy Report] genauer als der alte Bericht auf Portfolioebene, da er die Umsatzgenauigkeit anhand der historischen Ziele für das Portfolio und nicht des aktuellen Ziels bewertet und Daten für die anwendbare Zeitzone genauer darstellt.
+++

Daten der Stufe ++ + Anzeige sind nicht für [!DNL Google Ads] dynamische Suchanzeige (DSA), Performance-Max, Smart-Shopping und [!DNL YouTube]-Kampagnen verfügbar.
Die Werbenetzwerke stellen nicht die Kennung bereit, die erforderlich ist, um einer einzelnen Anzeige für diese Kampagnen Umsätze zuzuordnen. Folglich sind Leistungsdaten auf Anzeigenebene nicht für diese Kampagnentypen in der Ansicht [!UICONTROL Ads] oder in der Ansicht [!UICONTROL Ad Variation Report] verfügbar. Erwarten Sie Diskrepanzen zwischen den Gesamtdaten der Anzeigenebene für eine Kampagne und den Gesamtdaten für die Kampagne.
+++

+++Wie erkenne ich im [!UICONTROL Transaction Report], welche Konversionsmetrik aus einem Daten-Feed stammt oder vom Adobe Advertising-Tracking-Pixel verfolgt wird?
In einem Transaktionsbericht können Sie feststellen, ob eine enthaltene Konversionsmetrik vom Adobe Advertising-Tracking-Pixel verfolgt wurde, wenn Sie die benutzerdefinierte Spalte &quot;[!UICONTROL Tracking URL]&quot; einschließen. Tracking-URLs mit dem Adobe Advertising-Tracking-Pixel beginnen mit &quot;`http://pixel.everesttech.net`&quot;.
+++

+++ Die Daten in meinem [!UICONTROL Transaction Report] stimmen nicht mit den Daten in meinem [!UICONTROL Keyword Report] überein.
Wenn Sie beide Berichte nach Portfolio generieren, unterscheiden sich die Daten, wenn Sie die [!UICONTROL Keyword Report] mit historischen Daten generieren (d. h. basierend auf der Portfoliokonfiguration während der angegebenen Daten), anstatt Daten für die aktuellen Kampagnen zu verwenden. Wenn Sie den Wert &quot;[!UICONTROL Transaction Report]&quot;nach Portfolio generieren, enthält er Daten für die aktuellen Kampagnen im Portfolio.
+++

## Tabellen-Feeds

Die Ausgabe von +++ Berichten enthält eine Mischung aus Datumsbereichen.
Es können verschiedene Datumsbereiche angezeigt werden, wenn der Feed Daten mit einer anderen Datenaggregationsebene als &quot;[!UICONTROL Daily]&quot;aggregiert.

Um das Problem zu beheben, aktualisieren Sie den Tabellenfeed, um täglich aggregierte Daten einzuschließen. Diese Aufgabe umfasst die Aktualisierung der Berichtsvorlage, die Erstellung eines Berichts mithilfe der Vorlage, die Erstellung einer benutzerdefinierten [!DNL Microsoft Excel] Vorlage mithilfe des Berichts und die Aktualisierung der Feed-Einstellungen, um die neue Excel-Vorlage einzuschließen. Weitere Informationen finden Sie unter &quot;[Bearbeiten der Feed-Einstellungen für Tabellenberichte](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++

++ + Ein Tabellenfeed führt zu einem internen Fehler.
Dieser Fehler kann auftreten, wenn Sie die Spalten in der Berichtsvorlage ändern, aber die Vorlage [!DNL Microsoft Excel] nicht entsprechend aktualisieren.

Um das Problem zu beheben, aktualisieren Sie den Tabellenfeed, um die neuen Spalten einzuschließen. Diese Aufgabe umfasst die Aktualisierung der Berichtsvorlage, die Erstellung eines Berichts mithilfe der Vorlage, die Erstellung einer benutzerdefinierten [!DNL Excel] Vorlage mithilfe des Berichts und die Aktualisierung der Feed-Einstellungen, um die neue Excel-Vorlage einzuschließen. Weitere Informationen finden Sie unter &quot;[Bearbeiten der Feed-Einstellungen für Tabellenberichte](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++

+++ Wenn ich versuche, einen Tabellenfeed in [!DNL Excel] zu öffnen, meldet [!DNL Excel] den Fehler &quot;Unlesbarer Inhalt&quot;und Daten werden aus dem wiederhergestellten Inhalt entfernt.
Wenn die Vorlage [!DNL Microsoft Excel] die Daten nicht nach Startdatum in aufsteigender Reihenfolge sortiert, kann der Tabellenfeed leere Zeilen enthalten. Insbesondere zeigt [!DNL Excel] den Fehler &quot;Excel hat unlesbaren Inhalt in &#39;&lt;*Berichtsname*>.xlsx gefunden&quot;. Möchten Sie den Inhalt der Arbeitsmappe wiederherstellen? Wenn Sie der Quelle dieser Arbeitsmappe vertrauen, klicken Sie auf &quot;Ja&quot;. Wenn Sie auf &quot;Ja&quot;klicken, erhalten Sie die folgende Meldung: &quot;Entfernte Datensätze: Zellinformationen aus /xl/worksheets/sheet1.xml Teil&quot;, und der Tabellenfeed enthält leere Zeilen.

Um das Problem zu beheben, bearbeiten Sie die mit dem Feed verknüpfte Vorlage [!DNL Excel] , um die Daten nach [!DNL Start date in Ascending (Oldest to Newest) order] zu sortieren, und laden Sie dann die aktualisierte Vorlage über die Einstellungen des Tabellenfeeds hoch. Weitere Informationen finden Sie unter &quot;[Bearbeiten von Tabellenbericht-Feeds](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++
