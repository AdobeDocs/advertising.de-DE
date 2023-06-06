---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---
# Feld für automatisches Hochladen in Konto- und Kampagneneinstellungen

**[!UICONTROL Auto Upload]:** (Für synchronisierte Kampagnen mit [!UICONTROL EF Redirect] nur) Lädt bei der nächsten Synchronisierung von Search, Social und Commerce Folgendes automatisch in das Werbenetzwerk hoch: (a) Tracking-Parameter für Suche, Social und Commerce für Tracking-Vorlagen und dieselben Parameter, die an die endgültigen URLs angehängt sind, oder (b) neue Ziel-URLs, die mit dem Tracking-Code für Suche, Social und Commerce eingebettet sind. Für Advertiser mit einer [Adobe Advertising-Adobe Analytics-Integration](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) und einer serverseitigen s_kwcid-Konfiguration enthält der Upload auch s_kwcid-Parameter für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen. Sie können die Einstellung auf Kontoebene auf Kampagnenebene überschreiben.

**Hinweis:** Tracking-URLs werden täglich nur für Entitäten aktualisiert, die nicht synchronisiert sind (d. h. neue Entitäten, die hinzugefügt wurden, und vorhandene Entitäten, deren Eigenschaften geändert wurden). Wenn Sie diese Einstellung von deaktiviert auf aktiviert für einen vorhandenen Advertiser/Konto/eine vorhandene Kampagne ändern, werden die Tracking-URLs nicht für vorhandene Entitäten aktualisiert, die bereits synchronisiert sind. Wenden Sie sich an Ihr Adobe Account Team und fordern Sie eine einmalige manuelle Synchronisierung an, um Tracking zu den URLs vorhandener, synchronisierter Entitäten hinzuzufügen. Der automatische Upload-Prozess verarbeitet zukünftige Änderungen.
