---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Text-Anzeigenvorlage - Feed-Filter

**\[Feed-Filter\]:** Welche Zeilen in der Feed-Datei werden übertragen:

* *[!UICONTROL Propagate all rows found in feed:]* (Standard) Zum Übertragen von Daten für alle Zeilen.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Um Daten nur für Zeilen zu übertragen, die bis zu zehn angegebene Bedingungen erfüllen. Geben Sie die anzuwendenden Filter an:

   1. Wählen Sie den für alle Filter zu verwendenden Booleschen Vorgang aus: **[!UICONTROL AND]** oder **[!UICONTROL OR]**.

   1. Wählen Sie im ersten Menü einen Spaltennamen aus, wählen Sie einen Operator aus dem zweiten Menü aus und geben Sie dann entweder die entsprechenden Werte ein oder lassen Sie das Eingabefeld leer, um Daten für Zeilen ohne Bedingungen zu übertragen.

  Die Spaltenliste enthält alle verfügbaren Spalten im Feed.

  Zu den verfügbaren Operatoren gehören *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (ist nicht gleich), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]* und *[!UICONTROL greater than]*. Wenn Sie den Operator &quot;[!UICONTROL in]&quot; auswählen, können Sie eine kommagetrennte Liste von Werten eingeben. Wenn ein Datensatz einen der angegebenen Werte erfüllt, werden Daten für diese Zeilen übertragen. Geben Sie für alle anderen Operatoren nur einen Wert ein. Bei Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.

  Wenn Sie beispielsweise die Spalte &quot;product_type&quot;ausgewählt haben und nur Zeilen für Produktnamen mit &quot;Schuhe&quot;zurückgeben möchten, wählen Sie &quot;**[!UICONTROL contains]**&quot;und geben Sie im Eingabefeld `shoes` ein.

   1. (Um bis zu neun zusätzliche Filter anzuwenden) Klicken Sie für jeden zusätzlichen Filter auf **[!UICONTROL Add Condition]** und geben Sie dann den zusätzlichen Filter nach Schritt 2 an.
