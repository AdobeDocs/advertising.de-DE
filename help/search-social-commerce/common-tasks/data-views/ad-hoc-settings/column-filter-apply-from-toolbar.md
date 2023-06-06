---
title: Anwenden von Datenfiltern aus der Symbolleiste
description: Erfahren Sie, wie Sie die Seitendaten in der Symbolleiste filtern.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Anwenden von Datenfiltern aus der Symbolleiste

Sie können beliebig viele Filter auf eine Ansicht anwenden. Alle Filter werden mithilfe des AND-Operators verbunden.

1. Klicken Sie in der Symbolleiste auf ![Filter](/help/search-social-commerce/assets/filter.png "Filter").

1. Führen Sie in den Filtereinstellungen einen der folgenden Schritte aus:

   * Um einen Filter hinzuzufügen, klicken Sie auf ![Filter hinzufügen](/help/search-social-commerce/assets/add.png "Filter hinzufügen") **[!UICONTROL ADD FILTER]** und führen Sie dann die folgenden Schritte aus:

      1. (Optional) Um die Spaltennamen nach Textzeichenfolge zu filtern, geben Sie die Suchzeichenfolge in das **[!UICONTROL ADD FILTER]** Eingabefeld.

      1. Wählen Sie im Spaltenmenü einen Spaltennamen aus.

      1. Definieren Sie den Filter für die Spalte:

         * (Filter ohne Eingabefelder) Klicken Sie auf ![Abwärtspfeil](/help/search-social-commerce/assets/arrow-down-expand.png "Abwärtspfeil") neben dem zweiten Menü und aktivieren Sie dann die Kontrollkästchen neben den einzelnen einzuschließenden Werten.

         * (Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus und geben Sie dann den entsprechenden Wert ein.

            Wenn Sie beispielsweise die[!UICONTROL Clicks]&quot;, und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie *[!UICONTROL greater than]*&quot; und geben Sie `100` im Eingabefeld.

            Je nach Datentyp können die verfügbaren Operatoren Folgendes umfassen: *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* oder *[!UICONTROL no date].*

            **Hinweis:** Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie z. B. nach Kampagnen filtern, deren Name &quot;loan&quot;enthält, umfassen die Ergebnisse &quot;Consumer Loans&quot;und &quot;loan applications&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements]und [!UICONTROL Auto Targets] nur Ansichten; optional) Ändern Sie die Einstellung in &quot;[!UICONTROL Include rows with performance data only].&quot;

            **Warnung:** Wenn Sie die Option deaktivieren und die Ansicht viele Entitäten ohne Leistungsdaten enthält, dauert die Anzeige der Daten länger.
   * Um einen vorhandenen Filter zu bearbeiten, klicken Sie auf den Filter, ändern Sie die Filterdefinition und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

   * Um einen vorhandenen Filter zu entfernen, klicken Sie auf **[!UICONTROL X]** neben der Filterdefinition.


1. Klicken **[!UICONTROL Apply]**.
