---
title: Verwalten von Inventardaten-Feed-Dateien
description: Erfahren Sie, wie Sie die Einstellungen konfigurieren, die steuern, wie Feed-Daten verarbeitet werden.
exl-id: 7d19ecc0-c939-4996-b22b-970ce8644b09
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Verwalten von Inventardaten-Feed-Dateien

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Wenn Sie Ihre eigenen Feed-Daten übermitteln, müssen Sie Dateien hochladen, die Ihre Produktdaten enthalten, um basierend auf Ihren Produktdaten dynamisch Kampagnenstruktur, Anzeigen und Keywords zu erstellen. Sie können sie dann mit Anzeigennetzwerk-spezifischen Anzeigenvorlagen verknüpfen, die Daten über die Vorlagen verarbeiten und die Daten schließlich an die entsprechenden Anzeigennetzwerke senden. Sie können einer Feed-Datei mehrere Vorlagen zuordnen, aber jede Vorlage kann nur einer Feed-Datei zugeordnet werden.

>[!NOTE]
>
>Laden Sie keine Dateien hoch, wenn Sie Daten direkt von einem Konto im Händlerzentrum verwenden.

Sie können Daten-Feed-Dateien wie folgt hochladen und verarbeiten:

* **Automatisch per FTP:** Sie können Dateien direkt in ein FTP-Verzeichnis hochladen; der Feed-Service sucht alle zwei Stunden nach neuen Dateien. Nachdem Sie eine Datei zum ersten Mal hochgeladen haben, können Sie sie mit einer Ad-Network-spezifischen Vorlage verknüpfen. Später werden alle Dateien, die Sie mit demselben Namen hochladen, automatisch derselben Vorlage zugeordnet. Je nachdem, wie Sie [Feed-Dateneinstellungen konfigurieren](feed-settings-manage.md) können Search, Social und Commerce die Feed-Daten automatisch durch alle anwendbaren Vorlagen übertragen und optional die resultierenden Kampagnen- und Anzeigendaten an die entsprechenden Werbenetzwerke senden.

  Um ein FTP-Verzeichnis zum Ablegen und automatischen Verarbeiten von Datendateien einzurichten, wenden Sie sich an Ihr Adobe-Account-Team.

* **Manuelle Verarbeitung** Sie können [Feed-Dateien hochladen](#feed-file-upload) über die Ansicht [!UICONTROL Advanced] (ACM) manuell anzeigen. Nachdem Sie eine Feed-Datei mit einer oder mehreren Anzeigennetzwerk-spezifischen [Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) verknüpft haben, können Sie Kampagnen- und Anzeigendaten generieren, indem [die Feed-Daten entsprechend den Einstellungen für [-Daten ](feed-data-propagate.md) die Vorlagen übertragen](feed-settings-manage.md). Sie können optional eine Vorschau der generierten Daten in Kampagnenhierarchieansichten anzeigen, eine Bulksheet-Datei zur Überprüfung generieren oder eine Bulksheet-Datei zur sofortigen Veröffentlichung im Werbenetzwerk generieren. Wenn Sie die Daten nicht sofort posten, können Sie [Vorschau anzeigen](propagated-data-view.md) und [veröffentlichen](propagated-data-post.md) später. Sie können [ die vorhandene Feed-Datei durch eine neue Datei ersetzen](#feed-file-replace) ohne vorhandene Vorlagenzuordnungen zu verlieren.

## Anforderungen an die Feed-Datei

Eine einzelne Datei erfordert keine spezifischen Datenfelder, aber für jede Datei sind die folgenden erforderlich:

* Die erste Zeile der Datei muss Spaltennamen enthalten (auch *Kopfzeilen* genannt), die den dynamischen Parametern in den zugehörigen Vorlagen entsprechen. Die übrigen Zeilen müssen Daten enthalten, die den Spaltennamen entsprechen. Jede Datenzeile (Zeile) darf sich nur auf eine Kontokomponente beziehen, z. B. eine Kampagne oder eine Anzeige. Die Werte in allen Zeilen müssen entweder durch Tabulatoren oder Kommas getrennt werden. Siehe die [CSV-Beispieldatei](#example-csv-feed-file) und [TSV-Beispieldatei](#example-tsv-feed-file) unten.

* Die Datei kann eine beliebige Größe haben, muss jedoch eine der folgenden Dateierweiterungen aufweisen: `.tsv` (für tabulatorgetrennte Werte), `.txt` (für [!DNL Unicode]-konformen ASCII-Text), `.csv` (für kommagetrennte Werte) oder `.zip` (für eine einzelne Datei im komprimierten ZIP-Format, die in eine TSV-Datei entpackt wird).

* Beim Dateinamen wird zwischen Groß- und Kleinschreibung unterschieden und die folgenden Zeichen dürfen nicht enthalten sein: `# % & * | \ : " < > . ? /`

* Wenn Sie Dateien in einem FTP-Verzeichnis ablegen, müssen Sie für jede Version der Datei denselben Dateinamen verwenden.

* (Nur [!DNL Google Ads] Vorlagen) Wenn Ihre Vorlage den Anzeigenparameter Param2 oder Param2 in Textanzeigen verwendet, müssen die entsprechenden Datenfelder in der Feed-Datei numerische Daten ohne Währungssymbole enthalten.

* Um vorhandene Kontokomponenten zu aktualisieren, geben Sie den Namen der vorhandenen Kampagne (und gegebenenfalls ihre Komponenten) an. Wenn die vorhandene Struktur nicht angegeben wird, werden neue Komponenten erstellt.

### Beispiel für eine kommagetrennte Feed-Datei {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### Beispiel einer tabulatorgetrennten Feed-Datei {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## Best Practices

* Verwenden Sie für Daten, die internationale Zeichen enthalten, Dateien im TSV- oder TXT-Format.

* Um einen wiederholbaren Prozess mit eingeschränkter manueller Überprüfung oder Bearbeitung zu erzielen, richten Sie Feed-Dateien und ihre Kontostrukturdaten wie folgt ein:

   * Spalten und Zeilen einschließen, die genügend Daten enthalten, um eine Kontostruktur zu erstellen oder die vorhandene Kontostruktur zuzuordnen. Idealerweise verwenden Sie eine vorhandene Kontostruktur, die eng mit der Produkttaxonomie verknüpft ist und der die Feed-Daten einfach zugeordnet werden können.

   * Binden Sie Beschreibungen ein, die kurz genug sind, um sie in der Anzeigenkopie zu verwenden.

   * Verwenden Sie konsistente Datenmuster und Benennungskonventionen in allen Produktzeilen.

   * Entfernen Sie alle vorangestellten Leerzeichen und nachfolgenden Leerzeichen.

   * Entfernen Sie alle beschädigten Zeichen.

## Anzeigen oder Herunterladen einer Feed-Datei

Sie können jede Feed-Datei öffnen oder herunterladen, die manuell oder per FTP hochgeladen wurde.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Suchen Sie die Feed-Datei:

1. Suchen Sie in der Vorlagenliste eine Vorlage, die die Feed-Datei verwendet.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]** , um eine Liste aller Feed-Dateien zu öffnen.

1. Klicken Sie auf den Namen der Feed-Datei.

1. Öffnen oder speichern Sie die Datei entsprechend dem normalen Verfahren Ihres Browsers.

Weitere Informationen finden Sie in der Online-Hilfe Ihres Browsers.

## Manuelles Hochladen einer Feed-Datei {#feed-file-upload}

>[!NOTE]
> Wenn Sie eine Vorlage mit einer manuell hochgeladenen Datei verknüpfen, dann aber über FTP eine andere Datei mit demselben Namen, derselben Dateierweiterung und derselben grammatischen Groß-/Kleinschreibung hochladen, wird die FTP-Datei verwendet, wenn Sie die Daten über die Vorlage übertragen. Beispiel: myfile.csv ersetzt myfile.csv, aber Myfile.csv nicht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Upload]**.

1. Geben Sie die hochzuladende Datei an, indem Sie entweder den vollständigen Pfad und Dateinamen eingeben oder auf **[!UICONTROL Browse]** klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

1. Klicken Sie auf **[!UICONTROL Upload].

Alle Felder in der Datei werden validiert. Sie können Elemente mit ungültigen Feldlängen erst dann veröffentlichen, wenn Sie die Werte korrigiert haben. Alle Spaltennamen in der Datei werden in Vorlagen als dynamische Parameter verfügbar.

## Ersetzen einer Feed-Datei {#feed-file-replace}

Wenn Sie eine Feed-Datei ersetzen, bleiben alle vorhandenen Vorlagenzuordnungen erhalten, selbst wenn die neue Datei einen anderen Dateinamen oder eine andere Erweiterung aufweist. Die neue Datei wird verwendet, wenn Sie Daten durch alle Vorlagen übertragen, die ursprünglich mit der vorherigen Datei verknüpft waren.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Spalte &quot;[!UICONTROL Feed]&quot; für eine beliebige Vorlage auf ![Weitere Optionen](/help/search-social-commerce/assets/options.png "Weitere Optionen") und wählen Sie **[!UICONTROL Re-upload]** aus.

   * Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**. Aktivieren Sie in der Liste Feed-Datei das Kontrollkästchen neben dem vorhandenen Dateinamen. Klicken Sie über der Datentabelle auf **[!UICONTROL Upload]**.

   >[!NOTE]
   >
   >Die Quelle der Feed-Datei (“[!UICONTROL FTP]&quot; oder &quot;&amp;mdash“ für manuell hochgeladene Dateien) ist in der Spalte &quot;[!UICONTROL Source]&quot; enthalten.

1. Geben Sie die hochzuladende Datei an, indem Sie entweder den vollständigen Pfad und Dateinamen eingeben oder auf **[!UICONTROL Browse]** klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

Selbst wenn die neue Datei einen anderen Dateinamen oder eine andere Dateierweiterung aufweist, wird die vorhandene Datei mit der neuen Datei überschrieben.

1. Klicken Sie auf **[!UICONTROL Re-Upload]**.

Alle Felder in der Datei werden validiert. Sie können Elemente mit ungültigen Feldlängen erst dann veröffentlichen, wenn Sie die Werte korrigiert haben. Alle Spaltennamen in der Datei werden in Vorlagen als dynamische Parameter verfügbar.

## Feed-Dateien löschen

Sie können jede Feed-Datei löschen, die manuell oder über FTP hochgeladen wurde. Wenn Sie eine Feed-Datei löschen, ist sie mit keiner Vorlage mehr verknüpft.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Datei, die Sie löschen möchten.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Verbreiten von Feed-Daten über Vorlagen](feed-data-propagate.md)
>* [Anzeigen der von Feeds generierten Daten](propagated-data-view.md)
>* [Bearbeiten der von Feeds generierten Daten](propagated-data-edit.md)
>* [Post-Kampagnendaten, die von Feeds an Werbenetzwerke generiert werden](propagated-data-post.md)
>* [Buchungsauftrag für Inventar-Feed-Daten anhalten](stop-job.md)
>* [Status der von Feeds generierten Daten](propagated-data-status.md)
