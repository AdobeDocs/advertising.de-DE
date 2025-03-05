---
title: Über Erlebnisse in Advertising Creative
description: Erfahren Sie, wie Sie personalisierte Anzeigenerlebnisse konfigurieren und Anzeigenelemente basierend auf der Leistung optimieren können.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: e2b88275f2ebbc69f769cf905a0d20859bf0af3b
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---

# Über Erlebnisse in Advertising Creative 2.0

*Geschlossene Beta-Version*

<!-- Revisit Description metadata  -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] bietet zwei verschiedene Strukturen für das Anzeigen-Erlebnis für die Anzeigen in einer Kreativbibliothek<!-- can use a single library only -->:

* **Erlebnisse beim Targeting mit Entscheidungsbäumen:** [!DNL Creative] ermöglicht es Ihnen, personalisierte Anzeigenerlebnisse auf der gesamten Kunden-Journey mithilfe eines Entscheidungsbaummodells zu konfigurieren. Sie können alle Werbeelemente - Bilder, Überschriften, Angebote und Landingpages - je nach Zielgruppe anpassen.

  Sie können beispielsweise dasselbe Creative Bundle für Personen in Chicago und New York City angeben, die sich in einem bestimmten Zielgruppensegment von Adobe Analytics befinden, Personen in Chicago jedoch an andere Landingpages als New Yorker senden. Sie können auch ein anderes Bundle für Personen im Segment angeben, die an einem beliebigen Ort außer Chicago und New York City leben, und ein drittes Bundle für andere Personen, die nicht im Segment sind.

  Zu den Targeting-Optionen gehören:

   * Ihre Erstanbieter-Zielgruppensegmente aus Adobe Audience Manager, Adobe Analytics und Advertising Cloud DSP

   * Bestimmte geografische Standorte, einschließlich Länder, Bundesstaaten, DMAs in den USA, Städte und Postleitzahlen

   * Viewer, für die bestimmte Schlüssel-Wert-Paare (Datenübergabeziele) von DSP, Publisher oder Partner übergeben werden

   * [!DNL Creative] Retargeting von Pixeln und angegebenen Attributwerten

   * Spezifische Gerätetypen, Betriebssysteme und Browser

  Jedem Erlebnis können kreative Bundles zugewiesen werden. Für jedes Erlebnis können Sie die Optimierung und Planung für die Kreativ-Bundles anpassen und die standardmäßigen Landingpages und Tracking-URLs <!-- and any flexible attributes --> einzelne Kreative in jedem Bundle ändern.

* **Erlebnisse ohne Targeting mit Entscheidungsbaum:** [!DNL Creative] optimiert die Anzeigenelemente für das Anzeigenerlebnis, ohne die Zielgruppe einzugrenzen.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> Für jedes Erlebnis geben Sie Start- und Enddatum sowie einige Standardeinstellungen an, aber ein Großteil des Workflows ist nicht direkt im Erlebnis enthalten. Anstatt Kreative direkt zum Erlebnis hinzuzufügen, verwenden Sie [!UICONTROL Tag Manager], um ein Anzeigen-Tag für jede Anzeigengröße für das Erlebnis zu erstellen und dann Kreative hinzuzufügen, die kreative Optimierung und Planung zu konfigurieren und die Landingpages und Tracking-URLs anzupassen.

## Anzeigenoptimierung

<!-- MORE -->
[!DNL Creative] optimiert die Anzeigenelemente für jedes Erlebnis basierend auf der Leistung. Bei Erlebnissen, die auf bestimmte Zielgruppen ausgerichtet sind, können Anzeigen basierend auf der Leistung der einzelnen Anzeigenelemente für die Zielgruppen-Sets optimiert werden. Bei Erlebnissen ohne spezifische Zielgruppenziele werden die Anzeigenelemente allein auf der Grundlage der Leistung der einzelnen Anzeigenelemente optimiert.

## Implementieren und Verwalten von Erlebnissen

Nachdem Sie ein Live-Erlebnis (mit allen erforderlichen Anzeigenelementen) erstellt haben, können Sie [ein JavaScript- oder iframe-Tag für das gesamte Erlebnis generieren](experience-tag-export.md). Sie können das Erlebnis-Tag als Anzeige in eine Kampagne in Adobe Advertising DSP hochladen oder als Anzeige in einer DSP eines Drittanbieters implementieren. [!DNL Creative] stellt Anzeigen für das Erlebnis bereit, die auf den Optionen für Targeting und Anzeigenrotation sowie dem verfügbaren Anzeigeninventar basieren.

## Leistungsdaten für Ihre Erlebnisse

Wenn Sie die Option [!UICONTROL Metrics] in der Ansicht [!UICONTROL Creative] > [!UICONTROL Experiences] aktivieren, gibt jede Erlebniskarte oder -zeile die Anzahl der Impressionen und Klicks an, die das Erlebnis erhalten hat.

![Metriken-Option](/help/creative/assets/metrics-option.png "Metriken-Option")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

Sie können [detaillierte Leistungsdaten für jedes Erlebnis anzeigen](experience-performance-details.md) in der [!UICONTROL Experiences] anzeigen.

Erstellen Sie eine [!UICONTROL Custom Creative Report](/help/creative/report-custom-creative.md), um die Leistung für alle Erlebnisse zu überwachen.

## Erlebnisstatus {#experience-statuses}

<!-- verify that these are all still the same -->

Der Status eines Erlebnisses wird automatisch festgelegt, mit Ausnahme von *gelöscht* die Sie manuell festlegen.

*Live:* Das Erlebnis enthält alle erforderlichen Elemente, sodass Sie ein Erlebnis-Tag generieren können, das als Anzeige in einer DSP implementiert werden soll. <!-- A live experience may be scheduled to start in the future -->

*Entwurf:* Nicht allen Verzweigungen des Erlebnisses werden Kreative zugewiesen, sodass das Erlebnis unvollständig ist und Sie kein Erlebnis-Tag generieren können.

*Verarbeitung läuft* Ein zuvor Live-Erlebnis wurde bearbeitet, ist jetzt aber unvollständig. Es kann kein Erlebnis-Tag dafür generiert werden. **Hinweis:** Wenn Sie bereits ein Erlebnis-Tag für das Erlebnis implementiert haben, kann die zuvor aktive Version weiterhin bereitgestellt werden. Wenn Sie das Erlebnis später abschließen und es erneut aktivieren, kann die neue Version mithilfe der vorhandenen Tag-Implementierung bereitgestellt werden.

*Gelöscht:* Das Erlebnis wurde aus [!DNL Creative] gelöscht und ist in den [!UICONTROL Experiences] nicht mehr sichtbar.

>[!NOTE]
>
>Sie können den Status einer Anzeige in einer DSP ändern, ohne den Erlebnisstatus in [!DNL Creative] zu beeinflussen.

## Die [!UICONTROL Experiences]

Die [!UICONTROL Experiences] Ansicht zeigt alle zielgerichteten und nicht zielgerichteten Erlebnisse. Sie können die Erlebnisnamen, den Status, das Start- und Enddatum, die Anzahl und Dimensionen der zugewiesenen Kreativen oder Kreativ-Bundles sehen und sehen, ob das Erlebnis dynamische Anzeigen enthält. Wenn Sie die Option [!UICONTROL Metrics] in der [!UICONTROL Experiences] aktivieren, gibt jede Erlebniskarte oder Zeile die Anzahl der Impressionen und Klicks an, die das Erlebnis erhalten hat.

Sie können Ihre Erlebnisse erstellen und verwalten, einschließlich Optimierung und Zuweisung von Kreativen und Kreativ-Bundles zu Ihren Erlebnissen. Sie können auch Erlebnis-Tags erstellen und umbenennen und die Tags in den Formaten JavaScript und iframe zur Implementierung auf Ihren DSPs exportieren. Werbetreibende mit Advertising DSP können Tags optional direkt als Anzeigen in eine Advertising DSP-Kampagne hochladen.

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Erstellen eines Erlebnisses ohne Targeting](experience-create-no-targeting.md)
