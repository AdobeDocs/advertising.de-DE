---
title: Überprüfen und Bearbeiten von Einstellungen der Kampagnenkomponente mithilfe von Bulksheets
description: Erfahren Sie, wie Sie wichtige Parameter für Paket, Platzierung und Anzeige mithilfe von Tabellen stapelweise überprüfen und bearbeiten können.
feature: DSP Placements
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Überprüfen und Bearbeiten von Einstellungen der Kampagnenkomponente mithilfe von Bulksheets

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

Sie können die Einstellungen für die Pakete, Platzierungen und Anzeigen in einer einzelnen Kampagne im XLSX-Format ([!DNL Microsoft Excel] Tabelle) zur Überprüfung herunterladen. Standardmäßig enthält die heruntergeladene Datei separate Registerkarten für Paketeinstellungen, Package-Fluginformationen, Platzierungseinstellungen und Platzierungs-Anzeigenzeitpläne. Optional können Sie die Einstellungen für einige Kampagnenkomponenten-Typen ausschließen.

Um mehrere Einstellungen gleichzeitig zu aktualisieren, laden Sie eine gültige Bulksheet-Datei mit den Änderungen hoch. Um das Bulksheet zu erstellen, können Sie eine leere Bulksheet-Vorlage herunterladen, die Registerkarten für jeden Kampagnentyp enthält, neue oder aktualisierte Einstellungen eingeben oder in die Vorlagendatei einfügen und dann die Datei speichern, um sie hochzuladen. Zu bearbeitbaren Feldern gehören die meisten Einstellungen, die normalerweise bearbeitbar sind.

>[!NOTE]
>
>Sie können die Einstellungen auch nur für bestimmte Pakete und bestimmte Platzierungen herunterladen und bearbeiten. Siehe &quot;[Überprüfen und Bearbeiten von Paketeinstellungen mit Bulksheets](/help/dsp/campaign-management/packages/package-qa.md)&quot;und &quot;[Überprüfen und Bearbeiten von Platzierungseinstellungen mit Bulksheets](/help/dsp/campaign-management/placements/placement-qa.md)&quot;.

## Download-Einstellungen für Pakete, Platzierungen und Anzeigen in einer Kampagne

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Heben Sie im Dialogfeld [!UICONTROL QA Sheet Download] die Auswahl aller Kampagnenkomponenten auf, deren Einstellungen Sie aus der heruntergeladenen Datei ausschließen möchten, und klicken Sie auf **[!UICONTROL Download]**.

Standardmäßig sind Einstellungen für alle Kampagnenkomponenten ausgewählt.

Eine Benachrichtigung gibt an, wann die Datei zum Herunterladen verfügbar ist.

1. Führen Sie einen der folgenden Schritte aus, um die Datei herunterzuladen:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie rechts oben in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner Downloads des Browsers gespeichert. Eine Liste der enthaltenen Spalten finden Sie unter &quot;[Platzierungsspalten in heruntergeladenen/hochgeladenen Arbeitsblättern](#qa-sheet-columns)&quot;.

>[!NOTE]
>
>QS-Dateien auf Kampagnenebene können nicht bearbeitet und erneut hochgeladen werden. Um Änderungen an den Einstellungen der Kampagnenkomponente in diesen Dateien vorzunehmen, laden Sie [eine separate Einstellungsvorlagendatei (Setup-Datei)](#download-template) herunter, geben Sie Zeilen aus der QA-Datei in die Vorlage ein oder fügen Sie sie in die Vorlage ein und speichern Sie die Datei. Laden Sie dann die ausgefüllte Vorlagendatei hoch ](#upload-bulksheet-campaign-components).[

## Herunterladen einer Bulksheet-Vorlage für eine Kampagne {#download-template}

Laden Sie eine leere Bulksheet-Vorlage herunter, die Registerkarten für jeden Kampagnentyp enthält. Sie können später Zeilen zu jeder Registerkarte der Vorlage hinzufügen und [die bearbeitete Datei hochladen](##upload-bulksheet-campaign-components), um Änderungen an den Kampagnenkomponenten vorzunehmen.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Klicken Sie im Dialogfeld [!UICONTROL Upload Bulksheet] auf **[!UICONTROL Bulksheet Template].**

   Die Datei wird im Ordner Downloads des Browsers gespeichert. Eine Liste der enthaltenen Spalten finden Sie unter &quot;[Platzierungsspalten in heruntergeladenen/hochgeladenen Arbeitsblättern](#qa-sheet-columns)&quot;.

## Hochladen eines Bulksheets mit Paket-, Platzierungs- und Anzeigeneinstellungen für eine Kampagne{#upload-bulksheet-campaign-components}

Laden Sie die Einstellungen für Pakete, Platzierungen und Anzeigen in einer einzelnen Kampagne gleichzeitig in ein ausgefülltes Bulksheet hoch.

1. [Laden Sie bei Bedarf eine Bulksheet-Vorlage herunter](#download-template), geben Sie Paket-, Platzierungs- und/oder Anzeigeneinstellungen auf den entsprechenden Registerkarten einer Bulksheet-Vorlage ein oder fügen Sie sie ein und speichern Sie die Datei dann auf Ihrem Gerät oder Netzwerk.

   Siehe verfügbare Einstellungen unten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Im Dialogfeld [!UICONTROL Upload Bulksheet] :

   1. Ziehen Sie eine Datei in das Feld oder klicken Sie in das Feld, um eine Datei aus Ihrem Gerät oder Netzwerk auszuwählen.

   1. Klicken Sie auf **[!UICONTROL Upload]**.

1. (Optional) Um sicherzustellen, dass die Aktualisierungen verarbeitet wurden, klicken Sie rechts oben in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png) .

## Platzierungseinstellung Spalten in heruntergeladenen/hochgeladenen Arbeitsblättern{#qa-sheet-columns}

>[!TIP]
>
> In einer heruntergeladenen Tabelle werden alle bearbeitbaren Spalten blau hervorgehoben.

### Kampagnenebenen-Tabellen

| Abschnitt | Spalte | Beschreibung | Bearbeitbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | Die numerische ID der Platzierung. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Der Name der Platzierung. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Alle angewendeten Beschriftungen für die Berichterstellung. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Ein Link zum Öffnen der Platzierung im Bearbeitungsmodus. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | Der Platzierungsstatus: *[!UICONTROL active]* oder *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Der Platzierungstyp. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Der Name des übergeordneten Pakets, sofern zutreffend. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Das Startdatum der Platzierung. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Das Enddatum der Platzierung. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Ob Dayparting *[!UICONTROL ON]* oder *[!UICONTROL OFF]* ist.<br><b>Hinweis:</b> Um den tatsächlichen Dayparting-Zeitplan zu überprüfen, öffnen Sie die Platzierungseinstellungen in DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Das Platzierungsbudget, falls vorhanden. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Das Budgetintervall: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* oder *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Ziel des Pakets. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | Der Zielwert des Ziels. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Ob die Platzierung in Richtung *[!UICONTROL Budget]* oder *[!UICONTROL Impressions]* bewegt wird. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Das maximale Angebot für die Platzierung. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | Die Flugplatzstrategie für die Platzierung: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* oder *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | Die Innentagsgeschwindigkeit für die Platzierung: *[!UICONTROL Even]* oder *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Alle anzuwendenden Filterkriterien vor dem Angebot. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Ob Angebotsregeln (nicht mehr unterstützt) *[!UICONTROL ON]* oder *[!UICONTROL OFF]* sind. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Die primäre Frequenzbegrenzung für die Platzierung während des angegebenen [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Das Intervall für die primäre Frequenzbegrenzung: *[!UICONTROL Day]*, *[!UICONTROL Week]* oder *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Die sekundäre Frequenzbegrenzung für die Platzierung während des angegebenen [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Der Intervalltyp für die sekundäre Frequenzbegrenzung: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* oder *[!UICONTROL Minute]*. Die anwendbare Anzahl von Wochen, Tagen, Stunden oder Minuten wird durch die [!UICONTROL Secondary Frequency Cap Interval Value] angegeben. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Die Anzahl der Wochen, Tage, Stunden oder Minuten, für die der [!UICONTROL Secondary Frequency Cap] gilt. Wenn die sekundäre Begrenzung beispielsweise drei Impressionen pro sechs Stunden beträgt, wäre der Wert hier `6`. | Ja |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Die Anzahl der geografischen Zielorte, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Die geografischen Zielorte, getrennt durch Semikolons oder *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Die Anzahl der ausgeschlossenen geografischen Standorte oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Die ausgeschlossenen geografischen Standorte, getrennt durch Semikolons, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Die Anzahl der zielgerichteten öffentlichen Inventargeschäfte, sofern vorhanden, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Die Anzahl der ausgeschlossenen öffentlichen Inventargeschäfte, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Die Anzahl der zielgerichteten privaten Inventargeschäfte, sofern vorhanden, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Die Anzahl der ausgeschlossenen privaten Inventargeschäfte, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Die Anzahl der zielgerichteten [!UICONTROL On-Demand Inventory] Angebote, falls angegeben, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Die Anzahl der ausgeschlossenen On-Demand-Lagerergänzungen (falls vorhanden) oder *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Der Targeting-Typ von Traffic: *[!UICONTROL Website]* und/oder *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Gibt an, ob die Option &quot;Inventar-Targeting&quot;zum Ausschließen von ausgehendem Traffic &lt;i[!UICONTROL >ON]* oder *[!UICONTROL OFF]* lautet.<br>Über dem Inhalt angezeigte Anzeigen erscheinen in der Regel als Pop-up oder mit Inhalten gefüllt (im nativen Erlebnis) und nicht als normale Videoanzeigen in einem Videoplayer. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | Die Qualität der Zielseiten: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* oder *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | Die Anzahl der zielgerichteten Site-Kategorien, sofern vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Die Anzahl der ausgeschlossenen Site-Kategorien, sofern vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Die ausgeschlossenen Sites, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Die Zielsprachen der Site. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Nur Standard-Platzierungen für die Anzeige) Gibt an, ob die Bereitstellung von Anzeigen auf nicht geprüften Sites zulässig ist: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. Wenn die Platzierung auf den privaten Bestand ausgerichtet ist, kann diese Option Anzeigen auf blockierten Sites bereitstellen. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | Die Anzahl der Targeting-Sites (falls vorhanden) oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Die Zielgruppen, sofern angegeben, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Die ausgeschlossenen Zielgruppen, sofern angegeben, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Gibt an, ob demografische Segmente für die Platzierung (und andere Platzierungen in der Kampagne) aktiviert sind: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. [!DNL Comscore] Diese Funktion kann nur für Kampagnen aktiviert werden, für die die Funktion [!DNL Audience Verification] für [!DNL Nielsen] und/oder [!DNL Comscore] aktiviert ist.  Es fallen zusätzliche Gebühren an. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Ob das Anzeigen-Targeting geräteübergreifend erweitert werden soll: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. Geräteübergreifendes Targeting erweitert Ihr Targeting auf das gesamte bekannte Gerät einer Person entsprechend dem in den Kampagneneinstellungen angegebenen Gerätediagramm. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Include # | Die Anzahl der Zielthema-Codes, sofern vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Die Anzahl der ausgeschlossenen Themencodes, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | Die Anzahl der Zielgeräteziele (falls vorhanden) oder *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Die Anzahl der ausgeschlossenen Geräteziele, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Die Anzahl der ISP-Provider, für die Targeting durchgeführt wurde (falls vorhanden), oder *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Die Anzahl der ausgeschlossenen ISP-Provider (sofern vorhanden) oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | Die Anzahl der angewendeten Sicherheitsfilter für die Marke, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | Die Anzahl der angewendeten Blockierungsfilter für Betrug vor dem Gebot, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | Die Anzahl der angewendeten Sichtbarkeitsfilter vor dem Gebot, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Ob der Sicherheitsblock der Site aktiviert ist: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Die Anzahl der an die Platzierung angehängten Pixel für Ereignisverfolgung von Drittanbietern (0).*[!UICONTROL None]* | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Die Anzahl der Konversions-Tracking-Pixel, die an die Platzierung angehängt sind, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Ein statischer Drittanbieter-Gebührensatz, der als nicht abrechnungsfähige Kosten pro 1000 Impressionen verfolgt werden kann, falls zutreffend. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Die Anzahl der Anzeigen, die mit der Platzierung verbunden sind (sofern vorhanden), oder *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Die Namen aller Anzeigen, die mit der Platzierung verbunden sind, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | Die eindeutigen DSP-generierten Anzeigen-IDs aller Anzeigen, die mit der Platzierung verbunden sind, getrennt durch Semikolons. Um eine Liste mit Anzeigennamen und zugehörigen Anzeigen-IDs aus der [!UICONTROL Ads]-Ansicht herunterzuladen, erstellen Sie eine benutzerdefinierte Ansicht mit der Metrik [!UICONTROL Ad ID] und exportieren Sie dann die Daten ](/help/dsp/campaign-management/reports/campaign-export-data.md).[ | Ja |

>[!MORELIKETHIS]
>
>* [Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/packages/package-qa.md)
>* [Überprüfen und Bearbeiten von Platzierungseinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/placements/placement-qa.md)
