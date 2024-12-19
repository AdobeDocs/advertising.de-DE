---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Text und Vorlage - Einstellungen für negative Keywords auf Anzeigengruppenebene

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle Werbenetzwerke außer Yandex; optional) Löscht vorhandene negative Schlüsselwörter auf Anzeigengruppenebene, die zuvor mit der Vorlage erstellt wurden und nicht in den folgenden Listen angegeben sind. **Hinweis** Negative Keywords, die auf andere Weise erstellt wurden (z. B. in einfachen Bulksheets, in den [!UICONTROL Campaigns] oder im Anzeigeneditor des Werbenetzwerks) werden niemals mithilfe der Vorlage entfernt.

**[!UICONTROL Apply these negatives]:** (Alle Anzeigennetzwerke außer [!DNL Yandex]; optional) Alle statischen negativen Schlüsselwörter auf Anzeigengruppenebene, die hinzugefügt werden sollen. Um mehrere Keywords oder mehrere Übereinstimmungstypen für dasselbe Keyword anzugeben, geben Sie sie in separaten Zeilen ein. Verwenden Sie die folgende Syntax ohne Minuszeichen:

* Negative weit gefasste Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)
* Negative Übereinstimmung der Phrasen: `"keyword"`
* Negative exakte Übereinstimmung: `[keyword]`

Die übliche Syntax für Phrasen und exakte Übereinstimmungstypen wird in der Bulksheet verwendet, die erstellt wird, wenn Feed-Daten über die Vorlage übertragen werden. **Hinweis** Die negativen Keywords werden auf der Registerkarte &quot;[!UICONTROL Keywords]&quot; oder in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] nicht angezeigt.
