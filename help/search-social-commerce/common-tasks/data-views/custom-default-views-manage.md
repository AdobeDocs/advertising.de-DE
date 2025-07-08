---
title: Verwalten von standardmäßigen und benutzerdefinierten Ansichten
description: Erfahren Sie, wie Sie Ihre Standardansichten und benutzerdefinierten Ansichten anpassen.
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 399974645b5083e735ff7aa94eba0a1115b4ddeb
workflow-type: tm+mt
source-wordcount: '4453'
ht-degree: 0%

---

# Verwalten von standardmäßigen und benutzerdefinierten Ansichten

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

Mit den Standardansichten und benutzerdefinierten Ansichten können Sie die Leistungsdaten anpassen, die in den Datenansichten für die Suchkampagne angezeigt werden. Die Anzeigeeinstellungen umfassen die einzuschließenden Spalten, Filter, Datumsbereich, Konversions-Attributionseinstellungen und andere erweiterte Einstellungen. Sie können die Einstellungen entweder vorübergehend anwenden oder speichern. (Ausnahme: Filter für Standardansichten können nicht gespeichert werden.) Jede standardmäßige und standardmäßige benutzerdefinierte Ansicht gilt für eine bestimmte Ansicht (z. B. [!UICONTROL Portfolios] oder [!UICONTROL Campaigns]) und nur für ein bestimmtes Advertiser-Konto. In der veralteten Benutzeroberfläche ist jede universelle benutzerdefinierte Ansicht für alle Entitätsansichten für einen bestimmten Advertiser anwendbar und kann daher keine Eigenschaftsspalten (wie Entitätsname oder -status) enthalten, die je nach Entitätstyp variieren.

Standardansichten werden standardmäßig bei jeder Anmeldung angezeigt. Sie können zusätzliche benutzerdefinierte Ansichten erstellen und sie jederzeit anwenden. Optional können Sie jede benutzerdefinierte Ansicht, die Sie erstellen, für alle anderen Benutzer freigeben, die die Daten des Werbetreibenden anzeigen können. Nur die Person, die eine benutzerdefinierte Ansicht erstellt, kann sie löschen.

In der Legacy-Benutzeroberfläche ist jede Ansicht als Verknüpfung im Abschnitt [!UICONTROL Custom Views] des linken Bedienfelds verfügbar.

## Standardansicht oder benutzerdefinierte Ansicht anwenden

### (Neue Benutzeroberfläche) Standardansicht oder benutzerdefinierte Ansicht auf eine Verwaltungsansicht anwenden

1. Klicken Sie über der Datentabelle auf den Namen der aktuell angewendeten Ansicht (![Ansicht](/help/search-social-commerce/assets/view.png "Ansicht")).

1. Klicken Sie nach Bedarf auf eine der Registerkarten ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] und [!UICONTROL From Others]), um die Ansicht zu suchen.

1. Halten Sie den Cursor über den Namen der Ansicht und klicken Sie auf **[!UICONTROL Apply]**.

### (Alte Benutzeroberfläche) Standardansicht oder benutzerdefinierte Ansicht auf Kampagnen-Management-Ansicht anwenden

* (Standardansichten) Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]** \> **\[Entitätstyp\]**.

* (Benutzerdefinierte Ansichten) Über das linke Navigationsfenster:

   1. Klicken Sie im linken Bedienfeld auf das **[!UICONTROL Custom Views]**, um es zu erweitern.

      Die Ansichten werden nach der entsprechenden Entität sortiert.

   1. Erweitern Sie die verfügbaren Menüs.

      &quot;[!UICONTROL Universal Views]&quot; umfasst benutzerdefinierte Ansichten, die in allen Entitätsansichten verwendet werden können. Alle anderen benutzerdefinierten Ansichten sind nach Entitätstyp gruppiert.

   1. Klicken Sie auf den Namen der Ansicht.

      Wenn die Ansicht universell ist oder für die aktuelle Entität gilt, wird die Datentabelle gemäß der Ansichtskonfiguration erneut angezeigt. Wenn die Ansicht für eine andere Entität gilt, werden Daten für die entsprechende Entität gemäß der Ansichtskonfiguration angezeigt.

## Erstellen einer benutzerdefinierten Ansicht {#create-custom-view}

>[!NOTE]
>
>Zusätzlich zu den Anzeigeeinstellungen, die Sie für die benutzerdefinierte Ansicht festlegen, wird auch die aktuelle Spaltensortierreihenfolge gespeichert.

### (Neue Benutzeroberfläche) Erstellen einer benutzerdefinierten Ansicht aus einer Verwaltungsansicht

*Verfügbar in den Ansichten [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] und [!UICONTROL Ad Groups]*

Benutzerdefinierte Ansichten sind spezifisch für eine einzelne Ansicht (z. B. die [!UICONTROL Portfolios]).

1. Klicken Sie über der Datentabelle auf den Namen der aktuell angewendeten Ansicht (![Ansicht](/help/search-social-commerce/assets/view.png "Ansicht")).

1. Klicken Sie auf **[!UICONTROL Create View]**.

1. Geben Sie die [Einstellungen für benutzerdefinierte Ansicht](#view-settings-new-ui) an.

1. Ansicht speichern:

   * Um die Ansicht zu speichern und anzuwenden, klicken Sie auf **[!UICONTROL Save & Apply]**.

   * Um die Ansicht zu speichern, ohne sie anzuwenden, klicken Sie auf **[!UICONTROL Save]**.

### (Alte Benutzeroberfläche) Erstellen einer benutzerdefinierten Ansicht aus einer Kampagnen-Management-Ansicht

Benutzerdefinierte Ansichten gelten nur für die Ansichten des Kampagnen-Managements.

1. Klicken Sie rechts in der Symbolleiste oberhalb der Datentabelle auf den Namen der aktuellen Ansicht (der möglicherweise &quot;[!UICONTROL Default]&quot; lautet).

1. Geben Sie die [Einstellungen für benutzerdefinierte Ansicht](#view-settings) an.

1. Klicken Sie auf **[!UICONTROL Save as New]**.

1. Geben Sie den Namen der neuen Ansicht ein, und klicken Sie dann auf **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Verwenden Sie einen Namen, der Ihnen hilft, die Registerkarte und die Informationen zu identifizieren, für die sie gilt (z. B. „Ausgesetzte Kampagnen“ oder „Top 50-Anzeigen„).

## Standardansicht oder benutzerdefinierte Ansicht bearbeiten {#view-edit}

### (Neue Benutzeroberfläche) Standardansicht oder benutzerdefinierte Ansicht bearbeiten

*Verfügbar in den Ansichten [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] und [!UICONTROL Ad Groups]*

1. Klicken Sie über der Datentabelle auf den Namen der aktuell angewendeten Ansicht (![Ansicht](/help/search-social-commerce/assets/view.png "Ansicht")).

1. Klicken Sie nach Bedarf auf eine der Registerkarten ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] und [!UICONTROL From Others]), um die Ansicht zu suchen.

1. Halten Sie den Cursor über den Namen der Ansicht und klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png).

1. Bearbeiten Sie die [Einstellungen für benutzerdefinierte Ansichten](#view-settings-new-ui).

1. Ansicht speichern:

   * Um die Änderungen zu speichern, ohne sie anzuwenden, klicken Sie auf **[!UICONTROL Save]**.

   * Um die Änderungen zu speichern und anzuwenden, klicken Sie auf **[!UICONTROL Apply]**.<!-- Should be Save & Apply -->

### (Alte Benutzeroberfläche) Standardansicht oder benutzerdefinierte Ansicht bearbeiten

1. Öffnen Sie die Anzeigeeinstellungen:

   * (Wenn Sie die Ansicht bereits angewendet haben) Klicken Sie rechts in der Symbolleiste über der Datentabelle auf den Namen der aktuellen Ansicht (der möglicherweise &quot;[!UICONTROL Default]&quot; lautet).

   * (Benutzerdefinierte Ansichten, die nicht angewendet werden) Klicken Sie im linken Bereich auf ![Benutzerdefinierte Ansichten](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Benutzerdefinierte Ansichten"), um das [!UICONTROL Custom Views] zu erweitern. Klicken Sie auf den Namen der benutzerdefinierten Ansicht.

1. Bearbeiten Sie die [Ansichtseinstellungen](#view-settings).

   >[!NOTE]
   >
   >Sie können Änderungen an Filtern auf Ihre Standardansichtseinstellungen anwenden, aber nicht speichern.

1. Anwenden oder Speichern der Einstellungen:

   * Um die Einstellungen vorübergehend anzuwenden, ohne sie in der Ansicht zu speichern, klicken Sie auf **[!UICONTROL Apply]**.

     Die Einstellungen werden auf die Registerkarte angewendet, bis Sie von der Verwaltungsansicht der obersten Ebene wegnavigieren oder (falls zutreffend) [Daten für einen anderen Advertiser anzeigen](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (Für die von Ihnen erstellten Standardansichten und benutzerdefinierten Ansichten) Klicken Sie auf **[!UICONTROL Save]**, um die Einstellungen in der aktuellen Ansicht zu speichern.

   * Um die Einstellungen in einer neuen benutzerdefinierten Ansicht zu speichern, klicken Sie auf **[!UICONTROL Save As]**. Geben Sie im [!UICONTROL Enter New Custom View Name] den Namen der neuen Ansicht ein, und klicken Sie dann auf **[!UICONTROL Save]**.

## (Neue Benutzeroberfläche) Klonen einer standardmäßigen oder benutzerdefinierten Ansicht {#view-clone}

*Verfügbar in den Ansichten [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] und [!UICONTROL Ad Groups]*

1. Klicken Sie über der Datentabelle auf den Namen der aktuell angewendeten Ansicht (![Ansicht](/help/search-social-commerce/assets/view.png "Ansicht")).

1. Klicken Sie nach Bedarf auf eine der Registerkarten ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] und [!UICONTROL From Others]), um die Ansicht zu suchen.

1. Halten Sie den Cursor über den Namen der Ansicht und klicken Sie auf ![Klonen](/help/search-social-commerce/assets/clone-new.png).

1. Geben Sie einen neuen Ansichtsnamen ein und bearbeiten Sie die [benutzerdefinierten Ansichtseinstellungen](#view-settings-new-ui) nach Bedarf.

1. Ansicht speichern:

   * Um die Ansicht zu speichern und anzuwenden, klicken Sie auf **[!UICONTROL Save & Apply]**.

   * Um die Ansicht zu speichern, ohne sie anzuwenden, klicken Sie auf **[!UICONTROL Save]**.

## Standardansicht auf die Systemstandardeinstellungen zurücksetzen

Wenn Sie die Standardansichtseinstellungen wiederherstellen, werden alle gespeicherten Einstellungen entfernt und die Standardeinstellungen des Systems werden erneut angewendet.

Die Standardeinstellungen des Systems variieren je nach Verwaltungsansicht. Für die meisten Verwaltungsansichten zeigt die Systemstandardansicht Daten des Vortages für Elemente in aktivierten und aktiven Konten (z. B. nur aktive Anzeigengruppen in aktiven Kampagnen), wobei die Daten nach Kosten sortiert sind und die Konversionsdaten auf dem Transaktionsdatum basieren.

* Über die neue Benutzeroberfläche:

   1. Klicken Sie über der Datentabelle auf den Namen der aktuell angewendeten Ansicht (![Ansicht](/help/search-social-commerce/assets/view.png "Ansicht")).

   1. Klicken Sie nach Bedarf auf eine der Registerkarten ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] und [!UICONTROL From Others]), um die Ansicht zu suchen.

   1. Halten Sie den Cursor über den Namen der Ansicht und klicken Sie auf ![Wiederherstellen](/help/search-social-commerce/assets/revert-new.png).

* In den alten Ansichten für die Kampagnenverwaltung:

   1. Klicken Sie im linken Bedienfeld auf ![Benutzerdefinierte Ansichten](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Benutzerdefinierte "), um das [!UICONTROL Custom Views] zu erweitern.

      Die Ansichten werden nach der entsprechenden Entität sortiert.

   1. Klicken Sie neben dem Namen der Ansicht auf ![Auf Standardeinstellungen wiederherstellen](/help/search-social-commerce/assets/restore.png "Auf Standardeinstellungen wiederherstellen").

## Löschen einer benutzerdefinierten Ansicht

Sie können jede von Ihnen erstellte benutzerdefinierte Ansicht löschen.

Wenn Sie eine benutzerdefinierte Ansicht löschen, die auf die aktuelle Registerkarte angewendet wird, wird die benutzerdefinierte Ansicht auf der Registerkarte weiterhin angezeigt, bis Sie den Ansichtssatz verlassen (z. B. von Ansichten im Menü [!UICONTROL Search] zum Menü [!UICONTROL Reports] ) oder (falls zutreffend), bis Sie [Daten für einen anderen Advertiser anzeigen](/help/search-social-commerce/common-tasks/change-advertiser.md).

* Über die neue Benutzeroberfläche:

   1. Klicken Sie über der Datentabelle auf den Namen der aktuell angewendeten Ansicht (![Ansicht](/help/search-social-commerce/assets/view.png "Ansicht")).

   1. Klicken Sie nach Bedarf auf eine der Registerkarten ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] und [!UICONTROL From Others]), um die Ansicht zu suchen.

   1. Halten Sie den Cursor über den Namen der Ansicht und klicken Sie auf ![Löschen](/help/search-social-commerce/assets/delete-new.png).

   1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

* In den alten Ansichten für die Kampagnenverwaltung:

   1. Klicken Sie im linken Bedienfeld auf ![Benutzerdefinierte Ansichten](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Benutzerdefinierte "), um das [!UICONTROL Custom Views] zu erweitern.

   1. Halten Sie den Cursor über den Namen der benutzerdefinierten Ansicht, und klicken Sie dann auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

   1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Continue]**.

## Standardmäßige und benutzerdefinierte Anzeigeeinstellungen

<!-- Simplify attribution rule definitions here and elsewhere and include links to "How attribution rules are calculated -->

### (Neue Benutzeroberfläche) Einstellungen für die standardmäßige und benutzerdefinierte Ansicht {#view-settings-new-ui}

| **tab** | **Feld** | **Beschreibung** |
| --- | --- | --- |
| [Über allen Registerkarten] | -Name | Ein eindeutiger Name für die Ansicht. Der Name einer Standardansicht kann nicht bearbeitet werden.<p><b>Tipp:</b> Verwenden Sie einen Namen, der Ihnen hilft, die Registerkarte und die Informationen zu identifizieren, für die sie gilt (z. B. „Ausgesetzte Kampagnen“ oder „Top 50-Anzeigen„). |
|   | Für andere Benutzer freigeben | (Nur benutzerdefinierte Ansichten; optional) Stellt die Ansicht allen anderen Benutzern zur Verfügung, die die Daten des Werbetreibenden anzeigen können. Andere Benutzer können die Ansicht nicht bearbeiten oder löschen, aber sie können aus den Einstellungen eine neue Ansicht erstellen. |
| Spalten | Ausgewählte Spalten und Reihenfolge | Die Spalten der angezeigten Daten und ihre Reihenfolge:<ul><li> (So fügen Sie eine Spalte hinzu) Klicken Sie in der Liste Verfügbare Spalten auf einen Spaltennamen, und ziehen Sie ihn dann entweder in die Liste Ausgewählte Spalten und Sortierung oder klicken Sie auf ![Pfeil nach rechts](/help/search-social-commerce/assets/chevron-right.png), um ihn dorthin zu verschieben.</li><li>(So ändern Sie die horizontale Position einer Spalte) Klicken Sie in der Liste Ausgewählte Spalten und Reihenfolge auf den Spaltennamen, und ziehen Sie die Spalte dann entweder an die gewünschte Position, oder klicken Sie auf ![Nach-oben-](/help/search-social-commerce/assets/chevron-up.png) oder ![Nach-unten-](/help/search-social-commerce/assets/chevron-down.png), um sie dorthin zu verschieben. Der Name der oberen Spalte wird in der linken Spalte angezeigt.</li><li>(Um eine Spalte zu entfernen) Klicken Sie in der Liste Ausgewählte Spalten und Sortierung auf einen Spaltennamen, und ziehen Sie ihn dann entweder in die Liste Verfügbare Spalten oder klicken Sie auf ![Nach links](/help/search-social-commerce/assets/chevron-left.png), um ihn dorthin zu verschieben.</li></ul><b>Daten filtern</b><p>Um nur einen bestimmten Datentyp aufzulisten, klicken Sie auf eines der Symbole neben der Liste:<ul><li>![Eigenschaftensymbol](/help/search-social-commerce/assets/properties-icon-new.png) für Eigenschaftsnamen und IDs wie [!UICONTROL Portfolio Name] oder [!UICONTROL Status]</li><li>![Traffic-Symbol](/help/search-social-commerce/assets/traffic-metrics-icon-new.png) für standardmäßige Traffic-Metriken wie Impressionen und Klicks</li><li>![Umsatzsymbol](/help/search-social-commerce/assets/revenue-metrics-icon-new.png) (für Konversionsmetriken, die für den Advertiser verfolgt werden, einschließlich Konversions- und Site-Interaktionsmetriken, die mit Analytics synchronisiert wurden)</li><li>![Benutzerdefiniertes Symbol](/help/search-social-commerce/assets/custom-metrics-icon-new.png) (für benutzerdefinierte Metriken, die vom Advertiser erstellt wurden)</li><li>![Classification icon](/help/search-social-commerce/assets/classifications-icon-new.png) (für Label-Classifications).</li></ul> <b>Zusätzliche Hinweise:</b><ul><li>Informationen zum Hinzufügen, Erstellen oder Bearbeiten neuer Metriken finden Sie unter &quot;[Erstellen einer benutzerdefinierten Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md)&quot;, &quot;[Bearbeiten einer benutzerdefinierten Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md)&quot; und &quot;[Löschen einer benutzerdefinierten Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md)&quot;.</li><li>Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, werden keine Summen für geldbasierte Spalten (wie Kosten und CPC) berücksichtigt.</li><li>Sie können [das Spaltenset vorübergehend über das Spaltenüberschriftenmenü bearbeiten](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) und [das Spaltenset über das [!UICONTROL Columns] bearbeiten und sortieren](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Spaltensymbol](/help/search-social-commerce/assets/custom-columns.png "Spaltensymbol")).</li></ul> |
|   | Sortieren nach | Die Spalte, nach der die Daten sortiert werden sollen. Der Standardwert ist für jeden Berichtstyp unterschiedlich. |
|   | Sortierreihenfolge | Gibt an, ob die Daten in **aufsteigender** oder **absteigender** Reihenfolge sortiert werden sollen. |
| Filter | [Filterdefinitionen] | (Optional) Filter zum Anwenden auf Daten. Beim Anwenden von Filtern werden Zeilen nur dann zurückgegeben, wenn der Wert für eine Spalte die angegebenen Kriterien erfüllt.<p>Für jeden anzuwendenden Filter:<ol><li>Wählen Sie im Menü [!UICONTROL Add Filter] einen Spaltennamen aus. Die Liste enthält alle verfügbaren Spalten und ist nach Spaltentyp sortiert, wobei die Eigenschaftsspalten an erster Stelle stehen.</li><li>Filter für die Spalte definieren</li></ol>(Filter mit Eingabefeldern) Wählen Sie im zweiten Menü einen Operator und geben Sie dann den entsprechenden Wert ein. Bei Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.<p>Wenn Sie beispielsweise die Spalte „Klicks“ ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie _\>_ und geben Sie `100` in das Eingabefeld ein.<p>Je nach Datentyp können die verfügbaren Operatoren Folgendes umfassen: <i>größer als</i>, <i>kleiner als</i>, <i>gleich</i>, <i>enthält</i>, <i>enthält</i>, <i>beginnt mit</i>, <i>endet mit</i>,<i>kein Wert</i> oder <i>hat einen Wert</i> <i>before</i>, <i>after</i> oder <i>no date</i>.<p>(Filter ohne Eingabefelder) Klicken Sie ![Pfeil nach unten](/help/search-social-commerce/assets/arrow-down-expand.png) neben dem Menü Listenelemente auswählen und aktivieren Sie dann die Kontrollkästchen neben den einzelnen einzuschließenden Werten.<p><b>Hinweise:</b><ul><li>Sie können Änderungen an Filtern auf Ihre Standardansichtseinstellungen anwenden, aber nicht speichern.</li><li>Sie können auch [vorübergehend die entsprechenden Filter ändern](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) in der Ansicht ändern.</li></ul> |
| Zusätzliche Einstellungen | Datumsbereich | (Wenn „Datumsbereich einschließen“ ausgewählt ist)<p>Der Datumsbereich, für den Daten generiert werden sollen. Eine Option auswählen:<ul><li><i>[Vorgabenbereich]</i>: Eine Liste der allgemeinen Zeitinkremente, von &quot;<i>&quot; </i> &quot;<i> 180 Tage</i>. Wählen Sie eine aus der Liste aus. Der Standardwert lautet <i>Gestern</i>. Hinweis: <i>Letzter Monat</i>, <i>Letzte 3 Monate</i> und <i>Letzte 6 Monate</i> zeigen Daten für die vorherigen Kalendermonate an.</li><li><i>Benutzerdefinierter Datumsbereich: </i> Sie das Start- und Enddatum an. Geben Sie Daten im Format MM/TT/JJJJ oder M/TT/JJJJ ein oder klicken Sie ![Kalendersymbol](/help/search-social-commerce/assets/calendar.png) neben einem Feld und wählen Sie ein Datum aus.</li></ul> |
|   | Vergleich | Vergleicht Daten für den angegebenen Datumsbereich mit Daten für einen zweiten Datumsbereich. Wenn Sie diese Option auswählen, geben Sie den zweiten Datumsbereich an. Für jede reguläre Datenspalte werden zwei zusätzliche Spalten hinzugefügt. Anstatt beispielsweise nur eine Spalte für „Impressionen“ einzubeziehen, enthält der Bericht Spalten für „Impressionen - Bereich 1“, „Impressionen - Bereich 2“ und „Impressionsdifferenz“.<p><b>Hinweise:</b><ul><li>Die Spalte „Differenz“ wird für abgeleitete Metriken nicht angezeigt.</li><li>Bei Berichten, die große Datumsbereiche vergleichen, kann die Generierung länger dauern.</li></ul> |
|   | Vergleichsformat | (Wenn [!UICONTROL Comparison] aktiviert ist) So drücken Sie den Unterschied zwischen den Daten in den beiden ausgewählten Datumsbereichen in der Spalte &quot;[_Datenfeld_] Differenz“ aus. Eine Option auswählen:<ul><li><i>Varianz</i> (Standard): Zeigt die Differenz als numerischen Wert an.</li><li><i>% Änderung</i>: Zeigt die Differenz als Prozentsatz an.</li></ul> |
|   | Attributionsregel | (Nur Werbetreibende mit dem pixelbasierten Konversions-Tracking-Service von Adobe Advertising) Auf der Registerkarte wird erläutert, wie Konversionsdaten - möglicherweise über mehrere Anzeigenkanäle und Portfolios hinweg - in einer Ereignisreihe zugeordnet werden, die zu einer Konversion führt. Standardmäßig ist die in den Attributionseinstellungen für die Konversion auf Advertiser-Ebene angegebene Regel ausgewählt.<ul><li> <i>Erstes Ereignis</i>: Ordnet die Konversion dem ersten bezahlten Klick in der Reihe innerhalb des Klick-Lookback-Fensters des Werbetreibenden oder, falls keine bezahlten Klicks aufgetreten sind, der letzten Impression innerhalb des Impression-Lookback-Fensters des Werbetreibenden zu.</li><li><i>Gewicht des ersten Ereignisses Mehr</i>: Attributiert die Konversion auf alle Ereignisse in der Reihe, die innerhalb des Klick-Lookback-Fensters und Impression-Lookback-Fensters des Advertisers aufgetreten sind, gewichtet jedoch das erste Ereignis am meisten und die folgenden Ereignisse nacheinander weniger. Wenn der Konversion sowohl bezahlte Klicks als auch Impressions vorausgehen, wird die angegebene Impression-Überschreibungsgewichtung weiter auf die Impressions angewendet. Wenn der Konversion nur Impressions vorausgehen, werden die Impressions nach dem Durchsichtsgewicht des Advertisers gewichtet, anstatt nach dem Gewicht der Impression-Überschreibungen.</li><li><i>Ereignisverteilung</i>: Attributiert die Konversion zu gleichen Teilen jedem Ereignis in der Reihe, das im Klick-Lookback-Fenster und im Impression-Lookback-Fenster des Werbetreibenden aufgetreten ist. Wenn der Konversion sowohl bezahlte Klicks als auch Impressions vorausgehen, wird die angegebene Impression-Überschreibungsgewichtung weiter auf die Impressions angewendet. Wenn der Konversion nur Impressions vorausgehen, werden die Impressions nach dem Durchsichtsgewicht des Advertisers gewichtet, anstatt nach dem Gewicht der Impression-Überschreibungen.</li><li><i>Letztes Ereignis gewichten Mehr</i>: Ordnet die Konversion allen Ereignissen in der Reihe zu, die im Klick-Lookback-Fenster und Impression-Lookback-Fenster des Werbetreibenden stattgefunden haben. Gibt jedoch dem letzten Ereignis das meiste Gewicht und den vorangehenden Ereignissen sukzessive weniger Gewicht. Wenn der Konversion sowohl bezahlte Klicks als auch Impressions vorausgehen, wird die angegebene Impression-Überschreibungsgewichtung weiter auf die Impressions angewendet. Wenn der Konversion nur Impressions vorausgehen, werden die Impressions nach dem Durchsichtsgewicht des Advertisers gewichtet, anstatt nach dem Gewicht der Impression-Überschreibungen.</li><li><i>Letztes Ereignis</i> (Standard): Ordnet die Konversion dem letzten bezahlten Klick in der Reihe innerhalb des Klick-Lookback-Fensters des Werbetreibenden oder, falls keine bezahlten Klicks aufgetreten sind, der letzten Impression innerhalb des Impression-Lookback-Fensters des Werbetreibenden zu.</li><li><i>U-förmig</i>: Ordnet die Konversion allen Ereignissen in der Reihe zu, die im Klick-Lookback-Fenster des Werbetreibenden und im Impression-Lookback-Fenster stattgefunden haben. Gibt jedoch dem ersten und letzten Ereignis das größte Gewicht zu, wobei die Ereignisse in der Mitte des Konversionspfads sukzessive weniger Gewicht erhalten. Wenn der Konversion sowohl bezahlte Klicks als auch Impressions vorausgehen, wird die angegebene Impression-Überschreibungsgewichtung weiter auf die Impressions angewendet. Wenn der Konversion nur Impressions vorausgehen, werden die Impressions nach dem Durchsichtsgewicht des Advertisers gewichtet, anstatt nach dem Gewicht der Impression-Überschreibungen.</li></ul><p><b>Hinweise:</b><ul><li>Alle Attributionsregeln außer „Letztes Ereignis“ sind nur für Advertiser mit Adobe Advertising-Klick-Tracking und mit Konversions-Tracking von Adobe Advertising oder Adobe Analytics (mit Analytics-Integration) verfügbar.</li><li>Die Zuordnungsregeln gelten für Klicks auf bezahlte Anzeigen in jedem beliebigen Kanal. Sie gelten nicht für Impressionen für Paid Search-Anzeigen, die nicht auf Ereignisebene verfolgt werden können.</li><li>Wenn Sie Konversionsdaten mit einer beliebigen Attributionsregel außer einer der Regeln des „letzten Ereignisses“ melden, können die Ereignisse, die der Konversion vorangehen, über mehrere Portfolios hinweg auftreten. In diesem Fall enthält die Ansicht nur dann Daten für die Konversion, wenn die Anzeigen oder Keywords in diesen Portfolios in der Ansicht enthalten sind.</li><li>Für Standardansichten empfehlen wir, die standardmäßige Attributionsregel beizubehalten, mit der während der Angebotsoptimierung der [Zielwert](/help/search-social-commerce/glossary.md#o-p) (früher als „gewichteter Umsatz“ bezeichnet) für jede Gebotseinheit berechnet wird.</li></ul> |
|   | Konversionen basierend auf | So melden Sie Konversionsdaten:<ul><li><i>Klickdatum</i>: Zum Anzeigen von Transaktionen, die aus einem Klick resultieren, der während des angegebenen Zeitraums aufgetreten ist. Wenn ein Portfolio eine erhebliche Verzögerung zwischen Klicks und Transaktionen aufweist, ist diese Option nützlich, um den historischen Umsatz pro Klick für das Portfolio zu berechnen, der das im Laufe der Zeit zu erwartende Umsatzverhalten angibt.</li><li><i>Transaktionsdatum</i> (Standard): Zeigt Transaktionen an, deren Transaktionsdatum im angegebenen Zeitraum aufgetreten ist. Dies gibt an, wie viel Umsatz innerhalb des angegebenen Zeitraums erzielt wurde.</li></ul> |

### (Alte Benutzeroberfläche) Standardeinstellungen und Einstellungen für die benutzerdefinierte Ansicht {#view-settings}

| **tab** | **Feld** | **Beschreibung** |
| --- | --- | --- |
| [Über allen Registerkarten] | -Name | Ein eindeutiger Name für die Ansicht. Der Name einer Standardansicht kann nicht bearbeitet werden.<p><b>Tipp:</b> Verwenden Sie einen Namen, der Ihnen hilft, die Registerkarte und die Informationen zu identifizieren, für die sie gilt (z. B. „Ausgesetzte Kampagnen“ oder „Top 50-Anzeigen„). |
|   | Universale Ansicht | (Schreibgeschützt für vorhandene Ansichten) Stellt die Dateneinstellungen für alle Entitätsansichten zur Verfügung (für Kampagnen, Anzeigen usw.). Universelle Ansichten können Klassifizierungsspalten für Metriken und Beschriftungen enthalten - jedoch keine Eigenschaftenspalten (wie Entitätsname und -status), da sie sich nach Entitätstyp unterscheiden - sowie alle anderen Ansichtsattribute. Alle Filterkriterien werden, sofern zutreffend, auf die Entitätsansicht angewendet und andernfalls ignoriert. Alle Metrikfilter werden lokal ausgewertet (z. B. werden für Klicks \> 1000 Kampagnen Kampagnen mit mehr als 1000 Klicks angezeigt und die Ansicht Anzeigengruppen zeigt Anzeigengruppen mit mehr als 1000 Klicks an).<p>Die Eigenschaftenspalten für eine universelle Ansicht werden aus der Standardansicht der Entität abgerufen. Sie können die Standardeigenschaftsspalten für eine bestimmte Entität in den Standardansichtseinstellungen ändern.<p>Sobald Sie diese Option aktivieren oder deaktivieren, können Sie die Änderung nicht mehr in der vorhandenen Ansicht speichern, sondern eine neue Ansicht mit der Änderung erstellen. |
|   | Freigeben | (Nur vorhandene benutzerdefinierte Ansichten; optional) Stellt die Ansicht allen anderen Benutzern zur Verfügung, die die Daten des Werbetreibenden anzeigen können. Andere Benutzer können die Ansicht nicht bearbeiten oder löschen, aber sie können aus den Einstellungen eine neue Ansicht erstellen. In Ihren Ansichtslisten ist jede Ansicht, die eine andere Person teilt, kursiv gedruckt, z. B _„Kampagnen mit der besten Leistung_. |
| Spalten | Ausgewählte Spalten und Reihenfolge | Die Spalten der angezeigten Daten und ihre Reihenfolge:<ul><li> (So fügen Sie eine Spalte hinzu) Klicken Sie in der Liste Verfügbare Spalten auf einen Spaltennamen, und ziehen Sie ihn dann entweder in die Liste Ausgewählte Spalten und Sortierung oder klicken Sie auf ![Pfeil nach rechts](/help/search-social-commerce/assets/chevron-right.png), um ihn dorthin zu verschieben.</li><li>(So ändern Sie die horizontale Position einer Spalte) Klicken Sie in der Liste Ausgewählte Spalten und Reihenfolge auf den Spaltennamen, und ziehen Sie die Spalte dann entweder an die gewünschte Position, oder klicken Sie auf ![Nach-oben-](/help/search-social-commerce/assets/chevron-up.png) oder ![Nach-unten-](/help/search-social-commerce/assets/chevron-down.png), um sie dorthin zu verschieben. Der Name der oberen Spalte wird in der linken Spalte angezeigt.</li><li>(Um eine Spalte zu entfernen) Klicken Sie in der Liste Ausgewählte Spalten und Sortierung auf einen Spaltennamen, und ziehen Sie ihn dann entweder in die Liste Verfügbare Spalten oder klicken Sie auf ![Nach links](/help/search-social-commerce/assets/chevron-left.png), um ihn dorthin zu verschieben.</li></ul><b>Daten filtern</b><p>Um nur einen bestimmten Datentyp aufzulisten, klicken Sie auf eines der Symbole neben der Liste:<ul><li>![Eigenschaftensymbol](/help/search-social-commerce/assets/properties-icon.png) für Eigenschaftsnamen und IDs für Suchkomponenten wie Status</li><li>![Traffic-Symbol](/help/search-social-commerce/assets/traffic-metrics-icon.png) für standardmäßige Traffic-Metriken wie Impressionen und Klicks</li><li>![Umsatzsymbol](/help/search-social-commerce/assets/revenue-metrics-icon.png) (für Konversionsmetriken, die für den Advertiser verfolgt werden, einschließlich Konversions- und Site-Interaktionsmetriken, die mit Analytics synchronisiert wurden)</li><li>![Benutzerdefiniertes Symbol](/help/search-social-commerce/assets/custom-metrics-icon.png) (für benutzerdefinierte abgeleitete Metriken, die vom Advertiser erstellt wurden)</li><li>![Classification icon](/help/search-social-commerce/assets/classifications-icon.png) (für Label-Classifications).</li></ul> <b>Zusätzliche Hinweise:</b><ul><li>Informationen zum Hinzufügen, Erstellen oder Bearbeiten neuer Metriken finden Sie unter &quot;[Erstellen einer benutzerdefinierten Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md)&quot;, &quot;[Bearbeiten einer benutzerdefinierten Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md)&quot; und &quot;[Löschen einer benutzerdefinierten Metrik](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md)&quot;.</li><li>Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, werden keine Summen für geldbasierte Spalten (wie Kosten und CPC) berücksichtigt.</li><li>Sie können [das Spaltenset vorübergehend über das Spaltenüberschriftenmenü bearbeiten](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) und [das Spaltenset über das [!UICONTROL Columns] bearbeiten und sortieren](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Spaltensymbol](/help/search-social-commerce/assets/custom-columns.png "Spaltensymbol")).</li></ul> |
|   | Sortieren nach | Die Spalte, nach der die Daten sortiert werden sollen. Der Standardwert ist für jeden Berichtstyp unterschiedlich. |
|   | Sortierreihenfolge | Gibt an, ob die Daten in **aufsteigender** oder **absteigender** Reihenfolge sortiert werden sollen. Bewegen Sie den Schieberegler, um eine Option auszuwählen. |
| Filter | [Filterdefinitionen] | (Optional) Filter zum Anwenden auf Daten. Beim Anwenden von Filtern werden Zeilen nur dann zurückgegeben, wenn der Wert für eine Spalte die angegebenen Kriterien erfüllt.<p>Für jeden anzuwendenden Filter:<ol><li>Wählen Sie im Menü [!UICONTROL Add Filter] einen Spaltennamen aus. Die Liste enthält alle verfügbaren Spalten und ist nach Spaltentyp sortiert, wobei die Eigenschaftsspalten an erster Stelle stehen.</li><li>Filter für die Spalte definieren</li></ol>(Filter mit Eingabefeldern) Wählen Sie im zweiten Menü einen Operator und geben Sie dann den entsprechenden Wert ein. Bei Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden.<p>Wenn Sie beispielsweise die Spalte „Klicks“ ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie _\>_ und geben Sie `100` in das Eingabefeld ein.<p>Je nach Datentyp können die verfügbaren Operatoren Folgendes umfassen: <i>größer als</i>, <i>kleiner als</i>, <i>gleich</i>, <i>enthält</i>, <i>enthält</i>, <i>beginnt mit</i>, <i>endet mit</i>,<i>kein Wert</i> oder <i>hat einen Wert</i> <i>before</i>, <i>after</i> oder <i>no date</i>.<p>(Filter ohne Eingabefelder) Klicken Sie ![Pfeil nach unten](/help/search-social-commerce/assets/arrow-down-expand.png) neben dem Menü Listenelemente auswählen und aktivieren Sie dann die Kontrollkästchen neben den einzelnen einzuschließenden Werten.<p><b>Hinweise:</b><ul><li>Sie können Änderungen an Filtern auf Ihre Standardansichtseinstellungen anwenden, aber nicht speichern.</li><li>Sie können auch [vorübergehend die entsprechenden Filter ändern](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) in der Ansicht ändern.</li></ul> |
|   | Zeilen nur mit Leistungsdaten einschließen | (Nur die Ansichten Anzeigengruppen, Keyword, Produktgruppen, Platzierungen und automatische Targeting ) <p>Enthält nur Zeilen mit Leistungsdaten während der angegebenen Datumswerte. Standardmäßig ist diese Option aktiviert, um die Seitenladezeit zu reduzieren. <p><b>Warnung</b>: Wenn Sie die Option deaktivieren und die Ansicht viele Entitäten ohne Leistungsdaten enthält, dauert es länger, bis die Daten angezeigt werden.<p> <b>Hinweis</b>: Sie können Änderungen an Filtern auf Ihre standardmäßigen Anzeigeeinstellungen anwenden, aber nicht speichern. Standardansichten zeigen immer nur Entitäten mit Leistungsdaten an. |
| Datum | Datumsbereich | (Wenn „Datumsbereich einschließen“ ausgewählt ist)<p>Der Datumsbereich, für den Daten generiert werden sollen. Eine Option auswählen:<ul><li><i>[Vorgabenbereich]</i>: Eine Liste der allgemeinen Zeitinkremente, von &quot;<i>&quot; </i> &quot;<i> 180 Tage</i>. Wählen Sie eine aus der Liste aus. Der Standardwert lautet <i>Gestern</i>. Hinweis: <i>Letzter Monat</i>, <i>Letzte 3 Monate</i> und <i>Letzte 6 Monate</i> zeigen Daten für die vorherigen Kalendermonate an.</li><li><i>Benutzerdefinierter Datumsbereich: </i> Sie das Start- und Enddatum an. Geben Sie Daten im Format MM/TT/JJJJ oder M/TT/JJJJ ein oder klicken Sie ![Kalendersymbol](/help/search-social-commerce/assets/calendar.png) neben einem Feld und wählen Sie ein Datum aus.</li></ul> |
|   | Vergleich | Vergleicht Daten für den angegebenen Datumsbereich mit Daten für einen zweiten Datumsbereich. Wenn Sie diese Option auswählen, geben Sie den zweiten Datumsbereich an. Für jede reguläre Datenspalte werden zwei zusätzliche Spalten hinzugefügt. Anstatt beispielsweise nur eine Spalte für „Impressionen“ einzubeziehen, enthält der Bericht Spalten für „Impressionen - Bereich 1“, „Impressionen - Bereich 2“ und „Impressionsdifferenz“.<p><b>Hinweise:</b><ul><li>Die Spalte „Differenz“ wird für abgeleitete Metriken nicht angezeigt.</li><li>Bei Berichten, die große Datumsbereiche vergleichen, kann die Generierung länger dauern.</li></ul> |
|   | Vergleichsformat | (Wenn [!UICONTROL Comparison] aktiviert ist) So drücken Sie den Unterschied zwischen den Daten in den beiden ausgewählten Datumsbereichen in der Spalte &quot;[_Datenfeld_] Differenz“ aus. Eine Option auswählen:<ul><li><i>Varianz</i> (Standard): Zeigt die Differenz als numerischen Wert an.</li><li><i>% Änderung</i>: Zeigt die Differenz als Prozentsatz an.</li></ul> |
| Zusätzliche Einstellungen | Standard verwenden | Wendet die in den Attributionseinstellungen für die Konversion auf Advertiser-Ebene angegebenen Attributionseinstellungen an. |
|   | Attributionsregel | (Nur Werbetreibende mit dem pixelbasierten Konversions-Tracking-Service von Adobe Advertising) Auf der Registerkarte wird erläutert, wie Konversionsdaten - möglicherweise über mehrere Anzeigenkanäle und Portfolios hinweg - in einer Ereignisreihe zugeordnet werden, die zu einer Konversion führt. Standardmäßig ist die in den Attributionseinstellungen für die Konversion auf Advertiser-Ebene angegebene Regel ausgewählt.<ul><li> <i>Erstes Ereignis</i>: Ordnet die Konversion dem ersten bezahlten Klick in der Reihe innerhalb des Klick-Lookback-Fensters des Werbetreibenden oder, falls keine bezahlten Klicks aufgetreten sind, der letzten Impression innerhalb des Impression-Lookback-Fensters des Werbetreibenden zu.</li><li><i>Gewicht des ersten Ereignisses Mehr</i>: Attributiert die Konversion auf alle Ereignisse in der Reihe, die innerhalb des Klick-Lookback-Fensters und Impression-Lookback-Fensters des Advertisers aufgetreten sind, gewichtet jedoch das erste Ereignis am meisten und die folgenden Ereignisse nacheinander weniger. Wenn der Konversion sowohl bezahlte Klicks als auch Impressions vorausgehen, wird die angegebene Impression-Überschreibungsgewichtung weiter auf die Impressions angewendet. Wenn der Konversion nur Impressions vorausgehen, werden die Impressions nach dem Durchsichtsgewicht des Advertisers gewichtet, anstatt nach dem Gewicht der Impression-Überschreibungen.</li><li><i>Ereignisverteilung</i>: Attributiert die Konversion zu gleichen Teilen jedem Ereignis in der Reihe, das im Klick-Lookback-Fenster und im Impression-Lookback-Fenster des Werbetreibenden aufgetreten ist. Wenn der Konversion sowohl bezahlte Klicks als auch Impressions vorausgehen, wird die angegebene Impression-Überschreibungsgewichtung weiter auf die Impressions angewendet. Wenn der Konversion nur Impressions vorausgehen, werden die Impressions nach dem Durchsichtsgewicht des Advertisers gewichtet, anstatt nach dem Gewicht der Impression-Überschreibungen.</li><li><i>Letztes Ereignis gewichten Mehr</i>: Ordnet die Konversion allen Ereignissen in der Reihe zu, die im Klick-Lookback-Fenster und Impression-Lookback-Fenster des Werbetreibenden stattgefunden haben. Gibt jedoch dem letzten Ereignis das meiste Gewicht und den vorangehenden Ereignissen sukzessive weniger Gewicht. Wenn der Konversion sowohl bezahlte Klicks als auch Impressions vorausgehen, wird die angegebene Impression-Überschreibungsgewichtung weiter auf die Impressions angewendet. Wenn der Konversion nur Impressions vorausgehen, werden die Impressions nach dem Durchsichtsgewicht des Advertisers gewichtet, anstatt nach dem Gewicht der Impression-Überschreibungen.</li><li><i>Letztes Ereignis</i> (Standard): Ordnet die Konversion dem letzten bezahlten Klick in der Reihe innerhalb des Klick-Lookback-Fensters des Werbetreibenden oder, falls keine bezahlten Klicks aufgetreten sind, der letzten Impression innerhalb des Impression-Lookback-Fensters des Werbetreibenden zu.</li><li><i>U-förmig</i>: Ordnet die Konversion allen Ereignissen in der Reihe zu, die im Klick-Lookback-Fenster des Werbetreibenden und im Impression-Lookback-Fenster stattgefunden haben. Gibt jedoch dem ersten und letzten Ereignis das größte Gewicht zu, wobei die Ereignisse in der Mitte des Konversionspfads sukzessive weniger Gewicht erhalten. Wenn der Konversion sowohl bezahlte Klicks als auch Impressions vorausgehen, wird die angegebene Impression-Überschreibungsgewichtung weiter auf die Impressions angewendet. Wenn der Konversion nur Impressions vorausgehen, werden die Impressions nach dem Durchsichtsgewicht des Advertisers gewichtet, anstatt nach dem Gewicht der Impression-Überschreibungen.</li></ul><p><b>Hinweise:</b><ul><li>Alle Attributionsregeln außer „Letztes Ereignis“ sind nur für Advertiser mit Adobe Advertising-Klick-Tracking und mit Konversions-Tracking von Adobe Advertising oder Adobe Analytics (mit Analytics-Integration) verfügbar.</li><li>Die Zuordnungsregeln gelten für Klicks auf bezahlte Anzeigen in jedem beliebigen Kanal. Sie gelten nicht für Impressionen für Paid Search-Anzeigen, die nicht auf Ereignisebene verfolgt werden können.</li><li>Wenn Sie Konversionsdaten mit einer beliebigen Attributionsregel außer einer der Regeln des „letzten Ereignisses“ melden, können die Ereignisse, die der Konversion vorangehen, über mehrere Portfolios hinweg auftreten. In diesem Fall enthält die Ansicht nur dann Daten für die Konversion, wenn die Anzeigen oder Keywords in diesen Portfolios in der Ansicht enthalten sind.</li><li>Für Standardansichten empfehlen wir, die standardmäßige Attributionsregel beizubehalten, mit der während der Angebotsoptimierung der [Zielwert](/help/search-social-commerce/glossary.md#o-p) (früher als „gewichteter Umsatz“ bezeichnet) für jede Gebotseinheit berechnet wird.</li></ul> |
|   | Konversionen basierend auf | So melden Sie Konversionsdaten:<ul><li><i>Klickdatum</i>: Zum Anzeigen von Transaktionen, die aus einem Klick resultieren, der während des angegebenen Zeitraums aufgetreten ist. Wenn ein Portfolio eine erhebliche Verzögerung zwischen Klicks und Transaktionen aufweist, ist diese Option nützlich, um den historischen Umsatz pro Klick für das Portfolio zu berechnen, der das im Laufe der Zeit zu erwartende Umsatzverhalten angibt.</li><li><i>Transaktionsdatum</i> (Standard): Zeigt Transaktionen an, deren Transaktionsdatum im angegebenen Zeitraum aufgetreten ist. Dies gibt an, wie viel Umsatz innerhalb des angegebenen Zeitraums erzielt wurde.</li></ul> |
