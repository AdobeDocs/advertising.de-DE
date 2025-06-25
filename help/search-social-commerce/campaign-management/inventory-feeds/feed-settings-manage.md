---
title: Konfigurieren von Feed-Dateneinstellungen
description: Erfahren Sie, wie Sie die Einstellungen konfigurieren, die steuern, wie Feed-Daten verarbeitet werden.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Konfigurieren von Feed-Dateneinstellungen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Sie können über die Feed-Einstellungen konfigurieren, wie Anzeigengruppen, Schlüsselwörter und Anzeigen in Feed-Datendateien verarbeitet werden und wie die Daten in FTP-Dateien verarbeitet werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Settings]**.

1. Geben Sie die [Feed-Dateneinstellungen](#feed-data-settings) an:

   1. Wählen Sie im [!UICONTROL Obsolete Item Auto-Processing] Abschnitt Informationen in den Feldern aus.

   1. (Werbetreibende, die Daten über FTP oder über einen direkten Link auf ein Konto eines Händlerzentrums hochladen) Wählen Sie im Abschnitt [!UICONTROL FTP/GMC Account Auto-Processing] die entsprechenden Informationen in den Feldern aus.

   1. Wählen Sie im [!UICONTROL Miscellaneous Auto-Processing] Abschnitt Informationen in den Feldern aus.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Einstellungen für Feed-Daten {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Wendet alle [!UICONTROL Obsolete Item Auto-processing] Einstellungen auf Folgendes an:

* *[!UICONTROL Ad Groups Only]:* Nur veraltete Anzeigengruppen.

* *[!UICONTROL Keywords Only]:* Nur veraltete Schlüsselwörter und Produktgruppen.

* *[!UICONTROL Ad Variations Only]* (Standard): Nur veraltete Anzeigen.

* *[!UICONTROL Keywords and Ad Variations]:* Sowohl veraltete Keywords/Produktziele/Produktgruppen als auch veraltete Anzeigen.

>[!NOTE]
>
>* Bei [!DNL Google Ads]-Shopping-Anzeigen ist nur die Produktgruppe auf der untersten Ebene betroffen.
>* Bei [!DNL Yandex]-Konten werden unabhängig von dieser Einstellung bei Anzeigenvarianten immer veraltete Aufgaben zur automatischen Verarbeitung von Elementen ausgeführt.

**[!UICONTROL When the Scheduled End Date is reached]:** (Nur manuell veröffentlichte Daten) Was tun mit Zeileneinträgen in einer Feed-Datei, die mit einem bestimmten Enddatum und einer bestimmten Endzeit veröffentlicht werden, wenn die Endzeit eintrifft:

* *[!UICONTROL Delete]* (Standard): Löschen aller relevanten Komponenten, wenn die angegebene Endzeit eintrifft. Dieser Vorgang kann nicht rückgängig gemacht werden.

* *[!UICONTROL Pause]:* Pausiert alle relevanten Komponenten, wenn die angegebene Endzeit eintrifft. Sie können die Komponenten bei Bedarf später reaktivieren.

* *[!UICONTROL None]:* Ändern Sie nicht den Status der relevanten Komponenten.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Was ist mit vorhandenen Elementen zu tun, wenn sie nicht in einer neuen Feed-Datei enthalten sind, die manuell hochgeladen wurde, oder wenn sie gemäß den Zuordnungseinstellungen in der Vorlage nicht vorhandenen Kampagnen oder Anzeigengruppen zugeordnet sind?

* *[!UICONTROL Delete]:* Löschen Sie die vorhandenen Komponenten.

* *[!UICONTROL Pause]:* Pausieren der vorhandenen Komponenten. Sie werden reaktiviert, wenn eine neue Feed-Datei dieselben Zeileneinträge enthält und sie ihren Verlauf und ihre Qualitätswerte beibehalten. **Hinweis:** Wenn alle untergeordneten Produktgruppen für eine übergeordnete Produktgruppe fehlen, wird die übergeordnete Produktgruppe gelöscht, da Sie die Produktgruppen nicht anhalten können.

* *[!UICONTROL None]* (Standard): Ändern Sie die vorhandenen Komponenten nicht.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Was ist mit bestehenden Elementen zu tun, wenn 1) sie nicht a) in eine neue Feed-Datei aufgenommen werden, die in ein FTP-Verzeichnis hochgeladen wurde, b) das nächste Mal, wenn Search, Social und Commerce mit ihnen synchronisiert werden, in ein Merchant Center-Konto aufgenommen werden oder 2) sie nicht vorhandenen Kampagnen oder Anzeigengruppen gemäß den [!UICONTROL Map Only] in der Vorlage zugeordnet werden.

* *[!UICONTROL Delete]:* Löschen Sie die vorhandenen Komponenten.

* *[!UICONTROL Pause]:* Pausieren der vorhandenen Komponenten. Sie werden wieder aktiviert, wenn neue Daten dieselben Zeileneinträge enthalten und sie ihren Verlauf und ihre Qualitätsbewertung beibehalten. **Hinweis:** Wenn alle untergeordneten Produktgruppen für eine übergeordnete Produktgruppe fehlen, wird die übergeordnete Produktgruppe gelöscht, da Sie die Produktgruppen nicht anhalten können.

* *[!UICONTROL None]* (Standard): Ändern Sie die vorhandenen Komponenten nicht.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Was ist mit Zeileneinträgen zu tun, die einen Lagerbestand enthalten, wenn:

* (Bei Futtermitteln mit nur numerischen Lagerwerten in der angegebenen Spalte) Der Lagerbestand liegt bei oder unter einer bestimmten Menge. Die Standardmenge ist null (0).

* (Bei Feeds mit Textwerten in der angegebenen Spalte) Der Wert für [!UICONTROL Availability] ist &quot;[!UICONTROL out of stock]&quot;. Bei dem Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden. **Hinweis** **Geben Sie in den Feed-Vorlagen textbasierte Spalten auf Stock-Ebene mit dem Kontrollkästchen für &quot;[!UICONTROL This column has non-numeric values]&quot; an.

Wählen Sie die Aktion für beide Fälle aus:

* *[!UICONTROL Delete]* (Standard) Löschen Sie die Komponenten.

* *[!UICONTROL Pause]:* Komponenten anhalten. Wenn die Daten aktualisiert werden, werden die Komponenten wieder aktiviert, wenn die numerischen Lagerwerte die angegebene Menge überschreiten oder wenn die [!UICONTROL Availability] &quot;[!UICONTROL in stock]&quot; oder &quot;[!UICONTROL preorder]&quot; ist. Die Komponenten behalten ihre Historie und Qualitätsbewertung bei.

Der Bestand für jeden Zeileneintrag stammt aus einer Spalte in der Feed-Datei, die im Feld &quot;[!UICONTROL Stock Level]&quot; für jede Vorlage angegeben ist.

>[!TIP]
>
>* Bei Produkten oder Services, von denen Sie erwarten, dass sie erneut vorrätig sind oder die Verfügbarkeit für sie erhöhen, sollten Sie Anzeigengruppen, Keywords und Anzeigen pausieren, anstatt sie zu löschen und neu zu erstellen. Durch das Anhalten können sie ihre Qualitätswerte beibehalten.
>* Wenn Sie die veraltete automatische Verarbeitung für Anzeigengruppen aktivieren und neue Daten eine Lagerebene für die Anzeigengruppe enthalten, ist es sinnvoll, die Anzeigengruppe nur zu löschen oder auszusetzen, wenn die angegebene Lagerebene auf der Kategorieebene und nicht auf der Marken-/Artikelebene ist. Wenn Sie beispielsweise eine Anzeigengruppe „Cabrios“ haben, sollte die Lagerebene für die Anzeigengruppe der Gesamtbetrag für alle einzelnen Cabriolet-Modelle sein, die in der Anzeigengruppe dargestellt werden.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Werbetreibende, die Datendateien über FTP oder ein Konto eines Händlerzentrums hochladen) propagieren neue Daten automatisch über die entsprechenden Vorlagen. Die Option ist standardmäßig ausgewählt. Wenn Sie die Option deaktivieren, können Sie Daten für jede Feed-Datei, jedes Konto oder für jede Vorlage manuell weitergeben.

>[!NOTE]
>
>* Bei FTP-Dateien sucht der Feed-Service alle zwei Stunden im FTP-Verzeichnis nach Aktualisierungen (in der PST-Zeitzone nach geraden Stunden). Diese Option verarbeitet alle Dateien, die seit der letzten Prüfung hochgeladen wurden.
>* Für Merchant Center-Konten synchronisiert Search, Social und Commerce täglich um ca. 06:00 Uhr in der Zeitzone des Werbetreibenden mit dem Konto. Diese Option verarbeitet alle Daten, die seit der letzten Synchronisierung aktualisiert wurden.
>* Weitergegebene Daten sind auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] verfügbar, bis die Daten an das Werbenetzwerk oder die [!UICONTROL Bulksheets] gesendet werden.

**[!UICONTROL Post to the SE]:** (Werbetreibende, die Datendateien über FTP oder ein Händlerkonto hochladen) erstellt automatisch Bulksheet-Dateien in den richtigen Formaten für die relevanten Werbenetzwerke, nachdem neue Daten über die entsprechenden Vorlagen propagiert wurden. Mit dieser Option werden auch die Daten aus den Registerkarten &quot;[!UICONTROL Campaigns]&quot;, &quot;[!UICONTROL Ad Groups]&quot;, &quot;[!UICONTROL Keywords]&quot; und &quot;[!UICONTROL Ads]&quot; entfernt, sofern keine Unterkomponenten Fehler aufweisen.

Diese Option ist standardmäßig deaktiviert. Um diese Option zu aktivieren, aktivieren Sie das Kontrollkästchen und geben Sie dann an, ob Bulksheet-Dateien in die Werbenetzwerke gepostet werden sollen:

* *[!UICONTROL Immediately]* (Standard): Stellt die Bulk Sheet-Dateien in den entsprechenden Werbenetzwerken bereit, nachdem die Daten über die Vorlagen weitergegeben wurden. Die Bulksheet-Dateien bleiben 30 Tage lang in der [!UICONTROL Bulksheets] verfügbar.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:**&#x200B; sendet die Bulksheet-Dateien nicht in die entsprechenden Werbenetzwerke, sondern listet sie in der [!UICONTROL Bulksheets] Ansicht auf, aus der Sie sie später posten können. Die Bulksheet-Dateien bleiben 30 Tage lang in der [!UICONTROL Bulksheets] verfügbar. Wenn die Bulksheet-Datei größer als 10 MB, aber kleiner als 2 GB ist, liegt die Datei im ZIP-Format vor; Sie müssen die Datei nicht entpacken, um sie zu veröffentlichen. &#x200B;** Tipp:** Wenn Sie Ihre Landingpages noch nicht validiert haben, verwenden Sie diese Option, damit Sie sie in der [!UICONTROL Bulksheets] validieren können, bevor Sie die Daten an das Werbenetzwerk senden.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Schließt das Posten von Keyword-Phrasen mit mehr als einer angegebenen Anzahl von Wörtern im Werbenetzwerk aus. Wenn diese Option ausgewählt ist, werden Keyword-Phrasen mit mehr als der maximalen Anzahl von Wörtern propagiert und auf der Registerkarte [!UICONTROL Keywords] aufgeführt, aber sie werden nicht gepostet, wenn Sie versuchen, die Daten zu posten.

Diese Option ist standardmäßig deaktiviert, sodass alle Keywords veröffentlicht werden, unabhängig davon, wie viele Wörter die Phrase enthält. Wenn Sie diese Option wählen, wählen Sie die maximale Anzahl von Wörtern, die gepostet werden sollen (von 3-10).

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Verbreiten von Feed-Daten über Vorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Post-Kampagnendaten, die von Feeds an Werbenetzwerke generiert werden](propagated-data-post.md)
