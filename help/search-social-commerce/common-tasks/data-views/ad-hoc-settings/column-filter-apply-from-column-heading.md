---
title: Anwenden von Datenfiltern aus dem Spaltenüberschriftsmenü
description: Erfahren Sie, wie Sie die Seitendaten aus dem Menü einer Spaltenüberschrift filtern.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Anwenden eines Datenfilters aus einem Spaltenüberschriftsmenü

Sie können beliebig viele Filter gleichzeitig auf eine Spalte anwenden. Alle Filter werden mithilfe des AND-Operators verbunden. Informationen zum Hinzufügen mehrerer Filter gleichzeitig mit allen verfügbaren Metriken finden Sie unter[Anwenden von Datenfiltern aus der Symbolleiste](column-filter-apply-from-toolbar.md).&quot;

1. Klicken Sie rechts neben der Spaltenüberschrift auf ![Abwärtspfeil](/help/search-social-commerce/assets/arrow-down-dropdown.png "Abwärtspfeil")und klicken Sie anschließend auf **[!UICONTROL Add Filter]**.

1. Definieren Sie den Filter für die Spalte:

   * (Filter ohne Eingabefelder) Aktivieren Sie die Kontrollkästchen neben den jeweiligen einzuschließenden Werten und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

   * (Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus, geben Sie den entsprechenden Wert ein und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

      Wenn Sie beispielsweise die[!UICONTROL Clicks]&quot;, und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie *[!UICONTROL greater than]*&quot; und geben Sie `100` im Eingabefeld Je nach Datentyp können die verfügbaren Operatoren Folgendes enthalten: *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* oder *[!UICONTROL no date].*

      >[!NOTE]
      >
      >* Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie beispielsweise nach Kampagnen filtern, deren Name &quot;loan&quot;enthält, umfassen die Ergebnisse &quot;Consumer Loans&quot;und &quot;loan applications&quot;.
      >* Sie können nur einen einzigen numerischen Filter anwenden (z. B. [!UICONTROL Impressions] \> 100) pro Spalte.

