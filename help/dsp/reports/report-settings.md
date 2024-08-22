---
title: Benutzerdefinierte Berichtseinstellungen
description: Siehe Beschreibungen der benutzerdefinierten Berichtseinstellungen.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 4fb843e66edddd4585d4a9b142eb9a7750152d27
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 0%

---

# Benutzerdefinierte Berichtseinstellungen

**[!UICONTROL Name]:** Der Berichtsname. Die maximale Länge beträgt 180 Zeichen.

**[!UICONTROL Report Type]:** Der Berichtstyp: *[!UICONTROL Custom]* (der die meisten verfügbaren Optionen enthält), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]* oder *[!UICONTROL Household Conversions]*.

## [!UICONTROL Report Range] Abschnitt

Dieser Abschnitt bestimmt die Daten, die im Bericht enthalten sind. Informationen zum Einrichten von Datumsangaben für den Berichtsplan finden Sie im Abschnitt &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** Die Zeitzone für die Berichterstellung.

**[!UICONTROL Observe Daylight Savings Time]:** Betrachtet die Sommerzeit in den gemeldeten Zeiten.

**Bereich:** Der Datumsbereich, für den Daten generiert werden sollen. Die Anzahl der Tage variiert je nach Bericht und ausgewählten Dimensionen. Wählen Sie eine aus:

* **[!UICONTROL Last Calendar Week]:** Umfasst Daten für die vorherige Kalenderwoche.

* **[!UICONTROL Last Calendar Month]:** Umfasst Daten für den vorherigen Kalendermonat.

* **[!UICONTROL Custom Range]:** Umfasst Daten zwischen bestimmten Start- und Enddaten. Um Daten über den vorherigen Tag zu berichten, wählen Sie **[!UICONTROL Present]** aus.

## [!UICONTROL Report Run schedule] Abschnitt

In diesem Abschnitt werden die Daten festgelegt, zu denen der Bericht ausgeführt wird. Informationen zum Einrichten der Datumswerte, für die Berichtsdaten einbezogen werden sollen, finden Sie im Abschnitt &quot;[!UICONTROL Report range]&quot;.

**\[Zeitplan\]:** Wann der Bericht generiert werden soll:

* *[!UICONTROL Immediately]*: Hiermit wird der Bericht sofort zur Berichtswarteschlange hinzugefügt.

  >[!NOTE]
  >
  >Sie können auch [ einen benutzerspezifischen Bericht jederzeit ausführen](report-run-now.md) aus der [!UICONTROL Reports]-Ansicht.

* *[!UICONTROL On]\&lt;Datum\>:* Führt den Bericht an einem bestimmten Datum aus, um 09:00 Uhr in der Zeitzone des Kontos abgeschlossen zu sein.

* *[!UICONTROL Recurring]:* Führt den Bericht gemäß einem Zeitplan während eines bestimmten Zeitraums aus.

   * **\[Zeitplan\]:** Wie oft der Bericht ausgeführt wird:

      * *Täglich* verwenden, um den Bericht alle N Tage auszuführen. Wenn Sie den Bericht beispielsweise alle zwei Wochen (14 Tage) ausführen möchten, wählen Sie diese Option aus und geben Sie **14** ein.

      * *Wöchentlich* , um den Bericht an bestimmten Wochentagen auszuführen. Um den Bericht beispielsweise jeden Montag und Freitag auszuführen, wählen Sie diese Option aus und aktivieren Sie die Kontrollkästchen neben **Montag** und **Freitag**.

      * *Monatlich* , um den Bericht an einem bestimmten numerischen Tag des Monats von 1 bis 30 auszuführen. Beispiel: Wenn Sie den Bericht am ersten Tag eines jeden Monats ausführen, wählen Sie diese Option aus und geben Sie **1** ein.

   * **Von**: Das erste Datum, an dem der Bericht ausgeführt werden kann. Je nach festgelegtem Zeitplan kann die erste Berichtsinstanz nach diesem Datum auftreten.

   * **Bis**: Das Ablaufdatum des Berichts, das bis zu vier Kalendermonate entfernt sein kann. Bevor ein Bericht abläuft, erhalten alle angegebenen E-Mail-Ziele sieben Tage und einen Tag vor dem Ablaufdatum einen E-Mail-Warnhinweis. Um den Bericht länger zu halten, ändern Sie dieses Datum.

## [!UICONTROL Apply Filters] Abschnitt

**[!UICONTROL Add Filters]:** (Optional) Zusätzliche Dimensionen, anhand derer die Daten gefiltert werden können, unabhängig davon, ob die Dimensionen als Spalten im Bericht enthalten sind oder nicht. Die verfügbaren Filter variieren je nach Berichtstyp und können Folgendes umfassen: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* und *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* ist für die folgenden Berichtstypen nur verfügbar, wenn Ihr Unternehmen für [kontoübergreifende Berichte](report-about.md#cross-account-reporting) konfiguriert ist: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] und [!UICONTROL Conversion]. Wenden Sie sich an Ihr Adobe-Account-Team, um weitere Informationen zur kontoübergreifenden Berichterstellung zu erhalten.

Gehen Sie wie folgt vor, um einen oder mehrere Filter anzuwenden:

* Wählen Sie eine Dimension aus, wählen Sie den Operator (*gleich* oder *nicht gleich*) und wählen Sie dann den entsprechenden Wert aus. Wenn Sie beispielsweise nur Daten für Pre-oll-Anzeigen zurückgeben möchten, geben Sie &quot;[!UICONTROL Ad Type equals Preroll]&quot;an.
* (Optional) Fügen Sie dem Filter zusätzliche Kriterien hinzu.
* (Optional) Fügen Sie zusätzliche Filter hinzu, von denen jeder ein oder mehrere Kriterien aufweist.

## [!UICONTROL Build Your Report] Abschnitt

**[!UICONTROL Select To Add As Report Headers]:** Die Datenspalten oder Kopfzeilen, die in den Bericht aufgenommen werden sollen. Um eine Spalte hinzuzufügen, erweitern Sie die Kategorie und aktivieren Sie das Kontrollkästchen neben dem Spaltennamen. Die verfügbaren Spalten variieren je nach Bericht, und alle nicht verfügbaren Metriken sind deaktiviert. Zu den verfügbaren Datenkategorien gehören:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Der Bericht [!UICONTROL Household Reach & Frequency] kann nur eine Dimension enthalten.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Der Bericht [!UICONTROL Household Reach & Frequency] kann entweder Metriken mit Überschneidungen oder Metriken ohne Überlappung enthalten, nicht aber beides.

* [!UICONTROL Conversion Metrics] (sortiert nach Advertiser)

* [!UICONTROL Custom Goals] (sortiert nach Advertiser)

Beschreibungen aller Optionen finden Sie unter &quot;[Verfügbare Berichtsspalten](report-columns.md)&quot;.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Die Reihenfolge der Spaltenüberschriften. Sie können jede Spalte per Drag-and-Drop verschieben, um die Reihenfolge anzupassen.

**[!UICONTROL Format]:** Gibt an, ob ein Bericht im Format *[!UICONTROL CSV]* (kommagetrennte Werte) oder *[!UICONTROL Tab]* (tabulatorgetrennte Werte) erstellt werden soll.

**[!UICONTROL Headers]:** Gibt an, ob die Spaltenüberschriften *[!UICONTROL Include]* oder *[!UICONTROL Do Not Include]* lauten sollen.

## [!UICONTROL Multi-Touch Conversion Options] Abschnitt

**[!UICONTROL Attribution Rule Settings]:** Die Einstellungen variieren je nach Berichtstyp:

* **\[Attributionstyp\]:** ([!UICONTROL Household Conversion] Berichte mit den Spalten [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals]; Werbetreibende mit Adobe Advertising-Konversions-Tracking) Wie werden im Bericht Konversionsdaten in einer Reihe von Ereignissen zugeordnet, die zu einer Konversion führen:

   * *[!UICONTROL Unique]:* (Der Standardwert) Zählt, wie oft sich ein Dimensionswert (z. B. ein Gerät oder eine Platzierung) auf dem Weg zur Konversion befand.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Verteilt die Gutschrift jeder Konversion basierend auf der Häufigkeit des Auftretens des Dimensionswerts (z. B. ein Gerät oder eine Platzierung) auf dem Pfad zur Konversion. Wenn es beispielsweise insgesamt 10 Impressionen vor der Konvertierung gab, mit 8 bei CTV und 2 bei Mobile, werden 80 % der Gewichtung (0,8) an CTV-Bildschirme und 0,2 an Mobile vergeben.

* **\[Regeltyp\]:** (Alle [!UICONTROL Custom]-, [!UICONTROL Conversion]-, [!UICONTROL Device]-, [!UICONTROL Geo]-, [!UICONTROL Segment]- und [!UICONTROL Site]-Berichte mit den Spalten [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals]; Werbetreibende mit nur Adobe Advertising-Konversions-Tracking) Wie werden im Bericht Konversionsdaten in einer Reihe von Ereignissen zugeordnet, die zu einer Konversion führen? Sie können mehrere Regeln auswählen, wenn Sie Unterschiede zwischen den Regeln vergleichen möchten.

  >[!NOTE]
  >
  >Konversionspfade umfassen alle Impressionen und Klicks innerhalb der Impressions- oder Klick-Lookback-Fenster des Advertisers, die in [!DNL Advertising Search, Social, & Commerce] konfiguriert sind. Klicks erhalten während der Konversionszuordnung Vorrang vor Impressionen. Alle Klicks in einem Konversionspfad erhalten die volle Gutschrift auf der Grundlage der Attributionsregel. Impressionen erhalten nur dann eine Gutschrift, wenn im Konversionspfad keine Klicks verfolgt werden.

   * *[!UICONTROL Last Event]:* Ordnet Konversionen dem letzten Klick oder der letzten Impression im Konversionspfad zu.

   * *[!UICONTROL Weight Last More]:* Ordnet allen Ereignissen im Konversionspfad Konversionen zu, gibt jedoch dem letzten Ereignis die höchste Gewichtung und den vorhergehenden Ereignissen eine schrittweise geringere Gewichtung zu.

   * *[!UICONTROL Even Distribution]:* Ordnet Konversionen jedem Ereignis im Konversionspfad zu.

   * *[!UICONTROL Weight First More]:* Ordnet allen Ereignissen im Konversionspfad Konversionen zu, gibt jedoch dem ersten Ereignis die höchste Gewichtung und den folgenden Ereignissen eine schrittweise geringere Gewichtung zu.

   * *[!UICONTROL First Event]:* Ordnet Konversionen dem ersten Klick oder der ersten Impression im Konversionspfad zu.

   * *[!UICONTROL U-shaped]:* Ordnet die Konversion allen Ereignissen im Konversionspfad zu, gibt jedoch dem ersten und letzten Ereignis die höchste Gewichtung zu, wobei die Ereignisse in der Mitte des Konversionspfads nach und nach weniger berücksichtigt werden.

   * *[!UICONTROL Display Only]:* Ordnet Konversionen dem letzten DSP Klick oder Impression im Konversionspfad zu. Dazu gehören Video- und verbundene TV-Anzeigen sowie Klicks auf [!DNL Advertising Search, Social, & Commerce] -Anzeigen.

   * *[!UICONTROL Social Only]:* veraltet

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **Lookback:** ([!UICONTROL Household Conversion] Berichte mit den Spalten [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals]; Advertiser mit Adobe Advertising-Konversions-Tracking) Im Bericht wird die maximale Anzahl von Tagen nach einem Impressionsereignis angegeben, in denen ein Konversionsereignis zugeordnet werden kann. Der Standardwert ist *[!UICONTROL 30 days]* und der Höchstwert beträgt 92 Tage.

**[!UICONTROL Paths as Columns]:** (Alle [!UICONTROL Custom]-, [!UICONTROL Conversion]-, [!UICONTROL Device]-, [!UICONTROL Geo]-, [!UICONTROL Segment]- und [!UICONTROL Site]-Berichte mit den Spalten [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals]) Welche Konversionstypen werden in Berichten aufgeführt, wenn frühere Ereignisse auf demselben Gerät aufgetreten sind. Sie können bis zu drei Typen einbeziehen. Für jeden ausgewählten Typ wird eine separate Spalte für jede Konversionsmetrik eingefügt und dem angegebenen Suffix ([!UICONTROL (tl)], [!UICONTROL (ct)] oder [!UICONTROL (vt)]) angehängt:

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Umrechnungen, die Klicks (CT für Clickthrough) und Impressionen (VT für Durchsicht) zugeordnet sind. Auf Impressionen zugeordnete Konversionen werden mit der angegebenen Durchsichtsgewichtung multipliziert. Die standardmäßige Durchsichtsgewichtung beträgt 100 %, d. h. Konversionen, die Impressionen zugeordnet werden, werden als 100 % des Werts der Konversionen gezählt, die den Klicks zugeordnet sind.

* *[!UICONTROL With Clicks (CT)]:* Umfasst nur Konversionen, die Klicks zugeordnet sind.

* *[!UICONTROL Impressions Only (VT)]:* Umfasst nur Konversionen, die Impressionen zugeordnet wurden, da im Konversionspfad keine Klicks verfolgt wurden.

**[!UICONTROL Conversion Reporting Based On]:** So melden Sie Konversionsdaten:

* *[!UICONTROL Conversion Timestamp]:* (Die Standardeinstellung) Konversionen sind mit dem Konvertierungsdatum verknüpft.

* *[!UICONTROL Event Timestamp]:* Konversionen werden basierend auf dem Datum der Impression oder des Klicks gemeldet, die die Konversion verursacht haben, wie durch den angegebenen [!UICONTROL Attribution Rule Settings] bestimmt.

## [!UICONTROL Add Report Destinations] Abschnitt

**[!UICONTROL Destination Type]:** Wo sollen die abgeschlossenen Berichte und Fehlerbenachrichtigungen bereitgestellt werden? Sie können den Zieltyp nach dem Speichern des Berichts nicht mehr ändern.

>[!NOTE]
>
>Sie können abgeschlossene Berichte immer über die Ansicht [!UICONTROL Reports] > [!UICONTROL Custom Reports] herunterladen.

* *[!UICONTROL None]:* So stellen Sie keine Berichte oder Benachrichtigungen bereit.

* *[!UICONTROL S3]:* Um den abgeschlossenen Bericht an einen oder mehrere [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) Stellen zu senden, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL sFTP]:* Zum Senden des abgeschlossenen Berichts an einen oder mehrere SFTP-Speicherorte, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL FTP]:* Zum Senden des abgeschlossenen Berichts an einen oder mehrere FTP-Speicherorte, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL FTP SSL](Aktuell in Beta):* Senden des abgeschlossenen Berichts an einen oder mehrere FTP-SSL-Speicherorte, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL Email]:* Geben Sie die E-Mail-Adresse(n) an, an die abgeschlossene Berichte oder Benachrichtigungen gesendet werden sollen, wenn der Bericht aufgrund von Fehlern abgebrochen wird.

**[!UICONTROL Email]:** (Nur E-Mail-Zieltyp) Geben Sie für jede Adresse die Adresse ein und klicken Sie auf **+**.

**[!UICONTROL Destination Name]:** (Nur S3-, FTP-, sFTP- und FTP-SSL-Zieltypen) Die Namen der Berichtsziele, an die der benutzerdefinierte Bericht gesendet wird.

* Um ein vorhandenes Ziel anzugeben, wählen Sie einen Zielnamen aus der Liste aus. Sie können mehrere Zielnamen separat auswählen.

* So erstellen Sie ein neues Ziel:

   1. Klicken Sie auf **Neues Ziel hinzufügen**.

   1. Geben Sie die [Berichtsziel-Einstellungen](/help/dsp/reports/report-destinations/report-destination-settings.md) ein und klicken Sie auf **Speichern**.

   1. Klicken Sie in den Berichtseinstellungen auf **Zielnamen aktualisieren.**

      Das neue Ziel ist jetzt in der Liste der vorhandenen Ziele verfügbar und Sie können es optional zum Bericht hinzufügen.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Benutzerspezifischen Bericht duplizieren](/help/dsp/reports/report-copy.md)
>* [Benutzerspezifischen Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Einen benutzerspezifischen Bericht herunterladen](/help/dsp/reports/report-download.md)
>* [Ausführen eines benutzerspezifischen Berichts](/help/dsp/reports/report-run-now.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Über Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
