---
title: FTP-Zugriff auf Berichte
description: Erfahren Sie, wie Sie Berichte an einem schreibgeschützten FTP-Speicherort empfangen können.
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# FTP-Zugriff auf Berichte

Optional können Sie Berichte an einem schreibgeschützten FTP-Speicherort empfangen, von dem aus Sie die Dateien für zusätzliche automatisierte Prozesse abrufen können (um beispielsweise die Daten mit einem anderen Programm zu analysieren). Alle Basisberichte außer [!UICONTROL Search Engine Account Report] und allen erweiterten Berichten können als komprimierte TSV-Dateien (die Standardeinstellung) oder CSV-Dateien mit der Dateierweiterung .ZIP an einen FTP-Speicherort gesendet werden. Alle TSV- oder CSV-Dateikopfzeilen sind enthalten und können nicht unterdrückt werden.

Der FTP-Zugriff auf Berichte erfordert Zugriff auf ein bestimmtes FTP-Konto, und Sie müssen Berichtsvorlagen mit einer bestimmten Namenskonvention und einem Zeitplan einrichten.

## FTP-Konto für den Zugriff auf Berichte einrichten

* Wenden Sie sich an Ihr Adobe-Konto-Team , um ein FTP-Konto für den Zugriff auf Berichte einzurichten.

  Das Team stellt Ihnen Ihren Benutzernamen und Ihr Passwort zur Verfügung.

## Einrichten von Berichtsvorlagen für die FTP-Bereitstellung

Um Berichte in Ihrem vorgesehenen FTP-Verzeichnis zu generieren, erstellen Sie [Berichtsvorlage](templates/template-create.md) mit den folgenden Benennungskonventionen und Zeitplänen.

>[!NOTE]
>
>Alle erweiterten Berichte und alle Standardberichte mit Ausnahme des [!UICONTROL Search Engine Account Report] können an einen FTP-Speicherort gesendet werden.

1. Fügen Sie in die Berichtsvorlage die folgenden Informationen an beliebiger Stelle im Vorlagennamen ein:

   * `FTP` (in Großbuchstaben)

   * (Optional) Eines der drei Systemdaten, wobei die folgende Syntax (einschließlich Klammern) unter Berücksichtigung der Groß-/Kleinschreibung verwendet wird:

      * `[TODAY]` - Um das Datum, die Stunde und die Minute einzuschließen, an denen der Bericht ausgeführt wurde. Da dies den genauen Zeitpunkt enthält, kann dieselbe Vorlage mehrmals am Tag ausgeführt werden, ohne den vorherigen Bericht zu überschreiben.

      * `[SDATE]` - Zum Einschließen des Startdatums des Datumsbereichs des Berichts.

      * `[EDATE]` - Zum Einschließen des Enddatums des Datumsbereichs des Berichts.

   * (Optional) `[CSV]` (in Großbuchstaben und in eckigen Klammern), um Dateien im CSV-Format statt im Standard-TSV-Format zu erstellen.

   Beispiel: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` erstellt eine Datei wie 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Planen Sie die Ausführung des Berichts zu einem bestimmten Zeitpunkt.

   Die Berichte werden innerhalb einer Stunde nach Abschluss an das FTP-Konto gesendet.

>[!NOTE]
>
>* Um ausgefüllte Berichte per E-Mail zu senden, geben Sie beim Generieren des Berichts oder der Vorlage einfach die Adressen aller E-Mail-Empfänger ein.
>* Berichte werden gemäß ihren festgelegten Zeitplänen ausgeführt und innerhalb einer Stunde nach Abschluss an das FTP-Konto gesendet.

## Zugreifen auf Berichte in einem FTP-Repository

Um auf Ihre Berichte zuzugreifen, stellen Sie eine Verbindung mit einem der folgenden FTP-Hosts her, indem Sie die Anmeldedaten für Ihr FTP-Konto (`amo<userID>rpt`. B. amo1234rpt) und entweder ein Kennwort oder einen privaten Verbindungsschlüssel verwenden, falls einer eingerichtet ist:

* Internationale Kunden: `ftp3.adobe.net`
* US-Kunden: `ftp5.adobe.net`

>[!NOTE]
>
>Das Reporting-Repository ist schreibgeschützt und wird alle 15 Tage bereinigt.


>[!MORELIKETHIS]
>
>* [Erstellen einer Berichtsvorlage](/help/search-social-commerce/reports/automation/templates/template-create.md)
