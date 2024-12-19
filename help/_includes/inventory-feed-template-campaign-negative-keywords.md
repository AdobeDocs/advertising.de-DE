---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Text und Vorlage - Einstellungen für negative Keywords auf Kampagnenebene

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle Werbenetzwerke außer Yandex; optional) Löscht vorhandene negative Keywords auf Kampagnenebene, die zuvor mit der Vorlage erstellt wurden und nicht in den folgenden Listen angegeben sind. **Hinweis** Negative Keywords, die auf andere Weise erstellt wurden (z. B. in einfachen Bulksheets, in den [!UICONTROL Campaigns] oder im Anzeigeneditor des Werbenetzwerks) werden niemals mithilfe der Vorlage entfernt.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Alle Werbenetzwerke außer Yandex; optional) Ermöglicht die Angabe negativer Keywords für Kampagnen, deren Name eine angegebene Zeichenfolge enthält. Wenn Sie diese Option auswählen, können Sie bis zu drei Kampagnennamen und entsprechende Keywords hinzufügen.

Klicken Sie für jede Zeichenfolge auf **[!UICONTROL Add (Up to 3)]** und geben Sie die folgenden Informationen ein:

* **[!UICONTROL If campaign name contains]:** Eine Textzeichenfolge, nach der im Kampagnennamen gesucht werden soll. Bei der Abfrage wird zwischen Groß- und Kleinschreibung unterschieden (z. B. entspricht &quot;[!DNL Car]&quot; dem Kampagnennamen &quot;[!DNL Car Parts]&quot;, nicht jedoch &quot;[!DNL INTERIOR CAR ACCESSORIES]„).

* **[!UICONTROL Apply these negatives]:** Alle statischen negativen Keywords auf Kampagnenebene, die für Kampagnen hinzugefügt werden sollen, deren Name die angegebene Zeichenfolge enthält. Um mehrere Keywords oder mehrere Übereinstimmungstypen für dasselbe Keyword anzugeben, geben Sie sie in separaten Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

   * Negative weit gefasste Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)
   * Negative Übereinstimmung der Phrasen: `"keyword"`
   * Negative exakte Übereinstimmung: `[keyword]`

Die übliche Syntax für Phrasen und exakte Übereinstimmungstypen wird in der Bulksheet verwendet, die erstellt wird, wenn Feed-Daten über die Vorlage übertragen werden. **Hinweis** Die negativen Keywords werden auf der Registerkarte &quot;[!UICONTROL Keywords]&quot; oder in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] nicht angezeigt.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Alle Werbenetzwerke außer [!DNL Yandex]; optional) Alle statischen negativen Keywords auf Kampagnenebene, die für Kampagnen hinzugefügt werden sollen, deren Name nicht mit einer angegebenen Zeichenfolge übereinstimmt. Um mehrere Keywords oder mehrere Übereinstimmungstypen für dasselbe Keyword anzugeben, geben Sie sie in separaten Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

* Negative weit gefasste Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)
* Negative Übereinstimmung der Phrasen: `"keyword"`
* Negative exakte Übereinstimmung: `[keyword]`

Die übliche Syntax für Phrasen und exakte Übereinstimmungstypen wird in der Bulksheet verwendet, die erstellt wird, wenn Feed-Daten über die Vorlage übertragen werden. **Hinweis** Die negativen Keywords werden auf der Registerkarte &quot;[!UICONTROL Keywords]&quot; oder in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] nicht angezeigt.
