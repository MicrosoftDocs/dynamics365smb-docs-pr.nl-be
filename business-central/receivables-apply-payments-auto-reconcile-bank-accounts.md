---
title: Bankrekeningen reconciliëren en betalingen vereffenen
description: 'Schetst taken om uw bank-, tegoeden- en schuldenrekeningen te reconciliëren, kasontvangsten of onkosten te boeken en betalingen automatisch te vereffenen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Betalingen automatisch vereffenen en bankrekeningen reconciliëren
U moet regelmatig uw bankrekening en de rekeningen met tegoeden en betalingsverplichtingen reconciliëren, door betalingen die op de bank zijn vastgelegd te vereffenen met de gerelateerde openstaande (onbetaalde) facturen en creditnota's of andere openstaande posten in [!INCLUDE[prod_short](includes/prod_short.md)].  

U kunt deze taak op de pagina **Dagboek betalingsreconciliatie** uitvoeren door bijvoorbeeld een bankafschriftbestand of -feed te importeren om de betalingen snel in project te registreren. Betalingen worden vereffend met openstaande leveranciers- of klantenposten, op basis van overeenkomsten tussen de betalingtekst en de informatie in de posten. U kunt automatische vereffeningen controleren en wijzigen voordat u het dagboek boekt. U kunt ervoor kiezen om openstaande bankrekeningposten met betrekking tot de vereffende posten te sluiten wanneer u het dagboek boekt. De bankrekening wordt automatisch gereconcilieerd wanneer alle betalingen worden vereffend.

De logica die bepaalt hoe betalingstekst automatisch wordt afgestemd op invoerinformatie, is ingesteld op de pagina **Regels betalingsvereffening** als een aantal geprioriteerde regels die u kunt bewerken.

U kunt ook bankrekeningen reconciliëren zonder tegelijkertijd betalingen te vereffenen. U doet dit werk op de pagina **Bankreconciliatie**. Zie [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie.   

Als u bankafschriften als een bankfeed wilt importeren, moet u eerst de service Envestnet Yodlee Bank Feeds instellen en inschakelen en vervolgens uw bankrekeningen aan de gerelateerde online bankrekeningen koppelen. Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> U kunt ook bankafschriftbestanden importeren in een door komma's of puntkomma's gescheiden indeling (.CSV). Gebruik de begeleide instelling **Een importindeling voor het bankafschriftbestand instellen** om de importindelingen voor bankafschriften te definiëren en de indeling aan een bankrekening te koppelen. U kunt deze indelingen vervolgens gebruiken wanneer u bankafschriften importeert op de pagina **Bankreconciliatie**.

U kunt ook de extensie AMC Banking 365 Fundamentals gebruiken om een bankafschriftenbestand te converteren van elke denkbare indeling naar een gegevensstroom die u kunt importeren in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [De extensie AMC Banking 365 Fundamentals gebruiken](ui-extensions-amc-banking.md).  

De volgende tabel beschrijft een reeks taken, met koppelingen naar de onderwerpen waarin deze worden beschreven.  

| Als u dit wilt doen | Zie |
| --- | --- |
| Vereffen betalingen om klant- of leveranciersposten te openen door een bankafschrift te importeren en de bankrekening te reconciliëren wanneer alle betalingen zijn vereffend. |[Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md) |
| Vereffen handmatig betalingen door gedetailleerde informatie over afgestemde gegevens weer te geven en suggesties voor openstaande kandidaatposten om betalingen mee te vereffenen. |[Betalingen na automatische vereffening controleren of vereffenen](receivables-how-review-apply-payments-auto-application.md) |
| Betalingen oplossen die niet automatisch met de gerelateerde openstaande posten kunnen worden vereffend. Bijvoorbeeld omdat bedragen afwijken, of omdat geen gerelateerde post bestaat. |[Betalingen reconciliëren die niet automatisch kunnen worden vereffend](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Koppel tekst op betalingen aan specifieke klant-, leverancier- of grootboekrekeningen om periodieke ontvangsten of kosten altijd naar deze rekeningen te boeken als er geen documenten zijn voor vereffening. |[Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliatie](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Stel de regels in die bepalen hoe betalingen/banktransacties automatisch moeten worden vereffend met de gerelateerde openstaande dagboekposten wanneer u de functie **Automatisch vereffenen** gebruikt in het venster **Betalingsreconciliatiedagboek**.|[Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md)|

## Zie gerelateerde [Microsoft-training](/training/modules/use-journals-dynamics-365-business-central/index)

## Zie ook
[Bankrekeningen afstemmen](bank-how-reconcile-bank-accounts-separately.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
