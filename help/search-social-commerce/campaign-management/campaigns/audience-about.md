---
title: Über Zielgruppen
description: Erfahren Sie mehr über Optionen zum Nachverfolgen, Erstellen und Verwalten  [!DNL Google Ads]  und  [!DNL Microsoft Advertising]  Zielgruppen.
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/B77S28vEpSkrgNmhc-Ekn7PXh3W-y2g9et2y3gCQPK8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 0%

---

# Über die Verwaltung von [!DNL Google Ads] und [!DNL Microsoft Advertising] Zielgruppen in Search, Social und Commerce

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising]*

Die Zielgruppenbibliothek listet alle Ihre [!DNL Google Ads] kundendatenbasierten, marktinternen und ähnlichen Zielgruppen sowie Ihr [!DNL Microsoft Advertising] Remarketing und dynamisches Remarketing, benutzerdefiniert, Kundenabgleich, marktinterne und ähnliche Zielgruppen auf. Sie können jede der [!DNL Google Ads] Zielgruppen als [!DNL Google Ads] auf Kampagnenebene und Anzeigengruppenebene Ziele und Ausschlüsse verwenden. Darüber hinaus können Sie jede der [!DNL Microsoft Advertising] Zielgruppen als Zielgruppen [!DNL Microsoft Advertising] Kampagnenebene und Anzeigengruppenebene und (nur dynamische Remarketing-Zielgruppen) Ausschlüsse verwenden. Sie können eine Angebotsanpassung für jede Zielgruppe hinzufügen oder bearbeiten.

Sie können Zielgruppen auch mithilfe von Segmenten oder E-Mail-Listen aus Ihren bestehenden Adobe CX Enterprise-Zielgruppen und aus verschiedenen Arten von Kundendaten aus Ihrem CRM-System (Customer Relationship Management) erstellen und verwalten:

* **Adobe-Zielgruppensegmente:** Werbetreibende mit angemeldeten Adobe Audience Manager- oder Adobe Analytics-Konten können Zielgruppen für [!DNL Google Ads] Kundenabgleich aus ihren [!DNL Adobe] Segmenten erstellen:

   * (Werbetreibende mit [!DNL Analytics], die nicht auch über Audience Manager verfügen) Sie können Zielgruppen für [!DNL Google Ads] Kundenabgleich mit Benutzer-IDs aus [!DNL Analytics] Segmenten erstellen, die für Adobe CX Enterprise freigegeben sind.

   * [!DNL Google Ads] (Werbetreibende mit Audience Manager-Konten) Sie können Zielgruppen für den Kundenabgleich mithilfe von Benutzer-IDs aus Audience Manager-Segmenten erstellen, die Search, Social und Commerce als Ziel haben. Dazu können Adobe Analytics-Segmente gehören, die in Adobe CX Enterprise veröffentlicht werden, und Segmente, die mit der Adobe CX Enterprise-Zielgruppenbibliothek erstellt wurden.

  Um Zielgruppen für den Kundenabgleich zu erstellen, muss das [!DNL Google Ads] des Werbetreibenden ([&#x200B; für benutzerdefinierte Abgleiche) &#x200B;](https://support.google.com/adspolicy/answer/6299717) und für (Benutzer[ID-Segmente) &#x200B;](https://support.google.com/google-ads/answer/9199250) sein. Außerdem muss das Advertiser-Konto in Search, Social und Commerce so konfiguriert sein, dass Zielgruppen für den Kundenabgleich erstellt werden können.

  [!DNL Adobe] Segmentdaten und Cookie-Synchronisierungsdateien für kundendatenbasierte Zielgruppen werden täglich mit [!DNL Google Ads] synchronisiert.

* **Adobe Campaign-E-Mail-Listen:** Ihr Adobe-Accountteam kann Sie beim Einrichten eines Workflows unterstützen, um eine Zielgruppe für den [!DNL Google Ads]-Kundenabgleich aus einer E-Mail-Liste in [!DNL Campaign] zu erstellen und zu aktualisieren.

* **Kundendatenlisten:** Werbetreibende mit [!DNL Google Ads]- oder [!DNL Microsoft Advertising]-Konten, die für den Kundenabgleich infrage kommen, können eine Anzeigennetzwerk-spezifische kundendatenbasierte Zielgruppe &lt;!— oder dynamische Remarketing-Zielgruppe — die in der kundendatenbasierten Zielgruppe enthalten ist, erstellen und aktualisieren, zumindest für [!DNL Google Ads]?—> indem sie eine CSV-Datei mit primären Kennungen hochladen.

* **Dynamische Remarketing-Listen:** Werbetreibende mit [!DNL Microsoft Advertising]-Konten können dynamische Remarketing-Zielgruppen erstellen und verwalten, mit denen Sie potenzielle Kunden, die kürzlich auf unterschiedliche Weise mit Ihren Produkten interagiert haben (z. B. Produkt-Viewer oder frühere Käufer), erneut ansprechen können. Für dynamische Remarketing-Zielgruppen müssen Sie das JavaScript-Konversions- und Zielgruppen-Tracking-Tag des Anzeigennetzwerks auf Ihren Web-Seiten verwenden. Verwenden Sie dynamische Remarketing-Listen mit Shopping-Kampagnen in den Such- und Zielgruppennetzwerken, um Zielgruppen mit Produktanzeigen erneut anzusprechen, sowie mit Suchkampagnen, um Zielgruppen mit Textanzeigen und dynamischen Suchanzeigen erneut anzusprechen. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Angebotsmodifikatoren für dynamische Remarketing-Audience-Ziele werden in Portfolios mit der Einstellung &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot; nicht optimiert.

>[!NOTE]
>
>Search, Social und Commerce speichern keine Kundendaten, die Sie hochladen, oder aus den [!DNL Adobe] Segmenten, die zum Erstellen oder Bearbeiten einer [!DNL Google Ads] oder [!DNL Microsoft Advertising] Zielgruppe verwendet werden.

>[!MORELIKETHIS]
>
>* [Erstellen [!DNL Google Ads] Kundenabgleich von Zielgruppen aus [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Erstellen einer Zielgruppe  [!DNL Google Ads]  Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Verwalten von Zielgruppen für den Kundenabgleich mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
>* [Dynamische Remarketing-Audiences verwalten](audience-dynamic-remarketing-manage.md)
>* [Verwalten von Zielgruppenzielen für Kampagnen und Anzeigengruppen](audience-targets-manage.md)
>* [Verwalten von Zielgruppenausschlüssen für Kampagnen und Anzeigengruppen](audience-exclusions-manage.md)
