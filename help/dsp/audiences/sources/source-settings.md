---
title: Einstellungen der Zielgruppenquelle
description: Erfahren Sie mehr über die Einstellungen für Zielgruppenquellen.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Einstellungen der Zielgruppenquelle

**[!UICONTROL Data Visibility Level]:** Gibt an, ob die Segmente für einen einzelnen Advertiser mit Zugriff auf das Konto verfügbar sind (*[!UICONTROL Advertiser]*) oder für alle Advertiser mit Zugriff auf das Konto *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Nur Sichtbarkeit auf Advertiser-Ebene) Der Advertiser, für den die Segmente verfügbar sind. Wählen Sie einen aus der Liste der Advertiser mit Zugriff auf das Konto aus.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] Nur -Quellen) Die Adobe Experience Cloud-Organisations-ID für die [!DNL Adobe Experience Platform] -Konto.

**[!UICONTROL Convert PII to the following IDs]:** ([!DNL ActionIQ] und [!DNL Tealium] Nur Quellen) Der ID-Typ, in den Sie Ihre personenbezogenen Daten (PII) konvertieren möchten. Die Datengebühren werden entsprechend angewendet.

* *[!DNL RampID]:* So konvertieren Sie PII in eine RampID. Wenn Sie *[!DNL RampID]*, werden Ihre Segmente in [!DNL RampIDs] automatisch.

* *[!DNL Unified ID2.0]:* ([!DNL ActionIQ] Nur Quellen) So konvertieren Sie personenbezogene Daten in eine [Unified ID 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]:** (Schreibgeschützt; automatisch generiert) Der Quellschlüssel, mit dem Sie eine Zielverbindung in der Kundendatenplattform erstellen können, um Zielgruppen an Advertising DSP zu leiten. Sie können den Wert in die Zwischenablage kopieren, um ihn in die Zielverbindungseinstellungen oder in eine Datei einzufügen.

>[!MORELIKETHIS]
>
>* [Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen](source-create.md)
>* [Informationen zum Aktivieren authentifizierter Segmente aus Zielgruppen-Quellen](source-about.md)
>* [Authentifizierte Segmente von universellen ID-Partnern aktivieren](source-universal-id.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
