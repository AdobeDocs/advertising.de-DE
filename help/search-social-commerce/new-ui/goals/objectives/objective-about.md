---
title: (Neue Benutzeroberfläche) Über Ziele
description: Erfahren Sie mehr über Ziele, um Ihre Geschäftsziele zu erreichen.
feature: Search Objectives, Search Optimization
hide: yes
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
TQID: https://experienceleague.adobe.com/fcdOJhTTB-IML-aownM6-vyYM4NJspKpCraypmuLooE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 516
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Über Ziele

*Beta-Funktion*

Ziele sind Ziele, die ein Werbetreibender setzt, um seine Geschäftsziele zu erreichen, z. B. um Gewinne zu maximieren oder ein bestimmtes Verkaufsziel zu erreichen. Sowohl Advertising Search, Social und Commerce als auch Advertising DSP verwenden Ziele:

* Jedes Portfolio von Search, Social und Commerce muss ein Ziel haben, damit die Optimierungsfunktion Klick- und Umsatzmodelle für das Portfolio erstellen kann.

* In DSP werden Ziele als benutzerdefinierte Ziele für DSP-Konten angezeigt, die mit Such-, Social- und Commerce-Konten verknüpft sind. Jedes Paket, das die Optimierungsziele „Höchste Rendite auf Werbeausgaben (ROAS)“ oder „Niedrigste Kosten pro Akquise (CPA)“ verwendet, muss ein benutzerdefiniertes Ziel enthalten, das zum Erreichen des übergeordneten Optimierungsziels beiträgt.

Ein Ziel besteht aus den zu verfolgenden und zu optimierenden Konversionsmetriken sowie den relativen Gewichtungen dieser Metriken. Angenommen, ein Online-Magazin mit zwei Online-Abonnementebenen und einer Print-Abonnementebene und dem Ziel „Gewinne maximieren“ hat drei Metriken: „einfache Online-Abonnements“ mit einem Wert von 20 USD, „Premium-Online-Abonnements“ mit einem Wert von 40 USD und „Print-Abonnements“ mit einem Wert von 30 USD. Wenn das Magazin eine Gewichtung entsprechend dem einmaligen Geldwert des Abonnements angeben möchte, wären die relativen Gewichtungen der Metriken 1, 2 bzw. 1,5.

Für jede Metrik im Ziel haben Sie folgende Möglichkeiten:

* Konfigurieren Sie separate Gewichtungen für Konversionen von Mobilgeräten aus.

* Kennzeichnen Sie die Metrik als [!UICONTROL Goal] Metrik oder [!UICONTROL Assist] Metrik.

* Wenden Sie Gewichtungsempfehlungen auf die Metriken an.

>[!NOTE]
>* (Suche, Social und Commerce) Sie können ein Ziel mit einem Portfolio verknüpfen, wenn Sie [das Portfolio erstellen](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) oder [die Portfolioeinstellungen ändern](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md).
>* (Werbetreibende mit DSP-Konten, die mit Search-, Social- und Commerce-Konten verknüpft sind) In Advertising DSP können Sie ein Ziel als [benutzerdefiniertes Optimierungsziel](/help/dsp/campaign-management/packages/package-settings.md) für ein Paket mit Geschwindigkeit auf Paketebene auswählen.
>* Sie können dasselbe Ziel für mehrere Search-, Social- und Commerce-Portfolios und/oder mehrere DSP-Pakete verwenden.
>* Die Metriken für die einzelnen Ziele in der [!UICONTROL Objectives] enthalten keine Daten aus DSP.

## Verfügbare Metriken

Sie können eine der folgenden Komponenten in Ihre Ziele einbeziehen:

* Metriken, die Adobe Advertising mithilfe des [Adobe Advertising-Konversionsverfolgungspixels](/help/search-social-commerce/tracking/conversion-tracking-advertising.md) verfolgt.

* [Vom Advertiser verfolgte Metriken aus Konversions-Feed-Dateien](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* (Advertisers mit [!DNL Adobe Analytics for Advertising]) [Konversions- und Site-Interaktionsmetriken wurden aus Adobe Analytics synchronisiert](/help/integrations/analytics/overview.md).

  In Search, Social und Commerce [ die folgenden ](/help/integrations/analytics/analytics-data-in-advertising.md)Metriken zur Website-Interaktion automatisch in die Angebotsalgorithmen des Portfolios einbezogen: `timespent_secs_1stvisit`, `timespent_secs_total`, `pageviews_1stvisit`, `pageviews_total` und `bounces`.

* [!DNL Google] Metriken:<!-- Search only, or might DSP-only clients also have these? -->

   * [[!DNL Google Ads]-getrackte Konversionen](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) von synchronisierten [!DNL Google Ads].

   * (Advertiser mit [[!DNL Google Analytics] Integrationen](/help/search-social-commerce/admin/data-sources/data-source-about.md)) Seitenansichten, Sitzungen, Absprungrate (berechnet als Absprünge/Sitzungen) und Sitzungsdauer.

     In Search, Social und Commerce werden diese Metriken automatisch in die Angebotsalgorithmen des Portfolios einbezogen.

## Option zum Hochladen von Zielen in die Werbenetzwerke

Sie können [ Ziele für die Portfolios des Kontos als Konversionen in  [!DNL Google Ads] /oder  [!DNL Microsoft Advertising]  hochladen](/help/search-social-commerce/tools/objective-upload-to-networks.md) sodass Sie sie für die Optimierung auf Kampagnen- oder Anzeigengruppenebene verwenden können. Wenn Sie die Option aktivieren, übergeben Search, Social und Commerce die gewichteten Umsatzdaten auf EF-ID-Ebene (Klick-ID) täglich an das Werbenetzwerk. Dabei werden alle vom Anzeigennetzwerk verfolgten Metriken weggelassen.

>[!MORELIKETHIS]
>
>* [Erstellen eines Ziels](objective-create.md)
>* [Bearbeiten eines Ziels](objective-edit.md)
>* [Löschen eines Ziels](objective-delete.md)
>* [Wenden Sie Gewichtungsempfehlungen auf ein Ziel an](objective-apply-weight-recommendations.md)
>* [Zieleinstellungen](objective-settings.md)
>* [Leistungsdaten für Ziele herunterladen](objective-download-performance-data.md)
