---
title: Plannen van magazijnverplaatsingen in werkbladen | Microsoft Docs
description: Met de functie voor de opslaglocatieaanvulling kunt u verplaatsingen plannen in het voorstel. U kunt de regels die u wilt instellen als verplaatsingsinstructies echter ook handmatig plannen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 28c76ad47fe42e9e506869816dced0c4e1194d6d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313916"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Plannen van magazijnverplaatsingen in werkbladen
Met de functie voor de opslaglocatieaanvulling kunt u verplaatsingen plannen in het voorstel. U kunt de regels die u wilt instellen als verplaatsingsinstructies echter ook handmatig plannen.  

## <a name="to-calculate-a-replenishment-movement"></a>U kunt als volgt aanvullingsverplaatsingen berekenen  
Naarmate meer artikelen worden verzonden naar klanten, bevatten de opslaglocaties met de hoogste classificatie steeds minder artikelen. Als u deze opslaglocaties met de hoogste classificatie wilt vullen, voert u de functie **Opslagloc.-aanvulling berekenen** uit op de pagina **Verplaatsingsvoorstel**

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verplaatsingsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Opslaglocatieaanvulling berekenen**.  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] maakt regels die precies aangeven hoe u artikelen moet verplaatsen van laag- naar hooggeclassificeerde opslaglocaties.  

    > [!NOTE]  
    >  Een verplaatsing volgens FEFO wordt voorgesteld wanneer u de functie **Verplaatsing maken** activeert indien voor een artikel aan de de volgende voorwaarden wordt voldaan:  
    >   
    >  -   Het artikel heeft een vervaldatum.  
    > -   Op de vestigingskaart is het selectievakje **Picken volgens FEFO** ingeschakeld.  
    > -   Het selectievakje op de vestigingskaart **Opslaglocatie verplicht** is ingeschakeld.  
    > -   De velden **Van zone** en **Van opslaglocatie** zijn leeg.  

    Zie voor meer informatie [Picken op basis van FEFO](warehouse-picking-by-fefo.md).  

3.  Bekijk en wijzig de regels indien nodig. U kunt ook regels verwijderen als er onvoldoende tijd is om alle regels uit te voeren.  
4.  Kies de actie **Verplaatsing maken** om een instructie te maken voor de medewerkers in het magazijn.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>U kunt de volledige inhoud van een of meer opslaglocaties verplaatsen met de functie Opslaglocatie-inhoud ophalen  
Met het verplaatsingsvoorstel kunt u ook andere verplaatsingen van magazijnartikelen uitvoeren. Als u bijvoorbeeld artikelen in een opslaglocatie wilt plaatsen voor kwaliteitscontrole, kunt u deze actie met het voorstel plannen en vervolgens een verplaatsing maken met instructies voor een werknemer.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verplaatsingsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Opslaglocatie-inhoud ophalen**. Gebruik de aanvraagpagina om te filteren op de opslaglocaties en artikelen die op de verplaatsingsvoorstelregels moeten verschijnen.  
3.  Vul de relevante velden op de aanvraagpagina voor de batchverwerking in. Als u bijvoorbeeld de opslaglocatie-inhoud van alle opslaglocaties in een bepaalde zone van de vestiging wilt weergeven, vult u het veld **Zone** in. Als u regels wilt ophalen voor elke opslaglocatie met een bepaald artikel, vult u het veld **Artikelnr.** in.  

    > [!NOTE]  
    >  U kunt artikelen niet handmatig van of naar een opslaglocatie van het soort Ontvangen verplaatsen, omdat artikelen in een dergelijke opslaglocatie moeten worden geregistreerd als opgeslagen voordat ze deel uitmaken van de beschikbare voorraad.  

4.  Als u een groot aantal regels ophaalt, klikt u op **Sorteren** om een sortering te selecteren voor de regels in het voorstel. Klik vervolgens op **OK**.  

    > [!NOTE]  
    >  Verplaatsingsregels worden opgehaald volgens FEFO wanneer u de functie **Opslaglocatie-inhoud ophalen** activeert indien voor een artikel aan de volgende voorwaarden wordt voldaan:  
    >   
    >  -   Het artikel heeft een vervaldatum.  
    > -   Op de vestigingskaart is het selectievakje **Picken volgens FEFO** ingeschakeld.  
    > -   Het selectievakje op de vestigingskaart **Opslaglocatie verplicht** is ingeschakeld.  
    > -   De velden **Van zone** en **Van opslaglocatie** zijn leeg.  

5.  Maak de gewenste wijzigingen in een aantal van de opgehaalde regels. U moet voor elk te verplaatsen artikel de velden **Artikelnr.**, **Van opslaglocatie**, **Naar opslaglocatie** en **Aantal** invullen.  
6.  Verwijder de onvolledige regels waaruit u de informatie hebt overgenomen.  
7.  Wanneer u in de verplaatsingsvoorstelregels precies hebt aangegeven hoe de verplaatsing moet worden uitgevoerd door de magazijnmedewerker, kiest u de actie **Verplaatsing maken** om de instructies voor de werknemer te maken.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
