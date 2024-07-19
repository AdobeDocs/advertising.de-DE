---
title: '[!DNL Google Ads] Konversionsdaten'
description: Erfahren Sie mehr über die Typen der  [!DNL Google Ads] verfolgten Konversionsdaten, die in Search, Social und Commerce verfügbar sind.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# [!DNL Google Ads] Konversionsdaten in Search, Social und Commerce

Search, Social und Commerce synchronisieren automatisch [!DNL Google Ads]-verfolgte Konversionsdaten für alle Kampagnen in den [!DNL Google Ads] Such- und Einkaufsnetzwerken in Search, Social und Commerce, um Berichte und Optimierungen zu erstellen.

Alle Metriken stehen automatisch in Ihren Kampagnenverwaltungsansichten und Basisberichten zur Verfügung und stehen auch zur Optimierung in Portfoliozielen zur Verfügung.

## Verfügbare Konversionsdaten

Die Funktion &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;synchronisiert Daten für Konversionen, für die die Option &quot;[!DNL Include in 'Conversions']&quot;aktiviert ist. Dabei werden die Daten für die letzten 35 Tage abgerufen und dann Änderungen an den Daten täglich bis 09:00-10:00 in der Zeitzone des Advertisers abgerufen. Historische Daten können sich von Tag zu Tag ändern, da bei jedem Klick neue Konversionen verfolgt werden.

Bis zu drei Metriken für jede [[!DNL Google Ads]-verfolgte Konversion](https://support.google.com/google-ads/answer/4677036) (die Sie in [!DNL Google Ads] eingerichtet haben) sind automatisch in Search, Social und Commerce unter Verwendung der in [!DNL Google Ads] konfigurierten Konversionsnamen verfügbar. Zu den Metriken für jede Konversion gehören:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` - (Wenn Sie dies verfolgen) Der Konversionswert für den Suchbegriff, beginnend mit dem Präfix &quot;GGL&quot;(z. B. GGL-Kauf).

* `GGL_CT*` - Die Anzahl (Anzahl) der Konversionen, beginnend mit dem Präfix &quot;GGL_CT&quot;(z. B. GGL_CT_Purchase).

* `GGL_XD_CT*` - (Wenn für den Konvertierungstyp verfügbar, wenn Sie sie verfolgen) Die Anzahl (Anzahl) der geräteübergreifenden Konversionen, gemessen durch Google, beginnend mit dem Präfix &quot;GGL_XD_CT_&quot;(z. B. GGGL_XD_CT_Purchase).

[!DNL Google Ads] zeichnet jede Konversion nach [Angebotseinheit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klickdatum auf (nicht nach Konversionsdatum). Die Attribution basiert auf der standardmäßigen Zuordnungseinstellung für jede Metrik in [!DNL Google Ads]; die Adobe Advertising-Attribution ist nicht in berücksichtigt, da Daten auf Klickereignis-Ebene nicht verfügbar sind.

>[!NOTE]
>
>* Wenn Sie mehrere Konten mit denselben Konversionsnamen haben, werden möglicherweise doppelte Konversionsnamen im Adobe Advertising angezeigt. In diesem Fall ändern Sie [ den Anzeigenamen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) für eine der doppelten Metriken in [!UICONTROL Admin] > [!UICONTROL Conversions]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
>* Daten auf der Ebene der Angebotseinheit stimmen mit Daten in [!DNL Google Ads] auf derselben Ebene überein. Die eigenen Konversionsdaten von [!DNL Google Ads] für höhere Ebenen können jedoch zusätzliche Konversionen beinhalten, die nicht den untergeordneten Gebotseinheiten zugeordnet werden. Daten in Search, Social und Commerce werden immer auf der Ebene der Angebotseinheiten aggregiert, sodass beispielsweise ein Bericht auf Kampagnenebene möglicherweise nicht die gleichen Summen wie ein Bericht auf Kampagnenebene in Google Ads aufweist.
>* Datenabweichungen sind in der Regel nach der Morgensynchronisierung geringer als nach der Tageszeit, wenn noch keine zusätzlichen Konversionen synchronisiert wurden. Es wird empfohlen, die Daten morgens zu überprüfen.
>* Konversionsdaten sind nicht für [!DNL Google Display Network]-, [!DNL Gmail]-, [!DNL Mobile App]- und [!DNL YouTube]-Anzeigen verfügbar. Filtern Sie diese Arten von Anzeigen heraus, wenn Sie Daten in [!DNL Google Ads] mit Daten in Search, Social und Commerce vergleichen.
>* Daten für [!DNL Google Ads] -Konversionen sind nicht auf Zielgruppen- oder geografischer Standortebene verfügbar und werden daher nicht zur automatischen Optimierung der RLSA-Werte und der Ortsgebotsanpassungen verwendet.

## Vergleichen von Konversionsdaten in [!DNL Google Ads] mit Daten in Search, Social und Commerce

Wenn Sie Daten in Search, Social und Commerce mit denen in [!DNL Google Ads] vergleichen, verwenden Sie die Ansicht- oder Berichtsoption, um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

Verwenden Sie die folgenden Berichtseinstellungen, um vergleichbare Daten zu überprüfen.

### In [!DNL Google Ads] zu verwendende Berichtseinstellungen

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

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Report]**, halten Sie den Cursor über **[!UICONTROL Basic Reports]** und klicken Sie dann auf **[!UICONTROL Search Engine Account Report]**.

1. Geben Sie im Fenster [!UICONTROL Report Settings] die folgenden Berichtseinstellungen an:

   1. Wählen Sie im Abschnitt &quot;**[!UICONTROL Conversions Based]** on&quot;die Option &quot;**[!UICONTROL Click date]**&quot;.

   1. Geben Sie denselben Datumsbereich an, den Sie für den Bericht [!DNL Google Ads] verwendet haben.

   1. Wählen Sie im Abschnitt **[!UICONTROL Search/Content]** die Option **[!UICONTROL Search Only]** aus.

   1. Erweitern Sie im Abschnitt **[!UICONTROL Search Engine Hierarchy]** den Abschnitt [!UICONTROL Google Adwords] und wählen Sie das Konto aus.

   1. Öffnen Sie die Registerkarte [!UICONTROL Columns] und fügen Sie die Metriken [!DNL Google Ads] hinzu (beginnend mit &quot;GGL&quot;), die Sie vergleichen möchten.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen](campaign-implemention-overview.md)
>* [Überwachen und Verwalten der Leistung Ihrer Werbenetzwerk-Kampagnen](monitor-performance-campaigns.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Erstellen eines Konversions-Tags für  [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
