---
title: Implementieren von [!DNL Microsoft Advertising] Einkaufskampagnen
description: Erfahren Sie mehr über den Workflow zum Einrichten von [!DNL Microsoft Advertising] Einkaufskampagnen.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementieren von [!DNL Microsoft Advertising] -Einkaufskampagnen

Anzeigen in Einkaufskampagnen verwenden Daten zu Produkten in Ihrem vorhandenen [!DNL Microsoft Merchant Center]-Produkt-Feed anstelle von Suchbegriffen, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden.

[!DNL Microsoft] Einkaufskampagnen zielen auf die [!DNL Microsoft Advertising Shopping Network] ab. Die Einstellungen für Einkaufskampagnen umfassen ein bestimmtes Land, in dem die Produkte verkauft werden, und eine Priorität ([!DNL High], [!DNL Medium] oder [!DNL Low]). Optional können Sie Ihren Bestand filtern, um Produkte mit bestimmten Attributen zu bewerben und bestimmte Orte und Gerätetypen als Ziel festzulegen oder auszuschließen.

Sie können steuern, welche Produkte mit Ihren Shopping-Anzeigen angezeigt werden, indem Sie *[Produktgruppen mit mehreren Ebenen](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* auf Anzeigengruppenebene einrichten. Produktgruppen basieren auf beliebigen Produktattributen (Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID und benutzerdefinierte Beschriftungen). Sie können bis zu sieben Stufen von Produktgruppen erstellen, die ein- oder ausgeschlossen werden sollen, nicht jedoch &quot;[!DNL Add Products]&quot;. Sie können Angebote auf der niedrigsten Ebene von Produktgruppen festlegen, indem Sie dasselbe Angebot für alle übereinstimmenden Produkte verwenden. Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet [!DNL Microsoft Advertising] zuerst die Priorität auf Kampagnenebene, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt.

## Schritte zum Einrichten von [!DNL Microsoft Advertising] Warenkampagnen

Sie können Einkaufskampagnen einrichten, indem Sie [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) für [!DNL Microsoft Advertising], [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) oder einzeln verwenden. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

1. Richten Sie Ihr [!DNL Microsoft Merchant Center] -Konto ein und füllen Sie es mit Produktdaten aus.

1. [Erlauben Sie die Suche, Social und Commerce, Daten aus dem [!DNL Microsoft Merchant Center] Konto](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) herunterzuladen.

1. [Erstellen Sie eine Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) im Warennetzwerk.

1. [Erstellen Sie eine Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) innerhalb der Kampagne und legen Sie das Standardangebot für alle Anzeigen fest.

   Sie können das Standardangebot für einzelne Produktgruppen überschreiben.

1. Erstellen Sie Produktgruppen für die Anzeigengruppe:

   1. [Erstellen Sie eine Produktgruppe &quot;Alle Produkte&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Optional) [Erstellen Sie untergeordnete Produktgruppen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Erstellen Sie [Produktanzeigen](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) mit [Promotion-Zeilen, die potenziell in jede Shopping-Anzeige](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) innerhalb der Anzeigengruppe aufgenommen werden können.

      Microsoft Advertising generiert die Anzeigenkopie und die Landingpage-URL für jede Anzeige dynamisch.

      >[!NOTE]
      >
      >Selbst wenn die Anzeigengruppe keine Anzeigenentitäten enthält, zeigt [!DNL Microsoft Advertising] weiterhin Anzeigen für die Produkte an.

1. (Optional) Um Klicks auf die Anzeige zu verfolgen, generieren [eine Tracking-URL mit dem Tool &quot;Tracking-URLs&quot;](/help/search-social-commerce/tools/click-tracking-url-generate.md). Es empfiehlt sich, die Tracking-URL dem Feld [!UICONTROL Tracking Template] in den Konto-, Kampagnen- oder Produktgruppeneinstellungen hinzuzufügen. Um die Wartung zu erleichtern, fügen Sie sie auf der höchstmöglichen Ebene hinzu.

   Alternativ können Sie die Tracking-URL den Produktdaten im [!DNL Microsoft Merchant Center] -Konto hinzufügen. Fügen Sie dazu die Tracking-URL zusammen mit dem Wert im Feld &quot;link&quot;oder &quot;mobile_link&quot;entsprechend in eine benutzerdefinierte Spalte &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot;im Produkt-Feed ein. Der Wert im Feld &quot;bingads_redirect&quot;ersetzt die Werte in den Feldern &quot;link&quot; und &quot;mobile_link&quot;. Die mit dieser Methode generierten URLs enthalten keine Tracking-Parameter, die in den Konto- oder Kampagneneinstellungen für Search, Social und Commerce angegeben sind.

1. Überwachen Sie die Leistung durch [Generieren des [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Bei Bedarf:

   1. [Bearbeiten Sie die Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), um das Kampagnenbudget anzupassen.

      Wenn die Kampagne Teil eines Portfolios ist, ermöglicht es die Portfolioeinstellung &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;, dass Search, Social und Commerce die Budgets für alle Kampagnen im Portfolio optimieren.

   1. Passen Sie das Höchstgebot für bestehende Produktgruppen an, löschen Sie Produktgruppen, für die Sie keine Anzeigen mehr erstellen möchten, oder fügen Sie eine neue Produktgruppe &quot;Alle Produkte&quot;oder neue untergeordnete Produktgruppen hinzu, um Anzeigen für weitere Produkte zu erstellen.

>[!NOTE]
>
>* Sehen Sie sich die erforderlichen Felder für die Verwaltung von [!DNL Microsoft Shopping] Kampagnen und Produktgruppen mit [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) und [Inventar-Feed-Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md) an.
>* Weitere Informationen zu [!DNL Microsoft Shopping] -Kampagnen finden Sie in der [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/50903).
