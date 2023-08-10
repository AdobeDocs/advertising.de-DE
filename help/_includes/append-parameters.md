---
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Feld Parameter anhängen in Konto- und Kampagneneinstellungen

**[!UICONTROL Append Parameters]:** (Optional) Alle zusätzlichen Tracking-Parameter, die an die Basis-URLs angehängt werden.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Die Anlagenparameter auf Advertiser-Ebene sind standardmäßig auf Konto- und Kampagnenebene enthalten, Sie können jedoch beide Parameter überschreiben.

Sie können eine beliebige statische Textzeichenfolge verwenden, einschließlich Tracking-Parametern von Drittanbietern, oder einen der [unterstützte Tracking-Parameter](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), die einen entsprechenden Datenwert in die Basis-URL einfügen.

Trennen Sie mehrere Parameter durch Kommas oder Und-Zeichen (&amp;). Verschachtelte Klammern werden nicht unterstützt.

**Hinweise:**

* Änderungen an Anhängen von Parametern werden nicht von der [!UICONTROL Auto Upload] -Option. Wenn Sie die Anlagenparameter für vorhandene Basis-URLs ändern, werden keine neuen URLs automatisch generiert. Fügen Sie die neuen Parameter hinzu, indem Sie eine Bulksheet-Datei für das Konto oder die Kampagne herunterladen und die [!UICONTROL Base URL/Final URL] und dann das Bulksheet hochladen und posten.

* (Werbenetzwerke mit paralleler Verfolgung) Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.

* (Advertiser mit Adobe Advertising-Adobe Analytics-Integration) Einschließen eines AMO-ID-Parameters zum Senden von Such-, Social- und Commerce-Daten an [!DNL Analytics], siehe [Anzeigen von netzwerkspezifischen Formaten](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md). Es ist nicht erforderlich, den Parameter für [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten mit einer serverseitigen AMO-ID-Implementierung.
