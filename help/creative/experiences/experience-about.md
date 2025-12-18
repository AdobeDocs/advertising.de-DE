---
title: Über Erlebnisse in Advertising Creative
description: Erfahren Sie, wie Sie personalisierte Anzeigenerlebnisse konfigurieren und Anzeigenelemente basierend auf der Leistung optimieren können.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 39f77087769eda3cc200447aeb0a6d1648e23b42
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 0%

---

# Über Erlebnisse in Advertising Creative 2.0

Jedes Anzeigenerlebnis kann einen Anzeigentyp enthalten (Standardanzeige, Standardvideo oder dynamische Anzeige). [!DNL Advertising Creative 2.0] bietet zwei verschiedene Strukturen für das Anzeigen-Erlebnis für die Anzeigen in einer einzigen Creative Library.

* **Erlebnisse beim Targeting mit Entscheidungsbäumen:** [!DNL Creative] ermöglicht es Ihnen, personalisierte Anzeigenerlebnisse auf der gesamten Kunden-Journey mithilfe eines Entscheidungsbaummodells zu konfigurieren. Sie können alle Werbeelemente - Bilder, Überschriften, Angebote und Landingpages - je nach Zielgruppe anpassen.

  Sie können beispielsweise dasselbe Creative Bundle für Personen in Chicago und New York City angeben, die sich in einem bestimmten Zielgruppensegment von Adobe Analytics befinden, Personen in Chicago jedoch an andere Landingpages als New Yorker senden. Sie können auch ein anderes Bundle für Personen im Segment angeben, die an einem beliebigen Ort außer Chicago und New York City leben, und ein drittes Bundle für andere Personen, die nicht im Segment sind.

  Zu den Targeting-Optionen gehören:

   * Ihre Zielgruppensegmente aus Adobe Audience Manager, Adobe Analytics und Advertising DSP, alle anderen für das Konto importierten Erstanbietersegmente, Ihre benutzerdefinierten Segmente aus Advertising DSP, von Advertising DSP bereitgestellte Drittanbietersegmente und alle in der Zielgruppenbibliothek erstellten bestehenden Advertising DSP-Zielgruppen

   * Bestimmte geografische Standorte, einschließlich Länder, Bundesstaaten, DMAs in den USA, Städte und Postleitzahlen

   * Viewer, für die bestimmte Schlüssel-Wert-Paare (Datenübergabeziele) von DSP, Publisher oder Partner übergeben werden (z. B. SKU=01234567890123 oder Cart=empty)

   * [!DNL Creative] Retargeting von Pixeln und angegebenen Attributwerten

   * Spezifische Gerätetypen, Betriebssysteme und Browser

  Nachdem Sie eine Verzweigung für die Zielgruppe im Entscheidungsbaum erstellt haben, können Sie die Zielgruppe mit potenziellen Kreativen verbinden, indem Sie der Verzweigung Kreativ-Bundles zuweisen. Für jedes Erlebnis können Sie die Optimierung und Planung für die Kreativ-Bundles anpassen und die standardmäßigen Landingpages und Tracking-URLs <!-- later: and any flexible attributes --> einzelne Kreative in jedem Bundle ändern.

* **Erlebnisse ohne Targeting mit Entscheidungsbaum:** [!DNL Creative] optimiert die Anzeigenelemente für das Anzeigenerlebnis, ohne die Zielgruppe einzugrenzen. Für jedes Erlebnis geben Sie Start- und Enddatum sowie einige Standardeinstellungen an, aber ein Großteil des Workflows ist nicht direkt im Erlebnis enthalten. Anstatt Kreative direkt zum Erlebnis hinzuzufügen, verwenden Sie [!UICONTROL Tag Manager] , um ein Anzeigen-Tag für jede Anzeigengröße für das Erlebnis zu erstellen und dann Kreative hinzuzufügen, die kreative Optimierung und Planung zu konfigurieren und die Landingpages und Tracking-URLs anzupassen<!-- later: and any flexible attributes -->.

>[!NOTE]
>
> Da die beiden Erlebnistypen unterschiedliche Workflows aufweisen, können Sie ein nicht zielgerichtetes Erlebnis nicht in ein zielgerichtetes Erlebnis oder ein zielgerichtetes Erlebnis in ein nicht zielgerichtetes Erlebnis ändern.

## Bereitstellung und Optimierung von Anzeigen

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative] stellt Erstanbieter-Anzeigen und Trigger-Anzeigen von Drittanbietern für das Erlebnis bereit, die auf den angegebenen Optionen für Targeting (falls zutreffend), Planung, Anzeigenrotation und Optimierungsziel sowie dem verfügbaren Anzeigeninventar basieren.

* **Planung:** (Optional) Planen Sie die Ausführung bestimmter Kreativer während bestimmter, sequenzieller Zeiträume.

* **Anzeigenrotation:** Drehen Sie die Kreativen algorithmisch entsprechend dem angegebenen Optimierungsziel; entsprechend einer angegebenen Bundle-Sequenz; oder entsprechend der relativen Gewichtung.

* **Optimierungsziel:** Sie Anzeigenelemente für die beste Klickrate oder ein bestehendes benutzerdefiniertes [Advertising DSP-Ziel](/help/dsp/optimization/custom-goal.md)

  [!DNL Creative] optimiert Anzeigenerlebnisse, indem es den Assets mit der besten Performance einen Impression-Anteil verleiht. Bei Erlebnissen, die auf bestimmte Zielgruppen ausgerichtet sind, können Anzeigen basierend auf der Leistung der einzelnen Anzeigenelemente für die Zielgruppen-Sets optimiert werden. Bei Erlebnissen ohne spezifische Zielgruppenziele werden die Anzeigenelemente ausschließlich auf der Grundlage der Leistung der einzelnen Anzeigenelemente optimiert.

Beispielsweise können Sie die Ausführung von Creative 1 für die ersten beiden Wochen planen, um die Clickthrough-Rate zu optimieren, und Creative 2 für die folgenden zwei Wochen, um für ein bestimmtes benutzerdefiniertes Ziel zu optimieren.

## Implementieren und Verwalten von Erlebnissen

Nachdem Sie ein Live-Erlebnis (mit allen erforderlichen Anzeigenelementen) erstellt haben, können Sie [ein JavaScript- oder iframe-Tag für das gesamte Erlebnis generieren](experience-tag-export.md). Sie können das Erlebnis-Tag als Anzeige in eine Kampagne in Adobe Advertising DSP hochladen oder es als Anzeige in einer DSP eines Drittanbieters implementieren.

>[!NOTE]
>
>Das hierarchische Targeting-Verhalten kann je nach DSP variieren. Advertising DSP wendet Targeting auf Anzeigenebene zusätzlich zum Targeting auf Platzierungsebene an.

## Leistungsdaten für Ihre Erlebnisse

Die folgenden Leistungsdaten sind verfügbar:

* Wenn Sie die Option [!UICONTROL Metrics] in der Ansicht [!UICONTROL Creative] > [!UICONTROL Experiences] aktivieren, gibt jede Erlebniskarte oder -zeile die Anzahl der Impressionen und Klicks an, die das Erlebnis erhalten hat.

  ![Metriken-Option](/help/creative/assets/metrics-option.png "Metriken-Option")

* Sie können [detaillierte Leistungsdaten für jedes Erlebnis anzeigen](experience-performance-details.md) in der [!UICONTROL Experiences] anzeigen.

* Um die Leistung in all Ihren Erlebnissen zu überwachen, erstellen Sie [benutzerdefinierten Creative-Bericht](/help/creative/reports/report-manage.md).

## Warnhinweise

Eine Spalte &quot;[!UICONTROL Alerts]&quot; zeigt an, wenn bei einem Erlebnis oder einem untergeordneten Kreativen darunter ein Problem auftritt. Ein [!UICONTROL Pulse Panel] rechts in der Symbolleiste zeigt an, ob Warnhinweise für das Erlebnis verfügbar sind, einschließlich aller untergeordneten Kreativen. Weitere Informationen finden [ unter &quot;](/help/creative/reports/alerts-view.md) anzeigen“.

## Erlebnisstatus {#experience-statuses}

Der Status eines Erlebnisses wird automatisch festgelegt, mit Ausnahme von *Gelöscht* die Sie manuell festlegen.

| Status | Beschreibung |
| ------ | ----------- |
| [!UICONTROL Live] | Das Erlebnis enthält alle erforderlichen Elemente, sodass Sie ein Erlebnis-Tag generieren können, das als Anzeige in einer DSP implementiert werden soll. Der Start eines Live-Erlebnisses kann für die Zukunft geplant werden. |
| [!UICONTROL Draft] | Nicht allen Verzweigungen des Erlebnisses werden Kreative zugewiesen, sodass das Erlebnis unvollständig ist und Sie kein Erlebnis-Tag generieren können. |
| [!UICONTROL Processing] | Ein zuvor Live-Erlebnis wurde bearbeitet, ist jetzt jedoch unvollständig. Es kann kein Erlebnis-Tag dafür generiert werden. **Hinweis:** Wenn Sie bereits ein Erlebnis-Tag für das Erlebnis implementiert haben, kann die zuvor Live-Version weiterhin bereitgestellt werden. Wenn Sie das Erlebnis später abschließen und es erneut aktivieren, kann die neue Version mithilfe der vorhandenen Tag-Implementierung bereitgestellt werden. |
| [!UICONTROL Deleted] | Das Erlebnis wurde aus [!DNL Creative] gelöscht und ist in den [!UICONTROL Experiences] nicht mehr sichtbar. |

>[!NOTE]
>
>Sie können den Status einer Anzeige in einer DSP ändern, ohne den Erlebnisstatus in [!DNL Creative] zu beeinflussen.

## Die [!UICONTROL Experiences]

Die [!UICONTROL Experiences] Ansicht zeigt alle zielgerichteten und nicht zielgerichteten Erlebnisse. Sie können die Erlebnisnamen, den Status, das Start- und Enddatum, die Anzahl und Dimensionen der zugewiesenen Kreativen oder Kreativ-Bundles sehen und sehen, ob das Erlebnis dynamische Anzeigen enthält. Wenn Sie die Option [!UICONTROL Metrics] in der [!UICONTROL Experiences] aktivieren, gibt jede Erlebniskarte oder Zeile die Anzahl der Impressionen und Klicks an, die das Erlebnis erhalten hat. Wenn Sie sich im Kartenmodus befinden, können Sie mithilfe der Schaltflächen &lt; und > einen Bildlauf durch die Kreativen in einem Erlebnis mit mehreren Kreativen durchführen.

Sie können Ihre Erlebnisse erstellen und verwalten, Erlebnis-Tags erstellen und umbenennen und die Tags in den Formaten JavaScript und iframe zur Implementierung in Ihren DSPs exportieren. Werbetreibende mit Advertising DSP können optional Anzeigen-Tags direkt in eine Advertising DSP-Kampagne hochladen.

### Verfügbare Aktionen

Im Folgenden finden Sie die wichtigsten verfügbaren Aktionen. Eine vollständige Liste finden Sie im Inhaltsverzeichnis für das Kapitel Kreative > Erlebnisse .

* [Herunterladen von Daten in der Ansicht](experience-download-view.md)

* [Erstellen](/help/creative/experiences/experience-create-targeting.md) und [Bearbeiten](/help/creative/experiences/experience-edit-targeting.md) eines Erlebnisses mit Targeting

* [Erstellen](/help/creative/experiences/experience-create-no-targeting.md), [Bearbeiten](/help/creative/experiences/experience-edit-no-targeting.md) und [Manuelles Erstellen eines Anzeigen-Tags](/help/creative/experiences/experience-tag-create-manually.md) für ein Erlebnis ohne Targeting

* [Klonen](experience-clone.md) ein Erlebnis

* [Vorschau](experience-preview.md) ein Erlebnis

* [Demo-URL freigeben](experience-share-demo-url.md) für ein Erlebnis

* [Exportieren von Anzeigen-Tags für ein ](experience-tag-export.md), einschließlich des optionalen Uploads von Anzeigen-Tags direkt in eine Advertising DSP-Kampagne

* [Löschen](experience-delete.md) eines Erlebnisses

>[!MORELIKETHIS]
>
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Erstellen eines Erlebnisses ohne Targeting](experience-create-no-targeting.md)
