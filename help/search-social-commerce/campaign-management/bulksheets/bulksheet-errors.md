---
title: Massenblatt-Fehler
description: Referenzpotenzielle Gründe für jeden Bulksheet-Fehler.
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# Massenblatt-Fehler

&quot;Search&quot;, &quot;Social&quot;und &quot;Commerce&quot;generieren zwei Arten von Fehlerdateien während des Bulksheet-Vorgangs:

* **SE-Fehler:** Wenn eine Datei gepostet wird, das Werbenetzwerk jedoch nicht alle Daten akzeptiert, wird eine Fehlerdatei mit dem Namen `<uploaded file name>_se_errors.<extension used for the bulksheet>` erstellt. Wenn einige, aber nicht alle Zeilen akzeptiert wurden, zeigt die Fehlerdatei die Zeilen an, die nicht veröffentlicht wurden, und eine Erläuterung jedes Fehlers, damit Sie ihn korrigieren können. Die Fehler sind in der Spalte &quot;[!UICONTROL SE Error Message]&quot; enthalten.

>[!NOTE]
>
>Wenn Sie [!DNL Google Ads]-Anzeigen posten, die gegen die Werberichtlinien des Werbenetzwerks verstoßen, aber für Ausnahmen infrage kommen, werden diese Anzeigen automatisch mit Freistellungsanfragen neu gepostet. Wenn die Ausnahmeanfrage fehlschlägt, werden Informationen über die Verletzung in die Fehlerdatei aufgenommen.

* **EF-Fehler:** Wenn der Bulksheet-Vorgang keine Datei oder einzelne Zeilen in der Datei hochladen oder verarbeiten kann, wird eine Fehlerdatei mit dem Namen `<uploaded file name>_ef_errors.<extension used for the bulksheet>` erstellt. Wenn das Problem mit einzelnen Zeilen auftritt, werden diese Zeilen einbezogen.
mit einer Erläuterung jedes Fehlers, damit Sie ihn korrigieren können. Die Fehler sind in der Spalte &quot;[!UICONTROL EF Error Message]&quot; enthalten.

## [!UICONTROL SE Error] Nachrichten

Fehler in der Spalte [!UICONTROL SE Error] stammen direkt aus dem Werbenetzwerk.

## [!UICONTROL EF Error] Nachrichten

Die folgenden Fehler können in die Spalte [!UICONTROL EF Error] in den Dateien [!UICONTROL EF Errors] aufgenommen werden.

### Fehler herunterladen/erstellen

| Kategorie | Nachricht | Beschreibung |
|----|----|----|
| Allgemein | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Der Vorgang ist aufgrund eines nicht kategorisierten oder nicht verarbeiteten Fehlers vollständig fehlgeschlagen. Wenn das Problem weiterhin besteht, wenden Sie sich an Ihr Adobe-Account-Team, um die Ursache zu untersuchen. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Search, Social und Commerce konnten nicht mit dem Anzeigennetzwerk synchronisieren, bevor das Bulksheet erstellt wurde. Daher wurde kein Bulksheet erstellt. Wenn das Problem weiterhin besteht, wenden Sie sich an Ihr Adobe-Account-Team. |

### Fehler hochladen

| Kategorie | Nachricht | Beschreibung |
|----|----|----|
| Allgemein | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | Der Vorgang ist vollständig fehlgeschlagen. Wenn das Problem weiterhin besteht, wenden Sie sich an Ihr Adobe-Account-Team. |
| Alle Entitäten | [!UICONTROL Invalid Fields.] \[ungültige Felder und Fehler\] | Die angegebenen Daten fehlen oder sind ungültig. |
|  | [!UICONTROL Invalid Reference Given] | Die ID der Entität im Werbenetzwerk oder die ID einer übergeordneten Entität (z. B. die Konto-ID) entspricht keiner Entität in Search, Social und Commerce. Dies kann vorkommen, wenn Sie die ID im Bulksheet bearbeitet haben. |
|  | [!UICONTROL <Entity> is deleted or expired] | Die Entität ist abgelaufen oder wurde gelöscht und Sie können ihre Eigenschaften nicht ändern. Die Entität kann gelöscht werden, wenn jemand den Status manuell bearbeitet hat. |
|  | [!UICONTROL <Entity> status should be Active or Paused] | (Neue Entitäten) Eine neue Entität kann nur &quot;Aktiv&quot;oder &quot;Angehalten&quot;sein. |
|  | [!UICONTROL Duplicate Entries are present] | Für dieselbe Entität werden mehrere Zeilen mit unterschiedlichen Attributen in jeder Zeile einbezogen. Zusammenfassen der Änderungen in einer Zeile |
|  | [!UICONTROL Invalid AMO ID given] | Die AMO-ID für die Zeile ist nicht vorhanden. Dies kann vorkommen, wenn Sie die ID im Bulksheet bearbeitet haben. |
|  | [!UICONTROL Invalid row given] | Die Zeile enthält nicht genügend Informationen, um den Entitätstyp zu bestimmen. Bearbeiten Sie die Zeile, um alle erforderlichen Felder für den Entitätstyp einzuschließen. |
| Konten | [!UICONTROL Provide Valid Account Details] | (Bulksheets für mehrere Konten) Kontokennungen sind nicht in allen Zeilen enthalten. Geben Sie Werte für eine der folgenden Kombinationen von Spalten für jede Zeile ein: a) &quot;[!UICONTROL AMO ID]&quot;oder b) &quot;[!UICONTROL Account Name]&quot;und &quot;[!UICONTROL Platform]&quot;. |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search, Social und Commerce haben keinen Zugriff auf das Anzeigennetzwerkkonto, sodass Sie keine Kampagnendaten erstellen oder bearbeiten können. Stellen Sie sicher, dass die Anmeldeinformationen für das Suchkonto korrekt sind und dass das Konto aktiviert ist. |
| Kampagne | [!UICONTROL Invalid Shopping Country specified] | (Shopping-Kampagnen) Der Wert im Feld &quot;[!UICONTROL Sales Country]&quot; ist ungültig. Eine Liste der gültigen Länder sehen [für  [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) und [für  [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| Alle Kampagnenkomponenten | [!UICONTROL Campaign creation failed] | Die übergeordnete Kampagne wurde nicht erstellt, sodass diese Entität nicht erstellt wurde. Stellen Sie sicher, dass alle übergeordneten Entitäten alle erforderlichen Felder enthalten. |
| Anzeigengruppe | [!UICONTROL Campaign Row missing] | Die angegebene übergeordnete Kampagne existiert nicht, sodass die Anzeigengruppe nicht erstellt wurde. Erstellen Sie die übergeordnete Kampagne in einer neuen Zeile. |
|  | [!UICONTROL New adgroup has both keywords and placement] | Eine Anzeigengruppe kann entweder Suchbegriffe oder Platzierungen enthalten, jedoch nicht beides. Erstellen Sie separate Anzeigengruppen für Suchbegriffe und Platzierungen. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) Die Anzeigengruppe wurde nicht erstellt, da sie nicht mindestens ein Keyword enthält. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) Die Anzeigengruppe wurde nicht erstellt, da sie nicht mindestens eine Anzeige enthält. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) Die Anzeigengruppe wurde nicht erstellt, da sie nicht mindestens eine Anzeige enthält. |
| Alle Anzeigengruppenkomponenten | [!UICONTROL Adgroup creation failed] | Die übergeordnete Anzeigengruppe wurde nicht erstellt, sodass diese Entität nicht erstellt werden konnte. Dies kann an einem Fehler in den Anzeigengruppenfeldern oder an einem Fehler der übergeordneten Kampagne liegen. Stellen Sie sicher, dass alle übergeordneten Entitäten alle erforderlichen Felder enthalten. |
|  | [!UICONTROL Adgroup Row Missing] | Die angegebene übergeordnete Anzeigengruppe existiert nicht, sodass die Entität nicht erstellt werden konnte. Erstellen Sie die übergeordnete Anzeigengruppe in einer neuen Zeile. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | Das Feld &quot;[!UICONTROL Tracking Template]&quot; gilt nur für Konten, die finale/erweiterte URLs verwenden. Entfernen Sie den Wert, bis Sie das Konto zur Verwendung endgültiger/erweiterter URLs migriert haben. |
| Anzeige | [!UICONTROL Cannot modify attributes other than status code and url for <ad type>] | (Andere Anzeigentypen als Text, erweiterter Text, Produkt, App-Installation und dynamische Suche) Sie können nur den Status und die URL für diesen Anzeigentyp bearbeiten. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Jede Anzeigengruppe kann bis zu 50 Anzeigen enthalten, und dieses Bulksheet enthält mehr als 50 Anzeigen. Reduzieren Sie die Anzahl der Anzeigen. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | Die Anzeige befindet sich in einer abgelaufenen oder gelöschten übergeordneten Entität, sodass Sie sie nicht bearbeiten können. |
| Schlüsselwort | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | Die übergeordnete Kampagne oder Anzeigengruppe wird gelöscht oder abgelaufen, sodass Sie die Entität nicht ändern können. |
| Platzierung | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | Die übergeordnete Kampagne oder Anzeigengruppe wird gelöscht oder abgelaufen, sodass Sie die Entität nicht ändern können. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google Ads) Sie können Angebote für Platzierungen nur in Kampagnen erstellen, die nur im Suchnetzwerk oder nur im Inhaltsnetzwerk verfügbar sind, jedoch nicht in Kampagnen, die sowohl auf Such- als auch auf Inhaltsnetzwerke ausgerichtet sind. |
| Warengruppe | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Jede Ebene der Produktgruppe muss eine &quot;[!UICONTROL Everything Else]&quot;-Gruppe enthalten. Sie können eine Gruppe &quot;[!UICONTROL Everything Else]&quot; nicht manuell löschen. Sie wird automatisch gelöscht, wenn Sie alle anderen Produktgruppen auf derselben Ebene löschen. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | Die übergeordnete Kampagne oder Anzeigengruppe wird gelöscht oder abgelaufen, sodass Sie die Entität nicht ändern können. |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] nur) Die Nachricht ist ungenau. Jede Kampagne kann bis zu vier (nicht 10) Sitelinks enthalten, und dieses Bulksheet enthält mehr als vier. Entfernen Sie einige Sitelinks. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | Die übergeordnete Kampagne ist abgelaufen oder gelöscht, sodass Sie den Sitelink nicht bearbeiten können. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) Der Sitelink konnte nicht erstellt werden, da die Anzeige nicht erstellt wurde. |
| Standort-Ziel | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | Die übergeordnete Kampagne oder Anzeigengruppe wird gelöscht oder abgelaufen, sodass Sie die Standortziele nicht bearbeiten können. |
| Ausschlüsse | [!UICONTROL Other than status is modified] | Sie können nur den Status eines Ausschlusses (&quot;[!UICONTROL Active]&quot; oder &quot;[!UICONTROL Deleted]&quot;) bearbeiten. |
| Google-Remarketing-Listenziele/-zielgruppen | [!UICONTROL Invalid Audience given] | ([!DNL Google Ads] nur Kampagnen) Das RLSA-Ziel entspricht nicht einer vorhandenen RLSA (Zielgruppe). Korrigieren Sie die Werte in den Spalten &quot;[!UICONTROL Audience]&quot; und &quot;[!UICONTROL RLSA Target]&quot;. |

### Beitragsfehler

Die folgenden Fehler treten nur in [!UICONTROL EF Errors] -Dateien auf. Die meisten Posting-Fehler stammen aus dem Werbenetzwerk und sind in einer SE-Fehlerdatei enthalten.

| Kategorie | Nachricht | Beschreibung |
|----|----|----|
| Allgemein | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | Der Vorgang ist vollständig fehlgeschlagen. Wenn das Problem weiterhin besteht, wenden Sie sich an Ihr Adobe-Account-Team. |
| Alle Entitäten | [!UICONTROL Entity] wird in das Anzeigennetzwerk gepostet | Die Entität wurde im Werbenetzwerk veröffentlicht, aber nicht gleichzeitig mit Search, Social und Commerce synchronisiert, sodass die Entitätsdaten nicht sofort in Search, Social und Commerce verfügbar sind. Der Synchronisierungsprozess wird jetzt automatisch ausgelöst.<br><br>Wenn große Datenmengen synchronisiert werden, stehen die Daten möglicherweise mehrere Stunden oder länger nicht in Search, Social und Commerce zur Verfügung. |
| | [!UICONTROL Skipping <ENTITY> creation since <PARENT ENTITY> creation failed.] | Die übergeordnete Entität konnte nicht erstellt werden, sodass diese untergeordnete Entität nicht erstellt wurde. |

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](bulksheet-about.md)
>* [Herunterladen/Erstellen einer Bulksheet-Datei](bulksheet-download.md)
>* [Validieren von Landingpages in Bulksheet-Dateien](bulksheet-validate-landing-pages.md)
>* [Laden Sie eine Bulksheet-Datei oder eine korrigierte Fehlerdatei hoch](bulksheet-upload.md)
>* [Post-Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
