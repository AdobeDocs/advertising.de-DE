---
title: Konfigurieren der Feed-Dateneinstellungen
description: Erfahren Sie, wie Sie die Einstellungen konfigurieren, die steuern, wie Feed-Daten verarbeitet werden.
exl-id: fc72d1bc-aac7-4280-80c6-4fc53a96a49f
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---

# Konfigurieren der Feed-Dateneinstellungen

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Sie können konfigurieren, wie Anzeigengruppen, Suchbegriffe und Anzeigen in Feed-Datendateien verarbeitet und wie die Daten in FTP-Dateien speziell über die Feed-Einstellungen verarbeitet werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Settings]**.

1. Geben Sie die [Feed-Dateneinstellungen](#feed-data-settings):

   1. Im [!UICONTROL Obsolete Item Auto-Processing] Informationen in den Feldern auswählen.

   1. (Werbetreibende, die Daten via FTP oder über einen direkten Link zu einem Händlerstädtenkonto hochladen) Im [!UICONTROL FTP/GMC Account Auto-Processing] Informationen in den Feldern auswählen.

   1. Im [!UICONTROL Miscellaneous Auto-Processing] Informationen in den Feldern auswählen.

1. Klicken **[!UICONTROL Save]**.

## Feed-Dateneinstellungen {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Gilt für alle [!UICONTROL Obsolete Item Auto-processing] Einstellungen für:

* *[!UICONTROL Ad Groups Only]:* Nur veraltete Anzeigengruppen.

* *[!UICONTROL Keywords Only]:* Nur veraltete Suchbegriffe und Produktgruppen.

* *[!UICONTROL Ad Variations Only]* (Standard): Nur veraltete Anzeigen.

* *[!UICONTROL Keywords and Ad Variations]:* Sowohl veraltete Suchbegriffe/Produktziele/Produktgruppen als auch veraltete Anzeigen.

>[!NOTE]
>
>* Für [!DNL Google Ads] Shopping-Anzeigen, ist nur die Produktgruppe der niedrigsten Ebene betroffen.
>* Für [!DNL Yandex] Konten werden veraltete Aufgaben zur automatischen Verarbeitung von Elementen immer bei Anzeigenvarianten ausgeführt, unabhängig von dieser Einstellung.

**[!UICONTROL When the Scheduled End Date is reached]:** (Nur manuell gepostete Daten) Was ist mit Zeileneinträgen in einer Feed-Datei zu tun, die mit einem angegebenen Enddatum und einer festgelegten Endzeit veröffentlicht wird, sobald die Endzeit erreicht ist?

* *[!UICONTROL Delete]* (Standardeinstellung): Löschen Sie alle relevanten Komponenten, wenn die angegebene Endzeit erreicht ist. Sie können diesen Vorgang nicht rückgängig machen.

* *[!UICONTROL Pause]:* Halten Sie alle relevanten Komponenten an, wenn die angegebene Endzeit eintritt. Sie können die Komponenten bei Bedarf später reaktivieren.

* *[!UICONTROL None]:* Ändern Sie den Status der relevanten Komponenten nicht.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Was passiert mit vorhandenen Elementen, wenn sie nicht in einer neuen Feed-Datei enthalten sind, die manuell hochgeladen wurde, oder wenn sie nicht vorhandenen Kampagnen oder Anzeigengruppen gemäß den Einstellungen Nur zuordnen in der Vorlage zugeordnet sind?

* *[!UICONTROL Delete]:* Löschen Sie die vorhandenen Komponenten.

* *[!UICONTROL Pause]:* Halten Sie die vorhandenen Komponenten an. Sie werden reaktiviert, wenn eine neue Feed-Datei eines der gleichen Zeileneinträge enthält und sie ihren Verlauf und ihre Qualitätsbewertungen beibehalten. **Hinweis:** Wenn alle untergeordneten Produktgruppen für eine übergeordnete Produktgruppe fehlen, wird die übergeordnete Produktgruppe gelöscht, da Sie keine Produktgruppen anhalten können.

* *[!UICONTROL None]* (Standard): Ändern Sie die vorhandenen Komponenten nicht.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Was tun mit vorhandenen Elementen, wenn 1) sie nicht a) in einer neuen Feed-Datei enthalten sind, die in ein FTP-Verzeichnis hochgeladen wurde, oder b) in einem Händlercenter-Konto, wenn sie das nächste Mal synchronisiert werden, oder 2), wenn sie nicht vorhandenen Kampagnen oder Anzeigengruppen gemäß [!UICONTROL Map Only] -Einstellungen in der Vorlage.

* *[!UICONTROL Delete]:* Löschen Sie die vorhandenen Komponenten.

* *[!UICONTROL Pause]:* Halten Sie die vorhandenen Komponenten an. Sie werden reaktiviert, wenn neue Daten eines der gleichen Zeileneinträge enthalten und sie ihren Verlauf und ihre Qualitätsbewertung beibehalten. **Hinweis:** Wenn alle untergeordneten Produktgruppen für eine übergeordnete Produktgruppe fehlen, wird die übergeordnete Produktgruppe gelöscht, da Sie keine Produktgruppen anhalten können.

* *[!UICONTROL None]* (Standard): Ändern Sie die vorhandenen Komponenten nicht.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Vorgehensweise mit Zeileneinträgen, die eine Lagerbestandsebene enthalten, wenn:

* (Für Feeds mit nur numerischen Bestandswerten in der angegebenen Spalte) Die Lagerbestände liegen bei oder unter einer angegebenen Menge. Die Standardmenge ist null (0).

* (Für Feeds mit Textwerten in der angegebenen Spalte) Der Wert für [!UICONTROL Availability] is &quot;[!UICONTROL out of stock]&quot;; beim Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden. **Hinweis:** **Geben Sie in Feed-Vorlagen textbasierte Spalten auf Lagerebene mithilfe des Kontrollkästchens für ein[!UICONTROL This column has non-numeric values].&quot;

Wählen Sie die Aktion für beide Fälle aus:

* *[!UICONTROL Delete]* (Standard) Löschen Sie die Komponenten.

* *[!UICONTROL Pause]:* Halten Sie die Komponenten an. Bei der Aktualisierung der Daten werden die Komponenten reaktiviert, wenn die numerischen Lagerwerte über der angegebenen Menge liegen oder wenn die Variable [!UICONTROL Availability] is &quot;[!UICONTROL in stock]&quot; oder &quot;[!UICONTROL preorder]&quot;. Die Komponenten behalten ihren Verlauf und ihre Qualitätsbewertung bei.

Der Lagerbestand für jedes Zeilenelement stammt aus einer Spalte in der Feed-Datei, wie in der[!UICONTROL Stock Level]&quot; für jede Vorlage.

>[!TIP]
>
>* Bei Produkten oder Dienstleistungen, die Sie voraussichtlich neu anbieten oder die Verfügbarkeit erhöhen, sollten Sie Anzeigengruppen, Suchbegriffe und Anzeigen anhalten, anstatt sie zu löschen und neu zu erstellen. Durch Anhalten können sie ihre Qualitätsbewertungen beibehalten.
>* Wenn Sie die veraltete automatische Verarbeitung für Anzeigengruppen aktivieren und neue Daten eine Lagerposition für die Anzeigengruppe enthalten, ist es sinnvoll, die Anzeigengruppe nur dann zu löschen oder anzuhalten, wenn sich die angegebene Lagerbestandsebene auf der Kategorienebene und nicht auf der Marken-/Artikelebene befindet. Wenn Sie beispielsweise über eine Anzeigengruppe &quot;Konvertierungen&quot;verfügen, sollte die Aktienebene für die Anzeigengruppe die Gesamtsumme aller einzelnen konvertierbaren Modelle in der Anzeigengruppe sein.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Werbetreibende, die Datendateien über FTP oder ein Händlernetzwerk-Konto hochladen) Automatisch neue Daten über die entsprechenden Vorlagen übertragen. Die Option ist standardmäßig ausgewählt. Wenn Sie die Option deaktivieren, können Sie weiterhin manuell Daten für jede Feed-Datei, jedes Konto oder für jede Vorlage übertragen.

>[!NOTE]
>
>* Bei FTP-Dateien sucht der Feed-Dienst alle zwei Stunden nach Aktualisierungen im FTP-Verzeichnis (gerade nummerierte Stunden in der PST-Zeitzone). Diese Option verarbeitet alle Dateien, die seit der letzten Prüfung hochgeladen wurden.
>* Bei Handelscenter-Konten synchronisiert sich Search, Social und Commerce täglich um etwa 06:00 Uhr in der Zeitzone des Werbetreibenden mit dem Konto. Diese Option verarbeitet alle Daten, die seit der letzten Synchronisierung aktualisiert wurden.
>* Propagierte Daten sind über das [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten, bis die Daten im Werbenetzwerk oder in der [!UICONTROL Bulksheets] anzeigen.

**[!UICONTROL Post to the SE]:** (Werbetreibende, die Datendateien über FTP oder ein Händlernetzwerk-Konto hochladen) Erstellt automatisch Bulksheet-Dateien in den richtigen Formaten für die relevanten Anzeigennetzwerke, nachdem neue Daten über die entsprechenden Vorlagen übertragen wurden. Mit dieser Option werden auch die Daten aus dem [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten, es sei denn, Unterkomponenten weisen Fehler auf.

Diese Option ist standardmäßig deaktiviert. Um diese Option zu aktivieren, aktivieren Sie das Kontrollkästchen und geben Sie an, ob Bulksheet-Dateien in den Werbenetzwerken veröffentlicht werden sollen:

* *[!UICONTROL Immediately]* (Standardeinstellung): Sendet die Bulk-Sheet-Dateien an die entsprechenden Anzeigenetzwerke, nachdem die Daten über die Vorlagen übertragen wurden. Die Bulksheet-Dateien bleiben im [!UICONTROL Bulksheets] 30 Tage lang anzeigen.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Posten Sie die Bulksheet-Dateien nicht in den relevanten Werbenetzwerken, sondern listen Sie sie in der [!UICONTROL Bulksheets] -Ansicht, aus der Sie sie später posten können. Die Bulksheet-Dateien bleiben im [!UICONTROL Bulksheets] 30 Tage lang anzeigen. Wenn die Bulksheet-Datei größer als 10 MB, aber kleiner als 2 GB ist, liegt die Datei im ZIP-Format vor. Sie müssen die Datei nicht entpacken, um sie zu posten. **Tipp:** Wenn Sie Ihre Landingpages noch nicht validiert haben, verwenden Sie diese Option, damit Sie sie im [!UICONTROL Bulksheets] anzeigen, bevor Sie die Daten in das Werbenetzwerk posten.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Schließt das Posten von Suchbegriff-Wortgruppen mit mehr als einer angegebenen Anzahl von Wörtern in das Werbenetzwerk aus. Wenn diese Option aktiviert ist, werden Suchbegriffe mit mehr als der maximalen Wortanzahl propagiert und im [!UICONTROL Keywords] , aber sie werden nicht veröffentlicht, wenn Sie versuchen, die Daten zu posten.

Diese Option ist standardmäßig deaktiviert, sodass alle Suchbegriffe gepostet werden, unabhängig davon, wie viele Wörter der Satz enthält. Wenn Sie diese Option auswählen, wählen Sie die maximale Anzahl an Wörtern aus, die gepostet werden sollen (von 3 bis 10).

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Feed-Daten über Vorlagen übertragen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
