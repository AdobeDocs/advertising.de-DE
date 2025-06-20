---
title: Übersicht über die Implementierung von Adobe Advertising Creative
description: Erfahren Sie mehr über den grundlegenden Workflow für die Implementierung von  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Übersicht über die Implementierung von Adobe Advertising Creative

*Geschlossene Beta-Version*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

Das [!DNL Creative] Operations-Team arbeitet mit jedem Advertiser zusammen, um seine Kreativ- und Kreativerlebnisse einzurichten. Entweder werden die Anzeigenerlebnisse als Anzeigen in Ihrer DSP implementiert oder Ihr Team erhält die Drittanbieter-Anzeigentags, um sich selbst zu implementieren, und die anfänglichen Kosten-, Klick- und Konversionsdaten werden validiert.

Das Adobe-Account-Team, das Agency-Team oder der Advertiser (je nach den Bedingungen der service level agreement) müssen jedes Erlebnis laufend überwachen und nach Bedarf bearbeiten, um die Ziele des Advertisers zu erreichen.

## Aufgaben beim erstmaligen Einrichten für [!DNL Creative] Erlebnisse

Das Implementierungsteam und/oder Ihre Agentur arbeiten mit Ihnen zusammen, um Folgendes zu tun:

1. Definieren Sie Ihre Personalisierungsziele (z. B. ob Sie Anzeigen für die Interessentengewinnung oder das Retargeting personalisieren), alle verfügbaren Erst-, Zweit- und Drittanbieterdaten, einschließlich Kreativ-Assets und Zielgruppensegmente, und Ihre Strategie zum Erreichen Ihrer Ziele.<!-- and CRM data? used how/where? -->

1. (Neue Advertiser-Konten) Einrichten von administrativen Konten:

   1. Richten Sie das Konto des Werbetreibenden für [!DNL Creative] ein und erstellen Sie auch ein Konto in Advertising Search, Social und Commerce.

      Das [!DNL Creative] Konto wird in Advertising DSP eingerichtet, auch wenn der Werbetreibende nicht den Rest von DSP verwendet.

      Auch wenn der Advertiser kein [!DNL Search, Social, & Commerce] ist, wird das [!DNL Search, Social, & Commerce]-Konto verwendet, um Konversionsverfolgungstags zu erstellen und Konversionsspalten in [!DNL Creative] einzurichten.

   1. (Falls erforderlich) Erstellen Sie Benutzerkonten für den Advertiser, um seine Kreativen und Anzeigenerlebnisse anzuzeigen und zu verwalten und Berichte zu generieren.

1. (Optional) Wenn Sie Erstanbieter-Zielgruppensegmente erstellen möchten, die als Ziele für Ihre Kreativen einbezogen werden, erstellen Sie die Tags auf eine der folgenden Arten:

   * [Erstellen Sie Retargeting](/help/creative/pixels/retargeting-pixel-manage.md)Pixel, um Anzeigen für Besucher mit bestimmten Attributen auf bestimmte Landingpages oder Konversionsseiten neu auszurichten und dann Tags zu generieren, die in die entsprechenden Web-Seiten eingefügt werden.

   * (Werbetreibende mit DSP) Erstellen Sie in DSP [benutzerdefinierte Zielgruppensegmente](/help/dsp/audiences/custom-segment-create.md) um alle Besucherinnen und Besucher bestimmter Landingpages oder Konversionsseiten zu verfolgen und dann Tags zu generieren, die in die entsprechenden Web-Seiten eingefügt werden.

   Bei beiden Arten von Tags handelt es sich um Bild-Tags, mit denen auf der Webseite, auf der sie hinzugefügt werden, ein für Endbenutzer unsichtbares, transparentes Bild (Pixel) mit 1 Pixel x 1 Pixel angezeigt wird. Später können Sie Kreative in einem Anzeigenerlebnis so konfigurieren, dass sie bestimmte Retargeting-Pixel oder -Segmente auswählen. Die relevanten Anzeigenelemente werden dann nur Benutzern angezeigt, die zuvor mit dem Pixel oder Segment verknüpfte Website-Seiten besucht haben.

   Möglicherweise muss die IT-Abteilung oder andere Gruppe des Werbetreibenden die Tag-Bereitstellung planen oder darüber informiert werden.

   **Hinweis** Sie können Ihre Erstanbieter-Zielgruppen aus Adobe Audience Manager und Adobe Analytics auch als kreative Ziele verwenden. Sobald ein Besucher für eine von [!DNL Analytics] freigegebene Zielgruppe qualifiziert ist, können die Informationen in [!DNL Creative] in etwa 24-48 Stunden verarbeitet werden. <!--Are times still true? -->

1. Richten Sie die Kampagnenhierarchie in den DSPs ein, in denen Sie Ihre Anzeigenerlebnisse implementieren. Verwenden Sie Targeting, das mit dem Targeting in den Werbeanzeigen kompatibel ist, die Sie in den Kampagnen implementieren werden.

   Das hierarchische Targeting-Verhalten kann je nach DSP variieren. Advertising DSP wendet Targeting auf Anzeigenebene zusätzlich zum Targeting auf (nicht anstelle des Targeting auf Platzierungsebene an. Wenn sich eine Platzierung beispielsweise an Benutzende in Australien und eine Anzeige an Benutzende in Japan richtet, zielt die Anzeige für das Erlebnis auf den Zweig „Alle anderen“ ab. Stellen Sie sicher, dass Sie die gesamte Kampagnenstruktur durchdenken.

1. Richten Sie Anzeigen-Erlebnisse basierend auf Ihren Werbezielen ein:

   * **Automatisierungs-Workflow:** Das [!DNL Creative] Operations-Team kann dynamische Anzeigen für Ihr Unternehmen mithilfe von Anzeigenvorlagen und Daten-Feeds erstellen.

     Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **Manueller Workflow:** Manuelles Einrichten von Anzeigen-Erlebnissen:

      1. [Richten Sie Standard-Kreative ein, die Sie für Ihre Erlebnisse verwenden können](/help/creative/creative-libraries/creative-add-standard.md):

         * Für Kreative, die [!DNL Creative] hosten, laden Sie sie hoch. Dazu können Bild-Assets in einem Adobe Experience Manager-Konto gehören.

         * Für Kreative, die auf einem unterstützten Werbeserver eines Drittanbieters gehostet werden, verweisen Sie auf die Kreativdateien.

      1. (Optional) [Gruppieren Sie Kreative in Bundles](/help/creative/creative-libraries/bundle-manage.md) die Sie in einem Schritt an zielgerichtete Erlebnisse anhängen können.

      1. Einrichten von [Anzeigen-Erlebnissen](/help/creative/experiences/experience-about.md):

         * Sequenzkreative [ optionale Anzeigenziele für ](/help/creative/experiences/experience-create-targeting.md)zielgerichtete Anzeigenerlebnisse).

           Anzeigenziele können Folgendes umfassen: Retargeting von Pixeln, die Sie in [!DNL Creative] erstellen, Zielgruppensegmente in Adobe Experience Cloud (einschließlich DSP, Audience Manager oder [!DNL Analytics]), geografische Ziele oder bestimmte Daten-Trigger auf der Web-Seite (z. B. SKU=01234567890123 oder Cart=empty).

         * Erstellen Sie für [nicht zielgerichtete ](/help/creative/experiences/experience-create-no-targeting.md)-Erlebnisse“ allgemeine Erlebniseinstellungen.

           Anzeigenziele können Folgendes umfassen: Retargeting von Pixeln, die Sie in [!DNL Creative] erstellen, Zielgruppensegmente in Adobe Experience Cloud (einschließlich DSP, Audience Manager oder [!DNL Analytics]), geografische Ziele oder bestimmte Daten-Trigger auf der Web-Seite (z. B. SKU=01234567890123 oder Cart=empty).













1. Einrichten des Konversions-Trackings für Ihre Anzeigenerlebnisse:


Konversionsverfolgung einrichten. Je nach Implementierung kann dies Folgendes beinhalten:
Konversionsverfolgungstags auf den Web-Seiten des Werbetreibenden und/oder tägliche Einrichtung einer
Feed-Ablage für Konversionsdaten, die der Advertiser separat erfasst hat.


Sie können Konversionsverfolgungstags für Adobe Advertising in Advertising Search, Social und Commerce oder in Adobe Dynamic Tag Manager (ehemals Dynamic Tag Manager) generieren.
Hinweis: Sie müssen JavaScript-Konvertierungs-Tags verwenden, keine Bild-Tags.


Die IT-Abteilung des Werbetreibenden oder eine andere Gruppe muss ggf. einen Zeitplan festlegen oder informiert werden
Über die Tag-Bereitstellung.


(Optional) Führen Sie in Search, Social und Commerce jede Konversion durch (Transaktionseigenschaft)
Verfügbar als einzelner Spaltensatz in Datenansichten und Berichten.


Eine Konversion (Transaktionseigenschaft) wird in Suche, Social und Commerce nach aufgeführt.
Mindestens ein Konversionsereignis wurde verfolgt.


Wenn Sie keine bestimmten Metriken verfügbar machen, werden alle Konversionen konsolidiert
in einem Spaltensatz „Konversionen“.


Validieren Sie die verfolgten Daten.


(Optional) Richten Sie den Versand geplanter Berichte an bestimmte E-Mail-Adressen ein.


Anweisungen finden Sie im Hilfekapitel zu „Berichte“.


Richten Sie Anzeigenkampagnen auf Advertising DSP oder einer anderen DSP ein und stellen Sie JavaScript bereit
oder iFrame-Tags für die Anzeigenerlebnisse an den Advertiser senden, der sie als
Anzeigen von Drittanbietern in der DSP.


Überwachen der Leistung abgeschlossener Anzeigen-Erlebnisse, entweder Anzeigen vordefinierter
Leistungsdetails für einzelne Erlebnisse oder Erstellen benutzerdefinierter Leistungsberichte.


Aktualisieren Sie bei Bedarf die Anzeigenerlebnisse auf der Grundlage der Leistung und des aktualisierten Messaging.






>[!MORELIKETHIS]
>
>* [Über Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Organisation der Benutzeroberfläche](/help/creative/introduction/ui.md)
