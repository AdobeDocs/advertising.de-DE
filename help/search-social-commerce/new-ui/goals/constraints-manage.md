---
title: Verwalten von Einschränkungen für Suchangebotseinheiten
description: Erfahren Sie mehr über Einschränkungen zum Beschränken von Geboten für Gebotseinheiten in CPC-Kampagnen in alten Portfolios auf Keyword-Ebene.
feature: Search Campaign Management, Search Optimization
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '2649'
ht-degree: 0%

---

# Verwalten von Einschränkungen für Suchangebotseinheiten

*Gilt nur für Gebotseinheiten in CPC-Kampagnen in alten Portfolios auf Keyword-Ebene*

Einschränkungen für Gebotseinheiten sind Regeln, die optimierte Gebote für alle [Gebotseinheiten](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html) mit Kosten- und Umsatzmodellen einschränken, die mit der Einschränkung verknüpft sind.

## Über Einschränkungen

Jede Einschränkung gilt für eine bestimmte Währung und umfasst optional Auslösebedingungen, die während eines bestimmten Datenauswertungszeitraums erfüllt sein müssen, damit die Regel angewendet wird. Zu den auszuwertenden Daten können der Kanaltyp, der Übereinstimmungstyp, Klickdaten, Konversionsdaten oder abgeleitete Metriken gehören. Sie können beispielsweise Gebote auf eine bestimmte Währungsspanne beschränken, Gebote kontinuierlich um einen bestimmten Betrag erhöhen oder verringern oder Gebote nach dem Durchschnittsgebot für das Portfolio Gebote abgeben. Jede Einschränkung verfügt über ein anwendbares Startdatum und läuft entweder an einem bestimmten Datum ab oder wird auf unbestimmte Zeit angewendet.

Nachdem Sie eine Begrenzung eingerichtet haben, können Sie sie bestimmten Gebotseinheiten oder allen Gebotseinheiten innerhalb bestimmter Anzeigengruppen oder Kampagnen zuweisen. Jede Gebotseinheit kann eine Beschränkung aufweisen. Einschränkungen werden von untergeordneten Entitäten übernommen, können jedoch überschrieben werden. Eine Beschränkung, die auf der niedrigsten Ebene zugewiesen wird, überschreibt immer eine Beschränkung, die auf der übergeordneten Ebene zugewiesen wird. Wenn Sie einer Gebotseinheit eine Beschränkung zuweisen, erfolgt das Gebot innerhalb der für diese Gebotseinheit festgelegten Beschränkungen, unabhängig davon, wie viel Umsatz die Gebotseinheit generiert, wenn die Gebotseinheit über Kosten- und Umsatzmodelle verfügt.

>[!CAUTION]
>
>Wenn Sie einer Gebotseinheit Einschränkungen zuweisen, überschreiben Sie die Entscheidung des Gebotsoptimierungssystems und übernehmen die Verantwortung für den ROI dieser Gebotseinheit selbst.

>[!NOTE]
>
>* Aktive Einschränkungen beschränken die Gebotsabgabe nur für zugewiesene Gebotseinheiten in optimierten alten Portfolios auf Keyword-Ebene. Sie werden bei Gebotseinheiten ignoriert, die sich in hybriden Portfolios befinden, sich in aktiven Portfolios befinden oder nicht in Portfolios sind. **Tipp:** Aktivieren Sie in den Portfolioeinstellungen die Option „Portfolio-Beschränkungen automatisch anpassen“. Der empfohlene Wert für „Mehrere“ ist „1“.
> * Angebotsbeschränkungen werden bei Gebotseinheiten ignoriert, die nicht über genügend Daten verfügen, um Kosten- und Umsatzmodelle zu generieren.
>* (Kampagnen mit einer CPC- oder eCPC-Bid-Strategie) Wenn eine Bid-Beschränkung mit einem Bid-Limit auf Portfolioebene in Konflikt steht, überschreibt die Beschränkung die Beschränkung auf Portfolioebene. Wenn beispielsweise das Mindestgebot eines Portfolios 5 USD beträgt, Sie aber eine Gebotseinheit im Portfolio auf ein Mindestgebot von 3 USD beschränken, wird die Gebotseinheit auf 3 USD oder mehr geboten. Die Gesamtausgaben für begrenzte Gebotseinheiten werden jedoch durch den [&#x200B; „Spend Around Constraints“ des Portfolios &#x200B;](#spend-around-constraints).
>* Beschränkungen gelten für das Basisgebot. Jede Art von Angebotsanpassung am Basisangebot (z. B. Anhebung des Angebots für Endbenutzer auf Mobilgeräten) kann dazu führen, dass das Angebot außerhalb des für die Einschränkung zulässigen Bereichs liegt. Wenn die Einschränkung beispielsweise eine maximale CPC von 6 USD erfordert, das Basisgebot bereits 6 USD beträgt und das Portfolio die Angebotsanpassungen für Mobilgeräte automatisch mit 50 %-60 % optimiert, beträgt die maximale CPC 9,00-9,60 USD - nicht 6 USD.

### Einschränkungstypen {#constraint-types}

* **[!UICONTROL Bid]:** Gebote auf einen Währungsbereich beschränkt.

* **[!UICONTROL Bid Shift]:** Ändert innerhalb der Gebotsgrenzen die optimierten Gebote für alle zugehörigen Gebotseinheiten kontinuierlich um einen bestimmten Betrag. Eine Gebotsverschiebung führt dazu, dass die relevanten Portfolios um den Gesamtbetrag, der durch die Gebotsverschiebung verursacht wurde, zu viel oder zu wenig ausgeben, unabhängig von der Portfolioeinstellung „Ausgaben um Beschränkungen“. Hinweis: Wenn das aktuelle CPC-Gebot bereits größer oder gleich dem Max. Gebot oder kleiner oder gleich dem Min. Gebot ist, wird die Beschränkung ignoriert und das Gebot wird nicht geändert. Außerdem werden Einschränkungen hinsichtlich der Angebotsverschiebung nicht auf Gebotseinheiten angewendet, die nicht über genügend Daten verfügen, um Kosten- und Umsatzmodelle zu generieren.

* **[!UICONTROL Incremental Bidding]:** (gilt nur für Schlüsselwörter ohne Impressionen) Erhöht oder verringert das Gebot inkrementell mit einem bestimmten Satz, bis das Gebot ein bestimmtes Ziel erreicht.

* **[!UICONTROL Search Engine Min Bid]:** (nur [!DNL Google Ads]) Verwendet die von der Suchmaschine bestimmten CPC-Mindestgebote als Mindestgebote. Wenn die Suchmaschine ihre Mindestgebote ändert, ändert sich Ihr Gebot entsprechend. Sie können optional zusätzliche Gebotslimits für alle zugehörigen Gebotseinheiten angeben.

* **[!UICONTROL Impression Share]:** ([!DNL Google Ads] und [!DNL Microsoft Advertising] CPC-Kampagnen nur mit exakter Übereinstimmung) Beschränkt Gebote auf einen Geldbereich, wenn die Anzeigen zwischen einem minimalen und einem maximalen Impression-Anteil liegen. **Hinweis:** Wenn die Einschränkung nicht kosteneffizient ist, kann sie von der Optimierungsfunktion überschrieben werden.

### Wann Beschränkungen angewendet werden sollten

Einige Gründe für die Beschränkung von Gebotseinheiten sind:

* Um ungetestete Keywords und Anzeigen schnell verfügbar zu machen.

* Um Risiken für neue Portfolios, Konten, Kampagnen und Anzeigengruppen zu minimieren. Bevor Sie beispielsweise ein Portfolio starten, können Sie maximale Gebote für Gebotseinheiten mit hohem Traffic festlegen und dann die Werte jeden Tag schrittweise erhöhen. Dadurch kann das Gebotsmodell jeden Tag angepasst werden, ohne dass das Risiko großer Gebotserhöhungen besteht.

* So stellen Sie sicher, dass Tail-Keywords mit hohen Konversionsraten nicht heruntergefahren werden.

* Um bestimmte Termini aufzubieten, die für Ihre Marke oder bei Werbeaktionen von zentraler Bedeutung sind.

### Anzeigen von Informationen zu Einschränkungen in der Benutzeroberfläche

Neben dem Öffnen der [[!UICONTROL Constraints] können &#x200B;](#constraints-view) Informationen zu Ihren Einschränkungen auf folgende Weise anzeigen:

* All Ihre Einschränkungen sind Kennzeichnungswerte für eine einzelne [Kennzeichnungsklassifizierung](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html) genannt &quot;[!UICONTROL Constraints]&quot;.

   * &quot;[!UICONTROL Constraints]&quot; ist in der Liste &quot;[!UICONTROL Classifications]&quot; in Ihren standardmäßigen und benutzerdefinierten Ansichtseinstellungen sowie in terminierten Berichten enthalten. Sie können die Spalte dort hinzufügen, wo Sie die den entsprechenden Entitäten zugewiesenen Einschränkungen anzeigen möchten.

   * Wenn Sie eine Bulksheet herunterladen, wird &quot;[!UICONTROL Constraints]&quot; in der Spalte &quot;[!UICONTROL Classifications]&quot; für die entsprechenden Entitäten im [!UICONTROL Download Bulksheet]-Dialogfeld aufgeführt. Wenn Sie die Spalte einbeziehen, enthält die heruntergeladene Bulksheet alle Einschränkungen, die den entsprechenden Entitäten zugewiesen sind.

  Die [!UICONTROL Constraints] Klassifizierung ist nicht in der [!UICONTROL Label Classifications] enthalten - die [!UICONTROL Constraints] ist separat. Die [!UICONTROL Constraints] Klassifizierung ist auch nicht in der 30-Label-Klassifizierungsgrenze enthalten.

* [Die [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md) enthält Kosten-, Klick- und (optional) Konversionsdaten für Einschränkungen, die die Architektur der Kennzeichnungsklassifizierung verwenden.

### Die [!UICONTROL Constraints] {#constraints-view}

Die Ansicht [!UICONTROL Goals] > [!UICONTROL Constraints] listet alle Ihre Einschränkungen auf. Zu den verfügbaren Spalten gehören der Einschränkungsstatus, der Einschränkungstyp, das Start- und Enddatum, die Anzahl der Kampagnen, Anzeigengruppen, Schlüsselwörter, Anzeigen, Platzierungen, automatischen Targets und Produktgruppen, mit denen die Einschränkung verknüpft ist, Impressionen, Klicks und Kostendaten sowie Umsatzdaten für alle sichtbaren Konversionsmetriken.<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>Die Leistungsdaten für eine Zeile in der [!UICONTROL Constraints] entsprechen möglicherweise nicht den Leistungsdaten für die Entität der obersten Ebene, der die Einschränkung zugewiesen ist. Da eine Begrenzung, die auf der untersten Ebene zugewiesen wird, eine Beschränkung, die auf der übergeordneten Ebene zugewiesen wird, immer überschreibt, wird eine Begrenzung, die einer Kampagne oder Anzeigengruppe zugewiesen wird, möglicherweise nicht mehr den untergeordneten Anzeigengruppen und Schlüsselwörtern zugewiesen. Wenn beispielsweise Kampagne A Einschränkung A zugewiesen wird, erben automatisch alle Anzeigengruppen und Keywords in Kampagne A Einschränkung A. Diese Anzeigengruppen und Keywords können später jedoch anderen Einschränkungen zugewiesen werden, z. B. Einschränkung B, und sie verlieren dann ihre Zuordnung zu Einschränkung A.

>[!NOTE]
>
>Weisen Sie den Gebotseinheiten Beschränkungen zu, und heben Sie deren Zuweisung in der entsprechenden Ansicht der Entitätsverwaltung auf (z. B. in der Ansicht [!UICONTROL Campaigns] für Beschränkungen auf Kampagnenebene).

#### Verfügbare Aktionen

* [Erstellen einer &#x200B;](#constraint-create).

* [Bearbeiten von &#x200B;](#constraint-edit).

* [Ändern des Status von Einschränkungen](#constraint-change-status).

## Erstellen einer Einschränkung {#constraint-create}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. Klicken Sie in der Symbolleiste oben rechts über der Datentabelle auf **[!UICONTROL Create Constraint]**.

1. Geben Sie die [Einschränkungseinstellungen](#constraint-settings) ein.

   Um zwischen der Registerkarte [!UICONTROL Constraint Type] und der Registerkarte [!UICONTROL Conditions] zu wechseln, klicken Sie entweder auf die Registerkarte, die Sie öffnen möchten, oder klicken Sie auf die Schaltflächen [!UICONTROL Next] und [!UICONTROL Back] .

1. Klicken Sie auf **[!UICONTROL Review and Save]** , um die Einstellungen zu überprüfen.

1. Klicken Sie auf **[!UICONTROL Save]**.

Nachdem Sie eine Einschränkung erstellt haben, können [&#x200B; sie &#x200B;](#constraint-assign) Kampagnen, Anzeigengruppen, Keywords, Platzierungen und Produktgruppen auf Einheitenebene zuweisen.

## Einschränkungseinstellungen bearbeiten {#constraint-edit}

Sie können die Einstellungen für jeweils eine Beschränkung bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Optional) Filtern Sie die Liste [aus der Symbolleiste](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) oder aus einer [Spaltenüberschrift](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Aktivieren Sie das Kontrollkästchen neben der Einschränkung, die Sie bearbeiten möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten").

1. Bearbeiten Sie die [Einschränkungseinstellungen](#constraint-settings).

   Um zwischen der Registerkarte [!UICONTROL Constraint Type] und der Registerkarte [!UICONTROL Conditions] zu wechseln, klicken Sie entweder auf die Registerkarte, die Sie öffnen möchten, oder klicken Sie auf die Schaltflächen [!UICONTROL Next] und [!UICONTROL Back] .

1. Klicken Sie auf **[!UICONTROL Review and Save]** , um die Einstellungen zu überprüfen.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Ändern des Status von Einschränkungen {#constraint-change-status}

Sie können jede aktive Einschränkung anhalten, um sie zu deaktivieren. Sie können sie später aktivieren, indem Sie den Status wieder zurück in *aktiv* ändern.

Sie können auch eine Einschränkung löschen, wodurch alle Verknüpfungen mit Kontokomponenten entfernt werden und die Einschränkung für die zukünftige Verwendung nicht mehr verfügbar ist. Berichtsdaten für die Einschränkung sind nicht mehr verfügbar. **Hinweis:** Um eine Einschränkung einfach von einer Kontokomponente zu trennen, siehe &quot;[Zuweisung von Einschränkungen zu Suchangebotseinheiten aufheben](#constraints-unassign).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Optional) Filtern Sie die Liste [aus der Symbolleiste](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) oder aus einer [Spaltenüberschrift](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Aktivieren Sie das Kontrollkästchen neben jeder Einschränkung, deren Status geändert werden soll.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf die Schaltfläche Status :

   * Um alle ausgewählten Zeilen zu aktivieren, klicken Sie auf ![Aktivieren](/help/search-social-commerce/assets/activate-new.png "Aktivieren").

   * Um alle ausgewählten Zeilen anzuhalten, klicken Sie auf ![Pause](/help/search-social-commerce/assets/pause-new.png "Pause").

   * Um alle ausgewählten Zeilen zu löschen, klicken Sie auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen").

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Einschränkungseinstellungen {#constraint-settings}

| Tabulator | Parameter | Beschreibung |
|---|---|---|
| \[Grundlegende Informationen\] | [!UICONTROL Constraint Name] | Ein eindeutiger Name für die Einschränkung. |
| | [!UICONTROL Currency] | Die Währung, in der alle anwendbaren Gebotseinheiten geboten werden. Gebotseinheiten, für die eine andere Währung verwendet wird, werden ignoriert. |
| | [!UICONTROL Status] | Der Status der Einschränkung:<ul><li>**Aktiv:** (Standard) Die Begrenzung wird während der angegebenen Bedingungen und des angegebenen Datumsbereichs angewendet.</li><li>**Paused:** Die Einschränkung wird nicht angewendet.</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | Der Typ der Einschränkung. Beschreibungen der Einschränkungstypen und der für sie infrage kommenden Anzeigennetzwerke finden Sie unter &quot;[Einschränkungstypen](#constraint-types). |
| | [!UICONTROL Start Date] | Der erste Tag, an dem die Begrenzung wirksam wird. Der Standardwert ist der aktuelle Tag. Um das Datum zu ändern, geben Sie ein Datum ein oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar-new.png "Kalender"), um den Kalender zu öffnen und ein Datum auszuwählen. |
| | [Enddatum] | Ob die Einschränkung an einem bestimmten Datum ungültig wird. Wenn Sie die Einschränkung auf unbestimmte Zeit anwenden möchten, z. B. wenn die Gebotseinheit für die Marke des Unternehmens von zentraler Bedeutung ist, lassen Sie das Feld leer. Um die Einschränkung auf ein bestimmtes Datum zu beenden, geben Sie ein Datum ein oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar-new.png ""), um den Kalender zu öffnen und ein Datum auszuwählen. **Hinweis:** Die Einschränkung kann nicht vor morgen ablaufen. |
| | [!UICONTROL Set constraint options for Bid] | (Nur [!UICONTROL Bid] Einschränkungen) Zu den Einstellungen gehören:<ul><li>**[!UICONTROL Min Bid]:** Das Mindestgrundgebot für zugehörige Gebotseinheiten.</li><li>**[!UICONTROL Max Bid]:** Das maximale Basisgebot für zugehörige Gebotseinheiten.</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | (Nur [!UICONTROL Bid Shift]) Art und Umfang der Gebotsverschiebung, die kontinuierlich auf das Basisgebot angewandt wird:<ul><li>*[!UICONTROL Increases]:* Erhöht Gebote um einen bestimmten Prozentsatz oder Währungswert. Geben Sie den zu ändernden Betrag ein und wählen Sie dann entweder *$* oder *%*. Geben Sie auch einen **[!UICONTROL Max Limit]** ein, der das höchstmögliche Angebot (Obergrenze) bei Anwendung der Begrenzung darstellt. **Hinweis:** Wenn das aktuelle CPC-Angebot bereits gleich oder größer als das [!UICONTROL Max Limit] ist, wird die Einschränkung ignoriert und das Angebot wird nicht geändert.</li><li>*[!UICONTROL Decreases]:* Senkt Gebote um einen bestimmten Prozentsatz oder Währungswert. Geben Sie den zu ändernden Betrag ein und wählen Sie dann entweder *$ oder %*. Geben Sie auch einen **[!UICONTROL Min Limit]** ein, der das niedrigstmögliche Gebot (Untergrenze) ist, wenn die Begrenzung angewendet wird. **Hinweis:** Wenn das aktuelle CPC-Angebot bereits gleich oder kleiner als das [!UICONTROL Min Limit] ist, wird die Einschränkung ignoriert und das Angebot wird nicht geändert.</li></ul>**Hinweise:**<ul><li>Eine Gebotsverschiebung führt dazu, dass die betreffenden Portfolios um den durch die Gebotsverschiebung verursachten Gesamtbetrag zu hoch oder zu niedrig ausgegeben werden, unabhängig von der Portfolioeinstellung auf &quot;[!UICONTROL Spend Around Constraints]&quot;.</li><li>Wenn Sie ein Enddatum für die Begrenzung angeben und die Optimierungsfunktion die Ausgabenbeschränkungen für die Kampagnen im Portfolio automatisch anpasst, werden die Angebote nicht einfach auf die ursprünglichen Beträge nach dem Enddatum zurückgesetzt, sondern als optimal angepasst.</li><li>Gebotsverschiebungen werden nicht auf Gebotseinheiten ohne genügend Daten angewendet, um Kosten- und Umsatzmodelle zu generieren.</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | (Nur [!UICONTROL Incremental Bidding]) Ein Gebotsziel und wie viel und wie oft das Gebot inkrementell erhöht oder verringert werden soll, bis es das Ziel erreicht:<ul><li>**[!UICONTROL Bid target]:** Der Zielbietungsbetrag.</li><li>**[!UICONTROL Incrementally change bids by]** und **[Type]:** Wie stark die Gebote inkrementell erhöht oder verringert werden sollen und ob die Gebote durch einen Währungswert (**$**) oder einen Prozentsatz (*%*) geändert werden sollen.</li><li>**[!UICONTROL Every __ days]:** Wie oft Gebote erhöht werden sollen.</li></ul>Angenommen, das aktuelle Gebot für eines der Keywords beträgt 100 Cent und Sie möchten das Gebot täglich um 10 % ändern, bis Sie ein Gebotsziel von 500 Cent erreicht haben. Am Tag 1, nachdem die Begrenzung festgelegt wurde, beträgt das Gebot für dieses Keyword 110 Cent (aktuelles Gebot + 10 %). An Tag 2 beträgt das Gebot 120 Cent (aktuelles Gebot für Tag 1 + 20 %) usw. Wenn das Gebotsziel jedoch 50 Cent beträgt und die anderen Parameter dieselben sind, verringern sich die Gebote schrittweise, bis das Gebot 50 Cent erreicht. |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | ([!UICONTROL Search Engine Min Bid] Einschränkungen) Verwendet das erforderliche Mindestgebot, um eine Gebotseinheit auf der ersten Seite der Suchergebnisse in Google anzuzeigen ([!UICONTROL Google First Page CPC]). Geben Sie optional einen **[!UICONTROL Min Bid]** und/oder einen **[!UICONTROL Max Bid]** ein, um den Bereich der geeigneten Gebote für die Beschränkung zu definieren. Wenn Sie beispielsweise einen [!UICONTROL Min Bid] von 2,50 USD und einen [!UICONTROL Max Bid] von 4 USD angeben, bieten Sie nicht auf der Gebotseinheit, wenn das Gebot für die [!DNL Google Ads] erste Seite unter 2,50 USD oder über 4 USD liegt. |
| | [!UICONTROL Set constraint options for Impression Share] | (Nur [!UICONTROL Impression Share] Einschränkungen) Zu den Einstellungen gehören:<ul><li>**[!UICONTROL Min Bid]** (Optional) Das Mindestbasisgebot für die zugehörigen Gebotseinheiten.</li><li>**[!UICONTROL Max Bid]:** (Optional) Das maximale Basisgebot für zugehörige Gebotseinheiten.</li><li>**[!UICONTROL Min Impression Share]:** Der niedrigste Impressionsanteil, ausgedrückt in Prozent, der die Begrenzung für die entsprechenden Gebotseinheiten Trigger. Es muss zwischen 10 und 90 sein. **Hinweis:** Wenn die Einschränkung nicht kosteneffizient ist, kann sie von der Optimierungsfunktion überschrieben werden.</li><li>**[!UICONTROL Max Impression Share]:** Der höchste Impression-Anteil, in Prozent, der die Begrenzung für die entsprechenden Gebotseinheiten Trigger. Er muss zwischen 10 und 90 liegen.**Hinweis:** Wenn die Einschränkung nicht kosteneffizient ist, kann sie von der Optimierungsfunktion überschrieben werden.</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | Ob Bedingungen auf die Einschränkung angewendet werden sollen:<ul><li>*[!UICONTROL No Condition]:* (Standard) Die Einschränkung wird während des angegebenen Datumsbereichs bedingungslos angewendet.</li><li>*[!UICONTROL Satisfy]:* Die Einschränkung wird nur angewendet, wenn bestimmte Bedingungen während eines bestimmten Datenauswertungszeitraums erfüllt sind.</li></ul> |
| | [!UICONTROL Data Evaluation Period] | (Wenn Bedingungen festgelegt sind) Der Zeitraum, für den Daten für die angegebenen Kriterien bewertet werden sollen. Wenn Sie *[!UICONTROL Custom date range],**&#x200B; auswählen, geben Sie den &#x200B;** [!UICONTROL Start Date] **&#x200B; und die &#x200B;** [!UICONTROL End Date]** an, indem Sie jedes Datum im `MM-DD-YYYY` Format eingeben (z. B. 03-29-2026 für den 29. März 2026) oder indem Sie ![Kalenderschaltfläche](/help/search-social-commerce/assets/calendar-new.png "Kalenderschaltfläche") klicken, um den Kalender zu öffnen und jedes Datum auszuwählen. |
| | [!UICONTROL When to Apply Constraints] | (Wenn Bedingungen festgelegt sind) Wie viele Filterbedingungen müssen erfüllt sein, damit die Einschränkung angewendet wird:<ul><li>*[!UICONTROL Match All Filters]:* Wendet die Einschränkung an, wenn jede angegebene Filterbedingung erfüllt ist.</li><li>*[!UICONTROL Match Any Filters]:* Wendet die Einschränkung an, wenn mindestens eine der angegebenen Filterbedingungen erfüllt ist.</li></ul> |
| | [!UICONTROL Filters] | (Wenn Bedingungen festgelegt sind) Ein oder mehrere Kriterien, die erfüllt sein müssen. Um einen Filter zu erstellen, wählen Sie eine Eigenschaft oder Metrik aus der Liste aus. Wählen Sie für Eigenschaften (z. B. [!UICONTROL Channel Type]) die entsprechenden Werte in der Liste aus. Wählen Sie für Metriken (z. B. [!UICONTROL Clicks]) einen Operator aus und geben Sie dann den entsprechenden Wert ein. Um beispielsweise nur Gebotseinheiten mit mehr als 100 Klicks zurückzugeben, wählen Sie **Klicks**, wählen Sie **größer als** aus und geben Sie dann `100` in das Eingabefeld ein.</li></ul> |

## Zuweisen von Einschränkungen zu Suchangebotseinheiten {#constraint-assign}

Sie können Einschränkungen für Gebotseinheiten auf jede Kampagne, Anzeigengruppe, jedes Keyword, jede Platzierung, jede Shopping-Produktgruppe auf Einheitenebene (die niedrigste Ebene der Unterteilung) oder auf dynamische Suchziele anwenden.

Jede Entität kann nur eine Einschränkung aufweisen. Sie können einer oder mehreren Entitäten gleichzeitig eine einzelne Einschränkung zuweisen.

>[!NOTE]
>
>Wenn Sie später ein Keyword oder die Anzeigenkopie für eine Anzeige bearbeiten und so ein neues Keyword oder eine neue Anzeige erstellen, wird die Begrenzung nicht der neuen Entität zugewiesen.

1. Öffnen Sie im Hauptmenü die entsprechende Verwaltungsansicht.

   Um beispielsweise Begrenzungen auf Kampagnenebene zuzuweisen, navigieren Sie zu [!UICONTROL Manage] > [!UICONTROL Campaigns].

   <!-- for [campaigns](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [ad groups](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [keywords](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md), or [placements](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md). And ADD LINKS WHEN AVAILABLE for shopping product groups and dynamic search targets. -->

1. (Optional) Filtern Sie die Liste [aus der Symbolleiste](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) oder aus einer [Spaltenüberschrift](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Aktivieren Sie das Kontrollkästchen neben jeder Entität, der Sie eine einzelne Begrenzung zuweisen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

## Zuweisung von Einschränkungen zu Suchangebotseinheiten aufheben {#constraints-unassign}

**Hinweis:** Sie eine Einschränkung löschen und für die zukünftige Verwendung nicht verfügbar machen, finden Sie weitere Informationen unter [Ändern des Status von Einschränkungen](#constraint-change-status).

1. Öffnen Sie im Hauptmenü die entsprechende Verwaltungsansicht.

   Um beispielsweise die Zuweisung von Beschränkungen auf Kampagnenebene aufzuheben, navigieren Sie zu [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. Aktivieren Sie das Kontrollkästchen neben jeder Entität, deren Zuweisung von Einschränkungen Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Einschränkungszuweisungen für Kampagnen verwalten](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Einschränkungszuweisungen für Anzeigengruppen verwalten](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Verwalten von Einschränkungszuweisungen für Schlüsselwörter](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
>* [Einschränkungszuweisungen für Platzierungen verwalten](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)
>* [Die [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)
