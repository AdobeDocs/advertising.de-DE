---
title: Häufig gestellte Fragen zu benutzerdefinierten Berichten
description: Erfahren Sie Antworten auf häufig gestellte Fragen zu Leistungsberichten, einschließlich der Fehlerbehebung bei Datenproblemen.
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: 01fe9264fee43ed29f6cee022dadeb29fbd26f45
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# Häufig gestellte Fragen zu benutzerdefinierten Berichten

## Allgemeine Fragen

+++Was passiert, wenn der Datumsbereich für den Bericht beginnt, bevor Berichtsdaten verfügbar sind?
Der Bericht wird zwar erstellt, enthält jedoch nur Daten zu den Daten, für die Daten verfügbar sind. Weitere Informationen dazu, wann Daten für jeden Berichtstyp verfügbar sind, finden Sie unter &quot;[Die für Berichte verwendeten Daten](data-used-for-reports.md).
+++

+++Was ist der Unterschied zwischen auf dem Klick- und dem Transaktionsdatum basierenden Berichten?
Wenn Sie Konversionen nach Transaktionsdatum melden, umfassen die Daten Transaktionen, deren Transaktionsdatum im angegebenen Zeitraum aufgetreten ist. Diese Option ist die Standardeinstellung in Basisberichten und erweiterten Berichten und zeigt an, wie viel Umsatz innerhalb des angegebenen Zeitraums erzielt wurde.

Wenn Sie Konversionen nach Klickdatum melden, umfassen die Daten Transaktionen, die aus einem Klick resultierten, der während des angegebenen Zeitraums aufgetreten ist. Wenn es bei einem Portfolio zu erheblichen Verzögerungen zwischen Klicks und Transaktionen kommt, zeigt diese Art von Reporting den historischen Umsatz pro Klick für das Portfolio an, was Ihnen eine Vorstellung davon gibt, welche Umsatzverhaltensweisen im Laufe der Zeit zu erwarten sind.

![Bericht nach Klickdatum versus Bericht nach Transaktionsdatum](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Bericht nach Klickdatum versus Bericht nach Transaktionsdatum")
+++

+++Was passiert, wenn ich das Click-Lookback-Fenster oder das Impression-Lookback-Fenster ändere?
(Nur Werbetreibende mit Advertising Pixel-basiertem Konversionsverfolgungs-Service) Daten zu Ereignissen, die aus dem ersten Klick resultieren, werden über einen längeren oder kürzeren Zeitraum erfasst.

Das [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster eines Advertisers ](/help/search-social-commerce/glossary.md#i-j) die Anzahl der Tage nach dem Auftreten eines Paid-Click oder einer Display-Impression (bzw. einer Display-Impression), in denen das Ereignis einer Konversion zugeordnet werden kann. Das Ändern eines Werts in einen längeren oder kürzeren Zeitraum kann für Werbetreibende mit besonders kurzen oder langen Umsatzklicks oder zur Anzeige von Impression-zu-Umsatz-Zeiträumen wichtig sein.

**Best Practice:** Stellen Sie sicher, dass die Lookback-Fenster länger sind als die Umsätze per Klick und die Impressions-zu-Umsätzen-Zeiten für die meisten Ihrer Keywords oder Anzeigen angezeigt werden. Wenn sie kürzer sind, sind einige Konversionen nicht mit dem ersten Klick oder der ersten Impression verbunden.
+++

+++Wie weiß ich, welche Konversionen aus einer [!DNL Google Ads] Anzeigenerweiterung oder einem Produkteintrag resultierten?
Sie können sehen, welche Konversionen durch einen Klick auf eine [!DNL Google Ads] Anzeigenerweiterung (anstatt auf die Anzeige selbst) oder auf eine Produktliste entstanden sind, indem Sie eine [!UICONTROL Transaction Report] generieren. Der Wert der Spalte [!UICONTROL Link Type] zeigt den Typ und Titel eines Links an, auf den geklickt wurde:

* Produktlisten werden als `pla:<product ID>` aufgeführt, z. B. `pla:8525822`.

* Sitelinks werden als `sl:<Sitelink text>` aufgelistet, z. B. `sl:See Current Offers`.

  Sie können einen Sitelink auch identifizieren, wenn Sie die Spalte [!UICONTROL Tracking URL] in den Bericht einbeziehen. Die [!UICONTROL Tracking URL] für einen Sitelink enthält das Attribut `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Konversionen von [!DNL Google Ads] Standorten und Telefonerweiterungen sind in den Daten für die zugehörigen Anzeigen enthalten. Sie werden nicht separat gemeldet.

+++

+++Die Spalte &quot;[!UICONTROL Keyword]&quot; in meinem Bericht enthält den Wert „(Anzeigengruppeninhalt) &lt;*Anzeigengruppenname*>.“
Wenn die Zeile Daten für inhaltsaktivierte Suchkampagnen, Anzeigekampagnen oder Social-Media-Kampagnen enthält - die keine Keywords enthalten -, zeigt die Spalte [!UICONTROL Keyword] stattdessen den entsprechenden Anzeigengruppennamen an.
+++

+++Aufgrund von saisonalen oder Marktveränderungen zeigen meine Berichte atypische Daten. Wirkt sich dies auf Angebote aus, sobald sich die Bedingungen ändern?
Die Optimierungsfunktion erstellt täglich ihre Umsatzmodelle für jede Gebotseinheit, um sicherzustellen, dass sie Trends erkennt und sofort darauf reagiert. Die Modelle beinhalten langfristige historische Daten, um die Vorhersage der saisonalen Leistung zu erleichtern. Die Einstellung der Halbwertszeit des Umsatzmodells des Portfolios bestimmt <!-- add link to glossary? -->, wie stark aktuelle Umsatzdaten gewichtet werden. Best Practice ist es, die Halbwertszeit während eines Zeitraums mit atypischer Leistung zu reduzieren, sie jedoch nach der Anpassung des Umsatzmodells zu erhöhen. Wenden Sie sich an Ihr Adobe-Account-Team, wenn Sie Fragen haben, ob eine Anpassung der Halbwertszeit erforderlich ist.

Wenn Sie nicht möchten, dass sich die Daten für den Zeitraum auf zukünftige Gebote auswirken, können Sie diese Datumsangaben aus dem Modell ausschließen. Wenden Sie sich an Ihr Adobe-Accountteam, um die Daten auszuschließen.
+++

+++Kann ich einen Bericht zu einer bestimmten Kontoeigenschaftsmetrik erstellen, z. B. [!UICONTROL Device] oder [!UICONTROL Objective Name]?
Bei Kampagnenentitätsberichten ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] und [!UICONTROL Product Group Report]) werden die Metrikdaten dynamisch anhand der Eigenschaftsspalten aggregiert, die Sie in den Bericht aufnehmen. Sie können optional die Schlüsselspalte für den Bericht entfernen und nur die Eigenschaftsspalten einbeziehen, für die Sie Daten aggregieren möchten.

Wenn Sie beispielsweise ein [!UICONTROL Keyword Report] generieren, das die Spalten [!UICONTROL Ad Group] und  Gerät enthält, aggregiert der Bericht standardmäßig die Metriken für jedes Keyword nach Anzeigengruppe und Gerätetyp. Wenn Sie die Spalte [!UICONTROL Keyword] jedoch entfernen, bevor Sie den Bericht generieren, generiert der Bericht dynamisch Metriken für die angegebenen Anzeigengruppen nach Gerätetyp.

>[!NOTE]
>
>Sie können diese Funktion nicht verwenden, um Daten nach Kennzeichnungsklassifizierungen zu aggregieren. Alle Kennzeichnungsklassifizierungsspalten im Bericht werden weggelassen. Verwenden Sie stattdessen den [Klassifizierungsbericht für Kennzeichnungen](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Allgemeine Datenprobleme

+++Berichte, die anhand verschiedener Attributionsregeln erstellt wurden, weisen unterschiedliche Summen auf.
Wenn Sie einen Bericht mehrmals mit denselben Berichtsparametern, aber mit unterschiedlichen Attributionsregeln generieren, können die Daten aus einem der folgenden Gründe unterschiedlich sein:

* Klicken Sie auf Datumsbasierte Daten, die außerhalb des angegebenen Datumsbereichs liegen können.

  Wenn Sie den Berichtsparameter &quot;[!UICONTROL Conversions based on click date]&quot; verwenden, gilt der angegebene Datumsbereich für das Datum des Klicks anstelle des Transaktionsdatums. Wenn der Bericht auch die Attributionsregel „Erstes Ereignis“ oder „Letztes Ereignis“ verwendet, dann kann das erste oder letzte Ereignis, das zur Konversion geführt hat, außerhalb des angegebenen Datumsbereichs liegen. Angenommen, ein Benutzer hat am 30. April auf Keyword_1 geklickt, am 20. Mai auf Keyword_2 geklickt und am 21. Mai konvertiert. Wenn der Bericht die Attributionsregel &quot;[!UICONTROL First Event]&quot; und einen Datumsbereich vom 1. bis 21. Mai verwendet, wird das erste Ereignis (ein Klick auf Keyword_1 am 30. April) nicht in den Bericht aufgenommen. Wenn Sie den Bericht mit demselben Datumsbereich, aber unter Verwendung der Attributionsregel &quot;[!UICONTROL Last Event]&quot; ausführen, wird die Konversion in den Bericht aufgenommen, da der letzte Klick innerhalb des angegebenen Datumsbereichs stattgefunden hat.

* Die Portfoliofilterauswahl schließt einige der Ereignisse aus, die zur Konversion führen.

  Wenn Sie Berichte zu einer Untergruppe von Portfolios erstellen, beziehen Sie möglicherweise nicht die Kampagnen ein, die das Ereignis enthalten haben, dem die Konversion gemäß einer der Attributionsregeln zugeordnet wurde. Angenommen, ein Benutzer klickt auf Keyword_1 in Portfolio_1, klickt auf Keyword_2 in Portfolio_2 und konvertiert dann. Wenn der Bericht die Attributionsregel &quot;[!UICONTROL First Event]&quot; verwendet, muss Portfolio_1 einbezogen werden, damit die Konversion in den Bericht aufgenommen wird. Wenn der Bericht jedoch die Attributionsregel „Letztes Ereignis“ verwendet, muss Portfolio_2 einbezogen werden.

>[!TIP]
>
>Wenn Sie Konversionssummen unter verschiedenen Attributionsregeln vergleichen möchten, führen Sie Berichte mit dem Berichtsparameter &quot;[!UICONTROL Conversions based on transaction date]&quot; aus und wählen Sie alle Anzeigennetzwerke oder alle Portfolios aus. Wenn Sie keine anderen Filter festlegen, sollten die Konversionssummen übereinstimmen.

+++

+++Einzelne Datenfelder sind falsch, die Summen jedoch korrekt.
Diese Situation kann auftreten, wenn die Metrikformate Ganzzahlen verwenden:

* Wenn Sie eine [benutzerdefinierte Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) mit dem Format *Zahl ohne Dezimalpunkte* (die Daten als Ganzzahlen anzeigt) erstellen und sie in eine Ansicht oder einen Bericht aufnehmen, die bzw. der eine Attributionsregel für die gewichtete Konversion verwendet ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] oder [!UICONTROL Even Distribution]), wird die Ausgabe in Ganzzahlen angezeigt, nicht in Dezimalzahlen. In diesem Fall können einzelne Datenfelder falsch sein, obwohl die Summen korrekt sind. Wenn beispielsweise eine Reihenfolge gleichmäßig auf drei Ereignisse aufgeteilt wird, wird jedem der drei Ereignisse eine Reihenfolge (statt 0,33 Reihenfolge) zugeordnet. Um das Problem zu beheben, [ändern Sie das Metrikformat](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) in *Zahl zu 2 Dezimalpunkten*.

* Wenn Sie eine Umsatzmetrik haben, die als Ganzzahl gesendet wird, tritt dasselbe Problem auf. (Das Umsatzformat wird durch das Konversions-Tag gesteuert, das die Daten übermittelt.) Um das Problem zu beheben[ erstellen Sie eine benutzerdefinierte Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) die ausschließlich aus der Umsatzmetrik und mit dem Format *Zahl bis 2 Dezimalpunkte* besteht und nehmen Sie sie in Ansichten und Berichte und nicht in die ursprüngliche Metrik auf.
+++

+++Wenn Klick- oder Umsatzdaten fehlen, wie kann ich verhindern, dass sich dies auf zukünftige Angebote auswirkt?
Klickdatenprobleme treten auf, wenn Search, Social und Commerce nicht mehr mit dem Anzeigennetzwerk synchron sind. Wenden Sie sich an Ihr Adobe-Konto-Team, um das Konto manuell zu synchronisieren. Wenn Klickdaten für einen ganzen Tag fehlen, bitten Sie Ihr Adobe-Account-Team, diesen Tag aus den Kostenmodellen auszuschließen.

Probleme mit Umsatzdaten können aufgrund eines Tracking- oder Feed-Datei-Problems auftreten. Wenden Sie sich an Ihr Adobe-Konto-Team, um das Problem zu untersuchen. Wenn für einen ganzen Tag Umsatzdaten fehlen, bitten Sie Ihr Adobe-Accountteam, diesen Tag aus den Umsatzmodellen auszuschließen.
+++

+++Monetäre Daten werden im falschen Format angezeigt.
Standardmäßig werden alle monetären Daten in Berichten im Format für US-Dollar angezeigt (z. B. 1.000,00). Um den Wert im richtigen Währungsformat (aber ohne Währungssymbole im CSV- und TSV-Format) anzuzeigen, fügen Sie dem Bericht die Spalte &quot;[!UICONTROL Currency]&quot; hinzu. Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, sind alle &quot;[!UICONTROL Total]&quot; monetären Werte einfach die Summe aller Zahlen in der Spalte, unabhängig von der Währung.
+++

+++Warum sehe ich Dezimalwerte für eine Konversionsmetrik, die eine natürliche Zahl sein sollte (1, 2 usw.)?
In den folgenden Fällen werden möglicherweise Dezimalwerte angezeigt:

* Wenn Sie den Bericht mit einem anderen Konversionszuordnungsregelparameter als [!UICONTROL Last Event] oder [!UICONTROL First Event] ausgeführt haben, kann der Umsatz auf mehrere Ereignisse im Konversionspfad aufgeteilt werden.

* Wenn [!UICONTROL Transaction Report] mehrere [Gebotseinheiten](/help/search-social-commerce/glossary.md#a-b) mit unterschiedlichen Übereinstimmungstypen dieselbe Transaktions-ID haben, wird der Umsatz für die Tracking-ID gemäß der Anzahl der Klicks am angegebenen Klickdatum aufgeteilt.
+++

## Standardleistungsmetriken

+++Klickdaten fehlen in Berichten.
Im Folgenden finden Sie häufige Gründe für einen Mangel an Klickdaten.

| Ursache | Erkennung/Analyse | Auflösung |
|---|---|---|
| Fehler beim Abrufen der Klickdaten aus dem Werbekonto. | Es gibt keine systematische Möglichkeit, dieses Problem zu erkennen, aber Sie werden möglicherweise feststellen, dass eine Kampagne keine Kosten- oder Klickinformationen anzeigt, obwohl das Werbekonto Geld ausgegeben hat. | Wenden Sie sich an Ihr Adobe-Accountteam.<br><br>Wenn die Daten für mehr als 24 Stunden fehlen, schließen Sie diese Daten aus den Kostenprognosen aus, bis die Daten abgerufen werden. Ihr Adobe Account Team kann die Daten ausschließen. |
| Ein Problem mit der Rechnungsstellung zwischen dem Werbetreibenden und dem Werbenetzwerk verhindert, dass das Werbekonto Ausgaben tätigt. | Es gibt keine systematische Möglichkeit, dieses Problem zu erkennen, aber Sie werden möglicherweise feststellen, dass eine Kampagne keine Kosten- oder Klickinformationen anzeigt. | Wenn Sie wissen, dass ein Werbekonto aufgrund eines Abrechnungsproblems nicht in der Lage war, Ausgaben zu tätigen, schließen Sie diese Daten aus den Kostenprognosen aus. Ihr Adobe Account Team kann die Daten ausschließen. |

+++

+++Leistungsdaten unterscheiden sich von den Daten im Anzeigennetzwerk-Editor.
Wenn das Werbenetzwerk Aktualisierungen an vorherigen Daten sendet (häufig, weil Klickbetrug einigen Klicks zugeordnet wurde), aktualisiert Search, Social und Commerce die Daten nur, wenn eine Diskrepanz von mehr als 5 % besteht und das Adobe-Konto-Team eine Anfrage sendet.

Wenn Sie Impression Share-Daten vergleichen, die über einen Datumsbereich aggregiert sind, können die Daten, die in Such-, Social- und Commerce-Berichten enthalten sind, von den Daten abweichen, die das Werbenetzwerk meldet. Dieser Unterschied beruht darauf, wie die Daten von der API des Anzeigennetzwerks gemeldet werden, die Search, Social und Commerce verwenden, um Daten abzurufen. Zum Beispiel für [!DNL Google Ads]:

* Bei den meisten Impression Share-Metriken begrenzt [!DNL Google Ads] entweder das untere oder das obere Ende der Werte, die für Werte von unter 10 % oder über 90 % gemeldet werden. Daten werden als 0,0999 für &lt;10 % und 0,9001 für >90 % gemeldet

* Wenn innerhalb des Datumsbereichs eine Mischung aus begrenzten und nicht begrenzten Daten vorliegt, aggregieren Search, Social und Commerce die Impressionsdaten unter Verwendung der Werte, die in der vorliegenden API gesendet werden, und verwenden 0,0999 für Zeilen mit &lt;10 % und 0,9001 für Zeilen mit >90 %. Diese Aggregation könnte zu einer Abweichung von den [!DNL Google Ads] voraggregierten Daten führen, da [!DNL Google Ads] tatsächliche Prozentwerte wie 7 % oder 97 % verwenden können.
+++

+++Leistungsdaten in Berichten unterscheiden sich von Daten in [!DNL Google Analytics].
Die beiden Systeme messen unterschiedliche Daten, sodass unterschiedliche Daten zu erwarten sind. Beispiel:

* Search, Social und Commerce (und Google Ads) verfolgen Klicks, während [!DNL Google Analytics] Besuche pro 30-minütiger Browser-Sitzung verfolgt. Wenn ein(e) Benutzende(r) beispielsweise einmal auf Ihre Anzeige klickt, erneut auf die Schaltfläche „Zurück“ klickt und dann erneut auf die Anzeige klickt, zeichnen Search, Social und Commerce zwei Klicks auf, aber [!DNL Google Analytics] einen Besuch.

* [!DNL Google Analytics] zeigt alle Traffic-Daten an, während Search, Social und Commerce (und [!DNL Google Ads]) ungültige Klicks filtern (z. B. übermäßige, wiederholte Klicks).

* [!DNL Google Analytics] enthält Klick- und Umsatzdaten für alle Klicks. Search, Social und Commerce können keine Klick- und Umsatzdaten für Anzeigen und Keywords mit falschen oder fehlenden Tracking-URLs verfolgen.
+++

## Konversionsmetriken

+++Mein Bericht zeigt keine Konversionsdaten an.
Der Bericht enthält möglicherweise keine Konversionsmetriken, für die Konversionen aufgetreten sind.
+++

+++Einnahmen fehlen in Berichten.

**Werbetreibende, die Konversions-Tags für Adobe Advertising verwenden**

*Mögliche Ursachen:*

* Keywords oder Anzeigen wurden ohne Präfix des Klick-Tracking-Präfixes für Search, Social und Commerce zu den Tracking-Vorlagen oder Ziel-URLs hinzugefügt oder das Tracking-Präfix ist falsch.

* Das Konversionsverfolgungs-Tag ist nicht auf allen entsprechenden Web-Seiten korrekt implementiert oder wurde bearbeitet.

* Die Konversionsmetriken, die Search, Social und Commerce verfolgen, sind aus Berichten ausgeschlossen und daher nicht sichtbar.

* Der Umsatz-Parser für den Client wurde nicht implementiert.

*Mögliche Lösung oder Problemumgehung:*

1. Überprüfen Sie, ob die richtigen Spalten in den Berichten oder Datenansichten enthalten sind. Wenn die richtigen Spalten nicht zum Hinzufügen verfügbar sind, müssen Sie oder Ihr Adobe-Konto-Team [die Konversionsmetriken für Berichte verfügbar machen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Überprüfen Sie, ob die richtigen Konversionsverfolgungstags auf allen entsprechenden Web-Seiten implementiert sind. Bitten Sie bei Bedarf Ihr Adobe-Account-Team, eine Testtransaktion für jedes anwendbare Konversionsverfolgungs-Tag zu erstellen und die Details der Transaktion zu erfassen, wie z. B. die `transactionid` und Details aus dem Cookie (wie `trackingid`, `clickid` usw.).

1. Wenn die Option [!UICONTROL Auto Upload] für die Kampagne deaktiviert ist und Sie Keywords oder Anzeigen hinzugefügt haben, stellen Sie sicher, dass Sie eine Tracking-Vorlage oder Ziel-URL generiert haben, die das Weiterleitungs-Tracking für Search, Social und Commerce enthält. Ihr Adobe-Konto-Team kann einen internen Bericht ausführen, um festzustellen, ob Klick-Tracking-URLs (Tracking-Vorlagen oder Ziel-URLs) fehlen oder fehlerhaft sind.

   Generieren Sie bei Bedarf ein Tracking, indem Sie eine Bulksheet-Datei mit den richtigen URLs erstellen und die Datei über die Option **Tracking-URLs generieren** an das entsprechende Konto senden.

   Die Ziel-URL sollte mit &quot;http://pixel.everesttech.net&quot; oder &quot;https://pixel.everesttech.net&quot; beginnen.

1. Wenn keiner dieser Schritte das Problem behebt, wenden Sie [an die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Wenn der Client nicht gestartet wurde oder neu gestartet wurde, überprüft die Kundenunterstützung, ob ein Umsatz-Parser eingerichtet wurde. Wenn der Parser eingerichtet ist, überprüft er, ob Search, Social und Commerce Pixelkonvertierungen erhalten, und behebt das Problem.

**Werbetreibende, die Konversionsdaten-Feeds senden**

*Mögliche Ursachen:*

* Die Feed-Datei wurde nicht zugestellt, sie wurde nicht vollständig geparst, oder der Feed enthielt verwaiste Transaktionen.

* Die entsprechenden Konversionsmetriken sind aus Berichten ausgeschlossen und daher nicht sichtbar.

>[!NOTE]
>
>Daten werden in der Regel erst 2-4 Stunden nach Eingang des Feeds in der Benutzeroberfläche angezeigt.

*Mögliche Lösung oder Problemumgehung:*

1. Überprüfen Sie, ob die richtigen Spalten in den Berichten oder Datenansichten enthalten sind. Wenn die richtigen Spalten nicht zum Hinzufügen verfügbar sind, müssen Sie oder Ihr Adobe-Konto-Team [die Konversionsmetriken für Berichte verfügbar machen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Führen Sie die [!UICONTROL Portfolio Report] aus. Wenn es leer ist, führen Sie den [!UICONTROL Campaign Report] und die [!UICONTROL Search Engine Report] aus, um zu sehen, ob der Umsatz in diesen Berichten angezeigt wird. Ist dies der Fall, werden die Kampagnen möglicherweise nicht dem entsprechenden Portfolio zugewiesen.

1. Stellen Sie sicher, dass die Datei an den Umsatzserver gesendet wurde und dass das Format und die Dateibenennungskonvention der vorherigen Dateien entsprechen.

   Wenn sich das Format oder die Dateibenennungskonvention geändert hat, korrigieren Sie die Datei und senden Sie sie erneut.

1. Wenn die Datei gesendet wurde, wenden Sie [an die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung prüft, ob die Datei empfangen und geparst wurde. Wenn die Datei fehlerfrei verarbeitet wurde, überprüfen sie, ob verwaiste Transaktionen vorliegen.
+++

+++Einige erweiterte Berichte enthalten keine Konversionsdaten, die von einem Advertiser-Feed bereitgestellt werden.
Die [!UICONTROL Geo Distribution Report] und [!UICONTROL Domain Referral Report] verwenden Daten, die über den Konversionsverfolgungs-Service von Adobe Advertising erfasst werden und nur für Werbetreibende mit dem Service generiert werden können. Die Berichte enthalten keine Konversionsdaten, die außerhalb des Konversionsverfolgungs-Systems von Adobe Advertising verfolgt werden.
+++

+++Umsatzdaten unterscheiden sich von den eigenen Umsatzdaten des Werbetreibenden.

**Werbetreibende, die Konversions-Tags für Adobe Advertising verwenden**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abgelaufen oder gelöscht wird, aber der Werbetreibende kann es als gültigen Umsatz betrachten.

* Der Traffic zur Seite des Werbetreibenden stammt aus einem Lesezeichen oder einer organischen Suche anstelle aus einer Anzeige.

* Das Konversionsverfolgungs-Tag ist nicht auf allen entsprechenden Web-Seiten korrekt implementiert oder wurde bearbeitet.

*Mögliche Lösung oder Problemumgehung:*

1. Navigieren Sie zu **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die Transaktionen, die Search, Social und Commerce erhalten haben, mit den Daten des Werbetreibenden.

1. Wenn einige Transaktionen falsch sind oder fehlen, stellen Sie sicher, dass das entsprechende Konversionsverfolgungs-Tag auf allen entsprechenden Web-Seiten implementiert ist und nicht bearbeitet wurde, es sei denn, Ihr Adobe Account Team hat Sie dazu aufgefordert. Ein Tag kann fehlen oder geändert werden, wenn die Website kürzlich aktualisiert wurde.

   Search, Social und Commerce erwarten wohlgeformte URLs (mit Parametern in Name-Wert-Paaren) innerhalb der `ef_transaction_properties`-Variablen und innerhalb des `src` des `img`-Tags.

1. Wenn Sie das Problem nicht ermitteln und beheben können, wenden [ sich an die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung wird versuchen, die fehlenden Transaktionen zu identifizieren und dann nach verwaisten Transaktionen und Transaktionen zu suchen, die nicht von einer Anzeige stammen („unkorrelierte Konversionen„).

**Werbetreibende mit Konversionsdaten-Feeds, die `ef_id` Werte verwenden**

Siehe die möglichen Ursachen und Lösungen für Pixelimplementierungen oben.

**Werbetreibende mit Konversionsdaten-Feeds, die Transaktions-IDs verwenden**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abläuft oder gelöscht wird, aber der Werbetreibende kann es als gültigen Umsatz betrachten.

* Der Traffic zur Seite des Werbetreibenden stammt aus einem Lesezeichen oder einer organischen Suche anstelle aus einer Anzeige.

* Eine Offline-Konversion wurde gemeldet, bevor eine Online-Transaktion mit derselben Transaktions-ID stattfand. Die Online-Transaktion muss zuerst erfolgen.

*Mögliche Lösung oder Problemumgehung:*

1. Navigieren Sie zu **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die Transaktionen, die Search, Social und Commerce erhalten haben, mit den Feed-Daten des Werbetreibenden.

1. Wenn eine Transaktion in der Feed-Datei im Bericht fehlt, überprüfen Sie, ob vor der Offline-Konversion eine Online-Transaktion mit derselben Transaktions-ID (verfolgt über das Pixel) aufgetreten ist.

1. Wenn Sie das Problem nicht ermitteln und beheben können, wenden [ sich an die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung prüft auf Fehler bei der Datenanalyse und [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p).

**Werbetreibende mit anderen Arten von Konversionsdaten-Feeds**

*Mögliche Ursachen:*

* Search, Social und Commerce ignorieren den Umsatz, wenn das Cookie abgelaufen oder gelöscht wird, aber der Werbetreibende kann es als gültigen Umsatz betrachten.

* Der Traffic zur Seite des Werbetreibenden stammt aus einem Lesezeichen oder einer organischen Suche anstelle aus einer Anzeige.

* Es gibt [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p) also zählt Search, Social und Commerce nicht alle Einnahmen, die es erzielen sollte.

* Der Advertiser hat einen Search-, Social- und Commerce-Bericht mit einem anderen Datensatz verglichen, als er im Feed gesendet hat.

* Die Transaktions-IDs (`ev_transid` Werte) wurden nicht gesendet, sind nicht eindeutig oder falsch.

* Die Feed-Datei enthält doppelte Tracking-IDs.

* Beim Parsen der Datei sind Fehler aufgetreten.

* Die Deduplizierungslogik des Werbetreibenden unterscheidet sich von der Logik von Search, Social und Commerce.

*Mögliche Lösung oder Problemumgehung:*

1. Navigieren Sie zu **[!UICONTROL Insights]und[!UICONTROL Reports > Reports]** und generieren Sie eine [!UICONTROL Transaction Report]. Vergleichen Sie die Transaktionen, die Search, Social und Commerce erhalten haben, mit den Daten des Werbetreibenden.

1. Wenn einige Transaktionen falsch sind oder fehlen, stellen Sie sicher, dass a) die Feed-Datei alle erforderlichen Transaktions-IDs und keine doppelten Tracking-IDs enthält und b) die Transaktions-IDs eindeutig und korrekt sind.

1. Wenn Sie das Problem nicht ermitteln und beheben können, wenden [ sich an die Kundenunterstützung](/help/search-social-commerce/get-help.md).

   Die Kundenunterstützung prüft, ob Fehler beim Parsen von Daten und verwaiste Transaktionen vorliegen.
+++

+++Umsatzdaten unterscheiden sich von den Daten in Adobe Analytics
Siehe [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html?lang=de](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html?lang=de).<!-- change link URL to relative link -->
+++

## Spezifische Berichte

+++Sollte der [!UICONTROL Portfolio Report] dieselben Zahlen wie die [!UICONTROL Portfolios] anzeigen?
Die [!UICONTROL Portfolio Report]- und die [!UICONTROL Portfolios] zeigen dieselben Daten an, wenn alle Filter für die Ansicht, die Berichtsparameter und die Datenspalten für die Ansicht und den Bericht identisch sind. Wenn die [!UICONTROL Portfolios] beispielsweise Portfolios anzeigt, die für den Datumsbereich &quot;[!UICONTROL All but inactive]&quot; &quot;[!UICONTROL Last 7 days]&quot; sind und in denen nur die Standarddatenspalten angezeigt werden, zeigt eine [!UICONTROL Portfolio Report] mit den Standardparametern identische Daten an. Wenn Sie einen der Berichtsparameter ändern oder verschiedene Filter in der [!UICONTROL Portfolios] verwenden, können die Datenwerte unterschiedlich sein.
+++

+++Die Daten in meinen [!UICONTROL Portfolio Report] stimmen nicht mit den Daten in meinen [!UICONTROL Search Engine Report] oder [!UICONTROL Search Engine Account Report] überein.
Die [!UICONTROL Portfolio Report] zeigt nur Daten für die Kampagnen an, die den angegebenen Portfolios zugewiesen sind. Die [!UICONTROL Search Engine Report] und [!UICONTROL Search Engine Account Report] können jedoch auch Daten für Kampagnen enthalten, die keinem Portfolio zugewiesen sind.
+++

+++Wie unterscheidet sich die [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] von der [!UICONTROL Model Accuracy Report] auf Portfolioebene?
(Nur für Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzer) Die [!UICONTROL Forecast Accuracy Report], die unter [!UICONTROL Reports] > [!UICONTROL Model Accuracy] verfügbar sind, bietet dieselben Daten wie die [!UICONTROL Model Accuracy Report] auf Portfolioebene, mit dem Unterschied, dass Sie sie für mehrere Portfolios ausführen und die Attributionsregel ändern können. Sie können den Bericht auch mithilfe benutzerdefinierter Parameter ausführen und planen. Außerdem können Sie damit Tabellen-Feeds erstellen. Darüber hinaus ist der [!UICONTROL Forecast Accuracy Report] genauer als der alte Bericht auf Portfolioebene, da er die Umsatzgenauigkeit anhand der historischen Ziele für das Portfolio und nicht anhand des aktuellen Ziels bewertet und Daten für die jeweilige Zeitzone genauer darstellt.
+++

+++Daten auf Anzeigenebene sind nicht für [!DNL Google Ads] DSA (Dynamic Search Ad), DSA (Performance Max), Smart Shopping und [!DNL YouTube]-Kampagnen verfügbar.
Die Werbenetzwerke geben nicht die Kennung an, die erforderlich ist, um den Umsatz einer einzelnen Anzeige für diese Kampagnen zuzuordnen. Daher sind für diese Kampagnentypen in der [!UICONTROL Ads] oder in der [!UICONTROL Ad Variation Report] keine Leistungsdaten auf Anzeigenebene verfügbar. Rechnen Sie daher mit Abweichungen zwischen den gesamten Daten auf Anzeigenebene für eine Kampagne und den gesamten Daten für die Kampagne.
+++

+++Wie kann ich [!UICONTROL Transaction Report] wissen, welche Konversionsmetrik von einem Daten-Feed stammt oder vom Adobe Advertising-Tracking-Pixel verfolgt wird?
In einem Transaktionsbericht können Sie erkennen, ob eine eingeschlossene Konversionsmetrik vom Adobe Advertising-Tracking-Pixel verfolgt wurde, wenn Sie die benutzerdefinierte Spalte &quot;[!UICONTROL Tracking URL]&quot; einbeziehen. Tracking-URLs mit dem Adobe Advertising-Tracking-Pixel beginnen mit &quot;`http://pixel.everesttech.net`&quot;.
+++

+++Die Daten in meinen [!UICONTROL Transaction Report] stimmen nicht mit den Daten in meinen [!UICONTROL Keyword Report] überein.
Wenn Sie beide Berichte nach Portfolio erstellen, unterscheiden sich die Daten, wenn Sie die [!UICONTROL Keyword Report] anhand historischer Daten (d. h. basierend auf der Portfoliokonfiguration während der angegebenen Daten) und nicht anhand von Daten für die aktuellen Kampagnen erstellen. Wenn Sie die [!UICONTROL Transaction Report] nach Portfolio generieren, enthält sie Daten für die aktuellen Kampagnen im Portfolio.
+++

## Tabellen-Feeds

+++Die Berichtsausgabe enthält eine Mischung aus Datumsbereichen.
Möglicherweise werden unterschiedliche Datumsbereiche angezeigt, wenn der Feed Daten mithilfe einer anderen Datenaggregationsebene als &quot;[!UICONTROL Daily]&quot; aggregiert.

Um das Problem zu beheben, aktualisieren Sie den Tabellen-Feed, um täglich aggregierte Daten einzuschließen. Diese Aufgabe umfasst das Aktualisieren der Berichtsvorlage, das Generieren eines Berichts mithilfe der Vorlage, das Erstellen einer benutzerdefinierten [!DNL Microsoft Excel] mithilfe des Berichts und das anschließende Aktualisieren der Feed-Einstellungen, um die neue Excel-Vorlage einzuschließen. Weitere Informationen finden Sie unter [Bearbeiten von Tabellenbericht-Feed-Einstellungen](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).
+++

+++Ein Tabellenvorschub führt zu einem internen Fehler.
Dieser Fehler kann auftreten, wenn Sie die Spalten in der Berichtsvorlage ändern, die [!DNL Microsoft Excel] jedoch nicht entsprechend aktualisieren.

Um das Problem zu beheben, aktualisieren Sie den Tabellen-Feed, um die neuen Spalten einzuschließen. Diese Aufgabe umfasst das Aktualisieren der Berichtsvorlage, das Generieren eines Berichts mithilfe der Vorlage, das Erstellen einer benutzerdefinierten [!DNL Excel] mithilfe des Berichts und das anschließende Aktualisieren der Feed-Einstellungen, um die neue Excel-Vorlage einzuschließen. Weitere Informationen finden Sie unter [Bearbeiten von Tabellenbericht-Feed-Einstellungen](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).
+++

+++Wenn ich versuche, einen Tabellen-Feed in [!DNL Excel] zu öffnen, meldet [!DNL Excel] einen Fehler „Unlesbarer Inhalt“ und die Daten werden aus dem wiederhergestellten Inhalt entfernt.
Wenn die [!DNL Microsoft Excel]-Vorlage die Daten nicht nach Startdatum in aufsteigender Reihenfolge sortiert, kann der Tabellen-Feed leere Zeilen enthalten. Insbesondere wird [!DNL Excel] Fehler „Excel hat unlesbaren Inhalt in &quot;&lt;*Berichtname>.* gefunden.“ Möchten Sie den Inhalt der Arbeitsmappe wiederherstellen? Wenn Sie der Quelle dieser Arbeitsmappe vertrauen, klicken Sie auf „Ja“.“ Wenn Sie auf „Ja“ klicken, erhalten Sie die folgende Meldung: „Entfernte Datensätze: Zelleninformationen vom Teil /xl/worksheets/sheet1.xml&quot;, und der Tabellen-Feed enthält leere Zeilen.

Um das Problem zu beheben, bearbeiten Sie die mit dem Feed verknüpfte [!DNL Excel]-Vorlage, um Daten nach [!DNL Start date in Ascending (Oldest to Newest) order] zu sortieren, und laden Sie dann die aktualisierte Vorlage über die Einstellungen für Tabellen-Feeds hoch. Weitere Informationen finden Sie unter [Bearbeiten von Tabellenbericht-Feeds](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).
+++
