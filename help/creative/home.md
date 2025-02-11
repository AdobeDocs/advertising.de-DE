---
title: Neue Funktionen in Advertising Creative 2.0
description: Erfahren Sie mehr über die neuesten Updates und neuen Funktionen in Adobe Advertising Creative 2.0.
cloud: Experience Cloud
product: advertising cloud
solution: Advertising
index: false
exl-id: 0d25f665-b5f9-4d27-851a-2a456fe2cbf8
source-git-commit: ad113558764d690f8ce24247279bceb91214b140
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%

---

# Was ist in [!DNL Creative] 2.0 anders?

*Geschlossene Beta-Version*

<!-- The following features are new or recently changed. -->

| Datum | Funktion | Beschreibung | Für weitere Informationen |
| ---- | ------- | ----------- | -------------------- |
| 10. Februar 2025 | [!UICONTROL Creative Libraries] | Zuvor hatten Sie eine kreative Bibliothek. Jetzt können Sie für jeden Advertiser mehrere Bibliotheken erstellen. | Siehe &quot;[ zu Ihren Kreativbibliotheken](/help/creative/creative-libraries/creative-libraries-about.md).“ |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] | Die [!UICONTROL Creatives] enthält Registerkarten für [!UICONTROL Standard Ads] und [!UICONTROL Dynamic Ads].<ul><li>Auf der Registerkarte **[!UICONTROL Standard Ads]** Sie Bilder, HTML5, flexible HTML5 und Kreative von Drittanbietern hochladen und verwalten.</li><li>Auf der Registerkarte **[!UICONTROL Dynamic Ads]** können Sie dynamisch generierte Anzeigen verwalten, die aus hochgeladenen Feed-Dateien mithilfe definierter Anzeigenvorlagen erstellt werden. Die dynamische Anzeigengenerierung wurde zuvor in [!DNL Adobe Advertising Dynamic Creative Optimization (DCO)] durchgeführt.<br><br> Derzeit können Sie dynamische Anzeigen in der Vorschau anzeigen, duplizieren und löschen und dynamische Anzeigen an Kreativ-Bundles für zielgerichtete Anzeigenerlebnisse oder an Anzeigen-Tags für nicht zielgerichtete Erlebnisse anhängen. Nur Admin-Benutzer können dynamisch generierte Anzeigen erstellen.</li></ul> | Siehe &quot;[ zu Ihren Kreativbibliotheken](/help/creative/creative-libraries/creative-libraries-about.md).“ |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] | Gruppieren Sie mehrere Kreative in einem *Bundle*, um sie einfach zu einem Erlebnis hinzuzufügen. Sie können Standard-Anzeigenpakete erstellen und ihnen Standard-Kreative anhängen. Auf ähnliche Weise können Sie dynamische Anzeigenpakete erstellen und dynamische Kreative daran anhängen. | Siehe &quot;[Verwalten von Creative Bundles](/help/creative/creative-libraries/bundle-manage.md)&quot; |
| | [!UICONTROL Experiences] | In den Einstellungen für das Anzeigenerlebnis geben Sie jetzt an, ob das Erlebnis Entscheidungsbaum-Targeting verwenden soll oder nicht. Die Workflows für Erlebnisse mit Entscheidungsbaum-Targeting und Erlebnisse ohne Entscheidungsstruktur sind unterschiedlich. | Siehe &quot;[ Erlebnis mit Targeting erstellen](/help/creative/experiences/experience-create-targeting.md) und &quot;[Erlebnis ohne Targeting erstellen](/help/creative/experiences/experience-create-no-targeting.md). |
| | [!UICONTROL Experiences] | Sie können jetzt zielgerichtete Erlebnisse nur mit Kreativ-Bundles aus einer einzigen Kreativ-Bibliothek erstellen, nicht aus einzelnen Kreativen. Sie können dennoch einzelne Kreative aus einer einzelnen Bibliothek ohne Entscheidungsbaum-Targeting an nicht zielgerichtete Erlebnisse anhängen.<br><br>Aufgrund der strukturellen Änderungen werden Ihre bisherigen Erfahrungen im Laufe dieses Jahres eingestellt. | Self-Service-Kunden: Erstellen Sie Ihre Erlebnisse in der neuen Benutzeroberfläche neu. Siehe &quot;[ eines Erlebnisses mit Targeting](/help/creative/experiences/experience-create-targeting.md)&quot;.<br><br>Managed Service-Kunden: Ihr Adobe-Account-Team erstellt Ihre Erlebnisse in der neuen Benutzeroberfläche neu. |
| | [!UICONTROL Experiences] | Werbetreibende mit Advertising DSP können Tags optional direkt als Anzeigen in eine Advertising DSP-Kampagne hochladen. | Siehe &quot;[ und Implementieren eines Anzeigen-Erlebnis-Tags für ein Live-Erlebnis](/help/creative/experiences/experience-tag-export.md)&quot; |
| | DCO-Erlebnisse | Alte DCO-Erlebnisse werden im Laufe dieses Jahres eingestellt. Ihr Adobe-Account-Team erstellt Ihre DCO-Erlebnisse in [!DNL Creative] als dynamische Anzeigen neu. Ausnahme ist, dass DCO-Erlebnisse mit zusätzlichem Targeting als [!DNL Creative] Erlebnisse neu erstellt werden. | — |
| | Tags hinzufügen | Der Endpunkt des Anzeigenservers wird in den Advertising DSP-Anzeigenserver geändert.<br><br>Das Anzeigen-Tag enthält zusätzliche Parameter zur Weitergabe universeller IDs (zusätzlich zu Cookie-IDs). | Self-Service-Kunden: Sobald ein Erlebnis in [!DNL Creative] verfügbar ist, ersetzen Sie die Anzeigen-Tags in Ihren vorhandenen Kampagnen. Siehe &quot;[ und Implementieren eines Anzeigen-Erlebnis-Tags für ein Live-Erlebnis](/help/creative/experiences/experience-tag-export.md)&quot;.<br><br>Managed Service-Kunden: Ihr Adobe-Account-Team ersetzt die Anzeigen-Tags in Ihren bestehenden Kampagnen. |
| | Retargeting von Pixeln | Der Endpunkt für das Retargeting von Pixeln wird in den Adobe Advertising-UDB-Service geändert.<br><br>Das neue Pixel enthält zusätzliche Parameter, um zusätzlich zu den Cookie-IDs universelle IDs zu übergeben. | Self-Service-Kunden: Erstellen Sie neue Retargeting-Pixel und fügen Sie sie zu Ihren Web-Seiten hinzu. Siehe &quot;[Verwalten von Retargeting-Pixeln](/help/creative/pixels/retargeting-pixel-manage.md).“<br><br>Managed Service-Kunden: Ihr Adobe-Account-Team erstellt und teilt gegebenenfalls neue Retargeting-Pixel. Fügen Sie die neuen Pixel zu Ihren Web-Seiten hinzu. |
| | Konvertierungspixel | Die veralteten DCO-Pixel werden im Laufe dieses Jahres eingestellt, und es werden [!DNL Adobe] Konvertierungspixel erforderlich sein. | Self-Service-Kunden: Kunden mit [!DNL Analytics for Advertising] müssen die DCO-Konversionspixel durch die [!DNL Analytics for Advertising] [!DNL Last Event Service] Pixel und die Adobe Analytics Pixel ersetzen. Alle anderen müssen die DCO-Konvertierungspixel durch Adobe Advertising-Konvertierungspixel ersetzen.<br><br>Managed Service-Kunden: Ihr Adobe-Account-Team erstellt und teilt alle entsprechenden Adobe Advertising-Konversionspixel mit. Ersetzen Sie Ihre DCO-Konversionspixel durch Adobe Advertising-Konversionspixel. |

