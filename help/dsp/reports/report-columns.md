---
title: Verfügbare Berichtsspalten
description: Siehe Beschreibungen der verfügbaren Spalten in benutzerdefinierten Berichten.
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: 9eb020f9cb243dc4cf38adbc5af7f723439797d2
workflow-type: tm+mt
source-wordcount: '2467'
ht-degree: 0%

---

# Verfügbare Berichtsspalten

<!-- Add when added:

|[!UICONTROL Dimension]|[!UICONTROL Feed]|[!UICONTROL Deal List]|The name of a user-created deal list for which an ad was shown.|

-->

| Metriktyp | Untertyp | Spaltenname | Beschreibung |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | Die vom externen Anzeigenserver zugewiesene Werbe-ID. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | Die eindeutige Kennung für die Anzeige in DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | Der Name der Anzeige, wie er vom Benutzer zugewiesen wurde. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | Das Format der Anzeige. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | Die Klassifizierung der Anzeige als vom Benutzer geändert oder durch die Datumseingaben gekennzeichnet: *[!UICONTROL live]*, *[!UICONTROL scheduled]*, *[!UICONTROL completed]* oder *[!UICONTROL archived]*. |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | Der Name des Werbetreibenden. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | Das Gesamtbudget, das der Benutzer für die Kampagne zugewiesen hat. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | Das Enddatum der Kampagne. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | Die eindeutige Kennung der Kampagne in DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | Der Name der Kampagne, wie vom Benutzer zugewiesen. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | Das erste Datum für die Kampagne. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Title] | Der Inhalts-/Filmtitel. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Series] | Die Inhaltsreihe. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Genre] | Das Inhalts-Genre. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL ProdQ] | Die Produktionsqualität, wie vom IAB [Technology Laboratory](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md) definiert. Werte können `Unknown`, `Professionally Produced`, `Prosumer` oder `User Generated` sein. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Context] | Die Art des Inhalts, wie vom [IAB Technology Laboratory](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md) definiert. Werte können `Video,` `Game`, `Music`, `Application`, `Text`, `Other` oder `Unknown` sein. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Rating] | Die Inhaltsbewertung, z. B. PG oder R. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Livestream] | Ob die Anzeige in einem Livestream erschien: `Not Live` oder `Live`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Length (in seconds)] | Die Länge des Inhalts in Sekunden; wird normalerweise für Video oder Audio verwendet. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Language (as per ISO 639)] | Die Sprache des Inhalts mit ISO-639-1-alpha-2. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | Jahr, Monat und Tag. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | Tag [!UICONTROL of Week] | Der spezifische Tag, z. B. [!UICONTROL Monday] oder [!UICONTROL Tuesday]. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | Jahr, Monat, Tag und Stunde. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | Monat und Jahr. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | Die Zeit bis zur Stunde, von 0-23. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | Der Datumsbereich für die entsprechende Woche, von Sonntag bis Samstag. Beispiel: 18.02.2021 bis 2021.03.07. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | Der Anbieter des Browsers, in dem die Anzeige angezeigt wurde (z. B. Google oder Mozilla). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | Die Version des Browsers, in dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Safari 4.3] oder [!UICONTROL Chrome 7.0]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | Der Browser, in dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Chrome] oder [!UICONTROL Firefox]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Environment] | Die Geräteumgebungen, auf die sich die Platzierung bezieht: (*[!UICONTROL Desktop]*, *[!UICONTROL Mobile]* und/oder *[!UICONTROL Connected TV])*. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | Der Typ des Geräts, auf dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Set Top Box] oder [!UICONTROL Mobile Phone]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | Der Hersteller des Geräts, auf dem die Anzeige gezeigt wurde (z. B. [!UICONTROL Samsung], [!UICONTROL Lenovo] oder [!UICONTROL Apple]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | Das Modell des Geräts, auf dem die Anzeige angezeigt wurde (z. B. [!UICONTROL iPhone XS] oder [!UICONTROL Galaxy Note 7]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | Der Anbieter des Betriebssystems, auf dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Microsoft] oder [!UICONTROL Apple]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | Die Version des Betriebssystems, auf dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Windows 10] oder [!UICONTROL iOS Mojave]) |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | Das Betriebssystem, auf dem die Anzeige angezeigt wurde (z. B. [!UICONTROL Apple iOS] oder [!UICONTROL Android]). |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Name] | Der vom Benutzer zugewiesene Name für den Abschluss, wie in DSP eingegeben. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Type] | Ob das Geschäft *[!UICONTROL Guaranteed]* oder *[!UICONTROL Non-Guaranteed]* ist. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | Klassifizierung des Bestands: *[!UICONTROL Private],* *[!UICONTROL On Demand],* oder *[!UICONTROL Public]*. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Private Deal ID] | Die eindeutige Kennung, die einem privaten Abschluss über den externen Versorgungspartner zugewiesen wurde. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Publisher] | Der Partner auf der Angebotsseite, der das Inventar bereitstellt. Dies ist normalerweise ein Publisher, kann aber auch ein SSP sein. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | Der angebotsseitige Partner (SSP), dem die Medien zugeordnet werden. |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | Die Häufigkeit, mit der ein Gerät eine Anzeige erhalten hat, basierend auf dem eindeutigen Cookie oder der Geräte-ID. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | Die Stadt, der die gemeldeten Daten zugeordnet sind. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | Das Land, dem die gemeldeten Daten zugeordnet sind. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | Das Designated Market Area (DMA), dem die gemeldeten Daten zugeordnet werden. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Pin Code] | Die PIN-Nummer (Postal Index Number), der die gemeldeten Daten zugeordnet werden. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | Der Status, dem die gemeldeten Daten zugeordnet werden. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | Die Zielgruppe. Der Bericht unterstützt bis zu 10 eindeutige Zielgruppen. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | Die Kampagne. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | Die Länge des Kreativen. Der Bericht unterstützt bis zu 10 einzigartige kreative Längen. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | Das Gerät. Der Bericht unterstützt bis zu 10 eindeutige Geräte. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | Die Art des Feeds. Der Bericht unterstützt bis zu 10 eindeutige Feed-Typen. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | Der Medientyp Der Bericht unterstützt bis zu 10 eindeutige Medientypen. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | Der Publisher. Der Bericht unterstützt bis zu 10 Unique Publishers. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | Das Paket. <!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | Die Platzierung.<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | Die Website oder App, auf der die Anzeigenimpression bereitgestellt wurde. Der Bericht unterstützt bis zu 10 eindeutige Sites oder Apps. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | Das Platzierungs-Tag, das als benutzerdefinierte Kennung für die Platzierung verwendet wird. Der Bericht unterstützt bis zu 10 eindeutige Platzierungs-Tags. <!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Audience] | Die Zielgruppe. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Campaign] | Die Kampagne. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Creative Length] | Die Länge des Kreativen. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Device] | Das Gerät. (wie Videorecorder, Desktop usw.) |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Media Type] | Der Medientyp (wie Display, Audio usw.) |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Publisher] | Der Publisher. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Placement] | Die Platzierung. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Budget] | Das Budget für den Paketflug. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight End Date] | Das Enddatum für den Paketflug. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Rollover] | Jegliches Rollover-Budget für den Paketflug. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Start Date] | Das Startdatum für den Paketflug. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | Das Enddatum für das Paket. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | Der Geschwindigkeits-Zielbetrag für das Paket. Dieser Betrag ist entweder in Ausgaben oder in Impressionen enthalten. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | Die eindeutige Kennung für das Paket in DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | Der Name des Pakets |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | Das Startdatum des Pakets. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | Das Enddatum der Platzierung. |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | (Veraltet) Die Konversions-ID, die von DSP alten [!DNL TubeMogul]-Konversionsereignissen zugewiesen wurde. |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | (Veraltet) Der Konversionsname, der alten [!DNL TubeMogul]-Konversionsereignissen zugewiesen wurde. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | Die eindeutige Kennung der Platzierung in DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | Der Name der Platzierung, wie von der Benutzerin bzw. dem Benutzer zugewiesen. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | Das Platzierungsbudget. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | Das maximale Angebot für die Platzierung. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | Das Enddatum der Platzierung. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | Das Startdatum der Platzierung. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | Das Platzierungs-Tag, das als benutzerdefinierte Kennung für die Platzierung verwendet wird. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | Die Beschreibung, die einem fakturierbaren Segment zugeordnet ist. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | Der eindeutige Schlüssel, der einem fakturierbaren Segment zugeordnet ist. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | Der Name eines fakturierbaren Segments. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | Die Beschreibung, die mit einem Segment verknüpft ist und vom Datenanbieter bereitgestellt wird. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | Der mit einem Segment verknüpfte eindeutige Schlüssel. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | Der Name eines Segments. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | Der Name des mit einem Segment verknüpften Datenanbieters. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | Die eindeutige Kennung für die Site oder die App in DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | Der Name der Site. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Traffic Type] | Ob die Anzeige auf *[!UICONTROL sites]* oder *[!UICONTROL Apps]* angezeigt wurde. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | Die Videolänge, die nach dem Hochladen verarbeitet wird. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | Die eindeutige Kennung für das kreative Video in DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | Der Name des vom Benutzer zugewiesenen Kreativen. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | Die [!UICONTROL App/Site Distinct Uniques] geteilt durch [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | Die Gesamtzahl der Geräte, die nur in dieser App erreicht wurden. Ein Viewer, der für eine Anzeige über mehrere Herausgeber hinweg verfügbar gemacht wird, ist in diesem Wert nicht enthalten. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | Die [!UICONTROL Total Spend] geteilt durch [!UICONTROL App/Site Distinct Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | Die [!UICONTROL Total Spend] geteilt durch [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | Der geschätzte Prozentsatz des Zieluniversums des Haushalts, der eine Exposition erhalten hat. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | Die durchschnittliche Anzahl der Impressionen, die Unique Visitors angezeigt werden. Bei einigen Inventaren geben Herausgeber keine Gerätekennung weiter, und diese Impressionen sind nicht in diesem Wert enthalten. Im [!UICONTROL Frequency (by App/Site)] Bericht gibt es eine ähnliche Metrik, diese wird jedoch nicht geschätzt. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | (Im [!UICONTROL Frequency (by Impression)] Bericht enthalten) Die geschätzten Impressionen für einen bestimmten Häufigkeitsausbruch. DSP-Schätzungen basieren auf einer Stichprobe von Impressions. Bei einigen Inventaren geben Herausgeber keine Gerätekennung weiter, und diese Impressionen sind nicht in diesem Wert enthalten. Im [!UICONTROL Frequency (by App/Site)] Bericht gibt es eine ähnliche Metrik, diese wird jedoch nicht geschätzt. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | (Im [!UICONTROL Frequency (by Impression)] Bericht enthalten) Die Anzahl der eindeutigen Browser oder Geräte, die für eine bestimmte Häufigkeit aufgezeichnet wurden. DSP-Schätzungen basieren auf einer Stichprobe von Impressions. Übergeben Sie für einige Inventare keine Gerätekennung, und diese Impressionen sind in diesem Wert nicht enthalten. Im [!UICONTROL Frequency (by App/Site)] Bericht gibt es eine ähnliche Metrik, diese wird jedoch nicht geschätzt. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | Die Anzahl der Einzelhaushalte, die DSP (Auktionen) innerhalb des Datumsbereichs gesehen hat. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | Die Gesamtzahl der Impressionen, die infolge der Verwendung eines Gerätediagramms für personenbasiertes, geräteübergreifendes Targeting bereitgestellt wurden. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency] | Die Häufigkeit der Impressionen pro Haushalt. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | Die Häufigkeit, mit der Haushalte nur durch die gemeldete Dimension erreicht werden, einschließlich Schnittmengen von bis zu drei Werten für die Dimension. Wenn Sie beispielsweise die Dimension [!UICONTROL Placement] verwenden, können Sie die von einzelnen Platzierungen erreichte Häufigkeit, die von einer Kombination aus zwei beliebigen Platzierungen erreichten Frequenzen und die von Kombinationen aus drei beliebigen Platzierungen erreichten Frequenzen sehen. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | Die Anzahl der Haushalte, die nur von der gemeldeten Dimension erreicht wurden, berechnet als <code>[IP-Adressen, die nur von der gemeldeten Dimension erreicht wurden] - [IP-Adressen, die von einer anderen Dimension erreicht wurden]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | Der Prozentsatz der Haushalte, die nur von der gemeldeten Dimension erreicht wurden, berechnet als <code>[Prozentsatz der IP-Adressen, die von der Dimension erreicht wurden] - [der Prozentsatz der IP-Adressen, die von einer anderen Dimension erreicht wurden]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Impressions] | Die Gesamtzahl der bereitgestellten Ad-Impressions. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | Die Gesamtzahl der bereitgestellten Impressionen, die zur Sichtbarkeit gemessen werden konnten. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | Die Gesamtzahl der messbaren Impressions, die nur von der gemeldeten Dimension bereitgestellt werden, einschließlich Schnittmengen von bis zu drei Werten für die Dimension. Wenn Sie beispielsweise die Dimension [!UICONTROL Placement] verwenden, können Sie die messbaren Impressionen sehen, die von einzelnen Platzierungen erreicht wurden, die messbaren Impressionen, die von einer Kombination aus zwei beliebigen Platzierungen erreicht wurden, und die messbaren Impressionen, die von Kombinationen aus drei beliebigen Platzierungen erreicht wurden. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | Die Gesamtausgaben. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | Die Gesamtzahl der erreichten eindeutigen Haushalte (verschiedene IP-Adressen). |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | Die Gesamtzahl der eindeutigen Haushalte (verschiedene IP-Adressen), die nur von der gemeldeten Dimension erreicht werden, einschließlich Schnittmengen von bis zu drei Werten für die Dimension. Wenn Sie beispielsweise die Dimension [!UICONTROL Placement] verwenden, sehen Sie die eindeutigen Haushalte, die von einzelnen Platzierungen erreicht werden, die gemeinsamen Haushalte, die durch eine Kombination aus zwei beliebigen Platzierungen erreicht werden, und die gemeinsamen Haushalte, die durch Kombinationen aus drei beliebigen Platzierungen erreicht werden. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Incremental HH] | Die Gesamtausgaben, geteilt durch die inkrementellen Haushaltsausgaben, wurden erreicht. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Unique HH] | Die Gesamtausgaben geteilt durch den Einzelhaushalt erreicht. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Frequency] | Die Häufigkeit der Impressionen pro Haushalt. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Incremental Household Reached] | Die Anzahl der Haushalte, die nur von der gemeldeten Dimension erreicht wurden, berechnet als [IP-Adressen, die nur von der gemeldeten Dimension erreicht wurden] - [IP-Adressen, die von einer anderen Dimension erreicht wurden]. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL % Incremental Household Reached] | Der Prozentsatz der Haushalte, die nur von der gemeldeten Dimension erreicht wurden, berechnet als [Prozentsatz der IP-Adressen, die von der Dimension erreicht wurden] - [der Prozentsatz der IP-Adressen, die von einer anderen Dimension erreicht wurden]. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Impressions] | Die Gesamtzahl der bereitgestellten Ad-Impressions. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Measurable Impressions] | Die Gesamtzahl der bereitgestellten Impressionen, die zur Sichtbarkeit gemessen werden konnten. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Total Media Spend] | Die Gesamtausgaben. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Unique Household Reached] | Die Gesamtzahl der erreichten eindeutigen Haushalte (verschiedene IP-Adressen). |
| [!UICONTROL Metrics] | [!UICONTROL Identifier] | [!UICONTROL Identifier Type] | Der Typ der Zielgruppenkennung. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | Der Prozentsatz der gesamten Gebote, die bei der Max. CPM geboten wurden. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | Die durchschnittlichen Bruttokosten pro Akquise, berechnet nach <code>[!UICONTROL Gross Spend] / [!UICONTROL conversion metric]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | Die durchschnittlichen Bruttokosten pro Anzeigenklick, berechnet nach <code>[!UICONTROL Gross Spend]/[!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | Die durchschnittlichen Kosten pro abgeschlossener Videoansicht, berechnet nach <code>[!UICONTROL Gross Spend]/[!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPE] | Die durchschnittlichen Bruttokosten pro Anzeigeninteraktion, berechnet nach <code>[!UICONTROL Gross Spend]/[!UICONTROL Total Ad Engagements]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPI] | Die durchschnittlichen Bruttokosten pro Anzeigenaufruf, berechnet nach <code>[!UICONTROL Gross Spend]/[!UICONTROL Total Ad Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | Die durchschnittlichen Kosten pro 1000 Impressionen, berechnet nach <code>[!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | Die durchschnittlichen Kosten pro Videoansicht, berechnet nach <code>[!UICONTROL Gross Spend]/[!UICONTROL Views]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross Custom Goal CPA] | Die <code>[!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>, wobei [!UICONTROL Custom Goal] die Zielgewichtung für alle Konversionen ist, die an das benutzerdefinierte Ziel angehängt sind. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | Die durchschnittlichen Kosten pro 1000 sichtbaren Impressions, berechnet nach <code>[!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | Die durchschnittlichen Nettokosten pro Anzeigenklick, berechnet nach <code>[!UICONTROL Net Spend]/[!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | Die durchschnittlichen Nettokosten pro abgeschlossener Videoansicht, berechnet nach <code>[!UICONTROL Net Spend]/[!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPI] | Die durchschnittlichen Nettokosten pro Anzeigenaufruf, berechnet nach <code>[!UICONTROL Net Spend]/[!UICONTROL Total Ad Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | Die durchschnittlichen Nettokosten pro 1000 Impressionen, berechnet nach <code>[!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | Die durchschnittlichen Nettokosten pro Videoansicht, berechnet nach <code>[!UICONTROL Net Spend]/[!UICONTROL Views]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net vCPM] | Die durchschnittlichen Nettokosten pro 1000 sichtbaren Impressions, berechnet nach <code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | Die Anzahl der eindeutigen Benutzer, für die DSP ein Angebot für die Platzierung abgegeben hat. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Agency Fee] | Die Servicegebühr der Agentur. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Creative Spend] | Die Gesamtausgaben für von Adobe Creative bereitgestellte Anzeigen. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Data Spend] | Die gesamten Nettokosten der über DSP in Rechnung gestellten Zielgruppensegmentdatengebühren. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Media Spend] | Die gesamten Nettokosten abrechenbarer Medien, einschließlich der Technologiegebühr, die über DSP in Rechnung gestellt werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Other Spend] | Die Gesamtkosten für andere Servicegebühren (Verifizierungspartner von Drittanbietern, Anzeigenbestellung usw.), die über DSP in Rechnung gestellt werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Creative] | Die veranschlagte Steuer auf Werbeanzeigen, die von Adobe Creative geliefert werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | Die geschätzte Steuer auf Zielgruppensegmente und Daten-Services von Drittanbietern. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | Die veranschlagte Mediensteuer inklusive Steuern, die auf Medienkostenabrechnungs- und Technologiegebührendienste in DSP erhoben wird. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | Die geschätzte Steuer auf andere Service-Gebühren (einschließlich Verifizierungspartner von Drittanbietern, Themen-Targeting usw.), die über DSP in Rechnung gestellt wird. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Gross Spend] | Die Bruttoausgaben. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Margin %] | (Wenn die Margin-Verwaltung aktiviert ist) Der Prozentsatz der Margin, der durch <code>([!UICONTROL Gross Spend] - [!UICONTROL Net Spend]) / [!UICONTROL Gross Spend] berechnet wird</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | Die Summe der nicht fakturierbaren und fakturierbaren Medienkosten ohne technische Gebühren. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | Die durchschnittlichen Nettokosten pro 1000 sichtbaren Impressions, berechnet nach <code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non Billable Creative Spend] | Die Gesamtausgaben für Anzeigen, die nicht über Adobe Creative in Rechnung gestellt werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Spend] | Die Nettogesamtkosten der Zielgruppensegmentdatengebühren, die nicht über DSP in Rechnung gestellt werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Spend] | Die gesamten Nettokosten nicht abrechnungsfähiger Medien, einschließlich der Technologiegebühr, die nicht über DSP in Rechnung gestellt werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | Die Gesamtkosten für andere Service-Gebühren (Verifizierungspartner von Drittanbietern, Anzeigenbestellung usw.), die nicht über DSP in Rechnung gestellt werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Billable Spend] | Die Summe aus [!UICONTROL Billable Spend (Media)], [!UICONTROL Billable Spend (Data)] und [!UICONTROL Billable Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative CPM] | Die durchschnittlichen Nettomedienkosten pro 1000 Impressionen für Anzeigen, die von Adobe Creative bereitgestellt werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative Spend] | Die gesamten fakturierbaren und nicht fakturierbaren Ausgaben für Anzeigen, die von Adobe Creative bereitgestellt werden. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data eCPM] | Die durchschnittlichen Nettodatenkosten pro 1000 Impressionen, berechnet durch <code>[!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data Spend] | Die gesamten Nettokosten der Daten-Feeds für Zielgruppensegmente. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media CPM] | Die durchschnittlichen Nettomedienkosten pro 1000 Impressionen, berechnet nach <code>[!UICONTROL Net Spend (Media)]/[!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media Spend] | Die gesamten Nettokosten der Medien, einschließlich technischer Gebühren. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | Die Summe aus [!UICONTROL Net Spend (Media)], [!UICONTROL Net Spend (Data)] und [!UICONTROL Net Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | Die Summe aus [!UICONTROL Non-billable Spend (Media)], [!UICONTROL Non-billable Spend (Data)] und [!UICONTROL Non-billable Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other eCPM] | Die durchschnittlichen Nettokosten pro 1000 Impressionen für andere Gebühren, berechnet nach <code>[!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other Spend] | Die gesamten Nettokosten anderer Service-Gebühren (Verifizierungspartner von Drittanbietern, Anzeigenschaltung usw.). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | Der Prozentsatz der Ansichten, die die Anzeige insgesamt angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | Die Anzahl der Ansichten, die die gesamte Anzeige angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | Der Prozentsatz der anzeigbaren Impressionen, die die Anzeige insgesamt angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | Der Prozentsatz der Ansichten, die mindestens ein Viertel der Anzeige angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | Die Anzahl der Ansichten, die mindestens ein Viertel der Anzeige angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | Der Prozentsatz der Ansichten, die mindestens zwei Viertel der Anzeige angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | Die Anzahl der Ansichten, die mindestens zwei Viertel der Anzeige angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | Der Prozentsatz der sichtbaren Impressionen, die mindestens zwei Viertel der Anzeige gesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | Der Prozentsatz der Ansichten, die mindestens drei Viertel der Anzeige angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | Die Anzahl der Ansichten, die mindestens drei Viertel der Anzeige angesehen haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | Der durchschnittliche Prozentsatz, um den eine Anzeige bis zum Abschluss angesehen wurde, wobei alle Ansichten berücksichtigt wurden. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | Die Anzahl der Klicks auf die Anzeigenüberlagerung und die Banner. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | Der Prozentsatz der Klicks dividiert durch die Anzeigenimpressionen. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | Der Prozentsatz der Klicks dividiert durch die Videoansichten. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | Die Anzahl der Klicks auf Begleitbanner. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | Der Prozentsatz der Klicks dividiert durch die Impressionen der Begleitbanner. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | Die Anzahl der Banner-Impressions der Gegenstelle. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | Die Art der Internetverbindung, die für die Anzeige verwendet wurde (z. B. WiFi oder 4G LTE). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | Die Anzahl der Interaktionen auf einer geschalteten Anzeige. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | Die Gesamtzahl der Anzeigen-Impressions. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | Der Prozentsatz der bereitgestellten Impressionen, die zu Videoansichten geführt haben. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | Die durchschnittliche Dauer einer Videoansicht in Sekunden. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | Die Summe aller Klicks auf eine Anzeige. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | Die Gesamtzahl der Minuten, die eine Videoanzeige angesehen wurde. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | Die Gesamtzahl der Video-Anzeigenansichten. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | Die durchschnittliche Breite und Höhe des Spielers. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | Die Gesamtzahl der bereitgestellten Impressionen, die zur Sichtbarkeit gemessen werden konnten. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | Der Prozentsatz der erzielten Impressionen, die hinsichtlich der Sichtbarkeit gemessen werden konnten, berechnet als <code>[!UICONTROL Measurable Impressions] x 1000 / [!UICONTROL Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | Der Prozentsatz der Impressionen, die aufgrund inkompatibler iFrames nicht für die Sichtbarkeit messbar sind. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | Die Anzahl der Impressionen, die aufgrund eines nicht unterstützten Sichtbarkeits-Trackings auf der Anzeigeneinheit nicht für die Sichtbarkeit messbar sind. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | Der Prozentsatz der Impressionen, die aus anderen Gründen für die Sichtbarkeit nicht messbar sind. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | Die Anzahl der Ad-Impressions, die für die Sichtbarkeit nicht messbar sind. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | Der Prozentsatz der Anzeigenimpressionen, deren Sichtbarkeit nicht gemessen werden kann. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | Der Prozentsatz der Impressionen, die aufgrund eines nicht unterstützten Sichtbarkeits-Trackings auf dieser Anzeigeeinheit nicht für die Sichtbarkeit messbar sind. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | Der Prozentsatz der sichtbaren Impressions aus allen messbaren Impressions, berechnet als <code>[!UICONTROL Viewable Impressions]/[!UICONTROL Measurable Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | Die Anzahl der als anzeigbar angesehenen Anzeigen-Impressions. |
| [!UICONTROL Conversion Metrics] | [Gruppiert nach Advertiser in den Berichteinstellungen] | [Advertiser-spezifische Konversion] | Die Gesamtsumme für eine bestimmte Advertiser-spezifische Konversionsmetrik oder ein Adobe Analytics-Ereignis. |
| [!UICONTROL Custom Goals] | [Gruppiert nach Advertiser in den Berichteinstellungen] | [Advertiser-spezifisches benutzerdefiniertes Ziel] | Die gewichtete Summe aller Konversionen, die im angegebenen [&#x200B; enthalten sind](/help/dsp/optimization/custom-goal.md). |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Erstellen eines benutzerdefinierten Berichts](/help/dsp/reports/report-create.md)
>* [Duplizieren eines benutzerdefinierten Berichts](/help/dsp/reports/report-copy.md)
>* [Benutzerdefinierten Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
