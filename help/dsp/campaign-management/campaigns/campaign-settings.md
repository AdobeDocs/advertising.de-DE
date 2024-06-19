---
title: Kampagneneinstellungen
description: Siehe Beschreibungen der verfügbaren Kampagnenparameter.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: d572a406be9271c6ca14d35740f04d15ddbf7364
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Kampagneneinstellungen

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Der Kampagnenname.

**[!UICONTROL Advertiser]:** (Schreibgeschützt für bestehende Kampagnen) Der entsprechende Advertiser (Marke). Wählen Sie einen bestehenden Advertiser aus oder erstellen Sie einen neuen.

**[!UICONTROL Advertiser URL]:** Die offizielle Seite des Werbetreibenden. Dieses Feld beschleunigt Ihren Prozess zur Anzeigenvalidierung mit Inventarpartnern.

**[!UICONTROL Timezone]:** (Schreibgeschützt für vorhandene Kampagnen) Die Zeitzone für Berichterstellung und Gebote.

**[!UICONTROL Customer PO]:** (Optional) Eine Kundenbestellung für die Einfügebestellung/Bestellung.

**[Kampagnendaten]:** Beginn und Ende der Kampagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Ob Ränder für die Kampagne verwaltet werden: *[!UICONTROL Yes]* oder *[!UICONTROL No]* (Standardeinstellung).

Wenn Sie *[!UICONTROL Yes],* Geben Sie den Spannungstyp und Betrag an:

* **[!UICONTROL Margin Type]:** Der Typ des Rands. Sobald Sie die Margenverwaltung aktiviert und die Kampagne gespeichert haben, können Sie den Margentyp nicht mehr ändern.

   * *[!UICONTROL Fixed]:* (Standardeinstellung) Ermöglicht DSP automatische Berechnung und Begrenzung der Ausgaben basierend auf einem festen Marge-Prozentsatz der [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Ermöglicht die Verwaltung von Rändern bis zur Platzierungsebene durch Angabe eines separaten [!UICONTROL Budget Reserve %] und [!UICONTROL Gross Budget] für jedes Paket und jede Platzierung in der Kampagne. DSP optimiert sich auf der Grundlage der finanziellen Effizienz jeder Platzierung, ohne eine bestimmte Marge zu garantieren. Verwenden Sie dies für Einfügeaufträge, die aus mehreren Zeileneinträgen bestehen, für die Sie vereinbart haben, eine feste Menge von Einheiten oder Einheitentypen zu einem festen Preis bereitzustellen.

* **[!UICONTROL Fixed Margin %]:** (Nur Kampagnen mit festen Rändern) Das Standard-Markup für jede Einfügereihenfolge <!-- impression? -->als Prozentsatz. Dieser Betrag wird von der [!UICONTROL Gross Budget] , um das Budget der Kampagne zu bestimmen.

* **[!UICONTROL Budget Reserve %]:** (Nur Kampagnen mit festen Margen; optional) Behält einen bestimmten Prozentsatz der [!UICONTROL Gross Budget] als Schutzmaßnahme. Dieser Betrag wird von der [!UICONTROL Gross Budget] , um das Budget der Kampagne zu bestimmen.

**[!UICONTROL Gross Budget]:** (Nur Kampagnen mit Margenverwaltung) Das Bruttokampagnenbudget, bevor die festgelegten Grenzanpassungen angewendet werden.

Sie können optional ein zusätzliches Bruttobudget für Tag, Woche oder Monat hinzufügen:

1. Klicks **[!UICONTROL Add an additional Gross Budget]**.

1. Geben Sie die **[!UICONTROL Gross Budget]** und wählen Sie das Budgetintervall aus: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* oder *[!UICONTROL Monthly]*.

Das Nettogesamtbudget, das die Ausgabenobergrenze für die Kampagne darstellt, wird automatisch anhand der Margeneinstellungen berechnet und unter diesem Wert angegeben.

**[!UICONTROL Budget]:** (Kampagnen ohne Margenverwaltung) Das Gesamtbudget der Kampagne.

**[!UICONTROL Estimated Tax Withholding]:** Enthält einen Prozentsatz der Gesamtausgaben für Anzeigengebühren, Werbekosten und/oder Datengebühren auf Kontoebene für landesweite oder lokale Steuern. Bei den Sätzen handelt es sich um Schätzungen für Budgetierungs- und Schrittzwecke, sodass die berechneten Steuersätze variieren können.

So schätzen Sie die einzubehaltenden Steuern:

1. Klicks **[!UICONTROL Update rates here]**.

1. Geben Sie die **[!UICONTROL Estimated tax rate]** als Prozentsatz.

1. Aktivieren Sie das Kontrollkästchen neben jedem Gebührentyp, für den Steuern einbehalten werden sollen. Zu den Gebührentypen gehören:

   * *[!UICONTROL Include estimated tax - ads fee]:* Gilt für alle Werbeausgaben DSP Medien, einschließlich Steuern auf Kampagnenverwaltungsgebühren.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Gilt für alle Ausgaben für DSP mit Ausnahme von Medien und Daten. Ausgeschlossen sind Steuern für Kampagnenverwaltungsgebühren

   * *[!UICONTROL Include estimated tax - data fee]:* Gilt für alle Datenausgaben für DSP.

1. Klicks **[!UICONTROL Submit]**.

>[!NOTE]
>
>* In den USA können die Bundesstaaten bei der Einbeziehung von Steuergebühren für Anzeigen, Adserving und Daten variieren. Für Organisationen in anderen Ländern sind alle drei Kategorien von Steuergebühren zur Berücksichtigung der Mehrwertsteuer einzubeziehen.
>
>* Sie können diese Werte auch in den Gebühreneinstellungen des Kontos konfigurieren.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Schreibgeschützt für bestehende Kampagnen, die seit dem 22. Juni 2020 erstellt wurden; nicht verfügbar für Kampagnen, die vor dem 22. Juni 2020 erstellt wurden) Die Ebene, auf der Anzeigen DSP und Frequenzobergrenzen angewendet werden: *Gleiches Gerät* , um ein Gerät auszuwählen oder *Personen* , um eine Person auf allen ihren bekannten Geräten anzusprechen. **Hinweis:** Geräteübergreifende Unterstützung ist nicht für Platzierungen verfügbar, die universelle IDs ansprechen.

**[!UICONTROL Device Graph]:** (Schreibgeschützt für bestehende Kampagnen; Kampagnen mit benutzerspezifischem geräteübergreifendem Targeting) Das Gerätediagramm zur Verwendung für geräteübergreifendes Targeting und Frequenzmanagement:

* *[!UICONTROL LiveRamp - U.S. only]:* Verfügbar für alle Advertiser für geräteübergreifendes Targeting mit einem CPM-Preis von 0,35 USD für Impressionen, die durch Verwendung des [!DNL LiveRamp] Gerätediagramm (d. h. für Geräte, die nicht in den Zielgruppensegmenten gefunden werden). Sie können geräteübergreifendes Targeting auf Platzierungsebene einrichten.

  Diese Option steht auch allen Advertisern ohne Gebühren für Frequenzverwaltung und Attributionsmessung zur Verfügung.

  Die geräteübergreifende Unterstützung gilt nur für Platzierungen, die auf ältere IDs abzielen, jedoch nicht für Platzierungen, die universelle IDs ansprechen (einschließlich [!DNL LiveRamps]). Targeting, Frequenzverwaltung und Attribution für universelle IDs werden nur auf ID-Ebene angewendet.

**[!UICONTROL Frequency Cap]:** (Optional) Gibt an, wie oft ein eindeutiges Gerät, eine universelle ID oder eine Person (je nach spezifiziertem [!UICONTROL Cross Device Level] und der Platzierung [!UICONTROL Targeting] -Einstellung) können Anzeigen aus der Kampagne bereitgestellt werden. Optionen umfassen *[!UICONTROL Unlimited]* oder einen bestimmten Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
> Sie können Frequenzobergrenzen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

**[!UICONTROL Packages]:** Die [packages](/help/dsp/campaign-management/packages/package-about.md) in die Kampagne aufgenommen werden. Wählen Sie vorhandene Pakete aus und/oder erstellen Sie Pakete, die einbezogen werden sollen. Wenn Sie Pakete erstellen, lesen Sie Beschreibungen der [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md) für weitere Informationen.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Die folgenden Einstellungen ermöglichen nur Mess- und Berichterstellungsfunktionen. Die Leistungsoptimierung wird nur auf Paket- und Platzierungsebene ausgeführt.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Optional) Aktiviert [!DNL IAS] Messung und Berichterstellung der Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung unter Verwendung der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Measure On]:** Verzeichnis, in dem zu messen ist: *[!UICONTROL Display and VPAID video inventory]* (Standardeinstellung) oder *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >Die Sichtbarkeit von Videos ist nur im VPAID-Inventar messbar.

* **[!UICONTROL IAS Account ID (AnID)]:** (Werbetreibende mit eigenen [!DNL IAS] Konten; optional) Die [!DNL IAS] Konto-ID, die [!DNL IAS] werden direkt zur Nutzung abgerechnet.

* **[!UICONTROL IAS Team ID]:** (Werbetreibende mit eigenen [!DNL IAS] Konten; optional) Die Team-ID für die [!DNL IAS] -Konto, [!DNL IAS] werden direkt zur Nutzung abgerechnet. <!-- verify -->

**[!UICONTROL MOAT]:** (Optional) Aktiviert [!DNL MOAT] Messung und Berichterstellung der Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung. Es fallen zusätzliche Gebühren an.

#### Zielgruppenüberprüfung

**[!UICONTROL comScore Campaign Ratings]:** (Optional) Aktiviert [!DNL Comscore] validiert [!DNL Campaign Ratings] Messung und Berichterstellung der Zielgruppenüberprüfung unter Verwendung der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Target Gender]:** Das Zielgeschlecht: *[!UICONTROL Both]* (Standardeinstellung), *[!UICONTROL Male]* oder *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Die Altersgruppe für die Zielgruppe. Verwenden Sie die linken und rechten Schieberegler, um den Bereich nach Bedarf zu reduzieren.

* **[!UICONTROL Target Country]:** (Optional) Ein Land für die Zielgruppe. [!DNL Comscore] -Messimpressionen nur in unterstützten Ländern angezeigt werden.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Aktiviert das Tracking für die Platzierungsebene [!UICONTROL Attention Score] Metrik (die gewichtete durchschnittliche Anzahl der [!DNL Adelaide] &quot;[!DNL Attention Units]&quot;über Impressionen hinweg). Metriken sind für alle Platzierungstypen mit Ausnahme von [!DNL Roku] vernetztes Fernsehen, nur VPAID-Pre-Roll und Audio, das kein Podcast ist. DSP fügt automatisch ein JavaScript-Tag an alle zugehörigen kreativen Elemente an und [!DNL Adelaide] erfasst die Belichtungsdaten und sendet sie täglich an DSP. Sie können das Datum verwenden, um Ihre Ausgaben für Platzierungstaktiken mit besseren Aufmerksamkeitsbewertungen manuell zu optimieren.

Die [!UICONTROL Attention Score] -Feld im [!UICONTROL Metrics] Berichtabschnitt; innerhalb der [!UICONTROL Campaigns], [!UICONTROL Packages], und [!UICONTROL Placements] Ansichten und die [!UICONTROL Sites], [!UICONTROL Ads], und [!UICONTROL Inventory] Registerkarten der [Platzierungsdetails-Ansicht](/help/dsp/campaign-management/reports/placement-details-view.md).

Verwenden [!DNL Adelaide] Segmente für die Messung erhalten eine CPM-Gebühr für jede Impression, die von Anzeigen mit [!DNL Adelaide] Tags. Diese Gebühr unterscheidet sich von den Gebühren für [Targeting auf Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Ermöglicht die Messung und Berichterstellung der Sichtbarkeit von Erstanbietern mithilfe des [!DNL IAB Open Video Viewability (OpenVV)] Technologie, basierend auf dem spezifizierten Empfindlichkeitsniveau:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Über Campaign Management](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Eine Kampagne bearbeiten](campaign-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Kampagne](campaign-change-log.md)
