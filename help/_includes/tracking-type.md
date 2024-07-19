---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Feld Trackingtyp in Konto- und Kampagneneinstellungen

**[!UICONTROL Tracking Type]:** Die Methode, mit der URLs generiert werden:

* *[!UICONTROL EF Redirect]* (Standard): Für Clients, die den Adobe Advertising-Konversions-Tracking-Dienst verwenden möchten. Diese Methode erzeugt eindeutige Klick-Tracking-IDs und leitet Benutzer zu Tracking-Zwecken zum Adobe Advertising-Server weiter, bevor sie zur Landingpage des Clients gesendet werden.

  Diese Methode verfügt über standardmäßige Tracking-Optionen, die Sie optional anpassen können. Außerdem können Sie Parameter angeben, die an jede URL angehängt werden sollen.

* *[!UICONTROL No EF Redirect]:* Für Kunden, die nur ihre eigenen Klick-Trackingcodes verwenden möchten. Search, Social und Commerce bieten keine Klick-Tracking-IDs oder Umleitungs-Codes. Bei Konten mit Ziel-URLs ist jede Ziel-URL mit der Basis-URL identisch.

  **Notizen:**

   * Dieser Wert kann nur von Agenturkontomanagern, Adobe-Kontomanagern und Administratorbenutzern geändert werden.
   * Wenn Sie die Tracking-Methode ändern, müssen Sie die Tracking-URLs für das Konto neu generieren.
   * Tracking-Optionen auf Kampagnenebene überschreiben Einstellungen auf Kontoebene.
