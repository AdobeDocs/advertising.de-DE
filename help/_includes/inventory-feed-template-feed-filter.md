---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Text und Vorlage - Feedfilter

**\[Feed-Filter\]:** Welche Zeilen in der Feed-Datei übertragen werden sollen:

* *[!UICONTROL Propagate all rows found in feed:]* (Standard), um Daten für alle Zeilen auszudehnen.

* *[!UICONTROL Propagate rows that meet certain conditions:]* So übertragen Sie Daten nur für Zeilen, die bis zu zehn angegebene Bedingungen erfüllen. Angeben der anzuwendenden Filter:

   1. Wählen Sie den für alle Filter zu verwendenden booleschen Vorgang aus: **[!UICONTROL AND]** oder **[!UICONTROL OR]**.

   1. Wählen Sie einen Spaltennamen aus dem ersten Menü aus, wählen Sie einen Operator aus dem zweiten Menü aus und geben Sie dann entweder die entsprechenden Werte ein oder lassen Sie das Eingabefeld leer, um Daten für Zeilen ohne Bedingungen zu übertragen.

  Die Spaltenliste enthält alle verfügbaren Spalten im Feed.

  Zu den verfügbaren Operatoren gehören *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (ist nicht gleich), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]* und *[!UICONTROL greater than]*. Wenn Sie den Operator &quot;[!UICONTROL in]&quot; auswählen, können Sie eine kommagetrennte Liste von Werten eingeben. Wenn ein Datensatz einem der angegebenen Werte entspricht, werden die Daten für diese Zeilen weitergegeben. Geben Sie für alle anderen Operatoren nur einen Wert ein. Bei Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.

  Wenn Sie beispielsweise die Spalte „product_type“ ausgewählt haben und nur Zeilen für Produktnamen mit „Schuhe“ zurückgeben möchten, wählen Sie &quot;**[!UICONTROL contains]**&quot; aus und geben Sie `shoes` in das Eingabefeld ein.

   1. (So wenden Sie bis zu neun zusätzliche Filter an) Klicken Sie für jeden zusätzlichen Filter auf **[!UICONTROL Add Condition]** und geben Sie dann den zusätzlichen Filter pro Schritt 2 an.
