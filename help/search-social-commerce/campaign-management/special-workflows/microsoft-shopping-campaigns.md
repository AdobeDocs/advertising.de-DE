---
title: Implementieren  [!DNL Microsoft Advertising]  Einkaufskampagnen
description: Erfahren Sie mehr über den Workflow zum Einrichten von  [!DNL Microsoft Advertising] .
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementieren [!DNL Microsoft Advertising] Shopping-Kampagnen

Anzeigen in Shopping-Kampagnen verwenden Daten über Produkte in Ihrem vorhandenen [!DNL Microsoft Merchant Center]-Produkt-Feed anstelle von Keywords, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden sollen.

[!DNL Microsoft] Einkaufskampagnen zielen auf die [!DNL Microsoft Advertising Shopping Network] ab. Die Einstellungen für Shopping-Kampagnen umfassen ein bestimmtes Land, in dem die Produkte verkauft werden, sowie eine Priorität ([!DNL High], [!DNL Medium] oder [!DNL Low]). Sie können optional Ihren Bestand filtern, um Produkte mit bestimmten Attributen anzuzeigen, und bestimmte Standorte und Gerätetypen ansprechen oder ausschließen.

Sie können steuern, welche Produkte mit Ihren Shopping-Anzeigen angezeigt werden, indem Sie *[(Produktgruppen)](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* Anzeigengruppenebene einrichten. Produktgruppen basieren auf beliebigen Produktattributen (Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID und benutzerdefinierte Beschriftungen). Sie können bis zu sieben Ebenen von Produktgruppen erstellen, die Sie ein- oder von Angeboten ausschließen können, ohne &quot;[!DNL Add Products]&quot;. Sie können Gebote auf der niedrigsten Ebene der Produktgruppen festlegen und dasselbe Gebot für alle passenden Produkte verwenden. Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet [!DNL Microsoft Advertising] zuerst die Priorität auf Kampagnenebene, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot geeignet.

## Schritte zum Einrichten [!DNL Microsoft Advertising] Einkaufskampagnen

Sie können Shopping-Kampagnen [!DNL Microsoft Advertising] mithilfe von [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md), mithilfe von [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) oder einzeln einrichten. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

1. Richten Sie Ihr [!DNL Microsoft Merchant Center]-Konto ein und füllen Sie es mit Produktdaten.

1. [Erlauben Sie Search, Social und Commerce, Daten aus dem - [!DNL Microsoft Merchant Center]  herunterzuladen](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Erstellen einer Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) im Shopping-Netzwerk.

1. [Erstellen Sie innerhalb ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) Kampagne eine Anzeigengruppe und legen Sie das Standardangebot für alle Anzeigen fest.

   Sie können das Standardangebot für einzelne Produktgruppen überschreiben.

1. Erstellen Sie Produktgruppen für die Anzeigengruppe:

   1. [Erstellen Sie eine Produktgruppe „Alle Produkte“](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Optional) [Erstellen von untergeordneten Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Erstellen Sie [Produktanzeigen](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) mit [Promotion-Zeilen, die potenziell in jede Shopping-Anzeige ](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) der Anzeigengruppe aufgenommen werden sollen.

      Microsoft Advertising generiert für jede Anzeige dynamisch die Anzeigenkopie und die Landingpage-URL.

      >[!NOTE]
      >
      >Auch wenn die Anzeigengruppe keine Anzeigenentitäten enthält, zeigt [!DNL Microsoft Advertising] dennoch Anzeigen für die Produkte an.

1. (Optional) Zum Nachverfolgen von Klicks auf die Anzeige [generieren Sie eine Tracking-URL mit dem Tracking-URL](/help/search-social-commerce/tools/click-tracking-url-generate.md). Es empfiehlt sich, die Tracking-URL dem Feld [!UICONTROL Tracking Template] in den Einstellungen für das Konto, die Kampagne oder die Produktgruppe hinzuzufügen. Für eine einfachere Wartung fügen Sie sie auf der höchstmöglichen Ebene hinzu.

   Alternativ können Sie die Tracking-URL zu den Produktdaten im [!DNL Microsoft Merchant Center]-Konto hinzufügen. Fügen Sie dazu die Tracking-URL zusammen mit dem Wert im Feld „link“ bzw. „mobile_link“ in eine benutzerdefinierte Spalte &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; im Produkt-Feed ein. Der Wert im Feld „bingads_redirect“ ersetzt die Werte in den Feldern „link“ und „mobile_link“. Mit dieser Methode generierte URLs enthalten keine Tracking-Parameter, die in den Such-, Social- und Commerce-Konto- oder Kampagneneinstellungen angegeben sind.

1. Überwachen Sie die Leistung, [ Sie die [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md) generieren.

1. Bei Bedarf:

   1. [Bearbeiten Sie die Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) um das Kampagnenbudget anzupassen.

      Wenn die Kampagne Teil eines Portfolios ist, können Search, Social und Commerce mit der Portfolioeinstellung &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; die Budgets für alle Kampagnen im Portfolio optimieren.

   1. Passen Sie das maximale Angebot für bestehende Produktgruppen an, löschen Sie Produktgruppen, für die Sie keine Anzeigen mehr erstellen möchten, oder fügen Sie eine neue Produktgruppe „Alle Produkte“ oder neue untergeordnete Produktgruppen hinzu, um Anzeigen für zusätzliche Produkte zu erstellen.

>[!NOTE]
>
>* Ermitteln Sie die erforderlichen Felder für die Verwaltung von [!DNL Microsoft Shopping]-Kampagnen und Produktgruppen mithilfe [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) und [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Weitere Informationen zu [!DNL Microsoft Shopping]-Kampagnen finden Sie unter [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/50903).
