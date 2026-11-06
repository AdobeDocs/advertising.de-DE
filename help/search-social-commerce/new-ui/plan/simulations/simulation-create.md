---
title: Benutzerdefinierte Simulation ausführen oder erneut ausführen
description: Erfahren Sie, wie Sie eine benutzerdefinierte Simulation für ein Portfolio ausführen oder erneut ausführen.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
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
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%
---
# Benutzerdefinierte Simulation ausführen oder erneut ausführen

*Beta-Funktion*

Sie können eine benutzerdefinierte Simulation für ein (optimiertes [&#x200B; aktives) &#x200B;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status) erstellen. Sie können auch eine Simulation in der Liste auswählen, um eine neue Simulation für dasselbe Portfolio auszuführen, oder Simulationen mit ihren vorhandenen Einstellungen erneut ausführen.

Zum Erstellen einer benutzerdefinierten Simulation ist die Berechtigung [!UICONTROL Create Simulation] erforderlich. Für die Auswahl eines Portfolios ist die Berechtigung [!UICONTROL View Portfolios] erforderlich.

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin] und [!UICONTROL Account Manager] Benutzer können Simulationen sehen, die von anderen Benutzern erstellt wurden. Alle anderen Benutzer können nur die von ihnen erstellten benutzerdefinierten Simulationen sehen.

## Erstellen einer neuen Simulation {#simulation-create}

Sie können von der [!UICONTROL Simulations] aus starten oder [eine benutzerdefinierte Simulation von der [!UICONTROL Portfolios] aus ausführen](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Deaktivieren Sie alle ausgewählten Simulationszeilen, und klicken Sie dann auf **[!UICONTROL Run Simulation]**.

1. Portfolio auswählen:

   1. Klicken Sie auf **[!UICONTROL Select Portfolio]**.

   1. Portfolio auswählen.

      Um nach Portfolios zu suchen, die eine bestimmte Textzeichenfolge enthalten, geben Sie die Textzeichenfolge innerhalb des Suchfelds ein. Bei Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.

   1. Klicken Sie auf **[!UICONTROL Proceed]**.

1. Geben Sie die [benutzerdefinierten Simulationseinstellungen](#custom-simulation-settings) an:

   1. (Optional) Um das für die Simulation verwendete Portfolio zu ändern, klicken Sie **[!UICONTROL Change Portfolio]** neben dem Portfolionamen, wählen Sie das Portfolio aus und klicken Sie dann auf **[!UICONTROL Proceed]**.

   1. Auf der Registerkarte [!UICONTROL Basic Settings] :

      1. Eindeutige **[!UICONTROL Simulation Name]** eingeben.

      1. (Optional) Ändern Sie die grundlegenden Parameter für die Simulation.

   1. (Optional) Ändern Sie auf der Registerkarte [!UICONTROL Advanced Settings] die erweiterten Parameter für die Simulation.

   Die vorhandenen Parameter für das ausgewählte Portfolio werden standardmäßig angegeben. Wenn Sie die Werte ändern, werden die Ergebnisse angezeigt, die verschiedene Parameter erzeugen würden, ohne die vorhandenen Parameter des Portfolios zu ändern.

1. Klicken Sie auf **[!UICONTROL Next]**.

1. Überprüfen Sie die Einstellungen und bearbeiten Sie sie nach Bedarf.

1. Klicken Sie auf **[!UICONTROL Submit & Run]**.

Die Anfrage wird gesendet und die [!UICONTROL Simulations] geöffnet. Wenn der Simulationsbericht verfügbar ist, erhalten Sie und alle anderen angegebenen E-Mail-Empfänger eine Benachrichtigung mit einem Download-Link. Sie können auch [die Simulation aus der [!UICONTROL Simulations] herunterladen](simulation-download.md).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Simulation mit den vorhandenen Einstellungen erneut ausführen {#rerun-a-simulation-with-the-existing-settings}

Sie können bis zu 10 Simulationen gleichzeitig mit ihren vorhandenen Einstellungen erneut ausführen. Simulationen mit dem Status [!UICONTROL Queued] oder [!UICONTROL In Progress] können nicht erneut ausgeführt werden. Wenn Ihre Auswahl diese Simulationen enthält, werden sie übersprungen und die verbleibenden Simulationen werden gesendet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Aktivieren Sie die Kontrollkästchen neben den Simulationen, die Sie erneut ausführen möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle oder in der Symbolleiste für Massenaktionen auf **[!UICONTROL Re-Run Simulation]**.

Die Anfrage wird gesendet und die Ansicht wird aktualisiert.

## Neue Simulation für ein Portfolio in der Liste ausführen {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

Wenn Sie eine Simulation vor dem Klicken auswählen, [!UICONTROL Run Simulation] wird ihr Portfolio für eine neue Simulation ausgewählt. Das Formular verwendet die aktuellen Einstellungen des Portfolios, nicht die Einstellungen der ausgewählten Simulation. Mit dieser Aktion wird die vorhandene Simulation nicht bearbeitet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Aktivieren Sie das Kontrollkästchen neben einer Simulation für das Portfolio, das Sie verwenden möchten.

   Wenn Sie mehrere Simulationen auswählen, müssen diese alle dasselbe Portfolio verwenden. Das Portfolio muss aktiv oder optimiert sein.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Run Simulation]**.

1. Geben Sie die [benutzerdefinierten Simulationseinstellungen](#custom-simulation-settings) einschließlich eines eindeutigen **[!UICONTROL Simulation Name]** an. Ändern Sie die Parameter auf den Registerkarten **[!UICONTROL Basic Settings]** und **[!UICONTROL Advanced Settings]** nach Bedarf.

1. Klicken Sie auf **[!UICONTROL Next]**.

1. Überprüfen Sie die Einstellungen und bearbeiten Sie sie nach Bedarf.

1. Klicken Sie auf **[!UICONTROL Submit & Run]**.

Die Anfrage wird gesendet und die [!UICONTROL Simulations] geöffnet. Sie können [die Simulation herunterladen](simulation-download.md) nachdem sie erfolgreich abgeschlossen wurde.

## Benutzerdefinierte Simulationseinstellungen {#custom-simulation-settings}

Weitere Informationen zu den benutzerdefinierten Simulationseinstellungen finden Sie im Optimierungshandbuch, das bei Search, Social und Commerce verfügbar ist.

>[!MORELIKETHIS]
>
>* [Über Simulationen](simulation-about.md)
>* [Anzeigen von Simulationsdetails](simulation-view.md)
>* [Simulationen herunterladen](simulation-download.md)
