---
title: Nutzungsszenarios
description: Erfahren Sie mehr über Anwendungsfälle für die Freigabe Ihrer Advertising DSP-Mediendaten für Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Nutzungsszenarios für die Erfassung von Daten zur Exposition von Medien in Adobe Audience Manager

*Advertiser nur mit Advertising DSP*

*Advertiser mit nur einer Adobe Advertising-Adobe Audience Manager-Integration*

Im Folgenden finden Sie einige Möglichkeiten, wie Sie von der Erfassung Ihrer Advertising DSP-Daten zur Medienbelichtung <!-- ad impression data? --> in Audience Manager profitieren können.

## Neuigkeit und Frequenzverwaltung

Durch die Erfassung von Impressionsdaten in Audience Manager können Sie Ihr Frequenzmanagement verbessern, indem Sie Benutzersegmente erstellen, die einer bestimmten Anzeige oder Kampagne ausgesetzt waren. Sie können diese Segmente für Anzeigen-Targeting verwenden, wenn Sie die Häufigkeit erhöhen möchten, oder für die Unterdrückung von Anzeigen, wenn Sie die Häufigkeit begrenzen möchten.

Mit Audience Manager [!DNL Segment Builder] können Sie außerdem [Neuigkeits- und Frequenzsteuerungen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) auf alle [regelbasierten Eigenschaften](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) anwenden, die umsetzbare Signale enthalten. So können Sie z. B. die Anzahl der Wiedergaben eines bestimmten Kreativelements innerhalb einer Medienkampagne auf einen Benutzer begrenzen. Lesen Sie &quot;[Sofortige geräteübergreifende Unterdrückung](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot;, um zu erfahren, wie dies funktioniert.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Sequenzielles Messaging

Durch die Erfassung von Impressionsdaten können Sie ein Segment von Benutzern erstellen, die einer Kampagne oder Anzeige ausgesetzt waren, und dieses Segment für sequenzielles Messaging oder Unterdrückung verwenden. Sie können beispielsweise Benutzer, die kreativ `123` gesehen, aber nicht geklickt oder konvertiert haben, erneut ansprechen, indem Sie ihnen kreative `456` zeigen.

Um dieses Beispiel in Audience Manager auszuführen, führen Sie die folgenden Schritte aus:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Erstellen Sie eine Eigenschaft, um Benutzer zu erfassen, die das Kreativ gesehen haben.

   Um beispielsweise die Eigenschaft `Creative Trait 123` zu benennen, verwenden Sie die folgende Eigenschaftsregel:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Erstellen Sie eine Eigenschaft zum Erfassen von Benutzern, die klicken oder konvertieren.

   Um diese Eigenschaft beispielsweise `Click and Converter` zu nennen, verwenden Sie die folgende Eigenschaftsregel:

   ```
   d_event == click OR d_event=conv
   ```

1. Erstellen Sie ein Segment mit dem Namen &quot;`Retarget Users`&quot;, das mit Benutzern gefüllt wird, die kreativ `123` gesehen, aber nicht geklickt oder konvertiert haben. Verwenden Sie die folgende Eigenschaftsregel:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Ordnen Sie das Segment `Retarget Users` einem Ziel zu und wählen Sie Benutzer im Ziel mit kreativen `456` als Ziel aus.

## [!DNL Adobe Audience Analytics] und Daten zur Kampagnenexponierung

Sobald Kampagnendaten für Impressions- und Klickdaten in Audience Manager verfügbar sind, können Sie Eigenschaften und Benutzersegmente erstellen, die einer bestimmten Kampagne oder Taktik ausgesetzt waren oder damit interagiert wurden. Mit einer [[!DNL Audience Analytics] integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) können Ihre Audience Manager-Segmente mit [!DNL Analytics] synchronisiert werden, um sie weiter zu analysieren. Mögliche Anwendungsfälle sind:

* **Interaktionsanalyse zwischen DSP- und [!DNL Advertising Search, Social, & Commerce]-Anzeigen:** Die standardmäßige [[!DNL Analytics for Advertising] Integration](/help/integrations/analytics/overview.md) bietet keine Einblicke in die Interaktion zwischen DSP und [!DNL Search, Social, & Commerce], da beide Kanäle AMO-IDs verwenden, die den AMO-ID-Attributionsregeln entsprechen. Bei einem Suchklick wird eine Durchsicht der Anzeige außer Kraft gesetzt. Durch Erstellung eines DSP Belichtungssegments in Audience Manager können Sie mit [!DNL Audience Analytics] die Interaktion zwischen DSP und [!DNL Search, Social, & Commerce] Anzeigen in [!DNL Analytics] analysieren.

* **Frequenzanalyse:** Sie können in Audience Manager Segmente erstellen, die darauf basieren, wie oft ein Benutzer einer bestimmten Anzeige oder Kampagne ausgesetzt war. Anschließend können Sie die verschiedenen Belichtungssegmente in Analytics analysieren, um festzustellen, wie sich das Benutzerverhalten in Abhängigkeit von der Anzahl DSP Belichtungen ändert.

## [!DNL Audience Optimization Reports]

Sie können [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) nutzen, um potenzielle Performance-Chancen für Segmente in Ihren Kampagnen zu ermitteln. Diese Berichte kombinieren Kampagnenimpressions-, Klick- und Konversionsdaten mit Segmentmetriken, um segmentorientierte Optimierungen und einen effektiven Kanalmix zu erhalten.

### Typen relevanter Audience Optimization-Berichte

| Bericht | Beschreibung |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Vergleicht zugeordnete und nicht zugeordnete Segmente nach Impressionen und Konversionsraten. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Berichte]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Gibt Daten zu Impressionen, Clickthrough-Raten und Konversionen für eine breite Palette von Werbedimensionen zurück. |
| [[!UICONTROL Optimal Frequency] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Hilft Ihnen, das optimale Gleichgewicht zwischen der Anzahl der bereitgestellten Impressionen und Konversionen zu ermitteln. Damit können Sie die Anzahl der Impressionen anpassen, die angezeigt werden sollen, bevor Sie beginnen, rückläufige Erträge zu sehen. |
| [[!UICONTROL Unique User Reach] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Ein Punktdiagramm, in dem jede Blase im direkten Verhältnis zur Anzahl der Unique Users für die ausgewählte Dimension skaliert wird. |

### Überlegungen

* Wenn [!DNL Audience Optimization Reports] -Benutzer rollenbasierte Zugriffssteuerungen (RBAC) haben, muss [!DNL Adobe Customer Care] eine Zuordnung zwischen der Advertiser-ID und dem Audience Manager-Integrationscode der Organisation konfigurieren. Administratoren können dann RBAC-Berechtigungen für verschiedene Benutzer bereitstellen.

* Konversionsberichte in [!DNL Audience Optimization Reports] müssen vom Endbenutzer eingerichtet werden. Benutzer müssen Metadatendateien ausfüllen.

* [!DNL Audience Optimization Reports] unterstützt keine Änderungen an Kampagnen-Metadaten (z. B. Kampagnenname oder Platzierungsname).

* Klicks auf Suchanzeigen werden nur dann in [!DNL Audience Optimization Reports] berücksichtigt, wenn sie mit Impressionen korreliert werden. Mit anderen Worten: Suchklicks werden als Konversionen infolge von Impressionen behandelt. Daher sind viele Suchklicks möglicherweise nicht in [!DNL Audience Optimization Reports] enthalten.

>[!MORELIKETHIS]
>
>* [Überblick über das Senden von DSP-Expositionsdaten an Adobe Audience Manager](overview.md)
>* [Erfassen von Klick- und Impressionsdaten aus Advertising DSP-Kampagnen](collect.md)
