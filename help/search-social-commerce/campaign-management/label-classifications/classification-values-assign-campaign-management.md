---
title: Zuweisen von Klassifizierungswerten zu Kontokomponenten aus den Ansichten des Kampagnen-Managements
description: Erfahren Sie, wie Sie den Kontokomponenten Klassifizierungswerte zuweisen.
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# Zuweisen von Klassifizierungswerten zu Kontokomponenten aus den Ansichten des Kampagnen-Managements

Sie können Classification-Werte für die folgenden Suchentitäten aus den Kampagnen-Management-Ansichten zuweisen und entfernen: Kampagne, Anzeigengruppe, Keyword, Anzeige, Platzierung, Produktgruppe auf Einheitenebene und dynamische Suchzielgruppe. Bei Bedarf können Sie während des Zuweisungsprozesses Klassifizierungen und Klassifizierungswerte erstellen. Jede Kennzeichnungsklassifizierung kann bis zu 2.000 Werte aufweisen.

Jede Entität kann einen Bezeichnungswert pro Klassifizierung aufweisen. Beispielsweise kann „Schuhe_Kampagne“ den Farbwert „Rot“ und den Geowert „Los Angeles“ haben, aber es können nicht mehrere Werte für „Farbe“ oder „Geo“ sein.

Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die übernommenen Werte überschreiben.

>[!NOTE]
>
>Ihre Keywords und Werbetexte für einige Werbenetzwerke und Kampagnentypen sind [nicht veränderlich](/help/search-social-commerce/campaign-management/faqs-campaigns.md) was bedeutet, dass ihre Bearbeitung die vorhandene Entität löscht und eine neue erstellt. Wenn eine vorhandene Entität auf diese Weise gelöscht wird, wird die Bezeichnungsklassifizierung nicht der neuen Entität zugewiesen.

## (Neue Benutzeroberfläche) Zuweisen von Klassifizierungswerten zu Kontokomponenten

Sie können allen entsprechenden Kontokomponenten, die in der neuen Benutzeroberfläche verfügbar sind, Klassifizierungswerte zuweisen.

1. Öffnen Sie die Entitätsansicht über das Menü **[!UICONTROL Manage]** oder **[!UICONTROL Target]** .

1. Aktivieren Sie das Kontrollkästchen neben jeder relevanten Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Gehen Sie für jeden zutreffenden Classification-Wert wie folgt vor:

   1. Geben Sie in der Spalte **[!UICONTROL Classifications]** die Klassifizierung an:

      * Um eine vorhandene Klassifizierung zu verwenden, klicken Sie auf den Klassifizierungsnamen, um sie zu erweitern.

      * Um eine Klassifizierung zu erstellen, klicken Sie in der Spaltenüberschrift auf [!UICONTROL +] . Geben Sie im Eingabefeld den Klassifizierungsnamen ein und klicken Sie dann auf ![Speichern](/help/search-social-commerce/assets/save-checkmark.png "Speichern"), um die Klassifizierung sofort zu speichern. Um die neue Klassifizierung zu verwenden, klicken Sie auf den Klassifizierungsnamen, um sie zu erweitern.

        Der Name muss aus [ASCII-Zeichen 32-126](https://www.asciitable.com/) bestehen und die maximale Länge beträgt 27 Einzelbyte-Zeichen.

   1. Geben Sie in der Spalte **[!UICONTROL Value Name]** den Wert für die ausgewählte Klassifizierung an:

      * Um einen vorhandenen Wert zu verwenden, wählen Sie den Wert aus.

      * Um einen Wert zu erstellen, klicken Sie in der Spaltenüberschrift auf [!UICONTROL +] . Geben Sie im Eingabefeld den Wert ein und klicken Sie dann auf ![Speichern](/help/search-social-commerce/assets/save-checkmark.png "Speichern"), um den Wert sofort zu speichern und standardmäßig auszuwählen.

        Die maximale Länge beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

1. Klicken Sie auf **+[!UICONTROL Assign Now]**.

## (Alte Benutzeroberfläche) Zuweisen von Klassifizierungswerten zu Kontokomponenten

1. Klicken Sie auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, und wählen Sie dann die Ansicht der Kontokomponente aus.

1. Führen Sie einen der folgenden Schritte aus:

   * (Um einem Element Werte zuzuweisen) Halten Sie den Cursor über den Entitätsnamen, klicken Sie auf ![Menüschaltfläche](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menüschaltfläche") und wählen Sie dann **[!UICONTROL Classification]** aus.

   * (Um einem oder mehreren Entitäten Werte zuzuweisen) Gehen Sie wie folgt vor:

      * Aktivieren Sie das Kontrollkästchen neben jeder relevanten Zeile.

        Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      * Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und dann auf **[!UICONTROL Classification]**.

1. Führen Sie in der [!UICONTROL Assignment Details] einen der folgenden Schritte aus:

   * Um vorhandene Klassifizierungswerte in neue Werte zu ändern, wählen Sie **[!UICONTROL Set To]** aus.

     Die maximale Länge für jeden Wert beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

   * Um bestimmte Klassifizierungswerte zuzuweisen, ohne vorhandene Werte zu entfernen, wählen Sie **[!UICONTROL Assign]** aus.

   * Um bestimmte, aktuell zugewiesene Klassifizierungswerte zu entfernen, wählen Sie **[!UICONTROL Remove]** aus.

     Wenn Sie einen Klassifizierungswert entfernen, sind die Berichtsdaten für den Wert für die angegebenen Kontokomponenten nicht mehr verfügbar.

   * Um bestimmte Klassifizierungswerte zu löschen, wählen Sie **[!UICONTROL Delete]** aus.

     Durch das Löschen eines Klassifizierungswerts ist dieser nicht mehr für die zukünftige Verwendung verfügbar und die Berichtsdaten sind nicht mehr für diesen Wert verfügbar. Alle Zuweisungen zwischen den Werten und bestimmten Kontokomponenten werden entfernt, aber die Kontokomponenten werden nicht gelöscht.

1. Gehen Sie für jeden zutreffenden Classification-Wert wie folgt vor:

   1. Geben Sie in der Spalte **[!UICONTROL Classification]** den Klassifizierungsnamen an:

      * Um eine vorhandene Klassifizierung zu verwenden, klicken Sie auf den Klassifizierungsnamen, um sie zu erweitern.

      * Um eine Klassifizierung zu erstellen, klicken Sie auf [!UICONTROL +]. Geben Sie im Eingabefeld den Klassifizierungsnamen ein und klicken Sie dann auf ![Speichern](/help/search-social-commerce/assets/select.png "Speichern"), um die Klassifizierung sofort zu speichern.

        Der Name muss aus [ASCII-Zeichen 32-126](https://www.asciitable.com/) bestehen und die maximale Länge beträgt 27 Einzelbyte-Zeichen.

   1. Geben Sie in der Spalte **[!UICONTROL Value Name]** den Namen des Werts an:

      * Um einen vorhandenen Wert zu verwenden, klicken Sie auf den Namen des Werts, um ihn auszuwählen.

      * Um einen Wert zu erstellen, klicken Sie auf [!UICONTROL +]. Geben Sie im Eingabefeld den Wert ein und klicken Sie dann auf ![Speichern](/help/search-social-commerce/assets/select.png "Speichern"), um den Wert sofort zu speichern.

        Die maximale Länge beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

1. (Optional) Geben Sie zusätzliche Details ein:

   1. Klicken Sie neben **[!UICONTROL Additional Details]** auf ![Öffnen](/help/search-social-commerce/assets/chevron-up.png "Öffnen"), um die Details zu erweitern.

   1. Geben Sie eine optionale **[!UICONTROL Project Name]** und/oder eine optionale **[!UICONTROL Description]** ein.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Über Klassifizierungen von Kennzeichnungen](classification-about.md)
>* [Erstellen einer Kennzeichnungsklassifizierung](classification-create.md)
>* [Zuweisen von Klassifizierungswerten zu Kontokomponenten mithilfe von Bulksheets](classification-values-assign-bulksheets.md)
>* [Entfernen Sie Kennzeichnungswerte aus den Kontokomponenten](classification-values-remove.md)
>* [Löschen von Kennzeichnungswerten](classification-values-delete.md)
>* [Löschen von Kennzeichnungsklassifizierungen](classification-delete.md)
