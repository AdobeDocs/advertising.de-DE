---
title: Implementieren von Nur-Tracking-Konten [!DNL Naver]
description: Erfahren Sie, wie Sie Tracking-Kampagnen für Ihre [!DNL Naver] Konten einrichten, damit Sie die Leistung der Anzeigen, die Sie direkt im Werbenetzwerk kaufen, verfolgen, melden und visualisieren können.
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Implementieren von Nur-Tracking-Konten mit [!DNL Naver]

*[!DNL Naver]nur Konten*

Sie können Tracking-Kampagnen für Ihre [!DNL Naver] -Konten erstellen, damit Sie die Leistung der Anzeigen, die Sie direkt über das Werbenetzwerk kaufen, verfolgen, in Berichten darstellen und visualisieren können. Search, Social und Commerce synchronisieren keine Daten mit dem Anzeigennetzwerk, laden automatisch Tracking hoch und platzieren keine Angebote für das Konto.

Tracking-Kampagnen replizieren Ihre vorhandenen Kampagnen, Anzeigengruppen und Suchbegriffe. Nachdem Sie die Kontostruktur in Search, Social und Commerce erstellt und den ursprünglichen Kampagnen im Werbenetzwerk Tracking hinzugefügt haben, können Sie tägliche Metriken zum Netzwerk-Traffic für Ihre Suchbegriffe oder Anzeigen hochladen. Search, Social und Commerce können Ihre Konversionen dann Ihren Anzeigen und Suchbegriffen zuordnen.

Sie können Leistungsmetriken für alle Ihre Kampagnen und für jede einzelne Kampagne, Anzeigengruppe oder Keyword/Anzeige verfolgen. Sie können auch Informationen zu ihnen in die grundlegendsten, erweiterten und unterstützenden Berichte sowie Daten für Ihre anderen Werbenetzwerke aufnehmen. Der Export der Metriken in Adobe Analytics wird nicht unterstützt, Search, Social und Commerce können jedoch [Metriken, die Sie in  [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) verfolgen, mit Search, Social und Commerce synchronisieren.

>[!NOTE]
>
>Sie können einem Portfolio keine Tracking-Kampagnen zur Optimierung hinzufügen.

1. Erstellen von Tracking-Kampagnen in Search, Social und Commerce:

   1. Erstellen Sie [Details zum Platzhalter-Netzwerkkonto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Wenn Sie mehrere Konten in einem Werbenetzwerk haben, konsolidieren Sie sie in der Ansicht [!UICONTROL Accounts] in einem Konto.

      [!DNL Naver] bietet keine API-Unterstützung zum Hochladen von Tracking-Parametern in das Werbenetzwerk. Sie können jedoch Tracking-Parameter mithilfe von Bulksheets generieren und manuell im Werbenetzwerk hinzufügen (Schritt 2). Um die Tracking-Parameter zu generieren, müssen Sie die Tracking-Methode &quot;[!UICONTROL EF Redirect]&quot; verwenden. Sie können optional alle gewünschten Anlagenparameter hinzufügen.

      In Search, Social und Commerce wird der Parameter `ev_cl={ef_uniqueid}` automatisch in alle Tracking-URLs eingefügt, die in Bulksheets für das Konto generiert werden. Diese eindeutige ID wird verwendet, um die Kampagnendaten mit den von Ihnen hochgeladenen Kosten- und Klickdaten abzugleichen.

   1. Richten Sie Kampagnen zur Verfolgung ein:

      1. Erstellen Sie im Werbenetzwerk eine Bulksheet-Datei, die alle Entitäten und deren erforderliche übergeordnete Entitäten enthält, die von Search, Social und Commerce für das Konto verfolgt werden sollen.

         Sie können Daten über Suchbegriffe einbeziehen, einschließlich der übergeordneten Kampagnen und Anzeigengruppen.

      1. Bearbeiten Sie bei Bedarf die Bulksheet-Datei, sodass sie dem für  [!DNL Naver] Konten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md) erforderlichen Bulksheet-Format &quot;Search, Social, &amp; Commerce [entspricht.

      1. Laden Sie in Search, Social und Commerce die Bulksheet-Datei ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) hoch.[

         >[!NOTE]
         >
         >Hinweis: Search, Social und Commerce veröffentlichen die Daten nicht im Anzeigennetzwerkkonto.

1. Richten Sie das Tracking für die Kampagnen ein:

   1. Laden Sie in Search, Social und Commerce [eine neue Bulksheet-Datei](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) mit der Option &quot;[!UICONTROL Generate Tracking URLs]&quot;herunter.

   Mit der Option &quot;[!UICONTROL Generate Tracking URLs]&quot; wird das Feld [!UICONTROL Destination URL] für jeden Suchbegriff mit dem Trackingcode für Suche, Social und Commerce gefüllt, dem der Wert [!UICONTROL Base URL] vorangestellt ist.

   Im Folgenden finden Sie ein Beispiel für die Ziel-URL mit Tracking:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Kopieren Sie die [!UICONTROL Destination URL] -Werte in der heruntergeladenen Bulksheet-Datei in die entsprechenden Suchbegriffeinstellungen im Netzwerk.

      Sie können die URLs zu den relevanten Entitäten hinzufügen, indem Sie die Datei im Editor des Werbenetzwerks in das Netzwerk hochladen. In diesem Fall müssen Sie möglicherweise einige Spalten entsprechend den Datenanforderungen des Netzwerks entfernen. Andernfalls müssen Sie die URLs manuell im Netzwerk eingeben.

1. Laden Sie regelmäßig Klick- und Kostendaten herunter, die täglich aus dem Werbenetzwerk für die von Ihnen verfolgten Suchbegriffe oder Markenanzeigen auf Anzeigengruppenebene aggregiert werden, und laden Sie dann [die Klick- und Kostendaten hoch](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) in Search, Social und Commerce im erforderlichen Format.[](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)

   Schließen Sie die gesamte Kontohierarchie und alle Metriken ein, die Sie einbeziehen möchten. In &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;werden die hochgeladenen Daten mit den Daten in bestehenden Kampagnen abgeglichen.

1. (Optional) Wenn Sie die Tags des Adobe Advertising-Konversions-Trackingdienstes auf Ihren Webseiten verwenden, um Konversionen zu verfolgen, die nicht im Werbenetzwerk verfolgt werden, senden Sie Feed-Dateien mit täglich aggregierten Konversionsdaten, um sie zu Ihren Tracking-Kampagnen hinzuzufügen.

   Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Alle hochgeladenen Tracking-Daten sind in den Ansichten [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] und [!UICONTROL Keywords] von [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] verfügbar. Sie ist auch für Berichte in der Ansicht [!UICONTROL Insights & Reports] verfügbar.

>[!MORELIKETHIS]
>
>* [Anhang - Erforderliche Bulksheet-Daten für [!DNL Naver] Konten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Hochladen von Traffic- und Konversionsmetriken für  [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Metrikdatenanforderungen für  [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Klick-Tracking-Formate für  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
