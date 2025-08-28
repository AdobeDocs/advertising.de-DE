---
title: Voraussetzungen für die Integration von Adobe Advertising mit Customer Journey Analytics
description: Voraussetzungen für die Integration von Adobe Advertising mit Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: 194675147b64af37de6373116f246f1e61388a23
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Voraussetzungen für die Integration von Adobe Advertising mit Customer Journey Analytics

*Werbetreibende mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

* Werbetreibende mit [!DNL Analytics for Advertising] und Customer Journey Analytics:

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [Alle anderen Voraussetzungen für [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md).

* Werbetreibende mit Customer Journey Analytics, aber nicht [!DNL Analytics for Advertising]:

   * Adobe Experience Platform Web SDK-Bibliothek: `alloy.js`

     Die für Web SDK und für das Adobe Advertising Advertiser-Konto verwendete [!DNL Org ID] muss identisch sein. Diese ID finden Sie auf der [Registerkarte Zusammenfassung des Adobe Experience Cloud Debuggers](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=de).

     ![Übersichtsbildschirm des Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

     Sie benötigen die Unterstützung Ihres Experience Platform-Site-Administrators, um einen Experience Platform-Datenstrom und ein XDM-Schema zu erstellen.

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     Sie benötigen die Unterstützung Ihres internen Web-Analysten, um eine Verbindung zu Ihrem Datensatz herzustellen und Berichte zu konfigurieren.

>[!TIP]
>
>Verwenden Sie zum Verbessern der Datengenauigkeit die neueste Version jeder Bibliothek.

>[!MORELIKETHIS]
>
>* [Übersicht](overview.md)
>* (Adobe Analytics-Benutzer) [Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
