---
title: Op-order-assembleren-artikelen en voorraadartikelen samen verkopen
description: 'Als een onderdeel van een op-voorraad-assembleren artikel niet beschikbaar is, kunt u een assemblageorder aanmaken voor de resterende hoeveelheid.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Op-order-assembleren-artikelen en voorraadartikelen samen verkopen

Als het veld **Assemblagebeleid** op de artikelkaart van een component **Op voorraad assembleren** bevat, neemt het standaardproces voor de verkooporder aan dat het artikel al is geassembleerd en uit voorraad kan worden gepickt, als het beschikbaar is. Daarom wordt er geen assemblageorder automatisch gemaakt en gekoppeld aan de verkooporderregel. Als de hoeveelheid echter deels of helemaal niet beschikbaar is, kunt u een assemblageorder maken voor de resterende hoeveelheid. Vul hiervoor het veld **Op order te assembleren aantal** op de verkooporderregel in. Met deze instelling kunt u het artikel op order assembleren, ook al is het standaard ingesteld om op voorraad te worden geassembleerd.  

U hebt vergelijkbare flexibiliteit wanneer u op-order-assembleren artikelen verkoopt en een deel van de hoeveelheid al in voorraad is. U wilt die hoeveelheid aftrekken van de assemblageorder. Zie voor meer informatie over het verkopen van voorraadartikelen [Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Bepaalde regels zijn van toepassing op het veld **Te verzenden aantal** op verkooporderregels die een combinatie van op-order-assembleren-aantallen en voorraadaantallen bevatten. Ga voor meer informatie over de regels naar [Combinatiescenario's](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> De volgende procedure bevat niet de verkooporderstappen die u moet volgen voordat u een assemblageorder kunt maken voor hoeveelheden die niet beschikbaar zijn.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Op-order-assembleren-artikelen en voorraadartikelen samen verkopen

1. Op een verkooporderregel voor assembleren-op-voorraad een artikel voert u in het veld **Aantal** een aantal in dat groter is dan de voorraad. De pagina **Beschikbaarheid controleren** verschijnt. Ga voor meer informatie over de beschikbaarheid van artikelen naar [Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md).
2. Voer in het veld **Op order te assembleren aantal** de waarde uit het veld **Totaal aantal** in.  
3. Breng benodigde wijzigingen in de assemblagecomponenten aan. Zie voor meer informatie [Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md)  
4. Geef de verkooporder vrij om de artikelen beschikbaar te maken voor picken en voor assemblage van de niet-beschikbare artikelen. Zie voor meer informatie over deze standaardassemblagestappen [Artikelen samenstellen](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Het veld **Opslaglocatie** in de verkooporder kan de waarde bevatten uit het veld **Opslaglocatiecode assembleren-op-order verzending** of **Opslagloc.code Vanuit-assembl.** op de locatiekaart. In dat geval is het veld **Opslaglocatie** op de verkooporderregel mogelijk onjuist voor deze combinatie van hoeveelheden van assembleren-naar-order en assembleren-naar-voorraad. Het is verstandig om het veld **Opslaglocatie** te bekijken en te controleren of de opslaglocatie voor alle hoeveelheden werkt. U kunt ook twee verschillende hoeveelheden invoeren op aparte verkooporderregels.  

## <a name="see-also"></a>Zie ook

[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
