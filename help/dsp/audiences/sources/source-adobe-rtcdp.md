---
title: Verwenden der DSP-Integration mit [!DNL Adobe] [!DNL Real-time CDP]
description: Erfahren Sie, wie Sie DSP zur Aufnahme Ihrer [!DNL Adobe] [!DNL Real-time CDP] Erstanbietersegmente.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Konvertieren von Benutzer-IDs aus [!DNL Adobe Real-Time CDP] zu universellen IDs

*Beta-Funktion*

Verwenden Sie die DSP-Integration mit [die [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), das Teil der Adobe Experience Platform ist, um Ihre Hash-E-Mail-Adressen in universelle IDs für zielgerichtete Werbung zu konvertieren.

1. (Konvertieren von E-Mail-Adressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Richten Sie das Tracking für [!DNL Analytics] Messung:

   1. (Wenn Sie dies noch nicht getan haben) Führen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und [AMO-ID und EF-ID in Ihren Tracking-URLs](/help/integrations/analytics/ids.md).

   1. Registrieren Sie sich beim universellen ID-Partner und stellen Sie universellen ID-spezifischen Code auf Ihren Webseiten bereit, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) für Durchsichten zuzuordnen:

      * **Für [!DNL RampIDs]:** Sie müssen auf Ihren Webseiten ein zusätzliches JavaScript-Tag bereitstellen, um Konversionen aus den IDs in Desktop- und mobilen Webbrowsern (aber nicht mobilen Apps) zu ermöglichen, Durchsichten anzuzeigen. Wenden Sie sich an Ihr Adobe Account-Team, das Ihnen Anweisungen zur Registrierung für eine [!DNL LiveRamp] [!DNL LaunchPad] Tag aus [!DNL LiveRamp] Authentifizierungs-Traffic-Lösungen. Die Registrierung ist kostenlos, Sie müssen jedoch eine Vereinbarung unterzeichnen. Nachdem Sie sich registriert haben, generiert Ihr Adobe Account-Team ein eindeutiges Tag, das Ihr Unternehmen für die Implementierung auf Ihren Webseiten bereitstellen kann.

1. [Erstellen einer Zielgruppenquelle](source-manage.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren. Sie können Ihre Benutzer-IDs beliebig in [Verfügbare universelle ID-Formate](source-about.md).

   Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, den Sie im nächsten Schritt verwenden werden.

1. Konfigurieren Sie in Adobe Experience Platform eine Advertising DSP-Zielverbindung mit dem [!UICONTROL Source Key] , die in den DSP-Quelleinstellungen generiert wurde.

   Anweisungen zum Aktivieren der DSP-Zielverbindung, Auswählen von Segmenten und Zugreifen auf Kontrollberechtigungen finden Sie unter[Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   Die Quell-E-Mail-Adressen müssen mit dem SHA-256-Algorithmus gehasht werden.

1. Überprüfen Sie dies in Ihrer Zielgruppenbibliothek (die verfügbar ist, wenn Sie eine Zielgruppe aus [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in Platzierungseinstellungen), die das Segment füllt, und vergleichen Sie die Anzahl der universellen IDs mit der Anzahl der ursprünglichen Hash-E-Mail-Adressen.

   Die Segmente sollten in DSP innerhalb von 24 Stunden verfügbar sein. Nachdem DSP die Segmentdaten erhalten hat, sollte die Zielgruppenanzahl innerhalb von neun (9) Stunden sichtbar sein. Informationen zu akzeptablen ID-Übersetzungsraten und dazu, warum die Segmentzählungen variieren können, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances).&quot;

Segmente werden alle 24 Stunden aktualisiert. Die Aufnahme in ein Segment läuft jedoch standardmäßig nach 30 Tagen oder nach einem kundenspezifischen Ablaufzeitraum ab. Aktualisieren Sie Ihre Segmente, indem Sie sie vor Ablauf von Real-Time CDP erneut per Push an die Zielgruppe senden. Wenden Sie sich an Ihr Adobe-Account-Team, um einen benutzerdefinierten Segmentablauf anzufordern.

## Fehlerbehebung

Informationen zur Fehlerbehebung bei Problemen mit der Übersetzungsrate und der Benutzeranzahl finden Sie unter &quot;[Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md).&quot;

Wenden Sie sich zur Fehlerbehebung bei Problemen mit dem Konvertierungsverfahren an Ihr Adobe-Account-Team oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Zielkatalog - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
