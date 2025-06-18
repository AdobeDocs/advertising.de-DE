---
title: Benutzerdefinierte Berichtseinstellungen
description: Siehe Beschreibungen der benutzerdefinierten Berichtseinstellungen.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 8e6d2a1d39231176f3836246958b82691fbb5006
workflow-type: tm+mt
source-wordcount: '1541'
ht-degree: 0%

---

# Benutzerdefinierte Berichtseinstellungen

**[!UICONTROL Name]:** Der Berichtsname. Die maximale Länge beträgt 180 Zeichen.

**[!UICONTROL Report Type]:** Der Berichtstyp: *[!UICONTROL Custom]* (was die meisten verfügbaren Optionen umfasst), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, *[!UICONTROL Household Conversions]*, *[!UICONTROL Path to Conversions Beta]*,, *[!UICONTROL Path Length Beta]* oder *[!UICONTROL Time to Conversion Beta]*.

## [!UICONTROL Report Range]

In diesem Abschnitt werden die Daten festgelegt, die im Bericht enthalten sind. Informationen zum Einrichten von Datumsangaben für den Berichtsplan finden Sie im Abschnitt &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** Die Zeitzone für das Reporting.

**[!UICONTROL Observe Daylight Savings Time]:** Berücksichtigt die Sommerzeit in den gemeldeten Zeiten.

**Range:** Der Datumsbereich, für den Daten generiert werden sollen. Die Anzahl der verfügbaren Tage variiert je nach Bericht und den ausgewählten Dimensionen. Eine Option auswählen:

* **[!UICONTROL Previous Calendar Week]:** Enthält Daten zur vorherigen Kalenderwoche.

* **[!UICONTROL Previous Calendar Month]:** Enthält Daten für den vorherigen Kalendermonat.

* **[!UICONTROL Custom Range]:** Schließt Daten zwischen einem bestimmten Anfangs- und Enddatum ein. Um Daten über den Vortag zu melden, wählen Sie **[!UICONTROL Present]** aus.

## [!UICONTROL Report Run schedule]

In diesem Abschnitt werden die Daten festgelegt, an denen der Bericht ausgeführt wird. Informationen zum Einrichten der Datumsangaben, für die Berichtsdaten einbezogen werden sollen, finden Sie im Abschnitt &quot;[!UICONTROL Report range]&quot;.

**\[schedule\]:** Zeitpunkt für die Berichterstellung:

* *[!UICONTROL Immediately]*: Fügt den Bericht sofort der Berichtswarteschlange hinzu.

  >[!NOTE]
  >
  >Sie können auch [einen benutzerdefinierten Bericht jederzeit ausführen](report-run-now.md) über die [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;date\>:* Führt den Bericht an einem bestimmten Datum (bis 09:00 Uhr) in der Zeitzone des Kontos aus.

* *[!UICONTROL Recurring]:* Führt den Bericht nach einem Zeitplan für einen bestimmten Zeitraum aus.

   * **\[schedule\]:** Wie oft der Bericht ausgeführt wird:

      * *Täglich* um den Bericht alle N Tage auszuführen. Wenn der Bericht beispielsweise alle zwei Wochen (14 Tage) ausgeführt werden soll, wählen Sie diese Option aus und geben Sie **14** ein.

      * *Wöchentlich* um den Bericht an bestimmten Wochentagen auszuführen. Wenn Sie beispielsweise den Bericht montags und freitags ausführen möchten, wählen Sie diese Option aus und aktivieren Sie die Kontrollkästchen neben **Montag** und **Freitag**.

      * *Monatlich* um den Bericht an einem bestimmten numerischen Tag des Monats von 1 bis 30 auszuführen. Wenn der Bericht beispielsweise am ersten Tag jedes Monats ausgeführt wird, wählen Sie diese Option und geben Sie **1** ein.

   * **Von**: Das erste Datum, an dem der Bericht ausgeführt werden kann. Je nach angegebenem Zeitplan kann die erste Berichtsinstanz nach diesem Datum auftreten.

   * **Bis**: Das Ablaufdatum des Berichts, das bis zu vier Kalendermonate entfernt sein kann. Bevor ein Bericht abläuft, erhalten alle angegebenen E-Mail-Ziele sieben Tage und einen Tag vor dem Ablaufdatum einen E-Mail-Warnhinweis. Um den Bericht länger zu halten, ändern Sie dieses Datum.

## [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (Optional) Zusätzliche Dimensionen, nach denen die Daten gefiltert werden sollen, unabhängig davon, ob die Dimensionen als Spalten im Bericht enthalten sind oder nicht. Die verfügbaren Filter variieren je nach Berichtstyp und können Folgendes umfassen: *[!UICONTROL Account]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* und *[!UICONTROL Video Duration]*.

<!-- Add when available:
*[!UICONTROL Deal ID]*, *[!UICONTROL Deal List]*, 
-->

Gehen Sie wie folgt vor, um einen oder mehrere Filter anzuwenden:

* Wählen Sie eine Dimension aus, wählen Sie den Operator *gleich* oder *nicht gleich* aus und wählen Sie dann den entsprechenden Wert aus. Um beispielsweise Daten nur für Preroll-Anzeigen zurückzugeben, geben Sie &quot;[!UICONTROL Ad Type equals Preroll]&quot; an.
* (Optional) Fügen Sie dem Filter zusätzliche Kriterien hinzu.
* (Optional) Fügen Sie zusätzliche Filter hinzu, die jeweils ein oder mehrere Kriterien aufweisen.

\* *[!UICONTROL Account]* ist nur für die folgenden Berichtstypen verfügbar, wenn Ihre Organisation für [kontenübergreifendes Reporting](report-about.md#cross-account-reporting) konfiguriert ist: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] und [!UICONTROL Conversion]. Wenden Sie sich an Ihr Adobe-Account-Team , um weitere Informationen zur kontenübergreifenden Berichterstellung zu erhalten.

**[!UICONTROL Include data from Adobe Advertising SSC]:** (Nur Berichte zu Konversionspfad, Pfadlänge und Zeit bis zur Konversion) Enthält Daten zu Klicks auf Suchanzeigen aus angegebenen Advertising-Kampagnen für Suche, Social und Commerce. Bei Auswahl dieser Option:

1. Wählen Sie das Konto Suchen, Social und Commerce mit dem Filter **Filtern nach[!UICONTROL SSC Account]** aus.

1. Wählen Sie die Kampagnen mit dem Filter **Nach[!UICONTROL SSC Campaign]** filtern“ aus.

   Um mehrere Kampagnen auszuwählen, klicken Sie auf **[!UICONTROL Add Criteria]** für die zweite und die folgenden Kampagnen.

## [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** Die Datenspalten oder Kopfzeilen, die in den Bericht aufgenommen werden sollen. Um eine Spalte hinzuzufügen, erweitern Sie die Kategorie und aktivieren Sie das Kontrollkästchen neben dem Spaltennamen. Die verfügbaren Spalten variieren je nach Bericht, und alle nicht verfügbaren Metriken sind deaktiviert. Die verfügbaren Datenkategorien können Folgendes umfassen:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Die [!UICONTROL Household Reach & Frequency]- und [!UICONTROL Path to Conversion]-Berichte können nur eine Dimension enthalten.
  > Die [!UICONTROL Path Length]- und [!UICONTROL Time to Conversion] enthalten keine Dimensionen.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Der [!UICONTROL Household Reach & Frequency] kann entweder Überschneidungsmetriken oder Nicht-Überschneidungsmetriken enthalten, aber nicht beides.

* [!UICONTROL Conversion Metrics] (sortiert nach Advertiser)

* [!UICONTROL Custom Goals] (sortiert nach Advertiser)

Beschreibungen [ Optionen finden Sie unter „Verfügbare ](report-columns.md)&quot;.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Die Reihenfolge der Spaltenüberschriften. Sie können eine beliebige Spalte per Drag-and-Drop verschieben, um die Reihenfolge anzupassen.

**[!UICONTROL Format]:**, ob ein Bericht im *[!UICONTROL CSV]*-Format (kommagetrennte Werte) oder im *[!UICONTROL Tab]*-Format (tabulatorgetrennte Werte) generiert werden soll.

**[!UICONTROL Headers]:** Gibt an, ob Spaltenüberschriften *[!UICONTROL Include]* oder *[!UICONTROL Do Not Include]* werden.

## [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Die Einstellungen variieren je nach Berichtstyp:

* **\[Attributionstyp\]:** ([!UICONTROL Household Conversion] von Berichten mit [!UICONTROL Conversion Metrics]- oder [!UICONTROL Custom Goals] Spalten; Werbetreibende nur mit Adobe Advertising-Konversionsverfolgung) Wie kann innerhalb des Berichts die Konversionsdaten in einer Ereignisreihe zugeordnet werden, die zu einer Konversion führt:

   * *[!UICONTROL Unique]:* (Standard) Zählt, wie oft ein Dimensionswert (z. B. ein Gerät oder eine Platzierung) auf dem Konversionspfad war.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Verteilt die Gewichtung jeder Konversion auf Basis der Häufigkeit des Auftretens des Dimensionswerts (z. B. eines Geräts oder einer Platzierung) auf dem Konversionspfad. Wenn beispielsweise vor der Konversion insgesamt 10 Impressions vorhanden waren, davon 8 auf CTV und 2 auf Mobile, werden 80 % der Credits (0,8) auf CTV-Bildschirme und 0,2 auf Mobile übertragen.

* **\[Regeltyp\]:** (Alle [!UICONTROL Custom]-, [!UICONTROL Conversion]-, [!UICONTROL Device]-, [!UICONTROL Geo]-, [!UICONTROL Segment]- und [!UICONTROL Site]-Berichte mit [!UICONTROL Conversion Metrics]- oder [!UICONTROL Custom Goals]-Spalten; Werbetreibende nur mit Adobe Advertising-Konversionsverfolgung) Im Bericht, wie Konversionsdaten in einer Reihe von Ereignissen zugeordnet werden, die zu einer Konversion führen. Sie können mehr als eine Regel auswählen, wenn Sie die Unterschiede zwischen den Regeln vergleichen möchten.

  >[!NOTE]
  >
  >Konversionspfade umfassen alle Impressionen und Klicks innerhalb der Impressions- oder Lookback-Fenster des Advertisers, die in [!DNL Advertising Search, Social, & Commerce] konfiguriert sind. Klicks werden bei der Konversionszuordnung Impressionen bevorzugt. Alle Klicks in einem Konversionspfad erhalten eine vollständige Gutschrift basierend auf der Attributionsregel. Impressionen werden nur dann gutgeschrieben, wenn im Konversionspfad keine Klicks verfolgt werden.

   * *[!UICONTROL Last Event]:* Attributiert Konversionen dem letzten Klick oder Impression im Konversionspfad.

   * *[!UICONTROL Weight Last More]:* Attributiert Konvertierungen allen Ereignissen im Konvertierungspfad, gewichtet jedoch am meisten das letzte Ereignis und verringert sukzessive die Gewichtung der vorherigen Ereignisse.

   * *[!UICONTROL Even Distribution]:* Attributiert Konversionen gleichmäßig jedem Ereignis im Konversionspfad.

   * *[!UICONTROL Weight First More]:* Attributiert Konvertierungen allen Ereignissen im Konvertierungspfad, gewichtet jedoch das erste Ereignis am meisten und die folgenden Ereignisse nacheinander weniger.

   * *[!UICONTROL First Event]:* Attributiert Konversionen dem ersten Klick oder der ersten Impression im Konversionspfad.

   * *[!UICONTROL U-shaped]:* Ordnet die Konvertierung allen Ereignissen im Konvertierungspfad zu, gewichtet jedoch am meisten das erste und letzte Ereignis, wobei den Ereignissen in der Mitte des Konvertierungspfads nacheinander weniger Gewicht zugewiesen wird.

   * *[!UICONTROL Display Only]:* Attributkonvertierungen auf den letzten DSP-Klick oder die letzte Impression im Konversionspfad. Dazu gehören Video- und vernetzte TV-Anzeigen und Klicks auf [!DNL Advertising Search, Social, & Commerce].

   * *[!UICONTROL Social Only]:* veraltet

Siehe auch [So werden Attributionsregeln für Adobe Advertising berechnet](/help/search-social-commerce/reports/attribution-rules.md).

* **Lookback:** ([!UICONTROL Household Conversion] Berichte mit [!UICONTROL Conversion Metrics]- oder [!UICONTROL Custom Goals]-Spalten und [!UICONTROL Path to Conversion]-, [!UICONTROL Path Length]- oder [!UICONTROL Time to Conversion]-Berichten nur mit [!UICONTROL Conversion Metrics] Spalten; Advertiser nur mit Adobe Advertising-Konversionsverfolgung) Innerhalb des Berichts die maximale Anzahl von Tagen nach einem Impressionsereignis oder einem Klickereignis (für [!UICONTROL Path to Conversion]-, [!UICONTROL Path Length]- oder [!UICONTROL Time to Conversion]-Berichte), in denen ihm ein Konversionsereignis zugeordnet werden kann. Der Standardwert ist *[!UICONTROL 30 days]* und der maximale Wert ist 92 Tage.

  >[!TIP]
  >
  >Wenn Sie [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) verwenden, verwenden Sie dasselbe Lookback-Fenster wie in [!DNL Analytics].

**[!UICONTROL Paths as Columns]:** (Alle [!UICONTROL Custom]-, [!UICONTROL Conversion]-, [!UICONTROL Device]-, [!UICONTROL Geo]-, [!UICONTROL Segment]- und [!UICONTROL Site]-Berichte mit [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals] Spalten) Welche Konversionstypen werden gemeldet, wenn auf demselben Gerät vorhergehende Ereignisse aufgetreten sind? Sie können bis zu drei Typen einschließen. Für jeden ausgewählten Typ ist eine separate Spalte für jede Konversionsmetrik enthalten und mit dem angegebenen Suffix ([!UICONTROL (tl)], [!UICONTROL (ct)] oder [!UICONTROL (vt)]) versehen:

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Umfasst Konversionen, die Klicks (CT für Clickthrough) und Impressionen (VT für View-Through) zugeordnet werden. Konversionen, die Impressionen zugeordnet sind, werden mit der angegebenen Durchsichtsgewichtung multipliziert. Die standardmäßige Durchsichtsgewichtung beträgt 100 %, was bedeutet, dass Konversionen, die Impressionen zugeordnet sind, als 100 % des Werts von Konversionen gezählt werden, die Klicks zugeordnet sind.

* *[!UICONTROL With Clicks (CT)]:* Umfasst nur Konversionen, die Klicks zugeordnet wurden.

* *[!UICONTROL Impressions Only (VT)]:* Enthält nur Konversionen, die Impressionen zugeordnet wurden, da im Konversionspfad keine Klicks verfolgt wurden.

**[!UICONTROL Conversion Reporting Based On]:** So melden Sie Konversionsdaten:

* *[!UICONTROL Conversion Timestamp]:* (Standard) Konversionen sind mit dem Konvertierungsdatum verknüpft.

* *[!UICONTROL Event Timestamp]:* Konversionen werden basierend auf dem Datum der Impression oder des Klicks, die bzw. der die Konvertierung verursacht hat, gemeldet, wie durch die angegebene [!UICONTROL Attribution Rule Settings] bestimmt.

## [!UICONTROL Add Report Destinations]

**[!UICONTROL Destination Type]:** Versand der abgeschlossenen Berichte und Fehlerbenachrichtigungen Sie können den Zieltyp nicht mehr ändern, nachdem Sie den Bericht gespeichert haben.

>[!NOTE]
>
>Sie können fertige Berichte jederzeit über die Ansicht [!UICONTROL Reports] > [!UICONTROL Custom Reports] herunterladen.

* *[!UICONTROL None]:* Es werden keine Berichte oder Benachrichtigungen gesendet.

* *[!UICONTROL S3]:* Um den fertigen Bericht an einen oder mehrere [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) Orte zu senden, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL sFTP]:* Den ausgefüllten Bericht an einen oder mehrere SFTP-Speicherorte zu senden, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL FTP]:* Um den fertigen Bericht an einen oder mehrere FTP-Speicherorte zu senden, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL FTP SSL] (derzeit in Beta):* Senden des ausgefüllten Berichts an einen oder mehrere FTP-SSL-Speicherorte, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL Email]:* Um E-Mail-Adressen anzugeben, an die ausgefüllte Berichte oder Benachrichtigungen gesendet werden sollen, wenn der Bericht aufgrund von Fehlern abgebrochen wird.

**[!UICONTROL Email]:** (Nur E-Mail-Zieltyp) Geben Sie für jede Adresse die Adresse ein und klicken Sie auf **+**.

**[!UICONTROL Destination Name]:** (nur S3-, FTP-, sFTP- und FTP-SSL-Zieltypen) Die Namen der Berichtsziele, an die der benutzerdefinierte Bericht gesendet wird.

* Um ein vorhandenes Ziel anzugeben, wählen Sie einen Zielnamen aus der Liste aus. Sie können mehrere Zielnamen separat auswählen.

* So erstellen Sie ein neues Ziel:

   1. Klicken Sie **Neues Ziel hinzufügen**.

   1. Geben Sie die [Berichtszieleinstellungen](/help/dsp/reports/report-destinations/report-destination-settings.md) ein und klicken Sie auf **Speichern**.

   1. Klicken Sie in den Berichtseinstellungen auf **Zielnamen aktualisieren.**

      Das neue Ziel ist jetzt in der Liste der vorhandenen Ziele verfügbar und Sie können es optional zum Bericht hinzufügen.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Erstellen eines benutzerdefinierten Berichts](/help/dsp/reports/report-create.md)
>* [Duplizieren eines benutzerdefinierten Berichts](/help/dsp/reports/report-copy.md)
>* [Benutzerdefinierten Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Benutzerdefinierten Bericht herunterladen](/help/dsp/reports/report-download.md)
>* [Benutzerdefinierten Bericht ausführen](/help/dsp/reports/report-run-now.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Über Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
