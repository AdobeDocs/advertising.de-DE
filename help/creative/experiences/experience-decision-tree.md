---
title: Das Layout des Entscheidungsbaums
description: Erfahren Sie mehr über die KI-gesteuerten und manuellen Editoren für Entscheidungsbäume für Erlebnisse beim Targeting.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
TQID: 'https://experienceleague.adobe.com/JFrcVBHxv90Fchk-VfkmxAITQJswboszNMFOfaAQlL4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%
---
# Das Entscheidungsbaum-Layout für [!DNL Creative] Erlebnisse

Wenn Sie die Option &quot;[!UICONTROL Targeting]&quot; für ein Erlebnis aktivieren, richten Sie das Erlebnis mithilfe eines Entscheidungsbaums ein.

Zunächst beginnt jeder Entscheidungsbaum mit der Stammebene „Alle“. Sie können einen oder mehrere Zielknoten hinzufügen und dann den endgültigen Knoten in jeder Verzweigung des Entscheidungsbaums kreative Bundles zuweisen.

## KI-gesteuerter Editor (Beta) {#ai-editor}

Der KI-gesteuerte Editor wird standardmäßig geöffnet, wenn Sie ein Erlebnis mit Targeting erstellen oder bearbeiten. Es kombiniert eine Konversation mit dem KI-Agenten und einer interaktiven Entscheidungsbaum-Arbeitsfläche.

* Beschreiben Sie die Zielgruppenstruktur oder die gewünschten Änderungen in der Konversation und überprüfen Sie den resultierenden Baum vor dem Speichern.

* Bearbeiten Sie die Arbeitsfläche direkt, um Zielebenen und Knoten hinzuzufügen, Bundles zuzuweisen und URLs für die kreative Optimierung und Nachverfolgung zu konfigurieren. Sie müssen nicht zum manuellen Editor wechseln, um diese Steuerelemente verwenden zu können.

* Zeigen Sie den Erlebnisnamen, den Status und den Advertiser in der Kopfzeile an und verwenden Sie Knoten-IDs, sofern verfügbar, um Zielknoten zu identifizieren, wenn Sie Änderungen beschreiben.

* Passen Sie die Ansicht mit **[!UICONTROL Zoom in]**, **[!UICONTROL Zoom out]** und **[!UICONTROL Change orientation]** an. **[!UICONTROL Reset tree]** löscht den Baum nach der Bestätigung; es setzt nicht nur den Zoom zurück.

Während der Assistent eine Änderung verarbeitet, sind die Arbeitsfläche und ihre **[!UICONTROL Save]** vorübergehend deaktiviert. Warten Sie, bis die Verarbeitung abgeschlossen ist, bevor Sie eine weitere Änderung an der Arbeitsfläche vornehmen.

## Manueller Editor {#manual-editor}

Um den vorhandenen manuellen Editor im KI-gesteuerten Editor zu öffnen, klicken Sie auf **[!UICONTROL Manual Decision Tree]**. Sie können in der [!UICONTROL Experiences] auch **[!UICONTROL Create Decision Tree Manually (Legacy)]** aus den Aktionen des Erlebnisses auswählen. Siehe [Editoren wechseln oder Erlebniseinstellungen bearbeiten](experience-edit-targeting.md#switch-editors).

Im manuellen Editor wird die Baumstruktur standardmäßig vertikal angezeigt. Sie können zu einer horizontalen Ansicht wechseln und den Zoom mit einem Schieberegler anpassen. Ihre Anzeigeeinstellungen werden gespeichert, bis Sie sich abmelden.

Die folgenden Beispiele zeigen den manuellen Editor:

![Beispiel eines vertikalen Entscheidungsbaums ohne Ziele](/help/creative/assets/experience-decision-tree-no-targets.png "Beispiel eines vertikalen Entscheidungsbaums ohne Ziele")

![Beispiel eines horizontalen Entscheidungsbaums ohne Ziele](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Beispiel eines horizontalen Entscheidungsbaums ohne Ziele")

>[!IMPORTANT]
>
>Speichern Sie alle Änderungen, die Sie beibehalten möchten, bevor Sie den KI-gesteuerten Editor verlassen. Durch Klicken auf **[!UICONTROL Manual Decision Tree]**, **[!UICONTROL Experience Form]** oder **[!UICONTROL Cancel]** wird ein Bestätigungsdialogfeld geöffnet. Durch Klicken auf **[!UICONTROL Yes]** werden nicht gespeicherte Strukturänderungen verworfen. Durch Klicken auf **[!UICONTROL No]** bleiben Sie im Editor.

## Begriffe

**Tree:** Die gesamte Entscheidungsstruktur als Baum mit Verzweigungen.

**Zielknoten:** Ein Ziel innerhalb einer Verzweigung.

**Blattknoten:** Eine Reihe von Kreativen, die einem endgültigen Zielknoten zugewiesen sind.

## Ziele in einem Entscheidungsbaum

Jeder Entscheidungsbaum kann bis zu fünf Zielgruppenebenen haben. Die Ziele auf Erlebnisebene werden in Verbindung mit den Zielgruppenbestimmungsoptionen Ihrer DSP angewendet. Das hierarchische Zielgruppenbestimmungsverhalten kann je nach DSP variieren. Stellen Sie sicher, dass Ihre Anzeigenerlebnisse ein Targeting enthalten, das mit den Kampagnen kompatibel ist, in denen Sie es implementieren werden.

Jede Zielebene kann mehrere Verzweigungen mit jeweils einem oder mehreren Knoten mit demselben Zieltyp enthalten (Zielgruppensegment, geografischer Standorttyp, Werte für angegebene Datenübergabeschlüssel, Attribute für ein bestimmtes Retargeting-Pixel oder Gerätekategorie). Sie können den Zielknoten der untersten Ebene Kreativ-Bundles in jeder Anzeigengröße zuweisen, für die Sie ein Standardbild oder ein Kreativ-Video angegeben haben.

<!-- Add a screen shot of the AI editor -->Das folgende Beispiel zeigt Ziele im manuellen Editor:

![Beispiel eines Entscheidungsbaums mit Zielen](/help/creative/assets/experience-decision-tree.png "Beispiel eines Entscheidungsbaums mit Zielen")

Wenn Sie der letzten Ebene einen Zielknoten hinzufügen, geben Sie das Ziel für den neuen Knoten an. Ein zusätzlicher gleichrangiger Knoten, „Alles andere“, wird automatisch für alle erstellt, die nicht mit dem angegebenen Ziel übereinstimmen. Anschließend können Sie zusätzliche gleichrangige Knoten mit verschiedenen Zielen desselben Typs hinzufügen.

Wenn Sie jedoch einen Zielknoten zwischen vorhandenen Ebenen einfügen, wird der erste Knoten für die neue Ebene zunächst „Alle“ zugewiesen. Um eine bestimmte Zielgruppe zu identifizieren, erstellen Sie einen gleichrangigen Zielknoten auf derselben Ebene, für den Sie die tatsächliche Zielgruppe angeben. Diese Aktion erstellt den Zielknoten und ersetzt den Knoten „Alle“ durch einen Knoten „Alles andere“ (der alle Kreativ-Bundles enthält, die zuvor allen zugewiesen waren). Anschließend können Sie zusätzliche gleichrangige Knoten mit verschiedenen Zielen desselben Typs hinzufügen.

Für alle übergeordneten Knoten können Sie optional alle untergeordneten Zielknoten und kreativen Bundles kopieren und in einen anderen Knoten derselben Ebene einfügen. Sie können die eingefügten Knoten entweder zum vorhandenen Framework hinzufügen oder das vorhandene Framework durch sie ersetzen.

## Kreative in einem Entscheidungsbaum

Weisen Sie jedem endgültigen Zielknoten im Erlebnis kreative Bundles zu.

Innerhalb jedes Knotens mit kreativen Bundles können Sie optional die eingeschlossenen Kreativen a) algorithmisch drehen, um die Clickthrough-Rate oder ein benutzerdefiniertes Ziel zu optimieren, b) entsprechend einer bestimmten Gewichtung oder c) in einer bestimmten Sequenz. Optional können Sie auch die Kreativen in einer bestimmten Zeitsequenz drehen, indem Sie eine beliebige Kombination derselben Optionen auswählen.

Sie können bei Bedarf die URLs für Landingpages, Impression-Tracking-URLs und Klick-Tracking-URLs für einzelne Kreative anpassen. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Über Erlebnisse in Advertising Creative 2.0](experience-about.md)
>* [Erstellen eines Erlebnisses mit Targeting](/help/creative/experiences/experience-create-targeting.md)
>* [Einstellungen für zielgerichtete Erlebnisse](/help/creative/experiences/experience-settings-targeting.md)
