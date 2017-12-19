---
title: Voorraad beheren| Microsoft Docs
description: Beschrijft hoe u de fysieke producten beheert waarin u handelt, bijvoorbeeld de voorraad in uw magazijn.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 1aa1a7c2ec56c3f123bde67a9870be4efd99bdb5
ms.contentlocale: nl-be
ms.lasthandoff: 12/14/2017

---

# <a name="inventory"></a>Voorraad
Voor elk fysiek product dat u verhandelt, moet u een artikelkaart van het soort **Voorraad** maken. Artikelen die u aan klanten aanbiedt maar in voorraad houdt, kunt u als niet-voorraadartikelen registreren, die u indien nodig naar voorraadartikelen kunt converteren. U kunt de hoeveelheid van een artikel in voorraad verhogen of verlagen door rechtstreeks naar de artikelposten te boeken, bijvoorbeeld na een fysieke telling of als u geen inkopen registreert.

Positieve en negatieve voorraadmutaties worden natuurklijk ook geregistreerd wanneer u respectievelijk inkoop- en verkoopdocumenten boekt. Zie voor meer informatie [Procedure: Inkopen registreren](purchasing-how-record-purchases.md), [Procedure: Producten verkopen](sales-how-sell-products.md) en [Procedure: Verkopen factureren](sales-how-invoice-sales.md). De transfers tussen vestigingen wijzigen de voorraadaantallen in alle magazijnen van het bedrijf.   

Om het overzicht van artikelen te verhogen en deze te zoeken, kunt u artikelen categoriseren en er kenmerken aan toewijzen op basis waarvan u ze kunt zoeken en sorteren.

> [!NOTE]
> Naar de fysieke verwerking van artikelen wordt verwezen als magazijnactiviteiten. Zie voor meer informatie [Magazijnbeheer](warehouse-manage-warehouse.md).

## <a name="inventory-reconciliation"></a>Voorraadreconciliatie
Als u voorraadtransacties (bijvoorbeeld verkoopverzendingen, inkoopfacturen of voorraadherwaarderingen) boekt, worden de gewijzigde artikelkosten vastgelegd in artikelwaardeposten. Om deze wijziging van voorraadwaarde door te voeren in uw financiële boeken, worden de voorraadkosten automatisch geboekt naar de gerelateerde voorraadrekeningen in het grootboek. Voor iedere voorraadtransactie die u boekt, worden overeenkomende waarden geboekt naar de voorraadrekening, de correctierekening en de KPV-rekening in het grootboek. Zie voor meer informatie [Procedure: Voorraadkosten reconciliëren met het grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Hoewel voorraadkosten automatisch naar het grootboek worden geboekt, moeten de kosten van goederen toch worden doorgestuurd naar de gerelateerde uitgaande verkooptransactie, vooral in situaties waarin u goederen verkoopt voordat u de inkoop van die goederen factureert. Dit wordt kostenwaardering genoemd. Artikelkosten worden automatisch aangepast als u artikeltransacties boekt, maar u kunt artikelkosten ook handmatig wijzigen. Zie [Procedure: Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md) voor meer informatie.

|Als u dit wilt doen |Zie |
|---|----|
|Maak artikelkaarten voor voorraadartikelen waarin u handelt.|[Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md)|
|Bovenliggende artikelen structureren die u als pakketten verkoopt bestaande uit de onderdelen van de bovenliggende artikelen, of die u op bestelling of voor voorraad monteert.|[Procedure: Werken met stuklijsten](inventory-how-work-BOMs.md)|
|Onderhoud een overzicht van artikelen en help artikelen te zoeken en te sorteren door ze in categorieën te organiseren.|[Procedure: Artikelen categoriseren](inventory-how-categorize-items.md)|
|Wijs artikelkenmerken van verschillende waardesoorten aan uw artikelen toe zodat u artikelen gemakkelijker kunt sorteren en vinden.|[Procedure: Werken met artikelkenmerken](inventory-how-work-item-attributes.md)|
|Maak speciale artikelkaarten voor artikelen die u aan klanten aanbiedt, maar die u niet in voorraad houdt.|[Procedure: Werken met niet-voorraadartikelen](inventory-how-work-nonstock-items.md)|
|Inventarisatie uitvoeren, negatieve of positieve correcties uitvoeren en gegevens wijzigen, zoals locatie of lotnummer, in artikelposten of magazijnposten.|[Procedure: Voorraad tellen, corrigeren en herindelen](inventory-how-count-adjust-reclassify.md)|
|Beschikbaarheid van artikelen weergeven op vestiging, periode, verkoop- of inkoopgebeurtenis, of het gebruik in assemblage- of productiestuklijsten.|[Procedure: beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)|
|Voorraadartikelen verplaatsen tussen vestigingen met transferorders, om magazijnactiviteiten te beheren, of met het artikelherindelingsdagboek.|[Procedure: Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)|
|Reserveer voorraad of inkomende artikelen voor verkooporders, inkooporders, serviceorders, assemblageorders of productieorders.|[Procedure: Artikelen reserveren](inventory-how-to-reserve-items.md)|
|Wijs serienummers of lotnummers toe aan elk uitgaand of inkomend document of dagboekregel, bijvoorbeeld om artikelen te traceren bij terugroepacties.|[Procedure: Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)|
|Bepalen waar elk serie- of lotnummer is gebruikt in de voorraadketen, bijvoorbeeld in situaties waarin producten moeten worden teruggeroepen.|[Procedure: artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)|
|De bedrijfsvoering in verkoop- of inkoopafdelingen of planningskantoren voor een fabriek voor meerdere vestigingen beheren.|[Procedure: Werken met divisies](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)    
[Werken met [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

