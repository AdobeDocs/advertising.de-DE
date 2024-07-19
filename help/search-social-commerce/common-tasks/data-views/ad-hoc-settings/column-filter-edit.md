---
title: Spaltenfilter bearbeiten
description: Erfahren Sie, wie Sie Spaltenfilter bearbeiten.
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Spaltenfilter bearbeiten

## Filtersatz bearbeiten

1. Klicken Sie in der Symbolleiste auf ![Filter](/help/search-social-commerce/assets/filter.png "Filter") .

1. Führen Sie in den Filtereinstellungen einen der folgenden Schritte aus:

   * Um einen Filter hinzuzufügen, klicken Sie auf ![Filter hinzufügen](/help/search-social-commerce/assets/add.png "Filter hinzufügen") **[!UICONTROL ADD FILTER]** und führen Sie dann die folgenden Schritte aus:

      1. (Optional) Um die Spaltennamen nach Textzeichenfolge zu filtern, geben Sie die Suchzeichenfolge in das Eingabefeld **[!UICONTROL ADD FILTER]** ein.

      1. Wählen Sie im Spaltenmenü einen Spaltennamen aus.

      1. Definieren Sie den Filter für die Spalte:

         * (Filter ohne Eingabefelder) Klicken Sie neben dem zweiten Menü auf ![Nach-unten-Pfeil](/help/search-social-commerce/assets/arrow-down-expand.png "Nach-unten-Pfeil") , aktivieren Sie die Kontrollkästchen neben den jeweiligen einzuschließenden Werten und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

         * (Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus, geben Sie den entsprechenden Wert ein und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

           Wenn Sie beispielsweise die Spalte &quot;[!UICONTROL Clicks]&quot; ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie &quot;*[!UICONTROL greater than]*&quot; und geben Sie &quot;`100`&quot; in das Eingabefeld ein.

           Je nach Datentyp können die verfügbaren Operatoren *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* oder *[!UICONTROL no date]sein.*

           **Hinweis:** Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie z. B. nach Kampagnen suchen, deren Name &quot;loan&quot;enthält, umfassen die Ergebnisse &quot;Consumer Loans&quot;und &quot;loan applications&quot;.

   * Um einen vorhandenen Filter zu bearbeiten, klicken Sie auf den Filter, ändern Sie die Filterdefinition und klicken Sie dann auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

   * Um einen vorhandenen Filter zu entfernen, klicken Sie neben der Filterdefinition auf **[!UICONTROL X]** .

1. ([!UICONTROL Keywords] nur Ansicht; optional) Wählen Sie die Einstellung &quot;[!UICONTROL Include rows with no performance data]&quot; aus oder heben Sie die Auswahl auf.

   >[!WARNING]
   >
   >Wenn Sie diese Option auswählen, wird die Seitenladezeit verlängert.

1. Klicken Sie auf **[!UICONTROL Apply]**.

## Einzelfilter bearbeiten

1. (Falls erforderlich) Klicken Sie im Filtersatz über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more-filters.png "Mehr") , um den Filtersatz zu erweitern.

1. Klicken Sie über der Datentabelle auf die Filterdefinition.

1. Bearbeiten Sie die anzuwendenden Filter:

   1. (Optional) Bearbeiten Sie den Spaltennamen im Spaltenmenü.

   1. (Optional) Definieren Sie den Filter für die Spalte neu:

      * (Filter ohne Eingabefelder) Klicken Sie neben dem zweiten Menü auf ![Nach-unten-Pfeil](/help/search-social-commerce/assets/arrow-down-expand.png "Nach-unten-Pfeil") , aktivieren Sie die Kontrollkästchen neben den jeweiligen einzuschließenden Werten und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

      * (Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus, geben Sie den entsprechenden Wert ein und klicken Sie auf ![Filter aktualisieren](/help/search-social-commerce/assets/select.png "Filter aktualisieren").

        Wenn Sie beispielsweise die Spalte &quot;[!UICONTROL Clicks]&quot; ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie &quot;*[!UICONTROL greater than]*&quot; und geben Sie &quot;`100`&quot; in das Eingabefeld ein.

        Je nach Datentyp können die verfügbaren Operatoren *[!UICONTROL greater than]*, *kleiner als*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *nicht enthält* oder *beginnt mit* sein.

        **Hinweis:** Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie z. B. nach Kampagnen suchen, deren Name &quot;loan&quot;enthält, umfassen die Ergebnisse &quot;Consumer Loans&quot;und &quot;loan applications&quot;.
