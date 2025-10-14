---
title: Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?
description: Erfahren Sie, in welchen Situationen Kontokomponenten erstellt und gelöscht werden, wenn Sie Inventar-Feeds posten.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Wenn eine Inventar-Feed-Datei über eine Vorlage übertragen wird, werden die Kontokomponenten wie folgt erstellt und gelöscht.

>[!NOTE]
>
>Doppelte Anzeigen werden nie innerhalb einer Anzeigengruppe erstellt.

| Szenario | Beispiel | Aktion |
|----|----|----|
| Feed-Daten enthalten einen neuen Wert für eine Spalte, die in einem Kampagnennamen, Anzeigengruppennamen, Keyword oder einer Produktgruppe verwendet wird. | Vorherige Dateien:<br>campaign=hats<br>campaign=handschuhe<br><br>neue Datei:<br>campaign=shoes | Eine neue Kampagne, Anzeigengruppe, ein neues Keyword oder eine neue Produktgruppe wird erstellt, wenn sie nicht im Anzeigennetzwerk vorhanden ist. |
| Feed-Daten enthalten einen neuen Wert für eine Spalte, die in einer Anzeige verwendet wird. | Vorherige Datei: Eine Anzeige enthielt Preis=20<br><br>Neue Datei: Für die gleiche Anzeige, Preis=10 | Wenn die Anzeigenkopie für [!DNL Microsoft Advertising] erweiterte Textanzeigen, [!DNL Yahoo! Japan ads] oder [!DNL Yandex] Anzeigen geändert wird, wird die vorhandene Anzeige gelöscht und eine neue erstellt.<br><br>Wenn die Anzeigenkopie für andere Anzeigentypen geändert wird oder wenn die entsprechende Spalte für einen [!DNL Google Ads] Anzeigenparameter ({param1} oder {param2}) in einer Anzeige verwendet wird, wird die vorhandene Anzeige aktualisiert. |
| Die Vorlageneinstellungen für die Kampagne, die Anzeigengruppe, das Keyword oder die Produktgruppe haben sich seit der letzten Verbreitung geändert. | Vorherige Einstellung:Keyword=[Keyword]<br><br>Neue Einstellung: Keyword=&lt;Color>[Keyword] | Eine neue Kampagne, Anzeigengruppe, ein neues Keyword oder eine neue Produktgruppe wird erstellt, wenn sie nicht im Anzeigennetzwerk vorhanden ist. |
| Die Vorlageneinstellungen für eine Anzeige haben sich seit der letzten Verbreitung geändert. | Vorherige Einstellung: Anzeigenbeschreibung=„Jetzt [Kategorie] kaufen.“<br><br>Neue Einstellung: Anzeigenbeschreibung=„Jetzt [Marke] kaufen.“ | Wenn die Anzeigenkopie für [!DNL Microsoft Advertising] erweiterte Textanzeigen, [!DNL Yahoo! Japan ads] oder [!DNL Yandex] Anzeigen geändert wird, wird die vorhandene Anzeige gelöscht und eine neue erstellt.<br><br>Wenn die Anzeigenkopie für andere Anzeigentypen geändert wird oder wenn die Änderung eine Änderung in der Spalte widerspiegelt, die für einen einzelnen [!DNL Google Ads]-Anzeigenparameter ({param1} oder {param2}) in einer Anzeige verwendet wird, wird die vorhandene Anzeige aktualisiert. |
| Neue Feed-Daten enthalten keine Zeile für eine vorhandene Kampagne oder Anzeigengruppe. | Nicht zutreffend | Die vorhandenen Kampagnen und Anzeigengruppen bleiben unverändert. |
| Neue Feed-Daten enthalten keine Zeile für eine vorhandene Anzeigengruppe, Anzeige, ein Keyword oder eine Produktgruppe. | Nicht zutreffend | Die vorhandene Anzeigengruppe, Anzeige, das Keyword oder die Produktgruppe bleibt unverändert, wird angehalten oder wird gemäß den [Feed-Dateneinstellungen“ &#x200B;](feed-settings-manage.md#feed-data-settings). |
| Neue Feed-Daten für eine vorhandene übergeordnete Produktgruppe enthalten keine Zeilen für die vorhandenen untergeordneten Produktgruppen. | Nicht zutreffend | Die vorhandene übergeordnete Produktgruppe bleibt unverändert oder wird gemäß den [Feed-Dateneinstellungen) &#x200B;](feed-settings-manage.md#feed-data-settings). <b>Hinweis:</b> Wenn die Feed-Dateneinstellungen so konfiguriert sind, dass fehlende Zeileneinträge angehalten werden, wird die übergeordnete Produktgruppe weiterhin gelöscht, da Sie die Produktgruppen nicht anhalten können. |
| Neue Feed-Daten enthalten eine Zeile für eine Anzeigengruppe, Anzeige, ein Keyword oder eine Produktgruppe, die a) in früheren Daten war, aber b) seitdem weggelassen wurde und gemäß den [Feed-Dateneinstellungen“ angehalten &#x200B;](feed-settings-manage.md#feed-data-settings). | Nicht zutreffend | Die bestehende Anzeigengruppe, Anzeige, das Keyword oder die Produktgruppe wird reaktiviert, ohne dass der Verlauf oder der Qualitätswert verloren geht. |
| Neue Feed-Daten enthalten eine Zeile für eine Anzeigengruppe, Anzeige, ein Keyword oder eine Produktgruppe, die a) in früheren Daten war, aber b) seitdem weggelassen wurde und gemäß den [Feed-Dateneinstellungen“ gelöscht &#x200B;](feed-settings-manage.md#feed-data-settings). | Nicht zutreffend | Es wird eine neue Anzeigengruppe, Anzeige, ein Keyword oder eine neue Produktgruppe erstellt. |
| Sie haben die Option auf Kampagnen- oder Anzeigengruppenebene auf &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot; deaktiviert. | Die Liste der negativen Keywords enthält „Coupé“ und „Sportwagen“.<br><br>Die Anzeigengruppe enthält bereits das negative Keyword „SUV“. | Alle vorhandenen negativen Keywords, die nicht in der Liste enthalten sind, bleiben unverändert. |
| Sie haben die Option auf Kampagnen- oder Anzeigengruppenebene auf &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot; aktiviert, und es sind keine negativen Keywords auf der Liste vorhanden. | Die Liste der negativen Keywords enthält „Coupé“ und „Sportwagen“.<br><br>Die Anzeigengruppe enthält bereits das negative Keyword „SUV“. | Alle nicht spezifizierten negativen Keywords, die zuvor mit der Vorlage erstellt wurden, werden gelöscht, wenn eine Feed-Datei durch die Vorlage propagiert wird. Alle nicht spezifizierten negativen Keywords, die auf andere Weise erstellt wurden (z. B. in einfachen Bulksheets, in den [!UICONTROL Campaigns] oder im Anzeigeneditor des Anzeigennetzwerks), bleiben jedoch unverändert. | | Das geplante Enddatum für die Komponenten einer geposteten Feed-Datei tritt auf. | Nicht zutreffend | Die vorhandenen Kampagnen bleiben unverändert. Die vorhandenen Anzeigengruppen, Anzeigen und Keywords bleiben unverändert, werden angehalten oder gemäß den [Feed-Dateneinstellungen“ gelöscht](feed-settings-manage.md#feed-data-settings). |
| Der Lagerbestand eines Elements sinkt unter ein in den [Feed-Dateneinstellungen](feed-settings-manage.md#feed-data-settings) angegebenes Minimum. | Vorherige Datei: stock=10<br><br>Neue Datei: stock=0 | Die vorhandenen Kampagnen bleiben unverändert. Die vorhandenen Anzeigengruppen, Anzeigen, Keywords und Produktgruppen werden gemäß den Einstellungen für [-Daten entweder angehalten oder &#x200B;](feed-settings-manage.md#feed-data-settings). |
| Der Bestand eines Elements überschreitet den in den [Feed-Dateneinstellungen“ angegebenen &#x200B;](feed-settings-manage.md#feed-data-settings). | Vorherige Datei: stock=0<br><br> Neue Datei: stock=10 | Wenn die vorhandenen Anzeigen, Keywords oder Produktgruppen angehalten werden, werden sie reaktiviert, ohne den Verlauf oder die Qualitätsbewertung zu verlieren. Wenn keine Anzeigen, Keywords oder Produktgruppen vorhanden sind (z. B. wenn sie zuvor gelöscht wurden, weil der Bestand unter dem Minimum lag), werden neue erstellt. |

>[!MORELIKETHIS]
>
>* [Über die Automatisierung der Anzeigenverwaltung mithilfe von Inventar-Feeds](inventory-feeds-about.md)
