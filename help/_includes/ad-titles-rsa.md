---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Feld Anzeigentitel in RSA-Anzeigeneinstellungen

**[!UICONTROL Ad Titles]:** Mindestens drei und bis zu fünfzehn Anzeigentitel (Überschriften) mit optionalen Positionsstiften. Das Anzeigennetzwerk zeigt Anzeigen mit bis zu drei Überschriften an. Geben Sie mindestens drei ein. Die maximale Länge für jeden Titel beträgt 30 Zeichen, einschließlich dynamischer
Text (z. B. die Werte von Schlüsselwörtern und Anzeigenanpassungen).

Verwenden Sie zum Einfügen einer Anzeigenanpassung die folgenden Formate, wobei `Default text` ein optionaler Wert ist, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Um einen Titel an eine bestimmte Position zu heften, wählen Sie die Option Anheften aus (z. B. &quot;[!UICONTROL Pinned at position 1]„). Für jede Position muss mindestens ein Titel verfügbar sein. Wenn Sie mehrere Titel an derselben Position anheften, enthält die endgültige Anzeige immer einen dieser Titel an der angegebenen Position. Titel, die an Position 3 angeheftet sind, werden in der Anzeige möglicherweise nicht angezeigt.

Um einen zusätzlichen Titel hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]**.
