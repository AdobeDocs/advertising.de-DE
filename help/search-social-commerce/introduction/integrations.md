---
title: Integration mit Adobe Experience Cloud-Lösungen und -Diensten
description: Erfahren Sie mehr über Search-, Social- und Commerce-Integrationen mit Adobe Experience Cloud-Lösungen und -Diensten.
source-git-commit: 0c19479cb8ef4e9e037a46ab72f75b7423de5073
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Integration mit Adobe Experience Cloud-Lösungen und -Diensten

Advertising Search, Social und Commerce ist in Folgendes integriert [!DNL Adobe] Produkte.

* [Tags aus Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) - Sie können die [Adobe Advertising Cloud-Erweiterung](https://exchange.adobe.com/apps/ec/100155) für Adobe Experience Platform , um Adobe Advertising-Konversions-Tracking-Tags sowie Tracking-Tags von Drittanbietern für Ihre Anzeigen-Landingpages zu erstellen. (Sie können auch [Konversions-Tracking-Tags direkt in Search, Social und Commerce erstellen](/help/search-social-commerce/tools/conversion-tag-generate.md). Wenden Sie sich an Ihr Adobe Account Team oder Implementierungsteam, um Informationen zu Ihren Tags zu erhalten.

* Adobe Analytics - (Opt-in-Funktion) Adobe Advertising und [!DNL Analytics] wie folgt integriert sind:

   * Adobe Advertising und [!DNL Analytics] Daten nahtlos freigeben. [!DNL Analytics] kann Site-Interaktions- und Konversionsdaten täglich an Search, Social und Commerce senden, wo die Daten für die Anzeigenoptimierung und für die Berichterstellung verfügbar sind. Darüber hinaus kann Adobe Advertising Daten zum Anzeigen-Traffic von Ihren Werbenetzwerken täglich an senden, einschließlich Impressionen, Klicks und Kosten. [!DNL Analytics], wobei die Daten in allen Reporting-Tools verfügbar sind.

      Siehe[Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)&quot; für weitere Informationen zu [!DNL Analytics] Unterstützung für jedes Anzeigennetzwerk und jeden Anzeigentyp. Siehe auch &quot;[Übersicht über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)&quot; für weitere Informationen zum Datenaustausch.

      Zum Austausch von Daten, sowohl Adobe Advertising als auch [!DNL Analytics] muss zunächst konfiguriert werden. Wenden Sie sich an Ihr Adobe Account Team, um weitere Informationen zur Ersteinrichtung zu erhalten.

      >[!NOTE]
      >
      >Standardmäßig wird die [!DNL Analytics] Metriken sind nicht in den Bildschirmen &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;sichtbar. Sie müssen [die Metriken in Kampagnenverwaltungsansichten, Portfolios und Berichten verfügbar machen](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) nach [!DNL Adobe] Das Implementierungsteam hat ausgewählte standardmäßige oder benutzerdefinierte Ereignisse konfiguriert, die an die Adobe Advertising weitergegeben werden. Sie können optional die angezeigten Metriknamen ändern (ohne sie in [!DNL Analytics]). Sie können Metriken in der Benutzeroberfläche sichtbar machen und Metriken umbenennen aus [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

   * Advertiser mit [!DNL Analytics] Audience Manager kann [erstellen [!DNL Google Ads] Zielgruppen für Kundenabgleich](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) von [!DNL Analytics] Segmente, die für Adobe Experience Cloud freigegeben sind. Um zugelassen zu werden, muss ein Advertiser die [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) und stellen ein Tag auf ihren Websites bereit. Anschließend können Sie die Zielgruppen in [!DNL Google Ads] Kampagnen als Kampagnen- oder Anzeigengruppenebene [targets](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) oder [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager-Segmente (Opt-in-Funktion) Sie können [erstellen [!DNL Google Ads] Zielgruppen für Kundenabgleich](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) aus Audience Manager-Segmenten mit &quot;Search&quot;, &quot;Social&quot;und &quot;Commerce&quot;als Ziel. Dies kann Folgendes umfassen: [!DNL Analytics] Segmente, die in Adobe Experience Cloud veröffentlicht werden, und Segmente, die mithilfe der Adobe Experience Cloud-Zielgruppenbibliothek erstellt werden. Anschließend können Sie die Zielgruppen in [!DNL Google Ads] Kampagnen als Kampagnen- oder Anzeigengruppenebene [targets](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) oder [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

   Siehe[Adobe Advertising-Integrationen mit Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot;.

* Adobe Target - Sie können die Clickthrough-Signalfreigabe zwischen Search, Social, &amp; Commerce und [!DNL Target], richten Sie eine A/B-Test-Aktivität in ein. [!DNL Target] für Ihre Anzeigen und verwenden Sie dann [!DNL Analytics] Analysis Workspace zum Anzeigen der Testdaten.

* Adobe Campaign - Sie können [Erstellen und Aktualisieren einer [!DNL Google Ads] Zielgruppe für die Kundenabstimmung mithilfe einer E-Mail-Liste in [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud-Benachrichtigungen (wenn Sie über Adobe Experience Cloud angemeldet sind) Über den Benachrichtigungslink ([Warnhinweis-Benachrichtigungen](/help/search-social-commerce/assets/notifications-panel.png "Warnhinweis-Benachrichtigungen")) oben auf jeder Seite können Sie alle Adobe Experience Cloud-Systemaktualisierungen, Beiträge, Erwähnungen und freigegebenen Assets anzeigen. Wenden Sie sich an Ihr Adobe Account Team, um Informationen zum Zugriff auf Adobe Experience Cloud zu erhalten.

