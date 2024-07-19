---
title: Anwenden von Datenfiltern aus dem Spaltenüberschriftsmenü
description: Erfahren Sie, wie Sie die Seitendaten aus dem Menü einer Spaltenüberschrift filtern.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Anwenden eines Datenfilters aus einem Spaltenüberschriftsmenü

Sie können beliebig viele Filter gleichzeitig auf eine Spalte anwenden. Alle Filter werden mithilfe des AND-Operators verbunden. Informationen zum Hinzufügen mehrerer Filter gleichzeitig mit allen verfügbaren Metriken finden Sie unter &quot;[Anwenden von Datenfiltern aus der Symbolleiste](column-filter-apply-from-toolbar.md)&quot;.

1. Klicken Sie rechts neben der Spaltenüberschrift auf den Pfeil ![Nach-unten](/help/search-social-commerce/assets/arrow-down-dropdown.png "Nach-unten-Pfeil") und klicken Sie dann auf **[!UICONTROL Add Filter]**.

1. Definieren Sie den Filter für die Spalte:

   * (Filter ohne Eingabefelder) Aktivieren Sie die Kontrollkästchen neben dem jeweiligen einzuschließenden Wert und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

   * (Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus, geben Sie den entsprechenden Wert ein und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

     Wenn Sie beispielsweise die Spalte &quot;[!UICONTROL Clicks]&quot; ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie &quot;*[!UICONTROL greater than]*&quot; und geben Sie &quot;`100`&quot; in das Eingabefeld ein. Je nach Datentyp können die verfügbaren Operatoren *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, 2, 13 oder 14.**[!UICONTROL before]**[!UICONTROL after]**[!UICONTROL no date]

     >[!NOTE]
     >
     >* Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie beispielsweise nach Kampagnen filtern, deren Name &quot;loan&quot;enthält, umfassen die Ergebnisse &quot;Consumer Loans&quot;und &quot;loan applications&quot;.
     >* Sie können pro Spalte nur einen einfachen numerischen Filter (z. B. [!UICONTROL Impressions] \> 100) anwenden.
