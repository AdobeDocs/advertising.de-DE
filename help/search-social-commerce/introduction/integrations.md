---
title: Integration mit Adobe Experience Cloud-Lösungen und -Services
description: Erfahren Sie mehr über die Integration von Search, Social und Commerce mit Adobe Experience Cloud-Lösungen und -Services.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Integration mit Adobe Experience Cloud-Lösungen und -Services

Advertising Search, Social und Commerce ist mit den folgenden [!DNL Adobe] Produkten integriert.

* [Tags aus Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) - Sie können die [Adobe Advertising Cloud-Erweiterung](https://exchange.adobe.com/apps/ec/100155) für Adobe Experience Platform verwenden, um Adobe Advertising-Konversionsverfolgungstags sowie Verfolgungstags von Drittanbietern für Ihre Anzeigeneinstiegsseiten zu erstellen. (Sie können auch [Konversionsverfolgungstags direkt in Search, Social und Commerce erstellen](/help/search-social-commerce/tools/conversion-tag-generate.md).) Wenden Sie sich an Ihr Adobe-Account-Team oder Implementierungsteam, um Informationen zu erhalten, die in Ihre Tags aufgenommen werden sollen.

* Adobe Analytics - (Opt-in-Funktion) Adobe Advertising und [!DNL Analytics] werden wie folgt integriert:

   * Adobe Advertising und [!DNL Analytics] nahtlos Daten gemeinsam nutzen. [!DNL Analytics] können Daten zu Website-Interaktion und Konversion täglich an Search, Social und Commerce senden, wo die Daten zur Anzeigenoptimierung und für das Reporting zur Verfügung stehen. Außerdem kann Adobe Advertising Anzeigen-Traffic-Daten - einschließlich Impressionen, Klicks und Kosten - täglich von Ihren Werbenetzwerken an [!DNL Analytics] senden, wo die Daten in allen Reporting-Tools verfügbar sind.

     Siehe &quot;[Unterstütztes Inventar](/help/search-social-commerce/introduction/supported-inventory.md)&quot; für weitere Informationen zur [!DNL Analytics] Unterstützung für jedes Werbenetzwerk und jeden Anzeigentyp. Siehe auch &quot;[Überblick über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"} für weitere Informationen zum Datenaustausch.

     Um Daten auszutauschen, müssen zunächst sowohl Adobe Advertising als auch [!DNL Analytics] konfiguriert werden. Wenden Sie sich an Ihr Adobe-Kundenbetreuungsteam, um weitere Informationen zur Ersteinrichtung zu erhalten.

     >[!NOTE]
     >
     >Standardmäßig sind die [!DNL Analytics] Metriken auf den Bildschirmen „Suche“, „Social“ und &quot;Commerce&quot; nicht sichtbar. Sie müssen die [ explizit in Kampagnenverwaltungsansichten, Portfolios und Berichten verfügbar machen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) nachdem das [!DNL Adobe] Implementierungsteam ausgewählte Standard- oder benutzerdefinierte Ereignisse konfiguriert hat, die an das Adobe Advertising übergeben werden sollen. Sie können optional die angezeigten Metriknamen ändern (ohne sie in [!DNL Analytics] zu ändern). Sie können Metriken in der Benutzeroberfläche anzeigen lassen und Metriken unter [!UICONTROL Admin] > [!UICONTROL Conversions] umbenennen.

   * Werbetreibende mit [!DNL Analytics], aber nicht mit dem Audience Manager können [Zielgruppen  [!DNL Google Ads]  Kundenabgleich erstellen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) aus [!DNL Analytics] Segmenten erstellen, die für Adobe Experience Cloud freigegeben sind. Um berechtigt zu sein, muss ein Advertiser den [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) implementieren und ein Tag auf seinen Websites bereitstellen. Anschließend können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen (Zielgruppen) oder Ausschlüsse (Ausschlüsse) auf Kampagnenebene [&#128279;](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) [ Anzeigengruppe ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager-Segmente - (Opt-in-Funktion) Sie können Zielgruppen [erstellen [!DNL Google Ads] Kundenabgleich](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) aus Audience Manager-Segmenten erstellen, die „Search“, „Social“ und Commerce als Ziel haben. Dies kann [!DNL Analytics] Segmente umfassen, die in Adobe Experience Cloud veröffentlicht werden, sowie Segmente, die mithilfe der Adobe Experience Cloud-Zielgruppenbibliothek erstellt wurden. Anschließend können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen (Zielgruppen) oder Ausschlüsse (Ausschlüsse) auf Kampagnenebene [&#128279;](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) [ Anzeigengruppe ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Weitere Informationen finden Sie unter &quot;[Adobe Advertising-Integrationen ](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html) Adobe Audience Manager&quot;.

* Adobe Target - Sie können die Clickthrough-Signalfreigabe zwischen Search, Social, Commerce und [!DNL Target] implementieren, eine A/B-Testaktivität in [!DNL Target] für Ihre Anzeigen einrichten und dann [!DNL Analytics] Analysis Workspace verwenden, um die Testdaten anzuzeigen.

* Adobe Campaign - Sie können [eine Zielgruppe für den Kundenabgleich erstellen  [!DNL Google Ads]  aktualisieren, indem Sie eine E-Mail-Liste in  [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud-Benachrichtigungen - (Wenn Sie über Adobe Experience Cloud angemeldet sind) Über den Benachrichtigungslink ([Warnhinweise](/help/search-social-commerce/assets/notifications-panel.png "Warnhinweise")) oben auf jeder Seite können Sie alle Adobe Experience Cloud-Systemaktualisierungen, -Beiträge, -Erwähnungen und freigegebenen Assets anzeigen. Wenden Sie sich an Ihr Adobe-Konto-Team , um Informationen über den Zugriff auf Adobe Experience Cloud zu erhalten.
