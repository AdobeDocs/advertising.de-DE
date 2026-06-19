---
title: (Neue Benutzeroberfläche) Herunterladen/Erstellen einer Bulksheet-Datei
description: Erfahren Sie, wie Sie Bulksheet-Dateien erstellen, indem Sie Account-Daten für Ihre Werbenetzwerke in die neue Benutzeroberfläche für Search, Social und Commerce herunterladen.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 1637
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Herunterladen/Erstellen einer Bulksheet-Datei

Sie können Bulksheets mit benutzerdefinierten Einstellungen für ein oder mehrere Konten in einem oder mehreren ([&#x200B; Werbenetzwerken) &#x200B;](about.md#bulksheet-functionality-by-network). Bulksheets enthalten Daten in Search, Social und Commerce.

Bei synchronisierten Kampagnen können Sie optional vor dem Herunterladen der Daten mit dem Werbenetzwerk synchronisieren, um sicherzustellen, dass aktuelle Datenänderungen auf der Werbenetzwerk-Seite enthalten sind. Für alle Werbenetzwerke können Sie optional neue Klick-Tracking-URLs generieren, die in die Datei aufgenommen werden sollen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Download Bulksheet]**.

1. Geben Sie die [Bulksheet-Einstellungen](#bulksheet-settings) an:

   1. Wählen Sie auf der Registerkarte **[!UICONTROL Selections]** die Konten, Kampagnen oder Anzeigengruppen aus, um die Bulksheet-Optionen einzubeziehen und zu konfigurieren.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Rows and Columns]**, geben Sie die Kontokomponenten und Komponentenstatus an, für die Zeilen in das Bulksheet aufgenommen werden sollen, und geben Sie dann die Spalten an, die für jede ausgewählte Komponente eingeschlossen werden sollen.

      Eine Liste der verfügbaren Bulksheet-Zeilen finden Sie unter [Bulksheet-Zeilen nach Anzeigennetzwerk](#bulksheet-rows-by-ad-network).

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Filters]** und geben Sie dann Kriterien für die spezifischen Kampagnen, Anzeigengruppen, Anzeigen/Kreative, Schlüsselwörter, Platzierungen und andere Entitäten an, die in die Bulksheet aufgenommen werden sollen.

1. Klicken Sie auf **[!UICONTROL Download]**.

Zu Beginn der Aufgabe wird im Fenster eine Benachrichtigung angezeigt, das Fenster bleibt jedoch geöffnet, sodass Sie bei Bedarf weitere Bulksheets erstellen können. Wenn die Datei erstellt wird, erhalten Sie eine E-Mail-Benachrichtigung mit einem Link zur Datei. Je nach Menge der zu kompilierenden Daten kann die Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateigenerierung fehlschlägt, wird eine Fehlerdatei in der Bulksheets-Ansicht aufgeführt und Sie erhalten eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei.

## Bulksheet-Einstellungen {#bulksheet-settings}

### Registerkarte „Auswahlen“ {#bulksheet-selections-settings}

**\[Auswahl von Konto, Kampagne und Anzeigengruppe\]**

Erweitern Sie die Netzwerk- und Kontenhierarchie und aktivieren Sie dann das Kontrollkästchen neben jedem Konto, jeder Kampagne oder jeder Anzeigengruppe, dessen Daten in die Bulksheet aufgenommen werden sollen:

* Um alle Kampagnen und Anzeigengruppen für ein Konto einzubeziehen, aktivieren Sie das Kontrollkästchen neben dem Kontonamen.

* Um bestimmte Kampagnen einzubeziehen, erweitern Sie das -Konto und aktivieren Sie dann das Kontrollkästchen neben jeder einzuschließenden Kampagne. Um bestimmte Anzeigengruppen einzubeziehen, erweitern Sie eine Kampagne weiter und aktivieren Sie das Kontrollkästchen neben jeder Anzeigengruppe.

>[!NOTE]
>
>* Eine einzelne Bulksheet kann auf mehrere Konten innerhalb mehrerer Werbenetzwerke angewendet werden. Anzeigennetzwerkspezifische Spalten werden in Bulksheets mit dem Namen des Anzeigennetzwerks gekennzeichnet (z. B. „Mobilnetzbetreiber (Google-Anzeigen)„).
>* Um den Typ der Komponente anzuzeigen, die ein Element ist, halten Sie den Cursor darüber.
>* Standardmäßig werden nur aktive und aktivierte Konten sowie deren aktive Komponenten aufgelistet.

**[!UICONTROL Generate Tracking URLs]:** (Optional) Enthält Tracking-Vorlagen und Landingpage-Suffixe (für entsprechende Werbenetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Tracking-Codes in Konten mit Ziel-URLs für Schlüsselwörter, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen im Bulksheet. Standardmäßig ist diese Option aktiviert.

Wenn diese Option ausgewählt ist, werden die URLs gemäß den Parametern im Abschnitt &quot;[!UICONTROL Campaign Tracking]&quot; der Konto- oder Kampagneneinstellungen generiert. Wenn Tracking-URLs bereits vorhanden sind, werden sie standardmäßig nicht neu generiert, es sei denn, neue werden benötigt (z. B. wenn der Schlüsselwortübereinstimmungstyp, der Anzeigentext oder die Tracking-Parameter des Kontos geändert wurden).

>[!NOTE]
>
>* Wenn der Advertiser das Adobe Advertising-Konversionstracking verwendet und das entsprechende Konto nicht so konfiguriert ist, dass Tracking-URLs automatisch generiert und hochgeladen werden, müssen Sie neue Tracking-URLs generieren, wenn sich die Basis-URLs geändert haben.
>* Wenn Sie diese Option nicht auswählen, können Sie auch später Tracking-URLs generieren, wenn Sie die Datei hochladen oder veröffentlichen.

**[!UICONTROL Perform pre-sync]:** (Optional) Weist Search, Social und Commerce an, seine Dateien mit den angegebenen Kampagnen zu synchronisieren, um sicherzustellen, dass alle Daten identisch sind. Standardmäßig ist diese Option nicht ausgewählt.

>[!NOTE]
>
>Search, Social und Commerce werden einmal täglich automatisch mit dem Anzeigennetzwerk synchronisiert, sobald eine neue Kampagne im Anzeigennetzwerk erkannt wird, und jedes Mal, wenn Sie Kampagnendaten in Search, Social und Commerce ändern. Wählen Sie diese Option aus, wenn Sie der Meinung sind, dass die letzten Änderungen an Kampagnen- oder Kontodaten direkt im Werbenetzwerk oder mithilfe des Desktop-Editors des Werbenetzwerks vorgenommen wurden. Die Erstellung von Bulksheets dauert bei Auswahl dieser Option länger.

**[!UICONTROL Bulksheet Name]:** Der Name des neuen Bulksheets und der Dateityp. Standardmäßig wird die Datei im tabulatorgetrennten Werteformat erstellt und erhält einen der folgenden Namen:

* (Für alle Konten für ein Werbenetzwerk) `<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (Für ein einzelnes Konto) `<account name>_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (Für mehrere Konten) `MultipleAccounts_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`

Sie können die Datei umbenennen. Der Name darf die folgenden Zeichen nicht enthalten: `# % & * | \ : " < > . ? /`

Ändern Sie optional den Dateityp. Die Optionen umfassen *[!UICONTROL .tsv]* (für tabulatorgetrennte Werte), *[!UICONTROL .txt (unicode)]* (für Unicode-kompatiblen ASCII-Text), *[!UICONTROL .csv]* (für kommagetrennte Werte) oder *[!UICONTROL .zip]* (für das komprimierte ZIP-Format, das in eine TSV-Datei entpackt wird).

>[!TIP]
>
>Verwenden Sie für Bulksheets mit internationalen Zeichen das TSV- oder TXT-Format.

### Registerkarte Zeilen und Spalten {#bulksheet-rows-columns-settings}

**[!UICONTROL Bulksheet Rows]:** Die Entitäten und ihre entsprechenden Status, die als Datenzeilen in das Bulksheet aufgenommen werden sollen, mit einer Zeile pro Eintrag. Wenn Sie beispielsweise aktive Kampagnen einbeziehen, enthält die Bulksheet eine Zeile pro aktiver Kampagne. Nur ausgewählte Entitäten mit den ausgewählten Status werden eingeschlossen. Die Standardwerte sind basierend auf dem angegebenen Werbenetzwerk vorausgewählt. Standardmäßig werden nur aktive Instanzen der ausgewählten Entitäten einbezogen.

Um Entitäten hinzuzufügen oder zu entfernen, aktivieren oder deaktivieren Sie die Kontrollkästchen neben den Entitäten. Um Status für eine Entität hinzuzufügen oder zu entfernen, klicken Sie auf das Statusmenü neben der Entität und aktivieren oder deaktivieren Sie die Kontrollkästchen für die entsprechenden Status.

Eine Liste der verfügbaren Zeilen nach Anzeigennetzwerk finden Sie unter [Bulksheet rows by ad network](#bulksheet-rows-by-ad-network).

**[!UICONTROL Cascading Status Hierarchy]:** Filtert untergeordnete Entitäten mithilfe eines AND-Vorgangs nach denen mit dem angegebenen Status der übergeordneten Entität. Wenn Sie beispielsweise „Aktive Kampagne“, „Aktive Anzeigengruppe“ und „Aktive Schlüsselwörter“ auswählen, enthält die Bulksheet nur aktive Schlüsselwörter in aktiven Anzeigengruppen in aktiven Kampagnen.

Wenn Sie diese Option nicht auswählen, wird der übergeordnete Status nicht berücksichtigt und der Filter verwendet eine OR-Operation. Wenn Sie beispielsweise „Aktive Kampagne“, „Aktive Anzeigengruppe“ und „Aktive Schlüsselwörter“ auswählen, enthält die Bulksheet alle aktiven Kampagnen, alle aktiven Anzeigengruppen unabhängig vom Status der übergeordneten Kampagne und alle aktiven Schlüsselwörter unabhängig vom Status der übergeordneten Kampagne und Anzeigengruppe.

**[!UICONTROL Bulksheet Columns]:** Die Spalten, die in die heruntergeladene Bulksheet-Datei aufgenommen werden sollen:

* *[!UICONTROL AMO ID]:* (Erforderlich, wenn &quot;[!UICONTROL SE ID]&quot; nicht ausgewählt ist) Enthält eine [!DNL Adobe] generierte eindeutige Kennung für jede Entität/Zeile. Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden ihn jedoch nicht an das Werbenetzwerk. Später können Sie Daten für die Entität bearbeiten, indem Sie die [!UICONTROL AMO ID] als Kennung statt der Entitäts-ID und der übergeordneten Entitäts-IDs verwenden.

* *[!UICONTROL SE ID]:* (Erforderlich, wenn &quot;[!UICONTROL AMO ID]&quot; nicht ausgewählt ist) Enthält die eindeutige Kennung des Anzeigennetzwerks für jede eingeschlossene Spalte und deren übergeordnete Entitäten. Wenn Sie zu einem späteren Zeitpunkt Daten für eine Entität bearbeiten, die die [!UICONTROL SE ID] als Kennung enthält, müssen Sie auch Zeilen für die übergeordneten Entitäten einbeziehen (einschließlich deren [!UICONTROL SE ID]).

* *[!UICONTROL Platform]:* Enthält eine [!UICONTROL Platform] Spalte am Anfang jeder Zeile, um die Anzeigenplattform anzugeben (z. B. „Baidu„).

* *[!UICONTROL Acct Name]:* (Erforderlich, wenn &quot;[!UICONTROL AMO ID]&quot; nicht ausgewählt ist) Enthält den Namen des Anzeigen-Netzwerkkontos für jede Entität/Zeile.

* \[Entitätsspezifische Spalten\]: Um alle, keine oder nur ausgewählte Spalten einzubeziehen, die für jedes in [!UICONTROL Bulksheet Rows] ausgewählte Element relevant sind, klicken Sie auf ![Pfeil nach rechts](/help/search-social-commerce/assets/compressed-item.png "Pfeilspitze") neben dem Entitätsnamen, um es zu erweitern, und aktivieren oder deaktivieren Sie dann die Kontrollkästchen für einzelne Spalten. Standardmäßig sind alle relevanten Spalten für jede ausgewählte Entitätszeile enthalten.

>[!TIP]
>
>Stellen Sie sicher, dass Sie ausreichende Spalten zur Identifizierung des Elements in jeder Zeile der Bulksheet-Datei einbeziehen. Wenn Sie beispielsweise Schlüsselwortzeilen pro [!UICONTROL Bulksheet Rows]-Selektor einbeziehen, aber alle schlüsselwortbezogenen Spalten ausschließen, enthält das resultierende Bulksheet eine Zeile für jede Schlüsselwortinstanz, ohne dass festgestellt werden kann, welche Schlüsselwortinstanz zu einer bestimmten Zeile gehört. In diesem Fall können Sie die Bulksheet nur verwenden, um Daten zu aktualisieren, wenn Sie die entsprechende ID-Spalte und die entsprechenden Werte manuell hinzufügen.

### Registerkarte „Filter“ {#bulksheet-filters-settings}

Kriterien für bestimmte Kampagnen, Anzeigengruppen, Anzeigen/Kreative, Schlüsselwörter und/oder Platzierungen, die in die Bulksheet aufgenommen werden sollen:

1. Wählen Sie einen Parameter aus (Name oder ID der Entität oder ein beliebiges Element einer Kreativ-, Keyword- oder Platzierung), wählen Sie einen Operator aus und geben Sie dann den entsprechenden Wert ein.

   Wenn Sie beispielsweise nur Anzeigen mit „Schuhe“ in der Überschrift für ein [!DNL Google Ads] Konto zurückgeben möchten, wählen Sie *[!UICONTROL Headline]* aus, wählen Sie *[!UICONTROL contains]* aus und geben Sie dann `shoes` in das Eingabefeld ein.

1. (So wenden Sie zusätzliche Filter an) Klicken Sie für jeden zusätzlichen Filter auf **[!UICONTROL +Add Filter]**, wählen Sie **[!UICONTROL AND]** oder **[!UICONTROL OR]** aus, wählen Sie ein Werbeelement oder Keyword und einen Operator aus und geben Sie dann den entsprechenden Wert ein.

## Bulksheet-Zeilen nach Anzeigennetzwerk {#bulksheet-rows-by-ad-network}

| Bulksheet-Zeile | [!DNL Baidu] | [!DNL Google Ads] | [!DNL LY Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo DSP] | [!DNL Yahoo Native] | [!DNL Yandex] | Notizen |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Adgroup] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Creative] *ODER* [!UICONTROL Creative (except RSA)] | Ja | Ja | Ja | Ja | — | — | Ja | Ja | Ja | ([!DNL Google Ads]) Für alle Anzeigentypen außer responsiven Suchanzeigen verwenden, die in der [!UICONTROL Responsive Search Ad] Zeile verfügbar sind. |
| [!UICONTROL Responsive Search Ad] | — | Ja | — | Ja | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Ja | Ja | Ja | Ja | Ja | Ja | — | Ja | Ja | Verwenden Sie nur für nicht negative Keywords. Wenn Sie negative Keywords auf Kampagnen- oder Anzeigengruppenebene sehen möchten, verwenden Sie die Zeile [!UICONTROL Campaign Negative Keyword] oder [!UICONTROL Adgroup Negative Keyword] , sofern verfügbar. |
| [!UICONTROL Promoted Pin] | — | — | — | — | — | Ja | — | — | — | — |
| [!UICONTROL Placement] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Ja | — | Ja | — | — | — | — | — | Wird für dynamische Suchziele für eine Anzeigengruppe verwendet. |
| [!UICONTROL Shopping Product Group] | — | Ja | — | Ja | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Ja | — | Ja | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Negative Keyword] | Ja | Ja | Ja | Ja | — | — | — | Ja | — | Verwenden Sie nur für negative Keywords, die auf Kampagnen- oder Anzeigengruppenebene erstellt wurden. Um nicht negative Keywords anzuzeigen, verwenden Sie die [!UICONTROL Keyword] Zeile, sofern verfügbar. |
| [!UICONTROL Campaign Negative Website] | — | Ja | — | Ja | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Site Link] | — | Ja | — | — | — | — | — | Ja | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Ja | — |
| [!UICONTROL Adgroup Negative Keyword] | Ja | Ja | Ja | Ja | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Ja | — | Ja | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Ja | Ja | Ja | Ja | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | — | Ja | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Device Target] | — | Ja | — | Ja | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Device Target] | — | Ja | — | Ja | — | — | — | Ja | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Ja | — | Ja | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Ja | — | Ja | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Ja | — | — | — | — | — | — | — | — |

Einzelheiten zu den erforderlichen und optionalen Spalten für jedes Anzeigennetzwerk finden Sie in den Artikeln zum Anzeigennetzwerk-spezifischen Bulksheet-Datenformat:

* [Erforderliche und optionale Bulksheet-Daten für  [!DNL Baidu] &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)
* [Erforderliche und optionale Bulksheet-Daten für  [!DNL Google Ads] &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
* [Erforderliche und optionale Bulksheet-Daten für  [!DNL LY Ads] &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)
* [Erforderliche und optionale Bulksheet-Daten für  [!DNL Microsoft Advertising] &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
* [Erforderliche und optionale Bulksheet-Daten für  [!DNL Naver] &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
* [Erforderliche und optionale Bulksheet-Daten für  [!DNL Yahoo DSP] &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)
* [Erforderliche und optionale Bulksheet-Daten für  [!DNL Yandex] &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)

>[!MORELIKETHIS]
>
>* [&#x200B; (Neue Benutzeroberfläche) Verwalten von Kampagnendaten mithilfe von Bulksheets](about.md)
>* [(Neue Benutzeroberfläche) Hochladen einer Bulksheet- oder korrigierten Fehlerdatei](upload.md)
>* [&#x200B; (neue Benutzeroberfläche) Posten von Bulksheets oder korrigierte Fehlerdateien](post.md)
>* [(Neue Benutzeroberfläche) Validieren von Landingpages in Bulksheet-Dateien](validate-landing-pages.md)
