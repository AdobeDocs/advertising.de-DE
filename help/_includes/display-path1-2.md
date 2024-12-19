---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Die Felder Pfad 1 und Pfad 2 in einigen Anzeigeneinstellungen anzeigen

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Optional) Text, der zur Anzeige-URL hinzugefügt wird, die automatisch aus der endgültigen URL extrahiert wird. Jedem Pfad wird in der URL ein Schrägstrich (`/`) vorangestellt. Ein Pfad darf keine Schrägstriche (`/`) oder Zeilenumbrüche (`\n`) enthalten. Die maximale Länge für jeden Pfad beträgt 15 Zeichen oder 7 Doppelbyte-Zeichen.

Verwenden Sie zum Einfügen einer Anzeigenanpassung die folgenden Formate, wobei `Default text` ein optionaler Wert ist, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Wenn [!UICONTROL Display Path 1] beispielsweise „Angebote“ und [!UICONTROL Display Path 2] „lokal“ ist, wäre die Anzeige-URL `<display URL>/deals/local`, z. B. www.example.com/deals/local.
