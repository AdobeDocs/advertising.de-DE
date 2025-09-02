---
title: Überblick über die Integration zwischen Adobe Advertising und Adobe Customer Journey Analytics
description: Erfahren Sie mehr über Optionen zur Integration von Adobe Advertising mit Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: 14f2bd22c44237a817443d48e798457e6c78312e
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Überblick über die Integration zwischen Adobe Advertising und Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Werbetreibende mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising ist mit Adobe Customer Journey Analytics für bidirektionale Datenfreigabe und Berichterstellung integriert. Sie haben zwei Möglichkeiten, die Integration einzurichten:

* Werbetreibende mit sowohl [!DNL Analytics for Advertising] als auch Customer Journey Analytics verfügen über dieselben Funktionen wie über [!DNL Analytics for Advertising], einschließlich des Hinzufügens von Visualisierungen in Customer Journey Analytics.

  Clickthrough-Ereignisse werden weiterhin mit Adobe Experience Platform Web SDK (`alloy.js`) oder Adobe Experience Cloud Identity Service (`visitorAPI.js`) verfolgt. Werbetreibende mit Advertising DSP verwenden weiterhin ein JavaScript-Snippet, um Durchsichtsereignisse zu verfolgen. Zu den in Customer Journey Analytics verfügbaren Daten gehören:

   * Campaign-Leistungsdaten aus Adobe Advertising in Customer Journey Analytics

   * Site-Aktivität und Konversionen, die von [!DNL Google Ads] und [!DNL Microsoft Advertising] in Customer Journey Analytics verfolgt werden, täglich aktualisiert

   * Attributionsdaten aus [!DNL Analytics] in Adobe Advertising, wo sie zur Optimierung und Berichterstellung verwendet werden können

  In diesem Anwendungsfall sollten Sie weiterhin optional [historische Daten für AMO-IDs und EF-IDs zur Verwendung in Customer Journey Analytics erfassen](/help/integrations/analytics/rvars-to-evars.md).

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* (Künftige Beta-Funktion) Werbetreibende mit Customer Journey Analytics, aber nicht [!DNL Analytics for Advertising] können Daten nativ mithilfe der [Adobe Experience Platform zwischen Adobe Advertising und Customer Journey Analytics  [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de). Sie können Site-Ereignisse mithilfe von Cookies, gehashten IP-Adressen und universellen IDs ([!DNL LiveRamp RampIDs] und ID5-IDs) verfolgen und Site-Ereignisse bezahlter Medienaktivität zuordnen. Die folgenden Daten sind auf Kampagnen-, Anzeigengruppen-, Paket-, Platzierungs- und Keyword-Ebene verfügbar:

   * Campaign-Leistungsdaten aus Adobe Advertising in Customer Journey Analytics

     **Hinweis:** Daten aus [!DNL Apple] und [!DNL Tiktok] sind nicht verfügbar.

   * Website-Aktivität und Konversionen, die von [!DNL Google Ads] und [!DNL Microsoft Advertising] in Customer Journey Analytics verfolgt werden

   * Attributionsdaten aus Customer Journey Analytics in Adobe Advertising, wo sie zur Optimierung und Berichterstellung verwendet werden können

  In diesem Anwendungsfall verwenden Sie Web SDK, um Site-Ereignisse (mithilfe von Cookies, Hash-IP-Adressen oder universellen IDs) zu verfolgen und die Site-Ereignisse den Paid-Media-Aktivitäten in [!DNL Google Ads], [!DNL Microsoft Advertising] und [!DNL Meta] sowie Adobe DSP zuzuordnen. Sie verwenden Adobe Experience Platform auch für die Datenerfassung.

## So initiieren Sie eine native Integration zwischen Adobe Advertising und Customer Journey Analytics

Wenden Sie sich an Ihr Adobe-Kundenbetreuerteam, das die für den Einstieg erforderliche Erstkonfiguration durchführt und Sie bei der Planung Ihrer Implementierung und Datennutzung entsprechend den Anforderungen Ihres Unternehmens unterstützt.

>[!MORELIKETHIS]
>
>* [Voraussetzungen](prerequisites.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Customer Journey Analytics]](ids.md)
>* [Adobe Advertising-Metriken und -Dimensionen in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Adobe Analytics-Benutzer) [Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
