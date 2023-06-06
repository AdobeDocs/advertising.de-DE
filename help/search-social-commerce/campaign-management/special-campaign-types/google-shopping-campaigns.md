---
title: Implementierung [!DNL Google Ads] Warenkorb
description: Erfahren Sie mehr über den Arbeitsablauf für die Einrichtung [!DNL Google Ads] Einkaufskampagnen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Implementierung [!DNL Google Ads] Warenkorb

Anzeigen in Einkaufskampagnen verwenden Daten zu Produkten in Ihren vorhandenen [!DNL Google Merchant Center] Produkt-Feed anstelle von Keywords verwenden, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden.

[!DNL Google Ads] Kampagnen können die [!DNL Google Shopping Network] mithilfe der [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; Die Einstellungen für [!DNL Google Shopping] Kampagnen beinhalten eine Priorität ([!UICONTROL High], [!UICONTROL Medium]oder [!UICONTROL Low]). Sie können optional Ihre lokalen Lagerbestandsdaten in Ihren Einkaufsanzeigen anzeigen, indem Sie eine Einstellung auf Kampagnenebene verwenden.

Sie können steuern, welche Produkte mit Ihren Shopping-Anzeigen angezeigt werden, indem Sie mehrstufige *[Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* auf Anzeigengruppenebene. Produktgruppen basieren auf beliebigen Produktattributen (Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID und benutzerdefinierte Beschriftungen). Sie können bis zu sieben Stufen von Produktgruppen erstellen, die ein- oder ausgeschlossen werden. Sie können Angebote auf der niedrigsten Ebene von Produktgruppen festlegen, indem Sie dasselbe Angebot für alle übereinstimmenden Produkte verwenden. Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, [!DNL Google Ads] verwendet zuerst die Priorität auf Kampagnenebene, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt.

## Schritte zum Einrichten [!DNL Google Ads] Warenkorb

Sie können Einkaufskampagnen einrichten, indem Sie [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) für [!DNL Google Shopping]durch Verwendung von [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)oder einzeln. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

1. Richten Sie Ihre [!DNL Google Merchant Center] -Konto erstellen und mit Produktdaten füllen.

1. [Suche, Social und Commerce erlauben, Daten aus der [!DNL Google Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Kampagne erstellen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) im Warennetzwerk.

1. [Erstellen einer Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) innerhalb der Kampagne und legen Sie das Standardangebot für alle Anzeigen fest.

Sie können das Standardangebot für einzelne Produktgruppen überschreiben.

1. Erstellen Sie Produktgruppen für die Anzeigengruppe:

   1. [Erstellen einer Produktgruppe &quot;Alle Produkte&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Optional) [Untergeordnete Produktgruppen erstellen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).
   >[!NOTE]
   >Sie müssen keine Shopping-Anzeigen erstellen. Selbst wenn die Anzeigengruppe keine Anzeigenentitäten enthält, [!DNL Google Ads] zeigt weiterhin Anzeigen für die Produkte an.

1. (Optional) Um Klicks auf die Anzeige zu verfolgen, [eine Tracking-URL mit dem Tool Tracking-URLs generieren](/help/search-social-commerce/tools/click-tracking-url-generate.md)und fügen Sie sie dann den Einstellungen für Konto, Kampagne oder Produktgruppe hinzu.

1. Überwachen der Leistung nach [Generieren der [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) und [die [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Bei Bedarf:

   1. [Kampagnenparameter bearbeiten](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) , um das Kampagnenbudget anzupassen.

      Wenn die Kampagne Teil eines Portfolios ist, wird durch die Portfolioeinstellung &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; ermöglicht es Search, Social und Commerce, die Budgets für alle Kampagnen im Portfolio zu optimieren.

   1. [Passen Sie das Höchstangebot für bestehende Produktgruppen an](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [Produktgruppen löschen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) für die Sie keine Anzeigen mehr erstellen möchten, oder fügen Sie eine [neue Produktgruppe &quot;Alle Produkte&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) oder [Neue untergeordnete Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) um Anzeigen für weitere Produkte zu erstellen.

>[!NOTE]
>
>* Siehe erforderliche Felder für die Verwaltung [!DNL Google Shopping] Kampagnen und Produktgruppen mit [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) und [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Weitere Informationen finden Sie unter [!DNL Google Shopping] Kampagnen, siehe [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/2454022).

