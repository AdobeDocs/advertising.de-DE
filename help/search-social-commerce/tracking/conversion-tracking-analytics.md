---
title: Adobe Analytics-Konversions-Tracking
description: Erfahren Sie unter Adobe Advertising, wie Sie das Adobe Analytics-Konversions-Tracking für Ihre Kampagnen verwenden.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: 8deabf2c98901d706acdd035221e8c24e4a1d20d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Adobe Analytics-Konversions-Tracking

*Advertiser nur mit Adobe Advertising-Adobe Analytics-Integration*

Für Advertiser mit einer Adobe Advertising-Adobe Analytics-Integration kann Advertising Cloud Ihre Anzeigenklicks und -impressionen mit den Site-Interaktions- und Konversionsmetriken verbinden, die von [!DNL Analytics] verfolgt werden, wenn Sie eine Umleitung mit Token (`ef_id` -Parameter) in Ihren Klick-Tracking-URLs für Ihre [Angebotseinheiten](/help/search-social-commerce/glossary.md#a-b) verwenden. Die [!DNL Analytics] -Daten werden automatisch über eine tägliche Feed-Datei an Advertising Cloud gesendet.

Weitere Informationen zur Integration finden Sie unter &quot;[Überblick über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/dsp/integrations/analytics/overview.html){target="_blank"}&quot;.

>[!PREREQUISITES]
>
> Die Zeitzonen im Advertiser-Konto für Search, Social und Commerce müssen mit den Report Suites für Search, Social und übereinstimmen. [!DNL Analytics] Wenn sie nicht übereinstimmen, treten Datenabweichungen auf allen Systemen auf.

## Implementierungsübersicht

1. In [!DNL Analytics] ändert Ihr Implementierungsteam für Search, Social und Commerce die folgenden Konfigurationseinstellungen für jede Report Suite:

   * Die Gültigkeit für den `ef_id` [!DNL eVar] wird geändert und entspricht dem Klick-Lookback-Fenster des Advertisers für Adobe Advertising.

   * Die Adobe Advertising-Benutzer-ID.

   * Standardmäßige und benutzerdefinierte Ereignisse, die für die Optimierung verwendet werden sollen.

1. In Search, Social und Commerce Ihr Implementierungsteam:

   1. Synchronisiert die Hierarchie der bestehenden Anzeigennetzwerkkonten mit Search, Social und Commerce.

   1. Fügt Umleitungen mit &quot;`ef_id`&quot;-Token hinzu, das an die Tracking-URLs übergeben und an das Werbenetzwerk gesendet wird.

   Dieser Schritt leitet eine Umleitung zum Adobe Advertising-Tracking-Server voraus (mit Ausnahme von [!DNL Google Ads] - und [!DNL Microsoft Advertising] -Anzeigen in Browsern, die paralleles Tracking unterstützen) und fügt der URL zum Zeitpunkt des Anzeigenklicks einen dynamisch ausgefüllten Parameter &quot;ef_id&quot;hinzu. Wenn die parallele Verfolgung angewendet wird, werden Endbenutzer direkt von Ihrer Anzeige an Ihre endgültige URL gesendet und Ihre Tracking-Vorlage-URL (mit Klick-Messung) wird im Hintergrund geladen.

Sobald die Integration abgeschlossen ist, erhält Search, Social und Commerce automatisch alle auf der Seite erfassten Ereignisdaten, die in [!DNL Analytics] für die konfigurierten Report Suites verfolgt wurden.

>[!MORELIKETHIS]
>
>* [Konversions-Tracking-Optionen](conversion-tracking-about.md)
