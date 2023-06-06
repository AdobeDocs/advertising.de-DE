---
title: Verwalten von Bestandsdaten-Feed-Dateien
description: Erfahren Sie, wie Sie die Einstellungen konfigurieren, die steuern, wie Feed-Daten verarbeitet werden.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 0%

---

# Verwalten von Bestandsdaten-Feed-Dateien

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Wenn Sie Ihre eigenen Feed-Daten senden, müssen Sie Dateien mit Ihren Produktdaten hochladen, um basierend auf Ihren Produktdaten dynamisch Kampagnenstruktur, Anzeigen und Suchbegriffe zu erstellen. Anschließend können Sie sie mit Anzeigennetzwerkspezifischen Anzeigenvorlagen verknüpfen und die Daten über die Vorlagen verarbeiten, um sie schließlich an die relevanten Anzeigennetzwerke zu senden. Sie können mehrere Vorlagen mit einer Feed-Datei verknüpfen, aber jede Vorlage kann nur einer Feed-Datei zugeordnet werden.

>[!NOTE]
>
>Laden Sie keine Dateien hoch, wenn Sie Daten direkt von einem Händlernetzwerk-Konto verwenden.

Sie können Daten-Feed-Dateien auf eine der folgenden Arten hochladen und verarbeiten:

* **Automatische Verwendung von FTP:** Sie können Dateien direkt in ein FTP-Verzeichnis hochladen. Der Feed-Dienst sucht alle zwei Stunden nach neuen Dateien. Nachdem Sie eine Datei zum ersten Mal hochgeladen haben, können Sie sie mit einer netzwerkspezifischen Anzeigenvorlage verknüpfen. Später werden alle Dateien, die Sie mit demselben Namen hochladen, automatisch derselben Vorlage zugeordnet. Abhängig von der Vorgehensweise [Konfigurieren der Feed-Dateneinstellungen](feed-settings-manage.md), Search, Social und Commerce können die Feed-Daten automatisch über alle relevanten Vorlagen übertragen und optional die resultierenden Kampagnen- und Anzeigendaten an die relevanten Anzeigennetzwerke posten.

   Wenden Sie sich an Ihr Adobe Account-Team, um ein FTP-Verzeichnis zum Verwahren und automatischen Verarbeiten von Datendateien einzurichten.

* **Manuelle Verarbeitung:** Sie können [Feed-Dateien hochladen](#feed-file-upload) von [!UICONTROL Advanced] (ACM) angezeigt. Nachdem Sie eine Feed-Datei mit einer oder mehreren Ad-Netzwerk-spezifischen [templates](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)können Sie Kampagnen- und Anzeigendaten generieren, indem Sie [Feed-Daten über die Vorlagen übertragen](feed-data-propagate.md) gemäß [Feed-Dateneinstellungen](feed-settings-manage.md). Sie können optional die generierten Daten in den Kampagnen-Hierarchieansichten in der Vorschau anzeigen, eine Bulksheet-Datei zur Überprüfung generieren oder eine Bulksheet-Datei für die sofortige Veröffentlichung in das Werbenetzwerk generieren. Wenn Sie die Daten nicht sofort posten, können Sie [Vorschau anzeigen](propagated-data-view.md) und [posten](propagated-data-post.md) später. Sie können später [Ersetzen der vorhandenen Feed-Datei durch eine neue Datei](#feed-file-replace) ohne vorhandene Vorlagenzuordnungen zu verlieren.

## Dateivoraussetzungen für Feeds

In einer Datei sind keine spezifischen Datenfelder erforderlich, für jede Datei sind jedoch die folgenden erforderlich:

* Die erste Zeile in der Datei muss Spaltennamen enthalten (auch als *Kopfzeilen*), die den dynamischen Parametern in den verknüpften Vorlagen entsprechen. Die übrigen Zeilen müssen Daten enthalten, die den Spaltennamen entsprechen. Jede Datenzeile (Zeile) darf nur eine Kontokomponente enthalten, z. B. eine Kampagne oder eine Anzeige. Die Werte aller Zeilen müssen durch Tabulatoren oder Kommas getrennt werden. Siehe [CSV-Beispieldatei](#example-csv-feed-file) und [TSV-Beispieldatei](#example-tsv-feed-file) unten.

* Die Datei kann eine beliebige Größe aufweisen, muss jedoch über eine der folgenden Dateierweiterungen verfügen: `.tsv` (für tabulatorgetrennte Werte), `.txt` (für [!DNL Unicode]-konformer ASCII-Text), `.csv` (bei kommagetrennten Werten) oder `.zip` (für eine einzelne Datei im komprimierten ZIP-Format, die zu einer TSV-Datei dekomprimiert wird).

* Beim Dateinamen wird zwischen Groß- und Kleinschreibung unterschieden. Folgende Zeichen sind nicht zulässig: `# % & * | \ : " < > . ? /`

* Wenn Sie Dateien in ein FTP-Verzeichnis ablegen, müssen Sie für jede Version der Datei denselben Dateinamen verwenden.

* ([!DNL Google Ads] Nur Vorlagen) Wenn Ihre Vorlage den Parameter Param2 oder Param2 ad in Textanzeigen verwendet, müssen die entsprechenden Datenfelder in der Feed-Datei numerische Daten ohne monetäre Symbole enthalten.

* Um vorhandene Kontokomponenten zu aktualisieren, fügen Sie den Namen der vorhandenen Kampagne (und gegebenenfalls deren Komponenten) ein. Wenn die vorhandene Struktur nicht angegeben ist, werden neue Komponenten erstellt.

### Beispiel einer kommagetrennten Feed-Datei {#example-csv-feed-file}

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

* Um einen wiederholbaren Prozess mit eingeschränkter manueller Überprüfung oder Bearbeitung zu erreichen, richten Sie Feed-Dateien und ihre Kontostrukturdaten wie folgt ein:

   * Schließen Sie Spalten und Zeilen ein, die ausreichend Daten enthalten, um eine Kontostruktur zu erstellen oder der vorhandenen Kontostruktur zuzuordnen. Idealerweise sollten Sie eine vorhandene Kontostruktur verwenden, die eng mit der Produkttaxonomie verknüpft ist und der die Feed-Daten leicht zugeordnet werden können.

   * Fügen Sie Beschreibungen ein, die kurz genug sind, um in der Anzeigenkopie verwendet zu werden.

   * Verwenden Sie konsistente Datenmuster und Benennungskonventionen für alle Produktzeilen.

   * Entfernen Sie alle vorangehenden Leerzeichen und nachfolgenden Leerzeichen.

   * Entfernen Sie alle unleserlichen Zeichen.

## Anzeigen oder Herunterladen einer Feed-Datei

Sie können jede Feed-Datei öffnen oder herunterladen, die manuell oder über FTP hochgeladen wurde.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Suchen Sie die Feed-Datei:

1. Suchen Sie in der Vorlagenliste nach einer Vorlage, die die Feed-Datei verwendet.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]** , um eine Liste aller Feed-Dateien zu öffnen.

1. Klicken Sie auf den Feed-Dateinamen.

1. Öffnen oder speichern Sie die Datei entsprechend der üblichen Vorgehensweise Ihres Browsers.

Weitere Informationen finden Sie in der Online-Hilfe Ihres Browsers.

## Manuelles Hochladen einer Feed-Datei [#feed-file-upload]

>[!NOTE]
> Wenn Sie eine Vorlage mit einer manuell hochgeladenen Datei verknüpfen, aber dann per FTP eine andere Datei mit demselben Namen, derselben Dateierweiterung und derselben grammatischen Schreibweise hochladen, wird die FTP-Datei verwendet, wenn Sie die Daten über die Vorlage propagieren. Beispielsweise ersetzt &quot;myfile.csv&quot;die Datei &quot;myfile.csv&quot;, &quot;myfile.CSV&quot;jedoch nicht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Upload]**.

1. Geben Sie die hochzuladende Datei an, indem Sie entweder den vollständigen Pfad und den Dateinamen eingeben oder auf **[!UICONTROL Browse]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

1. Klicken **[!UICONTROL Upload].

Alle Felder in der Datei werden validiert. Sie können Elemente mit ungültigen Feldlängen erst später posten, wenn Sie die Werte korrigieren. Alle Spaltennamen in der Datei stehen in Vorlagen als dynamische Parameter zur Verfügung.

## Ersetzen einer Feed-Datei {#feed-file-replace}

Wenn Sie eine Feed-Datei ersetzen - auch wenn die neue Datei einen anderen Dateinamen oder eine andere Erweiterung aufweist - bleiben alle vorhandenen Vorlagenzuordnungen erhalten. Die neue Datei wird verwendet, wenn Sie Daten über alle Vorlagen übertragen, die ursprünglich mit der vorherigen Datei verknüpft waren.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Führen Sie einen der folgenden Schritte aus:

   * Im [!UICONTROL Feed] Spalte für eine beliebige Vorlage, klicken Sie auf ![Weitere Optionen](/help/search-social-commerce/assets/options.png "Weitere Optionen") und wählen Sie **[!UICONTROL Re-upload]**.

   * Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**. Aktivieren Sie in der Liste der Feed-Dateien das Kontrollkästchen neben dem vorhandenen Dateinamen. Klicken Sie über der Datentabelle auf **[!UICONTROL Upload]**.
   >[!NOTE]
   >
   >Die Quelle der Feed-Datei (&quot;[!UICONTROL FTP]&quot; oder &quot;&amp;mdash&quot;für manuell hochgeladene Dateien) ist im [!UICONTROL Source] Spalte.

1. Geben Sie die hochzuladende Datei an, indem Sie entweder den vollständigen Pfad und den Dateinamen eingeben oder auf **[!UICONTROL Browse]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

Selbst wenn die neue Datei einen anderen Dateinamen oder eine andere Erweiterung aufweist, wird die vorhandene Datei mit der neuen Datei überschrieben.

1. Klicken **[!UICONTROL Re-Upload]**.

Alle Felder in der Datei werden validiert. Sie können Elemente mit ungültigen Feldlängen erst später posten, wenn Sie die Werte korrigieren. Alle Spaltennamen in der Datei stehen in Vorlagen als dynamische Parameter zur Verfügung.

## Feed-Dateien löschen

Sie können jede Feed-Datei löschen, die manuell oder via FTP hochgeladen wurde. Wenn Sie eine Feed-Datei löschen, ist sie mit keiner Vorlage mehr verknüpft.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Datei, die Sie löschen möchten.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsnachricht auf **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Feed-Daten über Vorlagen übertragen](feed-data-propagate.md)
>* [Aus Feeds generierte Daten anzeigen](propagated-data-view.md)
>* [Aus Feeds generierte Daten bearbeiten](propagated-data-edit.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
>* [Status der aus Feeds generierten Daten](propagated-data-status.md)

