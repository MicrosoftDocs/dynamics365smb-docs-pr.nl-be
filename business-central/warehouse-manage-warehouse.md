---
title: Magazijnactiviteiten beheren
description: Nadat goederen zijn ontvangen en voordat goederen worden verzonden, vindt een aantal interne magazijnactiviteiten plaats om een effectieve doorloop in het magazijn te waarborgen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5774, 5776, 5777, 5785, 5793, 5797, 7318, 7364, 7401, 8909, 9000, 9008, 9009, 9050, 9053, 9056
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: c08331889a0a94e8760b8104b8d5769ea5d0edbf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529797"
---
# <a name="warehouse-management"></a>Magazijnbeheer

Nadat goederen zijn ontvangen en voordat goederen worden verzonden, vindt een aantal interne magazijnactiviteiten plaats om een effectieve doorloop in het magazijn te waarborgen en om bedrijfsvoorraden te organiseren en bij te houden.

Gebruikelijke magazijnactiviteiten zijn onder andere het in opslag brengen van artikelen, artikelen binnen of tussen magazijnen verplaatsen en artikelen picken voor assemblage, productie of verzending. Het assembleren van artikelen voor verkoop of voorraad kan ook als magazijnactiviteit worden beschouwd, maar dit wordt al ergens anders besproken. Zie voor meer informatie [Assemblagebeheer](assembly-assemble-items.md).  

In grote magazijnen kunnen deze verschillende afhandelingstaken door verschillende afdelingen worden uitgevoerd en kan de integratie worden beheerd door een gestuurde werkstroom. In eenvoudigere installaties is de stroom minder geformaliseerd en worden de magazijnactiviteiten uitgevoerd met zogeheten voorraadopslag en voorraadpicks. Zie [Ontwerpdetails: Magazijnoverzicht](design-details-warehouse-overview.md) voor meer informatie over standaard- en geavanceerde magazijnconfiguraties.

Voordat u magazijnactiviteiten kunt uitvoeren, moet u het systeem instellen voor de relevante complexiteit van magazijnverwerking. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

De voorraadtaken tellen, aanpassen en herindelen van artikelen kunnen magazijntaken omvatten die op magazijnposten moeten worden uitgevoerd voordat ze kunnen worden gesynchroniseerd met de gerelateerde artikelposten. Zie voor meer informatie [Voorraad tellen, corrigeren en herindelen](inventory-how-count-adjust-reclassify.md).

 De volgende tabel beschrijft een reeks taken, met koppelingen naar de onderwerpen waarin deze worden beschreven.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|De ontvangst (inclusief meerontvangst) van artikelen in magazijnvestigingen registreren, alleen met een inkooporder, in eenvoudige vestigingsconfiguraties, of met een magazijnontvangst, in het geval van semi- of volledig geautomatiseerde magazijnverwerking in de vestiging.|[Artikelen ontvangen](warehouse-how-receive-items.md)|
|De opslag- en pickprocessen omzeilen om een artikel van de ontvangst direct naar de productie of verzending door te sturen.|[Artikelen cross-docken](warehouse-how-to-cross-dock-items.md)|
|Artikelen opslaan die uit aankopen, verkoopretouren, transport of productieoutput zijn ontvangen, volgens het geconfigureerde magazijnproces.|[Artikelen opslaan](warehouse-put-away-items.md)|
|Artikelen verplaatsen tussen opslaglocaties in het magazijn.|[Artikelen verplaatsen](warehouse-move-items.md)|
|Artikelen picken die moeten worden verzonden, getransporteerd of gebruikt in assemblage of productie, volgens het geconfigureerde magazijnproces.|[Artikelen picken](warehouse-pick-items.md)|
|De verzending van artikelen van magazijnvestigingen registreren, alleen met een verkooporder, in eenvoudige vestigingsconfiguraties, of met een magazijnverzending, in het geval van semi- of volledig geautomatiseerde magazijnprocessen in de vestiging.|[Artikelen verzenden](warehouse-how-ship-items.md)|  

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Zie ook

[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
