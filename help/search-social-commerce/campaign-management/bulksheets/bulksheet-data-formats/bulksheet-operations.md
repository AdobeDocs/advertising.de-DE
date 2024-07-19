---
title: Vorgänge, die Sie in Bulksheets ausführen können
description: Referenzieren allgemeiner Informationen zum Hinzufügen, Bearbeiten und Löschen von Kampagnendaten mithilfe von Bulksheets.
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Vorgänge, die Sie in Bulksheets ausführen können

Sie können Kampagnendaten über Bulksheets für [unterstützte Werbenetzwerke](../bulksheet-about.md#bulksheet-functionality-by-network) hinzufügen, bearbeiten und löschen.

Fügen Sie für jede Kampagnenkomponente (Kampagne, Anzeigengruppe, Suchbegriff oder Textanzeige), die Sie hinzufügen, bearbeiten oder löschen möchten oder deren Eigenschaften Sie hinzufügen, bearbeiten oder löschen möchten, eine separate Datenzeile ein. Wenn Sie z. B. eine Kampagne mit einer Anzeigengruppe, einem Keyword und einer Anzeige erstellen möchten - insgesamt vier Komponenten - benötigen Sie vier separate Datenzeilen. Um die [!UICONTROL Ad Group Name] für eine Anzeigengruppe (eine Komponente) zu bearbeiten, benötigen Sie jedoch nur eine Zeile. Um vier verschiedene Eigenschaften für eine Anzeigengruppe (eine Komponente) zu bearbeiten, benötigen Sie ebenfalls nur eine Zeile.

Die folgenden Regeln gelten für die Arbeit mit Kampagnenkomponenten und deren Eigenschaften.

* Hinzufügen:

   * Um eine Komponente hinzuzufügen, schließen Sie alle Felder ein, die zum Hinzufügen dieser Komponente erforderlich sind, sowie optional Felder für die Eigenschaften der Komponente ein.

   * Um eine Eigenschaft für eine vorhandene Komponente hinzuzufügen, z. B. [!UICONTROL Ad Group End Date] für eine Anzeigengruppe, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente (Anzeigengruppe) erforderlich sind, sowie das Feld für die Eigenschaft ([!UICONTROL Ad Group End Date]).

* Um eine Eigenschaft für eine vorhandene Komponente zu bearbeiten, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, sowie das Feld für die Eigenschaft.

  Wenn Sie das Eigenschaftsfeld leer lassen, wird der vorhandene Wert beibehalten.

* Löschen:

   * Um eine vorhandene Komponente zu löschen, fügen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, und ändern Sie ihren Status in [!UICONTROL Deleted]. Um beispielsweise eine Anzeigengruppe [!DNL Google Ads] zu löschen, müssen Sie die Werte [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] mit den Werten <i>[!UICONTROL Deleted]</i> und [!UICONTROL Ad Group ID] einbeziehen.

   * ([!UICONTROL Param1], [!UICONTROL Param2] und [!UICONTROL Param3] -Werte) Um einen vorhandenen [!DNL paramN] -Wert für einen Suchbegriff zu löschen, schließen Sie alle Felder ein, die zum Bearbeiten des Suchbegriffs erforderlich sind, und löschen Sie auch den vorhandenen [!DNL paramN] -Wert, indem Sie den Wert `[delete]` (einschließlich der Klammern) in das entsprechende Feld eingeben.

   * (Zulässige Eigenschaftsfelder) Um einen vorhandenen Eigenschaftswert für eine Komponente zu löschen, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, und löschen Sie auch den Eigenschaftswert, indem Sie den Wert `[delete]` eingeben (einschließlich der Klammern). Zulässige Felder umfassen:

      * ([!UICONTROL Google Ads] only) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] und nur [!DNL Microsoft Advertising]) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Wenn Sie einen Wert in ein Feld einfügen, das nicht für die Aktion gilt, werden alle im Feld eingegebenen Werte ignoriert.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](../bulksheet-about.md)
>* [Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Herunterladen/Erstellen einer Bulksheet-Datei](../bulksheet-download.md)
