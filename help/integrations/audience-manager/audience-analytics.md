---
title: '[!DNL Adobe] [!DNL Audience Analytics] für Adobe Advertising-Kunden'
description: Erfahren Sie, wie Sie  [!DNL Adobe] [!DNL Audience Analytics] für Anwendungsfälle in der Werbung verwenden können
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] für Adobe Advertising-Kunden

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) ist eine Integration zwischen Adobe Audience Manager und Adobe Analytics, die es Audience Manager-Kunden ermöglicht, Segmente an [!DNL Analytics] zu senden, um mehr über die Site-Aktivität zu erfahren.

Adobe Advertising-Kunden können von der Verwendung von [!DNL Audience Analytics] profitieren. Die Integration bietet folgende Möglichkeiten:

* Senden Sie Adobe Advertising-Belichtungsdaten direkt an [!DNL Analytics], um die Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität zu bestimmen.

* Ermitteln Sie die Marketing-Kanäle und Site-Einstiegspunkte aus Werbeanzeigen mit Exposition gegenüber dem oberen Trichter.

* Schichtung der Integration mit [!DNL Analytics for Advertising], um demografische Segmente von Drittanbietern aus [Audience Manager  [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) mit [!DNL Analytics for Advertising] Daten zu integrieren, damit Sie mehr über Benutzerprofile erfahren.

  [!DNL Audience Marketplace] bietet Zugriff auf Daten-Feeds von Drittanbietern mit „Aktivierungs“-Abonnementmodellen, die es Käufern ermöglichen, Daten an ein Ziel zu senden. Wenn die Daten in einem [!DNL Analytics] Ziel verwendet werden, werden keine Aktivierungsgebühren erhoben.

* (Werbetreibende mit Advertising DSP) Fügen Sie zusätzliche Belichtungssegmente hinzu, um ganzheitliche Einblicke in das Journey-Management zu erhalten.

  Advertising DSP kann Belichtungsdaten als verwertbare Signale an Audience Manager senden, indem entweder Adobe Experience Platform oder Audience Manager-Impression-Tracking-Pixel implementiert werden. Die Weiterleitung derselben Daten an [!DNL Analytics] ermöglicht eine erweiterte Datenanalyse. Weitere Informationen finden [ unter „Übersicht über die Integration von Adobe Advertising Adobe Audience Manager-Media-Daten mit ](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

Weitere Informationen zu [!DNL Audience Analytics], einschließlich der Voraussetzungen und des Workflows, finden Sie unter &quot;[Übersicht über das Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)&quot;.

## Beispiele für die Verwendung von [!DNL Audience Analytics] mit Adobe Advertising-Daten

Im Folgenden finden Sie Beispiele dafür, wie Sie die kombinierten Daten in [!DNL Analytics] [!DNL Analysis Workspace] verwenden können.

### Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Aktivität anzeigen

Verwenden Sie Audience Manager-Belichtungssegmente, um die Auswirkungen der Site-Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität zu sehen. Fügen Sie Adobe Advertising- oder Makro-IDs von Drittanbietern in Ihre Tracking-Pixel ein, um die Auswirkungen auf einer detaillierten Ebene zu verfolgen, von der Kampagnenebene bis zur Ebene der Site, auf der die Benutzerin oder der Benutzer exponiert war.

Die wichtigsten Vorteile:

* Verfolgen Sie die Belichtung nach Trichter-/Anzeigentypen und verwenden Sie [!DNL Audience Analytics], um Eintrittsraten und Überschneidungen mit der nächsten Phase der Kunden-Journey zu bestimmen.

* Bestimmen Sie die Auswirkung der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität.

* Verbinden Sie [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event -->- und [!DNL Audience Analytics]-<!-- (which includes the user's last exposure event) -->, um eine ganzheitliche Journey zur Site zu bestimmen.

Im Folgenden finden Sie Beispiele für Berichte, die Sie in [!DNL Analysis Workspace] erstellen können.

![Siehe Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Verwenden [!DNL Audience Analytics] Segmentdaten von Drittanbietern für die Benutzerprofilanalyse

Verwenden Sie Audience Manager-Segmente von Drittanbietern, um eine umfassendere Analyse der Interaktion von Benutzenden mit Ihrer Site zu erhalten. Anhand dieser Informationen können Sie neue Drittanbieter-Zielgruppen ermitteln, für die Medien aktiviert werden sollen. Dies geschieht auf Basis der Interaktion von Profilen aus Drittanbietersegmenten mit wichtigen Leistungsindikatoren für die Sites der Medienkampagnen.

>[!TIP]
> Verwenden Sie die `Audiences ID` Audience Manager und `Audiences Name` Dimensionen in allen [!DNL Analytics], wie alle anderen Dimensionen, die [!DNL Analytics] erfasst.

Im Folgenden finden Sie Beispiele für Berichte, die Sie in [!DNL Analysis Workspace] erstellen können.

![Verwendung von Drittanbietersegmenten zur Anreicherung der Benutzerprofilanalyse](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
