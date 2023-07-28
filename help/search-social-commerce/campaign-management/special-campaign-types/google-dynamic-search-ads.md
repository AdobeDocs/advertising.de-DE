---
title: Implementierung [!DNL Google Ads] dynamische Suchanzeigen
description: Erfahren Sie mehr über den Workflow zur Einrichtung [!DNL Google Ads] dynamische Suchanzeigen.
exl-id: 4c806824-b582-46dc-8d88-85c73bfb0944
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Implementierung [!DNL Google Ads] dynamische Suchanzeigen

*[!DNL Google Ads]Suchkampagnen nur mit kreativem oder Keyword- und kreativem Tracking*

Dynamische Suchanzeigen verwenden Inhalte von Ihrer Website anstelle von Keywords, um zu entscheiden, wann Ihre Anzeigen angezeigt werden. Sie können die Seiten Ihrer Websites definieren, deren Inhalt für das Targeting Ihrer dynamischen Suchanzeigen verwendet wird, indem Sie entweder separate dynamische Suchziele für die Anzeigengruppe einrichten oder eine Einstellung auf Kampagnenebene auswählen, mit der Ihre Anzeigen mithilfe Ihrer Website-Inhalte gezielt ausgerichtet werden.

Sie können dynamische Suchanzeigen entweder einzeln oder mithilfe von Bulksheets einrichten. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

## Schritte zum Einrichten [!DNL Google Ads] dynamische Suchanzeigen

1. [Kampagne erstellen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) für dynamische Suchanzeigen:

   1. Setzen Sie das Kampagnenbudget zunächst auf 10 % der Ausgaben Ihrer täglichen Suchkampagne.

      Sie können das Budget später erhöhen, nachdem die Anzeigen ihren Wert nachweisen.

   1. (Wenn Sie [!DNL Google Ads] , um Ihre dynamischen Suchanzeigen basierend auf dem Inhalt Ihrer Website anzuzeigen) Geben Sie die Stammdomäne und die Sprache für die Domäne in der [!UICONTROL DSA Options] in den Kampagneneinstellungen.

      >[!NOTE]
      >
      >Ihre Domäne muss durch die [!DNL Google Ads] organischer Suchindex, der angesprochen werden soll. Wenn die Domäne Seiten in mehreren Sprachen enthält und Sie alle Seiten als Ziel auswählen möchten, erstellen Sie für jede Sprache eine separate Kampagne.

      Wenn Sie Ihre Website-Domäne nicht zum Targeting Ihrer Anzeigen verwenden, erstellen Sie für jede Anzeigengruppe dynamische Suchziele (siehe Schritt 4). Sie können Ziele erstellen [einzeln](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) oder [Massenblätter](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Stellen Sie sicher, dass die Kampagne auf den Suchkanal und nur auf die [!DNL Google Ads] Suchnetzwerk (nicht das Display-Netzwerk). Diese Einstellungen sind im Abschnitt [!UICONTROL Networks and Devices] Registerkarte.

   1. (Optional) Schließen Sie Suchbegriffe aus der [!UICONTROL Negatives] Registerkarte.

   1. (Optional) Konfigurieren Sie eine Tracking-Vorlage auf Kampagnenebene, die die Tracking-Vorlage auf Kontoebene außer Kraft setzt, aber auf niedrigeren Ebenen überschrieben werden kann.

      (Werbetreibende mit Adobe Analytics ohne serverseitiges Tracking) Wenn Sie das Tracking für den Rückwärtsfeed von Search, Social und Commerce zu Analytics einbeziehen möchten, fügen Sie den Trackingcode s_kwcid zu den Anfügeparametern auf Kontoebene hinzu, die den Code zur endgültigen URL hinzufügen. Siehe &quot;[Der Tracking-Parameter s_kwcid](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md).&quot;

1. [Erstellen einer Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) innerhalb der Kampagne, einschließlich der folgenden Schritte:

   1. Legen Sie die [!UICONTROL Ad Group Type] nach **[!UICONTROL Search Dynamic].**

   1. Legen Sie das Standardangebot für alle Anzeigen fest.

      Sie können das Standardangebot für einzelne dynamische Suchziele überschreiben, wenn Sie sie konfigurieren.

   1. (Optional) Konfigurieren Sie eine Tracking-Vorlage auf Anzeigengruppenebene, die alle Tracking-Vorlagen auf höherer Ebene außer Kraft setzt, aber auf Anzeigenebene überschrieben werden kann.

      Wenn Sie das Adobe Analytics-Tracking auf Kampagnenebene hinzugefügt haben und es für die Anzeigengruppe einbeziehen möchten, fügen Sie es hier hinzu. Siehe Schritt 1e.

1. [Erstellen Sie jede dynamische Suchanzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) innerhalb der Anzeigengruppe.

   [!DNL Google Ads] generiert für jede Anzeige dynamisch die Überschrift, die Anzeigen-URL und die Landingpage-URL. Sie können optional Umleitungen und Tracking zur Tracking-Vorlage auf Anzeigenebene hinzufügen, wodurch Tracking-Vorlagen auf höheren Ebenen außer Kraft gesetzt werden.
Wenn Sie das Adobe Analytics-Tracking auf höheren Ebenen mit Tracking auf Anzeigenebene überschreiben möchten, fügen Sie es hier hinzu. Siehe Schritte 1e und 2c.

1. (Erforderlich, wenn Sie die Stammdomäne und die Sprache für die Domäne nicht im Abschnitt DSA-Optionen der Kampagneneinstellungen einbeziehen; andernfalls optional) Erstellen Sie [dynamische Suchziele](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) für die Anzeigengruppe. Optional können Sie das Angebot auf Anzeigengruppenebene durch Angebote auf Zielebene überschreiben.

   Die Ziele definieren, ob das Werbenetzwerk alle oder eine Untergruppe der Seiten in Ihrer Website verwendet, um Ihre dynamischen Suchanzeigen auszurichten. Um die Leistung optimal zu verfolgen, konfigurieren Sie Ihre Kampagne mit einer Anzeigengruppe pro dynamisches Suchziel und fügen Sie eine Anzeigengruppe hinzu, die alle Kriterien erfüllt.

1. Gegebenenfalls [Bearbeiten der Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) , um das Kampagnenbudget anzupassen und den Traffic zu verfeinern, indem zusätzliche Suchbegriffe aus der Kampagne ausgeschlossen werden.
