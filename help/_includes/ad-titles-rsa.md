---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---
# Feld &quot;Anzeigentitel&quot;in den RSA-Anzeigeneinstellungen

**[!UICONTROL Ad Titles]:** Mindestens drei und bis zu fünfzehn Anzeigentitel (Überschriften) mit optionalen Positionsnadeln. Das Werbenetzwerk zeigt Anzeigen mit bis zu drei Überschriften an. mindestens drei eingeben. Die maximale Länge für jeden Titel beträgt 30 Zeichen, einschließlich dynamischer Texte (wie die Werte von Suchbegriffen und Anzeigenanpassungen).

Verwenden Sie zum Einfügen eines Anzeigenanpassers die folgenden Formate, wobei `Default text` ist ein optionaler Wert, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Um einen Titel an eine bestimmte Position anzuheften, wählen Sie die Pin-Option aus (z. B.[!UICONTROL Pinned at position 1]&quot;). Für jede Position muss mindestens ein Titel verfügbar sein. Wenn Sie mehrere Titel an dieselbe Position veröffentlichen, enthält die endgültige Anzeige immer einen dieser Titel an der angegebenen Position. Titel, die an Position 3 gekoppelt sind, können nicht mit der Anzeige angezeigt werden.

Um einen weiteren Titel hinzuzufügen, klicken Sie auf **[!UICONTROL + Add]**.
