---
title: Verfügbare Makros zum Tracking von URLs
description: Verweisen Sie auf die Makros, die Sie Ihren Landingpage-URLs, Tracking-URLs und Kreativen von Drittanbietern hinzufügen können.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
TQID: https://experienceleague.adobe.com/J5jfIECrL29NngVOulEgHKZBHYqBmoz4680HzEzhIng
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: e1ce403e53ed6da4b16f5d7e4bfbbc50e1317ea8
workflow-type: tm+mt
source-wordcount: 312
ht-degree: 0%

---

# Verfügbare Makros zum Tracking von URLs

<!-- More feature metadata???  -->

Sie können eines der folgenden Makros in Kreative von Drittanbietern, in Tracking-URLs von Drittanbietern für Ihre Erlebnisse und in URLs von Landingpages für Ihre eigene Verwendung einschließen.

Einige der verfügbaren Makros oder ihre Entsprechungen werden automatisch in Experience Tags eingeschlossen.

<!--
 Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |
| `${TC_1}` | Custom tracking code 1. | &mdash; | &mdash; |
| `${TC_2}` | Custom tracking code 2. | &mdash; | &mdash; |
| `${TC_3}` | Custom tracking code 3. | &mdash; | &mdash; |
| `${TC_4}` | Custom tracking code 4. | &mdash; | &mdash; |
| `${TC_5}` | Custom tracking code 5. | &mdash; | &mdash; |
| `${GDPR_ENFORCED}` | Whether GDPR enforcement is required for the bid request. Values: **1** = GDPR should be enforced, **0** = GDPR should not be enforced. | &mdash; | &mdash; |
| `${GDPR_CONSENT}` | The GDPR consent value received from the supply partner in the bid request. Typically: **1** = consent provided, **0** = no consent provided. | &mdash; | &mdash; |
-->

| Makro | Beschreibung | Automatisch in Experience Tags für Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Verfolgt und meldet die Kampagnen-ID aus der DSP | Ja |
| `${TM_SITE_ID_NUM}` | Verfolgt und meldet die Site-ID aus der DSP | Ja |
| `${TM_PLACEMENT_ID_NUM}` | Verfolgt und meldet die Platzierungs-ID aus der DSP | Ja |
| `${TM_AD_ID_NUM}` | Verfolgt und meldet die Anzeigen-ID aus der DSP | Ja |
| `${TM_CREATIVE_ID_NUM}` | Verfolgt und meldet die Kreativ-ID aus der DSP | Nicht zutreffend |
| `${TM_SESSION_ID}` | Verfolgt und meldet die Sitzungs-ID, die mit der Anzeigenanfrage verknüpft ist. Wenn kein Wert zurückgegeben wird, generiert Advertising Creative einen. | Ja |
| `${TM_ACC_EXPERIENCE_ID}` | Verfolgt und meldet die Advertising Creative Experience ID | — |
| `${TM_ACC_CREATIVE_ID}` | Verfolgt und meldet die Kreativ-ID von Advertising Creative | — |
| `${TM_RANDOM}` | Eine zufällig generierte Zahl zwischen 1 und 1.000.000. Wird häufig für Cache-Busting verwendet. | — |
| `${TM_TIMESTAMP}` | Der UNIX®-Zeitstempel (in Sekunden) | — |
| `${TM_CLICK_URL_URLENC}` | (Für Drittanbieter-Anzeigen von Anbietern, die URL-Codierung benötigen) Die codierte Klick-Umleitungs-URL, mit der Anzeigen-Server Anzeigenklicks verfolgen und zählen können. Wenn ein(e) Benutzende(r) auf die Anzeige klickt, wird das Makro aktiviert, und der Klick wird aufgezeichnet und zu Berichtszwecken gezählt. | Ja |
| `${TC_1}` | Benutzerdefinierter Trackingcode 1. | — |
| `${TC_2}` | Benutzerdefinierter Trackingcode 2. | — |
| `${TC_3}` | Benutzerdefinierter Trackingcode 3. | — |
| `${TC_4}` | Benutzerdefinierter Trackingcode 4. | — |
| `${TC_5}` | Benutzerdefinierter Trackingcode 5. | — |
| `${GDPR_ENFORCED}` | Ob für die Angebotsanfrage eine DSGVO-Durchsetzung erforderlich ist. Werte: **1** = Die DSGVO sollte durchgesetzt werden, **0** = die DSGVO sollte nicht durchgesetzt werden. | — |
| `${GDPR_CONSENT}` | Der DSGVO-Einverständniswert, der vom Bereitstellungspartner in der Angebotsanfrage empfangen wurde. Typischerweise: **1** = Einverständnis erteilt, **0** = kein Einverständnis erteilt. | — |

>[!MORELIKETHIS]
>
>* [Standard-Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Kreative Standardeinstellungen](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [Einstellungen für zielgerichtete Erlebnisse](/help/creative/experiences/experience-settings-targeting.md)
>* [Einstellungen für nicht zielgerichtete Erlebnisse](/help/creative/experiences/experience-settings-no-targeting.md)
