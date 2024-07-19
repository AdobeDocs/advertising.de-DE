---
title: Manuelles Importieren authentifizierter Segmente aus  [!DNL LiveRamp]
description: Erfahren Sie mehr über das Aktivieren authentifizierter Zielgruppen über  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]

*Beta-Funktion*

Sie können authentifizierte [!DNL LiveRamp]-Segmente manuell über das Dashboard [!DNL LiveRamp] [!DNL Connect] an DSP senden. Sie können importierte Segmente für Platzierungs-Targeting verwenden. Für Erstanbietersegmente betragen die Gebühren 0,15 USD pro gesendeter Display-Anzeigenimpressionen und 0,25 USD pro bereitgestellter Videoanzeigenimpressionen.

Das Zuordnen und Hochladen von Segmenten für jeden Importauftrag kann bis zu sieben Tage dauern.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Führen Sie die folgenden Schritte im Dashboard [!DNL Connect] aus:

   1. Aktivieren Sie die Zielkachel **[!DNL AAC API 1P Onboarding]**.

   1. Setzen Sie [!DNL Identifier Settings] nur auf **[!DNL Ramp ID]**.

      ![Bezeichnereinstellungen](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Optional) Wenn Sie weiterhin Cookie-basierte IDs empfangen möchten, erstellen Sie eine zweite [!DNL AAC API 1P Onboarding] Zielkachel mit den ausgewählten Optionen &quot;[!DNL Cookies]&quot;, &quot;[!DNL IDFA]&quot;und &quot;[!DNL AAID]&quot;.

   1. Überprüfen Sie in Ihrer Zielgruppenbibliothek (die beim Erstellen oder Bearbeiten einer Zielgruppe über [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen verfügbar ist), ob die gesamte Segmentanzahl importiert wurde.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
