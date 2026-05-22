---
title: Erstanbietersegmente importieren aus [!DNL AdFixus]
description: Erfahren Sie, wie Sie  [!DNL AdFixus]  Erstanbietersegmente, die universelle IDs  [!DNL AdFixus] , in DSP importieren.
feature: DSP Audiences
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 0%

---

# Importieren von First-Party-Segmenten aus [!DNL AdFixus]

*Gilt nur für Werbetreibende in Australien*

Verwenden Sie die Advertising DSP-Integration mit [!DNL AdFixus], um Ihre [!DNL AdFixus] universellen IDs mit Segmentzuordnungen für zielgruppengerechte Werbung zu importieren. [!DNL AdFixus] IDs sind nur in Australien verfügbar. DSP ändert [!DNL AdFixus] IDs nicht in andere ID-Typen und konvertiert andere ID-Typen nicht in [!DNL AdFixus] IDs. DSP erhebt keine Gebühr für den Import der IDs.

Nachdem Sie Ihre [!DNL AdFixus] in DSP importiert haben, können Sie Platzierungen aus [!DNL AdFixus] auf [!DNL AdFixus]-IDs und auf bestimmte First-Party-Segmente ausrichten. Sie können auch [!DNL AdFixus] Segmente zu wiederverwendbaren Zielgruppen hinzufügen. Die Details für jedes Segment umfassen die Anzahl der anwendbaren [!DNL AdFixus]-IDs.

Sie können die Impression, den Klick, die Häufigkeit und andere Metriken für Benutzer mit [!DNL AdFixus] IDs in benutzerdefinierten Berichten anzeigen. Werbetreibende mit [!DNL Analytics for Advertising] können auch Durchsichtsdaten für [!DNL AdFixus]-IDs aus Adobe Analytics sowie Daten aus Adobe Analytics in DSP anzeigen.

1. Verwenden Sie [!DNL AdFixus] , um die Erstanbieterdaten Ihres Unternehmens in Segmente mit [!DNL AdFixus] IDs zu konvertieren.

   Dies erfordert ein separates Konto mit [!DNL AdFixus] und einen aktiven Lizenzschlüssel. Außerdem müssen Sie [!DNL AdFixus] Code für Ihre Website-Eigenschaften und Domains implementieren. Arbeiten Sie direkt mit [!DNL AdFixus] zusammen, um Segmente mit IDs zu generieren.

1. (Werbetreibende mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Einrichten des Trackings für die [!DNL Analytics]:

   1. (Falls noch nicht geschehen) Füllen Sie alle [Voraussetzungen für die Implementierung [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) und die [AMO-ID und EF-ID in Ihren Tracking-URLs ](/help/integrations/analytics/ids.md).

   1. Stellen Sie [!DNL AdFixus]-spezifischen Code auf Ihren Web-Seiten bereit, damit Konversionen aus den [!DNL AdFixus]-IDs in Desktop- und mobilen Webbrowsern (aber nicht in mobilen Apps) in Viewthroughs abgeglichen werden.

1. Importieren Sie Ihre Erstanbieter-[!DNL AdFixus]:

   1. [Erstellen einer Zielgruppenquelle](source-manage.md) von [!UICONTROL Type] **[!UICONTROL AdFixus ID]**. Sie müssen den Nutzungsbedingungen zustimmen.

      Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel.

   1. Geben Sie den Quellschlüssel für Ihr [!DNL AdFixus]-Team frei, damit es die erforderlichen Segmente an DSP streamen kann.

1. Überprüfen Sie im Abschnitt [!UICONTROL First Party Segments] Ihrer Zielgruppenbibliothek (der verfügbar ist, wenn Sie eine Zielgruppe unter [!UICONTROL Audiences] > [!UICONTROL All Audiences] oder in den Platzierungseinstellungen erstellen oder bearbeiten), ob das Segment gefüllt wird. Vergleichen Sie die Anzahl der [!DNL AdFixus]-IDs mit der Anzahl der Benutzer-IDs in [!DNL AdFixus].

   Die Segmente sind in DSP verfügbar, sobald sie erstellt wurden.

Segmente werden aktualisiert und stehen alle drei Stunden für die Zielgruppenbestimmung zur Verfügung. Die in DSP angezeigte Anzahl wird jedoch alle 24 Stunden aktualisiert. **Hinweis** Die Aufnahme in ein Segment läuft nach einem bestimmten Ablaufzeitraum ab, den Sie in [!DNL AdFixus] konfigurieren. Aktualisieren Sie Ihre Segmente, indem Sie sie vor dem Ablauf erneut aus [!DNL AdFixus] pushen.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Zielkatalog - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
