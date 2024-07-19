---
title: Anzeigenspezifikationen
description: Verweisen Sie auf allgemeine und Publisher-spezifische Anzeigenspezifikationen.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Spezifikationen für unterstützte Anzeigentypen

## Videoanzeigen (Pre-Roll, CTV und universelle Videos)

### Unterstützte Screens

Anzeigen werden standardmäßig auf Desktop-, Mobil- und vernetzten TV-Geräten bereitgestellt. Die Zielgruppenbestimmung für Geräte ist verfügbar, um die Bereitstellung anzupassen.

### Unterstützte Drittanbieter-Anzeigenserver

Sie können Tag-Tabellen aus [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] und [!DNL Sizmek] verwenden. Eine vollständige Liste der unterstützten Anbieter finden Sie unter &quot;[Zertifizierte Ad Serving Partners](certified-ad-servers.md)&quot;.

### Anforderungen an Assets für hochauflösende Videos (erforderlich)

**Video-Tag-Typ:** VPAID 2.0 JavaScript oder VAST (CTV). Alle VPAID-Anzeigeneinheiten müssen der [VPAID 2.0-Spezifikation](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) entsprechen, wie vom Interactive Advertising Bureau (IAB) definiert.

**Video-Codec:** MP4/H.264

**Auflösung:** 1280x720 für 720p, 1920x1080 für 1080p

**Bitrate:** 1500-2500 kBit/s für 720p, 2500-3500 kBit/s für 1080p

**H.264 Profil/Level:** Hohes Profil, Level 3.1 für 720p; High Profile, Level 4.0 für 1080p

**Video-Framerate:** 29,970 fps (allgemein als 30 fps bezeichnet) für NTSC-Länder, 25 fps für PAL-Länder, 23,976 fps (allgemein als 24 fps bezeichnet) für Film-Look-Inhalte

**Videofarbraum:** 4:2:0 YUV-Chroma-Subsampling

**Video Interlacing:** Progressives Scannen, d. h. ohne Zeilensprung. Keine Bewegung innerhalb des Felds (Mischrahmen) oder Zwischenzeilenanzeige.

**Kopfzeilen (Split):** Nicht zulässig

**Audio-Codec:** AAC-LC oder HE-AACv1

**Audio-Bitrate:** 128-192 kBit/s für AAC-LC, 64-128 kBit/s für HE-AACv1

**Audiokanal:** 2-Kanal-Stereo-Mix

**Audio-Probenrate:** 44,1 kHz oder 48 kHz, bezogen auf das Quellmaterial

**Audiopegel:** 24 LKFS (+/- 2,0 dB) in den USA gemäß ATSC A/85; 23 LUFS (+/- 1,0) in der EU gemäß EBU R128

#### Zusätzliche Anforderungen an Publisher für vernetzte TV-Anzeigen

* **A+E-Netzwerk:** Siehe die [Anzeigenspezifikationen des A+E-Netzwerks](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **Erkennung:** Siehe die [Anzeigenspezifikationen der Erkennung](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **Disney (einschl. Hulu):** Siehe [Anzeigenspezifikationen von Disney](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max:** Siehe [Anzeigenspezifikationen von HBO Max](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUniversal:**

   * [Digitales Video](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Pfau](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount:** Siehe die [Anzeigenspezifikationen des Paramount](https://www.paramount.com/digital-ads).

## Display-Anzeigen

### Unterstützte Screens

Anzeigen werden standardmäßig auf Desktop- und Mobilgeräten bereitgestellt. Die Zielgruppenbestimmung für Geräte ist verfügbar, um die Bereitstellung anzupassen.

### Unterstützte Dateitypen

**Bild:** GIF, JPG/JPEG, PNG

**HTML5:** Bilddateitypen: GIF, JPG/JPEG, PNG, SVG

### Voraussetzungen für Image Assets (erforderlich)

Universelle Anzeige wird unterstützt.

**Empfohlene Anzeigengrößen:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x600, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x 90

**Unterstützte Drittanbieter-Anzeigenserver:** Sie können Tag-Tabellen von [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] und [!DNL Sizmek] verwenden. Eine vollständige Liste der unterstützten Anbieter finden Sie unter &quot;[Zertifizierte Ad Serving Partners](certified-ad-servers.md)&quot;.

## Audioanzeigen

### Unterstützte Screens

Desktop, Mobilgerät, Tablet, Smart-Lautsprecher und vernetztes TV

### Unterstützte Drittanbieter-Anzeigenserver

Sie können Tag-Tabellen aus [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] und [!DNL Sizmek] verwenden. Eine vollständige Liste der unterstützten Anbieter finden Sie unter &quot;[Zertifizierte Ad Serving Partners](certified-ad-servers.md)&quot;.

### Voraussetzungen für Audio Assets (erforderlich)

**Dateityp:** MP3, OGG, AAC

**Kopfzeilen (schief):** Nicht zulässig

**Maximale Dateigröße:** 2 MB

**Bitrate:** 128

**Dateilänge:** 0-60s

#### Zusätzliche Anforderungen an Publisher

* **[!DNL iHeartRadio]**
   * Länge: 5, 15, 30 oder 60 Sekunden
   * Dateityp: MP3
   * Maximale Dateigröße: 320 kBit/s
   * Volumen: 44,1 kHz

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
   * Volumen: RMS normalisiert auf -14; dBFS-Spitzenwert normalisiert auf -0,2 dBFS

* **[!DNL TargetSpot]**
   * Länge: 15, 30 oder 60 Sekunden
   * Dateityp: MP3

* **[!DNL TuneIn]**
   * Länge: 10, 15 oder 30 Sekunden
   * Dateityp: MP3, OGG
   * Volumen: 44,1 kHz

### Anforderungen für begleitende Banneranzeigen (optional)

**Unterstützte Größen:** 300x250, 500x500, 640x640, 1024x1024

#### Zusätzliche Anforderungen an Publisher

* **[!DNL iHeartRadio]:**
   * Dateityp: JPEG, JPG, PNG, GIF, SWF, HTML
   * Maximale Dateigröße: 2,2 MB
   * Dimensionen: 300x250

* **[!DNL Pandora]:**
   * Dateityp: JPEG, GIF
   * Maximale Dateigröße: Größe: 100 KB
   * Dimensionen: 300x250 (Mobil- oder Desktop) oder 500x500 (Desktop)

* **[!DNL SoundCloud]:**
   * Dateityp: Statischer JPG, PNG
   * Maximale Dateigröße: unter 400 KB
   * Dimensionen: 1024x1024

* **[!DNL Spotify]:**
   * Dateityp: Statischer JPG, PNG
   * Maximale Dateigröße: 200 KB
   * Dimensionen: 300x250

* **[!DNL TuneIn]:**
   * Dateityp: JPEG, JPG, PNG, GIF, HTML
   * Maximale Dateigröße: 2 MB
   * Dimensionen: 300x250

## Native Display-Anzeigen

Jede Anzeige kann entweder ein Standbild oder ein bewegliches GIF (Kinemagramm) enthalten.

### Unterstützte Screens

Anzeigen werden standardmäßig auf Desktop- und Mobilgeräten bereitgestellt. Die Zielgruppenbestimmung für Geräte ist verfügbar, um die Bereitstellung anzupassen.

### Erforderliche Assets für alle nativen In-Feed-Formate

#### Bild-Asset

**Auflösung:** Mindestens 600x600px; empfohlen mindestens 1200x627px

**Dateityp:** JPEG (Bild- oder Videoanzeigendeckbild), GIF (Cinemograph)

**Dateigröße:** Weniger als 1 MB (Bild sollte frei von Text sein.)

#### Advertiser-Logo

**Auflösung:** Mindestens 80x80px; empfohlen mindestens 300x300px

**Dateityp:** JPEG oder PNG.

**Seitenverhältnis:** 1x1-Verhältnis

>[!NOTE]
>
>Je nachdem, über welchem Bild es überlagert wird, können Sie zwischen hellen oder dunklen Logoelementen wählen.

#### Text/Kopieren

**Überschrift:** Maximal 200 Zeichen; 25 Zeichen empfohlen

**Beschriftung:** Maximal 200 Zeichen; 100 Zeichen werden empfohlen

**gesponsert von:** Maximal 200 Zeichen; 30 Zeichen empfohlen

**Aktionsaufruf (nur MoPub):** Maximal 15 Zeichen

>[!NOTE]
>
>Das endgültige Layout wird vom Publisher zur Laufzeit definiert. Wenn eine Anzeige die empfohlene Zeichenanzahl überschreitet, dürfen einige Inventaranbieter die Anzeige möglicherweise nicht bereitstellen, oder der Herausgeber oder SSP kann den Text abschneiden.

#### Landingpage-URL

Die Clickthrough-URL mit optionalen Klicktrackern.

Anforderungen an Klick-Tracker:

* Impression-Tracking-Pixel von Drittanbietern: Nur 1x1-Bild-URL-Format

* Sichtbarkeit JavaScript-Tracker: Nur für IAS unterstützt; nur 1x1-Bilder im JS.append-Format

* Clicktracking-Pixel von Drittanbietern: Muss zu der in die URL eingebetteten Landingpage weitergeleitet werden (HTTP 302-Weiterleitung)

* Klick-Tracker mit Data Management Platform (DMP) mit 200 oder mehr Antworten werden nicht unterstützt.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Erstellen mehrerer Drittanbieteranzeigen](ad-create-multiple.md)
>* [Bearbeiten einer Anzeige](ad-edit.md)
