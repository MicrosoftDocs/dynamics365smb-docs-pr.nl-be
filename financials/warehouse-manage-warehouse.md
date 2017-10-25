---
title: Magazijnactiviteiten | Microsoft Docs
description: Nadat goederen zijn ontvangen en voordat goederen worden verzonden, vindt een aantal interne magazijnactiviteiten plaats om een effectieve doorloop in het magazijn te waarborgen en om bedrijfsvoorraden te organiseren en bij te houden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c1ea1c4a5ea4b917243d60981ec35050895f82a7
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="warehouse-management"></a>Magazijnbeheer
Nadat goederen zijn ontvangen en voordat goederen worden verzonden, vindt een aantal interne magazijnactiviteiten plaats om een effectieve doorloop in het magazijn te waarborgen en om bedrijfsvoorraden te organiseren en bij te houden.

Gebruikelijke magazijnactiviteiten zijn onder andere het in opslag brengen van artikelen, artikelen binnen of tussen magazijnen verplaatsen en artikelen picken voor assemblage, productie of verzending. Het assembleren van artikelen voor verkoop of voorraad kan ook als magazijnactiviteit worden beschouwd, maar dit wordt al ergens anders besproken. Zie voor meer informatie [Assemblagebeheer](assembly-assemble-items.md).  

In grote magazijnen kunnen deze verschillende afhandelingstaken door verschillende afdelingen worden uitgevoerd en kan de integratie worden beheerd door een gestuurde werkstroom. In eenvoudigere installaties is de stroom minder geformaliseerd en worden de magazijnactiviteiten uitgevoerd met zogeheten voorraadopslag en voorraadpicks. Zie [Ontwerpdetails: Magazijnoverzicht](design-details-warehouse-overview.md) voor meer informatie over standaard- en geavanceerde magazijnconfiguraties.

Voordat u magazijnactiviteiten kunt uitvoeren, moet u het systeem instellen voor de relevante complexiteit van magazijnverwerking. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|De ontvangst van artikelen in magazijnvestigingen registreren, alleen met een inkooporder, in eenvoudige vestigingsconfiguraties, of met een magazijnontvangst, in het geval van semi- of volledig geautomatiseerde magazijnverwerking in de vestiging.|[Procedure: Artikelen ontvangen](warehouse-how-receive-items.md)|
|De opslag- en pickprocessen omzeilen om een artikel van de ontvangst direct naar de productie of verzending door te sturen.|[Procedure: artikelen cross-docken](warehouse-how-to-cross-dock-items.md)|    
|Artikelen opslaan die uit aankopen, verkoopretouren, transport of productieoutput zijn ontvangen, volgens het geconfigureerde magazijnproces.|[Artikelen opslaan](warehouse-put-away-items.md)|
|Artikelen verplaatsen tussen opslaglocaties in het magazijn.|[Artikelen verplaatsen](warehouse-move-items.md)|
|Artikelen picken die moeten worden verzonden, getransporteerd of gebruikt in assemblage of productie, volgens het geconfigureerde magazijnproces.|[Artikelen picken](warehouse-pick-items.md)|
|De verzending van artikelen van magazijnvestigingen registreren, alleen met een verkooporder, in eenvoudige vestigingsconfiguraties, of met een magazijnverzending, in het geval van semi- of volledig geautomatiseerde magazijnprocessen in de vestiging.|[Procedure: Artikelen verzenden](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Zie ook  
 [Voorraad](inventory-manage-inventory.md)  
 [Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
 [Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

