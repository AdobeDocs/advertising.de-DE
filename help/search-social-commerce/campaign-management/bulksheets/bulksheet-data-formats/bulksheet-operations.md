---
title: Vorgänge, die Sie in Bulksheets ausführen können
description: Referenzieren allgemeiner Informationen zum Hinzufügen, Bearbeiten und Löschen von Kampagnendaten mithilfe von Bulksheets.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Vorgänge, die Sie in Bulksheets ausführen können

Sie können Kampagnendaten über Bulksheets für [unterstützte Werbenetzwerke](../bulksheet-about.md#bulksheet-functionality-by-network).

Fügen Sie für jede Kampagnenkomponente (Kampagne, Anzeigengruppe, Suchbegriff oder Textanzeige), die Sie hinzufügen, bearbeiten oder löschen möchten, eine separate Datenzeile ein. oder deren Eigenschaften Sie hinzufügen, bearbeiten oder löschen möchten. Wenn Sie z. B. eine Kampagne mit einer Anzeigengruppe, einem Keyword und einer Anzeige erstellen möchten - insgesamt vier Komponenten - benötigen Sie vier separate Datenzeilen. So bearbeiten Sie die [!UICONTROL Ad Group Name] für eine Anzeigengruppe (eine Komponente) benötigen Sie jedoch nur eine Zeile. Um vier verschiedene Eigenschaften für eine Anzeigengruppe (eine Komponente) zu bearbeiten, benötigen Sie ebenfalls nur eine Zeile.

Die folgenden Regeln gelten für die Arbeit mit Kampagnenkomponenten und deren Eigenschaften.

* Hinzufügen:

   * Um eine Komponente hinzuzufügen, schließen Sie alle Felder ein, die zum Hinzufügen dieser Komponente erforderlich sind, sowie optional Felder für die Eigenschaften der Komponente ein.

   * So fügen Sie eine Eigenschaft für eine vorhandene Komponente hinzu, z. B. die [!UICONTROL Ad Group End Date] für eine Anzeigengruppe alle Felder einschließen, die zum Bearbeiten dieser Komponente (Anzeigengruppe) erforderlich sind, sowie das Feld für die Eigenschaft ([!UICONTROL Ad Group End Date]).

* Um eine Eigenschaft für eine vorhandene Komponente zu bearbeiten, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, sowie das Feld für die Eigenschaft.

   Wenn Sie das Eigenschaftsfeld leer lassen, wird der vorhandene Wert beibehalten.

* Löschen:

   * Um eine vorhandene Komponente zu löschen, fügen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, und ändern Sie ihren Status in [!UICONTROL Deleted]. So löschen Sie beispielsweise eine [!DNL Google Ads] Anzeigengruppe, müssen Sie die [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] mit dem Wert <i>[!UICONTROL Deleted]</i>und [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2]und [!UICONTROL Param3] nur -Werte) So löschen Sie eine vorhandene [!DNL paramN] für einen Suchbegriff alle Felder einschließen, die zum Bearbeiten des Suchbegriffs erforderlich sind, und auch das vorhandene löschen [!DNL paramN] Wert durch Eingabe des Werts `[delete]` (einschließlich der Klammern) im entsprechenden Feld.

   * (Zulässige Eigenschaftsfelder) Um einen vorhandenen Eigenschaftswert für eine Komponente zu löschen, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, und löschen Sie auch den Eigenschaftswert, indem Sie den Wert eingeben. `[delete]` (einschließlich der Klammern). Zulässige Felder umfassen:

      * ([!UICONTROL Google Ads] nur) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] und [!DNL Microsoft® Advertising] nur) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Wenn Sie einen Wert in ein Feld einfügen, das nicht für die Aktion gilt, werden alle im Feld eingegebenen Werte ignoriert.

>[!MORELIKETHIS]
>
>* [Verwalten von Kampagnendaten mithilfe von Bulksheets](../bulksheet-about.md)
>* [Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)

