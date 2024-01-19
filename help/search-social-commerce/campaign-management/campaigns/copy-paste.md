---
title: Erstellen und Bearbeiten von Kampagnendaten stapelweise durch Kopieren und Einfügen
description: Erfahren Sie, wie Sie mit der Funktion zum Kopieren und Einfügen Kampagnendaten stapelweise verwalten können.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Erstellen und Bearbeiten von Kampagnendaten stapelweise durch Kopieren und Einfügen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex]und vorhandene [!DNL Baidu] Nur Konten*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] views*

Sie können bis zu 10.000 Zeilen aus dem [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Ansichten anzeigen und sie in [!DNL Microsoft Excel] oder einen anderen Editor zum Bearbeiten von Nicht-ID-Feldern verwenden. Sie können dann die [!DNL Excel] und fügen Sie sie als tabulatorgetrennte Daten wieder in die Ansicht ein, um die Änderungen vorzunehmen. Die Funktion verwendet die Zwischenablage Ihres Computers.

Mit dieser Funktion können Sie vorhandene Kampagnenobjekte (mit ID-Feldern) bearbeiten und neue Kampagnenobjekte ohne ID-Felder erstellen.

## Datenzeilen kopieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, die Sie kopieren möchten.

   Sie können bis zu 10.000 Zeilen kopieren.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr")und klicken Sie anschließend auf **[!UICONTROL Copy]**.

   Alternativ können Sie den Tastaturbefehl &quot;Kopieren&quot;Ihres Betriebssystems verwenden, z. B. **[!DNL Ctrl+C]** für [!DNL Microsoft Windows] oder **[!DNL Command-C]** für [!DNL Apple Mac].

1. Im [!UICONTROL Copy to Clipboard] dialog, klicken Sie **[!UICONTROL Continue]**. Wenn die Daten kopiert werden können, klicken Sie auf **[!UICONTROL Copy]**.

1. Fügen Sie die Zeilen in [!DNL Excel] oder einem anderen Editor.

## Datenzeilen bearbeiten und erstellen

1. Bearbeiten Sie die Daten gemäß den folgenden Anforderungen:

   * Die eingefügten Daten müssen eine Kopfzeile und die erforderlichen Kampagnenobjektwerte enthalten. Siehe die erforderlichen Bulksheet-Spalten für [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft-Werbung](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Netzwerk anzeigen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Japan](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), und [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). Die Spaltenreihenfolge spielt keine Rolle.

      * Bei vorhandenen Objekten, die Sie bearbeiten möchten, müssen Sie alle relevanten ID-Spalten, Entitätsnamen und das zu bearbeitende Attribut einschließen. Bearbeiten Sie nicht die numerische ID für das Objekt.

      * Schließen Sie bei neuen Kampagnenobjekten alle relevanten Entitätsnamen und Attribute ein, jedoch keine Objekt-IDs (die automatisch generiert werden). Wenn Sie beispielsweise eine neue Anzeige erstellen, lassen Sie die [!UICONTROL Ad ID] Feld leer. Das Werbenetzwerk erstellt beim Posten des Objekts automatisch eine ID.

   * Der Wert in einer nicht erforderlichen Spalte kann null (leer) sein, aber jede Zeile muss über dieselbe Anzahl von tabulatorgetrennten Werten verfügen.

1. Speichern Sie die Daten als tabulatorgetrennte Werte.

## Fügen Sie Datenzeilen in die Kampagnenverwaltungsansichten ein.

>[!NOTE]
>
>Wenn die eingefügten Zeilen Daten enthalten, die mit denen der vorhandenen Entitäten identisch sind oder eine vorhandene Entität duplizieren, werden die doppelten Daten ignoriert.

1. In [!DNL Excel] oder anderen Editor die entsprechenden tabulatorgetrennten Zeilen kopieren.

1. Klicken Sie im Hauptmenü &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Öffnen Sie die Ansicht, in die die Daten eingefügt werden sollen (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr")und klicken Sie anschließend auf **[!UICONTROL Paste]**.

   Alternativ können Sie den Tastaturbefehl &quot;Einfügen&quot;Ihres Betriebssystems verwenden, z. B. **[!DNL Ctrl+V]** für [!DNL Microsoft Windows] oder **[!DNL Command-V]** für [!DNL Apple Mac].

1. Fügen Sie die Daten in das Eingabefeld ein und klicken Sie auf **[!UICONTROL Process]**.

1. (Optional) Geben Sie zusätzliche Details ein:

   * (If **[!UICONTROL Additional Details]** ist komprimiert) Klicken ![Öffnen](/help/search-social-commerce/assets/chevron-up.png "Öffnen") , um die Details zu erweitern.

   * Optionale Eingabe **[!UICONTROL Job Name]** und/oder optional **[!UICONTROL Job Description]**.

1. Klicks **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Verwalten von Kampagnendaten mithilfe von Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Einstellungen direkt in einer Zeile bearbeiten](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Verwalten von Kampagnen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Verwalten von Anzeigengruppen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Anzeigen verwalten](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
