---
title: Standard- und benutzerdefinierte Ansichten verwalten
description: Erfahren Sie, wie Sie Ihre Standardansichten und benutzerdefinierten Ansichten anpassen können.
exl-id: b28f58f6-c80a-45f8-8c5f-b821a76dab6d
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: d32c14acdd6bff51ac985dd75c5e7694967481a9
workflow-type: tm+mt
source-wordcount: '2835'
ht-degree: 0%

---

# Standard- und benutzerdefinierte Ansichten verwalten

Ihre Standardansichten und benutzerdefinierten Ansichten ermöglichen es Ihnen, die Leistungsdaten anzupassen, die in den Datenansichten der Suchkampagnen angezeigt werden. Zu den Anzeigeeinstellungen gehören die einzuschließenden Spalten, Filter, Datumsbereich, Attributionseinstellungen für Konversionen und andere erweiterte Einstellungen. Sie können die Einstellungen entweder vorübergehend anwenden oder speichern. (Ausnahme: Filter für Standardansichten können nicht gespeichert werden.) Jede standardmäßige und reguläre benutzerdefinierte Ansicht gilt für eine bestimmte Entitätsansicht (z. B. [!UICONTROL Campaigns]) und nur spezifische Advertiser-Konten. Jede universelle benutzerdefinierte Ansicht gilt für alle Entitätsansichten eines bestimmten Advertisers und kann daher keine Eigenschaftsspalten (wie Entitätsname oder Status) enthalten, die je nach Entitätstyp variieren.

Standardmäßig werden bei jeder Anmeldung Standardansichten angezeigt. Sie können weitere benutzerdefinierte Ansichten erstellen und diese jederzeit anwenden. Optional können Sie jede von Ihnen erstellte benutzerdefinierte Ansicht für alle anderen Benutzer freigeben, die die Daten des Advertisers anzeigen können. In Ihrer Ansicht wird jede Ansicht, die eine andere Person teilt, kursiv angezeigt, z. B. &quot;*Kampagnen mit Top-Leistung*.&quot; Nur die Person, die eine benutzerdefinierte Ansicht erstellt, kann sie löschen.

Jede Ansicht ist als Tastaturbefehl im [!UICONTROL Custom Views] im linken Bereich.

## Anwenden einer standardmäßigen oder benutzerdefinierten Ansicht

* (Standardansichten) Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **\[Entitätstyp\]**.

* (Benutzerdefinierte Ansichten) Im linken Navigationsbereich:

   1. Klicken Sie im linken Bereich auf die **[!UICONTROL Custom Views]** , um es zu erweitern.

      Ansichten werden nach der jeweiligen Entität sortiert.

   1. Erweitern Sie die verfügbaren Menüs.

      &quot;[!UICONTROL Universal Views]&quot; enthält benutzerdefinierte Ansichten, die in allen Entitätsansichten verwendet werden können. Alle anderen benutzerdefinierten Ansichten werden nach Entitätstyp gruppiert.

   1. Klicken Sie auf den Namen der Ansicht.

      Wenn die Ansicht universell ist oder für die aktuelle Entität gilt, wird die Datentabelle gemäß der Ansichtskonfiguration erneut angezeigt. Wenn die Ansicht für eine andere Entität gilt, werden die Daten für die jeweilige Entität gemäß der Ansichtskonfiguration angezeigt.

## Erstellen einer benutzerdefinierten Ansicht {#create-custom-view}

Benutzerdefinierte Ansichten gelten nur für die Kampagnenverwaltungsansichten.

>[!NOTE]
>
>Zusätzlich zu den Anzeigeeinstellungen, die Sie für die benutzerdefinierte Ansicht festlegen, wird auch die aktuelle Spaltensortierungsreihenfolge gespeichert.

1. Klicken Sie auf der rechten Seite der Symbolleiste über der Datentabelle auf den Namen der aktuellen Ansicht (möglicherweise &quot;[!UICONTROL Default]&quot;).

1. Geben Sie die [Einstellungen für benutzerdefinierte Ansichten](#view-settings):

   1. (Optional) Um die Dateneinstellungen für alle Entitätsansichten verfügbar zu machen (für [!UICONTROL Campaigns], [!UICONTROL Ads]usw.), wählen Sie **[!UICONTROL Universal View]**.

      Nachdem Sie diese Option aktiviert oder deaktiviert haben, können Sie die Änderung nicht in der vorhandenen Ansicht speichern, sondern eine neue Ansicht mit der Änderung erstellen.

   1. (Optional) Um die Ansicht allen anderen Benutzern zur Verfügung zu stellen, die die Daten des Advertisers anzeigen können, verschieben Sie die **[!UICONTROL Shared]** Regler zu *[!UICONTROL Yes]*.

   1. (Optional) Auf der Registerkarte **[!UICONTROL Columns]** ändern Sie die für die Registerkarte verfügbaren Spalten, deren Reihenfolge und die Sortierung der Zeilen.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Filters]** und geben Sie dann die anzuwendenden Filter an.

      Beim Anwenden von Filtern werden nur Zeilen zurückgegeben, wenn der Wert für eine Metrik bestimmte Kriterien erfüllt, unabhängig davon, ob die Metrik als Spalte im Bericht enthalten ist oder nicht.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Date]** und ändern Sie die Standardeinstellungen für das Datum.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Additional Settings]** und ändern Sie die Einstellungen.

1. Klicken **[!UICONTROL Save as New]**.

1. Geben Sie den Namen der neuen Ansicht ein und klicken Sie auf **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Verwenden Sie einen Namen, der Ihnen dabei hilft, den Tab und die Informationen zu identifizieren, auf die er angewendet wird (z. B. &quot;Anhaltende Kampagnen&quot;oder &quot;Top 50-Werbeanzeigen&quot;).

### Bearbeiten einer standardmäßigen oder benutzerdefinierten Ansicht

1. Öffnen Sie die Ansichtseinstellungen:

   * (Wenn Sie die Ansicht bereits angewendet haben) Klicken Sie auf der rechten Seite der Symbolleiste über der Datentabelle auf den Namen der aktuellen Ansicht (möglicherweise &quot;[!UICONTROL Default]&quot;).

   * (Benutzerdefinierte Ansichten, die nicht angewendet werden) Klicken Sie im linken Bereich auf ![Benutzerdefinierte Ansichten](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Benutzerdefinierte Ansichten") , um die [!UICONTROL Custom Views] Menü. Klicken Sie auf den Namen der benutzerdefinierten Ansicht.

1. Bearbeiten Sie die [Ansichtseinstellungen](#view-settings):

   1. (Optional) So aktivieren oder deaktivieren Sie die Dateneinstellungen für alle Ansichten der Suchentität (für [!UICONTROL Campaigns], [!UICONTROL Ad Groups]usw.) auswählen oder die Auswahl aufheben **[!UICONTROL Universal View]**.

      Sie können die Änderung nicht in der vorhandenen Ansicht speichern, sondern eine neue Ansicht mit der Änderung erstellen.

   1. (Optional; benutzerdefinierte Ansichten, die Sie nur erstellt haben) Wenn die Ansicht nicht bereits öffentlich ist, stellen Sie sie allen anderen Benutzern zur Verfügung, die die Daten des Advertisers durch Verschieben der **[!UICONTROL Shared]** Regler zu *[!UICONTROL Yes]*.

   1. (Optional) Auf der Registerkarte **[!UICONTROL Columns]** ändern Sie die für die Registerkarte verfügbaren Spalten, deren Reihenfolge und die Sortierung der Zeilen.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Filters]** und bearbeiten Sie dann die anzuwendenden Filter.

      Beim Anwenden von Filtern werden nur Zeilen zurückgegeben, wenn der Wert für eine Metrik bestimmte Kriterien erfüllt, unabhängig davon, ob die Metrik als Spalte im Bericht enthalten ist oder nicht.

      >[!NOTE]
      >
      >Sie können Änderungen an Filtern auf Ihre standardmäßigen Ansichtseinstellungen anwenden, aber nicht speichern.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Date]** und ändern Sie die Standardeinstellungen für das Datum.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Additional Settings]** und ändern Sie die Einstellungen.

1. Wenden Sie die Einstellungen an oder speichern Sie sie:

   * Um die Einstellungen vorübergehend anzuwenden, ohne sie in der Ansicht zu speichern, klicken Sie auf **[!UICONTROL Apply]**.

     Die Einstellungen werden auf die Registerkarte angewendet, bis Sie von der Verwaltungsansicht der obersten Ebene abrücken oder (falls zutreffend) [Anzeigen von Daten für einen anderen Advertiser](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (Für von Ihnen erstellte Standardansichten und benutzerdefinierte Ansichten) Um die Einstellungen in der aktuellen Ansicht zu speichern, klicken Sie auf **[!UICONTROL Save]**.

   * Um die Einstellungen in einer neuen, benutzerdefinierten Ansicht zu speichern, klicken Sie auf **[!UICONTROL Save As]**. Im [!UICONTROL Enter New Custom View Name] , geben Sie den Namen der neuen Ansicht ein und klicken Sie auf **[!UICONTROL Save]**.

## Zurücksetzen einer Standardansicht auf die Standardeinstellungen des Systems

Durch das Wiederherstellen der standardmäßigen Ansichtseinstellungen werden alle gespeicherten Einstellungen entfernt und die Standardeinstellungen des Systems angewendet.

Die Standardeinstellungen des Systems variieren je nach Registerkarte. Für die meisten Registerkarten zeigt die standardmäßige Systemansicht Daten für den vorherigen Tag für Elemente in aktivierten Konten an, die aktiv sind (z. B. nur aktive Anzeigengruppen in aktiven Kampagnen), wobei die Daten nach Kosten sortiert sind und Konversionsdaten auf der Grundlage des Transaktionsdatums basieren.

1. Klicken Sie im linken Bereich auf ![Benutzerdefinierte Ansichten](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Benutzerdefinierte Ansichten") , um die [!UICONTROL Custom Views] Menü.

   Ansichten werden nach der jeweiligen Entität sortiert.

1. Klicken Sie neben dem Namen der Ansicht auf ![Standardeinstellungen wiederherstellen](/help/search-social-commerce/assets/revert.png "Standardeinstellungen wiederherstellen").

## Benutzerdefinierte Ansicht löschen

Sie können jede von Ihnen erstellte benutzerdefinierte Ansicht löschen.

Wenn Sie eine benutzerdefinierte Ansicht löschen, die auf die aktuelle Registerkarte angewendet wird, wird auf der Registerkarte weiterhin die benutzerdefinierte Ansicht angezeigt, bis Sie sich außerhalb des Ansichtssatzes bewegen (z. B. aus Ansichten innerhalb der [!UICONTROL Search] Menü [!UICONTROL Reports] Menü) oder (falls zutreffend) bei [Anzeigen von Daten für einen anderen Advertiser](/help/search-social-commerce/common-tasks/change-advertiser.md).

1. Klicken Sie im linken Bereich auf ![Benutzerdefinierte Ansichten](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Benutzerdefinierte Ansichten") , um die [!UICONTROL Custom Views] Menü.

1. Halten Sie den Cursor über den Namen der benutzerdefinierten Ansicht und klicken Sie auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

1. Klicken Sie in der Bestätigungsnachricht auf **[!UICONTROL Continue]**.

## Standard- und benutzerdefinierte Ansichtseinstellungen {#view-settings}

| **Registerkarte** | **Feld** | **Beschreibung** |
| --- | --- | --- |
| [Über allen Registerkarten] | Name | Ein eindeutiger Name für die Ansicht. Sie können den Namen einer Standardansicht nicht bearbeiten. <p><b>Tipp:</b> Verwenden Sie einen Namen, der Ihnen dabei hilft, den Tab und die Informationen zu identifizieren, auf die er angewendet wird (z. B. &quot;Anhaltende Kampagnen&quot;oder &quot;Top 50-Werbeanzeigen&quot;). |
|   | Universelle Ansicht | Macht die Dateneinstellungen in allen Entitätsansichten verfügbar (für Kampagnen, Anzeigen usw.). Universelle Ansichten können Metrik- und Beschriftungs-Classification-Spalten - jedoch nicht Eigenschaftenspalten (wie Entitätsname und Status) enthalten, da sie sich nach Entitätstyp unterscheiden - sowie alle anderen Ansichtsattribute. Alle Filterkriterien werden ggf. auf die Entitätsansicht angewendet und andernfalls ignoriert. Alle Metrikfilter werden lokal ausgewertet (z. B. für Klicks \> 1000 zeigt die Kampagnenansicht Kampagnen mit mehr als 1000 Klicks an, und in der Anzeigengruppenansicht werden Anzeigengruppen mit mehr als 1000 Klicks angezeigt).<p>Die Eigenschaftsspalten für eine universelle Ansicht werden aus der Standardansicht der Entität abgerufen. Sie können die Standardeigenschaftsspalten für eine bestimmte Entität in den Standardansichtseinstellungen ändern.<p>Nachdem Sie diese Option aktiviert oder deaktiviert haben, können Sie die Änderung nicht in der vorhandenen Ansicht speichern, sondern eine neue Ansicht mit der Änderung erstellen. |
|   | Freigeben | (Nur benutzerdefinierte Ansichten; optional) Stellt die Ansicht allen anderen Benutzern zur Verfügung, die die Daten des Advertisers anzeigen können. Andere Benutzer können die Ansicht nicht bearbeiten oder löschen, sie können jedoch eine neue Ansicht aus den Einstellungen erstellen. In Ihren Ansichtslisten wird jede Ansicht, die eine andere Person teilt, kursiv angezeigt, z. B. &quot;_Kampagnen mit Top-Leistung_.&quot; |
| Spalten | Ausgewählte Spalten und Reihenfolge | Die angezeigten Datenspalten und ihre Reihenfolge:<ul><li> (Um eine Spalte hinzuzufügen) Klicken Sie in der Liste Verfügbare Spalten auf einen Spaltennamen und ziehen Sie ihn dann entweder in die Liste Ausgewählte Spalten und Sortierung oder klicken Sie auf ![Rechtspfeil](/help/search-social-commerce/assets/chevron-right.png) um es dorthin zu verschieben.</li><li>(Um die horizontale Position einer Spalte zu ändern) Klicken Sie in der Liste Ausgewählte Spalten und Sortierung auf den Spaltennamen und ziehen Sie ihn dann an die gewünschte Position oder klicken Sie auf ![Pfeil nach oben](/help/search-social-commerce/assets/chevron-up.png) oder ![Nach unten](/help/search-social-commerce/assets/chevron-down.png) um es dorthin zu verschieben. Der Name der oberen Spalte wird in der linken Spalte angezeigt.</li><li>(Um eine Spalte zu entfernen) Klicken Sie in der Liste Ausgewählte Spalten und Sortierung auf einen Spaltennamen und ziehen Sie ihn dann entweder in die Liste Verfügbare Spalten oder klicken Sie auf ![Linkspfeil](/help/search-social-commerce/assets/chevron-left.png) um es dorthin zu verschieben.</li></ul><b>Daten filtern</b><p>Um nur einen bestimmten Datentyp aufzulisten, klicken Sie auf eines der Symbole neben der Liste:<ul><li>![Eigenschaftssymbol](/help/search-social-commerce/assets/properties-icon.png) für Eigenschaftsnamen und IDs für Suchkomponenten, z. B. Status</li><li>![Traffic-Symbol](/help/search-social-commerce/assets/traffic-metrics-icon.png) für standardmäßige Traffic-Metriken wie Impressionen und Klicks</li><li>![Umsatzsymbol](/help/search-social-commerce/assets/revenue-metrics-icon.png) (für Umsatzmetriken/Transaktionseigenschaften, die für den Advertiser verfolgt werden, einschließlich Konversions- und Site-Interaktionsmetriken, die aus Analytics synchronisiert werden)</li><li>![benutzerdefiniertes Symbol](/help/search-social-commerce/assets/custom-metrics-icon.png) (für benutzerdefinierte abgeleitete Metriken, die vom Advertiser erstellt wurden)</li><li>![Classification-Symbol](/help/search-social-commerce/assets/classifications-icon.png) (für Beschriftungsklassifizierungen).</li></ul> <b>Zusätzliche Hinweise:</b><ul><li>Informationen zum Hinzufügen, Erstellen oder Bearbeiten neuer Metriken finden Sie unter &quot;Benutzerdefinierte Metrik erstellen&quot;, &quot;Benutzerdefinierte Metrik bearbeiten&quot;und &quot;Benutzerdefinierte Metrik löschen&quot;.</li><li>Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, werden die Summen nicht für monetäre Spalten (wie Kosten und CPC) berücksichtigt.</li><li>Sie können [Bearbeiten Sie den Spaltensatz vorübergehend über das Menü der Spaltenüberschrift](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md), und [Bearbeiten und sortieren Sie den Spaltensatz im [!UICONTROL Columns] icon](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Symbol &quot;Spalten&quot;](/help/search-social-commerce/assets/custom-columns.png "Symbol &quot;Spalten&quot;")).</li></ul> |
|   | Sortieren nach | Die Spalte, nach der die Daten sortiert werden sollen. Der Standardwert ist für jeden Berichtstyp unterschiedlich. |
|   | Sortierfolge | Sortieren der Daten in **Aufsteigend** oder **Absteigend** bestellen. Verschieben Sie den Regler, um eine Option auszuwählen. |
| Filter | [Filterdefinitionen] | (Optional) Auf Daten anzuwendende Filter. Beim Anwenden von Filtern werden nur Zeilen zurückgegeben, wenn der Wert für eine Spalte bestimmte Kriterien erfüllt.<p>Für jeden anzuwendenden Filter:<ol><li>Wählen Sie im Menü Filter hinzufügen einen Spaltennamen aus. Die Liste enthält alle verfügbaren Spalten und ist nach Spaltentyp sortiert, wobei die Eigenschaftsspalten zuerst angezeigt werden.</li><li>Filter für die Spalte definieren</li></ol>(Filter mit Eingabefeldern) Wählen Sie einen Operator aus dem zweiten Menü aus und geben Sie dann den entsprechenden Wert ein. Bei Werten wird nicht zwischen Groß- und Kleinschreibung unterschieden. Klicks ![Häkchen](/help/search-social-commerce/assets/select.png) wenn Sie fertig sind.<p>Wenn Sie beispielsweise die Spalte &quot;Klicks&quot;ausgewählt haben und nur Zeilen mit mehr als 100 Klicks zurückgeben möchten, wählen Sie _\>_ und eingeben `100` im Eingabefeld.<p>Je nach Datentyp können die verfügbaren Operatoren Folgendes umfassen: <i>größer als</i>, <i>kleiner als</i>, <i>gleich</i>, <i>contains</i>, <i>enthält nicht</i>, <i>beginnt mit</i>, <i>endet mit</i>,<i>kein Wert</i>oder <i>hat Wert</i> <i>before</i>, <i>after</i>oder <i>kein Datum</i>.<p>(Filter ohne Eingabefelder) Klicken Sie ![Pfeil nach unten](/help/search-social-commerce/assets/arrow-down-expand.png) neben dem Menü &quot;Listenelemente auswählen&quot;und aktivieren Sie dann die Kontrollkästchen neben den einzelnen einzuschließenden Werten. Klicks ![Häkchen](/help/search-social-commerce/assets/select.png) wenn Sie fertig sind.<p><b>Hinweise:</b><ul><li>Sie können Änderungen an Filtern auf Ihre standardmäßigen Ansichtseinstellungen anwenden, aber nicht speichern.</li><li>Sie können auch [Ändern Sie vorübergehend die entsprechenden Filter](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) in der Ansicht.</li></ul> |
|   | Zeilen nur mit Leistungsdaten einschließen | (Nur Anzeigengruppen, Suchbegriff, Produktgruppen, Platzierungen und automatische Targeting-Ansichten) <p>Umfasst nur Zeilen mit Leistungsdaten während der angegebenen Datumsangaben. Standardmäßig ist diese Option ausgewählt, um die Seitenladezeit zu verkürzen. <p><b>Warnung</b>: Wenn Sie die Option deaktivieren und die Ansicht viele Entitäten ohne Leistungsdaten enthält, dauert die Anzeige der Daten länger.<p> <b>Hinweis</b>: Sie können Änderungen an Filtern auf Ihre standardmäßigen Ansichtseinstellungen anwenden, aber nicht speichern. Standardansichten zeigen immer nur Entitäten mit Leistungsdaten an. |
| Datum | Datumsbereich | (Wenn &quot;Datumsbereich einschließen&quot;ausgewählt ist)<p>Der Datumsbereich, für den Daten generiert werden sollen. Wählen Sie eine Option aus:<ul><li><i>[Vorgabenbereich]</i>: Eine Liste der gängigen Zeitabstände, die von <i>Heute</i> nach <i>Letzte 180 Tage</i>. Wählen Sie einen aus der Liste aus. Der Standardwert ist <i>Gestern</i>. Hinweis: <i>Letzter Monat</i>, <i>Letzte 3 Monate</i>, und <i>Letzte 6 Monate</i> Daten der vorherigen Kalendermonate anzeigen.</li><li><i>Benutzerdefinierter Datumsbereich:</i> Geben Sie das Start- und Enddatum an. Geben Sie Datumsangaben in das Format MM/TT/JJJJ oder M/D/JJJJ ein oder klicken Sie auf ![Kalendersymbol](/help/search-social-commerce/assets/calendar.png) neben einem Feld und wählen Sie ein Datum aus.</li></ul> |
|   | Vergleich | Vergleicht Daten für den angegebenen Datumsbereich mit Daten für einen zweiten Datumsbereich. Wenn Sie diese Option auswählen, werden für jede reguläre Datenspalte zwei zusätzliche Spalten hinzugefügt. Anstatt beispielsweise nur eine Spalte für &quot;Impressionen&quot;einzuschließen, enthält der Bericht Spalten für &quot;Impressionsbereich 1&quot;, &quot;Impressionsbereich 2&quot;und &quot;Impressionsdifferenz&quot;.<p><b>Hinweise:</b><ul><li>Die Differenzspalte wird für abgeleitete Metriken nicht angezeigt.</li><li>Berichte, die große Datumsbereiche vergleichen, können länger dauern.</li></ul> |
|   | Vergleichsformat | So geben Sie den Unterschied zwischen den Daten in den beiden ausgewählten Datumsbereichen in der &quot;[_Datenfeld_] Differenz&quot;. Wählen Sie eine Option aus:<ul><li><i>Abweichung</i> (Standard): Zeigt die Differenz als numerischen Wert an.</li><li><i>Veränderung in %</i>: Zeigt die Differenz in Prozent an.</li></ul> |
| Zusätzliche Einstellungen | Use Default | Wendet die Attributionseinstellungen an, die in den Attributionseinstellungen für die Konvertierung auf Advertiser-Ebene angegeben sind. |
|   | Attributionsregel | (Nur Werbetreibende mit dem pixelbasierten Konversions-Tracking-Dienst des Adobe Advertisings) Wie können auf der Registerkarte Konversionsdaten - potenziell über mehrere Anzeigenkanäle und Portfolios hinweg - in einer Reihe von Ereignissen zugeordnet werden, die zu einer Konversion führen. Standardmäßig ist die in den Konversions-Attributionseinstellungen auf Advertiser-Ebene angegebene Regel ausgewählt.<ul><li> <i>Erstes Ereignis</i>: Ordnet die Konversion dem ersten gebührenpflichtigen Klick in der Reihe innerhalb des Klick-Lookback-Fensters des Werbetreibenden zu oder, wenn keine gebührenpflichtigen Klicks aufgetreten sind, dem letzten Impression im Impression-Lookback-Fenster des Werbetreibenden.</li><li><i>Gewichtung des ersten Ereignisses - Mehr</i>: Ordnet die Konversion allen Ereignissen in der Reihe zu, die im Klick-Lookback-Fenster und im Impression-Lookback-Fenster des Werbetreibenden stattgefunden haben. Das erste Ereignis erhält jedoch die höchste Gewichtung und die nachfolgenden Ereignisse erhalten eine schrittweise geringere Gewichtung. Wenn der Konversion sowohl gebührenpflichtige Klicks als auch Impressionen vorangehen, wird die angegebene Impressionsüberschreibungsgewichtung weiter auf die Impressionen angewendet. Wenn der Konversion nur Impressionen vorangehen, werden die Impressionen nach der Viewthrough-Gewichtung des Werbetreibenden und nicht nach der Impressions-Überschreibung gewichtet.</li><li><i>Sogar Distribution</i>: Weist die Konversion gleichmäßig jedem Ereignis in der Reihe zu, das im Klick-Lookback-Fenster des Advertisers und im Impression-Lookback-Fenster aufgetreten ist. Wenn der Konversion sowohl gebührenpflichtige Klicks als auch Impressionen vorangehen, wird die angegebene Impressionsüberschreibungsgewichtung weiter auf die Impressionen angewendet. Wenn der Konversion nur Impressionen vorangehen, werden die Impressionen nach der Viewthrough-Gewichtung des Werbetreibenden und nicht nach der Impressions-Überschreibung gewichtet.</li><li><i>Last Event-Mehr</i>: Ordnet die Konversion allen Ereignissen in der Reihe zu, die innerhalb des Klick-Lookback-Fensters und des Impression-Lookback-Fensters des Werbetreibenden stattgefunden haben, gibt jedoch dem letzten Ereignis die höchste Gewichtung und den vorherigen Ereignissen eine schrittweise geringere Gewichtung zu. Wenn der Konversion sowohl gebührenpflichtige Klicks als auch Impressionen vorangehen, wird die angegebene Impressionsüberschreibungsgewichtung weiter auf die Impressionen angewendet. Wenn der Konversion nur Impressionen vorangehen, werden die Impressionen nach der Viewthrough-Gewichtung des Werbetreibenden und nicht nach der Impressions-Überschreibung gewichtet.</li><li><i>Letztes Ereignis</i> (Standard): Ordnet die Konversion dem letzten bezahlten Klick in der Serie innerhalb des Klick-Lookback-Fensters des Advertisers zu oder, wenn keine gebührenpflichtigen Klicks aufgetreten sind, dem letzten Impression im Impression-Lookback-Fenster des Advertisers zu.</li><li><i>U-förmig</i>: Ordnet die Konversion allen Ereignissen in der Reihe zu, die innerhalb des Klick-Lookback-Fensters und des Impression-Lookback-Fensters des Advertisers stattgefunden haben. Dabei wird jedoch das erste Ereignis und das letzte Ereignis am meisten berücksichtigt, wobei die Ereignisse in der Mitte des Konversionspfads schrittweise weniger berücksichtigt werden. Wenn der Konversion sowohl gebührenpflichtige Klicks als auch Impressionen vorangehen, wird die angegebene Impressionsüberschreibungsgewichtung weiter auf die Impressionen angewendet. Wenn der Konversion nur Impressionen vorangehen, werden die Impressionen nach der Viewthrough-Gewichtung des Werbetreibenden und nicht nach der Impressions-Überschreibung gewichtet.</li></ul><p><b>Hinweise:</b><ul><li>Alle Attributionsregeln außer Letztes Ereignis sind nur für Advertiser mit Adobe Advertising-Klick-Tracking und Konversions-Tracking von Adobe Advertising oder Adobe Analytics verfügbar (mit Analytics-Integration).</li><li>Zuordnungsregeln gelten für Klicks auf gebührenpflichtige Anzeigen in beliebigen Kanälen. Sie gelten nicht für Impressionen für Paid Search-Anzeigen, die nicht auf Ereignisebene verfolgt werden können.</li><li>Wenn Sie Konversionsdaten mit einer beliebigen Attributionsregel mit Ausnahme einer der &quot;letzten Ereignisse&quot;-Regeln melden, können die Ereignisse, die zur Konversion führen, über mehrere Portfolios hinweg auftreten. Ist dies der Fall, enthält die Ansicht nur Daten für die Konversion, wenn die Anzeigen oder Suchbegriffe in diesen Portfolios in der Ansicht enthalten sind.</li><li>Für Standardansichten empfehlen wir, die standardmäßige Zuordnungsregel beizubehalten, die zur Berechnung der [Zielwert](/help/search-social-commerce/glossary.md#o-p) (ehemals &quot;gewichteter Umsatz&quot;) für jede Gebotseinheit während der Angebotsoptimierung.</li></ul> |
|   | Konversionen basierend auf | So melden Sie Konversionsdaten:<ul><li><i>Transaktionsdatum</i> (Standard): Zum Anzeigen von Transaktionen, deren Transaktionsdatum im angegebenen Zeitraum auftrat. Dies gibt an, wie viel Umsatz innerhalb des festgelegten Zeitraums erzielt wurde.</li><li><i>Klickdatum</i>: Zum Anzeigen von Transaktionen, die aus einem Klick resultierten, der während des angegebenen Zeitraums erfolgte. Wenn ein Portfolio erhebliche Verzögerungen zwischen Klicks und Transaktionen aufweist, ist diese Option für die Berechnung des historischen Umsatzes pro Klick für das Portfolio nützlich, was das zu erwartende Umsatzwuster im Laufe der Zeit anzeigt. |
