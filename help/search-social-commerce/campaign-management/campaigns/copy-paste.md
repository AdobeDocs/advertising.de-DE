---
title: Erstellen und Bearbeiten von Kampagnendaten in großen Mengen mithilfe von Kopieren und Einfügen
description: Erfahren Sie, wie Sie mit der Funktion zum Kopieren und Einfügen Kampagnendaten massenweise verwalten können.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Erstellen und Bearbeiten von Kampagnendaten in großen Mengen mithilfe von Kopieren und Einfügen

Nur *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] und bestehende [!DNL Baidu] Konten*

*[!UICONTROL Campaigns]-, [!UICONTROL Ad Groups]-, [!UICONTROL Keywords]- und [!UICONTROL Ads]*

Sie können bis zu 10.000 Zeilen aus den [!UICONTROL Campaigns]-, [!UICONTROL Ad Groups]-, [!UICONTROL Keywords]- und [!UICONTROL Ads] kopieren und in [!DNL Microsoft Excel] oder einen anderen Editor einfügen, um alle Nicht-ID-Felder zu bearbeiten. Sie können dann die [!DNL Excel] Zeilen kopieren und als tabulatorgetrennte Daten zurück in die Ansicht einfügen, um die Änderungen vorzunehmen. Die Funktion verwendet die Zwischenablage Ihres Computers.

Mit dieser Funktion können Sie vorhandene Kampagnenobjekte (mit ID-Feldern) bearbeiten und neue Kampagnenobjekte ohne ID-Felder erstellen.

## Datenzeilen kopieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, die Sie kopieren möchten.

   Sie können bis zu 10.000 Zeilen kopieren.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und dann auf **[!UICONTROL Copy]**.

   Alternativ können Sie den Tastaturbefehl „Kopieren“ Ihres Betriebssystems verwenden, z. B. **[!DNL Ctrl+C]** für [!DNL Microsoft Windows] oder **[!DNL Command-C]** für [!DNL Apple Mac].

1. Klicken Sie im Dialogfeld [!UICONTROL Copy to Clipboard] auf **[!UICONTROL Continue]**. Wenn die Daten kopierbereit sind, klicken Sie auf **[!UICONTROL Copy]**.

1. Einfügen der Zeilen in [!DNL Excel] oder einen anderen Editor.

## Datenzeilen bearbeiten und erstellen

1. Bearbeiten Sie die Daten entsprechend den folgenden Anforderungen:

   * Die eingefügten Daten müssen eine Kopfzeile und die erforderlichen Kampagnenobjektwerte enthalten. Weitere Informationen finden Sie in den erforderlichen Bulksheet-Spalten für [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Display Network](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Japan](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md) und [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). Die Spaltenreihenfolge spielt keine Rolle.

      * Bei vorhandenen Objekten, die Sie bearbeiten möchten, müssen Sie alle relevanten ID-Spalten, Entitätsnamen und das zu bearbeitende Attribut einbeziehen. Die numerische ID für das Objekt nicht bearbeiten.

      * Schließen Sie für neue Kampagnenobjekte alle relevanten Entitätsnamen und Attribute ein, jedoch keine Objekt-IDs (die automatisch generiert werden). Wenn Sie beispielsweise eine neue Anzeige erstellen, lassen Sie das Feld [!UICONTROL Ad ID] leer. Das Anzeigennetzwerk erstellt automatisch eine ID, wenn Sie das Objekt posten.

   * Der Wert in einer nicht erforderlichen Spalte kann null (leer) sein, aber jede Zeile muss dieselbe Anzahl tabulatorgetrennter Werte aufweisen.

1. Speichern Sie die Daten als tabulatorgetrennte Werte.

## Datenzeilen in die Kampagnenverwaltungsansichten einfügen

>[!NOTE]
>
>Wenn die eingefügten Zeilen Daten enthalten, die mit denen in den vorhandenen Entitäten identisch sind oder eine vorhandene Entität duplizieren, werden die doppelten Daten ignoriert.

1. Kopieren Sie in [!DNL Excel] oder einem anderen Editor die entsprechenden tabulatorgetrennten Zeilen.

1. Klicken Sie im Hauptmenü von Search, Social und Commerce auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Öffnen Sie die Ansicht, in die Sie Daten einfügen möchten (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und dann auf **[!UICONTROL Paste]**.

   Alternativ können Sie den Tastaturbefehl „Paste“ (Einfügen) Ihres Betriebssystems verwenden, z. B. **[!DNL Ctrl+V]** für [!DNL Microsoft Windows] oder **[!DNL Command-V]** für [!DNL Apple Mac].

1. Fügen Sie die Daten in das Eingabefeld ein, und klicken Sie dann auf **[!UICONTROL Process]**.

1. (Optional) Geben Sie zusätzliche Details ein:

   * (Wenn **[!UICONTROL Additional Details]** komprimiert ist) Klicken Sie auf ![Öffnen](/help/search-social-commerce/assets/chevron-up.png "Öffnen"), um die Details zu erweitern.

   * Geben Sie eine optionale **[!UICONTROL Job Name]** und/oder eine optionale **[!UICONTROL Job Description]** ein.

1. Klicken Sie auf **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Bearbeiten von Einstellungen direkt in einer Zeile](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Kampagnen verwalten](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Anzeigengruppen verwalten](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Schlüsselwörter verwalten](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Anzeigen verwalten](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
