---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---
# Anzeigenbeschreibungsfeld in den RSA-Anzeigeneinstellungen

**[!UICONTROL Ad Descriptions]:** Mindestens zwei und bis zu vier Anzeigenbeschreibungen mit optionalen Positionstiften. Das Werbenetzwerk zeigt Anzeigen mit bis zu zwei Beschreibungen an. mindestens zwei eingeben. Die maximale Länge für jede Beschreibung beträgt 90 Zeichen, einschließlich dynamischer Texte (z. B. Suchbegriffe und Anzeigenanpassungen).

Verwenden Sie zum Einfügen eines Anzeigenanpassers die folgenden Formate, wobei `Default text` ist ein optionaler Wert, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Um eine Beschreibung an eine bestimmte Position anzuheften, wählen Sie die Pinoption aus (z. B.[!UICONTROL Pinned at position 1]&quot;). Für jede Position muss mindestens eine Beschreibung verfügbar sein. Wenn Sie mehrere Beschreibungen an derselben Position veröffentlichen, enthält die endgültige Anzeige immer eine dieser Beschreibungen an der angegebenen Position. In Position 2 enthaltene Beschreibungen werden möglicherweise nicht zusammen mit der Anzeige angezeigt.

Um eine weitere Beschreibung hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]**.
