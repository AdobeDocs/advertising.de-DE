---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Text-Anzeigenvorlage - Einstellungen für negative Suchbegriffe auf Anzeigengruppenebene

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle Werbenetzwerke außer Yandex; optional) Löscht vorhandene negative Suchbegriffe auf Anzeigengruppenebene, die zuvor mit der Vorlage erstellt wurden, die nicht in den unten stehenden Listen angegeben sind. **Hinweis:** Negative Suchbegriffe, die mit anderen Mitteln erstellt wurden (z. B. in einfachen Bulksheets, den [!UICONTROL Campaigns] -Ansichten oder im Anzeigeneditor des Werbenetzwerks), werden niemals mithilfe der Vorlage entfernt.

**[!UICONTROL Apply these negatives]:** (Alle Anzeigennetzwerke außer [!DNL Yandex]; optional) Alle auf der Ebene der statischen Anzeigengruppe hinzuzufügenden negativen Suchbegriffe. Um mehrere Suchbegriffe oder mehrere Übereinstimmungstypen für denselben Suchbegriff anzugeben, geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

* Negative breite Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)
* Negative Wortgruppenübereinstimmung: `"keyword"`
* Negative exakte Übereinstimmung: `[keyword]`

Die gebräuchliche Syntax für Wortgruppen und exakte Übereinstimmungstypen wird im Bulksheet verwendet, das generiert wird, wenn Sie Feed-Daten über die Vorlage propagieren. **Hinweis:** Sie können die negativen Suchbegriffe nicht auf der Registerkarte [!UICONTROL Keywords] oder in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] sehen.
