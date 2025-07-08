---
title: Anwenden von Datenfiltern über ein Spaltenüberschriftenmenü
description: Erfahren Sie, wie Sie die Seitendaten aus über ein Spaltenüberschriftenmenü filtern.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Anwenden eines Datenfilters über ein Spaltenüberschriftenmenü

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

Sie können beliebig viele Filter gleichzeitig auf eine Spalte anwenden.<!-- True only for entity names, I think: All filters are joined using the AND operator. --> Informationen zum Hinzufügen von mehr als einem Filter gleichzeitig mit allen verfügbaren Metriken finden Sie unter [Anwenden von Datenfiltern in der Symbolleiste](column-filter-apply-from-toolbar.md).

1. Klicken Sie auf der rechten Seite der Spaltenüberschrift auf ![Pfeil nach unten](/help/search-social-commerce/assets/arrow-down-dropdown.png "Pfeil nach unten") und klicken Sie dann auf **[!UICONTROL Add Filter]**.

1. Definieren Sie den Filter für die Spalte :

   * (Filter ohne Eingabefelder) Aktivieren Sie die Kontrollkästchen neben den einzuschließenden Werten und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Hinzufügen").

   * (Filter mit Eingabefeldern) Wählen Sie im zweiten Menü einen Operator aus, geben Sie den entsprechenden Wert ein und klicken Sie dann auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Hinzufügen").

     Wenn Sie beispielsweise die Spalte &quot;[!UICONTROL Clicks]&quot; ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie &quot;*[!UICONTROL greater than]*&quot; aus und geben Sie je nach Datentyp `100` in das Eingabefeld ein. Zu den verfügbaren Operatoren können *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* oder *[!UICONTROL no date]gehören.*

     >[!NOTE]
     >
     >* Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie beispielsweise nach Kampagnen filtern, bei denen im Namen „Kredit“ angegeben ist, umfassen die Ergebnisse „Verbraucherkredite“ und „Kreditanträge“.
     >* Pro Spalte kann nur ein einfacher numerischer Filter angewendet werden (z. B. [!UICONTROL Impressions] \> 100).

>[!MORELIKETHIS]
>
>* [Anwenden von Datenfiltern über die Symbolleiste](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [Spaltenfilter bearbeiten](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [Spaltenfilter entfernen]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
