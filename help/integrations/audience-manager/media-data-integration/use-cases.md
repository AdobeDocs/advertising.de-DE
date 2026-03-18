---
title: Anwendungsfälle
description: Erfahren Sie mehr über Anwendungsfälle für die Freigabe Ihrer Advertising DSP-Mediendaten mit Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Anwendungsfälle für die Erfassung von Medienexpositionsdaten in Adobe Audience Manager

*Nur Werbetreibende mit Advertising DSP*

*Werbetreibende mit einer Adobe Advertising-Adobe Audience Manager-Integration*

Im Folgenden finden Sie einige Möglichkeiten, wie Sie von der Erfassung Ihrer Advertising DSP Media Exposure-<!-- ad impression data? --> in Audience Manager profitieren können.

## Verwaltung von Neuigkeit und Häufigkeit

Durch die Erfassung von Impressionsdaten in Audience Manager können Sie Ihre Häufigkeitsverwaltung verbessern, indem Sie Segmente von Benutzenden erstellen, die mit einer bestimmten Anzeige oder Kampagne Kontakt hatten. Sie können diese Segmente für das Anzeigen-Targeting verwenden, wenn Sie die Häufigkeit erhöhen möchten, oder für die Anzeigenunterdrückung, wenn Sie die Häufigkeit begrenzen möchten.

Außerdem können Sie mit Audience Manager [!DNL Segment Builder] ([- und Häufigkeitskontrollen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) auf alle [regelbasierten Eigenschaften](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) anwenden, die verwertbare Signale enthalten. Auf diese Weise können Sie beispielsweise einschränken, wie oft einem Benutzer innerhalb einer Medienkampagne ein bestimmter Kreativer angezeigt wird. Lesen Sie [Instant Cross-Device ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot;, um zu erfahren, wie Sie dies tun können.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Sequenzielles Messaging

Durch die Erfassung von Impressionsdaten können Sie ein Segment von Benutzenden erstellen, die einer Kampagne oder Anzeige ausgesetzt waren, und dieses Segment für sequenzielles Messaging oder Unterdrückung verwenden. Sie können beispielsweise Benutzende, die kreative `123` gesehen, aber nicht geklickt oder konvertiert haben, erneut ansprechen, indem Sie ihnen kreative `456` zeigen.

Gehen Sie wie folgt vor, um dieses Beispiel in Audience Manager auszuführen:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Erstellen Sie eine Eigenschaft , um Benutzer zu erfassen, die die kreativen Inhalte gesehen haben.

   Um beispielsweise die Eigenschaft `Creative Trait 123` zu benennen, verwenden Sie die folgende Eigenschaftsregel:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Erstellen Sie eine Eigenschaft , um Benutzer zu erfassen, die klicken oder konvertieren.

   Um beispielsweise diese Eigenschaft `Click and Converter` zu benennen, verwenden Sie die folgende Eigenschaftsregel:

   ```
   d_event == click OR d_event=conv
   ```

1. Erstellen Sie ein Segment namens `Retarget Users` , das mit Benutzern gefüllt wird, die kreative `123` gesehen, aber nicht geklickt oder konvertiert haben. Verwenden Sie die folgende Eigenschaftsregel:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Ordnen Sie die `Retarget Users` einem Ziel zu und sprechen Sie Benutzende im Ziel mit kreativen `456` an.

## [!DNL Adobe Audience Analytics]- und Kampagnen-Belichtungsdaten

Sobald Kampagnenimpressions- und Klick-Daten in Audience Manager verfügbar sind, können Sie Eigenschaften und Segmente von Benutzenden erstellen, die einer bestimmten Kampagne oder Taktik ausgesetzt waren oder mit ihr interagiert haben. Mit einer [[!DNL Audience Analytics] Integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) können Ihre Audience Manager-Segmente mit [!DNL Analytics] synchronisiert werden, um weitere Analysen durchzuführen. Zu den möglichen Anwendungsfällen gehören die folgenden:

* **Interaktionsanalyse zwischen DSP- und [!DNL Advertising Search, Social, & Commerce]-Anzeigen:** Der Standard [[!DNL Analytics for Advertising] Integration](/help/integrations/analytics/overview.md) bietet keine Einblicke in die Interaktion zwischen DSP und [!DNL Search, Social, & Commerce], da beide Kanäle AMO-IDs verwenden, die den AMO-ID-Attributionsregeln folgen, für die ein Suchklick eine Display-Durchsicht überschreibt. Durch Erstellung eines DSP-Belichtungssegments in Audience Manager können Sie [!DNL Audience Analytics] verwenden, um die Interaktion zwischen DSP und [!DNL Search, Social, & Commerce] Ads in [!DNL Analytics] zu analysieren.

* **Häufigkeitsanalyse:** Sie können in Audience Manager Segmente erstellen, die darauf basieren, wie oft ein Benutzer einer bestimmten Anzeige oder Kampagne ausgesetzt wurde. Anschließend können Sie die verschiedenen Belichtungssegmente in Analytics analysieren, um zu sehen, wie sich das Benutzerverhalten je nach Anzahl der DSP-Belichtungen ändert.

## [!DNL Audience Optimization Reports]

Sie können [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) nutzen, um potenzielle Leistungsmöglichkeiten für Segmente in Ihren Kampagnen zu identifizieren. Diese Berichte kombinieren Kampagnen-Impressions-, Klick- und Konversionsdaten mit Segmentmetriken, um segmentorientierte Optimierungen und einen effektiven Kanal-Mix zu erzielen.

### Typen relevanter Audience Optimization-Berichte

| Bericht | Beschreibung |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Vergleicht zugeordnete und nicht zugeordnete Segmente nach Impressions und Konversionsraten. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Berichte]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Gibt Daten zu Impressionen, Clickthrough-Raten und Konversionen für einen breiten Bereich von Werbedimensionen zurück. |
| [[!UICONTROL Optimal Frequency] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Hilft Ihnen dabei, das optimale Gleichgewicht zwischen der Anzahl der bereitgestellten Impressions und Konversionen zu ermitteln. Damit können Sie die Anzahl der Impressionen anpassen, die angezeigt werden sollen, bevor Sie beginnen, abnehmende Rückgaben zu sehen. |
| [[!UICONTROL Unique User Reach] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Ein Blasendiagramm, in dem die Größe jeder Blase direkt proportional zur Anzahl der eindeutigen Benutzer für Ihre ausgewählte Dimension ist. |

### Aspekte

* Wenn [!DNL Audience Optimization Reports] Benutzer über rollenbasierte Zugriffssteuerungen (RBAC) verfügen, müssen [!DNL Adobe Customer Care] eine Zuordnung zwischen der Advertiser-ID und dem Audience Manager-Datenquellen-Integrations-Code des Unternehmens konfigurieren. Administratoren können dann verschiedenen Benutzern RBAC-Rechte gewähren.

* Das Konversionsbericht in [!DNL Audience Optimization Reports] muss vom Endbenutzer eingerichtet werden. Benutzer müssen Metadatendateien ausfüllen.

* [!DNL Audience Optimization Reports] unterstützt keine Änderungen an Kampagnenmetadaten (z. B. Kampagnenname oder Platzierungsname).

* Klicks auf Suchanzeigen werden nur dann in [!DNL Audience Optimization Reports] eingeschlossen, wenn sie mit Impressionen korrelieren. Mit anderen Worten werden Suchklicks nach Impressionen als Konversionen behandelt. Daher sind viele Klicks auf die Suche möglicherweise nicht in [!DNL Audience Optimization Reports] enthalten.

>[!MORELIKETHIS]
>
>* [Übersicht über das Senden von DSP Media Exposure-Daten an Adobe Audience Manager](overview.md)
>* [Erfassen von Klick- und Impressionsdaten aus Advertising DSP-Kampagnen](collect.md)
