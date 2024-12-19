---
title: Implementieren  [!DNL Google Ads]  Einkaufskampagnen
description: Erfahren Sie mehr über den Workflow zum Einrichten von  [!DNL Google Ads] .
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Implementieren [!DNL Google Ads] Shopping-Kampagnen

Anzeigen in Shopping-Kampagnen verwenden Daten über Produkte in Ihrem vorhandenen [!DNL Google Merchant Center]-Produkt-Feed anstelle von Keywords, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden sollen.

[!DNL Google Ads] Kampagnen können die [!DNL Google Shopping Network] mithilfe der [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network]&quot; ansprechen. Die Einstellungen für [!DNL Google Shopping] Kampagnen enthalten eine Priorität ([!UICONTROL High], [!UICONTROL Medium] oder [!UICONTROL Low]). Optional können Sie Ihre lokalen Inventarinformationen in Ihren Shopping-Anzeigen mit einer Einstellung auf Kampagnenebene anzeigen.

Sie können steuern, welche Produkte mit Ihren Shopping-Anzeigen angezeigt werden, indem Sie *[(Produktgruppen)](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* Anzeigengruppenebene einrichten. Produktgruppen basieren auf beliebigen Produktattributen (Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID und benutzerdefinierte Beschriftungen). Sie können bis zu sieben Ebenen von Produktgruppen erstellen, um Angebote ein- oder auszuschließen. Sie können Gebote auf der niedrigsten Ebene der Produktgruppen festlegen und dasselbe Gebot für alle passenden Produkte verwenden. Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet [!DNL Google Ads] zuerst die Priorität auf Kampagnenebene, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot geeignet.

## Schritte zum Einrichten [!DNL Google Ads] Einkaufskampagnen

Sie können Shopping-Kampagnen [!DNL Google Shopping] mithilfe von [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md), mithilfe von [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) oder einzeln einrichten. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

1. Richten Sie Ihr [!DNL Google Merchant Center]-Konto ein und füllen Sie es mit Produktdaten.

1. [Erlauben Sie Search, Social und Commerce, Daten aus dem - [!DNL Google Merchant Center]  herunterzuladen](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Erstellen einer Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) im Shopping-Netzwerk.

1. [Erstellen Sie innerhalb ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) Kampagne eine Anzeigengruppe und legen Sie das Standardangebot für alle Anzeigen fest.

   Sie können das Standardangebot für einzelne Produktgruppen überschreiben.

1. Erstellen Sie Produktgruppen für die Anzeigengruppe:

   1. [Erstellen Sie eine Produktgruppe „Alle Produkte“](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Optional) [Erstellen von untergeordneten Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Sie müssen keine Shopping-Anzeigen erstellen. Auch wenn die Anzeigengruppe keine Anzeigenentitäten enthält, zeigt [!DNL Google Ads] dennoch Anzeigen für die Produkte an.

1. (Optional) Zum Nachverfolgen von Klicks auf die Anzeige [generieren Sie eine Tracking-URL mit dem Tracking-URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)Tool und fügen Sie sie dann den Einstellungen für das Konto, die Kampagne oder die Produktgruppe hinzu.

1. Überwachen Sie die Leistung durch [Generieren des [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) und [des [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Bei Bedarf:

   1. [Bearbeiten Sie die Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) um das Kampagnenbudget anzupassen.

      Wenn die Kampagne Teil eines Portfolios ist, können Search, Social und Commerce mit der Portfolioeinstellung &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; die Budgets für alle Kampagnen im Portfolio optimieren.

   1. [Passen Sie das maximale Angebot für bestehende Produktgruppen an](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [löschen Sie Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) für die Sie keine Anzeigen mehr erstellen möchten, oder fügen Sie eine [neue Produktgruppe „Alle Produkte“ ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) oder [neue untergeordnete Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), um Anzeigen für zusätzliche Produkte zu erstellen.

>[!NOTE]
>
>* Ermitteln Sie die erforderlichen Felder für die Verwaltung von [!DNL Google Shopping]-Kampagnen und Produktgruppen mithilfe [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) und [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Weitere Informationen zu [!DNL Google Shopping]-Kampagnen finden Sie unter [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/2454022).
