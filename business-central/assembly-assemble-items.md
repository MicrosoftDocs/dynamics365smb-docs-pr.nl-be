---
title: Assemblagebeheer
description: Leer hoe u producten aan klanten kunt leveren door materiaal in eenvoudige processen te combineren zonder gebruik te maken van productiefuncties.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="assembly-management"></a><a name="assembly-management"></a>Assemblagebeheer

Bedrijven kunnen producten aan klanten leveren door materiaal te combineren zonder gebruik te maken van productiefuncties. Functies voor het assembleren van artikelen kunnen worden geïntegreerd met gerelateerde functies zoals verkoop, planning, reserveringen en magazijn.  

Een component is een verkoopbaar artikel dat een assemblagestuklijst bevat. Ga voor meer informatie over assemblagestuklijsten naar [Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md).

Assemblageorders zijn net als productieorders interne orders. Gebruik assemblageorders om het assemblageproces te beheren en verkoopbehoeften te koppelen aan magazijnactiviteiten. Bij assemblageorders is zowel output als verbruik betrokken bij het boeken. Assemblageorderkoppen zijn vergelijkbaar met outputdagboekregels. Assemblageorderregels zijn vergelijkbaar met verbruikdagboekregels.  

U kunt een just-in-time voorraadstrategie gebruiken en producten aanpassen aan de verzoeken van klanten. Assemblageorders kunnen nu automatisch worden gemaakt en gekoppeld wanneer u een verkooporderregel maakt. De koppeling tussen de verkoopvraag en het assemblageaanbod opent verschillende kansen wanneer u verkooporders verwerkt:

* Pas componenten in een handomdraai aan.
* Beloof leveringsdata op basis van beschikbaarheid van materiaal.
* Boek output en verzending van het geassembleerde artikel rechtstreeks vanuit de verkooporders ervan.

Ga voor meer informatie over het verkopen van artikelen naar [Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).  

Regels op verkooporders kunnen artikelen bevatten om uit voorraad te picken en artikelen om voor de order te assembleren. De op-order-assembleren-hoeveelheden hebben voorrang op voorraadhoeveelheden bij gedeeltelijke verzending. Ga voor meer informatie over het verkopen van voorraad- en componentartikelen naar [Combinatiescenario's](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Wanneer een aantal voor assembleren-op-order klaar is om te worden verzonden, kan de medewerker een voorraadpick boeken voor de verkooporderregels. Het boeken van een voorraadpick doet een aantal dingen:

* Maak een voorraadverplaatsing voor de componenten
* Boek de assemblyuitvoer en de verkooporderverzending.

Zie voor meer informatie over assembleren-op-order artikelen en voorraadpicks [Op-order-assembleren-artikelen met voorraadpicks afhandelen](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.

|**Functie**|**Zie**|  
|------------|-------------|  
|Meer informatie over het assembleren van artikelen voor verkooporders en opslag.|[Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Gebruik vestigingskaarten en uw voorraadinstellingen om te bepalen hoe artikelen van en naar assemblage stromen.|[Standaardmagazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Maak een offerte voor een op maat gemaakte component en zet de offerte vervolgens om in een verkoop wanneer de klant deze accepteert.|[Een offerte maken voor een assembleren voor order-verkoop](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Combineer materiaal om een op-order artikel of een voorraadartikel te maken.|[Artikelen samenstellen](assembly-how-to-assemble-items.md)|  
|Verkoop componenten die nu niet verkrijgbaar zijn door een gekoppelde assemblageorder te maken om het volledige of gedeeltelijke verkooporderaantal te leveren.|[Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md)|
|Als sommige op-order-assembleren-artikelen al in voorraad zijn, trekt u die hoeveelheid af van de assemblageorder en reserveert u deze vanuit voorraad.|[Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Wanneer componenten niet in voorraad zijn, gebruikt u een assemblageorder om een deel of de gehele hoeveelheid te leveren.|[Op-order-assembleren-artikelen en voorraadartikelen samen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Maak aangepaste componenten voor verkoopraamcontracten voordat u de verkooporders maakt.|[Afroepassemblyorders maken](assembly-how-to-create-blanket-assembly-orders.md)|
|Een geboekte assemblyorder ongedaan maken, bijvoorbeeld omdat de order met fouten is geboekt.|[Boeken van assemblage ongedaan maken](assembly-how-to-undo-assembly-posting.md)|
|Meer informatie over het werken met assemblagestuklijsten en hoe ze verschillen van productiestuklijsten.|[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)|
|Meer informatie over het boeken van assemblageverbruik en -output, en hoe [!INCLUDE [prod_short](includes/prod_short.md)] artikel- en resourcekosten verdeelt over het grootboek.|[Ontwerpdetails: Assemblageorderboeking](design-details-assembly-order-posting.md)|  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Werken met stuklijsten](inventory-how-work-BOMs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Ontwerpdetails: Leveringsplanning](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
