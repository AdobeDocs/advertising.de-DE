---
title: Verwenden von [!DNL Roku] inventory
description: Erfahren Sie mehr über DSP Partnerschaft mit [!DNL Roku], einschließlich Lagerbestandsoptionen, genehmigten Drittanbieter für die Nachverfolgung und Best Practices für [!DNL Roku]-spezifische Platzierungen.
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: f3099c84fe2d6b1610ddf4ca07d59b119718afee
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Verwenden von [!DNL Roku] Bestand

Advertising DSP bietet Funktionen für Werbung für [!DNL Roku].

## Zielgruppenübereinstimmung

Die Partnerschaft [!DNL Roku] und DSP ordnet Ihre [!DNL DSP] Zielgruppen mit [!DNL Roku] IDs für 1:1 deterministische Zielgruppen-Targeting für den [!DNL Roku]-Bestand zu.

## [!DNL Roku] Inventaroptionen

Sie können entweder a) private Deal-IDs direkt mit [!DNL Roku] einrichten und dann die Deal-ID-Daten in DSP eingeben oder b) die [!DNL On Demand] Galerie besuchen, um [!DNL Roku] Profile zu abonnieren:

>[!NOTE]
>
>[!DNL Roku] inventory ist nicht an offenen Marktplätzen und Börsen verfügbar.

* Richten Sie für Ihre privaten Angebote [ Informationen über die Deal-IDs in DSP](/help/dsp/inventory/deal-id-create.md) ein und wählen Sie dann &quot;[!UICONTROL Roku Network - Audience]&quot; und &quot;[!UICONTROL The Roku Channel - Audience]&quot; innerhalb von [!DNL Roku] Platzierungen aus.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Sie können [den folgenden [!DNL Roku] Bestand in der [!DNL On Demand] Galerie](/help/dsp/inventory/on-demand-inventory-subscribe.md) abonnieren und dann genehmigte Angebote innerhalb von [!DNL Roku] Platzierungen als Ziel auswählen:

   * &quot;[!UICONTROL Roku Network - Audience]&quot; für den Bestand im gesamten [!DNL Roku] Ökosystem mit Premium-Inhaltspartnern wie [!DNL The CW], [!DNL ABC] und [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel - Audience]&quot; für [!DNL Roku] eigene und betriebene (O&amp;O) App-Inhalte.

### Vorteile der Anpassung privater Marketplace mit [!DNL Roku]

Private Deals ermöglichen es Ihnen, die Deal-Parameter nach Ihren Bedürfnissen anzupassen.

* **Verhandlungspreis:** Arbeiten Sie mit dem Verkaufsteam von [!DNL Roku] zusammen, um ein Geschäft auszuhandeln und zu strukturieren, das Ihren Kampagnenanforderungen entspricht.

* **Skalierungspriorität:** Private Marktplätze (PMPs) erhalten eine höhere Priorität als Angebote, die immer aktiviert werden (z. B. [!DNL On Demand] Angebote).

* **Frequenzverwaltung:** Die standardmäßige Frequenzlimitierung ist eine (1) und pro 30 Minuten pro Benutzer. Sie können die Obergrenze jedoch nach Stunde, Tag, Woche, Monat oder dem gesamten Flugzeitraum anpassen.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->[!DNL Roku]

* **[!DNL Roku]Daten-Targeting:** [!DNL Roku] Zielgruppen werden aus [!DNL Roku] Geräte- und Fernsehsignalen erstellt, von [!DNL The Roku Channel] verfolgten Daten (z. B. Affinität zum TV-Genre, Streaming-TV-Verhalten und Kabelabonnementstatus) sowie zusätzlichen Daten aus dem CRM-System (Customer Relationship Management) von [!DNL Roku].

* **[!DNL Roku]Content-Targeting:** Private Angebote können Apps nach Genre, Anwendung der App-Blockierungsliste, saisonale und zehnpol-Ereignisse und nur innerhalb von [!DNL The Roku Channel] anzeigen.

## [!DNL Roku] Platzierungen

Erstellen Sie in DSP Kampagnen [ [!DNL Roku]-spezifische Platzierungen](/help/dsp/campaign-management/placements/placement-create.md) mit dem Platzierungstyp &quot;[!UICONTROL Connected TV (Roku)]&quot;. Fügen Sie [!DNL Roku] Platzierungen in [!DNL Roku]-spezifischen Paketen mit definierten Zielen hinzu.

Jede [!DNL Roku] Platzierung muss mindestens einen [!DNL Roku] Deal oder eine Quelle als Ziel haben. Um DSP Zielgruppenabgleich mit [!DNL Roku] zu verwenden, schließen Sie mindestens ein Zielgruppensegment ein, das mit dem deterministischen Datensatz [!DNL Roku] (opted-in) abgeglichen werden kann.

### [!DNL Roku]-Genehmigte Drittanbieter-Tracking-Anbieter

[!DNL Roku] Platzierungen können Drittanbieter-Ereignispixel und Konversionspixel der folgenden Anbieter enthalten: [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] und [!DNL Research Now].

### Best Practices nach Platzierungsstrategie

Im Folgenden finden Sie die empfohlenen Vorgehensweisen für [!DNL Roku]-spezifische Platzierungen.

So maximieren Sie die inkrementelle Reichweite:

* Unterdrücken Sie die angezeigten Zielgruppen in [!DNL Roku O&O], indem Sie Zielgruppen ausschließen, die Sie bereits mit [!DNL The Roku Channel] erreicht haben.

* Unterdrücken Sie die angezeigten Zielgruppen in [!DNL All Roku], indem Sie Zielgruppen ausschließen, die Sie bereits auf der [!DNL Roku] -Plattform erreicht haben.

Für die schnellste Einrichtung:

* Targeting vorhandener, immer genutzter Angebote für [!DNL The Roku Channel] in [[!DNL On Demand] Bestand](/help/dsp/inventory/on-demand-inventory-subscribe.md), um schnell auf den in Ihrem Besitz befindlichen und betriebenen Bestand von [!DNL Roku] zuzugreifen.
* Targeting vorhandener, stets vorhandener Angebote für [!DNL Roku Network] in [[!DNL On Demand] Bestand](/help/dsp/inventory/on-demand-inventory-subscribe.md), um schnell Skalierungen auf der [!DNL Roku]-Plattform zu erzielen.

Maximale Skalierung:

* Passen Sie einen [!DNL Roku] privaten Marktplatz für priorisierten Zugriff auf [!DNL Roku] Angebot zu einem ausgehandelten Preis an.

>[!MORELIKETHIS]
>
>* [Manuelles Erstellen von Details zur Angebots-ID](/help/dsp/inventory/deal-id-create.md)
> * [Registrieren und Anfordern des Zugriffs auf [!DNL On Demand] Premium Inventory Deals](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Erstellen einer Platzierung](/help/dsp/campaign-management/placements/placement-create.md)
