---
title: Erstellen einer wiederverwendbaren Zielgruppe
description: Erfahren Sie, wie Sie wiederverwendbare Zielgruppen erstellen, die aus Zielgruppensegmenten und anderen gespeicherten Zielgruppen bestehen. Verwenden Sie optional einen KI-unterstützten Zielgruppenagenten, indem Sie Ihre Zielgruppe in Eingabeaufforderungen in natürlicher Sprache beschreiben. Der Agent empfiehlt Drittanbietersegmente und erstellt Zielgruppenausdrücke zur Verwendung als Ziele oder Ausschlüsse.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a4b509995f362ed81e00485409b0c729b5130e35
workflow-type: tm+mt
source-wordcount: 1667
ht-degree: 0%

---

# Erstellen einer wiederverwendbaren Zielgruppe

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Sie können wiederverwendbare Zielgruppen, d. h. Gruppen von Zielgruppensegmenten und sogar andere gespeicherte Zielgruppen, speichern und verwalten. Diese können Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden. Erstellen Sie Zielgruppen manuell oder verwenden Sie den KI-unterstützten Zielgruppen-Agenten, um neue wiederverwendbare Zielgruppen zu generieren, indem Sie alle Erstanbieter- und Drittanbietersegmente verwenden, die Ihnen je nach Ihren angegebenen Anforderungen zur Verfügung stehen.

>[!NOTE]
>
>(Werbetreibende, für die DSP Hash-E-Mail-IDs in LiveRampID-Segmente konvertiert) Erstanbieter-RampID-Segmente, die nicht mit einer aktiven, geplanten oder angehaltenen Platzierung verknüpft sind, werden angehalten. Das Segment wird in der Segmentliste als „Automatisch angehalten“ angegeben.

## Manuelles Erstellen einer wiederverwendbaren Zielgruppe

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

1. In den [!UICONTROL New Audience] Einstellungen:

   1. Eindeutige **[!UICONTROL Audience Name]** eingeben.

   1. (Optional) Deaktivieren Sie die zu **[!UICONTROL Share with all advertisers in my account]** Option.

      Wenn Sie eine Zielgruppe freigeben, wird die Zielgruppe als Ziel oder Ausschluss für alle Advertiser im Konto verfügbar. Die einzelnen Segmente in der Zielgruppe stehen jedoch nur Benutzenden zur Verfügung, für die die Segmente freigegeben sind. Wenn Sie beispielsweise eine Zielgruppe mit Adobe Analytics-Segmenten für einen Advertiser freigeben, der nicht demselben [!DNL Analytics] zugeordnet ist, wird das Segment in dieser Zielgruppe für diesen Advertiser nicht in der Vorschau angezeigt. Nur die Segmente, die diesem Advertiser zur Verfügung stehen, werden in der Zielgruppe in der Vorschau angezeigt.

   1. Klicken Sie auf **[!UICONTROL Save]**.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Switch to manual mode]** im rechten Bedienfeld.

   Die Option KI ist die Standardeinstellung.

1. Erstellen Sie die Zielgruppe:

   >[!NOTE]
   >
   >Beim Erstellen der Zielgruppe werden [&#x200B; Daten zur &#x200B;](audience-about.md) im rechten Bedienfeld aktualisiert

   * Gehen Sie wie folgt vor, um die Segmentlogik mithilfe der Segmente auf den Registerkarten [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] und [!UICONTROL Saved Audiences] manuell &#x200B;](audience-settings.md) erstellen.

      * (Optional) Suchen Sie nach einem Segmentnamen, einer Beschreibung oder einem Pfad.

        Die Suchergebnisse enthalten Segmente, die auf den von Ihnen verwendeten genauen Begriffen basieren. Wenn Sie mehrere Begriffe eingeben, müssen alle Begriffe für ein Segment gefunden werden.

      * Um das erste Segment hinzuzufügen, suchen Sie das Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

      * So fügen Sie ein Segment zu einer vorhandenen Segmentgruppe hinzu:

         1. Klicken Sie auf die Segmentgruppe im rechten Bedienfeld.

         1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* oder *[!UICONTROL Exclude All]*.

            *[!UICONTROL Exclude All]* ist nicht für die erste Segmentgruppe verfügbar. Für eine Zielgruppe, die nur Ausschlüsse enthält, erstellen Sie diese Zielgruppe als *[!UICONTROL Include Any]* und wählen Sie dann innerhalb einer Platzierung diese Zielgruppe aus dem Menü Ausgeschlossene Zielgruppen aus.

         1. Suchen Sie das neue Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

            Die Segmentgruppe wird automatisch mit dem neuen Segment aktualisiert.

      * Hinzufügen einer neuen Segmentgruppe:

         1. Klicken Sie im rechten Bedienfeld auf **[!UICONTROL + New Group]** .

            1. (Optional) Ändern Sie bei Bedarf die Logik zwischen der vorherigen Gruppe und der neuen Gruppe in *[!UICONTROL And]* oder *[!UICONTROL Or]*.

            1. Suchen Sie die Segmente für die neue Gruppe im linken Bereich und aktivieren Sie die Kontrollkästchen neben den Segmentnamen.

            1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* oder *[!UICONTROL Exclude All]*.

   * So verwenden Sie die Segmentlogik einer bestehenden Audience:

      1. Kopieren Sie die Segmentlogik aus der bestehenden Audience auf eine der folgenden Arten:

         * Halten Sie in der Ansicht Alle Zielgruppen den Cursor über die Zeile Zielgruppe und klicken Sie dann auf **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Klicken Sie in den Einstellungen für die vorhandene Zielgruppe oben im Bedienfeld Segmentlogik auf **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Erstellen Sie in einem Texteditor manuell die Segmentlogik mit alphanumerischen Segment-IDs und [boolesche Syntax](audience-segment-logic-syntax.md) und kopieren Sie sie in die Zwischenablage.

      1. Klicken Sie auf **[!UICONTROL paste in an audience rule to begin building]**, fügen Sie die vorhandene Segmentlogik in das Eingabefeld ein und klicken Sie dann auf **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Wenn die Zielgruppe bereits eine Segmentlogik enthält, überschreibt das Einfügen einer neuen Segmentlogik die vorhandene Logik.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Erstellen einer wiederverwendbaren Zielgruppe mit generativer KI

*Beta-Funktion*

*Support nur für Englisch*

>[!NOTE]
>
>Diese Funktion befindet sich im Beta-Modus und kann sich ändern. Stellen Sie sicher, dass der generierte Zielgruppenausdruck die gewünschte Zielgruppe darstellt, bevor Sie die Zielgruppe erstellen und für Ihre Platzierungen verwenden.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

1. In den [!UICONTROL New Audience] Einstellungen:

   1. Eindeutige **[!UICONTROL Audience Name]** eingeben.

   1. (Optional) Deaktivieren Sie die zu **[!UICONTROL Share with all advertisers in my account]** Option.

      Wenn Sie eine Zielgruppe freigeben, wird die Zielgruppe als Ziel oder Ausschluss für alle Advertiser im Konto verfügbar. Die einzelnen Segmente in der Zielgruppe stehen jedoch nur Benutzenden zur Verfügung, für die die Segmente freigegeben sind. Wenn Sie beispielsweise eine Zielgruppe mit Adobe Analytics-Segmenten für einen Advertiser freigeben, der nicht demselben [!DNL Analytics] zugeordnet ist, wird das Segment in dieser Zielgruppe für diesen Advertiser nicht in der Vorschau angezeigt. Nur die Segmente, die diesem Advertiser zur Verfügung stehen, werden in der Zielgruppe in der Vorschau angezeigt.

   1. Klicken Sie auf **[!UICONTROL Save]**.

1. Erstellen Sie die Zielgruppe:

   1. Geben Sie eine oder mehrere Eingabeaufforderungen ein, um die Zielgruppeneigenschaften zu beschreiben, die Sie ein- und ausschließen möchten. Um jede Eingabeaufforderung zu senden, klicken Sie auf ![Senden-](/help/dsp/assets/submit-prompt.png "-Eingabeaufforderung").

      Weitere Informationen finden Sie unter &quot;[&#x200B; von Eingabeaufforderungen](#writing-prompts) und &quot;[Best Practices für die Erstellung einer Zielgruppenbeschreibung](#audience-brief-best-practices).

      Gegebenenfalls schlägt der Agent zusätzliche Segmentfilter vor, um eine effektivere Zielgruppenbeschreibung zu erstellen. Sie können die Vorschläge annehmen oder ablehnen.

      Wenn der Zielgruppen-Agent relevante Segmente findet, wird basierend auf Ihren Kriterien ein boolescher Zielgruppenausdruck erstellt. Außerdem wird um Ihre Genehmigung gebeten, bevor nach übereinstimmenden Segmenten zur Zusammenstellung der Zielgruppe gesucht wird. Sie können optional die Anfrage ignorieren und stattdessen weitere Zielgruppenkriterien angeben.

   1. Wenn der Zielgruppenagent einen Zielgruppenausdruck präsentiert, der Ihre Zielgruppe angemessen beschreibt, weisen Sie den Zielgruppenagenten an, mit der Zusammenstellung der Zielgruppe fortzufahren.

      Sie können „Fortfahren“, „OK“, „OK“, „Ja“ oder ein anderes ähnliches Wort eingeben. Der Agent listet alle vorgeschlagenen Segmente für jede Eigenschaft auf (z. B. „Eltern„). Erweitern Sie eine Eigenschaft, um Details zu den einzelnen Segmenten anzuzeigen, die für diese Eigenschaft vorgeschlagen werden.

   1. Geben Sie bei Bedarf zusätzliche Kriterien an. Wenn der Zielgruppen-Agent einen Zielgruppen-Ausdruck präsentiert, der all Ihre Kriterien erfüllt, weisen Sie den Zielgruppen-Agenten an, mit der Zusammenstellung der Zielgruppe fortzufahren.

      Geben Sie zum Zusammenstellen der Zielgruppe „Fortfahren“, „OK“, „OK“, „Ja“ oder ein anderes ähnliches Wort ein. Der Agent listet alle vorgeschlagenen Segmente für jede Eigenschaft auf (z. B. „Eltern„). Erweitern Sie eine Eigenschaft, um Details zu den einzelnen Segmenten anzuzeigen, die für diese Eigenschaft vorgeschlagen werden.

1. Wenn Sie mit der zusammengestellten Zielgruppe zufrieden sind, klicken Sie auf **[!UICONTROL Create]** , um die angegebene Zielgruppe zu erstellen.

   >[!NOTE]
   >
   >Sie können die Zielgruppe später nicht mehr mit dem Zielgruppen-Agenten bearbeiten. Stattdessen [&#x200B; Sie den Zielgruppenausdruck manuell &#x200B;](/help/dsp/audiences/reusable-audience-edit.md).

### Grundlagen der Eingabeaufforderungen zum Schreiben {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### Was sollte eine Eingabeaufforderung enthalten?

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

Weitere Möglichkeiten zur Optimierung der [&#x200B; für Zielgruppen finden Sie &#x200B;](#audience-brief-best-practices) „Best Practices für die Erstellung einer Zielgruppenkurze“.

<!--
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### Was können Sie in eine Eingabeaufforderung einbeziehen?

* Verweise auf vorhandene Zielgruppenausdrücke.

* Text in Sprachen außer Englisch.

#### Beispiele für Antworten von Zielgruppenagenten und wie geantwortet wird

Wenn der Zielgruppenagent eine Antwort von Ihnen benötigt, können Sie mit Schlüsselwörtern in der Anfrage oder unter Verwendung gängiger Synonyme antworten.

#### Audience Agent stellt eine Frage

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Ihre bejahende Antwort: „Weiter“, „OK“, „Ja“ oder ein anderes ähnliches Wort

Sie können die Anfrage auch ignorieren und stattdessen weitere Zielgruppenkriterien angeben.

##### Zielgruppenagent, der Sie zur Auswahl aus mehreren Optionen auffordert

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Ihre Antwort: `1`, `proceed`, `2`, `maximum reach` usw.

Sie können die Anfrage auch ignorieren und stattdessen weitere Zielgruppenkriterien angeben.

### Best Practices für die Erstellung einer Zielgruppenbeschreibung {#audience-brief-best-practices}

Eine Audience Brief ist eine strategische Zusammenfassung, die die Zielgruppe für eine Kampagne definiert. Ein gut formulierter Überblick hilft dem DSP-Zielgruppenagenten, die relevantesten Segmente zu identifizieren, um Ihre Zielgruppe zusammenzustellen.

#### Wesentliche Komponenten einer effektiven Zielgruppenbeschreibung

Nehmen Sie in Ihre Zusammenfassung so viele Zielgruppenattribut-Typen wie möglich aus der folgenden Liste auf. Geben Sie die Attribute an, die Sie ausschließen möchten.

<!--
 What about these:

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

#### Beispiel für eine gut strukturierte Zielgruppenbeschreibung für eine Interessenskampagne

Im Folgenden finden Sie ein Beispiel für eine überzeugende Zielgruppenbeschreibung für eine Kampagne, mit der Sie auf einen Premium-Abonnement-Service für das Speisen-Kit aufmerksam machen und die Testversion optimieren können:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Über die Zielgruppenverwaltung](audience-about.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Syntax für die Logik von Zielgruppensegmenten](audience-segment-logic-syntax.md)
>* [Verfügbare Datenanbieter von Drittanbietern](third-party-data-providers.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
