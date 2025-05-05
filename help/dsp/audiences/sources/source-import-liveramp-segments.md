---
title: Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]
description: Erfahren Sie mehr über das Aktivieren authentifizierter Zielgruppen durch [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]

*Beta-Funktion*

Sie können authentifizierte [!DNL LiveRamp] über das Dashboard [!DNL LiveRamp] [!DNL Connect] manuell an DSP senden. Importierte Segmente können für das Platzierungs-Targeting verwendet werden. Für Erstanbietersegmente betragen die Gebühren 0,15 USD pro bereitgestellter Display-Anzeigenimpression und 0,25 USD pro bereitgestellter Video-Anzeigenimpression.

Die Segmentzuordnung und das Hochladen für jeden Importvorgang kann bis zu sieben Tage dauern.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Führen Sie die folgenden Schritte im [!DNL Connect]-Dashboard aus:

   1. Aktivieren Sie die **[!DNL AAC API 1P Onboarding]** der Zielkachel.

   1. Legen Sie [!DNL Identifier Settings] nur auf **[!DNL Ramp ID]** fest.

      ![Kennungseinstellungen](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Optional) Wenn Sie weiterhin Cookie-basierte Kennungen erhalten möchten, erstellen Sie eine zweite [!DNL AAC API 1P Onboarding] Zielkachel, in der &quot;[!DNL Cookies]&quot;, &quot;[!DNL IDFA]&quot; und &quot;[!DNL AAID]&quot; ausgewählt sind.

   1. Überprüfen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob die gesamte Segmentanzahl importiert wurde.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=de)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
