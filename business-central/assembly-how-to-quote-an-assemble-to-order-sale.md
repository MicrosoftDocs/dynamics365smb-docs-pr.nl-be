---
title: 'Procedure: een offerte maken voor een op-order-assembleren-verkoop | Microsoft Docs'
description: U kunt assemblagebeheer gebruiken om een assemblageartikel op verzoek van een klant aan te passen tijdens het verkoopproces.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 323466061d845e04a38ba660b38dd21483bcb8c1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749605"
---
# <a name="quote-an-assemble-to-order-sale"></a>Een offerte maken voor een assembleren voor order-verkoop
U kunt assemblagebeheer gebruiken om een assemblageartikel op verzoek van een klant aan te passen tijdens het verkoopproces. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).  

Als u een ander soort artikel verkoopt, kunt u ook een verkoopofferte maken voor een aangepast assemblageartikel voordat u deze omzet in een verkooporder. Dit proces omvat verschillende extra stappen wanneer u het vergelijkt met het maken van een normale verkoopofferte, en gebruikt assemblageoffertes, een variatie van een gekoppelde assemblageorder.

> [!NOTE]  
>  Zoals alle soorten van offertes worden de aantallen op assemblageoffertes niet gebruikt in beschikbaarheid, plannen of reserveringen.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Een verkoopofferte voor een op-order-assembleren-artikel maken  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopofferte** in en kies de desbetreffende koppeling.  
2.  Maak een nieuwe verkoopofferteregel met één regel voor een assemblageartikel. Zie voor meer informatie [Verkoopoffertes maken](sales-how-make-offers.md).  
3.  Voer de volledige aantal het in veld **Aantal voor op order assembleren** in.

    > [!NOTE]  
    >  U moet geen offerte maken voor een gedeeltelijke hoeveelheid. Daarom moet u dezelfde hoeveelheid invoeren die u hebt ingevoerd in het veld **Hoeveelheid** op de verkoopofferteregel.  

4.  Kies op het sneltabblad **Regels** de optie **Regel** en vervolgens **Op order assembleren** en **Op orderregels assembleren**. Of kies het veld **Aant. op order assembleren** op de regel.  
5.  Bekijk of wijzig de assemblageorderregels volgens de offerte die de klant heeft aangevraagd op de pagina **Op orderregels assembleren**. Als u meer informatie wilt, kiest u de actie **Document weergeven** om het volledige offerteraamcontract te openen. U kunt de inhoud van de meeste velden niet wijzigen en u kunt niet boeken.  
6.  Wanneer u de assemblageorderregels hebt bijgewerkt volgens de offerte sluit u de pagina **Op orderregels assembleren** om terug te keren naar de pagina **Verkoopofferte**.  
7.  Als de klant de offerte heeft geaccepteerd, maakt u een verkooporder voor het genoteerde assemblageartikel. Zie voor meer informatie [Verkoopoffertes maken](sales-how-make-offers.md). De gekoppelde assemblageofferte en eventuele aanpassingen zijn gekoppeld aan die nieuwe verkooporder, als voorbereiding op de assemblage van het artikel of de artikelen die verkocht worden.  

## <a name="see-also"></a>Zie ook  
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met stuklijsten](inventory-how-work-BOMs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]