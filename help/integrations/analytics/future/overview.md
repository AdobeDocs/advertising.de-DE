---
title: Adobe Advertising-Integrationen mit Adobe Analytics
description: Erfahren Sie, wie Adobe Advertising Daten mit Adobe Analytics austauschen kann und wie Sie die Daten in Search, Social und Commerce verwenden können.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: f2860a4b-f905-4545-bead-1bbc92564592
    internal-label: Advertising integrations
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
    internal-label: Analytics integration
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%
---
# Adobe Advertising-Integrationen mit Adobe Analytics

Sie haben folgende Möglichkeiten, um Adobe Advertising mit Analytics zu integrieren.

## Datenaustausch zwischen [!DNL Analytics] und Adobe Advertising

### [!DNL Analytics] Daten nach Adobe Advertising abrufen

Mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), [!DNL Search, Social, & Commerce] und DSP:

* **[!DNL Analytics]Segmente** Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Segmente eines Werbetreibenden oder einer Agentur, die in [!DNL Analytics] erstellt und in Adobe CX Enterprise veröffentlicht wurden.

* **[!DNL Analytics]Site-Interaktionsmetriken**

* **[!DNL Analytics]standardmäßige, benutzerdefinierte und reservierte Metriken**

### Senden von Adobe Advertising-Daten an [!DNL Analytics]

* **Traffic-Metriken von Adobe Advertising**

* **Dimensionen aus Adobe Advertising**

>[!NOTE]
>
>[!DNL Search, Social, & Commerce] wird diese Funktion für die meisten Werbenetzwerke und Kampagnentypen unterstützt. Weitere Informationen finden Sie im [!DNL Search, Social, & Commerce] unter „Unterstütztes Inventar“.<!-- add link when that's published in ExL -->

### Verwenden [!DNL Analytics] Segmenten zum Erstellen [!DNL Google Ads] Zielgruppen {#audience-manager-google-audiences}

*Opt-in-Werbetreibende nur mit [!DNL Advertising Search, Social, & Commerce]*

<!-- Verify all -->

In [!DNL Search, Social, & Commerce] können Sie [!DNL Google Ads] Zielgruppen für den Google-Kundenabgleich aus Benutzer-IDs erstellen, indem Sie Ihre vorhandenen [!DNL Analytics] verwenden. Dazu gehören Adobe Analytics-Segmente, die in Adobe CX Enterprise veröffentlicht werden, und Segmente, die mit dem Adobe CX Enterprise-[!DNL Audience Library] erstellt werden. Weitere Informationen finden Sie unter &quot;[Erstellen [!DNL Google Ads]  Kundenabgleich von Zielgruppen  [!DNL Adobe]  Zielgruppen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).

[Kundenabgleich-Zielgruppen mit Benutzer-IDs](https://support.google.com/google-ads/answer/9199250) funktionieren wie Zielgruppen, die auf Website-Tags basieren. Eindeutigen Zielgruppenmitgliedern wird jedoch eine Nicht-PII-ID zugewiesen, um gegenüber standardmäßigen Zielgruppen für Kundenabgleich und Website-Tags deutliche Vorteile zu erzielen.

Um die erforderlichen Benutzer-IDs zu erstellen, müssen Sie ein Adobe Advertising JavaScript-Tag <!-- with a user ID parameter -->auf Ihren Websites verwenden. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

![Prozess der Segmenterstellung](/help/integrations/assets/ad_search_user_id_pic.png)

Nach der Erstellung können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen oder Ausschlüsse [&#x200B; Kampagnen oder Anzeigengruppen &#x200B;](#audience-manager-targets).

### Verwenden [!DNL Analytics] Segmente zum Targeting oder Ausschließen von Anzeigen {#analytics-targets}

* (Opt-in-Werbetreibende mit [!DNL Search, Social, & Commerce]) Sie können in Ihren [!DNL Google Ads]-Kampagnen beliebige [!DNL Google Ads]-Zielgruppen [erstellt mit [!DNL Analytics] Segmenten](#audience-manager-google-audiences) als Zielgruppen oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene verwenden.

* (Advertisers mit DSP) Sie können Ihre vorhandenen [!DNL Analytics] als Ziele für Ihre Anzeigenplatzierungen verwenden. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Advertisers mit Advertising Creative) Sie können Ihre vorhandenen [!DNL Analytics] als Ziele für bestimmte Kreative in Ihren Anzeigenerlebnissen verwenden.
