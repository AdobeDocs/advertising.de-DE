---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Text-Anzeigenvorlage - Einstellungen für negative Keywords auf Kampagnenebene

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle Werbenetzwerke außer Yandex; optional) Löscht vorhandene negative Suchbegriffe auf Kampagnenebene, die zuvor mit der Vorlage erstellt wurden, die nicht in den unten stehenden Listen angegeben sind. **Hinweis:** Negative Suchbegriffe, die mit anderen Mitteln erstellt wurden (z. B. in einfachen Bulksheets, den [!UICONTROL Campaigns] -Ansichten oder im Anzeigeneditor des Werbenetzwerks), werden niemals mithilfe der Vorlage entfernt.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Alle Werbenetzwerke außer Yandex; optional) Ermöglicht die Angabe negativer Suchbegriffe für Kampagnen, deren Name eine bestimmte Zeichenfolge enthält. Wenn Sie diese Option auswählen, können Sie bis zu drei Kampagnennamen-Zeichenfolgen und zugehörige Suchbegriffe hinzufügen.

Klicken Sie für jede Zeichenfolge auf **[!UICONTROL Add (Up to 3)]** und geben Sie die folgenden Informationen ein:

* **[!UICONTROL If campaign name contains]:** Eine Textzeichenfolge, nach der an einer beliebigen Stelle im Kampagnennamen gesucht werden soll. Bei der Abfrage wird zwischen Groß- und Kleinschreibung unterschieden (z. B. &quot;[!DNL Car]&quot; entspricht dem Kampagnennamen &quot;[!DNL Car Parts]&quot;, nicht aber &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;).

* **[!UICONTROL Apply these negatives]:** Alle statischen negativen Suchbegriffe auf Kampagnenebene, die für Kampagnen hinzugefügt werden, deren Name die angegebene Zeichenfolge enthält. Um mehrere Suchbegriffe oder mehrere Übereinstimmungstypen für denselben Suchbegriff anzugeben, geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

   * Negative breite Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)
   * Negative Wortgruppenübereinstimmung: `"keyword"`
   * Negative exakte Übereinstimmung: `[keyword]`

Die gebräuchliche Syntax für Wortgruppen und exakte Übereinstimmungstypen wird im Bulksheet verwendet, das generiert wird, wenn Sie Feed-Daten über die Vorlage propagieren. **Hinweis:** Sie können die negativen Suchbegriffe nicht auf der Registerkarte [!UICONTROL Keywords] oder in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] sehen.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Alle Anzeigennetzwerke außer [!DNL Yandex]; optional) Alle statischen negativen Suchbegriffe auf Kampagnenebene, die für Kampagnen hinzugefügt werden sollen, deren Name nicht mit einer angegebenen Zeichenfolge übereinstimmt. Um mehrere Suchbegriffe oder mehrere Übereinstimmungstypen für denselben Suchbegriff anzugeben, geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

* Negative breite Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)
* Negative Wortgruppenübereinstimmung: `"keyword"`
* Negative exakte Übereinstimmung: `[keyword]`

Die gebräuchliche Syntax für Wortgruppen und exakte Übereinstimmungstypen wird im Bulksheet verwendet, das generiert wird, wenn Sie Feed-Daten über die Vorlage propagieren. **Hinweis:** Sie können die negativen Suchbegriffe nicht auf der Registerkarte [!UICONTROL Keywords] oder in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] sehen.
