---
title: Verfügbare Felder für dynamische Anzeigen-Feed-Dateien
description: Erfahren Sie mehr über die Felder, die Sie in die Feed-Dateien aufnehmen können, die Sie zum Erstellen dynamischer Anzeigen verwenden.
feature: Creative Dynamic Creatives
source-git-commit: 67ee38860ac5cb7e9340f8e9d4667353e509b1ec
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Anhang: Verfügbare Felder für dynamische Anzeigen-Feed-Dateien

Die folgenden Feed-Felder sind im Advertising Creative-Backend verfügbar. Sie können eine [Feed-Datei](/help/creative/feeds/asset-manage.md) hochladen, die Ihre organisationsspezifischen Feldnamen verwendet. Bevor Sie jedoch einen [Katalog](/help/creative/feeds/catalog-manage.md) aus Ihrer Feed-Datei erstellen können, müssen Sie jedes Feld in der Feed-Datei einem der folgenden Felder in der [Feed-Vorlage](/help/creative/feeds/feed-template-manage.md) zuordnen, die Sie zum Erstellen des Katalogs verwenden werden.

Das einzige Feld, das eine Entsprechung in Ihrer Feed-Datei haben muss, ist `PART_NUM`.

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| Feldname | Datentyp | Erforderlich? |
|------------|-----------|-----------|
| PART_NUM | varchar(64) | JA |
| PRODUCT_NAME | Text | NEIN |
| PRODUCT_URL | Text | NEIN |
| PREIS | DECIMAL(10,2) | NEIN |
| DISCOUNT_PRICE | DECIMAL(10,2) | NEIN |
| IMAGE | varchar(1024) | NEIN |
| IMAGE_HEIGHT | int | NEIN |
| IMAGE_WIDTH | int | NEIN |
| IMAGE_1 | varchar(1024) | NEIN |
| IMAGE_2 | varchar(1024) | NEIN |
| IMAGE_3 | varchar(1024) | NEIN |
| IMAGE_4 | varchar(1024) | NEIN |
| IMAGE_5 | varchar(1024) | NEIN |
| IMAGE_6 | varchar(1024) | NEIN |
| IMAGE_7 | varchar(1024) | NEIN |
| IMAGE_8 | varchar(1024) | NEIN |
| IMAGE_9 | varchar(1024) | NEIN |
| IMAGE_10 | varchar(1024) | NEIN |
| TEXT_1 | Text | NEIN |
| TEXT_2 | Text | NEIN |
| TEXT_3 | Text | NEIN |
| TEXT_4 | Text | NEIN |
| TEXT_5 | Text | NEIN |
| TEXT_6 | Text | NEIN |
| TEXT_7 | Text | NEIN |
| TEXT_8 | Text | NEIN |
| TEXT_9 | Text | NEIN |
| TEXT_10 | Text | NEIN |
| TEXT_11 | Text | NEIN |
| TEXT_12 | Text | NEIN |
| TEXT_13 | Text | NEIN |
| TEXT_14 | Text | NEIN |
| TEXT_15 | Text | NEIN |
| ADDITIONAL_PRICE_1 | DECIMAL(10,2) | NEIN |
| ADDITIONAL_PRICE_2 | DECIMAL(10,2) | NEIN |
| ADDITIONAL_PRICE_3 | DECIMAL(10,2) | NEIN |
| AD_SIZE | varchar(32) | NEIN |
| RANG | int | NEIN |
| LAND | Text | NEIN |
| STATUS | Text | NEIN |
| STADT | Text | NEIN |
| PLZ | Text | NEIN |
| DMA | Text | NEIN |
| PROFILE_FILTER_1 | Text | NEIN |
| PROFILE_FILTER_2 | Text | NEIN |
| PROFILE_FILTER_3 | Text | NEIN |
| PROFILE_FILTER_4 | Text | NEIN |
| PROFILE_FILTER_5 | Text | NEIN |
| DATAPASS_FILTER_1 | Text | NEIN |
| DATAPASS_FILTER_2 | Text | NEIN |
| DATAPASS_FILTER_3 | Text | NEIN |
| DATAPASS_FILTER_4 | Text | NEIN |
| DATAPASS_FILTER_5 | Text | NEIN |
| AUDIENCE_SEGMENT | Text | NEIN |
| SPRACHE | Text | NEIN |
| CREATIVE_ATTRIBUTE_1 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_2 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_3 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_4 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_5 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_6 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_7 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_8 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_9 | varchar(256) | NEIN |
| CREATIVE_ATTRIBUTE_10 | varchar(256) | NEIN |
| IS_DEFAULT | Aufzählung | NEIN |

>[!MORELIKETHIS]
>
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Verwalten von Asset-Dateien](/help/creative/feeds/asset-manage.md)
>* [Verwalten von Feed-Vorlagen](/help/creative/feeds/feed-template-manage.md)
>* [Kataloge verwalten](/help/creative/feeds/catalog-manage.md)
