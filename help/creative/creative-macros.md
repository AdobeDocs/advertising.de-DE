---
title: Verfügbare Makros zum Tracking von URLs
description: Verweisen Sie auf die Makros, die Sie Ihren Landingpage-URLs, Tracking-URLs und Kreativen von Drittanbietern hinzufügen können.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
source-git-commit: fe3e991f1fba2944e7a3f8e4930c48c7dbd28770
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Verfügbare Makros zum Tracking von URLs

*Geschlossene Beta-Version*

<!-- More feature metadata??? -->

Sie können eines der folgenden Makros in Kreative von Drittanbietern, in Tracking-URLs von Drittanbietern für Ihre Erlebnisse und in URLs von Landingpages für Ihre eigene Verwendung einschließen.

Einige der verfügbaren Makros oder ihre Entsprechungen werden automatisch in Experience Tags eingeschlossen.

<!-- Later: 

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

-->

| Makro | Beschreibung | Automatisch in Experience Tags für Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Verfolgt und meldet die Kampagnen-ID aus der DSP | Ja |
| `${TM_SITE_ID_NUM}` | Verfolgt und meldet die Site-ID aus der DSP | Ja |
| `${TM_PLACEMENT_ID_NUM}` | Verfolgt und meldet die Platzierungs-ID aus der DSP | Ja |
| `${TM_AD_ID_NUM}` | Verfolgt und meldet die Anzeigen-ID aus der DSP | Ja |
| `${TM_CREATIVE_ID_NUM}` | Verfolgt und meldet die Kreativ-ID aus der DSP | Nicht zutreffend |
| `${TM_SESSION_ID}` | Verfolgt und meldet die Impression-ID aus der DSP. Wenn kein Wert zurückgegeben wird, generiert Advertising Creative einen. | Ja |
| `${TM_ACC_EXPERIENCE_ID}` | Verfolgt und meldet die Advertising Creative Experience ID | — |
| `${TM_ACC_CREATIVE_ID}` | Verfolgt und meldet die Kreativ-ID von Advertising Creative | — |
| `${TM_RANDOM}` | Eine zufällige Zahl zwischen 1 und 1000000 | — |
| `${TM_TIMESTAMP}` | Der UNIX®-Zeitstempel (in Sekunden) | — |
| `${TM_CLICK_URL_URLENC}` | (Für Drittanbieter-Anzeigen von Anbietern, die URL-Codierung benötigen) Die codierte Klick-Umleitungs-URL, mit der Anzeigen-Server Anzeigenklicks verfolgen und zählen können. Wenn der/die Benutzende auf die Anzeige klickt, wird das Makro aktiviert, und der Klick wird aufgezeichnet und zu Berichtszwecken gezählt. | Ja |

>[!MORELIKETHIS]
>
>* [Standard-Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Kreative Standardeinstellungen](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [Einstellungen für zielgerichtete Erlebnisse](/help/creative/experiences/experience-settings-targeting.md)
>*[Einstellungen für nicht zielgerichtete Erlebnisse](/help/creative/experiences/experience-settings-no-targeting.md)
