---
title: Voorraadplanning | Microsoft Docs
description: Bereid een gedetailleerd uitvoerbaar plan en het productieschema van de eindmontage voor verkoop- en productievraag voor.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 85b5583d18042b05aea264d59ed9484dddeb4d12
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="planning"></a>Planning
De productiebewerkingen die vereist zijn om input om te zetten in gereed product, moeten per dag of per week worden gepland afhankelijk van het volume en de aard van de producten. [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat functies voor de verwachte en werkelijke vraag van verkoop, montage en productie, en functies voor distributieplanning met SKU's en transfers.

> [!NOTE]
> Dit onderwerp heeft hoofdzakelijk betrekking op de planning voor bedrijven die zich bezighouden met productie- of assemblagebeheer waar resulterende aanvulorders productie-, assemblage-, transfer- en inkooporders zijn. De belangrijkste interface voor dit planningswerk is het venster **Planningsvoorstel**.

> [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt ook voorraadplanning voor de groothandel, waar de resulterende aanvulorders alleen transfer- en inkooporders kunnen zijn. De belangrijkste interface voor dit planningswerk is het venster **Inkoopvoorstel**, dat indirect in dit onderwerp wordt beschreven aangezien de meeste planningsfunctionaliteiten op beide voorstellen van toepassing zijn.

Voordat u productieorders kunt plannen en uitvoeren, moet u de productiecapaciteiten configureren, zoals het maken van productieagenda's, productiestuklijsten en bewerkingsplaatsen. Zie [Productie instellen](production-configure-production-processes.md) voor meer informatie.

Planning kan worden beschouwd als de voorbereiding van vereiste aanvulorders in de montage- of productieafdelingen om te voldoen aan vraag. Zie [Assemblagebeheer](assembly-assemble-items.md) en [Productie](production-manage-manufacturing.md) voor meer informatie.

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Een korte inleiding krijgen over de wijze waarop het planningssysteem kan worden gebruikt voor het inschatten van de vraag en het maken van een gebalanceerd leveringsplan.|[Informatie over het plannen van functionaliteit](production-about-planning-functionality.md)|
|Begrijpen hoe alle aspecten van het planningssysteem werken en hoe de algoritmen kunnen worden aangepast om te voldoen aan planningsvereisten in verschillende omgevingen.|[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)|
|Leren hoe met de planninglogica onderscheid wordt gemaakt tussen de vraag bij vestigingen volgens de SKU-instellingen en de vraag zonder vestigingscodes.|[Planning met of zonder vestigingen](production-planning-with-without-locations.md)|
|De productievraag aan de hand van verwachte verkoop- en productieorders voorspellen.|[Een productieprognose maken](production-how-to-create-a-forecast.md)|  
|Automatisch een-op-een-productieorders maken op basis van een verkooporder voor de exacte vraag van de betreffende verkooporderregel.|[Productieorders maken op basis van verkooporders](production-how-to-create-production-orders-from-sales-orders.md)|
|Een projectproductieorder maken rechtstreeks op basis van een verkooporder met meerdere regels voor een productieproject.|[Projectorders plannen](production-how-to-plan-project-orders.md)|
|Het venster **Orderplanning** gebruiken om een handmatige planning te maken voor de verkoop- of productievraag, voor één productiestuklijstniveau tegelijk.|[Nieuwe vraag order voor order plannen](production-how-to-plan-for-new-demand.md)|
|Het venster **Planningsvoorstel** gebruiken om de MPS- en MRP-opties uit te voeren om automatisch een leveringsplan op hoog niveau of een gedetailleerd leveringsplan op alle artikelniveaus te maken.|[Volledige planning, MPS of MRP uitvoeren](production-how-to-run-mps-and-mrp.md)|
|Het inkoopvoorstel gebruiken om automatisch een gedetailleerd leveringsplan te maken voor artikelen die alleen worden aangevuld door inkopen of transfers.|De pagina **Inkoopvoorstel**|  
|Een productieorder starten of bijwerken als ruw geplande bewerkingen in het hoofdproductieschema.|[Productieorders direct opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md)|
|Afdelings- of bewerkingsplaatsagenda's opnieuw berekenen wegens planningswijzigingen.|De sectie "Een afdelingsagenda berekenen" in [Productieagenda's instellen](production-how-to-create-work-center-calendars.md)|
|De ordervraag (getraceerd aantal), prognose , raamverkooporder of planningparameter (niet-getraceerd aantal) traceren die een planningregel heeft doen stijgen.|[Relaties tussen vraag en aanbod bijhouden](production-how-track-demand-supply.md)|
|De geplande beschikbare voorraad voor een artikel bekijken in verschillende weergaven en nagaan welke brutobehoeften, geplande ontvangsten en andere gebeurtenissen hierop in de loop van de tijd van invloed zijn.|[Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)|  
|Geselecteerde planningsactiviteiten, zoals het wijzigen of toevoegen van planningsvoorstelregels, in een grafische weergave van de toeleveringsketen uitvoeren.|[Planningsuggesties in een grafische weergave wijzigen](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Zie ook
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

