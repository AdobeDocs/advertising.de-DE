---
title: Konvertierungsdaten [!DNL Google Ads]
description: Erfahren Sie mehr über die Typen von  [!DNL Google Ads]-getrackten Konversionsdaten, die in Search, Social und Commerce verfügbar sind.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '661'
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

[!DNL Google Ads] zeichnet jede Konvertierung nach [Gebotseinheit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klickdatum (nicht Konvertierungsdatum) auf. Die Attribution basiert auf der standardmäßigen Attributionseinstellung für jede Metrik in [!DNL Google Ads]. Die Adobe Advertising-Attribution wird nicht berücksichtigt, da keine Daten auf Klickereignis-Ebene verfügbar sind.

>[!NOTE]
>
>* Wenn Sie mehrere Konten mit denselben Konversionsnamen haben, werden möglicherweise doppelte Konversionsnamen in Adobe Advertising angezeigt. Wenn dies auftritt, [ändern Sie den Anzeigenamen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) für eine der doppelten Metriken unter [!UICONTROL Admin] > [!UICONTROL Conversions]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
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

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Report]**, halten Sie den Cursor über **[!UICONTROL Basic Reports]** und klicken Sie dann auf **[!UICONTROL Search Engine Account Report]**.

1. Geben Sie im [!UICONTROL Report Settings] die folgenden Berichteinstellungen an:

   1. Wählen Sie im Abschnitt **[!UICONTROL Conversions Based]** auf die Option **[!UICONTROL Click date]**.

   1. Geben Sie denselben Datumsbereich an, den Sie für den [!DNL Google Ads] Bericht verwendet haben.

   1. Wählen Sie im **[!UICONTROL Search/Content]** Abschnitt **[!UICONTROL Search Only]** aus.

   1. Erweitern Sie im Abschnitt **[!UICONTROL Search Engine Hierarchy]** den Abschnitt [!UICONTROL Google Adwords] und wählen Sie das Konto aus.

   1. Öffnen Sie die Registerkarte [!UICONTROL Columns] und fügen Sie die [!DNL Google Ads] Metriken (beginnend mit „GGL„) hinzu, die Sie vergleichen möchten.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Konten und Kampagnen des Werbenetzwerks](campaign-implemention-overview.md)
>* [Überwachen und Verwalten der Leistung Ihrer Werbenetzwerk-Kampagnen](monitor-performance-campaigns.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Erstellen eines Konvertierungs-Tags für [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konversionen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
