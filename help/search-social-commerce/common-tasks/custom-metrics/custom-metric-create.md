---
title: Erstellen einer benutzerdefinierten Metrik
description: Erfahren Sie, wie Sie benutzerdefinierte Metriken konfigurieren, die anhand von Standardmetriken berechnet werden.
exl-id: a9ce503a-67ee-477e-8f79-31b4a9c6e51a
feature: Search Common Tasks, Search Custom Metrics
TQID: 'https://experienceleague.adobe.com/g-J8AlulQ20I-vxQrPkPaP-Ap66bBIng0eKDPqhV9U4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: a1695a4d-41fb-5bb6-a22a-9e7a1b3222d7
    internal-label: Search Custom Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 9837cac1a920b1b3b88b04b150cb604832209eaf
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%
---
# Erstellen einer benutzerdefinierten Metrik

## (Neue Benutzeroberfläche) Erstellen einer benutzerdefinierten Metrik aus einer Verwaltungsansicht

*In den meisten Entitätsansichten im Menü &quot;[!UICONTROL Manage]&quot; verfügbar<!-- [!UICONTROL Plan] > [!UICONTROL Simulations],--> [!UICONTROL Setup] > [!UICONTROL Label Classifications], [!UICONTROL Goals] > [!UICONTROL Objectives] und [!UICONTROL Constraints], und [!UICONTROL Targeting] > [!UICONTROL Placements]*

1. Führen Sie über der Datentabelle einen der folgenden Schritte aus:

   * Klicken Sie auf den Namen der aktuell angewendeten Ansicht (![View](/help/search-social-commerce/assets/view.png "View")). Halten Sie den Cursor über den Namen einer bearbeitbaren Ansicht und klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") , um die Anzeigeeinstellungen zu öffnen.

     Die von Ihnen erstellte benutzerdefinierte Metrik wird in allen Ihren Ansichten verfügbar sein.

   * Klicken Sie auf ![Benutzerdefinierte Spalten](/help/search-social-commerce/assets/custom-columns-new.png "Benutzerdefinierte Spalten"), um die Spaltenkonfigurationseinstellungen zu öffnen.

1. Klicken Sie unter der sich öffnenden Spaltenliste auf ![Benutzerdefinierte Metrik erstellen](/help/search-social-commerce/assets/add.png "Benutzerdefinierte Metrik erstellen") **[!UICONTROL Create Custom Metric]**.

1. Geben Sie die [benutzerdefinierten Metrikeinstellungen](custom-metric-settings.md) an.

1. Klicken Sie auf **[!UICONTROL Create]**.

## (Neue Benutzeroberfläche) Erstellen einer benutzerdefinierten Metrik aus den Einstellungen des Berichts oder der Berichtsvorlage {#create-from-report-settings}

1. Gehen Sie in den Einstellungen für Berichte oder Berichtsvorlagen zum Schritt **[!UICONTROL Columns]** .

1. Geben Sie im Abschnitt **[!UICONTROL Custom Metrics]** die Metrikeinstellungen an:

   * **[!UICONTROL Custom Metric Name]:** Geben Sie einen Namen für die Metrik ein.

   * **[!UICONTROL Format]:** Wählen Sie **[!UICONTROL Currency]**, **[!UICONTROL Number to 2 Decimal Places]**, **[!UICONTROL Number to 3 Decimal Places]**, **[!UICONTROL Number w/out Decimal Places]** oder **[!UICONTROL Percentage]** aus.

   * **[Formeleingabefeld]:** Erstellen Sie die Formel, indem Sie Metriken aus **[!UICONTROL Insert Metric]** auswählen und auf die Operatorschaltflächen (`+`, `-`, `*`, `/`, `(` und `)`) klicken. Sie können die Formel auch manuell eingeben. Platzieren Sie den Cursor an der Stelle, an der die einzelnen Metriken oder Operatoren eingefügt werden sollen.

1. Klicken Sie auf **[!UICONTROL Add Metric]**.

   Nachdem die Metrik erfolgreich erstellt wurde, wird die Liste der verfügbaren Spalten nach dem Metriknamen gefiltert. Beim Erstellen der Metrik wird sie nicht automatisch in den Bericht aufgenommen.

1. Um die Metrik in den Bericht aufzunehmen, wählen Sie sie in der Liste der verfügbaren Spalten aus und klicken Sie auf ![Nach-rechts](/help/search-social-commerce/assets/arrow-right-customize.png "Nach-rechts"), um sie in die Liste der ausgewählten Spalten zu verschieben.

## (Alte Benutzeroberfläche) Erstellen einer benutzerdefinierten Metrik aus einer Kampagnen-Management-Ansicht

1. Führen Sie über der Datentabelle einen der folgenden Schritte aus:

   * Klicken Sie auf den Namen der Standardansicht oder der benutzerdefinierten Ansicht, um die Anzeigeeinstellungen zu öffnen.

   * Klicken Sie auf ![Benutzerdefinierte Spalten](/help/search-social-commerce/assets/custom-columns.png "Benutzerdefinierte Spalten"), um die Spaltenkonfigurationseinstellungen zu öffnen.

1. Klicken Sie unter der sich öffnenden Spaltenliste auf ![Neue benutzerdefinierte Metrik erstellen](/help/search-social-commerce/assets/add.png "Neue benutzerdefinierte Metrik erstellen") **[!UICONTROL Create New Custom Metric]**.

1. Geben Sie die [benutzerdefinierten Metrikeinstellungen](custom-metric-settings.md) an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## (Alte Benutzeroberfläche) Erstellen einer benutzerdefinierten Metrik aus einem Bericht oder Berichtsvorlagenformular

1. Wechseln Sie innerhalb eines Berichts- oder Berichtsvorlagenformulars zur Registerkarte **[!UICONTROL Columns]** .

1. Klicken Sie im rechten Abschnitt auf **[!UICONTROL Create]**.

1. Geben Sie die [benutzerdefinierten Metrikeinstellungen](custom-metric-settings.md) an.

1. Klicken Sie auf **[!UICONTROL Submit]**.

## (Alte Benutzeroberfläche) Erstellen einer benutzerdefinierten Metrik aus den [!UICONTROL Portfolios]

1. Klicken Sie über der Datentabelle auf ![Ausgewählte Ansicht bearbeiten](/help/search-social-commerce/assets/view-settings.png "Ausgewählte Ansicht bearbeiten").

1. Klicken Sie auf die Registerkarte **[!UICONTROL Columns]** .

1. Klicken Sie im rechten Abschnitt auf **[!UICONTROL Create]**.

1. Geben Sie die [benutzerdefinierten Metrikeinstellungen](custom-metric-settings.md) an.

1. Klicken Sie auf **[!UICONTROL Submit]**.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Metriken](custom-metric-about.md)
>* [Bearbeiten einer benutzerdefinierten Metrik](custom-metric-edit.md)
>* [Löschen einer benutzerdefinierten Metrik](custom-metric-delete.md)
>* [Benutzerdefinierte Metrikeinstellungen](custom-metric-settings.md)
