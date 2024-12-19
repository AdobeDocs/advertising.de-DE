---
title: Konvertierungsdaten [!DNL Microsoft Advertising]
description: Erfahren Sie mehr über die Typen  [!DNL Microsoft Advertising] verfolgten Konversionsdaten, die in Search, Social und Commerce verfügbar sind.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: b8a34f3d85947536eb92ee481966f84694250f29
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] von Konversionsdaten in Search, Social und Commerce

Search, Social und Commerce synchronisieren automatisch alle Konversionen, die von Ihren [[!DNL Microsoft Advertising] UET-Tags (Universal Event Tracking) ](https://help.ads.microsoft.com/#apex/ads/en/53056) werden, für Website-Konversionen, einschließlich View-Through-Konversionen, um Berichte zu erstellen und zu optimieren.

Alle Metriken sind automatisch in Ihren Kampagnenverwaltungsansichten und Basisberichten verfügbar und können auch in Portfoliozielen zur Optimierung [!DNL Microsoft Advertising] Kampagnen verwendet werden.

## Verfügbare Konversionsdaten

Search, Social und Commerce synchronisieren Daten für Konversionen, für die die Option &quot;[!DNL Include in 'Conversions']&quot; aktiviert ist. Dabei werden die Daten der letzten 35 Tage abgerufen und anschließend die Änderungen an den Daten täglich um 09:00-10:00 Uhr in der Zeitzone des Werbetreibenden abgerufen. Historische Daten können sich von Tag zu Tag ändern, da neue Konversionen für jeden Klick verfolgt werden.

Zwei Metriken für jede [[!DNL Microsoft Advertising]-getrackte Konversion](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (die Sie in [!DNL Microsoft Advertising] eingerichtet haben) sind automatisch in Search, Social und Commerce verfügbar und verwenden die in [!DNL Microsoft Advertising] konfigurierten Konversionsnamen. Zu den Metriken für jede Konversion gehören:

* `<conversion-name>` - Der Konversionswert für das Keyword (z. B. Kauf).

  >[!TIP]
  >
  >Verwenden Sie diesen Typ der Konversionsmetrik im Ziel für Portfolios, die [!DNL Microsoft Advertising] Kampagnen mit den Bid-Strategien „Max. Konversionswert“ und „Target-ROAS“ enthalten.

* `CT_<conversion-name>` — Die Anzahl (Anzahl) der Konversionen, beginnend mit dem Präfix „CT_“ (z. B. CT_Purchase).

  >[!TIP]
  >
  >Verwenden Sie diesen Typ der Konversionsmetrik im Ziel für Portfolios, die [!DNL Microsoft Advertising] Kampagnen mit den Bid-Strategien Max. Konversionen und Target CPA enthalten.

Daten sind basierend auf der Klickzeit und auf der Konversions-/Transaktionszeit ab dem Datum verfügbar, an dem die Funktion für das Konto aktiviert wurde.

[!DNL Microsoft Advertising] zeichnet jede Konvertierung nach [Gebotseinheit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klickdatum (nicht Konvertierungsdatum) auf. Die Attribution basiert auf der standardmäßigen Attributionseinstellung für jede Metrik in [!DNL Microsoft Advertising]. Die Adobe Advertising-Attribution wird nicht berücksichtigt, da keine Daten auf Klickereignis-Ebene verfügbar sind.

>[!NOTE]
>
>* Wenn Sie mehrere Konten mit denselben Konversionsnamen haben, werden möglicherweise doppelte Konversionsnamen in Adobe Advertising angezeigt. Wenn dies auftritt, [ändern Sie den Anzeigenamen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) für eine der doppelten Metriken unter [!UICONTROL Admin] > [!UICONTROL Conversions]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
>* Daten auf der Ebene der Gebotseinheiten stimmen mit Daten im Anzeigennetzwerk auf derselben Ebene überein. Die eigenen Konversionsdaten des Anzeigennetzwerks für höhere Ebenen können jedoch zusätzliche Konversionen enthalten, die nicht den untergeordneten Gebotseinheiten zugeordnet werden. Daten in Search, Social und Commerce werden immer ab der Ebene der Gebotseinheiten aggregiert, sodass beispielsweise ein Bericht auf Kampagnenebene nicht dieselben Summen wie ein Bericht auf Kampagnenebene im Werbenetzwerk hat.
>* Die Datenvarianz ist in der Regel nach der morgendlichen Synchronisierung geringer als nach der späteren am Tag, wenn zusätzliche Konversionen noch nicht synchronisiert wurden. Es wird empfohlen, die Daten morgens zu validieren.
>* Daten sind nicht auf Audience- oder geografischer Standortebene verfügbar und werden daher nicht zur automatischen Optimierung von RLSA- und Standortangebotsanpassungen verwendet.

## Vergleichen von Konversionsdaten in [!DNL Microsoft Advertising] mit Daten in Search, Social und Commerce

Verwenden Sie die folgenden Berichtseinstellungen, um vergleichbare Daten zu validieren.

### In [!DNL Microsoft Advertising] zu verwendende Berichtseinstellungen

Generieren Sie den Bericht für die ausgewählten Konversionsaktionen nach Tag und schließen Sie Daten für alle Anzeigenstatus ein.

### In Search, Social und Commerce zu verwendende Berichteinstellungen

Verwenden Sie in Search, Social und Commerce die Option Anzeigen oder Bericht , um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Report]**, halten Sie den Cursor über **[!UICONTROL Basic Reports]** und klicken Sie dann auf **[!UICONTROL Search Engine Account Report]**.

1. Geben Sie im [!UICONTROL Report Settings] die folgenden Berichteinstellungen an:

   1. Wählen Sie im Abschnitt **[!UICONTROL Conversions Based]** auf die Option **[!UICONTROL Click date]**.

   1. Geben Sie denselben Datumsbereich an, den Sie für den [!DNL Microsoft Advertising] Bericht verwendet haben.

   1. Wählen Sie im **[!UICONTROL Search/Content]** Abschnitt **[!UICONTROL Search Only]** aus.

   1. Erweitern Sie im Abschnitt **[!UICONTROL Search Engine Hierarchy]** den Abschnitt [!UICONTROL Microsoft Advertising] und wählen Sie das Konto aus.

   1. Öffnen Sie die Registerkarte [!UICONTROL Columns] und fügen Sie die [!DNL Microsoft Advertising] Metriken hinzu, die Sie vergleichen möchten.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Übersicht über die Implementierung von Konten und Kampagnen des Werbenetzwerks](campaign-implemention-overview.md)
>* [Überwachen und Verwalten der Leistung Ihrer Werbenetzwerk-Kampagnen](monitor-performance-campaigns.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
