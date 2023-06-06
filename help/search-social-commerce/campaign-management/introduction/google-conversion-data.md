---
title: "[!DNL Google Ads] Konversionsdaten"
description: Erfahren Sie mehr über die Typen [!DNL Google Ads]-getrackte Konversionsdaten, die in Search, Social und Commerce verfügbar sind.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] Konversionsdaten in Search, Social und Commerce

Automatische Synchronisierung von Search, Social und Commerce [!DNL Google Ads]-getrackte Konversionsdaten für alle Kampagnen auf der [!DNL Google Ads] Suchen und Einkaufen von Netzwerken in Search, Social und Commerce zur Berichterstellung und Optimierung. Search, Social und Commerce synchronisiert Daten für Konversionen, für die die[!DNL Include in 'Conversions']&quot; aktiviert ist, wobei die Daten für die letzten 30 Tage abgerufen und dann täglich Änderungen an den Daten abgerufen werden.

## Verfügbare Konversionsdaten

Bis zu drei Transaktionseigenschaften für jede [[!DNL Google Ads]-verfolgte Konversion](https://support.google.com/google-ads/answer/4677036) (die Sie in [!DNL Google Ads]) sind automatisch in Search, Social und Commerce verfügbar, wobei die Konversionsnamen verwendet werden, die in [!DNL Google Ads]. Zu den Transaktionseigenschaften für jede Konversion gehören:

* `GGL*` — (Wenn Sie es verfolgen) Die Summe der Konversionswerte für den Suchbegriff, beginnend mit dem Präfix &quot;GGL&quot;(z. B. GGL-Kauf).

* `GGL_CT*` — Die Anzahl (Anzahl) der Konversionen, beginnend mit dem Präfix &quot;GGL_CT&quot;(z. B. GGL_CT_Purchase).

* `GGL_XD_CT*` — (Wenn für den Konvertierungstyp verfügbar, wenn Sie sie verfolgen) Die Anzahl (Anzahl) der geräteübergreifenden Konversionen, gemessen von Google, beginnend mit dem Präfix &quot;GGL_XD_CT_&quot; (z. B. GGGL_XD_CT_Purchase).

Daten sind ab dem Datum verfügbar, an dem die Funktion für das Konto aktiviert wurde, und werden täglich um 9 Uhr aktualisiert:00-10:00 in der Zeitzone des Werbetreibenden.

[!DNL Google Ads] erfasst jede Konversion von [Bid-Unit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klicken auf Datum (nicht Konvertierungsdatum). Die Attribution basiert auf der standardmäßigen Attributionseinstellung für jede Metrik in [!DNL Google Ads]; Die Attribution der Adobe-Werbung ist nicht berücksichtigt, da Klick-Daten auf Ereignisebene nicht verfügbar sind. Jeden Tag ruft Search, Social und Commerce Konversionsdaten aus den letzten 30 Tagen ab und berechnet dann alle inkrementellen Konversionen seit dem Vortag unter Verwendung des Klickdatums aus [!DNL Google Ads] und die Angabe des vorherigen Tages als Transaktionsdatum. Daher können sich historische Daten von Tag zu Tag ändern, wenn bei jedem Klick neue Konversionen verfolgt werden. Wenn Sie Daten in Search, Social &amp; Commerce mit denen in [!DNL Google Ads], verwenden Sie die Ansicht- oder Berichtsoption, um &quot;[!UICONTROL Conversions by: Click date]&quot; (nicht nach Transaktionsdatum).

Alle Metriken stehen automatisch in Ihren Kampagnenverwaltungsansichten und Basisberichten zur Verfügung und stehen auch zur Optimierung in Portfoliozielen zur Verfügung.

>[!NOTE]
>
>* Wenn Sie mehrere Konten mit denselben Konversionsnamen haben, werden in der Adobe Advertising möglicherweise doppelte Konversionsnamen angezeigt. Tritt dies auf, [Anzeigenamen ändern](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) für eine der doppelten Metriken in [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
>* Daten auf der Ebene der Angebotseinheit stimmen mit den Daten in [!DNL Google Ads] auf derselben Ebene. Allerdings [!DNL Google Ads]Die eigenen Konversionsdaten für höhere Ebenen können zusätzliche Konversionen umfassen, die nicht den untergeordneten Gebotseinheiten zugeordnet werden. Daten in Search, Social und Commerce werden immer auf der Ebene der Angebotseinheiten aggregiert, sodass beispielsweise ein Bericht auf Kampagnenebene möglicherweise nicht die gleichen Summen wie ein Bericht auf Kampagnenebene in Google Ads aufweist.
>* Datenabweichungen sind in der Regel nach der Morgensynchronisierung geringer als nach der Tageszeit, wenn noch keine zusätzlichen Konversionen synchronisiert wurden. Es wird empfohlen, die Daten morgens zu überprüfen.
>* Konversionsdaten sind nicht verfügbar für [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App]und [!DNL YouTube] Anzeigen. Filtern Sie diese Arten von Anzeigen heraus, wenn Sie Daten in [!DNL Google Ads] mit Daten in Search, Social und Commerce.
>* Daten für [!DNL Google Ads] Konversionen sind nicht auf Zielgruppen- oder geografischer Standortebene verfügbar und werden daher nicht zur automatischen Optimierung von RLSA und Ortsgebotsanpassungen verwendet.


## Vergleichen von Konversionsdaten in [!DNL Google Ads] mit Daten in Search, Social und Commerce

Verwenden Sie die folgenden Berichtseinstellungen, um vergleichbare Daten zu überprüfen.

### Berichtseinstellungen zur Verwendung in [!DNL Google Ads]

1. Wählen Sie in der Symbolleiste die Option **[!DNL Reports]>[!DNL Report]**.

1. Auswählen **[!DNL + Custom]>[!DNL Table]**.

1. Geben Sie im linken Bereich die Zeilen und Spalten im Bericht an:

   1. Suchen Sie nach **[!DNL Day]** und ziehen Sie es auf [!DNL Row] Abschnitt.

   1. Suchen Sie nach **[!DNL All conv].** und ziehen Sie es auf [!DNL Column] Abschnitt.

   1. Suchen Sie nach **[!DNL Conversion action]** und ziehen Sie es auf [!DNL Column] Abschnitt.

1. Wählen Sie in der Symbolleiste Berichtseinstellungen die Option **[!DNL Filter]>[!DNL Ad status]** und wählen Sie dann alle Felder aus.

1. Wählen Sie in der Symbolleiste Berichtseinstellungen die Option **[!DNL Download]>[!DNL Excel .csv]**.

### Berichtseinstellungen für die Verwendung in Search, Social und Commerce

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
>* [Über die Kampagnenverwaltung in Search, Social und Commerce](campaign-management-about.md)
>* [Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen](campaign-implemention-overview.md)
>* [Überwachen und verwalten Sie die Leistung Ihrer Werbenetzwerk-Kampagnen.](monitor-performance-campaigns.md)

