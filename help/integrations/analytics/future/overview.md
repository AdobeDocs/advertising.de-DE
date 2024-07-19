---
title: Adobe Advertising-Integrationen mit Adobe Analytics
description: Erfahren Sie, wie Adobe Advertising Daten mit Adobe Analytics austauschen kann und wie Sie die Daten in Search, Social und Commerce verwenden können.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Adobe Advertising-Integrationen mit Adobe Analytics

Sie können Adobe Advertising wie folgt in Analytics integrieren.

## Daten zwischen [!DNL Analytics] und Adobe Advertising austauschen

### [!DNL Analytics] Daten in Adobe Advertising abrufen

Mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), [!DNL Search, Social, & Commerce] und DSP ziehen Sie ein:

* **[!DNL Analytics]Segmente:** Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Segmente eines Advertisers oder einer Agentur, die in [!DNL Analytics] erstellt und auf Experience Cloud veröffentlicht wurden.

* **[!DNL Analytics]Site-Interaktionsmetriken**

* **[!DNL Analytics]standardmäßige, benutzerdefinierte und reservierte Metriken**

### Adobe Advertising-Daten an [!DNL Analytics] senden

* **Traffic-Metriken von Adobe Advertising**

* **Dimensionen von Adobe Advertising**

>[!NOTE]
>
>Für [!DNL Search, Social, & Commerce] wird diese Funktion für die meisten Anzeigennetzwerke und Kampagnentypen unterstützt. Weitere Informationen finden Sie unter &quot;Unterstützter Bestand&quot;im [!DNL Search, Social, & Commerce]-Handbuch.<!-- add link when that's published in ExL -->

### Verwenden Sie [!DNL Analytics] Segmente zum Erstellen von [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Advertiser mit aktivierter Funktion &quot;Nur 1&quot;*[!DNL Advertising Search, Social, & Commerce]

<!-- Verify all -->

Innerhalb von [!DNL Search, Social, & Commerce] können Sie [!DNL Google Ads] Google-Kundenabgleichzielgruppen aus Benutzer-IDs mithilfe Ihrer vorhandenen [!DNL Analytics]-Segmente erstellen. Dazu gehören Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden, und Segmente, die mit Adobe Experience Cloud [!DNL Audience Library] erstellt werden. Weitere Informationen finden Sie unter &quot;[Erstellen [!DNL Google Ads] von Kundenabgleichs-Zielgruppen aus  [!DNL Adobe] Zielgruppen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

[Die Kundenabgleich-Zielgruppen aus Benutzer-IDs](https://support.google.com/google-ads/answer/9199250) funktionieren wie Website-Tag-basierte Zielgruppen, aber eindeutige Vorteile gegenüber standardmäßigen Kunden-Übereinstimmungen und Website-Tag-basierten Zielgruppen werden eindeutigen Zielgruppenmitgliedern eine Nicht-PII-ID zugewiesen.

Um die erforderlichen Benutzer-IDs zu erstellen, müssen Sie auf Ihren Websites ein Adobe Advertising JavaScript-Tag <!-- with a user ID parameter -->verwenden. Wenden Sie sich für weitere Informationen an Ihr Adobe-Account-Team.

![Prozess zur Segmenterstellung](/help/integrations/assets/ad_search_user_id_pic.png)

Nachdem Sie die Zielgruppen erstellt haben, können Sie sie in [!DNL Google Ads] Kampagnen als Ziele oder Ausschlüsse auf Kampagnenebene oder auf Anzeigengruppenebene verwenden](#audience-manager-targets).[

### Verwenden von [!DNL Analytics] Segmenten zum Targeting oder Ausschließen von Anzeigen {#analytics-targets}

* (Opted-in-Advertiser mit [!DNL Search, Social, & Commerce]) Sie können beliebige [!DNL Google Ads]-Zielgruppen verwenden, die mit [ unter Verwendung von  [!DNL Analytics] Segmenten](#audience-manager-google-audiences) als Ziele auf Kampagnen- oder Anzeigengruppenebene oder Ausschlüsse in Ihren [!DNL Google Ads]-Kampagnen erstellt wurden.

* (Werbetreibende mit DSP) Sie können Ihre vorhandenen [!DNL Analytics]-Segmente als Ziele für Ihre Werbeeinblendungen verwenden. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Werbetreibende mit Advertising Creative) Sie können Ihre vorhandenen [!DNL Analytics]-Segmente als Ziele für bestimmte Kreativinhalte in Ihren Werbeinhalten verwenden.
