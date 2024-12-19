---
title: 'Erforderliche Bulksheet-Daten für  [!DNL Naver] '
description: Referenzieren Sie die erforderlichen Kopfzeilenfelder und Datenfelder in Bulksheets für  [!DNL Naver]  Konten.
exl-id: 1bfcdbb6-8026-4230-ab6b-b7c79b0d185a
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Anhang - Erforderliche Bulksheet-Daten für [!DNL Naver]

Füllen Sie Ihre [!DNL Naver]-Konten in Search, Social und Commerce, indem Sie in [!DNL Naver] eine Bulksheet-Datei generieren und diese dann in Search, Social und Commerce hochladen.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Verfügbare Datenfelder

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Feld | Campaign | Anzeigengruppe | Schlüsselwort | Beschreibung |
|----|----|----|----|----|
| [!UICONTROL Platform] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. Erforderlich, es sei denn, jede Zeile enthält eine AMO-ID für die Entität. |
| [!UICONTROL Acct Name] | Erforderlich/Optional | Erforderlich/Optional | Erforderlich/Optional | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. Erforderlich, es sei denn, jede Zeile enthält eine AMO-ID für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich | Erforderlich | Erforderlich | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| [!UICONTROL Ad Group Name] | Nicht zutreffend | Erforderlich | Erforderlich | Der eindeutige Name, der eine Anzeigengruppe identifiziert. |
| [!UICONTROL Keyword] | Nicht zutreffend | Nicht zutreffend | Erforderlich | Die Keyword-Zeichenfolge. |
| [!UICONTROL Base URL] | Nicht zutreffend | Nicht zutreffend | optional | Die Landingpage-URL, zu der Endbenutzer beim Klicken auf Ihre Anzeige geleitet werden, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter.<br><br>Basis-/endgültige URLs auf Keyword-Ebene überschreiben URLs auf Anzeigenebene und höher. |
| [!UICONTROL Destination URL] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (Zu Informationszwecken in generierten Bulksheets enthalten; nicht im Werbenetzwerk veröffentlicht) Bei Konten mit Ziel-URLs ist dieser Wert die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Werbetreibenden verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Sie enthält alle Anlagenparameter, die für die Kampagne oder das Konto „Suche“, „Social“ und &quot;Commerce&quot; konfiguriert wurden. Wenn Sie Tracking-URLs generiert haben, basiert dieser Wert auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie Anzeigennetzwerkspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Suche, Social und Commerce ersetzt werden.<br><br>Bei Konten mit endgültigen URLs zeigt diese Spalte denselben Wert wie die [!UICONTROL Base URL/Final URL column] an. |
| \[Advertiser-spezifische Label-Klassifizierung\] | optional | optional | optional | (Benannt nach einer Advertiser-spezifischen Kennzeichnungsklassifizierung, z. B. „Farbe“ für eine Kennzeichnungsklassifizierung namens „Farbe„) Ein Wert für die angegebene Klassifizierung, der mit der Entität verknüpft ist. Pro Entität kann nur ein Wert angegeben werden (z. B. „Rot“ für die Kennzeichnung „Farbe“ für Kampagne A). Die maximale Länge beträgt 100 Zeichen. Der Wert kann ASCII- und Nicht-ASCII-Zeichen enthalten.<br><br>Kennzeichnungsklassifizierungen und ihre Kennzeichnungswerte werden auf alle untergeordneten Komponenten angewendet; neue Komponenten, die später hinzugefügt werden, werden automatisch mit der Kennzeichnung verknüpft. Kennzeichnungsklassifizierungen für Produktgruppen werden auf die Ebene der Einheit (mit der höchsten Granularität) angewendet.<br><br>Beim Classification-Namen und Classification-Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden. |
| [!UICONTROL Constraints] | optional | optional | optional | Eine Begrenzung, die der Entität zugewiesen ist. Pro Entität kann nur eine Einschränkung zugewiesen werden.<br><br>Abhängigkeiten werden von untergeordneten Entitäten übernommen, sodass Sie keine Werte für untergeordnete Entitäten eingeben müssen, es sei denn, Sie möchten die übernommenen Werte überschreiben. |
| [!UICONTROL Campaign Status] | Optional: Erstellen oder Bearbeiten<br> Erforderlich: Löschen | Nicht zutreffend | Nicht zutreffend | Der Anzeigestatus der Kampagne: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur für bestehende Kampagnen). Der Standardwert für neue Kampagnen ist <i>[!UICONTROL Active]</i>. Um eine aktive oder pausierte Kampagne zu löschen, geben Sie den Wert &quot;[!UICONTROL Deleted]&quot; ein. |
| [!UICONTROL Ad Group Status] | Nicht zutreffend | Optional: Erstellen oder Bearbeiten<br> Erforderlich: Löschen | Nicht zutreffend | Der Anzeigestatus der Anzeigengruppe: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Anzeigengruppen). Der Standardwert für neue Anzeigengruppen ist <i>[!UICONTROL Active]</i>. Um eine aktive oder pausierte Anzeigengruppe zu löschen, geben Sie den Wert &quot;[!UICONTROL Deleted]&quot; ein. |
| [!UICONTROL Keyword Status] | Nicht zutreffend | Nicht zutreffend | Optional: Erstellen oder Bearbeiten<br> Erforderlich: Löschen | Der Anzeigestatus des Keywords: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Keywords). Die Standardeinstellung für neue Schlüsselwörter ist <i>[!UICONTROL Active]</i>. Um ein aktives oder angehaltenes Keyword zu löschen, geben Sie den Wert &quot;[!UICONTROL Deleted]&quot; ein. |
| [!UICONTROL Campaign ID] | Nicht zutreffend: Erstellen<br>Erforderlich/Optional: Bearbeiten oder Löschen | optional | optional | Die eindeutige ID, die eine vorhandene Kampagne identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält eine AMO-ID für die Kampagne. |
| [!UICONTROL Ad Group ID] | Nicht zutreffend | Nicht zutreffend: Erstellen<br>Erforderlich/Optional: Bearbeiten oder Löschen | optional | Die eindeutige ID, die eine vorhandene Anzeigengruppe identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Anzeigengruppennamen ändern, es sei denn, die Zeile enthält eine AMO-ID für die Anzeigengruppe. |
| [!UICONTROL Keyword ID] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend: Erstellen<br>Erforderlich/Optional: Bearbeiten<br>Erforderlich: Löschen | Die eindeutige ID, die ein vorhandenes Keyword identifiziert. In CSV- und TSV-Dateien muss vor ihr ein einfaches Anführungszeichen (&#39;) stehen.[^1] Nur erforderlich, wenn Sie den Schlüsselwortnamen ändern, es sei denn, die Zeile enthält a) ausreichend Eigenschaftenspalten zur Identifizierung des Schlüsselworts oder b) eine AMO-ID. |
| [!UICONTROL AMO ID] | k. A.: Erstellen<br>Optional: Bearbeiten oder Löschen | k. A.: Erstellen<br>Optional: Bearbeiten oder Löschen | k. A.: Erstellen<br>Optional: Bearbeiten oder Löschen | (In generierten Bulksheets) Eine [!DNL Adobe] eindeutige Kennung für eine synchronisierte Entität. Bei responsiven Suchanzeigen ist die AMO-ID erforderlich, um Anzeigen zu bearbeiten oder zu löschen, es sei denn, Sie schließen die [!UICONTROL Ad ID] ein. Um Daten für alle anderen Entitätstypen mit einer AMO-ID zu bearbeiten, muss die AMO-ID die Daten bearbeiten oder löschen, es sei denn, Sie beziehen die Entitäts-ID und die übergeordnete Entitäts-ID ein.<br><br>Search, Social und Commerce verwenden den Wert zum Bestimmen der richtigen Identität, die bearbeitet werden soll, senden die ID jedoch nicht an das Werbenetzwerk. |
| [!UICONTROL EF Error Message] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige von Fehlermeldungen von Search, Social und Commerce zu Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL EF Errors] Dateien enthalten. Dieser Wert wird nicht an das Werbenetzwerk gesendet. |
| [!UICONTROL SE Error Message] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets zu Informationszwecken enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Werbenetzwerk bezüglich Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL SE Errors] Dateien enthalten. Dieser Wert wird nicht an das Werbenetzwerk gesendet. |

[^1]: Excel konvertiert große Zahlen in wissenschaftliche Notation (z. B. 2.12E+09 für 2115585666), wenn es die Datei öffnet. Um Ziffern in der Standardnotation anzuzeigen, wählen Sie eine beliebige Zelle in der Spalte aus und klicken Sie in die Leiste Formel .

>[!MORELIKETHIS]
>
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Vorgänge, die Sie in Bulksheets ausführen können](bulksheet-operations.md)
>* [Unterstützte Bulksheet-Dateiformate](bulksheet-file-formats.md)
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
>* [Klick-Tracking-Formate für [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Hochladen einer Bulksheet-Datei oder einer korrigierten Fehlerdatei](../bulksheet-upload.md)
>* [Nur [!DNL Naver] Tracking-Konten implementieren](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
