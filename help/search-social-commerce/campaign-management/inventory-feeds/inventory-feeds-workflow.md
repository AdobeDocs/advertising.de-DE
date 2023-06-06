---
title: Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds
description: Erfahren Sie mehr über den Workflow zur automatischen Verwaltung der Kontostruktur und Bereitstellung dynamischer Anzeigen basierend auf Daten zu Ihrem Produkt- oder Service-Inventar.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Workflow für die Verwaltung von Kampagnendaten mithilfe von Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Testen Sie zunächst mindestens eine Feed-Datei oder ein Konto und dann können Sie den Prozess vollständig automatisieren oder ihn bei jedem Schritt weiter steuern:

1. (Optional) Wenden Sie sich an Ihr Adobe Account Team, um ein FTP-Verzeichnis für die Speicherung von Datendateien einzurichten.

   Wenn Sie den FTP-Ordner verwenden, sucht der Feed-Dienst alle zwei Stunden nach neuen Dateien.

   Andernfalls können Sie Dateien manuell im [!UICONTROL Advanced (ACM)] anzeigen.

1. Satz [Parameter für die Verarbeitung von Feed-Daten](feed-settings-manage.md#feed-data-settings).

   Wenn Sie FTP verwenden, veröffentlichen Sie anfangs nicht automatisch Daten in den Werbenetzwerken. Nachdem Sie die Ausgabe aus der ersten Datei überprüft haben und mit den Ergebnissen zufrieden sind, können Sie die Einstellungen ändern.

1. Hochladen einer Datendatei in das FTP-Verzeichnis, [manuell eine Datendatei hochladen](feed-files-manage.md) im [!UICONTROL Advanced (ACM) view]oder [Zugriff auf ein Google- oder Microsoft®-Merchant-Center-Konto aktivieren](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Um Dateien manuell hochzuladen, können Sie warten, bis Sie eine Vorlage erstellen, die die Datendatei verwendet.

1. (Optional) Erstellen Sie Gruppen von [modifiers](modifiers-manage.md) zur Verwendung als Variablen in verschiedenen Datenfeldern in Feed-Datenvorlagen.

1. [Erstellen einer oder mehrerer Vorlagen](ad-templates/ad-template-manage.md) die die Datenspalten verwenden, um Kampagnen, Anzeigengruppen, Suchbegriffe und/oder Anzeigenkopien für ein bestimmtes Anzeigennetzwerkkonto zu erstellen.

1. [Übertragen von Feed-Daten über die Vorlagen](feed-data-propagate.md), der die Spaltennamen in der Vorlage durch Daten in der Datei oder dem Konto ersetzt. Abhängig von den Vorlagenoptionen erstellt Search, Social und Commerce entweder eine neue Kontostruktur (Kampagnen, Anzeigengruppen, Suchbegriffe) für die Anzeigen mit Standardeinstellungen oder ordnet die Anzeigen der vorhandenen Kontostruktur zu.

1. (Optional) [Vorschau der Ausgabe anzeigen](propagated-data-view.md) im [!UICONTROL Advanced (ACM)] Ansichten und optional eine Zusammenfassung der Datenänderungen auf der [!UICONTROL Propagations] Registerkarte.

1. [Posten der Daten](propagated-data-post.md) zu den entsprechenden Anzeigennetzkonten hinzugefügt.

1. (Wenn Sie zum Hochladen Ihrer Daten FTP oder ein Händlercenter-Konto verwenden; (optional) Nachdem Sie die Ausgabe aus der ersten Feed-Datei validiert haben, [Parameter bearbeiten](feed-settings-manage.md#feed-data-settings) um nachfolgende Daten automatisch über die verknüpften Vorlagen zu übertragen und an die entsprechenden Werbenetzwerke zu posten.

1. (Wenn Sie neue Datendateien haben) Laden Sie bei Bedarf neue Dateien hoch, propagieren Sie die Daten über Vorlagen und posten Sie die Daten in das relevante Anzeigennetzwerk. Sie können die Daten optional in einem Schritt propagieren und posten.

>[!MORELIKETHIS]
>
>* [Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds](inventory-feeds-about.md)
>* [Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?](when-are-components-created-deleted.md)

