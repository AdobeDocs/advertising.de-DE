---
title: '[!DNL Adobe] [!DNL Audience Analytics] für Adobe Advertising-Kunden'
description: Erfahren Sie, wie Sie [!DNL Adobe] [!DNL Audience Analytics] für Anwendungsfälle in der Werbung verwenden
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
TQID: 'https://experienceleague.adobe.com/XFaacUNElL25w5SMS5fzWkfRwnXr2WxhsBLe3sTccg4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: f2860a4b-f905-4545-bead-1bbc92564592
    internal-label: Advertising integrations
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
    internal-label: Audience Manager integration
  - id: d9510790-d834-436d-8423-8d69cd50464a
    internal-label: Ads
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: faa6de4fca9b018a704740bbdc3aa5369ee11721
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%
---
# [!DNL Adobe] [!DNL Audience Analytics] für Adobe Advertising-Kunden

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) ist eine Integration zwischen Adobe Audience Manager und Adobe Analytics, die es Audience Manager-Kunden ermöglicht, Segmente an [!DNL Analytics] zu senden, um mehr über die Site-Aktivität zu erfahren.

Adobe Advertising-Kunden können von der Verwendung von [!DNL Audience Analytics] profitieren. Die Integration bietet folgende Möglichkeiten:

* Senden Sie Adobe Advertising-Belichtungsdaten direkt an [!DNL Analytics], um die Auswirkungen der Aktivität des oberen funnel auf die nachgelagerte Site-Aktivität zu ermitteln.

* Ermitteln Sie die Marketing-Kanäle und Site-Einstiegspunkte aus funnel-Werbeanzeigen der oberen Preisklasse.

* Sie können die Integration mit [!DNL Analytics for Advertising] abgleichen, um demografische Segmente von Drittanbietern aus [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) mit [!DNL Analytics for Advertising] Daten zu integrieren, damit Sie mehr über Benutzerprofile erfahren.

  [!DNL Audience Marketplace] bietet Zugriff auf Daten-Feeds von Drittanbietern mit „Aktivierungs“-Abonnementmodellen, die es Käufern ermöglichen, Daten an ein Ziel zu senden. Wenn die Daten in einem [!DNL Analytics] Ziel verwendet werden, werden keine Aktivierungsgebühren erhoben.

* (Werbetreibende mit Advertising DSP) Fügen Sie zusätzliche Belichtungssegmente hinzu, um ganzheitliche Einblicke in das Journey-Management zu erhalten.

  Advertising DSP kann Belichtungsdaten als verwertbare Signale an Audience Manager senden, indem entweder Adobe Experience Platform oder Audience Manager-Impression-Tracking-Pixel implementiert werden. Die Weiterleitung derselben Daten an [!DNL Analytics] ermöglicht eine erweiterte Datenanalyse. Weitere Informationen finden [&#x200B; unter „Übersicht über das Senden von DSP-](/help/integrations/audience-manager/media-data-integration/overview.md) an Adobe Audience Manager&quot;.

Weitere Informationen zu [!DNL Audience Analytics], einschließlich der Voraussetzungen und des Workflows, finden Sie unter &quot;[Übersicht über Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)&quot;.

## Beispiele für die Verwendung [!DNL Audience Analytics] Daten mit Adobe Advertising-Daten

Im Folgenden finden Sie Beispiele dafür, wie Sie die kombinierten Daten in [!DNL Analytics] [!DNL Analysis Workspace] verwenden können.

### Auswirkungen der Aktivität „Oberer funnel&quot; auf nachgelagerte Aktivitäten anzeigen

Verwenden Sie Expositionssegmente für Audience Manager, um die Auswirkungen der Site-Aktivität des oberen funnel auf die nachgelagerte Site-Aktivität zu sehen. Fügen Sie Adobe Advertising- oder Makro-IDs von Drittanbietern in Ihre Tracking-Pixel ein, um die Auswirkungen auf einer detaillierten Ebene zu verfolgen, von der Kampagnenebene bis zur Ebene der Site, auf der die Benutzerin oder der Benutzer exponiert war.

Die wichtigsten Vorteile:

* Verfolgen Sie die Offenlegung nach funnel/Anzeigentypen und verwenden Sie [!DNL Audience Analytics], um Einstiegsraten und Überschneidungen mit der nächsten Phase der Kunden-Journey zu bestimmen.

* Bestimmen Sie die Auswirkungen der Aktivität des oberen funnel auf die nachgelagerte Site-Aktivität.

* Verbinden Sie [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event -->- und [!DNL Audience Analytics], um eine ganzheitliche Journey zur Website zu bestimmen.

<!-- (which includes the user's last exposure event) -->

Im Folgenden finden Sie Beispiele für Berichte, die Sie in [!DNL Analysis Workspace] erstellen können.

![Siehe Auswirkungen der Aktivität „Oberer funnel&quot; auf die nachgelagerte Site-Aktivität](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Verwenden [!DNL Audience Analytics] Segmentdaten von Drittanbietern für die Benutzerprofilanalyse

Verwenden Sie Audience Manager-Segmente von Drittanbietern, um eine umfassendere Analyse der Interaktion von Benutzenden mit Ihrer Site zu erhalten. Anhand dieser Informationen können Sie neue Drittanbieter-Zielgruppen ermitteln, für die Medien aktiviert werden sollen. Dies geschieht auf Basis der Interaktion von Profilen aus Drittanbietersegmenten mit wichtigen Leistungsindikatoren für die Sites der Medienkampagnen.

>[!TIP]
> Verwenden Sie die `Audiences ID` und `Audiences Name` Dimensionen von Audience Manager in allen [!DNL Analytics], wie alle anderen Dimensionen, die [!DNL Analytics] erfasst.

Im Folgenden finden Sie Beispiele für Berichte, die Sie in [!DNL Analysis Workspace] erstellen können.

![Verwendung von Drittanbietersegmenten zur Anreicherung der Benutzerprofilanalyse](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
