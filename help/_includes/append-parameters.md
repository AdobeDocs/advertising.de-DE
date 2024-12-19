---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Feld „Parameter anhängen“ in den Konto- und Kampagneneinstellungen

**[!UICONTROL Append Parameters]:** (Optional) Alle zusätzlichen Tracking-Parameter, die an die Basis-URLs angehängt werden sollen.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Die Append-Parameter auf Advertiser-Ebene sind standardmäßig auf Konto- und Kampagnenebene enthalten, Sie können sie jedoch auch überschreiben.

Sie können eine beliebige statische Textzeichenfolge verwenden, einschließlich Tracking-Parametern von Drittanbietern oder beliebige [unterstützte Tracking-Parameter](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md) die einen entsprechenden Datenwert in die Basis-URL einfügen.

Trennen Sie mehrere Parameter durch Kommas oder kaufmännische Und-Zeichen (&amp;). Verschachtelte Klammern werden nicht unterstützt.

**Hinweise:**

* Änderungen an den Anhängen von Parametern werden nicht durch die Option [!UICONTROL Auto Upload] gesteuert. Wenn Sie die Anlagenparameter für vorhandene Basis-URLs ändern, werden neue URLs nicht automatisch generiert. Fügen Sie die neuen Parameter hinzu, indem Sie eine Bulksheet-Datei für das Konto oder die Kampagne herunterladen, die [!UICONTROL Base URL/Final URL]-Felder aktualisieren und dann die Bulksheet hochladen und veröffentlichen.

* (Werbenetzwerke mit parallelem Tracking) Verwenden Sie keine Makros, die keine Klicks aus Quellen ersetzen, die paralleles Tracking ermöglichen. Wenn der Werbetreibende Makros verwenden muss, sollte das Adobe-Account-Team den Support oder das Implementierungsteam kontaktieren, um diese hinzuzufügen.

* (Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration) Informationen zum Einschließen eines AMO-ID-Parameters zum Senden von Such-, Social- und Commerce-Daten an [!DNL Analytics] finden Sie in den [Anzeigennetzwerkspezifischen Formaten](/help/integrations/analytics/ids.md#amo-id-formats). Es ist nicht erforderlich, den Parameter für [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten mit einer serverseitigen AMO ID-Implementierung manuell hinzuzufügen.
