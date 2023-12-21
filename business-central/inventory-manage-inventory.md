---
title: Voorraad beheren
description: 'In dit artikel wordt beschreven hoe u de fysieke producten die u inruilt, kunt beheren door een voorraadartikelkaart te maken.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.forms: '5804, 2106, 5823, 5751, 5750, 772, 5829, 5828, 513, 304, 40, 38, 167, 117, 5827, 9223, 158, 354, 9152, 286, 5754, 5402, 209, 297, 298, 99000782'
ms.date: 12/19/2023
ms.author: bholtorf
---

# Voorraad beheren

Voor elk fysiek product dat u verhandelt, moet u een artikelkaart van het type **Voorraad** maken. Artikelen die u aan klanten aanbiedt maar in voorraad houdt, kunt u als catalogusartikelen registreren, die u indien nodig naar voorraadartikelen kunt converteren. U kunt de hoeveelheid van een artikel in voorraad verhogen of verlagen door rechtstreeks naar de artikelposten te boeken, bijvoorbeeld na een fysieke telling of als u geen inkopen registreert.

Positieve en negatieve voorraadmutaties worden natuurlijk ook geregistreerd wanneer u respectievelijk inkoop- en verkoopdocumenten boekt. Zie voor meer informatie [Inkopen registreren](purchasing-how-record-purchases.md), [Producten verkopen](sales-how-sell-products.md) en [Verkopen factureren](sales-how-invoice-sales.md). De transfers tussen vestigingen wijzigen de voorraadaantallen in alle magazijnen van het bedrijf.

Om het overzicht van artikelen te verbeteren en deze te helpen zoeken, kunt u artikelen categoriseren en er kenmerken aan toewijzen op basis waarvan u ze kunt zoeken en sorteren.

> [!NOTE]
> Naar de fysieke verwerking van artikelen wordt verwezen als magazijnactiviteiten. Zie voor meer informatie [Overzicht van magazijnbeheer](design-details-warehouse-management.md).

Planning voor artikelen om aan vraag te voldoen, wordt behandeld als onderdeel van de functionaliteit voor vraagplanning. Lees meer op [Planning](production-planning.md).  

## Voorraadreconciliatie

Als u voorraadtransacties (bijvoorbeeld verkoopverzendingen, inkoopfacturen of voorraadherwaarderingen) boekt, worden de gewijzigde artikelkosten vastgelegd in artikelwaardeposten. Om deze wijziging van voorraadwaarde door te voeren in uw financiële boeken, worden de voorraadkosten automatisch geboekt naar de gerelateerde voorraadrekeningen in het grootboek. Voor iedere voorraadtransactie die u boekt, worden overeenkomende waarden geboekt naar de voorraadrekening, de correctierekening en de KPV-rekening in het grootboek. Lees meer op [Voorraadkosten reconciliëren met het grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Hoewel voorraadkosten automatisch naar het grootboek worden geboekt, moeten de kosten van goederen toch worden doorgestuurd naar de gerelateerde uitgaande verkooptransactie, vooral in situaties waarin u goederen verkoopt voordat u de inkoop van die goederen factureert. Dit wordt kostenwaardering genoemd. Artikelkosten worden automatisch aangepast als u artikeltransacties boekt, maar u kunt artikelkosten ook handmatig wijzigen. Lees meer op [Artikelkosten aanpassen](inventory-how-adjust-item-costs.md).  

## Verwante taken

De volgende tabel geeft een overzicht van gerelateerde taken.

|Tot |Zie |
|---|----|
|Maak artikelkaarten voor voorraadartikelen waarin u handelt.|[Nieuwe artikelen registreren](inventory-how-register-new-items.md)|
|Bovenliggende artikelen structureren die u als pakketten verkoopt bestaande uit de onderdelen van de bovenliggende artikelen, of die u op bestelling of voor voorraad assembleert.|[Werken met stuklijsten](inventory-how-work-BOMs.md)|
|Onderhoud een overzicht van artikelen en help artikelen te zoeken en te sorteren door ze in categorieën te organiseren.|[Artikelen categoriseren](inventory-how-categorize-items.md)|
|Wijs artikelkenmerken van verschillende waardesoorten aan uw artikelen toe zodat u artikelen gemakkelijker kunt sorteren en vinden.|[Werken met artikelkenmerken](inventory-how-work-item-attributes.md)|
|Maak speciale artikelkaarten voor artikelen die u aan klanten aanbiedt, maar die u niet in voorraad houdt.|[Werken met catalogusartikelen](inventory-how-work-nonstock-items.md)|
|Voer een inventarisatie van uw voorraad uit met de pagina's **Inventarisatieorder** en **Inventarisatieregistratie**.|[Voorraad tellen met documenten](inventory-how-count-inventory-with-documents.md)|
|Inventarisatie uitvoeren, negatieve of positieve correcties uitvoeren en gegevens wijzigen, zoals locatie of lotnummer, in artikelposten of magazijnposten.|[Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md)|
|Beschikbaarheid van artikelen weergeven op vestiging, periode, verkoop- of inkoopgebeurtenis, of het gebruik in assemblage- of productiestuklijsten.|[Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)|
|Voorraadartikelen verplaatsen tussen vestigingen met transferorders, om magazijnactiviteiten te beheren, of met het artikelherindelingsdagboek.|[Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)|
|Voorraad of inkomende artikelen registreren voor verkooporders, inkooporders, serviceorders, assemblageorders, transferorders of productieorders.|[Artikelen reserveren](inventory-how-to-reserve-items.md)|
|Artikeltracering instellen zodat u artikelserienummers kunt volgen, bijvoorbeeld wanneer u artikelen moet traceren in geval van terugroepacties.|[Artikeltracering instellen met serie-, partij- en pakketnummers](inventory-how-setup-item-tracking.md)|
|Wijs serienummers of lotnummers toe aan elk uitgaand of inkomend document of journaalregel.|[Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)|
|Bepalen waar elk serie- of lotnummer is gebruikt in de voorraadketen, bijvoorbeeld in situaties waarin producten moeten worden teruggeroepen.|[Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)|
|Een eigen artikelbeschrijving van de leverancier of klant instellen op uw artikelkaart, zodat u hun artikelbeschrijving snel kunt invoegen op handelsdocumenten.|[Artikelverwijzingen gebruiken](inventory-how-use-item-cross-refs.md)|
|Het invoeren van artikelen op verkoop- of inkoopregels of het boeken van artikelen in transacties voorkomen.|[Artikelen blokkeren](inventory-how-block-items.md)|
|De bedrijfsvoering in verkoop- of inkoopafdelingen of planningskantoren voor een fabriek voor meerdere vestigingen beheren.|[Werken met divisies](inventory-responsibility-centers.md)|
|Resources gebruiken met specifieke functies voor verschillende services en service-items.|[Resourcetoewijzing instellen](service-how-setup-resource-allocation.md)|

## Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
