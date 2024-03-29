---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---
# Feld &quot;Suffix der Einstiegsseite&quot;in den GGL- und MS-Kontoeinstellungen, den Kampagneneinstellungen und einigen Anzeigeneinstellungen

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] und [!DNL Microsoft Advertising] Nur Konten; optional) Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen. Schließen Sie alle Parameter ein, die Ihr Unternehmen verfolgen muss. Beispiel: `param1=value1&param2=value2`

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klick-ID des Anzeigennetzwerks enthalten (`gclid` für [!DNL Google Ads] oder `msclkid` für [!DNL Microsoft Advertising]) im Suffix.

Konten mit einer Adobe Analytics-Integration müssen den Parameter s_kwcid verwenden. Wenn das Konto über eine serverseitige s_kwcid-Implementierung verfügt, wird der Parameter automatisch hinzugefügt, wenn ein Benutzer auf eine Anzeige klickt. Andernfalls müssen Sie sie hier manuell hinzufügen. Siehe [erforderliche Suffix-Formate für Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderliche Suffix-Formate für Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Hinweise:**

* Dieses Feld wird nicht von der [!UICONTROL Auto Upload] Tracking-Einstellung.

* Die Suffixe der Landingpage auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Verwenden Sie den Editor des Werbenetzwerks, um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren.
