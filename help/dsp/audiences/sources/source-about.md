---
title: Über Erstanbieter-Zielgruppenquellen
description: Erfahren Sie, wie Sie andere Benutzer-IDs in Erstanbietersegmenten in universelle IDs für das Targeting von Cookies konvertieren.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 78ee6ddbfb87915475bcf84bd7cd405a58eccf14
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Über Erstanbieter-Zielgruppenquellen

*Beta-Funktion*

DSP können Erstanbietersegmente erfassen, die aus in Ihrer Kundendatenplattform (CDP) erstellten Hash-E-Mail-IDs bestehen, und sie in Segmente umwandeln, die aus universellen IDs bestehen. Jede resultierende ID basiert auf Personen, und auf ID-Ebene werden die Höchstwerte für die Anzeigenfrequenz<!-- Move that info. to somewhere else? --> angewendet.

Zu den Segmentdetails gehören die Größe jedes universellen ID-Typs sowie die Größe für jeden Gerätetyp, der von Cookies oder Geräte-IDs verfolgt wird.

## Universelle ID-Typen {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Sie können Ihre Erstanbietersegmente in Segmente mit authentifizierten (deterministischen) IDs von den folgenden universellen ID-Partnern übersetzen.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Für das Retargeting angemeldeter Benutzer.

     [!DNL RampIDs] ist für Benutzer in Nordamerika, Australien und Neuseeland verfügbar.

     Die Gebühren betragen 0,15 USD pro gesendeter Display-Anzeigenimpressionen und 0,25 USD pro bereitgestellter Videoanzeigen-Impression.

   * Für Messungen mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com):

   * Für das Retargeting angemeldeter Benutzer.

     [!DNL UID2 IDs] stehen Benutzern im Europäischen Wirtschaftsraum und einigen weiteren Ländern nicht zur Verfügung. Siehe die [ Liste der verbotenen Länder](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Die Gebühren betragen 0,15 USD pro gesendeter Display-Anzeigenimpressionen und 0,25 USD pro bereitgestellter Videoanzeigen-Impression.

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Unterstützte Kundendatenplattformen für Erstanbietersegmente

DSP hat Connectoren für die folgenden CDPs eingerichtet, um Ihre Erstanbietersegmente schnell zu erfassen.

DSP können auch über Batch-, Streaming- oder API-basierte Datenfreigabe eine Verbindung zu allen zusätzlichen CDPs herstellen. Wenden Sie sich zur Integration in eine neue Kundendatenplattform an Ihr Adobe-Account-Team.

### [!DNL Adobe Real-Time Customer Data Platform]

DSP ist ein integriertes *Ziel* für [den  [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), der Teil der Adobe Experience Platform ist.

In [!DNL Real-Time CDP] sind Ziele Verbindungen zu externen Datenplattformen, die eine nahtlose Datenaktivierung ermöglichen. Sie können Ziele verwenden, um Ihre Hash-E-Mail-Adressen für zielgerichtete Werbung in DSP zu aktivieren. Weitere Informationen zu Zielen finden Sie im Experience Platform [Leitfaden zu Zielen](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), einschließlich einer Produktübersicht, Anweisungen zum Erstellen von Ziel-Arbeitsbereichen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) und [Erstellen von Zielverbindungen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) und zum Aktivieren von Daten für Ziele [aktivieren](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).[

Um DSP die Aufnahme Ihrer Erstanbietersegmente mit [!DNL Adobe] [!DNL Real-time CDP] und die Konvertierung Ihrer Hash-E-Mail-Adressen in universelle IDs zu ermöglichen, lesen Sie &quot;[Konvertieren von Benutzer-IDs aus  [!DNL Adobe Real-Time CDP] in universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)&quot;.

### [!DNL ActionIQ]

Sie können die Erstanbieterdaten Ihres Unternehmens aus der [!DNL ActionIQ]-Kundendatenplattform mit DSP teilen, um Ihre Hash-E-Mail-Adressen in universelle IDs für zielgerichtete Werbung in DSP zu konvertieren. Diese Integration muss angepasst werden. Wenden Sie sich für weitere Informationen an Ihr Adobe-Account-Team.

### [!DNL Amperity]

Sie können die Erstanbieterdaten Ihres Unternehmens aus der [!DNL Amperity]-Kundendatenplattform mit DSP teilen, um Ihre Hash-E-Mail-Adressen in universelle IDs für zielgerichtete Werbung in DSP zu konvertieren. Weitere Informationen finden Sie unter &quot;[Konvertieren von Benutzer-IDs aus  [!DNL Amperity] in universelle IDs](/help/dsp/audiences/sources/source-amperity.md)&quot;.

### [!DNL Optimizely]

Sie können die Erstanbieterdaten Ihres Unternehmens aus der [!DNL Optimizely]-Kundendatenplattform mit DSP teilen, um Ihre Hash-E-Mail-Adressen in universelle IDs für zielgerichtete Werbung in DSP zu konvertieren. Weitere Informationen finden Sie unter &quot;[Konvertieren von Benutzer-IDs aus  [!DNL Optimizely] in universelle IDs](/help/dsp/audiences/sources/source-optimizely.md)&quot;.

### [!DNL Tealium]

Sie können die Erstanbieterdaten Ihres Unternehmens über die [!DNL Tealium]-Kundendatenplattform mit [!DNL Amazon Web Services] freigeben. Weitere Informationen zum Konvertieren Ihrer Hash-E-Mail-Adressen in universelle IDs für zielgerichtete Werbung in DSP finden Sie unter &quot;[Konvertieren von Benutzer-IDs aus  [!DNL Tealium] in universelle IDs](/help/dsp/audiences/sources/source-tealium.md)&quot;.

>[!MORELIKETHIS]
>
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Adobe Real-Time CDP] in universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Amperity] in universelle IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Optimizely] in universelle IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Tealium] in universelle IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
