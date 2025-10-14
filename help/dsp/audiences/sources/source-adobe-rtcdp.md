---
title: Verwenden der DSP-Integration mit [!DNL Adobe] [!DNL Real-time CDP]
description: Erfahren Sie, wie Sie DSP für die Aufnahme  [!DNL Adobe] [!DNL Real-time CDP] Erstanbietersegmenten aktivieren.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Adobe Real-Time CDP] in universelle IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de), die Teil von Adobe Experience Platform ist, um Ihre gehashten E-Mail-Adressen für die zielgruppengerechte Werbung in universelle IDs zu konvertieren.

1. (So konvertieren Sie E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Einrichten des Trackings für die [!DNL Analytics]:

   1. (Falls noch nicht geschehen) Füllen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und die [AMO-ID und EF-ID in Ihren Tracking-URLs &#x200B;](/help/integrations/analytics/ids.md).

   1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie auf Ihren Web-Seiten einen universellen ID-spezifischen Code bereit, um Konversionen aus den IDs in Desktop-Browsern und mobilen Webbrowsern (aber nicht in mobilen Apps) abzugleichen und Anleitungen zu erhalten:

      * **[!DNL RampIDs]:** Sie müssen ein zusätzliches JavaScript-Tag auf Ihren Web-Seiten bereitstellen, damit die Konversionen der IDs in Desktop- und mobilen Webbrowsern (aber nicht in mobilen Apps) für die Viewthroughs übereinstimmen. Wenden Sie sich an Ihr Adobe-Konto-Team, das Ihnen Anweisungen zur Registrierung für ein [!DNL LiveRamp] [!DNL LaunchPad]-Tag von [!DNL LiveRamp] Authentication Traffic Solutions gibt. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nach der Registrierung generiert Ihr Adobe-Account-Team ein eindeutiges Tag, das Ihr Unternehmen auf Ihren Web-Seiten implementieren kann.

1. [Erstellen einer Zielgruppenquelle](source-manage.md) um Zielgruppen in Ihr DSP-Konto oder ein Advertiser-Konto zu importieren. Sie können Ihre Benutzerkennungen in eines der ([&#x200B; universellen ID-Formate) &#x200B;](source-about.md).

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, den Sie im nächsten Schritt verwenden werden.

1. Konfigurieren Sie in Adobe Experience Platform eine Advertising DSP-Zielverbindung mit dem -[!UICONTROL Source Key], der in den DSP-Quelleinstellungen generiert wurde.

   Anweisungen zum Aktivieren der DSP-Zielverbindung, zum Auswählen von Segmenten und zum Zugriff auf Kontrollberechtigungen finden Sie unter &quot;[Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=de)&quot;.

   Die Quell-E-Mail-Adressen müssen mit dem SHA-256-Algorithmus gehasht werden.

1. Überprüfen Sie in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob das Segment aufgefüllt ist, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen.

   Die Segmente sollten innerhalb von 24 Stunden in DSP verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein. Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentanzahl variieren kann, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).

Segmente werden alle 24 Stunden aktualisiert. Die Aufnahme in ein Segment läuft jedoch standardmäßig nach 30 Tagen oder nach einem vom Kunden angegebenen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie vor dem Ablauf erneut aus Real-Time CDP pushen. Um eine benutzerdefinierte Segmentgültigkeit anzufordern, wenden Sie sich an Ihr Adobe-Account-Team.

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Übersetzungsraten und Problemen mit der Benutzeranzahl finden Sie unter &quot;[&#x200B; für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md).

Wenden Sie sich zur Fehlerbehebung bei Konvertierungsproblemen an Ihr Adobe-Kundenbetreuungsteam oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=de)
>* Adobe Experience Platform [Zielkatalog - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=de)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
