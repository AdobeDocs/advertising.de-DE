---
title: Implementieren von [!DNL Google Ads] Einkaufskampagnen
description: Erfahren Sie mehr über den Workflow zum Einrichten von [!DNL Google Ads] Einkaufskampagnen.
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 3c702a01df1186e74c4f329a08199ce829be0827
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Implementieren von [!DNL Google Ads] -Einkaufskampagnen

Anzeigen in Einkaufskampagnen verwenden Daten zu Produkten in Ihrem vorhandenen [!DNL Google Merchant Center]-Produkt-Feed anstelle von Suchbegriffen, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden.

[!DNL Google Ads] Kampagnen können die [!DNL Google Shopping Network] mit dem [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network]&quot; als Ziel auswählen. Die Einstellungen für [!DNL Google Shopping] -Kampagnen beinhalten eine Priorität ([!UICONTROL High], [!UICONTROL Medium] oder [!UICONTROL Low]). Sie können optional Ihre lokalen Lagerbestandsdaten in Ihren Einkaufsanzeigen anzeigen, indem Sie eine Einstellung auf Kampagnenebene verwenden.

Sie können steuern, welche Produkte mit Ihren Shopping-Anzeigen angezeigt werden, indem Sie *[Produktgruppen mit mehreren Ebenen](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* auf Anzeigengruppenebene einrichten. Produktgruppen basieren auf beliebigen Produktattributen (Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID und benutzerdefinierte Beschriftungen). Sie können bis zu sieben Stufen von Produktgruppen erstellen, die ein- oder ausgeschlossen werden. Sie können Angebote auf der niedrigsten Ebene von Produktgruppen festlegen, indem Sie dasselbe Angebot für alle übereinstimmenden Produkte verwenden. Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet [!DNL Google Ads] zuerst die Priorität auf Kampagnenebene, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt.

## Schritte zum Einrichten von [!DNL Google Ads] Warenkampagnen

Sie können Einkaufskampagnen einrichten, indem Sie [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) für [!DNL Google Shopping], [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) oder einzeln verwenden. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

1. Richten Sie Ihr [!DNL Google Merchant Center] -Konto ein und füllen Sie es mit Produktdaten aus.

1. [Erlauben Sie die Suche, Social und Commerce, Daten aus dem [!DNL Google Merchant Center] Konto](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) herunterzuladen.

1. [Erstellen Sie eine Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) im Warennetzwerk.

1. [Erstellen Sie eine Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) innerhalb der Kampagne und legen Sie das Standardangebot für alle Anzeigen fest.

   Sie können das Standardangebot für einzelne Produktgruppen überschreiben.

1. Erstellen Sie Produktgruppen für die Anzeigengruppe:

   1. [Erstellen Sie eine Produktgruppe &quot;Alle Produkte&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Optional) [Erstellen Sie untergeordnete Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Sie müssen keine Shopping-Anzeigen erstellen. Selbst wenn die Anzeigengruppe keine Anzeigenentitäten enthält, zeigt [!DNL Google Ads] weiterhin Anzeigen für die Produkte an.

1. (Optional) Um Klicks auf die Anzeige zu verfolgen, generieren Sie [eine Tracking-URL mit dem Tool &quot;Tracking-URLs&quot;](/help/search-social-commerce/tools/click-tracking-url-generate.md) und fügen Sie sie dann zu den Konto-, Kampagnen- oder Produktgruppeneinstellungen hinzu.

1. Überwachen Sie die Leistung durch [ Generieren der [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) und [des [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Bei Bedarf:

   1. [Bearbeiten Sie die Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), um das Kampagnenbudget anzupassen.

      Wenn die Kampagne Teil eines Portfolios ist, ermöglicht es die Portfolioeinstellung &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;, dass Search, Social und Commerce die Budgets für alle Kampagnen im Portfolio optimieren.

   1. [Passen Sie das Höchstangebot für bestehende Produktgruppen an](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [löschen Sie Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), für die Sie keine Anzeigen mehr erstellen möchten, oder fügen Sie eine [neue Produktgruppe &quot;Alle Produkte&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) oder eine [neue untergeordnete Produktgruppe](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) hinzu, um Anzeigen für weitere Produkte zu erstellen.

>[!NOTE]
>
>* Sehen Sie sich die erforderlichen Felder für die Verwaltung von [!DNL Google Shopping] Kampagnen und Produktgruppen mit [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) und [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md) an.
>* Weitere Informationen zu [!DNL Google Shopping] -Kampagnen finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/2454022).
