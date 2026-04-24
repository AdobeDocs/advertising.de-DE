---
title: Advertiser account settings
description: See descriptions of the available advertiser settings.
role: User, Admin
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# Advertiser account settings

*Nicht für schreibgeschützte Benutzer verfügbar*

<!-- Not published -->

## [!UICONTROL General] settings

**[!UICONTROL Advertiser Name]:** The advertiser name.

**[!UICONTROL Category]:** The category in which the advertiser&#39;s business operates. The category is communicated to the publishers when you bid on inventory. Make sure you choose a category that aligns with your ads, or publishers may reject your ads.

>[!NOTE]
>
>If you select *[!UICONTROL Other]*, then the advertiser can&#39;t access DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** The advertiser&#39;s homepage or main website URL (beginning with `http://` or `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (New advertiser accounts only) Makes all private exchange feeds configured for the organization&#39;s DSP account available to the advertiser.

### [!UICONTROL Adobe IMS IDs]

Advertisers with additional Adobe CX Enterprise products can share data across some products using the organization&#39;s unique ID for CX Enterprise. You can configure specific product integrations in the [!UICONTROL Integrations] section.

**[!UICONTROL Account IMS org and ID]:** (Advertisers with additional CX Enterprise products that are licensed through an CX Enterprise account with multiple advertisers; optional) The advertiser&#39;s CX Enterprise organization ID.

**[!UICONTROL Advertiser IMS org and ID]:** (Advertisers with direct licenses for additional CX Enterprise products; optional) The advertiser&#39;s CX Enterprise organization ID.

### [!UICONTROL Integrations]

(Optional) Additional CX Enterprise products linked to the DSP account. The products must be associated with the same CX Enterprise organization ID provided in the [!UICONTROL Adobe IMS IDs] section.

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Advertisers with [!DNL Advertising Search, Social, & Commerce] or who use Adobe Advertising conversion pixels) A [!DNL Search, Social, & Commerce] account with which DSP exchanges attribution data.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Advertisers with Adobe Analytics; optional; applicable only to data collected using Adobe Advertising conversion tracking tags that include an [!DNL EF Redirect] and token only) One or more [!DNL Analytics] report suites to which DSP sends data it collects from publishers and supply-side partners. Analytics also sends the data it collects from the client&#39;s site to DSP.

For the data to appear in the report suites, the appropriate [!DNL Search, Social, & Commerce] advertiser-level setting must be enabled. In addition, the advertiser&#39;s [!DNL Analytics] account must be configured to receive data from Adobe Advertising.

>[!WARNING]
>
>If you remove a previously linked report suite, DSP no longer exchanges data with that suite. Erwarten Sie Datenschwankungen.

Weitere Informationen zur Integration mit [!DNL Analytics] finden Sie unter [Übersicht über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Werbetreibende mit Adobe Audience Manager oder Adobe Analytics; optional) Ein Audience Manager- oder [!DNL Analytics], aus dem DSP Segmentmetadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Adobe-Zielgruppen des Werbetreibenden abruft. Dazu gehören Daten für:

* Audience Manager-Segmente
* [!DNL Analytics] Segmente, die in Adobe CX Enterprise veröffentlicht werden
* Segmente, die mit dem Adobe CX Enterprise-[!DNL Audience Library] erstellt werden
* Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Adobe Advertising gesendet werden

Die erste Synchronisierung dauert etwa 24 Stunden. Danach werden die Daten in Echtzeit mit einer Verzögerung von ein bis zwei Sekunden synchronisiert.
<!--
 I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting]

Sie können optional Standardziele für die neuen Platzierungen des Advertisers konfigurieren. Benutzer können die Standardziele für jede neue Platzierung überschreiben.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Das Standardland für das Geo-Targeting jeder Platzierung. Benutzer können für jede Platzierung das Land ändern und spezifischere Geotargeting konfigurieren.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Alle Zielgruppen oder Segmente, die standardmäßig unterdrückt werden sollen. Benutzer können die Ausschlüsse für jede Platzierung ändern.

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

Typen von [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39] anzuwendenden kontextuellen Filtern. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene“ ](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Inventarkontext, der standardmäßig blockiert werden soll. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Optional) Mindestens ein Typ von Inventarattributen, die standardmäßig ausgewählt werden sollen. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Optional) Mindestens ein Typ von Inventarattributen, die standardmäßig blockiert werden sollen. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Optional) The degree of adult content for which to block ads by default: *[!UICONTROL Do Not Block]* (the default), *[!UICONTROL Standard]*, or *[!UICONTROL Strict]*. Es können zusätzliche Gebühren anfallen.

**[!UICONTROL Alcohol Content]:** (Optional) The degree of alcohol content for which to block ads by default: *[!UICONTROL Do Not Block]* (the default), *[!UICONTROL Standard]*, or *[!UICONTROL Strict]*. Es können zusätzliche Gebühren anfallen.

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

Types of sites to block based on fraudulent traffic and suspicious activities measured through [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39]. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene“ ](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** By default, blocks all 100% invalid traffic, including traffic on hijacked devices, for new placements. Es können zusätzliche Gebühren anfallen.

**[!UICONTROL Also block sites with]:** (Optional) An additional level of fraud and invalid traffic that causes DSP to block ads by default:  *[!UICONTROL None]* (the default, which doesn&#39;t block additional traffic), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, or *[!UICONTROL >25% Average Fraud/IVT levels]*. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Optional) One or more types of fraud that cause DSP to block ads by default: *[!UICONTROL Fraud]* (which blocks all sites with fraud), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, and/or *[!UICONTROL Fraud: Zero Ads]*. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Optional) A type of suspicious website or app activity that causes DSP to block ads by default: *[!UICONTROL None]* (the default, which doesn&#39;t block ads based on suspicious activity), *[!UICONTROL Suspicious Activity - High Risk]*, or *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Es können zusätzliche Gebühren anfallen.

#### [!UICONTROL Pre-Bid Viewability]

Optional pre-bid viewability filters by [!DNL DoubleVerify] and [!DNL Integral Ad Science] to apply to placements. The advertiser-level defaults are selected for new placements. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene“ ](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Video

** **[!UICONTROL Include URL's whose average video viewability rate is]**. With this option, select the criteria.

** **[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

** **[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. With this option, select the criteria.

** **[!UICONTROL Include URL's whose average player size composition is]**. With this option, select the criteria.

** **[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Display

** **[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. With this option, select the criteria.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. With this option, select the criteria.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

An optional **[!UICONTROL Video Viewability Targets]** filter and an optional **[!UICONTROL Display Viewability Targets]** filter. Es können zusätzliche Gebühren anfallen.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Standardmäßig wird festgelegt, welche Ebene [[!DNL Ads.txt] Vorangebotfilterung](https://iabtechlab.com/ads-txt-about/) durch die Verwendung der [!DNL Authorized Digital Sellers]-Liste jedes Herausgebers verwendet werden soll:
* *[!UICONTROL Opt out of ads.txt (default)]*: Zu kaufen Inventar von allen Verkäufern.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Priorisierung des Kaufbestands bei den autorisierten Direktverkäufern und Wiederverkäufern einer Domain.
* *[!UICONTROL Ads.txt sellers only]*: Zum Kauf des Inventars nur von den autorisierten Direktverkäufern und Wiederverkäufern einer Domain.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von den autorisierten Direktverkäufern einer Domain zu kaufen.

Sie können die Einstellung auf Advertiser-Ebene auf der [Platzierungsebene“ ](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** aktiviert standardmäßig einen Echtzeit-Filter nach Gebotsabgabe, um sicherzustellen, dass Anzeigen auf den Sites geschaltet werden, auf die der Werbetreibende abzielt. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** (nur [!DNL DoubleVerify] Kunden; optional) Eine [!DNL DoubleVerify Authentic Brand Safety] Segment-ID, die mit dem [!DNL DoubleVerify] des Unternehmens verknüpft ist und standardmäßig für alle Platzierungen verwendet werden soll. Durch die Angabe einer ID werden Impressionen nach dem Angebot anhand der benutzerdefinierten Markensicherheitsregeln blockiert, die für die angegebene Segment-ID konfiguriert sind. DSP stellt Ihrem Konto die Nutzung der Segment-ID in Rechnung.

Die ID muss mit „51“ beginnen und aus acht Ziffern bestehen. Sie können die ID auf Advertiser-Ebene auf Platzierungsebene ändern oder löschen.

>[!MORELIKETHIS]
>
>* [Advertiser-Konto erstellen](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the advertiser list for the account](/help/dsp/admin/advertiser-view.md) -->
