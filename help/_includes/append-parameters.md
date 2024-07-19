---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Feld Parameter anhängen in Konto- und Kampagneneinstellungen

**[!UICONTROL Append Parameters]:** (Optional) Alle zusätzlichen Tracking-Parameter, die an die Basis-URLs angehängt werden sollen.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Die Anlagenparameter auf Advertiser-Ebene sind standardmäßig auf Konto- und Kampagnenebene enthalten, Sie können jedoch beide Parameter überschreiben.

Sie können eine beliebige statische Textzeichenfolge, einschließlich Tracking-Parametern von Drittanbietern, oder einen der [unterstützten Tracking-Parameter](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md) verwenden, die einen entsprechenden Datenwert in die Basis-URL einfügen.

Trennen Sie mehrere Parameter durch Kommas oder Und-Zeichen (&amp;). Verschachtelte Klammern werden nicht unterstützt.

**Notizen:**

* Änderungen an Anhängen von Parametern werden nicht durch die [!UICONTROL Auto Upload] -Option gesteuert. Wenn Sie die Anlagenparameter für vorhandene Basis-URLs ändern, werden keine neuen URLs automatisch generiert. Fügen Sie die neuen Parameter hinzu, indem Sie eine Bulksheet-Datei für das Konto oder die Kampagne herunterladen, die Felder [!UICONTROL Base URL/Final URL] aktualisieren und dann das Bulksheet hochladen und posten.

* (Werbenetzwerke mit paralleler Verfolgung) Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.

* (Werbetreibende mit Adobe Advertising-Adobe Analytics-Integration) Um einen AMO-ID-Parameter einzuschließen, mit dem Such-, Social- und Commerce-Daten an [!DNL Analytics] gesendet werden können, lesen Sie die Informationen unter [Anzeigennetzwerkspezifische Formate](/help/integrations/analytics/ids.md#amo-id-formats). Es ist nicht erforderlich, den Parameter für [!DNL Google Ads] - und [!DNL Microsoft Advertising] -Konten mit einer serverseitigen AMO-ID-Implementierung manuell hinzuzufügen.
