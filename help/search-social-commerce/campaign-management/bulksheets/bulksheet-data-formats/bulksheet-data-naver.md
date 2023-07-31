---
title: Erforderliche Bulksheet-Daten für [!DNL Naver] Konten
description: Referenzieren Sie die erforderlichen Kopfzeilenfelder und Datenfelder in Bulksheets für [!DNL Naver] Konten.
exl-id: bd6e3dab-47b0-428a-825d-bd9c21494fb0
feature: Search Bulksheets
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 1%

---

# Anhang - Erforderliche Bulksheet-Daten für [!DNL Naver] Konten

Ihre [!DNL Naver] Konten in Search, Social &amp; Commerce durch Generieren einer Bulksheet-Datei in [!DNL Naver]und dann in Search, Social und Commerce hochladen.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Verfügbare Datenfelder

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Feld | Kampagne | Anzeigengruppe | Schlüsselwort | Beschreibung |
|----|----|----|----|----|
| [!UICONTROL Platform] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets zu Informationszwecken enthalten) Die Anzeigenplattform. Erforderlich, es sei denn, jede Zeile enthält eine AMO-ID für die Entität. |
| [!UICONTROL Acct Name] | Erforderlich/Optional | Erforderlich/Optional | Erforderlich/Optional | Der eindeutige Name, der ein Anzeigennetzwerkkonto identifiziert. Erforderlich, es sei denn, jede Zeile enthält eine AMO-ID für die Entität. |
| [!UICONTROL Campaign Name] | Erforderlich | Erforderlich | Erforderlich | Der eindeutige Name, der eine Kampagne für ein Konto identifiziert. |
| [!UICONTROL Ad Group Name] | Nicht zutreffend | Erforderlich | Erforderlich | Der eindeutige Name, der eine Anzeigengruppe identifiziert. |
| [!UICONTROL Keyword] | Nicht zutreffend | Nicht zutreffend | Erforderlich | Die Suchbegriff-Zeichenfolge. |
| [!UICONTROL Base URL] | Nicht zutreffend | Nicht zutreffend | Optional | Die Landingpage-URL, an die Endbenutzer beim Klicken auf Ihre Anzeige herangeführt werden, einschließlich aller für die Kampagne oder das Konto konfigurierten Anlagenparameter.<br><br>Basis-/endgültige URLs auf Suchbegriffebene überschreiben URLs auf Anzeigenebene und höher. |
| [!UICONTROL Destination URL] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets zu Informationszwecken enthalten; nicht im Werbenetzwerk veröffentlicht) Bei Konten mit Ziel-URLs ist dieser Wert die URL, die eine Anzeige mit einer Basis-URL/Landingpage auf der Website des Advertisers verknüpft (manchmal über eine andere Site, die den Klick verfolgt und den Benutzer dann zur Landingpage weiterleitet). Sie enthält alle für die Kampagne oder das Konto &quot;Search, Social und Commerce&quot;konfigurierten Anlagenparameter. Wenn Sie Tracking-URLs generiert haben, basiert dieser Wert auf den Tracking-Parametern in Ihren Konto- und Kampagneneinstellungen. Wenn Sie Anzeigennetzwerkspezifische Parameter angehängt haben, können diese durch die entsprechenden Parameter für Suche, Social und Commerce ersetzt werden.<br><br>Bei Konten mit finalen URLs zeigt diese Spalte denselben Wert wie die [!UICONTROL Base URL/Final URL column]. |
| \[Advertiser-spezifische Beschriftungsklassifizierung\] | Optional | Optional | Optional | (Benannt für eine Advertiser-spezifische Beschriftungs-Classification, z. B. &quot;Farbe&quot;für eine Beschriftungsklassifizierung namens &quot;Farbe&quot;) Ein Wert für die angegebene Classification, die mit der Entität verknüpft ist. Sie können pro Entität nur einen Wert einbeziehen (z. B. &quot;rot&quot;für die Klassifizierung &quot;Farbe&quot;für Kampagne A). Die maximale Länge beträgt 100 Zeichen. Der Wert kann ASCII- und Nicht-ASCII-Zeichen enthalten.<br><br>Beschriftungsklassifizierungen und ihre Beschriftungswerte werden auf alle untergeordneten Komponenten angewendet. Neue Komponenten, die später hinzugefügt werden, werden automatisch mit der Beschriftung verknüpft. Beschriftungsklassifizierungen für Produktgruppen werden auf die Einheitenebene (am detailliertesten) angewendet.<br><br>Beim Classification-Namen und Classification-Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden. |
| [!UICONTROL Constraints] | Optional | Optional | Optional | Eine Beschränkung, die der Entität zugewiesen wird. Sie können pro Entität nur eine Begrenzung zuweisen.<br><br>Einschränkungen werden von untergeordneten Entitäten übernommen. Sie müssen daher keine Werte für untergeordnete Entitäten eingeben, es sei denn, Sie möchten die vererbten Werte überschreiben. |
| [!UICONTROL Campaign Status] | Optional: Erstellen oder bearbeiten<br>Erforderlich: Löschen | Nicht zutreffend | Nicht zutreffend | Der Anzeigestatus der Kampagne: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i> (nur bestehende Kampagnen). Die Standardeinstellung für neue Kampagnen ist <i>[!UICONTROL Active]</i>. Um eine aktive oder ausgesetzte Kampagne zu löschen, geben Sie den Wert ein: &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | Nicht zutreffend | Optional: Erstellen oder bearbeiten<br>Erforderlich: Löschen | Nicht zutreffend | Der Anzeigestatus der Anzeigengruppe: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i> (nur bestehende Anzeigengruppen). Die Standardeinstellung für neue Anzeigengruppen ist <i>[!UICONTROL Active]</i>. Um eine aktive oder ausgesetzte Anzeigengruppe zu löschen, geben Sie den Wert ein: &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | Nicht zutreffend | Nicht zutreffend | Optional: Erstellen oder bearbeiten<br>Erforderlich: Löschen | Der Anzeigestatus des Suchbegriffs: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>oder <i>[!UICONTROL Deleted]</i> (nur vorhandene Suchbegriffe). Die Standardeinstellung für neue Suchbegriffe ist <i>[!UICONTROL Active]</i>. Um einen aktiven oder ausgesetzten Suchbegriff zu löschen, geben Sie den Wert ein:[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Campaign ID] | Nicht zutreffend: Erstellen<br>Erforderlich/Optional: Bearbeiten oder löschen | Optional | Optional | Die eindeutige ID, die eine bestehende Kampagne identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Kampagnennamen ändern, es sei denn, die Zeile enthält eine AMO-ID für die Kampagne. |
| [!UICONTROL Ad Group ID] | Nicht zutreffend | Nicht zutreffend: Erstellen<br>Erforderlich/Optional: Bearbeiten oder löschen | Optional | Die eindeutige ID, die eine bestehende Anzeigengruppe identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Anzeigengruppennamen ändern, es sei denn, die Zeile enthält eine AMO-ID für die Anzeigengruppe. |
| [!UICONTROL Keyword ID] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend: Erstellen<br>Erforderlich/Optional: Bearbeiten<br>Erforderlich: Löschen | Die eindeutige ID, die einen vorhandenen Suchbegriff identifiziert. In CSV- und TSV-Dateien muss ein einfaches Anführungszeichen (&#39;) vorangestellt werden.[^1] Nur erforderlich, wenn Sie den Keyword-Namen ändern, es sei denn, die Zeile enthält a) ausreichend Eigenschaftsspalten, um den Suchbegriff zu identifizieren, oder b) eine AMO-ID. |
| [!UICONTROL AMO ID] | Nicht zutreffend: Erstellen<br>Optional: Bearbeiten oder löschen | Nicht zutreffend: Erstellen<br>Optional: Bearbeiten oder löschen | Nicht zutreffend: Erstellen<br>Optional: Bearbeiten oder löschen | (In generierten Bulksheets) Ein [!DNL Adobe]-generierte eindeutige Kennung für eine synchronisierte Entität. Für responsive Suchanzeigen ist die AMO-ID erforderlich, um Anzeigen zu bearbeiten oder zu löschen, es sei denn, Sie enthalten die [!UICONTROL Ad ID]. Um Daten für alle anderen Entitätstypen mit AMO-ID zu bearbeiten, muss die AMO-ID die Daten bearbeiten oder löschen, es sei denn, Sie enthalten die Entitäts-ID und die übergeordnete Entitäts-ID.<br><br>Search, Social und Commerce verwenden den Wert zur Bestimmung der richtigen Identität, die bearbeitet werden soll, veröffentlichen die ID jedoch nicht im Werbenetzwerk. |
| [!UICONTROL EF Error Message] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (In generierten Bulksheets für Informationszwecke enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus Search, Social und Commerce zu Daten in der Zeile; Fehlermeldungen sind in [!UICONTROL EF Errors] -Dateien. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |
| [!UICONTROL SE Error Message] | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | (Zu Informationszwecken in generierten Bulksheets enthalten) Platzhalter für die Anzeige von Fehlermeldungen aus dem Anzeigennetzwerk bezüglich Daten aus der Zeile; Fehlermeldungen werden in [!UICONTROL SE Errors] -Dateien. Dieser Wert wird nicht im Werbenetzwerk veröffentlicht. |

[^1]: Excel konvertiert beim Öffnen der Datei große Zahlen in wissenschaftliche Notation (z. B. 2.12E+09 für 2115585666). Um Ziffern in der Standardnotation anzuzeigen, wählen Sie eine beliebige Zelle in der Spalte aus und klicken Sie in die Formelleiste.

>[!MORELIKETHIS]
>
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Vorgänge, die Sie in Bulksheets ausführen können](bulksheet-operations.md)
>* [Unterstützte Massendateiformate](bulksheet-file-formats.md)
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
>* [Klick-Tracking-Formate für [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Hochladen einer Bulksheet-Datei oder einer korrigierten Fehlerdatei](../bulksheet-upload.md)
>* [Implementierung [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
