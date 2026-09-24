---
title: Fehlerbehebung bei Leistungs- und Versandproblemen mit dem KI-Assistenten
description: Erfahren Sie, wie Sie mit dem Fehlerbehebungsagenten des KI-Assistenten Ausgaben-, Geschwindigkeits- und Versandprobleme für DSP-Pakete und -Platzierungen diagnostizieren können.
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
source-git-commit: 2e97652901e16bd1079fac445f9a2a4794dcda56
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%
---
# Fehlerbehebung bei Leistungs- und Bereitstellungsproblemen mit dem DSP-KI-Assistenten

Der Agent zur Fehlerbehebung des KI-Assistenten kann Faktoren identifizieren, die die Leistung einschränken, und bietet Empfehlungen zur Lösung von Problemen. Der Fehlerbehebungsagent kann:

* Hilfe bei der Diagnose von Leistungs- und Versandproblemen für ein ausgewähltes Live-Paket oder eine ausgewählte Platzierung:

  * (Nur Platzierungen) Ausgabenprobleme, einschließlich zu hoher Ausgaben, zu geringer Ausgaben und Ausgabenüberschreitung. Der Agent bewertet die damit verbundenen Faktoren für Geschwindigkeit, Gebote, Targeting und Budgetbegrenzung als Teil der Diagnose.

  * (Nur Pakete) Leistungsprobleme, einschließlich steigender CPA oder sinkender ROAS. Der Agent diagnostiziert keine Interaktionsmetriken wie CTR, CPC, Klicks oder Impressionen.

  Jedes Gespräch behandelt eine einzelne Diagnose für ein einzelnes Paket oder eine einzelne Platzierung. Sobald der Agent ein Ergebnis geliefert hat, beginnen Sie ein neues Gespräch, um Fragen zu einem anderen Problem oder zu einem anderen Paket oder einer anderen Platzierung zu stellen.

  Der Agent kann weder Einstellungen ändern noch Kampagnen oder Kampagnenkomponenten erstellen oder bearbeiten. Außerdem können keine Probleme für pausierte, abgeschlossene, archivierte oder geplante Pakete oder Platzierungen diagnostiziert werden.

* Suchen Sie im [Advertising DSP-Handbuch](/help/dsp/home.md) und (Werbetreibende mit Advertising Creative) im [Advertising Creative-Handbuch](/help/creative/home.md) auf dieselbe Weise wie in der [Benutzeroberfläche für Agenten-Chat](/help/dsp/agent-chat.md) nach konzeptionellen Inhalten und Anleitungen. Fragen Sie nach Kampagnenverwaltung, Optimierung, Zielgruppen-Management, Angeboten, Berichten und anderen Produktfunktionen.

>[!IMPORTANT]
>
>KI-generierte Antworten können ungenau oder irreführend sein. Überprüfen Sie die Antworten und Quellen immer, bevor Sie sie für Entscheidungen verwenden, die sich auf Kosten oder Aufwand auswirken.

## Beispielabfragen

>[!NOTE]
>
>Sie müssen keinen Datumsbereich angeben. Wenn Sie keine angeben, wählt der Agent je nach Problemtyp einen angemessenen Standardwert aus.

### Platzierungen: Ausgabenprobleme

* Meine Platzierung hat gestern aufgehört zu verbringen, obwohl der Deal aktiv ist. Warum?

* Warum wurde für diese Platzierung in den letzten 5 Tagen nicht genügend Geld ausgegeben?

* Wir haben die Hälfte des Fluges hinter uns und sind deutlich schneller. Warum?

### Pakete: Leistungsprobleme

* Warum wurde die CPA für dieses Paket in den letzten Wochen erhöht?

* Warum lehnt die ROAS bei diesem Paket ab?

>[!TIP]
>
>Wenn Sie eine Ziel-CPA im Sinn haben, schließen Sie diese in Ihre Abfrage ein (z. B. „Diagnose der CPA mit einem Ziel von 50 USD„). Wenn Sie keine angeben, verwendet der Agent ein Standardziel.

### Produktfunktionen:

* Wie erstelle ich eine Platzierung?

* Welche Zielgruppenbestimmungsoptionen sind in Adobe DSP verfügbar?

* Wie kann ich eine Anzeige an eine Platzierung anhängen?

* Welche Folgen hat die Verwendung der verschiedenen Schrittmachungsoptionen in den Platzierungseinstellungen?

* Wann sollte ich die einzelnen Optimierungsziele verwenden?

* Warum dienen programmgesteuerte garantierte (PG)-Platzierungen nicht für Impressionen?

* Welche Berichte enthalten Daten auf Haushaltsebene?

* Was ist der Unterschied zwischen einem zielgerichteten Erlebnis und einem nicht zielgerichteten Erlebnis in [!DNL Creative]?

* Wie erstelle ich ein Anzeigen-Tag für ein [!DNL Creative] Erlebnis?

## Senden einer Abfrage für ein Live-Paket oder eine Live-Platzierung

Sie können mehrere Fragen in einer Nachricht stellen, aber nur jeweils eine Nachricht. Warten Sie auf eine Antwort, bevor Sie eine weitere senden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Führen Sie einen der folgenden Schritte aus:

   * (Für Pakete) Klicken Sie in der [!UICONTROL Packages] auf **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** neben dem Paketnamen.

   * (Für Platzierungen) Klicken Sie im Untermenü auf **[!UICONTROL Placements]**. Klicken Sie neben dem Platzierungsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Geben Sie Ihre Abfrage ein und klicken Sie auf ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt").

   <!-- For more information, see "[Writing prompts](#writing-prompts)." -->

   Bei Leistungs- und Versandabfragen enthält die Antwort Faktoren, die die Leistung einschränken, und gibt Empfehlungen zur Lösung der Probleme.

   Bei Dokumentationsabfragen enthält die Antwort Inline-Zitate und unten eine **[!UICONTROL Documentation Sources]**. Es können auch Folgefragen und Vorschläge angezeigt werden.

1. (Nur Dokumentationsabfragen; optional) Führen Sie einen der folgenden Schritte aus, um eine Seite zu öffnen, die als Datenquelle verwendet wird:

   * Klicken Sie auf das nummerierte Zitat.

   * Klicken Sie auf **[!UICONTROL Documentation Sources]** , um eine Liste aller in der Antwort genannten Seiten anzuzeigen, und klicken Sie dann auf den Seitenlink.

1. (Optional) Bewerten Sie die Antwort mithilfe des Symbols „Daumen hoch“ oder „Daumen runter“.

>[!TIP]
>
>Wenn Sie nach einem anderen Problem oder einem anderen Paket oder einer anderen Platzierung fragen möchten, beginnen Sie ein neues Gespräch.
