---
title: Einschränkungszuweisungen für Kampagnen verwalten
description: Erfahren Sie, wie Sie Kampagnen Einschränkungen zuweisen.
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: d886a228-24d7-4d8e-b68a-76e56b4304ed
TQID: https://experienceleague.adobe.com/qwisQ3OqMeymlREsTVY-Wf59ln37hBLR0X4R7RjkuTM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Einschränkungszuweisungen für Kampagnen verwalten

*Beta-Funktion*

Sie können Gebotsbeschränkungen für die folgenden Suchentitäten zuweisen und entfernen: Kampagne, Anzeigengruppe, Keyword, Platzierung, Produktgruppe auf Einheitenebene und dynamische Suchzielgruppe. Jede Entität kann nur eine Einschränkung aufweisen.

Beschränkungen werden von untergeordneten Entitäten übernommen, sodass Sie untergeordneten Entitäten keine Beschränkungen zuweisen müssen, es sei denn, Sie möchten die übernommenen Werte überschreiben.

Wenn Sie die Zuweisung einer Einschränkung aufheben, wird die Verknüpfung mit den Kontokomponenten und allen untergeordneten Komponenten entfernt, und es sind keine Berichtsdaten für die Einschränkung mehr für diese Komponenten verfügbar. Durch Aufheben der Zuweisung einer Beschränkung werden weder die Beschränkung noch die Kontokomponenten selbst gelöscht.

>[!NOTE]
>
>* Wenn Sie später ein Keyword oder die Anzeigenkopie für eine nicht veränderliche Anzeige bearbeiten und so ein neues Keyword oder eine neue Anzeige erstellen, wird die Begrenzung nicht der neuen Entität zugewiesen.
>* Aktive Einschränkungen beschränken die Gebotsabgabe nur für zugewiesene Gebotseinheiten in optimierten alten Portfolios auf Keyword-Ebene. Sie werden bei Gebotseinheiten ignoriert, die sich in aktiven Portfolios befinden, sich in hybriden Portfolios befinden oder nicht in Portfolios sind.

## Weisen Sie ausgewählten Kampagnen in der neuen [!UICONTROL Campaigns] eine Einschränkung zu

Eine einzelne Einschränkung kann einer oder mehreren Kampagnen zugewiesen werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, der Sie eine einzelne Einschränkung zuweisen.

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

## Entfernen von Einschränkungen aus ausgewählten Kampagnen in der neuen [!UICONTROL Campaigns]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, deren Zuweisung von Einschränkungen Sie aufheben möchten.

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
>* [(Neue Benutzeroberfläche) Verwalten von Einschränkungen für Suchangebotseinheiten](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Neue Benutzeroberfläche) Verwalten von Einschränkungszuweisungen für Anzeigengruppen](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [(Neue Benutzeroberfläche) Verwalten von Einschränkungszuweisungen für Schlüsselwörter](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [(Neue Benutzeroberfläche) Verwalten von Einschränkungszuweisungen für Platzierungen](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
