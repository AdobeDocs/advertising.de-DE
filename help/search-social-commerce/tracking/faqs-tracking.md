---
title: Häufig gestellte Fragen zum Tracking
description: Erfahren Sie mehr über Antworten auf häufig gestellte Fragen zum Tracking, einschließlich Fehlerbehebungsproblemen.
source-git-commit: f5e2044af460ebf561e075ed6b1fb057ed47acc3
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Häufig gestellte Fragen zum Tracking

## Tracking-Funktionen

++ Kann ich Kampagnen nachverfolgen, die von Adobe Advertising nicht verwaltet werden?

Ja. Wenn Search, Social und Commerce eines Ihrer Anzeigennetzwerkkonten synchronisiert, werden die Klickdaten des Anzeigennetzwerks für alle [unterstützte Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) in diesem Konto. Sie verfolgt auch die Konversionsdaten, wenn Sie die Umleitung &quot;Search, Social, &amp; Commerce&quot;zu Ihren Anzeigen- und/oder Keyword-Ziel-URLs oder Tracking-Vorlagen hinzugefügt und die Konversions-Tracking in Ihre Konversionsseiten implementiert haben. Machen Sie sich mit Ihrem Adobe Account Team klar, welche Kampagnen Sie in Search, Social und Commerce einfach verfolgen möchten und welche Sie verwalten möchten.
+++

+++ Wie erhalte ich eine Zuordnung für mehrere Ereignisse?

Für Advertiser, die Konversions-Tracking-Tags für Suche, Social, &amp; Commerce oder Adobe Analytics verwenden, bietet Adobe Advertising mehrere Optionen für die Zuordnung von Konversionsdaten aus einer Reihe von Ereignissen, die zu einer Konversion führen. Mit einer Einstellung auf Advertiser-Ebene wird bestimmt, wie Konversionsdaten ereignisübergreifend zugeordnet werden, selbst wenn sie über mehrere Anzeigenkanäle hinweg auftreten, solange die Kanäle das Impression-Tracking auf Ereignisebene ermöglichen. Standardmäßig werden Konversionen dem letzten (letzten) Ereignis zugeordnet. Die Einstellung kann jedoch anders konfiguriert werden, z. B. um Konversionen dem ersten Ereignis zuzuordnen oder alle Ereignisse gleichmäßig zu gewichten. Eine Änderung der Zuordnungsregel wirkt sich auf die Berechnung künftiger Angebote aus.

Werbetreibende, die alle Konversionsdaten in einer Feed-Datei bereitstellen, müssen die Konversion den zugehörigen Transaktionsereignissen selbst zuordnen.

>[!NOTE]
>
>In den Ansichten, Berichten und benutzerdefinierten Simulationen für Kampagnenverwaltung und Portfoliomanagement können Sie die Regel ändern, mit der Konversionsdaten in den Ansichten und Berichtsergebnissen zugeordnet werden, ohne dass sich dies auf die Berechnung künftiger Angebote auswirkt.

+++

+++ Wie erkennt Adobe Advertising doppelte Transaktionen?

Duplizierte Transaktionen können auftreten, wenn ein Benutzer die Bestätigungsseite nach Abschluss einer Transaktion aktualisiert. Adobe Advertising verwendet die `ev_transid` -Attribut verwenden, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu vermeiden.

Im Folgenden finden Sie die Deduplizierungslogik des Adobe Advertisings:

* **Wenn ein Client einen Wert für die `ev_transid` Attribut:** Nachfolgende Pixelanforderungen werden als Duplikate der vorherigen betrachtet, wenn die folgenden identisch sind: die `ev_transid`; die Tracking-ID für denselben Suchbegriff, dieselbe Anzeige oder dieselbe Platzierung; und den Wert für eine bestimmte Transaktionseigenschaft.

  Wenn beispielsweise mehrere Kreditanträge dieselbe Anwendungs-ID und denselben Darlehensbetrag für denselben Suchbegriff in einem bestimmten Werbenetzwerk haben, werden sie als Duplikate betrachtet und nur der erste Kreditantrag wird gezählt.

* **Wenn ein Client keinen Wert für die `ev_transid` Attribut:** Nachfolgende Transaktionen werden als Duplikate der vorherigen Transaktion betrachtet, wenn sie eine Tracking-ID für denselben Suchbegriff, dieselbe Anzeige oder dieselbe Platzierung gemeinsam haben. und denselben Wert für eine bestimmte Transaktionseigenschaft.

  Wenn beispielsweise mehrere Kreditanträge dieselbe Schlüsselwort-ID und denselben Darlehensbetrag aufweisen, werden sie als Duplikate betrachtet und nur der erste Kreditantrag wird gezählt.
+++

## Typen der Tracking-Implementierung

+++ Ich möchte den Adobe Advertising Conversion-Tracking-Dienst nicht mehr für eine oder mehrere Kampagnen oder Konten verwenden. Wie kann ich den Trackingcode schnell aus den Tracking-URLs entfernen?

Wenden Sie sich zunächst an Ihr Adobe-Kundenbetreuungsteam, um die Auswirkungen des Entfernens von Tracking-URLs zu verstehen.

Ändern Sie die Tracking-Methode im Konto oder in der Kampagne in &quot;[!UICONTROL No EF Redirect].&quot; Erstellen Sie dann ein Bulksheet mit dem[!UICONTROL Generate Tracking URLs]und veröffentlichen Sie sie im Werbenetzwerk. Alle vorhandenen Tracking-URLs oder Ziel-URLs werden ersetzt.
+++

## Datenfragen

+++ Woher weiß ich, welche Transaktionseigenschaft aus einem Daten-Feed stammt oder vom Adobe Advertising-Konversions-Tracking-Tag verfolgt wird?

In [!UICONTROL Transaction Report]können Sie feststellen, ob eine enthaltene Transaktionseigenschaft vom Adobe Advertising-Konversions-Tracking-Pixel verfolgt wurde, wenn Sie die benutzerdefinierte Spalte &quot;[!UICONTROL Tracking URL].&quot; Tracking-URLs mit dem Adobe Advertising-Tracking-Pixel beginnen mit `http://pixel.everesttech.net`.
+++

+++ Was sind verwaiste Transaktionen?

Verwaiste Transaktionen sind Transaktionsereignisse, die nicht mit einem bestimmten Suchbegriff oder einer bestimmten Anzeige verknüpft werden können. Adobe Advertising ordnet Transaktionen/Umsätze einem Suchbegriff oder einer Anzeige zu, indem sie die mit dem Umsatzereignis empfangenen Tracking-IDs mit der eindeutigen Tracking-ID in der Tracking-URL des Suchbegriffs oder der Anzeige abgleichen.

Wenn ein Kundenbetreuungsteam vermutet, dass verwaiste Transaktionen für einen Umsatzrückgang verantwortlich sind, prüft das Kundenunterstützungsteam nach Waisen und untersucht das Problem, falls es solche findet.

In den folgenden Situationen treten Waisen auf.

**Pixel-Implementierungen**

Verwaiste Transaktionen treten bei Pixelimplementierungen fast nie auf. Pixelverwaiste treten jedoch auf, wenn:

* Die Klickdaten sind für das Klickdatum der Konversion nicht verfügbar. In diesem Fall werden die Daten wieder zugeordnet, wenn Search, Social und Commerce die Klickdaten aus dem Werbenetzwerk abrufen.

* Die Klickprotokolle werden nicht vor den Konvertierungsprotokollen verarbeitet.

**Feed-Implementierungen**

* Die im Feed gesendete Tracking-ID stammt aus einem Konto, von dem Search, Social und Commerce nichts weiß.

* Das Konto ist nicht synchron oder während des Synchronisierungsprozesses sind Fehler aufgetreten.

* Die Tracking-ID wurde hinzugefügt und aus dem Werbenetzwerk entfernt, während Search, Social und Commerce nicht mit dem Werbenetzwerk synchronisiert waren. Daher enthält Search, Social und Commerce keine Informationen über die ID. Dieses Problem führt weiterhin zu verwaisten Umsätzen, wenn sich der Umsatzempfang verzögert.

* Der Client hat eine Tracking-ID gesendet, die im Feed falsch formatiert ist und nicht mit der Tracking-ID in der URL übereinstimmt. Dies tritt normalerweise aufgrund eines Formatierungsproblems oder der Abkürzung von Tracking-IDs im Feed auf.

* In der Konfigurationsdatei ist der reguläre Ausdruck, mit dem die Tracking-ID aus den URLs extrahiert wird, falsch oder veraltet. Manchmal ändert der Advertiser die Tracking-ID in der URL oder verwendet ein völlig neues Tracking-System. Dazu muss das Implementierungsteam von Search, Social und Commerce den regulären Ausdruck aktualisieren. In solchen Fällen ist ein Großteil des Umsatzes verwaist.

**Feed-Implementierungen mit einer Transaktions-ID**

Vor dem Datum, für das Daten im Offline-Feed verfügbar sind, sind keine Online-Transaktionen verfügbar.

**Feed-Implementierungen mit einem Token (ef_id)**

In Search, Social und Commerce kann ein entsprechender Klick auf den Server oder das Werbenetzwerk nicht gefunden werden. Dies kann daran liegen, dass die Klickdaten für das Klickdatum der Konversion nicht verfügbar sind oder (selten), da die Klickprotokolle nicht vor den Konversionsprotokollen verarbeitet wurden. Wenn Search, Social und Commerce die Klickdaten aus dem Anzeigennetzwerk erhalten oder die Klicklogs verarbeitet werden, werden die Daten der Konversion zugeordnet.
+++

## Probleme bei der Umsatzverfolgung

+++ Wie repariere ich alte/falsche Daten aus einer Feed-Datei?

Wenden Sie sich an die Kundenunterstützung mit der korrigierten Datendatei.
+++

+++Mehrere Suchbegriffe haben dieselben Tracking-URLs.

**Auswirkungen**

Bei Feed-Implementierungen mit mehreren Tracking-IDs werden Daten für mehrere Keywords gemeldet. Bei anderen Implementierungen können Konversionen dem falschen Suchbegriff zugeordnet werden, da das System eine Konvertierung willkürlich einem der Suchbegriffe zuweist.

**Mögliche Ursache**

Die URL für einen neuen Suchbegriff oder eine neue Anzeige wurde aus einem anderen Suchbegriff oder einer anderen Anzeige kopiert.

Das sollte nicht bei Display- oder Social-Anzeigen passieren.

**Mögliche Lösung oder Problemumgehung**

* Wenn Sie Ihre eigenen Suchbegriffe und Anzeigen verwalten, erstellen Sie eine Bulksheet-Datei mit den richtigen URLs für die doppelten URLs und posten Sie sie mit dem **[!UICONTROL Generate Tracking URLs]** -Option, die URLs für alle Suchbegriffe und Anzeigen neu generiert.

* Wenn ein Adobe Account Team Ihre Suchbegriffe verwaltet, bitten Sie sie, neue URLs für die doppelten URLs zu erstellen.
+++
