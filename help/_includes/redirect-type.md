---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Feld Umleitungstyp in Konto- und Kampagneneinstellungen

**[!UICONTROL Redirect Type]:** (Für [!UICONTROL EF Redirect] nur) Die Methode, mit der Endbenutzer zur endgültigen URL oder Ziel-URL weitergeleitet werden. Die ausgewählte Option gilt für alle Anzeigen, Suchbegriffe und Platzierungen in dem Konto oder der Kampagne. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen und die Standardeinstellung auf Kampagnenebene wird von den Kontoeinstellungen übernommen.

* *[!UICONTROL Standard]:* So leiten Sie den Endbenutzer einfach zur angegebenen URL weiter.

* *[!UICONTROL Token]:* So leiten Sie den Endbenutzer zur URL um und zeichnen die Such-, Social- und Commerce-ID für den Klick auf (`ef_id`) als Abfragezeichenfolgenparameter, der als Token verwendet wird. Wählen Sie diese Option aus, wenn Sie Offline-Transaktionen melden, von Search, Social und Commerce Daten mit Adobe Analytics austauschen möchten oder alle Konversionen verfolgen möchten, die in [!DNL Apple Safari] Browser.

**Hinweise:**

* Wenn Sie von [!UICONTROL Standard] nach [!UICONTROL Token]oder umgekehrt, müssen Sie Tracking-URLs für das Konto neu generieren.
* Sie können die Einstellung auf Kontoebene auf Kampagnenebene überschreiben.
