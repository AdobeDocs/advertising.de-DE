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

## Audience Manager und andere [!DNL Adobe]-Segmente für Anzeigen-Targeting synchronisieren

[!DNL Search, Social, & Commerce] und DSP können Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Audience Manager oder Agenturen eines Advertisers und anderer [!DNL Adobe] Zielgruppen abrufen. Diese eindeutige Verbindung steht nur Marketing-Experten zur Verfügung, die Adobe Advertising verwenden. Siehe &quot;[Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting](/help/integrations/audience-manager/import-audiences.md)&quot;.

### Verwenden von Audience Manager und anderen [!DNL Adobe] Segmenten zum Erstellen von [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Advertiser mit aktivierter Funktion &quot;Nur 1&quot;*[!DNL Advertising Search, Social, & Commerce]

Innerhalb von [!DNL Search, Social, & Commerce] können Sie [!DNL Google Ads] Kundenabgleichzielgruppen aus Benutzer-IDs erstellen, indem Sie Ihre bestehenden Audience Manager-Segmente verwenden, die [!UICONTROL Adobe Media Optimizer (HTTP)] und [!UICONTROL Adobe Media Optimizer Batch Destination] als Ziele haben. ([!DNL Media Optimizer] ist ein früherer Name für [!DNL Search, Social, & Commerce].) Dazu gehören Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden, und Segmente, die mit Adobe Experience Cloud [!DNL Audience Library] erstellt werden. Weitere Informationen finden Sie unter &quot;[Erstellen [!DNL Google Ads] von Kundenabgleichs-Zielgruppen aus  [!DNL Adobe] Zielgruppen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

[Die Kundenabgleich-Zielgruppen aus Benutzer-IDs](https://support.google.com/google-ads/answer/9199250) funktionieren wie Website-Tag-basierte Zielgruppen, aber eindeutige Vorteile gegenüber standardmäßigen Kunden-Übereinstimmungen und Website-Tag-basierten Zielgruppen werden eindeutigen Zielgruppenmitgliedern eine Nicht-PII-ID zugewiesen.

Um die erforderlichen Benutzer-IDs zu erstellen, müssen Sie auf Ihren Websites ein Adobe Advertising JavaScript-Tag <!-- with a user ID parameter -->verwenden. Wenden Sie sich für weitere Informationen an Ihr Adobe-Account-Team.

![Prozess zur Segmenterstellung](/help/integrations/assets/ad_search_user_id_pic.png)

Nachdem Sie die Zielgruppen erstellt haben, können Sie sie in [!DNL Google Ads] Kampagnen als Ziele oder Ausschlüsse auf Kampagnenebene oder auf Anzeigengruppenebene verwenden](#audience-manager-targets).[

### Verwenden von Audience Manager und anderen [!DNL Adobe] Segmenten für Target oder Ausschließen von Anzeigen {#audience-manager-targets}

* (Opted-in-Advertiser mit [!DNL Search, Social, & Commerce]) Sie können beliebige [!DNL Google Ads]-Zielgruppen verwenden, die mit [ unter Verwendung von  [!DNL Adobe] Segmenten](#audience-manager-google-audiences) als Ziele auf Kampagnen- oder Anzeigengruppenebene oder Ausschlüsse in Ihren [!DNL Google Ads]-Kampagnen erstellt wurden.

* (Werbetreibende mit DSP) Sie können Ihre vorhandenen [!DNL Adobe]-Segmente als Ziele für Ihre Werbeeinblendungen verwenden. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Werbetreibende mit Advertising Creative) Sie können Ihre vorhandenen [!DNL Adobe]-Segmente als Ziele für bestimmte Kreativinhalte in Ihren Werbeinhalten verwenden.

>[!NOTE]
>
>Weitere Informationen zum Erstellen von Zielgruppen in den Audience Manager- und Experience Cloud [!DNL Audience Library]-Schnittstellen sowie gängige Anwendungsfälle für verschiedene Zielgruppentypen finden Sie unter &quot;[Optionen zur Zielgruppenerstellung](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)&quot;.

## Senden DSP Medien-Belichtungsdaten an den Audience Manager

*Advertiser nur mit DSP*

DSP Kunden mit Adobe Audience Manager können Daten aus Anzeigenkampagnen mithilfe von Pixelaufrufen an Audience Manager erfassen. Anschließend können Sie die Kampagnendaten zur Erstellung regelbasierter Eigenschaften verwenden, mit denen Sie neue Segmente definieren können, um verschiedene Anwendungsfälle zu ermöglichen, wie z. B. erweiterte Segmentierung, Frequenzverwaltung, Marketing-Analyse und Einblicke in Berichte und Berichte.

Weitere Informationen finden Sie unter &quot;[Übersicht über das Senden von DSP-Expositionsdaten an Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

## Mit Audience Analytics können Sie umfassendere Einblicke in die Site-Aktivität erhalten.

Adobe Advertising-Kunden mit [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) können sowohl Adobe Advertising-getrackte Daten als auch Audience Manager-Segmente an [!DNL Analytics] senden, um erweiterte Einblicke in die Site-Aktivität zu erhalten.

Weitere Informationen finden Sie unter &quot;[[!DNL Adobe Audience Analytics] für Adobe Advertising Customers](/help/integrations/audience-manager/audience-analytics.md)&quot;.
