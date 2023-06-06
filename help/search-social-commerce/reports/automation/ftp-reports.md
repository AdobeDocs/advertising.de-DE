---
title: FTP-Zugriff auf Berichte
description: Erfahren Sie, wie Sie Berichte an einem schreibgeschützten FTP-Speicherort empfangen können.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# FTP-Zugriff auf Berichte

Sie können optional Berichte an einem schreibgeschützten FTP-Speicherort empfangen, von dem Sie die Dateien für zusätzliche automatisierte Prozesse abrufen können (z. B. um die Daten mit einem anderen Programm zu analysieren). Alle Basisberichte außer [!UICONTROL Search Engine Account Report] und alle erweiterten Berichte können als komprimierte TSV-Dateien (Standard) oder CSV-Dateien mit der Dateierweiterung .ZIP an einen FTP-Speicherort gesendet werden. Alle TSV- oder CSV-Dateikopfzeilen sind enthalten und können nicht unterdrückt werden.

Für den FTP-Zugriff auf Berichte ist der Zugriff auf ein bestimmtes FTP-Konto erforderlich. Außerdem müssen Sie Berichtsvorlagen mithilfe einer bestimmten Namenskonvention und eines Zeitplans einrichten.

## Einrichten eines FTP-Kontos für den Zugriff auf Berichte

* Wenden Sie sich an Ihr Adobe Account Team, um ein FTP-Konto für den Zugriff auf Berichte einzurichten.

   Das Team stellt Ihnen Ihren Benutzernamen und Ihr Passwort zur Verfügung.

## Berichtsvorlagen für den FTP-Versand einrichten

Um Berichte in Ihrem dafür vorgesehenen FTP-Verzeichnis zu generieren, erstellen Sie eine [Berichtsvorlage](templates/template-create.md) mit den folgenden Benennungskonventionen und -zeitplänen.

>[!NOTE]
>
>Alle erweiterten Berichte und alle Basisberichte außer [!UICONTROL Search Engine Account Report] kann an einen FTP-Speicherort bereitgestellt werden.

1. Schließen Sie in der Berichtsvorlage an einer beliebigen Stelle im Vorlagennamen die folgenden Informationen ein:

   * `FTP` (in Großbuchstaben).

   * (Optional) Jedes der drei Systemdaten unter Verwendung der folgenden Syntax, bei der zwischen Groß- und Kleinschreibung unterschieden wird, einschließlich Klammern:

      * `[TODAY]` - So fügen Sie das Datum, die Stunde und die Minute hinzu, in der der Bericht ausgeführt wurde. Da dies die genaue Uhrzeit enthält, kann dieselbe Vorlage mehrmals am Tag ausgeführt werden, ohne den vorherigen Bericht zu überschreiben.

      * `[SDATE]` — So fügen Sie das Startdatum des Berichtsdatumsbereichs hinzu.

      * `[EDATE]` — So fügen Sie das Enddatum des Berichtsdatumsbereichs hinzu.
   * (Optional) `[CSV]` (in Großbuchstaben und in Klammern eingeschlossen), um Dateien im CSV-Format und nicht im standardmäßigen TSV-Format zu erstellen.

   Beispiel: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` würde eine Datei wie 202305051656-Portfolio-FTP-20230428-20110504.csv erstellen.

1. Planen Sie die Ausführung des Berichts zu einem bestimmten Zeitpunkt.

   Die Berichte werden innerhalb einer Stunde nach Abschluss an das FTP-Konto gesendet.

>[!NOTE]
>
>* Um abgeschlossene Berichte per E-Mail zu versenden, geben Sie bei der Erstellung des Berichts oder der Vorlage einfach die Adressen aller E-Mail-Empfänger an.
>* Berichte werden entsprechend ihren festgelegten Zeitplänen ausgeführt und innerhalb einer Stunde nach Abschluss an das FTP-Konto gesendet.


## Zugriff auf Berichte in einem FTP-Repository

Um auf Ihre Berichte zuzugreifen, stellen Sie mithilfe der Anmeldedaten für Ihr FTP-Konto (`amo<userID>rpt`, z. B. amo1234rpt) und entweder ein Kennwort oder einen privaten Verbindungsschlüssel, wenn eines eingerichtet ist:

* Internationale Kunden: `ftp3.adobe.net`
* US-Kunden: `ftp5.adobe.net`

>[!NOTE]
>
>Das Berichte-Repository ist schreibgeschützt und wird alle 15 Tage gelöscht.


>[!MORELIKETHIS]
>
>* [Berichtsvorlage erstellen](/help/search-social-commerce/reports/automation/templates/template-create.md)

