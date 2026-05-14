---
title: Benutzerdefinierte Simulation ausführen oder erneut ausführen
description: Erfahren Sie, wie Sie eine benutzerdefinierte Simulation für ein Portfolio ausführen oder erneut ausführen.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2504e6a4eebeab74352606a89a5012ab96c89c47
workflow-type: tm+mt
source-wordcount: 505
ht-degree: 0%

---

# Benutzerdefinierte Simulation ausführen oder erneut ausführen

*Beta-Funktion*

Sie können eine benutzerdefinierte Simulation für ein (optimiertes [ aktives) ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) erstellen. Sie können auch die Parameter einer vorhandenen Simulation ändern und die Simulation neu generieren oder eine vorhandene Simulation mit den vorhandenen Parametern erneut ausführen.

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin] und [!UICONTROL Account Manager] Benutzer können Simulationen sehen, die von anderen Benutzern erstellt wurden. Alle anderen Benutzer können nur die von ihnen erstellten benutzerdefinierten Simulationen sehen.

## Erstellen einer neuen Simulation

1. Führen Sie einen der folgenden Schritte aus:

* In der [!UICONTROL Simulations]:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

   1. Klicken Sie über der Datentabelle auf **[!UICONTROL Run Simulation]**.

   1. Portfolio auswählen:

      1. Klicken Sie auf **[!UICONTROL Select Portfolio]**.

      1. Portfolio auswählen.

         Um nach Portfolios zu suchen, die eine bestimmte Textzeichenfolge enthalten, geben Sie die Textzeichenfolge innerhalb des Suchfelds ein. Bei Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.

      1. Klicken Sie auf **[!UICONTROL Proceed]**.

* In der [!UICONTROL Portfolios]:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

   1. Halten Sie den Cursor über der Portfoliozeile. Klicken Sie neben dem Portfolionamen auf **[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**.

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

Wenn der Simulationsbericht verfügbar ist, erhalten Sie und alle anderen angegebenen E-Mail-Empfänger eine Benachrichtigung mit einem Link, um die Daten in einer ZIP-Datei herunterzuladen, die eine Arbeitsmappe (XLSX-Datei) enthält.

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Bearbeiten Sie die Einstellungen für eine vorhandene Simulation und führen Sie sie erneut aus

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Aktivieren Sie das Kontrollkästchen neben der Simulation, um sie neu zu generieren.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Run Simulation]**.

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

Wenn der Simulationsbericht verfügbar ist, erhalten Sie und alle anderen angegebenen E-Mail-Empfänger eine Benachrichtigung mit einem Link, um die Daten in einer ZIP-Datei herunterzuladen, die eine Arbeitsmappe (XLSX-Datei) enthält.

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Simulation mit den vorhandenen Einstellungen erneut ausführen

Sie können Simulationen, die derzeit nicht in der Warteschlange sind, erneut ausführen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Aktivieren Sie die Kontrollkästchen neben den Simulationen, die Sie erneut ausführen möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Rerun](/help/search-social-commerce/assets/rerun.png "Rerun").

## Benutzerdefinierte Simulationseinstellungen {#custom-simulation-settings}

Weitere Informationen zu den benutzerdefinierten Simulationseinstellungen finden Sie im Optimierungshandbuch, das bei Search, Social und Commerce verfügbar ist.

>[!MORELIKETHIS]
>
>* [Über Simulationen](simulation-about.md)
>* [Anzeigen von Simulationsdetails](simulation-view.md)
>* [Simulationen herunterladen](simulation-download.md)
