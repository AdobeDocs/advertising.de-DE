---
title: Adobe Advertising-Integrationen mit Adobe Audience Manager
description: Erfahren Sie mehr über die verschiedenen Möglichkeiten, wie Adobe Advertising Daten mit Adobe Audience Manager austauschen kann.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Adobe Advertising-Integrationen mit Adobe Audience Manager

Sie können Adobe Advertising wie folgt mit Audience Manager integrieren.

## Synchronisieren von Audience Manager und anderen [!DNL Adobe] für das Anzeigen-Targeting

[!DNL Search, Social, & Commerce] und DSP können Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Audience Manager eines Werbetreibenden oder einer Agentur und andere [!DNL Adobe] Zielgruppen abrufen. Diese eindeutige Verbindung steht nur Marketern zur Verfügung, die Adobe Advertising verwenden. Siehe &quot;[&#x200B; von Adobe Audience Manager-Segmenten für das Anzeigen-Targeting](/help/integrations/audience-manager/import-audiences.md).“

### Verwenden von Audience Manager und anderen [!DNL Adobe] zum Erstellen von [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Opt-in-Werbetreibende nur mit [!DNL Advertising Search, Social, & Commerce]*

Audience Manager In [!DNL Search, Social, & Commerce] können Sie aus Benutzer-IDs [!DNL Google Ads] Zielgruppen für den Kundenabgleich erstellen, indem Sie Ihre bestehenden Benutzersegmente verwenden, die [!UICONTROL Adobe Media Optimizer (HTTP)] und [!UICONTROL Adobe Media Optimizer Batch Destination] als Ziele haben. ([!DNL Media Optimizer] ist ein früherer Name für [!DNL Search, Social, & Commerce].) Dies umfasst Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden, und Segmente, die mit dem Adobe Experience Cloud-[!DNL Audience Library] erstellt werden. Weitere Informationen finden Sie unter &quot;[Erstellen [!DNL Google Ads]  Kundenabgleich von Zielgruppen  [!DNL Adobe]  Zielgruppen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).

[Kundenabgleich-Zielgruppen mit Benutzer-IDs](https://support.google.com/google-ads/answer/9199250) funktionieren wie Zielgruppen, die auf Website-Tags basieren. Eindeutigen Zielgruppenmitgliedern wird jedoch eine Nicht-PII-ID zugewiesen, um gegenüber standardmäßigen Zielgruppen für Kundenabgleich und Website-Tags deutliche Vorteile zu erzielen.

Um die erforderlichen Benutzer-IDs zu erstellen, müssen Sie ein Adobe Advertising-JavaScript-Tag <!-- with a user ID parameter -->auf Ihren Websites verwenden. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

![Prozess der Segmenterstellung](/help/integrations/assets/ad_search_user_id_pic.png)

Nach der Erstellung können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen oder Ausschlüsse [&#x200B; Kampagnen oder Anzeigengruppen &#x200B;](#audience-manager-targets).

### Verwenden von Audience Manager und anderen [!DNL Adobe], um Anzeigen anzusprechen oder auszuschließen {#audience-manager-targets}

* (Opt-in-Werbetreibende mit [!DNL Search, Social, & Commerce]) Sie können in Ihren [!DNL Google Ads]-Kampagnen beliebige [!DNL Google Ads]-Zielgruppen [erstellt mit [!DNL Adobe] Segmenten](#audience-manager-google-audiences) als Zielgruppen oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene verwenden.

* (Advertisers mit DSP) Sie können Ihre vorhandenen [!DNL Adobe] als Ziele für Ihre Anzeigenplatzierungen verwenden. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Advertisers mit Advertising Creative) Sie können Ihre vorhandenen [!DNL Adobe] als Ziele für bestimmte Kreative in Ihren Anzeigenerlebnissen verwenden.

>[!NOTE]
>
>Weitere Informationen zum Erstellen von Zielgruppen in den Benutzeroberflächen für Audience Manager und Experience Cloud-[!DNL Audience Library] sowie zu häufigen Anwendungsfällen für verschiedene Zielgruppentypen finden Sie unter [Optionen zur Zielgruppenerstellung](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=de).

## Senden von DSP Media Exposure-Daten an Audience Manager

*Werbetreibende nur mit DSP*

DSP-Kunden mit Adobe Audience Manager können Daten aus Anzeigenkampagnen mithilfe von Pixelaufrufen an den Audience Manager erfassen. Anschließend können Sie mit den Kampagnendaten regelbasierte Eigenschaften erstellen. Damit können Sie neue Segmente definieren, um verschiedene DSP-Anwendungsfälle zu ermöglichen, z. B. erweiterte Segmentierung, Frequenzverwaltung, Marketing-Analysen und Reporting-Insights.

Weitere Informationen finden [&#x200B; unter „Übersicht über das Senden von DSP Media Exposure-Daten &#x200B;](/help/integrations/audience-manager/media-data-integration/overview.md) Adobe Audience Manager&quot;.

## Bessere Einblicke in Site-Aktivitäten mit Audience Analytics

Adobe Advertising-Kunden mit [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=de) können sowohl Adobe Advertising-getrackte Daten als auch Audience Manager-Segmente an [!DNL Analytics] senden, um erweiterte Einblicke in die Site-Aktivität zu erhalten.

Weitere Informationen finden Sie unter &quot;[[!DNL Adobe Audience Analytics]  für Adobe Advertising-Kunden](/help/integrations/audience-manager/audience-analytics.md).
