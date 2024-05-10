---
title: Adobe Analytics-Konversions-Tracking
description: Erfahren Sie unter Adobe Advertising, wie Sie das Adobe Analytics-Konversions-Tracking für Ihre Kampagnen verwenden.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Adobe Analytics-Konversions-Tracking

*Advertiser nur mit Adobe Advertising-Adobe Analytics-Integration*

Für Advertiser mit einer Adobe Advertising-Adobe Analytics-Integration kann Advertising Cloud Ihre Anzeigenklicks und -impressionen mit den Site-Interaktions- und Konversionsmetriken verbinden, die von [!DNL Analytics] bei Verwendung einer Umleitung mit einem Token (`ef_id` -Parameter) in Ihren Klick-Tracking-URLs für Ihre [Bid-Einheiten](/help/search-social-commerce/glossary.md#a-b). Die [!DNL Analytics] Daten werden automatisch über eine tägliche Feed-Datei an Advertising Cloud gesendet.

Siehe &quot;[Übersicht über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot;, um weitere Informationen zur Integration zu erhalten.

>[!PREREQUISITES]
>
> Zeitzonen im Advertiser-Konto für Search, Social und Commerce, die [!DNL Analytics] Report Suites und die Anzeigennetzwerkkonten müssen übereinstimmen. Wenn sie nicht übereinstimmen, treten Datenabweichungen auf allen Systemen auf.

## Implementierungsübersicht

1. In [!DNL Analytics], ändert Ihr Implementierungsteam für Search, Social und Commerce die folgenden Konfigurationseinstellungen für jede Report Suite:

   * Der Ablauf für die `ef_id` [!DNL eVar] wurde geändert, um dem Klick-Lookback-Fenster des Advertisers für Adobe Advertising zu entsprechen.

   * Die Adobe Advertising-Benutzer-ID.

   * Standardmäßige und benutzerdefinierte Ereignisse, die für die Optimierung verwendet werden sollen.

1. In Search, Social und Commerce Ihr Implementierungsteam:

   1. Synchronisiert die Hierarchie der bestehenden Anzeigennetzwerkkonten mit Search, Social und Commerce.

   1. Fügt Umleitungen mit hinzu`ef_id`&quot; Token, das an die Tracking-URLs übergeben und an das Werbenetzwerk sendet.

   Dieser Schritt leitet eine Umleitung zum Adobe Advertising-Tracking-Server voraus (mit Ausnahme von [!DNL Google Ads] und [!DNL Microsoft Advertising] Anzeigen in Browsern, die paralleles Tracking unterstützen) und fügt der URL zum Zeitpunkt des Anzeigenklicks einen dynamisch ausgefüllten Parameter &quot;ef_id&quot;hinzu. Wenn die parallele Verfolgung angewendet wird, werden Endbenutzer direkt von Ihrer Anzeige an Ihre endgültige URL gesendet und Ihre Tracking-Vorlage-URL (mit Klick-Messung) wird im Hintergrund geladen.

Sobald die Integration abgeschlossen ist, erhält Search, Social und Commerce automatisch alle auf der Seite erfassten Ereignisdaten [!DNL Analytics] für die Report Suites, die konfiguriert wurden.

>[!MORELIKETHIS]
>
>* [Konversions-Tracking-Optionen](conversion-tracking-about.md)
