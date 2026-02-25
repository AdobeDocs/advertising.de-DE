---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Informationen zum Hochladen von Kontodaten für Berichte und Simulationen

<!-- Move all related files into one page? -->

Wenn Sie Online-Werbenetzwerke verwenden, für die Search, Social und Commerce keine API-Unterstützung bereitstellen, können Sie Kampagneninhalte und Offline-Kosten-, Klick- und Konversionsdaten für ein Konto für Reporting- und Leistungssimulationen hochladen. Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md) können auch Daten für ihre Konten in Adobe Analytics anzeigen.

Diese Funktion ist für Werbenetzwerke verfügbar, die der standardmäßigen dreistufigen Kampagnenstruktur entsprechen (Kampagne, Anzeigengruppe oder Anzeigensatz und Gebotseinheit (Anzeige oder Keyword)). Bei Adobe DSP ist die Funktion für Pakete und die einem Paket zugewiesenen Platzierungen verfügbar, jedoch nicht für Kampagnen oder Platzierungen mit Platzierungs-Geschwindigkeit.

Für die folgenden Netzwerke ist vorkonfigurierter Support verfügbar:<!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

Klick-Tracking in Search, Social und Commerce und Konversionstracking in Adobe Advertising werden von dieser Funktion nicht unterstützt.

## Verfügbare Funktionen in Search, Social und Commerce

* Tracking und Reporting:

   * Schreibgeschützte Kampagnenkomponenten bis hinunter zur Ebene der Gebotseinheiten in den Kampagnenverwaltungsansichten.

   * Leistungsdaten bis zur Anzeigengruppenebene <!-- verify the entity level --> in Kampagnenverwaltungsansichten und benutzerdefinierten Berichten. Werbetreibende mit [!DNL Adobe Analytics for Advertising]) erhalten zusätzlich Leistungsdaten auf Anzeigengruppenebene <!-- verify the entity level --> innerhalb der für den Werbetreibenden angegebenen Adobe Analytics Report Suites.&lt;!— Überprüfen, ob die Datentypen begrenzt sind - Kosten, Klick, Anzeige, Impression, Umsatz? —>

* Leistungssimulationen beim Hinzufügen der Kampagnen zu einem Portfolio.<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  Search, Social und Commerce optimieren nichts für diese Kampagnentypen innerhalb eines Portfolios und geben auch keine Angebote dafür ab.

## Workflow zum Einrichten von Offline-Konten

<!-- subtitle wording? -->

1. [Einrichten eines Dummy-Kontodatensatzes](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md).

1. Erstellen Sie eine Datendatei für ein einzelnes Konto<!--  in what file format? --> einschließlich des Status auf Tagesebene für Kampagnen, Anzeigengruppen und Anzeigen.

Die Daten müssen den Datenanforderungen für das Werbenetzwerk entsprechen, sodass die Datenfelder für jede Entität je nach Werbenetzwerk variieren können.

1. <!-- For all ad networks (excluding DSP), -->Laden Sie die Anfangsdaten für ein einzelnes Konto auf eine der folgenden Arten hoch:

* Laden Sie eine Datei manuell von Ihrem Gerät oder Netzwerk hoch.

* Laden Sie die Daten in einen von Search, Social und Commerce zugewiesenen Ordner in einem [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3])-Bucket hoch.

  >[!PREREQUISITES]
  >
  >* Wenden Sie sich an Ihr Adobe-Accountteam , um das Hochladen von Account-Daten für Ihr Search-, Social- und Commerce Advertiser-Konto zu aktivieren. Das Team erleichtert die Erstellung eines organisationsspezifischen Ordners in einem [!DNL S3] Behälter und teilt Ihnen mit, wann er abgeschlossen ist.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* Rufen Sie den [!DNL S3] Cloud-Speicherpfad, die Zugriffsschlüssel-ID und den geheimen Zugriffsschlüssel für Ihr Konto ab. Für alle Datenupload-<!-- naming convention?-->-Konten des Unternehmens werden dieselbe Zugriffsschlüssel-ID und derselbe geheime Zugriffsschlüssel verwendet.

1. Täglich neue Datendateien hochladen.

1. Nachdem Sie Daten für 30 Tage hochgeladen haben, können Sie die Kampagnen optional zu <!--what type? how should we refer to them? --> Portfolios hinzufügen und Simulationen generieren.

Sie können [Protokoll jedes Daten-Uploads anzeigen](upload-log.md) um den Status anzuzeigen. Wenn Sie einen Upload starten, der Upload jedoch nicht vollständig erfolgreich ist, erhalten Sie außerdem eine Fehlerbenachrichtigung über [Benachrichtigungszentrum](/help/search-social-commerce/notifications/notification-about.md), die auf Ihren Benachrichtigungseinstellungen basiert.

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [Informationen zum Hochladen von Kontodaten für Berichte und Simulationen](data-upload-accounts-about.md)
>* [Hochladen von Kontodaten in einen [!DNL Amazon] [!DNL S3] Bucket](upload-data-from-s3-bucket.md)
>* [Kontodaten manuell hochladen](upload-data-manually.md)
>* [Protokoll der hochgeladenen Kontodatendateien anzeigen](upload-log.md)
>* [Verwalten von Anzeigen-Netzwerkkonten für Daten-Uploads](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
