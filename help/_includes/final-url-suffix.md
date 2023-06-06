---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Endgültige URL-Suffix-Definition

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] und [!DNL Microsoft Advertising] nur Konten; optional) Alle Parameter, die an das Ende der endgültigen URLs angehängt werden, um Informationen zu verfolgen; enthalten alle Parameter, die Ihr Unternehmen verfolgen muss. Beispiel:`param1=value1&param2=value2`

In Konten, die das Adobe Advertising-Konversions-Tracking verwenden, muss das Suffix die Klick-ID des Anzeigennetzwerks (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für [!DNL Google Ads]).

Konten mit einer Adobe Analytics-Integration müssen den Parameter s_kwcid verwenden. Wenn das Konto über eine serverseitige s_kwcid-Implementierung verfügt, wird der Parameter automatisch hinzugefügt, wenn ein Benutzer auf eine Anzeige klickt. ansonsten müssen Sie es hier manuell hinzufügen. Siehe [erforderliche Suffix-Formate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderliche Suffix-Formate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dieses Feld wird nicht von der [!UICONTROL Auto Upload] Tracking-Einstellung.
>* Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Verwenden Sie den Editor des Werbenetzwerks, um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren.

