---
title: Glossar
description: Siehe Definitionen von Schlüsselbegriffen.
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Glossar {#glossary}

*Geschlossene Beta-Version*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**click-through:** Ein Anzeigenklick, der zu einer Konversion führt.

**Datenweiterleitungsziel:** Datenweiterleitungsziele ermöglichen die Auswahl von Anzeigenelementen basierend auf Daten, die in Echtzeit vom DSP, Publisher oder Partner bereitgestellt werden. Dazu können auch Drittanbieterdaten gehören.

<!-- verify this -->In einem Werbeerlebnis kann jedes Ziel für den Datendurchlauf bis zu fünf Schlüssel-Wert-Paare enthalten. Sie geben die Schlüssel und mindestens einen Wert im ersten Zielknoten auf dieser Ebene an, und dieselben Schlüssel sind für gleichrangige Zielknoten verfügbar. Jedes der Schlüssel-Wert-Paare wird als Makro an das Anzeigen-Tag für dieses Erlebnis angehängt. Zum Zeitpunkt der Anzeigenimpression ist der DSP, der Publisher oder der Partner dafür verantwortlich, die Werte durch für diese Impression spezifische Daten zu ersetzen. Die Informationen werden an [!DNL Creative] zurückgegeben, damit es auf der Grundlage der in dem Erlebnis definierten Regeln ein geeignetes Anzeigenerlebnis anzeigen kann.

Um beispielsweise eine oder mehrere mögliche Kreative auf Betrachterinnen auszurichten, die sich im Segment 1234 befinden, konfigurieren Sie die Datenübergabe-Ziele `gender=female` und `segment=1234` für den Zielknoten. Die DSP, die die Impression bereitstellt, füllt das -Tag mit den Geschlechts- und Segmentinformationen, und Besucherinnen und Besuchern, die die angegebenen Anforderungen erfüllen, wird eine der zugehörigen Kreativen angezeigt.

**Interaktion-Through:** Eine Interaktion mit der Anzeige (z. B. das Scrollen durch eine Karussellanzeige oder das Erweitern einer Anzeige), die zu einer Konversion führt. Dieser Ereignistyp ist unabhängig vom Klicken auf die Anzeige, um zu einer Landingpage oder einem Ereignis auf der Landingpage zu gelangen.

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**View-Through:** Eine Anzeigenimpression oder eine Zeichenfolge von Impressionen, die zu einer Konversion führt, ohne dass der Benutzer auf eine Anzeige klickt.
