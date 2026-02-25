---
title: Entfernen von Kennzeichnungswerten aus Kontokomponenten
description: Erfahren Sie, wie Sie Zuordnungen zwischen Kennzeichnungswerten und Kontokomponenten entfernen können.
exl-id: 8697367b-0bf9-48c9-8dd3-e733360e1df2
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Entfernen von Kennzeichnungswerten aus Kontokomponenten

Das Entfernen eines Klassifizierungswerts entfernt die Verknüpfung mit der Kontokomponente und allen untergeordneten Komponenten. Berichtsdaten für den Classification-Wert sind für diese Komponenten nicht mehr verfügbar. Wenn Sie einen Klassifizierungswert entfernen, werden weder der Wert noch die Kontokomponenten gelöscht.

>[!NOTE]
>
>Informationen zum Löschen eines Werts aus einer Kennzeichnungsklassifizierung finden Sie unter [Löschen von Kennzeichnungsklassifizierungswerten](classification-values-delete.md).

## (Neue Benutzeroberfläche) Entfernen von Kennzeichnungswerten aus den Kontokomponenten

Sie können Klassifizierungswerte aus allen anwendbaren Kontokomponenten entfernen, die in der neuen Benutzeroberfläche verfügbar sind.

1. Öffnen Sie die Entitätsansicht über das Menü **[!UICONTROL Manage]** oder **[!UICONTROL Target]** .

1. Aktivieren Sie das Kontrollkästchen neben jeder relevanten Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Classification-Wert, der aus den ausgewählten Entitäten entfernt werden soll.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Um alle zugewiesenen Werte auszuwählen, klicken Sie auf **[!UICONTROL Select All]**. Um die Auswahl aller zugewiesenen Werte aufzuheben, klicken Sie auf **[!UICONTROL Deselect All]**.

1. Klicken Sie auf **[!UICONTROL Unassign Selected]**.

## (Alte Benutzeroberfläche) Entfernen von Kennzeichnungswerten aus den Kontokomponenten

1. Wählen Sie in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** die Entitätsansicht aus.

1. Führen Sie einen der folgenden Schritte aus:

   * (Um Werte aus einer einzelnen Entität zu entfernen) Halten Sie den Cursor über den Entitätsnamen, klicken Sie auf ![Menüschaltfläche](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menüschaltfläche") und wählen Sie dann **[!UICONTROL Classification]** aus.

   * (Um Werte aus einer oder mehreren Entitäten zu entfernen) Gehen Sie wie folgt vor:

      * Aktivieren Sie das Kontrollkästchen neben jeder Zeile.

        Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      * Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und dann auf **[!UICONTROL Classification]**.

1. Wählen Sie in der [!UICONTROL Assignment Details] **[!UICONTROL Remove]** aus.

1. Gehen Sie für jeden zu entfernenden Classification-Wert wie folgt vor:

   * Klicken Sie in der Spalte **[!UICONTROL Classification]** auf den Klassifizierungsnamen, um ihn zu erweitern.

   * Klicken Sie in der Spalte **[!UICONTROL Value Name]** auf den Namen des Werts, um ihn auszuwählen.

1. (Optional) Geben Sie zusätzliche Details ein:

   * Klicken Sie neben **[!UICONTROL Additional Details]** auf ![Öffnen](/help/search-social-commerce/assets/chevron-up.png "Öffnen"), um die Details zu erweitern.

   * Geben Sie eine optionale **[!UICONTROL Project Name]** und/oder eine optionale **[!UICONTROL Description]** ein.

   * Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Über Klassifizierungen von Kennzeichnungen](classification-about.md)
>* [Erstellen einer Kennzeichnungsklassifizierung](classification-create.md)
>* [Zuweisen von Klassifizierungswerten zu Kontokomponenten aus den Ansichten des Kampagnen-Managements](classification-values-assign-campaign-management.md)
>* [Zuweisen von Klassifizierungswerten zu Kontokomponenten mithilfe von Bulksheets](classification-values-assign-bulksheets.md)
>* [Löschen von Kennzeichnungswerten](classification-values-delete.md)
>* [Löschen von Kennzeichnungsklassifizierungen](classification-delete.md)
