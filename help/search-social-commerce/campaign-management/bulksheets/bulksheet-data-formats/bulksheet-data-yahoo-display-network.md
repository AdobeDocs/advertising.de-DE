---
title: 'Bulksheet-Daten für  [!DNL Yahoo! Display Network] '
description: Referenzieren Sie die Header- und Datenfelder in heruntergeladenen Bulksheets für - [!DNL Yahoo! Display Network] .
exl-id: 8d938009-6edc-4420-8863-21ed241616f8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Anhang - Bulksheet-Daten für [!DNL Yahoo! Display Network] Konten

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

Sie können Daten für [!DNL Yahoo! Display Network] Konten massenweise herunterladen, aber keine Bulksheets in das Werbenetzwerk hochladen oder posten.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Verfügbare Datenfelder

| Feld | Campaign | Anzeigengruppe | Anzeige | Beschreibung |
|----|----|----|----|----|
| [!UICONTROL Platform] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. |
| [!UICONTROL Acct  Name] | Falls enthalten | Falls enthalten | Falls enthalten | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. |
| [!UICONTROL Campaign Name] | Falls enthalten | Falls enthalten | Falls enthalten | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| [!UICONTROL Ad Group Name] | Nicht zutreffend | Falls enthalten | Falls enthalten | Der eindeutige Name, der eine Anzeigengruppe identifiziert. |
| [!UICONTROL Ad Name] | Nicht zutreffend | Nicht zutreffend | Falls enthalten | Der eindeutige Name, der die Anzeige innerhalb einer Anzeigengruppe identifiziert. Die maximale Länge beträgt 50 Zeichen. |
| [!UICONTROL Ad Title] | Nicht zutreffend | Nicht zutreffend | Falls enthalten | Die Überschrift einer Anzeige. |
| [!UICONTROL Description Line 1] | Nicht zutreffend | Nicht zutreffend | Falls enthalten | Die erste Zeile des Hauptteils einer Anzeige. |
| [!UICONTROL Description Line 2] | Nicht zutreffend | Nicht zutreffend | Falls enthalten | Die zweite Zeile des Hauptteils einer Anzeige. |
| [!UICONTROL Base URL/Final URL] | Nicht zutreffend | Nicht zutreffend | Falls enthalten | Die Landingpage-URL, zu der Endbenutzer beim Klicken auf Ihre Anzeige geleitet werden, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter. Basis-/endgültige URLs auf Keyword-Ebene überschreiben URLs auf Anzeigenebene und höher. |
| [!UICONTROL Destination URL] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (Zu Informationszwecken in generierten Bulksheets enthalten; nicht im Werbenetzwerk veröffentlicht) Bei Konten mit Ziel-URLs ist dieser Wert die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Werbetreibenden verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Sie enthält alle Anlagenparameter, die für die Kampagne oder das Konto „Suche“, „Social“ und &quot;Commerce&quot; konfiguriert wurden. Wenn Sie Tracking-URLs generiert haben, basiert dieser Wert auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie Anzeigennetzwerkspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Suche, Social und Commerce ersetzt werden. |
| \[Advertiser-spezifische Label-Klassifizierung\] | Falls enthalten | Falls enthalten | Falls enthalten | (Benannt nach einer Advertiser-spezifischen Kennzeichnungsklassifizierung, z. B. „Farbe“ für eine Kennzeichnungsklassifizierung namens „Farbe„) Ein Wert für die angegebene Klassifizierung, der mit der Entität verknüpft ist. |
| [!UICONTROL Constraints] | Falls enthalten | Falls enthalten | Nicht zutreffend | Eine Begrenzung, die der Entität zugewiesen ist. |
| [!UICONTROL Campaign Status] | Falls enthalten | Nicht zutreffend | Nicht zutreffend | Der Anzeigestatus der Kampagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | Nicht zutreffend | Falls enthalten | Nicht zutreffend | Der Anzeigestatus der Anzeigengruppe: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | Nicht zutreffend | Nicht zutreffend | Falls enthalten | Der Anzeigestatus des Keywords: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Keywords). |
| [!UICONTROL Campaign ID] | Falls enthalten | Falls enthalten | Falls enthalten | Die eindeutige ID, die eine vorhandene Kampagne identifiziert. |
| [!UICONTROL Ad Group ID] | Nicht zutreffend | Falls enthalten | Falls enthalten | Die eindeutige ID, die eine vorhandene Anzeigengruppe identifiziert. |
| [!UICONTROL Keyword ID] | Nicht zutreffend | Nicht zutreffend | Falls enthalten | Die eindeutige ID, die ein vorhandenes Keyword identifiziert. |
| [!UICONTROL AMO ID] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets) Eine von Adobe generierte eindeutige Kennung für eine synchronisierte Entität. |
| [!UICONTROL EF Error Message] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige von Fehlermeldungen von Search, Social und Commerce zu Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL EF Errors] Dateien enthalten. |

>[!MORELIKETHIS]
>
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
