---
title: Bulksheet-Datei herunterladen/erstellen
description: Erfahren Sie, wie Sie Bulksheet-Dateien erstellen, indem Sie Kontodaten für Ihre Werbenetzwerke herunterladen.
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Bulksheet-Datei herunterladen/erstellen

Sie können Bulksheets mit benutzerdefinierten Einstellungen für ein oder mehrere Konten in einem oder mehreren [unterstützten Anzeigennetzwerken](bulksheet-about.md#bulksheet-functionality-by-network) erstellen. Bulksheets enthalten Daten in Search, Social und Commerce.

Bei synchronisierten Kampagnen können Sie optional mit dem Werbenetzwerk synchronisieren, bevor Sie die Daten herunterladen, um sicherzustellen, dass die letzten Datenänderungen auf der Werbenetzwerksseite eingeschlossen sind. Für alle Werbenetzwerke können Sie optional neue Klick-Tracking-URLs generieren, die in die Datei aufgenommen werden sollen.

>[!NOTE]
>
>Sie können auch [eine Bulksheet-Datei erstellen, die auf den sichtbaren Spalten in einer Kampagnenverwaltungsansicht](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md) basiert.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Download Bulksheet]**.

1. Geben Sie die [Bulksheet-Einstellungen](#bulksheet-download-settings) an:

1. Geben Sie auf der Registerkarte **[!UICONTROL Selections]** Informationen in die Felder ein oder wählen Sie sie aus.

1. (Optional) Klicken Sie auf die Registerkarte &quot;**[!UICONTROL Rows and Columns]**&quot;, geben Sie die Kontokomponenten und Komponentenstatus an, für die im Bulksheet Zeilen eingefügt werden sollen, und geben Sie dann die Spalten an, die für jede ausgewählte Komponente einbezogen werden sollen.

   Eine Liste der verfügbaren Bulksheet-Zeilen finden Sie unter &quot;[Bulksheet-Zeilen nach Anzeigennetzwerk](#bulksheet-rows-by-ad-network)&quot;.

1. (Optional) Klicken Sie auf die Registerkarte &quot;**[!UICONTROL Filters]**&quot;und geben Sie dann Kriterien für bestimmte Kampagnen, Anzeigengruppen, Anzeigen/Kreativinhalte, Suchbegriffe, Platzierungen und andere Entitäten an, die in das Bulksheet aufgenommen werden sollen:

   1. Wählen Sie einen Parameter (Entitätsname oder ID oder ein Element einer Anzeige, eines Suchbegriffs oder einer Platzierung), wählen Sie einen Operator und geben Sie dann den entsprechenden Wert ein. Um beispielsweise nur Anzeigen mit &quot;Schuhe&quot;in der Überschrift für ein [!DNL Google Ads]-Konto zurückzugeben, wählen Sie *Überschrift*, wählen Sie *[!UICONTROL contains]* und geben Sie dann im Eingabefeld `shoes` ein.

   1. (Um weitere Filter anzuwenden) Klicken Sie für jeden zusätzlichen Filter auf &quot;**[!UICONTROL +Add Filter]**&quot;, wählen Sie &quot;**[!UICONTROL AND]**&quot; oder &quot;**[!UICONTROL OR]**&quot;, wählen Sie ein Anzeigenelement oder einen Suchbegriff und einen Operator aus und geben Sie dann den entsprechenden Wert ein.

1. Klicken Sie auf **[!UICONTROL Download]**.

Wenn die Aufgabe beginnt, wird im Fenster eine Benachrichtigung angezeigt, sie bleibt jedoch geöffnet, sodass Sie bei Bedarf weitere Bulksheets erstellen können. Alle angegebenen Filter und Ausschlüsse, die auf neue, von Ihnen ausgewählte Konten angewendet werden, werden beibehalten. Wenn die Aufgabe beginnt, wird die Datei in der Bulksheets-Ansicht aufgeführt. Bei der Erstellung der Datei erhalten Sie eine E-Mail-Benachrichtigung mit einem Link zur Datei. Je nach Menge der zu erstellenden Daten kann die Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateierstellung jedoch fehlschlägt, wird in der Bulksheets-Ansicht eine Fehlerdatei aufgelistet und Sie erhalten eine E-Mail-Benachrichtigung mit einer Verknüpfung zur Fehlerdatei.

## Massenblatt-Download-Einstellungen {#bulksheet-download-settings}

| Registerkarte | Parameter | Beschreibung |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | Die Konten, Kampagnen oder Anzeigengruppen, in die die Daten hochgeladen werden sollen:<ul><li>Um ein Konto sowie alle Kampagnen und Anzeigengruppen auszuwählen, aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie auf >>, um es in die Spalte [!UICONTROL Selected Filters] zu verschieben.</li><li>Um einzelne Kampagnen oder Anzeigengruppen auszuwählen, klicken Sie auf das Symbol neben dem Konto, um es zu erweitern. Klicken Sie (bei Bedarf) auf das Symbol neben der Kampagne, um sie zu erweitern. Aktivieren Sie das Kontrollkästchen neben dem Namen der Kampagne oder Anzeigengruppe und klicken Sie auf >>, um sie in die Spalte [!UICONTROL Selected Filters] zu verschieben. Um beispielsweise nur Daten für Kampagne 1 in Konto 1 abzurufen, erweitern Sie Konto 1, aktivieren Sie das Kontrollkästchen neben Kampagne 1 und verschieben Sie es in die Spalte [!UICONTROL Selected Filters] .</li></ul><b>Notizen:</b><ul><li>Ein einzelnes Bulksheet kann für mehrere Konten in mehreren Werbenetzwerken gelten. Netzwerkspezifische Anzeigenspalten werden in Bulksheets mit dem Anzeigennetzwerknamen (z. B. &quot;Mobilnetzbetreiber (Google Ads)&quot;) beschriftet.</li><li>Um zu sehen, welcher Komponententyp ein Element ist, halten Sie den Cursor darüber.</li><li>Bei Kampagnen ist der erste Buchstabe des Anzeigennetzwerknamens in Klammern hinter dem Kontonamen (z. B. &quot;Acme Realty (G)&quot;für ein [!DNL Google Ads] -Konto).</li><li>Standardmäßig werden nur aktive und aktivierte Konten und ihre aktiven Komponenten aufgelistet. Um angehaltene und gelöschte Komponenten anzuzeigen, klicken Sie neben [!UICONTROL Show] auf den Pfeil nach unten ](/help/search-social-commerce/assets/arrow-down-expand.png "Nach-unten-Pfeil") und wählen Sie **[!UICONTROL All] aus.![ |
| | [!UICONTROL Generate Tracking URLs] | (Optional) Enthält Tracking-Vorlagen und Suffixe für Landingpages (für anwendbare Anzeigennetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Trackingcodes in Konten mit Ziel-URLs, für Suchbegriffe, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen im Bulksheet. Standardmäßig ist diese Option aktiviert.<br><br>Wenn diese Option ausgewählt ist, werden die URLs gemäß den Parametern im Abschnitt [!UICONTROL Campaign Tracking] der Kontoeinstellungen oder Kampagneneinstellungen generiert. Standardmäßig werden Tracking-URLs nur dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Keyword-Übereinstimmungstyp, der Anzeigentext oder die Tracking-Parameter des Kontos geändert haben).<br><br><b>Notizen:</b><ul><li>Wenn der Advertiser das Adobe Advertising-Konversions-Tracking verwendet und das entsprechende Konto nicht für die automatische Generierung und das Hochladen von Tracking-URLs konfiguriert ist, müssen Sie neue Tracking-URLs generieren, wenn sich die Basis-URLs geändert haben.</li><li>Wenn Sie diese Option nicht auswählen, können Sie auch später beim Hochladen oder Posten der Datei Tracking-URLs generieren.</li></ul> |
| | [!UICONTROL Perform Pre-sync] | (Optional) Weist Search, Social und Commerce an, seine Dateien mit den angegebenen Kampagnen zu synchronisieren, um sicherzustellen, dass alle Daten identisch sind. Standardmäßig ist diese Option nicht aktiviert.<br><b>Hinweis:</b> Die Suche, Social und Commerce synchronisiert sich täglich automatisch mit dem Werbenetzwerk, sobald eine neue Kampagne im Werbenetzwerk erkannt wird und Sie jedes Mal Kampagnendaten aus Search, Social und Commerce ändern. Wählen Sie diese Option aus, wenn Sie der Meinung sind, dass kürzlich erfolgte Änderungen an Kampagnen- oder Kontodaten direkt im Werbenetzwerk oder im Desktop-Editor des Werbenetzwerks vorgenommen wurden. Die Erstellung von Massenblättern dauert bei Auswahl dieser Option länger. |
| | [!UICONTROL Bulksheet Name] | Name des neuen Bulksheets und Dateityp. Standardmäßig wird die Datei im tabulatorgetrennten Wertformat erstellt und erhält den Namen einer der folgenden Optionen:<ul><li>(für alle Konten im Werbenetzwerk) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(für einzelne Konten) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(für mehrere Konten) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>Sie können die Datei umbenennen. Der Name darf die folgenden Zeichen nicht enthalten: `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>Ändern Sie optional den Dateityp. Zu den Optionen gehören &quot;*[!UICONTROL .tsv]*&quot;(für tabulatorgetrennte Werte), &quot;*[!UICONTROL .txt]*&quot;(für Unicode-kompatiblen ASCII-Text), &quot;*[!UICONTROL .csv]*&quot;(für kommagetrennte Werte) oder &quot;*[!UICONTROL .zip]*&quot;(für komprimiertes ZIP-Format, das die ZIP-Datei entpackt).<br><br><b>Tipp:</b> Verwenden Sie für Bulksheets mit internationalen Zeichen das Format TSV oder TXT. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | Die Entitäten und ihre entsprechenden Status, die in das Bulksheet mit einer Datenzeile pro Eintrag aufgenommen werden sollen. Wenn Sie beispielsweise aktive Kampagnen einbeziehen, enthält das Bulksheet pro aktiver Kampagne eine Zeile. Es werden nur ausgewählte Entitäten mit dem ausgewählten Status einbezogen. Die Standardeinstellungen werden basierend auf dem angegebenen Werbenetzwerk vorausgewählt. Standardmäßig werden nur aktive Instanzen der ausgewählten Entitäten eingeschlossen. Eine Liste der verfügbaren Bulksheet-Zeilen finden Sie unter &quot;[Bulksheet-Zeilen nach Anzeigennetzwerk](#bulksheet-rows-by-ad-network)&quot;.<br><br>Um Entitäten hinzuzufügen oder zu entfernen, aktivieren bzw. deaktivieren Sie die Kontrollkästchen neben den Entitäten. Um Status für eine Entität hinzuzufügen oder zu entfernen, klicken Sie neben dem Statusmenü auf und aktivieren bzw. deaktivieren Sie die Kontrollkästchen neben den Entitäten. |
| | [!UICONTROL Cascading Status Hierarchy] | Filtert mithilfe eines AND-Vorgangs den Umfang der untergeordneten Entitäten auf diejenigen mit dem angegebenen Status der übergeordneten Entität. Wenn Sie beispielsweise &quot;Aktive Kampagne&quot;, &quot;Aktive Anzeigengruppe&quot;und &quot;Aktiver Suchbegriff&quot;auswählen, enthält das Bulksheet in aktiven Kampagnen nur aktive Suchbegriffe in aktiven Anzeigengruppen.<br><br>Wenn Sie diese Option nicht auswählen, wird der übergeordnete Status nicht berücksichtigt und der Filter verwendet einen ODER-Vorgang. Wenn Sie beispielsweise &quot;Aktive Kampagne&quot;, &quot;Aktive Anzeigengruppe&quot;und &quot;Aktiver Suchbegriff&quot;auswählen, enthält das Bulksheet alle aktiven Kampagnen, alle aktiven Anzeigengruppen unabhängig vom Status der übergeordneten Kampagne sowie alle aktiven Suchbegriffe, unabhängig vom Status der übergeordneten Kampagne und Anzeigengruppe. |
| | [!UICONTROL Bulksheet Columns] | Die Spalten, die in die heruntergeladene Bulksheet-Datei aufgenommen werden sollen:<ul><li>*[!UICONTROL AMO ID]*: (Erforderlich, wenn &quot;[!UICONTROL SE ID]&quot; nicht ausgewählt ist) Umfasst eine [!DNL Adobe]-generierte eindeutige Kennung für jede Entität/Zeile. Search, Social und Commerce verwenden den Wert, um die richtige Identität zu ermitteln, die bearbeitet werden soll, aber nicht im Werbenetzwerk veröffentlicht wird. Später können Sie Daten für die Entität mit dem Wert &quot;[!UICONTROL AMO ID]&quot;als Kennung und nicht mit der Entitäts-ID und den IDs der übergeordneten Entität bearbeiten.</li><li>*[!UICONTROL SE ID]*: (Erforderlich, wenn &quot;[!UICONTROL AMO ID]&quot; nicht ausgewählt ist) Umfasst die eindeutige Kennung des Anzeigennetzwerks für jede enthaltene Spalte und deren übergeordnete Entitäten. Wenn Sie später Daten für eine Entität bearbeiten, die &quot;[!UICONTROL SE ID]&quot;als Kennung verwendet, müssen Sie auch Zeilen für die übergeordneten Entitäten einschließen (einschließlich ihrer [!UICONTROL SE ID] -Werte).</li><li>*[!UICONTROL Platform]*: Enthält eine [!UICONTROL Platform column] am Anfang jeder Zeile, um die Anzeigenplattform anzugeben (z. B. &quot;Baidu&quot;).</li><li>*[!UICONTROL Acct Name]*: (Erforderlich, wenn &quot;[!UICONTROL AMO ID]&quot; nicht ausgewählt ist) Umfasst den Namen des Anzeigennetzwerkkontos für jede Entität/Zeile.</li><li>\[Spalten, die einbezogen werden sollen\]: Um alle, keine oder nur ausgewählte Spalten einzubeziehen, die für jede ausgewählte Entität im Abschnitt [!UICONTROL Bulksheet Rows] relevant sind. Um die einzelnen Spalten anzuzeigen, die für eine Entität relevant sind, klicken Sie neben dem Entitätsnamen auf den Pfeil nach rechts ](/help/search-social-commerce/assets/compressed-item.png "Pfeil nach rechts"). ![ Standardmäßig sind alle relevanten Spalten für jede ausgewählte Entitätszeile eingeschlossen. Deaktivieren Sie das Kontrollkästchen neben einer Entität oder neben einer einzelnen Spalte, um sie aus dem Bulksheet auszuschließen.</li></ul><br><br><b>Tipp:</b> Stellen Sie sicher, dass Sie ausreichende Spalten zur Identifizierung des Elements in jeder Zeile der Bulksheet-Datei einschließen. Angenommen, Sie nehmen Suchbegriffzeilen pro &quot;[!UICONTROL Bulksheet Rows]&quot;-Auswahl ein, aber Sie schließen alle suchbegriffbezogenen Spalten aus. Das resultierende Bulksheet enthält eine Zeile für jede Suchbegriffinstanz. Da jedoch keine suchbegriffbezogenen Spalten enthalten sind - nicht einmal die AMO-ID oder die SE-ID - können Sie nicht ermitteln, welche Suchbegriffsinstanz sich auf eine bestimmte Zeile bezieht, und Sie können das Bulksheet nicht verwenden, um Daten zu aktualisieren, es sei denn, Sie fügen manuell die entsprechende ID-Spalte und -Werte hinzu. |
| [!UICONTROL Filters] | | Kriterien für bestimmte Kampagnen, Anzeigengruppen, Anzeigen/Kreative, Suchbegriffe und/oder Platzierungen, die in das Bulksheet aufgenommen werden sollen:<ol><li>Wählen Sie einen Parameter aus (Entitätsname oder ID oder ein Element eines Kreativ-, Keyword- oder Platzierungselements), wählen Sie einen Operator und geben Sie dann den entsprechenden Wert ein.<br>Um beispielsweise nur Anzeigen mit &quot;Schuhe&quot;in der Überschrift für ein [!DNL Google Ads] -Konto zurückzugeben, wählen Sie *[!UICONTROL Headline]*, wählen Sie *[!UICONTROL contains]* und geben Sie dann im Eingabefeld `shoes` ein.</li><li>(Um weitere Filter anzuwenden) Klicken Sie für jeden zusätzlichen Filter auf &quot;**[!UICONTROL +Add Filter]**&quot;, wählen Sie &quot;**[!UICONTROL AND]**&quot; oder &quot;**[!UICONTROL OR]**&quot;, wählen Sie ein Anzeigenelement oder einen Suchbegriff und einen Operator aus und geben Sie dann den entsprechenden Wert ein.</li></ul> |

## Massenblatt-Zeilen nach Anzeigennetzwerk {#bulksheet-rows-by-ad-network}

| Massenblatt-Zeile | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Hinweise |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Adgroup] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Creative] *oder* [!UICONTROL Creative (except RSA)] | Ja | Ja | Ja | — | — | Ja | Ja | Ja | Ja | ([!DNL Google  Ads]) Verwenden Sie für alle Anzeigentypen außer für responsive Suchanzeigen, die in der Zeile [!UICONTROL Responsive Search Ad] verfügbar sind. |
| [!UICONTROL Responsive Search Ad] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Ja | Ja | Ja | Ja | Ja | — | Ja | Ja | Ja | Nur für nicht-negative Suchbegriffe. Um negative Suchbegriffe anzuzeigen, die auf Kampagnen- oder Anzeigengruppenebene erstellt wurden, verwenden Sie die Zeile [!UICONTROL Campaign Negative Keyword] oder [!UICONTROL Adgroup Negative Keyword] , sofern verfügbar. |
| [!UICONTROL Promoted Pin] | — | — | — | — | Ja | — | — | — | — | — |
| [!UICONTROL Placement] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Ja | Ja | — | — | — | — | — | — | Verwenden Sie für dynamische Suchziele für eine Anzeigengruppe. |
| [!UICONTROL Shopping Product Group] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Negative Keyword] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | Verwenden Sie dies nur für negative Suchbegriffe, die auf Kampagnen- oder Anzeigengruppenebene erstellt wurden. Um nicht-negative Suchbegriffe anzuzeigen, verwenden Sie die Zeile [!UICONTROL Keyword] , sofern verfügbar. |
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
>* [Post-Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
>* [Validieren von Landingpages in Bulksheet-Dateien](bulksheet-validate-landing-pages.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
