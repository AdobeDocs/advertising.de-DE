---
title: Konfigurieren der Feed-Dateneinstellungen
description: Erfahren Sie, wie Sie die Einstellungen konfigurieren, die steuern, wie Feed-Daten verarbeitet werden.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Konfigurieren der Feed-Dateneinstellungen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Sie können konfigurieren, wie Anzeigengruppen, Suchbegriffe und Anzeigen in Feed-Datendateien verarbeitet und wie die Daten in FTP-Dateien speziell über die Feed-Einstellungen verarbeitet werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Settings]**.

1. Geben Sie die [Feed-Dateneinstellungen](#feed-data-settings) an:

   1. Wählen Sie im Abschnitt [!UICONTROL Obsolete Item Auto-Processing] Informationen in den Feldern aus.

   1. (Werbetreibende, die Daten über FTP oder über einen direkten Link zu einem Händlernetzwerk-Konto hochladen) Wählen Sie im Abschnitt [!UICONTROL FTP/GMC Account Auto-Processing] Informationen in den Feldern aus.

   1. Wählen Sie im Abschnitt [!UICONTROL Miscellaneous Auto-Processing] Informationen in den Feldern aus.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Feed-Dateneinstellungen {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Wendet alle [!UICONTROL Obsolete Item Auto-processing]-Einstellungen auf Folgendes an:

* *[!UICONTROL Ad Groups Only]:* Nur veraltete Anzeigengruppen.

* *[!UICONTROL Keywords Only]:* Nur veraltete Suchbegriffe und Produktgruppen.

* *[!UICONTROL Ad Variations Only]* (Standard): Nur veraltete Anzeigen.

* *[!UICONTROL Keywords and Ad Variations]:* Sowohl veraltete Suchbegriffe/Produktziele/Produktgruppen als auch veraltete Anzeigen.

>[!NOTE]
>
>* Bei [!DNL Google Ads] Shopping-Anzeigen ist nur die Produktgruppe der niedrigsten Ebene betroffen.
>* Bei [!DNL Yandex] -Konten werden veraltete Aufgaben zur automatischen Verarbeitung von Elementen immer bei Anzeigenvarianten ausgeführt, unabhängig von dieser Einstellung.

**[!UICONTROL When the Scheduled End Date is reached]:** (Nur manuell gepostete Daten) Was ist mit Zeileneinträgen in einer Feed-Datei zu tun, die mit einem angegebenen Enddatum und einer angegebenen Endzeit gesendet wird, sobald die Endzeit erreicht ist:

* *[!UICONTROL Delete]* (Standard): Löschen Sie alle relevanten Komponenten, wenn die angegebene Endzeit erreicht ist. Sie können diesen Vorgang nicht rückgängig machen.

* *[!UICONTROL Pause]:* Halten Sie alle relevanten Komponenten an, wenn die angegebene Endzeit eintritt. Sie können die Komponenten bei Bedarf später reaktivieren.

* *[!UICONTROL None]:* Ändern Sie den Status der relevanten Komponenten nicht.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Was ist mit vorhandenen Elementen zu tun, wenn sie nicht in einer neuen Feed-Datei enthalten sind, die manuell hochgeladen wurde, oder wenn sie nicht vorhandenen Kampagnen oder Anzeigengruppen gemäß den Einstellungen Nur zuordnen in der Vorlage zugeordnet sind:

* *[!UICONTROL Delete]:* Löschen Sie die vorhandenen Komponenten.

* *[!UICONTROL Pause]:* Halten Sie die vorhandenen Komponenten an. Sie werden reaktiviert, wenn eine neue Feed-Datei eines der gleichen Zeileneinträge enthält und sie ihren Verlauf und ihre Qualitätsbewertungen beibehalten. **Hinweis:** Wenn alle untergeordneten Produktgruppen für eine übergeordnete Produktgruppe fehlen, wird die übergeordnete Produktgruppe gelöscht, da Sie keine Produktgruppen anhalten können.

* *[!UICONTROL None]* (Standard): Ändern Sie die vorhandenen Komponenten nicht.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Was ist mit vorhandenen Elementen zu tun, wenn 1) sie nicht enthalten sind a) in einer neuen Feed-Datei, die in ein FTP-Verzeichnis hochgeladen wurde, oder b) in einem Händlercenterkonto beim nächsten Synchronisieren von Search, Social und Commerce oder 2), wenn sie nicht vorhandenen Kampagnen oder Anzeigengruppen gemäß den [!UICONTROL Map Only] -Einstellungen in der Vorlage zugeordnet werden.

* *[!UICONTROL Delete]:* Löschen Sie die vorhandenen Komponenten.

* *[!UICONTROL Pause]:* Halten Sie die vorhandenen Komponenten an. Sie werden reaktiviert, wenn neue Daten eines der gleichen Zeileneinträge enthalten und sie ihren Verlauf und ihre Qualitätsbewertung beibehalten. **Hinweis:** Wenn alle untergeordneten Produktgruppen für eine übergeordnete Produktgruppe fehlen, wird die übergeordnete Produktgruppe gelöscht, da Sie keine Produktgruppen anhalten können.

* *[!UICONTROL None]* (Standard): Ändern Sie die vorhandenen Komponenten nicht.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Was ist mit Zeileneinträgen zu tun, die einen Lagerbestand enthalten, wenn:

* (Für Feeds mit nur numerischen Bestandswerten in der angegebenen Spalte) Die Lagerbestände liegen bei oder unter einer angegebenen Menge. Die Standardmenge ist null (0).

* (Bei Feeds mit Textwerten in der angegebenen Spalte) Der Wert für [!UICONTROL Availability] ist &quot;[!UICONTROL out of stock]&quot;. Beim Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden. **Hinweis:** **Geben Sie in Feed-Vorlagen textbasierte Spalten auf Lagerebene an, indem Sie das Kontrollkästchen für &quot;[!UICONTROL This column has non-numeric values]&quot;aktivieren.

Wählen Sie die Aktion für beide Fälle aus:

* *[!UICONTROL Delete]* (Standard) Löschen Sie die Komponenten.

* *[!UICONTROL Pause]:* Halten Sie die Komponenten an. Wenn die Daten aktualisiert werden, werden die Komponenten reaktiviert, wenn die numerischen Bestandswerte über der angegebenen Menge liegen oder wenn der [!UICONTROL Availability] &quot;[!UICONTROL in stock]&quot; oder &quot;[!UICONTROL preorder]&quot; ist. Die Komponenten behalten ihren Verlauf und ihre Qualitätsbewertung bei.

Der Lagerbestand für jedes Zeilenelement stammt aus einer Spalte in der Feed-Datei, wie im Feld &quot;[!UICONTROL Stock Level]&quot; für jede Vorlage angegeben.

>[!TIP]
>
>* Bei Produkten oder Dienstleistungen, die Sie voraussichtlich neu anbieten oder die Verfügbarkeit erhöhen, sollten Sie Anzeigengruppen, Suchbegriffe und Anzeigen anhalten, anstatt sie zu löschen und neu zu erstellen. Durch Anhalten können sie ihre Qualitätsbewertungen beibehalten.
>* Wenn Sie die veraltete automatische Verarbeitung für Anzeigengruppen aktivieren und neue Daten eine Lagerposition für die Anzeigengruppe enthalten, ist es sinnvoll, die Anzeigengruppe nur dann zu löschen oder anzuhalten, wenn sich die angegebene Lagerbestandsebene auf der Kategorienebene und nicht auf der Marken-/Artikelebene befindet. Wenn Sie beispielsweise über eine Anzeigengruppe &quot;Konvertierungen&quot;verfügen, sollte die Aktienebene für die Anzeigengruppe die Gesamtsumme aller einzelnen konvertierbaren Modelle in der Anzeigengruppe sein.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Werbetreibende, die Datendateien über FTP oder ein Händlernetzwerk-Konto hochladen) Übernimmt automatisch neue Daten über die entsprechenden Vorlagen. Die Option ist standardmäßig ausgewählt. Wenn Sie die Option deaktivieren, können Sie weiterhin manuell Daten für jede Feed-Datei, jedes Konto oder für jede Vorlage übertragen.

>[!NOTE]
>
>* Bei FTP-Dateien sucht der Feed-Dienst alle zwei Stunden nach Aktualisierungen im FTP-Verzeichnis (gerade nummerierte Stunden in der PST-Zeitzone). Diese Option verarbeitet alle Dateien, die seit der letzten Prüfung hochgeladen wurden.
>* Bei Handelscenter-Konten synchronisiert sich Search, Social und Commerce täglich um ca. 06:00 Uhr in der Zeitzone des Werbetreibenden mit dem Konto. Diese Option verarbeitet alle Daten, die seit der letzten Synchronisierung aktualisiert wurden.
>* Propagierte Daten sind über die Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] verfügbar, bis die Daten an das Anzeigennetzwerk oder die Ansicht [!UICONTROL Bulksheets] gesendet werden.

**[!UICONTROL Post to the SE]:** (Werbetreibende, die Datendateien über FTP oder ein Händlernetzwerk-Konto hochladen) Erstellt automatisch Bulksheet-Dateien in den richtigen Formaten für die relevanten Anzeigennetzwerke, nachdem neue Daten über die entsprechenden Vorlagen übertragen wurden. Mit dieser Option werden auch die Daten aus den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] entfernt, sofern keine Unterkomponenten Fehler aufweisen.

Diese Option ist standardmäßig deaktiviert. Um diese Option zu aktivieren, aktivieren Sie das Kontrollkästchen und geben Sie an, ob Bulksheet-Dateien in den Werbenetzwerken veröffentlicht werden sollen:

* *[!UICONTROL Immediately]* (Standard): Sendet die Massenblattdateien an die relevanten Anzeigennetzwerke, nachdem die Daten über die Vorlagen übertragen wurden. Die Bulksheet-Dateien bleiben 30 Tage in der Ansicht [!UICONTROL Bulksheets] verfügbar.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Posten Sie die Bulksheet-Dateien nicht in den relevanten Werbenetzwerken, sondern listen Sie sie in der Ansicht [!UICONTROL Bulksheets] auf, aus der Sie sie später posten können. Die Bulksheet-Dateien bleiben 30 Tage in der Ansicht [!UICONTROL Bulksheets] verfügbar. Wenn die Bulksheet-Datei größer als 10 MB, aber kleiner als 2 GB ist, liegt die Datei im ZIP-Format vor. Sie müssen die Datei nicht entpacken, um sie zu posten. **Tipp:** Wenn Sie Ihre Landingpages noch nicht validiert haben, verwenden Sie diese Option, damit Sie sie in der [!UICONTROL Bulksheets] -Ansicht validieren können, bevor Sie die Daten an das Werbenetzwerk senden.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Schließt das Posten von Suchbegriffsätzen mit mehr als einer angegebenen Anzahl von Wörtern in das Werbenetzwerk aus. Wenn diese Option aktiviert ist, werden Suchbegriffe mit mehr als der maximalen Wortanzahl propagiert und auf der Registerkarte [!UICONTROL Keywords] aufgelistet, sie werden jedoch nicht veröffentlicht, wenn Sie versuchen, die Daten zu posten.

Diese Option ist standardmäßig deaktiviert, sodass alle Suchbegriffe gepostet werden, unabhängig davon, wie viele Wörter der Satz enthält. Wenn Sie diese Option auswählen, wählen Sie die maximale Anzahl an Wörtern aus, die gepostet werden sollen (von 3 bis 10).

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Übertragen von Feed-Daten über Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
