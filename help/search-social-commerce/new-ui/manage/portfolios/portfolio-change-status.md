---
title: (Neue Benutzeroberfläche) Ändern des Status eines Portfolios
description: Erfahren Sie, wie Sie den Status eines Portfolios ändern oder ein inaktives Portfolio löschen können.
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 081453404883619e0a70bba080c857bf7e3136cc
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Ändern des Status eines Portfolios

*Beta-Funktion*

Der Status eines Portfolios kann einer der folgenden sein:

* **Inaktiv:** Die Optimierungsfunktion erfasst zu Berichtszwecken Kosten-/Klick-/Impressionsdaten für die relevanten Kampagnen, modelliert jedoch weder die Daten noch optimiert sie Kampagnenbudgets und Gebote.

* **Aktiv:** Die Optimierungsfunktion sammelt Kosten-/Klick-/Impressionsdaten und Umsatzdaten für die relevanten Kampagnen und modelliert die Daten, optimiert jedoch keine Kampagnenbudgets oder Gebote. Aktivieren Sie ein inaktives Portfolio, um mit der Datenmodellierung zu beginnen, oder stufen Sie ein optimiertes Portfolio in den aktiven Status herunter, um die Optimierung zu stoppen.

* **Optimiert:** Die Optimierungsfunktion sammelt Kosten-/Klick-/Impressionsdaten und Umsatzdaten für die relevanten Kampagnen, modelliert die Daten und optimiert Kampagnenbudgets und Gebote (sofern relevant) am festgelegten Portfolio-Startdatum. Das Ändern des Status in „Optimiert“ wird auch als Starten des Portfolios bezeichnet.

Wenn Sie nicht mehr Kosten-/Klick-/Impressionsdaten und Umsatzdaten für die entsprechenden Kampagnen erfassen möchten, löschen Sie das Portfolio. Durch Löschen eines Portfolios wird es in Search, Social und Commerce nicht mehr verfügbar.

Alle Änderungen am Portfoliostatus werden im Änderungsverlauf des Portfolios protokolliert.

## Portfolios optimieren, aktivieren oder deaktivieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Halten Sie den Cursor über der Portfoliozeile und klicken Sie ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") neben dem [!UICONTROL Portfolio Status].

1. Status ändern:

   * Um ein inaktives oder optimiertes Portfolio zu aktivieren, wählen Sie **[!UICONTROL Active]** aus.

   * Um ein aktives Portfolio zu deaktivieren, wählen Sie **[!UICONTROL Inactive]** aus.

   * Um ein aktives Portfolio zu optimieren (zu starten), wählen Sie **[!UICONTROL Optimized]** aus.

     >[!NOTE]
     >
     >* Sie können ein Portfolio nur starten, wenn es bereits aktiv ist und mindestens eine aktive Kampagne mit mindestens einer aktiven Anzeige und einem Keyword/einer aktiven Platzierung enthält.
     >* Bevor Sie ein Portfolio aufrufen, müssen Sie Konversionsverfolgungstags in den Web-Seiten des Werbetreibenden implementieren.
     >* Bevor Sie ein Portfolio starten, empfiehlt es sich, eine Basisanalyse durchzuführen.
     >* Wenn Sie ein neues Portfolio starten, stellen Sie sicher, dass das Startdatum heute oder später ist.>* Ändern Sie das Portfolio nicht in der ersten Woche nach dem Start, auch wenn die Leistung unbeständig ist.
     >* Sobald Search, Social und Commerce mit der Optimierung eines Portfolios beginnen, sollten Sie es alle zukünftigen Angebotsänderungen verwalten lassen (falls zutreffend). Search, Social und Commerce überschreiben alle Änderungen, die Sie innerhalb des Werbenetzwerks vornehmen.
     >* Nachdem Sie ein Portfolio gestartet haben, können Sie vorübergehend manuelle Gebote für jede CPC-Kampagne im Portfolio festlegen, indem Sie Kampagnen-Bulksheets erstellen und veröffentlichen. Alle Gebotsänderungen, die sich aus den veröffentlichten Daten ergeben, sind für einen Tag gültig. Danach setzt Search, Social und Commerce die Angebote gemäß ihrer eigenen Optimierungsstrategie fort.

## Löschen eines inaktiven Portfolios

Sie können nur inaktive Portfolios löschen. Wenn das Portfolio optimiert oder aktiv ist, müssen Sie zunächst seinen Status in inaktiv ändern, bevor Sie die Möglichkeit haben, es zu löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Halten Sie den Cursor über der Portfoliozeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Aktivieren Sie das Kontrollkästchen neben dem Portfolio. Klicken Sie in der Symbolleiste für Massenaktionen auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen").

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Erstellen eines Portfolios](portfolio-create.md)
>* [(Neue Benutzeroberfläche) Bearbeiten eines Portfolios](portfolio-edit.md)
>* [Über Portfolios](portfolio-about.md)
