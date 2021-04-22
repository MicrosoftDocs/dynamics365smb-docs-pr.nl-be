---
title: Projectorders plannen | Microsoft Docs
description: Deze planningstaak wordt gestart vanaf een verkooporder en gebruikt de pagina **Verkooporderplanning**. Wanneer u eenmaal een projectproductieorder hebt gemaakt, kunt u deze verder plannen op de pagina **Orderplanning**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 28568cd8ab7751e15bf24acd3c727828bba9f76c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787964"
---
# <a name="plan-project-orders"></a>Projectorders plannen
Deze planningstaak wordt gestart vanaf een verkooporder en gebruikt de pagina **Verkooporderplanning**. Wanneer u eenmaal een projectproductieorder hebt gemaakt, kunt u deze verder plannen op de pagina **Orderplanning**.  

## <a name="to-create-a-project-production-order"></a>Een projectproductieorder maken  

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.  
2.  Selecteer de verkooporder die het productieproject vertegenwoordigt en kies de actie **Planning**.  
4.  Kies op de pagina **Verkooporderplanning** de actie **Prod.-order maken**.  
5.  Selecteer op de pagina **Prod.order voor verkooporder maken** de optie **Projectorder** in het veld **Ordersoort**.  
6.  Kies de knop **Ja**.  
7.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productieorder** in en kies de gerelateerde koppeling.
8. Open de zojuist gemaakte productieorder.  

    Het veld **Bronsoort** van de productieorder bevat **Verkoopkop** en de order heeft meerdere regels (één voor elk verkoopregelartikel dat moet worden geproduceerd).  
9. Kies de actie **Planning**.
10. Op de pagina **Orderplanning** kiest u de actie **Vernieuwen** om nieuwe vraag te berekenen.  

De orderkopregel voor de projectorder wordt weergegeven met daaronder alle uitgevouwen regels met vraag waaraan niet is voldaan. Hoewel de productieorder regels bevat voor verschillende geproduceerde artikelen, wordt de totale vraag voor alle productieorderregels onder één orderkopregel op de pagina **Orderplanning** vermeld, samen met de oorspronkelijke klantnaam. U kunt nu doorgaan met de planning van regels zoals beschreven in [Nieuwe vraag order voor order plannen](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Vraagregels in de projectproductieorder die een **Prod.-order** hebben in het veld **Aanvullingsmethode**, vertegenwoordigen onderliggende productieorders. Nadat u deze productieorders hebt gemaakt, moet u opnieuw een plan berekenen op de pagina **Orderplanning** om de eventuele niet-afgehandelde vraag naar deze materialen te bepalen. In dat geval worden deze als vraagregels onder een normale productieorderkopregel weergegeven, wat betekent dat de projectrelatie niet langer zichtbaar is op de pagina. Wanneer u echter ordertracering gebruikt, kunt u vooruit- en terugkijken naar alle orders voor voorzieningen die onder de oorspronkelijke verkooporder zijn gemaakt  

## <a name="see-also"></a>Zie ook
[Gepland](production-planning.md)   
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]