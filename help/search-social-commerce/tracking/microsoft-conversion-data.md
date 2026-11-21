---
title: Konvertierungsdaten [!DNL Microsoft Advertising]
description: Erfahren Sie mehr über die Arten von Konversionsdaten mit [!DNL Microsoft Advertising]-Tracking, die in Search, Social und Commerce verfügbar sind.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
TQID: 'https://experienceleague.adobe.com/ZK-uDqw0sThnMzX6bdR-d33gh-AlLTaytJr1fS7pdgs'
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
source-wordcount: '652'
ht-degree: 0%
---
# [!DNL Microsoft Advertising] von Konversionsdaten in Search, Social und Commerce

Search, Social und Commerce synchronisieren automatisch alle Konversionen, die von Ihren [[!DNL Microsoft Advertising] UET-Tags (Universal Event Tracking) &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/53056) werden, für Website-Konversionen, einschließlich View-Through-Konversionen, um Berichte zu erstellen und zu optimieren.

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

[!DNL Microsoft Advertising] zeichnet jede Konvertierung nach [Gebotseinheit](/help/search-social-commerce/glossary.md#a-b), Gerät und Klickdatum (nicht Konvertierungsdatum) auf. Die Attribution basiert auf der standardmäßigen Attributionseinstellung für jede Metrik in [!DNL Microsoft Advertising]. Die Adobe Advertising-Attribution wird nicht berücksichtigt, da keine Daten auf Klick-Ereignisebene verfügbar sind.

>[!NOTE]
>
>* Wenn Sie mehrere Konten mit denselben Konversionsnamen haben, werden in Adobe Advertising möglicherweise doppelte Konversionsnamen angezeigt. Wenn dies auftritt, [ändern Sie den Anzeigenamen](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#change-the-display-name-for-a-conversion-metric) für eine der doppelten Metriken unter [!UICONTROL Goals] > [!UICONTROL Conversions]. Die Berichterstellung ist nicht korrekt, wenn zwei verschiedene Metriken denselben Namen haben.
>* Daten auf der Ebene der Gebotseinheiten stimmen mit Daten im Anzeigennetzwerk auf derselben Ebene überein. Die eigenen Konversionsdaten des Anzeigennetzwerks für höhere Ebenen können jedoch zusätzliche Konversionen enthalten, die nicht den untergeordneten Gebotseinheiten zugeordnet werden. Daten in Search, Social und Commerce werden immer ab der Ebene der Gebotseinheiten aggregiert, sodass beispielsweise ein Bericht auf Kampagnenebene nicht dieselben Summen wie ein Bericht auf Kampagnenebene im Werbenetzwerk hat.
>* Die Datenvarianz ist in der Regel nach der morgendlichen Synchronisierung geringer als nach der späteren am Tag, wenn zusätzliche Konversionen noch nicht synchronisiert wurden. Es wird empfohlen, die Daten morgens zu validieren.
>* Daten sind nicht auf Audience- oder geografischer Standortebene verfügbar und werden daher nicht zur automatischen Optimierung von RLSA- und Standortangebotsanpassungen verwendet.

## Vergleichen von Konversionsdaten in [!DNL Microsoft Advertising] mit Daten in Search, Social und Commerce

Verwenden Sie die folgenden Berichtseinstellungen, um vergleichbare Daten zu validieren.

### In [!DNL Microsoft Advertising] zu verwendende Berichtseinstellungen

Generieren Sie den Bericht für die ausgewählten Konversionsaktionen nach Tag und schließen Sie Daten für alle Anzeigenstatus ein.

### In Search, Social und Commerce zu verwendende Berichteinstellungen

Verwenden Sie in Search, Social und Commerce die Option Anzeigen oder Bericht , um Konversionen basierend auf dem Klickdatum (nicht dem Transaktionsdatum) anzuzeigen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Klicken Sie auf **[!UICONTROL Create Report]**, klicken Sie im linken Bereich auf **[!UICONTROL Basic Reports]**, und wählen Sie dann **[!UICONTROL Search Engine Account Report]** aus. Klicken Sie auf **[!UICONTROL Proceed]**.

1. Öffnen Sie im [!UICONTROL Create Report] die Registerkarte **[!UICONTROL Basic Settings]** und geben Sie die folgenden [Berichteinstellungen](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md) an:

   1. Legen Sie **[!UICONTROL Data Aggregation]** auf **[!UICONTROL Daily]** fest.

   1. Legen Sie **[!UICONTROL Conversions Based on]** auf **[!UICONTROL Click date]** fest.

   1. Geben Sie denselben Datumsbereich an, den Sie für den [!DNL Microsoft Advertising] Bericht verwendet haben.

   1. Legen Sie **[!UICONTROL Search/Content]** auf **[!UICONTROL Search Only]** fest.

   1. Wenn **[!UICONTROL Filter By]** angezeigt wird, wählen Sie **[!UICONTROL Search engine]** aus.

   1. Erweitern Sie in **[!UICONTROL Search Engine Hierarchy]** [!DNL Microsoft Advertising] und aktivieren Sie das Kontrollkästchen neben dem Konto, das Sie vergleichen möchten. Klicken Sie auf **[!UICONTROL Add selected items]** , um das Konto in **[!UICONTROL Selected Filters]** zu verschieben.

1. Öffnen Sie die Registerkarte **[!UICONTROL Columns]** und fügen Sie die [!DNL Microsoft Advertising] Metriken hinzu, die Sie vergleichen möchten.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Einrichten von Netzwerkkonten und Kampagnen für Werbeanzeigen](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Über die Verwaltung von Kampagnen und Portfolios](/help/search-social-commerce/manage/manage-about.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#view-the-conversion-metrics-tracked-for-an-advertiser)
