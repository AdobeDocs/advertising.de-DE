---
title: Implementieren  [!DNL Google Ads]  dynamischen Suchanzeigen
description: Erfahren Sie mehr über den Workflow zum Einrichten  [!DNL Google Ads]  dynamischen Suchanzeigen.
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Implementieren [!DNL Google Ads] dynamischen Suchanzeigen

*[!DNL Google Ads]Search-only-Kampagnen mit Tracking auf Kreativ- oder Keyword- und Kreativebene*

Dynamische Suchanzeigen verwenden Inhalte von Ihrer Website anstelle von Keywords, um zu entscheiden, wann Ihre Anzeigen angezeigt werden sollen. Sie können die Seiten in Ihren Websites definieren, deren Inhalt für das Targeting Ihrer dynamischen Suchanzeigen verwendet wird, indem Sie entweder separate dynamische Suchziele für die Anzeigengruppe einrichten oder eine Einstellung auf Kampagnenebene auswählen, um Ihre Anzeigen anhand Ihrer Website-Inhalte auszurichten.

Sie können dynamische Suchanzeigen entweder einzeln oder mithilfe von Bulksheets einrichten. Die folgenden Anweisungen enthalten Links zum Erstellen einzelner Entitäten.

## Schritte zum Einrichten [!DNL Google Ads] dynamischen Suchanzeigen

1. [Erstellen einer Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) für dynamische Suchanzeigen:

   1. Legen Sie zunächst das Kampagnenbudget auf 10 % Ihrer täglichen Ausgaben für Suchkampagnen fest.

      Sie können das Budget später erhöhen, nachdem die Anzeigen ihren Wert bewiesen haben.

   1. (Wenn [!DNL Google Ads] dynamische Suchanzeigen basierend auf dem Inhalt Ihrer Website anzeigen möchten) Geben Sie im Abschnitt [!UICONTROL DSA Options] der Kampagneneinstellungen die Stamm-Domain und die Sprache für die Domain an.

      >[!NOTE]
      >
      >Ihre Domain muss vom [!DNL Google Ads] organischen Suchindex indiziert sein, damit sie als Ziel ausgewählt werden kann. Wenn die Domain Seiten in mehreren Sprachen enthält und Sie alle ansprechen möchten, erstellen Sie für jede Sprache eine separate Kampagne.

      Wenn Sie Ihre Website-Domain nicht zum Targeting Ihrer Anzeigen verwenden, erstellen Sie für jede Anzeigengruppe dynamische Suchziele (siehe Schritt 4). Sie können die Ziele ([) &#x200B;](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) mithilfe von [Bulk Sheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) erstellen.

   1. Stellen Sie sicher, dass die Kampagne auf den Suchkanal und nur auf das [!DNL Google Ads] Suchnetzwerk (nicht auf das Anzeigennetzwerk) ausgerichtet ist. Diese Einstellungen sind auf der Registerkarte [!UICONTROL Networks and Devices] verfügbar.

   1. (Optional) Schließen Sie Schlüsselwörter auf der Registerkarte [!UICONTROL Negatives] aus.

   1. (Optional) Konfigurieren einer Tracking-Vorlage auf Kampagnenebene, durch die die Tracking-Vorlage auf Kontoebene überschrieben wird, die jedoch auf den niedrigeren Ebenen überschrieben werden kann.

      (Werbetreibende mit Adobe Analytics ohne Server-seitiges Tracking) Wenn Sie das Tracking für den Reverse Feed von Search, Social und Commerce zu Analytics einbeziehen möchten, fügen Sie den AMO ID-Tracking-Code zu den Append-Parametern auf Kontoebene hinzu, wodurch der Code zur endgültigen URL hinzugefügt wird. Siehe &quot;[Adobe Advertising-IDs verwendet von [!DNL Analytics]](/help/integrations/analytics/ids.md).“

1. [Erstellen einer Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) innerhalb der Kampagne, einschließlich der folgenden Schritte:

   1. Legen Sie die [!UICONTROL Ad Group Type] auf **[!UICONTROL Search Dynamic]fest.**

   1. Standardangebot für alle Anzeigen festlegen.

      Sie können das Standardangebot für einzelne dynamische Suchziele überschreiben, wenn Sie sie konfigurieren.

   1. (Optional) Konfigurieren Sie eine Tracking-Vorlage auf Anzeigengruppenebene, die alle Tracking-Vorlagen auf höheren Ebenen überschreibt, aber auf Anzeigenebene überschrieben werden kann.

      Wenn Sie Adobe Analytics-Tracking auf Kampagnenebene hinzugefügt haben und es in die Anzeigengruppe aufnehmen möchten, fügen Sie es hier hinzu. Siehe Schritt 1e.

1. [Erstellen Sie jede dynamische Suchanzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) innerhalb der Anzeigengruppe.

   [!DNL Google Ads] generiert für jede Anzeige dynamisch die Überschrift, die Anzeige-URL und die Landingpage-URL. Optional können Sie der Tracking-Vorlage auf Anzeigenebene Umleitungen und Tracking hinzufügen, wodurch Tracking-Vorlagen auf höheren Ebenen überschrieben werden.
Wenn Sie ein Adobe Analytics-Tracking auf höheren Ebenen mit einem Tracking auf Anzeigenebene überschreiben möchten, fügen Sie es hier hinzu. Siehe Schritte 1e und 2c.

1. (Erforderlich, wenn Sie die Stamm-Domain und die Sprache für die Domain nicht im Abschnitt DSA-Optionen der Kampagneneinstellungen angeben; andernfalls optional) Erstellen [dynamische Suchziele](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) für die Anzeigengruppe. Sie können das Gebot auf Anzeigengruppenebene optional mit Geboten auf Zielgruppenebene überschreiben.

   Die Ziele definieren, ob das Anzeigennetzwerk alle oder eine Teilmenge der Seiten auf Ihrer Website verwendet, um Ihre dynamischen Suchanzeigen gezielt anzusprechen. Um die Leistung optimal zu verfolgen, konfigurieren Sie Ihre Kampagne mit einer Anzeigengruppe pro dynamischem Suchziel und schließen Sie eine Anzeigengruppe ein, die alle Kriterien berücksichtigt.

1. Bearbeiten Sie bei [&#x200B; die Kampagneneinstellungen, &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) das Kampagnenbudget anzupassen und den Traffic zu verfeinern, indem Sie zusätzliche Keywords aus der Kampagne ausschließen.
