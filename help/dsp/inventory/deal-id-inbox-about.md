---
title: Über die [!UICONTROL Deal ID Inbox]
description: Erfahren Sie mehr über die [!UICONTROL Deal ID inbox]-Funktion, mit der Sie private Angebote akzeptieren können, die Sie bereits mit Herausgebern ausgehandelt haben  [!DNL FreeWheel], [!DNL Google Authorized Buyers] früher bekannt als [!DNL AdX]), and [!DNL Magnite DV+] (früher [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Über die [!UICONTROL Deal ID Inbox]

Mit dem Advertising DSP-[!UICONTROL Deal ID inbox] können Sie schnell Angebote einrichten, die DSP von Publishern über Supply Side Platforms (SSPs) importiert hat, sodass Sie nicht jedes Angebot manuell einrichten müssen. Sie können die garantierten und nicht garantierten privaten Inventarangebote akzeptieren, die Sie bereits mit Herausgebern in [!DNL FreeWheel], [!DNL Google Authorized Buyers] (ehemals als [!DNL AdX] bezeichnet) und [!DNL Magnite DV+] (ehemals [!DNL Rubicon]) aus dem [!UICONTROL Deal ID inbox] ausgehandelt haben.

>[!NOTE]
>
>Advertising DSP ist die erste DSP, die mit der [!DNL FreeWheel]-API integriert wird.

In der [!UICONTROL Deal ID inbox] können Sie die Details des Angebots so anzeigen, wie es Ihr Publisher sieht, Ihre Angebotseinrichtung beschleunigen und manuelle Eingabefehler vermeiden.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP aktualisiert alle Deal-Details automatisch täglich um 4:30 Uhr EST. Außerdem werden alle [!DNL FreeWheel] Angebote und bestehenden Angebote ab [!DNL Google] und [!DNL Magnite DV+] stündlich aktualisiert. Sie können die Angebotsdetails auch manuell aktualisieren, um jederzeit neue Angebote einzutragen.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Für programmgesteuerte garantierte -Angebote über [!DNL Google Authorized Buyers] müssen Sie mindestens 90 % Ihres Budgets einhalten, sonst verliert Ihr Konto den Zugriff auf [!DNL Google] -Angebote im [!UICONTROL Deal ID inbox].

## Implementieren des [!UICONTROL Deal ID Inbox]

Um Ihre Angebote im [!UICONTROL Deal ID inbox] zu erhalten, müssen Ihre SSP-Konten das DSP-Konto Ihres Unternehmens Ihrem SSP-Konto zuordnen. DSP kann die Kontonamen des Unternehmens für die entsprechenden SSPs freigeben. Wenden Sie sich an Ihr Adobe-Account-Team.

Bitten Sie den Publisher während der Vertragsverhandlungen, das Angebot an Ihren Käufer und nicht an das übergeordnete DSP-Konto zu senden. Die Abschlusskennung kann je nach SSP ein Name oder eine ID sein.

## Aktionen, die Sie mit Ihren Angeboten durchführen können

* **Angebote überprüfen** um sicherzustellen, dass der SSP die richtigen Publisher-, Flugdaten-, CPM- und anderen Angebotsdetails gesendet hat. Wenn der Publisher einen Fehler gemacht hat, kontaktieren Sie ihn außerhalb von DSP, damit er den Deal korrigieren und erneut senden kann.

* **Akzeptieren von Angeboten** nachdem sie geprüft wurden, und sie werden nicht mehr in der [!UICONTROL Deal ID inbox] angezeigt. Akzeptierte Angebote sind unter [!UICONTROL Inventory] > [!UICONTROL Deals] aufgeführt und können in den Platzierungen der Werbetreibenden gezielt ausgewählt werden.

* **Ignoriere Angebote** die nicht benötigt werden oder nicht angefordert werden. Ignorierte Angebote werden auf die Registerkarte [!UICONTROL Ignored Deals] im [!UICONTROL Deal ID inbox] verschoben, die als Archiv dient. DSP warnt SSPs und Publisher nicht, wenn Sie einen Deal ignorieren.

* **Ändern Sie Details für bereits akzeptierte Angebote** über [!UICONTROL Inventory] > [!UICONTROL Deals] (nicht im [!UICONTROL Deal ID inbox]). Ebenso sind Advertiser dafür verantwortlich, wenn Herausgeber Änderungen an Angeboten senden, diese Änderungen in [!UICONTROL Inventory] > [!UICONTROL Deals] zu implementieren, da der [!UICONTROL Deal ID inbox] nach der Einrichtung von Angeboten keine Änderungen aus den SSPs synchronisiert.

## Welche Arten von Angeboten können nicht akzeptiert werden?

Wenn eine Angebotsliste kein Symbol ![Akzeptieren](/help/dsp/assets/accept.png) oder eine [!UICONTROL Accept] Schaltfläche enthält, können Sie sie nicht vom [!UICONTROL Deal ID inbox] akzeptieren. Stattdessen können Sie [die Details der Angebots-ID manuell erstellen](/help/dsp/inventory/deal-id-create.md).

Folgende Arten von Angeboten können Sie nicht akzeptieren:

* [!DNL Google] Angebote, die nicht in USD enthalten sind.

* [!DNL Magnite DV+] Angebote, die nicht in USD enthalten sind

* [!DNL FreeWheel] Angebote, die nicht in Ihrer Kontowährung enthalten sind.

* Angebote, die vor dem heutigen Tag enden.

* Alte [!DNL Magnite DV+]-Angebote, die als „mehrere Medientypen“ gekennzeichnet waren.

Die Details des Angebots enthalten den Grund, warum das Angebot nicht akzeptiert werden kann.

>[!MORELIKETHIS]
>
>* [Akzeptieren eines Angebots im Angebots-ID-Posteingang](deal-id-inbox-accept.md)
>* [Übersicht über die Inventar-Funktionen](inventory-overview.md)
