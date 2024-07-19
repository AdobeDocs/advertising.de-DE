---
title: Häufig gestellte Fragen zu Kampagnen
description: Hier finden Sie Antworten auf Fragen zur Kampagnenverwaltung und zu Kampagnendaten.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Häufig gestellte Fragen zur Kampagnenverwaltung

## Allgemeine Informationen

+++ Kann ich Kampagnen und Komponenten von einem Konto in ein anderes verschieben?

Verschieben oder kopieren Sie keine Kampagnen- oder Kampagnenkomponente mit einer eindeutigen ID in ein Konto mit einer anderen Konto-ID. Dies führt zu Datenfehlern.
+++

+++ Wann werden Klickdaten aus den Werbenetzwerken aktualisiert?

Der Prozess zum Abrufen der Klickdaten des Vortags aus den Suchmaschinen beginnt um 6:00 Uhr in der Zeitzone des Werbetreibenden.

Darüber hinaus werden [!DNL Google Ads] Leistungsmetriken auf Kampagnenebene im Suchnetzwerk für den aktuellen Tag um 08:00 und 16:00 Uhr in der Zeitzone des Advertisers abgerufen.
+++

+++Welche Aktionen führen dazu, dass Suchbegriffe und Anzeigen ihren Verlauf verlieren?

>[!NOTE]
>
>(Werbetreibende mit Portfolios) Erwarten Sie, dass die Leistung neuer Keyword- und Übereinstimmungstyp-Kombinationen schwankt, während Search, Social und Commerce Daten erfassen, um Modelle für sie zu erstellen.

**Aktionen in den Ansichten [!UICONTROL Search] > [!UICONTROL Campaigns], im Bulksheet-Veröffentlichungsprozess und im eigenen Editor des Anzeigennetzwerks:**

Der vorhandene Suchbegriff oder die Anzeige wird gelöscht und ein anderer erstellt, wenn:

* ([!DNL Baidu], [!DNL Google Ads] und [!DNL Yandex]) Sie bearbeiten einen Suchbegriffnamen.

* ([!DNL Google Ads], [!DNL Microsoft Advertising] und [!DNL Yandex]) Sie ändern den Übereinstimmungstyp eines Suchbegriffs.

* Sie verschieben einen Suchbegriff zwischen Anzeigengruppen.

* ([!DNL Google Ads] dynamische Suchanzeigen, [!DNL Microsoft Advertising] erweiterte Textanzeigen und alle Anzeigentypen in anderen unterstützten Werbenetzwerken) Sie bearbeiten eine Anzeigenkopie (Überschrift/Titel oder Beschreibung) oder ein Anzeigenbild.

* Sie verschieben eine Anzeige zwischen Anzeigengruppen.

**Ereignisse im Prozess der Produktbestand-Feed-Veröffentlichung:**

Eine vorhandene Anzeige oder ein Suchbegriff wird gelöscht und eine andere erstellt, wenn:

* Eine Feed-Datei enthält einen neuen Wert für eine Spalte, die in einer Anzeigenvariante verwendet wird.

* Die Vorlageneinstellungen für eine Anzeige haben sich seit der letzten Verbreitung geändert.

* Eine neue Feed-Datei enthält eine Zeile für eine Anzeige oder ein Keyword, die/das a) in einer vorherigen Datei enthalten, aber b) seitdem nicht mehr enthalten war und gemäß den Feed-Dateneinstellungen angehalten oder gelöscht wurde.

Abhängig von den [Feed-Dateneinstellungen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) kann eine vorhandene Anzeige oder ein Keyword gelöscht werden, wenn:

* Eine neue Feed-Datei enthält keine Zeile für eine vorhandene Anzeige oder einen Suchbegriff.

* Das geplante Enddatum für die Komponenten einer veröffentlichten Feed-Datei tritt auf.

* Der Lagerbestand eines Elements sinkt unter das in den Feed-Dateneinstellungen angegebene Minimum.
+++

+++([!DNL Google Ads] Kampagnen) Änderungen an den Anzeigenamen für meine [!DNL Google]-verfolgten Konversionen wurden rückgängig gemacht.

Wenn Sie die Anzeigenamen der Konversionsmetriken in Search, Social und Commerce ändern, werden Ihre Änderungen mit den in [!DNL Google Ads] konfigurierten Namen überschrieben. Nehmen Sie beliebige Namensänderungen in [!DNL Google Ads] vor.
+++

+++(Google Ads-Kampagnen) Kann ich ein freigegebenes Budget für Kampagnen in Portfolios verwenden?

Die besten Ergebnisse erzielen Sie, wenn Sie [!DNL Google Ads]-Kampagnen nicht zu einem gemeinsamen [!DNL Google Ads]-Budget hinzufügen, wenn sie sich in optimierten Portfolios befinden, die für &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;konfiguriert sind. Wenn dies der Fall ist, überschreibt [!DNL Google Ads] die für Search, Social und Commerce optimierten Kampagnenbudgets, was zu Ineffizienzen bei Angeboten führen kann.
+++

+++([!DNL Google Ads] Kampagnen) Kann ich mobile und nicht mobile Benutzer an verschiedene Landingpages senden?

Sie können die Parameter [!DNL Google Ads] [!DNL ValueTrack] `{ifmobile}` und `{ifnotmobile}` verwenden, um den Domänennamen der Landingpage auf zwei Arten zu bestimmen, je nach Fall für Ihre Sites:

* Fügen Sie die mobile Bezeichnung als Host-Server mit `{ifmobile:m}{ifnotmobile:www}` hinzu.

  Beispiel: `http://{ifmobile:m}{ifnotmobile:www}.example.com` bringt mobile Benutzer zu m.example.com und Nicht-Mobilbenutzer zu www.example.com.

* Fügen Sie die mobile Bezeichnung als Domäne der obersten Ebene mit `{ifmobile:mobi}{ifnotmobile:com}` hinzu.

  Beispiel: `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` bringt mobile Benutzer zu www.example.mobi und Nicht-Mobilbenutzer zu www.example.com.

In beiden Fällen enthalten die Basis-URLs mit Such-, Social- und Commerce-Tracking die nicht kodierten `{}` -Tags und alle zusätzlichen Parameter, die an die Basis-URL angehängt sind.

>[!NOTE]
>
>Verwenden Sie keine vollständige URL als Wert für ifnotmobile und ifmobile Parameter. Verwenden Sie nur den variablen Teil der URL (z. B. &quot;m&quot;versus &quot;www&quot;oder &quot;mobi&quot;versus &quot;com&quot;).

+++

+++([!DNL Google Ads] Kampagnen im Suchnetzwerk) Welche Daten werden für heute angezeigt?

[!DNL Google Ads] Leistungsmetriken auf Kampagnenebene im Suchnetzwerk für den aktuellen Tag werden um 8:00 Uhr und 16:00 Uhr in der Zeitzone des Werbetreibenden abgerufen.

Auf der Registerkarte [!UICONTROL Campaigns] in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] und in der Ansicht [!UICONTROL Optimization] > [!UICONTROL Portfolios] enthalten die Daten die zuletzt synchronisierten Daten, wenn Sie einen Bericht über [!UICONTROL Today] oder einen benutzerdefinierten Datumsbereich erstellen, der den aktuellen Tag enthält.

>[!NOTE]
>
>Daten für Klicks, Impressionen und Konversionen werden um drei Stunden verzögert und erst nach der nächsten Datenabfrage abgeschlossen.

+++

+++Was ist der Unterschied zwischen einer Tracking-Vorlage und einem Landingpage-Suffix?

Verwenden Sie das Suffix einer Landingpage nur für Werbenetzwerke, die paralleles Tracking unterstützen. In Search, Social und Commerce sollten sowohl Tracking-Vorlagen als auch Landingpage-Suffixe eine Klick-ID aus dem Anzeigennetzwerk enthalten, Tracking-Vorlagen enthalten jedoch zusätzliche Tracking-Parameter.

Weitere Informationen dazu, wie Tracking-Vorlagen und Suffixe von Landingpages geladen werden, wenn ein Benutzer auf eine Anzeige klickt, finden Sie in den nächsten häufig gestellten Fragen zum [parallelen Tracking-Support](#parallel-tracking) .

+++

+++([!DNL Google Ads] und [!DNL Microsoft Advertising]) Unterstützt Search, Social und Commerce das parallele Tracking für Anzeigen in [!DNL Google Ads] oder [!DNL Microsoft Advertising]? {#parallel-tracking}

Beim parallelen Tracking werden Kunden direkt von Ihrer Anzeige an Ihre endgültige URL gesendet. Dazu können angehängte Parameter aus dem finalen URL-Suffix oder das &quot;Suffix der Landingpage&quot;gehören. Ihre Tracking-Vorlagen-URL (mit zusätzlichen Parametern für die Klick-Messung) wird separat im Hintergrund geladen. Daher wird Ihre Landingpage schneller geladen.

Search, Social und Commerce unterstützt das parallele Tracking von Such- und Einkaufskampagnen mithilfe der Klick-ID des Anzeigennetzwerks (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für [!DNL Google Ads]). Verwenden Sie eine [Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) oder [Kampagnenebene](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (in den Werbenetzwerken als &quot;[!DNL final URL suffix]&quot; bezeichnet), die an Landingpage-URLs angehängt wird, um Klicks auf untergeordnete Anzeigen von Browsern zu verfolgen, die paralleles Tracking unterstützen. Siehe die erforderlichen Suffix-Formate für  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderliche Suffix-Formate für  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).[

Wenn ein Benutzer Ihre Anzeige in einem Browser anzeigt, der kein paralleles Tracking unterstützt, verwendet das Werbenetzwerk stattdessen das sequenzielle Tracking: Kunden werden zunächst an Ihre Tracking-Vorlage-URL gesendet. Dadurch können Kunden zu Tracking-Zwischenservern umgeleitet werden, bevor sie zur endgültigen URL weitergeleitet werden (was zusätzliche Parameter in einem Landingpage-Suffix enthalten kann). Alle Tracking-Vorlagen für ein Anzeigen-Netzwerk-Konto sollten denselben Klick-ID-Parameter enthalten, den Sie in der [!UICONTROL Landing Page Suffix] verwenden. Weitere Informationen finden Sie in den Vorlagenformaten [ Tracking für  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und in den Formaten der [Tracking-Vorlage für  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) .
+++

+++ Warum enthalten Tracking-URLs für meine Anzeigen &quot;`&EV_HASH={<hash>}`?&quot;

Wenn Sie Anzeigen mit einem [Produkt-Inventar-Feed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) für ein Konto mit der Pixelumleitung &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;und mit Keyword- und kreativem Tracking hochladen, fügt Search, Social und Commerce den Hash-Parameter und Wert zur Tracking-Vorlage oder Ziel-URL der Anzeige hinzu, um zu ermitteln, ob diese mit der Inventar-Feed-Funktion erstellt wurde.
+++

## Inventar-Feeds

+++(Produkt-Inventar-Feeds) Sollte ich Anzeigen anhalten oder löschen, die veraltet sind oder für ein Produkt gelten, dessen Lagerbestand unter einem bestimmten Minimum liegt?

Dies hängt von den Geschäftsanforderungen des Werbetreibenden ab.

Wenn Sie Anzeigen anhalten, werden sie reaktiviert, wenn Sie dieselbe Anzeige erneut senden oder die Lagerbestände über das Minimum hinausgehen. Auf diese Weise können Sie den Verlauf der Anzeige beibehalten.

Wenn Sie Anzeigen löschen und erneut senden, werden neue Anzeigen erstellt und historische Daten für die neuen Anzeigen gesammelt. Wenn Sie jedoch nicht erwarten, gelöschte Anzeigen erneut einzureichen, ist es nicht wichtig, historische Daten zu haben.
+++

+++(Produkt-Inventar-Feeds) Wenn ich eine Anzeigenvorlage lösche und dann eine neue, identische Vorlage erstelle, fehlen Elemente in der nächsten Feed-Datei, die angehalten wird (wenn die Feed-Dateieinstellungen dafür konfiguriert sind)?

Wenn in der nächsten Feed-Datei Zeileneinträge fehlen und Sie diese Zeileneinträge noch nicht über eine vorherige Feed-Datei aus der neuen Vorlage gepostet haben, werden die fehlenden Zeileneinträge nicht als &quot;fehlend&quot;erkannt, sodass sie nicht erstellt werden. Um dies zu vermeiden, propagieren Sie die vorherige Feed-Datei durch die neue Vorlage und posten Sie die Daten, bevor Sie Daten aus einer neuen Datei propagieren und posten.
+++

+++(Produktbestand-Feeds) Kann ich die Preise für meine Produkte aktualisieren, ohne dass sich dies auf die Qualitätsbewertung einer Anzeige auswirkt?

Für [!DNL Google Ads] -Kampagnen ja: Die Variablen [!DNL Google Ads] `{Param 1}` und `{Param 2}` ermöglichen es Ihnen, numerische Werte dynamisch in eine Anzeigenvariante einzufügen, ohne die Anzeige zu löschen und neu zu erstellen und somit die Qualitätsbewertung nicht zu beeinträchtigen.

Um eine `{Param 1}` - oder `{Param 2}` -Variable für Ihre Preisdaten zu verwenden, ordnen Sie die Preisspalte in Ihrer Datendatei dieser Variablen in den entsprechenden Feed-Vorlagen zu und fügen Sie dann die -Variable in Ihre Anzeigenvariationsvorlagen ein.

Wenn die Spalte beispielsweise &quot;Preis&quot;heißt, öffnen Sie die Feed-Vorlage, die die Anzeigen erstellt, klicken Sie in das Eingabefeld neben **[!UICONTROL Param 1]** und klicken Sie dann in der Liste [!UICONTROL Feeds/Available Columns] auf die Spalte **[!UICONTROL Price]** , wodurch `[Price]` als Wert für [!UICONTROL Param 1] eingefügt wird. Fügen Sie dann in die Anzeigenvariationsvorlage unten in der Feed-Vorlage den Wert &quot;`{param1:default text}`&quot;ein, wobei &quot;Standardtext&quot;Text ist, der verwendet werden soll, wenn die Parameterspalte in der Feed-Datei für eine Anzeigenzeile leer ist.

Wenn Sie Daten senden, können die Datenfelder für die Spalten [!UICONTROL Param1] und [!UICONTROL Param2] bis zu 25 Zeichen enthalten, darunter numerische Daten, Währungssymbole und Währungscodes sowie die folgenden nicht numerischen Zeichen: `, . % + - /`
+++

+++ Meine Kampagnen, die aus Inventar-Feeds generiert wurden, haben viele verwaiste Transaktionen.

Wenn die [Feed-Dateneinstellungen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) so konfiguriert sind, dass Anzeigen in verschiedenen Situationen gelöscht werden, können alle verzögerten Konversionen, die nach Klicks auf die Anzeige auftreten, zu [verwaisten Transaktionen](/help/search-social-commerce/glossary.md#o-p) führen. Die Best Practice ist, Anzeigen anzuhalten, anstatt sie zu löschen. Wenn eine Werbeanzeige nach langer Zeit immer noch keinen Umsatz erhalten hat, können Sie sie über ein Bulksheet oder die Anzeigenverwaltungsansicht löschen.
+++

## Leistungsprobleme im Zusammenhang mit Konten und Kampagnen

+++ Einige meiner Kampagnen geben mehr oder weniger aus als die Kampagnenbudgets.

* Dies ist in einem optimierten Portfolio normal, das mit der Option &quot;[!UICONTROL Auto-adjust campaign budget limits]&quot; konfiguriert ist. Wenn diese Option aktiviert ist, können Sie bis zum *N*-fachen des Budgets jeder Kampagne ausgeben, wobei *N* der Wert der Einstellung &quot;[!UICONTROL Multiple]&quot; ist. Diese Option ermöglicht es der Optimierungsfunktion, die Ausgaben für einzelne Kampagnen nach Bedarf anzupassen und gleichzeitig das gesamte Portfolio so zu steuern, dass es sein Ziel erreicht.
* Wenn [!DNL Google Ads]-Kampagnen ein gemeinsames Budget verwenden, passt [!DNL Google Ads] die Ausgaben für einzelne Kampagnen nach Bedarf an, um das gesamte gemeinsam genutzte Budget auszugeben.
+++
