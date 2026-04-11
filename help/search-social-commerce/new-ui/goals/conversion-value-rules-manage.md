---
title: (Neue Benutzeroberfläche) Regeln  [!DNL Google Ads]  Konversionswerte verwalten
description: Erfahren Sie, wie Sie Konversionswertregeln  [!DNL Google Ads]  Search, Social und Commerce anzeigen und verwalten können.
source-git-commit: ef9ed1031152857719e1691e50a57628d51505de
workflow-type: tm+mt
source-wordcount: '1831'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Verwalten [!DNL Google Ads] Konversionswertregeln

*Beta-Funktion*

[!DNL Google Ads] [Konversionswertregeln](https://support.google.com/google-ads/answer/10518330) können Sie die Werte von Konversionsereignissen basierend auf Benutzerinformationen anpassen, einschließlich des Gerätetyps, des Standorts und des Zielgruppensegments. Sie können Regeln für wertbasierte Gebote in Kampagnen mit Suche, Anzeige, Shopping und Performance Max mit Google Smart Bidding verwenden. Bei Kampagnen mit den Gebotsstrategien Maximieren von Konversionen und Ziel-ROAS bevorzugen [!DNL Google Ads] Algorithmen ab sofort Konversionen mit einem höheren Wert.

Konversionswertregeln auf Kampagnenebene setzen Regeln auf Kontoebene außer Kraft. Wenn eine Konversion mehrere Konversionswertregeln erfüllt, wird nur eine der Regeln angewendet. Normalerweise wird die spezifischste Regel angewendet. Weitere Informationen finden Sie jedoch in der [[!DNL Google Ads] Dokumentation zu Prioritäten für die verschiedenen Regelbedingungstypen](https://support.google.com/google-ads/answer/10520348).

## Die [!UICONTROL Conversion Value Rules] Ansicht und Funktionalität

Search, Social und Commerce synchronisieren die Konversionswertregeln automatisch mit Ihren [!DNL Google Ads]. Alle in der [!DNL Google Ads] erstellten Regeln werden innerhalb von 24 Stunden synchronisiert und sind in der Ansicht [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules] verfügbar.

Einige Konten können ihre Konversionswertregeln verwalten:

* In Konten, für die Konversionen auf individueller Konto- oder Kampagnenebene verfolgt werden, können Sie [Erstellen](#google-conversion-value-rule-create), [Bearbeiten](#google-conversion-value-rule-edit) und [Status &#x200B;](#google-conversion-value-rule-change-status) Regeln auf Konto- und Kampagnenebene ändern.

  Die Konten können zwar mit [!DNL Google Ads] Manager-Konten verknüpft werden, sie können jedoch kein kontenübergreifendes Konversions-Tracking verwenden (bei dem Konversionen über alle Konten im Manager-Konto hinweg verfolgt werden).

* In Konten, die das kontenübergreifende Konversionstracking verwenden, werden die Regeln auf Konto- und Kampagnenebene vom Manager-Konto übernommen und sind schreibgeschützt.

## Konversionswertregeln mit den Portfolios Suche, Social und Commerce

Wenn das Advertiser-Konto so konfiguriert ist, dass Search-, Social- und Commerce-Ziele in [!DNL Google Ads] hochgeladen werden, und Sie eine Kampagne einbeziehen, die eine Konversionswertregel in ein Portfolio mit einem Ziel verwendet, wendet [!DNL Google Ads] die Konversionswertregel auf den im Ziel angegebenen ursprünglichen Konversionswert an. Infolgedessen unterscheiden sich Konversionsdaten in Search, Social und Commerce von den Konversionsdaten in [!DNL Google Ads].

Angenommen, das Ziel verwendet eine einzige Konversionsmetrik „Leads“ und gibt Konversionen von Mobilgeräten das Gewicht 10 und Konversionen von Nicht-Mobilgeräten das Gewicht 10 an. Search, Social und Commerce zählen ein Ereignis aus einem der Gerätetypen als Konversion 1 (1) und schreiben den Konversionswert als 10 zu. Angenommen, eine Kampagne in diesem Portfolio verwendet eine Konversionswertregel: „Wenn das Gerät ein Mobilgerät ist, multiplizieren Sie sie mit 2.“ Wenn ein mobiles Leads-Ereignis für diese Kampagne verfolgt wird, schreibt [!DNL Google Ads] die Konversionszählung auch als eins (1), aber den Konversionswert als (10 x 2) = 20 zu.

Weitere Informationen zu Ihren Regeln, einschließlich der ursprünglichen Konversionswerte vor der Anwendung der Regeln, finden Sie [&#x200B; Bericht zu Konversionswertregeln in  [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

## Erstellen einer [!DNL Google Ads] Konversionswertregel {#google-conversion-value-rule-create}

Sie können Konversionswertregeln auf Konto- und Kampagnenebene in [!DNL Google Ads] Konten erstellen, für die Konversionen auf individueller Kontoebene oder darunter verfolgt werden. Sie können keine Regeln für Konten mit kontoübergreifenden Konversionen erstellen, die auf Master-Kontoebene verfolgt werden.

Jede Regel umfasst bis zu zwei Bedingungen sowie die Konversionswertanpassung, die angewendet werden soll, wenn die Bedingungen erfüllt sind. Alle Regeln in einem Konto müssen denselben Typ von primären und (optionalen) sekundären Bedingungen verwenden. Wenn beispielsweise Regel 1 die primäre Bedingung „Zielgruppe“ und die sekundäre Bedingung „Standort“ enthält, müssen alle anderen Regeln im Konto die primäre Bedingung „Zielgruppe“ aufweisen. Wenn die anderen Regeln eine sekundäre Bedingung enthalten, muss sie „Standort“ lauten.

Für jede Kampagne können mehrere Regeln auf Kampagnenebene erstellt werden. [!DNL Google Ads] bietet jedoch noch nicht die Möglichkeit, neue Regeln auf Kontoebene außerhalb des [!DNL Google Ads]-Editors zu erstellen, wenn bereits eine Regel auf Kontoebene vorhanden ist. Um zusätzliche Regeln auf Kontoebene zu erstellen, melden Sie sich direkt bei [!DNL Google Ads] an und verwenden Sie den [!DNL Google Ads].

**Hinweis** Konversionswertregeln auf Kampagnenebene überschreiben die Regeln auf Kontoebene, und auf eine Konversion kann nur eine Regel angewendet werden. Weitere Informationen finden Sie unter [wie [!DNL Google Ads] bestimmt, welche Regel auf eine Konversion angewendet wird, wenn die Konversion die Bedingungen für mehrere Regeln erfüllt](https://support.google.com/google-ads/answer/10520348).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Standardmäßig ist die Registerkarte **[!UICONTROL Campaign]** ausgewählt, um alle Regeln auf Kampagnenebene anzuzeigen.

1. (Optional) Um stattdessen eine Regel auf Kontoebene zu erstellen, klicken Sie auf die Registerkarte **[!UICONTROL Account]** .

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Create Campaign Rule]** (auf der Registerkarte [!UICONTROL Campaign]) oder **[!UICONTROL Create Account Rule]** (auf der Registerkarte [!UICONTROL Account]).

1. Wählen Sie das Werbenetzwerk und das Konto aus. Wählen Sie für Regeln auf Kampagnenebene auch die Kampagne aus. Klicken Sie dann auf **[!UICONTROL Next]**.

1. Konfigurieren Sie [Einstellungen für Konversionsregeln](#google-ads-conversion-value-rule-settings).

   Sie müssen eine primäre Bedingung und eine Wertanpassung konfigurieren. Sie können optional eine sekundäre Bedingung konfigurieren.

   Innerhalb einer Bedingung werden mehrere Ziele oder Ausschlüsse mit dem booleschen Operator ODER verbunden, sodass jede Option zum Initiieren einer Wertanpassung erfüllt sein kann. Wenn Sie eine sekundäre Bedingung einbeziehen, wird die sekundäre Bedingung mit dem booleschen Operator ALL mit der primären Bedingung verbunden, sodass beide Bedingungen erfüllt sein müssen, um eine Wertanpassung zu initiieren. Beispiel: Wenn \[Standort Algerien ODER Tunesien\] UND \[Gerät ist Mobil ODER Tablet\] ist, fügen Sie 1.5 hinzu.

   **Hinweis:** Alle Regeln in einem Konto müssen denselben Typ von primären und (optionalen) sekundären Bedingungen verwenden. Wenn beispielsweise Regel 1 die primäre Bedingung „Zielgruppe“ und die sekundäre Bedingung „Standort“ enthält, müssen alle anderen Regeln im Konto die primäre Bedingung „Zielgruppe“ aufweisen. Wenn die anderen Regeln eine sekundäre Bedingung enthalten, muss sie „Standort“ lauten.

1. Klicken Sie auf **[!UICONTROL Review and Save]** , um die Einstellungen zu überprüfen.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Bearbeiten einer [!DNL Google Ads] Konversionswertregel {#google-conversion-value-rule-edit}

Sie können eine Konversionswertregel in Konten/Kampagnen bearbeiten, für die Konversionen auf individueller Kontoebene oder darunter verfolgt werden. Sie können keine Regel für ein Konto mit kontoübergreifenden Konversionen bearbeiten, die auf Master-Kontoebene verfolgt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Standardmäßig ist die Registerkarte **[!UICONTROL Campaign]** ausgewählt, um alle Regeln auf Kampagnenebene anzuzeigen.

1. (Optional) Um stattdessen alle Regeln auf Kontoebene anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Account]** .

1. Aktivieren Sie das Kontrollkästchen neben der Regel.

1. In der Symbolleiste für Massenaktionen

   * Um pausierte Regeln zu aktivieren, klicken Sie auf (/help/search-social-commerce/assets/edit-new.png „Bearbeiten).

1. Bearbeiten Sie die [Einstellungen für Konversionsregeln](#google-ads-conversion-value-rule-settings).

   Die Bedingungstypen für eine vorhandene Regel können nicht bearbeitet werden, die Bedingungen und Wertanpassungen können jedoch bearbeitet werden.

   Sie müssen eine primäre Bedingung und eine Wertanpassung konfigurieren. Sie können optional eine sekundäre Bedingung konfigurieren.

   **Hinweis:** Wenn Sie eine sekundäre Bedingung hinzufügen, muss sie vom gleichen Bedingungstyp sein wie andere Regeln im Konto. Wenn beispielsweise Regel 1 oder andere Regeln im Konto die sekundäre Bedingung „Standort“ aufweisen, muss, wenn die anderen Regeln eine sekundäre Bedingung enthalten, die sekundäre Bedingung „Standort“ sein. Wenn Sie eine sekundäre Bedingung einbeziehen, wird die sekundäre Bedingung mit dem booleschen Operator ALL mit der primären Bedingung verbunden, sodass beide Bedingungen erfüllt sein müssen, um eine Wertanpassung zu initiieren.

1. Klicken Sie auf **[!UICONTROL Review and Save]** , um die Einstellungen zu überprüfen.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Ändern des Status einer [!DNL Google Ads] Konversionswertregel {#google-conversion-value-rule-change-status}

Sie können eine Konversionswertregel in Konten und Kampagnen, für die Konversionen auf individueller Kontoebene verfolgt werden, anhalten, aktivieren oder löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Standardmäßig ist die Registerkarte **[!UICONTROL Campaign]** ausgewählt, um alle Regeln auf Kampagnenebene anzuzeigen.

1. (Optional) Um stattdessen alle Regeln auf Kontoebene anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Account]** .

1. Aktivieren Sie das Kontrollkästchen neben jeder zu ändernden Zeile.

1. In der Symbolleiste für Massenaktionen

   * Um pausierte Regeln zu aktivieren, klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Activate]**.

   * Um aktive Regeln anzuhalten, klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Pause]**.

   * Um aktive oder angehaltene Regeln zu löschen, klicken Sie auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Regeleinstellungen für Konversionswert [!DNL Google Ads] {#google-conversion-value-rule-settings}

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
>* &#x200B;

