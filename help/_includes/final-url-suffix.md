---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Endgültige URL-Suffix-Definition

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** (Nur [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten; optional) Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen; Schließen Sie alle Parameter ein, die Ihr Unternehmen verfolgen muss. Beispiel:`param1=value1&param2=value2`

Bei Konten, die das Adobe Advertising-Konversions-Tracking verwenden, muss das Suffix die Klick-Kennung des Werbenetzwerks enthalten (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für [!DNL Google Ads]).

Konten mit einer Adobe Analytics-Integration müssen den Parameter [AMO ID](/help/integrations/analytics/ids.md) verwenden. Wenn das Konto über eine serverseitige AMO ID-Implementierung verfügt, wird der Parameter automatisch hinzugefügt, wenn ein Benutzer auf eine Anzeige klickt. Andernfalls müssen Sie ihn hier manuell hinzufügen. Siehe die [erforderlichen Suffixformate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderlichen Suffixformate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dieses Feld wird von der Einstellung „Tracking [!UICONTROL Auto Upload]&quot; nicht aktualisiert.
>* Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Zur einfacheren Wartung verwenden Sie nur das Suffix auf Kontoebene, es sei denn, eine andere Nachverfolgung für einzelne Kontokomponenten ist erforderlich. Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den Editor des Anzeigennetzwerks.
