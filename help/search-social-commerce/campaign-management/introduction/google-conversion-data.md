---
title: '''[!DNL Google Ads] Konversionsdaten"'
description: Erfahren Sie mehr über die Typen [!DNL Google Ads]-getrackte Konversionsdaten, die in Search, Social und Commerce verfügbar sind.
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# [!DNL Google Ads] Konversionsdaten in Search, Social und Commerce

Automatische Synchronisierung von Search, Social und Commerce [!DNL Google Ads]-getrackte Konversionsdaten für alle Kampagnen auf der [!DNL Google Ads] Suchen und Einkaufen von Netzwerken in Search, Social und Commerce für Reporting und Optimierung.

Alle Metriken stehen automatisch in Ihren Kampagnenverwaltungsansichten und Basisberichten zur Verfügung und stehen auch zur Optimierung in Portfoliozielen zur Verfügung.

## Verfügbare Konversionsdaten

In Search, Social und Commerce werden Daten für Konversionen synchronisiert, für die die[!DNL Include in 'Conversions']&quot; aktiviert ist, wobei die Daten für die letzten 35 Tage abgerufen und dann Änderungen an den Daten täglich bis 09 abgerufen werden.:00-10:00 in der Zeitzone des Werbetreibenden. Historische Daten können sich von Tag zu Tag ändern, da bei jedem Klick neue Konversionen verfolgt werden.

Bis zu drei Transaktionseigenschaften für jede [[!DNL Google Ads]-verfolgte Konversion](https://support.google.com/google-ads/answer/4677036) (die Sie in [!DNL Google Ads]) sind automatisch in Search, Social und Commerce verfügbar, wobei die Konversionsnamen verwendet werden, die in [!DNL Google Ads]. Zu den Transaktionseigenschaften für jede Konversion gehören:

* `GGL*` — (Wenn Sie dies verfolgen) Der Konversionswert für den Suchbegriff, beginnend mit dem Präfix &quot;GGL&quot;(z. B. GGL-Kauf).

* `GGL_CT*` — Die Anzahl (Anzahl) der Konversionen, beginnend mit dem Präfix &quot;GGL_CT&quot;(z. B. GGL_CT_Purchase).

* `GGL_XD_CT*` — (Wenn für den Konvertierungstyp verfügbar, wenn Sie sie verfolgen) Die Anzahl (Anzahl) der geräteübergreifenden Konversionen, gemessen von Google, beginnend mit dem Präfix &quot;GGL_XD_CT_&quot; (z. B. GGGL_XD_CT_Purchase).

[!DNL Google Ads] erfasst jede Konversion von [Bid-Unit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klicken auf Datum (nicht Konvertierungsdatum). Die Attribution basiert auf der standardmäßigen Attributionseinstellung für jede Metrik in [!DNL Google Ads]; Die Zuordnung von Adobe Advertisingen wird nicht berücksichtigt, da Klick-Daten auf Ereignisebene nicht verfügbar sind.

>[!NOTE]
>
>* Wenn Sie mehrere Konten mit denselben Konversionsnamen haben, werden möglicherweise doppelte Konversionsnamen in Adobe Advertising angezeigt. Tritt dies auf, [Anzeigenamen ändern](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) für eine der doppelten Metriken in [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
>* Daten auf der Ebene der Angebotseinheit stimmen mit den Daten in [!DNL Google Ads] auf derselben Ebene. Allerdings [!DNL Google Ads]Die eigenen Konversionsdaten für höhere Ebenen können zusätzliche Konversionen umfassen, die nicht den untergeordneten Gebotseinheiten zugeordnet werden. Daten in Search, Social und Commerce werden immer auf der Ebene der Angebotseinheiten aggregiert, sodass beispielsweise ein Bericht auf Kampagnenebene möglicherweise nicht die gleichen Summen wie ein Bericht auf Kampagnenebene in Google Ads aufweist.
>* Datenabweichungen sind in der Regel nach der Morgensynchronisierung geringer als nach der Tageszeit, wenn noch keine zusätzlichen Konversionen synchronisiert wurden. Es wird empfohlen, die Daten morgens zu überprüfen.
>* Konversionsdaten sind nicht verfügbar für [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], und [!DNL YouTube] Anzeigen. Filtern Sie diese Arten von Anzeigen heraus, wenn Sie Daten in [!DNL Google Ads] mit Daten in Search, Social und Commerce.
>* Daten für [!DNL Google Ads] Konversionen sind nicht auf Zielgruppen- oder geografischer Standortebene verfügbar und werden daher nicht zur automatischen Optimierung von RLSA und Ortsgebotsanpassungen verwendet.

## Vergleichen von Konversionsdaten in [!DNL Google Ads] mit Daten in Search, Social und Commerce

Wenn Sie Daten in Search, Social &amp; Commerce mit denen in [!DNL Google Ads]verwenden Sie die Ansicht- oder Berichtsoption, um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

Verwenden Sie die folgenden Berichtseinstellungen, um vergleichbare Daten zu überprüfen.

### Berichtseinstellungen zur Verwendung in [!DNL Google Ads]

Erstellen Sie den Bericht für die ausgewählten Konversionsaktionen nach Tag und fügen Sie Daten für alle Anzeigenstatus ein.

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### Berichtseinstellungen für die Verwendung in Search, Social und Commerce

Verwenden Sie in Search, Social und Commerce die Ansicht- oder Berichtsoption, um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Report]** halten Sie den Cursor darüber. **[!UICONTROL Basic Reports]** und klicken Sie anschließend auf **[!UICONTROL Search Engine Account Report]**.

1. Im [!UICONTROL Report Settings] -Fenster die folgenden Berichtseinstellungen festlegen:

   1. Im **[!UICONTROL Conversions Based]** Wählen Sie im Bereich **[!UICONTROL Click date]**.

   1. Geben Sie denselben Datumsbereich an, den Sie für die [!DNL Google Ads] Bericht.

   1. Im **[!UICONTROL Search/Content]** Bereich, wählen Sie **[!UICONTROL Search Only]**.

   1. Im **[!UICONTROL Search Engine Hierarchy]** -Abschnitt, erweitern Sie die [!UICONTROL Google Adwords] und wählen Sie das Konto aus.

   1. Öffnen Sie die [!UICONTROL Columns] und fügen Sie die [!DNL Google Ads] Metriken (beginnend mit &quot;GGL&quot;), die Sie vergleichen möchten.

1. Klicken **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen](campaign-implemention-overview.md)
>* [Überwachen und verwalten Sie die Leistung Ihrer Werbenetzwerk-Kampagnen.](monitor-performance-campaigns.md)
>* [Anzeigen der für einen Advertiser verfolgten Transaktionseigenschaften](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
