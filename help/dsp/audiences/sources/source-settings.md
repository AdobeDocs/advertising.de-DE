---
title: Einstellungen der Zielgruppenquelle
description: Learn about the settings for audience sources.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Einstellungen der Zielgruppenquelle

*Beta-Funktion*

**[!UICONTROL Data Visibility Level]:** Ob die Segmente einem einzelnen Advertiser mit Zugriff auf das Konto (*[!UICONTROL Advertiser]*) oder allen Advertisern mit Zugriff auf das *[!UICONTROL Account]* zur Verfügung stehen.

**[!UICONTROL Advertiser]:** (Nur Sichtbarkeit auf Advertiser-Ebene) Der Advertiser, für den die Segmente verfügbar sind. Select one from the list of advertisers with access to the account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] sources only) The Adobe CX Enterprise organization ID for the [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** The ID types to which you&#39;ll convert your personally identifiable information (PII). If you select multiple types, the generated segment is populated with values for each selected ID type (such as a [!DNL RampID] and a [!DNL Unified ID2.0] for each email address). Data charges are applied accordingly.

For [!DNL RampID] and [!DNL Unified ID2.0], the vendor looks up each email address to see if an ID already exists and translates the address to a matching ID when available. If an ID doesn&#39;t exist for the address, then it creates a new ID.

>[!NOTE]
>
>You can target only one type of ID in a single placement. To test performance by ID type, [create a separate placement](/help/dsp/campaign-management/placements/placement-create.md) for each ID type in the segment.

* *[!DNL RampID]:* To convert PII to a [!DNL RampID]. You can use [!DNL RampIDs] for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

* *[!DNL Unified ID2.0] (Beta):* To convert PII to a [Unified ID 2.0](https://unifiedid.com) ID for retargeting logging-in users.

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** The terms of service agreement for converting PII to universal IDs. You or another user in the DSP account must accept the terms once before you can convert data to a new ID type. For customers with managed service contracts, your Adobe Account Team will get your consent and accept the terms on your organization&#39;s behalf. To read the terms, click **>**. To accept the terms, scroll to the bottom of the terms and click **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Read-only; generated automatically) The source key you can use to create a destination connection in the customer data platform to push audiences to Advertising DSP. You can copy the value to your clipboard to paste into the destination connection settings or into a file.

>[!MORELIKETHIS]
>
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Manually import authenticated segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=de)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
