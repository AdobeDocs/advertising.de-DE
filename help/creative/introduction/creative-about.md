---
title: Über Adobe Advertising Creative
description: Informationen über [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Über Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

Als Teil von Adobe Advertising ist Advertising Creative eine Self-Service-Plattform für die Automatisierung von personalisierten Echtzeit-Anzeigen-Erlebnissen und die optionale Optimierung Ihrer Anzeigen auf der Ebene der Werbeelemente.<!-- Verify --> Sie können die Anzeigenerlebnisse als Anzeigen in jeder DSP implementieren, einschließlich Adobe Advertising DSP.

## Benutzerdefinierte Kreativ-Bibliotheken wiederverwendbarer Kreativer

Mit Ihren Creative-Bibliotheken können Sie die Kreativen verwalten, die Sie für Ihre Anzeigenerlebnisse verwenden werden. Sie können mehrere Bibliotheken mit jeweils einzelnen Kreativen und Kreativgruppen (so genannten *-Bundles* erstellen, die Sie an Erlebnisse anhängen).

### [!DNL Adobe] Asset-Integrationen

[!DNL Creative] ist direkt in Adobe Experience Manager integriert, sodass Sie die [!DNL Adobe] Bild-Assets, die Ihr Design-Team erstellt und für Standard-Bild-Anzeigen genehmigt, einfach hochladen können.

## Regelbasierte und nicht zielgerichtete Erlebnisse

* **Zielgerichtete, regelbasierte Erlebnisse:** Erstellen Sie Geschichten mithilfe eines regelbasierten Entscheidungsbaum-Modells - Entfalten Sie eine choreografierte Reihe von Anzeigen, die in Echtzeit auf der Grundlage dessen angepasst werden, was Sie über Ihre Zielgruppe wissen. Die Storys können sich beispielsweise je nach Kundenverhalten, Geografie, Demografie, Retargeting, Position auf der Kunden-Journey und mehr ändern.

* **Nicht zielgerichtete Erlebnisse:** Anzeigen-Elemente zu planen und zu optimieren, ohne die Zielgruppe einzuschränken.

### [!DNL Adobe] von Datenintegrationen

Sie können Ihre Erstanbieter-Zielgruppensegmente aus Adobe Audience Manager und Adobe Analytics sowie benutzerdefinierte Zielgruppensegmente, die Sie in Advertising DSP erstellen, und Retargeting-Pixel, die Sie mit [!DNL Creative] erstellen, als Ziele für bestimmte Kreative in einem Werbeerlebnis verwenden. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Implementierung von Erlebnissen als Anzeigen

Nachdem Sie ein Erlebnis erstellt haben, können Sie ein JavaScript- oder iframe-Tag für das Erlebnis generieren und das Tag als Drittanbieteranzeige in einer Advertising DSP-Kampagne oder in einem anderen DSP implementieren.

### Optimierung von Werbeelementen

Optional können Sie [!DNL Creative] erlauben, die Anzeigenelemente für jedes Erlebnis basierend auf der Leistung zu optimieren - unabhängig davon, ob Sie bestimmte Zielgruppenziele definieren oder nicht -, indem Sie eine optimierte, gewichtete Anzeigenrotation verwenden, die von [!DNL Adobe AI] basiert.

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## Retargeting von Pixeln

Sie können Retargeting-Pixel erstellen, die als Ziele für Kreative in einem Werbeerlebnis verwendet werden. Die Ziele zeigen Anzeigen nur Benutzern mit bestimmten Attributen an, die zuvor bestimmte Web-Seiten besucht haben.

## Impression-, Klick- und Konversions-Tracking

[!DNL Creative] verfolgt automatisch alle Impressionen und Klicks auf Anzeigen, die aus einem Erlebnis bereitgestellt werden. Sie können Kreativen in Creative Libraries optional auch Impression-Tracking- und Klick-Tracking-URLs von Drittanbietern sowie benutzerdefinierte Tracking-URLs in einem Erlebnis hinzufügen.

[!DNL Creative] verfolgt auch Konversionen aus geschalteten Anzeigen, die aus Ihren Anzeigenerlebnissen erstellt wurden.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Leistungsberichte

Sie können detaillierte Leistungsberichte auf Erlebnisebene unter Kreative > Erlebnisse anzeigen.

Sie können unter Berichte > Benutzerdefinierte Berichte auch benutzerdefinierte Creative-Berichte erstellen, um die Leistung auf Erlebnisebene in allen Ihren Erlebnissen zu überwachen. Wenn Sie Ihre [!DNL Creative] Erlebnisse als Anzeigen in DSP-Kampagnen verwenden, sind Leistungsdaten für diese Anzeigen in zusätzlichen benutzerdefinierten Berichten verfügbar, genau wie Daten für Ihre anderen DSP-Anzeigen. <!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

Optional können Sie Ihre benutzerdefinierten Berichte an bestimmte [Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md) senden.

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Über Ihre Kreativbibliotheken](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Über Erlebnisse in Advertising Creative](/help/creative/experiences/experience-about.md)
