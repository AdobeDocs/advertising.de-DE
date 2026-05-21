---
title: Verwalten von Kennzeichnungsklassifizierungen
description: Erfahren Sie mehr über die Verwendung von Kennzeichnungsklassifizierungen zum Gruppieren Ihrer Kontokomponenten.
feature: Search Label Classifications
source-git-commit: 84eb5f060a696e057f706c0066c18c9afc1511e1
workflow-type: tm+mt
source-wordcount: '1515'
ht-degree: 0%

---

# Verwalten von Kennzeichnungsklassifizierungen

Mit Klassifizierungen von Kennzeichnungen können Sie Ihre Kontokomponenten in aussagekräftigen Sätzen gruppieren. Sie können beispielsweise eine übergeordnete Kennzeichnungsklassifizierung mit dem Namen „Geo“ erstellen, einen anderen Kennzeichnungswert für jede geografische Region (z. B. „Großbritannien“ und „Japan„) innerhalb der Klassifizierung erstellen und dann die Kennzeichnungswerte Ihren [Gebotseinheiten“ oder &#x200B;](/help/search-social-commerce/glossary.md#a-b) übergeordneten Kampagnen zuweisen. Sie können dann einen beliebigen Beschriftungswert als separate Spalte in Ihre Ansichten und Berichte aufnehmen und Ihre Berichte in verschiedene Klassifizierungsgruppen und -werte unterwerfen.

## Komponenten von Kennzeichnungsklassifizierungen

### Klassifizierungen kennzeichnen

Jeder Advertiser kann über bis zu 30 Label-Klassifizierungen verfügen, bei denen es sich um Kategorien der obersten Ebene handelt. Nachdem Sie eine Kennzeichnungsklassifizierung erstellt haben, können Sie bestimmte Kennzeichnungswerte für die Klassifizierung erstellen.

### Kennzeichnungswerte

Jede Kennzeichnungsklassifizierung kann bis zu 2.000 Werte aufweisen. Nachdem Sie bestimmte Kennzeichnungswerte für eine Klassifizierung erstellt haben, können Sie sie Kampagnen, Anzeigengruppen, Schlüsselwörtern, Anzeigen, Platzierungen und Produktgruppen (über [&#x200B; Kampagnenverwaltungsansichten oder &#x200B;](#classification-values-assign-campaign-management)mithilfe [&#x200B; Bulksheets) &#x200B;](#classification-values-assign-bulksheets).

Jede geeignete Entität kann Kennzeichnungswerte für mehrere Klassifizierungen, aber nur einen Kennzeichnungswert pro Klassifizierung haben. Kennzeichnungswerte werden von untergeordneten Entitäten übernommen, können jedoch überschrieben werden. Der Wert, der auf der niedrigsten Ebene zugewiesen wird, überschreibt immer die Werte, die auf den übergeordneten Ebenen zugewiesen werden.

## Die Ansicht Kennzeichnungen - Klassifizierungen

Die Ansicht [!UICONTROL Reports] > [!UICONTROL Labels Classifications] enthält [!UICONTROL Classifications] und [!UICONTROL Label Values] Unteransichten. Standardmäßig werden Daten für Ihre Kennzeichnungsklassifizierungen und -werte auf Schlüsselwortebene angezeigt, Sie können jedoch optional Daten für Ihre Klassifizierungen und Werte auf Anzeigenebene anzeigen.

## Verfügbare Aktionen

* Zeigen Sie Daten für Ihre Label-Klassifizierungen an.

* Zeigen Sie Daten für Ihre Kennzeichnungsklassifizierungswerte an.

* [Erstellen Sie eine Klassifizierung für die Bezeichnung](#classification-create).

* Weisen Sie den Kontokomponenten Klassifizierungswerte zu [aus Kampagnenverwaltungsansichten oder &#x200B;](#classification-values-assign-campaign-management)mithilfe [&#x200B; Bulksheets](#classification-values-assign-bulksheets).

* [Entfernen Sie Kennzeichnungswerte aus den &#x200B;](#classification-values-remove).

* [Löschen von Kennzeichnungswerten](#classification-values-delete).

* [Löschen von Kennzeichnungsklassifizierungen](#classification-delete).

## Erstellen einer Kennzeichnungsklassifizierung {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. Klicken Sie auf **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Create Classification]**.

1. Geben Sie einen eindeutigen Klassifizierungsnamen für die Bezeichnung ein und klicken Sie dann auf **[!UICONTROL Create]**.

   Der Name muss für das Advertiser-Konto eindeutig sein und aus [ASCII-Zeichen 32-126](https://www.asciitable.com/) bestehen. Die maximale Länge beträgt 27 Einzelbyte-Zeichen. Der Name darf nicht mit dem Namen einer vorhandenen Berichtsspalte oder einer vorhandenen Bulksheet-Spalte identisch sein. Siehe die Namen der Bulksheet-Spalten für [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), [Yahoo! Display Network](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md) und [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md).

## Zuweisen von Klassifizierungswerten zu Kontokomponenten aus den Ansichten des Kampagnen-Managements {#classification-values-assign-campaign-management}

Sie können Classification-Werte für die folgenden Suchentitäten aus den Kampagnen-Management-Ansichten zuweisen und entfernen: Kampagne, Anzeigengruppe, Keyword, Anzeige, Platzierung, Produktgruppe auf Einheitenebene und dynamische Suchzielgruppe. Bei Bedarf können Sie während des Zuweisungsprozesses Klassifizierungen und Klassifizierungswerte erstellen. Jede Kennzeichnungsklassifizierung kann bis zu 2.000 Werte aufweisen.

Jede Entität kann einen Bezeichnungswert pro Klassifizierung aufweisen. Beispielsweise kann „Schuhe_Kampagne“ den Farbwert „Rot“ und den Geowert „Los Angeles“ haben, aber es können nicht mehrere Werte für „Farbe“ oder „Geo“ sein.

Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die übernommenen Werte überschreiben.

>[!NOTE]
>
>Ihre Keywords und Werbetexte für einige Werbenetzwerke und Kampagnentypen sind [nicht veränderlich](/help/search-social-commerce/campaign-management/faqs-campaigns.md) was bedeutet, dass ihre Bearbeitung die vorhandene Entität löscht und eine neue erstellt. Wenn eine vorhandene Entität auf diese Weise gelöscht wird, wird die Bezeichnungsklassifizierung nicht der neuen Entität zugewiesen.

1. Öffnen Sie die Entitätsansicht über das Menü **[!UICONTROL Manage]** oder **[!UICONTROL Target]** .

1. Aktivieren Sie das Kontrollkästchen neben jeder relevanten Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Gehen Sie für jeden zutreffenden Classification-Wert wie folgt vor:

   1. Geben Sie in der Spalte **[!UICONTROL Classifications]** die Klassifizierung an:

      * Um eine vorhandene Klassifizierung zu verwenden, klicken Sie auf den Klassifizierungsnamen, um sie zu erweitern.

      * Um eine Klassifizierung zu erstellen, klicken Sie in der Spaltenüberschrift auf [!UICONTROL +] . Geben Sie im Eingabefeld den Klassifizierungsnamen ein und klicken Sie dann auf ![Speichern](/help/search-social-commerce/assets/save-checkmark.png "Speichern"), um die Klassifizierung sofort zu speichern. Um die neue Klassifizierung zu verwenden, klicken Sie auf den Klassifizierungsnamen, um sie zu erweitern.

        Der Name muss aus [ASCII-Zeichen 32-126](https://www.asciitable.com/) bestehen und die maximale Länge beträgt 27 Einzelbyte-Zeichen.

   1. Geben Sie in der Spalte **[!UICONTROL Value Name]** den Wert für die ausgewählte Klassifizierung an:

      * Um einen vorhandenen Wert zu verwenden, wählen Sie den Wert aus.

      * Um einen Wert zu erstellen, klicken Sie in der Spaltenüberschrift auf [!UICONTROL +] . Geben Sie im Eingabefeld den Wert ein und klicken Sie dann auf ![Speichern](/help/search-social-commerce/assets/save-checkmark.png "Speichern"), um den Wert sofort zu speichern und standardmäßig auszuwählen.

        Die maximale Länge beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

1. Klicken Sie auf **+[!UICONTROL Assign Now]**.

## Zuweisen von Klassifizierungswerten zu Kontokomponenten mithilfe von Bulksheets {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

Sie können Kennzeichnungsklassifizierungen mit Werten für die folgenden Suchentitäten mithilfe von Bulksheets verknüpfen: Kampagne, Anzeigengruppe, Keyword, Anzeige, Platzierung, Produktgruppe auf Einheitenebene und Ziel der dynamischen Suche. Jede Kennzeichnungsklassifizierung kann bis zu 2.000 Werte aufweisen.

Jede Entität kann einen Bezeichnungswert pro Klassifizierung aufweisen. Beispielsweise kann „Schuhe_Kampagne“ den Farbwert „Rot“ und den Geowert „Los Angeles“ haben, aber es können nicht mehrere Werte für „Farbe“ oder „Geo“ sein.

Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die übernommenen Werte überschreiben.

>[!NOTE]
>
>Ihre Keywords und Werbetexte für einige Werbenetzwerke und Kampagnentypen sind [nicht veränderlich](/help/search-social-commerce/campaign-management/faqs-campaigns.md) was bedeutet, dass ihre Bearbeitung die vorhandene Entität löscht und eine neue erstellt. Wenn eine vorhandene Entität auf diese Weise gelöscht wird, wird die Bezeichnungsklassifizierung nicht der neuen Entität zugewiesen.

1. [Eine Bulksheet herunterladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) die die Entitäten enthält, denen Sie Kennzeichnungsklassifizierungswerte zuweisen möchten:

   * Erweitern Sie auf der Registerkarte [!UICONTROL Rows and Columns] die [!UICONTROL Campaign] im [!UICONTROL Bulksheet Columns].

   * Erweitern Sie die [!UICONTROL Label Classification].

   * Wählen Sie jede Klassifizierung aus, für die Sie eine Spalte in die Bulksheet-Datei aufnehmen möchten.

     Wenn Sie beispielsweise die Kennzeichnungen „Farbe“ und „Geo“ einbeziehen, enthält das Bulksheet die Spalten „Farbe“ und „Geo“.

1. Öffnen Sie die Datei in einem Editor und fügen Sie den Titelklassifizierungsspalten Beschriftungswerte für die Entitäten hinzu, mit denen sie verknüpft werden sollen. Die maximale Länge für jeden Wert beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

   Siehe die Beispielwerte im nächsten Abschnitt.

   Neben dem Hinzufügen von Werten können Sie auch vorhandene Werte löschen, indem Sie sie aus den entsprechenden Zeilen entfernen. Um Werte sowohl aus einer übergeordneten Entität als auch aus ihren untergeordneten Entitäten zu entfernen, schließen Sie entweder a) nur die übergeordnete Entitätszeile ein und entfernen Sie den vorhandenen Klassifizierungswert, oder b) beziehen Sie sowohl die übergeordnete Entität als auch ihre untergeordneten Entitäten ein und entfernen Sie den vorhandenen Klassifizierungswert aus allen übergeordneten und untergeordneten Zeilen.

1. [Datei hochladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) um die Verknüpfungen zu erstellen.<!-- Update once the new bulksheet UI is GA -->

Die hochgeladenen Kennzeichnungswerte sind in den entsprechenden Entitätsansichten sichtbar.

### Beispiel für Kennzeichnungsklassifizierungswerte, die in Bulksheets hochgeladen werden sollen

Dieses Beispiel enthält Spalten für die Kennzeichnungsklassifizierungen „Farbe“ und „Geo“. Ersetzen Sie für Ihre eigenen Bulksheets Spalten durch Ihre eigenen Klassifizierungsnamen für Bezeichnungen.

| Konto | Campaign | Anzeigengruppe | Schlüsselwort | Anzeige | Platzierung | Bezeichnungen | Farbe | Geo |
|---|---|---|---|---|---|---|---|---|
| ACT1 | C1 | | | | | | Grün | |
| ACT1 | C1 | AG1 | | | | | | |
| ACT1 | C1 | AG1 | K1 | | | | | UK |
| ACT1 | C1 | AG1 | K2 | | | | Rot | AU |
| ACT1 | C1 | AG1 | K3 | | | | Blau | DE |
| ACT1 | C1 | AG1 | | A1 | | | | |
| ACT1 | C1 | AG1 | | A1 | | | Rot | |
| ACT1 | C1 | AG1 | | | P1 | | Rot | AU |
| ACT1 | C1 | AG1 | | | P2 | | Blau | DE |

## Entfernen von Kennzeichnungswerten aus Kontokomponenten {#classification-values-remove}

Das Entfernen eines Klassifizierungswerts entfernt die Verknüpfung mit der Kontokomponente und allen untergeordneten Komponenten. Berichtsdaten für den Classification-Wert sind für diese Komponenten nicht mehr verfügbar. Wenn Sie einen Klassifizierungswert entfernen, werden weder der Wert noch die Kontokomponenten gelöscht.

>[!NOTE]
>
>Informationen zum Löschen eines Werts aus einer Kennzeichnungsklassifizierung finden Sie unter [Löschen von Kennzeichnungsklassifizierungswerten](#classification-values-delete).

1. Öffnen Sie die Entitätsansicht über das Menü **[!UICONTROL Manage]** oder **[!UICONTROL Target]** .

1. Aktivieren Sie das Kontrollkästchen neben jeder relevanten Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Classification-Wert, der aus den ausgewählten Entitäten entfernt werden soll.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Um alle zugewiesenen Werte auszuwählen, klicken Sie auf **[!UICONTROL Select All]**. Um die Auswahl aller zugewiesenen Werte aufzuheben, klicken Sie auf **[!UICONTROL Deselect All]**.

1. Klicken Sie auf **[!UICONTROL Unassign Selected]**.

## Löschen von Kennzeichnungsklassifizierungswerten {#classification-values-delete}

Durch das Löschen von Kennzeichnungsklassifizierungswerten sind diese nicht mehr für die zukünftige Verwendung verfügbar und es sind keine Berichtsdaten für die Werte mehr verfügbar. Alle Zuweisungen zwischen den Werten und ihren übergeordneten Kennzeichnungsklassifizierungen und bestimmten Kontokomponenten werden entfernt, aber die übergeordneten Kennzeichnungsklassifizierungen und die Kampagnenkomponenten werden nicht gelöscht.

>[!NOTE]
>
>Um einfach einen Classification-Wert von einer Account-Komponente zu trennen, siehe &quot;[Entfernen von Label-Classification-Werten aus Account-Komponenten](#classification-values-remove)&quot;.

1. Klicken Sie auf **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Label Values]** .

1. (Optional) Filtern Sie die Liste, um bestimmte Kennzeichnungswerte einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben den einzelnen zu löschenden Kennzeichnungswerten.

   Sie können bis zu 200 Zeilen gleichzeitig löschen.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Löschen von Kennzeichnungsklassifizierungen

Durch das Löschen einer Klassifizierung werden alle Verknüpfungen zwischen ihren untergeordneten Werten und den Kontokomponenten entfernt. Eine gelöschte Klassifizierung und ihre Werte sind für die zukünftige Verwendung nicht verfügbar. Berichtsdaten für die Classification-Werte sind nicht mehr verfügbar.

>[!NOTE]
>
>Um einfach einen Classification-Wert von einer Account-Komponente zu trennen, siehe &quot;[Entfernen von Label-Classification-Werten aus Account-Komponenten](#classification-values-remove)&quot;.

1. Klicken Sie auf **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. (Optional) Filtern Sie die Liste, um bestimmte Kennzeichnungsklassifizierungen einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben jeder zu löschenden Kennzeichnungsklassifizierung.

   Sie können bis zu 200 Zeilen gleichzeitig löschen.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.
