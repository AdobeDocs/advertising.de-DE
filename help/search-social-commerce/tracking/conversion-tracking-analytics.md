---
title: Adobe Analytics-Konversionsverfolgung
description: Erfahren Sie mehr über die Verwendung des Adobe Analytics-Konversions-Trackings für Ihre Kampagnen in Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: a6dc9edb12484499069a68222a3007ae08d9dfea
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Adobe Analytics-Konversionsverfolgung

*Werbetreibende nur mit einer Adobe Advertising-Adobe Analytics-Integration*

Für Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration kann Advertising Cloud Ihre Anzeigenklicks und Impressions mit den Site-Interaktions- und Konversionsmetriken verbinden, die von [!DNL Analytics] verfolgt werden, wenn Sie eine Umleitung mit Token (`ef_id`) in Ihren Klick-Tracking-URLs für Ihre [Gebotseinheiten](/help/search-social-commerce/glossary.md#a-b) verwenden. Die [!DNL Analytics] werden automatisch über eine tägliche Feed-Datei an Advertising Cloud gesendet.

Weitere Informationen [&#x200B; Integration finden Sie unter  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/de/docs/advertising/integrations/analytics/overview){target="_blank"}Übersicht über“.

>[!PREREQUISITES]
>
> Die Zeitzonen im Advertiser-Konto für Suche, Social und Commerce, die [!DNL Analytics] Report Suites und die Konten im Werbenetzwerk müssen übereinstimmen. Wenn sie nicht übereinstimmen, treten Datenvarianzen zwischen den Systemen auf.

## Implementierungsübersicht

1. In [!DNL Analytics] ändert Ihr Implementierungs-Team für Search, Social und Commerce die folgenden Konfigurationseinstellungen für jede Report Suite:

   * Die Gültigkeit für die `ef_id` [!DNL eVar] wird geändert, sodass sie mit dem Click-Lookback-Fenster des Advertisers für das Adobe Advertising übereinstimmt.

   * Die Adobe Advertising-Benutzer-ID.

   * Für die Optimierung zu verwendende Standard- und benutzerdefinierte Ereignisse.

1. In Search, Social und Commerce stellt Ihr Implementierungsteam Folgendes bereit:

   1. Synchronisiert die bestehende Hierarchie der Anzeigennetzwerkkonten in Search, Social und Commerce.

   1. Fügt Umleitungen mit dem Token &quot;`ef_id`&quot; hinzu, die an die Tracking-URLs übergeben werden, und sendet sie an das Werbenetzwerk.

   Dieser Schritt stellt eine Umleitung zum Adobe Advertising-Tracking-Server voran (mit Ausnahme von [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Anzeigen in Browsern, die paralleles Tracking unterstützen) und fügt der URL zum Zeitpunkt des Anzeigenklicks einen dynamisch ausgefüllten Parameter „ef_id“ hinzu. Wenn paralleles Tracking angewendet wird, werden Endbenutzer direkt von Ihrer Anzeige an Ihre endgültige URL gesendet und Ihre Tracking-Vorlagen-URL (mit Klick-Messung) wird im Hintergrund geladen.

Nach Abschluss der Integration erhält Search, Social und Commerce automatisch alle in [!DNL Analytics] für die konfigurierten Report Suites nachverfolgten On-Page-Ereignisdaten.

>[!MORELIKETHIS]
>
>* [Konversionsverfolgungs-Optionen](conversion-tracking-about.md)
