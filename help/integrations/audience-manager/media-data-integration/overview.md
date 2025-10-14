---
title: Übersicht über das Senden von DSP Media Exposure-Daten an Adobe Audience Manager
description: Erfahren Sie, wie Sie Audience Manager-Ereignispixel verwenden, um Daten auf Impression- und Klick-Ebene aus Advertising DSP-Kampagnen zu erfassen
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: c204955ec48826d00a5f78e5be4849f53d09e224
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Übersicht über das Senden von DSP Media Exposure-Daten an Adobe Audience Manager

*Nur Werbetreibende mit Advertising DSP*

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Audience Manager-Integration*

Advertising DSP-Kunden mit Adobe Audience Manager können Audience Manager-Ereignispixel verwenden, um Daten auf Impression- und Klick-Ebene aus DSP-Kampagnen zu erfassen. Die Ereignispixel senden die Daten als aktionsfähige Signale an den Audience Manager. Diese Signale ermöglichen verschiedene DSP-Anwendungsfälle, z. B. erweiterte Segmentierung, Frequenzverwaltung, Marketing-Analysen und Reporting-Erkenntnisse.

DSP lädt Sie nicht auf, diese Signale an den Audience Manager zu senden. Sie zahlen jedoch die Standardkosten für die Aufnahme von Audience Manager auf der Grundlage von Server-Aufrufen pro Audience Manager. Audience Manager entfernt doppelte Ereignisse, die auf zwei verschiedene Arten verfolgt werden, sodass jedes Ereignis nur einmal berechnet wird.

>[!NOTE]
>
> Audience Manager unterstützt auch die Erfassung von Daten aus den Protokolldateien des Anzeigenservers, was weniger Flexibilität bietet. Dieser Prozess wird in dieser Dokumentation nicht behandelt.

## Primäre Vorteile

* DSP-Kampagnendaten fließen in Echtzeit in den Audience Manager und Sie können damit regelbasierte Eigenschaften erstellen, mit denen Sie Segmente definieren können.

* Segmente stehen unmittelbar nach der Benutzereigenschaften- und Segmentqualifikation für das Targeting zur Verfügung, wodurch die Zielgruppenbestimmung in Echtzeit unterstützt wird.

* Sie können die Kampagnendaten für Anwendungsfälle wie Frequenzlimitierung für Kreative, Retargeting von Benutzenden, die mit früheren Kampagnen konfrontiert waren, und Analyse des nachgelagerten Site-Verhaltens und der Einstiegspunkte nutzen.

* Die aggregierten Daten bieten eine einheitliche Ansicht der Kampagnenleistung, helfen bei der Identifizierung benutzerdefinierter Konversionspfade und können verwendet werden, um die Ereignissequenz zu verbessern, die zu Konversionen durch Audience Manager-[!DNL Audience Optimization Reports] oder durch eine [[!DNL Audience Analytics] Integration mit Adobe Analytics) &#x200B;](/help/integrations/audience-manager/audience-analytics.md).

## So werden die Daten verfolgt

Die Audience Manager-Impression- und Klickereignis-Pixel sind Cookie-basiert. Die Pixel erfassen keine Ereignisse, die in Umgebungen ohne Cookies auftreten, z. B. Mobile Apps und Connected TV (CTV).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Impression-Tracking-Pixel

Der Audience Manager verfolgt die Impressionsdaten für eine Anzeige, wenn Sie ein 1-Pixel-transparentes Ereignis-Tracking-Pixel an die Anzeige anhängen. Das Ereignis-Pixel wird jedes Mal geladen, wenn die Anzeige einem Benutzer bereitgestellt und vom Webbrowser geladen wird. Das Pixel wird aus einer Client-spezifischen Subdomain von [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=de) geladen, bei der es sich um eine ältere Domain für Audience Manager handelt, und enthält Parameter als Schlüssel-Wert-Paare. Der Ereignisaufruf erfasst Impression- und Konversionsdaten und sendet sie an die Datenerfassungsserver des Audience Managers.

### Klick-Tracking-Pixel

Der Audience Manager verfolgt Klicks ähnlich wie Impressions, mit dem Unterschied, dass er nicht jedes Mal das Transparenzereignis-Pixel lädt, wenn die Anzeige geschaltet wird. Stattdessen werden die Klickdaten in der Clickthrough-URL der Anzeige verfolgt. Die Anzeige verweist auf eine Client-spezifische Subdomain von [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=de), bei der es sich um eine ältere Domain für Audience Manager handelt, zur Verarbeitung durch die Datenerfassungsserver des Audience Managers. Der Server leitet den Benutzer dann zur gewünschten Landingpage weiter. Die URL enthält Parameter als Schlüssel-Wert-Paare.

>[!NOTE]
>
>Wenn Ihr Unternehmen [!DNL Analytics]-Tracking verwendet, benötigen Sie möglicherweise kein Audience Manager-Klick-Tracking. Adobe Analytics erfasst Klicksignale und kann diese über die [Server-seitige Weiterleitung“ an &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=de) Audience Manager senden.

>[!MORELIKETHIS]
>
>* [Erfassen von Klick- und Impressionsdaten aus Advertising DSP-Kampagnen](collect.md)
>* [Anwendungsfälle](use-cases.md)
