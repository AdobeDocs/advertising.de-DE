---
title: Nur [!DNL Naver] Tracking-Konten implementieren
description: Erfahren Sie, wie Sie Tracking-Kampagnen für Ihre  [!DNL Naver]  einrichten, damit Sie die Leistung der Anzeigen, die Sie direkt im Anzeigennetzwerk kaufen, verfolgen, in Berichten erfassen und visualisieren können.
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Implementieren [!DNL Naver] Nur-Tracking-Konten

Nur *[!DNL Naver]Konten*

Sie können Tracking-Kampagnen für Ihre [!DNL Naver]-Konten erstellen, damit Sie die Leistung der Anzeigen, die Sie direkt über das Werbenetzwerk kaufen, verfolgen, Berichte dazu erstellen und visualisieren können. Search, Social und Commerce synchronisiert keine Daten mit dem Werbenetzwerk, lädt automatisch Tracking hoch und gibt keine Gebote für das Konto ab.

Tracking-Kampagnen replizieren Ihre vorhandenen Kampagnen, Anzeigengruppen und Keywords. Nachdem Sie die Kontostruktur in Search, Social und Commerce erstellt und das Tracking zu den ursprünglichen Kampagnen im Anzeigennetzwerk hinzugefügt haben, können Sie tägliche Netzwerk-Traffic-Metriken für Ihre Keywords oder Anzeigen hochladen. Search, Social und Commerce können dann Ihre Konversionen Ihren Anzeigen und Keywords zuordnen.

Sie können Leistungsmetriken für all Ihre Kampagnen und für jede einzelne Kampagne, Anzeigengruppe oder jedes Keyword/jede einzelne Anzeige verfolgen. Sie können Informationen dazu auch in den meisten Basis-, Erweitert- und Assist-Berichten zusammen mit Daten für Ihre anderen Werbenetzwerke aufnehmen. Der Export von Metriken nach Adobe Analytics wird nicht unterstützt, aber Search, Social und Commerce können [Metriken, die Sie verfolgen,  [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) Search, Social und Commerce synchronisieren.

>[!NOTE]
>
>Es ist nicht möglich, einem Portfolio Tracking-Kampagnen zur Optimierung hinzuzufügen.

1. Erstellen Sie Tracking-Kampagnen in Search, Social und Commerce:

   1. Erstellen [Dummy-Netzwerkkontodetails](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Wenn Sie mehrere Konten in einem einzigen Werbenetzwerk haben, konsolidieren Sie sie in der [!UICONTROL Accounts] in einem Konto.

      [!DNL Naver] bietet keine API-Unterstützung zum Hochladen von Tracking-Parametern in das Werbenetzwerk. Sie können jedoch Tracking-Parameter mithilfe von Bulksheets generieren und manuell innerhalb des Werbenetzwerks hinzufügen (gemäß Schritt 2). Zum Generieren der Tracking-Parameter müssen Sie die Tracking-Methode &quot;[!UICONTROL EF Redirect]&quot; verwenden. Sie können optional beliebige Append-Parameter hinzufügen.

      Search, Social und Commerce schließen den `ev_cl={ef_uniqueid}` automatisch in alle Tracking-URLs ein, die in Bulksheets für das Konto generiert werden. Diese eindeutige ID wird verwendet, um die Kampagnendaten mit den hochgeladenen Kosten und Klickdaten abzugleichen.

   1. Richten Sie Kampagnen ein, um Folgendes zu verfolgen:

      1. Erstellen Sie innerhalb des Werbenetzwerks eine Bulksheet-Datei mit allen Entitäten und den erforderlichen übergeordneten Entitäten, die von Search, Social und Commerce für das Konto verfolgt werden sollen.

         Sie können Daten zu Schlüsselwörtern einbeziehen, einschließlich der übergeordneten Kampagnen und Anzeigengruppen.

      1. Bearbeiten Sie bei Bedarf die Bulksheet-Datei so, dass sie dem Format für Suche, Social und Commerce [Bulksheets erforderlich für [!DNL Naver] Accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md) folgt.

      1. Laden Sie in Search, Social und Commerce [Bulksheet-Datei hoch](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Hinweis: Search, Social und Commerce senden die Daten nicht an das Anzeigennetzwerkkonto.

1. Einrichten des Trackings für die Kampagnen:

   1. Wählen Sie in Search, Social und Commerce [eine neue Bulksheet-Datei herunterladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) indem Sie die Option auf &quot;[!UICONTROL Generate Tracking URLs]&quot; verwenden.

   Durch die Verwendung der Option &quot;[!UICONTROL Generate Tracking URLs]&quot; wird das [!UICONTROL Destination URL] für jedes Keyword mit dem Tracking-Code für Search, Social und Commerce gefüllt, der dem [!UICONTROL Base URL] vorangestellt ist.

   Im Folgenden finden Sie ein Beispiel für die Ziel-URL mit -Tracking:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Kopieren Sie die [!UICONTROL Destination URL] Werte in der heruntergeladenen Bulksheet-Datei in die relevanten Keyword-Einstellungen im Netzwerk.

      Sie können die URLs zu den entsprechenden Entitäten hinzufügen, indem Sie die Datei im Editor des Anzeigennetzwerks in das Netzwerk hochladen. In diesem Fall müssen Sie je nach den Datenanforderungen des Netzwerks möglicherweise einige Spalten entfernen. Andernfalls müssen Sie die URLs manuell im Netzwerk eingeben.

1. Laden Sie regelmäßig Klick- und Kostendaten herunter, die täglich aus dem Anzeigennetzwerk für die Keywords oder Markenanzeigen auf Anzeigengruppenebene aggregiert werden, die Sie nachverfolgen, und [laden Sie die Klick- und Kostendaten &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) „Suche“, „Social“ und &quot;Commerce&quot; im [&#x200B; Format &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Schließen Sie die vollständige Kontenhierarchie und alle Metriken ein, die Sie einbeziehen möchten. Search, Social und Commerce stimmen die hochgeladenen Daten mit den Daten in bestehenden Kampagnen überein.

1. (Optional) Wenn Sie auf Ihren Web-Seiten Service-Tags des Adobe Advertising-Konversionsverfolgungs-Services verwenden, um Konversionen zu verfolgen, die nicht im Werbenetzwerk verfolgt werden, senden Sie Feed-Dateien mit täglich aggregierten Konversionsdaten, um sie zu Ihren Tracking-Kampagnen hinzuzufügen.

   Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Alle hochgeladenen Tracking-Daten sind in den Ansichten [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] und [!UICONTROL Keywords] unter [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] verfügbar. Er ist auch für Berichte in der [!UICONTROL Insights & Reports] verfügbar.

>[!MORELIKETHIS]
>
>* [Anhang - Erforderliche Bulksheet-Daten für  [!DNL Naver] Konten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Traffic- und Konversionsmetriken für  [!DNL Naver] -Tracking-Konten hochladen](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Anforderungen an Metrikdaten für  [!DNL Naver] -Nur-Tracking-Konten](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Klick-Tracking-Formate für [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
