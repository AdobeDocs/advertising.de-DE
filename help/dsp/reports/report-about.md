---
title: Über benutzerdefinierte Berichte
description: Erfahren Sie mehr über Optionen zum manuellen Erstellen benutzerdefinierter Berichte oder die Verwendung vorkonfigurierter Berichtsvorlagen.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: a643a2d255431c5ce93f2df092d92932d4cccc02
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 0%

---

# Über benutzerdefinierte Berichte

Benutzerdefinierte Berichte ermöglichen es Ihnen, den Inhalt und die Bereitstellung Ihrer Berichtsdaten mithilfe der Kampagnendimensionen (wie Advertiser, Platzierung, Sites oder Geos) und der Metriken, die Ihnen am wichtigsten sind, anzupassen. Sie haben folgende Möglichkeiten:

* Vollständige Konfiguration der Kampagnenleistungsberichte auf granularer Ebene.

* Wählen Sie aus vorkonfigurierten Berichtsvorlagen und passen Sie sie optional weiter an.

Sie können Berichte einmal generieren oder sie täglich, wöchentlich oder monatlich um 03 :00 in der angegebenen Zeitzone gemäß den angegebenen Kriterien planen (z. B. alle 15 Tage oder am 1. eines jeden Monats). Nachdem ein Bericht generiert wurde, können Sie ihn von [!UICONTROL Reports] > [!UICONTROL Custom Reports] oder von verknüpften [Berichtszielen](/help/dsp/reports/report-destinations/report-destination-about.md) der folgenden Typen herunterladen:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP-SSL-<!-- (in beta) -->
* SFTP

>[!NOTE]
>
>Sie können On-Demand-Daten auch auf allen Kampagnenebenen (Kampagne, Paket, Platzierung oder Anzeige) in [&#x200B; entsprechenden Kampagnenverwaltungsansicht anzeigen](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Verfügbare Berichtstypen

* **[!UICONTROL Custom]:** Dieser Bericht ist eine leere Vorlage, mit der Sie Ihren eigenen benutzerdefinierten Bericht erstellen können, indem Sie die meisten Dimensionen und Metriken verwenden. [!UICONTROL Conversion]-, [!UICONTROL Device]-, [!UICONTROL Geo]- und [!UICONTROL Site]-Berichte sind Varianten dieser Vorlage mit vorab ausgewählten Spalten und Dimensionen für die jeweiligen Anwendungsfälle.

* Vorkonfigurierte Berichtsvorlagen

   * **[!UICONTROL All-in Cost BETA]**: (Nur Werbetreibende mit Advertising Creative und Advertising DSP; Beta-Funktion) Verwenden Sie diesen Bericht, um zu sehen, wie viel Advertising DSP-Ausgaben der Anzeigenauslieferung für Adobe Creative zugeordnet wurden. Sie können Kreativ-, Attribut-, Ziel- und andere Daten auf Kampagnen-, Paket-, Platzierungs- und Anzeigenebene anzeigen.

   * **[!UICONTROL Billing]:** Verwenden Sie diesen Bericht, um wichtige Abrechnungsmetriken wie Ausgabenmetriken für die Medienabrechnung nach Kampagne zu verstehen. Daten sind nicht für Platzierungen verfügbar, die auf universelle IDs abzielen.

     >[!NOTE]
     >
     >Dieser Bericht enthält Daten zum Abrechnungssegment. Wenn einem Benutzer oder Gerät eine Impression bereitgestellt wird, die zu mehreren Segmenten gehört, wird nur ein abrechnungsfähiges Segment mit der Impression gutgeschrieben.

   * **[!UICONTROL Content]:** Verwenden Sie diesen Bericht, um die Bereitstellung von Impressionen und andere Metriken anhand bestimmter Inhaltsdimensionen (wie Genre, Produktionsqualität und Inhaltsbewertung) zu verstehen, sodass Sie die Zielgruppenbestimmung optimieren und die Markensicherheit gewährleisten können. Zusätzlich zu den Inhaltsdimensionen enthält der Bericht die meisten Standarddimensionen, Metriken und Filter. Daten nach Inhaltsdimension sind für [!DNL Freewheel], [!DNL Index], [!DNL Magnite], [!DNL Microsoft], [!DNL Nexxen], [!DNL Pubmatic], [!DNL Sharethrough] und [!DNL Triplelift] verfügbar. Inhaltssignale werden von Publishern während des Bid-Streams weitergeleitet und unterliegen der Verfügbarkeit.

   * **[!UICONTROL Conversion]:** Verwenden Sie diesen Bericht, um zu verstehen, wie Ihre Kampagnen auf der Grundlage von Konversionsmetriken funktionieren, die mit dem Konversionstracking von Adobe Advertising erfasst wurden. Dieser Bericht enthält die Multi-Touch-Attribution.

   * **[!UICONTROL Custom Creative]:** (Nur Werbetreibende mit Advertising Creative) Verwenden Sie diesen Bericht, um die Leistung in allen Ihren Advertising Creative-Anzeigenerlebnissen zu überwachen.

   * **[!UICONTROL Device]:** Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach gerätebezogenen Dimensionen anzuzeigen.

   * **[!UICONTROL Frequency (by Impression)]:** Verwenden Sie diesen Bericht, um die Verteilung der Impressionen zu verstehen, die Unique Viewers angezeigt werden (z. B. wie viele Unique Viewers eine Impression, zwei Impressions, drei Impressions usw. gesehen haben). Daten sind nach Platzierung oder Kampagne verfügbar.

     >[!NOTE]
     >
     >* Die Daten liegen nach dem 1. März 2019 vor.
     >* Die Häufigkeit wird anhand einer Stichprobe von Daten geschätzt.
     >* Bei einigen Inventaren geben die Herausgeber keine Gerätekennung weiter, was die Frequenzverfolgung verhindert. Dieser Bericht enthält nur Impressions, für die eine Gerätekennung verfügbar war.

   * **[!UICONTROL Frequency (by App/Site)]:** Verwenden Sie diesen Bericht, um zu verstehen, wie viele eindeutige Benutzer Ihre Anzeigen per App oder Site erreicht haben. Sie können auch sehen, wie viele Unique Users Ihre Anzeigen über nur eine bestimmte App oder Site erreicht haben („Unique Users„).

     >[!NOTE]
     >
     >* Die Daten liegen nach dem 15. November 2018 vor.
     >* Bei einigen privaten Inventaren geben Herausgeber keine Gerätekennung weiter, was die Frequenzverfolgung verhindert.

   * **[!UICONTROL Geo]**: Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach geografischen Dimensionen anzuzeigen.

   * **[!UICONTROL Household Conversions]:** Verwenden Sie diesen Bericht, um View-Through-Konvertierungen auf Haushaltsebene basierend auf der IP-Adresse und nicht auf der Geräte-/Cookie-Ebene anzuzeigen. Verwenden Sie die Erkenntnisse, um die Kampagnenleistung zu messen und zu optimieren. Weitere Informationen finden [&#x200B; unter „FAQs &#x200B;](/help/dsp/reports/faq-reports.md) Haushaltsberichte“. Daten sind nicht für Platzierungen verfügbar, die auf universelle IDs abzielen.

   * **[!UICONTROL Household Reach & Frequency]:** Verwenden Sie diesen Bericht, um Impressionen, Reichweite und Häufigkeit für eine einzelne Dimension in allen Anzeigenformaten auf Haushaltsebene basierend auf der IP-Adresse und nicht auf der Geräte-/Cookie-Ebene anzuzeigen. Nutzen Sie die Erkenntnisse, um Ihren Medienmix zu optimieren, die Leistung zu verbessern und Möglichkeiten für eine inkrementelle Reichweite zu identifizieren. Weitere Informationen finden [&#x200B; unter „FAQs &#x200B;](/help/dsp/reports/faq-reports.md) Haushaltsberichte“. Daten sind nicht für Platzierungen verfügbar, die auf universelle IDs abzielen.

   * **[!UICONTROL Margin]:** Verwenden Sie diesen Bericht, um Schlüsselmetriken wie Marge, Gewinn und andere Ausgabenmetriken nach Kampagne oder Platzierung anzuzeigen. Daten sind nicht für Platzierungen verfügbar, die auf universelle IDs abzielen.

   * **[!UICONTROL Path to Conversion]:** Verwenden Sie diesen Bericht, um zu ermitteln, wie Sie basierend auf leistungsstärksten Anzeigeninteraktionssequenzen Budgets optimieren und Anzeigen personalisieren können. Der Bericht zeigt die Sequenz von Interaktionspunkten im selben Haushalt an, die zu jeder der ausgewählten Konversionsmetriken im angegebenen Datenbereich führen. Der Bericht verwendet einen angegebenen Lookback-Zeitraum zwischen der ersten Interaktion und einer Konversion und kann eine Dimension enthalten:

      * [!UICONTROL Channel Assist Type]: Zeigt, wie die folgenden Marketing-Kanäle den Konvertierungsprozess unterstützt haben: [!UICONTROL Audio Impression], [!UICONTROL CTV Impression], [!UICONTROL Display Click], [!UICONTROL Display Impression], [!UICONTROL Native Click], [!UICONTROL Native Impression], [!UICONTROL Search Click], [!UICONTROL Video Click] oder [!UICONTROL Video Impression].

      * [!UICONTROL Campaign ID] oder [!UICONTROL Campaign Name]: Zeigt an, welche Kampagnen den Konvertierungsprozess unterstützt haben.

      * [!UICONTROL Ad ID] oder [!UICONTROL Ad Name] zeigt an, welche DSP-Anzeigen zu Konversionen geführt haben.

      * [!UICONTROL Ad ID & Paid Keyword (SSC)] oder [!UICONTROL Ad Name & Paid Keyword (SSC)] zeigt an, welche Keywords für Suche, Social und Commerce zu Konversionen geführt haben.

     Zu den Spalten im Bericht gehören &quot;[!UICONTROL Event #1]&quot; bis &quot;[!UICONTROL Event #10]&quot;, &quot;[!UICONTROL Path Length]&quot;, &quot;% \&lt;Name der Konversionsmetrik 1\>,“ &quot;% \&lt;Name der Konversionsmetrik 2\>&quot; usw.

     Es werden bis zu den 10 neuesten Interaktionspunkten berücksichtigt. Die Pfadzeilen werden nach der Anzahl der Konvertierungen sortiert.

     Einen Vergleich dieses Berichts mit Berichten, die von [!DNL Advanced Measurement Services] und Adobe Analytics erstellt wurden, finden Sie unter [Häufig gestellte Fragen zu benutzerdefinierten Berichten](/help/dsp/reports/faq-reports.md).

   * **[!UICONTROL Path Length]:** Verwenden Sie diesen Bericht, um die Anzahl der für Konversionen erforderlichen Benutzerinteraktionspunkte im Zeitverlauf zu verfolgen, sodass Sie die optimale Anzeigenfrequenz auswählen können. Der Bericht zeigt die Anzahl der Konversionen nach Pfadlänge (Interaktionspunkte) an, z. B. wie viele Konversionen stattgefunden haben, nachdem Benutzende nur eine Anzeigeninteraktion, zwei Anzeigeninteraktionen usw. hatten. Der Bericht kann Daten für mehrere Konversionsmetriken enthalten und verwendet einen angegebenen Lookback-Zeitraum zwischen der ersten Interaktion und einer Konversion. Die Spalten im Bericht enthalten &quot;[!UICONTROL Path Length]&quot;, &quot;[!UICONTROL Number of] \&lt;Name der Konversionsmetrik 1\>,“ &quot;% \&lt;Name der Konversionsmetrik 1\>,“ \&lt;Name der Konversionsmetrik 2\>,“ &quot;% \&lt;Name der Konversionsmetrik 2\>&quot; usw.

     Es werden Daten für jede Pfadlänge von bis zu 10 angezeigt. Daten für Pfadlängen von mehr als 10 werden gruppiert.

   * **[!UICONTROL Segment]:** Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach Segment anzuzeigen.

     >[!NOTE]
     >
     >* Dieser Bericht soll zeigen, wie verschiedene Zielsegmente funktionieren. Es werden Daten zur Segmentzugehörigkeit verwendet. Wenn einer Person oder einem Gerät, die bzw. das zu zwei oder mehr Zielsegmenten gehört, eine Impression bereitgestellt wird, enthält dieser Bericht eine Zeile für jedes Segment. Aus diesem Grund stimmen die Gesamtwerte in diesem Bericht möglicherweise nicht mit dem tatsächlichen Versand überein.
     >* Konversionsmetriken und benutzerdefinierte Zieldaten für Segmente sind nach dem 2. August 2019 verfügbar. Alle anderen Daten für Segmente stehen ab dem 1. Juni 2018 zur Verfügung.

   * **[!UICONTROL Site]:** Enthält standardmäßig Standardmetriken, Nettoausgaben für Medien insgesamt und abrechenbare Nettoausgaben insgesamt nach Standort.

   * **[!UICONTROL Time to Conversion]:** Verwenden Sie diesen Bericht, um das optimale Attribution-Lookback-Fenster zu bestimmen und Kampagnen mit längeren Konversionszeiten zu identifizieren, die vom Retargeting profitieren können. Der Bericht zeigt die Anzahl der Konversionen nach der Zeitdauer in Tagen von der letzten Interaktion (Anzeigenbelichtung oder Klick) bis zur Konversion an. Der Bericht kann Daten für mehrere Konversionsmetriken enthalten und verwendet einen angegebenen Lookback-Zeitraum zwischen der ersten Interaktion und einer Konversion. Die Spalten im Bericht enthalten &quot;[!UICONTROL Time Taken (in days)]&quot;, &quot;[!UICONTROL Number of] \&lt;Name der Konversionsmetrik 1\>,“ &quot;% \&lt;Name der Konversionsmetrik 1\>,“ \&lt;Name der Konversionsmetrik 2\>,“ &quot;% \&lt;Name der Konversionsmetrik 2\>&quot; usw. Konversionen, die länger als der Lookback-Zeitraum dauern, werden in einer Zeile gruppiert (wenn der Bericht beispielsweise einen 30-tägigen Lookback-Zeitraum verwendet, werden alle Konversionen, die länger als 30 Tage dauern, in einer Zeile mit dem Wert &quot;[!UICONTROL Time Taken (in days)]&quot; „30+&quot; gruppiert).

## Kontoübergreifende Berichterstattung {#cross-account-reporting}

Jedes Unternehmen mit mehreren DSP-Konten kann optional kontenübergreifende Daten in benutzerdefinierten Berichten aktivieren, je nach den Anforderungen des Unternehmens. Beispielsweise können Sie Konto A Zugriff auf Daten von Konto B und Konto B Zugriff auf Daten von Konto C (aber nicht auf Daten von Konto A) gewähren. Wenden Sie sich zur Aktivierung und Konfiguration dieser Funktion an Ihr Adobe-Account-Team.

Sobald die Funktion für Ihr Unternehmen aktiviert ist, können [&#x200B; einen &#x200B;](report-settings.md) Berichtstypen nach Konto filtern: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] und [!UICONTROL Conversion].

Ihre Kontoeinstellungen unter [!UICONTROL Settings] > [!UICONTROL Account] geben a) die anderen Konten an, deren Daten für Ihr Konto verfügbar sind, und b) die anderen Konten, die auf die Daten Ihres Kontos zugreifen können.

## Die [!UICONTROL Custom Reports]

[!UICONTROL Reports] > [!UICONTROL Custom Reports] listet Ihre vorhandenen Berichte auf, einschließlich generierter Berichte, Berichte, die für die zukünftige Generierung geplant sind, und Berichte, die fehlgeschlagen sind. Die Spalte &quot;[!UICONTROL Report Run]&quot; zeigt ab dem 22. August 2024 die Daten an, an denen der Bericht ausgelöst wurde. Standardmäßig werden alle nicht archivierten Berichte, die vom Benutzer erstellt wurden, aufgelistet, wobei der neueste Bericht oben steht. Sie können die Liste weiter nach Status filtern, unabhängig davon, ob es sich um einen wiederkehrenden oder einen einmaligen Bericht handelt, nach Berichtstyp, Zieltyp und dem Ersteller des Berichts.

Sie können neue benutzerspezifische Berichte erstellen, vorhandene Berichte bearbeiten oder duplizieren, um neue Berichte zu erstellen, Berichte sofort ausführen, eine Berichtsinstanz der letzten vier Monate herunterladen und Berichte löschen.

## Berichtsstatus {#custom-report-status}

* **[!UICONTROL Yet to start]:** Der Bericht wurde noch nie ausgeführt.

* **[!UICONTROL Report generating]:** Der Bericht wird derzeit erstellt.

* **[!UICONTROL Ready to download]:** (Nur wiederkehrende Berichte) Mindestens eine Instanz des Berichts kann heruntergeladen werden, und es sind mehrere Berichtsinstanzen geplant.

* **[!UICONTROL Failed]:** Der Berichtsvorgang ist fehlgeschlagen. Um zu sehen, warum einzelne Berichtinstanzen für ein Berichtskabel fehlgeschlagen sind, klicken Sie auf ![den Abwärtspfeil](/help/dsp/assets/chevron-down.png " den Abwärtspfeil") neben [!UICONTROL Download]. Fehlgeschlagene Berichtsaufträge werden mit einem Fehlersymbol gekennzeichnet (![Fehleranzeige](/help/dsp/assets/indicator-critical.png "Fehleranzeige")). Eine Beschreibung des Fehlers finden Sie, indem Sie den Cursor über das Fehlersymbol halten.

* **[!UICONTROL Completed]:** Der Bericht ist für nicht wiederkehrende Berichte abgeschlossen. Für wiederkehrende Berichte werden alle Berichtsinstanzen abgeschlossen. Sie können alle in den letzten vier Monaten abgeschlossenen Berichte herunterladen.

* **[!UICONTROL Archived]:** Der Bericht ist archiviert und kann nicht ausgeführt werden. Dieser Status wird festgelegt, wenn die Berichterstellung für einen Bericht mehrmals fehlschlägt. Derzeit können Sie diesen Status nicht über die Benutzeroberfläche festlegen.

>[!MORELIKETHIS]
>
>* [Erstellen eines benutzerdefinierten Berichts](/help/dsp/reports/report-create.md)
>* [Benutzerdefinierten Bericht herunterladen](/help/dsp/reports/report-download.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [FAQs zu Haushaltsberichten](/help/dsp/reports/faq-reports.md)
>* [Typen von Leistungsberichten in Ansichten des Kampagnen-Managements](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
>* [Über [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
