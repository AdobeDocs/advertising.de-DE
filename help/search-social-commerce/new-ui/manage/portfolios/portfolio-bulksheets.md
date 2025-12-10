---
title: Massenbearbeitung von Portfolioeinstellungen mithilfe von Bulksheet-Dateien
description: Erfahren Sie, wie Sie die Einstellungen für mehrere Portfolios mithilfe einer Bulksheet-Datei bearbeiten.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: 14f85e5ff5655be045fa4a2280edc1fe01978029
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Massenbearbeitung von Portfolioeinstellungen mithilfe von Bulksheet-Dateien

*Beta-Funktion*

Eine Portfolio-Bulksheet ist eine Datei, die Portfolioeinstellungen in einem bestimmten Format enthält und zur schnellen Überprüfung und Änderung der Einstellungen verwendet werden kann. Sie können Bulksheets mit Einstellungen für ein oder mehrere Portfolios generieren (herunterladen). Die Datei wird als [!DNL Excel] Arbeitsmappe mit zwei Arbeitsblättern (XLSX-Format) heruntergeladen. Die Arbeitsmappe enthält:

* Ein schreibgeschütztes [!UICONTROL Instructions]-Arbeitsblatt mit Informationen zum Bearbeiten der Felder.

* Eine [!UICONTROL Portfolio Settings Edit] Registerkarte mit einer Zeile pro eingeschlossenem Portfolio. Sie können die Felder nach Bedarf bearbeiten, die Datei lokal speichern und anschließend [die bearbeitete Datei hochladen](#portfolio-bulksheet-upload) in Search, Social und Commerce. Die bearbeitbaren Felder sind farblich hervorgehoben.

## Herunterladen einer Bulksheet-Datei mit Portfolioeinstellungen

1. Aktivieren Sie das Kontrollkästchen neben jedem Portfolio, das in die Bulksheet aufgenommen werden soll.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**.

1. Geben Sie den Namen der zu erstellenden Bulksheet-Datei ein und klicken Sie dann auf **[!UICONTROL Export Now]**.

   Die Datei wird im Standard-Downloads-Ordner Ihres Browsers gespeichert.

## Hochladen einer Bulksheet-Datei mit aktualisierten Portfolioeinstellungen {#portfolio-bulksheet-upload}

Die Datei muss im XLSX-Format vorliegen.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**. &lt;!— Sollte &quot;Portfolio-Einstellungen importieren“ sein — „Details“ sind möglicherweise zu vage und schlagen vor, dass sie etwas Anderes enthalten könnten. —>

1. Im Dialogfeld [!UICONTROL Import Portfolio Details File] : <!-- reword if we change the name of the operation -->

   1. Ziehen Sie eine Datei per Drag-and-Drop in das Feld oder klicken Sie auf **[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? -->, um eine Datei auf Ihrem Gerät oder Netzwerk auszuwählen.

   1. Klicken Sie auf **[!UICONTROL Import]**.

Sie können den Status des Uploads über die Schaltfläche [!UICONTROL Global Sync Status] (![Globaler Synchronisierungsstatus](/help/search-social-commerce/assets/global-sync-status.png "Globaler Synchronisierungsstatus")) neben der Datumsbereichsauswahl überprüfen.<!-- icon similar to Refresh -->. Wenn eine der Änderungen nicht erfolgreich war, können Sie eine Fehlerdatei herunterladen, die anzeigt, was fehlgeschlagen ist.

Benachrichtigungen werden auch zum Benachrichtigungszentrum hinzugefügt und Sie können den Bereich Benachrichtigungen über das Symbol ![Benachrichtigungen](/help/search-social-commerce/assets/notifications-new.png "Benachrichtigungen") neben der Schaltfläche [!UICONTROL Global Sync Status] öffnen (![Globaler Synchronisierungsstatus](/help/search-social-commerce/assets/global-sync-status.png "Globaler Synchronisierungsstatus")).

## Datenanforderungen für hochgeladene Bulksheet-Dateien

Alle Bulksheet-Dateien müssen die [!UICONTROL Portfolio ID] enthalten, und jede Datenzeile muss einen Wert für die [!UICONTROL Portfolio ID] enthalten, damit sie verarbeitet werden kann. Weitere Informationen zu den Datenanforderungen finden Sie auf der Registerkarte [!UICONTROL Instructions] der heruntergeladenen Bulksheet-Datei.

Erläuterungen zu den Spalten der Portfolioeinstellungen auf der Registerkarte [!UICONTROL Portfolio Settings Edit] finden Sie im Optimierungshandbuch , das bei Search, Social und Commerce verfügbar ist.

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [(Neue Benutzeroberfläche) Bearbeiten eines Portfolios](portfolio-edit.md)
>* [Erstellen eines Portfolios](portfolio-create.md)
>* [(Neue Benutzeroberfläche) Über Portfolios](portfolio-about.md)
