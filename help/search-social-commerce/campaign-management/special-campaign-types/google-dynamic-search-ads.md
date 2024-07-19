---
title: Implementieren von dynamischen Suchanzeigen [!DNL Google Ads]
description: Erfahren Sie mehr über den Workflow zum Einrichten von dynamischen Suchanzeigen. [!DNL Google Ads]
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Dynamische Suchanzeigen von [!DNL Google Ads] implementieren

*[!DNL Google Ads]Nur Suchkampagnen mit ausschließlich kreativem oder Keyword- und kreativem Tracking*

Dynamische Suchanzeigen verwenden Inhalte von Ihrer Website anstelle von Keywords, um zu entscheiden, wann Ihre Anzeigen angezeigt werden. Sie können die Seiten Ihrer Websites definieren, deren Inhalt für das Targeting Ihrer dynamischen Suchanzeigen verwendet wird, indem Sie entweder separate dynamische Suchziele für die Anzeigengruppe einrichten oder eine Einstellung auf Kampagnenebene auswählen, mit der Ihre Anzeigen mithilfe Ihrer Website-Inhalte gezielt ausgerichtet werden.

Sie können dynamische Suchanzeigen entweder einzeln oder mithilfe von Bulksheets einrichten. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

## Schritte zum Einrichten von dynamischen Suchanzeigen für [!DNL Google Ads]

1. [Erstellen Sie eine Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) für dynamische Suchanzeigen:

   1. Setzen Sie das Kampagnenbudget zunächst auf 10 % der Ausgaben Ihrer täglichen Suchkampagne.

      Sie können das Budget später erhöhen, nachdem die Anzeigen ihren Wert nachweisen.

   1. (Wenn Sie möchten, dass [!DNL Google Ads] Ihre dynamischen Suchanzeigen basierend auf dem Inhalt Ihrer Website anzeigt) Geben Sie die Stammdomäne und die Sprache für die Domäne im Abschnitt [!UICONTROL DSA Options] der Kampagneneinstellungen an.

      >[!NOTE]
      >
      >Ihre Domäne muss durch den organischen Suchindex [!DNL Google Ads] indexiert sein, damit ein Targeting erfolgt. Wenn die Domäne Seiten in mehreren Sprachen enthält und Sie alle Seiten als Ziel auswählen möchten, erstellen Sie für jede Sprache eine separate Kampagne.

      Wenn Sie Ihre Website-Domäne nicht zum Targeting Ihrer Anzeigen verwenden, erstellen Sie für jede Anzeigengruppe dynamische Suchziele (siehe Schritt 4). Sie können die Ziele [einzeln](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) oder mit [Bulk Sheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) erstellen.

   1. Stellen Sie sicher, dass die Kampagne auf den Suchkanal ausgerichtet ist und nur das Suchnetzwerk [!DNL Google Ads] (nicht das Display-Netzwerk). Diese Einstellungen sind auf der Registerkarte [!UICONTROL Networks and Devices] verfügbar.

   1. (Optional) Schließen Sie Suchbegriffe auf der Registerkarte [!UICONTROL Negatives] aus.

   1. (Optional) Konfigurieren Sie eine Tracking-Vorlage auf Kampagnenebene, die die Tracking-Vorlage auf Kontoebene außer Kraft setzt, aber auf niedrigeren Ebenen überschrieben werden kann.

      (Werbetreibende mit Adobe Analytics ohne serverseitiges Tracking) Wenn Sie das Tracking für den Rückwärtsfeed von Search, Social und Commerce zu Analytics einbeziehen möchten, fügen Sie den AMO-ID-Trackingcode den Anfügeparametern auf Kontoebene hinzu, die den Code zur endgültigen URL hinzufügen. Siehe &quot;[Von  [!DNL Analytics]](/help/integrations/analytics/ids.md) verwendete Adobe Advertising-IDs&quot;.

1. [Erstellen Sie eine Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) innerhalb der Kampagne, einschließlich der folgenden Schritte:

   1. Setzen Sie den [!UICONTROL Ad Group Type] auf **[!UICONTROL Search Dynamic].**

   1. Legen Sie das Standardangebot für alle Anzeigen fest.

      Sie können das Standardangebot für einzelne dynamische Suchziele überschreiben, wenn Sie sie konfigurieren.

   1. (Optional) Konfigurieren Sie eine Tracking-Vorlage auf Anzeigengruppenebene, die alle Tracking-Vorlagen auf höherer Ebene außer Kraft setzt, aber auf Anzeigenebene überschrieben werden kann.

      Wenn Sie das Adobe Analytics-Tracking auf Kampagnenebene hinzugefügt haben und es für die Anzeigengruppe einbeziehen möchten, fügen Sie es hier hinzu. Siehe Schritt 1e.

1. [Erstellen Sie jede dynamische Suchanzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) innerhalb der Anzeigengruppe.

   [!DNL Google Ads] generiert dynamisch die Überschrift, die Anzeigen-URL und die Landingpage-URL für jede Anzeige. Sie können optional Umleitungen und Tracking zur Tracking-Vorlage auf Anzeigenebene hinzufügen, wodurch Tracking-Vorlagen auf höheren Ebenen außer Kraft gesetzt werden.
Wenn Sie das Adobe Analytics-Tracking auf höheren Ebenen mit Tracking auf Anzeigenebene überschreiben möchten, fügen Sie es hier hinzu. Siehe Schritte 1e und 2c.

1. (Erforderlich, wenn Sie die Stammdomäne und die Sprache für die Domäne nicht im Abschnitt DSA-Optionen der Kampagneneinstellungen einbeziehen; andernfalls ist es optional) Erstellen Sie [dynamische Suchziele](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) für die Anzeigengruppe. Optional können Sie das Angebot auf Anzeigengruppenebene durch Angebote auf Zielebene überschreiben.

   Die Ziele definieren, ob das Werbenetzwerk alle oder eine Untergruppe der Seiten in Ihrer Website verwendet, um Ihre dynamischen Suchanzeigen auszurichten. Um die Leistung optimal zu verfolgen, konfigurieren Sie Ihre Kampagne mit einer Anzeigengruppe pro dynamisches Suchziel und fügen Sie eine Anzeigengruppe hinzu, die alle Kriterien erfüllt.

1. Bearbeiten Sie bei Bedarf die Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) , um das Kampagnenbudget anzupassen und den Traffic durch Ausschluss zusätzlicher Suchbegriffe aus der Kampagne zu verfeinern.[
