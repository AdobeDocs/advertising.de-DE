---
title: Häufig gestellte Fragen zum Tracking
description: Erfahren Sie Antworten auf häufige Fragen zum Tracking, einschließlich der Fehlerbehebung.
exl-id: e5302c09-0b40-47ae-bc88-9299e6bd3044
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---

# Häufig gestellte Fragen zum Tracking

## Tracking-Funktionen

+++Kann ich Kampagnen verfolgen, die von Adobe Advertising nicht verwaltet werden?

Ja. Wenn Search, Social und Commerce eines Ihrer Werbenetzwerkkonten synchronisiert, werden die Klickdaten des Werbenetzwerks für alle [unterstützten Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) in diesem Konto verfolgt. Es verfolgt auch Konversionsdaten, wenn Sie die Weiterleitung von Search, Social und Commerce zu Ihren Anzeigen- und/oder Keyword-Ziel-URLs oder Tracking-Vorlagen hinzugefügt und das Konversions-Tracking auf Ihren Konversionsseiten implementiert haben. Klären Sie mit Ihrem Adobe-Account-Team, welche Kampagnen Search, Social und Commerce einfach verfolgen sollen und welche Sie verwalten möchten.
+++

+++Wie erhalte ich die Attribution mehrerer Ereignisse?

Für Werbetreibende, die Konversionsverfolgungstags für Suche, Social und Commerce oder Adobe Analytics verwenden, bietet Adobe Advertising mehrere Optionen für die Zuordnung von Konversionsdaten über eine Reihe von Ereignissen hinweg, die zu einer Konversion führen. Eine Einstellung auf Advertiser-Ebene bestimmt, wie Konversionsdaten ereignisübergreifend zugeordnet werden, selbst wenn sie über mehrere Anzeigenkanäle hinweg auftreten, solange die Kanäle die Impression-Nachverfolgung auf Ereignisebene ermöglichen. Standardmäßig werden Konversionen dem letzten (letzten) Ereignis zugeordnet. Die Einstellung kann jedoch anders konfiguriert werden, z. B. um Konversionen dem ersten Ereignis zuzuordnen oder alle Ereignisse gleichmäßig zu gewichten. Das Ändern der Attributionsregel wirkt sich darauf aus, wie zukünftige Gebote berechnet werden.

Werbetreibende, die alle Konversionsdaten in einer Feed-Datei bereitstellen, müssen die Konversion den zugehörigen Transaktionsereignissen selbst zuordnen.

>[!NOTE]
>
>In Ansichten, Berichten zur Kampagnenverwaltung und Portfolioverwaltung sowie in benutzerdefinierten Simulationen (für einige Benutzer verfügbar) können Sie die Regel ändern, mit der Konversionsdaten in den Ansichten und Berichtsergebnissen zugeordnet werden, ohne die Berechnung künftiger Gebote zu beeinflussen.

+++

+++Wie erkennt Adobe Advertising doppelte Transaktionen?

Doppelte Transaktionen können auftreten, wenn ein Benutzer die Bestätigungsseite nach Abschluss einer Transaktion aktualisiert. Adobe Advertising verwendet das `ev_transid`-Attribut, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu eliminieren.

Im Folgenden finden Sie eine Deduplizierungslogik für Adobe Advertising:

* **Wenn ein Client einen Wert für das `ev_transid`-Attribut sendet:** Nachfolgende Pixelanfragen werden als Duplikate der vorherigen betrachtet, wenn Folgendes alle gleich sind: die `ev_transid`, die Tracking-ID für dasselbe Keyword, dieselbe Anzeige oder dieselbe Platzierung und der Wert für eine bestimmte Konversionsmetrik.

  Wenn beispielsweise mehrere Kreditanträge dieselbe Antragskennung und denselben Darlehensbetrag für dasselbe Keyword in einem bestimmten Werbenetzwerk haben, werden sie als Duplikate betrachtet und nur der erste Kreditantrag wird gezählt.

* **Wenn ein Client keinen Wert für das `ev_transid` sendet:** Nachfolgende Transaktionen werden als Duplikate der vorherigen betrachtet, wenn sie eine Tracking-ID für dasselbe Keyword, dieselbe Anzeige oder dieselbe Platzierung verwenden; und denselben Wert für eine bestimmte Konversionsmetrik.

  Wenn beispielsweise mehrere Kreditanträge dieselbe Keyword-ID und denselben Darlehensbetrag haben, werden sie als Duplikate betrachtet, und nur der erste Kreditantrag wird gezählt.
+++

## Typen der Tracking-Implementierung

+++Ich möchte den Adobe Advertising-Konversionsverfolgungs-Service für eine oder mehrere Kampagnen oder Konten nicht mehr verwenden. Wie kann ich den Trackingcode schnell aus den Tracking-URLs entfernen?

Wenden Sie sich zunächst an Ihr Adobe-Account-Team, um die Auswirkungen des Entfernens von Tracking-URLs zu verstehen.

Ändern Sie im Konto oder in der Kampagne die Tracking-Methode in &quot;[!UICONTROL No EF Redirect]&quot;. Erstellen Sie dann eine Bulksheet mit der Option &quot;[!UICONTROL Generate Tracking URLs]&quot; und veröffentlichen Sie sie im Anzeigennetzwerk. Alle vorhandenen Tracking-URLs oder Ziel-URLs werden ersetzt.
+++

## Datenfragen

+++Wie weiß ich, welche Konversionsmetrik von einem Daten-Feed stammt oder vom Adobe Advertising-Konversions-Tracking-Tag verfolgt wird?

In einem [!UICONTROL Transaction Report] können Sie erkennen, ob eine eingeschlossene Konversionsmetrik vom Adobe Advertising-Konversionsverfolgungspixel verfolgt wurde, wenn Sie die benutzerdefinierte Spalte &quot;[!UICONTROL Tracking URL]&quot; einbeziehen. Tracking-URLs mit dem Adobe Advertising-Tracking-Pixel beginnen mit `http://pixel.everesttech.net`.
+++

+++Was sind verwaiste Transaktionen?

Verwaiste Transaktionen sind Transaktionsereignisse, die nicht mit einem bestimmten Keyword oder einer bestimmten Anzeige verknüpft werden können. Adobe Advertising ordnet Transaktion/Umsatz einem Keyword oder einer Anzeige zu, indem die mit dem Umsatzereignis empfangenen Tracking-IDs mit der eindeutigen Tracking-ID in der Tracking-URL des Keywords oder der Anzeige abgeglichen werden.

Wenn ein Adobe-Account-Team vermutet, dass verwaiste Transaktionen für einen Umsatzrückgang verantwortlich sind, sucht das Kundenunterstützungs-Team nach Waisen und untersucht das Problem, falls es welche findet.

Waisen treten in den folgenden Situationen auf.

**Pixel-Implementierungen**

Verwaiste Transaktionen treten bei Pixelimplementierungen fast nie auf. Pixel-Waisen sind jedoch aufgetreten, wenn:

* Die Klickdaten sind für das Klickdatum der Konvertierung nicht verfügbar. In diesem Fall werden die Daten zurückzugeordnet, wenn Search, Social und Commerce die Klickdaten aus dem Werbenetzwerk abrufen.

* Die Klicklogs werden nicht vor den Konversionsprotokollen verarbeitet.

**Feed-Implementierungen**

* Die Tracking-ID, die im Feed gesendet wird, stammt aus einem Konto, von dem Search, Social und Commerce nichts wissen.

* Das Konto ist nicht synchronisiert oder während des Synchronisierungsprozesses sind Fehler aufgetreten.

* Die Tracking-ID wurde hinzugefügt und aus dem Anzeigennetzwerk entfernt, während Search, Social und Commerce nicht mit dem Anzeigennetzwerk synchronisiert waren, sodass Search, Social und Commerce keine Informationen über die ID haben. Dieses Problem verursacht weiterhin verwaiste Einnahmen, wenn es zu einer Verzögerung beim Empfang von Einnahmen kommt.

* Der Client hat eine Tracking-ID gesendet, die im Feed falsch formatiert ist und nicht mit der Tracking-ID in der URL übereinstimmt. Dies geschieht normalerweise aufgrund eines Formatierungsproblems oder wenn Tracking-IDs im Feed gekürzt werden.

* In der Konfigurationsdatei ist der reguläre Ausdruck, der zum Extrahieren der Tracking-ID aus den URLs verwendet wird, falsch oder veraltet. Manchmal ändert der Werbetreibende die Tracking-ID in der URL oder verwendet ein völlig neues Tracking-System, was erfordert, dass das Implementierungs-Team für Search, Social und Commerce den regulären Ausdruck aktualisiert. In solchen Fällen ist ein Großteil der Einnahmen verwaist.

**Feed-Implementierungen mit einer Transaktions-ID**

Vor den Daten, für die Daten im Offline-Feed verfügbar sind, sind keine Online-Transaktionen verfügbar.

**Feed-Implementierungen mit einem Token (ef_id)**

Search, Social und Commerce finden keinen entsprechenden Klick auf dem Server oder im Werbenetzwerk. Dies kann daran liegen, dass die Klickdaten für das Klickdatum der Konversion nicht verfügbar sind oder (selten) daran, dass die Klickprotokolle vor den Konversionsprotokollen nicht verarbeitet wurden. Wenn Search, Social und Commerce die Klickdaten vom Anzeigennetzwerk erhalten oder die Klickprotokolle verarbeitet werden, werden die Daten der Konversion zugeordnet.
+++

## Probleme bei der Umsatzverfolgung

+++Wie korrigiere ich alte/falsche Daten aus einer Feed-Datei?

Wenden Sie sich mit der korrigierten Datendatei an die Kundenunterstützung.
+++

+++Mehrere Schlüsselwörter haben dieselben Tracking-URLs.

**Implikationen**

Bei Feed-Implementierungen mit mehreren Tracking-IDs werden Daten mit mehreren Keywords gemeldet. Bei anderen Implementierungen können Konversionen dem falschen Keyword zugeordnet werden, da das System einem der Keywords willkürlich eine Konvertierung zuweist.

**Mögliche Ursache**

Die URL für ein neues Keyword oder eine neue Anzeige wurde aus einem anderen Keyword oder einer anderen Anzeige kopiert.

Dies sollte nicht mit Display- oder Social-Media-Anzeigen geschehen.

**Mögliche Lösung oder Problemumgehung**

* Wenn Sie Ihre eigenen Keywords und Anzeigen verwalten, erstellen Sie eine Bulksheet-Datei mit den richtigen URLs für die doppelten URLs und veröffentlichen Sie sie mit der Option **[!UICONTROL Generate Tracking URLs]** im entsprechenden Konto, wodurch die URLs für alle Keywords und Anzeigen neu generiert werden.

* Wenn ein Adobe-Account-Team Ihre Keywords verwaltet, bitten Sie es, neue URLs für die doppelten URLs zu erstellen.
+++
