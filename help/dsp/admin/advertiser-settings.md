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

## [!UICONTROL General]

**[!UICONTROL Advertiser Name]:** Der Name des Werbetreibenden.

**[!UICONTROL Category]:** Die Kategorie, in der das Unternehmen des Werbetreibenden tätig ist. Die Kategorie wird den Herausgebern mitgeteilt, wenn Sie im Inventar bieten. Achten Sie darauf, eine Kategorie auszuwählen, die mit Ihren Anzeigen übereinstimmt. Andernfalls können Herausgeber Ihre Anzeigen ablehnen.

>[!NOTE]
>
>Wenn Sie *[!UICONTROL Other]* auswählen, kann der Werbetreibende nicht auf DSP-[!DNL On Demand Inventory] zugreifen.

**[!UICONTROL Advertiser URL]:** Die Homepage- oder Haupt-Website-URL des Werbetreibenden (beginnend mit `http://` oder `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Nur neue Advertiser-Konten) Stellt dem Advertiser alle für das DSP-Konto des Unternehmens konfigurierten privaten Exchange-Feeds zur Verfügung.

### [!UICONTROL Adobe IMS IDs]

Werbetreibende mit zusätzlichen Adobe Experience Cloud-Produkten können Daten über einige Produkte hinweg freigeben, indem sie die eindeutige ID des Unternehmens für das Experience Cloud verwenden. Im Abschnitt [!UICONTROL Integrations] können Sie bestimmte Produktintegrationen konfigurieren.

**[!UICONTROL Account IMS org and ID]:** (Werbetreibende mit zusätzlichen Experience Cloud-Produkten, die über ein Experience Cloud-Konto mit mehreren Werbetreibenden lizenziert werden; optional) Die Experience Cloud-Organisations-ID des Werbetreibenden.

**[!UICONTROL Advertiser IMS org and ID]:** (Werbetreibende mit Direktlizenzen für zusätzliche Experience Cloud-Produkte; optional) Die Experience Cloud-Organisations-ID des Werbetreibenden.

### [!UICONTROL Integrations]

(Optional) Zusätzliche Experience Cloud-Produkte in Verbindung mit dem DSP-Konto. Die Produkte müssen mit derselben Experience Cloud-Organisations-ID verknüpft sein, die im Abschnitt [!UICONTROL Adobe IMS IDs] angegeben ist.

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Werbetreibende mit [!DNL Advertising Search, Social, & Commerce] oder die Adobe Advertising-Konversionspixel verwenden) Ein [!DNL Search, Social, & Commerce], mit dem DSP Attributionsdaten austauscht.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Werbetreibende mit Adobe Analytics; optional; gilt nur für Daten, die mithilfe von Adobe Advertising-Konversionsverfolgungstags erfasst werden, die nur eine [!DNL EF Redirect] und ein Token enthalten) Eine oder mehrere [!DNL Analytics] Report Suites, an die DSP Daten sendet, die sie von Herausgebern und Anbieterpartnern erfasst. Analytics sendet auch die Daten, die es von der Website des Clients erfasst, an DSP.

Damit die Daten in den Report Suites angezeigt werden, muss die entsprechende Einstellung auf Advertiser[!DNL Search, Social, & Commerce]Ebene aktiviert sein. Darüber hinaus muss das [!DNL Analytics] des Werbetreibenden so konfiguriert sein, dass es Daten von Adobe Advertising empfängt.

>[!WARNING]
>
>Wenn Sie eine zuvor verknüpfte Report Suite entfernen, tauscht DSP keine Daten mehr mit dieser Suite aus. Erwarten Sie Datenschwankungen.

Weitere Informationen zur Integration mit [!DNL Analytics] finden Sie unter [Übersicht über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Werbetreibende mit Adobe Audience Manager oder Adobe Analytics; optional) Ein Audience Manager- oder [!DNL Analytics], aus dem DSP Segmentmetadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Adobe-Zielgruppen des Werbetreibenden abruft. Dazu gehören Daten für:

* Audience Manager-Segmente
* [!DNL Analytics] Segmente, die in Adobe Experience Cloud veröffentlicht werden
* Segmente, die mit dem Adobe Experience Cloud-[!DNL Audience Library] erstellt werden
* Segmente, die in Adobe Experience Platform erstellt und über den Audience Manager an Adobe Advertising gesendet werden

Die erste Synchronisierung dauert etwa 24 Stunden. Danach werden die Daten in Echtzeit mit einer Verzögerung von ein bis zwei Sekunden synchronisiert.
<!-- I don't think this is true anymore:
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

#### [!UICONTROL Contextual Filtering]

Typen von [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39] anzuwendenden kontextuellen Filtern. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene“ ](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Inventarkontext, der standardmäßig blockiert werden soll. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Optional) Mindestens ein Typ von Inventarattributen, die standardmäßig ausgewählt werden sollen. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Optional) Mindestens ein Typ von Inventarattributen, die standardmäßig blockiert werden sollen. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Optional) Der Grad von Inhalten für Erwachsene, für die Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standard), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren anfallen.

**[!UICONTROL Alcohol Content]:** (Optional) Der Alkoholgehalt, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standard), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren anfallen.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Arten von Websites, die aufgrund von betrügerischem Traffic und verdächtigen Aktivitäten blockiert werden sollen, gemessen durch [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39]. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene“ ](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** blockiert standardmäßig den gesamten zu 100 % ungültigen Traffic für neue Platzierungen, einschließlich Traffic auf entführten Geräten. Es können zusätzliche Gebühren anfallen.

**[!UICONTROL Also block sites with]:** (Optional) Eine zusätzliche Ebene von Betrug und ungültigem Traffic, die dazu führt, dass DSP Anzeigen standardmäßig blockiert: *[!UICONTROL None]* (die Standardeinstellung, die zusätzlichen Traffic nicht blockiert), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* oder *[!UICONTROL >25% Average Fraud/IVT levels]*. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Optional) Eine oder mehrere Arten von Betrug, der dazu führt, dass DSP Anzeigen standardmäßig blockiert: *[!UICONTROL Fraud]* (der alle Websites mit Betrug blockiert), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* und/oder *[!UICONTROL Fraud: Zero Ads]*. Es können zusätzliche Gebühren anfallen.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Optional) Ein Typ einer verdächtigen Website- oder App-Aktivität, der dazu führt, dass DSP Anzeigen standardmäßig blockiert: *[!UICONTROL None]* (der Standard, der Anzeigen nicht aufgrund verdächtiger Aktivitäten blockiert), *[!UICONTROL Suspicious Activity - High Risk]* oder *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Es können zusätzliche Gebühren anfallen.

#### [!UICONTROL Pre-Bid Viewability]

Optionale Pre-Bid-Sichtbarkeitsfilter nach [!DNL DoubleVerify] und [!DNL Integral Ad Science] zur Anwendung auf Platzierungen. Die Standardeinstellungen auf Advertiser-Ebene sind für neue Platzierungen ausgewählt. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene“ ](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Video

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average video viewability rate is]**. Wählen Sie mit dieser Option die Kriterien aus.

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. Wählen Sie mit dieser Option die Kriterien aus.

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average player size composition is]**. Wählen Sie mit dieser Option die Kriterien aus.

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Anzeige

**&#x200B; **&#x200B;[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. Wählen Sie mit dieser Option die Kriterien aus.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. Wählen Sie mit dieser Option die Kriterien aus.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

Ein optionaler **[!UICONTROL Video Viewability Targets]** und ein optionaler **[!UICONTROL Display Viewability Targets]**. Es können zusätzliche Gebühren anfallen.

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

**[!UICONTROL DoubleVerify Account]:** (nur [!DNL DoubleVerify] Kunden; optional) Eine [!DNL DoubleVerify Authentic Brand Safety] Segment-ID, die mit dem [!DNL DoubleVerify] des Unternehmens verknüpft ist und standardmäßig für alle Platzierungen verwendet werden soll. Durch die Angabe einer ID werden Impressionen nach dem Angebot anhand der benutzerdefinierten Markensicherheitsregeln blockiert, die für die angegebene Segment-ID konfiguriert sind. DSP stellt Ihrem Konto die Nutzung für die Segment-ID in Rechnung.

Die ID muss mit „51“ beginnen und aus acht Ziffern bestehen. Sie können die ID auf Advertiser-Ebene auf Platzierungsebene ändern oder löschen.

>[!MORELIKETHIS]
>
>* [Advertiser-Konto erstellen](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
