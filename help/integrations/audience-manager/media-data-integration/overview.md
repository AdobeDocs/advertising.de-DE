---
title: Übersicht über das Senden von DSP Media Exposure-Daten an Adobe Audience Manager
description: Erfahren Sie, wie Sie Audience Manager-Ereignispixel verwenden, um Daten auf Impression- und Klick-Ebene aus Advertising DSP-Kampagnen zu erfassen
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Übersicht über das Senden von DSP Media Exposure-Daten an Adobe Audience Manager

*Nur Werbetreibende mit Advertising DSP*

*Werbetreibende mit einer Adobe Advertising-Adobe Audience Manager-Integration*

Advertising DSP-Kunden mit Adobe Audience Manager können Audience Manager-Ereignispixel verwenden, um Daten auf Impression- und Klick-Ebene aus DSP-Kampagnen zu erfassen. Die Ereignispixel senden die Daten als verwertbare Signale an Audience Manager. Diese Signale ermöglichen verschiedene DSP-Anwendungsfälle, z. B. erweiterte Segmentierung, Frequenzverwaltung, Marketing-Analysen und Reporting-Insights.

DSP berechnet Ihnen keine Gebühren für das Senden dieser Signale an Audience Manager. Sie zahlen jedoch standardmäßige Audience Manager-Aufnahmekosten basierend auf Server-Aufrufen pro Audience Manager-Vertrag. Audience Manager entfernt doppelte Ereignisse, die auf zwei verschiedene Arten verfolgt werden, sodass jedes Ereignis nur einmal berechnet wird.

>[!NOTE]
>
> Audience Manager unterstützt auch die Erfassung von Daten aus Anzeigenserver-Protokolldateien, was weniger Flexibilität bietet. Dieser Prozess wird in dieser Dokumentation nicht behandelt.

## Primäre Vorteile

* DSP Campaign-Daten fließen in Echtzeit in Audience Manager ein und Sie können damit regelbasierte Eigenschaften erstellen, mit denen Sie Segmente definieren können.

* Segmente stehen unmittelbar nach der Benutzereigenschaften- und Segmentqualifikation für das Targeting zur Verfügung, wodurch die Zielgruppenbestimmung in Echtzeit unterstützt wird.

* Sie können die Kampagnendaten für Anwendungsfälle wie Frequenzlimitierung für Kreative, Retargeting von Benutzenden, die mit früheren Kampagnen konfrontiert waren, und Analyse des nachgelagerten Site-Verhaltens und der Einstiegspunkte nutzen.

* Die aggregierten Daten bieten eine einheitliche Ansicht der Kampagnenleistung, helfen bei der Identifizierung benutzerdefinierter Konversionspfade und können verwendet werden, um die Ereignissequenz zu verbessern, die über Audience Manager [!DNL Audience Optimization Reports] oder eine [[!DNL Audience Analytics] Integration mit Adobe Analytics) zu Konversionen &#x200B;](/help/integrations/audience-manager/audience-analytics.md).

## Tracking der Daten

Die Impression- und Klickereignis-Pixel von Audience Manager sind Cookie-basiert. Die Pixel erfassen keine Ereignisse, die in Umgebungen ohne Cookies auftreten, z. B. Mobile Apps und Connected TV (CTV).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Impression-Tracking-Pixel

Audience Manager verfolgt die Impressionsdaten für eine Anzeige, wenn Sie der Anzeige ein 1 x L-Pixel großes, transparentes Ereignisverfolgungspixel anhängen. Das Ereignis-Pixel wird jedes Mal geladen, wenn die Anzeige einem Benutzer bereitgestellt und vom Webbrowser geladen wird. Das Pixel wird aus einer Client-spezifischen Subdomain von [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=de) geladen, die eine ältere Domain für Audience Manager ist, und enthält Parameter als Schlüssel-Wert-Paare. Der Ereignisaufruf erfasst Impression- und Konversionsdaten und sendet sie an die Datenerfassungs-Server von Audience Manager.

### Klick-Tracking-Pixel

Audience Manager verfolgt Klicks ähnlich wie Impressions, mit dem Unterschied, dass das transparente Ereignis-Pixel nicht bei jeder Bereitstellung der Anzeige geladen wird. Stattdessen werden die Klickdaten in der Clickthrough-URL der Anzeige verfolgt. Die Anzeige verweist auf eine Client-spezifische Subdomain von [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=de), bei der es sich um eine ältere Domain für Audience Manager handelt, zur Verarbeitung durch die Datenerfassungsserver von Audience Manager. Der Server leitet den Benutzer dann zur gewünschten Landingpage weiter. Die URL enthält Parameter als Schlüssel-Wert-Paare.

>[!NOTE]
>
>Wenn Ihr Unternehmen [!DNL Analytics]-Tracking verwendet, benötigen Sie möglicherweise kein Audience Manager-Klick-Tracking. Adobe Analytics erfasst Klicksignale und kann diese über die [Server-seitige Weiterleitung“ an Audience Manager &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=de).

>[!MORELIKETHIS]
>
>* [Erfassen von Klick- und Impressionsdaten aus Advertising DSP-Kampagnen](collect.md)
>* [Anwendungsfälle](use-cases.md)
