---
title: Overzicht van taken om tegoeden te beheren | Microsoft Docs
description: Beschrijft taken om tegoeden te beheren en betalingen te vereffenen met klanten- of leveranciersposten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 21568c29177dd3f297caa1884352fc9c4f4e46e7
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="managing-receivables"></a>Tegoeden beheren
Een veel voorkomende stap in het financiële ritme is het reconciliëren van bankrekeningen. Hierbij moet u betalingen vereffenen met klant- of leveranciersposten, om verkoopfacturen en inkoopcreditnota's te sluiten.  

Een van de snelste manieren om in [!INCLUDE[d365fin](includes/d365fin_md.md)] betalingen vast te leggen in het venster **Dagboek betalingsreconciliatie** is door een bankafschriftbestand of -feed te importeren. Betalingen worden vereffend met openstaande leveranciers- of klantenposten, op basis van overeenkomsten in de gegevens tussen de betalingtekst en de informatie in de posten. U kunt de resultaten controleren en wijzigen voordat u het dagboek boekt en bankrekeningposten voor posten sluiten wanneer u het dagboek boekt. De bankrekening wordt gereconcilieerd wanneer alle betalingen zijn vereffend.

Er zijn echter andere plekken in de toepassingen om betalingen te vereffenen en bankrekeningen te reconciliëren:  

* Het venster **Bankreconciliaties**, waarin u ook posten kunt controleren. Zie [Bankrekeningen apart reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie.  
* Het venster **Betalingsregistratie**, waar u betalingen kunt vereffenen en handmatig controleren, die zijn ontvangen als contant, cheque of banktransactie, aan de hand van een gegenereerde lijst met niet-betaalde verkoopdocumenten. Deze functionaliteit is alleen beschikbaar voor verkoopdocumenten.  
* Het venster **Ontvangstendagboek**, waar u handmatig ontvangsten kunt boeken op de betreffende grootboek- of klantrekening of een andere rekening, door een betalingsregel in te voeren. U kunt de ontvangst of terugbetaling vereffenen met een of meer openstaande posten, voordat u het ontvangstendagboek boekt of via de klantposten.  

Een andere taak bij het beheer van tegoeden is het innen van openstaande saldi, inclusief rentefacturen, en het versturen van aanmaningen. [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt ook manieren om deze taken uit te voeren. Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).  

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

| Als u dit wilt doen | Zie |
| --- | --- |
| Vereffen betalingen om klant- of leveranciersposten te openen op basis van een geïmporteerd bankafschriftbestand of een bankfeed en de bankrekening te reconciliëren wanneer alle betalingen zijn vereffend. |[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Vereffen betalingen met openstaande klantposten op basis van handmatige invoer in een lijst met onbetaalde verkoopdocumenten. |[Klantbetalingen van een lijst met onbetaalde verkoopdocumenten handmatig reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Boek ontvangsten of terugbetalingen voor klanten in het ontvangstendagboek en vereffen deze met klantposten via het dagboek of via geboekte posten. |[Klantbetalingen handmatig reconciliëren](receivables-how-apply-sales-transactions-manually.md) |
| Klanten te herinneren aan achterstallige bedragen, rente en rentefacturen te berekenen en rekeningen met vorderingen te beheren. |[Openstaande saldi innen](receivables-collect-outstanding-balances.md) |
|Zorg dat u de kosten van verzonden artikelen kent door toegevoegde artikelkosten op te tellen, zoals vracht, fysieke verwerking, verzekering en transport, die u maakt nadat u hebt verkocht.|[Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden](payables-how-assign-item-charges.md)|
|Stel een tolerantie in waarmee het systeem een factuur sluit hoewel de betaling, inclusief een eventuele korting, het bedrag op de factuur niet volledig dekt.|[Werken met betalingstolerantie en contantkortingstolerantie](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

