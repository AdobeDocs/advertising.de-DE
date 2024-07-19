---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---
# Feld &quot;Benutzerdefinierte Parameter&quot;in den GGL- und MS-Kampagneneinstellungen, den MS-Anzeigengruppeneinstellungen sowie den MS-Einstellungen für Multimedia und responsive Anzeigen

**[!UICONTROL Custom Parameters]:** (Optional; gilt nur für Zielgruppenkampagnen für [!DNL Microsoft Advertising]) Name- und Wertpaare für bis zu drei benutzerdefinierte Parameter. Die maximale Länge für Namen beträgt 16 alphanumerische Zeichen. Die maximale Länge für Werte beträgt 200 Zeichen, einschließlich eingebetteter Parameter.

Sie können Ihre benutzerdefinierten Parameternamen in die Tracking-Vorlagen für die Entität und ihre untergeordneten Entitäten aufnehmen. Wenn ein Benutzer auf eine relevante Anzeige klickt, ersetzt das Werbenetzwerk den Parameternamen durch den definierten Parameterwert. Wenn Sie beispielsweise den Kundenparameter `{_color}=red` erstellen und Ihre Tracking-Vorlage `http://tracker.example.com/?color={_color}&u={lpurl}` enthält, wird beim Klicken auf eine Anzeige im Farbparameter &quot;Rot&quot;eingefügt.

Benutzerdefinierte Parameter auf Anzeigengruppe oder ([!DNL Microsoft Advertising] nur) Anzeigenebene überschreiben die Kampagnenebene
benutzerdefinierte Parameter mit demselben Namen.
