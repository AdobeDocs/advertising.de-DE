---
title: Anwenden von Datenfiltern aus der Symbolleiste
description: Erfahren Sie, wie Sie die Seitendaten in der Symbolleiste filtern.
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Anwenden von Datenfiltern aus der Symbolleiste

Sie können beliebig viele Filter auf eine Ansicht anwenden. Alle Filter werden mithilfe des AND-Operators verbunden.

1. Klicken Sie in der Symbolleiste auf ![Filter](/help/search-social-commerce/assets/filter.png "Filter").

1. Führen Sie in den Filtereinstellungen einen der folgenden Schritte aus:

   * Um einen Filter hinzuzufügen, klicken Sie auf ![Filter hinzufügen](/help/search-social-commerce/assets/add.png "Filter hinzufügen") **[!UICONTROL ADD FILTER]** und führen Sie dann die folgenden Schritte aus:

      1. (Optional) Um die Spaltennamen nach Textzeichenfolge zu filtern, geben Sie die Suchzeichenfolge in das Eingabefeld **[!UICONTROL ADD FILTER]** ein.

      1. Wählen Sie im Spaltenmenü einen Spaltennamen aus.

      1. Definieren Sie den Filter für die Spalte:

         * (Filter ohne Eingabefelder) Klicken Sie neben dem zweiten Menü auf ![Nach-unten-Pfeil](/help/search-social-commerce/assets/arrow-down-expand.png "Nach-unten-Pfeil") und aktivieren Sie dann die Kontrollkästchen neben den einzelnen einzuschließenden Werten.

         * (Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus und geben Sie dann den entsprechenden Wert ein.

           Wenn Sie beispielsweise die Spalte &quot;[!UICONTROL Clicks]&quot; ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie &quot;*[!UICONTROL greater than]*&quot; und geben Sie &quot;`100`&quot; in das Eingabefeld ein.

           Je nach Datentyp können die verfügbaren Operatoren *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* oder *[!UICONTROL no date]sein.*

           **Hinweis:** Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie z. B. nach Kampagnen filtern, deren Name &quot;loan&quot;enthält, umfassen die Ergebnisse &quot;Consumer Loans&quot;und &quot;loan applications&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements] und [!UICONTROL Auto Targets] Ansichten (nur optional) Ändern Sie die Einstellung in &quot;[!UICONTROL Include rows with performance data only]&quot;.

           **Warnung:** Wenn Sie die Option deaktivieren und die Ansicht viele Entitäten ohne Leistungsdaten enthält, dauert die Anzeige der Daten länger.

   * Um einen vorhandenen Filter zu bearbeiten, klicken Sie auf den Filter, ändern Sie die Filterdefinition und klicken Sie dann auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

   * Um einen vorhandenen Filter zu entfernen, klicken Sie neben der Filterdefinition auf **[!UICONTROL X]** .

1. Klicken Sie auf **[!UICONTROL Apply]**.
