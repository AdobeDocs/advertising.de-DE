---
title: Integration mit Adobe Experience Cloud-Lösungen und -Services
description: Erfahren Sie mehr über die Integration von Search, Social und Commerce mit Adobe Experience Cloud-Lösungen und -Services.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Integration mit Adobe Experience Cloud-Lösungen und -Services

Advertising Search, Social und Commerce ist mit den folgenden [!DNL Adobe] Produkten integriert.

* [Tags aus Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) - Sie können die [Adobe Advertising Cloud-Erweiterung](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) für Adobe Experience Platform verwenden, [Konversionsverfolgungstags für Adobe Advertising ](/help/search-social-commerce/tools/conversion-tag-generate.md) sowie Verfolgungstags von Drittanbietern für Ihre Anzeigenlandingpages zu erstellen. Wenn Ihr Unternehmen kein Experience Platform-Konto hat, können Sie die Erweiterung trotzdem direkt in der [Benutzeroberfläche für die Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/#/data-collection/) installieren, die Adobe Experience Cloud-Kunden kostenlos zur Verfügung steht.

  Wenden Sie sich zur Installation der erforderlichen Erweiterung an Ihren Organisationsadministrator, um Zugriff auf die Datenerfassungsfunktionen in der Benutzeroberfläche zu erhalten, und bitten Sie ihn, Ihnen die `manage_properties` zu gewähren.

  **Hinweis:** Sie können auch Konversionsverfolgungstags [ Search, Social und Commerce erstellen](/help/search-social-commerce/tools/conversion-tag-generate.md).

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics - (Opt-in-Funktion) Adobe Advertising und [!DNL Analytics] werden wie folgt integriert:

   * Adobe Advertising und [!DNL Analytics] nahtlos Daten gemeinsam nutzen. [!DNL Analytics] können Daten zu Website-Interaktion und Konversion täglich an Search, Social und Commerce senden, wo die Daten zur Anzeigenoptimierung und für das Reporting zur Verfügung stehen. Außerdem kann Adobe Advertising Daten zu Anzeigen-Traffic, einschließlich Impressionen, Klicks und Kosten, täglich von Ihren Werbenetzwerken an [!DNL Analytics] senden, wo die Daten in allen Reporting-Tools verfügbar sind.

     Siehe &quot;[Unterstütztes Inventar](/help/search-social-commerce/introduction/supported-inventory.md)&quot; für weitere Informationen zur [!DNL Analytics] Unterstützung für jedes Werbenetzwerk und jeden Anzeigentyp. Siehe auch &quot;[Überblick über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"} für weitere Informationen zum Datenaustausch.

     Um Daten auszutauschen, müssen zunächst sowohl Adobe Advertising als auch [!DNL Analytics] konfiguriert werden. Weitere Informationen zur Ersteinrichtung erhalten Sie von Ihrem Adobe Account Team.

     >[!NOTE]
     >
     >Standardmäßig sind die [!DNL Analytics] Metriken auf den Bildschirmen „Suche“, „Social“ und &quot;Commerce&quot; nicht sichtbar. Sie müssen die [ explizit in Kampagnenverwaltungsansichten, Portfolios und Berichten verfügbar machen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) nachdem das [!DNL Adobe] Implementierungsteam Standardereignisse oder benutzerdefinierte Ereignisse konfiguriert hat, die an Adobe Advertising übergeben werden sollen. Sie können optional die angezeigten Metriknamen ändern (ohne sie in [!DNL Analytics] zu ändern). Sie können Metriken in der Benutzeroberfläche anzeigen lassen und Metriken unter [!UICONTROL Admin] > [!UICONTROL Conversions] umbenennen.

   * Werbetreibende mit [!DNL Analytics], aber nicht mit Audience Manager können [Zielgruppen  [!DNL Google Ads]  Kundenabgleich erstellen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) aus [!DNL Analytics] Segmenten erstellen, die mit Adobe Experience Cloud geteilt werden. Um berechtigt zu sein, muss ein Advertiser den [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) implementieren und ein Tag auf seinen Websites bereitstellen. Anschließend können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen (Zielgruppen) oder Ausschlüsse (Ausschlüsse) auf Kampagnenebene [ ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) [ Anzeigengruppe ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager-Segmente - (Opt-in-Funktion) Sie können [Zielgruppen erstellen [!DNL Google Ads] Kundenabgleich durchführen](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) aus Audience Manager-Segmenten, die „Search“, „Social“ und Commerce als Ziel haben. Dies kann [!DNL Analytics] Segmente umfassen, die in Adobe Experience Cloud veröffentlicht werden, sowie Segmente, die mithilfe der Adobe Experience Cloud-Zielgruppenbibliothek erstellt wurden. Anschließend können Sie die Audiences in [!DNL Google Ads] Kampagnen als Zielgruppen (Zielgruppen) oder Ausschlüsse (Ausschlüsse) auf Kampagnenebene [ ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) [ Anzeigengruppe ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Weitere Informationen finden Sie unter &quot;[Adobe Advertising-Integrationen ](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html) Adobe Audience Manager&quot;.

* Adobe Target - Sie können die Clickthrough-Signalfreigabe zwischen Search, Social, Commerce und [!DNL Target] implementieren, eine A/B-Testaktivität in [!DNL Target] für Ihre Anzeigen einrichten und dann [!DNL Analytics] Analysis Workspace verwenden, um die Testdaten anzuzeigen.

* Adobe Campaign - Sie können [eine Zielgruppe für den Kundenabgleich erstellen  [!DNL Google Ads]  aktualisieren, indem Sie eine E-Mail-Liste in  [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud-Benachrichtigungen - (Wenn Sie über Adobe Experience Cloud angemeldet sind) Über den Benachrichtigungslink ([Warnhinweise](/help/search-social-commerce/assets/notifications-panel.png "Warnhinweise")) oben auf jeder Seite können Sie alle Adobe Experience Cloud-Systemaktualisierungen, -Beiträge, -Erwähnungen und freigegebenen Assets anzeigen. Wenden Sie sich an Ihr Adobe-Accountteam , um Informationen zum Zugriff auf Adobe Experience Cloud zu erhalten.
