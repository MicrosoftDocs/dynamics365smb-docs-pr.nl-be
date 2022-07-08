---
title: Productie of assemblage picken in standaardmagazijnconfiguraties
description: Als voor de magazijnvestiging pickverwerking is vereist, maar niet verzendingsverwerking, gebruikt u de pagina Voorraadpick om het picken van de onderdelen te beheren en vast te leggen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 80a34d18c94038ded7bcf405cabd1c67ddf82539
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078426"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Picken voor assemblage of productie in standaardmagazijnconfiguraties

Hoe u onderdelen voor productie- of assemblageorders opslaat, is afhankelijk van de vestigingsinstellingen van het magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Picken voor productie in standaardmagazijnconfiguraties

De afboekingsmethode heeft ook invloed op de stroom van componenten in de productie. Zie voor meer informatie [Materialen afboeken op basis van de uitvoer van een bewerking](production-how-to-flush-components-according-to-operation-output.md).

In geavanceerde magazijnconfiguraties waar locaties zowel picks als verzendingen vereisen, moet u de pagina **Magazijnpick** gebruiken om componenten met de afboekingsmethode ingesteld op *Handmatig*, *Picken + voorwaarts* of *Picken + achterwaarts* naar productieorders te brengen. Zie voor meer informatie [Picken voor productie of assemblage in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

In standaardmagazijnconfiguraties waarbij voor de vestiging pickverwerking vereist is, maar verzendingsverwerking niet, kunt u ook de pagina **Voorraadpick** gebruiken om het picken te ordenen en vast te leggen van materiaal met de afboekingsmethode ingesteld op *Handmatig*. Wanneer u een voorraadpick registreert voor een interne bewerking, zoals productie, wordt het verbruik van de gepickte materialen tegelijkertijd geboekt. Als alternatief kunt u **Voorraadverplaatsing** met verwijzing naar een brondocument gebruiken om componenten met de afboekingsmethode ingesteld op *Handmatig*, *Picken en + voorwaarts* of *Picken en achterwaarts* naar productieorders te brengen.

Wanneer productiebewerkingen zijn geïntegreerd in magazijnprocessen, ofwel door opslaglocaties of door gestuurde opslag en picks, dan is de opslaglocatie die gedefinieerd is op elke productieordermateriaalregel, de opslaglocatie waaruit de onderdelen worden verbruikt. Alle vereiste onderdelen moeten beschikbaar zijn op die opslaglocatie. Anders wordt de handmatige of afgeboekte verbruiksboeking voor dat onderdeel gestopt.

**Voorraadverplaatsing** met verwijzingen naar het brondocument en **Magazijnpick** kunnen niet worden gebruikt om componenten met de afboekingsmethoden *Voorwaarts* en *Achterwaarts* te picken. **Voorraadpick** kan niet worden gebruikt om componenten te picken met een andere afboekingsmethode dan *Handmatig*. Gebruik om de overige componenten te verwerken **Voorraadbeweging** zonder verwijzing naar een brondocument. Zie voor meer informatie [Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

> [!NOTE]  
>  Voor voorraadpicks, voorraadverplaatsingen en magazijnpicks bestaan de volgende belangrijke verschillen:  
>   
>  -   Wanneer u een voorraadpick registreert voor een interne bewerking, zoals productie, wordt het verbruik van de gepickte materialen tegelijkertijd geboekt. Wanneer u een voorraadpick of magazijnpick registreert voor een interne bewerking, legt u enkel de fysieke verplaatsing vast van de vereiste materialen naar een opslaglocatie in het bewerkingsgebied zonder het verbruik te boeken.  
> -   Bij gebruik van voorraadpicks definieert het veld **Bin Code** op de materiaalregel op een productieorder de opslaglocatie *nemen* waar materialen in mindering worden gebracht wanneer het verbruik wordt geboekt. Bij gebruik van voorraadpicks of magazijnpicks definieert het veld **Opslaglocatie** op materiaalregels in de productieorder de opslaglocatie *plaats* in het bewerkingsgebied waarin de magazijnmedewerker de materialen moet plaatsen.  

Een eerste systeemvereiste voor het picken of verplaatsen van componenten voor brondocumenten is dat er een uitgaande magazijnaanvraag aanwezig is om het magazijngebied in kennis te stellen van het feit dat er een component nodig is. Een uitgaand magazijnverzoek wordt gemaakt telkens wanneer de productieorderstatus wordt gewijzigd in Vrijgegeven of wanneer een vrijgegeven productieorder wordt gemaakt.  

## <a name="to-pick-production-components-in-basic-warehouse-configurations-using-inventory-pick"></a>Productiecomponenten in standaardmagazijnconfiguraties picken met behulp van Voorraadpick

In standaardmagazijnconfiguraties waarbij de locatie alleen is ingesteld voor het gebruik van picken, kunt u onderdelen voor productieactiviteiten kiezen via de pagina **Voorraadpick**. Zie voor meer informatie [Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadpicks** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Brondocumenten ophalen** en selecteer de vrijgegeven productieorder om de productieorderonderdelen te openen.  
3.  Voer de pick uit en leg de werkelijke pickinformatie vast in het veld **Te verwerken aantal**.  
4.  Wanneer de regels gereed zijn voor boeken, kiest u de actie **Boeken**. Het boeken leidt tot het maken van de benodigde magazijnposten en tot het boeken van het verbruik van de artikelen.  

Het is ook mogelijk om rechtstreeks vanuit een vrijgegeven productieorder een **Voorraadpick** te maken. Kies de actie **Voorraadopslag/-pick/-verplaatsing maken**, schakel het selectievakje **Voorraadpick maken** in en klik op de knop **OK**.

Als alternatief kunt u de **Voorraadbeweging** met verwijzing naar het brondocument gebruiken om artikelen tussen opslaglocaties te verplaatsen. U moet het verbruik apart registreren. Zie voor meer informatie [Productieverbruik in batches boeken](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Picken voor assemblage in standaardmagazijnconfiguraties

In geavanceerde magazijnconfiguraties waarin locaties picks en verzendingen vereisen, moet u de pagina **Magazijnpick** gebruiken om componenten naar productie- of assemblageorders te brengen. Zie voor meer informatie [Picken voor productie of assemblage in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

In standaardmagazijnconfiguraties kunt u ook picken voor assemblageorders door gebruik te maken van de pagina **Voorraadverplaatsing**. 

In standaardmagazijnconfiguraties waarbij de locatie wel pickverwerking vereist, maar geen verzendingsverwerking, wordt de pagina **Voorraadpick** ook gebruikt om te picken, te assembleren en te verzenden voor verkooporders waarbij artikelen moeten worden geassembleerd voordat ze kunnen worden verzonden. Zie voor meer informatie [Op-order-assembleren-artikelen met voorraadpicks afhandelen](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Op-order-assembleren-artikelen met voorraadpicks afhandelen

De pagina **Voorraadpick** wordt ook gebruikt voor het picken en verzenden voor verkoop waarbij artikelen moeten worden geassembleerd voordat ze verzonden kunnen worden. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).

Artikelen die verzonden moeten worden, zijn pas fysiek op een opslaglocatie aanwezig wanneer ze in het assemblagegebied worden geassembleerd en worden geboekt als uitvoer naar opslaglocatie. Dit betekent dat het picken van op-order-assembleren-artikelen voor verzending een bijzondere werkstroom volgt. Vanuit een opslaglocatie brengen magazijnmedewerkers de assemblageartikelen naar de verzenddock waar de voorraadpick wordt geboekt. Tijdens de geboekte voorraadpick worden de assemblageuitvoer, het materiaalverbruik en de verkoopverzending geboekt.

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] zo instellen dat automatisch een voorraadverplaatsing wordt gemaakt wanneer de voorraadpick voor het assemblageartikel wordt gemaakt. Als u dit wilt inschakelen, selecteert u het veld **Verplaatsingen automatisch aanmaken** op de pagina **Assemblage-instelling**. Zie voor meer informatie [Onderdelen verplaatsen naar een bewerkingsgebied bij standaard magazijnbeheer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Voorraadpickregels voor verkoopartikelen worden op verschillende manieren gemaakt, al naar gelang geen, enkele of alle verkoopregelaantallen op order zijn geassembleerd.

Bij een normale verkoop waarbij u voorraadpicks gebruikt om verzending van voorraadaantallen te boeken, wordt er één voorraadpickregel, of meerdere wanneer het artikel in verschillende opslaglocaties is geplaatst, gemaakt voor iedere verkooporderregel. Deze pickregel is gebaseerd op het aantal in het veld **Te verzenden aantal**.

Bij een op-order-assembleren-verkoop, waarbij het volledige aantal op de verkooporderregel op order wordt geassembleerd, wordt één voorraadpickregel voor dat aantal gemaakt. Dit betekent dat de waarde in het veld Te assembleren aantal overeenkomt met de waarde in het veld **Te verzenden aantal**. Het veld **Op order assembleren** wordt geselecteerd op de regel.

Als een assemblage-uitvoerstroom voor de locatie is ingesteld, wordt de waarde in het veld **Opslagloc. verz. asm.-op-order** of de waarde in het veld **Opslagloc.code Vanuit-assembl.**, in die volgorde, ingevoegd in het veld **Opslaglocatie** op de voorraadpickregel.

Als geen opslaglocatie op de verkooporderregel is opgegeven en assemblage-uitvoerstroom voor de locatie is ingesteld, is het veld **Opslaglocatie** op de voorraadpickregel leeg. De magazijnmedewerker moet de pagina **Opslaglocatie-inhoud** openen en de opslaglocatie selecteren waar de assemblageartikelen worden geassembleerd.

In combinatiescenario's waarbij een deel van de hoeveelheid eerst moet worden geassembleerd en een ander deel uit de voorraad moet worden gepickt, moeten minimaal twee voorraadpickregels worden gemaakt. Eén pickregel dient voor het op-order-assembleren-aantal. De andere pickregel is afhankelijk van welke opslaglocaties aan het resterend aantal in voorraad kunnen voldoen. Opslaglocatiescodes op de twee regels worden op verschillende manieren ingevuld, zoals voor de twee verschillende typen verkoop respectievelijk wordt beschreven. Zie voor meer informatie de sectie Combinatiescenario's in [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>De verbruiksopslaglocatie vullen

In dit stroomdiagram wordt weergegeven hoe het veld **Opslaglocatie** op de productieordercomponentregels wordt ingevuld op basis van uw vestigingsinstellingen.

![Stroomdiagram Opslaglocatie.](media/binflow.png "BinFlow")

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Zie ook

[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
