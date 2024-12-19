---
source-git-commit: 24aa1afe9611ca6ae46795c9bca2964e1d9c4f97
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---
# Feld „Geräte“ in den Einstellungen für GPL und MS-Kampagnen und Anzeigengruppen

**[!UICONTROL Devices]:** (Optional; nicht verfügbar für Kampagnen mit [!DNL Google Ads] Performance Max oder [!DNL Microsoft Advertising] Video- oder CTV-Videoanzeigen) Konfigurieren Sie Angebotsanpassungen für verschiedene Gerätetypen als Prozentsatz des Angebots auf Keyword-Ebene. Wenn beispielsweise das Gebot auf Keyword-Ebene 1 USD und die Gebotsanpassung für Smartphones 50 % beträgt, beträgt das Smartphone-Gebot 1,50 USD. Standardmäßig werden keine Werte eingegeben (Gebotsanpassung = 0) und alle Geräte werden auf Keyword-Ebene geboten.

Gültige Prozentsätze können [!DNL Google Ads] -100 für Smartphones und Tablets (d. h. keine Gebote für den Gerätetyp) und -90 bis 900 für alle Gerätetypen umfassen.

Gültige Prozentsätze können [!DNL Microsoft Advertising] Folgendes umfassen:

* Smartphones und Tablets: -100 (nicht zu bieten für den Gerätetyp) und von -90 bis 900
* Desktop: von 0 bis 900

>[!NOTE]
>* Die Einstellungen auf Anzeigengruppenebene setzen die Einstellungen auf Kampagnenebene außer Kraft. Wenn Sie jedoch ein Gerät auf Kampagnenebene ausschließen, können Sie den Ausschluss nicht auf Anzeigengruppenebene überschreiben.
>* Wenn Sie diese Kampagne einem standardoptimierten Portfolio zuweisen, bestimmt Search, Social und Commerce automatisch das grundlegende Gebot auf Keyword-Ebene, damit das Portfolio sein Ziel erreichen kann. Das Anzeigennetzwerk passt dann das Angebot wie für verschiedene Gerätetypen angegeben an.
>* (Für alle Kampagnen/Anzeigengruppen mit Ausnahme von [!DNL Microsoft Advertising] Anzeigengruppen im Zielgruppennetzwerk) Wenn Sie diese Kampagne einem standardmäßigen optimierten Portfolio zuweisen, das auf &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot; konfiguriert ist, ändert die Optimierungsfunktion die angegebenen Geräteangebotsanpassungen auf Anzeigengruppenebene, solange der ideale Wert, den sie berechnet, unter die in den Portfolioeinstellungen angegebenen Mindest- und Höchstwerte fällt und die Anzeigengruppe Gebote für den Gerätetyp nicht ausschließt.
