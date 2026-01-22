---
title: Über Ihre Kreativbibliotheken
description: Erfahren Sie mehr über die Verwaltung der Kreativen für Ihre Anzeigenerlebnisse.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 8d549853be10ebfbb71b14e013b04178466e87fe
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# Über Ihre Kreativbibliotheken

Mit Ihren Kreativ-Bibliotheken können Sie die Kreativen verwalten, die Sie in Ihren Werberlebnissen verwenden werden. Sie können mehrere Bibliotheken mit jeweils einer Reihe von Kreativen und *Kreativ-Bundles* erstellen, bei denen es sich um Kreativgruppen handelt, die Sie einem Erlebnis als eine Einheit hinzufügen können.

Ihre Bibliotheken können Folgendes enthalten:

* **Individuelle Kreative:** Sie können einzelne Kreative direkt in Anzeigenerlebnisse einbeziehen, für die keine Benutzerziele definiert sind. Sie können Ihre Kreativen auch verwenden, um Bundles zu erstellen, die Sie in zielgerichtete ([) Erlebnisse ](/help/creative/experiences/experience-about.md) können.

   * **Standard-Kreative** Sie können Kreative in [verschiedenen Formaten) hochladen ](#creative-creative-formats) verwalten. Geben Sie für jeden Kreativen die Standardsprache für jede Anzeige an, mit der Sie das Kreative verknüpfen, sowie die Standardlandingpage, die geöffnet wird, wenn ein Benutzer auf eine Anzeige klickt, die das Kreative enthält. Sie können optional Beschriftungen angeben, die als Filter in verschiedenen Ansichten innerhalb von [!DNL Creative] und als Spaltenwerte im [!UICONTROL Custom Creative Report] verwendet werden sollen, wenn Sie die Verwendung der [!UICONTROL Creative Label] Dimension einbeziehen.

   * **Dynamische Kreative:** Sie können dynamisch generierte Kreative erstellen, indem Sie dynamische Variablen in einer Anzeigenvorlage den Werten in einer Feed-Datei zuordnen. Alle Benutzer können vorhandene dynamische Anzeigen in der Vorschau anzeigen, duplizieren und löschen.

* **Kreativ-Bundles:** Kreative in Bundles zusammen, die für mehrere Erlebnisse mit definierten Benutzerzielen verwendet werden können. Sie können *Standard-Display* Bundles erstellen, die aus Standard-Display-Anzeigen, *Standard-Video-Bundles* die aus Standard-Video-Anzeigen bestehen, und *Dynamische Display-Bundles* die aus dynamisch generierten Display-Anzeigen bestehen.

## Unterstützte Creative-Formate {#creative-creative-formats}

### Formate für Standard-Kreative

Sie können die folgenden Kreativtypen in den [unterstützten Kreativgrößen“ hinzufügen und ](creative-sizes.md).

>[!IMPORTANT]
>
>* Selbst wenn Sie beabsichtigen, HTML5, Flexible HTML5 oder Kreative von Drittanbietern für Ihre standardmäßigen Display-Anzeigenerlebnisse zu verwenden, müssen Sie für jede verwendete Kreativgröße auch Image-Kreative hinzufügen.
>* Für jedes standardmäßige Anzeigeerlebnis ist ein Standardbild erforderlich, das für jede dem Erlebnis zugewiesene Kreativgröße erstellt wird. Die Standardbildkreative werden verwendet, wenn ein Browser nicht JavaScript-fähig ist oder wenn der Anzeigenserver die Anzeige aufgrund von Verzögerungen nicht personalisieren kann.
>* Für jedes Standard-Videoerlebnis ist ein Standardvideo für jede dem Erlebnis zugewiesene kreative Dauer erforderlich.<!-- when is it used? -->

#### Flexible HTML5

Flexible HTML5-Kreative sind HTML5-Kreative mit allen Bildern und anderen Attributen als standardmäßige HTML-Tags, die Sie direkt in [!DNL Creative] bearbeiten können, entweder in einer Kreativbibliothek oder in einem individuellen Erlebnis (wodurch eine Variation des ursprünglichen Kreativen erstellt wird). In DSP sind flexible HTML5-Kreative für eine einzelne bestimmte Anzeigengröße (in Pixel) vorgesehen. Sie können optional die Standardwerte der Attribute ändern, die in einem flexiblen HTML5-Creative angegeben sind. Später können Sie benutzerdefinierte Werte für die Attribute innerhalb eines bestimmten Erlebnisses angeben, wodurch eine Variante des übergeordneten kreativen Elements erstellt wird.

Sie können flexible HTML5-Kreative entweder als ZIP-Dateien hochladen oder eine der Ihrem Konto zur Verfügung stehenden Vorlagen als Ausgangspunkt verwenden. Siehe [Spezifikationen für flexible HTML5-Kreative](html5-creative-specification.md).

#### Kreative für Standardbildschirme

Zu den Standard-Display-Anzeigen gehören:

* HTML5-Kreative lokal oder aus Adobe GenStudio for Performance Marketing hochgeladen.
* Bilddateien, lokal oder von Adobe Experience Manager hochgeladen.

##### HTML5-Kreative

* **GenStudio-Erlebnisse:** Sie können alle Anzeigenvarianten aus einem [Anzeigen-Erlebnis](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/display-ad-experiences) in [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) as a HTML5 Creative importieren. Externe Links werden in lokale Referenzen konvertiert. Der HTML-Inhalt kann bis zu 20 MB groß sein, und Einzelbilder können bis zu 50 MB groß sein.

  Nachdem Sie ein GenStudio-Erlebnis importiert haben, können Sie die Metadaten (Name, Sprache, Tags) für die importierten kreativen, nicht jedoch für die kreativen Inhalte bearbeiten. Wenn Sie das GenStudio-Erlebnis in GenStudio bearbeiten, importieren Sie das Erlebnis in [!DNL Creative] erneut, um die neueste Version zu verwenden.

  >[!NOTE]
  >
  >Um diese Funktion verwenden zu können, müssen sowohl das GenStudio- als auch das Advertising Creative-Konto dieselbe Organisations-ID verwenden. Außerdem muss der Anwender über die Berechtigungen für den Zugriff auf GenStudio verfügen.

* **Hochgeladene Dateien:** Sie können auch einfache oder statische HTML5-Kreative mit allen angegebenen Attributen und Bildern als ZIP-Dateien hochladen. Sie können keine Attribute bearbeiten oder Bilder hinzufügen. Laden Sie stattdessen eine neue ZIP-Datei hoch, um ein neues Kreativprofil hinzuzufügen. Siehe [Spezifikationen für einfache und statische HTML5-Kreative](html5-creative-specification.md).

##### Image-Kreative

Sie können Bildkreative im GIF-, JPEG-, JPG- oder PNG-Format einbeziehen. Sie können genehmigte Bilder von Ihren Adobe Experience Manager-Konten oder Bilder von Ihrem Gerät oder Netzwerk hochladen.

Für jedes standardmäßige Display- und Erlebniserlebnis ist ein Standardbild für jede dem Erlebnis zugewiesene Kreativgröße erforderlich.

#### Kreative von Drittanbietern

Geben Sie JavaScript-Tracking-Tags für Kreative ein, die auf Werbe-Servern von Drittanbietern gehostet werden. Das Skript variiert je nach Anzeigenserver. Das folgende Beispiel:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### Video-Kreative {#creative-video-specs}

Sie können Erstanbieter-Videokreative für Web-, Mobil- oder vernetztes Fernsehen von Ihrem Gerät oder Netzwerk hochladen. Für jedes Standard-Video- und -Erlebnis ist für jede dem Erlebnis zugewiesene kreative Dauer ein Standard-Kreativvideo erforderlich. DSP transkodiert alle Videokreativen automatisch als VAST 2.0-Tags, damit Sie eine Vorschau davon anzeigen können. In [!UICONTROL Tag Manager] können Sie optional [DSP-spezifische Transkodierung](/help/creative/experiences/experience-tag-video-transcoding.md) auf jedes Video- und Erlebnis-Tag anwenden.

Siehe folgendes Video: Creative Requirements. **Hinweis:** Wenn Sie Videoerlebnisse in Advertising DSP hochladen, lesen Sie auch den Abschnitt [Voraussetzungen für High-Definition-Video-Assets](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets) von DSP, der möglicherweise eingeschränkter ist.

**Dateityp:** .mov, .mp4, .webm

**Dateigröße:** Maximal 512 MB

**Seitenverhältnis des Videos:** 16:9, 4:3

**Videoauflösung:** 640x360 für 360p, 1280x720 für 720p, 1920x1080 für 1080p

**Videolänge:** Maximal 90 Sekunden

**Bitrate:** 600-1200 kbps für 360p, 1500-2500 kbps für 720p, 3000-5000+ kbps für 1080p

**Video-Bildwechselfrequenz:** 23,98 Bilder/s. Zusätzliche Frameraten können je nach regionalen oder Publisher-Anforderungen akzeptiert werden

**Video-Codec:** H.264 (Industriestandard), AV1, H.265

**Audioformat:** ACC (Industriestandard/MP4), Opus (WebM/AV1)

**Audio-Bitrate:** 16-512 kBit/s

**Audio-Abtastrate:** 44100-48000 Hz

**Audiorate:** 44,1 kHz oder 48 kHz

**Sonstiges Audio** Die hochgeladene Datei darf nicht verschachtelt und gemischt sein und eine Audiospur enthalten. Möglicherweise ist kein Ton vorhanden, aber die Videodatei muss eine Audiospur enthalten.

### Format für dynamische Anzeigen

Sie können Kreative dynamisch im statischen HTML5- und dynamischen HTML5-Format generieren, indem Sie dynamische Variablen in einer Anzeigenvorlage den Werten in einer Feed-Datei zuordnen. Zu den dynamischen Kreativen können Kreative gehören, die aus Ihren veralteten Adobe Advertising Dynamic Creative Optimization (DCO)-Erlebnissen migriert wurden.

## Die [!UICONTROL Creative Libraries]

Weitere [ zum Anpassen der einzelnen Ansichten finden ](/help/creative/introduction/customize-data-views.md) unter „Anpassen der Datenansichten“.

### Die [!UICONTROL Creative Libraries] Hauptansicht

Die [!UICONTROL Creative Libraries] Hauptansicht zeigt alle Ihre Kreativbibliotheken an. Die Daten für jede Bibliothek umfassen die Anzahl der Erlebnisse, denen die Bundles der Bibliothek zugewiesen sind, die Anzahl der Bundles, die Anzahl der Kreativen, die Anzahl der kreativen Größen, die Anzahl der Standardsprachziele, das Erstellungsdatum und das letzte Änderungsdatum für ein Element der Bibliothek. Der Tabellenmodus enthält auch eine Spalte für den Advertiser.

Wenn Sie sich im Kartenmodus befinden, können Sie mithilfe der Schaltflächen &lt; und > mit mehreren Kreativen durch die Bilder in einer Bibliothek scrollen.

#### Verfügbare Aktionen

* [Neue Bibliothek erstellen](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* Für jede Kreativbibliothek gilt Folgendes:

   * [Bearbeiten eines Bibliotheksnamens](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Eine Bibliothek öffnen, um die der Bibliothek zugewiesenen Kreativen und Bundles anzuzeigen](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [Bibliotheken löschen](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### Die [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

Auf der Registerkarte [!UICONTROL Standard Ads] werden alle von Ihnen erstellten Standard-Kreativen angezeigt. Die Daten für jeden Kreativen umfassen die Kreativgröße, den Kreativtyp und das Erstellungsdatum. Der Tabellenmodus enthält auch Spalten für die Standardsprache und die standardmäßige Landingpage.

##### Verfügbare Aktionen

* [Hinzufügen von Standard-Kreativen zu einer Bibliothek](creative-add-standard.md)

* [Bearbeiten von Standard-Kreativen](creative-edit-standard.md)

* [Vorschau eines Standard-Kreativen anzeigen](creative-preview.md)

* [Standard-Kreative zu Standard-Display-Bundles hinzufügen und Standard-Kreative aus einem Standard-Display-Bundle entfernen](creative-attach-detach-bundles.md)

* [Hinzufügen von Videokreativen zu Standard-Videopaketen und Entfernen von Videokreativen aus einem Standard-Videopaket](creative-attach-detach-bundles.md)

* [Standardkreative duplizieren](creative-duplicate.md)

* [Standard-Kreative herunterladen](creative-download.md)

* [Standard-Kreative löschen](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

Auf der Registerkarte [!UICONTROL Dynamic Ads] werden alle dynamischen Kreativen angezeigt, die dynamisch für Ihre Kreativkataloge erstellt wurden, mit Ausnahme der dynamischen Kreativen, die Sie [ der Registerkarte ](creative-delete.md) manuell [!UICONTROL Dynamic Ads] haben. Wenn Sie [manuell dupliziert](creative-duplicate.md) beliebige dynamische Kreative <!-- I don't think existing ads are deletd via feeds, so this probably isn't true: since a catalog was last processed -->, enthält die Liste der Kreativen für diesen Katalog auch die doppelten Kreativen.

Die Daten für jedes Kreativ umfassen den Kreativtyp, die Größe des Kreativs, die Anzahl der Kataloge, zu denen das Kreativ gehört, und das Erstellungsdatum. Der Tabellenmodus enthält auch Spalten für die Anzeigenvorlage, über die die kreative Seite generiert wurde, und die Anzahl der Angebote.

>[!NOTE]
>
>Bei jeder Verarbeitung eines Katalogs werden die Daten der vorhandenen dynamischen Kreativen für diesen Katalog aktualisiert.<!-- Verify this!!! And is there anything more to say w/regard to  -->

##### Verfügbare Aktionen

* [Hinzufügen dynamischer Kreativer zu einer Bibliothek](creative-add-dynamic.md)

* [Bearbeiten eines dynamischen Kreativen](creative-edit-dynamic.md)

* [Vorschau für dynamische Kreative](creative-preview.md)

* [Fügen Sie dynamische Kreative zu dynamischen Display-Bundles hinzu und entfernen Sie dynamische Kreative aus einem dynamischen Display-Bundle](creative-attach-detach-bundles.md)

* [Dynamische Kreative duplizieren](creative-duplicate.md)

* [Dynamische Kreative löschen](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### Die Ansicht [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

Die [!UICONTROL Bundles] zeigt alle standardmäßigen und dynamischen Bundle-Container an. Sie können die Kreativnamen, die Kreativgrößen und die Sprachen der in den einzelnen Bundles enthaltenen Kreativen anzeigen. Wenn Sie sich im Kartenmodus befinden, können Sie mithilfe der Schaltflächen &lt; und > mit mehreren Kreativen durch die Bilder in einem Paket scrollen.

#### Verfügbare Aktionen

* Hinzufügen von Bundles mit Standardbildschirmen, Standardvideos und dynamischen Anzeigen zu einer Bibliothek

* Auflisten und Vorschau der Kreativen in einem Bundle

* Bundle-Namen bearbeiten

* Fügen Sie Standarddarstellungskreative zu Standarddarstellungspaketen hinzu und entfernen Sie Standarddarstellungskreative aus einem Standarddarstellungspaket

* Hinzufügen von Standard-Video-Kreativen zu Standard-Video-Bundles und Entfernen von Standard-Video-Kreativen aus einem Standard-Video-Bundle

* Bundles duplizieren

* Bundles löschen

>[!MORELIKETHIS]
>
>* [Verwalten von Kreativbibliotheken](/help/creative/creative-libraries/creative-library-manage.md)
>* [Standard-Kreative zu einer Kreativbibliothek hinzufügen](creative-add-standard.md)
>* [Verwalten von kreativen Bundles](bundle-manage.md)
>* [Anpassen der Datenansichten](/help/creative/introduction/customize-data-views.md)
