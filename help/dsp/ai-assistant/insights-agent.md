---
title: Erstellen von Berichten mit dem KI-Assistenten
description: Erfahren Sie, wie Sie mit dem Insights-Agenten des Adobe Advertising DSP-KI-Assistenten Kampagnenmetriken abfragen, Berichte generieren und CSV-Dateien herunterladen können.
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
source-git-commit: ffe7424d4e225a95b279b06a7df3b85bf0cbcdbf
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%
---
# Erstellen von Berichten mit dem KI-Assistenten

*Beta-Funktion*

Verwenden Sie den Insights-Agenten des KI-Assistenten, um Metriken und vollständige Berichte für Ihre Kampagnen, Kampagnenkomponenten, Advertising Creative-Erlebnisse, Werbetreibenden und Anzeigenziele zu erhalten, ohne manuell einen Bericht zu erstellen. Sie können einfache Fragen zu einer bestimmten Metrik stellen, z. B. Ausgaben oder CPA für eine Kampagne, oder einen komplexeren Bericht für eine bestimmte Dimension (z. B. eine einzelne Kampagne oder Zielgruppe) oder über Dimensionen hinweg (Aufschlüsselungen für jede Kampagne und jeden Advertiser) anfordern. Sie können die Ergebnisse als CSV-Datei herunterladen.

>[!IMPORTANT]
>
>KI-generierte Antworten können ungenau oder irreführend sein. Überprüfen Sie die Antworten und Quellen immer, bevor Sie sie für Entscheidungen verwenden, die sich auf Kosten oder Aufwand auswirken.

## Beispielabfragen

* Wie viel hat [Campaign Name] letzte Woche ausgegeben?

* Wie viele Konversionen hat [Campaign Name] in diesem Monat erhalten?

* CPA nach Paket anzeigen für [Kampagnenname].

* Welche Platzierungen liegen um mehr als 20 % zurück?

* Vergleichen Sie die Nettoausgaben für alle Kampagnen und Pakete in den letzten 15 Tagen.

## Senden einer Abfrage

Sie können mehrere Fragen in einer Nachricht stellen, aber nur jeweils eine Nachricht. Warten Sie auf eine Antwort, bevor Sie eine weitere senden.

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Agent-Chat](/help/dsp/assets/agent-chat.png "Agent-Chat").

1. Erstellen Sie die Abfrage:

   1. Führen Sie einen der folgenden Schritte aus:

      * Geben Sie Ihre eigene Abfrage ein.

      * So zeigen Sie Beispiele für Abfragen an:

        1. Klicken Sie auf **[!UICONTROL Insights]** , um den Abschnitt zu erweitern.

        1. (Optional) So kopieren Sie den Text einer Beispielabfrage in das Eingabefeld:

           1. Klicken Sie auf das Beispiel.

           1. (Optional) Bearbeiten Sie den Text entsprechend Ihren Anforderungen.

   1. (Optional) Um Ihre Abfrage auf einen bestimmten Dimensionswert zu konzentrieren (z. B. auf eine bestimmte Kampagne), fügen Sie optional den Cursor an die Stelle ein, an der der Dimensionswert angezeigt werden soll. Klicken Sie auf ![Entität erwähnen](/help/dsp/assets/prompt-entity.png "Entität erwähnen"), wählen Sie die Dimension aus und wählen Sie dann den Dimensionswert aus.

      Beispielsweise können Sie für den [!UICONTROL Campaign] Dimension aus einer Liste aller Kampagnen auswählen, über die Sie einen Bericht erstellen möchten.

      Zu den verfügbaren Dimensionen gehören:

      * Kampagnenentitäten: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
      * Der Werbetreibende: [!UICONTROL Advertiser]
      * Advertising Creative-Entitäten: [!UICONTROL Experience]
      * Anzeigenziele: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

   Weitere Informationen zu Abfragen finden Sie unter &quot;[&#x200B; Practices zum Schreiben von Abfragen und Eingabeaufforderungen](ai-assistant-about.md#writing-queries).

1. Klicken Sie ![Abfrage senden](/help/dsp/assets/submit-prompt.png "Abfrage senden") oder drücken Sie die **Eingabetaste** auf der Tastatur. Wenn der Agent zusätzliche Informationen anfordert, geben Sie die erforderlichen Informationen ein.

   Die ersten Zeilen des Berichts werden mit Links zur Vorschau des vollständigen Berichts und zum Herunterladen des Berichts angezeigt.

   Einige Zeilen des generierten Berichts werden angezeigt.

>[!TIP]
>
>Wenn Sie nach einem anderen Problem oder einem anderen Paket oder einer anderen Platzierung fragen möchten, [&#x200B; Sie eine neue Unterhaltung &#x200B;](#conversation-new).

## Herunterladen oder Vorschau eines vollständigen Berichts aus der Chatbox

* Um eine Kopie des vollständigen Berichts herunterzuladen, klicken Sie auf ![Export](/help/dsp/assets/download.png "Export").

  Die Datei wird als [!DNL Microsoft Excel] kommagetrennte Wertedatei (.csv) gemäß dem normalen Verfahren Ihres Browsers heruntergeladen. Der Dateiname lautet &quot;DSP_Insights_Report_&lt;job_number>&quot;.

* Um den vollständigen Bericht in einem Seitenbereich in der Vorschau anzuzeigen, klicken Sie auf ![Vorschau](/help/dsp/assets/agent-chat-preview.png "Vorschau"). Um den Bericht aus der Vorschau herunterzuladen, klicken Sie auf ![Export](/help/dsp/assets/download.png "Export").

  Wenn Sie den Bericht herunterladen, wird er als [!DNL Microsoft Excel] Datei mit kommagetrennten Werten (.csv) gemäß dem normalen Verfahren Ihres Browsers heruntergeladen. Der Dateiname lautet &quot;DSP_Insights_Report_&lt;job_number>&quot;.

## Neue Unterhaltung beginnen {#conversation-new}

Jede Konversation oder jeder Abfrage-Thread wird separat gespeichert, sodass Sie zwischen Ihren vorherigen Konversationen unterscheiden können.

1. Klicken Sie oben im [chatbox](#ai-assistant-open) auf ![Neue Konversation beginnen](/help/dsp/assets/new-selection.png "eine neue Konversation beginnen").

1. [Senden einer Abfrage](#query-submit).

## Chatbox erweitern und minimieren

1. Klicken Sie oben im [chatbox](#ai-assistant-open) auf ![Vollbild aufrufen](/help/dsp/assets/fullscreen.png "Vollbild aufrufen") um in den Vollbildmodus zu wechseln.

1. Um die Chatbox wieder in den Bedienfeldmodus zu versetzen, klicken Sie auf **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [Über den KI-Assistenten in Advertising DSP](ai-assistant-about.md)
>* [Arbeiten Sie mit früheren KI-Assistenten-Konversationen](previous-conversations.md)
