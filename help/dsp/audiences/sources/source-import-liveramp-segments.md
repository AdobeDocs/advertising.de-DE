---
title: Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]
description: Erfahren Sie mehr über das Aktivieren authentifizierter Zielgruppen über [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
TQID: 'https://experienceleague.adobe.com/ln4e1Jmq7vRhOIeg25UwNR8yToni5CuokxAcmEPMwEQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: b4dc2b3d-fdb5-55cd-9190-f1076d8563e4
    internal-label: DSP Audiences
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%
---
# Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]

Sie können authentifizierte [!DNL LiveRamp] über das Dashboard [!DNL LiveRamp] [!DNL Connect] manuell an DSP senden. Importierte Segmente können für das Platzierungs-Targeting verwendet werden. Für Erstanbietersegmente betragen die Gebühren USD 0,15 pro bereitgestellter Display-Anzeigenimpression und USD 0,25 pro bereitgestellter Video-Anzeigenimpression.

Die Segmentzuordnung und das Hochladen für jeden Importvorgang kann bis zu sieben Tage dauern.

<!--
Is this first step relevant for this process?

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
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
>* [Importieren von First-Party-Segmenten aus [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
