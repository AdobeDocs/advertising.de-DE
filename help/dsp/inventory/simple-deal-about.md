---
title: Über [!UICONTROL Simple Ad Serving]
description: Erfahren Sie mehr über [!UICONTROL Simple Ad Serving] Angebote mit Pixel für die Ereignisverfolgung.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: dad30b0bd24c0286c1de6520471cb90707046ff3
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Über [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] bietet eine garantierte, unentschiedene Bereitstellung von Anzeigen und Reporting für einen bestimmten Herausgeber und einen einzelnen Anzeigentyp mithilfe einer einzigen, dedizierten Platzierung. Verwenden Sie [!DNL Simple Ad Serving], wenn Ihr Publisher Ihr Angebot nicht über Angebots-IDs ausführen kann. Zielgruppenbestimmung, Budgetplanung und -begrenzung sowie Frequenzlimitierung werden vollständig vom Publisher gesteuert. Führen Sie diese Angebote über Pixel zum Ereignis-Tracking aus.

Bei [!UICONTROL Simple Ad Serving] wird jede Anzeige direkt vom Publisher (Site-Server) bereitgestellt, und DSP stellt ein Pixel zur Ereignisverfolgung bereit, das an den Publisher gesendet wird, der das Pixel implementieren und die DSP-Anzeigen verarbeiten muss. Je nach Inventartyp messen die Ereignispixel Impressions-, Clickthrough- und Videowiedergabeereignisse.

Die folgenden Anzeigentypen sind verfügbar:

* Desktop Standard Pre-Roll
* Pre-Roll für Tablets und Mobilgeräte
* Connected TV Standard Pre-Roll
* Anzeige
* Audio

Sie können in der Ansicht [!UICONTROL Simple Ad Serving] > [!UICONTROL Inventory] ein [!UICONTROL Deals] Angebot erstellen. DSP generiert automatisch eine Platzierung mit dem Untertyp &quot;[!DNL Simple ad serving]&quot; für die Anzeige. Die Platzierung zielt auf den Abschluss ab, erlaubt jedoch keine zusätzliche Zielgruppenbestimmung, kein Budget und keine Frequenzlimitierung. Sie können nur einige der Abschlusseinstellungen bearbeiten, z. B. den Abschlussnamen, CPM, Impressionen und Flugdaten.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] Platzierungen entsprechen nicht den verfügbaren Mitteln des Kontos oder den Kampagnen- und Paketbudgets. Die Ausgaben werden jedoch erfasst und auf diese Budgets angerechnet. Selbst wenn der CPM 0 $ beträgt, werden Ereignisdaten immer verfolgt.

>[!MORELIKETHIS]
>
>* [Erstellen eines [!UICONTROL Simple Ad Serving] Angebots](simple-deal-create.md)
>* [Bearbeiten [!UICONTROL Simple Ad Serving] Deal-Einstellungen](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] Einstellungen](simple-deal-settings.md)
>* [Detailbericht für einen Abschluss anzeigen](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
