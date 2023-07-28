---
title: Häufig gestellte Fragen zu Kampagnen
description: Hier finden Sie Antworten auf Fragen zur Kampagnenverwaltung und zu Kampagnendaten.
exl-id: b5975869-4bc3-461d-8cb7-eeefab157137
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# Häufig gestellte Fragen zur Kampagnenverwaltung

## Allgemeine Informationen

+++ Kann ich Kampagnen und Komponenten von einem Konto in ein anderes verschieben?

Verschieben oder kopieren Sie keine Kampagnen- oder Kampagnenkomponente mit einer eindeutigen ID in ein Konto mit einer anderen Konto-ID. Dies führt zu Datenfehlern.
+++

+++ Wann werden Klickdaten aus den Werbenetzwerken aktualisiert?

Der Prozess zum Abrufen der Klickdaten des Vortags aus den Suchmaschinen beginnt um 6:00 Uhr in der Zeitzone des Werbetreibenden.

Darüber hinaus [!DNL Google Ads] Leistungsmetriken auf Kampagnenebene im Suchnetzwerk für den aktuellen Tag werden um 8:00 Uhr und 16:00 Uhr in der Zeitzone des Advertisers abgerufen.
+++

+++Welche Aktionen führen dazu, dass Suchbegriffe und Anzeigen ihren Verlauf verlieren?

>[!NOTE]
>
>(Werbetreibende mit Portfolios) Erwarten Sie, dass die Leistung neuer Keyword- und Übereinstimmungstyp-Kombinationen schwankt, während Search, Social und Commerce Daten erfasst, um neue Modelle zu erstellen.

**Aktionen im [!UICONTROL Search] > [!UICONTROL Campaigns] -Ansichten im Bulksheet-Posting-Prozess und im eigenen Editor des Werbenetzwerks:**

Der vorhandene Suchbegriff oder die Anzeige wird gelöscht und ein anderer erstellt, wenn:

* ([!DNL Baidu], [!DNL Google Ads], und [!DNL Yandex]) Sie bearbeiten einen Suchbegriffnamen.

* ([!DNL Google Ads], [!DNL Microsoft Advertising], und [!DNL Yandex]) Sie ändern den Übereinstimmungstyp eines Suchbegriffs.

* Sie verschieben einen Suchbegriff zwischen Anzeigengruppen.

* ([!DNL Google Ads] dynamische Suchanzeigen, [!DNL Microsoft Advertising] erweiterte Textanzeigen und alle Anzeigentypen in anderen unterstützten Werbenetzwerken) Sie bearbeiten Anzeigenkopien (Überschrift/Titel oder Beschreibung) oder ein Anzeigenbild.

* Sie verschieben eine Anzeige zwischen Anzeigengruppen.

**Ereignisse im Prozess der Produktbestand-Feed-Veröffentlichung:**

Eine vorhandene Anzeige oder ein Suchbegriff wird gelöscht und eine andere erstellt, wenn:

* Eine Feed-Datei enthält einen neuen Wert für eine Spalte, die in einer Anzeigenvariante verwendet wird.

* Die Vorlageneinstellungen für eine Anzeige haben sich seit der letzten Verbreitung geändert.

* Eine neue Feed-Datei enthält eine Zeile für eine Anzeige oder ein Keyword, die/das a) in einer vorherigen Datei enthalten, aber b) seitdem nicht mehr enthalten war und gemäß den Feed-Dateneinstellungen angehalten oder gelöscht wurde.

Je nach [Feed-Dateneinstellungen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), kann eine vorhandene Anzeige oder ein Suchbegriff gelöscht werden, wenn:

* Eine neue Feed-Datei enthält keine Zeile für eine vorhandene Anzeige oder einen Suchbegriff.

* Das geplante Enddatum für die Komponenten einer veröffentlichten Feed-Datei tritt auf.

* Der Lagerbestand eines Elements sinkt unter das in den Feed-Dateneinstellungen angegebene Minimum.
+++

+++([!DNL Google Ads] Kampagnen) Änderungen an den Anzeigenamen für meine [!DNL Google]-getrackte Konversionen zurückgesetzt wurden.

Wenn Sie die Anzeigenamen der Transaktionseigenschaften in Search, Social und Commerce ändern, werden Ihre Änderungen mit den Namen überschrieben, die in [!DNL Google Ads]. Nehmen Sie Namensänderungen in vor [!DNL Google Ads].
+++

+++(Google Ads-Kampagnen) Kann ich ein freigegebenes Budget für Kampagnen in Portfolios verwenden?

Die besten Ergebnisse erzielen Sie, wenn Sie [!DNL Google Ads] Kampagnen an [!DNL Google Ads] freigegebenes Budget, wenn sie sich in optimierten Portfolios befinden, die für &quot;[!UICONTROL Auto adjust campaign budget limits].&quot; Wenn ja, [!DNL Google Ads] überschreibt die optimierten Kampagnenbudgets für Suche, Social und Commerce, was zu Ineffizienzen bei Angeboten führen kann.
+++

+++([!DNL Google Ads] Kampagnen) Kann ich mobile und nicht mobile Benutzer an verschiedene Landingpages senden?

Sie können die [!DNL Google Ads] [!DNL ValueTrack] parameters `{ifmobile}` und `{ifnotmobile}` , um den Domänennamen der Landingpage auf zwei Arten zu bestimmen, je nach Fall für Ihre Sites:

* Fügen Sie die mobile Bezeichnung als Host-Server mit `{ifmobile:m}{ifnotmobile:www}`.

  Beispiel: `http://{ifmobile:m}{ifnotmobile:www}.example.com` bringt mobile Benutzer zu m.example.com und Nicht-Mobilbenutzer zu www.example.com.

* Fügen Sie die mobile Bezeichnung als Top-Level-Domäne mit `{ifmobile:mobi}{ifnotmobile:com}`.

  Beispiel: `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` bringt mobile Benutzer zu www.example.mobi und Nicht-Mobilbenutzer zu www.example.com.

In beiden Fällen enthalten die Basis-URLs mit Such-, Social- und Commerce-Tracking die nicht kodierten `{}` Tags und alle zusätzlichen Parameter, die an die Basis-URL angehängt sind.

>[!NOTE]
>
>Verwenden Sie keine vollständige URL als Wert für ifnotmobile und ifmobile Parameter. Verwenden Sie nur den variablen Teil der URL (z. B. &quot;m&quot;versus &quot;www&quot;oder &quot;mobi&quot;versus &quot;com&quot;).

+++

+++([!DNL Google Ads] Kampagnen im Suchnetzwerk) Für welche Daten wird heute angezeigt?

[!DNL Google Ads] Leistungsmetriken auf Kampagnenebene im Suchnetzwerk für den aktuellen Tag werden um 8:00 Uhr und 16:00 Uhr in der Zeitzone des Advertisers abgerufen.

Im [!UICONTROL Campaigns] in beiden [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] und [!UICONTROL Optimization] > [!UICONTROL Portfolios] anzeigen, wenn Sie einen Bericht zu [!UICONTROL Today] oder einem benutzerdefinierten Datumsbereich, der den aktuellen Tag enthält, enthalten die Daten die zuletzt abgerufen Daten.

>[!NOTE]
>
>Daten für Klicks, Impressionen und Konversionen werden um drei Stunden verzögert und erst nach der nächsten Datenabfrage abgeschlossen.

+++

+++([!DNL Google Ads] und [!DNL Microsoft Advertising]) Unterstützt Search, Social und Commerce das parallele Tracking von Anzeigen in [!DNL Google Ads] oder [!DNL Microsoft Advertising]?

Beim parallelen Tracking werden Kunden direkt von Ihrer Anzeige an Ihre endgültige URL gesendet. Ihre Tracking-Vorlagen-URL (mit Klick-Messung) wird im Hintergrund geladen. Dadurch wird Ihre Landingpage schneller geladen.

Search, Social und Commerce unterstützt das parallele Tracking für Such- und Einkaufskampagnen mithilfe der Klick-ID des Anzeigennetzwerks (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für [!DNL Google Ads]). Verwenden Sie eine [Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) oder [Kampagnenebene](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (genannt &quot;[!DNL final URL suffix]&quot; in den Werbenetzwerken), die an Landingpage-URLs angehängt wird, um Klicks auf untergeordnete Anzeigen von Browsern zu verfolgen, die paralleles Tracking unterstützen. Siehe [erforderliche Suffix-Formate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderliche Suffix-Formate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Wenn ein Benutzer Ihre Anzeige in einem Browser anzeigt, der kein paralleles Tracking unterstützt, verwendet das Werbenetzwerk stattdessen das sequenzielle Tracking: Kunden werden zunächst an Ihre Tracking-Vorlage-URL gesendet, wodurch Kunden zu Tracking-Zwischenservern weitergeleitet werden, bevor sie zur endgültigen URL weitergeleitet werden. Alle Tracking-Vorlagen für ein Anzeigen-Netzwerk-Konto sollten denselben Klick-ID-Parameter enthalten, den Sie in der Variablen [!UICONTROL Landing Page Suffix]. Siehe [Tracking-Vorlagenformate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [Tracking-Vorlagenformate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++ Warum enthalten Tracking-URLs für meine Anzeigen &quot;`&EV_HASH={<hash>}`?&quot;

Wenn Sie Anzeigen mit einer [Produktinventar-Feed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) für ein Konto mit der Pixelumleitung &quot;Suchen&quot;, &quot;Sozial&quot;und &quot;Commerce&quot;und mit Keyword- und kreativem Tracking, fügt &quot;Suchen&quot;, &quot;Sozial&quot;und &quot;Commerce&quot;den Hash-Parameter und Wert zur Tracking-Vorlage oder Ziel-URL der Anzeige hinzu, um zu ermitteln, ob diese mit der Inventar-Feed-Funktion erstellt wurde.
+++

## Inventar-Feeds

+++(Produkt-Inventar-Feeds) Sollte ich Anzeigen anhalten oder löschen, die veraltet sind oder für ein Produkt bestimmt sind, dessen Lagerbestand unter einem bestimmten Minimum liegt?

Dies hängt von den Geschäftsanforderungen des Werbetreibenden ab.

Wenn Sie Anzeigen anhalten, werden sie reaktiviert, wenn Sie dieselbe Anzeige erneut senden oder die Lagerbestände über das Minimum hinausgehen. Auf diese Weise können Sie den Verlauf der Anzeige beibehalten.

Wenn Sie Anzeigen löschen und erneut senden, werden neue Anzeigen erstellt und historische Daten müssen gesammelt werden. Wenn Sie jedoch nicht erwarten, gelöschte Anzeigen erneut einzureichen, ist es nicht wichtig, historische Daten zu haben.
+++

+++(Produkt-Inventar-Feeds) Wenn ich eine Anzeigenvorlage lösche und dann eine neue, identische Vorlage erstelle, fehlen Elemente in der nächsten Feed-Datei, die angehalten wird (wenn die Feed-Dateieinstellungen dafür konfiguriert sind)?

Wenn in der nächsten Feed-Datei Zeileneinträge fehlen und Sie diese Zeileneinträge noch nicht aus der neuen Vorlage über eine vorherige Feed-Datei veröffentlicht haben, werden die fehlenden Zeileneinträge nicht als &quot;fehlend&quot;erkannt und werden daher nicht erstellt. Um dies zu vermeiden, propagieren Sie die vorherige Feed-Datei durch die neue Vorlage und posten Sie die Daten, bevor Sie Daten aus einer neuen Datei propagieren und posten.
+++

+++(Produktbestand-Feeds) Kann ich die Preise für meine Produkte aktualisieren, ohne dass sich dies auf die Qualitätsbewertung einer Anzeige auswirkt?

Für [!DNL Google Ads] Kampagnen, ja: Die [!DNL Google Ads] `{Param 1}` und `{Param 2}` -Variablen ermöglichen es Ihnen, numerische Werte dynamisch in eine Anzeigenvariante einzufügen, ohne die Anzeige zu löschen und neu zu erstellen, sodass dies keine Auswirkungen auf die Qualitätsbewertung hat.

So verwenden Sie `{Param 1}` oder `{Param 2}` für Ihre Preisdaten verwenden, ordnen Sie die Preisspalte in Ihrer Datendatei dieser Variablen in den entsprechenden Feed-Vorlagen zu und fügen Sie dann die Variable in Ihre Anzeigenvariationsvorlagen ein.

Wenn die Spalte beispielsweise &quot;Preis&quot;heißt, öffnen Sie die Feed-Vorlage, die die Anzeigen erstellt, und klicken Sie auf das Eingabefeld neben **[!UICONTROL Param 1]** und klicken Sie dann auf **[!UICONTROL Price]** in der [!UICONTROL Feeds/Available Columns] list, die `[Price]` als Wert für [!UICONTROL Param 1]. Fügen Sie dann in die Anzeigenvariationsvorlage am unteren Rand der Feed-Vorlage `{param1:default text}`, wobei &quot;Standardtext&quot;Text ist, der verwendet werden soll, wenn die Parameterspalte in der Feed-Datei für eine Anzeigenzeile leer ist.

Wenn Sie Daten senden, werden die Datenfelder für die [!UICONTROL Param1] und [!UICONTROL Param2] -Spalten können bis zu 25 Zeichen enthalten, darunter numerische Daten, Währungssymbole und Währungscodes sowie die folgenden nicht numerischen Zeichen: `, . % + - /`
+++

+++ Meine Kampagnen, die aus Inventar-Feeds generiert wurden, haben viele verwaiste Transaktionen.

Wenn die Variable [Feed-Dateneinstellungen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) so konfiguriert sind, dass Anzeigen in verschiedenen Situationen gelöscht werden, kann dies dazu führen, dass verzögerte Konversionen, die nach dem Klicken auf die Anzeige auftreten, [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p). Die Best Practice ist, Anzeigen anzuhalten, anstatt sie zu löschen. Wenn eine Werbeanzeige nach einem langen Zeitraum immer noch keinen Umsatz erhalten hat, können Sie sie über ein Bulksheet oder die Anzeigenverwaltungsansicht löschen.
+++

## Leistungsprobleme im Zusammenhang mit Konten und Kampagnen

+++ Einige meiner Kampagnen geben mehr oder weniger aus als die Kampagnenbudgets.

* Dies ist in einem optimierten Portfolio normal, das mit dem[!UICONTROL Auto-adjust campaign budget limits]&quot;. Wenn diese Option aktiviert ist, können Sie bis zu *N* die Zeiten für das Budget jeder Kampagne, wobei *N* ist der Wert von &quot;[!UICONTROL Multiple]&quot;. Diese Option ermöglicht es der Optimierungsfunktion, die Ausgaben für einzelne Kampagnen nach Bedarf anzupassen und gleichzeitig das gesamte Portfolio so zu steuern, dass es sein Ziel erreicht.
* Wenn [!DNL Google Ads] Kampagnen verwenden ein freigegebenes Budget und [!DNL Google Ads] passt die Ausgaben für einzelne Kampagnen nach Bedarf an, um den gesamten gemeinsamen Haushalt auszugeben.
+++
