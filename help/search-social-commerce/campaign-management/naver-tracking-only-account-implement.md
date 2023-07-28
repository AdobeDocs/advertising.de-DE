---
title: Implementierung [!DNL Naver] Nur-Tracking-Konten
description: Erfahren Sie, wie Sie Tracking-Kampagnen für Ihre [!DNL Naver] Konten, damit Sie die Leistung der Anzeigen, die Sie direkt über das Werbenetzwerk kaufen, verfolgen, in Berichte aufnehmen und visualisieren können.
exl-id: 8013d4e8-0b4f-41a7-9c1b-10c55349930f
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Implementierung [!DNL Naver] Nur-Tracking-Konten

*[!DNL Naver]Nur Konten*

Sie können Tracking-Kampagnen für Ihre [!DNL Naver] Konten, damit Sie die Leistung der Anzeigen, die Sie direkt über das Werbenetzwerk kaufen, verfolgen, in Berichte aufnehmen und visualisieren können. Search, Social und Commerce synchronisiert keine Daten mit dem Anzeigennetzwerk, lädt automatisch Tracking hoch und platziert keine Angebote für das Konto.

Tracking-Kampagnen replizieren Ihre vorhandenen Kampagnen, Anzeigengruppen und Suchbegriffe. Nachdem Sie die Kontostruktur in Search, Social und Commerce erstellt und den ursprünglichen Kampagnen im Werbenetzwerk Tracking hinzugefügt haben, können Sie tägliche Metriken zum Netzwerk-Traffic für Ihre Suchbegriffe oder Anzeigen hochladen. Search, Social und Commerce können Ihre Konversionen dann Ihren Anzeigen und Suchbegriffen zuordnen.

Sie können Leistungsmetriken für alle Ihre Kampagnen und für jede einzelne Kampagne, Anzeigengruppe oder Keyword/Anzeige verfolgen. Sie können auch Informationen zu ihnen in die grundlegendsten, erweiterten und unterstützenden Berichte sowie Daten für Ihre anderen Werbenetzwerke aufnehmen. Der Export der Metriken in Adobe Analytics wird nicht unterstützt, Search, Social und Commerce können jedoch synchronisiert werden. [Metriken, die Sie verfolgen in [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) in Search, Social und Commerce.

>[!NOTE]
>
>Sie können einem Portfolio keine Tracking-Kampagnen zur Optimierung hinzufügen.

1. Erstellen von Tracking-Kampagnen in Search, Social und Commerce:

   1. Erstellen [Details zum Platzhalter-Netzwerkkonto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Wenn Sie über mehrere Konten in einem Werbenetzwerk verfügen, konsolidieren Sie sie in einem Konto im [!UICONTROL Accounts] anzeigen.

      [!DNL Naver] bietet keine API-Unterstützung zum Hochladen von Tracking-Parametern in das Werbenetzwerk. Sie können jedoch Tracking-Parameter mithilfe von Bulksheets generieren und manuell im Werbenetzwerk hinzufügen (Schritt 2). Um die Tracking-Parameter zu generieren, müssen Sie die Variable[!UICONTROL EF Redirect]&quot;Tracking-Methode. Sie können optional alle gewünschten Anlagenparameter hinzufügen.

      Search, Social und Commerce enthält automatisch den Parameter . `ev_cl={ef_uniqueid}` in allen Tracking-URLs, die es in Bulksheets für das Konto generiert. Diese eindeutige ID wird verwendet, um die Kampagnendaten mit den von Ihnen hochgeladenen Kosten- und Klickdaten abzugleichen.

   1. Richten Sie Kampagnen zur Verfolgung ein:

      1. Erstellen Sie im Werbenetzwerk eine Bulksheet-Datei, die alle Entitäten und deren erforderliche übergeordnete Entitäten enthält, die von Search, Social und Commerce für das Konto verfolgt werden sollen.

         Sie können Daten über Suchbegriffe einbeziehen, einschließlich der übergeordneten Kampagnen und Anzeigengruppen.

      1. Bearbeiten Sie bei Bedarf die Bulksheet-Datei, sodass sie der Suche, Social und Commerce folgt. [Bulksheet-Format für [!DNL Naver] Konten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. In Search, Social und Commerce, [Bulksheet-Datei hochladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Hinweis: Search, Social und Commerce sendet die Daten nicht an das Anzeigennetzwerkkonto.

1. Richten Sie das Tracking für die Kampagnen ein:

   1. In Search, Social und Commerce, [eine neue Bulksheet-Datei herunterladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) Verwendung der Option &quot;[!UICONTROL Generate Tracking URLs].&quot;

   Verwenden von &quot;[!UICONTROL Generate Tracking URLs]&quot; füllt die Option [!UICONTROL Destination URL] für jeden Suchbegriff ein, wobei dem Trackingcode für Suche, Social und Commerce vorangestellt wird. [!UICONTROL Base URL] -Wert.

   Im Folgenden finden Sie ein Beispiel für die Ziel-URL mit Tracking:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Kopieren Sie die [!UICONTROL Destination URL] -Werte in der heruntergeladenen Bulksheet-Datei in die entsprechenden Suchbegriffeinstellungen im Netzwerk.

      Sie können die URLs zu den relevanten Entitäten hinzufügen, indem Sie die Datei im Editor des Werbenetzwerks in das Netzwerk hochladen. In diesem Fall müssen Sie möglicherweise einige Spalten entsprechend den Datenanforderungen des Netzwerks entfernen. Andernfalls müssen Sie die URLs manuell im Netzwerk eingeben.

1. Laden Sie regelmäßig Klick- und Kostendaten herunter, die täglich aus dem Werbenetzwerk für die von Ihnen verfolgten Suchbegriffe oder Markenanzeigen auf Anzeigengruppenebene aggregiert werden, und [Klicks- und Kostendaten hochladen](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) nach &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;im [erforderliches Format](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Schließen Sie die gesamte Kontohierarchie und alle Metriken ein, die Sie einbeziehen möchten. In &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;werden die hochgeladenen Daten mit den Daten in vorhandenen Kampagnen abgeglichen.

1. (Optional) Wenn Sie die Tags des Adobe Advertising-Konversions-Trackingdienstes auf Ihren Webseiten verwenden, um Konversionen zu verfolgen, die nicht im Werbenetzwerk verfolgt werden, senden Sie Feed-Dateien mit täglich aggregierten Konversionsdaten, um sie zu Ihren Tracking-Kampagnen hinzuzufügen.

   Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Alle hochgeladenen Tracking-Daten sind verfügbar über [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] innerhalb der [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups], und [!UICONTROL Keywords] Ansichten. Sie ist auch für Berichte im [!UICONTROL Insights & Reports] anzeigen.

>[!MORELIKETHIS]
>
>* [Anhang - Erforderliche Bulksheet-Daten für [!DNL Naver] Konten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Hochladen von Traffic- und Konversionsmetriken für [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Anforderungen an Metrikdaten für [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Klick-Tracking-Formate für [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
