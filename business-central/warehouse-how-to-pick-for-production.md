---
title: Picken voor productie in standaardmagazijnconfiguraties | Microsoft Docs
description: Als voor de magazijnvestiging pickverwerking is vereist, maar niet verzendingsverwerking, gebruikt u het venster **Voorraadpick** om het picken van onderdelen te beheren en vast te leggen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: fe294cd56c01e1440ff04f7146fada64774f4e8b
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="pick-for-production-or-assembly"></a>Picken voor productie of assemblage
Hoe u onderdelen voor productie- of assemblageorders opslaat, is afhankelijk van de vestigingsinstellingen van het magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

In standaardmagazijnconfiguraties waarbij voor de vestiging pickverwerking vereist is, maar verzendingsverwerking niet, gebruikt u het venster **Voorraadpick** om het picken van onderdelen te beheren en vast te leggen.  

In standaardmagazijnconfiguraties moet u picken voor assemblageorders door gebruik te maken van het venster **Voorraadverplaatsing**. Zie voor meer informatie de sectie 'Op-order-assembleren-artikelen met voorraadpicks afhandelen' in [Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md).  

In geavanceerde magazijnconfiguraties waarin locaties picks en verzendingen vereisen, gebruikt u het venster **Magazijnpick** om componenten naar productie- of assemblageorders te brengen.

> [!NOTE]  
>  Voor voorraadpicks en voorraadverplaatsingen gelden de volgende belangrijke verschillen:  
>   
>  -   Wanneer u een voorraadpick registreert voor een interne bewerking, zoals productie, wordt het verbruik van de gepickte materialen tegelijkertijd geboekt. Wanneer u een voorraadpick registreert voor een interne bewerking, legt u enkel de fysieke verplaatsing vast van de vereiste materialen naar een opslaglocatie in het bewerkingsgebied zonder het verbruik te boeken.  
> -   Bij gebruik van voorraadpicks definieert het veld **Bin Code** op de materiaalregel op een productieorder de opslaglocatie *nemen* waar materialen in mindering worden gebracht wanneer het verbruik wordt geboekt. Bij gebruik van voorraadpicks definieert het veld **Opslaglocatie** op materiaalregels op de productieorder de opslaglocatie *plaats* in het bewerkingsgebied waarin de magazijnmedewerker de materialen moet plaatsen.  

Een eerste systeemvereiste voor het picken of verplaatsen van componenten voor brondocumenten is dat er een uitgaande magazijnaanvraag aanwezig is om het magazijngebied in kennis te stellen van het feit dat er een component nodig is. Een uitgaand magazijnverzoek wordt gemaakt telkens wanneer de productieorderstatus wordt gewijzigd in Vrijgegeven of wanneer een vrijgegeven productieorder wordt gemaakt.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Onderdelen picken in standaardmagazijnconfiguraties
In standaardmagazijnconfiguraties waarbij de locatie alleen is ingesteld voor het gebruik van picken, kunt u onderdelen voor productieactiviteiten kiezen via het venster **Voorraadpick**. Zie voor meer informatie [Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadpicks** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Brondocumenten ophalen** en selecteer de vrijgegeven productieorder om de productieorderonderdelen te openen.  
3.  Voer de pick uit en leg de pickinformatie vast in het veld **Gepickt aantal**.  
4.  Wanneer de regels gereed zijn voor boeken, kiest u de actie **Boeken**. Het boeken leidt tot het maken van de benodigde magazijnposten en tot het boeken van het verbruik van de artikelen.  

Het is ook mogelijk om rechtstreeks vanuit een vrijgegeven productieorder een **Voorraadpick** te maken. Kies de actie **Voorraadopslag/-pick maken**, schakel het selectievakje **Voorraadpick maken** in en klik op de knop **OK**.

U kunt ook het venster **Voorraadverplaatsing** gebruiken voor ad hoc verplaatsing van artikelen tussen opslaglocaties, dat wil zeggen, zonder verwijzing naar een brondocument.
Zie voor meer informatie [Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Op-order-assembleren-artikelen met voorraadpicks afhandelen
Het venster **Voorraadpick** wordt ook gebruikt voor het picken en verzenden voor verkoop waarbij artikelen moeten worden geassembleerd voordat ze verzonden kunnen worden. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).

Artikelen die verzonden moeten worden, zijn pas fysiek op een opslaglocatie aanwezig wanneer ze in het assemblagegebied worden geassembleerd en worden geboekt als uitvoer naar opslaglocatie. Dit betekent dat het picken van op-order-assembleren-artikelen voor verzending een bijzondere werkstroom volgt. Vanuit een opslaglocatie brengen magazijnmedewerkers de assemblageartikelen naar de verzenddock waar de voorraadpick wordt geboekt. Tijdens de geboekte voorraadpick worden de assemblageuitvoer, het materiaalverbruik en de verkoopverzending geboekt.

U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] zo instellen dat automatisch een voorraadverplaatsing wordt gemaakt wanneer de voorraadpick voor het assemblageartikel wordt gemaakt. Als u dit wilt inschakelen, selecteert u het veld **Verplaatsingen automatisch aanmaken** in het venster **Assemblage-instelling**. Zie voor meer informatie [Onderdelen verplaatsen naar een bewerkingsgebied bij standaard magazijnbeheer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Voorraadpickregels voor verkoopartikelen worden op verschillende manieren gemaakt, al naar gelang geen, enkele of alle verkoopregelaantallen op order zijn geassembleerd.

Bij een normale verkoop waarbij u voorraadpicks gebruikt om verzending van voorraadaantallen te boeken, wordt er één voorraadpickregel, of meerdere wanneer het artikel in verschillende opslaglocaties is geplaatst, gemaakt voor iedere verkooporderregel. Deze pickregel is gebaseerd op het aantal in het veld **Te verzenden aantal**.

Bij een op-order-assembleren-verkoop, waarbij het volledige aantal op de verkooporderregel op order wordt geassembleerd, wordt één voorraadpickregel voor dat aantal gemaakt. Dit betekent dat de waarde in het veld Te assembleren aantal overeenkomt met de waarde in het veld **Te verzenden aantal**. Het veld **Op order assembleren** wordt geselecteerd op de regel.

Als een assemblage-uitvoerstroom voor de locatie is ingesteld, wordt de waarde in het veld **Opslagloc. verz. asm.-op-order** of de waarde in het veld **Opslagloc.code Vanuit-assembl.**, in die volgorde, ingevoegd in het veld **Opslaglocatie** op de voorraadpickregel.

Als geen opslaglocatie op de verkooporderregel is opgegeven en assemblage-uitvoerstroom voor de locatie is ingesteld, is het veld **Opslaglocatie** op de voorraadpickregel leeg. De magazijnmedewerker moet het venster **Opslaglocatie-inhoud** openen en de opslaglocatie selecteren waar de assemblageartikelen worden geassembleerd.

In combinatiescenario's waarbij een deel van de hoeveelheid eerst moet worden geassembleerd en een ander deel uit de voorraad moet worden gepickt, moeten minimaal twee voorraadpickregels worden gemaakt. Eén pickregel dient voor het op-order-assembleren-aantal. De andere pickregel is afhankelijk van welke opslaglocaties aan het resterend aantal in voorraad kunnen voldoen. Opslaglocatiescodes op de twee regels worden op verschillende manieren ingevuld, zoals voor de twee verschillende typen verkoop respectievelijk wordt beschreven. Zie voor meer informatie het gedeelte Combinatiescenario's in [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a>Onderdelen picken in geavanceerde magazijnconfiguraties
In geavanceerde magazijnconfiguraties waarbij de locatie is ingesteld voor het gebruik van picken en verzending, kunt u componenten voor productie- en assemblageactiviteiten kiezen via het venster **Magazijnpick**. Zie voor meer informatie [Artikelen picken met een magazijnpick](warehouse-how-to-pick-items-for-warehouse-shipment.md).

U kunt tevens het venster **Verplaatsingsvoorstel** gebruiken voor ad hoc verplaatsing van artikelen tussen opslaglocaties, dat wil zeggen, zonder verwijzing naar een brondocument. Zie [Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md) voor meer informatie.  

Een magazijnpickdocument kan niet vanaf het begin worden gemaakt omdat een pickactiviteit altijd onderdeel is van een werkstroom, zowel bij een pull- als bij een push-scenario.  

Bij een push-scenario kan een magazijnpickdocument gemaakt worden door de actie **Magazijnpick maken** in het brondocument te selecteren, zoals een vrijgegeven assemblageorder of een magazijnverzending. Zie voor meer informatie [Artikelen picken met een magazijnpick](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Tevens kunt u bij een pull-scenario een magazijnpickdocument maken door het venster **Pickvoorstel** te gebruiken om pickverzoeken, voor zowel verzending als voor interne doeleinden, vast te stellen en vervolgens de benodigde magazijnpickdocumenten te maken.  

De volgende procedure beschrijft een pull-scenario, waarbij u onderdelen voor een vrijgegeven productieorder pickt met behulp van het venster **Werkblad Pick**. De procedure geldt ook voor assemblageorders.  

Als u een pick-verzoek wilt maken, bij zowel een pull- als een push-scenario, moeten de betreffende brondocumenten vrijgegeven worden. Voor interne doeleinden kunnen brondocumenten op de volgende manieren vrijgegeven worden.  

 |Brondocument|Vrijgavemethode|  
 |---------------------|--------------------|  
 |Productieorder|Wijzig de ordersoort in vrijgegeven productieorder.|  
 |Assemblageorder|Status wijzigen in Vrijgegeven.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Onderdelen picken op basis van het pickvoorstel  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pickvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Magazijndocumenten ophalen** en selecteer vervolgens de onderdeelregels van de vrijgegeven productieorder.  
3.  Inspecteer en sorteer de regels om een efficiënte pickronde samen te stellen en combineer ze eventueel met andere voorstelregels zodat de werknemer zo min mogelijk tijd nodig heeft.  
4.  Kies de actie **Pick maken**.  
5.  Bepaal hoe de magazijn-pickdocumenten gemaakt moeten worden en hoe de pickregels gesorteerd moeten worden door de velden in het venster **Pick maken** in te vullen.  
6.  Kies de knop **OK**.

Magazijnpickdocumenten worden nu gemaakt met een pickregel voor elk onderdeel dat voor de interne activiteit benodigd is.

Indien het gebied voor interne activiteit, zoals een productie-shopfloor, een standaardopslaglocatie heeft voor het plaatsen van onderdelen die voor de activiteit benodigd zijn, wordt de code van deze opslaglocatie ingevoerd in de Plaatsen-regels in het magazijnpickdocument, zodat de magazijnmedewerkers weten waar de artikelen geplaatst moeten worden. Zie [Standaard magazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) voor meer informatie.

## <a name="filling-the-consumption-bin"></a>De verbruiksopslaglocatie vullen
In dit stroomdiagram wordt weergegeven hoe het veld **Opslaglocatie** op de productieordercomponentregels wordt ingevuld op basis van uw locatie-instellingen.

![Diagram van opslaglocatiestroom](media/binflow.png "Opslaglocatiestroom")

## <a name="see-also"></a>Zie ook
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

