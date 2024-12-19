---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---
# Feld Anzeigenbeschreibungen in den RSA-Anzeigeneinstellungen

**[!UICONTROL Ad Descriptions]:** Mindestens zwei und bis zu vier Anzeigenbeschreibungen mit optionalen Positionsstiften. Das Anzeigennetzwerk zeigt Anzeigen mit bis zu zwei Beschreibungen an. Geben Sie mindestens zwei ein. Die maximale Länge für jede Beschreibung beträgt 90 Zeichen, einschließlich dynamischer Texte (z. B. Werte von Schlüsselwörtern und Anzeigenanpassungen).

Verwenden Sie zum Einfügen einer Anzeigenanpassung die folgenden Formate, wobei `Default text` ein optionaler Wert ist, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Um eine Beschreibung an eine bestimmte Position zu heften, wählen Sie die Option „Anheften“ (z. B. &quot;[!UICONTROL Pinned at position 1]„). Für jede Position muss mindestens eine Beschreibung verfügbar sein. Wenn Sie mehrere Beschreibungen an derselben Position anheften, enthält die endgültige Anzeige immer eine dieser Beschreibungen an der angegebenen Position. An Position 2 angeheftete Beschreibungen werden in der Anzeige möglicherweise nicht angezeigt.

Um eine zusätzliche Beschreibung hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]**.
