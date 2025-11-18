---
title: Verwalten benutzerdefinierter Berichte
description: Erfahren Sie, wie Sie die erlebnisübergreifende [!UICONTROL Custom Creative Report] generieren und verwalten.
feature: Creative Reporting
source-git-commit: 41b8d295436bdbe6cea402e5bb234caa7a36f4df
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

Sie können benutzerdefinierte Berichte erstellen, duplizieren, bearbeiten, ausführen, herunterladen und löschen.

## Erstellen eines benutzerdefinierten Berichts {#report-create}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Create]**.

1. Geben Sie die [Berichteinstellungen](#report-settings) an.

1. Klicken Sie auf **[!UICONTROL Create Custom Report]**.

## Duplizieren eines benutzerdefinierten Berichts

Duplizieren Sie einen benutzerdefinierten Bericht, um einen neuen Bericht mit ähnlichen Einstellungen zu erstellen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Klicken Sie neben dem Berichtsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Copy]**.

1. (Optional) Bearbeiten Sie die [Berichteinstellungen](#report-settings.md) nach Bedarf.

   Der Berichtsname ist standardmäßig &quot;\&lt;*vorhandener Berichtsname*\> \#2“ (oder die nächste Nummer in der Sequenz).

## Benutzerdefinierten Bericht bearbeiten {#report-edit}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Klicken Sie neben dem Berichtsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Berichteinstellungen](#report-settings.md).

1. Klicken Sie auf **[!UICONTROL Edit Custom Report]**.

## Benutzerdefinierten Bericht ausführen {#report-run-now}

Sie können alle Berichte ausführen, die noch nicht abgelaufen sind und derzeit nicht ausgeführt werden.

>[!NOTE]
>
>Sie können einen benutzerdefinierten Bericht auch ausführen, wenn Sie [ erstellen](#report-create) oder [bearbeiten](#report-edit).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Klicken Sie neben dem Berichtsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Run Now]**.

   Wenn der Bericht abgeschlossen ist, wird er an die in den Berichtseinstellungen angegebenen Ziele gesendet.

## Benutzerdefinierten Bericht herunterladen

Sie können eine beliebige abgeschlossene Berichtsinstanz aus den letzten vier Monaten herunterladen, die den Status &quot;[!UICONTROL Ready to Download]&quot; oder &quot;[!UICONTROL Completed]&quot; aufweist.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Führen Sie in der Spalte [!UICONTROL Download Report] für die Berichtszeile die folgenden Schritte aus:

   * Um die neueste Instanz des Berichts herunterzuladen, klicken Sie auf **[!UICONTROL Download]**.

   * (Berichte mit mehreren Instanzen) Klicken Sie auf ![Abwärtspfeil](/help/dsp/assets/chevron-down.png " Abwärtspfeil") neben [!UICONTROL Download] und klicken Sie dann auf das Abschlussdatum für den Bericht, den Sie herunterladen möchten. Herunterladbare Berichtsinstanzen werden mit einem Download-Symbol gekennzeichnet (![Download-Symbol](/help/dsp/assets/indicator-downloadable.png "Download-Symbol")).

     Wenn viele Instanzen verfügbar sind, klicken Sie bei Bedarf unten in der Liste auf **[!UICONTROL Load More]** .

     Wenn ein Bericht am selben Tag mehrmals ausgeführt wird, werden die Berichtsinstanzen für diesen Tag in chronologischer Reihenfolge aufgelistet, wobei die neueste Instanz oben aufgeführt wird.

     Fehlgeschlagene Berichtsaufträge werden mit einem Fehlersymbol gekennzeichnet (![Fehleranzeige](/help/dsp/assets/indicator-critical.png " Fehleranzeige")) und können nicht heruntergeladen werden. Eine Beschreibung des Fehlers finden Sie, indem Sie den Cursor über das Fehlersymbol halten.

## Benutzerdefinierten Bericht löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Klicken Sie neben dem Berichtsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Berichteinstellungen {#report-settings}

**[!UICONTROL Name]:** Der Berichtsname. Die maximale Länge beträgt 180 Zeichen.

**[!UICONTROL Report Type]:** Der Berichtstyp.

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
  >Sie können auch [einen benutzerdefinierten Bericht jederzeit ausführen](#report-run-now) über die [!UICONTROL Reports].

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

**[!UICONTROL Select To Add As Report Headers]:** Die Datenspalten oder Kopfzeilen, die in den Bericht aufgenommen werden sollen. Um eine Spalte hinzuzufügen, erweitern Sie die Kategorie und aktivieren Sie das Kontrollkästchen neben dem Spaltennamen. Die verfügbaren Spalten variieren je nach Bericht, und alle nicht verfügbaren Metriken sind deaktiviert.<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Die Reihenfolge der Spaltenüberschriften. Sie können eine beliebige Spalte per Drag-and-Drop verschieben, um die Reihenfolge anzupassen.

**[!UICONTROL Format]:**, ob ein Bericht im *[!UICONTROL CSV]*-Format (kommagetrennte Werte) oder im *[!UICONTROL Tab]*-Format (tabulatorgetrennte Werte) generiert werden soll.

**[!UICONTROL Headers]:** Gibt an, ob Spaltenüberschriften *[!UICONTROL Include]* oder *[!UICONTROL Do Not Include]* werden.

### [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Die Einstellungen variieren je nach Berichtstyp:

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

* *[!UICONTROL FTP SSL](derzeit in Beta):* Senden des ausgefüllten Berichts an einen oder mehrere FTP-SSL-Speicherorte, die Sie im Feld **[!UICONTROL Destination Name]** auswählen müssen.

* *[!UICONTROL Email]:* Um E-Mail-Adressen anzugeben, an die ausgefüllte Berichte oder Benachrichtigungen gesendet werden sollen, wenn der Bericht aufgrund von Fehlern abgebrochen wird.

**[!UICONTROL Email]:** (Nur E-Mail-Zieltyp) Geben Sie für jede Adresse die Adresse ein und klicken Sie auf **+**.

**[!UICONTROL Destination Name]:** (nur S3-, FTP-, sFTP- und FTP-SSL-Zieltypen) Die Namen der [Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} an die der benutzerdefinierte Bericht gesendet wird.

* Um ein vorhandenes Ziel anzugeben, wählen Sie einen Zielnamen aus der Liste aus. Sie können mehrere Zielnamen separat auswählen.

* So erstellen Sie ein neues Ziel:

   1. Klicken Sie **Neues Ziel hinzufügen**.

   1. Geben Sie die [Berichtszieleinstellungen](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} ein und klicken Sie auf **Speichern**.

   1. Klicken Sie in den Berichtseinstellungen auf **Zielnamen aktualisieren.**

      Das neue Ziel ist jetzt in der Liste der vorhandenen Ziele verfügbar und Sie können es optional zum Bericht hinzufügen.


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [Leistungsberichte auf Erlebnisebene](/help/creative/experiences/experience-performance-details.md)
>* [Über benutzerdefinierte Berichte in DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [Über [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
