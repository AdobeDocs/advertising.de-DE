---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Feld „Weiterleitungstyp“ in den Konto- und Kampagneneinstellungen

**[!UICONTROL Redirect Type]:** (Nur für [!UICONTROL EF Redirect]) Die Methode, mit der Endbenutzer zur endgültigen URL oder Ziel-URL weitergeleitet werden. Die ausgewählte Option gilt für alle Anzeigen, Keywords und Platzierungen im Konto oder in der Kampagne. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen, und die Standardeinstellung auf Kampagnenebene wird von den Kontoeinstellungen übernommen.

* *[!UICONTROL Standard]:* Um den Endbenutzer einfach zur angegebenen URL umzuleiten.

* *[!UICONTROL Token]:* Um den Endbenutzer zur URL umzuleiten und auch die ID für Suche, Social und Commerce für den Klick (`ef_id`) als Abfragezeichenfolgenparameter aufzuzeichnen, der als Token verwendet wird. Wählen Sie diese Option aus, wenn Sie Offline-Transaktionen melden, Search, Social und Commerce Daten mit Adobe Analytics austauschen sollen oder alle Konversionen verfolgen möchten, die in [!DNL Apple Safari] Browsern auftreten.

**Hinweise:**

* Wenn Sie von [!UICONTROL Standard] zu [!UICONTROL Token] oder umgekehrt wechseln, müssen Sie die Tracking-URLs für das Konto neu generieren.
* Die Einstellung auf Kontoebene kann auf Kampagnenebene außer Kraft gesetzt werden.
