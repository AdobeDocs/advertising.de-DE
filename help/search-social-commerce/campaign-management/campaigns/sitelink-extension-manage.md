---
title: Verwalten freigegebener Sitelinks
description: Erfahren Sie, wie Sie freigegebene Sitelink-Erweiterungen erstellen und verwalten.
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: c3b8e387cfc38d195e77761791e689fd094d8f39
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Verwalten freigegebener Sitelinks

*[!DNL Google Ads]und [!DNL Microsoft Advertising] nur*

Erstellen und verwalten Sie freigegebene Sitelinks auf Kontoebene für synchronisierte [!DNL Google Ads] - oder [!DNL Microsoft Advertising] -Konten aus der Bibliothek [!UICONTROL Extensions] > [!UICONTROL Sitelinks].

## Erstellen eines freigegebenen Sitelink

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die [freigegebenen Sitelink-Einstellungen](#shared-sitelink-settings) ein.

1. Klicken Sie auf **[!UICONTROL Post]**.

Nachdem Sie einen Sitelink erstellt haben, können Sie ihn [einem Konto, einer Kampagne oder einer Anzeigengruppe zuweisen](sitelink-extension-associate.md).

## Bearbeiten freigegebener Sitelink-Einstellungen

Sie können jeweils einen freigegebenen Sitelink bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Aktivieren Sie das Kontrollkästchen neben dem zu bearbeitenden Sitelink.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die Einstellungen für [freigegebene Sitelink](#shared-sitelink-settings).

1. Klicken Sie auf **[!UICONTROL Post]**.

## Löschen freigegebener Sitelinks

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem freigegebenen Sitelink, den Sie löschen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter &quot;[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicken Sie in der Symbolleiste auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und wählen Sie **[!UICONTROL Delete]** aus.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Freigegebene Sitelink-Einstellungen {#shared-sitelink-settings}

Weitere Richtlinien und Gründe für die Ablehnung von Sitelink finden Sie in den Anforderungen für die Sitelink-Erweiterung [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) und [[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206) .

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Der Text, der für den Link angezeigt werden soll. Sie kann bis zu 25 Einzelbyte- oder 12 Doppelbyte-Zeichen enthalten. Der Link-Text muss innerhalb des Kontos oder der Kampagne eindeutig sein.

>[!NOTE]
>
>([!DNL Google Ads]) Der vorhandene Text von 35 Zeichen wird in Anzeigen auf Desktops und Tablets, jedoch nicht auf Mobilgeräten angezeigt.

**[!UICONTROL Status]:** Der Anzeigestatus des Sitelinks: *[!UICONTROL Active]* oder *[!UICONTROL Deleted]* (nur vorhandene Sitelinks). Die Standardeinstellung für neue Sitelinks ist *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Zusätzlicher Text, den die Suchmaschine unter dem Link-Text anzeigen kann. Um eine Beschreibung einzuschließen, geben Sie Werte für beide Beschreibungsfelder ein. Jedes Beschreibungsfeld kann bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.

**[!UICONTROL Start Date]:** (Kampagnen mit bestehenden Sitelinks oder nur ohne Sitelinks; optional) Das erste Datum, an dem der Sitelink mit Anzeigen in der Kampagne angezeigt werden kann. Die Standardeinstellung für neue Sitelinks ist der aktuelle Tag. Um ein künftiges Startdatum anzugeben, geben Sie ein Datum im Format MM/TT/JJJJ oder M/D/JJJJ ein oder klicken Sie auf   und ein Datum auswählen.

**[!UICONTROL End Date]:** (Optional) Das letzte Datum, an dem der Sitelink mit Anzeigen in der Kampagne angezeigt werden kann. Standardmäßig kann der Sitelink auf unbestimmte Zeit angezeigt werden. Um ein Enddatum anzugeben, geben Sie ein Datum im Format MM/TT/JJJJ oder M/D/JJJJ ein oder klicken Sie auf   und ein Datum auswählen.

**[!UICONTROL Mobile Preference]:** (Optional) Ermöglicht dem Netzwerk, die Anzeigenerweiterung für Benutzer mobiler Geräte und nicht für Benutzer von Desktop- oder Tablet-Geräten anzuzeigen. Standardmäßig ist die Option nicht aktiviert und die Anzeigenerweiterung wird auf einem beliebigen Gerätetyp angezeigt.

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
>* ([!DNL Google Ads]) Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder die Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die finale URL/Landingpage in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` , um eine Umleitung einzuschließen.

* Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;Automatisches Hochladen&quot;enthalten, setzt die Suche, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Klick-Tracking-Code voran.

* Informationen zu unterstützten Parametern zum Einbetten der endgültigen URL finden Sie in der ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder ([!DNL Google Ads] only) den Parametern &quot;Nur Tracking-Vorlage&quot;im Abschnitt &quot;Verfügbare [!DNL ValueTrack] Parameter&quot;in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

* Sie können optional URL-Parameter und alle für die Kampagne definierten benutzerdefinierten Parameter einbeziehen, getrennt durch kaufmännische Und-Zeichen (&amp;), z. B. `{lpurl}?matchtype={matchtype}&device={device}`.

* Sie können optional Umleitungen und Tracking von Drittanbietern hinzufügen.

>[!NOTE]
>
>* Wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, setzt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode voran.
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Suchbegriffeinstellungen einen Wert enthalten, wird der Suchbegriffwert angewendet.
>* ([!DNL Google Ads]) Wenn Sie eine Tracking-Vorlage auf Sitelink- oder Suchbegriffebene aktualisieren, werden die relevanten Anzeigen erneut zur Überprüfung eingereicht. Sie können Ihre Tracking-Vorlagen auf Konto-, Kampagnen- oder Anzeigengruppenebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
>* ([!DNL Microsoft Advertising]) Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
>* Vermeiden Sie bei [!DNL Google Ads] die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.

>[!MORELIKETHIS]
>
>* [Über Sitelink-Erweiterungen](sitelink-extension-about.md)
>* [Verknüpfen freigegebener Sitelinks mit Konten, Kampagnen und Anzeigengruppen](sitelink-extension-associate.md)
