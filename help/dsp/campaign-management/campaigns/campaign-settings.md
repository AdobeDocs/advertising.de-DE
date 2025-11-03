---
title: Kampagneneinstellungen
description: Siehe Beschreibungen der verfügbaren Kampagneneinstellungen.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9d26e097f007b570c0f0e3b7f02c683a84d5e647
workflow-type: tm+mt
source-wordcount: '1434'
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

**[!UICONTROL Margin Management]:** (Self-Service-Konten, die von Agenturen mit Margen bedient werden) Optionen für die Margenverwaltung:

* **[!UICONTROL Would you like to manage margins for this campaign?]:**, ob die Ränder für die Kampagne verwaltet werden sollen: *[!UICONTROL Yes]* oder *[!UICONTROL No]* (Standard). Wenn Sie *[!UICONTROL Yes]wählen, geben* die zusätzlichen Einstellungen an. Sobald Sie die Verwaltung der Spanne aktiviert und die Kampagne gespeichert haben, können Sie die Verwaltung der Spanne nicht mehr deaktivieren.

* **[!UICONTROL How would you like to compute agency fees?]:** (Nur Kampagnen mit Margin-Management) Berechnung der Agenturgebühren, die den einbehaltenen und nicht in den Nettoausgaben enthaltenen Teil des Bruttobudgets der Kampagne ausmachen:

   * *[!UICONTROL Margin % of Total Budget]:* (Standard) Die Gebühren als Prozentsatz der Bruttoausgaben berechnen. Geben Sie die [!UICONTROL Agency Fee Type] (fest oder zusammengesetzt) und die [!UICONTROL Margin %] oder [!UICONTROL Composite Margin %] an.

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* Berechnen Sie die Gebühren als einen bestimmten Prozentsatz Ihrer Medienkosten, Daten- und anderen Kosten und/oder [!DNL Adobe] technischen Gebühren. Geben Sie die [!UICONTROL Markup %] an und wählen Sie die Komponenten aus, auf die das Markup angewendet werden soll.

* **[!UICONTROL Agency Fee Type]:** (Kampagnen, die [!UICONTROL Margin % of Total Budget] verwenden) Die Art der Agenturgebühr.

   * *[!UICONTROL Fixed]:* (Standard) Ermöglicht es DSP, einen festen Prozentsatz der Bruttoausgaben als Agenturgebühren einzubehalten. Geben Sie die [!UICONTROL Margin %] an.

   * *[!UICONTROL Composite]:* Ermöglicht DSP, einen Prozentsatz der Bruttoausgaben einzubehalten, um sowohl Agenturgebühren als auch [!DNL Adobe]-Tech-Gebühren zu berücksichtigen. Geben Sie die [!UICONTROL Composite Margin %] an.

* **[!UICONTROL Margin %]:** (Kampagnen, die [!UICONTROL Margin % of Total Budget] mit festen Margen verwenden) Der Prozentsatz der Bruttoausgaben, die als Agenturgebühren einzubehalten sind. Änderungen am Wert der Spanne werden nur auf künftige Bruttoausgaben und nicht auf die historischen Bruttoausgaben für die Kampagne angewendet. Der [!UICONTROL Estimated Tax Withholding] ist vor Anwendung der Marge von den Bruttoausgaben auszuschließen. Sehen Sie sich die folgenden Beispiele an, in denen davon ausgegangen wird, dass die Kampagne nicht zu viel oder zu wenig ausgibt.

   * Beispiel 1: Angenommen, der [!UICONTROL Gross Budget] ist `100 USD` und der [!UICONTROL Margin %] ist während des gesamten Fluges `5%`. Am Ende des Kampagnenflugs werden die Agenturgebühren als `5 USD` berechnet (was `5% of 100 USD` ist), und die Nettoausgaben sind `95 USD` (was `campaign budget [100 USD] - agency fees [5 USD]` ist).

   * Beispiel 2 mit Änderungen der Spanne: Angenommen, [!UICONTROL Margin %] wurde für dieselbe Kampagne von `5%` in `10%` geändert, als die Bruttoausgaben `40 USD` wurden. Für den Zeitraum vor der Änderung werden die Agenturgebühren als `2 USD` berechnet (was `5% of 40 USD` ist); für den Zeitraum nach der Änderung werden die Agenturgebühren als `6 USD` berechnet (was `10% of 60 USD` ist). Die gesamten Agenturgebühren werden als `8 USD` berechnet (was `2 USD + 6 USD` ist), und die Nettoausgaben sind `92 USD` (was `campaign budget [100 USD] - total agency fees [8 USD]` ist).

   * Beispiel 3 mit Steuereinbehaltung: Angenommen, die [!UICONTROL Gross Budget] ist `100 USD`, die [!UICONTROL Estimated Tax Withholding] am Ende des Kampagnenflugs ist `10 USD` und die [!UICONTROL Margin %] ist während des gesamten Flugs `5%`. Am Ende des Kampagnenflugs werden die Agenturgebühren als `4.5 USD` berechnet (was `5% of (campaign budget [100 USD] - tax withholding [USD 10])` ist), und die Nettoausgaben sind `85.5 USD` (was `campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]` ist).

* **[!UICONTROL Composite Margin %]:** (Kampagnen, die [!UICONTROL Margin % of Total Budget] mit zusammengesetzten Margen verwenden) Der Prozentsatz der Bruttoausgaben, der als [!DNL Adobe] und Agenturgebühren zusammen einzubehalten ist. Die Agenturgebühren werden durch Abzug der Adobe Tech-Gebühren vom zusammengesetzten Margenbetrag berechnet. Änderungen am zusammengesetzten Wert der Spanne werden nur auf die künftigen Bruttoausgaben und nicht auf die historischen Bruttoausgaben für die Kampagne angewendet. Der [!UICONTROL Estimated Tax Withholding] ist vor Anwendung der Gesamtspanne von den Bruttoausgaben auszuschließen.

  Angenommen, der [!UICONTROL Gross Budget] ist `100 USD`, die [!DNL Adobe] Tech-Gebühren am Ende des Kampagnenflugs sind `10 USD` und der [!UICONTROL Composite Margin %] wird während des gesamten Flugs `17%`. Am Ende des Kampagnenflugs (vorausgesetzt, dass die Kampagne nicht zu viel oder zu viel ausgibt) werden die Agenturgebühren als `7 USD` berechnet (was `(17% of 100 USD) - 10` ist) und die Nettoausgaben sind `93 USD` (was `campaign budget [100 USD] - agency fees [7 USD]` ist).

* **[!UICONTROL Markup %]:** (Kampagnen, die [!UICONTROL Apply Markup % on top of individual cost components] verwenden) Der Prozentsatz, der auf bestimmte Kostenkomponenten zur Berechnung der Agenturgebühren angewendet werden soll. Änderungen am Aufschlagwert werden nur auf zukünftige Kosten und nicht auf die historischen Kosten für die Kampagne angewendet.

* **[!UICONTROL Select cost components on which markup will be applied]:** (Kampagnen, die [!UICONTROL Apply Markup % on top of individual cost components] verwenden) Die Kostenkomponenten, für die die [!UICONTROL Markup %] angewendet wird. Wählen Sie alle entsprechenden Komponenten aus: *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]* und/oder *[!UICONTROL Adobe tech fees]*. Änderungen an der Komponentenauswahl werden nur auf die zukünftigen Kosten und nicht auf die historischen Kosten für die Kampagne angewendet.

  Beispielsweise wird die [!UICONTROL Markup %] für &quot;`10%`&quot; und &quot;[!UICONTROL Media cost]&quot; [!UICONTROL Data and Other costs]. Wenn zu einem beliebigen Zeitpunkt während des Kampagnenflugs die Medienkosten `20 USD`, Daten und andere Kosten `5 USD` werden und [!DNL Adobe] Technologiegebühren `2 USD` werden, werden die Agenturgebühren als `2.50 USD` berechnet (was `10% of (20 USD + 5 USD)` ist, und die Bruttoausgaben `29.50 USD` (was `media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]` ist).

**[!UICONTROL Gross Budget]:** (Nur Kampagnen mit Margin-Verwaltung) Das Bruttokampagnenbudget, bevor die angegebenen marginalen Anpassungen angewendet werden.

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
>* [Über die Kampagnenverwaltung](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Bearbeiten einer Kampagne](campaign-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Kampagne](campaign-change-log.md)
