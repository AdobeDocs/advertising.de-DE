---
title: '''[!DNL Adobe] [!DNL Audience Analytics] für Adobe Advertising Customers'
description: Erfahren Sie, wie Sie  [!DNL Adobe] [!DNL Audience Analytics] für Werbeanwendungsfälle verwenden.
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] für Adobe Advertising-Kunden

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) ist eine Integration zwischen Adobe Audience Manager und Adobe Analytics, die es Audience Manager ermöglicht, Segmente an [!DNL Analytics] zu senden, um erweiterte Einblicke in die Site-Aktivität zu erhalten.

Adobe Advertising-Kunden können von der Verwendung von [!DNL Audience Analytics] profitieren. Die Integration ermöglicht Ihnen Folgendes:

* Senden Sie Adobe Advertising-Belichtungsdaten direkt an [!DNL Analytics], um die Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität zu ermitteln.

* Bestimmen Sie die Marketing-Kanäle und Site-Einstiegspunkte aus Anzeigen zur oberen Trichterexposition.

* Fügen Sie die Integration mit [!DNL Analytics for Advertising] ein, um demografische Drittanbietersegmente aus [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) mit [!DNL Analytics for Advertising] -Daten zu integrieren, um weitere Einblicke in Benutzerprofile zu erhalten.

  [!DNL Audience Marketplace] bietet Zugriff auf Drittanbieter-Daten-Feeds mit Abonnementmodellen &quot;Aktivierung&quot;, mit denen Käufer Daten an ein Ziel senden können. Wenn die Daten innerhalb eines [!DNL Analytics] -Ziels verwendet werden, werden keine Aktivierungsgebühren erhoben.

* (Werbetreibende mit Advertising DSP) Fügen Sie zusätzliche Expositionssegmente für Einblicke in das ganzheitliche Journey-Management hinzu.

  Advertising DSP kann Belichtungsdaten als umsetzbare Signale an Audience Manager senden, indem Adobe Experience Platform- oder Audience Manager-Impressions-Tracking-Pixel implementiert werden. Die Weiterleitung derselben Daten an [!DNL Analytics] ermöglicht eine erweiterte Datenanalyse. Weitere Informationen finden Sie unter &quot;[Überblick über die Adobe Advertising-Mediendatenintegration mit Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

Weitere Informationen zu [!DNL Audience Analytics], einschließlich der Voraussetzungen und des Workflows, finden Sie unter &quot;[Audience Analytics overview](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)&quot;.

## Beispiele für die Verwendung von [!DNL Audience Analytics]-Daten mit Adobe Advertising-Daten

Im Folgenden finden Sie Beispiele dafür, wie Sie die kombinierten Daten innerhalb von [!DNL Analytics] [!DNL Analysis Workspace] verwenden können.

### Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Aktivität anzeigen

Verwenden Sie Expositionssegmente der Audience Manager, um die Auswirkungen der Aktivität der oberen Trichtersite auf die nachgelagerte Site-Aktivität zu sehen. Schließen Sie Adobe Advertising- oder Drittanbieter-Makro-IDs in Ihre Tracking-Pixel ein, um die Auswirkungen auf einer detaillierten Ebene von der Kampagnenebene bis zur Ebene der Site zu verfolgen, auf der der Benutzer verfügbar war.

Hauptvorteile:

* Verfolgen Sie die Belichtung nach Trichter-/Anzeigentypen und verwenden Sie [!DNL Audience Analytics], um Einstiegsraten und Überschneidungen mit der nächsten Journey-Phase des Kunden zu ermitteln.

* Ermitteln Sie die Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität.

* Verbinden Sie [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> und [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> , um eine ganzheitliche Journey zur Site zu bestimmen.

Im Folgenden finden Sie Beispiele für Berichte, die Sie in [!DNL Analysis Workspace] erstellen können.

![Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität anzeigen](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Verwenden von [!DNL Audience Analytics] Segmentdaten von Drittanbietern für die Benutzerprofilanalyse

Verwenden Sie Audience Manager von Drittanbietern, um eine genauere Analyse der Interaktion der Benutzer mit Ihrer Site zu erhalten. Mithilfe der Informationen können Sie neue Zielgruppen von Drittanbietern bestimmen, für die Medien aktiviert werden sollen. Dies hängt davon ab, wie Profile aus Drittanbietersegmenten mit wichtigen Leistungsindikatoren für die Sites von Medienkampagnen interagieren.

>[!TIP]
> Verwenden Sie die Dimensionen `Audiences ID` und `Audiences Name` des Audience Managers in [!DNL Analytics], wie alle anderen Dimensionen, die [!DNL Analytics] erfasst.

Im Folgenden finden Sie Beispiele für Berichte, die Sie in [!DNL Analysis Workspace] erstellen können.

![Verwenden von Drittanbietersegmenten zur Anreicherung der Benutzerprofilanalyse](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
