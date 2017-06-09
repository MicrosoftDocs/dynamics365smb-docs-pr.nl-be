---
title: Voorraad | Microsoft Docs
description: Beschrijft hoe u fysieke artikelen beheert.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>Voorraad
Voor elk fysiek product dat u verhandelt, moet u een artikelkaart van het soort **Voorraad** maken. Artikelen die u aan klanten aanbiedt maar in voorraad houdt, kunt u als niet-voorraadartikelen registreren, die u indien nodig naar voorraadartikelen kunt converteren. U kunt de hoeveelheid van een artikel in voorraad verhogen of verlagen door rechtstreeks naar de artikelposten te boeken, bijvoorbeeld na een fysieke telling of als u geen inkopen registreert.

Positieve en negatieve voorraadmutaties worden natuurklijk ook geregistreerd wanneer u respectievelijk inkoop- en verkoopdocumenten boekt. Zie voor meer informatie [Procedure: Inkopen registreren](purchasing-how-record-purchases.md), [Procedure: Producten verkopen](sales-how-sell-products.md) en [Procedure: Verkopen factureren](sales-how-invoice-sales.md). De transfers tussen vestigingen wijzigen de voorraadaantallen in alle magazijnen van het bedrijf.   

Om het overzicht van artikelen te verhogen en deze te zoeken, kunt u artikelen categoriseren en er kenmerken aan toewijzen op basis waarvan u ze kunt zoeken en sorteren.

U moet ervoor zorgen dat de kosten van uw artikelen worden doorgestuurd naar de gerelateerde uitgaande verkooptransactie, vooral in situaties waarin u goederen verkoopt voordat u de inkoop van deze artikelen factureert. Dit wordt kostenherwaardering genoemd en u kunt dat handmatig doen of instellen dat het automatisch gebeurt wanneer u een artikeltransactie boekt.

Wijzigingen in voorraadwaarde van handel worden automatisch met uw financiële boeken afgestemd wanneer u artikeltransacties boekt.

|Als u dit wilt doen |Zie |
|---|----|
|Maak artikelkaarten voor voorraadartikelen waarin u handelt.|[Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md)|
|Bovenliggende artikelen structureren die u als pakketten verkoopt bestaande uit de onderdelen van de bovenliggende artikelen, of die u op bestelling of voor voorraad monteert.|[Procedure: Met stuklijsten werken](inventory-how-work-BOMs.md)|
|Onderhoud een overzicht van artikelen en help artikelen te zoeken en te sorteren door ze in categorieën te organiseren.|[Procedure: Artikelen categoriseren](inventory-how-categorize-items.md)|
|Wijs artikelkenmerken van verschillende waardesoorten aan uw artikelen toe zodat u artikelen gemakkelijker kunt sorteren en vinden.|[Procedure: Werken met artikelkenmerken](inventory-how-work-item-attributes.md)|
|Maak speciale artikelkaarten voor artikelen die u aan klanten aanbiedt, maar die u niet in voorraad houdt.|[Procedure: Werken met niet-voorraadartikelen](inventory-how-work-nonstock-items.md)|
|Verlaag of verhoog het voorraadaantal van een artikel, bijvoorbeeld na een inventarisering of als eenvoudige manier om inkoopontvangsten vast te leggen.|[Procedure: Voorraad wijzigen](inventory-how-adjust-inventory.md)|
|Beschikbaarheid van artikelen weergeven op vestiging, op periode, op verkoop- of inkoopgebeurtenis, of op het gebruik op assemblagestuklijsten.|[Procedure: Een beschikbaarheidoverzicht krijgen](inventory-how-availability-overview.md)|
|Voorraadartikelen verplaatsen tussen vestigingen met transferorders, om magazijnactiviteiten te beheren, of met het artikelherindelingsdagboek.|[Procedure: Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)|
|Vermeerder of verminder de waarde van een of meer artikelen in voorraad door de huidige, berekende waarde ervan te boeken.|[Procedure: Voorraad herwaarderen](inventory-how-revalue-inventory.md)|
|Herwaardeer artikelkosten, automatisch of handmatig, om kostenwijzigingen door te sturen van inkomende posten naar de gerelateerde uitgaande posten.|[Procedure: Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md)|
|Leren hoe wijzigingen in voorraadwaarde van handel automatisch met uw financiële boeken worden afgestemd.|[Geavanceerd: Voorraadreconciliatie](advanced-inventory-reconciliation.md)|

## <a name="see-also"></a>Zie ook  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)    
[Toeleveringsketen](madeira-supply-chain.md)  
[Werken met [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
