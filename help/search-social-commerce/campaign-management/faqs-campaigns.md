---
title: Häufig gestellte Fragen zu Kampagnen
description: Antworten auf Fragen zur Kampagnenverwaltung und zu den Ansichten der Kampagnendaten.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: 88b415fff52d623a5daeb00355bfe00054d5402b
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Häufig gestellte Fragen zur Kampagnenverwaltung

## Allgemeine Informationen

+++Kann ich Kampagnen und Komponenten von einem Konto in ein anderes verschieben?

Verschieben oder kopieren Sie keine Kampagnen- oder Kampagnenkomponente, die eine eindeutige ID hat, in ein Konto mit einer anderen Konto-ID. Dies führt zu Datenfehlern.
+++

+++Wann werden Klickdaten aus den Werbenetzwerken aktualisiert?

Der Prozess des Abrufs der Klickdaten des Vortages aus den Suchmaschinen beginnt um 06:00 in der Zeitzone des Werbetreibenden.

Darüber hinaus werden [!DNL Google Ads] Leistungsmetriken auf Kampagnenebene im Suchnetzwerk für den aktuellen Tag um 08 :00 16 :00 in der Zeitzone des Werbetreibenden abgerufen.
+++

+++Welche Aktionen führen dazu, dass Keywords und Anzeigen ihren Verlauf verlieren?

>[!NOTE]
>
>(Werbetreibende mit Portfolios) Erwarten, dass die Performance neuer Keyword- und Match-Type-Kombinationen volatil ist, während Search, Social und Commerce Daten sammeln, um Modelle für sie zu erstellen.

**Aktionen in den [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns], im Bulksheet-Buchungsprozess und im eigenen Editor des Anzeigennetzwerks:**

Das vorhandene Keyword oder die Anzeige wird gelöscht und ein weiteres wird erstellt, wenn:

* ([!DNL Baidu], [!DNL Google Ads] und [!DNL Yandex]) Sie bearbeiten einen Schlüsselwortnamen.

* ([!DNL Google Ads], [!DNL Microsoft Advertising] und [!DNL Yandex]) Sie ändern den Übereinstimmungstyp eines Keywords.

* Sie verschieben ein Keyword zwischen Anzeigengruppen.

* ([!DNL Google Ads] dynamische Suchanzeigen, [!DNL Microsoft Advertising] erweiterte Textanzeigen und alle Anzeigentypen in anderen unterstützten Anzeigennetzwerken) Sie bearbeiten eine Anzeigenkopie (Überschrift/Titel oder Beschreibung) oder ein Anzeigenbild.

* Sie können eine Anzeige zwischen Anzeigengruppen verschieben.

**Ereignisse im Buchungsprozess des Produktinventar-Feeds:**

Eine vorhandene Anzeige oder ein vorhandenes Keyword wird gelöscht und eine andere wird erstellt, wenn:

* Eine Feed-Datei enthält einen neuen Wert für eine Spalte, die in einer Anzeigenvariante verwendet wird.

* Die Vorlageneinstellungen für eine Anzeige haben sich seit der letzten Verbreitung geändert.

* Eine neue Feed-Datei enthält eine Zeile für eine Anzeige oder ein Keyword, die bzw. das a) in einer vorherigen Datei enthalten war, aber b) seitdem weggelassen wurde und gemäß den Feed-Dateneinstellungen angehalten oder gelöscht wurde.

Abhängig von den [Feed-Dateneinstellungen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) kann eine vorhandene Anzeige oder ein vorhandenes Keyword gelöscht werden, wenn:

* Eine neue Feed-Datei enthält keine Zeile für eine vorhandene Anzeige oder ein vorhandenes Keyword.

* Das geplante Enddatum für die Komponenten einer geposteten Feed-Datei tritt auf.

* Der Lagerbestand eines Elements sinkt unter ein in den Feed-Dateneinstellungen angegebenes Minimum.
+++

+++([!DNL Google Ads] Kampagnen) Änderungen an den Anzeigenamen für meine [!DNL Google] Konversionen wurden rückgängig gemacht.

Wenn Sie die Anzeigenamen der Konversionsmetriken in Search, Social und Commerce ändern, werden Ihre Änderungen mit den in [!DNL Google Ads] konfigurierten Namen überschrieben. Nehmen Sie in [!DNL Google Ads] alle Namensänderungen vor.
+++

+++(Google Ads-Kampagnen) Kann ich für Kampagnen in Portfolios ein gemeinsames Budget verwenden?

Für optimale Ergebnisse sollten Sie [!DNL Google Ads] Kampagnen nicht zu einem [!DNL Google Ads] freigegebenen Budget hinzufügen, wenn sie sich in optimierten Portfolios befinden, die auf &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; konfiguriert sind. Wenn Sie dies tun, überschreibt [!DNL Google Ads] die für Search, Social und Commerce optimierten Kampagnenbudgets, was zu Ineffizienzen bei Geboten führen kann.
+++

+++([!DNL Google Ads] Kampagnen) Kann ich mobile und nicht mobile Benutzer an verschiedene Landingpages senden?

Sie können die [!DNL Google Ads] [!DNL ValueTrack] Parameter `{ifmobile}` und `{ifnotmobile}` verwenden, um den Domain-Namen der Landingpage auf eine von zwei Arten zu bestimmen, je nachdem, was für Ihre Sites gilt:

* Fügen Sie die Mobile-Bezeichnung mithilfe von `{ifmobile:m}{ifnotmobile:www}` als Host-Server ein.

  Beispielsweise führt `http://{ifmobile:m}{ifnotmobile:www}.example.com` Benutzer von Mobilgeräten zu m.example.com und Benutzer von anderen Geräten zu www.example.com.

* Fügen Sie die Mobile-Bezeichnung mithilfe von `{ifmobile:mobi}{ifnotmobile:com}` als Domain der obersten Ebene ein.

  Beispielsweise führt `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` mobile Benutzer zu www.example.mobi und nicht mobile Benutzer zu www.example.com.

In beiden Fällen enthalten die Basis-URLs mit Search-, Social- und Commerce-Tracking die nicht kodierten `{}`-Tags und alle zusätzlichen Parameter, die an die Basis-URL angehängt werden.

>[!NOTE]
>
>Verwenden Sie keine vollständige URL als Wert für die Parameter „ifnotmobile“ und „ifmobile“. Verwenden Sie nur den variablen Teil der URL (z. B. „m“ versus „www“ oder „mobi“ versus „com„).

+++

+++([!DNL Google Ads] Kampagnen im Suchnetzwerk) Welche Daten werden für heute angezeigt?

[!DNL Google Ads] Leistungsmetriken auf Kampagnenebene im Suchnetzwerk für den aktuellen Tag werden um 08:00 und 16 :00 in der Zeitzone des Werbetreibenden abgerufen.

Wenn Sie auf der Registerkarte [!UICONTROL Campaigns] sowohl in der Ansicht [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] als auch in der Ansicht [!UICONTROL Optimization] > [!UICONTROL Portfolios] Berichte zu [!UICONTROL Today] oder einem benutzerdefinierten Datumsbereich erstellen, der den aktuellen Tag enthält, umfassen die Daten die zuletzt synchronisierten Daten.

>[!NOTE]
>
>Daten für Klicks, Impressionen und Konversionen sind um drei Stunden verzögert und erst beim nächsten Daten-Pull vollständig.

+++

+++Was ist der Unterschied zwischen einer Tracking-Vorlage und einem Landingpage-Suffix?

Verwenden Sie ein Landingpage-Suffix nur für Werbenetzwerke, die paralleles Tracking unterstützen. In Search, Social und Commerce sollten sowohl Tracking-Vorlagen als auch Landingpage-Suffixe eine Klick-Kennung aus dem Werbenetzwerk enthalten, aber Tracking-Vorlagen enthalten zusätzliche Tracking-Parameter.

In den nächsten häufig gestellten Fragen [Unterstützung für paralleles Tracking](#parallel-tracking) finden Sie weitere Informationen darüber, wie Tracking-Vorlagen und Landingpage-Suffixe geladen werden, wenn ein Benutzer auf eine Anzeige klickt.

+++

+++([!DNL Google Ads] und [!DNL Microsoft Advertising]) Unterstützt Search, Social und Commerce das parallele Tracking für Anzeigen in [!DNL Google Ads] oder [!DNL Microsoft Advertising]? {#parallel-tracking}

Das parallele Tracking sendet Kundinnen und Kunden direkt von Ihrer Anzeige an Ihre endgültige URL. Diese kann angehängte Parameter aus einem endgültigen URL-Suffix oder dem „Landingpage-Suffix“ enthalten. Die Tracking-Vorlagen-URL (mit zusätzlichen Parametern für die Klick-Messung) wird separat im Hintergrund geladen, was dazu führt, dass die Landingpage schneller geladen wird.

Search, Social und Commerce unterstützen paralleles Tracking für Search- und Shopping-Kampagnen mit der Klickkennung des Anzeigennetzwerks (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für [!DNL Google Ads]). Verwenden Sie eine [&#128279;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings)Kontoebene[&#x200B; oder &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)Kampagnenebene[!UICONTROL Landing Page Suffix] (in den Werbenetzwerken als &quot;[!DNL final URL suffix]&quot; bezeichnet), die an Landingpage-URLs angehängt wird, um Klicks auf untergeordnete Anzeigen von Browsern zu verfolgen, die paralleles Tracking unterstützen. Siehe die [erforderlichen Suffixformate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderlichen Suffixformate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Wenn ein(e) Benutzende(r) Ihre Anzeige in einem Browser aufruft, der kein paralleles Tracking unterstützt, verwendet das Werbenetzwerk stattdessen das sequenzielle Tracking: Kundinnen und Kunden werden zunächst an die URL Ihrer Tracking-Vorlage gesendet, die Kundinnen und Kunden möglicherweise zu Tracking-Zwischenservern weiterleitet, bevor sie zur endgültigen URL weitergeleitet werden (die zusätzliche Parameter in einem Landingpage-Suffix enthalten kann). Alle Tracking-Vorlagen für ein Werbenetzwerkkonto sollten denselben Klick-Kennungsparameter enthalten, den Sie in der [!UICONTROL Landing Page Suffix] verwenden. Siehe [Tracking-Vorlagenformate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [Tracking-Vorlagenformate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Warum enthalten Tracking-URLs für meine Anzeigen &quot;`&EV_HASH={<hash>}`?“

Wenn Sie Anzeigen mit einem [Produktinventar-Feed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) für ein Konto mit der Pixelumleitung Search, Social und Commerce und mit Keyword- und Kreativtracking-Ebene hochladen, fügt Search, Social und Commerce den Hash-Parameter und den Wert zur Tracking-Vorlage oder Ziel-URL der Anzeige hinzu, um zu identifizieren, dass sie mit der Inventar-Feed-Funktion erstellt wurde.
+++

## Inventar-Feeds

+++(Produktinventar-Feeds) Sollte ich Anzeigen, die veraltet sind oder für ein Produkt mit einem Lagerbestand unterhalb eines bestimmten Mindestbestands sind, anhalten oder löschen?

Dies hängt von den geschäftlichen Anforderungen des Werbetreibenden ab.

Wenn Sie die Anzeigen pausieren, werden sie wieder aktiviert, wenn Sie dieselbe Anzeige erneut senden oder der Lagerbestand über das Minimum hinausgeht. Auf diese Weise können Sie den Verlauf der Anzeige speichern.

Wenn Sie Anzeigen löschen und erneut senden, werden neue Anzeigen erstellt und historische Daten müssen für die neuen Anzeigen gesammelt werden. Wenn Sie jedoch nicht erwarten, gelöschte Anzeigen erneut zu senden, ist es nicht wichtig, historische Daten zu haben.
+++

+++(Produktinventar-Feeds) Wenn ich eine Anzeigenvorlage lösche und dann eine neue, identische erstellen, fehlen Elemente in der nächsten Feed-Datei, die angehalten wird (wenn die Feed-Dateieinstellungen dafür konfiguriert sind)?

Wenn in der nächsten Feed-Datei Zeileneinträge fehlen und Sie diese Zeileneinträge noch nicht über eine vorherige Feed-Datei aus der neuen Vorlage gebucht haben, werden die fehlenden Zeileneinträge nicht als „fehlend“ erkannt und daher nicht erstellt. Um dies zu vermeiden, übertragen Sie die vorherige Feed-Datei über die neue Vorlage und veröffentlichen Sie die Daten, bevor Sie sie aus einer neuen Datei übertragen und posten.
+++

+++(Produktinventar-Feeds) Kann ich die Preise für meine Produkte aktualisieren, ohne die Qualitätsbewertung einer Anzeige zu beeinflussen?

Ja: Mit den Variablen [!DNL Google Ads] [!DNL Google Ads] und `{Param 1}` können Sie für `{Param 2}` Kampagnen numerische Werte dynamisch in eine Anzeigenvariante einfügen, ohne die Anzeige zu löschen und neu zu erstellen und somit ohne die Qualitätsbewertung zu beeinflussen.

Um eine `{Param 1}`- oder `{Param 2}` für Ihre Preisdaten zu verwenden, ordnen Sie die Preisspalte in Ihrer Datendatei dieser Variablen in den entsprechenden Feed-Vorlagen zu und nehmen Sie die Variable dann in Ihre Anzeigenvariantenvorlagen auf.

Wenn die Spalte beispielsweise „Preis“ heißt, öffnen Sie die Feed-Vorlage, in der die Anzeigen erstellt werden, klicken Sie in das Eingabefeld neben **[!UICONTROL Param 1]** und klicken Sie dann auf die Spalte **[!UICONTROL Price]** in der [!UICONTROL Feeds/Available Columns], die `[Price]` als Wert für die [!UICONTROL Param 1] einfügt. Fügen Sie dann in die Anzeigenvariantenvorlage am unteren Rand der Feed-Vorlage `{param1:default text}` ein, wobei „Standardtext“ für Text steht, der verwendet werden soll, wenn die Parameterspalte in der Feed-Datei für eine Anzeigenzeile leer ist.

Wenn Sie Daten senden, können die Datenfelder für die [!UICONTROL Param1]- und [!UICONTROL Param2]-Spalten bis zu 25 Zeichen, einschließlich numerischer Daten, Währungssymbole und Währungs-Codes, sowie die folgenden nicht numerischen Zeichen enthalten: `, . % + - /`
+++

+++Meine über Inventar-Feeds generierten Kampagnen weisen viele verwaiste Transaktionen auf.

Wenn die [Feed-Dateneinstellungen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) so konfiguriert sind, dass Anzeigen in verschiedenen Situationen gelöscht werden, können verzögerte Konversionen, die nach Klicks auf die Anzeige auftreten, zu [verwaisten Transaktionen](/help/search-social-commerce/glossary.md#o-p) führen. Es empfiehlt sich, Anzeigen anzuhalten, anstatt sie zu löschen. Wenn eine Anzeige nach langer Zeit immer noch keinen Umsatz erhalten hat, können Sie sie über eine Bulksheet- oder Ad-Management-Ansicht löschen.
+++

## Account- und kampagnenbezogene Leistungsprobleme

+++Einige meiner Kampagnen geben mehr oder weniger aus als die Kampagnenbudgets.

* Dies ist in einem optimierten Portfolio, das mit der Option &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; konfiguriert wird, normal. Wenn diese Option aktiviert ist, kann das Budget jeder Kampagne bis *N* Mal verwendet werden, wobei *N* der Wert der Einstellung &quot;[!UICONTROL Multiple]&quot; ist. Diese Option ermöglicht es der Optimierungsfunktion, die Ausgaben für einzelne Kampagnen bei Bedarf anzupassen und gleichzeitig das gesamte Portfolio so zu steuern, dass es seine Zielsetzung erfüllt.
* Wenn [!DNL Google Ads] Kampagnen ein freigegebenes Budget verwenden, passt [!DNL Google Ads] die Ausgaben für einzelne Kampagnen nach Bedarf an, um das gesamte freigegebene Budget auszugeben.
+++
