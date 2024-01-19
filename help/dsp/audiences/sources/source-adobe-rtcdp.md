---
title: Workflow für die Verwendung der DSP Integration mit [!DNL Adobe] [!DNL Real-time CDP]
description: Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL Adobe] [!DNL Real-time CDP] Erstanbietersegmente.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Workflow für die Verwendung der DSP Integration mit [!DNL Adobe Real-Time CDP]

1. [Übersetzen von Kundendatensegmenten in DSP [!DNL LiveRamp RampIDs]](source-universal-id.md) die in einer bidbaren Umgebung erkennbar sind.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Erstellen einer Zielgruppenquelle](source-create.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren.

1. Konfigurieren Sie unter Experience Platform eine Advertising DSP-Zielverbindung mit dem [!UICONTROL Source Key] , die in den DSP-Quelleinstellungen generiert wurde.

   Anweisungen zum Aktivieren der DSP-Zielverbindung, Auswählen von Segmenten und Zugreifen auf Kontrollberechtigungen finden Sie unter[Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

Weitere Unterstützung erhalten Sie von Ihrem Adobe-Account-Team oder `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [Authentifizierte Segmente von universellen ID-Partnern aktivieren](source-universal-id.md)
>* [Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen](source-create.md)
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Zielkatalog - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Workflow für die Verwendung der DSP Integration mit [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
