---
title: 'Ontwerpdetails: Maximum aantal | Microsoft Docs'
description: Het beleid Maximum aantal is een manier om voorraad bij te houden met behulp van een bestelpunt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 857a01bac28d85a35668f3aa01e8807a6f6dc845
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "936659"
---
# <a name="design-details-maximum-qty"></a>Ontwerpdetails: Maximaal aantal
Het beleid Maximum aantal is een manier om voorraad bij te houden met behulp van een bestelpunt.  

 Alles over het beleid voor een vast bestelaantal geldt ook voor dit beleid. Het enige verschil is de hoeveelheid van de voorgestelde voorziening. Wanneer het beleid voor maximaal aantal wordt gebruikt, wordt het bestelaantal dynamisch bepaald op basis van het geplande voorraadniveau en verschilt daarom gewoonlijk per order.  

## <a name="calculated-per-time-bucket"></a>Berekend per tijdsinterval  
 Het bestelaantal wordt bepaald op het moment (het einde van het tijdsinterval) dat het planningssysteem detecteert dat het bestelpunt is overschreden. Op dit moment meet het systeem het verschil tussen het huidige geplande voorraadniveau en de opgegeven maximale voorraad. Dit vormt het aantal dat opnieuw moet worden besteld. Het systeem controleert vervolgens of de voorziening al elders is besteld voor ontvangst binnen de doorlooptijd. Als dit het geval is, wordt het aantal van de nieuwe voorzieningenorder verminderd met de reeds bestelde aantallen.  

 Het systeem zorgt dat de geplande voorraad ten minste het bestelpuntniveau bereikt, voor het geval dat de gebruiker is vergeten een maximaal voorraadaantal op te geven.  

## <a name="combines-with-order-modifiers"></a>Combineert met orderaanpassingsfuncties  
 Afhankelijk van de instellingen kan het het beste zijn om het maximale aantal-beleid te combineren met orderwijzigingen om een minimaal orderaantal te garanderen of af te ronden op een geheel aantal inkoopeenheden, of te splitsen in meerdere lots zoals bepaald door het maximale orderaantal.  

## <a name="combines-with-calendars"></a>Combineert met agenda's  
 Voordat het planningssysteem een nieuwe voorzieningenorder voorstelt, wordt gecontroleerd of de order is gepland voor een niet-werkdag, volgens agenda's die zijn gedefinieerd in het veld **Basisagendacode** op de pagina's **Bedrijfsgegevens** en **Vestiging**.  

 Als de verwachte datum een vrije dag is, verplaatst het planningssysteem de order voorwaarts naar de dichtstbijzijnde werkdatum. Dit kan resulteren in een order die voldoet een bestelpunt maar aan een bepaalde vraag niet voldoet. Voor dergelijke vraag in onbalans maakt het systeem een extra voorziening.  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md)   
 [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
 [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
 [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
