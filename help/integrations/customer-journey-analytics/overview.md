---
title: Überblick über die Integration zwischen Adobe Advertising und Adobe Customer Journey Analytics
description: Erfahren Sie mehr über Optionen zur Integration von Adobe Advertising mit Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: ed3c3b4331b743d0c40f04fb8543c535d80ca1d5
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Überblick über die Integration zwischen Adobe Advertising und Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Werbetreibende mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising ist in Adobe Customer Journey Analytics integriert, um eine bidirektionale Datenfreigabe zu ermöglichen. Sie haben zwei Möglichkeiten, die Integration einzurichten:

* Werbetreibende mit sowohl [!DNL Analytics for Advertising] als auch Customer Journey Analytics verfügen über dieselben Funktionen wie über [!DNL Analytics for Advertising], einschließlich des Hinzufügens von Visualisierungen in Customer Journey Analytics.

  Clickthrough-Ereignisse werden weiterhin mit Adobe Experience Platform Web SDK (`alloy.js`) oder Adobe Experience Cloud Identity Service (`visitorAPI.js`) verfolgt. Werbetreibende mit Advertising DSP verwenden weiterhin ein JavaScript-Snippet, um Durchsichtsereignisse zu verfolgen. Zu den in Customer Journey Analytics verfügbaren Daten gehören:

   * Kampagnenleistungsdaten aus Adobe Advertising

     **Hinweis:** Daten aus [!DNL Apple] und [!DNL Tiktok] sind nicht verfügbar.

   * Website-Aktivität und Konversionen, die von [!DNL Google Ads], [!DNL Microsoft Advertising] und [!DNL Meta] verfolgt werden

   * Attributionsdaten aus [!DNL Analytics], die für die Optimierung und Berichterstellung in Adobe Advertising verwendet werden können

  In diesem Anwendungsfall müssen Sie keine zusätzlichen Schritte ausführen, außer optional [historische Daten für AMO-IDs und EF-IDs zur Verwendung in Customer Journey Analytics zu erfassen](/help/integrations/analytics/rvars-to-evars.md).

* (Künftige Beta-Funktion) Werbetreibende mit Customer Journey Analytics, aber nicht [!DNL Analytics for Advertising] können nativ die folgenden Daten zwischen Adobe Advertising und Customer Journey Analytics austauschen, indem sie Clickthrough- und View-Through-Ereignisse mit dem Adobe Experience Platform Web SDK (`alloy.js`) verfolgen. Daten sind auf Kampagnen-, Anzeigengruppen-, Paket-, Platzierungs- und Keyword-Ebene verfügbar.

   * Kampagnenleistungsdaten aus Adobe Advertising

     **Hinweis:** Daten aus [!DNL Apple] und [!DNL Tiktok] sind nicht verfügbar.

   * Website-Aktivität und Konversionen, die von [!DNL Google Ads], [!DNL Microsoft Advertising] und [!DNL Meta] verfolgt werden

   * Attributionsdaten aus Customer Journey Analytics, die für die Optimierung und Berichterstellung in Adobe Advertising verwendet werden können

  **Hinweis:** Es sind noch keine organischen Daten verfügbar.<!-- Does that belong somewhere up above? -->

  In diesem Anwendungsfall verwenden Sie Web SDK, um Site-Ereignisse (mithilfe von Cookies, Hash-IP-Adressen oder universellen IDs) zu verfolgen und die Site-Ereignisse den Paid-Media-Aktivitäten in [!DNL Google Ads], [!DNL Microsoft Advertising] und [!DNL Meta] sowie Adobe DSP zuzuordnen. Sie verwenden Adobe Experience Platform auch für die Datenerfassung.

## So initiieren Sie eine native Integration zwischen Adobe Advertising und Customer Journey Analytics

Wenden Sie sich an Ihr Adobe-Kundenbetreuerteam, das die für den Einstieg erforderliche Erstkonfiguration durchführt und Sie bei der Planung Ihrer Implementierung und Datennutzung entsprechend den Anforderungen Ihres Unternehmens unterstützt.

>[!MORELIKETHIS]
>
>* [Voraussetzungen](prerequisites.md)
>* (Adobe Analytics-Benutzer) [Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
