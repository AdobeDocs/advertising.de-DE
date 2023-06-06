---
title: Verwalten freigegebener Sitelinks
description: Erfahren Sie, wie Sie freigegebene Sitelink-Erweiterungen erstellen und verwalten.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Verwalten freigegebener Sitelinks

*[!DNL Google Ads]und [!DNL Microsoft Advertising] only*

Erstellen und verwalten Sie freigegebene Sitelinks auf Kontoebene für alle synchronisierten [!DNL Google Ads] oder [!DNL Microsoft Advertising] -Konto aus [!UICONTROL Extensions] > [!UICONTROL Sitelinks] -Bibliothek.

## Erstellen eines freigegebenen Sitelink

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die [freigegebene Sitelink-Einstellungen](#shared-sitelink-settings).

1. Klicken **[!UICONTROL Post]**.

Nachdem Sie einen Sitelink erstellt haben, können Sie [Zuweisung zu einem Konto, einer Kampagne oder einer Anzeigengruppe](sitelink-extension-associate.md).

## Bearbeiten freigegebener Sitelink-Einstellungen

Sie können jeweils einen freigegebenen Sitelink bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Aktivieren Sie das Kontrollkästchen neben dem zu bearbeitenden Sitelink.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die [freigegebene Sitelink-Einstellungen](#shared-sitelink-settings).

1. Klicken **[!UICONTROL Post]**.

## Löschen freigegebener Sitelinks

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem freigegebenen Sitelink, den Sie löschen möchten.

   Tipps zur Auswahl mehrerer Zeilen finden Sie unter[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicken Sie in der Symbolleiste auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und wählen Sie **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsnachricht auf **[!UICONTROL Delete]**.

## Freigegebene Sitelink-Einstellungen {#shared-sitelink-settings}

Weitere Richtlinien und Gründe für die Ablehnung von Sitelink finden Sie in der [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) und [[!DNL Microsoft Advertising]](https://about.ads.microsoft.com/en-us/resources/policies/ad-extensions-policies) Anforderungen an die Sitelink-Erweiterung.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Der Text, der für den Link angezeigt werden soll. Sie kann bis zu 25 Einzelbyte- oder 12 Doppelbyte-Zeichen enthalten. Der Link-Text muss innerhalb des Kontos oder der Kampagne eindeutig sein.

>[!NOTE]
>
>([!DNL Google Ads]) Vorhandener Text mit 35 Zeichen wird in Anzeigen auf Desktops und Tablets, nicht aber auf Mobilgeräten angezeigt.

**[!UICONTROL Status]:** Der Anzeigestatus des Sitelink:  *[!UICONTROL Active]* oder *[!UICONTROL Deleted]* (nur bestehende Sitelinks). Die Standardeinstellung für neue Sitelinks ist *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Zusätzlicher Text, den die Suchmaschine unter dem Link-Text anzeigen kann. Um eine Beschreibung einzuschließen, geben Sie Werte für beide Beschreibungsfelder ein. Jedes Beschreibungsfeld kann bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.

**[!UICONTROL Start Date]:** (Kampagnen mit bestehenden Sitelinks oder nur ohne Sitelinks; (optional) Das erste Datum, an dem der Sitelink mit Anzeigen in der Kampagne angezeigt werden kann. Die Standardeinstellung für neue Sitelinks ist der aktuelle Tag. Um ein künftiges Startdatum anzugeben, geben Sie ein Datum im Format MM/TT/JJJJ oder M/D/JJJJ ein oder klicken Sie auf und wählen Sie ein Datum aus.

**[!UICONTROL End Date]:** (Optional) Das letzte Datum, an dem der Sitelink mit Anzeigen in der Kampagne angezeigt werden kann. Standardmäßig kann der Sitelink auf unbestimmte Zeit angezeigt werden. Um ein Enddatum anzugeben, geben Sie ein Datum im Format MM/TT/JJJJ oder M/D/JJJJ ein oder klicken Sie auf und wählen Sie ein Datum aus.

**[!UICONTROL Mobile Preference]:** (Optional) Ermöglicht dem Netzwerk, zu versuchen, die Anzeigenerweiterung für Benutzer mobiler Geräte und nicht für Benutzer von Desktop- oder Tablet-Geräten anzuzeigen. Standardmäßig ist die Option nicht aktiviert und die Anzeigenerweiterung wird auf einem beliebigen Gerätetyp angezeigt.

>[!NOTE]
>
>Das Netzwerk garantiert nicht, dass die Anzeigenerweiterung auf dem bevorzugten Gerätetyp angezeigt wird.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** Die Landingpage-URL, zu der Suchmaschinenbenutzer beim Klicken auf Ihre Anzeige weitergeleitet werden. Schließen Sie alle Parameter ein, die den Inhalt der Seite bestimmen. Wenn Sie einen Wert eingeben, überschreibt er die Basis-URL für die Anzeige.

Nachdem Sie den Datensatz gespeichert haben, enthält die Basis-URL alle für die Kampagne oder das Konto konfigurierten Anlagenparameter.

>[!NOTE]
>
>* (Konten mit finalen URLs) Die Basis-URL kann Umleitungen innerhalb der Landingpage-Domäne oder -Subdomäne, aber keine Umleitungen außerhalb der Landingpage-Domäne enthalten. Das Werbenetzwerk extrahiert die Domäne aus dieser URL und fügt optionale Anzeigepfade für die Anzeige hinzu, um die Anzeigen-URL für die Anzeige zu erstellen.
>* ([!DNL Google Ads]) Jeder Sitelink in einer Kampagne oder Anzeigengruppe muss über eine eindeutige Landingpage verfügen und der Inhalt für jede Sitelink-Landingpage muss ungefähr 80 % eindeutiger Inhalte aufweisen. Sie können beispielsweise keine Sitelinks mit Links zu mehreren Ankern auf derselben Seite haben.
>* ([!DNL Google Ads]) Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.


**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die finale/Landingpage-URL in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` , um eine Umleitung einzuschließen.

* Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;EF Redirect&quot;und &quot;Auto Upload&quot;beinhalten, setzt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Klick-Tracking-Code voran.

* Informationen zu unterstützten Parametern zum Einbetten der endgültigen URL finden Sie unter ([!DNL Microsoft Advertising] nur) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder ([!DNL Google Ads] nur) die Parameter &quot;Nur Tracking-Vorlage&quot;im Abschnitt &quot;Verfügbare ValueTrack-Parameter&quot;im [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

* Sie können optional URL-Parameter und alle für die Kampagne definierten benutzerdefinierten Parameter einbeziehen, getrennt durch kaufmännische Und-Zeichen (&amp;), z. B. `{lpurl}?matchtype={matchtype}&device={device}`.

* Sie können optional Umleitungen und Tracking von Drittanbietern hinzufügen.

>[!NOTE]
>
>* Wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot;&quot;Search, Social und Commerce setzt beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode voran.
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Suchbegriffeinstellungen einen Wert enthalten, wird der Suchbegriffwert angewendet.
>* ([!DNL Google Ads]) Wenn Sie eine Tracking-Vorlage auf Sitelink- oder Suchbegriffebene aktualisieren, werden die relevanten Anzeigen erneut zur Überprüfung eingereicht. Sie können Ihre Tracking-Vorlagen auf Konto-, Kampagnen- oder Anzeigengruppenebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
>* ([!DNL Microsoft Advertising]) Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
>* Für [!DNL Google Ads]vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.


>[!MORELIKETHIS]
>
>* [Über Sitelink-Erweiterungen](sitelink-extension-about.md)
>* [Verknüpfen freigegebener Sitelinks mit Konten, Kampagnen und Anzeigengruppen](sitelink-extension-associate.md)

