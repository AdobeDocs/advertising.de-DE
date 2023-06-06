---
title: Spaltenfilter bearbeiten
description: Erfahren Sie, wie Sie Spaltenfilter bearbeiten.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Spaltenfilter bearbeiten

## Filtersatz bearbeiten

1. Klicken ![Filter](/help/search-social-commerce/assets/filter.png "Filter") in der Symbolleiste.

1. Führen Sie in den Filtereinstellungen einen der folgenden Schritte aus:

   * Um einen Filter hinzuzufügen, klicken Sie auf ![Filter hinzufügen](/help/search-social-commerce/assets/add.png "Filter hinzufügen") **[!UICONTROL ADD FILTER]** und führen Sie dann die folgenden Schritte aus:

      1. (Optional) Um die Spaltennamen nach Textzeichenfolge zu filtern, geben Sie die Suchzeichenfolge in das **[!UICONTROL ADD FILTER]** Eingabefeld.

      1. Wählen Sie im Spaltenmenü einen Spaltennamen aus.

      1. Definieren Sie den Filter für die Spalte:

         * (Filter ohne Eingabefelder) Klicken Sie auf ![Abwärtspfeil](/help/search-social-commerce/assets/arrow-down-expand.png "Abwärtspfeil") Aktivieren Sie neben dem zweiten Menü die Kontrollkästchen neben den einzelnen einzuschließenden Werten und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

         * (Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus, geben Sie den entsprechenden Wert ein und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

            Wenn Sie beispielsweise die[!UICONTROL Clicks]&quot;, und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie *[!UICONTROL greater than]*&quot; und geben Sie `100` im Eingabefeld.

            Je nach Datentyp können die verfügbaren Operatoren Folgendes umfassen: *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]* oder *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* oder *[!UICONTROL no date].*

            **Hinweis:** Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie z. B. nach Kampagnen suchen, deren Name &quot;loan&quot;enthält, umfassen die Ergebnisse &quot;Consumer Loans&quot;und &quot;loan applications&quot;.
   * Um einen vorhandenen Filter zu bearbeiten, klicken Sie auf den Filter, ändern Sie die Filterdefinition und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

   * Um einen vorhandenen Filter zu entfernen, klicken Sie auf **[!UICONTROL X]** neben der Filterdefinition.


1. ([!UICONTROL Keywords] nur Ansicht; optional) Wählen Sie die Einstellung &quot;[!UICONTROL Include rows with no performance data].&quot;

   >[!WARNING]
   >
   >Wenn Sie diese Option auswählen, wird die Seitenladezeit verlängert.

1. Klicken **[!UICONTROL Apply]**.

## Einzelfilter bearbeiten

1. (Falls erforderlich) Klicken Sie im Filtersatz über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more-filters.png "Mehr") , um den Filtersatz zu erweitern.

1. Klicken Sie über der Datentabelle auf die Filterdefinition.

1. Bearbeiten Sie die anzuwendenden Filter:

   1. (Optional) Bearbeiten Sie den Spaltennamen im Spaltenmenü.

   1. (Optional) Definieren Sie den Filter für die Spalte neu:

      * (Filter ohne Eingabefelder) Klicken Sie auf ![Abwärtspfeil](/help/search-social-commerce/assets/arrow-down-expand.png "Abwärtspfeil") Aktivieren Sie neben dem zweiten Menü die Kontrollkästchen neben den einzelnen einzuschließenden Werten und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

      * (Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus, geben Sie den entsprechenden Wert ein und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

         Wenn Sie beispielsweise die[!UICONTROL Clicks]&quot;, und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie *[!UICONTROL greater than]*&quot; und geben Sie `100` im Eingabefeld

         Je nach Datentyp können die verfügbaren Operatoren Folgendes umfassen: *[!UICONTROL greater than]*, *kleiner als*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *nicht enthält* oder *beginnt mit.*

         **Hinweis:** Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie z. B. nach Kampagnen suchen, deren Name &quot;loan&quot;enthält, umfassen die Ergebnisse &quot;Consumer Loans&quot;und &quot;loan applications&quot;.
