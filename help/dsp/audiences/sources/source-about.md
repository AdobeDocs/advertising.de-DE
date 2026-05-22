---
title: Über First-Party-Zielgruppenquellen
description: Erfahren Sie, wie Sie andere Benutzerkennung in Erstanbietersegmenten in universelle IDs für das Cookie-lose Targeting konvertieren können.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
TQID: https://experienceleague.adobe.com/8wdjwhNF-KDspEa1wSYWwlDOJxc3LiyqnSwEE-Fq9bY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 710
ht-degree: 0%

---

# Über First-Party-Zielgruppenquellen

Mit der Funktion „Zielgruppenquelle“ können Sie Erstanbietersegmente, die universelle IDs enthalten, unverändert importieren oder in Segmente mit angegebenen universellen ID-Typen konvertieren:

* Werbetreibende in Australien können First-Party-Segmente importieren, die bereits [!DNL AdFixus] universelle IDs enthalten.

* DSP kann First-Party-Segmente aufnehmen, die aus gehashten E-Mail-IDs, Cookies und Mobile-Advertising-IDs (MAIDs) bestehen, die in zusätzlichen Kundendatenplattformen (CDPs) erstellt wurden, und diese in Segmente konvertieren, die aus [!DNL LiveRamp] [!DNL RampIDs]- und [!DNL Unified ID 2.0 (UID2.0)]-IDs bestehen.

Für alle ID-Typen ist jede resultierende ID personenbasiert und die Begrenzung der Anzeigenfrequenz wird auf ID-Ebene angewendet<!-- Move that info. to somewhere else? -->. Zu den Segmentdetails gehören die Größe jedes universellen ID-Typs und die Größe für jeden Gerätetyp, der von Cookies oder Geräte-IDs verfolgt wird.

## Universelle ID-Typen, in die Sie First-Party-Segmente übersetzen können {#universal-id-types}

<!--
  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Sie können Ihre Erstanbietersegmente aus [!DNL ActionIQ], [!DNL Adobe] [!DNL Real-time CDP], [!DNL Amperity], [!DNL Optimizely] und [!DNL Tealium] in Segmente mit authentifizierten (deterministischen) IDs der folgenden universellen ID-Partner übersetzen.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Für das Retargeting angemeldeter Benutzer.

     [!DNL RampIDs] sind für Benutzer in Nordamerika, Australien und Neuseeland verfügbar.

     Die Gebühren betragen USD 0,15 pro bereitgestellter Display-Anzeigeneindruck und USD 0,25 pro bereitgestellter Video-Anzeigeneindruck.

   * Zur Messung mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com):

   * Für das Retargeting angemeldeter Benutzer.

     [!DNL UID2 IDs] sind im Europäischen Wirtschaftsraum und in einigen weiteren Ländern nicht verfügbar. Siehe die [Liste der Länder, für die ein Verbot gilt](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Die Gebühren betragen USD 0,15 pro bereitgestellter Display-Anzeigeneindruck und USD 0,25 pro bereitgestellter Video-Anzeigeneindruck.

<!--
 Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. Contact your Adobe Account Team for instructions.
-->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Unterstützte Kundendatenplattformen für First-Party-Segmente

DSP hat Connectoren zu den folgenden CDPs eingerichtet, um Ihre First-Party-Segmente schnell aufzunehmen.

DSP kann auch mithilfe von Batch-, Streaming- oder API-basierter Datenfreigabe eine Verbindung zu beliebigen zusätzlichen CDPs herstellen. Wenden Sie sich zur Integration in eine neue CDP an Ihr Adobe-Account-Team.

### [!DNL ActionIQ]

Sie können die First-Party-Daten Ihres Unternehmens über die [!DNL ActionIQ] Kundendatenplattform mit DSP teilen, um Ihre gehashten E-Mail-Adressen in universelle IDs für zielgruppengerechte Werbung in DSP zu konvertieren. Diese Integration muss angepasst werden. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

### [!DNL Adobe Real-Time CDP]

DSP ist ein integriertes *Ziel* für [die [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), das Teil von Adobe Experience Platform ist.

In [!DNL Real-Time CDP] sind Ziele Verbindungen zu externen Datenplattformen, die eine nahtlose Datenaktivierung ermöglichen. Sie können Ziele verwenden, um Ihre gehashten E-Mail-Adressen, Cookies und Mobile-Advertising-IDs für zielgruppengerechte Werbung in DSP zu aktivieren. Weitere Informationen zu Zielen finden Sie im Experience Platform [Handbuch zu Zielen](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), einschließlich einer Übersicht über das Produkt, Anweisungen zum [Erstellen von Ziel-](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) und [Erstellen von &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) und [Aktivieren von Daten für Ziele](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Informationen dazu, wie DSP Ihre [!DNL Adobe] [!DNL Real-time CDP] Erstanbietersegmente aufnehmen und Ihre Hash-E-Mail-Adressen, Cookies und Mobile-Advertising-IDs in universelle IDs konvertieren kann, finden Sie unter &quot;[Konvertieren von Benutzer-IDs  [!DNL Adobe Real-Time CDP]  universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md).

### [!DNL AdFixus]

Australische Werbetreibende können die Advertising DSP-Integration mit [!DNL AdFixus] verwenden, um First-Party-Segmente zu importieren, die [!DNL AdFixus] universelle IDs enthalten. Dieser Pfad ist nicht mit der Übersetzung von Hash-E-Mail-IDs oder MAIDs innerhalb eines CDP-Connectors in [!DNL RampIDs] oder [!DNL UID2]-IDs identisch. Weitere Informationen finden Sie unter [Importieren von Erstanbietersegmenten aus [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md).

### [!DNL Amperity]

Sie können die First-Party-Daten Ihres Unternehmens über die [!DNL Amperity] Kundendatenplattform mit DSP teilen, um Ihre gehashten E-Mail-Adressen in universelle IDs für zielgruppengerechte Werbung in DSP zu konvertieren. Weitere Informationen finden Sie unter &quot;[Konvertieren von Benutzer-IDs  [!DNL Amperity]  universelle IDs](/help/dsp/audiences/sources/source-amperity.md)&quot;.

### [!DNL Optimizely]

Sie können die First-Party-Daten Ihres Unternehmens über die [!DNL Optimizely] Kundendatenplattform mit DSP teilen, um Ihre gehashten E-Mail-Adressen in universelle IDs für zielgruppengerechte Werbung in DSP zu konvertieren. Weitere Informationen finden Sie unter &quot;[Konvertieren von Benutzer-IDs  [!DNL Optimizely]  universelle IDs](/help/dsp/audiences/sources/source-optimizely.md)&quot;.

### [!DNL Tealium]

Sie können die First-Party-Daten Ihres Unternehmens über die [!DNL Tealium]-Kundendatenplattform mithilfe von [!DNL Amazon Web Services] freigeben. Weitere Informationen zum Konvertieren Ihrer gehashten E-Mail-Adressen in universelle IDs für zielgruppengerechte Werbung in DSP finden Sie unter &quot;[Konvertieren von Benutzer [!DNL Tealium] IDs in universelle IDs](/help/dsp/audiences/sources/source-tealium.md)&quot;.

>[!MORELIKETHIS]
>
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Adobe Real-Time CDP]  universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Amperity]  universelle IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Optimizely]  universelle IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Tealium]  universelle IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Importieren von First-Party-Segmenten aus [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
