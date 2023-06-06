---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Text-Anzeigenvorlage - Einstellungen für negative Suchbegriffe auf Anzeigengruppenebene

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle Anzeigennetze außer Yandex; (optional) Löscht vorhandene negative Suchbegriffe auf Anzeigengruppenebene, die zuvor mit der Vorlage erstellt wurden, die nicht in den unten stehenden Listen angegeben sind. **Hinweis:** Negative Suchbegriffe, die mit anderen Mitteln erstellt wurden (z. B. in einfachen Bulksheets, [!UICONTROL Campaigns] -Ansichten oder im Anzeigen-Editor des Werbenetzwerks) niemals mithilfe der Vorlage entfernt werden.

**[!UICONTROL Apply these negatives]:** (Alle Anzeigennetze außer [!DNL Yandex]; (optional) Alle statischen negativen Suchbegriffe auf Anzeigengruppenebene, die hinzugefügt werden sollen. Um mehrere Suchbegriffe oder mehrere Übereinstimmungstypen für denselben Suchbegriff anzugeben, geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

* Negatives breites Match: `keyword` (nicht unterstützt von [!DNL Microsoft Advertising])
* Negative Wortgruppenübereinstimmung: `"keyword"`
* Negative exakte Übereinstimmung: `[keyword]`

Die gebräuchliche Syntax für Wortgruppen und exakte Übereinstimmungstypen wird im Bulksheet verwendet, das generiert wird, wenn Sie Feed-Daten über die Vorlage propagieren. **Hinweis:** Sie können die negativen Suchbegriffe nicht im [!UICONTROL Keywords] oder im [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] anzeigen.
