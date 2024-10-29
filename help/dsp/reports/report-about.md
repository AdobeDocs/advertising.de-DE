---
title: Über benutzerdefinierte Berichte
description: Erfahren Sie mehr über die Optionen zum manuellen Erstellen benutzerdefinierter Berichte oder zum Verwenden vorkonfigurierter Berichtsvorlagen.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 0ecceaf30ce135dd0083e34dd5c8c5bafb5a3c16
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 0%

---

# Über benutzerdefinierte Berichte

Mit benutzerspezifischen Berichten können Sie den Inhalt und die Bereitstellung Ihrer Berichtsdaten mithilfe der Kampagnendimensionen (wie Advertiser, Platzierung, Sites oder Geos) und den Metriken anpassen, die für Sie am wichtigsten sind. Sie haben folgende Möglichkeiten:

* Konfigurieren Sie die Berichte zur Kampagnenleistung vollständig auf granularer Ebene.

* Wählen Sie aus vorkonfigurierten Berichtvorlagen aus und passen Sie diese optional weiter an.

Sie können Berichte einmalig erstellen oder jeden Tag, jede Woche oder jeden Monat um 03:00 Uhr in der angegebenen Zeitzone gemäß bestimmten Kriterien planen (z. B. alle 15 Tage oder am 1. jedes Monats). Nachdem ein Bericht generiert wurde, können Sie ihn von [!UICONTROL Reports] > [!UICONTROL Custom Reports] oder verknüpften [Berichtszielen](/help/dsp/reports/report-destinations/report-destination-about.md) der folgenden Typen herunterladen:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>Sie können On-Demand-Daten auch auf allen Ebenen einer Kampagne (Kampagne, Paket, Platzierung oder Anzeige) [in der entsprechenden Kampagnenverwaltungsansicht](/help/dsp/campaign-management/reports/campaign-reports-about.md) anzeigen.

## Verfügbare Berichtstypen

* **[!UICONTROL Custom]:** Dieser Bericht ist eine leere Vorlage, mit der Sie Ihren eigenen benutzerspezifischen Bericht mit den meisten Dimensionen und Metriken erstellen können. Die Berichte [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo] und [!UICONTROL Site] sind Varianten dieser Vorlage mit vorausgewählten Spalten und Dimensionen für die jeweiligen Anwendungsfälle.

* Vorkonfigurierte Berichtsvorlagen

   * **[!UICONTROL Billing]:** Verwenden Sie diesen Bericht, um wichtige Abrechnungsmetriken wie Ausgabenmetriken für die Medienabrechnung nach Kampagne zu verstehen. Für Platzierungen mit universellen IDs sind keine Daten verfügbar.

     >[!NOTE]
     >
     >Dieser Bericht enthält Daten zum Rechnungsstellungssegment. Wenn einem Benutzer oder Gerät eine Impression gezeigt wird, die zu mehreren Segmenten gehört, wird nur einem abrechnungsfähigen Segment die Impression gutgeschrieben.

   * **[!UICONTROL Conversion]:** Verwenden Sie diesen Bericht, um zu verstehen, wie Ihre Kampagnen auf der Grundlage von Konversionsmetriken funktionieren, die mithilfe des Adobe Advertising-Konversions-Trackings erfasst wurden. Dieser Bericht enthält die Mehrfachkontaktattribution.

   * **[!UICONTROL Device]:** Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach gerätebezogenen Dimensionen anzuzeigen.

   * **[!UICONTROL Frequency (by Impression)]:** Verwenden Sie diesen Bericht, um die Verteilung der Impressionen zu verstehen, die Unique Viewers angezeigt werden (z. B. wie viele Unique Viewers eine Impression, zwei Impressionen, drei Impressionen usw. gesehen haben. Die Daten sind nach Platzierung oder Kampagne verfügbar.

     >[!NOTE]
     >
     >* Die Daten sind nach dem 1. März 2019 verfügbar.
     >* Die Häufigkeit wird anhand einer Datenstichprobe geschätzt.
     >* Für einige Bestände übermitteln Herausgeber keine Geräte-ID, was das Frequenztracking verhindert. Dieser Bericht enthält nur Impressionen, für die eine Geräte-ID verfügbar war.

   * **[!UICONTROL Frequency (by App/Site)]:** Verwenden Sie diesen Bericht, um zu verstehen, wie viele Unique Users Ihre Anzeigen nach App oder Site erreicht haben. Sie können auch sehen, wie viele Unique Users Ihre Anzeigen über eine bestimmte App oder Site erreicht haben (&quot;Unique Users&quot;).

     >[!NOTE]
     >
     >* Die Daten sind nach dem 15. November 2018 verfügbar.
     >* Bei einigen privaten Beständen geben Herausgeber keine Geräte-ID weiter, was die Frequenzverfolgung verhindert.

   * **[!UICONTROL Geo]**: Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach geografischen Dimensionen anzuzeigen.

   * **[!UICONTROL Margin]:** Verwenden Sie diesen Bericht, um wichtige Metriken wie Marge, Gewinn und andere Ausgabenmetriken nach Kampagne oder Platzierung anzuzeigen. Für Platzierungen mit universellen IDs sind keine Daten verfügbar.

   * **[!UICONTROL Segment]:** Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach Segment anzuzeigen.

     >[!NOTE]
     >
     >* Dieser Bericht soll zeigen, wie unterschiedliche Zielsegmente funktionieren. Es verwendet Daten zur Segmentmitgliedschaft. Wenn eine Impression einer Person oder einem Gerät bereitgestellt wird, die bzw. das zu zwei oder mehr Zielsegmenten gehört, enthält dieser Bericht für jedes Segment eine Zeile. Aus diesem Grund stimmen die Summen in diesem Bericht möglicherweise nicht mit dem tatsächlichen Versand überein.
     >* Konversionsmetriken und benutzerdefinierte Zieldaten für Segmente sind nach dem 2. August 2019 verfügbar. Alle anderen Daten für Segmente sind ab dem 1. Juni 2018 verfügbar.

   * **[!UICONTROL Site]:** Standardmäßig enthält Standardmetriken, die Gesamtnettoausgaben der Medien und die gesamten abrechnungsfähigen Nettoausgaben pro Site.

   * **[!UICONTROL Household Reach & Frequency]:** Verwenden Sie diesen Bericht, um Impressionen, Reichweite und Häufigkeit für eine einzelne Dimension in Anzeigenformaten basierend auf der IP-Adresse auf Haushaltsebene und nicht auf Geräte-/Cookie-Ebene anzuzeigen. Nutzen Sie die Einblicke, um Ihren Medienmix zu optimieren, die Leistung zu verbessern und Möglichkeiten für eine inkrementelle Reichweite zu identifizieren. Weitere Informationen finden Sie unter &quot;[FAQs zu Haushaltsberichten](/help/dsp/reports/faq-reports.md)&quot;. Für Platzierungen mit universellen IDs sind keine Daten verfügbar.

   * **[!UICONTROL Household Conversions]:** Verwenden Sie diesen Bericht, um Durchsichtskonversionen auf Haushaltsebene basierend auf der IP-Adresse und nicht auf der Geräte-/Cookie-Ebene anzuzeigen. Verwenden Sie die Einblicke, um die Kampagnenleistung zu messen und zu optimieren. Weitere Informationen finden Sie unter &quot;[FAQs zu Haushaltsberichten](/help/dsp/reports/faq-reports.md)&quot;. Für Platzierungen mit universellen IDs sind keine Daten verfügbar.

   * **[!UICONTROL Path to Conversion Beta]:** (Beta-Funktion) Verwenden Sie diesen Bericht, um zu ermitteln, wie Budgets optimiert und Anzeigen basierend auf den leistungsstärksten Anzeigeninteraktionssequenzen personalisiert werden können. Der Bericht zeigt die Abfolge von Interaktionspunkten im selben Haushalt an, die zu jeder der ausgewählten Konversionsmetriken im angegebenen Datenbereich führen. Der Bericht verwendet einen festgelegten Lookback-Zeitraum zwischen der ersten Interaktion und einer Konversion und kann eine Dimension enthalten:

      * [!UICONTROL Channel Assist Type]: Zeigt an, wie die folgenden Marketingkanäle den Konvertierungsprozess unterstützt haben: [!UICONTROL Audio Impression], [!UICONTROL CTV Impression], [!UICONTROL Display Click], [!UICONTROL Display Impression], [!UICONTROL Native Click], [!UICONTROL Native Impression], [!UICONTROL Search Click], [!UICONTROL Video Click] oder [!UICONTROL Video Impression].

      * [!UICONTROL Campaign ID] oder [!UICONTROL Campaign Name]: Zeigt an, welche Kampagnen den Konvertierungsprozess unterstützt haben.

      * [!UICONTROL Ad ID] oder [!UICONTROL Ad Name] zeigt, welche DSP Anzeigen zu Konversionen geführt haben.

      * [!UICONTROL Ad ID & Paid Keyword (SSC)] oder [!UICONTROL Ad Name & Paid Keyword (SSC)] zeigt an, welche Suchbegriffe aus Suche, Social und Commerce zu Konversionen geführt haben.

     Zu den Spalten im Bericht gehören &quot;[!UICONTROL Event #1]&quot; bis &quot;[!UICONTROL Event #10],&quot;[!UICONTROL Path Length]&quot;, &quot;% \&lt;Konversionsmetrikname 1\>&quot;, &quot;% \&lt;Konversionsmetrikname 2\>&quot;usw.

     Es werden bis zu 10 aktuelle Interaktionspunkte einbezogen. Die Pfadzeilen werden nach der Anzahl der Konvertierungen geordnet.

   * **[!UICONTROL Path Length Beta]:** (Beta-Funktion) Verwenden Sie diesen Bericht, um die Anzeigenhäufigkeit basierend auf der Anzahl der für Konversionen erforderlichen Benutzerinteraktionspunkte zu verwalten. Der Bericht zeigt die Anzahl der Konversionen nach Pfadlänge (Interaktionspunkte) an, z. B. wie viele Konversionen auftraten, nachdem Benutzer nur eine Anzeigeninteraktion, zwei Anzeigeninteraktionen usw. hatten. Der Bericht kann Daten für mehrere Konversionsmetriken enthalten und verwendet einen festgelegten Lookback-Zeitraum zwischen der ersten Interaktion und einer Konversion. Zu den Spalten im Bericht gehören &quot;[!UICONTROL Path Length]&quot;, &quot;[!UICONTROL Number of] \&lt;Konversionsmetrikname 1\>&quot;, &quot;% \&lt;Konversionsmetrikname 1\>&quot;, \&lt;Konversionsmetrikname 2\>, &quot;% \&lt;Konversionsmetrikname 2\>&quot;usw.

     Daten werden für jede Pfadlänge von bis zu 10 angezeigt; Daten für Pfadlängen über 10 werden gruppiert.

   * **[!UICONTROL Time to Conversion Beta]:** (Beta-Funktion) Verwenden Sie diesen Bericht, um das optimale Attributions-Lookback-Fenster zu ermitteln und neue Möglichkeiten für das Retargeting zu identifizieren. Der Bericht zeigt die Anzahl der Konversionen nach der Zeitdauer in Tagen von der letzten Interaktion (Anzeigenexposition oder Klick) bis zur Konversion an. Der Bericht kann Daten für mehrere Konversionsmetriken enthalten und verwendet einen festgelegten Lookback-Zeitraum zwischen der ersten Interaktion und einer Konversion. Zu den Spalten im Bericht gehören &quot;[!UICONTROL Time Taken (in days)]&quot;, &quot;[!UICONTROL Number of] \&lt;Konversionsmetrikname 1\>&quot;, &quot;% \&lt;Konversionsmetrikname 1\>&quot;, \&lt;Konversionsmetrikname 2\>, &quot;% \&lt;Konversionsmetrikname 2\>&quot;usw. Konversionen, die länger als den Lookback-Zeitraum dauern, werden in einer Zeile gruppiert (wenn der Bericht beispielsweise einen 30-Tage-Lookback-Zeitraum verwendet, werden alle Konversionen, die länger als 30 Tage dauern, in einer Zeile mit dem Wert &quot;[!UICONTROL Time Taken (in days)]&quot;von &quot;30+&quot;gruppiert).

## Kontoübergreifende Berichterstellung {#cross-account-reporting}

Jede Organisation mit mehreren DSP-Konten kann je nach den Anforderungen der Organisation in benutzerspezifischen Berichten optional kontoübergreifende Daten aktivieren. Sie können beispielsweise Konto A Zugriff auf die Daten von Konto B gewähren und Konto B Zugriff auf die Daten von Konto C gewähren (jedoch nicht auf Konto As). Wenden Sie sich zur Aktivierung und Konfiguration dieser Funktion an Ihr Adobe-Account-Team.

Sobald die Funktion für Ihr Unternehmen aktiviert wurde, können Sie einen der folgenden Berichtstypen nach Konto filtern: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] und [!UICONTROL Conversion].[](report-settings.md)

Ihre Kontoeinstellungen unter [!UICONTROL Settings] > [!UICONTROL Account] geben a) die anderen Konten an, deren Daten für Ihr Konto verfügbar sind, und b) die anderen Konten, die auf die Daten Ihres Kontos zugreifen können.

## Die Ansicht [!UICONTROL Custom Reports]

[!UICONTROL Reports] > [!UICONTROL Custom Reports] listet Ihre vorhandenen Berichte auf, einschließlich der erstellten Berichte, der Berichte, die für die zukünftige Generierung geplant sind, und der Berichte, die fehlgeschlagen sind. Die Spalte &quot;[!UICONTROL Report Run]&quot; zeigt Datumsangaben an, ab denen der Bericht am 22. August 2024 ausgelöst wurde. Standardmäßig werden alle nicht archivierten Berichte aufgelistet, die vom Benutzer erstellt wurden, wobei der neueste Bericht oben angezeigt wird. Sie können die Liste weiter nach Status, wiederkehrenden oder einmaligen Berichten, Berichtstyp, Zieltyp und Ersteller filtern.

Sie können neue benutzerdefinierte Berichte erstellen, vorhandene Berichte bearbeiten oder duplizieren, um neue Berichte zu erstellen, sofort Berichte ausführen, eine beliebige Berichtsinstanz aus den letzten vier Monaten herunterladen und Berichte löschen.

## Berichtsstatus {#custom-report-status}

* **[!UICONTROL Yet to start]:** Der Bericht wurde nie ausgeführt.

* **[!UICONTROL Report generating]:** Der Bericht wird derzeit erstellt.

* **[!UICONTROL Ready to download]:** (Nur wiederkehrende Berichte) Eine oder mehrere Instanzen des Berichts können heruntergeladen werden, und es werden weitere Berichtsinstanzen geplant.

* **[!UICONTROL Failed]:** Der Berichtsauftrag ist fehlgeschlagen. Um zu sehen, warum einzelne Report-Instanzen für einen Bericht-Token fehlschlugen, klicken Sie auf ![den Pfeil nach unten](/help/dsp/assets/chevron-down.png "den Pfeil nach unten") neben [!UICONTROL Download]. Fehlgeschlagene Berichtaufträge werden mit einem Fehlersymbol (![Fehleranzeige](/help/dsp/assets/indicator-critical.png "Fehleranzeige")) angezeigt. Halten Sie den Cursor über das Fehlersymbol, um eine Beschreibung des Fehlers zu erhalten.

* **[!UICONTROL Completed]:** Bei nicht wiederkehrenden Berichten ist der Bericht abgeschlossen. Bei wiederkehrenden Berichten sind alle Berichtsinstanzen abgeschlossen. Sie können alle Berichte herunterladen, die in den letzten vier Monaten abgeschlossen wurden.

* **[!UICONTROL Archived]:** Der Bericht wird archiviert und kann nicht ausgeführt werden. Dieser Status wird festgelegt, wenn die Berichterstellung für einen Bericht mehrmals fehlschlägt. Derzeit können Sie diesen Status nicht über die Benutzeroberfläche festlegen.

>[!MORELIKETHIS]
>
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Einen benutzerspezifischen Bericht herunterladen](/help/dsp/reports/report-download.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [FAQs zu Haushaltsberichten](/help/dsp/reports/faq-reports.md)
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
>* [Info [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
