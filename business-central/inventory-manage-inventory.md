---
title: Voorraad beheren
description: In dit onderwerp wordt beschreven hoe u de fysieke producten die u inruilt, kunt beheren door een voorraadartikelkaart te maken.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 24337d2cd96e4511f1917980c94af407381e96d2
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6325330"
---
# <a name="how-to-manage-inventory"></a>Procedure: Voorraad beheren
Voor elk fysiek product dat u verhandelt, moet u een artikelkaart van het soort **Voorraad** maken. Artikelen die u aan klanten aanbiedt maar in voorraad houdt, kunt u als catalogusartikelen registreren, die u indien nodig naar voorraadartikelen kunt converteren. U kunt de hoeveelheid van een artikel in voorraad verhogen of verlagen door rechtstreeks naar de artikelposten te boeken, bijvoorbeeld na een fysieke telling of als u geen inkopen registreert.

Positieve en negatieve voorraadmutaties worden natuurklijk ook geregistreerd wanneer u respectievelijk inkoop- en verkoopdocumenten boekt. Zie voor meer informatie [Inkopen registreren](purchasing-how-record-purchases.md), [Producten verkopen](sales-how-sell-products.md) en [Verkopen factureren](sales-how-invoice-sales.md). De transfers tussen vestigingen wijzigen de voorraadaantallen in alle magazijnen van het bedrijf.   

Om het overzicht van artikelen te verhogen en deze te zoeken, kunt u artikelen categoriseren en er kenmerken aan toewijzen op basis waarvan u ze kunt zoeken en sorteren.

> [!NOTE]
> Naar de fysieke verwerking van artikelen wordt verwezen als magazijnactiviteiten. Zie voor meer informatie [Magazijnbeheer](warehouse-manage-warehouse.md).

Planning voor artikelen om aan de vraag te voldoen, wordt behandeld als onderdeel van de functionaliteit voor vraagplanning. Zie [Planning](production-planning.md) voor meer informatie.  

## <a name="inventory-reconciliation"></a>Voorraadreconciliatie
Als u voorraadtransacties (bijvoorbeeld verkoopverzendingen, inkoopfacturen of voorraadherwaarderingen) boekt, worden de gewijzigde artikelkosten vastgelegd in artikelwaardeposten. Om deze wijziging van voorraadwaarde door te voeren in uw financiële boeken, worden de voorraadkosten automatisch geboekt naar de gerelateerde voorraadrekeningen in het grootboek. Voor iedere voorraadtransactie die u boekt, worden overeenkomende waarden geboekt naar de voorraadrekening, de correctierekening en de KPV-rekening in het grootboek. Zie voor meer informatie [Voorraadkosten reconciliëren met het grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Hoewel voorraadkosten automatisch naar het grootboek worden geboekt, moeten de kosten van goederen toch worden doorgestuurd naar de gerelateerde uitgaande verkooptransactie, vooral in situaties waarin u goederen verkoopt voordat u de inkoop van die goederen factureert. Dit wordt kostenwaardering genoemd. Artikelkosten worden automatisch aangepast als u artikeltransacties boekt, maar u kunt artikelkosten ook handmatig wijzigen. Zie [Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md) voor meer informatie.  

## <a name="related-tasks"></a>Verwante taken

De volgende tabel geeft een overzicht van gerelateerde taken.

|Als u dit wilt doen: |Zie |
|---|----|
|Maak artikelkaarten voor voorraadartikelen waarin u handelt.|[Nieuwe artikelen registreren](inventory-how-register-new-items.md)|
|Bovenliggende artikelen structureren die u als pakketten verkoopt bestaande uit de onderdelen van de bovenliggende artikelen, of die u op bestelling of voor voorraad monteert.|[Werken met stuklijsten](inventory-how-work-BOMs.md)|
|Onderhoud een overzicht van artikelen en help artikelen te zoeken en te sorteren door ze in categorieën te organiseren.|[Artikelen categoriseren](inventory-how-categorize-items.md)|
|Wijs artikelkenmerken van verschillende waardesoorten aan uw artikelen toe zodat u artikelen gemakkelijker kunt sorteren en vinden.|[Werken met artikelkenmerken](inventory-how-work-item-attributes.md)|
|Maak speciale artikelkaarten voor artikelen die u aan klanten aanbiedt, maar die u niet in voorraad houdt.|[Werken met catalogusartikelen](inventory-how-work-nonstock-items.md)|
|Voer een inventarisatie van uw voorraad uit met de pagina's **Inventarisatieorder** en **Inventarisatieregistratie**.|[Voorraad tellen met documenten](inventory-how-count-inventory-with-documents.md)|
|Inventarisatie uitvoeren, negatieve of positieve correcties uitvoeren en gegevens wijzigen, zoals locatie of lotnummer, in artikelposten of magazijnposten.|[Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md)|
|Beschikbaarheid van artikelen weergeven op vestiging, periode, verkoop- of inkoopgebeurtenis, of het gebruik in assemblage- of productiestuklijsten.|[Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)|
|Voorraadartikelen verplaatsen tussen vestigingen met transferorders, om magazijnactiviteiten te beheren, of met het artikelherindelingsdagboek.|[Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)|
|Reserveer voorraad of inkomende artikelen voor verkooporders, inkooporders, serviceorders, assemblageorders of productieorders.|[Artikelen reserveren](inventory-how-to-reserve-items.md)|
|Wijs serienummers of lotnummers toe aan elk uitgaand of inkomend document of dagboekregel, bijvoorbeeld om artikelen te traceren bij terugroepacties.|[Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)|
|Stel een eigen artikelbeschrijving van de leverancier of klant in op uw artikelkaart, zodat u hun artikelbeschrijving snel kunt invoegen op handelsdocumenten.|[Artikelkruisverwijzingen gebruiken](inventory-how-use-item-cross-refs.md)|
|Bepalen waar elk serie- of lotnummer is gebruikt in de voorraadketen, bijvoorbeeld in situaties waarin producten moeten worden teruggeroepen.|[Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)|
|Het invoeren van artikelen op verkoop- of inkoopregels of het boeken van artikelen in transacties voorkomen.|[Artikelen blokkeren](inventory-how-block-items.md)|
|De bedrijfsvoering in verkoop- of inkoopafdelingen of planningskantoren voor een fabriek voor meerdere vestigingen beheren.|[Werken met divisies](inventory-responsibility-centers.md)|
|Gebruik resources met specifieke vaardigheden voor verschillende services en service-items.|[Resourcetoewijzing instellen](service-how-setup-resource-allocation.md)|

## <a name="see-also"></a>Zie ook

[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]