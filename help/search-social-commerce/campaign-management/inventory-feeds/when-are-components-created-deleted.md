---
title: Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?
description: Erfahren Sie, in welchen Situationen Sie Kontokomponenten erstellen und löschen, wenn Sie Inventar-Feeds veröffentlichen.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Wenn eine Inventar-Feed-Datei über eine Vorlage propagiert wird, werden Kontokomponenten wie folgt erstellt und gelöscht.

>[!NOTE]
>
>In einer Anzeigengruppe werden keine doppelten Anzeigen erstellt.

| Szenario | Beispiel | Aktion |
|----|----|----|
| Feed-Daten enthalten einen neuen Wert für eine Spalte, die in einem Kampagnennamen, Anzeigengruppennamen, Suchbegriff oder Produktgruppe verwendet wird. | Frühere Dateien:<br>campaign=hats<br>campaign=gloves<br><br>Neue Datei:<br>campaign=shoes | Eine neue Kampagne, Anzeigengruppe, ein Suchbegriff oder eine neue Produktgruppe wird erstellt, wenn sie nicht im Werbenetzwerk vorhanden ist. |
| Feed-Daten enthalten einen neuen Wert für eine Spalte, die in einer Anzeige verwendet wird. | Vorherige Datei: Eine Anzeige enthielt &quot;price=20<br><br>Neue Datei: Für dieselbe Anzeige &quot;price=10&quot; | Wenn die Anzeigenkopie für [!DNL Microsoft Advertising] erweiterte Textanzeigen, [!DNL Yahoo! Japan ads] oder [!DNL Yandex] Anzeigen geändert wird, wird die vorhandene Anzeige gelöscht und eine neue erstellt.<br><br>Wenn die Anzeigenkopie für andere Anzeigentypen geändert wird oder wenn die entsprechende Spalte für einen [!DNL Google Ads] Anzeigenparameter ({param1} oder {param2}) in einer Anzeige verwendet wird, wird die vorhandene Anzeige aktualisiert. |
| Die Vorlageneinstellungen für die Kampagne, Anzeigengruppe, das Keyword oder die Produktgruppe haben sich seit der letzten Verbreitung geändert. | Vorherige Einstellung:Keyword=[Keyword]<br><br>Neue Einstellung: Keyword=&lt;Farbe>[Keyword] | Eine neue Kampagne, Anzeigengruppe, ein Suchbegriff oder eine neue Produktgruppe wird erstellt, wenn sie nicht im Werbenetzwerk vorhanden ist. |
| Die Vorlageneinstellungen für eine Anzeige haben sich seit der letzten Verbreitung geändert. | Vorherige Einstellung: Ad description=&quot;Buy [category] now.&quot;<br><br>Neue Einstellung: Ad description=&quot;Buy [brand] now.&quot; | Wenn die Anzeigenkopie für [!DNL Microsoft Advertising] erweiterte Textanzeigen, [!DNL Yahoo! Japan ads] oder [!DNL Yandex] Anzeigen geändert wird, wird die vorhandene Anzeige gelöscht und eine neue erstellt.<br><br>Wenn die Anzeigenkopie für andere Anzeigentypen geändert wird oder wenn die Änderung eine Änderung in der Spalte widerspiegelt, die für einen einzelnen [!DNL Google Ads] Anzeigenparameter ({param1} oder {param2}) in einer Anzeige verwendet wird, wird die vorhandene Anzeige aktualisiert. |
| Neue Feed-Daten enthalten keine Zeile für eine bestehende Kampagne oder Anzeigengruppe. | Nicht zutreffend | Die vorhandenen Kampagnen und Anzeigengruppen bleiben unverändert. |
| Neue Feed-Daten enthalten keine Zeile für eine bestehende Anzeigengruppe, Anzeige, Keyword oder Produktgruppe. | Nicht zutreffend | Die vorhandene Anzeigengruppe, Anzeige, Keyword oder Produktgruppe bleibt unverändert, wird gemäß den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) ausgesetzt oder gelöscht. |
| Neue Feed-Daten für eine bestehende übergeordnete Produktgruppe enthalten keine Zeilen für die vorhandenen untergeordneten Produktgruppen. | Nicht zutreffend | Die vorhandene übergeordnete Produktgruppe bleibt unverändert oder wird gemäß den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) gelöscht. <b>Hinweis:</b> Wenn die Feed-Dateneinstellungen so konfiguriert sind, dass fehlende Zeileneinträge angehalten werden, wird die übergeordnete Produktgruppe dennoch gelöscht, da Sie keine Produktgruppen anhalten können. |
| Neue Feed-Daten enthalten eine Zeile für eine Anzeigengruppe, Anzeige, Keyword oder Produktgruppe, die a) in vorherigen Daten, b) seither jedoch nicht mehr enthalten war und gemäß den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) angehalten wurde. | Nicht zutreffend | Die vorhandene Anzeigengruppe, Anzeige, Keyword oder Produktgruppe wird reaktiviert, ohne dass der Verlauf oder die Qualitätsbewertung verloren geht. |
| Neue Feed-Daten enthalten eine Zeile für eine Anzeigengruppe, Anzeige, Keyword oder Produktgruppe, die a) in vorherigen Daten, b) jedoch seitdem nicht mehr enthalten war und gemäß den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) gelöscht wurde. | Nicht zutreffend | Eine neue Anzeigengruppe, Anzeige, Keyword oder Produktgruppe wird erstellt. |
| Sie haben die Option auf Kampagnen- oder Anzeigengruppenebene auf &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot;deaktiviert. | Die negative Suchbegriffliste enthält &quot;Coupe&quot;und &quot;Sportwagen&quot;.<br><br>Die Anzeigengruppe enthält bereits das negative Keyword &quot;SUV&quot;. | Alle vorhandenen negativen Suchbegriffe, die nicht auf der Liste stehen, bleiben unverändert. |
| Sie haben die Option auf Kampagnen- oder Anzeigengruppenebene auf &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot;aktiviert und negative Suchbegriffe, die nicht auf der Liste stehen, sind vorhanden. | Die negative Suchbegriffliste enthält &quot;Coupe&quot;und &quot;Sportwagen&quot;.<br><br>Die Anzeigengruppe enthält bereits das negative Keyword &quot;SUV&quot;. | Alle nicht spezifizierten negativen Suchbegriffe, die zuvor mit der Vorlage erstellt wurden, werden gelöscht, wenn eine Feed-Datei über die Vorlage propagiert wird. Nicht spezifizierte negative Suchbegriffe, die mit anderen Mitteln erstellt wurden (z. B. in einfachen Bulksheets, den [!UICONTROL Campaigns] -Ansichten oder im Anzeigeneditor des Werbenetzwerks) bleiben jedoch unverändert. | | Das geplante Enddatum für die Komponenten einer veröffentlichten Feed-Datei tritt auf. | Nicht zutreffend | Die bestehenden Kampagnen bleiben unverändert. Die vorhandenen Anzeigengruppen, Anzeigen und Suchbegriffe bleiben unverändert, werden gemäß den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) ausgesetzt oder gelöscht. |
| Der Lagerbestand eines Elements sinkt unter den in den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) angegebenen Mindestwert. | Vorherige Datei: stock=10<br><br>Neue Datei: stock=0 | Die bestehenden Kampagnen bleiben unverändert. Die vorhandenen Anzeigengruppen, Anzeigen, Suchbegriffe und Produktgruppen werden gemäß den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) entweder angehalten oder gelöscht. |
| Der Lagerbestand eines Elements liegt über dem in den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) angegebenen Minimum. | Vorherige Datei: stock=0<br><br> Neue Datei: stock=10 | Wenn die vorhandenen Anzeigen, Suchbegriffe oder Produktgruppen angehalten werden, werden sie reaktiviert, ohne dass der Verlauf oder die Qualitätsbewertung verloren geht. Wenn keine Anzeigen, Suchbegriffe oder Produktgruppen vorhanden sind (z. B. wenn sie zuvor gelöscht wurden, weil das Lagerbestand unter dem Minimum lag), werden neue erstellt. |

>[!MORELIKETHIS]
>
>* [Über die Automatisierung der Anzeigenverwaltung mithilfe von Inventar-Feeds](inventory-feeds-about.md)
