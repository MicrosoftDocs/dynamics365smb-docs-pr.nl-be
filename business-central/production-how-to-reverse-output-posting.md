---
title: Outputboeking tegenboeken | Microsoft Docs
description: Het kan voorkomen dat een outputboeking moet worden tegengeboekt. Dit is bijvoorbeeld het geval als er een gegevensinvoerfout is gemaakt en er een onjuiste hoeveelheid output is geboekt op een productieorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 33be858c687381a50f42d1c59ca735358f113d72
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788762"
---
# <a name="reverse-output-posting"></a>Outputboeking tegenboeken
Het kan voorkomen dat een outputboeking moet worden tegengeboekt. Dit is bijvoorbeeld het geval als er een gegevensinvoerfout is gemaakt en er een onjuiste hoeveelheid output is geboekt op een productieorder.  

## <a name="to-reverse-an-output-posting"></a>Een outputboeking tegenboeken  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies de desbetreffende koppeling. Selecteer uw batch.  
2. Vul de benodigde velden in. Zie voor meer informatie [Output en bewerkingstijd in batches boeken](production-how-to-post-output-quantity.md).
3.  Selecteer in het veld **Vereffenen met post** de bijbehorende artikelpost. Hiermee voert u een tegenboeking uit van de capaciteit en artikelposten.  
4. Boek de tegenboeking door het dagboek te boeken.  

De posten van het outputdagboek worden als positieve herwaardering geboekt op de artikelposten.  

## <a name="see-also"></a>Zie ook  
 [Productie](production-manage-manufacturing.md)    
 [Productie instellen](production-configure-production-processes.md)  
 [Gepland](production-planning.md)      
 [Voorraad](inventory-manage-inventory.md)  
 [Inkoop](purchasing-manage-purchasing.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
