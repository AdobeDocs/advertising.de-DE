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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] und vorhandene [!DNL Baidu] Konten nur*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] Ansichten*

Sie können bis zu 10.000 Zeilen aus den Ansichten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] kopieren und in [!DNL Microsoft Excel] oder einen anderen Editor einfügen, um Nicht-ID-Felder zu bearbeiten. Anschließend können Sie die [!DNL Excel] -Zeilen kopieren und sie als tabulatorgetrennte Daten wieder in die Ansicht einfügen, um die Änderungen vorzunehmen. Die Funktion verwendet die Zwischenablage Ihres Computers.

Mit dieser Funktion können Sie vorhandene Kampagnenobjekte (mit ID-Feldern) bearbeiten und neue Kampagnenobjekte ohne ID-Felder erstellen.

## Datenzeilen kopieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, die Sie kopieren möchten.

   Sie können bis zu 10.000 Zeilen kopieren.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und klicken Sie dann auf **[!UICONTROL Copy]**.

   Alternativ können Sie den Tastaturbefehl Ihres Betriebssystems &quot;Kopieren&quot;verwenden, z. B. **[!DNL Ctrl+C]** für [!DNL Microsoft Windows] oder **[!DNL Command-C]** für [!DNL Apple Mac].

1. Klicken Sie im Dialogfeld [!UICONTROL Copy to Clipboard] auf **[!UICONTROL Continue]**. Wenn die Daten kopiert werden können, klicken Sie auf &quot;**[!UICONTROL Copy]**&quot;.

1. Fügen Sie die Zeilen in [!DNL Excel] oder einen anderen Editor ein.

## Datenzeilen bearbeiten und erstellen

1. Bearbeiten Sie die Daten gemäß den folgenden Anforderungen:

   * Die eingefügten Daten müssen eine Kopfzeile und die erforderlichen Kampagnenobjektwerte enthalten. Siehe die erforderlichen Bulksheet-Spalten für [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Display Network](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Japan](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md) und [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). Die Spaltenreihenfolge spielt keine Rolle.

      * Bei vorhandenen Objekten, die Sie bearbeiten möchten, müssen Sie alle relevanten ID-Spalten, Entitätsnamen und das zu bearbeitende Attribut einschließen. Bearbeiten Sie nicht die numerische ID für das Objekt.

      * Schließen Sie bei neuen Kampagnenobjekten alle relevanten Entitätsnamen und Attribute ein, jedoch keine Objekt-IDs (die automatisch generiert werden). Wenn Sie beispielsweise eine neue Anzeige erstellen, lassen Sie das Feld [!UICONTROL Ad ID] leer. Das Werbenetzwerk erstellt beim Posten des Objekts automatisch eine ID.

   * Der Wert in einer nicht erforderlichen Spalte kann null (leer) sein, aber jede Zeile muss über dieselbe Anzahl von tabulatorgetrennten Werten verfügen.

1. Speichern Sie die Daten als tabulatorgetrennte Werte.

## Fügen Sie Datenzeilen in die Kampagnenverwaltungsansichten ein.

>[!NOTE]
>
>Wenn die eingefügten Zeilen Daten enthalten, die mit denen der vorhandenen Entitäten identisch sind oder eine vorhandene Entität duplizieren, werden die doppelten Daten ignoriert.

1. Kopieren Sie in [!DNL Excel] oder einem anderen Editor die entsprechenden tabulatorgetrennten Zeilen.

1. Klicken Sie im Hauptmenü von Search, Social und Commerce auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Öffnen Sie die Ansicht, in die Daten eingefügt werden sollen (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und klicken Sie dann auf **[!UICONTROL Paste]**.

   Alternativ können Sie den Tastaturbefehl Ihres Betriebssystems &quot;Einfügen&quot;verwenden, z. B. **[!DNL Ctrl+V]** für [!DNL Microsoft Windows] oder **[!DNL Command-V]** für [!DNL Apple Mac].

1. Fügen Sie die Daten in das Eingabefeld ein und klicken Sie dann auf **[!UICONTROL Process]**.

1. (Optional) Geben Sie zusätzliche Details ein:

   * (Wenn **[!UICONTROL Additional Details]** komprimiert ist) Klicken Sie auf ![Öffnen](/help/search-social-commerce/assets/chevron-up.png "Öffnen") , um die Details zu erweitern.

   * Geben Sie optional **[!UICONTROL Job Name]** und/oder optional **[!UICONTROL Job Description]** ein.

1. Klicken Sie auf **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Einstellungen direkt in einer Zeile bearbeiten](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Verwalten von Kampagnen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Verwalten von Anzeigengruppen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Suchbegriffe verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Anzeigen verwalten](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
