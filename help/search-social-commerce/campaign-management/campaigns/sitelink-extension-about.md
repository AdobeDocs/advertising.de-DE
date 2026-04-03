---
title: Über Sitelink-Erweiterungen
description: Informationen zu Sitelink-Erweiterungen.
exl-id: c2d96440-62da-4b57-a98e-d7b94882d6c5
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/lOrTOUXOFT7cvY5cEilRiROSfIbmcI9v8vU2MVZlg7U
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 344
ht-degree: 0%

---

# Über Sitelink-Erweiterungen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising]*

Ein Sitelink ist ein zusätzlicher Text-Link in einer Textanzeigenliste. Verwenden Sie Sitelinks, um Benutzer direkt zu bestimmten Seiten Ihrer Site zu führen. Das Anzeigennetzwerk bestimmt anhand der Relevanz des Sitelinks für die Anzeige, welche Sitelinks mit einer Anzeige angezeigt werden sollen. Optional können Sie für jeden Sitelink einen beschreibenden Text hinzufügen, der in der Anzeige enthalten sein kann. Das Werbenetzwerk kann automatisch eine Anzeigenkopie aus vorhandenen Anzeigen im Konto mit dem Sitelink anzeigen, wenn die Anzeigenkopie für den Sitelink von großer Bedeutung ist. [!DNL Google Ads] können 2-6 Sitelinks in einer Desktop-Anzeige und bis zu vier Sitelinks in einer Mobile-Anzeige angezeigt werden. [!DNL Microsoft Advertising] können zwei, vier oder sechs Sitelinks mit Beschreibungen oder 4-6 Sitelinks ohne Beschreibungen anzeigen.

Sie erstellen auf Kontoebene freigegebenen Sitelink-Text und Einstellungen, einschließlich der Daten, während derer die Sitelinks mit Anzeigen angezeigt werden können.

## Die [!UICONTROL Sitelinks]- und [!UICONTROL Associations]

In der [!UICONTROL Extensions] > [!UICONTROL Sitelinks] Bibliothek unter [!UICONTROL Campaigns] > [!UICONTROL Campaigns] werden alle Sitelinks auf Kontoebene aufgelistet. Dort können Sie Ihre freigegebenen Sitelinks erstellen und verwalten. In der Hilfe zum Anzeigennetzwerk finden Sie die maximale Anzahl von Anzeigenerweiterungen pro [[!DNL Google Ads] Konto](https://support.google.com/google-ads/answer/6372658) und pro [[!DNL Microsoft Advertising] Konto](https://help.ads.microsoft.com/#apex/3/en/52001). Sitelinks in Ihrer Bibliothek werden erst dann mit Ihren Anzeigen verwendet, wenn Sie sie Kontoentitäten zuweisen.

In der Ansicht [!UICONTROL Extensions] > [!UICONTROL Associations] können Sie allen Anzeigen auf Konto- (nur [!DNL Google Ads]), Kampagnen- oder Anzeigengruppenebene (nur [!DNL Google Ads]) beliebige Ihrer Sitelinks als mögliche Erweiterungen zuweisen.

## Leistungsdaten für Sitelinks

Search, Social und Commerce ordnen die Klicks auf eine Anzeigenerweiterung und die daraus resultierende Konversion dem Keyword zu, das mit der Anzeige verbunden ist, in der die Erweiterung enthalten ist. In Search, Social und Commerce sind keine Kosten- oder Klickdaten auf der Erweiterungs-Ebene verfügbar. In [der [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) können Sie jedoch erkennen, ob eine Transaktion aus einem Sitelink resultierte (und nicht aus der Anzeige selbst), wenn der Wert in der Spalte Linktyp als `sl:<Sitelink text>` aufgeführt ist, z. B. „sl:See Aktuelle Angebote“.

In [!DNL Google Ads] und [!DNL Microsoft Advertising] können Sie auf der Registerkarte [!DNL Ad Extensions] Kosten- und Klickdaten anzeigen.

>[!MORELIKETHIS]
>
>* [Verwalten freigegebener Sitelink-Erweiterungen](sitelink-extension-manage.md)
>* [Verknüpfen freigegebener Sitelink-Erweiterungen mit Kampagnen oder Anzeigengruppen](sitelink-extension-associate.md)
