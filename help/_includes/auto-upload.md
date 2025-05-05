---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---
# Feld „Automatischer Upload“ in den Konto- und Kampagneneinstellungen

**[!UICONTROL Auto Upload]:** (nur für synchronisierte Kampagnen mit [!UICONTROL EF Redirect]) Lädt beim nächsten Synchronisieren von Search, Social und Commerce automatisch Folgendes in das Werbenetzwerk hoch: (a) Tracking-Parameter für Search, Social und Commerce für Tracking-Vorlagen und dieselben Parameter, die an die endgültigen URLs angehängt werden, oder (b) neue Ziel-URLs, die in den Tracking-Code für Search, Social und Commerce eingebettet sind. Für Werbetreibende mit einer [Adobe Advertising-Adobe Analytics-Integration](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=de) und einer serverseitigen AMO-ID-Konfiguration (s_kwcid) enthält der Upload auch [AMO-ID-Parameter](/help/integrations/analytics/ids.md#amo-id) für Ihre [!DNL Google Ads]- und [!DNL Microsoft Advertising]. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen. Die Einstellung auf Kontoebene kann auf Kampagnenebene außer Kraft gesetzt werden.

**Hinweis:** Tracking-URLs werden täglich nur für Entitäten aktualisiert, die nicht synchronisiert sind (d. h. neue hinzugefügte Entitäten und vorhandene Entitäten, deren Eigenschaften geändert wurden). Wenn Sie diese Einstellung für einen vorhandenen Advertiser/ein vorhandenes Konto/eine vorhandene Kampagne von „Deaktiviert“ in „Aktiviert“ ändern, werden die Tracking-URLs daher nicht für vorhandene Entitäten aktualisiert, die bereits synchronisiert sind. Um Tracking zu den URLs vorhandener, synchronisierter Entitäten hinzuzufügen, wenden Sie sich an Ihr Adobe-Account-Team und fordern Sie einen einmaligen, manuellen Synchronisierungsprozess an. Der automatische Upload-Prozess handhabt zukünftige Änderungen.
