---
title: Implementierung [!DNL Microsoft Advertising] Warenkorb
description: Erfahren Sie mehr über den Workflow zur Einrichtung [!DNL Microsoft Advertising] Einkaufskampagnen.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementierung [!DNL Microsoft Advertising] Warenkorb

Anzeigen in Einkaufskampagnen verwenden Daten zu Produkten in Ihren vorhandenen [!DNL Microsoft Merchant Center] Produkt-Feed anstelle von Keywords verwenden, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden.

[!DNL Microsoft] Shopping-Kampagnen zielen auf [!DNL Microsoft Advertising Shopping Network]. Die Einstellungen für Einkaufskampagnen umfassen ein bestimmtes Land, in dem die Produkte verkauft werden, und eine Priorität ([!DNL High], [!DNL Medium]oder [!DNL Low]). Optional können Sie Ihren Bestand filtern, um Produkte mit bestimmten Attributen zu bewerben und bestimmte Orte und Gerätetypen als Ziel festzulegen oder auszuschließen.

Sie können steuern, welche Produkte mit Ihren Shopping-Anzeigen angezeigt werden, indem Sie mehrstufige *[Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* auf Anzeigengruppenebene. Produktgruppen basieren auf beliebigen Produktattributen (Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID und benutzerdefinierte Beschriftungen). Sie können bis zu sieben Stufen von Produktgruppen erstellen, die ein- oder ausgeschlossen werden sollen, ausgenommen &quot;[!DNL Add Products].&quot; Sie können Angebote auf der niedrigsten Ebene von Produktgruppen festlegen, indem Sie dasselbe Angebot für alle übereinstimmenden Produkte verwenden. Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, [!DNL Microsoft Advertising] verwendet zuerst die Priorität auf Kampagnenebene, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt.

## Schritte zum Einrichten [!DNL Microsoft Advertising] Warenkorb

Sie können Einkaufskampagnen mithilfe von [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) für [!DNL Microsoft Advertising]durch Verwendung von [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)oder einzeln. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

1. Richten Sie Ihre [!DNL Microsoft Merchant Center] -Konto erstellen und mit Produktdaten füllen.

1. [Suche, Social und Commerce erlauben, Daten aus der [!DNL Microsoft Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Kampagne erstellen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) im Warennetzwerk.

1. [Erstellen einer Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) innerhalb der Kampagne und legen Sie das Standardangebot für alle Anzeigen fest.

Sie können das Standardangebot für einzelne Produktgruppen überschreiben.

1. Erstellen Sie Produktgruppen für die Anzeigengruppe:

   1. [Erstellen einer Produktgruppe &quot;Alle Produkte&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Optional) [Untergeordnete Produktgruppen erstellen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Erstellen [Produktanzeigen](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) mit [Werbelinien, die potenziell in jede Shopping-Anzeige eingeschlossen werden sollen](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) innerhalb der Anzeigengruppe.

      Microsoft Advertising generiert dynamisch die Anzeigenkopie und die Landingpage-URL für jede Anzeige.

      >[!NOTE]
      >
      >Selbst wenn die Anzeigengruppe keine Anzeigenentitäten enthält, [!DNL Microsoft Advertising] zeigt weiterhin Anzeigen für die Produkte an.

1. (Optional) Um Klicks auf die Anzeige zu verfolgen, [eine Tracking-URL mit dem Tool Tracking-URLs generieren](/help/search-social-commerce/tools/click-tracking-url-generate.md). Es empfiehlt sich, die Tracking-URL zur [!UICONTROL Tracking Template] in den Konto-, Kampagnen- oder Produktgruppeneinstellungen. Um die Wartung zu erleichtern, fügen Sie sie auf der höchstmöglichen Ebene hinzu.

   Alternativ können Sie die Tracking-URL den Produktdaten innerhalb der [!DNL Microsoft Merchant Center] -Konto. Fügen Sie dazu die Tracking-URL zusammen mit dem Wert im Feld &quot;link&quot;oder &quot;mobile_link&quot;in eine benutzerdefinierte Spalte ein.[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot;im Produkt-Feed. Der Wert im Feld &quot;bingads_redirect&quot;ersetzt die Werte in den Feldern &quot;link&quot; und &quot;mobile_link&quot;. Die mit dieser Methode generierten URLs enthalten keine Tracking-Parameter, die in den Konto- oder Kampagneneinstellungen für Search, Social und Commerce angegeben sind.

1. Überwachen der Leistung nach [Generieren der [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Bei Bedarf:

   1. [Kampagnenparameter bearbeiten](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) , um das Kampagnenbudget anzupassen.

      Wenn die Kampagne Teil eines Portfolios ist, wird durch die Portfolioeinstellung &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; ermöglicht Search, Social und Commerce die Budgetoptimierung für alle Kampagnen im Portfolio.

   1. Passen Sie das Höchstgebot für bestehende Produktgruppen an, löschen Sie Produktgruppen, für die Sie keine Anzeigen mehr erstellen möchten, oder fügen Sie eine neue Produktgruppe &quot;Alle Produkte&quot;oder neue untergeordnete Produktgruppen hinzu, um Anzeigen für weitere Produkte zu erstellen.

>[!NOTE]
>
>* Siehe erforderliche Felder für die Verwaltung [!DNL Microsoft Shopping] Kampagnen und Produktgruppen mit [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) und [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Weitere Informationen finden Sie unter [!DNL Microsoft Shopping] Kampagnen, siehe [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/50903).
