---
title: Ausführen und Herunterladen von Simulationen aus der [!UICONTROL Portfolios]
description: Erfahren Sie, wie Sie eine benutzerdefinierte Simulation ausführen und wöchentliche Simulationen aus der Ansicht „Portfolios“ herunterladen.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# Ausführen und Herunterladen von Simulationen aus der [!UICONTROL Portfolios]

*Beta-Funktion*

Sie können eine benutzerdefinierte Simulation für ein einzelnes [optimiertes oder aktives](portfolio-about.md#portfolio-status) Portfolio ausführen und automatisierte wöchentliche Simulationen für bis zu 100 Portfolios aus der [!UICONTROL Portfolios] herunterladen.

Zum Ausführen einer benutzerdefinierten Simulation ist die Berechtigung [!UICONTROL Create Simulation] erforderlich. Das Herunterladen von wöchentlichen Simulationen erfordert die Berechtigung [!UICONTROL View Simulation] .

>[!NOTE]
>
>Sie können auch [eine benutzerdefinierte Simulation in der [!UICONTROL Simulations] erstellen oder erneut ](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md).

## Benutzerdefinierte Simulation ausführen {#run-simulation}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Halten Sie den Cursor über der Portfoliozeile. Klicken Sie neben dem Portfolionamen auf **[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**.

   * Aktivieren Sie das Kontrollkästchen neben dem Portfolio. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL More]>[!UICONTROL Run Simulation]**.

1. Geben Sie die [benutzerdefinierten Simulationseinstellungen](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md#custom-simulation-settings) an:

   1. Geben Sie auf der Registerkarte **[!UICONTROL Basic Settings]** einen eindeutigen **[!UICONTROL Simulation Name]** ein und ändern Sie die grundlegenden Parameter nach Bedarf.

   1. (Optional) Ändern Sie auf der Registerkarte **[!UICONTROL Advanced Settings]** die erweiterten Parameter.

   Die aktuellen Einstellungen des ausgewählten Portfolios werden als Standardeinstellungen verwendet. Durch Ändern der Simulationseinstellungen werden die Portfolioeinstellungen nicht geändert.

1. Klicken Sie auf **[!UICONTROL Next]**.

1. Überprüfen Sie die Einstellungen und nehmen Sie nach Bedarf Änderungen vor.

1. Klicken Sie auf **[!UICONTROL Submit & Run]**.

Die Anfrage wird gesendet und die [!UICONTROL Simulations] geöffnet. Sie können [die Simulation herunterladen](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md) nachdem sie erfolgreich abgeschlossen wurde.

## Wöchentliche Simulationen herunterladen {#download-simulations}

Sie können wöchentliche Simulationen für jeweils ein Ausführungsdatum als [!DNL Microsoft Excel] Arbeitsmappe (XLSX-Datei) herunterladen. Nur aktive und optimierte Portfolios mit für dieses Datum verfügbaren Simulationsberichten werden einbezogen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Portfolio, dessen wöchentliche Simulation Sie herunterladen möchten. Wählen Sie bis zu 100 Portfolios aus.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL More]>[!UICONTROL Download Simulation]**.

1. Wählen Sie **[!UICONTROL Weekly Simulation]** ein Ausführungsdatum aus.

   Standardmäßig ist das neueste verfügbare Datum ausgewählt. Wenn für einige ausgewählte Portfolios keine Berichte verfügbar sind, zeigt das Dialogfeld an, wie viele Portfolios ausgeschlossen werden. Wählen Sie bei Bedarf ein anderes Datum aus. Ein Bericht kann nicht heruntergeladen werden, wenn für keine ausgewählten Portfolios eine Simulation für dieses Datum verfügbar ist.

1. Klicken Sie auf die Schaltfläche Herunterladen , deren Titel die Anzahl der Portfolios mit den verfügbaren Berichten enthält (z. B. **[!UICONTROL Download 2 portfolios]**).

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen. Die Abschlussmeldung gibt an, wie viele Portfolios enthalten waren.

Verwenden Sie die [[!UICONTROL Simulations], um benutzerdefinierte Simulationen herunterzuladen oder einzelne wöchentliche Simulationen auszuwählen](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md).

>[!MORELIKETHIS]
>
>* [(Neue Benutzeroberfläche) Anzeigen von Details zur Portfolioleistung](portfolio-details.md)
>* [Über Portfolios](portfolio-about.md)
>* [Benutzerdefinierte Simulation ausführen oder erneut ausführen](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)
>* [Simulationen herunterladen](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)
