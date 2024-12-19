---
title: Fehler-Codes für  [!DNL FreeWheel]  Anzeigenübermittlungen
description: Verweisen Sie auf die Fehler-Codes, die für Anzeigenübermittlungen an zurückgegeben werden [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 3%

---

# Fehler-Codes für [!DNL FreeWheel] Anzeigenübermittlungen

Die Fehlermeldungen für fehlgeschlagene Anzeigenübermittlungen können entweder von Advertising DSP oder von [!DNL FreeWheel] stammen. Fehlermeldungen werden in der Spalte [!UICONTROL API Response] im Dialogfeld [[!UICONTROL Freewheel Status] angezeigt](freewheel-check-status.md).

## Interne Advertising DSP-Fehler

| Fehlermeldung | Beschreibung | Nächste Schritte |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] hat noch nicht geantwortet, dass die Übermittlung erfolgreich war oder fehlgeschlagen ist. | Überprüfen Sie den Status in 10 Minuten erneut. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] akzeptiert keine Werbeanzeigen in Großbritannien ohne zugewiesene Uhrnummern. | Weisen Sie der Anzeige eine Uhrnummer zu und senden Sie die Anzeige dann erneut. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | Der Transcoder hatte die Transkodierung der Anzeige nicht abgeschlossen, als Sie versuchten, die Anzeige zu senden. | Warten Sie zehn Minuten und senden Sie dann die Anzeige erneut. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | Der eingereichte Deal ist nicht als programmgesteuert garantierter Deal eingerichtet. [!DNL FreeWheel] akzeptiert nur garantierte Angebote. | Richten Sie die Angebots-ID als programmgesteuert garantierten Abschluss ein. Die Anzeige wird automatisch an [!DNL FreeWheel] gesendet, wenn Sie die programmgesteuerte garantierte Standardplatzierung am Ende des Workflows „Angebots-ID“ speichern. |
| [!DNL Invalid external_deal_id:] \&lt;DEAL_ID\> | Die übermittelte Angebots-ID ist entweder nicht vorhanden oder am Adobe-Ende nicht aktiv. | Vergewissern Sie sich, dass der Deal aktiv ist, und senden Sie die Anzeige dann erneut. |
| [!DNL \[public_id=]\&lt;deal\>] existiert nicht | Die übermittelte Angebots-ID ist am [!DNL FreeWheel] Ende nicht vorhanden. | Wenden Sie sich an Ihren [!DNL FreeWheel], um die Angebots-ID zu bestätigen. |
| [!DNL Ad with identifier] \&lt;*Anzeigename*\> [!DNL was not found.] | Der gesendete Anzeigenschlüssel ist entweder nicht vorhanden oder am Adobe-Ende nicht aktiv. | Finden Sie den richtigen Anzeigenschlüssel und senden Sie die Anzeige dann erneut. |
| [!DNL Pending Submission] | Die Übermittlung ist noch ausstehend. | Aktualisieren Sie die Seite. |

{style="table-layout:auto"}

## [!DNL Freewheel] API-Fehler

| Code | Bedeutung | Beschreibung | Nächste Schritte |
|--- |--- |--- |--- |
| 401 | Nicht autorisiert | Falsche, fehlende oder ungültige Zugriffsberechtigungen. | Wenden Sie sich an Ihr Adobe-Account-Team. |
| 403 | Verboten | Der Server hat die Anfrage verstanden, weigert sich jedoch, sie zu autorisieren. | Wenden Sie sich an Ihr Adobe-Account-Team. |
| 404 | Nicht gefunden | Die angeforderte Ressource ist nicht verfügbar. Wenn die Creative ID im PUT-Vorgang nicht gefunden wird, wird eine 404 zurückgegeben. | Wenden Sie sich an Ihr Adobe-Account-Team. |
| 405 | Methode nicht zulässig | Eine Anfrage einer Ressource wurde mit einer Anfragemethode durchgeführt, die von dieser Ressource nicht unterstützt wird (z. B. mit GET bei einer Methode, für die Daten per POST gesendet werden müssen, oder mit PUT bei einer schreibgeschützten Ressource). | Wenden Sie sich an Ihr Adobe-Account-Team. |
| 408 | Zeitüberschreitung der Anfrage | Zeitüberschreitung während der Verarbeitung dieser Anfrage. Zeitüberschreitungen werden in der Regel durch gleichzeitige Anfragen nach exklusivem Zugriff auf bestimmte Ressourcen verursacht. | Senden Sie die Anfrage erneut, wenn Sie diesen Status erhalten. Wenn das Problem weiterhin besteht, wenden Sie sich an Ihr Adobe-Account-Team. |
| 422 | Nicht verarbeitbare Entität | Ungültige Ressource. Dieser Fehler tritt auf, wenn der Anfragetext ungültig ist oder die erstellte/aktualisierte Ressource ungültig ist (beispielsweise, wenn die Angebots-ID nicht gefunden wurde). Siehe [Fehler der FreeWheel-API 422](#freewheel-422-errors) für weitere Informationen. | Wenden Sie sich an Ihr Adobe-Account-Team. |
| 500 | Interner Server-Fehler | API-Systemfehler. | Wenden Sie sich an Ihr Adobe-Account-Team. |

{style="table-layout:auto"}

## [!DNL Freewheel] API 422-Fehler {#freewheel-422-errors}

| Code | HTTP-Code | Beschreibung |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | Die Anfragedaten haben ein ungültiges JSON-Format. Überprüfen Sie die Fehlermeldung auf Details. |
| DATA_VALIDATION_FAILURE | 422 | In den Anfragedaten fehlen erforderliche Felder oder der Datentyp ist ungültig. Überprüfen Sie die Fehlermeldung auf Details. |
| DATA_DEAL_INVALID | 422 | Der Abschluss wurde falsch konfiguriert oder ist nicht vorhanden. Überprüfen Sie die Fehlermeldung auf Details. |
| DATA_DEAL_GET_FAILURE | 422 | Der Deal wurde nicht gefunden oder seine Konfiguration hat ein Problem. Überprüfen Sie die Fehlermeldung auf Details. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | Die Kreativ-URL ist ungültig. Überprüfen Sie die Fehlermeldung auf Details. |
| DATA_CREATIVE_LINK_FAILURE | 422 | Das Kreativteam war nicht mit den Knoten der Werbeeinheit des Deals verknüpft. Überprüfen Sie die Fehlermeldung auf Details. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | Der Kreative wurde nicht aktualisiert. Überprüfen Sie die Fehlermeldung auf Details. |
| DATA_DSP_GET_FAILURE | 422 | Die DSP ist nicht im System vorhanden. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | Die Verknüpfung des Kreativen mit den Werbeeinheiten wurde nicht aufgehoben. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | Der Kreative wurde nicht gelöscht. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | Die URL wurde nicht erkannt. |
| DATA_ENTITY_NOT_FOUND | 422 | Der Kreative existiert nicht. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Überblick über die Einrichtung von garantierten programmgesteuerten Angeboten in [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Akzeptieren eines Angebots im Angebots-ID-Posteingang](deal-id-inbox-accept.md)
>* [Senden einer Anzeige für einen programmgesteuerten garantierten Abschluss an [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Überprüfen Sie den Status der Anzeigen  [!DNL FreeWheel]  programmgesteuerte garantierte -Angebote](/help/dsp/inventory/freewheel-check-status.md)
