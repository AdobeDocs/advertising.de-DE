---
title: Das Layout des Entscheidungsbaums
description: Erfahren Sie mehr über das Entscheidungsbaum-Layout für Erlebnisse beim Targeting.
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Das Entscheidungsbaum-Layout für [!DNL Creative] Erlebnisse

*Geschlossene Beta-Version*

Wenn Sie die Option &quot;[!UICONTROL Targeting]&quot; für ein Erlebnis aktivieren, richten Sie das Erlebnis mithilfe eines Entscheidungsbaums ein.

Zunächst beginnt jeder Entscheidungsbaum mit der Stammebene „Alle“. Sie können einen oder mehrere Zielknoten hinzufügen und dann den endgültigen Knoten in jeder Verzweigung des Entscheidungsbaums kreative Bundles zuweisen.

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
-->

<!-- insert screen capture -->

## Begriffe

**Tree:** Die gesamte Entscheidungsstruktur als Baum mit Verzweigungen.

**Zielknoten:** Ein Ziel innerhalb einer Verzweigung.

**Blattknoten:** Eine Reihe von Kreativen, die einem endgültigen Zielknoten zugewiesen sind.

## Ziele in einem Entscheidungsbaum

Jeder Entscheidungsbaum kann bis zu fünf Zielgruppenebenen haben. Jede Zielebene kann mehrere Verzweigungen mit jeweils einem oder mehreren Knoten mit demselben Zieltyp enthalten (Zielgruppensegment, geografischer Standorttyp, Werte für angegebene Datenübergabeschlüssel, Attribute für ein bestimmtes Retargeting-Pixel oder Gerätekategorie). Sie können den Zielknoten der untersten Ebene kreative Bundles in jeder Anzeigengröße zuweisen, für die Sie ein Standardbild für kreative Inhalte angegeben haben.

<!--insert screen capture -->

Wenn Sie der letzten Ebene einen Zielknoten hinzufügen, geben Sie das Ziel für den neuen Knoten an. Ein zusätzlicher gleichrangiger Knoten, „Alles andere“, wird automatisch für alle erstellt, die nicht mit dem angegebenen Ziel übereinstimmen. Anschließend können Sie zusätzliche gleichrangige Knoten mit verschiedenen Zielen desselben Typs hinzufügen.

Wenn Sie jedoch einen Zielknoten zwischen vorhandenen Ebenen einfügen, wird der erste Knoten für die neue Ebene zunächst „Alle“ zugewiesen. Um eine bestimmte Zielgruppe zu identifizieren, erstellen Sie einen gleichrangigen Zielknoten auf derselben Ebene, für den Sie die tatsächliche Zielgruppe angeben. Dadurch wird der Zielknoten erstellt und der Knoten „Alle“ durch einen Knoten „Alles andere“ ersetzt (der alle Kreativ-Bundles enthält, die zuvor allen zugewiesen waren). Anschließend können Sie zusätzliche gleichrangige Knoten mit verschiedenen Zielen desselben Typs hinzufügen.

Für alle übergeordneten Knoten können Sie optional alle untergeordneten Zielknoten und kreativen Bundles kopieren und in einen anderen Knoten derselben Ebene einfügen, indem Sie sie entweder zum vorhandenen Framework hinzufügen oder das vorhandene Framework ersetzen.

## Kreative in einem Entscheidungsbaum

Weisen Sie jedem endgültigen Zielknoten im Erlebnis kreative Bundles zu.

Innerhalb jedes Knotens mit kreativen Bundles können Sie die enthaltenen Kreativen entweder nach einer bestimmten Gewichtung oder algorithmisch drehen, um die Clickthrough-Rate oder ein benutzerdefiniertes Ziel zu optimieren. Optional können Sie die Kreativen auch in einer bestimmten Zeitsequenz drehen, indem Sie dieselben Optionen verwenden.

Sie können bei Bedarf die URLs für Landingpages, Impression-Tracking-URLs und Klick-Tracking-URLs für einzelne Kreative anpassen. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Über Erlebnisse auf Advertising Creative 2.0](experience-about.md)
