---
title: Kampagneneinstellungen
description: Siehe Beschreibungen der verfügbaren Kampagneneinstellungen.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Kampagneneinstellungen

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Der Kampagnenname.

**[!UICONTROL Advertiser]:** (Schreibgeschützt für bestehende Kampagnen) Der entsprechende Advertiser (die Marke). Wählen Sie einen vorhandenen Advertiser aus oder erstellen Sie einen neuen.

**[!UICONTROL Advertiser URL]:** Die offizielle Seite des Werbetreibenden. Dieses Feld beschleunigt den Prozess der Anzeigenvalidierung mit Inventarpartnern.

**[!UICONTROL Timezone]:** (Schreibgeschützt für bestehende Kampagnen) Die Zeitzone für Berichte und Gebote.

**[!UICONTROL Customer PO]:** (Optional) Eine Kundenbestellung für die Einfügebestellung/Bestellung.

**[Kampagnendaten]:** Start- und Enddatum der Kampagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:**, ob die Ränder für die Kampagne verwaltet werden sollen: *[!UICONTROL Yes]* oder *[!UICONTROL No]* (Standard).

Bei Auswahl von *[!UICONTROL Yes]geben* die Art und den Betrag der Spanne an:

* **[!UICONTROL Margin Type]:** Die Art des Rands. Sie können den Margin-Typ nicht mehr ändern, sobald Sie die Margin-Verwaltung aktiviert und die Kampagne gespeichert haben.

   * *[!UICONTROL Fixed]:* (Standard) Ermöglicht es DSP, die Ausgaben automatisch zu berechnen und auf der Grundlage eines festen prozentualen Margenanteils der [!UICONTROL Gross Budget] zu begrenzen.

   * *[!UICONTROL Dynamic]:* Ermöglicht die Verwaltung der Margen bis hinunter zur Platzierungsebene durch Angabe einer separaten [!UICONTROL Budget Reserve %] und [!UICONTROL Gross Budget] für jedes Paket und jede Platzierung in der Kampagne. DSP optimiert anhand der finanziellen Effizienz jeder Platzierung, ohne eine bestimmte Marge zu garantieren. Verwenden Sie diese Option für Einfügungsaufträge, die aus mehreren Positionen bestehen, für die Sie sich bereit erklärt haben, einen festen Betrag von Einheiten oder Einheitentypen zu einem festen Satz zu liefern.

* **[!UICONTROL Fixed Margin %]:** (Nur Kampagnen mit festen Rändern) Das standardmäßige Markup für jede Einfügereihenfolge <!-- impression? --> als Prozentsatz. Dieser Betrag wird von der [!UICONTROL Gross Budget] abgezogen, um das Nettokampagnenbudget zu definieren.

* **[!UICONTROL Budget Reserve %]:** (Nur Kampagnen mit festen Margen; optional) Reserviert einen bestimmten Prozentsatz der [!UICONTROL Gross Budget] als Schutz. Dieser Betrag wird von der [!UICONTROL Gross Budget] abgezogen, um das Nettokampagnenbudget zu definieren.

**[!UICONTROL Gross Budget]:** (Nur Kampagnen mit Margin-Verwaltung) Das Bruttokampagnenbudget, bevor die angegebenen marginalen Anpassungen angewendet werden.

Sie können optional ein zusätzliches tägliches, wöchentliches oder monatliches Bruttobudget hinzufügen:

1. Klicken Sie auf **[!UICONTROL Add an additional Gross Budget]**.

1. Geben Sie den **[!UICONTROL Gross Budget]** ein und wählen Sie das Budgetintervall aus: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* oder *[!UICONTROL Monthly]*.

Das Nettogesamtbudget, das die Ausgabenobergrenze für die Kampagne darstellt, wird automatisch auf der Grundlage der Einstellungen für die Spanne berechnet und unter diesem Wert angegeben.

**[!UICONTROL Budget]:** (Kampagnen ohne Margin-Verwaltung) Das Gesamtbudget der Kampagne.

**[!UICONTROL Estimated Tax Withholding]:** Behält einen Prozentsatz der Gesamtausgaben für Anzeigengebühren, Anzeigenbereitstellungsgebühren und/oder Datengebühren auf Kontoebene für Länder- oder Kommunalsteuern bei. Die Sätze sind Schätzungen für Budgetierungs- und Schrittmachungszwecke, sodass die in Rechnung gestellten Steuersätze variieren können.

So schätzen Sie die einzubehaltenden Steuern:

1. Klicken Sie auf **[!UICONTROL Update rates here]**.

1. Geben Sie die **[!UICONTROL Estimated tax rate]** als Prozentsatz an.

1. Aktivieren Sie das Kontrollkästchen neben jedem Gebührentyp, für den Steuern einbehalten werden sollen. Zu den Gebührentypen gehören:

   * *[!UICONTROL Include estimated tax - ads fee]:* Gilt für alle Advertising DSP-Medienausgaben, einschließlich Steuern auf Kampagnenverwaltungsgebühren.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Gilt für alle Ausgaben für Advertising DSP mit Ausnahme von Medien und Daten. Steuern auf Kampagnenverwaltungsgebühren sind nicht enthalten

   * *[!UICONTROL Include estimated tax - data fee]:* Gilt für alle Daten, die für Advertising DSP ausgegeben werden.

1. Klicken Sie auf **[!UICONTROL Submit]**.

>[!NOTE]
>
>* In den USA können die Bundesstaaten hinsichtlich der Einbeziehung von Steuergebühren in Anzeigen, Anzeigen und Daten variieren. Für Organisationen in anderen Ländern sind alle drei Kategorien von Steuergebühren in die Mehrwertsteuer einzubeziehen.
>
>* Sie können diese Werte auch in den Gebühreneinstellungen des Kontos konfigurieren.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Schreibgeschützt für bestehende Kampagnen, die seit dem 22. Juni 2020 erstellt wurden; nicht verfügbar für Kampagnen, die vor dem 22. Juni 2020 erstellt wurden) Die Ebene, auf der DSP Anzeigen auswählt und Häufigkeitsbegrenzungen anwendet: *Dasselbe Gerät* zum Targeting eines Geräts oder *Personen* zum Targeting einer Person auf allen ihren bekannten Geräten. **Hinweis:** Geräteübergreifende Unterstützung ist nicht für Platzierungen verfügbar, die auf universelle IDs abzielen.

**[!UICONTROL Device Graph]:** (Schreibgeschützt für bestehende Kampagnen; Kampagnen mit personenbasiertem geräteübergreifenden Targeting) Das Gerätediagramm, das für geräteübergreifendes Targeting und Frequenzverwaltung verwendet werden soll:

* *[!UICONTROL LiveRamp - U.S. only]:* Verfügbar für alle Advertiser für geräteübergreifendes Targeting unter 0,35 USD CPM für Impressionen, die mithilfe des [!DNL LiveRamp] Gerätediagramms bereitgestellt werden (d. h. für Geräte, die nicht in den Zielgruppensegmenten gefunden werden). Sie können geräteübergreifendes Targeting auf Platzierungsebene einrichten.

  Diese Option steht auch allen Werbetreibenden ohne Gebühren für das Frequenzmanagement und die Attributionsmessung zur Verfügung.

  Die geräteübergreifende Unterstützung gilt nur für Platzierungen, die auf ältere IDs abzielen, aber nicht für Platzierungen, die auf universelle IDs abzielen (einschließlich [!DNL LiveRamps]). Zielgruppenbestimmung, Frequenzverwaltung und Attribution für universelle IDs werden nur auf ID-Ebene angewendet.

**[!UICONTROL Frequency Cap]:** (Optional) Die Häufigkeit, mit der ein eindeutiges Gerät, eine universelle ID oder eine Person (abhängig von der angegebenen [!UICONTROL Cross Device Level] und der [!UICONTROL Targeting] der Platzierung) Anzeigen aus der Kampagne erhalten kann. Zu den Optionen gehören *[!UICONTROL Unlimited]* oder ein bestimmter Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
> Sie können Häufigkeitsbegrenzungen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP berücksichtigt die strengste Häufigkeitsbegrenzung in der Kampagnenhierarchie.

**[!UICONTROL Packages]:** Die [Pakete](/help/dsp/campaign-management/packages/package-about.md) die in die Kampagne aufgenommen werden sollen. Vorhandene Pakete auswählen und/oder Pakete erstellen, die einbezogen werden sollen. Wenn Sie Pakete erstellen, finden Sie unter Beschreibungen zu den [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md) weitere Informationen.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Die folgenden Einstellungen aktivieren nur Mess- und Berichtsfunktionen. Die Leistungsoptimierung wird nur auf Paket- und Platzierungsebene ausgeführt.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Optional) Ermöglicht [!DNL IAS] Messung und Berichterstellung von Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung unter Verwendung der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Measure On]:** Der Bestand, auf dem gemessen werden soll: *[!UICONTROL Display and VPAID video inventory]* (Standard) oder *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >Die Sichtbarkeit von Videos kann nur im VPAID-Inventar gemessen werden.

* **[!UICONTROL IAS Account ID (AnID)]:** (Werbetreibende mit eigenen [!DNL IAS]-Konten; optional) Die [!DNL IAS]-Konto-ID des Unternehmens, die [!DNL IAS] direkt für die Nutzung in Rechnung stellen.

* **[!UICONTROL IAS Team ID]:** (Werbetreibende mit eigenen [!DNL IAS]-Konten; optional) Die Team-ID für das [!DNL IAS]-Konto der Organisation, die [!DNL IAS] direkt für die Nutzung in Rechnung stellen. <!-- verify -->

#### Zielgruppenüberprüfung

**[!UICONTROL Comscore Campaign Ratings]:** (Optional) Ermöglicht [!DNL Comscore] validierte [!DNL Campaign Ratings] Messung und Berichterstellung zur Zielgruppenüberprüfung unter Verwendung der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Target Gender]:** Das anzusprechende Geschlecht: *[!UICONTROL Both]* (Standard), *[!UICONTROL Male]* oder *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Der Altersbereich bis zum Ziel. Verwenden Sie die Regler links und rechts, um den Bereich nach Bedarf zu reduzieren.

* **[!UICONTROL Target Country]:** (Optional) Ein Land für die Zielgruppenbestimmung. [!DNL Comscore] Maßnahmen können Impressionen nur in unterstützten Ländern anzeigen.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Aktiviert das Tracking für die [!UICONTROL Attention Score]-Metrik auf Platzierungsebene (die gewichtete durchschnittliche Anzahl [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; über Impressionen hinweg). Metriken sind für alle Platzierungstypen verfügbar, mit Ausnahme von [!DNL Roku] Connected TV, VPAID-only Pre-Roll und Audio, das kein Podcast ist. DSP hängt allen zugehörigen Kreativen automatisch ein JavaScript-Tag an. [!DNL Adelaide] verfolgt die Belichtungsdaten und sendet sie täglich an DSP. Sie können das Datum verwenden, um Ihre Ausgaben manuell für Platzierungstaktiken mit besseren Aufmerksamkeitswerten zu optimieren.

Das Feld [!UICONTROL Attention Score] ist im [!UICONTROL Metrics] von Berichten, in den [!UICONTROL Campaigns]-, [!UICONTROL Packages]- und [!UICONTROL Placements] sowie auf den Registerkarten [!UICONTROL Sites], [!UICONTROL Ads] und [!UICONTROL Inventory] der [Platzierungsdetailansicht](/help/dsp/campaign-management/reports/placement-details-view.md) verfügbar.

Bei der Verwendung [!DNL Adelaide] Messsegmente fallen für jede Impression, die von Anzeigen mit [!DNL Adelaide] Messungstags bereitgestellt wird, eine CPM-Gebühr an. Diese Gebühr ist getrennt von den Gebühren für [Zielgruppenbestimmung auf Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Ermöglicht die Messung und Berichterstellung der Sichtbarkeit durch Erstanbieter mithilfe der [!DNL IAB Open Video Viewability (OpenVV)]-Technologie basierend auf der angegebenen Empfindlichkeitsstufe:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Über Campaign Management](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Bearbeiten einer Kampagne](campaign-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Kampagne](campaign-change-log.md)
