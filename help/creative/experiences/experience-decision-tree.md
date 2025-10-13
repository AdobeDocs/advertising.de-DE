---
title: Das Layout des Entscheidungsbaums
description: Erfahren Sie mehr über das Entscheidungsbaum-Layout für Erlebnisse beim Targeting.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: 8a163cfd950d7388817425cde122105846604283
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Das Entscheidungsbaum-Layout für [!DNL Creative] Erlebnisse

Wenn Sie die Option &quot;[!UICONTROL Targeting]&quot; für ein Erlebnis aktivieren, richten Sie das Erlebnis mithilfe eines Entscheidungsbaums ein.

Zunächst beginnt jeder Entscheidungsbaum mit der Stammebene „Alle“. Sie können einen oder mehrere Zielknoten hinzufügen und dann den endgültigen Knoten in jeder Verzweigung des Entscheidungsbaums kreative Bundles zuweisen. Standardmäßig wird der Entscheidungsbaum vertikal angezeigt, Sie können den Baum jedoch auch horizontal anzeigen.

![Beispiel eines vertikalen Entscheidungsbaums ohne Ziele](/help/creative/assets/experience-decision-tree-no-targets.png "Beispiel eines vertikalen Entscheidungsbaums ohne Ziele")

![Beispiel eines horizontalen Entscheidungsbaums ohne Ziele](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Beispiel eines horizontalen Entscheidungsbaums ohne Ziele")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
>-->

## Begriffe

**Tree:** Die gesamte Entscheidungsstruktur als Baum mit Verzweigungen.

**Zielknoten:** Ein Ziel innerhalb einer Verzweigung.

**Blattknoten:** Eine Reihe von Kreativen, die einem endgültigen Zielknoten zugewiesen sind.

## Ziele in einem Entscheidungsbaum

Jeder Entscheidungsbaum kann bis zu fünf Zielgruppenebenen haben. Die Ziele auf Erlebnisebene werden in Verbindung mit den Zielgruppenbestimmungsoptionen Ihrer DSP angewendet. Das hierarchische Zielgruppenbestimmungsverhalten kann je nach DSP variieren. Stellen Sie sicher, dass Ihre Anzeigenerlebnisse ein Targeting enthalten, das mit den Kampagnen kompatibel ist, in denen Sie es implementieren werden.

Jede Zielebene kann mehrere Verzweigungen mit jeweils einem oder mehreren Knoten mit demselben Zieltyp enthalten (Zielgruppensegment, geografischer Standorttyp, Werte für angegebene Datenübergabeschlüssel, Attribute für ein bestimmtes Retargeting-Pixel oder Gerätekategorie). Sie können den Zielknoten der untersten Ebene Kreativ-Bundles in jeder Anzeigengröße zuweisen, für die Sie ein Standardbild oder ein Kreativ-Video angegeben haben.

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
