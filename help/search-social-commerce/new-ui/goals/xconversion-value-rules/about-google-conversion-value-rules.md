---
title: Über  [!DNL Google Ads] -Wertregeln
description: Erfahren Sie, wie Sie Konversionswertregeln  [!DNL Google Ads]  Search, Social und Commerce anzeigen und verwalten können.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Über [!DNL Google Ads] Konversionswertregeln

Search, Social und Commerce synchronisieren die [Konversionswertregeln](https://support.google.com/google-ads/answer/10518330) automatisch mit Ihren [!DNL Google Ads]. Mit Konversionswertregeln können Sie die Werte von Konversionsereignissen basierend auf Benutzerinformationen anpassen, einschließlich des Gerätetyps, des Standorts und des Zielgruppensegments. Sie können Regeln für wertbasierte Gebote in Kampagnen mit Suche, Anzeige, Shopping und Performance Max mit Google Smart Bidding verwenden. Bei Kampagnen mit den Gebotsstrategien Maximieren von Konversionen und Ziel-ROAS bevorzugen [!DNL Google Ads] Algorithmen ab sofort Konversionen mit einem höheren Wert.

Konversionswertregeln auf Kampagnenebene setzen Regeln auf Kontoebene außer Kraft. Wenn eine Konversion mehrere Konversionswertregeln erfüllt, wird nur eine der Regeln angewendet. Normalerweise wird die spezifischste Regel angewendet. Weitere Informationen finden Sie jedoch in der [[!DNL Google Ads] Dokumentation zu Prioritäten für die verschiedenen Regelbedingungstypen](https://support.google.com/google-ads/answer/10520348).

## Die [!UICONTROL Conversion Value Rules] Ansicht und Funktionalität

Alle in der [!DNL Google Ads] erstellten Regeln werden innerhalb von 24 Stunden synchronisiert und sind in der Ansicht [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules] verfügbar. Einige Konten können ihre Konversionswertregeln verwalten:

* In Konten, für die Konversionen auf individueller Konto- oder Kampagnenebene verfolgt werden, können Sie den Status Ihrer Regeln auf Konto- und Kampagnenebene erstellen, bearbeiten und ändern.

  Die Konten können zwar mit [!DNL Google Ads] Manager-Konten verknüpft werden, sie können jedoch kein kontenübergreifendes Konversions-Tracking verwenden (bei dem Konversionen über alle Konten im Manager-Konto hinweg verfolgt werden).

* In Konten, die das kontenübergreifende Konversionstracking verwenden, werden die Regeln auf Konto- und Kampagnenebene vom Manager-Konto übernommen und sind schreibgeschützt.

## Konversionswertregeln mit den Portfolios Suche, Social und Commerce

Wenn das Advertiser-Konto so konfiguriert ist, dass Search-, Social- und Commerce-Ziele in [!DNL Google Ads] hochgeladen werden, und Sie eine Kampagne einbeziehen, die eine Konversionswertregel in ein Portfolio mit einem Ziel verwendet, wendet [!DNL Google Ads] die Konversionswertregel auf den im Ziel angegebenen ursprünglichen Konversionswert an. Infolgedessen unterscheiden sich Konversionsdaten in Search, Social und Commerce von den Konversionsdaten in [!DNL Google Ads].

Angenommen, das Ziel verwendet eine einzige Konversionsmetrik „Leads“ und gibt Konversionen von Mobilgeräten das Gewicht 10 und Konversionen von Nicht-Mobilgeräten das Gewicht 10 an. Search, Social und Commerce zählen ein Ereignis aus einem der Gerätetypen als Konversion 1 (1) und schreiben den Konversionswert als 10 zu. Angenommen, eine Kampagne in diesem Portfolio verwendet eine Konversionswertregel: „Wenn das Gerät ein Mobilgerät ist, multiplizieren Sie sie mit 2.“ Wenn ein mobiles Leads-Ereignis für diese Kampagne verfolgt wird, schreibt [!DNL Google Ads] die Konversionszählung auch als eins (1), aber den Konversionswert als (10 x 2) = 20 zu.

Weitere Informationen zu Ihren Regeln, einschließlich der ursprünglichen Konversionswerte vor der Anwendung der Regeln, finden Sie [&#x200B; Bericht zu Konversionswertregeln in  [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

>[!MORELIKETHIS]
>
>* [Erstellen  [!DNL Google Ads]  Konversionswertregel](create-google-conversion-value-rule.md)
>* [Bearbeiten  [!DNL Google Ads]  Konversionswertregel](edit-google-conversion-value-rule.md)
>* [Ändern des Status  [!DNL Google Ads]  Konversionswertregel](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] Regeleinstellungen für Konversionswerte](google-conversion-value-rule-settings.md)

