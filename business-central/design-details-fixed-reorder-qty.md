---
title: 'Ontwerpdetails: Vast bestelaantal | Microsoft Docs'
description: Het beleid Vast bestelaantal is gerelateerd aan de voorraadplanning van typische C-producten (lage voorraadkosten, laag verouderingsrisico en/of veel artikelen). Dit beleid wordt gewoonlijk gebruikt in relatie met een bestelpunt met de verwachte vraag tijdens de doorlooptijd van het artikel.
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
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5084c8a49972ea51600867d90acedc2698609732
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-fixed-reorder-qty"></a>Ontwerpdetails: Vast bestelaantal
Het beleid Vast bestelaantal is gerelateerd aan de voorraadplanning van typische C-producten (lage voorraadkosten, laag verouderingsrisico en/of veel artikelen). Dit beleid wordt gewoonlijk gebruikt in relatie met een bestelpunt met de verwachte vraag tijdens de doorlooptijd van het artikel.  

## <a name="calculated-per-time-bucket"></a>Berekend per tijdsinterval  
 Als het planningssysteem ontdekt dat het bestelpunt in een bepaald tijdsinterval (bestelfrequentie) is bereikt of overschreden - boven of op het bestelpunt aan het begin van de periode en onder of op het bestelpunt aan het einde van de periode - wordt voorgesteld een nieuwe voorzieningenorder voor het opgegeven bestelaantal te maken en deze voorwaarts te plannen vanaf de eerste datum na het einde van het tijdsinterval.  

 Door bestelpunten in combinatie met tijdsintervallen te gebruiken, wordt het aantal voorzieningsvoorstellen verminderd. Dit geeft een handmatig proces aan van het frequent door het magazijn lopen om de werkelijke inhoud in de verschillende opslaglocaties te controleren.  

## <a name="creates-only-necessary-supply"></a>Maakt alleen benodigde voorzieningen  
 Voordat een nieuwe voorzieningenorder wordt voorgesteld om aan een bestelpunt te voldoen, controleert het planningssysteem of al voorziening is besteld voor ontvangst binnen de doorlooptijd van het artikel. Als een bestaande voorzieningenorder het probleem oplost door de geplande voorraad binnen de looptijd op of boven het bestelpunt te brengen, stelt het systeem geen nieuwe voorzieningenorder voor.  

 Orders voor voorzieningen die specifiek zijn gemaakt om te voldoen aan een bestelpunt, worden uitgesloten van de normale afstemming van voorzieningen en kunnen op geen enkele manier achteraf worden gewijzigd. Dus als een artikel dat het bestelpunt gebruikt, moet worden uitgefaseerd (niet aangevuld), is het raadzaam openstaande orders voor voorzieningen handmatig te controleren of het bestelbeleid te wijzigen in lot-voor-lot, waarbij het systeem overbodige voorzieningen reduceert of annuleert.  

## <a name="combines-with-order-modifiers"></a>Combineert met orderaanpassingsfuncties  
 De ordervelden Min. bestelaantal, Max. bestelaantal en Vaste lotgrootte zouden geen grote rol moeten afspelen wanneer het beleid voor vaste bestelaantallen wordt gebruikt. Het planningssysteem houdt echter toch rekening met deze wijzigingsfactoren en verlaagt het aantal tot het opgegeven maximum orderaantal (en maakt twee of meer voorzieningen om het totale orderaantal te bereiken), verhoogt de order tot het opgegeven maximum aantal of rondt het orderaantal af op een opgegeven orderveelvoud.  

## <a name="combines-with-calendars"></a>Combineert met agenda's  
 Voordat het planningssysteem een nieuwe voorzieningenorder voorstelt, wordt gecontroleerd of de order is gepland voor een niet-werkdag, volgens agenda's die zijn gedefinieerd in het veld **Basisagendacode** in de vensters **Bedrijfsgegevens** en **Vestiging**.  

 Als de verwachte datum een vrije dag is, verplaatst het planningssysteem de order voorwaarts naar de dichtstbijzijnde werkdatum. Dit kan resulteren in een order die voldoet een bestelpunt maar aan een bepaalde vraag niet voldoet. Voor dergelijke vraag in onbalans maakt het systeem een extra voorziening.  

## <a name="should-not-be-used-with-forecast"></a>Moet niet worden gebruikt met prognose  
 Omdat de verwachte vraag al is uitgedrukt in het bestelpuntniveau, is het niet nodig een prognose in de planning van een artikel op te nemen met behulp van een bestelpunt. Als het belangrijk is dat de planning op een prognose wordt gebaseerd, gebruikt u het lot-voor-lot beleid.  

## <a name="must-not-be-used-with-reservations"></a>Mag niet met reserveringen worden gebruikt  
 Als de gebruiker een aantal heeft gereserveerd, bijvoorbeeld een aantal in voorraad, voor een of andere toekomstige vraag, wordt de basis van de planning verstoord. Zelfs als de geplande voorraad met betrekking tot het bestelpunt aanvaardbaar is, zijn de hoeveelheden mogelijk niet beschikbaar. Het systeem probeert dit mogelijk te compenseren door uitzonderingsorders aan te maken. Het wordt echter aangeraden het veld Reserveren in te stellen op Nooit voor artikelen die worden gepland met behulp van een bestelpunt.  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md)   
 [Ontwerpdetails: Maximaal aantal](design-details-maximum-qty.md)   
 [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
 [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
 [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)

