---
title: '[!DNL Microsoft Advertising] Konversionsdaten'
description: Erfahren Sie mehr über die Typen der  [!DNL Microsoft Advertising]-verfolgten Konversionsdaten, die in Search, Social und Commerce verfügbar sind.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] Konversionsdaten in Search, Social und Commerce

Search, Social und Commerce synchronisieren automatisch alle Konversionen, die von Ihren [[!DNL Microsoft Advertising] Universal Event Tracking (UET)-Tags](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) verfolgt werden, für Website-Konversionen, einschließlich Durchsichtskonversionen, zur Berichterstellung und Optimierung.

Alle Metriken sind automatisch in Ihren Kampagnenverwaltungsansichten und Basisberichten verfügbar und stehen auch zur Verwendung in Portfoliozielen zur Optimierung von [!DNL Microsoft Advertising] -Kampagnen zur Verfügung.

## Verfügbare Konversionsdaten

Die Funktion &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;synchronisiert Daten für Konversionen, für die die Option &quot;[!DNL Include in 'Conversions']&quot;aktiviert ist. Dabei werden die Daten für die letzten 35 Tage abgerufen und dann Änderungen an den Daten täglich bis 09:00-10:00 in der Zeitzone des Advertisers abgerufen. Historische Daten können sich von Tag zu Tag ändern, da bei jedem Klick neue Konversionen verfolgt werden.

Zwei Metriken für jede [[!DNL Microsoft Advertising]-verfolgte Konversion](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (die Sie in [!DNL Microsoft Advertising] eingerichtet haben) stehen automatisch in Search, Social und Commerce zur Verfügung und verwenden die in [!DNL Microsoft Advertising] konfigurierten Konversionsnamen. Zu den Metriken für jede Konversion gehören:

* `<conversion-name>` - Der Konversionswert für den Suchbegriff (z. B. Kauf).

  >[!TIP]
  >
  >Verwenden Sie diesen Konversionsmetriktyp im Ziel für Portfolios mit [!DNL Microsoft Advertising] Kampagnen mit den Angebotsstrategien &quot;Max. Konversionswert&quot;und &quot;Target ROAS&quot;.

* `CT_<conversion-name>` - Die Anzahl (Anzahl) der Konversionen, beginnend mit dem Präfix &quot;CT_&quot; (z. B. CT_Purchase).

  >[!TIP]
  >
  >Verwenden Sie diesen Konversionsmetriktyp im Ziel für Portfolios mit [!DNL Microsoft Advertising] Kampagnen mit den Max. Konversions- und Target-CPA-Angebotsstrategien.

Daten sind basierend auf der Klickzeit und der Konversions-/Transaktionszeit ab dem Datum verfügbar, an dem die Funktion für das Konto aktiviert ist.

[!DNL Microsoft Advertising] zeichnet jede Konversion nach [Angebotseinheit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klickdatum auf (nicht nach Konversionsdatum). Die Attribution basiert auf der standardmäßigen Zuordnungseinstellung für jede Metrik in [!DNL Microsoft Advertising]; die Adobe Advertising-Attribution ist nicht in berücksichtigt, da Daten auf Klickereignis-Ebene nicht verfügbar sind.

>[!NOTE]
>
>* Wenn mehrere Konten mit denselben Konversionsnamen vorhanden sind, werden unter Adobe Advertising möglicherweise doppelte Konversionsnamen angezeigt. In diesem Fall ändern Sie [ den Anzeigenamen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) für eine der doppelten Metriken in [!UICONTROL Admin] > [!UICONTROL Conversions]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
>* Daten auf der Ebene der Angebotseinheit stimmen mit Daten im Anzeigennetzwerk auf derselben Ebene überein. Die eigenen Konversionsdaten des Werbenetzwerks für höhere Ebenen können jedoch zusätzliche Konversionen enthalten, die nicht den untergeordneten Gebotseinheiten zugeordnet werden. Daten in Search, Social und Commerce werden immer auf der Ebene der Angebotseinheiten aggregiert, sodass beispielsweise ein Bericht auf Kampagnenebene möglicherweise nicht die gleichen Summen wie ein Bericht auf Kampagnenebene im Werbenetzwerk aufweist.
>* Datenabweichungen sind in der Regel nach der Morgensynchronisierung geringer als nach der Tageszeit, wenn noch keine zusätzlichen Konversionen synchronisiert wurden. Es wird empfohlen, die Daten morgens zu überprüfen.
>* Daten sind nicht auf Zielgruppen- oder geografischer Standortebene verfügbar und werden daher nicht zur automatischen Optimierung von RLSA und Ortsgebotsanpassungen verwendet.

## Vergleichen von Konversionsdaten in [!DNL Microsoft Advertising] mit Daten in Search, Social und Commerce

Verwenden Sie die folgenden Berichtseinstellungen, um vergleichbare Daten zu überprüfen.

### In [!DNL Microsoft Advertising] zu verwendende Berichtseinstellungen

Erstellen Sie den Bericht für die ausgewählten Konversionsaktionen nach Tag und fügen Sie Daten für alle Anzeigenstatus ein.

### Berichtseinstellungen für die Verwendung in Search, Social und Commerce

Verwenden Sie in Search, Social und Commerce die Ansicht- oder Berichtsoption, um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Report]**, halten Sie den Cursor über **[!UICONTROL Basic Reports]** und klicken Sie dann auf **[!UICONTROL Search Engine Account Report]**.

1. Geben Sie im Fenster [!UICONTROL Report Settings] die folgenden Berichtseinstellungen an:

   1. Wählen Sie im Abschnitt &quot;**[!UICONTROL Conversions Based]** on&quot;die Option &quot;**[!UICONTROL Click date]**&quot;.

   1. Geben Sie denselben Datumsbereich an, den Sie für den Bericht [!DNL Microsoft Advertising] verwendet haben.

   1. Wählen Sie im Abschnitt **[!UICONTROL Search/Content]** die Option **[!UICONTROL Search Only]** aus.

   1. Erweitern Sie im Abschnitt **[!UICONTROL Search Engine Hierarchy]** den Abschnitt [!UICONTROL Microsoft Advertising] und wählen Sie das Konto aus.

   1. Öffnen Sie die Registerkarte [!UICONTROL Columns] und fügen Sie die [!DNL Microsoft Advertising] -Metriken hinzu, die Sie vergleichen möchten.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Anzeigennetzwerkkonten und -kampagnen](campaign-implemention-overview.md)
>* [Überwachen und Verwalten der Leistung Ihrer Werbenetzwerk-Kampagnen](monitor-performance-campaigns.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
