---
title: Häufig gestellte Fragen zum Tracking
description: Erfahren Sie mehr über Antworten auf häufig gestellte Fragen zum Tracking, einschließlich Fehlerbehebungsproblemen.
exl-id: e5302c09-0b40-47ae-bc88-9299e6bd3044
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---

# Häufig gestellte Fragen zum Tracking

## Tracking-Funktionen

+++ Kann ich Kampagnen verfolgen, die von Adobe Advertising nicht verwaltet werden?

Ja. Wenn Search, Social und Commerce eines Ihrer Anzeigennetzwerkkonten synchronisieren, werden die Klickdaten des Anzeigennetzwerks für alle [unterstützten Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) in diesem Konto verfolgt. Sie verfolgt auch die Konversionsdaten, wenn Sie die Umleitung von Search, Social und Commerce zu Ihren Anzeigen- und/oder Keyword-Ziel-URLs oder Tracking-Vorlagen hinzugefügt und das Konversions-Tracking in Ihre Konversionsseiten implementiert haben. Machen Sie sich mit Ihrem Adobe Account-Team klar, welche Kampagnen Sie in Search, Social und Commerce einfach nachverfolgen möchten und welche Kampagnen Sie verwalten möchten.
+++

+++ Wie erhalte ich eine Zuordnung für mehrere Ereignisse?

Für Advertiser, die Konversions-Tracking-Tags für Search, Social und Commerce oder Adobe Analytics verwenden, bietet Adobe Advertising mehrere Optionen für die Zuordnung von Konversionsdaten aus einer Reihe von Ereignissen, die zu einer Konversion führen. Mit einer Einstellung auf Advertiser-Ebene wird bestimmt, wie Konversionsdaten ereignisübergreifend zugeordnet werden, selbst wenn sie über mehrere Anzeigenkanäle hinweg auftreten, solange die Kanäle das Impression-Tracking auf Ereignisebene ermöglichen. Standardmäßig werden Konversionen dem letzten (letzten) Ereignis zugeordnet. Die Einstellung kann jedoch anders konfiguriert werden, z. B. um Konversionen dem ersten Ereignis zuzuordnen oder alle Ereignisse gleichmäßig zu gewichten. Eine Änderung der Zuordnungsregel wirkt sich auf die Berechnung künftiger Angebote aus.

Werbetreibende, die alle Konversionsdaten in einer Feed-Datei bereitstellen, müssen die Konversion den zugehörigen Transaktionsereignissen selbst zuordnen.

>[!NOTE]
>
>In den Ansichten, Berichten und benutzerdefinierten Simulationen für Kampagnenverwaltung und Portfoliomanagement können Sie die Regel ändern, mit der Konversionsdaten in den Ansichten und Berichtsergebnissen zugeordnet werden, ohne dass sich dies auf die Berechnung künftiger Angebote auswirkt.

+++

+++Wie erkennt Adobe Advertising doppelte Transaktionen?

Duplizierte Transaktionen können auftreten, wenn ein Benutzer die Bestätigungsseite nach Abschluss einer Transaktion aktualisiert. Adobe Advertising verwendet das Attribut `ev_transid` , um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu vermeiden.

Im Folgenden finden Sie eine Adobe Advertising der Deduplizierungslogik:

* **Wenn ein Client einen Wert für das Attribut `ev_transid` sendet:** Nachfolgende Pixelanfragen werden als Duplikate der vorherigen betrachtet, wenn die folgenden Elemente identisch sind: die `ev_transid`, die Tracking-ID für denselben Suchbegriff, dieselbe Anzeige oder Platzierung und der Wert für eine bestimmte Konversionsmetrik.

  Wenn beispielsweise mehrere Kreditanträge dieselbe Anwendungs-ID und denselben Darlehensbetrag für denselben Suchbegriff in einem bestimmten Werbenetzwerk haben, werden sie als Duplikate betrachtet und nur der erste Kreditantrag wird gezählt.

* **Wenn ein Client keinen Wert für das Attribut `ev_transid` sendet:** Nachfolgende Transaktionen werden als Duplikate der vorherigen Transaktion betrachtet, wenn sie eine Tracking-ID für denselben Suchbegriff, dieselbe Anzeige oder dieselbe Platzierung gemeinsam haben, und denselben Wert für eine bestimmte Konversionsmetrik.

  Wenn beispielsweise mehrere Kreditanträge dieselbe Schlüsselwort-ID und denselben Darlehensbetrag aufweisen, werden sie als Duplikate betrachtet und nur der erste Kreditantrag wird gezählt.
+++

## Typen der Tracking-Implementierung

+++ Ich möchte die Verwendung des Adobe Advertising-Konversions-Tracking-Dienstes für eine oder mehrere Kampagnen oder Konten beenden. Wie kann ich den Trackingcode schnell aus den Tracking-URLs entfernen?

Wenden Sie sich zunächst an Ihr Adobe-Account-Team, um zu erfahren, welche Auswirkungen das Entfernen von Tracking-URLs hat.

Ändern Sie die Tracking-Methode im Konto oder in der Kampagne in &quot;[!UICONTROL No EF Redirect]&quot;. Erstellen Sie dann ein Bulksheet mit der Option &quot;[!UICONTROL Generate Tracking URLs]&quot; und posten Sie es im Werbenetzwerk. Alle vorhandenen Tracking-URLs oder Ziel-URLs werden ersetzt.
+++

## Datenfragen

+++ Wie weiß ich, welche Konversionsmetrik aus einem Daten-Feed stammt oder vom Adobe Advertising-Konversions-Tracking-Tag verfolgt wird?

In einem [!UICONTROL Transaction Report] können Sie feststellen, ob eine enthaltene Konversionsmetrik vom Adobe Advertising-Konversions-Tracking-Pixel verfolgt wurde, wenn Sie die benutzerdefinierte Spalte &quot;[!UICONTROL Tracking URL]&quot; einschließen. Tracking-URLs mit dem Adobe Advertising-Tracking-Pixel beginnen mit `http://pixel.everesttech.net`.
+++

+++ Was sind verwaiste Transaktionen?

Verwaiste Transaktionen sind Transaktionsereignisse, die nicht mit einem bestimmten Suchbegriff oder einer bestimmten Anzeige verknüpft werden können. Adobe Advertising ordnet Transaktionen/Umsätze einem Suchbegriff oder einer Anzeige zu, indem die mit dem Umsatzereignis empfangenen Tracking-IDs mit der eindeutigen Tracking-ID in der Tracking-URL des Suchbegriffs oder der Anzeige abgeglichen werden.

Wenn ein Adobe-Account-Team vermutet, dass verwaiste Transaktionen für einen Umsatzrückgang verantwortlich sind, sucht das Kundenunterstützungsteam nach Waisen und untersucht das Problem, falls es welche findet.

In den folgenden Situationen treten Waisen auf.

**Pixel-Implementierungen**

Verwaiste Transaktionen treten bei Pixelimplementierungen fast nie auf. Pixelverwaiste treten jedoch auf, wenn:

* Die Klickdaten stehen für das Klickdatum der Konversion nicht zur Verfügung. In diesem Fall werden die Daten wieder zugeordnet, wenn Search, Social und Commerce die Klickdaten aus dem Werbenetzwerk abrufen.

* Die Klickprotokolle werden nicht vor den Konvertierungsprotokollen verarbeitet.

**Feed-Implementierungen**

* Die im Feed gesendete Tracking-ID stammt aus einem Konto, von dem Search, Social und Commerce nichts wissen.

* Das Konto ist nicht synchron oder während des Synchronisierungsprozesses sind Fehler aufgetreten.

* Die Tracking-ID wurde hinzugefügt und aus dem Werbenetzwerk entfernt, während Search, Social und Commerce nicht mit dem Werbenetzwerk synchronisiert waren. Daher enthält Search, Social und Commerce keine Informationen über die ID. Dieses Problem führt weiterhin zu verwaisten Umsätzen, wenn sich der Umsatzempfang verzögert.

* Der Client hat eine Tracking-ID gesendet, die im Feed falsch formatiert ist und nicht mit der Tracking-ID in der URL übereinstimmt. Dies tritt normalerweise aufgrund eines Formatierungsproblems oder der Abkürzung von Tracking-IDs im Feed auf.

* In der Konfigurationsdatei ist der reguläre Ausdruck, mit dem die Tracking-ID aus den URLs extrahiert wird, falsch oder veraltet. Manchmal ändert der Advertiser die Tracking-ID in der URL oder verwendet ein völlig neues Tracking-System. Dazu muss das Implementierungsteam von Search, Social und Commerce den regulären Ausdruck aktualisieren. In solchen Fällen ist ein Großteil des Umsatzes verwaist.

**Feed-Implementierungen mit einer Transaktions-ID**

Vor dem Datum, für das Daten im Offline-Feed verfügbar sind, sind keine Online-Transaktionen verfügbar.

**Feed-Implementierungen mit einem Token (ef_id)**

Search, Social und Commerce können einen entsprechenden Klick auf den Server oder das Werbenetzwerk nicht finden. Dies kann daran liegen, dass die Klickdaten für das Klickdatum der Konversion nicht verfügbar sind oder (selten), da die Klickprotokolle nicht vor den Konversionsprotokollen verarbeitet wurden. Wenn Search, Social und Commerce die Klickdaten aus dem Anzeigennetzwerk erhalten oder die Klicklogs verarbeitet werden, werden die Daten der Konversion zugeordnet.
+++

## Probleme bei der Umsatzverfolgung

+++ Wie repariere ich alte/falsche Daten aus einer Feed-Datei?

Wenden Sie sich an die Kundenunterstützung mit der korrigierten Datendatei.
+++

+++Mehrere Suchbegriffe haben dieselben Tracking-URLs.

**Implikationen**

Bei Feed-Implementierungen mit mehreren Tracking-IDs werden Daten für mehrere Keywords gemeldet. Bei anderen Implementierungen können Konversionen dem falschen Suchbegriff zugeordnet werden, da das System eine Konvertierung willkürlich einem der Suchbegriffe zuweist.

**Mögliche Ursache**

Die URL für einen neuen Suchbegriff oder eine neue Anzeige wurde aus einem anderen Suchbegriff oder einer anderen Anzeige kopiert.

Das sollte nicht bei Display- oder Social-Anzeigen passieren.

**Mögliche Lösung oder Problemumgehung**

* Wenn Sie Ihre eigenen Suchbegriffe und Anzeigen verwalten, erstellen Sie eine Bulksheet-Datei mit den richtigen URLs für die doppelten URLs und posten Sie sie mithilfe der Option **[!UICONTROL Generate Tracking URLs]** für das entsprechende Konto, wodurch URLs für alle Suchbegriffe und Anzeigen neu generiert werden.

* Wenn ein Adobe-Account-Team Ihre Suchbegriffe verwaltet, bitten Sie sie, neue URLs für die doppelten URLs zu erstellen.
+++
