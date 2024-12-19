---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---
# Benutzerdefinierte Parameter in den Kampagneneinstellungen für GPL und MS, Einstellungen für MS-Anzeigengruppen und Einstellungen für MS Multimedia und responsive Anzeigen

**[!UICONTROL Custom Parameters]:** (optional; gilt nur für Audience-Kampagnen für [!DNL Microsoft Advertising]) Name-Wert-Paare für bis zu drei benutzerdefinierte Parameter. Die maximale Länge für Namen beträgt 16 alphanumerische Zeichen; die maximale Länge für Werte beträgt 200 Zeichen, einschließlich eingebetteter Parameter.

Sie können Ihre benutzerdefinierten Parameternamen in die Tracking-Vorlagen für die Entität und ihre untergeordneten Entitäten aufnehmen. Wenn ein(e) Benutzende(r) auf eine relevante Anzeige klickt, ersetzt das Anzeigennetzwerk den Parameternamen durch den definierten Parameterwert. Wenn Sie beispielsweise einen `{_color}=red` für Kundenparameter erstellen und Ihre Tracking-Vorlage `http://tracker.example.com/?color={_color}&u={lpurl}` enthält, wird beim Klicken auf eine Anzeige „Rot“ in den Farbparameter eingefügt.

Benutzerdefinierte Parameter auf Anzeigengruppen- oder (nur [!DNL Microsoft Advertising]) Anzeigenebene überschreiben die Kampagnenebene
Benutzerdefinierte Parameter mit demselben Namen.
