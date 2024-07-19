---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---
# Feld für automatisches Hochladen in Konto- und Kampagneneinstellungen

**[!UICONTROL Auto Upload]:** (Nur für synchronisierte Kampagnen mit [!UICONTROL EF Redirect]) Lädt Folgendes automatisch in das Anzeigennetzwerk hoch, wenn sich Search, Social und Commerce das nächste Mal damit synchronisieren: a) Suchen, Social und Commerce-Tracking-Parameter für Tracking-Vorlagen und dieselben Parameter, die an die endgültigen URLs angehängt sind, oder b) neue Ziel-URLs, die mit dem Tracking-Code von Search, Social und Commerce eingebettet sind. Bei Advertisern mit einer [Adobe Advertising-Adobe Analytics-Integration](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) und einer serverseitigen AMO-ID-Konfiguration (s_kwcid) enthält der Upload auch [AMO-ID-Parameter](/help/integrations/analytics/ids.md#amo-id) für Ihre [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen. Sie können die Einstellung auf Kontoebene auf Kampagnenebene überschreiben.

**Hinweis:** Tracking-URLs werden täglich nur für nicht synchronisierte Entitäten aktualisiert (d. h. neue Entitäten, die hinzugefügt wurden, und vorhandene Entitäten, deren Eigenschaften sich geändert haben). Wenn Sie diese Einstellung von deaktiviert auf aktiviert für einen vorhandenen Advertiser/Konto/eine vorhandene Kampagne ändern, werden die Tracking-URLs nicht für vorhandene Entitäten aktualisiert, die bereits synchronisiert sind. Wenden Sie sich an Ihr Adobe-Account-Team und fordern Sie eine einmalige, manuelle Synchronisierung an, um Tracking zu den URLs vorhandener, synchronisierter Entitäten hinzuzufügen. Der automatische Upload-Prozess verarbeitet zukünftige Änderungen.
