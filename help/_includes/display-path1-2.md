---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---
# Anzeige der Felder Pfad 1 und Anzeigepfad 2 in einigen Anzeigeneinstellungen

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Optional) Text, der der Anzeigen-URL hinzugefügt wird, die automatisch aus der endgültigen URL extrahiert wird. Jeder Pfad wird in der URL durch einen Schrägstrich (`/`). Ein Pfad darf keinen Schrägstrich (`/`) oder Zeilenumbruch (`\n`). Die maximale Länge für jeden Pfad beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.

Verwenden Sie zum Einfügen eines Anzeigenanpassers die folgenden Formate, wobei `Default text` ist ein optionaler Wert, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Wenn beispielsweise [!UICONTROL Display Path 1] auf &quot;Angebote&quot;gesetzt ist und [!UICONTROL Display Path 2] den Wert &quot;local&quot;hat, würde die Anzeige-URL `<display URL>/deals/local`, z. B. www.example.com/deals/local.
