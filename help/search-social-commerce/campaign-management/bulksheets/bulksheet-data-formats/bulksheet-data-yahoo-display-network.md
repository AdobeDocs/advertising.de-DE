---
title: Massenblattdaten für [!DNL Yahoo! Display Network] Konten
description: Referenzieren Sie die Kopfzeilenfelder und Datenfelder in heruntergeladenen Bulksheets für [!DNL Yahoo! Display Network] Konten.
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Anhang - Bulksheet-Daten für [!DNL Yahoo! Display Network] Konten

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

Sie können Daten herunterladen für [!DNL Yahoo! Display Network] -Konten in Batches, können jedoch keine Bulksheets in das Werbenetzwerk hochladen oder dort posten.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Verfügbare Datenfelder

| Feld | Kampagne | Anzeigengruppe | Anzeige | Beschreibung |
|----|----|----|----|----|
| [!UICONTROL Platform] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. |
| [!UICONTROL Acct  Name] | Ist enthalten | Ist enthalten | Ist enthalten | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. |
| [!UICONTROL Campaign Name] | Ist enthalten | Ist enthalten | Ist enthalten | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| [!UICONTROL Ad Group Name] | Nicht zutreffend | Ist enthalten | Ist enthalten | Der eindeutige Name, der eine Anzeigengruppe identifiziert. |
| [!UICONTROL Ad Name] | Nicht zutreffend | Nicht zutreffend | Ist enthalten | Der eindeutige Name, der die Anzeige innerhalb einer Anzeigengruppe identifiziert. Die maximale Länge beträgt 50 Zeichen. |
| [!UICONTROL Ad Title] | Nicht zutreffend | Nicht zutreffend | Ist enthalten | Die Überschrift einer Anzeige. |
| [!UICONTROL Description Line 1] | Nicht zutreffend | Nicht zutreffend | Ist enthalten | Die erste Zeile des Hauptteils einer Anzeige. |
| [!UICONTROL Description Line 2] | Nicht zutreffend | Nicht zutreffend | Ist enthalten | Die zweite Zeile des Hauptteils einer Anzeige. |
| [!UICONTROL Base URL/Final URL] | Nicht zutreffend | Nicht zutreffend | Ist enthalten | Die Landingpage-URL, an die Endbenutzer beim Klicken auf Ihre Anzeige herangeführt werden, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter. Basis-/endgültige URLs auf Suchbegriffebene überschreiben URLs auf Anzeigenebene und höher. |
| [!UICONTROL Destination URL] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (in generierten Bulksheets zu Informationszwecken enthalten; bei Konten mit Ziel-URLs ist dieser Wert die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Advertisers verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Sie enthält alle für die Kampagne oder das Konto &quot;Search, Social und Commerce&quot;konfigurierten Anlagenparameter. Wenn Sie Tracking-URLs generiert haben, basiert dieser Wert auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie Anzeigennetzwerkspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Search, Social und Commerce ersetzt werden. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Ist enthalten | Ist enthalten | Ist enthalten | (Benannt für eine Advertiser-spezifische Beschriftungs-Classification, z. B. &quot;Farbe&quot;für eine Beschriftungsklassifizierung namens &quot;Farbe&quot;) Ein Wert für die angegebene Classification, die mit der Entität verknüpft ist. |
| [!UICONTROL Constraints] | Ist enthalten | Ist enthalten | Nicht zutreffend | Eine Beschränkung, die der Entität zugewiesen wird. |
| [!UICONTROL Campaign Status] | Ist enthalten | Nicht zutreffend | Nicht zutreffend | Der Anzeigestatus der Kampagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | Nicht zutreffend | Ist enthalten | Nicht zutreffend | Der Anzeigestatus der Anzeigengruppe: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | Nicht zutreffend | Nicht zutreffend | Ist enthalten | Der Anzeigestatus des Suchbegriffs: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Suchbegriffe). |
| [!UICONTROL Campaign ID] | Ist enthalten | Ist enthalten | Ist enthalten | Die eindeutige ID, die eine bestehende Kampagne identifiziert. |
| [!UICONTROL Ad Group ID] | Nicht zutreffend | Ist enthalten | Ist enthalten | Die eindeutige ID, die eine bestehende Anzeigengruppe identifiziert. |
| [!UICONTROL Keyword ID] | Nicht zutreffend | Nicht zutreffend | Ist enthalten | Die eindeutige ID, die einen vorhandenen Suchbegriff identifiziert. |
| [!UICONTROL AMO ID] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets) Eine von der Adobe generierte eindeutige Kennung für eine synchronisierte Entität. |
| [!UICONTROL EF Error Message] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets für Informationszwecke enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus Search, Social und Commerce zu Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL EF Errors] Dateien. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
