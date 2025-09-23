---
title: Einschränkungszuweisungen für Anzeigengruppen verwalten
description: Erfahren Sie, wie Sie Anzeigengruppen Einschränkungen zuweisen.
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: c9960b5a-4b6c-4ef0-8501-5478af2c40da
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Einschränkungszuweisungen für Anzeigengruppen verwalten

*Beta-Funktion*

Sie können Gebotsbeschränkungen für die folgenden Suchentitäten zuweisen und entfernen: Kampagne, Anzeigengruppe, Keyword, Platzierung, Produktgruppe auf Einheitenebene und dynamische Suchzielgruppe. Jede Entität kann nur eine Einschränkung aufweisen.

Beschränkungen werden von untergeordneten Entitäten übernommen, sodass Sie untergeordneten Entitäten keine Beschränkungen zuweisen müssen, es sei denn, Sie möchten die übernommenen Werte überschreiben.

Wenn Sie die Zuweisung einer Einschränkung aufheben, wird die Verknüpfung mit den Kontokomponenten und allen untergeordneten Komponenten entfernt, und es sind keine Berichtsdaten für die Einschränkung mehr für diese Komponenten verfügbar. Durch Aufheben der Zuweisung einer Beschränkung werden weder die Beschränkung noch die Kontokomponenten selbst gelöscht.

## Weisen Sie ausgewählten Anzeigengruppen in der neuen [!UICONTROL Ad Groups] eine Einschränkung zu

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Anzeigengruppe, der Sie eine einzelne Einschränkung zuweisen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

## Weisen Sie ausgewählten Suchangebotseinheiten aus den veralteten [!UICONTROL Campaigns] eine Einschränkung zu

1. Wählen Sie in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** die Ansicht Kontomomponente aus.

1. Aktivieren Sie das Kontrollkästchen neben jeder relevanten Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL More]** und anschließend auf **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie die entsprechende Einschränkung aus.

1. (Optional) Geben Sie zusätzliche Details ein:

   1. Klicken Sie neben [!UICONTROL Additional Details] auf **[!UICONTROL Open]** , um die Details zu erweitern.

   1. Geben Sie eine optionale **[!UICONTROL Project Name]** und/oder eine optionale **[!UICONTROL Description]** ein.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Heben Sie die Zuweisung von Einschränkungen zu ausgewählten Anzeigengruppen in der neuen [!UICONTROL Ad Groups] auf

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Anzeigengruppe, deren Zuweisung von Einschränkungen Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

## Heben Sie die Zuweisung von Einschränkungen zu Suchangebotseinheiten in den veralteten [!UICONTROL Campaigns] auf

>[!NOTE]
>
>Informationen zum Löschen einer Einschränkung, sodass sie für die zukünftige Verwendung nicht mehr verfügbar ist, finden Sie unter „Löschen von Einschränkungen für Suchangebotseinheiten“ im Kapitel „Optimierungshandbuch“ zu „Bid-Einschränkungen“, das in Search, Social und Commerce verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

1. Wählen Sie in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** die Ansicht Kontomomponente aus.

1. Aktivieren Sie das Kontrollkästchen neben jeder Komponente, von der Sie die Einschränkung entfernen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL More]** und anschließend auf **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie im Bestätigungsdialogfeld **[!UICONTROL Yes, Unassign]** aus.

>[!MORELIKETHIS]
>
>* [Einschränkungszuweisungen für Kampagnen verwalten](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
