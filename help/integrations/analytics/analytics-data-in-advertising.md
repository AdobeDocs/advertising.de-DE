---
title: Daten in Adobe Advertising [!DNL Analytics]
description: Daten in Adobe Advertising [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Daten in Adobe Advertising [!DNL Analytics]

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

## Analytics-Segmente

Alle Segmente, die in [!DNL Analytics] erstellt und auf Experience Cloud veröffentlicht wurden.

Es dauert 24-48 Stunden, bis neue Segmente im Adobe Advertising angezeigt werden. Aktualisierungen vorhandener Segmente werden innerhalb von etwa acht Stunden synchronisiert.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Site-Interaktionsmetriken

>[!NOTE]
>
>* [!DNL Analytics] übergibt Ereignisse für die EF ID [!DNL eVar] an Adobe Advertising.  Die Standardintegration unterstützt nicht das Senden von berechneten Metriken oder anderen Dimensionen ([!DNL eVars]) in Adobe Advertising. Wenn die berechnete Metrik jedoch vollständig in einem benutzerspezifischen Ereignis erfasst werden kann, kann das benutzerspezifische Ereignis vom Adobe Advertising aufgenommen werden.
>* [!DNL Analytics] übergibt stündlich Daten an Adobe Advertising.

* [!UICONTROL Timespent_secs_1stvisit]: Die Anzahl der Sekunden, die der Besucher während seines ersten Besuchs auf der Website verbracht hat.
* [!UICONTROL Timespent_secs_total]: Die Gesamtzahl der Sekunden, die auf der Website bei allen Besuchen im ClickLookback-Fenster verbracht wurden.
* [!UICONTROL Pageviews_1stvisit]: Die Anzahl der Seitenansichten auf der Website beim ersten Besuch des Besuchers.
* [!UICONTROL Pageviews_total]: Die Gesamtzahl der Seitenansichten auf der Website für alle Besuche im ClickBack-Fenster.
* [[!UICONTROL Bounces] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: Die Häufigkeit, mit der ein [!UICONTROL EF ID] erfasst [!DNL Analytics].

## Konversionsmetriken

[!DNL Analytics] übergibt Konversionsmetriken täglich an Adobe Advertising.

### Standard-Konversionsmetriken

* [[!UICONTROL Revenue] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Benutzerdefinierte Konversionsmetriken

Diese Metriken sind spezifisch für die Report Suite. Daher variieren die verfügbaren Metriken für jeden Kunden und jede Report Suite.

### Benutzerdefinierte Konversionsmetriken, die aus [!DNL eVars] und [!DNL Props] erstellt wurden

Die verfügbaren Metriken variieren je nach Kunde. Siehe &quot;[ von Konversionsmetriken aus Adobe Analytics erstellen [!DNL eVars] und [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;.

### Reservierte Konversionsmetriken

Diese Metriken sind spezifisch für die Report Suite. Daher variieren die verfügbaren Metriken für jeden Kunden und jede Report Suite.

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
