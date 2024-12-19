---
title: Zuweisen von Klassifizierungswerten zu Kontokomponenten mithilfe von Bulksheets
description: Erfahren Sie, wie Sie mit Bulksheets Klassifizierungswerte zu Kontokomponenten zuweisen können.
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Zuweisen von Klassifizierungswerten zu Kontokomponenten mithilfe von Bulksheets

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

1. [Datei hochladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) um die Verknüpfungen zu erstellen.

Die hochgeladenen Kennzeichnungswerte sind in den entsprechenden Entitätsansichten sichtbar.

## Beispiel für Kennzeichnungsklassifizierungswerte, die in Bulksheets hochgeladen werden sollen

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

>[!MORELIKETHIS]
>
>* [Über Klassifizierungen von Kennzeichnungen](classification-about.md)
>* [Erstellen einer Kennzeichnungsklassifizierung](classification-create.md)
>* [Zuweisen von Klassifizierungswerten zu Kontokomponenten aus den Ansichten des Kampagnen-Managements](classification-values-assign-campaign-management.md)
>* [Entfernen Sie Kennzeichnungswerte aus den Kontokomponenten](classification-values-remove.md)
>* [Löschen von Kennzeichnungswerten](classification-values-delete.md)
>* [Löschen von Kennzeichnungsklassifizierungen](classification-delete.md)
