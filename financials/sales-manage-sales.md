---
title: Overzicht van taken om verkoop te beheren | Microsoft Docs
description: Hierin wordt beschreven hoe u verkoopactiviteiten kunt beheren.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 95f235e743ed97b1ac90a6e0583b9bd19dcb7ead
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="sales"></a>Verkoop
U maakt een verkoopfactuur of een verkooporder om uw overeenkomst met een klant vast te leggen om bepaalde producten tegen bepaalde leverings- en betalingsvoorwaarden te verkopen.

U moet verkooporders gebruiken als uw verkoopproces vereist dat u delen van een orderaantal kunt verzenden, bijvoorbeeld omdat de volledige hoeveelheid niet in één keer beschikbaar is. Als u artikelen verkoopt door rechtstreeks van uw leverancier bij de klant te leveren, als een doorverzending, moet u ook verkooporders gebruiken. Wat betreft alle andere aspecten werken verkooporders op dezelfde manier als verkoopfacturen. Bij verkooporders kunt u door middel van de functionaliteit Ordertoezegging ook vastgestelde leverdatums aan klanten mededelen.  

U kunt met de klant onderhandelen door eerst een verkoopofferte te maken, die u kunt omzetten in een verkoopfactuur of verkooporder wanneer er een overeenkomst is. Nadat de klant de overeenkomst heeft bevestigd, kunt u een orderbevestiging verzenden om uw verplichting vast te leggen dat de producten worden geleverd zoals is overeengekomen.

U kunt een geboekte verkoopfactuur gemakkelijk corrigeren of annuleren voordat het is betaald. Dit is handig als u een typfout wilt corrigeren of als de klant om een wijziging in het begin van het orderproces verzoekt. Als de geboekte verkoopfactuur is betaald, moet u een verkoopcreditnota of een verkoopretourorder maken om de verkoop tegen te boeken.

Goede verkoop- en marketingmethoden zijn gebaseerd op de juiste beslissingen op het juiste tijdstip. Marketingfunctionaliteit in [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt nauwkeurige en tijdige overzichten van uw contactgegevens, zodat u uw potentiële klanten efficiënter kunt bedienen en de klanttevredenheid kunt verhogen. Zie [CRM - Marketing en Sales](marketing-relationship-management.md) voor meer informatie.

In bedrijfsomgevingen waar de klant moet betalen voordat producten worden geleverd, zoals in de detailhandel, moet u wachten op de betalingsontvangst voordat u de producten levert. In de meeste gevallen verwerkt u inkomende betalingen enkele weken na levering door de betalingen te vereffenen met de gerelateerde geboekte, niet-betaalde verkoopfacturen. Zie voor meer informatie [Procedure: Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

Verkoopdocumenten kunnen worden verzonden als PDF-bestanden die aan e-mail zijn gekoppeld. De hoofdtekst van de e-mail bevat een uittreksel van het verkoopdocument, zoals producten, totaalbedrag en een koppeling naar de PayPal-site. Zie [Procedure: Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie.

Voor alle verkoopprocessen kunt u een goedkeuringswerkstroom opnemen, bijvoorbeeld om te vereisen dat grote verkopen worden goedgekeurd door de administrateur. Zie voor meer informatie [Werkstromen gebruiken](across-use-workflows.md).

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

| Als u dit wilt doen | Zie |
| --- | --- |
| Maak een verkoopofferte waarbij u producten aanbiedt tegen overeen te komen condities voordat de offerte wordt omgezet in een verkoopfactuur. |[Procedure: Voorstellen maken](sales-how-make-offers.md) |
| Maak een verkoopfactuur om uw overeenstemming met een klant vast te leggen om producten tegen bepaalde leverings- en betalingscondities te verkopen. |[Procedure: Verkopen factureren](sales-how-invoice-sales.md) |
| Verwerk een verkooporder die betrekking heeft op gedeeltelijke verzending of doorverzending. |[Procedure: Producten verkopen](sales-how-sell-products.md) |
|Standaardverkoop- of inkoopregels instellen die u snel kunt invoegen in documenten, bijvoorbeeld voor terugkerende aanvullingsorders.|[Procedure: Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md)|  
| Koppel een verkooporder aan een inkooporder om een doorverzendartikel te verkopen dat direct vanaf de leverancier bij de klant wordt geleverd. |[Procedure: Doorverzendingen maken](sales-how-drop-shipment.md) |
|Laat een niet-voorraadartikel verzenden van een leverancier naar uw magazijn, zodat u het artikel naar uw klant kunt verzenden.|[Procedure: Speciale orders maken](sales-how-to-create-special-orders.md)|
| Voer een actie op een onbetaalde geboekte verkoopfactuur uit om automatisch een creditnota te maken en de verkoopfactuur te annuleren of opnieuw te maken zodat u correcties kunt aanbrengen. |[Procedure: Niet-betaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md) |
| Maak een verkoopcreditnota om een bepaalde geboekte verkoopfactuur terug te boeken om te weerspiegelen welke producten de klant terugstuurt en welk betalingsbedrag u zult terugbetalen. |[Procedure: Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) |
|Beheer de toezegging van de klant om grote aantallen in te kopen, die in de loop van de tijd in meerdere verzendingen worden geleverd.|[Procedure: Werken met verkoopraamcontracten](sales-how-to-create-blanket-sales-orders.md)|
|Verkoop componenten die nu niet verkrijgbaar zijn door een gekoppelde assemblageorder te maken om het volledige of gedeeltelijke verkooporderaantal te leveren.|[Procedure: Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md)|
|Factureer een klant één keer voor meerdere zendingen, door de zendingen te combineren op een factuur.|[Procedure: verzendingen combineren op één factuur](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Informeer klanten over orderleverdatums door berekening van ofwel de datum waarop het artikel beschikbaar is voor toezegging (ATP) of de datum waarop het artikel kan worden toegezegd (CTP).|[Procedure: Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)|

## <a name="see-also"></a>Zie ook
[Verkopen instellen](sales-setup-sales.md)  
[Procedure: Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Projectbeheer](projects-manage-projects.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

