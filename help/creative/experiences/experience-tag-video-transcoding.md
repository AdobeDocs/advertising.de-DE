---
title: Anpassen der Transkodierungsoptionen für ein Video- und Erlebnis-Tag
description: Erfahren Sie, wie Sie die Transkodierungsoptionen für ein Video-Anzeigen-Tag anpassen.
feature: Creative Experiences
exl-id: 6100213c-2e7d-4e98-a3ab-045ca10e5174
TQID: https://experienceleague.adobe.com/N-tKrSHyE18QVazmdUlurPsW-7QVwGKAOPl2ArnI-2c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 0%

---

# Anpassen der Transkodierungsoptionen für ein Video- und Erlebnis-Tag

Sie können die Transkodierungsoptionen für ein Video- und Anwendererlebnis anpassen, um eine schnelle Wiedergabe und Qualitätskontrolle über alle Publisher hinweg sicherzustellen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Tag Manager]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Tag Manager]**.

1. Halten Sie den Cursor über die Zeile für das entsprechende Anzeigen-Tag, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Video Settings]**.

1. Wählen Sie in der Liste der **[!UICONTROL Publisher-specific transcodes]** die DSP aus, deren Transkodierung Sie anwenden möchten.

1. Klicken Sie auf **[!UICONTROL Save Settings]**.

## Standardmäßige ([!DNL Adobe] DSP) Transkodierungsspezifikation

| Dateityp | Dimensionen | Video-Bitrate | Video-Bildwechselfrequenz | Audiobitrate | Audio-Abtastrate | Audiopegel |
|---|---|---|---|---|---|---|
| MP4 | 640 x 360 | 1000 kBit/s | 23,98 Bilder/s | 128 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 400 x 300 | 1000 kBit/s | 23,98 Bilder/s | 128 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 1024 x 768 | 500 kBit/s | 23,98 Bilder/s | 128 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 640 x 480 | 1000 kBit/s | 23,98 Bilder/s | 128 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 960 x 540 | 2.000 kBit/s | 23,98 Bilder/s | 128 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 960 x 720 | 2.000 kBit/s | 23,98 Bilder/s | 128 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 1280 x 720 | 2.000 kBit/s | 23,98 Bilder/s | 128 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 1920 x 1080 | 3.500 kBit/s | 23,98 Bilder/s | 128 kBit/s | 44,100 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 640 x 360 | 800 kBit/s | 23,98 Bilder/s | 96 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 640 x 360 | 400 kBit/s | 23,98 Bilder/s | 128 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| MP4 | 1920 x 1080 | 16000 kBit/s | 23,98 Bilder/s | 256 kBit/s | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |

>[!MORELIKETHIS]
>
>* [Über Ihre Kreativbibliotheken](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Erstellen eines Erlebnisses mit Targeting](/help/creative/experiences/experience-create-targeting.md)
>* [Manuelles Erstellen eines Anzeigen-Tags für eine entsprechende Kreativgröße](experience-tag-create-manually.md)
>* [Exportieren und Implementieren eines Anzeigen-Erlebnis-Tags für ein Live-Erlebnis](experience-tag-export.md)
