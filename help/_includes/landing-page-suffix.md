---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---
# Feld für das Landingpage-Suffix in den GPL- und MS-Kontoeinstellungen, Kampagneneinstellungen und einigen Anzeigeneinstellungen

**[!UICONTROL Landing Page Suffix]:** (Nur [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten; optional) Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen; Schließen Sie alle Parameter ein, die Ihr Unternehmen verfolgen muss. Beispiel: `param1=value1&param2=value2`

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klickkennung des Werbenetzwerks (`gclid` für [!DNL Google Ads] oder `msclkid` für [!DNL Microsoft Advertising]) im Suffix enthalten.

Konten mit einer Adobe Analytics-Integration müssen den Parameter s_kwcid verwenden. Wenn das Konto über eine serverseitige Implementierung von s_kwcid verfügt, wird der Parameter automatisch hinzugefügt, wenn ein Benutzer auf eine Anzeige klickt. Andernfalls müssen Sie ihn hier manuell hinzufügen. Siehe die [erforderlichen Suffixformate für Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderlichen Suffixformate für Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Hinweise:**

* Dieses Feld wird von der Einstellung „Tracking [!UICONTROL Auto Upload]&quot; nicht aktualisiert.

* Landingpage-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Zur einfacheren Wartung verwenden Sie nur das Suffix auf Kontoebene, es sei denn, eine andere Nachverfolgung für einzelne Kontokomponenten ist erforderlich. Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den Editor des Anzeigennetzwerks.
