---
title: '[!UICONTROL Custom Creative Report]'
description: Erfahren Sie, wie Sie die erlebnisübergreifende [!UICONTROL Custom Creative Report] generieren.
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '2026'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*Beta-Funktion*

Mit dem [!UICONTROL Custom Creative Report] können Sie den Inhalt und die Bereitstellung von Berichtsdaten für alle Ihre Anzeigenerlebnisse anpassen.

Sie können Berichte einmal generieren oder sie können täglich, wöchentlich oder monatlich um 03 :00 in der angegebenen Zeitzone gemäß den angegebenen Kriterien planen (z. B. alle 15 Tage oder am 1. eines jeden Monats). Nachdem ein Bericht generiert wurde, können Sie ihn von [!UICONTROL Reports] > [!UICONTROL Custom Reports] oder von verknüpften [Berichtszielen](/help/dsp/reports/report-destinations/report-destination-about.md) der folgenden Typen herunterladen:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP-SSL-<!-- (in beta) -->
* SFTP

## Erstellen eines [!UICONTROL Custom Creative Report]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Create]**.

1. Geben Sie die [Berichteinstellungen](#report-settings) an.

1. Klicken Sie auf **[!UICONTROL Create Custom Report]**.

## Berichteinstellungen {#report-settings}

**[!UICONTROL Name]:** Der Berichtsname. Die maximale Länge beträgt 180 Zeichen.

**[!UICONTROL Report Type]:** Der Berichtstyp: *[!UICONTROL Custom Creative Beta]*.

### [!UICONTROL Report Range]

In diesem Abschnitt werden die Daten festgelegt, die im Bericht enthalten sind. Informationen zum Einrichten von Datumsangaben für den Berichtsplan finden Sie im Abschnitt &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** Die Zeitzone für das Reporting.

**[!UICONTROL Observe Daylight Savings Time]:** Berücksichtigt die Sommerzeit in den gemeldeten Zeiten.

**Range:** Der Datumsbereich, für den Daten generiert werden sollen. Die Anzahl der verfügbaren Tage variiert je nach Bericht und den ausgewählten Dimensionen. Eine Option auswählen:

* **[!UICONTROL Previous Calendar Week]:** Enthält Daten zur vorherigen Kalenderwoche.

* **[!UICONTROL Previous Calendar Month]:** Enthält Daten für den vorherigen Kalendermonat.

* **[!UICONTROL Custom Range]:** Schließt Daten zwischen einem bestimmten Anfangs- und Enddatum ein. Um Daten über den Vortag zu melden, wählen Sie **[!UICONTROL Present]** aus.

### [!UICONTROL Report Run schedule]

In diesem Abschnitt werden die Daten festgelegt, an denen der Bericht ausgeführt wird. Informationen zum Einrichten der Datumsangaben, für die Berichtsdaten einbezogen werden sollen, finden Sie im Abschnitt &quot;[!UICONTROL Report range]&quot;.

**\[schedule\]:** Zeitpunkt für die Berichterstellung:

* *[!UICONTROL Immediately]*: Fügt den Bericht sofort der Berichtswarteschlange hinzu.

  >[!NOTE]
  >
  >Sie können auch [einen benutzerdefinierten Bericht jederzeit ausführen](/help/dsp/reports/report-run-now.md) über die [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;date\>:* Führt den Bericht an einem bestimmten Datum (bis 09) :00 der Zeitzone des Kontos aus.

* *[!UICONTROL Recurring]:* Führt den Bericht nach einem Zeitplan für einen bestimmten Zeitraum aus.

   * **\[schedule\]:** Wie oft der Bericht ausgeführt wird:

      * *Täglich* um den Bericht alle N Tage auszuführen. Wenn der Bericht beispielsweise alle zwei Wochen (14 Tage) ausgeführt werden soll, wählen Sie diese Option aus und geben Sie **14** ein.

      * *Wöchentlich* um den Bericht an bestimmten Wochentagen auszuführen. Wenn Sie beispielsweise den Bericht montags und freitags ausführen möchten, wählen Sie diese Option aus und aktivieren Sie die Kontrollkästchen neben **Montag** und **Freitag**.

      * *Monatlich* um den Bericht an einem bestimmten numerischen Tag des Monats von 1 bis 30 auszuführen. Wenn der Bericht beispielsweise am ersten Tag jedes Monats ausgeführt wird, wählen Sie diese Option und geben Sie **1** ein.

   * **Von**: Das erste Datum, an dem der Bericht ausgeführt werden kann. Je nach angegebenem Zeitplan kann die erste Berichtsinstanz nach diesem Datum auftreten.

   * **Bis**: Das Ablaufdatum des Berichts, das bis zu vier Kalendermonate entfernt sein kann. Bevor ein Bericht abläuft, erhalten alle angegebenen E-Mail-Ziele sieben Tage und einen Tag vor dem Ablaufdatum einen E-Mail-Warnhinweis. Um den Bericht länger zu halten, ändern Sie dieses Datum.

### [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (Optional) Zusätzliche Dimensionen, nach denen die Daten gefiltert werden sollen, unabhängig davon, ob die Dimensionen als Spalten im Bericht enthalten sind oder nicht. Die verfügbaren Filter variieren je nach Berichtstyp und können *[!UICONTROL Advertiser]*, *[!UICONTROL Experience]*, *[!UICONTROL Creative Library]* und *[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->umfassen.

Gehen Sie wie folgt vor, um einen oder mehrere Filter anzuwenden:

* Wählen Sie eine Dimension aus, wählen Sie den Operator *gleich* oder *nicht gleich* aus und wählen Sie dann den entsprechenden Wert aus. Um beispielsweise Daten nur für Preroll-Anzeigen zurückzugeben, geben Sie &quot;[!UICONTROL Ad Type equals Preroll]&quot; an.
* (Optional) Fügen Sie dem Filter zusätzliche Kriterien hinzu.
* (Optional) Fügen Sie zusätzliche Filter hinzu, die jeweils ein oder mehrere Kriterien aufweisen.

### [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** Die Datenspalten oder Kopfzeilen, die in den Bericht aufgenommen werden sollen. Um eine Spalte hinzuzufügen, erweitern Sie die Kategorie und aktivieren Sie das Kontrollkästchen neben dem Spaltennamen. Die verfügbaren Spalten variieren je nach Bericht, und alle nicht verfügbaren Metriken sind deaktiviert. Beschreibungen [ Optionen finden Sie unter „Verfügbare ](#report-custom-creative-columns)&quot;.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Die Reihenfolge der Spaltenüberschriften. Sie können eine beliebige Spalte per Drag-and-Drop verschieben, um die Reihenfolge anzupassen.

**[!UICONTROL Format]:**, ob ein Bericht im *[!UICONTROL CSV]*-Format (kommagetrennte Werte) oder im *[!UICONTROL Tab]*-Format (tabulatorgetrennte Werte) generiert werden soll.

**[!UICONTROL Headers]:** Gibt an, ob Spaltenüberschriften *[!UICONTROL Include]* oder *[!UICONTROL Do Not Include]* werden.

### [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Die Einstellungen variieren je nach Berichtstyp:

* **\[Attributionstyp\]:** (Nur Werbetreibende mit Adobe Advertising-Konversionsverfolgung) Wie können innerhalb des Berichts Konversionsdaten in einer Ereignisreihe zugeordnet werden, die zu einer Konversion führt:

   * *[!UICONTROL Unique]:* (Standard) Zählt, wie oft ein Dimensionswert (z. B. ein Gerät oder eine Platzierung) auf dem Konversionspfad war.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Verteilt die Gewichtung jeder Konversion auf Basis der Häufigkeit des Auftretens des Dimensionswerts (z. B. eines Geräts oder einer Platzierung) auf dem Konversionspfad. Wenn beispielsweise vor der Konversion insgesamt 10 Impressions vorhanden waren, davon 8 auf CTV und 2 auf Mobile, werden 80 % der Credits (0,8) auf CTV-Bildschirme und 0,2 auf Mobile übertragen.

* **\[Regeltyp\]:** (Nur Werbetreibende mit Adobe Advertising-Konversionsverfolgung) Im Bericht, wie Konversionsdaten in einer Ereignisreihe zugeordnet werden, die zu einer Konversion führen. Sie können mehr als eine Regel auswählen, wenn Sie die Unterschiede zwischen den Regeln vergleichen möchten.

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

**[!UICONTROL Paths as Columns]:** Welche Konversionstypen gemeldet werden sollen, wenn auf demselben Gerät frühere Ereignisse aufgetreten sind. Sie können bis zu drei Typen einschließen. Für jeden ausgewählten Typ ist eine separate Spalte für jede Konversionsmetrik enthalten und mit dem angegebenen Suffix ([!UICONTROL (tl)], [!UICONTROL (ct)] oder [!UICONTROL (vt)]) versehen:

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Umfasst Konversionen, die Klicks (CT für Clickthrough) und Impressionen (VT für View-Through) zugeordnet werden. Konversionen, die Impressionen zugeordnet sind, werden mit der angegebenen Durchsichtsgewichtung multipliziert. Die standardmäßige Durchsichtsgewichtung beträgt 100 %, was bedeutet, dass Konversionen, die Impressionen zugeordnet sind, als 100 % des Werts von Konversionen gezählt werden, die Klicks zugeordnet sind.

* *[!UICONTROL With Clicks (CT)]:* Umfasst nur Konversionen, die Klicks zugeordnet wurden.

* *[!UICONTROL Impressions Only (VT)]:* Enthält nur Konversionen, die Impressionen zugeordnet wurden, da im Konversionspfad keine Klicks verfolgt wurden.

### [!UICONTROL Add Report Destinations]

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

**[!UICONTROL Destination Name]:** (nur S3-, FTP-, sFTP- und FTP-SSL-Zieltypen) Die Namen der [Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} an die der benutzerdefinierte Bericht gesendet wird.

* Um ein vorhandenes Ziel anzugeben, wählen Sie einen Zielnamen aus der Liste aus. Sie können mehrere Zielnamen separat auswählen.

* So erstellen Sie ein neues Ziel:

   1. Klicken Sie **Neues Ziel hinzufügen**.

   1. Geben Sie die [Berichtszieleinstellungen](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} ein und klicken Sie auf **Speichern**.

   1. Klicken Sie in den Berichtseinstellungen auf **Zielnamen aktualisieren.**

      Das neue Ziel ist jetzt in der Liste der vorhandenen Ziele verfügbar und Sie können es optional zum Bericht hinzufügen.

## Verfügbare Berichtsspalten {#report-custom-creative-columns}

| Metriktyp | Untertyp | Spaltenname | Beschreibung |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | Die Dimensionen der veröffentlichten Anzeige. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | Ob es sich bei der geschalteten Anzeige um eine Standardbildanzeige oder Videoanzeige für das Erlebnis handelte. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | Ob Anzeigen algorithmisch (*algorithmisch*), in einer bestimmten Sequenz (*sequenziert*) oder nach relativen Gewichtungen (*gewichtet*) gedreht wurden. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | Die ID, die dem Kreativen zugewiesen [!UICONTROL Creative]. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | Der Name des Kreativen. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | Der Typ des Kreativen (z. B. [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | Die ID, die dem übergeordneten Kreativen zugewiesen [!UICONTROL Creative]. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | Der Name des übergeordneten Kreativen. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | Der Typ des übergeordneten Kreativen (z. B. [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | Die Landingpage-URL. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | Der spezifische Typ der Benutzerinteraktion. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | Der gerichtete Fluss- oder Navigationspfad der Klickinteraktion des Benutzers innerhalb des kreativen Erlebnisses. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | Der Browser, in dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Chrome] oder [!UICONTROL Firefox]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | Das Betriebssystem, auf dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Windows]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | Der Typ des Geräts, auf dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Desktop]). |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | Der Name der DSP, auf der Anzeigen ausgeführt wurden. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | Die ID der Platzierung, für die Anzeigen ausgeführt wurden. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | Der Name der Platzierung, für die Anzeigen ausgeführt wurden. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | Die ID der Site, auf der Anzeigen ausgeführt wurden. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | Der Name der Site, auf der Anzeigen ausgeführt wurden. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | Die ID, die dem Anzeigen-Erlebnis-Tag zugewiesen [!UICONTROL Creative]. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | Der Name des Werbetreibenden. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | Datum und Uhrzeit des Ereignisses. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | Die ID, die dem Erlebnis zugewiesen [!UICONTROL Creative]. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | Der Name des Erlebnisses. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | Der spezifische Pfad durch den Entscheidungsbaum für die Zielgruppenbestimmung, der bestimmt, welche kreative Erlebnisvariante dem Benutzer bzw. der Benutzerin bereitgestellt wurde. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | Der Name des Anzeigen-Tags. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | Die Stadt, der die gemeldeten Daten zugeordnet sind. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | Der Ländercode für das Land, dem die gemeldeten Daten zugeordnet sind. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | Das Designated Market Area (DMA), dem die gemeldeten Daten zugeordnet werden. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | Der Status-Code für den Status, dem die gemeldeten Daten zugeordnet sind. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | Die Postleitzahl, der die gemeldeten Daten zugeordnet werden. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | (Dynamische Anzeigen) Die ID der Zielproduktkategorie. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | (Dynamische Anzeigen) Der Name der Zielproduktkategorie. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | (Dynamische Anzeigen) Das erste kreative Attribut. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | (Dynamische Anzeigen) Das zweite kreative Attribut. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | (Dynamische Anzeigen) Das dritte kreative Attribut. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | (Dynamische Anzeigen) Das vierte kreative Attribut. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | (Dynamische Anzeigen) Das fünfte kreative Attribut. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | (Dynamische Anzeigen) Die Zielprodukt-ID. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | (Dynamische Anzeigen) Der Name des Zielprodukts. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | Die IDs für bis zu fünf Benutzersegmente, die mit dem Anzeigendesign übereinstimmen. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | Die ID für ein Retargeting-Pixel, dem die gemeldeten Daten zugewiesen werden. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | Der Name eines Retargeting-Pixels, dem die gemeldeten Daten zugeordnet werden. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | Die Attribute für ein Zielgruppensegment, dem die gemeldeten Daten zugeordnet sind. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | Die Summe aller Klicks auf eine Anzeige. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | Die Klickrate, d. h. der Prozentsatz der Klicks dividiert durch die Ad-Impressions. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | Der Prozentsatz der bereitgestellten Impressionen, die zu Benutzerinteraktionen geführt haben. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | Die Anzahl der Interaktionen auf einer geschalteten Anzeige. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | Die Gesamtzahl der Anzeigen-Impressions. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | Der Prozentsatz der Impressionen mit einem Cookie für die erneute Zielgruppenbestimmung. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | (Nur dynamische Anzeigen) Die Summe aller Klicks auf Anzeigen für ein Produkt. Wenn das Produkt null ist, ist dieser Wert null (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | (Nur dynamische Anzeigen) Die Summe aller Konversionen auf Anzeigen für ein Produkt. Wenn das Produkt null ist, ist dieser Wert null (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | (Nur dynamische Anzeigen) Der Prozentsatz der Anzeigen für ein Produkt, die zu Konversionen geführt haben. Wenn das Produkt null ist, ist dieser Wert null (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | (Nur dynamische Anzeigen) Die Clickthrough-Rate für Anzeigen für ein Produkt, d. h. der Prozentsatz der Klicks dividiert durch die Anzeigenimpressionen. Wenn das Produkt null ist, ist dieser Wert null (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | (Nur dynamische Anzeigen) Die Gesamtzahl der Impressionen für ein Produkt. Wenn das Produkt null ist, ist dieser Wert null (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | (Nur dynamische Anzeigen) Der Gesamtumsatz der geschalteten Anzeigen für ein Produkt. Wenn das Produkt null ist, ist dieser Wert null (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | Die Gesamteinnahmen aus geschalteten Anzeigen. |
| [!UICONTROL Conversion Metrics] | [Gruppiert nach Advertiser in den Berichteinstellungen] | [Advertiser-spezifische Konversion] | Die Gesamtsumme für eine bestimmte Advertiser-spezifische Konversionsmetrik oder ein Adobe Analytics-Ereignis. |
| [!UICONTROL Custom Goals] | [Gruppiert nach Advertiser in den Berichteinstellungen] | [Advertiser-spezifisches benutzerdefiniertes Ziel] | (Werbetreibende mit Advertising DSP) Die gewichtete Summe aller Konversionen, die im angegebenen benutzerdefinierten Ziel [Advertising DSP enthalten sind](/help/dsp/optimization/custom-goal.md). |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Leistungsberichte auf Erlebnisebene](/help/creative/experiences/experience-performance-details.md)
>* [Über benutzerdefinierte Berichte in DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [Über [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
