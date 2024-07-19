---
title: Erstellen mehrerer Drittanbieteranzeigen
description: Erfahren Sie, wie Sie mehrere Anzeigen von Drittanbietern auf einmal erstellen.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Erstellen mehrerer Drittanbieteranzeigen

Sie können bis zu 500 Anzeigen von Drittanbietern gleichzeitig erstellen, indem Sie Tags hochladen, die auf Kreativ-Assets verweisen, die auf Werbeservern von Drittanbietern gehostet werden. Sie können Tracking-Pixel für die Anzeigen einbeziehen.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Sie können entweder [!DNL DoubleClick] - und [!DNL Flashtalking] -Tag-Blätter oder eine manuell ausgefüllte Datei mit der bereitgestellten Vorlage hochladen.

>[!TIP]
>
> Die Best Practice ist die Verwendung von Drittanbieteranzeigen, die sicher über HTTPS bereitgestellt werden. URLs, die über HTTPS bereitgestellt werden, beginnen mit &quot;https&quot;.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne, in die die Anzeige eingefügt werden soll.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**. Klicken Sie im Abschnitt &quot;Anzeigentypen&quot;des Menüs auf **[!UICONTROL Bulk upload ads]**.

1. Wählen Sie den Anzeigen-Server aus, auf dem die Anzeige gehostet wird: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* oder *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] - und [!DNL Flashtalking] -Anzeigen) Wählen Sie den Tag-Typ aus, der für jedes Video-Asset und jedes Display-Asset verwendet werden soll. Die verfügbaren Optionen variieren je nach Anzeigenserver.

1. (Anzeigen auf allen Anzeigen-Servern außer [!DNL DoubleClick] und [!DNL Flashtalking]) Klicken Sie auf **[!UICONTROL Download this template]** , um eine Vorlage im XLSX-Format (Tabelle 3) herunterzuladen, die Sie mit Anzeigendaten füllen und lokal speichern können. [!DNL Microsoft Excel] Die erforderlichen Spalten umfassen [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag] und [!UICONTROL Ad Types].

1. Klicken Sie auf **[!UICONTROL Upload]** und wählen Sie eine Datei im .xlsx- oder .xls-Format von Ihrem Gerät oder Netzwerk aus.

   Laden Sie für Anzeigen von [!DNL DoubleClick] und [!DNL Flashtalking] nicht bearbeitete Tag-Arbeitsblätter vom Anzeigen-Server hoch. Verwenden Sie für andere Adserver die Vorlage, die Sie in Schritt 3 heruntergeladen haben.

1. Klicken Sie nach Abschluss des Uploads auf **[!UICONTROL Start Building Ads]**.

1. Überprüfen Sie die Details und den Status jeder Anzeige:

   1. (Universelle Videoanzeigen mit [!DNL Google] - oder [!DNL Flashtalking] -Tags) Klicken Sie auf das Feld **[!UICONTROL Ad Type]** und wählen Sie **[!UICONTROL Universal Video]** aus.

   1. (Universelle Videoanzeigen) Klicken Sie für jede neue Anzeige auf ![Bearbeiten](/help/dsp/assets/edit.png), wählen Sie das gewünschte Videoformat [3} aus und klicken Sie dann auf **Speichern**.](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

   1. Überprüfen Sie den Status jeder Anzeige, der auf Validierungsprüfungen für das hochgeladene Tag basiert.

   1. (Optional) Führen Sie für jede Anzeige einen der folgenden Schritte aus:

      * Um eine Anzeige in der Vorschau anzuzeigen, klicken Sie in der Anzeigenzeile auf ![play](/help/dsp/assets/play.png) .

      * Um die Anzeigendetails zu bearbeiten, klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png), bearbeiten Sie die Details und klicken Sie dann auf **Speichern**.

      * Um eine Anzeige zu entfernen, klicken Sie in der Anzeigenzeile auf **[!UICONTROL X]** .

1. Klicken Sie auf **[!UICONTROL Create *N *Anzeige(en)]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie auf **[!UICONTROL Done]**.

   * (Wenn eine Anzeige abgelehnt wird, optional) Um den Anzeigendatensatz zu bearbeiten und die Anzeige erneut zur Überprüfung einzureichen:

      1. Klicken Sie auf den Anzeigennamen.

      1. Bearbeiten Sie die Anzeigeneinstellungen.

      1. Klicken Sie auf **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Universelle Videoanzeigen können nur an universelle Videoplatzierungen angehängt werden.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Video: Anleitung zum Massen-Upload von Anzeigen-Tags von Drittanbietern](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [FAQs über universelle Videos](/help/dsp/campaign-management/faq-universal-video.md)
