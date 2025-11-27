---
title: Herunterladen/Erstellen einer Bulksheet-Datei
description: Erfahren Sie, wie Sie Bulksheet-Dateien erstellen, indem Sie Kontodaten für Ihre Werbenetzwerke herunterladen.
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Herunterladen/Erstellen einer Bulksheet-Datei

Sie können Bulksheets mit benutzerdefinierten Einstellungen für ein oder mehrere Konten in einem oder mehreren ([&#x200B; Werbenetzwerken) &#x200B;](bulksheet-about.md#bulksheet-functionality-by-network). Bulksheets enthalten Daten in Search, Social und Commerce.

Bei synchronisierten Kampagnen können Sie optional vor dem Herunterladen der Daten mit dem Werbenetzwerk synchronisieren, um sicherzustellen, dass aktuelle Datenänderungen auf der Werbenetzwerk-Seite enthalten sind. Für alle Werbenetzwerke können Sie optional neue Klick-Tracking-URLs generieren, die in die Datei aufgenommen werden sollen.

>[!NOTE]
>
>Sie können auch [eine Bulksheet-Datei basierend auf den sichtbaren Spalten in einer Kampagnen-Management-Ansicht erstellen](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Download Bulksheet]**.

1. Geben Sie die [Bulksheet-Einstellungen](#bulksheet-download-settings) an:

1. Geben Sie auf der Registerkarte **[!UICONTROL Selections]** Informationen in die Felder ein oder wählen Sie diese aus.

1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Rows and Columns]**, geben Sie die Kontokomponenten und Komponentenstatus an, für die Zeilen in das Bulksheet aufgenommen werden sollen, und geben Sie dann die Spalten an, die für jede ausgewählte Komponente eingeschlossen werden sollen.

   Eine Liste der verfügbaren Bulksheet-Zeilen finden Sie unter [Bulksheet-Zeilen nach Anzeigennetzwerk](#bulksheet-rows-by-ad-network).

1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Filters]** und geben Sie dann Kriterien für bestimmte Kampagnen, Anzeigengruppen, Anzeigen/Kreative, Schlüsselwörter, Platzierungen und andere Entitäten an, die in die Bulksheet aufgenommen werden sollen:

   1. Wählen Sie einen Parameter aus (Name oder ID der Entität oder ein beliebiges Element einer Anzeige, eines Keywords oder einer Platzierung), wählen Sie einen Operator aus und geben Sie dann den entsprechenden Wert ein. Wenn Sie beispielsweise nur Anzeigen mit „Schuhe“ in der Überschrift für ein [!DNL Google Ads] Konto zurückgeben möchten, wählen Sie *Überschrift* aus, wählen Sie *[!UICONTROL contains]* aus und geben Sie dann `shoes` in das Eingabefeld ein.

   1. (So wenden Sie zusätzliche Filter an) Klicken Sie für jeden zusätzlichen Filter auf **[!UICONTROL +Add Filter]**, wählen Sie **[!UICONTROL AND]** oder **[!UICONTROL OR]** aus, wählen Sie ein Werbeelement oder Keyword und einen Operator aus und geben Sie dann den entsprechenden Wert ein.

1. Klicken Sie auf **[!UICONTROL Download]**.

Zu Beginn der Aufgabe wird im Fenster eine Benachrichtigung angezeigt, das Fenster bleibt jedoch geöffnet, sodass Sie bei Bedarf weitere Bulksheets erstellen können. Alle angegebenen Filter und Ausschlüsse, die für alle ausgewählten neuen Konten gelten, werden beibehalten. Wenn die Aufgabe beginnt, wird die Datei in der Bulksheets-Ansicht aufgeführt. Wenn die Datei erstellt wird, erhalten Sie eine E-Mail-Benachrichtigung mit einem Link zur Datei. Je nach Menge der zu kompilierenden Daten kann die Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateigenerierung jedoch fehlschlägt, wird eine Fehlerdatei in der Bulksheets-Ansicht aufgelistet und Sie erhalten eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei.

## Einstellungen für den Bulksheet-Download {#bulksheet-download-settings}

| Tabulator | Parameter | Beschreibung |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | Die Konten, Kampagnen oder Anzeigengruppen, in die die Daten hochgeladen werden sollen:<ul><li>Um ein Konto und alle zugehörigen Kampagnen und Anzeigengruppen auszuwählen, aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken dann auf >>, um es in die Spalte [!UICONTROL Selected Filters] zu verschieben.</li><li>Um einzelne Kampagnen oder Anzeigengruppen auszuwählen, klicken Sie auf neben dem Konto, um es zu erweitern, klicken Sie (falls erforderlich) auf neben der Kampagne, um sie zu erweitern, aktivieren Sie das Kontrollkästchen neben dem Namen der Kampagne oder Anzeigengruppe und klicken Sie dann auf >>, um sie in die Spalte [!UICONTROL Selected Filters] zu verschieben. Wenn Sie beispielsweise Daten nur für Kampagne 1 in Konto 1 abrufen möchten, erweitern Sie Konto 1, aktivieren Sie das Kontrollkästchen neben Kampagne 1 und verschieben Sie es in die Spalte [!UICONTROL Selected Filters] .</li></ul><b>Hinweise:</b><ul><li>Eine einzige Bulksheet kann für mehrere Konten innerhalb mehrerer Werbenetzwerke gelten. Anzeigennetzwerkspezifische Spalten werden in Bulksheets mit dem Namen des Anzeigennetzwerks gekennzeichnet (z. B. „Mobilnetzbetreiber (Google-Anzeigen)„).</li><li>Um zu sehen, welcher Typ von Komponente ein Element ist, halten Sie den Cursor darüber.</li><li>Bei Kampagnen befindet sich der erste Buchstabe des Anzeigennetzwerknamens in Klammern hinter dem Kontonamen (z. B. „Acme Realty (G)“ für ein [!DNL Google Ads] Konto).</li><li>Standardmäßig werden nur aktive und aktivierte Konten sowie deren aktive Komponenten aufgelistet. Um pausierte und gelöschte Komponenten anzuzeigen, klicken Sie auf ![Nach-unten](/help/search-social-commerce/assets/arrow-down-expand.png "Pfeil") neben [!UICONTROL Show] und wählen Sie **[!UICONTROL All] aus. |
| | [!UICONTROL Generate Tracking URLs] | (Optional) Enthält Tracking-Vorlagen und Landingpage-Suffixe (für entsprechende Werbenetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Tracking-Codes in Konten mit Ziel-URLs für Schlüsselwörter, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen im Bulksheet. Standardmäßig ist diese Option aktiviert.<br><br>Wenn diese Option aktiviert ist, werden die URLs gemäß den Parametern im Abschnitt &quot;[!UICONTROL Campaign Tracking]&quot; der Konto- oder Kampagneneinstellungen generiert. Wenn Tracking-URLs bereits vorhanden sind, werden sie standardmäßig nicht neu generiert, es sei denn, neue werden benötigt (z. B. wenn der Schlüsselwortübereinstimmungstyp, der Anzeigentext oder die Tracking-Parameter des Kontos geändert wurden).<br><br><b>Hinweise:</b><ul><li>Wenn der Advertiser das Adobe Advertising-Konversionstracking verwendet und das entsprechende Konto nicht so konfiguriert ist, dass Tracking-URLs automatisch generiert und hochgeladen werden, müssen Sie neue Tracking-URLs generieren, wenn sich die Basis-URLs geändert haben.</li><li>Wenn Sie diese Option nicht auswählen, können Sie auch später Tracking-URLs generieren, wenn Sie die Datei hochladen oder veröffentlichen.</li></ul> |
| | [!UICONTROL Perform Pre-sync] | (Optional) Weist Search, Social und Commerce an, seine Dateien mit den angegebenen Kampagnen zu synchronisieren, um sicherzustellen, dass alle Daten identisch sind. Standardmäßig ist diese Option nicht ausgewählt.<br><b>Hinweis:</b> Search, Social und Commerce werden einmal täglich automatisch mit dem Anzeigennetzwerk synchronisiert, wenn eine neue Kampagne im Anzeigennetzwerk erkannt wird, und jedes Mal, wenn Sie Kampagnendaten in Search, Social und Commerce ändern. Wählen Sie diese Option aus, wenn Sie der Meinung sind, dass die letzten Änderungen an Kampagnen- oder Kontodaten direkt im Werbenetzwerk oder mithilfe des Desktop-Editors des Werbenetzwerks vorgenommen wurden. Die Erstellung von Bulksheets dauert bei Auswahl dieser Option länger. |
| | [!UICONTROL Bulksheet Name] | Der Name des neuen Bulksheets und der Dateityp. Standardmäßig wird die Datei im tabulatorgetrennten Werteformat erstellt und erhält einen der folgenden Namen:<ul><li>(für alle Konten für das Werbenetzwerk) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(für einzelne Konten) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(Für mehrere Konten) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>Sie können die Datei umbenennen. Der Name darf die folgenden Zeichen nicht enthalten: `# % & * \| \ : : < > . ? or /`.<br><br>Ändern Sie optional den Dateityp. Die Optionen umfassen *[!UICONTROL .tsv]* (für tabulatorgetrennte Werte), *[!UICONTROL .txt]* (für Unicode-kompatiblen ASCII-Text), *[!UICONTROL .csv]* (für kommagetrennte Werte) oder *[!UICONTROL .zip]* (für das komprimierte ZIP-Format, das in eine TSV-Datei entpackt wird).<br><br><b>Tipp:</b> Verwenden Sie für Bulksheets mit internationalen Zeichen das TSV- oder TXT-Format. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | Die Entitäten und ihre entsprechenden Status, die in das Bulksheet aufgenommen werden sollen, mit einer Datenzeile pro Eintrag. Wenn Sie beispielsweise aktive Kampagnen einbeziehen, enthält die Bulksheet eine Zeile pro aktiver Kampagne. Nur ausgewählte Entitäten mit den ausgewählten Status werden eingeschlossen. Die Standardwerte sind basierend auf dem angegebenen Werbenetzwerk vorausgewählt. Standardmäßig werden nur aktive Instanzen der ausgewählten Entitäten einbezogen. Eine Liste der verfügbaren Bulksheet-Zeilen finden Sie unter [Bulksheet-Zeilen nach Anzeigennetzwerk](#bulksheet-rows-by-ad-network).<br><br>Um Entitäten hinzuzufügen oder zu entfernen, aktivieren bzw. deaktivieren Sie die Kontrollkästchen neben den Entitäten. Um Status für eine Entität hinzuzufügen oder zu entfernen, klicken Sie auf neben dem Menü Status und aktivieren bzw. deaktivieren Sie die Kontrollkästchen neben den Entitäten. |
| | [!UICONTROL Cascading Status Hierarchy] | Filtert den Umfang untergeordneter Entitäten mithilfe eines AND-Vorgangs nach denen mit den angegebenen Status der übergeordneten Entität. Wenn Sie beispielsweise „Aktive Kampagne“, „Aktive Anzeigengruppe“ und „Aktive Schlüsselwörter“ auswählen, enthält die Bulksheet nur aktive Schlüsselwörter in aktiven Anzeigengruppen in aktiven Kampagnen.<br><br>Wenn Sie diese Option nicht auswählen, wird der übergeordnete Status nicht berücksichtigt und der Filter verwendet eine OR-Operation. Wenn Sie beispielsweise „Aktive Kampagne“, „Aktive Anzeigengruppe“ und „Aktive Schlüsselwörter“ auswählen, enthält die Bulksheet alle aktiven Kampagnen, alle aktiven Anzeigengruppen, unabhängig vom Status der übergeordneten Kampagne, und alle aktiven Schlüsselwörter, unabhängig vom Status der übergeordneten Kampagne und Anzeigengruppe. |
| | [!UICONTROL Bulksheet Columns] | Die Spalten, die in die heruntergeladene Bulksheet-Datei aufgenommen werden sollen:<ul><li>*[!UICONTROL AMO ID]*: (Erforderlich, wenn &quot;[!UICONTROL SE ID]&quot; nicht ausgewählt ist) Enthält eine [!DNL Adobe] generierte eindeutige Kennung für jede Entität/Zeile. Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden ihn jedoch nicht an das Werbenetzwerk. Später können Sie Daten für die Entität bearbeiten, indem Sie die [!UICONTROL AMO ID] als Kennung statt der Entitäts-ID und der übergeordneten Entitäts-IDs verwenden.</li><li>*[!UICONTROL SE ID]*: (Erforderlich, wenn &quot;[!UICONTROL AMO ID]&quot; nicht ausgewählt ist) Enthält die eindeutige Kennung des Anzeigennetzwerks für jede eingeschlossene Spalte und deren übergeordnete Entitäten. Wenn Sie zu einem späteren Zeitpunkt Daten für eine Entität bearbeiten, die die [!UICONTROL SE ID] als Kennung enthält, müssen Sie auch Zeilen für die übergeordneten Entitäten einbeziehen (einschließlich deren [!UICONTROL SE ID]).</li><li>*[!UICONTROL Platform]*: Enthält eine [!UICONTROL Platform column] am Anfang jeder Zeile, um die Anzeigenplattform anzugeben (z. B. „Baidu„).</li><li>*[!UICONTROL Acct Name]*: (Erforderlich, wenn &quot;[!UICONTROL AMO ID]&quot; nicht ausgewählt ist) Enthält den Namen des Anzeigen-Netzwerkkontos für jede Entität/Zeile.</li><li>\[Einzuschließende Spalten\]: Einbeziehung aller, keiner oder nur der ausgewählten Spalten, die für jede ausgewählte Entität im [!UICONTROL Bulksheet Rows] relevant sind. Um die für eine Entität relevanten Spalten anzuzeigen, klicken Sie auf ![Pfeil nach rechts](/help/search-social-commerce/assets/compressed-item.png "Pfeil nach rechts") neben dem Entitätsnamen. Standardmäßig sind alle relevanten Spalten für jede ausgewählte Entitätszeile enthalten. Deaktivieren Sie das Kontrollkästchen neben einem Element oder neben einer einzelnen Spalte, um es aus der Bulksheet auszuschließen.</li></ul><br><br><b>Tipp</b> Stellen Sie sicher, dass Sie geeignete Spalten angeben, um das Element in jeder Zeile der Bulksheet-Datei zu identifizieren. Angenommen, Sie schließen pro [!UICONTROL Bulksheet Rows]-Selektor Keyword-Zeilen ein, aber Sie schließen alle Keyword-bezogenen Spalten aus. Das resultierende Bulksheet enthält eine Zeile für jede Keyword-Instanz. Da jedoch keine schlüsselwortbezogenen Spalten enthalten sind - nicht einmal die AMO-ID oder SE-ID - können Sie nicht identifizieren, welche Schlüsselwortinstanz zu einer bestimmten Zeile gehört, und Sie können die Bulksheet nicht zur Aktualisierung der Daten verwenden, es sei denn, Sie fügen die entsprechende ID-Spalte und die entsprechenden Werte manuell hinzu. |
| [!UICONTROL Filters] | | Kriterien für bestimmte Kampagnen, Anzeigengruppen, Anzeigen/Kreative, Schlüsselwörter und/oder Platzierungen, die in die Bulksheet aufgenommen werden sollen:<ol><li>Wählen Sie einen Parameter aus (Name oder ID der Entität oder ein beliebiges Element einer Kreativ-, Keyword- oder Platzierung), wählen Sie einen Operator aus und geben Sie dann den entsprechenden Wert ein.<br>Wenn Sie beispielsweise nur Anzeigen mit „Schuhe“ in der Überschrift für ein [!DNL Google Ads]-Konto zurückgeben möchten, wählen Sie *[!UICONTROL Headline]* aus, wählen Sie *[!UICONTROL contains]* aus und geben Sie dann `shoes` in das Eingabefeld ein.</li><li>(So wenden Sie zusätzliche Filter an) Klicken Sie für jeden zusätzlichen Filter auf **[!UICONTROL +Add Filter]**, wählen Sie **[!UICONTROL AND]** oder **[!UICONTROL OR]** aus, wählen Sie ein Werbeelement oder Keyword und einen Operator aus und geben Sie dann den entsprechenden Wert ein.</li></ul> |

## Bulksheet-Zeilen nach Anzeigennetzwerk {#bulksheet-rows-by-ad-network}

| Bulksheet-Zeile | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Notizen |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Adgroup] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Creative] *ODER* [!UICONTROL Creative (except RSA)] | Ja | Ja | Ja | — | — | Ja | Ja | Ja | Ja | ([!DNL Google  Ads]) Wird für alle Anzeigentypen mit Ausnahme responsiver Suchanzeigen verwendet, die in der [!UICONTROL Responsive Search Ad] Zeile verfügbar sind. |
| [!UICONTROL Responsive Search Ad] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Ja | Ja | Ja | Ja | Ja | — | Ja | Ja | Ja | Verwenden Sie nur für nicht negative Keywords. Wenn Sie negative Keywords auf Kampagnen- oder Anzeigengruppenebene sehen möchten, verwenden Sie die Zeile [!UICONTROL Campaign Negative Keyword] oder [!UICONTROL Adgroup Negative Keyword] , sofern verfügbar. |
| [!UICONTROL Promoted Pin] | — | — | — | — | Ja | — | — | — | — | — |
| [!UICONTROL Placement] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Ja | Ja | — | — | — | — | — | — | Wird für dynamische Suchziele für eine Anzeigengruppe verwendet. |
| [!UICONTROL Shopping Product Group] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Negative Keyword] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | Verwenden Sie nur für negative Keywords, die auf Kampagnen- oder Anzeigengruppenebene erstellt wurden. Um nicht negative Keywords anzuzeigen, verwenden Sie die [!UICONTROL Keyword] Zeile, sofern verfügbar. |
| [!UICONTROL Campaign Negative Website] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Site Link] | — | Ja | — | — | — | — | — | Ja | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Ja | — |
| [!UICONTROL Adgroup Negative Keyword] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Device Target] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Device Target] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Ja | — | — | — | — | — | — | — | — |

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](bulksheet-about.md)
>* [Buchen Sie Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
>* [Validieren von Landingpages in Bulksheet-Dateien](bulksheet-validate-landing-pages.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
