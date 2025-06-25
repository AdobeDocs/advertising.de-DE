---
title: Verwalten von freigegebenen Sitelinks
description: Erfahren Sie, wie Sie freigegebene Sitelink-Erweiterungen erstellen und verwalten.
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Verwalten von freigegebenen Sitelinks

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising]*

Erstellen und verwalten Sie freigegebene Sitelinks auf Kontoebene für alle synchronisierten [!DNL Google Ads] oder [!DNL Microsoft Advertising] Konten aus der Bibliothek [!UICONTROL Extensions] > [!UICONTROL Sitelinks] .

## Erstellen eines freigegebenen Sitelink

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Anzeigennetzwerk und den Kontonamen aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Geben Sie die [Einstellungen für freigegebene Sitelinks](#shared-sitelink-settings) ein.

1. Klicken Sie auf **[!UICONTROL Post]**.

Nachdem Sie einen Sitelink erstellt haben, können [ ihn einem Konto, einer Kampagne oder einer Anzeigengruppe zuweisen](sitelink-extension-associate.md).

## Einstellungen für freigegebene Sitelinks bearbeiten

Sie können jeweils nur einen freigegebenen Sitelink bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Sitelink, der bearbeitet werden soll.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die [Einstellungen für freigegebene Sitelinks](#shared-sitelink-settings).

1. Klicken Sie auf **[!UICONTROL Post]**.

## Freigegebene Sitelinks löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem freigegebenen Sitelink, den Sie löschen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und wählen Sie **[!UICONTROL Delete]** aus.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Einstellungen für freigegebene Sitelinks {#shared-sitelink-settings}

Weitere Richtlinien und Gründe für die Ablehnung von Sitelink finden Sie in den [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) und [[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206) Anforderungen an Sitelink-Erweiterungen.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Der Text, der für den Link angezeigt werden soll. Es kann bis zu 25 Einzelbyte- oder 12 Doppelbyte-Zeichen enthalten. Der Link-Text muss innerhalb des Kontos oder der Kampagne eindeutig sein.

>[!NOTE]
>
>([!DNL Google Ads]) Vorhandener Text mit 35 Zeichen wird in Anzeigen auf Desktops und Tablets angezeigt, nicht jedoch auf Mobilgeräten.

**[!UICONTROL Status]:** Der Anzeigestatus des Sitelinks: *[!UICONTROL Active]* oder *[!UICONTROL Deleted]* (nur vorhandene Sitelinks). Der Standardwert für neue Sitelinks ist *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Zusätzlicher Text, der von der Suchmaschine unter dem Link-Text angezeigt werden kann. Um eine Beschreibung einzuschließen, geben Sie Werte für beide Beschreibungsfelder ein. Jedes Beschreibungsfeld kann bis zu 35 Einzelbyte- oder 17 Doppelbyte-Zeichen enthalten.

**[!UICONTROL Start Date]:** (nur Kampagnen mit vorhandenen alten Sitelinks oder ohne Sitelinks; optional) Das erste Datum, an dem der Sitelink mit Anzeigen in der Kampagne angezeigt werden kann. Der Standardwert für neue Sitelinks ist der aktuelle Tag. Um ein Datum in der Zukunft anzugeben, geben Sie ein Datum im Format MM/TT/JJJJ oder M/TT/JJJJ ein oder klicken Sie auf   und wählen Sie ein Datum.

**[!UICONTROL End Date]:** (Optional) Das letzte Datum, an dem der Sitelink mit Anzeigen in der Kampagne angezeigt werden kann. Standardmäßig kann der Sitelink unbegrenzt angezeigt werden. Um ein Enddatum festzulegen, geben Sie ein Datum im Format MM/TT/JJJJ oder M/TT/JJJJ ein oder klicken Sie auf   und wählen Sie ein Datum.

**[!UICONTROL Mobile Preference]:** (Optional) Ermöglicht dem Netzwerk, zu versuchen, die Anzeigenerweiterung für Benutzer von Mobilgeräten anzuzeigen, anstatt für Desktop- oder Tablet-Benutzer. Standardmäßig ist die Option nicht aktiviert und die Anzeigenerweiterung wird auf jedem Gerätetyp angezeigt.

>[!NOTE]
>
>Das Netzwerk garantiert nicht, dass es die Anzeigenerweiterung auf dem bevorzugten Gerätetyp anzeigt.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** Die Landingpage-URL, zu der Suchmaschinenbenutzer beim Klicken auf Ihre Anzeige geleitet werden. Schließen Sie alle Parameter ein, die den Inhalt der Seite bestimmen. Wenn Sie einen Wert eingeben, überschreibt dieser die Basis-URL für die Anzeige.

Nachdem Sie den Datensatz gespeichert haben, enthält die Basis-URL alle für die Kampagne oder das Konto konfigurierten Anlagenparameter.

>[!NOTE]
>
>* (Konten mit endgültigen URLs) Die Basis-URL kann Umleitungen innerhalb der Landingpage-Domain oder Subdomain enthalten, jedoch keine Umleitungen außerhalb der Landingpage-Domain. Das Werbenetzwerk extrahiert die Domain aus dieser URL und fügt optionale Anzeigepfade für die Anzeige hinzu, um die Anzeige-URL für die Anzeige zu erstellen.
>* ([!DNL Google Ads]) Jeder Sitelink in einer Kampagne oder Anzeigengruppe muss über eine eindeutige Landingpage verfügen und der Inhalt für jede Sitelink-Landingpage muss zu etwa 80 % über eindeutige Inhalte verfügen. Sie können beispielsweise keine Sitelinks mit Links zu mehreren Ankern innerhalb derselben Seite haben.
>* ([!DNL Google Ads]) Verwenden Sie keine Makros, da diese nicht durch Klicks aus Quellen ersetzt werden, die paralleles Tracking ermöglichen. Wenn der Werbetreibende Makros verwenden muss, sollte das Adobe-Account-Team den Kunden-Support oder das Implementierungsteam kontaktieren, um diese hinzuzufügen.

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und auch die endgültige/Landingpage-URL in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`, um eine Umleitung einzuschließen.

* Bei Adobe Advertising-Konversionsverfolgung, die angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und „Automatisches Hochladen“ enthalten, stellt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Klick-Tracking-Code voran.

* Informationen zu den unterstützten Parametern zum Einbetten der endgültigen URL finden Sie unter den Parametern (nur [!DNL Microsoft Advertising]) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder (nur [!DNL Google Ads]) „Tracking-Vorlage“ im Abschnitt zu „Verfügbare [!DNL ValueTrack]&quot; in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

* Sie können optional URL-Parameter und beliebige benutzerdefinierte Parameter einbeziehen, die für die Kampagne definiert wurden und durch kaufmännische Und-Zeichen (&amp;) getrennt sind, z. B. `{lpurl}?matchtype={matchtype}&device={device}`.

* Optional können Sie Umleitungen und Tracking von Drittanbietern hinzufügen.

>[!NOTE]
>
>* Wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, stellt Search, Social und Commerce beim Speichern des Datensatzes automatisch seinem eigenen Umleitungs- und Trackingcode das Präfix voran.
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Keyword-Einstellungen einen Wert enthalten, wird der Keyword-Wert angewendet.
>* ([!DNL Google Ads]) Wenn Sie eine Tracking-Vorlage auf Sitelink- oder Keyword-Ebene aktualisieren, werden die entsprechenden Anzeigen erneut zur Überprüfung eingereicht. Sie können Ihre Tracking-Vorlagen auf Konto-, Kampagnen- oder Anzeigengruppenebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
>* ([!DNL Microsoft Advertising]) Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
>* Vermeiden Sie [!DNL Google Ads] die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die paralleles Tracking ermöglichen. Wenn der Werbetreibende Makros verwenden muss, sollte das Adobe-Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um diese hinzuzufügen.

>[!MORELIKETHIS]
>
>* [Über Sitelink-Erweiterungen](sitelink-extension-about.md)
>* [Verknüpfen freigegebener Sitelinks mit Konten, Kampagnen und Anzeigengruppen](sitelink-extension-associate.md)
