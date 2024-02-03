---
source-git-commit: 24aa1afe9611ca6ae46795c9bca2964e1d9c4f97
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---
# Gerätefeld in den Kampagnen- und Anzeigengruppeneinstellungen für GGL und MS

**[!UICONTROL Devices]:** (Optional; nicht verfügbar für [!DNL Google Ads] Leistungsmax-Kampagnen oder [!DNL Microsoft Advertising] Video- oder CTV-Videoanzeigen) Konfigurieren Sie Angebotsanpassungen für verschiedene Gerätetypen als Prozentsatz des Angebots auf Suchbegriffebene. Wenn das Angebot auf Suchbegriffebene beispielsweise 1 USD und die Angebotsanpassung für Smartphones 50 % beträgt, beträgt das Gebot für Smartphones 1,50 USD. Standardmäßig werden keine Werte eingegeben (Angebotsanpassung = 0) und alle Geräte werden beim Angebot auf Suchbegriffebene geboten.

Für [!DNL Google Ads], können gültige Prozentsätze -100 für Smartphones und Tablets (um kein Gebot für den Gerätetyp zu erhalten) und von -90 bis 900 für alle Gerätetypen umfassen.

Für [!DNL Microsoft Advertising], können gültige Prozentsätze Folgendes umfassen:

* Smartphones und Tablets: -100 (kein Gebot für den Gerätetyp) und von -90 bis 900
* Desktop: von 0 bis 900

>[!NOTE]
>* Die Einstellungen auf Anzeigengruppenebene überschreiben die Einstellungen auf Kampagnenebene. Wenn Sie jedoch ein Gerät auf Kampagnenebene ausschließen, können Sie den Ausschluss auf Anzeigengruppenebene nicht überschreiben.
>* Wenn Sie diese Kampagne einem standardoptimierten Portfolio zuweisen, bestimmt Search, Social und Commerce automatisch das grundlegende Angebot auf Suchbegriffebene, das dem Portfolio hilft, sein Ziel zu erreichen. Das Anzeigennetzwerk passt dann das Angebot an, wie für verschiedene Gerätetypen angegeben.
>* (Für alle Kampagnen/Anzeigengruppen außer [!DNL Microsoft Advertising] Anzeigengruppen im Zielgruppen-Netzwerk) Wenn Sie diese Kampagne einem standardoptimierten Portfolio zuweisen, das für konfiguriert ist.[!UICONTROL Auto-optimize Bid Adjustment Values],&quot;ändert die Optimierungsfunktion die angegebenen Gerätegebotsanpassungen auf Anzeigengruppenebene, sofern der von ihr berechnete ideale Wert innerhalb der in den Portfolioeinstellungen angegebenen Mindest- und Höchstwerte liegt und die Anzeigengruppe Gebote für den Gerätetyp nicht ausschließt.
