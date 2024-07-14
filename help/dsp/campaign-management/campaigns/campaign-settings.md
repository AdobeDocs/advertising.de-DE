---
title: Kampagneneinstellungen
description: Siehe Beschreibungen der verfügbaren Kampagnenparameter.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 0fbdc7e38026d71483c2de1406a4110066690130
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Kampagneneinstellungen

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Der Kampagnenname.

**[!UICONTROL Advertiser]:** (Schreibgeschützt für vorhandene Kampagnen) Der jeweilige Advertiser (Marke). Wählen Sie einen bestehenden Advertiser aus oder erstellen Sie einen neuen.

**[!UICONTROL Advertiser URL]:** Die offizielle Seite des Advertisers. Dieses Feld beschleunigt Ihren Prozess zur Anzeigenvalidierung mit Inventarpartnern.

**[!UICONTROL Timezone]:** (Schreibgeschützt für vorhandene Kampagnen) Die Zeitzone für die Berichterstellung und Gebotsabgabe.

**[!UICONTROL Customer PO]:** (Optional) Eine Kundenbestellung für die Einfügebestellung/die Einfügebestellung.

**[Kampagnendaten]:** Das Start- und Enddatum der Kampagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Gibt an, ob Ränder für die Kampagne verwaltet werden sollen: *[!UICONTROL Yes]* oder *[!UICONTROL No]* (Standard).

Wenn Sie *[!UICONTROL Yes]auswählen, geben Sie* den Randtyp und den Betrag an:

* **[!UICONTROL Margin Type]:** Der Typ des Rands. Sobald Sie die Margenverwaltung aktiviert und die Kampagne gespeichert haben, können Sie den Margentyp nicht mehr ändern.

   * *[!UICONTROL Fixed]:* (Standardeinstellung) Ermöglicht DSP automatische Berechnung und Begrenzung der Ausgaben basierend auf einem festen Margenprozentsatz des [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Ermöglicht Ihnen, die Ränder bis zur Platzierungsebene zu verwalten, indem Sie für jedes Paket und jede Platzierung in der Kampagne einen separaten [!UICONTROL Budget Reserve %] und [!UICONTROL Gross Budget] angeben. DSP optimiert sich auf der Grundlage der finanziellen Effizienz jeder Platzierung, ohne eine bestimmte Marge zu garantieren. Verwenden Sie dies für Einfügeaufträge, die aus mehreren Zeileneinträgen bestehen, für die Sie vereinbart haben, eine feste Menge von Einheiten oder Einheitentypen zu einem festen Preis bereitzustellen.

* **[!UICONTROL Fixed Margin %]:** (Nur Kampagnen mit festen Rändern) Das standardmäßige Markup für jede Einfügereihenfolge <!-- impression? --> in Prozent. Dieser Betrag wird von der [!UICONTROL Gross Budget] abgezogen, um das Netto-Kampagnenbudget zu definieren.

* **[!UICONTROL Budget Reserve %]:** (Nur Kampagnen mit festen Margen; optional) Behält einen bestimmten Prozentsatz von [!UICONTROL Gross Budget] als Schutz bei. Dieser Betrag wird von der [!UICONTROL Gross Budget] abgezogen, um das Netto-Kampagnenbudget zu definieren.

**[!UICONTROL Gross Budget]:** (Nur Kampagnen mit Margenverwaltung) Das Bruttokampagnenbudget, bevor die festgelegten Grenzanpassungen angewendet werden.

Sie können optional ein zusätzliches Bruttobudget für Tag, Woche oder Monat hinzufügen:

1. Klicken Sie auf **[!UICONTROL Add an additional Gross Budget]**.

1. Geben Sie den Wert **[!UICONTROL Gross Budget]** ein und wählen Sie das Budgetintervall aus: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* oder *[!UICONTROL Monthly]*.

Das Nettogesamtbudget, das die Ausgabenobergrenze für die Kampagne darstellt, wird automatisch anhand der Margeneinstellungen berechnet und unter diesem Wert angegeben.

**[!UICONTROL Budget]:** (Kampagnen ohne Margenverwaltung) Das Gesamtbudget der Kampagne.

**[!UICONTROL Estimated Tax Withholding]:** Hält einen Prozentsatz der Gesamtausgaben für Anzeigengebühren, Werbekosten und/oder Datengebühren auf Kontoebene für landesweite oder lokale Steuern ein. Bei den Sätzen handelt es sich um Schätzungen für Budgetierungs- und Schrittzwecke, sodass die berechneten Steuersätze variieren können.

So schätzen Sie die einzubehaltenden Steuern:

1. Klicken Sie auf **[!UICONTROL Update rates here]**.

1. Geben Sie den Wert **[!UICONTROL Estimated tax rate]** als Prozentsatz an.

1. Aktivieren Sie das Kontrollkästchen neben jedem Gebührentyp, für den Steuern einbehalten werden sollen. Zu den Gebührentypen gehören:

   * *[!UICONTROL Include estimated tax - ads fee]:* Gilt für alle Advertising DSP-Medienausgaben, einschließlich Steuern auf Kampagnenverwaltungsgebühren.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Gilt für alle Ausgaben in Advertising DSP mit Ausnahme von Medien und Daten. Ausgeschlossen sind Steuern für Kampagnenverwaltungsgebühren

   * *[!UICONTROL Include estimated tax - data fee]:* Gilt für alle Datenausgaben in Advertising DSP.

1. Klicken Sie auf **[!UICONTROL Submit]**.

>[!NOTE]
>
>* In den USA können die Bundesstaaten bei der Einbeziehung von Steuergebühren für Anzeigen, Adserving und Daten variieren. Für Organisationen in anderen Ländern sind alle drei Kategorien von Steuergebühren zur Berücksichtigung der Mehrwertsteuer einzubeziehen.
>
>* Sie können diese Werte auch in den Gebühreneinstellungen des Kontos konfigurieren.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Schreibgeschützt für bestehende Kampagnen, die seit dem 22. Juni 2020 erstellt wurden; nicht verfügbar für Kampagnen, die vor dem 22. Juni 2020 erstellt wurden) Die Ebene, auf der Anzeigen DSP und Frequenzobergrenzen angewendet werden: *Gleiches Gerät* für das Targeting eines Geräts oder *Personen* für das Targeting einer Person auf allen bekannten Geräten. **Hinweis:** Geräteübergreifende Unterstützung ist für Platzierungen mit universellen IDs nicht verfügbar.

**[!UICONTROL Device Graph]:** (Schreibgeschützt für vorhandene Kampagnen; Kampagnen mit personenbasiertem geräteübergreifenden Targeting nur) Das Gerätediagramm, das für geräteübergreifendes Targeting und Frequenzmanagement verwendet werden soll:

* *[!UICONTROL LiveRamp - U.S. only]:* Verfügbar für alle Advertiser für geräteübergreifendes Targeting bei 0,35 USD CPM für Impressionen, die mithilfe des [!DNL LiveRamp]-Gerätediagramms bereitgestellt werden (d. h. für Geräte, die nicht in den Zielgruppensegmenten gefunden werden). Sie können geräteübergreifendes Targeting auf Platzierungsebene einrichten.

  Diese Option steht auch allen Advertisern ohne Gebühren für Frequenzverwaltung und Attributionsmessung zur Verfügung.

  Die geräteübergreifende Unterstützung gilt nur für Platzierungen, die auf ältere IDs abzielen, jedoch nicht für Platzierungen, die universelle IDs verwenden (einschließlich [!DNL LiveRamps]). Targeting, Frequenzverwaltung und Attribution für universelle IDs werden nur auf ID-Ebene angewendet.

**[!UICONTROL Frequency Cap]:** (Optional) Die Häufigkeit, mit der ein eindeutiges Gerät, eine universelle ID oder eine Person (je nach spezifiziertem [!UICONTROL Cross Device Level] und der Einstellung [!UICONTROL Targeting] der Platzierung) für Anzeigen aus der Kampagne bereitgestellt werden kann. Zu den Optionen gehören *[!UICONTROL Unlimited]* oder ein bestimmter Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
> Sie können Frequenzobergrenzen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

**[!UICONTROL Packages]:** Die [Pakete](/help/dsp/campaign-management/packages/package-about.md), die in die Kampagne aufgenommen werden sollen. Wählen Sie vorhandene Pakete aus und/oder erstellen Sie Pakete, die einbezogen werden sollen. Wenn Sie Pakete erstellen, finden Sie weitere Informationen unter Beschreibungen der [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md) .

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Die folgenden Einstellungen ermöglichen nur Mess- und Berichterstellungsfunktionen. Die Leistungsoptimierung wird nur auf Paket- und Platzierungsebene ausgeführt.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Optional) Aktiviert die Messung und Berichterstellung von Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung in [!DNL IAS] unter Verwendung der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Measure On]:** Der Bestand, der gemessen werden soll: *[!UICONTROL Display and VPAID video inventory]* (Standard) oder *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >Die Sichtbarkeit von Videos ist nur im VPAID-Inventar messbar.

* **[!UICONTROL IAS Account ID (AnID)]:** (Werbetreibende mit eigenen [!DNL IAS]-Konten; optional) Die [!DNL IAS]-Konto-ID des Unternehmens, die [!DNL IAS] direkt für die Verwendung in Rechnung stellt.

* **[!UICONTROL IAS Team ID]:** (Werbetreibende mit eigenen [!DNL IAS]-Konten; optional) Die Team-ID für das [!DNL IAS]-Konto des Unternehmens, die [!DNL IAS] direkt für die Verwendung anrechnet. <!-- verify -->

**[!UICONTROL MOAT]:** (Optional) Ermöglicht die Messung und Berichterstellung von Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenerkennung (2}). [!DNL MOAT] Es fallen zusätzliche Gebühren an. **Hinweis:** [!DNL Oracle] wird sein Werbegeschäft bis zum 30. September 2024 einschränken, einschließlich aller Dienste von [!DNL MOAT].

#### Zielgruppenüberprüfung

**[!UICONTROL Comscore Campaign Ratings]:** (Optional) Aktiviert die [!DNL Comscore] validierte [!DNL Campaign Ratings] Messung und Berichterstellung der Zielgruppenüberprüfung unter Verwendung der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Target Gender]:** Das Geschlecht als Ziel: *[!UICONTROL Both]* (Standard), *[!UICONTROL Male]* oder *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Der Altersbereich, der als Ziel dienen soll. Verwenden Sie die linken und rechten Schieberegler, um den Bereich nach Bedarf zu reduzieren.

* **[!UICONTROL Target Country]:** (Optional) Ein Land, das als Ziel ausgewählt werden soll. [!DNL Comscore] misst Impressionen, die nur in unterstützten Ländern bereitgestellt werden.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Aktiviert das Tracking für die Metrik auf Platzierungsebene [!UICONTROL Attention Score] (die gewichtete durchschnittliche Anzahl von [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; über Impressionen hinweg). Metriken sind für alle Platzierungstypen verfügbar, mit Ausnahme von [!DNL Roku] vernetztem TV, nur VPAID-basiertem Pre-Roll und Audio, das kein Podcast ist. DSP hängt automatisch ein JavaScript-Tag an alle zugehörigen kreativen Elemente an, und [!DNL Adelaide] verfolgt die Belichtungsdaten und sendet sie täglich an DSP. Sie können das Datum verwenden, um Ihre Ausgaben für Platzierungstaktiken mit besseren Aufmerksamkeitsbewertungen manuell zu optimieren.

Das Feld [!UICONTROL Attention Score] ist im Abschnitt [!UICONTROL Metrics] der Berichte, in den Ansichten [!UICONTROL Campaigns], [!UICONTROL Packages] und [!UICONTROL Placements] sowie auf den Registerkarten [!UICONTROL Sites], [!UICONTROL Ads] und [!UICONTROL Inventory] der Ansicht mit den Platzierungsdetails](/help/dsp/campaign-management/reports/placement-details-view.md) verfügbar.[

Bei Verwendung von [!DNL Adelaide] -Segmenten für die Messung wird eine CPM-Gebühr für jede Impression erhoben, die von Anzeigen mit [!DNL Adelaide] -Messungs-Tags bereitgestellt wird. Diese Gebühr ist separat von den Gebühren für das [Aufmerksamkeit-Targeting auf Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Ermöglicht die Messung und Berichterstellung der Sichtbarkeit von Erstanbietern mithilfe der [!DNL IAB Open Video Viewability (OpenVV)]-Technologie, basierend auf der angegebenen Empfindlichkeitsstufe:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Info zu Campaign Management](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Bearbeiten einer Kampagne](campaign-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Kampagne](campaign-change-log.md)
