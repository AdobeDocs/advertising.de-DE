---
title: '[!DNL Analytics] Daten in Adobe Advertising'
description: '[!DNL Analytics] Daten in Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Analytics] Daten in Adobe Advertising

*Werbetreibende, die nur über eine Adobe Advertising-Adobe Analytics-Integration verfügen*

## Analytics-Segmente

Alle in erstellten Segmente [!DNL Analytics] und in Experience Cloud veröffentlicht.

Es dauert 24 bis 48 Stunden, bis neue Segmente im Adobe Advertising angezeigt werden. Aktualisierungen vorhandener Segmente werden innerhalb von etwa acht Stunden synchronisiert.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Metriken zur Site-Interaktion

>[!NOTE]
>
>* [!DNL Analytics] übergibt Ereignisse für die EF ID [!DNL eVar] in den Adobe Advertising.  Die Standardintegration unterstützt nicht das Senden berechneter Metriken oder anderer Dimensionen ([!DNL eVars]) in den Adobe Advertising. Wenn die berechnete Metrik jedoch vollständig in einem benutzerspezifischen Ereignis erfasst werden kann, kann der Adobe Advertising das benutzerspezifische Ereignis erfassen.
>* [!DNL Analytics] übergibt Daten stündlich an den Adobe Advertising.

* [!UICONTROL Timespent_secs_1stvisit]: Die Anzahl der Sekunden, die während des ersten Besuchs des Besuchers auf der Site verbracht wurden.
* [!UICONTROL Timespent_secs_total]: Die Gesamtanzahl der Sekunden, die innerhalb des Klick-Lookback-Fensters bei allen Besuchen auf der Site verbracht wurden.
* [!UICONTROL Pageviews_1stvisit]: Die Anzahl der Seitenansichten auf der Site während des ersten Besuchs des Besuchers.
* [!UICONTROL Pageviews_total]: Die Gesamtzahl der Seitenansichten auf der Site bei allen Besuchen im Klick-Lookback-Fenster.
* [[!UICONTROL Bounces] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: Die Häufigkeit, mit der [!DNL Analytics] erfasst [!UICONTROL EF ID].

## Konversionsmetriken

[!DNL Analytics] übergibt täglich Konversionsmetriken an den Adobe Advertising.

### Standardkonversionsmetriken

* [[!UICONTROL Revenue] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Benutzerspezifische Konversionsmetriken

Diese Metriken sind spezifisch für die Report Suite, sodass die verfügbaren Metriken für jeden Kunden und jede Report Suite variieren.

### Benutzerdefinierte Konversionsmetriken, die aus [!DNL eVars] und [!DNL Props]

Die verfügbaren Metriken variieren für jeden Kunden. Siehe &quot;[Konversionsmetriken aus Adobe Analytics erstellen [!DNL eVars] und [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Reservierte Konversionsmetriken

Diese Metriken sind spezifisch für die Report Suite, sodass die verfügbaren Metriken für jeden Kunden und jede Report Suite variieren.

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
