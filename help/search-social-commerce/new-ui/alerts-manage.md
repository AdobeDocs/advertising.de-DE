---
title: (Neue Benutzeroberfläche) Verwalten benutzerdefinierter Warnhinweise
description: Erfahren Sie, wie Sie benutzerdefinierte Warnhinweise und Warnhinweisvorlagen erstellen, konfigurieren, anhalten, aktivieren, löschen, anzeigen und exportieren.
feature: Search Alerts
source-git-commit: 0fddeb8f01bd7c310544973ae2aff78339eb2144
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Verwalten benutzerdefinierter Warnhinweise

Erstellen Sie Warnhinweisvorlagen, um zu ermitteln, wann ein Portfolio, eine Kampagne oder eine Anzeigengruppe während eines bestimmten Zeitraums bestimmte Bedingungen erfüllt (z. B. eine Leistungsmetrik), und generieren Sie dann einen Warnhinweis. Warnhinweise sind für einen einzelnen Werbetreibenden verfügbar. Warnhinweise enthalten alle Spalten in der entsprechenden Standardansicht. Warnhinweise auf Kampagnenebene enthalten beispielsweise alle Spalten in der [!UICONTROL Campaigns].

Sie können Warnhinweisvorlagen entweder über die Registerkarte [!UICONTROL Alert Templates] im [!UICONTROL Custom Alerts] oder über eine beliebige Seite erstellen.

Wenn eine Warnhinweisinstanz für eine Warnhinweisvorlage ausgelöst wird:

* Die angegebenen Empfänger erhalten eine E-Mail-Benachrichtigung. Wenn der Warnhinweis bis zu 1.000 Datensätze enthält, enthält der E-Mail-Hinweis eine [CSV](/help/search-social-commerce/glossary.md#c-d)-Datei mit den Warnhinweisdaten, einschließlich der Daten für alle Entitäten, die den Warnhinweis ausgelöst haben.

* Der Warnhinweis wird auf der Registerkarte [!UICONTROL Triggered Alerts] im [!UICONTROL Custom Alert Templates] angezeigt.<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## Die [!UICONTROL Custom Alerts]

Um den [!UICONTROL Custom Alerts] zu öffnen, klicken Sie ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis") oben rechts.

Das [!UICONTROL Custom Alerts] enthält die [!UICONTROL Alert Templates], in der alle für das Konto erstellten Warnhinweisvorlagen aufgelistet sind, aus denen Sie Warnhinweisvorlagen erstellen, bearbeiten, anhalten, reaktivieren und löschen können. In der [!UICONTROL Triggered Alerts] Ansicht werden die generierten Warnhinweisinstanzen aufgelistet.

## Verfügbare Aktionen

* [Ausgelöste Warnhinweise anzeigen](#alert-view)

* [Benutzerdefinierte Warnhinweisvorlagen anzeigen](#alert-template-view)

* [Erstellen einer benutzerdefinierten Warnhinweisvorlage](#alert-template-create)

* [Bearbeiten einer benutzerdefinierten Warnhinweisvorlage](#alert-template-edit)

* [Anhalten einer benutzerdefinierten Warnmeldungsvorlage](#alert-template-pause)

* [Aktivieren einer benutzerdefinierten Warnhinweisvorlage](#alert-template-activate)

* [Löschen einer benutzerdefinierten Warnhinweisvorlage](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## Ausgelöste Warnhinweise anzeigen {#alert-view}

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis").

1. Klicken Sie auf die Registerkarte **[!UICONTROL Triggered Alerts]** .

1. (Optional) Filtern Sie die Liste, um Warnhinweise für einen bestimmten Entitätstyp einzuschließen, oder suchen Sie im Vorlagennamen nach einer Textzeichenfolge. Bei Suchabfragen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

## Benutzerdefinierte Warnhinweisvorlagen anzeigen {#alert-template-view}

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis"), um die Registerkarte [!UICONTROL Alert Templates] zu öffnen.

1. (Optional) Filtern Sie die Liste, um Warnhinweise für einen bestimmten Entitätstyp einzuschließen, oder suchen Sie im Vorlagennamen nach einer Textzeichenfolge. Bei Suchabfragen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

1. (Optional) Um alle Kriterien für eine Warnhinweisvorlage anzuzeigen, klicken Sie auf die Anzahl der Kriterien (z. B. ![Schaltfläche für benutzerdefinierte Warnhinweiskriterien &#x200B;](/help/search-social-commerce/assets/custom-alert-criteria.png "Beispiel für benutzerdefinierte Warnhinweiskriterien").

## Erstellen einer benutzerdefinierten Warnhinweisvorlage {#alert-template-create}

Neue Warnhinweisvorlagen haben den Status &quot;[!UICONTROL Active]&quot;.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis") > **[!UICONTROL Create Custom Alert]**.

   Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis") > **[!UICONTROL View Custom Alerts]**. Daraufhin wird die Registerkarte [!UICONTROL Alert Templates] geöffnet. Klicken Sie auf **[!UICONTROL Create Alert]**.

1. Geben Sie [Warnhinweiseinstellungen](#alert-template-settings) auf den Registerkarten **[!UICONTROL Entity]**, **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** und **[!UICONTROL Scheduling and Delivery]** an.

   Sie können zwischen Registerkarten wechseln, indem Sie auf den Registerkartennamen (z. B. „Filter„) oder auf **[!UICONTROL Next]** unten rechts klicken.

1. Klicken Sie auf der Registerkarte [!UICONTROL Summary] auf **[!UICONTROL Create Alert]**.

## Bearbeiten einer benutzerdefinierten Warnhinweisvorlage {#alert-template-edit}

1. Klicken Sie oben rechts auf ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis") > **[!UICONTROL View Custom Alerts]**, wodurch die Registerkarte [!UICONTROL Alert Templates] geöffnet wird.

1. (Optional) Filtern Sie die Liste, um Warnhinweise für einen bestimmten Entitätstyp einzuschließen, oder suchen Sie im Vorlagennamen nach einer Textzeichenfolge. Bei Suchabfragen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

1. Klicken Sie neben dem Vorlagennamen auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten").

1. Bearbeiten Sie im [!UICONTROL Edit Custom Alert] die [Warnhinweiseinstellungen](#alert-template-settings) auf den Registerkarten **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** und **[!UICONTROL Scheduling and Delivery]**.

   Sie können zwischen Registerkarten wechseln, indem Sie auf den Registerkartennamen (z. B. „Filter„) oder auf **[!UICONTROL Next]** unten rechts klicken.

1. Klicken Sie auf der Registerkarte [!UICONTROL Summary] auf **[!UICONTROL Update Alert]**.

## Anhalten einer benutzerdefinierten Warnmeldungsvorlage {#alert-template-pause}

1. Klicken Sie oben rechts auf ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis") > **[!UICONTROL View Custom Alerts]**, wodurch die Registerkarte [!UICONTROL Alert Templates] geöffnet wird.

1. (Optional) Filtern Sie die Liste, um Warnhinweise für einen bestimmten Entitätstyp einzuschließen, oder suchen Sie im Vorlagennamen nach einer Textzeichenfolge. Bei Suchabfragen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

1. Wählen Sie in der Vorlagenzeile *[!UICONTROL Paused]* aus.

## Aktivieren einer benutzerdefinierten Warnhinweisvorlage {#alert-template-activate}

1. Klicken Sie oben rechts auf ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis") > **[!UICONTROL View Custom Alerts]**, wodurch die Registerkarte [!UICONTROL Alert Templates] geöffnet wird.

1. (Optional) Filtern Sie die Liste, um Warnhinweise für einen bestimmten Entitätstyp einzuschließen, oder suchen Sie im Vorlagennamen nach einer Textzeichenfolge. Bei Suchabfragen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

1. Wählen Sie in der Vorlagenzeile *[!UICONTROL Active]* aus.

## Löschen einer benutzerdefinierten Warnhinweisvorlage {#alert-template-delete}

Sie können nur die von Ihnen erstellten Warnhinweisvorlagen löschen.

1. Klicken Sie oben rechts auf ![Benutzerdefinierter Warnhinweis](/help/search-social-commerce/assets/custom-alert.png "Benutzerdefinierter Warnhinweis") > **[!UICONTROL View Custom Alerts]**, wodurch die Registerkarte [!UICONTROL Alert Templates] geöffnet wird.

1. (Optional) Filtern Sie die Liste, um Warnhinweise für einen bestimmten Entitätstyp einzuschließen, oder suchen Sie im Vorlagennamen nach einer Textzeichenfolge. Bei Suchabfragen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

1. Klicken Sie in der Vorlagenzeile auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen").

1. Klicken Sie im Bestätigungsnachrichtenfeld auf **[!UICONTROL Delete]**.

## Einstellungen für benutzerdefinierte Warnhinweisvorlagen {#alert-template-settings}

| Tabulator | Parameter | Beschreibung |
|--- |--- |--- |
|  | [!UICONTROL Name] | Der Name des Warnhinweises. Sie muss mindestens fünf Zeichen enthalten. |
| [!UICONTROL Date Range] | [!UICONTROL Select Entity] | Der zu bewertende Entitätstyp: <i>[!UICONTROL Portfolio]</i>, <i>[!UICONTROL Campaign]</i> oder <i>[!UICONTROL Ad Group]</i>. |
| [!UICONTROL Date Range] | [!UICONTROL Period] | Der Datumsbereich, für den die Bedingungen für den Warnhinweis ausgewertet werden sollen. Metriken werden aggregiert über den gesamten Datumsbereich ausgewertet. Die Optionen reichen von *[!UICONTROL Yesterday]* bis *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] | \[Definierte Filter\] | Die Bedingungen für das Auslösen des Warnhinweises zu dem auf der Registerkarte [!UICONTROL Scheduling and Delivery] angegebenen Zeitpunkt. Die verfügbaren Spalten variieren je nach Entitätstyp. Alle Filter werden mit der booleschen Funktion UND verbunden, was bedeutet, dass alle angegebenen Bedingungen erfüllt sein müssen.<ul><li><p>Gehen Sie wie folgt vor, um einen Filter hinzuzufügen:<p><ol><li><p>(Optional) Um die Spaltennamen nach Textzeichenfolgen zu filtern, geben Sie die Suchzeichenfolge in das [!UICONTROL ADD FILTER] Eingabefeld ein.</p></li><li><p>Wählen Sie in der Spaltenliste einen Spaltennamen aus.</p></li><li><p>Definieren Sie den Filter für die Spalte :</p></li><ul><li><p>(Filter ohne Eingabefelder) Klicken Sie ![Nach unten](/help/search-social-commerce/assets/arrow-down-expand.png "Nach unten") neben dem zweiten Menü und aktivieren Sie dann die Kontrollkästchen neben den einzelnen einzuschließenden Werten.</p></li><li><p>(Alle anderen Filter mit Eingabefeldern) Wählen Sie im zweiten Menü einen Operator aus, und geben Sie dann den entsprechenden Wert ein.</p><p>Wenn Sie beispielsweise die Spalte „Klicks“ ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie „Mehr als“ aus und geben Sie im Eingabefeld 100 ein.</p><p>Je nach Datentyp können die verfügbaren Operatoren Folgendes umfassen <i>größer als</i>, <i>kleiner als</i>, <i>gleich</i>, <i>enthält</i>, <i>beginnt nicht mit</i>, <i>endet mit</i>, <i>kein Wert</i>, <i>hat einen Wert</i>, <i>vorher</i> <i> </i> <i> </i>, oderkein Datum</i> <i>.</p><p>**Hinweis** Bei Textwerten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie beispielsweise nach Kampagnen filtern, bei denen im Namen „Darlehen“ enthalten ist, können die Ergebnisse „Verbraucherkredite“ und „Kreditanträge“ enthalten.</p></li></ol><li><p>Um einen Filter zu entfernen, klicken Sie ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen") neben der Filterdefinition.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[Wenn\] | Wie oft der Warnhinweis auf die angegebenen Bedingungsfilter prüft und, wenn alle Bedingungen erfüllt sind, E-Mail-Benachrichtigungen sendet:<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*Wochentag*> um &lt;*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*Tag NN*> um &lt;*NN*> `[AM\|PM]`]</p></li></ul>**Hinweis:** Dieser Wert hat keinen Einfluss auf den Auswertungszeitraum. |
|  | [!UICONTROL Email Recipients] | (Nur vom Ersteller der Warnhinweisvorlage bearbeitbar; für alle anderen schreibgeschützt) Benutzer von Registered Search, Social und Commerce, an die Benachrichtigungen gesendet werden sollen, wenn ein Warnhinweis ausgelöst wird. Standardmäßig ist der Name Ihres Benutzerkontos ausgewählt. Optional können Sie Benutzer mit Zugriff auf die Daten des Werbetreibenden hinzufügen oder entfernen.<br><br>Wenn der Warnhinweis bis zu 1.000 Datensätze enthält, wird eine CSV-Version des Warnhinweises an die E-Mail-Nachricht angehängt. |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
