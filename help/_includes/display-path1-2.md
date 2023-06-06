---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Anzeige der Felder Pfad 1 und Anzeigepfad 2 in einigen Anzeigeneinstellungen

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Optional) Text, der der Anzeigen-URL hinzugefügt wird, die automatisch aus der endgültigen URL extrahiert wird. Jeder Pfad wird in der URL durch einen Schrägstrich (`/`). Ein Pfad darf keinen Schrägstrich (`/`) oder Zeilenumbruch (`\n`). Die maximale Länge für jeden Pfad beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.

Verwenden Sie zum Einfügen eines Anzeigenanpassers die folgenden Formate, wobei `Default text` ist ein optionaler Wert, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Wenn beispielsweise der Anzeigepfad 1 &quot;Angebote&quot;und der Anzeigepfad 2 &quot;lokal&quot;lautet, wäre die Anzeige-URL `<display URL>/deals/local`, z. B. www.example.com/deals/local.
