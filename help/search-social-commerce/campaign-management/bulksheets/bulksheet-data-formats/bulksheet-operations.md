---
title: Vorgänge, die Sie in Bulksheets ausführen können
description: Verweisen Sie auf allgemeine Informationen zum Hinzufügen, Bearbeiten und Löschen von Kampagnendaten mithilfe von Bulksheets.
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Vorgänge, die Sie in Bulksheets ausführen können

Sie können Kampagnendaten über Bulksheets für (unterstützte Werbenetzwerke[ hinzufügen, bearbeiten und ](../bulksheet-about.md#bulksheet-functionality-by-network).

Fügen Sie für jede Kampagnenkomponente (Kampagne, Anzeigengruppe, Keyword oder Textanzeige), die Sie hinzufügen, bearbeiten oder löschen möchten oder deren Eigenschaften Sie hinzufügen, bearbeiten oder löschen möchten, eine separate Datenzeile ein. Wenn Sie beispielsweise eine Kampagne mit einer Anzeigengruppe, einem Keyword und einer Anzeige erstellen möchten - insgesamt vier Komponenten -, benötigen Sie vier separate Datenzeilen. Um die [!UICONTROL Ad Group Name] für eine Anzeigengruppe (eine Komponente) zu bearbeiten, benötigen Sie jedoch nur eine Zeile. Um vier verschiedene Eigenschaften für eine Anzeigengruppe (eine Komponente) zu bearbeiten, benötigen Sie nur eine Zeile.

Die folgenden Regeln gelten für das Arbeiten mit Kampagnenkomponenten und deren Eigenschaften.

* Wird hinzugefügt:

   * Um eine Komponente hinzuzufügen, schließen Sie alle Felder ein, die erforderlich sind, um diese Komponente hinzuzufügen, sowie optional Felder für jede der Komponenteneigenschaften.

   * Um eine Eigenschaft für eine vorhandene Komponente hinzuzufügen, z. B. den [!UICONTROL Ad Group End Date] für eine Anzeigengruppe, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente (Anzeigengruppe) erforderlich sind, sowie das Feld für die Eigenschaft ([!UICONTROL Ad Group End Date]).

* Um eine Eigenschaft für eine vorhandene Komponente zu bearbeiten, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, sowie das Feld für die Eigenschaft.

  Wenn Sie das Eigenschaftsfeld leer lassen, wird der vorhandene Wert beibehalten.

* wird gelöscht:

   * Um eine vorhandene Komponente zu löschen, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, und ändern Sie ihren Status in [!UICONTROL Deleted]. Um beispielsweise eine [!DNL Google Ads] Anzeigengruppe zu löschen, müssen Sie die [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] mit dem Wert <i>[!UICONTROL Deleted]</i> und [!UICONTROL Ad Group ID] einbeziehen.

   * (Nur [!UICONTROL Param1]-, [!UICONTROL Param2]- und [!UICONTROL Param3]) Um einen vorhandenen [!DNL paramN] für ein Keyword zu löschen, schließen Sie alle Felder ein, die zum Bearbeiten des Keywords erforderlich sind, und löschen Sie auch den vorhandenen [!DNL paramN], indem Sie den `[delete]` (einschließlich der Klammern) in das entsprechende Feld eingeben.

   * (Zulässige Eigenschaftsfelder) Um einen vorhandenen Eigenschaftswert für eine Komponente zu löschen, schließen Sie alle Felder ein, die zum Bearbeiten dieser Komponente erforderlich sind, und löschen Sie den Eigenschaftswert auch, indem Sie den `[delete]` (einschließlich der Klammern) eingeben. Zulässige Felder umfassen:

      * (Nur [!UICONTROL Google Ads]) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * (Nur [!DNL Google Ads] und [!DNL Microsoft Advertising]) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Wenn Sie einen Wert in ein Feld einbeziehen, das nicht für die Aktion gilt, werden alle in das Feld eingegebenen Werte ignoriert.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](../bulksheet-about.md)
>* [Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
