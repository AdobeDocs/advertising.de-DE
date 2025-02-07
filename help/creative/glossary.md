---
title: Glossar
description: Siehe Definitionen von Schlüsselbegriffen.
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Glossar {#glossary}

*Geschlossene Beta-Version*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**click-through:** Ein Anzeigenklick, der zu einer Konversion führt.

**Datenweiterleitungsziel:** Datenweiterleitungsziele ermöglichen die Auswahl von Anzeigenelementen basierend auf Daten, die in Echtzeit von der DSP, dem Publisher oder dem Partner bereitgestellt werden. Dazu können auch Drittanbieterdaten gehören.

<!-- verify this -->In einem Werbeerlebnis kann jedes Ziel für den Datendurchlauf bis zu fünf Schlüssel-Wert-Paare enthalten. Sie geben die Schlüssel und mindestens einen Wert im ersten Zielknoten auf dieser Ebene an, und dieselben Schlüssel sind für gleichrangige Zielknoten verfügbar. Jedes der Schlüssel-Wert-Paare wird als Makro an das Anzeigen-Tag für dieses Erlebnis angehängt. Zum Zeitpunkt der Anzeigenimpression ist die DSP, der Publisher oder der Partner dafür verantwortlich, die Werte durch für diese Impression spezifische Daten zu ersetzen. Die Informationen werden an [!DNL Creative] zurückgegeben, damit es auf der Grundlage der in dem Erlebnis definierten Regeln ein geeignetes Anzeigenerlebnis anzeigen kann.

Um beispielsweise eine oder mehrere mögliche Kreative auf Betrachterinnen auszurichten, die sich im Segment 1234 befinden, konfigurieren Sie die Datenübergabe-Ziele `gender=female` und `segment=1234` für den Zielknoten. Die DSP, die die Impression bereitstellt, füllt das -Tag mit den Geschlecht- und Segmentinformationen, und Besuchern, die die angegebenen Anforderungen erfüllen, wird eine der zugehörigen Kreativen angezeigt.

**Interaktion-durch:** Eine Anzeigeninteraktion (z. B. ein Video ansehen oder eine Anzeige erweitern), die zu einer Konversion führt.

<!-- or flexible html5 creative variation? -->
**Variante eines flexiblen HTML5-Kreativ-Assets** Eine Ableitung eines flexiblen HTML5-Kreativ-Assets in Ihrem [!UICONTROL Creative Libraries], die generiert wird, wenn Sie das Kreativ-Asset einem Erlebnis zuweisen und eines der Standardattribute innerhalb des Erlebnisses ändern.

<!-- Not sure if this will be implemented, and how:
You can view all derived creatives, including not only the base creatives you've added but also each child creative derivation, in the card view in [!UICONTROL Creative] > [!UICONTROL Libraries]. In the toolbar, click __?__ , and then select Derived Creatives. [Clarify how to tell which have variations. I can't find any now.]
-->

**View-Through:** Eine Anzeigenimpression oder eine Zeichenfolge von Impressionen, die zu einer Konversion führt, ohne dass der Benutzer auf eine Anzeige klickt.
