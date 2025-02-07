---
title: Übersicht über die Implementierung von Adobe Advertising Creative
description: Erfahren Sie mehr über den grundlegenden Workflow für die Implementierung von  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Übersicht über die Implementierung von Adobe Advertising Creative

*Geschlossene Beta-Version*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

Das [!DNL Creative] Operations-Team arbeitet mit jedem Werbetreibenden zusammen, um seine Kreativ- und Kreativerlebnisse einzurichten. Entweder werden die Werberlebnisse als Anzeigen in Ihrer DSP implementiert oder Ihr Team erhält die Drittanbieter-Werbe-Tags, um sich selbst zu implementieren, und die anfänglichen Kosten-, Klick- und Konversionsdaten werden validiert.

Das Adobe-Account-Team, das Agenturteam oder der Advertiser (je nach den Bedingungen der service level agreement) müssen jedes Erlebnis laufend überwachen und nach Bedarf bearbeiten, um die Ziele des Advertisers zu erreichen.

## Aufgaben beim erstmaligen Einrichten für [!DNL Creative] Kampagnen <!-- Experiences? "Campaigns" may be confusing now. -->

Das Implementierungsteam und/oder Ihre Agentur arbeiten mit Ihnen zusammen, um Folgendes zu tun:

1. Definieren Sie Ihre Personalisierungsziele (z. B. ob Sie Anzeigen für die Interessentengewinnung oder das Retargeting personalisieren), alle verfügbaren Erst-, Zweit- und Drittanbieterdaten, einschließlich Kreativ-Assets, Zielgruppensegmente und CRM-<!-- used how/where? -->, und Ihre Strategie zum Erreichen Ihrer Ziele.

1. (Neue Advertiser-Konten) Einrichten von administrativen Konten:

   1. Richten Sie das Konto des Werbetreibenden für [!DNL Creative]<!-- and/or DSP? --> ein und erstellen Sie auch ein Konto in Advertising Search.

      Die Einrichtung des [!DNL Creative] Kontos erfolgt in Advertising DSP, auch wenn der Werbetreibende kein DSP-Kunde ist.

      Auch wenn der Advertiser kein [!DNL Search] ist, wird das [!DNL Search]-Konto verwendet, um Konversionsverfolgungstags zu erstellen und Konversionsspalten in [!DNL Creative] einzurichten.

   1. (Falls erforderlich) Erstellen Sie Benutzerkonten für den Advertiser, um seine Kreativen und Anzeigenerlebnisse anzuzeigen und zu verwalten und Berichte zu generieren.

1. (Optional) Wenn Sie Erstanbieter-Zielgruppensegmente erstellen möchten, die als Ziele für Ihre Kreativen einbezogen werden, erstellen Sie die Tags auf eine der folgenden Arten:

   * [Erstellen Sie Retargeting](/help/creative/pixels/retargeting-pixel-manage.md)Pixel, um Anzeigen für Besucher mit bestimmten Attributen auf bestimmte Landingpages oder Konversionsseiten neu auszurichten und dann Tags zu generieren, die in die entsprechenden Web-Seiten eingefügt werden.

   * (Werbetreibende mit DSP) Erstellen Sie innerhalb [ DSP benutzerdefinierte Zielgruppensegmente](/help/dsp/audiences/custom-segment-create.md) um alle Besucherinnen und Besucher bestimmter Landingpages oder Konversionsseiten zu verfolgen und dann Tags zu generieren, die in die entsprechenden Web-Seiten eingefügt werden.

   Bei beiden Arten von Tags handelt es sich um Bild-Tags, mit denen auf der Webseite, auf der sie hinzugefügt werden, ein für Endbenutzer unsichtbares, transparentes Bild (Pixel) mit 1 Pixel x 1 Pixel angezeigt wird. Später können Sie Kreative in einem Anzeigenerlebnis so konfigurieren, dass sie bestimmte Retargeting-Pixel oder -Segmente auswählen. Die relevanten Anzeigenelemente werden dann nur Benutzern angezeigt, die zuvor mit dem Pixel oder Segment verknüpfte Website-Seiten besucht haben.

   Möglicherweise muss die IT-Abteilung oder andere Gruppe des Werbetreibenden die Tag-Bereitstellung planen oder darüber informiert werden.

   **Hinweis** Sie können Ihre Erstanbieter-Zielgruppen aus Adobe Audience Manager und Adobe Analytics auch als kreative Ziele verwenden. Sobald ein Besucher für eine von [!DNL Analytics] freigegebene Zielgruppe qualifiziert ist, können die Informationen in [!DNL Creative] in etwa 24-48 Stunden verarbeitet werden. <!--Still true? And what about AAM and DSP? -->

1. Richten Sie Anzeigen-Erlebnisse basierend auf Ihren Werbezielen ein:

   * **Automatisierungs-Workflow:** Das [!DNL Creative] Operations-Team kann dynamische Anzeigen für Ihr Unternehmen mithilfe von Anzeigenvorlagen und Daten-Feeds erstellen.

     Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **Manueller Workflow:** Manuelles Einrichten von Anzeigen-Erlebnissen:

      1. Richten Sie Kreative ein, die Sie für Ihre Erlebnisse verwenden können:

         * Für Kreative, die [!DNL Creative] hosten, laden Sie sie hoch.<!-- Add x-ref and reword if necessary to cover all cases -->

         * Für Kreative, die auf einem unterstützten Werbeserver eines Drittanbieters gehostet werden, [verweisen Sie auf die Kreativdateien](/help/creative/creative-libraries/creative-third-party-manage.md).

      1. (Optional) [Gruppieren Sie Kreative in Bundles](/help/creative/creative-libraries/bundle-manage.md) die Sie in einem Schritt an Erlebnisse anhängen können.

      1. Sequenzierung von Kreativen und optionalen Anzeigenzielen als [Anzeigenerlebnisse](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done -->

     Anzeigenziele können Folgendes umfassen: Retargeting von Pixeln, die Sie in [!DNL Creative] erstellen, Zielgruppensegmente in Adobe Experience Cloud (einschließlich DSP, Audience Manager oder [!DNL Analytics]), geografische Ziele oder bestimmte Daten-Trigger auf der Web-Seite (z. B. SKU=01234567890123 oder Cart=empty).&lt;!— Ich sehe keine Zielgruppensegmente zur Verfügung und sehe RADIUS-Ziele (die nicht funktionieren), aber keine anderen Geoziele — überprüfen Sie alle diese. —>

1. Einrichten des Konversions-Trackings für Ihre Anzeigenerlebnisse:


Konversionsverfolgung einrichten. Je nach Implementierung kann dies Folgendes beinhalten:
Konversionsverfolgungstags auf den Web-Seiten des Werbetreibenden und/oder tägliche Einrichtung einer
Feed-Ablage für Konversionsdaten, die der Advertiser separat erfasst hat.


Sie können Konversionsverfolgungstags für Advertising Cloud in Advertising Cloud generieren
Suchen Sie oder innerhalb von Adobe Dynamic Tag Manager (früher Dynamic Tag Manager genannt).
Hinweis: Sie müssen JavaScript-Konvertierungs-Tags verwenden, keine Bild-Tags.


Die IT-Abteilung des Werbetreibenden oder eine andere Gruppe muss ggf. einen Zeitplan festlegen oder informiert werden
Über die Tag-Bereitstellung.


(Optional) Führen Sie in Advertising Cloud Search jede Konvertierung durch (Transaktionseigenschaft)
Verfügbar als einzelner Spaltensatz in Datenansichten und Berichten.


Eine Konversion (Transaktionseigenschaft) wird in Advertising Cloud Search aufgeführt, nachdem bei
Mindestens ein Konversionsereignis wurde verfolgt.


Wenn Sie keine bestimmten Metriken verfügbar machen, werden alle Konversionen konsolidiert
in einem Spaltensatz „Konversionen“.


Validieren Sie die verfolgten Daten.


(Optional) Richten Sie den Versand geplanter Berichte an bestimmte E-Mail-Adressen ein.


Anweisungen finden Sie im Hilfekapitel zu „Berichte“.


Richten Sie Anzeigenkampagnen auf Advertising Cloud DSP oder einer anderen DSP ein und stellen Sie JavaScript bereit
oder iFrame-Tags für die Anzeigenerlebnisse an den Advertiser senden, der sie als
Anzeigen von Drittanbietern in der DSP.


Überwachen der Leistung abgeschlossener Anzeigen-Erlebnisse, entweder Anzeigen vordefinierter
Leistungsdetails für einzelne Erlebnisse oder Erstellen benutzerdefinierter Leistungsberichte.


Aktualisieren Sie bei Bedarf die Anzeigenerlebnisse auf der Grundlage der Leistung und des aktualisierten Messaging.






>[!MORELIKETHIS]
>
>* [Über Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Organisation der Benutzeroberfläche](/help/creative/introduction/ui.md)
