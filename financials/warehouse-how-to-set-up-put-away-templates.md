---
title: Opslagsjablonen instellen | Microsoft Docs
description: Dankzij gestuurde opslag en pick kan op elk tijdstip de meest geschikte opslaglocatie worden gevonden. Dit gebeurt op basis van de opslagsjabloon dat u voor het magazijn hebt ingesteld, de opslaglocatievolgorde die u aan de verschillende opslaglocaties hebt toegewezen en de minimum- en maximumaantallen die u voor vaste opslaglocaties hebt ingesteld.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0316dfe2d8e601077ed67317b4a077036e0a8c33
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-put-away-templates"></a>Opslagsjablonen instellen
Dankzij gestuurde opslag en pick kan op elk tijdstip de meest geschikte opslaglocatie worden gevonden. Dit gebeurt op basis van de opslagsjabloon dat u voor het magazijn hebt ingesteld, de opslaglocatievolgorde die u aan de verschillende opslaglocaties hebt toegewezen en de minimum- en maximumaantallen die u voor vaste opslaglocaties hebt ingesteld.  

U kunt een aantal opslagsjablonen instellen en er vervolgens een van selecteren als hoofdsjabloon voor opslagactiviteiten in uw magazijn. U kunt ook een bepaalde opslagsjabloon koppelen aan een artikel of SKU waarvoor speciale opslagvereisten gelden.  

## <a name="to-set-up-put-away-templates"></a>U kunt als volgt opslagsjablonen instellen  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Opslagsjablonen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Voer een unieke id in voor de sjabloon die u wilt maken.  
4.  Typ desgewenst een korte omschrijving.  
5.  Voer op de eerste regel de opslaglocatievereisten in die u de hoogste prioriteit wilt geven bij opslagactiviteiten in het programma.  
6.  Op de tweede regel voert u de vereisten in die u van secundair belang acht bij het zoeken naar een opslaglocatie. De tweede regel wordt alleen gebruikt indien een opslaglocatie die aan de voorwaarden van de eerste regel voldoet niet kan worden gevonden.  
7.  Vul de regels in totdat u alle acceptabele plaatsingsvereisten hebt ingevoerd waaraan moet worden voldaan bij de opslag van artikelen.  
8.  Schakel het selectievakje **Vrije opslaglocatie zoeken** op de laatste regel van de opslagsjabloon in.  

U kunt verschillende opslagsjablonen maken en deze naar wens toepassen. Er wordt allereerst rekening gehouden met de opslagsjabloon die u hebt geselecteerd voor het artikel of de SKU. Als deze velden niet zijn ingevuld, wordt de opslagsjabloon gebruikt die u voor het magazijn hebt geselecteerd op het sneltabblad **Opslaglocatiebeleid** van de vestigingskaart.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

