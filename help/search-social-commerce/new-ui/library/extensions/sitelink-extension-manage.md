---
title: Verwalten freigegebener Sitelink-Erweiterungen
description: Erfahren Sie, wie Sie freigegebene Sitelink-Erweiterungen erstellen, bearbeiten und löschen.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%
---
# Verwalten freigegebener Sitelink-Erweiterungen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Konten*

Ein Sitelink ist ein zusätzlicher Text-Link in einer Textanzeigenliste. Verwenden Sie Sitelinks, um Benutzer direkt zu bestimmten Seiten auf Ihrer Site zu führen. Das Anzeigennetzwerk bestimmt, welche Site-Links angezeigt werden, basierend auf ihrer Relevanz für die Anzeige.

Optional können Sie für jeden Sitelink einen beschreibenden Text einfügen. Das Werbenetzwerk kann auch Kopien von vorhandenen Anzeigen im Konto anzeigen, wenn dies für den Sitelink äußerst relevant ist. [!DNL Google Ads] können 2-6 Sitelinks in einer Desktop-Anzeige und bis zu vier Sitelinks in einer Mobile-Anzeige anzeigen. [!DNL Microsoft Advertising] können zwei, vier oder sechs Sitelinks mit Beschreibungen oder 4-6 ohne Beschreibungen anzeigen.

Sie erstellen freigegebenen Sitelink-Text und Einstellungen auf Kontoebene für ein [synchronisiertes Anzeigennetzwerkkonto](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Sitelinks in der -Bibliothek werden erst dann für Anzeigen verwendet, wenn Sie sie mit Kontoentitäten verknüpfen.

## Über die [!UICONTROL Sitelinks]- und [!UICONTROL Associations] {#sitelink-view-about}

In **[!UICONTROL Library]>[!UICONTROL Extensions]** wird auf der Registerkarte **[!UICONTROL Sitelinks]** eine Liste der freigegebenen Sitelinks auf Kontoebene angezeigt. Auf der Registerkarte **[!UICONTROL Associations]** werden die Verknüpfungen zwischen Erweiterungen und Kontoentitäten aufgelistet.

Zum Anzeigen dieser Registerkarten ist die Berechtigung [!UICONTROL View Extensions] erforderlich. Das Erstellen, Bearbeiten und Löschen von Sitelinks sowie das Erstellen oder Löschen von Verknüpfungen erfordert die Berechtigung [!UICONTROL Edit Extensions] .

In der Hilfe zum Anzeigen-Netzwerk finden Sie die maximale Anzahl von Erweiterungen pro [Google Ads-](https://support.google.com/google-ads/answer/6372658) und pro [Microsoft Advertising-Konto](https://help.ads.microsoft.com/#apex/3/en/52001).

### Verfügbare Aktionen

* [Erstellen eines freigegebenen Sitelink](#sitelink-create)

* [Einstellungen für freigegebene Sitelinks bearbeiten](#sitelink-edit)

* [Freigegebene Sitelinks löschen](#sitelink-delete)

* [Verknüpfen freigegebener Sitelinks mit Konten, Kampagnen und Anzeigengruppen](ad-extension-association-manage.md#sitelink-associate)

* [Löschen von Erweiterungsverknüpfungen](ad-extension-association-manage.md#association-delete)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

## Erstellen eines freigegebenen Sitelink {#sitelink-create}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Library]>[!UICONTROL Extensions]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Sitelinks]** .

1. Klicken Sie auf **[!UICONTROL Create Sitelink]**.

1. Wählen Sie in **[!UICONTROL Basic Settings]** das Anzeigennetzwerk und das Konto aus.

1. Geben Sie die [Einstellungen für freigegebene Sitelinks](#shared-sitelink-settings) ein.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen. Um eine Einstellung zu ändern, klicken Sie im entsprechenden Abschnitt auf **[!UICONTROL Edit]**.

1. Klicken Sie auf **[!UICONTROL Create]**.

Nachdem Sie den Sitelink erstellt haben[ (verknüpfen Sie ihn mit einem Konto, einer Kampagne oder einer Anzeigengruppe](ad-extension-association-manage.md#sitelink-associate).

## Einstellungen für freigegebene Sitelinks bearbeiten {#sitelink-edit}

Sie können jeweils nur einen freigegebenen Sitelink bearbeiten. Sie können das Startdatum nach der Erstellung nicht ändern.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Library]>[!UICONTROL Extensions]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Sitelinks]** .

1. Aktivieren Sie das Kontrollkästchen neben einem Sitelink.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Einstellungen für freigegebene Sitelinks](#shared-sitelink-settings).

1. Klicken Sie auf **[!UICONTROL Review and Save]**, überprüfen Sie die Einstellungen, und klicken Sie dann auf **[!UICONTROL Update]**.

Sie können auch die **[!UICONTROL Base URL]** oder **[!UICONTROL Tracking Template]** eines Sitelinks direkt in der Datentabelle bearbeiten, indem Sie auf seinen Wert klicken.

## Freigegebene Sitelinks löschen {#sitelink-delete}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Library]>[!UICONTROL Extensions]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Sitelinks]** .

1. Aktivieren Sie das Kontrollkästchen neben jedem freigegebenen Sitelink, der gelöscht werden soll.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

Wenn Sie eine Verknüpfung entfernen möchten, ohne den freigegebenen Sitelink aus der Bibliothek zu löschen, [ Sie stattdessen die Verknüpfung ](ad-extension-association-manage.md#association-delete).

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

## Einstellungen für freigegebene Sitelinks {#shared-sitelink-settings}

Weitere Richtlinien und Gründe für die Ablehnung von Sitelink finden Sie unter [Google Ads Sitelink-Anforderungen](https://support.google.com/adspolicy/answer/1054210) und [Microsoft Advertising Sitelink-Anforderungen](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Der Text, der für den Link angezeigt werden soll. Es kann bis zu 25 Einzelbyte- oder 12 Doppelbyte-Zeichen enthalten. Der Link-Text muss innerhalb des Kontos oder der Kampagne eindeutig sein.

>[!NOTE]
>
>([!DNL Google Ads]) Vorhandener Text mit 35 Zeichen wird in Anzeigen auf Desktops und Tablets angezeigt, nicht jedoch auf Mobilgeräten.

**[!UICONTROL Status]:** Der Anzeigestatus des Sitelinks: **[!UICONTROL Active]** oder **[!UICONTROL Deleted]** für vorhandene Sitelinks. Neue Sitelinks sind standardmäßig aktiv.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Zusätzlicher Text, der vom Werbenetzwerk unter dem Link-Text angezeigt werden kann. Um eine Beschreibung einzufügen, geben Sie beide Felder ein. Jede kann bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.

**[!UICONTROL Start Date]:** (Optional; nur Erstellung) Das erste Datum, an dem der Sitelink angezeigt werden kann. Der Standardwert ist der aktuelle Tag. Um ein Datum in der Zukunft anzugeben, geben Sie es im Format MM/TT/JJJJ ein oder verwenden Sie die Datumsauswahl. Das Startdatum ist für vorhandene Sitelinks schreibgeschützt.

**[!UICONTROL End Date]:** (Optional) Das letzte Datum, an dem der Sitelink angezeigt werden kann. Standardmäßig kann der Sitelink unbegrenzt angezeigt werden. Um ein Enddatum festzulegen, geben Sie es im Format MM/TT/JJJJ ein oder verwenden Sie die Datumsauswahl.

**[!UICONTROL Mobile Preference]:** (Optional) Ermöglicht dem Netzwerk, zu versuchen, die Erweiterung für Benutzer von Mobilgeräten anzuzeigen, anstatt für Desktop- oder Tablet-Benutzer. Standardmäßig ist diese Option nicht aktiviert und die Erweiterung kann auf jedem Gerätetyp angezeigt werden. Das Netzwerk garantiert nicht, dass es die Erweiterung auf dem bevorzugten Gerätetyp anzeigt.

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-URL, einschließlich der Off-Landing-Domain-Umleitungen und Tracking-Parameter, wobei die endgültige Landingpage-URL in einen -Parameter eingebettet ist. Beispiel: `https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`.

In dieser Ansicht müssen Werte, die für [!UICONTROL Base URL] und [!UICONTROL Tracking Template] eingegeben wurden, mit `http://` oder `https://` beginnen und dürfen keine Leerzeichen enthalten.

* Wenn die Kampagneneinstellungen **[!UICONTROL EF Redirect]** und **[!UICONTROL Auto Upload]** enthalten, stellen Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode als Präfix voran.

* Informationen zu Parametern, die die endgültige URL einbetten, finden Sie in der [Dokumentation zu Microsoft Advertising ](https://help.ads.microsoft.com/#apex/3/en/56799) den Parametern „Nur Tracking-Vorlage“ in der [Dokumentation zu Google Ads ValueTrack](https://support.google.com/google-ads/answer/6305348).

* Sie können URL-Parameter und benutzerdefinierte Parameter auf Kampagnenebene einbeziehen, die durch kaufmännische Und-Zeichen (`&`) und Umleitungen und Tracking von Drittanbietern getrennt sind.

* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt Vorlagen auf höheren Ebenen.

>[!NOTE]
>
>* Bei Konten mit endgültigen URLs kann die Basis-URL Umleitungen innerhalb der Landingpage-Domain oder Subdomain enthalten, jedoch nicht außerhalb der Landingpage-Domain. Das Anzeigennetzwerk extrahiert die Domain, um die Anzeige-URL zu erstellen.
>* ([!DNL Google Ads]) Jeder Sitelink in einer Kampagne oder Anzeigengruppe muss über eine eindeutige Landingpage mit etwa 80 % eindeutigem Inhalt verfügen. Verwenden Sie auf derselben Seite keine Links zu mehreren Ankern als separate Sitelink-Landingpages.
>* ([!DNL Google Ads]) Durch die Aktualisierung einer Tracking-Vorlage auf Sitelink- oder Keyword-Ebene werden die relevanten Anzeigen erneut zur Überprüfung übermittelt. Durch die Aktualisierung auf Konto-, Kampagnen- oder Anzeigengruppenebene werden die Anzeigen nicht erneut gesendet.
>* ([!DNL Microsoft Advertising]) Sie können Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne die Anzeigen erneut zur Genehmigung einzureichen.
>* ([!DNL Google Ads]) Vermeiden Sie Makros, die nicht durch Klicks aus Quellen ersetzt werden, die paralleles Tracking ermöglichen. Wenn Makros erforderlich sind, fügt Ihr Adobe-Account-Team diese zusammen mit dem Support oder dem Implementierungsteam hinzu.

## Leistungsdaten für Sitelinks {#sitelink-performance}

Search, Social und Commerce zugeordnet sind, die auf eine Anzeigenerweiterung und die daraus resultierenden Konversionen in das Keyword klicken, das mit der Anzeige verknüpft ist, in der die Erweiterung angezeigt wird. Kosten- und Klickdaten auf Erweiterungsebene sind in Search, Social und Commerce nicht verfügbar.

In der [!UICONTROL Transaction Report] identifiziert ein [!UICONTROL Link Type] Wert von `sl:<Sitelink text>`, z. B. `sl:See Current Offers`, eine Transaktion über einen Sitelink und nicht über die Anzeige selbst. Siehe &quot;[Transaktionsbericht](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md).

Sie können die Kosten für die Erweiterung anzeigen und auf Daten in der Benutzeroberfläche des Anzeigennetzwerks klicken.

>[!MORELIKETHIS]
>
>* [Verwalten von Google Ads Shared Callout-Erweiterungen](callout-extension-manage.md)
>* [Verwalten von Anzeigenerweiterungsverknüpfungen](ad-extension-association-manage.md)
