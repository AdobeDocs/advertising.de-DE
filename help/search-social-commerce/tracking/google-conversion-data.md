---
title: Konvertierungsdaten [!DNL Google Ads]
description: Erfahren Sie mehr über die Arten von Konversionsdaten mit [!DNL Google Ads]-Tracking, die in Search, Social und Commerce verfügbar sind.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
TQID: 'https://experienceleague.adobe.com/7qqQKfVhueHMc7hJDEac86la9dp36hwtrLF5ikxJzJM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
    internal-label: Conversions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%
---
# [!DNL Google Ads] von Konversionsdaten in Search, Social und Commerce

Search, Social und Commerce synchronisieren automatisch [!DNL Google Ads] Konversionsdaten für alle Kampagnen in den [!DNL Google Ads] Such- und Shopping-Netzwerken in Search, Social und Commerce, um Berichte zu erstellen und zu optimieren.

Alle Metriken sind automatisch in Ihren Kampagnenverwaltungsansichten und Basisberichten verfügbar und können auch zur Optimierung in Portfoliozielen verwendet werden.

## Verfügbare Konversionsdaten

Search, Social und Commerce synchronisieren Daten für Konversionen, für die die Option &quot;[!DNL Include in 'Conversions']&quot; aktiviert ist. Dabei werden die Daten der letzten 35 Tage abgerufen und anschließend die Änderungen an den Daten täglich um 09:00-10:00 Uhr in der Zeitzone des Werbetreibenden abgerufen. Historische Daten können sich von Tag zu Tag ändern, da neue Konversionen für jeden Klick verfolgt werden.

Bis zu drei Metriken für jede [[!DNL Google Ads]-getrackte Konversion](https://support.google.com/google-ads/answer/4677036) (die Sie in [!DNL Google Ads] eingerichtet haben) sind automatisch in Search, Social und Commerce verfügbar und verwenden die in [!DNL Google Ads] konfigurierten Konversionsnamen. Zu den Metriken für jede Konversion gehören:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (Wenn Sie es verfolgen) Der Konversionswert für das Keyword, beginnend mit dem Präfix „GGL“ (z. B. GGL Purchase).

* `GGL_CT*` - Die Anzahl (Anzahl) der Konversionen, beginnend mit dem Präfix „GGL_CT“ (z. B. GGL_CT_Purchase).

* `GGL_XD_CT*` - (wenn für den Konversionstyp verfügbar, wenn Sie ihn verfolgen) Die Anzahl (Anzahl) geräteübergreifender Konversionen, wie von Google gemessen, beginnend mit dem Präfix „GGL_XD_CT_“ (z. B. GGL_XD_CT_Purchase).

[!DNL Google Ads] zeichnet jede Konvertierung nach [Gebotseinheit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klickdatum (nicht Konvertierungsdatum) auf. Die Attribution basiert auf der standardmäßigen Attributionseinstellung für jede Metrik in [!DNL Google Ads]. Die Adobe Advertising-Attribution wird nicht berücksichtigt, da keine Daten auf Klick-Ereignisebene verfügbar sind.

>[!NOTE]
>
>* Wenn Sie mehrere Konten mit denselben Konversionsnamen haben, werden in Adobe Advertising möglicherweise doppelte Konversionsnamen angezeigt. Wenn dies auftritt, [ändern Sie den Anzeigenamen](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#change-the-display-name-for-a-conversion-metric) für eine der doppelten Metriken unter [!UICONTROL Goals] > [!UICONTROL Conversions]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
>* Daten auf der Ebene der Gebotseinheit stimmen mit Daten in [!DNL Google Ads] auf derselben Ebene überein. Die eigenen Konversionsdaten von [!DNL Google Ads] für höhere Ebenen können jedoch zusätzliche Konversionen enthalten, die nicht den untergeordneten Bid-Einheiten zugeordnet werden. Daten in Search, Social und Commerce werden immer ab der Ebene der Gebotseinheiten aggregiert, sodass beispielsweise ein Bericht auf Kampagnenebene nicht dieselben Summen wie ein Bericht auf Kampagnenebene in Google Ads hat.
>* Die Datenvarianz ist in der Regel nach der morgendlichen Synchronisierung geringer als nach der späteren am Tag, wenn zusätzliche Konversionen noch nicht synchronisiert wurden. Es wird empfohlen, die Daten morgens zu validieren.
>* Konversionsdaten sind für [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App] und [!DNL YouTube] Anzeigen nicht verfügbar. Filtern Sie diese Arten von Anzeigen heraus, wenn Sie Daten in [!DNL Google Ads] mit Daten in Search, Social und Commerce vergleichen.
>* Daten für [!DNL Google Ads] Konversionen sind weder auf der Zielgruppen- noch auf der geografischen Standortebene verfügbar und werden daher nicht zur automatischen Optimierung von RLSA- und Standortangebotsanpassungen verwendet.

## Vergleichen von Konversionsdaten in [!DNL Google Ads] mit Daten in Search, Social und Commerce

Wenn Sie Daten in Search, Social und Commerce mit denen in [!DNL Google Ads] vergleichen, verwenden Sie die Option Anzeigen oder Bericht , um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

Verwenden Sie die folgenden Berichtseinstellungen, um vergleichbare Daten zu validieren.

### In [!DNL Google Ads] zu verwendende Berichtseinstellungen

Generieren Sie den Bericht für die ausgewählten Konversionsaktionen nach Tag und schließen Sie Daten für alle Anzeigenstatus ein.

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

### In Search, Social und Commerce zu verwendende Berichteinstellungen

Verwenden Sie in Search, Social und Commerce die Option Anzeigen oder Bericht , um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Klicken Sie auf **[!UICONTROL Create Report]**, klicken Sie im linken Bereich auf **[!UICONTROL Basic Reports]**, und wählen Sie dann **[!UICONTROL Search Engine Account Report]** aus. Klicken Sie auf **[!UICONTROL Proceed]**.

1. Öffnen Sie im [!UICONTROL Create Report] die Registerkarte **[!UICONTROL Basic Settings]** und geben Sie die folgenden [Berichteinstellungen](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md) an:

   1. Legen Sie **[!UICONTROL Data Aggregation]** auf **[!UICONTROL Daily]** fest.

   1. Legen Sie **[!UICONTROL Conversions Based on]** auf **[!UICONTROL Click date]** fest.

   1. Geben Sie denselben Datumsbereich an, den Sie für den [!DNL Google Ads] Bericht verwendet haben.

   1. Legen Sie **[!UICONTROL Search/Content]** auf **[!UICONTROL Search Only]** fest.

   1. Wenn **[!UICONTROL Filter By]** angezeigt wird, wählen Sie **[!UICONTROL Search engine]** aus.

   1. Erweitern Sie in **[!UICONTROL Search Engine Hierarchy]** [!DNL Google Ads] und aktivieren Sie das Kontrollkästchen neben dem Konto, das Sie vergleichen möchten. Klicken Sie auf **[!UICONTROL Add selected items]** , um das Konto in **[!UICONTROL Selected Filters]** zu verschieben.

1. Öffnen Sie die Registerkarte **[!UICONTROL Columns]** und fügen Sie die [!DNL Google Ads] Metriken (beginnend mit „GGL„) hinzu, die Sie vergleichen möchten.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Einrichten von Netzwerkkonten und Kampagnen für Werbeanzeigen](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Über die Verwaltung von Kampagnen und Portfolios](/help/search-social-commerce/manage/manage-about.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#view-the-conversion-metrics-tracked-for-an-advertiser)
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konversionen](/help/search-social-commerce/goals/conversions/conversions-upload-offline-enhanced-conversions.md)
