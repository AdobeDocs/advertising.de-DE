---
title: '''[!DNL Microsoft Advertising] Konversionsdaten"'
description: Erfahren Sie mehr über die Typen [!DNL Microsoft Advertising]-verfolgte Konversionsdaten, die in Search, Social und Commerce verfügbar sind.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Konversionsdaten in Search, Social und Commerce

Search, Social und Commerce synchronisieren automatisch alle Konversionen, die von Ihrer [[!DNL Microsoft Advertising] Universal Event Tracking (UET)-Tags](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) für Website-Konversionen, einschließlich Durchsichtskonversionen, zur Berichterstellung und Optimierung.

Alle Metriken sind automatisch in Ihren Kampagnenverwaltungsansichten und Basisberichten verfügbar und stehen auch zur Verwendung in Portfoliozielen zur Optimierung der [!DNL Microsoft Advertising] Kampagnen.

## Verfügbare Konversionsdaten

In Search, Social und Commerce werden Daten für Konversionen synchronisiert, für die die Variable[!DNL Include in 'Conversions']&quot; aktiviert ist, wobei die Daten für die letzten 35 Tage abgerufen und dann Änderungen an den Daten täglich bis 09 abgerufen werden.:00-10:00 in der Zeitzone des Werbetreibenden. Historische Daten können sich von Tag zu Tag ändern, da bei jedem Klick neue Konversionen verfolgt werden.

Zwei Metriken für jede [[!DNL Microsoft Advertising]-verfolgte Konversion](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (die Sie in [!DNL Microsoft Advertising]) sind automatisch in Search, Social und Commerce verfügbar und verwenden die in konfigurierten Konversionsnamen [!DNL Microsoft Advertising]. Zu den Metriken für jede Konversion gehören:

* `<conversion-name>` — Der Konversionswert für den Suchbegriff (z. B. Kauf).

  >[!TIP]
  >
  >Verwenden Sie diesen Konversionsmetriktyp im Ziel für Portfolios, die Folgendes enthalten: [!DNL Microsoft Advertising] Kampagnen mit den Angebotsstrategien Max. Konversionswert und Target ROAS.

* `CT_<conversion-name>` — Die Anzahl (Anzahl) der Konversionen, beginnend mit dem Präfix &quot;CT_&quot; (z. B. CT_Purchase).

  >[!TIP]
  >
  >Verwenden Sie diesen Konversionsmetriktyp im Ziel für Portfolios, die Folgendes enthalten: [!DNL Microsoft Advertising] Kampagnen mit den Max Conversions- und Target-CPA-Angebotsstrategien.

Daten sind basierend auf der Klickzeit und der Konversions-/Transaktionszeit ab dem Datum verfügbar, an dem die Funktion für das Konto aktiviert ist.

[!DNL Microsoft Advertising] erfasst jede Konversion von [Bid-Unit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klicken auf Datum (nicht Konvertierungsdatum). Die Attribution basiert auf der standardmäßigen Attributionseinstellung für jede Metrik in [!DNL Microsoft Advertising]; Die Adobe Advertising-Attribution wird nicht berücksichtigt, da Klick-Ereignisdaten nicht verfügbar sind.

>[!NOTE]
>
>* Wenn mehrere Konten mit denselben Konversionsnamen vorhanden sind, werden unter Adobe Advertising möglicherweise doppelte Konversionsnamen angezeigt. Tritt dies auf, [Anzeigenamen ändern](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) für eine der doppelten Metriken in [!UICONTROL Admin] > [!UICONTROL Conversions]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
>* Daten auf der Ebene der Angebotseinheit stimmen mit Daten im Anzeigennetzwerk auf derselben Ebene überein. Die eigenen Konversionsdaten des Werbenetzwerks für höhere Ebenen können jedoch zusätzliche Konversionen enthalten, die nicht den untergeordneten Gebotseinheiten zugeordnet werden. Daten in Search, Social und Commerce werden immer auf der Ebene der Angebotseinheiten aggregiert, sodass beispielsweise ein Bericht auf Kampagnenebene möglicherweise nicht die gleichen Summen wie ein Bericht auf Kampagnenebene im Werbenetzwerk aufweist.
>* Datenabweichungen sind in der Regel nach der Morgensynchronisierung geringer als nach der Tageszeit, wenn noch keine zusätzlichen Konversionen synchronisiert wurden. Es wird empfohlen, die Daten morgens zu überprüfen.
>* Daten sind nicht auf Zielgruppen- oder geografischer Standortebene verfügbar und werden daher nicht zur automatischen Optimierung von RLSA und Ortsgebotsanpassungen verwendet.

## Vergleichen von Konversionsdaten in [!DNL Microsoft Advertising] mit Daten in Search, Social und Commerce

Verwenden Sie die folgenden Berichtseinstellungen, um vergleichbare Daten zu überprüfen.

### Berichtseinstellungen zur Verwendung in [!DNL Microsoft Advertising]

Erstellen Sie den Bericht für die ausgewählten Konversionsaktionen nach Tag und fügen Sie Daten für alle Anzeigenstatus ein.

### Berichtseinstellungen für die Verwendung in Search, Social und Commerce

Verwenden Sie in Search, Social und Commerce die Ansicht- oder Berichtsoption, um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Report]** halten Sie den Cursor darüber. **[!UICONTROL Basic Reports]** und klicken Sie anschließend auf **[!UICONTROL Search Engine Account Report]**.

1. Im [!UICONTROL Report Settings] -Fenster die folgenden Berichtseinstellungen festlegen:

   1. Im **[!UICONTROL Conversions Based]** Wählen Sie im Bereich **[!UICONTROL Click date]**.

   1. Geben Sie denselben Datumsbereich an, den Sie für die [!DNL Microsoft Advertising] Bericht.

   1. Im **[!UICONTROL Search/Content]** Bereich, wählen Sie **[!UICONTROL Search Only]**.

   1. Im **[!UICONTROL Search Engine Hierarchy]** -Abschnitt, erweitern Sie die [!UICONTROL Microsoft Advertising] und wählen Sie das Konto aus.

   1. Öffnen Sie die [!UICONTROL Columns] und fügen Sie die [!DNL Microsoft Advertising] Metriken, die Sie vergleichen möchten.

1. Klicks **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen](campaign-implemention-overview.md)
>* [Überwachen und verwalten Sie die Leistung Ihrer Werbenetzwerk-Kampagnen.](monitor-performance-campaigns.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
