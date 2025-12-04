---
title: Spezifikationen hinzufügen
description: Verweisen Sie auf allgemeine und publisherspezifische Anzeigenspezifikationen.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: a6f9bb2d714e7ddb22f74c9c614772eca30f9e40
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Spezifikationen für unterstützte Anzeigentypen

## Videoanzeigen (Pre-Roll, CTV und Universal Video)

### Unterstützte Screens

Die Werbeanzeigen werden standardmäßig auf Desktop- und Mobilgeräten sowie auf angeschlossenen Fernsehgeräten bereitgestellt. Die Geräte-Zielgruppenbestimmung ist verfügbar, um den Versand anzupassen.

### Unterstützte Werbeserver von Drittanbietern

Sie können Tag-Blätter aus [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] und [!DNL Sizmek] verwenden. Eine vollständige Liste der unterstützten Anbieter finden Sie unter &quot;[&#x200B; Ad Serving Partners](certified-ad-servers.md).

### Voraussetzungen für HD-Video-Assets

**Video-Tag-Typ:** VPAID 2.0 JavaScript oder VAST (CTV). Alle VPAID-Anzeigeneinheiten müssen der [VPAID 2.0-Spezifikation](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) entsprechen, die vom Interactive Advertising Bureau (IAB) definiert wurde.

**Video-Codec:** MP4/H.264

**Auflösung:** 1280x720 für 720p, 1920x1080 für 1080p

**Bitrate:** 1500-2500 kbps für 720p, 2500-3500 kbps für 1080p

**H.264 Profil/Level:** High Profile, Level 3.1 für 720p; High Profile, Level 4.0 für 1080p

**Video-Bildwechselfrequenz:** 29.970 fps (allgemein als 30 fps bezeichnet) für NTSC-Länder, 25 fps für PAL-Länder, 23.976 fps (allgemein als 24 fps bezeichnet) für Film-Look-Inhalte

**Video-Farbraum:** 4:2:0 YUV-Chroma-Unterabtastung

**Video-Interlacing**: Progressives Scanning, d. h. ohne Interlacing. Keine Bewegung innerhalb des Feldes (Blending Frames) oder Interlacing

**Führer (Schiefer):** nicht erlaubt

**Audio-Codec:** AAC-LC oder HE-AACv1

**Audio-Bitrate:** 128-192 kbps für AAC-LC, 64-128 kbps für HE-AACv1

**Audiokanal:** 2-Kanal Stereo-Mix

**Audio-Abtastrate:** 44,1 kHz oder 48 kHz, je nach Ausgangsmaterial

**Audiopegel:** 24 LKFS (+/- 2,0 dB) in den USA gemäß ATSC A/85; 23 LUFS (+/- 1,0) in der EU gemäß EBU R128

#### Zusätzliche Publisher-Anforderungen für Connected TV Ads

* **A+E-Netzwerk:** Siehe A+E-Netzwerk [Anzeigenspezifikationen](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **Discovery:** Siehe die Discovery-[Anzeigenspezifikationen](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **Disney (inkl. Hulu):** Siehe Disneys [Anzeigenspezifikationen](https://www.disneyadvertising.com/mediakit/#specifications).

* **HBO Max:** Siehe HBO Max [Anzeigenspezifikationen](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUniversal:**

   * [Digitales Video](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Pfau](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount:** Siehe Paramount-[Anzeigenspezifikationen](https://www.paramount.com/digital-ads).

## Anzeigen anzeigen

### Unterstützte Screens

Anzeigen werden standardmäßig auf Desktop- und Mobilgeräten bereitgestellt. Die Geräte-Zielgruppenbestimmung ist verfügbar, um den Versand anzupassen.

### Unterstützte Dateitypen

**image:** GIF, JPG/JPEG, PNG

**HTML5:** Bilddateitypen: GIF, JPG/JPEG, PNG, SVG

### Voraussetzungen für Image-Assets

Die universelle Anzeige wird unterstützt.

**Empfohlene Anzeigengrößen:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x600, 320x50, 320x480, 480x60, 640 x 480, 88 x 31, 728 x 90, 970 x 250, 970 x 90

**Unterstützte Werbeserver von Drittanbietern:** Sie können Tag-Blätter von [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] und [!DNL Sizmek] verwenden. Eine vollständige Liste der unterstützten Anbieter finden Sie unter &quot;[&#x200B; Ad Serving Partners](certified-ad-servers.md).

## Audio-Anzeigen

### Unterstützte Screens

Desktop, Mobilgerät, Tablet, Smart-Lautsprecher und Connected TV

### Unterstützte Werbeserver von Drittanbietern

Sie können Tag-Blätter aus [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] und [!DNL Sizmek] verwenden. Eine vollständige Liste der unterstützten Anbieter finden Sie unter &quot;[&#x200B; Ad Serving Partners](certified-ad-servers.md).

### Voraussetzungen für Audio Assets

**Dateityp:** MP3, OGG, AAC

**Führer (Schiefer):** Nicht erlaubt

**Maximale Dateigröße:** 2 MB

**bitrate:** 128

**Dateilänge:** 0-60s

#### Zusätzliche Publisher-Anforderungen

* **[!DNL iHeartRadio]**
   * Länge: 5, 15, 30 oder 60 Sekunden
   * Dateityp: MP3
   * Maximale Dateigröße: 320 Kbit/s
   * Lautstärke: 44,1 kHz

* **[!DNL Pandora]**
   * Länge: 15 oder 30 Sekunden
   * Dateityp: MP4 (In-App), MP3 (Desktop)
   * Maximale Dateigröße: 2,2 MB

* **[!DNL SoundCloud]**
   * Länge: 6, 15 oder 30 Sekunden
   * Dateityp: MP3
   * Maximale Dateigröße: 5 MB

* **[!DNL Spotify]**
   * Länge: Bis zu 30 Sekunden
   * Dateityp: OGG
   * Maximale Dateigröße: 500 MB
   * Volumen: RMS auf -14 normalisiert; dBFS-Peak auf -0,2 dBFS normalisiert

* **[!DNL TargetSpot]**
   * Länge: 15, 30 oder 60 Sekunden
   * Dateityp: MP3

* **[!DNL TuneIn]**
   * Länge: 10, 15 oder 30 Sekunden
   * Dateityp: MP3, OGG
   * Lautstärke: 44,1 kHz

### Voraussetzungen für begleitende Bannerwerbung (optional)

**Unterstützte Größen:** 300x250, 500x500, 640x640, 1024x1024

#### Zusätzliche Publisher-Anforderungen

* **[!DNL iHeartRadio]:**
   * Dateityp: JPEG, JPG, PNG, GIF, SWF, HTML
   * Maximale Dateigröße: 2,2 MB
   * Abmessungen: 300x250

* **[!DNL Pandora]:**
   * Dateityp: JPEG, GIF
   * Maximale Dateigröße: Größe: 100 KB
   * Abmessungen: 300 x 250 (mobil oder Desktop) oder 500 x 500 (Desktop)

* **[!DNL SoundCloud]:**
   * Dateityp: Statischer JPG, PNG
   * Maximale Dateigröße: Unter 400 KB
   * Abmessungen: 1024x1024

* **[!DNL Spotify]:**
   * Dateityp: Statischer JPG, PNG
   * Maximale Dateigröße: 200 KB
   * Abmessungen: 300x250

* **[!DNL TuneIn]:**
   * Dateityp: JPEG, JPG, PNG, GIF, HTML
   * Maximale Dateigröße: 2 MB
   * Abmessungen: 300x250

## Native Display-Anzeigen

Jede Anzeige kann entweder ein Standbild oder einen bewegten GIF (Cinemagraph) enthalten.

### Unterstützte Screens

Anzeigen werden standardmäßig auf Desktop- und Mobilgeräten bereitgestellt. Die Geräte-Zielgruppenbestimmung ist verfügbar, um den Versand anzupassen.

### Assets für alle nativen In-Feed-Formate erforderlich

#### Bild-Asset

**Auflösung:** Minimum 600x600px; Empfohlenes Minimum 1200x627px

**Dateityp:** JPEG (Bild-Ad oder Video-Ad-Cover-Bild), GIF (Cinemograph)

**Dateigröße:** Weniger als 1 MB (Bild sollte textfrei sein.)

#### Advertiser-Logo

**Auflösung:** Minimum 80x80px; Empfohlenes Minimum 300x300px

**Dateityp:** JPEG oder PNG.

**Seitenverhältnis:** 1 x 1

>[!NOTE]
>
>Wählen Sie je nach Bild, über das das Logo gelegt werden soll, zwischen hellen oder dunklen Logo-Assets.

#### Text/Kopie

**Überschrift:** 200 Zeichen; 25 Zeichen empfohlen

**Beschriftung:** maximal 200 Zeichen; 100 Zeichen empfohlen

**Gesponsert von:** Maximal 200 Zeichen; 30 Zeichen empfohlen

**Call to action (nur MoPub):** maximal 15 Zeichen

>[!NOTE]
>
>Das endgültige Layout wird zur Laufzeit vom Publisher definiert. Wenn eine Anzeige die empfohlene Zeichenanzahl überschreitet, müssen einige Inventaranbieter die Anzeige möglicherweise nicht bereitstellen, oder der Publisher oder SSP kann den Text abschneiden.

#### Landingpage-URL

Die Clickthrough-URL mit optionalen Clicktrackern.

Voraussetzungen für Klick-Tracker:

* Impression-Tracking-Pixel von Drittanbietern: Nur 1 x 1 Bild-URL-Format

* Sichtbarkeit JavaScript-Tracker: Wird nur für IAS unterstützt; 1x1-Bilder im JS.append-Format

* Klick-Tracking-Pixel von Drittanbietern: Müssen zur Landingpage weitergeleitet werden, die in der URL eingebettet ist (HTTP 302-Umleitung)

* Clicktracker der Data Management-Plattform (DMP) mit 200 oder mehr Antworten werden nicht unterstützt.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Erstellen Sie mehrere Anzeigen von Drittanbietern](ad-create-multiple.md)
>* [Bearbeiten einer Anzeige](ad-edit.md)
