---
title: Häufig gestellte Fragen
description: xxx
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%
---
# Häufig gestellte Fragen xxx

## Anrede

https://adobeadcloud.zendesk.com/agent/tickets/14214
Standardmäßig meldet Adobe Analytics alle erfassten Ereignisse in jedem Bericht. "[!UICONTROL Unspecified]"-Ereignisse stellen Formularabschlussereignisse dar, die nicht mit Adobe Advertising verbunden waren. Im Bericht der Anzeigenplattform würden beispielsweise organische Konversionen oder Konversionen, die von einer E-Mail-Kampagne gesteuert werden, in „Nicht angegeben“ fallen.

Sie können den Filter verwenden, um nicht angegebene Ereignisse aus Berichten zu entfernen, indem Sie das Häkchen der Option „Nicht angegebene Ereignisse einschließen (keine)“ entfernen. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## Anrede

https://adobeadcloud.zendesk.com/agent/tickets/24323
Positionieren Sie Analytics-Ereignis-Tags an denselben Stellen wie die Ad Cloud-Pixel, um sicherzustellen, dass XXX übereinstimmen.

## Anrede

https://adobeadcloud.zendesk.com/agent/tickets/24323

F.: Bei der internen Sicherheitsüberprüfung wurden bestimmte Funktionen als Sicherheitsbedenken gekennzeichnet, die wir bei der Integration von Ad Cloud in unsere bestehende Adobe Analytics-Installation aktiviert hatten.

Die fragliche Integration erfolgt zwischen AdCloud und Adobe Audience Manager. Diese Funktion erhöht die Übereinstimmungsrate für die Besucher-ID zwischen AdCloud und Adobe Audience Manager. Dazu sendet sie Netzwerkanfragen an pagead.l.doubleclick.net, star-mini.c10r.facebook.com und pug88000nf.pubmatic.com, um festzustellen, ob diese Services über eine vorhandene ID für den Besucher verfügen, die genutzt werden kann. Dies sind die Netzwerkanfragen, die als Sicherheitsrisiko gekennzeichnet wurden und für alle Site-Besucher auftreten.

Unser Prüfer bittet uns, diese Funktion zu deaktivieren. Was passiert, wenn wir diese Netzwerkanfragen blockieren?

A: Wir haben mit unserem Produkt geprüft und festgestellt, dass die betreffenden Pixel dazu dienen, die Cookie-Übereinstimmungsraten zwischen Ad Cloud, bestimmten Inventar-/SSP-Partnern (in Bezug auf DSP) und AAM zu erhöhen.  Wenn sie entfernt werden, sieht der Kunde möglicherweise eine verringerte Übereinstimmungsrate zwischen AAC/AAM und den Inventarpartnern, für die die entsprechenden Pixel vorgesehen sind, erwartet jedoch nicht, dass sie erheblich ist.

Für die Ad Cloud-Suche wird zwar angezeigt, dass die CX Enterprise-Organisations-ID des Werbetreibenden für MathWorks eingerichtet ist, unser Produktteam sieht jedoch kein MathWorks-Setup, um Zielgruppen in Ad Cloud zu aktivieren. Verwenden Sie Adobe Audience Manager zum Senden von Zielgruppen an die Ad Cloud-Suche? Andernfalls hat das Entfernen dieser Elemente keine Auswirkungen auf den aktuellen Workflow. Die AAM-Kundenunterstützung kann beim Entfernen dieser Pixel helfen, wenn Sie nicht möchten, dass sie ausgelöst werden.

