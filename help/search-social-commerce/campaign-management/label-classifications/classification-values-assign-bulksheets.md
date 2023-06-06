---
title: Zuweisen von Classification-Werten zu Kontokomponenten mithilfe von Bulksheets
description: Erfahren Sie, wie Sie mit Bulksheets Classification-Werte zu Kontokomponenten zuweisen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 7%

---

# Zuweisen von Classification-Werten zu Kontokomponenten mithilfe von Bulksheets

Sie können Beschriftungsklassifizierungen mithilfe von Bulksheets mit Werten für die folgenden Suchentitäten verknüpfen: Kampagne, Anzeigengruppe, Keyword, Anzeige, Platzierung, Produktgruppe auf Einheitsebene und dynamisches Suchziel. Jede Beschriftungsklassifizierung kann bis zu 2000 Werte aufweisen.

Jede Entität kann einen Beschriftungswert pro Classification haben. Shoes_Campaign kann beispielsweise den Farbwert &quot;red&quot;und den Geo-Wert &quot;Los Angeles&quot;haben, aber nicht mehrere Werte für Color oder Geo.

Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die vererbten Werte überschreiben.

>[!NOTE]
>
>Ihre Suchbegriffe und Werbetexte für einige Werbenetzwerke und Kampagnentypen sind [nicht veränderlich](/help/search-social-commerce/campaign-management/faqs-campaigns.md), was bedeutet, dass die Bearbeitung dieser Elemente die vorhandene Entität löscht und eine neue erstellt. Wenn eine vorhandene Entität auf diese Weise gelöscht wird, wird die Titel-Classification der neuen Entität nicht zugewiesen.

1. [Bulksheet herunterladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) enthält die Entitäten, denen Sie Beschriftungs-Classification-Werte zuweisen möchten:

   * Im [!UICONTROL Rows and Columns] Registerkarte, erweitern Sie die [!UICONTROL Campaign] in der [!UICONTROL Bulksheet Columns] -Bereich.

   * Erweitern Sie die [!UICONTROL Label Classification] Liste.

   * Wählen Sie jede Classification aus, für die Sie eine Spalte in die Bulksheet-Datei aufnehmen möchten.

      Wenn Sie beispielsweise die Beschriftungsklassifizierungen &quot;Farbe&quot;und &quot;Geo&quot;einschließen, enthält das Bulksheet die Spalten &quot;Farbe&quot;und &quot;Geo&quot;.

1. Öffnen Sie die Datei in einem Editor und fügen Sie den Beschriftungsklassifizierungsspalten Beschriftungswerte für die Entitäten hinzu, mit denen sie verknüpft werden sollen. Die maximale Länge pro Wert beträgt 100 Zeichen. Sie kann ASCII- und Nicht-ASCII-Zeichen enthalten.

   Siehe die Beispielwerte im nächsten Abschnitt.

   Sie können nicht nur Werte hinzufügen, sondern auch vorhandene Werte löschen, indem Sie sie aus den entsprechenden Zeilen entfernen. Um Werte aus einer übergeordneten Entität und ihren untergeordneten Entitäten zu entfernen, schließen Sie entweder a) nur die Zeile der übergeordneten Entität ein und entfernen Sie den vorhandenen Classification-Wert oder b) schließen Sie sowohl die übergeordnete Entität als auch ihre untergeordneten Entitäten ein und entfernen Sie den vorhandenen Classification-Wert aus allen übergeordneten und untergeordneten Zeilen.

1. [Datei hochladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) , um die Verknüpfungen zu erstellen.

Die hochgeladenen Beschriftungswerte sind in den relevanten Entitätsansichten sichtbar.

## Beispiel für Beschriftungs-Classification-Werte, die in Bulksheets hochgeladen werden sollen

Dieses Beispiel enthält Spalten für Beschriftungsklassifizierungen &quot;Farbe&quot;und &quot;Geo&quot;. Ersetzen Sie für Ihre eigenen Bulksheets Spalten durch Ihre eigenen Titel-Classification-Namen.

| Konto | Kampagne | Anzeigengruppe | Schlüsselwort | Anzeige | Platzierung | Bezeichnungen | Farbe | Geo |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 |  |  |  |  |  | Grün |  |
| Acct1 | C1 | AG1 |  |  |  |  |  |  |
| Acct1 | C1 | AG1 | K1 |  |  |  |  | Vereinigtes Königreich |
| Acct1 | C1 | AG1 | K2 |  |  |  | Rot | AU |
| Acct1 | C1 | AG1 | K3 |  |  |  | Blau | DE |
| Acct1 | C1 | AG1 |  | A1 |  |  |  |  |
| Acct1 | C1 | AG1 |  | A1 |  |  | Rot |  |
| Acct1 | C1 | AG1 |  |  | P1 |  | Rot | AU |
| Acct1 | C1 | AG1 |  |  | P2 |  | Blau | DE |

>[!MORELIKETHIS]
>
>* [Über Beschriftungsklassifizierungen](classification-about.md)
>* [Erstellen einer Bezeichnungsklassifizierung](classification-create.md)
>* [Zuweisen von Classification-Werten zu Kontokomponenten aus Kampagnenverwaltungsansichten](classification-values-assign-campaign-management.md)
>* [Entfernen von Beschriftungs-Classification-Werten aus Kontokomponenten](classification-values-remove.md)
>* [Löschen von Bezeichnungsklassifizierungswerten](classification-values-delete.md)
>* [Beschriftungsklassifizierungen löschen](classification-delete.md)

