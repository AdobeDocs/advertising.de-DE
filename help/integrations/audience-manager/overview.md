---
title: Adobe Advertising-Integrationen mit Adobe Audience Manager
description: Erfahren Sie mehr über die verschiedenen Möglichkeiten, wie Adobe Advertising Daten mit Adobe Audience Manager austauschen kann.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
TQID: https://experienceleague.adobe.com/4O4O-DmHhClvSiOSxM9blAEvVslzYzRobEyU6RGeMEQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2: id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 517
ht-degree: 0%

---

# Adobe Advertising-Integrationen mit Adobe Audience Manager

Sie können Adobe Advertising wie folgt mit Audience Manager integrieren.

## Synchronisieren von Audience Manager und anderen [!DNL Adobe] für das Anzeigen-Targeting

[!DNL Search, Social, & Commerce] und DSP können Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Audience Manager-Zielgruppen eines Werbetreibenden oder einer Agentur und andere [!DNL Adobe] Zielgruppen abrufen. Diese eindeutige Verbindung steht nur Marketern zur Verfügung, die Adobe Advertising verwenden. Siehe &quot;[ von Adobe Audience Manager-Segmenten für das Anzeigen-Targeting](/help/integrations/audience-manager/import-audiences.md).“

### Verwenden von Audience Manager und anderen [!DNL Adobe], um [!DNL Google Ads] Zielgruppen zu erstellen {#audience-manager-google-audiences}

*Opt-in-Werbetreibende nur mit [!DNL Advertising Search, Social, & Commerce]*

In [!DNL Search, Social, & Commerce] können Sie aus Benutzer-IDs [!DNL Google Ads] Zielgruppen für den Kundenabgleich erstellen, indem Sie Ihre vorhandenen Audience Manager-Segmente verwenden, die [!UICONTROL Adobe Media Optimizer (HTTP)] und [!UICONTROL Adobe Media Optimizer Batch Destination] als Ziele haben. ([!DNL Media Optimizer] ist ein früherer Name für [!DNL Search, Social, & Commerce].) Dazu gehören Adobe Analytics-Segmente, die in Adobe CX Enterprise veröffentlicht werden, und Segmente, die mit dem Adobe CX Enterprise-[!DNL Audience Library] erstellt werden. Weitere Informationen finden Sie unter &quot;[Erstellen [!DNL Google Ads]  Kundenabgleich von Zielgruppen  [!DNL Adobe]  Zielgruppen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).

[Kundenabgleich-Zielgruppen mit Benutzer-IDs](https://support.google.com/google-ads/answer/9199250) funktionieren wie Zielgruppen, die auf Website-Tags basieren. Eindeutigen Zielgruppenmitgliedern wird jedoch eine Nicht-PII-ID zugewiesen, um gegenüber standardmäßigen Zielgruppen für Kundenabgleich und Website-Tags deutliche Vorteile zu erzielen.

Um die erforderlichen Benutzer-IDs zu erstellen, müssen Sie ein Adobe Advertising JavaScript-Tag <!-- with a user ID parameter -->auf Ihren Websites verwenden. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

![Prozess der Segmenterstellung](/help/integrations/assets/ad_search_user_id_pic.png)

Nach der Erstellung können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen oder Ausschlüsse [ Kampagnen oder Anzeigengruppen ](#audience-manager-targets).

### Verwenden von Audience Manager und anderen [!DNL Adobe], um Anzeigen anzusprechen oder auszuschließen {#audience-manager-targets}

* (Opt-in-Werbetreibende mit [!DNL Search, Social, & Commerce]) Sie können in Ihren [!DNL Google Ads]-Kampagnen beliebige [!DNL Google Ads]-Zielgruppen [erstellt mit [!DNL Adobe] Segmenten](#audience-manager-google-audiences) als Zielgruppen oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene verwenden.

* (Advertisers mit DSP) Sie können Ihre vorhandenen [!DNL Adobe] als Ziele für Ihre Anzeigenplatzierungen verwenden. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Advertisers mit Advertising Creative) Sie können Ihre vorhandenen [!DNL Adobe] als Ziele für bestimmte Kreative in Ihren Anzeigenerlebnissen verwenden.

>[!NOTE]
>
>Weitere Informationen zum Erstellen von Zielgruppen in den [!DNL Audience Library] von Audience Manager und Adobe CX Enterprise sowie zu häufigen Anwendungsfällen für verschiedene Zielgruppentypen finden Sie unter [Optionen zur Zielgruppenerstellung](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).

## Senden von DSP Media Exposure-Daten an Audience Manager

*Nur Werbetreibende mit DSP*

DSP-Kunden mit Adobe Audience Manager können Daten aus Anzeigenkampagnen mithilfe von Pixelaufrufen an Audience Manager erfassen. Anschließend können Sie mit den Kampagnendaten regelbasierte Eigenschaften erstellen. Damit können Sie neue Segmente definieren, um verschiedene DSP-Anwendungsfälle zu ermöglichen, z. B. erweiterte Segmentierung, Frequenzverwaltung, Marketing-Analysen und Reporting-Insights.

Weitere Informationen finden [ unter „Übersicht über das Senden von DSP-](/help/integrations/audience-manager/media-data-integration/overview.md) an Adobe Audience Manager&quot;.

## Bessere Einblicke in Site-Aktivitäten mit Audience Analytics

Adobe Advertising-Kunden mit -[[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) können sowohl von Adobe Advertising verfolgte Daten als auch Audience Manager-Segmente an [!DNL Analytics] senden, um erweiterte Einblicke in die Site-Aktivität zu erhalten.

Weitere Informationen finden Sie unter &quot;[[!DNL Adobe Audience Analytics]  für Adobe Advertising-Kunden](/help/integrations/audience-manager/audience-analytics.md).
