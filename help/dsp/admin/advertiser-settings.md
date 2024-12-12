---
title: Advertiser-Kontoeinstellungen
description: Siehe Beschreibungen der verfügbaren Advertiser-Einstellungen.
role: User, Admin
source-git-commit: 20f69d2e8d5d289015c911f153609c0805307f0a
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Advertiser-Kontoeinstellungen

*Nicht für schreibgeschützte Benutzer verfügbar*

<!-- Not published -->

## [!UICONTROL General] Einstellungen

**[!UICONTROL Advertiser Name]:** Der Name des Advertisers.

**[!UICONTROL Category]:** Die Kategorie, in der das Geschäft des Advertisers tätig ist. Die Kategorie wird den Herausgebern mitgeteilt, wenn Sie ein Angebot für den Bestand abgeben. Stellen Sie sicher, dass Sie eine Kategorie auswählen, die Ihren Anzeigen entspricht, oder Herausgeber können Ihre Anzeigen ablehnen.

>[!NOTE]
>
>Wenn Sie *[!UICONTROL Other]* auswählen, kann der Werber nicht auf DSP [!DNL On Demand Inventory] zugreifen.

**[!UICONTROL Advertiser URL]:** Die Homepage oder die Haupt-Website-URL des Advertisers (beginnend mit `http://` oder `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Nur neue Advertiser-Konten) Stellt alle für das DSP des Unternehmens konfigurierten privaten Exchange-Feeds für den Advertiser zur Verfügung.

### [!UICONTROL Adobe IMS IDs]

Werbetreibende mit zusätzlichen Adobe Experience Cloud-Produkten können Daten mithilfe der eindeutigen ID des Unternehmens für Experience Cloud über einige Produkte hinweg freigeben. Sie können bestimmte Produktintegrationen im Abschnitt [!UICONTROL Integrations] konfigurieren.

**[!UICONTROL Account IMS org and ID]:** (Werbetreibende mit zusätzlichen Experience Cloud-Produkten, die über ein Experience Cloud-Konto mit mehreren Advertisern lizenziert sind; optional) Die Experience Cloud-Organisations-ID des Advertisers.

**[!UICONTROL Advertiser IMS org and ID]:** (Advertiser mit Direktlizenzen für zusätzliche Experience Cloud-Produkte; optional) Die Experience Cloud-Organisations-ID des Advertisers.

### [!UICONTROL Integrations]

(Optional) Zusätzliche Experience Cloud-Produkte, die mit dem DSP verknüpft sind. Die Produkte müssen derselben Experience Cloud-Organisations-ID zugeordnet sein, die im Abschnitt [!UICONTROL Adobe IMS IDs] angegeben ist.

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Werbetreibende mit [!DNL Advertising Search, Social, & Commerce] oder die Adobe Advertising-Konversionspixel verwenden) Ein [!DNL Search, Social, & Commerce]-Konto, mit dem DSP Attributionsdaten austauschen.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Werbetreibende mit Adobe Analytics; optional; nur auf Daten anwendbar, die mit Adobe Advertising-Konversions-Tracking-Tags erfasst wurden, die nur ein [!DNL EF Redirect] und ein Token enthalten) Eine oder mehrere [!DNL Analytics] Report Suites, an die DSP Daten von Herausgebern und Partnern auf der Angebotsseite sendet. Analytics sendet außerdem die erfassten Daten von der Site des Kunden an DSP.

Damit die Daten in den Report Suites angezeigt werden, muss die entsprechende Einstellung auf Advertiser-Ebene [!DNL Search, Social, & Commerce] aktiviert sein. Darüber hinaus muss das [!DNL Analytics] -Konto des Advertisers für den Empfang von Daten von Adobe Advertising konfiguriert werden.

>[!WARNING]
>
>Wenn Sie eine zuvor verknüpfte Report Suite entfernen, tauscht DSP keine Daten mehr mit dieser Suite aus. Datenfluktuationen werden erwartet.

Weitere Informationen zur Integration mit [!DNL Analytics] finden Sie unter &quot;[Überblick über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)&quot;.

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Werbetreibende mit Adobe Audience Manager oder Adobe Analytics; optional) Ein Audience Manager- oder [!DNL Analytics]-Konto, aus dem DSP Segmentmetadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Adobe-Zielgruppen des Advertisers abruft. Dazu gehören Daten für:

* Audience Manager-Segmente
* [!DNL Analytics] Segmente, die in Adobe Experience Cloud veröffentlicht werden
* Segmente, die mit dem Adobe Experience Cloud [!DNL Audience Library] erstellt wurden
* Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Adobe Advertising gesendet werden

Die anfängliche Synchronisation dauert etwa 24 Stunden. Danach werden die Daten in Echtzeit mit einer Verzögerung von einer bis zwei Sekunden synchronisiert.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Einstellungen

Sie können optional Standardziele für die neuen Platzierungen des Werbetreibenden konfigurieren. Benutzer können die Standardziele für jede neue Platzierung überschreiben.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Das Standardland für das Geotargeting jeder Platzierung. Benutzer können für jede Platzierung das Land ändern und spezifischeres Geotargeting konfigurieren.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Alle Zielgruppen oder Segmente, die standardmäßig unterdrückt werden sollen. Benutzer können die Ausschlüsse für jede Platzierung ändern.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Typen der anzuwendenden kontextuellen Filter [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39]. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md) überschreiben.

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Inventarkontext, die standardmäßig blockiert werden sollen. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Optional) Ein oder mehrere Arten von Bestandsattributen, die standardmäßig als Ziel dienen sollen. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Bestandsattributen, die standardmäßig blockiert werden. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Optional) Der Grad des Erwachseneninhalts, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standard), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Alcohol Content]:** (Optional) Der Alkoholgehalt, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standard), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren erhoben werden.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Arten von zu blockierenden Sites basierend auf betrügerischem Traffic und verdächtigen Aktivitäten, die durch [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39] gemessen werden. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md) überschreiben.

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Standardmäßig wird der gesamte 100 % ungültige Traffic, einschließlich des Traffics auf entführten Geräten, für neue Platzierungen blockiert. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Also block sites with]:** (Optional) Eine zusätzliche Stufe von Betrug und ungültigem Traffic, die dazu führt, dass DSP Anzeigen standardmäßig blockieren: *[!UICONTROL None]* (der Standard, der zusätzlichen Traffic nicht blockiert), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* oder *[!UICONTROL >25% Average Fraud/IVT levels]*. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Betrug, durch den Anzeigen standardmäßig blockiert DSP: *[!UICONTROL Fraud]* (blockiert alle Websites mit Betrug), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* und/oder *[!UICONTROL Fraud: Zero Ads]*. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Optional) Ein Typ verdächtiger Website- oder App-Aktivitäten, der dazu führt, dass DSP Anzeigen standardmäßig blockieren: *[!UICONTROL None]* (der Standard, der Anzeigen nicht aufgrund verdächtiger Aktivitäten blockiert), *[!UICONTROL Suspicious Activity - High Risk]* oder *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Es können zusätzliche Gebühren erhoben werden.

#### [!UICONTROL Pre-Bid Viewability]

Optionale Sichtbarkeitsfilter vor dem Angebot durch [!DNL DoubleVerify] und [!DNL Integral Ad Science], die auf Platzierungen angewendet werden sollen. Die Standardeinstellungen auf Advertiser-Ebene werden für neue Platzierungen ausgewählt. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md) überschreiben.

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Video

** **[!UICONTROL Include URL's whose average video viewability rate is]**. Wählen Sie mit dieser Option die Kriterien aus.

** **[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

** **[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. Wählen Sie mit dieser Option die Kriterien aus.

** **[!UICONTROL Include URL's whose average player size composition is]**. Wählen Sie mit dieser Option die Kriterien aus.

** **[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Anzeige

** **[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. Wählen Sie mit dieser Option die Kriterien aus.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. Wählen Sie mit dieser Option die Kriterien aus.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

Ein optionaler Filter **[!UICONTROL Video Viewability Targets]** und ein optionaler Filter **[!UICONTROL Display Viewability Targets]** . Es können zusätzliche Gebühren erhoben werden.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Standardmäßig, welcher Grad von [[!DNL Ads.txt] Prebid-Filterung](https://iabtechlab.com/ads-txt-about/) verwendet werden soll, indem die [!DNL Authorized Digital Sellers] -Liste jedes Herausgebers genutzt wird:
* *[!UICONTROL Opt out of ads.txt (default)]*: Um Inventar von allen Verkäufern zu kaufen.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Zur Priorisierung des Kaufinventars von autorisierten Direktverkäufern und Wiederverkäufern einer Domain.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von autorisierten Direktverkäufern und Wiederverkäufern einer Domain zu kaufen.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von autorisierten Direktverkäufern einer Domain zu kaufen.

Sie können die Einstellung auf Advertiser-Ebene auf [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md) überschreiben.

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Standardmäßig ermöglicht einen Filter nach dem Angebot in Echtzeit, um sicherzustellen, dass Anzeigen auf den Sites bereitgestellt werden, auf denen der Advertiser ausgerichtet ist. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] nur Kunden; optional) Eine [!DNL DoubleVerify Authentic Brand Safety] Segment-ID, die dem [!DNL DoubleVerify] -Konto des Unternehmens zugeordnet ist und standardmäßig für alle Platzierungen verwendet wird. Durch die Angabe einer ID werden Impressionen nach dem Gebot blockiert, indem die für die angegebene Segment-ID konfigurierten benutzerspezifischen Markensicherheitsregeln verwendet werden. DSP stellt Ihr Konto für die Verwendung der Segment-ID in Rechnung.

Die ID muss mit &quot;51&quot;beginnen und aus acht Ziffern bestehen. Sie können die ID auf Advertiser-Ebene auf Platzierungsebene ändern oder löschen.

>[!MORELIKETHIS]
>
>* [Erstellen eines Advertiser-Kontos](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
