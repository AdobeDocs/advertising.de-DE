---
title: Benutzerdefinierte Berichtseinstellungen
description: Siehe Beschreibungen der benutzerdefinierten Berichtseinstellungen.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '1257'
ht-degree: 0%

---

# Benutzerdefinierte Berichtseinstellungen

**[!UICONTROL Name]** Der Berichtsname. Die maximale Länge beträgt 180 Zeichen.

**[!UICONTROL Report Type]** Berichtstyp: *[!UICONTROL Custom]* (die die meisten verfügbaren Optionen enthält), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]* oder *[!UICONTROL Household Conversions]*.

## [!UICONTROL Apply Filters] Abschnitt

**[!UICONTROL Timezone]:** Die Zeitzone für das Reporting.

**[!UICONTROL Observe Daylight Savings Time]:** Betrachtet die Sommerzeit in den gemeldeten Zeiten.

**\[Datumsbereich\]:** Der Datumsbereich, für den Daten generiert werden sollen. Die Anzahl der Tage variiert je nach Bericht und ausgewählten Dimensionen. Wählen Sie eine aus:

* **[!UICONTROL Previous N days]:** Umfasst Daten für eine bestimmte Anzahl von Tagen vor heute.

* **[!UICONTROL Custom]:** Umfasst Daten zwischen bestimmten Start- und Enddaten. Um Daten über den Vortag zu berichten, wählen Sie **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Umfasst Daten für den vorherigen Kalendermonat.

**[!UICONTROL Add Filters]:** (Optional) Zusätzliche Dimensionen zum Filtern der Daten, unabhängig davon, ob die Dimensionen als Spalten im Bericht enthalten sind oder nicht. Die verfügbaren Filter variieren je nach Berichtstyp und können Folgendes umfassen: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]*, und *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* ist nur für die folgenden Berichtstypen verfügbar, wenn Ihr Unternehmen für [kontoübergreifende Berichterstattung](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], und [!UICONTROL Conversion]. Wenden Sie sich an Ihr Adobe-Account-Team, um weitere Informationen zur kontoübergreifenden Berichterstellung zu erhalten.

Gehen Sie wie folgt vor, um einen oder mehrere Filter anzuwenden:

* Wählen Sie eine Dimension aus und wählen Sie den Operator (*gleich* oder *nicht gleich*) und wählen Sie dann den entsprechenden Wert aus. Wenn Sie beispielsweise nur Daten für Pre-Pup-Anzeigen zurückgeben möchten, geben Sie &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Optional) Fügen Sie dem Filter zusätzliche Kriterien hinzu.
* (Optional) Fügen Sie zusätzliche Filter hinzu, von denen jeder ein oder mehrere Kriterien aufweist.

## [!UICONTROL Build Your Report] Abschnitt

**[!UICONTROL Select To Add As Report Headers]:**  Die Datenspalten oder Kopfzeilen, die in den Bericht aufgenommen werden sollen. Um eine Spalte hinzuzufügen, erweitern Sie die Kategorie und aktivieren Sie das Kontrollkästchen neben dem Spaltennamen. Die verfügbaren Spalten variieren je nach Bericht, und alle nicht verfügbaren Metriken sind deaktiviert. Zu den verfügbaren Datenkategorien gehören:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Die [!UICONTROL Household Reach & Frequency] -Bericht kann nur eine Dimension enthalten.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Die [!UICONTROL Household Reach & Frequency] -Bericht kann entweder Metriken mit Überschneidungen oder Metriken ohne Überlappung enthalten, jedoch nicht beides.

* [!UICONTROL Conversion Metrics] (sortiert nach Advertiser)

* [!UICONTROL Custom Goals] (sortiert nach Advertiser)

Siehe &quot;[Verfügbare Berichtsspalten](report-columns.md)&quot; für Beschreibungen aller Optionen.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Die Reihenfolge der Spaltenüberschriften. Sie können jede Spalte per Drag-and-Drop verschieben, um die Reihenfolge anzupassen.

**[!UICONTROL Format]:** Gibt an, ob ein Bericht in *[!UICONTROL CSV]* (kommagetrennte Werte) oder *[!UICONTROL Tab]* (tabulatorgetrennte Werte).

**[!UICONTROL Headers]:** Ob *[!UICONTROL Include]* oder *[!UICONTROL Do Not Include]* Spaltenüberschriften.

## [!UICONTROL Multi-Touch Conversion Options] Abschnitt

**[!UICONTROL Attribution Rule Settings]:** Die Einstellungen variieren je nach Berichtstyp:

* **\[Attributionstyp\]:** ([!UICONTROL Household Conversion] Berichte mit [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals] -Spalten; Advertiser mit Adobe Advertising-Konversions-Tracking) Wie werden im Bericht Konversionsdaten in einer Reihe von Ereignissen zugeordnet, die zu einer Konversion führen:

   * *[!UICONTROL Unique]:* (Standard) Zählt, wie oft sich ein Dimensionswert (z. B. ein Gerät oder eine Platzierung) auf dem Weg zur Konversion befunden hat.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:*  Verteilt die Gutschrift jeder Konversion basierend auf der Häufigkeit des Auftretens des Dimensionswerts (z. B. ein Gerät oder eine Platzierung) auf dem Pfad zur Konversion. Wenn es beispielsweise insgesamt 10 Impressionen vor der Konvertierung gab, mit 8 bei CTV und 2 bei Mobile, werden 80 % der Gewichtung (0,8) an CTV-Bildschirme und 0,2 an Mobile vergeben.

* **\[Regeltyp\]:** (Alle [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], und [!UICONTROL Site] Berichte mit [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals] -Spalten; Advertiser mit Adobe Advertising-Konversions-Tracking) Wie werden im Bericht Konversionsdaten in einer Reihe von Ereignissen zugeordnet, die zu einer Konversion führen? Sie können mehrere Regeln auswählen, wenn Sie Unterschiede zwischen den Regeln vergleichen möchten.

  >[!NOTE]
  >
  >Konversionspfade umfassen alle Impressionen und Klicks innerhalb der Impressions- oder Klick-Lookback-Fenster des Advertisers, die in [!DNL Advertising Search, Social, & Commerce]. Klicks erhalten während der Konversionszuordnung Vorrang vor Impressionen. Alle Klicks in einem Konversionspfad erhalten die volle Gutschrift auf der Grundlage der Attributionsregel. Impressionen erhalten nur dann eine Gutschrift, wenn im Konversionspfad keine Klicks verfolgt werden.

   * *[!UICONTROL Last Event]:* Ordnet Konversionen dem letzten Klick oder der letzten Impression im Konversionspfad zu.

   * *[!UICONTROL Weight Last More]:* Ordnet allen Ereignissen im Konversionspfad Konversionen zu, gibt jedoch dem letzten Ereignis die höchste Gewichtung und den vorherigen Ereignissen eine schrittweise geringere Gewichtung zu.

   * *[!UICONTROL Even Distribution]:* Weist Konversionen gleichmäßig jedem Ereignis im Konversionspfad zu.

   * *[!UICONTROL Weight First More]:* Ordnet allen Ereignissen im Konversionspfad Konversionen zu, gibt jedoch dem ersten Ereignis die höchste Gewichtung und den folgenden Ereignissen eine schrittweise geringere Gewichtung zu.

   * *[!UICONTROL First Event]:* Ordnet Konversionen dem ersten Klick oder der ersten Impression im Konversionspfad zu.

   * *[!UICONTROL U-shaped]:* Ordnet die Konversion allen Ereignissen im Konversionspfad zu, gibt jedoch dem ersten und letzten Ereignis die höchste Gewichtung, bei einer nacheinander geringeren Gewichtung der Ereignisse in der Mitte des Konversionspfads.

   * *[!UICONTROL Display Only]:*  Ordnet Konversionen dem letzten DSP Klick oder Impression im Konversionspfad zu. Dazu gehören Video- und vernetzte TV-Anzeigen sowie Klicks auf [!DNL Advertising Search, Social, & Commerce] Anzeigen.

   * *[!UICONTROL Social Only]:* Obsolete

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **Lookback:** ([!UICONTROL Household Conversion] Berichte mit [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals] -Spalten; Advertiser mit Adobe Advertising-Konversions-Tracking) Die maximale Anzahl von Tagen nach einem Impressionsereignis, in denen ein Konversionsereignis ihm zugeordnet werden kann. Der Standardwert ist *[!UICONTROL 30 days]* und die maximale Dauer beträgt 92 Tage.

**[!UICONTROL Paths as Columns]:**  (Alle [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], und [!UICONTROL Site] Berichte mit [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals] -Spalten) Welche Konversionstypen werden in Berichten aufgeführt, wenn auf demselben Gerät frühere Ereignisse aufgetreten sind. Sie können bis zu drei Typen einbeziehen. Für jeden ausgewählten Typ wird für jede Konversionsmetrik eine separate Spalte eingefügt und dem angegebenen Suffix ([!UICONTROL (tl)], [!UICONTROL (ct)]oder [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Umrechnungen, die Klicks (CT für Clickthrough) und Impressionen (VT für Durchsicht) zugeordnet werden. Auf Impressionen zugeordnete Konversionen werden mit der angegebenen Durchsichtsgewichtung multipliziert. Die standardmäßige Durchsichtsgewichtung beträgt 100 %, d. h. Konversionen, die Impressionen zugeordnet werden, werden als 100 % des Werts der Konversionen gezählt, die den Klicks zugeordnet sind.

* *[!UICONTROL With Clicks (CT)]:* Umfasst nur Konversionen, die Klicks zugeordnet sind.

* *[!UICONTROL Impressions Only (VT)]:* Umfasst nur Konversionen, die Impressionen zugeordnet wurden, da im Konversionspfad keine Klicks verfolgt wurden.

**[!UICONTROL Conversion Reporting Based On]:**  So melden Sie Konversionsdaten:

* *[!UICONTROL Conversion Timestamp]:* (Standard) Konversionen sind mit dem Konvertierungsdatum verknüpft.

* *[!UICONTROL Event Timestamp]:* Konversionen werden basierend auf dem Datum der Impression oder des Klicks gemeldet, die die Konversion verursacht haben, wie durch die angegebene [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Abschnitt

**[!UICONTROL Destination Type]:** Wählen Sie einen der folgenden Zieltypen aus:

* *[!UICONTROL S3]:* So senden Sie den abgeschlossenen Bericht an eine oder mehrere [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) -Speicherorte, die Sie im **[!UICONTROL Destination Name]** -Feld.
* *[!UICONTROL sFTP]:* So senden Sie den abgeschlossenen Bericht an einen oder mehrere SFTP-Standorte, die Sie im Abschnitt **[!UICONTROL Destination Name]** -Feld.
* *[!UICONTROL FTP]:* So senden Sie den abgeschlossenen Bericht an einen oder mehrere FTP-Speicherorte, die Sie im Abschnitt **[!UICONTROL Destination Name]** -Feld.
* *[!UICONTROL FTP SSL](Aktuell in Beta):* So senden Sie den abgeschlossenen Bericht an einen oder mehrere FTP-SSL-Speicherorte, die Sie im Abschnitt **[!UICONTROL Destination Name]** -Feld.
* *[!UICONTROL Email]:* Angabe der E-Mail-Adresse(n), an die abgeschlossene Berichte oder Benachrichtigungen gesendet werden sollen, wenn der Bericht aufgrund von Fehlern abgebrochen wird.

>[!NOTE]
>
> Sie können den Zieltyp nach dem Speichern des Berichts nicht mehr ändern.

**[!UICONTROL Email]:** (Nur E-Mail-Zieltyp) Geben Sie für jede Adresse die Adresse ein und klicken Sie auf **+**.

**[!UICONTROL Destination Name]:** (Nur S3-, FTP-, sFTP- und FTP-SSL-Zieltypen) Die Namen der Berichtsziele, an die der benutzerdefinierte Bericht gesendet wird.

* Um ein vorhandenes Ziel anzugeben, wählen Sie einen Zielnamen aus der Liste aus. Sie können mehrere Zielnamen separat auswählen.

* So erstellen Sie ein neues Ziel:

   1. Klicks **Neues Ziel hinzufügen**.

   1. Geben Sie die [Berichtszieleinstellungen](/help/dsp/reports/report-destinations/report-destination-settings.md)und klicken Sie auf **Speichern**.

   1. Klicken Sie in den Berichtseinstellungen auf **Aktualisieren Sie die Zielnamen.**

      Das neue Ziel ist jetzt in der Liste der vorhandenen Ziele verfügbar und Sie können es optional zum Bericht hinzufügen.

**[!UICONTROL Frequency]:** (Für jeden [!UICONTROL Destination Name]) Wie oft der Bericht an das Ziel gesendet wird: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]* oder *[!UICONTROL Monthly]*.

**[!UICONTROL Start Day]:** (Für jeden [!UICONTROL Destination Name] mit [!UICONTROL Frequency] von *[!UICONTROL Weekly]* oder *[!UICONTROL Monthly]*) Welcher Tag zum Generieren des Berichts. Wählen Sie für wöchentliche Berichte den Wochentag aus. Wählen Sie für monatliche Berichte den numerischen Tag des Monats aus.

## [!UICONTROL Save Report] Abschnitt

**[!UICONTROL When to Generate]:** Wann wird der Bericht generiert? *[!UICONTROL On Schedule]* oder *[!UICONTROL Run Now]*. Geplante Berichte werden um 9:00 Uhr in der Zeitzone des Kontos bereitgestellt.

**[!UICONTROL End Date]:** Das Ablaufdatum des Berichts, das bis zu vier Monate entfernt sein kann. Bevor ein Bericht abläuft, erhalten alle angegebenen E-Mail-Empfänger sieben Tage und einen Tag vor dem Ablaufdatum einen E-Mail-Warnhinweis. Um den Bericht länger zu halten, ändern Sie das Ablaufdatum in den Berichtseinstellungen.

>[!NOTE]
>
>Sie können [jederzeit einen benutzerspezifischen Bericht ausführen](report-run-now.md) aus dem [!UICONTROL Reports] anzeigen.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Benutzerspezifischen Bericht duplizieren](/help/dsp/reports/report-copy.md)
>* [Benutzerspezifischen Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Benutzerspezifischen Bericht ausführen](/help/dsp/reports/report-run-now.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Über Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
