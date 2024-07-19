---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Endgültige URL-Suffix-Definition

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] und [!DNL Microsoft Advertising] Konten nur; optional) Alle Parameter, die an das Ende der endgültigen URLs angehängt werden, um Informationen zu verfolgen; schließen Sie alle Parameter ein, die Ihr Unternehmen verfolgen muss. Beispiel:`param1=value1&param2=value2`

In Konten, die das Adobe Advertising-Konversions-Tracking verwenden, muss das Suffix die Klick-ID des Anzeigennetzwerks enthalten (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für [!DNL Google Ads]).

Konten mit einer Adobe Analytics-Integration müssen den Parameter [AMO ID](/help/integrations/analytics/ids.md) verwenden. Wenn das Konto über eine serverseitige AMO-ID-Implementierung verfügt, wird der Parameter automatisch hinzugefügt, wenn ein Benutzer auf eine Anzeige klickt. Andernfalls müssen Sie sie hier manuell hinzufügen. Siehe die erforderlichen Suffix-Formate für  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderliche Suffix-Formate für  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).[

>[!NOTE]
>
>* Dieses Feld wird nicht durch die Tracking-Einstellung [!UICONTROL Auto Upload] aktualisiert.
>* Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Verwenden Sie den Editor des Werbenetzwerks, um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren.
