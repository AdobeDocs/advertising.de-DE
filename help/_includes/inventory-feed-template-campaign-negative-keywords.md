---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Text-Anzeigenvorlage - Einstellungen für negative Keywords auf Kampagnenebene

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle Anzeigennetze außer Yandex; (optional) Löscht vorhandene negative Suchbegriffe auf Kampagnenebene, die zuvor mit der Vorlage erstellt wurden, die nicht in den unten stehenden Listen angegeben sind. **Hinweis:** Negative Suchbegriffe, die mit anderen Mitteln erstellt wurden (z. B. in einfachen Bulksheets, [!UICONTROL Campaigns] -Ansichten oder im Anzeigen-Editor des Werbenetzwerks) niemals mithilfe der Vorlage entfernt werden.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Alle Anzeigennetze außer Yandex; optional) Ermöglicht die Angabe negativer Suchbegriffe für Kampagnen, deren Name eine bestimmte Zeichenfolge enthält. Wenn Sie diese Option auswählen, können Sie bis zu drei Kampagnennamen-Zeichenfolgen und zugehörige Suchbegriffe hinzufügen.

Klicken Sie für jede Zeichenfolge auf **[!UICONTROL Add (Up to 3)]** und geben Sie folgende Informationen ein:

* **[!UICONTROL If campaign name contains]:**  Eine Textzeichenfolge, die an einer beliebigen Stelle im Kampagnennamen gesucht werden soll. Bei der Abfrage wird zwischen Groß- und Kleinschreibung unterschieden (z. B. &quot;[!DNL Car]&quot; stimmt mit dem Kampagnennamen überein. &quot;[!DNL Car Parts]&quot;, aber nicht &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;).

* **[!UICONTROL Apply these negatives]:**  Alle statischen negativen Suchbegriffe auf Kampagnenebene, die für Kampagnen hinzugefügt werden sollen, deren Name die angegebene Zeichenfolge enthält. Um mehrere Suchbegriffe oder mehrere Übereinstimmungstypen für denselben Suchbegriff anzugeben, geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

   * Negatives breites Match: `keyword` (nicht unterstützt von [!DNL Microsoft Advertising])
   * Negative Wortgruppenübereinstimmung: `"keyword"`
   * Negative exakte Übereinstimmung: `[keyword]`

Die gebräuchliche Syntax für Wortgruppen und exakte Übereinstimmungstypen wird im Bulksheet verwendet, das generiert wird, wenn Sie Feed-Daten über die Vorlage propagieren. **Hinweis:** Sie können die negativen Suchbegriffe nicht im [!UICONTROL Keywords] oder im [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] anzeigen.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Alle Anzeigennetze außer [!DNL Yandex]; (optional) Alle statischen negativen Suchbegriffe auf Kampagnenebene, die für Kampagnen hinzugefügt werden, deren Name nicht mit einer angegebenen Zeichenfolge übereinstimmt. Um mehrere Suchbegriffe oder mehrere Übereinstimmungstypen für denselben Suchbegriff anzugeben, geben Sie sie in separate Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

* Negatives breites Match: `keyword` (nicht unterstützt von [!DNL Microsoft Advertising])
* Negative Wortgruppenübereinstimmung: `"keyword"`
* Negative exakte Übereinstimmung: `[keyword]`

Die gebräuchliche Syntax für Wortgruppen und exakte Übereinstimmungstypen wird im Bulksheet verwendet, das generiert wird, wenn Sie Feed-Daten über die Vorlage propagieren. **Hinweis:** Sie können die negativen Suchbegriffe nicht im [!UICONTROL Keywords] oder im [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] anzeigen.
