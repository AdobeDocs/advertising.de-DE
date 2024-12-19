---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Feld „Tracking-Typ“ in den Konto- und Kampagneneinstellungen

**[!UICONTROL Tracking Type]:** Die Methode, mit der URLs generiert werden:

* *[!UICONTROL EF Redirect]* (Standard): Für Clients, die den Adobe Advertising-Konversionsverfolgungs-Service verwenden möchten. Diese Methode generiert eindeutige Klick-Tracking-IDs und leitet Benutzende zu Tracking-Zwecken an den Adobe Advertising-Server weiter, bevor sie an die Landingpage des Clients gesendet werden.

  Diese Methode verfügt über standardmäßige Tracking-Optionen, die Sie optional anpassen können, und Sie können auch Parameter angeben, die an jede URL angehängt werden sollen.

* *[!UICONTROL No EF Redirect]:* Für Kunden, die nur ihre eigenen Klick-Trackingcodes verwenden möchten. Search, Social und Commerce bieten keine Klick-Tracking-IDs oder Umleitungs-Codes. Bei Konten mit Ziel-URLs ist jede Ziel-URL mit der Basis-URL identisch.

  **Hinweise:**

   * Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzer können diesen Wert ändern.
   * Wenn Sie die Tracking-Methode ändern, müssen Sie die Tracking-URLs für das Konto neu generieren.
   * Tracking-Optionen auf Kampagnenebene setzen Einstellungen auf Kontoebene außer Kraft.
