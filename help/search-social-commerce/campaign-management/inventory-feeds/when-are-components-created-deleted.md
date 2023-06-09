---
title: Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?
description: Erfahren Sie, in welchen Situationen Sie Kontokomponenten erstellen und löschen, wenn Sie Inventar-Feeds veröffentlichen.
source-git-commit: f8d17ba787496917f4011f9dcbcb5587fe5c83cb
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Wenn eine Inventar-Feed-Datei über eine Vorlage propagiert wird, werden Kontokomponenten wie folgt erstellt und gelöscht.

>[!NOTE]
>
>In einer Anzeigengruppe werden keine doppelten Anzeigen erstellt.

| Szenario | Beispiel | Aktion |
|----|----|----|
| Feed-Daten enthalten einen neuen Wert für eine Spalte, die in einem Kampagnennamen, Anzeigengruppennamen, Suchbegriff oder Produktgruppe verwendet wird. | Vorherige Dateien:<br>Campaign=Hats<br>Campaign=Gloves<br><br>Neue Datei:<br>Campaign=Shoes | Eine neue Kampagne, Anzeigengruppe, ein Suchbegriff oder eine neue Produktgruppe wird erstellt, wenn sie nicht im Werbenetzwerk vorhanden ist. |
| Feed-Daten enthalten einen neuen Wert für eine Spalte, die in einer Anzeige verwendet wird. | Vorherige Datei: Eine Anzeige enthielt den Preis = 20<br><br>Neue Datei: Für dieselbe Anzeige: price=10 | Wenn die Anzeige für [!DNL Microsoft® Advertising] erweiterte Textanzeigen, [!DNL Yahoo! Japan ads]oder [!DNL Yandex] -Anzeigen geändert, die vorhandene Anzeige gelöscht und eine neue erstellt wird.<br><br>Wenn die Anzeigenkopie für andere Anzeigentypen geändert wird oder wenn die entsprechende Spalte für eine [!DNL Google Ads] Anzeigenparameter ({param1} oder {param2}), dann wird die vorhandene Anzeige aktualisiert. |
| Die Vorlageneinstellungen für die Kampagne, Anzeigengruppe, das Keyword oder die Produktgruppe haben sich seit der letzten Verbreitung geändert. | Vorherige Einstellung:Keyword=[Schlüsselwort]<br><br>Neue Einstellung: Schlüsselwort=&lt;color>[Schlüsselwort] | Eine neue Kampagne, Anzeigengruppe, ein Suchbegriff oder eine neue Produktgruppe wird erstellt, wenn sie nicht im Werbenetzwerk vorhanden ist. |
| Die Vorlageneinstellungen für eine Anzeige haben sich seit der letzten Verbreitung geändert. | Vorherige Einstellung: Ad description=&quot;Buy [category] jetzt.&quot;<br><br>Neue Einstellung: Ad description=&quot;Buy [Marke] jetzt.&quot; | Wenn die Anzeige für [!DNL Microsoft® Advertising] erweiterte Textanzeigen, [!DNL Yahoo! Japan ads]oder [!DNL Yandex] -Anzeigen geändert, die vorhandene Anzeige gelöscht und eine neue erstellt wird.<br><br>Wenn die Anzeigenkopie für andere Anzeigentypen geändert wird oder wenn die Änderung eine Änderung in der Spalte widerspiegelt, die für eine einzelne Anzeige verwendet wird [!DNL Google Ads] Anzeigenparameter ({param1} oder {param2}), dann wird die vorhandene Anzeige aktualisiert. |
| Neue Feed-Daten enthalten keine Zeile für eine bestehende Kampagne oder Anzeigengruppe. | Nicht zutreffend | Die vorhandenen Kampagnen und Anzeigengruppen bleiben unverändert. |
| Neue Feed-Daten enthalten keine Zeile für eine bestehende Anzeigengruppe, Anzeige, Keyword oder Produktgruppe. | Nicht zutreffend | Die vorhandene Anzeigengruppe, Anzeige, Keyword oder Produktgruppe bleibt unverändert, wird angehalten oder gelöscht, entsprechend der Variablen [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings). |
| Neue Feed-Daten für eine bestehende übergeordnete Produktgruppe enthalten keine Zeilen für die vorhandenen untergeordneten Produktgruppen. | Nicht zutreffend | Die vorhandene übergeordnete Produktgruppe bleibt unverändert oder wird gelöscht, entsprechend der Variablen [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings). <b>Hinweis:</b> Wenn die Feed-Dateneinstellungen so konfiguriert sind, dass fehlende Zeileneinträge angehalten werden, wird die übergeordnete Produktgruppe dennoch gelöscht, da Sie Produktgruppen nicht anhalten können. |
| Neue Feed-Daten enthalten eine Zeile für eine Anzeigengruppe, Anzeige, ein Keyword oder eine Produktgruppe, die a) in vorherigen Daten, b) jedoch seitdem weggelassen wurde und gemäß dem [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings). | Nicht zutreffend | Die vorhandene Anzeigengruppe, Anzeige, Keyword oder Produktgruppe wird reaktiviert, ohne dass der Verlauf oder die Qualitätsbewertung verloren geht. |
| Neue Feed-Daten enthalten eine Zeile für eine Anzeigengruppe, Anzeige, Keyword oder Produktgruppe, die a) in vorherigen Daten, b) jedoch seitdem weggelassen wurde und gemäß der [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings). | Nicht zutreffend | Eine neue Anzeigengruppe, Anzeige, Keyword oder Produktgruppe wird erstellt. |
| Sie haben die Option auf Kampagnen- oder Anzeigengruppenebene auf &quot;[!UICONTROL Delete negative keywords when omitted from list].&quot; | Die negative Suchbegriffliste enthält &quot;Coupe&quot;und &quot;Sportwagen&quot;.<br><br>Die Anzeigengruppe enthält bereits das negative Keyword &quot;SUV&quot;. | Alle vorhandenen negativen Suchbegriffe, die nicht auf der Liste stehen, bleiben unverändert. |
| Sie haben die Option auf Kampagnen- oder Anzeigengruppenebene auf &quot;[!UICONTROL Delete negative keywords when omitted from list],&quot; und negative Suchbegriffe, die nicht in der Liste aufgeführt sind, vorhanden sind. | Die negative Suchbegriffliste enthält &quot;Coupe&quot;und &quot;Sportwagen&quot;.<br><br>Die Anzeigengruppe enthält bereits das negative Keyword &quot;SUV&quot;. | Alle nicht spezifizierten negativen Suchbegriffe, die zuvor mit der Vorlage erstellt wurden, werden gelöscht, wenn eine Feed-Datei über die Vorlage propagiert wird. Alle nicht spezifizierten negativen Suchbegriffe, die mit anderen Mitteln erstellt wurden (z. B. in einfachen Bulksheets, [!UICONTROL Campaigns] -Ansichten oder im Anzeigen-Editor des Werbenetzwerks) unverändert bleiben. | | Das geplante Enddatum für die Komponenten einer veröffentlichten Feed-Datei tritt auf. | Nicht zutreffend | Die bestehenden Kampagnen bleiben unverändert. Die vorhandenen Anzeigengruppen, Anzeigen und Suchbegriffe bleiben unverändert, werden angehalten oder gelöscht, je nach [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings). |
| Der Lagerbestand eines Artikels sinkt unter das in der Variablen [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings). | Vorherige Datei: stock=10<br><br>Neue Datei: stock=0 | Die bestehenden Kampagnen bleiben unverändert. Die vorhandenen Anzeigengruppen, Anzeigen, Suchbegriffe und Produktgruppen werden je nach [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings). |
| Der Lagerbestand eines Artikels liegt über dem in der Variablen [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings). | Vorherige Datei: stock=0<br><br> Neue Datei: stock=10 | Wenn die vorhandenen Anzeigen, Suchbegriffe oder Produktgruppen angehalten werden, werden sie reaktiviert, ohne dass der Verlauf oder die Qualitätsbewertung verloren geht. Wenn keine Anzeigen, Suchbegriffe oder Produktgruppen vorhanden sind (z. B. wenn sie zuvor gelöscht wurden, weil das Lagerbestand unter dem Minimum lag), werden neue erstellt. |

>[!MORELIKETHIS]
>
>* [Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds](inventory-feeds-about.md)
