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

## Audience Manager und andere synchronisieren [!DNL Adobe] Segmente für Anzeigen-Targeting

[!DNL Search, Social, & Commerce] und DSP können Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für den gesamten Audience Manager eines Advertisers oder einer Agentur und andere abrufen [!DNL Adobe] Zielgruppen. Diese eindeutige Verbindung steht nur Marketing-Experten zur Verfügung, die Adobe Advertising verwenden. Siehe &quot;[Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting](/help/integrations/audience-manager/import-audiences.md).&quot;

### Audience Manager und andere verwenden [!DNL Adobe] Zu erstellende Segmente [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Opt-in-Advertiser mit [!DNL Advertising Search, Social, & Commerce] only*

Within [!DNL Search, Social, & Commerce], können Sie [!DNL Google Ads] Kundenabgleich von Zielgruppen aus Benutzer-IDs mithilfe Ihrer bestehenden Audience Manager-Segmente mit [!UICONTROL Adobe Media Optimizer (HTTP)] und [!UICONTROL Adobe Media Optimizer Batch Destination] als Ziele. ([!DNL Media Optimizer] ist der frühere Name für [!DNL Search, Social, & Commerce]. Dazu gehören Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden, und Segmente, die mit Adobe Experience Cloud erstellt werden [!DNL Audience Library]. Weitere Informationen finden Sie unter &quot;[Erstellen [!DNL Google Ads] Kundenabgleich-Zielgruppen aus [!DNL Adobe] Zielgruppen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Kundenabgleich von Zielgruppen aus Benutzer-IDs](https://support.google.com/google-ads/answer/9199250) funktioniert wie Website-Tag-basierte Zielgruppen, aber eindeutige Vorteile gegenüber standardmäßigen Kunden-Übereinstimmungen und Website-Tag-basierten Zielgruppen werden eindeutigen Zielgruppenmitgliedern eine Nicht-PII-ID zugewiesen.

Um die erforderlichen Benutzer-IDs zu erstellen, müssen Sie ein Adobe Advertising-JavaScript-Tag verwenden <!-- with a user ID parameter -->auf Ihren Websites. Wenden Sie sich für weitere Informationen an Ihr Adobe-Account-Team.

![Segmenterstellungsvorgang](/help/integrations/assets/ad_search_user_id_pic.png)

Nachdem Sie die Zielgruppen erstellt haben, können Sie sie in [!DNL Google Ads] Kampagnen als [Ziele oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene](#audience-manager-targets).

### Verwenden Sie Audience Manager und andere [!DNL Adobe] Segmente in Target oder Ausschließen von Anzeigen {#audience-manager-targets}

* (Opt-in-Advertiser mit [!DNL Search, Social, & Commerce]) Sie können jede [!DNL Google Ads] Zielgruppen, die [erstellt mit [!DNL Adobe] Segmente](#audience-manager-google-audiences) als Ziele oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene in Ihrem [!DNL Google Ads] Kampagnen.

* (Advertiser mit DSP) Sie können Ihre vorhandene [!DNL Adobe] Segmente als Ziele für Ihre Anzeigenplatzierungen. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Advertiser mit Advertising Creative) Sie können Ihre vorhandene [!DNL Adobe] Segmente als Ziele für bestimmte Kreativinhalte in Ihren Anzeigenerlebnissen.

>[!NOTE]
>
>Weitere Informationen zum Erstellen von Zielgruppen im Audience Manager und Experience Cloud [!DNL Audience Library] Schnittstellen und gängige Anwendungsfälle für verschiedene Zielgruppentypen finden Sie unter[Optionen zur Zielgruppenerstellung](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Senden DSP Medien-Belichtungsdaten an den Audience Manager

*Advertiser nur mit DSP*

DSP Kunden mit Adobe Audience Manager können Daten aus Anzeigenkampagnen mithilfe von Pixelaufrufen an Audience Manager erfassen. Anschließend können Sie die Kampagnendaten zur Erstellung regelbasierter Eigenschaften verwenden, mit denen Sie neue Segmente definieren können, um verschiedene Anwendungsfälle zu ermöglichen, wie z. B. erweiterte Segmentierung, Frequenzverwaltung, Marketing-Analyse und Einblicke in Berichte und Berichte.

Siehe &quot;[Übersicht über das Senden von DSP-Exposure-Daten an Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; für weitere Informationen.

## Mit Audience Analytics können Sie umfassendere Einblicke in die Site-Aktivität erhalten.

Adobe Advertising von Kunden mit [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) kann sowohl Adobe Advertising-getrackte Daten als auch Audience Manager-Segmente an senden [!DNL Analytics] für erweiterte Einblicke in die Site-Aktivität.

Weitere Informationen finden Sie unter &quot;[[!DNL Adobe Audience Analytics] für Adobe Advertising-Kunden](/help/integrations/audience-manager/audience-analytics.md).&quot;
