---
title: Adobe Advertising-Integrationen mit Adobe Analytics
description: Erfahren Sie, wie Adobe Advertising Daten mit Adobe Analytics austauschen kann und wie Sie die Daten in Search, Social und Commerce verwenden können.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 06996ee9eb635fe204c0c3938e6937e8871c8a90
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Adobe Advertising-Integrationen mit Adobe Analytics

Sie können Adobe Advertising auf folgende Weise in Analytics integrieren.

## Daten tauschen zwischen [!DNL Analytics] und Adobe Advertising

### Pull [!DNL Analytics] Daten in Adobe Advertising

Mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] und DSP abrufen:

* **[!DNL Analytics]Segmente:**  Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Segmente eines Advertisers oder einer Agentur, die in [!DNL Analytics] und in Experience Cloud veröffentlicht.

* **[!DNL Analytics]Site-Interaktionsmetriken**

* **[!DNL Analytics]standardmäßige, benutzerdefinierte und reservierte Metriken**

### Senden von Adobe Advertising-Daten an [!DNL Analytics]

* **Traffic-Metriken aus Adobe Advertising**

* **Dimensionen von Adobe Advertising**

>[!NOTE]
>
>Für [!DNL Search, Social, & Commerce]festgelegt ist, wird diese Funktion für die meisten Anzeigennetzwerke und Kampagnentypen unterstützt. Siehe &quot;Unterstütztes Inventar&quot;im [!DNL Search, Social, & Commerce] Handbuch für weitere Informationen.<!-- add link when that's published in ExL -->

### Verwendung [!DNL Analytics] Zu erstellende Segmente [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Opt-in-Advertiser mit [!DNL Advertising Search, Social, & Commerce] only*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], können Sie [!DNL Google Ads] Google-Kundenabgleich von Zielgruppen aus Benutzer-IDs mithilfe Ihrer vorhandenen [!DNL Analytics] Segmente. Dazu gehören Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden, und Segmente, die mit Adobe Experience Cloud erstellt werden [!DNL Audience Library]. Weitere Informationen finden Sie in der produktinternen Hilfe unter [!DNL Search, Social, & Commerce].

[Kundenabgleich von Zielgruppen aus Benutzer-IDs](https://support.google.com/google-ads/answer/9199250) funktioniert wie Website-Tag-basierte Zielgruppen, aber eindeutige Vorteile gegenüber standardmäßigen Kunden-Übereinstimmungen und Website-Tag-basierten Zielgruppen werden eindeutigen Zielgruppenmitgliedern eine Nicht-PII-ID zugewiesen.

Um die erforderlichen Benutzer-IDs zu erstellen, müssen Sie ein Adobe Advertising JavaScript-Tag verwenden <!-- with a user ID parameter -->auf Ihren Websites. Wenden Sie sich für weitere Informationen an Ihr Adobe Account Team.

![Segmenterstellungsvorgang](/help/integrations/assets/ad_search_user_id_pic.png)

Nachdem Sie die Zielgruppen erstellt haben, können Sie sie in [!DNL Google Ads] Kampagnen als [Ziele oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene](#audience-manager-targets).

### Verwendung [!DNL Analytics] Segmente in Target oder Ausschließen von Anzeigen {#analytics-targets}

* (Opt-in-Advertiser mit [!DNL Search, Social, & Commerce]) Sie können jede [!DNL Google Ads] Zielgruppen, die [erstellt mit [!DNL Analytics] Segmente](#audience-manager-google-audiences) als Ziele oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene in Ihrem [!DNL Google Ads] Kampagnen.

* (Advertiser mit DSP) Sie können Ihre vorhandene [!DNL Analytics] Segmente als Ziele für Ihre Anzeigenplatzierungen. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Advertiser mit Advertising Creative) Sie können Ihre vorhandene [!DNL Analytics] Segmente als Ziele für bestimmte Kreativinhalte in Ihren Anzeigenerlebnissen.
