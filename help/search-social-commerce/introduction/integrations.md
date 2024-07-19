---
title: Integration mit Adobe Experience Cloud-Lösungen und -Diensten
description: Erfahren Sie mehr über die Integration von Search, Social und Commerce mit Adobe Experience Cloud-Lösungen und -Diensten.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Integration mit Adobe Experience Cloud-Lösungen und -Diensten

Advertising Search, Social und Commerce ist in die folgenden [!DNL Adobe] -Produkte integriert.

* [Tags aus Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) - Sie können die [Adobe Advertising Cloud-Erweiterung](https://exchange.adobe.com/apps/ec/100155) für Adobe Experience Platform verwenden, um Adobe Advertising-Konversions-Tracking-Tags sowie Tracking-Tags von Drittanbietern für Ihre Anzeigen-Landingpages zu erstellen. (Sie können auch [Konversions-Tracking-Tags direkt in Search, Social und Commerce erstellen](/help/search-social-commerce/tools/conversion-tag-generate.md).) Wenden Sie sich an Ihr Adobe Account-Team oder Implementierungsteam, um Informationen zu erhalten, die in Ihre Tags aufgenommen werden sollen.

* Adobe Analytics - (Opt-in-Funktion) Adobe Advertising und [!DNL Analytics] sind wie folgt integriert:

   * Adobe Advertising und [!DNL Analytics] geben Daten nahtlos frei. [!DNL Analytics] kann Site-Interaktions- und Konversionsdaten täglich an Search, Social und Commerce senden, wo die Daten für die Anzeigenoptimierung und für die Berichterstellung verfügbar sind. Außerdem kann Adobe Advertising Daten zum Anzeigen-Traffic - einschließlich Impressionen, Klicks und Kosten - täglich von Ihren Werbenetzwerken an [!DNL Analytics] senden, wo die Daten in allen Reporting-Tools verfügbar sind.

     Weitere Informationen zur Unterstützung von [!DNL Analytics] für jedes Anzeigennetzwerk und jeden Anzeigentyp finden Sie unter &quot;[Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md)&quot;. Weitere Informationen zum Datenaustausch finden Sie unter &quot;[Überblick über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot;.

     Zum Datenaustausch müssen zunächst sowohl Adobe Advertising als auch [!DNL Analytics] konfiguriert werden. Wenden Sie sich an Ihr Adobe-Account-Team, um weitere Informationen zur Ersteinrichtung zu erhalten.

     >[!NOTE]
     >
     >Standardmäßig sind die Metriken &quot;[!DNL Analytics]&quot;nicht in den Bildschirmen &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;sichtbar. Sie müssen die Metriken explizit [in Kampagnenverwaltungsansichten, Portfolios und Berichten zur Verfügung stellen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md), nachdem das Implementierungsteam von [!DNL Adobe] Standardereignisse oder benutzerspezifische Ereignisse für die Weiterleitung an Adobe Advertising konfiguriert hat. Sie können optional die angezeigten Metriknamen ändern (ohne sie in [!DNL Analytics] zu ändern). Sie können Metriken in der Benutzeroberfläche sichtbar machen und Metriken von [!UICONTROL Admin] > [!UICONTROL Conversions] umbenennen.

   * Werbetreibende mit [!DNL Analytics], jedoch nicht Audience Manager, können [Kundenabgleich-Zielgruppen ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) aus [!DNL Analytics] Segmenten erstellen, die für Adobe Experience Cloud freigegeben sind.  [!DNL Google Ads]  Um zugelassen zu werden, muss ein Advertiser den [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) implementieren und ein Tag auf seinen Websites bereitstellen. Anschließend können Sie die Zielgruppen in [!DNL Google Ads] Kampagnen als Ziele auf Kampagnenebene oder auf Anzeigengruppenebene [Ziele](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) oder [Ausschlüsse](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) verwenden.

* Adobe Audience Manager-Segmente - (Opt-in-Funktion) Sie können [Kundenabgleichzielgruppen erstellen [!DNL Google Ads] aus Audience Manager-Segmenten, die &quot;Search&quot;, &quot;Social&quot;und &quot;Commerce&quot;als Ziel haben. ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) Dies kann [!DNL Analytics] -Segmente umfassen, die in Adobe Experience Cloud veröffentlicht werden, sowie Segmente, die mit der Adobe Experience Cloud-Zielgruppenbibliothek erstellt werden. Anschließend können Sie die Zielgruppen in [!DNL Google Ads] Kampagnen als Ziele auf Kampagnenebene oder auf Anzeigengruppenebene [Ziele](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) oder [Ausschlüsse](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) verwenden.

  Weitere Informationen finden Sie unter &quot;[Adobe Advertising-Integrationen mit Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot;.

* Adobe Target - Sie können die Clickthrough-Signalfreigabe zwischen Search, Social und Commerce und [!DNL Target] implementieren, eine A/B-Test-Aktivität in [!DNL Target] für Ihre Anzeigen einrichten und dann [!DNL Analytics] Analysis Workspace verwenden, um die Testdaten anzuzeigen.

* Adobe Campaign - Sie können [eine  [!DNL Google Ads] Kundenabgleichs-Zielgruppe mithilfe einer E-Mail-Liste in  [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md) erstellen und aktualisieren.

* Adobe Experience Cloud-Benachrichtigungen - (Wenn Sie über Adobe Experience Cloud angemeldet sind) Über den Benachrichtigungslink ([Warnhinweis-Benachrichtigungen](/help/search-social-commerce/assets/notifications-panel.png "Warnhinweis-Benachrichtigungen")) oben auf jeder Seite können Sie alle Adobe Experience Cloud-Systemaktualisierungen, Beiträge, Erwähnungen und freigegebenen Assets anzeigen. Wenden Sie sich an Ihr Adobe-Account-Team, um Informationen über den Zugriff auf Adobe Experience Cloud zu erhalten.
