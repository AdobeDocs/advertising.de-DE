---
title: Über benutzerdefinierte Berichte
description: Erfahren Sie mehr über die Optionen zum manuellen Erstellen benutzerdefinierter Berichte oder zum Verwenden vorkonfigurierter Berichtsvorlagen.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 44f7f9b31afbe6b863acd389df641057b1e6dea1
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# Über benutzerdefinierte Berichte

Mit benutzerspezifischen Berichten können Sie den Inhalt und die Bereitstellung Ihrer Berichtsdaten mithilfe der Kampagnendimensionen (wie Advertiser, Platzierung, Sites oder Geos) und den Metriken anpassen, die für Sie am wichtigsten sind. Sie haben folgende Möglichkeiten:

* Konfigurieren Sie die Berichte zur Kampagnenleistung vollständig auf granularer Ebene.

* Wählen Sie aus vorkonfigurierten Berichtvorlagen aus und passen Sie diese optional weiter an.

Sie können Berichte einmal generieren oder planen, dass sie täglich, wöchentlich oder monatlich um 03:00 Uhr in der angegebenen Zeitzone generiert werden. Dies geschieht gemäß bestimmten Kriterien (z. B. alle 15 Tage oder am 1. jedes Monats). Nachdem ein Bericht generiert wurde, können Sie ihn von [!UICONTROL Reports] > [!UICONTROL Custom Reports] oder verknüpften [Berichtszielen](/help/dsp/reports/report-destinations/report-destination-about.md) der folgenden Typen herunterladen:

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
     >* Daten sind nach dem 1. März 2019 verfügbar.
     >* Die Häufigkeit wird anhand einer Datenstichprobe geschätzt.
     >* Für einige Bestände übermitteln Herausgeber keine Geräte-ID, was das Frequenztracking verhindert. Dieser Bericht enthält nur Impressionen, für die eine Geräte-ID verfügbar war.

   * **[!UICONTROL Frequency (by App/Site)]:** Verwenden Sie diesen Bericht, um zu verstehen, wie viele Unique Users über die App oder die Site erreicht wurden. Sie können auch sehen, wie viele Unique Users nur über eine bestimmte App oder Site erreicht wurden (&quot;Unique Users&quot;).

     >[!NOTE]
     >
     >* Daten sind nach dem 15. November 2018 verfügbar.
     >* Bei einigen privaten Beständen geben Herausgeber keine Geräte-ID weiter, was die Frequenzverfolgung verhindert.

   * **[!UICONTROL Geo]**: Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach geografischen Dimensionen anzuzeigen.

   * **[!UICONTROL Margin]:** Verwenden Sie diesen Bericht, um wichtige Metriken wie Marge, Gewinn und andere Ausgabenmetriken nach Kampagne oder Platzierung anzuzeigen. Für Platzierungen mit universellen IDs sind keine Daten verfügbar.

   * **[!UICONTROL Segment]:** Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach Segment anzuzeigen.

     >[!NOTE]
     >
     >* Dieser Bericht soll zeigen, wie unterschiedliche Zielsegmente funktionieren. Es verwendet Daten zur Segmentmitgliedschaft. Wenn eine Impression einer Person oder einem Gerät bereitgestellt wird, die bzw. das zu zwei oder mehr Zielsegmenten gehört, enthält dieser Bericht für jedes Segment eine Zeile. Aus diesem Grund stimmen die Summen in diesem Bericht möglicherweise nicht mit dem tatsächlichen Versand überein.
     >* Konversionsmetriken und benutzerdefinierte Zieldaten für Segmente sind nach dem 2. August 2019 verfügbar. Alle anderen Daten für Segmente sind ab dem 1. Juni 2018 verfügbar.

   * **[!UICONTROL Site]:** Standardmäßig enthält Standardmetriken, die Gesamtnettoausgaben der Medien und die gesamten abrechnungsfähigen Nettoausgaben pro Site.

   * **[!UICONTROL Household Reach & Frequency]:** Verwenden Sie diesen Bericht, um Impressionen, Reichweite und Häufigkeit für eine einzelne Dimension in Anzeigenformaten basierend auf der IP-Adresse auf Haushaltsebene und nicht auf Geräte-/Cookie-Ebene anzuzeigen. Nutzen Sie die Einblicke, um Ihren Medienmix zu optimieren, die Leistung zu verbessern und Möglichkeiten für eine inkrementelle Reichweite zu identifizieren. Weitere Informationen finden Sie unter &quot;[FAQs zu Haushaltsberichten](/help/dsp/reports/faq-household-report.md)&quot;. Für Platzierungen mit universellen IDs sind keine Daten verfügbar.

   * **[!UICONTROL Household Conversions]:** Verwenden Sie diesen Bericht, um Durchsichtskonversionen auf Haushaltsebene basierend auf der IP-Adresse und nicht auf der Geräte-/Cookie-Ebene anzuzeigen. Verwenden Sie die Einblicke, um die Kampagnenleistung zu messen und zu optimieren. Weitere Informationen finden Sie unter &quot;[FAQs zu Haushaltsberichten](/help/dsp/reports/faq-household-report.md)&quot;. Für Platzierungen mit universellen IDs sind keine Daten verfügbar.

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
>* [FAQs zu Haushaltsberichten](/help/dsp/reports/faq-household-report.md)
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
>* [Info [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
