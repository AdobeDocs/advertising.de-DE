---
title: Erstellen einer wiederverwendbaren Zielgruppe mit generativer KI
description: Erfahren Sie, wie Sie mit dem KI-unterstützten Zielgruppen-Agenten wiederverwendbare Zielgruppen in Adobe Advertising DSP erstellen. Beschreiben Sie Ihre Zielgruppe in Eingabeaufforderungen in natürlicher Sprache; der Agent schlägt Segmente von Drittanbietern vor und erstellt Zielgruppenausdrücke zur Verwendung als Ziele oder Ausschlüsse.
feature: DSP Audiences
hidefromtoc: true
hide: true
exl-id: 82c9f122-2bdd-409f-a4d6-1da21ecbe913
source-git-commit: 63402a5148f5e4dc310b9d2229a9dddd5fe2f113
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Erstellen einer wiederverwendbaren Zielgruppe mit generativer KI

*Beta-Funktion*

*Eingabeaufforderungen nur in englischer Sprache*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Verwenden Sie den KI-unterstützten Zielgruppenagenten, um entsprechend Ihren angegebenen Anforderungen neue wiederverwendbare Zielgruppen mit allen Drittanbietersegmenten zu generieren, die Ihnen zur Verfügung stehen. Sie können Ihre Zielgruppen als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Diese Funktion befindet sich im Beta-Modus und kann sich ändern. Stellen Sie sicher, dass der generierte Zielgruppenausdruck die gewünschte Zielgruppe darstellt, bevor Sie die Zielgruppe erstellen und für Ihre Platzierungen verwenden.

## Erstellen einer wiederverwendbaren Zielgruppe mit generativer KI

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

1. Eindeutige **[!UICONTROL Audience Name]** eingeben.

1. (Optional) Deaktivieren Sie die zu **[!UICONTROL Share with all advertisers in my account]** Option.

   Wenn Sie eine Zielgruppe freigeben, wird die Zielgruppe als Ziel oder Ausschluss für alle Advertiser im Konto verfügbar. Die einzelnen Segmente in der Zielgruppe stehen jedoch nur Benutzenden zur Verfügung, für die die Segmente freigegeben sind.

1. Klicken Sie auf **[!UICONTROL Save]**.

1. Erstellen Sie die Zielgruppe:

   Für Benutzer mit Beta-Berechtigungen ist die Option KI die Standardoption. Um [&#x200B; Zielgruppe selbst zusammenzustellen](/help/dsp/audiences/reusable-audience-create.md) klicken Sie unten auf die Schaltfläche „In den manuellen Modus wechseln“.

   1. Geben Sie eine oder mehrere Eingabeaufforderungen ein, um die Zielgruppeneigenschaften zu beschreiben, die Sie ein- und ausschließen möchten. Um jede Eingabeaufforderung zu senden, klicken Sie auf ![Senden-](/help/dsp/assets/submit-prompt.png "-Eingabeaufforderung").

      Weitere Informationen finden Sie unter &quot;[&#x200B; von Eingabeaufforderungen](#writing-prompts) und &quot;[Best Practices für die Erstellung einer Zielgruppenbeschreibung](#audience-brief-best-practices).

      Wenn der Zielgruppen-Agent relevante Segmente findet, erstellt er einen Zielgruppen-Ausdruck basierend auf Ihren Kriterien. Außerdem wird um Ihre Genehmigung gebeten, bevor nach übereinstimmenden Segmenten zur Zusammenstellung der Zielgruppe gesucht wird.

      Sie können optional die Anfrage ignorieren und stattdessen weitere Zielgruppenkriterien angeben.

   1. Wenn der Zielgruppenagent einen Zielgruppenausdruck präsentiert, der Ihre Zielgruppe angemessen beschreibt, weisen Sie den Zielgruppenagenten an, mit der Zusammenstellung der Zielgruppe fortzufahren.

      Sie können „Fortfahren“, „OK“, „OK“, „Ja“ oder ein anderes ähnliches Wort eingeben.

   1. Geben Sie bei Bedarf zusätzliche Kriterien an. Wenn der Zielgruppen-Agent einen Zielgruppen-Ausdruck präsentiert, der all Ihre Kriterien erfüllt, weisen Sie den Zielgruppen-Agenten an, mit der Zusammenstellung der Zielgruppe fortzufahren.

      Geben Sie zum Zusammenstellen der Zielgruppe „Fortfahren“, „OK“, „OK“, „Ja“ oder ein anderes ähnliches Wort ein.

1. Wenn Sie mit der zusammengestellten Zielgruppe zufrieden sind, klicken Sie auf **[!UICONTROL Create]** , um die angegebene Zielgruppe zu erstellen.

   >[!NOTE]
   >
   >Sie können die Zielgruppe später nicht mehr mit dem Zielgruppen-Agenten bearbeiten. Stattdessen [&#x200B; Sie den Zielgruppenausdruck manuell &#x200B;](/help/dsp/audiences/reusable-audience-edit.md).

## Grundlagen der Eingabeaufforderungen {#writing-prompts}

### Was sollte eine Eingabeaufforderung enthalten?

* Beschreiben Sie die Zielgruppe in einer klaren, beschreibenden Sprache.

   * Sie können entweder ganze Sätze oder nur eine Zeichenfolge eingeben. Interpunktion ist nicht erforderlich, außer wenn es aus Gründen der Übersichtlichkeit erforderlich ist.

   * Im Allgemeinen wird bei Eingabeaufforderungen nicht zwischen Groß- und Kleinschreibung unterschieden.

   * Der Zielgruppenagent erkennt die häufigsten Synonyme.

* Seien Sie spezifisch und geben Sie Details zu allen Zielgruppeneigenschaften an, die Sie einbeziehen möchten, sowie zu allen Eigenschaften, die Sie ausdrücklich ausschließen möchten. Je mehr Details Sie angeben, desto größer ist die Chance, dass Sie die Ergebnisse erhalten, die Ihren Anforderungen entsprechen.

* Identifizieren Sie Standorte, Gerätetypen und Datenanbieter, die ein- oder ausgeschlossen werden sollen.

* Geben Sie iterativ Details an, um Ihre Kriterien und den generierten Zielgruppenausdruck zu verfeinern, bevor Sie die Zielgruppe speichern.

* Erfahren Sie mehr über Eingabeaufforderungen durch Experimentieren.

  Wenn Ihre Eingabeaufforderung nicht klar ist, fordert der Zielgruppen-Agent einfach eine weitere Eingabeaufforderung an, sodass Sie es erneut versuchen können.

  Der Zielgruppen-Agent speichert einen generierten Zielgruppenausdruck nicht automatisch als Zielgruppe. Sie können eine Zielgruppe nur speichern, indem Sie auf die Schaltfläche [!UICONTROL Create] klicken, die sich außerhalb des Eingabeaufforderungsbereichs befindet, sodass Sie alle Änderungen rückgängig machen können, die Sie nicht beibehalten möchten.

Unter &quot;[&#x200B; Practices für die Erstellung einer Zielgruppe - &#x200B;](#audience-brief-best-practices)&quot; finden Sie weitere Möglichkeiten zur Optimierung der Aufforderungen für Zielgruppen.

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### Was können Sie in eine Eingabeaufforderung einbeziehen?

* Verweise auf vorhandene Zielgruppenausdrücke.

* Text in Sprachen außer Englisch.

### Beispiele für Antworten von Zielgruppenagenten und wie geantwortet wird

Wenn der Zielgruppenagent eine Antwort von Ihnen benötigt, können Sie mit Schlüsselwörtern in der Anfrage oder unter Verwendung gängiger Synonyme antworten.

#### Audience Agent stellt eine Frage

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Ihre bejahende Antwort: „Weiter“, „OK“, „Ja“ oder ein anderes ähnliches Wort

Sie können die Anfrage auch ignorieren und stattdessen weitere Zielgruppenkriterien angeben.

#### Zielgruppenagent, der Sie zur Auswahl aus mehreren Optionen auffordert

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Ihre Antwort: `1`, `proceed`, `2`, `maximum reach` usw.

Sie können die Anfrage auch ignorieren und stattdessen weitere Zielgruppenkriterien angeben.

## Best Practices für die Erstellung einer Zielgruppenbeschreibung {#audience-brief-best-practices}

Eine Audience Brief ist eine strategische Zusammenfassung, die die Zielgruppe für eine Kampagne definiert. Ein gut formulierter Überblick hilft dem DSP-Zielgruppenagenten, die relevantesten Segmente zu identifizieren, um Ihre Zielgruppe zusammenzustellen.

### Wesentliche Komponenten einer effektiven Zielgruppenbeschreibung

Nehmen Sie in Ihre Zusammenfassung so viele Zielgruppenattribut-Typen wie möglich aus der folgenden Liste auf. Geben Sie die Attribute an, die Sie ausschließen möchten.

<!-- What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Demografie**

  Umfasst Attribute wie Altersbereich, Geschlecht, Familienstand, Haushaltszusammensetzung (Familiengröße, Anwesenheit von Kindern, Mehrgenerationenhaushalte).

* **Sozioökonomische Indikatoren**

  Legt die finanzielle Kapazität durch HHI-Bänder (Haushaltseinkommen), Bildungsniveau, Beruf/Stellenbezeichnung, Beschäftigungsstatus und Wohnungseigentumsstatus fest.

* **Geografische Parameter**

  Definiert den Standortbereich, einschließlich Land/Länder, Region (EMEA, APAC, NA), Bevölkerungsdichte (urban/suburban/rural).

* **Interessen und Affinitäten**

  Identifiziert Leidenschaften und Präferenzen wie Hobbys (Sport, Kunst, Outdoor-Aktivitäten), Mediennutzungsmuster, Markenaffinitäten und Lifestyle-Aktivitäten (Reisen, Essen, Unterhaltung).

* **Psychographie**

  Erfasst Denkweisen und Werte, einschließlich Ziele (Statussuche, Selbstverbesserung), Kernwerte (Nachhaltigkeit, Innovation, Tradition), Persönlichkeitsmerkmale (Risikofreudige, frühzeitige Anwendende) und Kaufmotivationen.

* **Verhaltenssignale**

  Beobachtbare Aktionen einschließlich Kaufverhalten (Shopping-Häufigkeit, Kanalvoreinstellungen, Markentreue), Online-Verhalten (Website-Besuche, Inhaltsinteraktion, Social-Media-Aktivitäten) und Offline-Verhalten (Store-Besuche, Veranstaltungsteilnahme, Mitgliedschaften).

* **Marktinteraktion**

  Identifiziert die Kaufbereitschaft durch recherchierte Produkt-/Servicekategorien, den Kaufzeitplan (unmittelbar, kurzfristig, langfristig) und relevante Lebensereignisse, die Kaufentscheidungen auslösen.

* **Lebensstadium**

  Aktuelle Phase des Verständnisses einschließlich der Karrierephase (Student, Einsteiger, in der Mitte der Karriere, Führungskraft, im Ruhestand), Familienphase (frisch verheiratete Frauen, neue Eltern, leere Nester) und wichtige Übergänge im Leben.

### Beispiel für eine gut strukturierte Zielgruppenübersicht für eine Interessenskampagne

Im Folgenden finden Sie ein Beispiel für eine überzeugende Zielgruppenbeschreibung für eine Kampagne, mit der Sie auf einen Premium-Abonnement-Service für das Speisen-Kit aufmerksam machen und die Testversion optimieren können:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Duplizieren Sie eine wiederverwendbare Zielgruppe](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [Wiederverwendbare Zielgruppe bearbeiten](/help/dsp/audiences/reusable-audience-edit.md)
>* [Anzeigen von Details zu wiederverwendbaren Zielgruppen](/help/dsp/audiences/reusable-audience-view-details.md)
>* [Freigeben einer wiederverwendbaren Zielgruppe](/help/dsp/audiences/reusable-audience-share.md)
>* [Exportieren Sie eine wiederverwendbare Zielgruppe](/help/dsp/audiences/reusable-audience-export.md)
>* [Kopieren Sie den Segmentschlüssel für eine wiederverwendbare Zielgruppe in die Zwischenablage](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [Löschen einer wiederverwendbaren Zielgruppe](/help/dsp/audiences/reusable-audience-delete.md)
