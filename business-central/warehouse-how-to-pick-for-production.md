---
title: Picken voor productie, assemblage of taken in standaardmagazijn
description: Als voor de magazijnvestiging vereist is dat u picks verwerkt, maar geen verzendingen, gebruikt u de pagina Voorraadpick om het picken van de onderdelen vast te leggen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617889"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Picken voor productie, assemblage of taken in standaardmagazijnconfiguraties

Hoe u onderdelen voor productie- of assemblageorders opslaat, is afhankelijk van de vestigingsinstellingen van het magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Picken voor productie in standaardmagazijnconfiguraties

Als een vestiging pickverwerking vereist maar geen verwerking van verzending, kunt u de pagina **Voorraadpick** gebruiken. Met de pagina **Voorraadpick** kunt u het picken van artikelen organiseren en vastleggen waarvan de afboekingsmethode is ingesteld op **Handmatig**. Wanneer u een voorraadpick registreert, wordt het verbruik van de gepickte componenten geboekt. U kunt ook een **Voorraadverplaatsing** met verwijzing naar een brondocument gebruiken om componenten met de afboekingsmethode ingesteld op **Handmatig**, **Picken en + voorwaarts** of **Picken en achterwaarts** toe te wijzen aan productieorders.

Als de productie is geïntegreerd met magazijnprocessen via opslaglocaties of gerichte opslag en picks, worden componenten uit de opslaglocatie op de productieorderregel verbruikt. Alle vereiste onderdelen moeten beschikbaar zijn op die opslaglocatie. Anders wordt handmatige of afgeboekte verbruiksboeking voor dat onderdeel gestopt.

> [!NOTE]  
> Voor voorraadpicks, voorraadverplaatsingen en magazijnpicks bestaan de volgende belangrijke verschillen:  
>
> - Wanneer u een voorraadpick registreert voor een interne bewerking, zoals productie, wordt het verbruik van de gepickte materialen tegelijkertijd geboekt. Wanneer u een voorraadpick of magazijnpick registreert voor een interne bewerking, legt u enkel de fysieke verplaatsing vast van de vereiste materialen naar een opslaglocatie in het bewerkingsgebied zonder het verbruik te boeken.  
> - Bij gebruik van voorraadpicks definieert het veld **Bin Code** op de materiaalregel op een productieorder de opslaglocatie *nemen* waar materialen in mindering worden gebracht wanneer het verbruik wordt geboekt. Bij gebruik van voorraadpicks of magazijnpicks definieert het veld **Opslaglocatie** op materiaalregels in de productieorder de opslaglocatie *plaats* in het bewerkingsgebied waarin de magazijnmedewerker de materialen moet plaatsen.  

Als u componenten wilt picken of verplaatsen voor brondocumenten, moet een uitgaande magazijnaanvraag het magazijngebied in kennis stellen van het feit dat er een component nodig is. De uitgaande magazijnaanvraag wordt gemaakt wanneer u het volgende doet:

- De status van een productieorder wijzigen in Vrijgegeven.
- Een vrijgegeven productieorder maken.  

Afboekingsmethoden hebben heeft ook invloed op de stroom van componenten in productie. Zie voor meer informatie [Materialen afboeken op basis van de uitvoer van een bewerking](production-how-to-flush-components-according-to-operation-output.md). **Voorraadverplaatsing** met verwijzingen naar het brondocument en **Magazijnpick** kunnen niet worden gebruikt om componenten met de afboekingsmethoden *Voorwaarts* en *Achterwaarts* te picken. **Voorraadpick** kan niet worden gebruikt om componenten te picken met een andere afboekingsmethode dan *Handmatig*. Gebruik om de overige componenten te verwerken **Voorraadbeweging** zonder verwijzing naar een brondocument. Zie voor meer informatie [Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

In geavanceerde magazijnconfiguraties waar locaties zowel picks als verzendingen vereisen, moet u de pagina **Magazijnpick** gebruiken om componenten met de afboekingsmethode ingesteld op *Handmatig*, *Picken + voorwaarts* of *Picken + achterwaarts* naar productieorders te brengen. Zie voor meer informatie [Picken voor productie of assemblage in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Onderdelen picken voor productie en taken in standaardmagazijnconfiguraties

In standaardmagazijnconfiguraties waarbij de locatie alleen is ingesteld voor het gebruik van picken, kunt u onderdelen voor productieactiviteiten en taakplanningsregels kiezen via de pagina **Voorraadpick**. Zie voor meer informatie [Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> De mogelijkheid om componenten voor taakplanningsregels te picken is toegevoegd aan [!INCLUDE[d365fin](includes/d365fin_md.md)] in 2022 releasewave 2. Om de mogelijkheid te gebruiken, moet een beheerder **Functie-update: Voorraad- en magazijnpicks vanuit projecten inschakelen** inschakelen op de pagina **Functiebeheer**.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de waarde in het veld **Resterend aantal** op de taakplanningsregel wanneer deze voorraadpicks maakt. Als u voorraadkeuzes voor taken wilt gebruiken, moet u de schakelaar **Gebruikslink toepassen** inschakelen op de pagina **Projectkaart** voor het project. Hiermee kunt u het gebruik volgen ten opzichte van uw plan. Als u de schakelaar niet aanzet, blijft het resterende aantal op **0** en wordt de voorraadkeuze niet gemaakt. Zie [Bijhouden van projectgebruik instellen](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadpicks** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Brondocumenten ophalen** en selecteer de vrijgegeven productieorder om de productieorderonderdelen te openen.  
3. Pick de component uit en leg de pickinformatie vast in het veld **Te verwerken aantal**.  
4. Wanneer de regels gereed zijn voor boeken, kiest u de actie **Boeken**. Het boeken leidt tot het maken van de benodigde magazijnposten en tot het boeken van het verbruik van de artikelen.  

Het is ook mogelijk om rechtstreeks vanuit een vrijgegeven productieorder een **Voorraadpick** te maken. Kies de actie **Voorraadopslag/-pick/-verplaatsing maken**, schakel het selectievakje **Voorraadpick maken** in en klik op de knop **OK**.

Als alternatief kunt u een **Voorraadbeweging** met verwijzing naar het brondocument gebruiken om artikelen tussen opslaglocaties te verplaatsen. U moet het verbruik apart registreren. Zie voor meer informatie [Productieverbruik in batches boeken](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Picken voor assemblage in standaardmagazijnconfiguraties

Gebruik de volgende pagina's om assemblageorders te picken:

- De pagina **Voorraadverplaatsing**.
- Als de locatie picks vereist maar geen verzendingen, gebruik dan de pagina **Voorraadkeuze** om te picken, assembleren en verzenden voor verkooporders waarbij artikelen moeten worden geassembleerd voordat ze kunnen worden verzonden. Zie voor meer informatie [Op-order-assembleren-artikelen met voorraadpicks afhandelen](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

In geavanceerde magazijnconfiguraties waarin locaties picks en verzendingen vereisen, moet u de pagina **Magazijnpick** gebruiken om componenten naar productie- of assemblageorders te brengen. Zie voor meer informatie [Picken voor productie of assemblage in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Op-order-assembleren-artikelen met voorraadpicks afhandelen

De pagina **Voorraadpick** wordt ook gebruikt voor het picken en verzenden voor verkoop waarbij artikelen moeten worden geassembleerd voordat ze verzonden kunnen worden. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).

Te verzenden op order assembleren-artikelen worden pas als aanwezig in een opslaglocatie beschouwd wanneer ze in het assemblagegebied worden geassembleerd en worden geboekt als uitvoer naar een opslaglocatie. Het picken van deze artikelen voor verzending volgt daarom een speciale stroom. Vanuit een opslaglocatie brengen magazijnmedewerkers de assemblageartikelen naar de verzenddock waar de voorraadpick wordt geboekt. Tijdens de geboekte voorraadpick worden de assemblageuitvoer, het materiaalverbruik en de verkoopverzending geboekt.

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] zo instellen dat automatisch een voorraadverplaatsing wordt gemaakt wanneer de voorraadpick voor het assemblageartikel wordt gemaakt. Als u automatisch verplaatsingen wilt maken, kiest u het veld **Verplaatsingen automatisch aanmaken** op de pagina **Assemblage-instelling**. Zie voor meer informatie [Onderdelen verplaatsen naar een bewerkingsgebied bij standaard magazijnbeheer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

[!INCLUDE[prod_short](includes/prod_short.md)] maakt voorraadpickregels voor verkoopartikelen anders, afhankelijk van de vraag of geen, enkele of alle verkoopregelaantallen op order zijn geassembleerd.

- In verkoop waar u voorraadpicks gebruikt om voorraadverzending te boeken, makt [!INCLUDE[prod_short](includes/prod_short.md)] één voorraadpickregel voor elke verkooporderregel. Als het artikel in verschillende opslaglocaties wordt geplaatst, wordt er meer dan één regel gemaakt. De pickregels worden gebaseerd op het aantal in het veld **Te verzenden aantal**.
- Bij een verkoop waarbij het volledige aantal op de verkooporderregel op order wordt geassembleerd, wordt één voorraadpickregel voor het aantal gemaakt. De waarde in het veld Te assembleren aantal is hetzelfde als de waarde in het veld **Te verzenden aantal**. Het veld **Op order assembleren** wordt geselecteerd op de regel.

Als een assemblage-uitvoerstroom voor de locatie is ingesteld, wordt de waarde in het veld **Opslagloc. verz. asm.-op-order** of de waarde in het veld **Opslagloc.code Vanuit-assembl.**, in die volgorde, ingevoegd in het veld **Opslaglocatie** op de voorraadpickregel.

Als geen opslaglocatie op de verkooporderregel is opgegeven en assemblage-uitvoerstroom voor de locatie is ingesteld, is het veld **Opslaglocatie** op de voorraadpickregel leeg. De magazijnmedewerker moet de pagina **Opslaglocatie-inhoud** openen en de opslaglocatie selecteren waar de assemblageartikelen worden geassembleerd.

Wanneer eerst een deel van de hoeveelheid moet worden geassembleerd en een ander deel uit voorraad moet worden gepickt, maakt [!INCLUDE[prod_short](includes/prod_short.md)] minimaal twee voorraadpickregels. Eén pickregel dient voor het op-order-assembleren-aantal. De andere pickregel is afhankelijk van welke opslaglocaties aan het resterend aantal in voorraad kunnen voldoen. Opslaglocatiescodes op de twee regels worden op verschillende manieren ingevuld, zoals voor de twee verschillende typen verkoop respectievelijk wordt beschreven. Zie voor meer informatie de sectie Combinatiescenario's in [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>De verbruiksopslaglocatie vullen

In dit stroomdiagram wordt weergegeven hoe het veld **Opslaglocatie** op de productieordercomponentregels wordt ingevuld op basis van uw vestigingsinstellingen.

![Stroomdiagram Opslaglocatie.](media/binflow.png "BinFlow")

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Zie ook

[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
