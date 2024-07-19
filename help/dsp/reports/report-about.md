---
title: Über benutzerdefinierte Berichte
description: Erfahren Sie mehr über die Optionen zum manuellen Erstellen benutzerdefinierter Berichte oder zum Verwenden vorkonfigurierter Berichtsvorlagen.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 1d8f7c8a365b53a0345ef4155802802acbf3f027
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Über benutzerdefinierte Berichte

Mit benutzerspezifischen Berichten können Sie den Inhalt und die Bereitstellung Ihrer Berichtsdaten mithilfe der Kampagnendimensionen (wie Advertiser, Platzierung, Sites oder Geos) und den Metriken anpassen, die für Sie am wichtigsten sind. Sie haben folgende Möglichkeiten:

* Konfigurieren Sie die Berichte zur Kampagnenleistung vollständig auf granularer Ebene.
* Wählen Sie aus vorkonfigurierten Berichtvorlagen aus und passen Sie diese optional weiter an.

Sie können Berichte einmal generieren oder planen, dass sie in der angegebenen Zeitzone täglich, wöchentlich oder monatlich um 03:00 Uhr generiert werden. Nachdem ein Bericht generiert wurde, wird er an jeden angegebenen E-Mail-Empfänger oder an verknüpfte [Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md) der folgenden Typen gesendet:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP-SSL (in der Beta-Version)

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

>[!MORELIKETHIS]
>
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [FAQs zu Haushaltsberichten](/help/dsp/reports/faq-household-report.md)
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
>* [Info [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
