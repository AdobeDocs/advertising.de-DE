---
title: Fehlerbehebung bei Leistungs- und Versandproblemen mit dem KI-Assistenten
description: Verwenden Sie den Fehlerbehebungsagenten des Adobe Advertising DSP-KI-Assistenten, um Ausgaben-, Geschwindigkeits- und Bereitstellungsprobleme für DSP-Pakete und -Platzierungen zu diagnostizieren.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 0f6d32b5409cc95f09d0b0f28cdeee72a7861892
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%
---
# Fehlerbehebung bei Leistungs- und Bereitstellungsproblemen mit dem KI-Assistenten

*Beta-Funktion*

*Support nur für Englisch*

Der Agent zur Fehlerbehebung des KI-Assistenten identifiziert Faktoren, die die Leistung von Live-Paketen und -Platzierungen einschränken, und bietet schrittweise Anweisungen und Empfehlungen, die auf historischen Daten basieren, um Probleme zu beheben. Der Fehlerbehebungsagent kann bei der Diagnose der folgenden Arten von Leistungs- und Bereitstellungsproblemen helfen:

* (Nur Platzierungen) Ausgabenprobleme, einschließlich zu hoher Ausgaben, zu geringer Ausgaben und Ausgabenüberschreitung. Der Agent bewertet die damit verbundenen Faktoren für Geschwindigkeit, Gebote, Targeting und Budgetbegrenzung als Teil der Diagnose.

* (Nur Pakete) Leistungsprobleme, einschließlich steigender CPA oder sinkender ROAS. Der Agent diagnostiziert keine Interaktionsmetriken wie CTR, CPC, Klicks oder Impressionen.

Jedes Gespräch behandelt eine einzelne Diagnose für ein einzelnes Paket oder eine einzelne Platzierung. Sobald der Agent ein Ergebnis geliefert hat, beginnen Sie ein neues Gespräch, um Fragen zu einem anderen Problem oder zu einem anderen Paket oder einer anderen Platzierung zu stellen.

Der Agent kann keine Einstellungen ändern, Kampagnen oder Kampagnenkomponenten erstellen oder bearbeiten oder Probleme für ein pausiertes, abgeschlossenes, archiviertes oder geplantes Paket oder eine Platzierung diagnostizieren.

>[!IMPORTANT]
>
>KI-generierte Antworten können ungenau oder irreführend sein. Überprüfen Sie die Antworten und Quellen immer, bevor Sie sie für Entscheidungen verwenden, die sich auf Kosten oder Aufwand auswirken.

## Beispielabfragen

### Fehlerbehebung bei Problemen mit Platzierungsausgaben

* Meine Platzierung hat gestern aufgehört zu verbringen, obwohl der Deal aktiv ist. Warum?

* Warum wurde für diese Platzierung in den letzten 5 Tagen nicht genügend Geld ausgegeben?

* Wir haben die Hälfte des Fluges hinter uns und sind deutlich schneller. Warum?

### Fehlerbehebung bei Problemen mit der Paketleistung

* Warum wurde die CPA für dieses Paket in den letzten Wochen erhöht?

* Warum lehnt die ROAS bei diesem Paket ab?

## Senden einer Abfrage über den KI-Assistenten

Sie können mehrere Fragen in einer Nachricht stellen, aber nur jeweils eine Nachricht. Warten Sie auf eine Antwort, bevor Sie eine weitere senden.

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Agent-Chat](/help/dsp/assets/agent-chat.png "Agent-Chat").

1. Erstellen Sie die Abfrage:

   * Geben Sie Ihre eigene Abfrage ein.

   * Um Beispiele für Abfragen anzuzeigen, klicken Sie auf **[!UICONTROL Troubleshoot]** , um den Abschnitt zu erweitern.

     1. (Optional) So kopieren Sie den Text einer Beispielabfrage in das Eingabefeld:

        1. Klicken Sie auf das Beispiel.

        1. (Optional) Bearbeiten Sie den Text entsprechend Ihren Anforderungen.

   Weitere Informationen zu Abfragen finden Sie unter &quot;[&#x200B; Practices zum Schreiben von Abfragen und Eingabeaufforderungen](ai-assistant-about.md#writing-queries).

   >[!NOTE]
   >
   >* Wenn Sie keinen Datumsbereich angeben, wählt der Agent je nach Problemtyp einen angemessenen Standardwert aus. Wenn Sie beispielsweise nach Kampagnenmetriken fragen, ohne einen Datumsbereich anzugeben, gelten die Ergebnisse für die Dauer der Kampagne.
   >* Wenn Sie eine Ziel-CPA im Sinn haben, schließen Sie diese in Ihre Abfrage ein (z. B. „Diagnose der CPA mit einem Ziel von 50 USD„). Wenn Sie keine angeben, verwendet der Agent ein Standardziel.

1. Klicken Sie ![Abfrage senden](/help/dsp/assets/submit-prompt.png "Abfrage senden") oder drücken Sie die **Eingabetaste** auf der Tastatur.

1. Wenn der KI-Assistent Sie um zusätzliche Informationen bittet, geben Sie diese an.

>[!TIP]
>
>Wenn Sie nach einem anderen Problem oder einem anderen Paket oder einer anderen Platzierung fragen möchten, [&#x200B; Sie eine neue Unterhaltung &#x200B;](#conversation-new).

## Senden einer Abfrage über die [!UICONTROL Packages]- oder [!UICONTROL Placements]

Sie können mehrere Fragen in einer Nachricht stellen, aber nur jeweils eine Nachricht. Warten Sie auf eine Antwort, bevor Sie eine weitere senden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Führen Sie einen der folgenden Schritte aus:

   * (Für Pakete) Klicken Sie in der [!UICONTROL Packages] auf **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** neben dem Paketnamen.

   * (Für Platzierungen) Klicken Sie im Untermenü auf **[!UICONTROL Placements]**. Klicken Sie neben dem Platzierungsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Erstellen Sie die Abfrage:

   * Geben Sie Ihre eigene Abfrage ein.

   * Um Beispiele für Abfragen anzuzeigen, klicken Sie auf **[!UICONTROL Troubleshoot]** , um den Abschnitt zu erweitern.

     1. (Optional) So kopieren Sie den Text einer Beispielabfrage in das Eingabefeld:

        1. Klicken Sie auf das Beispiel.

        1. (Optional) Bearbeiten Sie den Text entsprechend Ihren Anforderungen.

   Weitere Informationen zu Abfragen finden Sie unter &quot;[&#x200B; Practices zum Schreiben von Abfragen und Eingabeaufforderungen](ai-assistant-about.md#writing-queries).

   >[!NOTE]
   >
   >* Wenn Sie keinen Datumsbereich angeben, wählt der Agent je nach Problemtyp einen angemessenen Standardwert aus. Wenn Sie beispielsweise nach Kampagnenmetriken fragen, ohne einen Datumsbereich anzugeben, gelten die Ergebnisse für die Dauer der Kampagne.
   >* Wenn Sie eine Ziel-CPA im Sinn haben, schließen Sie diese in Ihre Abfrage ein (z. B. „Diagnose der CPA mit einem Ziel von 50 USD„). Wenn Sie keine angeben, verwendet der Agent ein Standardziel.

1. Klicken Sie ![Abfrage senden](/help/dsp/assets/submit-prompt.png "Abfrage senden") oder drücken Sie die **Eingabetaste** auf der Tastatur.

1. Wenn der KI-Assistent Sie um zusätzliche Informationen bittet, geben Sie diese an.

>[!TIP]
>
>Wenn Sie nach einem anderen Problem oder einem anderen Paket oder einer anderen Platzierung fragen möchten, [&#x200B; Sie eine neue Unterhaltung &#x200B;](#conversation-new).

## Neue Unterhaltung beginnen {#conversation-new}

Jede Konversation (oder jeder Abfrage-Thread) wird separat gespeichert, sodass Sie zwischen Ihren vorherigen Konversationen unterscheiden können.

1. Klicken Sie oben im [chatbox](#ai-assistant-open) auf ![Neue Konversation beginnen](/help/dsp/assets/new-selection.png "eine neue Konversation beginnen").

1. [Senden einer Abfrage](#query-submit).

## Chatbox erweitern und minimieren

1. Klicken Sie oben im [chatbox](#ai-assistant-open) auf ![Vollbild aufrufen](/help/dsp/assets/fullscreen.png "Vollbild aufrufen") um in den Vollbildmodus zu wechseln.

1. Um die Chatbox wieder in den Bedienfeldmodus zu versetzen, klicken Sie auf **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [Über den KI-Assistenten in Advertising DSP](ai-assistant-about.md)
>* [Arbeiten Sie mit früheren KI-Assistenten-Konversationen](previous-conversations.md)
