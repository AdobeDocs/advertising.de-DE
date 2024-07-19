---
title: Über die [!UICONTROL Deal ID Inbox]
description: Erfahren Sie mehr über die Funktion [!UICONTROL Deal ID inbox] , mit der Sie private Angebote akzeptieren können, die Sie bereits mit Herausgebern am  [!DNL FreeWheel], [!DNL Google Authorized Buyers]  (ehemals  [!DNL AdX]), and [!DNL Magnite DV+] (früher  [!DNL Rubicon]) ausgehandelt haben.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Über die [!UICONTROL Deal ID Inbox]

Mit Advertising DSP [!UICONTROL Deal ID inbox] können Sie schnell Angebote einrichten, die DSP über angebotsseitige Plattformen (SSPs) von Herausgebern importiert hat, sodass Sie nicht jedes Geschäft manuell einrichten müssen. Sie können die garantierten und nicht garantierten privaten Inventargeschäfte akzeptieren, die Sie bereits mit Herausgebern über [!DNL FreeWheel], [!DNL Google Authorized Buyers] (ehemals [!DNL AdX]) und [!DNL Magnite DV+] (ehemals [!DNL Rubicon]) aus dem [!UICONTROL Deal ID inbox] ausgehandelt haben.

>[!NOTE]
>
>Advertising DSP ist die erste DSP, die in die [!DNL FreeWheel] -API integriert wird.

In der [!UICONTROL Deal ID inbox] können Sie die Details des Geschäfts sehen, wie sie Ihr Herausgeber sieht, die Einrichtung Ihrer Geschäfte beschleunigen und manuelle Einstiegsfehler vermeiden.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP aktualisiert automatisch täglich um 4:30 Uhr EST alle Details des Angebots. Außerdem werden alle [!DNL FreeWheel]-Angebote aktualisiert und bestehende Angebote von [!DNL Google] und [!DNL Magnite DV+] stündlich aktualisiert. Sie können die Details des Deals auch manuell aktualisieren, um jederzeit neue Angebote zu füllen.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Für programmgarantierte Angebote über [!DNL Google Authorized Buyers] müssen Sie mindestens 90% Ihres Budgets bereitstellen oder Ihr Konto verliert den Zugriff auf [!DNL Google]-Angebote in der [!UICONTROL Deal ID inbox].

## Implementieren des [!UICONTROL Deal ID Inbox]

Um Ihre Angebote im [!UICONTROL Deal ID inbox] zu erhalten, müssen Ihre SSP-Konten das DSP Ihrer Organisation Ihrem SSP-Konto zuordnen. DSP können die Kontonamen des Unternehmens für die relevanten SSPs freigeben. Wenden Sie sich für weitere Informationen an Ihr Adobe Account-Team.

Teilen Sie dem Herausgeber bei den Vertragsverhandlungen mit, dass er den Deal an den Käufer und nicht an das DSP übergeben soll. Die Deal-ID kann je nach SSP ein Name oder eine ID sein.

## Maßnahmen, die Sie bei Ihren Angeboten ergreifen können

* **Überprüfen Sie die Angebote**, um sicherzustellen, dass der SSP den richtigen Herausgeber, die Flugdaten, den CPM und andere Geschäftsdetails gesendet hat. Wenn der Herausgeber einen Fehler gemacht hat, kontaktieren Sie ihn außerhalb von DSP, damit er den Vorgang korrigieren und erneut senden kann.

* **Akzeptiert Angebote** nach der Überprüfung, und sie erscheinen nicht mehr in der [!UICONTROL Deal ID inbox]. Akzeptierte Angebote werden unter [!UICONTROL Inventory] > [!UICONTROL Deals] aufgelistet und können innerhalb der Platzierungen von Werbetreibenden gezielt ausgewählt werden.

* **Ignorieren von Geschäften**, die nicht benötigt werden oder unerwünscht sind. Ignorierte Angebote werden in die Registerkarte [!UICONTROL Ignored Deals] innerhalb der [!UICONTROL Deal ID inbox] verschoben, die als Archiv dient. DSP benachrichtigt keine SSPs und Herausgeber, wenn Sie einen Deal ignorieren.

* **Ändern Sie die Details für bereits akzeptierte Angebote** von [!UICONTROL Inventory] > [!UICONTROL Deals] (nicht in den [!UICONTROL Deal ID inbox]). Wenn Herausgeber Änderungen an Angeboten senden, sind Advertiser für die Implementierung dieser Änderungen in [!UICONTROL Inventory] > [!UICONTROL Deals] verantwortlich, da die [!UICONTROL Deal ID inbox] Änderungen von den SSPs nach der Einrichtung von Angeboten nicht synchronisiert.

## Welche Arten von Angeboten können nicht akzeptiert werden?

Wenn eine Liste von Angeboten kein ![Akzeptieren](/help/dsp/assets/accept.png) -Symbol oder keine [!UICONTROL Accept] -Schaltfläche enthält, können Sie sie nicht über die [!UICONTROL Deal ID inbox] akzeptieren. Stattdessen können Sie [die Details der Deal-ID manuell erstellen](/help/dsp/inventory/deal-id-create.md).

Sie können die folgenden Arten von Angeboten nicht akzeptieren:

* [!DNL Google] Angebote, die nicht in USD enthalten sind.

* [!DNL Magnite DV+] Angebote, die nicht in USD enthalten sind

* [!DNL FreeWheel] Angebote, die nicht in Ihrer Kontowährung enthalten sind.

* Angebote mit einem Enddatum bis heute

* Alte [!DNL Magnite DV+] Angebote, die als &quot;mehrere Medientypen&quot;gekennzeichnet waren.

Die Details des Deals enthalten den Grund dafür, dass das Geschäft nicht akzeptiert werden kann.

>[!MORELIKETHIS]
>
>* [Akzeptieren eines Angebots im Posteingang der Angebots-ID](deal-id-inbox-accept.md)
>* [Überblick über die Inventarfunktionen](inventory-overview.md)
