---
title: Verwenden der DSP-Integration mit [!DNL Adobe] [!DNL Real-time CDP]
description: Erfahren Sie, wie Sie DSP die Aufnahme  [!DNL Adobe] [!DNL Real-time CDP] Erstanbietersegmenten ermöglichen.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
TQID: https://experienceleague.adobe.com/Ggt-YiAoGurfI5eET66xJwMBTSq-w5FO7wH60WZshEk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 50af5a8fc6e5e82268489259073e27911ca5a45c
workflow-type: tm+mt
source-wordcount: 596
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Adobe Real-Time CDP] in universelle IDs

Verwenden Sie die DSP-Integration mit [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), die Teil von Adobe Experience Platform ist, um Ihre Benutzer-IDs - einschließlich Hash-E-Mail-Adressen, Cookies und IDs für mobile Werbung - in universelle IDs für zielgruppengerechte Werbung zu konvertieren.

1. (Um Benutzer-IDs in [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> zu konvertieren; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Einrichten des Trackings für die [!DNL Analytics]:

   1. (Falls noch nicht geschehen) Füllen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und die [AMO-ID und EF-ID in Ihren Tracking-URLs ](/help/integrations/analytics/ids.md).

   1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie auf Ihren Web-Seiten einen universellen ID-spezifischen Code bereit, um Konversionen aus den IDs in Desktop-Browsern und mobilen Webbrowsern (aber nicht in mobilen Apps) abzugleichen und Anleitungen zu erhalten:

      * **[!DNL RampIDs]:** Sie müssen ein zusätzliches JavaScript-Tag auf Ihren Web-Seiten bereitstellen, damit die Konversionen der IDs in Desktop- und mobilen Webbrowsern (aber nicht in mobilen Apps) für die Viewthroughs übereinstimmen. Wenden Sie sich an Ihr Adobe-Konto-Team, das Ihnen Anweisungen zur Registrierung für ein [!DNL LiveRamp] [!DNL LaunchPad]-Tag von [!DNL LiveRamp] Authentication Traffic Solutions (ats.js) gibt. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nach der Registrierung erstellt Ihr Adobe-Account-Team ein eindeutiges Tag, das Ihr Unternehmen auf Ihren Web-Seiten implementieren kann.

1. [Erstellen einer Zielgruppenquelle](source-manage.md) um Zielgruppen in Ihr DSP-Konto oder ein Advertiser-Konto zu importieren. Sie können Ihre Benutzerkennungen in eines der ([ universellen ID-Formate) ](source-about.md).

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, den Sie im nächsten Schritt verwenden werden.

1. Konfigurieren Sie in Adobe Experience Platform eine Advertising DSP-Zielverbindung mit dem -[!UICONTROL Source Key], der in den DSP-Quelleinstellungen generiert wurde.

   E-Mail-Adressen müssen mit dem SHA-256-Algorithmus gehasht werden.

   Anweisungen zum Aktivieren der DSP-Zielverbindung, Aktivieren von Zielgruppen und Überprüfen des Datenexports finden Sie unter [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

   >[!NOTE]
   >
   >Die alte Verbindung, die nur die Unterstützung für Hash-E-Mail-Adressen umfasst, wird jetzt als &quot;[Legacy Adobe Advertising Cloud DSP-Verbindung“ ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection-legacy). Wenn Sie bereits die alte Verbindung verwenden, müssen Sie nicht sofort Änderungen vornehmen. Die alte Verbindung wird jedoch letztendlich entfernt.

1. Überprüfen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob das Segment aufgefüllt ist, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Benutzer-IDs.

   Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppengröße innerhalb von neun (9) Stunden sichtbar sein. Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentanzahl variieren kann, finden Sie unter [Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).

Segmente werden alle 24 Stunden aktualisiert. Die Aufnahme in ein Segment läuft jedoch standardmäßig nach 30 Tagen oder nach einem vom Kunden angegebenen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie vor dem Ablauf erneut aus Real-Time CDP pushen. Um eine benutzerdefinierte Segmentgültigkeit anzufordern, wenden Sie sich an Ihr Adobe Account Team.

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Übersetzungsraten und Problemen mit der Benutzeranzahl finden Sie unter &quot;[ für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md).

Wenden Sie sich zur Fehlerbehebung bei Konvertierungsproblemen an Ihr Adobe-Account-Team oder an `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Zielkatalog - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
