---
title: Regeleinstellungen für Konversionswert [!DNL Google Ads]
description: Verweisen Sie auf die Einstellungen  [!DNL Google Ads]  Konversionswertregeln.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Regeleinstellungen für Konversionswert [!DNL Google Ads]

<!-- Go through all -->

| Abschnitt | Parameter | Beschreibung |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | Das Werbenetzwerk. |
| | [!UICONTROL Account] | Das Netzwerkkonto der Anzeige. |
| | [!UICONTROL Campaign] | Die Werbekampagne. |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[Bedingungstyp\] | (Schreibgeschützt für bestehende Regeln) Der Bedingungstyp, der erfüllt sein muss, damit eine Wertanpassung Trigger wird:<ul><li>**Gerät:** alle oder bestimmte Gerätetypen auszuwählen.</li><li>**Standort:** Um alle Länder und Gebiete anzusprechen oder bestimmte Standorte anzusprechen und auszuschließen.</li><li>**Zielgruppen:** Alle oder bestimmte Zielgruppen anzusprechen</li></ul>**Hinweis:** Alle Regeln in einem Konto müssen denselben Typ von primären und (optionalen) sekundären Bedingungen verwenden. Wenn beispielsweise Regel 1 die primäre Bedingung „Zielgruppe“ und die sekundäre Bedingung „Standort“ enthält, müssen alle anderen Regeln im Konto die primäre Bedingung „Zielgruppe“ aufweisen. Wenn die anderen Regeln eine sekundäre Bedingung enthalten, muss sie „Standort“ lauten. |
| | Bedingungstyp > Gerät | (Nur Gerätebedingungen) Welche Gerätetypen angesprochen werden sollen:<ul><li>**Alle Geräte** - Zum Auswählen aller Gerätetypen.</li><li>**Geräte auswählen** - Geben Sie einen oder mehrere Gerätetypen als Ziel an: **Desktop**, **Mobile** und **Tablet**.</li></ul>Innerhalb einer Bedingung werden mehrere Ziele mithilfe des booleschen Operators OR verbunden, sodass jede Option zum Initiieren einer Wertanpassung erfüllt werden kann. Beispiel: Wenn \[Gerät ist Mobil ODER Tablet\], dann fügen Sie 1.5. |
| | Bedingungstyp > Standort | (Nur Standortbedingungen) Die Standortziele und -ausschlüsse:<ul><li>**Alle Länder und Gebiete** — Um alle Länder und Orte anzusprechen oder bestimmte Orte anzusprechen und auszuschließen.</li><li>**Speicherort eingeben** - Zum Auswählen und Ausschließen bestimmter Speicherorte.</li></ul><ul><li>Um einen Speicherort oder Unterspeicherort zu erweitern, klicken Sie auf > nach dem Namen.</li><li>Um eine Zielgruppe hinzuzufügen, wählen Sie die Zielgruppe einmal aus, um ein grünes Häkchen anzuzeigen.</li><li>Um eine Zielgruppe auszuschließen, wählen Sie die Zielgruppe ein zweites Mal aus, um eine rote **[!UICONTROL X]** anzuzeigen.</li><li>Um eine Zielgruppe oder einen Ausschluss zu entfernen, führen Sie einen der folgenden Schritte aus:<ul><li>Klicken Sie ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen") neben dem Element in der Spalte &quot;[!UICONTROL Selections]&quot;.</li><li>Wählen Sie das Ziel aus, bis kein Häkchen oder [!UICONTROL X] angezeigt wird.</li></ul></li></ul>Innerhalb einer Bedingung werden mehrere Ziele oder Ausschlüsse mit dem booleschen Operator ODER verbunden, sodass jede Option zum Initiieren einer Wertanpassung erfüllt sein kann. Beispiel: Wenn \[Standort Algerien ODER Tunesien\] ist, fügen Sie 1.5 hinzu. |
| | Bedingungstyp > Zielgruppe | (Nur Zielgruppenbedingungen) Die Zielgruppe zielt auf Folgendes ab:<ul><li>**Alle Zielgruppensegmente** - Zum Auswählen aller Zielgruppensegmente [!DNL Google Ads].</li><li>**Zielgruppensegmente eingeben** - Zum Targeting bestimmter Zielgruppensegmente [!DNL Google Ads].</li></ul><ul><li>Um eine Kategorie oder Unterkategorie in ihre Segmente zu erweitern, klicken Sie auf > nach dem Namen.</li><li>Um ein Ziel hinzuzufügen, wählen Sie das Ziel aus.</li><li>Um eine Zielgruppe zu entfernen, heben Sie die Auswahl der Zielgruppe auf oder klicken Sie ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen") neben dem Element in der Spalte „Auswahl“.</li></ul>Innerhalb einer Bedingung werden mehrere Ziele oder Ausschlüsse mit dem booleschen Operator ODER verbunden, sodass jede Option zum Initiieren einer Wertanpassung erfüllt sein kann. Beispiel: Wenn \[Zielgruppe sind Sonderangebotsreisende ODER Familienurlauber\], dann ist 1.5.<br><br>**Hinweis:** Nachdem Sie eine Zielgruppe gespeichert haben, können Sie zusätzliche Zielgruppen hinzufügen, sie jedoch nicht außerhalb des [!DNL Google Ads]-Editors entfernen. Wenn Sie eine Zielgruppe entfernen müssen, melden Sie sich direkt bei [!DNL Google Ads] an und verwenden Sie den [!DNL Google Ads]. |
| Bedingungen > Sekundäre Bedingung | | (Optional, schreibgeschützt für bestehende Regeln) Der Bedingungstyp, der erfüllt werden muss, um eine Wertanpassung in den Trigger zu bringen. Wenn Sie eine sekundäre Bedingung einbeziehen, wird die sekundäre Bedingung mit dem booleschen Operator ALL mit der primären Bedingung verbunden, sodass beide Bedingungen erfüllt sein müssen, um eine Wertanpassung zu initiieren. Beispiel: Wenn \[Standort Algerien ODER Tunesien\] UND \[Gerät ist Mobil ODER Tablet\] ist, fügen Sie 1.5.<br><br> hinzu. Beschreibungen zu Primären Bedingungen finden Sie in den Einträgen.<br><br>**Hinweis:** Alle Regeln in einem Konto müssen denselben Typ von primären und (optionalen) sekundären Bedingungen verwenden. Wenn beispielsweise Regel 1 die primäre Bedingung „Zielgruppe“ und die sekundäre Bedingung „Standort“ enthält, müssen alle anderen Regeln im Konto die primäre Bedingung „Zielgruppe“ aufweisen. Wenn die anderen Regeln eine sekundäre Bedingung enthalten, muss sie „Standort“ lauten. |
| Wertberichtigung | Wert | Geben Sie den Anpassungstyp an, und geben Sie dann einen positiven Wert ein:<ul><li>**Hinzufügen** - Fügt den angegebenen Wert zum übergebenen Konversionswert hinzu. Der Wert muss größer als null (0) sein.</li><li>**Multiplizieren** - Multipliziert den Konversionswert, der mit dem angegebenen Wert übergeben wird. Der Wert muss zwischen 0,5 und 10 liegen.</li></ul> |

>[!MORELIKETHIS]
>
>* [Über [!DNL Google Ads] Konversionswertregeln](about-google-conversion-value-rules.md)
>* [Erstellen  [!DNL Google Ads]  Konversionswertregel](create-google-conversion-value-rule.md)
>* [Bearbeiten  [!DNL Google Ads]  Konversionswertregel](edit-google-conversion-value-rule.md)
>* [Ändern des Status  [!DNL Google Ads]  Konversionswertregel](change-the-status-of-google-conversion-value-rule.md)

