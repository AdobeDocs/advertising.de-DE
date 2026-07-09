---
title: Fehlerbehebung bei Adobe Advertising-Daten in Customer Journey Analytics
description: Erfahren Sie, wie Sie Probleme mit Adobe Advertising-Daten in Customer Journey Analytics beheben.
feature: Integration with Adobe Customer Journey Analytics
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: cb1e07d89c0d8107fce38695b73352cd57246879
workflow-type: tm+mt
source-wordcount: 716
ht-degree: 0%

---

# Fehlerbehebung bei Adobe Advertising-Daten in Customer Journey Analytics

Im Folgenden finden Sie mögliche Datenprobleme und deren Ursachen.

## Zusammenfassende Berichte

+++ In Customer Journey Analytics sind keine zusammenfassenden Berichtsdaten für Advertising DSP oder Advertising Search, Social und Commerce verfügbar.

Überprüfen Sie Folgendes:

* Customer Journey Analytics Workspace verweist auf die richtige Datenansicht.

* Der Feed von Adobe Advertising an Customer Journey Analytics ist aktiviert. Wenden Sie sich an Ihr Adobe-Accountteam.

* Ihre Adobe Advertising-Dimension/Ihr Klassifizierungs-/Lookup-Datensatz und Ihr Zusammenfassungsdatensatz sind in Ihrer Customer Journey Analytics-Verbindung enthalten.

* Ihre Adobe Advertising-Dimensionen und Zusammenfassungsmetriken sind in Ihrer Customer Journey Analytics-Datenansicht enthalten.

Wenn Sie alle oben genannten Einstellungen überprüfen, aber immer noch keine Zusammenfassungsdaten sehen, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support).

+++

+++ Zusammenfassende Berichtsdaten sind in Customer Journey Analytics für Advertiser 1 verfügbar, nicht jedoch für Advertiser 2.

Überprüfen Sie Folgendes:

* Der Feed von Adobe Advertising an Customer Journey Analytics ist für Advertiser 2 aktiviert. Wenden Sie sich an Ihr Adobe-Accountteam.

* Die Einstellung &quot;[!UICONTROL Backfill all existing data]&quot; ist für Ihre drei Datensätze (Dimension/Klassifizierung/Suche, Zusammenfassung und Ereignismetriken) in TRICs in Ihrer Customer Journey Analytics-Verbindung aktiviert.

Wenn Sie alle oben genannten Bedingungen überprüfen, aber immer noch keine Zusammenfassungsdaten sehen, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support).

+++

+++ (Benutzer von Search, Social und Commerce) Zusammenfassende Berichtsdaten sind in Customer Journey Analytics für ein [!DNL Google Ads]-, [!DNL Meta Ads]- oder [!DNL Microsoft Advertising]-Konto verfügbar, jedoch nicht für ein anderes.

Stellen Sie sicher, dass der Feed von Adobe Advertising an Customer Journey Analytics für das spezifische Werbenetzwerkkonto aktiviert ist. Wenden Sie sich an Ihr Adobe-Accountteam.

Wenn der Feed für ein Konto aktiviert ist, aber immer noch keine Zusammenfassungsdaten angezeigt werden, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support). Fügen Sie die [!UICONTROL Account ID] für das Anzeigennetzwerkkonto ein.

+++

+++ Zusammenfassende Berichtsdaten in Customer Journey Analytics Workspace unterscheiden sich von den Daten in Advertising DSP oder Advertising Search, Social und Commerce oder Zusammenfassungsdaten fehlen für einige Kampagnen- und Kampagnenentitäten.

Überprüfen Sie Folgendes:

* Sie verwenden dieselben Datumsbereiche sowohl in [!DNL Workspace] als auch im Adobe Advertising-Bericht.

* Alle Filter und Segmente, die in [!DNL Workspace] und im Adobe Advertising-Bericht angewendet werden, verursachen keine Datenunterschiede.

* Der [!UICONTROL Time Zone] für Ihre Customer Journey Analytics-Datenansicht entspricht dem [[!UICONTROL Default Timezone] für Ihr Advertising DSP-Konto](/help/dsp/admin/user-own-profile-edit.md).

* Die Einstellung &quot;[!UICONTROL Backfill all existing data]&quot; ist für Ihre drei Datensätze (Dimension/Klassifizierung/Suche, Zusammenfassung und Ereignismetriken) in TRICs in Ihrer Customer Journey Analytics-Verbindung aktiviert.

Wenn Sie sich einer Datendiskrepanz sicher sind, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support). Fügen Sie die [!UICONTROL Account ID] für das Anzeigennetzwerkkonto ein.. Schließen Sie Screenshots und Tabellen ein, um die Diskrepanz zu zeigen. Ihr Adobe-Konto-Team kann den Daten-Feed bei Bedarf nachträglich korrigieren, um die Diskrepanz zu beheben.

+++

## Reporting auf Ereignisebene

+++ Konversionsdaten (z. B. `Page Views`) sind für eine Reporting-Dimension (z. B. `Campaign`) in CJA Customer Journey Analytics Workspace nicht verfügbar.

Überprüfen Sie Folgendes, beginnend mit den Elementen mit den geringsten Hindernissen für die Überprüfung:

* Sie verwenden die richtige Datenansicht.

* Die entsprechenden Konversionsmetriken sind Web-/Online-Ereignisse, die Adobe Advertising Dimensionen zuordnen kann.

* Adobe Advertising verfolgt Clickthroughs und Viewthroughs auf der entsprechenden Site. <!-- Link to validation instructions in the user guide -->

* In der Customer Journey Analytics-Verbindung für den Klassifizierungsdatensatz sind die Werte für die [!DNL Key]- und [!DNL Matching Key] korrekt: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* Der [!DNL Adobe Advertising]-Service wird dem Adobe Experience Platform-Datenstrom hinzugefügt, das zugeordnete Schema für den Datenstrom wird `XDM ExperienceEvent Schema` und die Feldergruppe `Adobe Advertising Cloud ExperienceEvent Full Extension` wird dem `XDM ExperienceEvent` hinzugefügt.

* Die Adobe Advertising-Einstellungen werden in der WebSDK-Erweiterung korrekt konfiguriert und veröffentlicht.

Wenn Sie alle oben genannten Einstellungen überprüfen, aber immer noch keine Konversionsdaten sehen, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support). Fügen Sie die [!UICONTROL Account ID] für das Anzeigennetzwerkkonto ein.

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [Übersicht](overview.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Customer Journey Analytics]](ids.md)
>* [Voraussetzungen](prerequisites.md)
>* [Einrichten von Datenerfassung, Datenübertragung und Reporting](set-up.md)
>* [Adobe Advertising-Metriken und -Dimensionen in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Adobe Analytics-Benutzer) [Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
