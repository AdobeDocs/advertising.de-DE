---
title: Überprüfen und Bearbeiten der Einstellungen von Kampagnenkomponenten mithilfe von Bulksheets
description: Erfahren Sie, wie Sie wichtige Paket-, Platzierungs- und Anzeigeneinstellungen mithilfe von Tabellen stapelweise überprüfen und bearbeiten können.
feature: DSP Placements
exl-id: 1ec8362a-d37b-4fd7-becd-3a5b4f0c9504
source-git-commit: d4d35eff8aa02244ea174784420992537371ff7c
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Überprüfen und Bearbeiten der Einstellungen von Kampagnenkomponenten mithilfe von Bulksheets

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

Sie können die Einstellungen für die Pakete, Platzierungen und Anzeigen in einer einzelnen Kampagne im XLSX-Format ([!DNL Microsoft Excel]-Kalkulationstabelle) zur Überprüfung herunterladen. Standardmäßig enthält die heruntergeladene Datei separate Registerkarten für Paketeinstellungen, Paketfluginformationen, Platzierungseinstellungen und Platzierungs- und Anzeigenzeitpläne. Optional können Sie die Einstellungen für einige Kampagnenkomponentententypen ausschließen.

Um mehrere Einstellungen gleichzeitig zu aktualisieren, laden Sie eine gültige Bulksheet-Datei mit den Änderungen hoch. Um eine Bulksheet zu erstellen, können Sie eine leere Bulksheet-Vorlage herunterladen, die Registerkarten für jeden Typ von Kampagnenkomponente enthält, neue oder aktualisierte Einstellungen in die Vorlagendatei eingeben oder einfügen und dann die Datei speichern, um sie hochzuladen. Bearbeitbare Felder enthalten die meisten Einstellungen, die normalerweise bearbeitet werden können.

>[!NOTE]
>
>Sie können die Einstellungen auch nur für bestimmte Pakete und bestimmte Platzierungen herunterladen und bearbeiten. Siehe [Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/packages/package-qa.md) und [Überprüfen und Bearbeiten von Platzierungseinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/placements/placement-qa.md).

## Download-Einstellungen für die Pakete, Platzierungen und Anzeigen in einer Kampagne

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Heben Sie im Dialogfeld [!UICONTROL QA Sheet Download] die Auswahl aller Kampagnenkomponenten auf, deren Einstellungen Sie aus der heruntergeladenen Datei ausschließen möchten, und klicken Sie dann auf **[!UICONTROL Download]**.

Standardmäßig sind Einstellungen für alle Kampagnenkomponenten ausgewählt.

Eine Benachrichtigung gibt an, wann die Datei zum Herunterladen verfügbar ist.

1. Führen Sie einen der folgenden Schritte aus, um die Datei herunterzuladen:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie oben rechts in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner Downloads des Browsers gespeichert. Unter &quot;[ in heruntergeladenen/hochgeladenen ](#qa-sheet-columns)&quot; finden Sie eine Liste der eingeschlossenen Spalten.

>[!NOTE]
>
>QA-Dateien auf Kampagnenebene können nicht bearbeitet und erneut hochgeladen werden. Um Änderungen an den Einstellungen der Kampagnenkomponenten in diesen Dateien vorzunehmen, [laden Sie eine separate Einstellungsvorlagendatei (Setup-Datei) herunter](#download-template) geben Sie Zeilen aus der QA-Datei in die Vorlage ein oder fügen Sie sie ein und speichern Sie die Datei und [laden Sie dann die ausgefüllte Vorlagendatei hoch](#upload-bulksheet-campaign-components).

## Herunterladen einer Bulksheet-Vorlage für eine Kampagne {#download-template}

Laden Sie eine leere Bulksheet-Vorlage herunter, die Registerkarten für jeden Typ von Kampagnenkomponente enthält. Sie können später Zeilen zu jeder Registerkarte der Vorlage hinzufügen und [die bearbeitete Datei hochladen](##upload-bulksheet-campaign-components) um Änderungen an den Kampagnenkomponenten vorzunehmen.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Klicken Sie im Dialogfeld [!UICONTROL Upload Bulksheet] auf **[!UICONTROL Bulksheet Template].**

   Die Datei wird im Ordner Downloads des Browsers gespeichert. Unter &quot;[ in heruntergeladenen/hochgeladenen ](#qa-sheet-columns)&quot; finden Sie eine Liste der eingeschlossenen Spalten.

## Hochladen einer Bulksheet mit Paket-, Platzierungs- und Anzeigeneinstellungen für eine Kampagne{#upload-bulksheet-campaign-components}

Laden Sie Einstellungen für Pakete, Platzierungen und Anzeigen in einer Kampagne gleichzeitig in einer ausgefüllten Bulksheet hoch.

1. [Bulksheet-Vorlage herunterladen](#download-template) Geben Sie bei Bedarf Paket-, Platzierungs- und/oder Anzeigeneinstellungen in die entsprechenden Registerkarten einer Bulksheet-Vorlage ein oder fügen Sie sie ein und speichern Sie dann die Datei auf Ihrem Gerät oder Netzwerk.

   Siehe die verfügbaren Einstellungen unten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Im Dialogfeld [!UICONTROL Upload Bulksheet] :

   1. Ziehen Sie eine Datei per Drag-and-Drop in das Feld oder klicken Sie in das Feld, um eine Datei auf Ihrem Gerät oder Netzwerk auszuwählen.

   1. Klicken Sie auf **[!UICONTROL Upload]**.

1. (Optional) Um sicherzustellen, dass die Aktualisierungen verarbeitet wurden, klicken ![ rechts ](/help/dsp/assets/downloads.png) der oberen Menüleiste auf „Vorgänge“.

## Platzierungseinstellungen in heruntergeladenen/hochgeladenen Arbeitsblättern{#qa-sheet-columns}

>[!TIP]
>
> In einer heruntergeladenen Tabelle werden alle bearbeitbaren Spalten blau hervorgehoben.

### Tabellen auf Kampagnenebene

| Abschnitt | Spalte | Beschreibung | Bearbeitbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | Die numerische ID der Platzierung. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Der Name der Platzierung. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Alle angewendeten Kennzeichnungen für das Reporting. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Ein Link zum Öffnen der Platzierung im Bearbeitungsmodus. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | Der Platzierungsstatus: *[!UICONTROL active]* oder *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Der Platzierungstyp. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Der Name des übergeordneten Pakets, falls zutreffend. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Das Startdatum der Platzierung. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Das Enddatum der Platzierung. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Ob DayParting *[!UICONTROL ON]* oder *[!UICONTROL OFF]* ist.<br><b>Hinweis:</b> Um den aktuellen DayParting-Zeitplan zu überprüfen, öffnen Sie die Platzierungseinstellungen in DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Das Platzierungsbudget, falls vorhanden. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Das Budgetintervall: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* oder *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Das Ziel des Pakets. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | Der Zielwert des Ziels. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Gibt an, ob die Platzierung in Richtung *[!UICONTROL Budget]* oder *[!UICONTROL Impressions]* verläuft. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Das maximale Angebot für die Platzierung. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | Die Geschwindigkeits-Strategie für die Platzierung: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* oder *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | Die Intraday-Geschwindigkeit für die Platzierung: *[!UICONTROL Even]* oder *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Etwaige anzuwendende Filterkriterien für den Vorangebotstermin. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Ob Gebotsregeln (veraltet) *[!UICONTROL ON]* oder *[!UICONTROL OFF]* sind. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Die primäre Häufigkeitsbegrenzung für die Platzierung während des angegebenen [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Das Intervall für die primäre Frequenzbegrenzung: *[!UICONTROL Day]*, *[!UICONTROL Week]* oder *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Die sekundäre Frequenzbegrenzung für die Platzierung während des angegebenen [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Der Intervalltyp für die sekundäre Frequenzbegrenzung: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* oder *[!UICONTROL Minute]*. Die entsprechende Anzahl von Wochen, Tagen, Stunden oder Minuten wird durch die [!UICONTROL Secondary Frequency Cap Interval Value] angegeben. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Die Anzahl der Wochen, Tage, Stunden oder Minuten, für die die [!UICONTROL Secondary Frequency Cap] gilt. Wenn die sekundäre Begrenzung beispielsweise drei Impressions pro sechs Stunden beträgt, wird der Wert hier `6`. | Ja |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Die Anzahl der geografischen Zielorte, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Die geografischen Zielorte, getrennt durch Semikolons oder *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Die Anzahl der ausgeschlossenen geografischen Standorte oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Die ausgeschlossenen geografischen Standorte, durch Semikolons oder *[!UICONTROL None]* getrennt. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Die Anzahl der anvisierten öffentlichen Inventarangebote (sofern vorhanden), *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Die Anzahl der ausgeschlossenen öffentlichen Inventarangebote (sofern vorhanden) oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Die Anzahl der anvisierten privaten Inventarangebote (sofern vorhanden), *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Die Anzahl der ausgeschlossenen privaten Lagerabschlüsse, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Die Anzahl der zielgerichteten [!UICONTROL On-Demand Inventory]-Angebote, sofern vorhanden, angegeben, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Die Anzahl der ausgeschlossenen On-Demand-Lagerabschlüsse, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Der ausgewählte Traffic-Typ: *[!UICONTROL Website]* und/oder *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Ob die Inventar-Targeting-Option zum Ausschließen des ausgehenden Traffics &lt;i[!UICONTROL >ON]* oder *[!UICONTROL OFF]* ist.<br>Outstream-Anzeigen werden normalerweise über dem Inhalt als Popup oder mit Inhalten gefüllt (im nativen Erlebnis) und nicht als normale Videoanzeigen in einem Videoplayer angezeigt. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | Die Qualität der anzusprechenden Websites: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* oder *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | Die Anzahl der anvisierten Site-Kategorien, falls vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Die Anzahl der ausgeschlossenen Site-Kategorien, falls vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Die ausgeschlossenen Sites, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Die Zielsprachen der Website. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Nur standardmäßige Display-Platzierungen) Gibt an, ob die Bereitstellung von Anzeigen auf nicht geprüften Sites zugelassen werden soll: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. Wenn die Platzierung auf ein privates Inventar abzielt, kann diese Option Anzeigen auf blockierten Websites bereitstellen. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | Die Anzahl der Zielwebsites, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Die ausgewählten Zielgruppen, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Die ausgeschlossenen Zielgruppen, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Ob für die Platzierung (und andere Platzierungen in der Kampagne) demografische Segmente [!DNL Comscore] aktiviert sind: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. Diese Funktion kann nur für Kampagnen aktiviert werden, für die die [!DNL Audience Verification]-Funktion für [!DNL Nielsen] und/oder [!DNL Comscore] aktiviert ist.  Es fallen zusätzliche Gebühren an. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Gibt an, ob das Anzeigen-Targeting über Geräte hinweg erweitert werden soll: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. Beim geräteübergreifenden Targeting wird das Targeting für das gesamte bekannte Gerät einer Person gemäß dem in den Kampagneneinstellungen angegebenen Gerätediagramm erweitert. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Enthalten # | Die Anzahl der anvisierten Themen-Codes (sofern vorhanden) oder *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Die Anzahl der ausgeschlossenen Topic-Codes, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | Die Anzahl der Zielgeräte-Ziele, falls vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Die Anzahl der ausgeschlossenen Geräteziele, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Die Anzahl der ausgewählten ISP-Provider (falls vorhanden) oder *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Die Anzahl der ausgeschlossenen ISP-Provider (sofern vorhanden) oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | Die Anzahl der angewendeten Markensicherheitsfilter (falls vorhanden) oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | Die Anzahl der angewendeten Filter zum Sperren von Betrug vor Gebotsabgabe, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | Die Anzahl der angewendeten Pre-Bid-Sichtbarkeitsfilter (falls vorhanden) oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Unabhängig davon, ob Site Safety Block aktiviert ist: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Die Anzahl der mit der Platzierung oder dem *[!UICONTROL None]* verbundenen Ereignisverfolgungspixel eines Drittanbieters. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Die Anzahl der an die Platzierung angehängten Konversionsverfolgungspixel oder *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Ein statischer Gebührensatz eines Drittanbieters, der als nicht fakturierbare Kosten pro 1000 Impressionen erfasst werden soll, falls zutreffend. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Die Anzahl der Anzeigen, die der Platzierung beigefügt sind, falls vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Die Namen aller Anzeigen, die an die Platzierung angehängt sind, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | Die eindeutigen DSP-generierten Anzeigen-IDs aller Anzeigen, die an die Platzierung angehängt sind, getrennt durch Semikolons. Um eine Liste mit Anzeigennamen und zugehörigen Anzeigen-IDs aus der [!UICONTROL Ads]-Ansicht herunterzuladen, erstellen Sie eine benutzerdefinierte Ansicht, die die [!UICONTROL Ad ID]-Metrik enthält, und exportieren [die Daten](/help/dsp/campaign-management/reports/campaign-export-data.md). | Ja |

>[!MORELIKETHIS]
>
>* [Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/packages/package-qa.md)
>* [Überprüfen und Bearbeiten von Platzierungseinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/placements/placement-qa.md)
