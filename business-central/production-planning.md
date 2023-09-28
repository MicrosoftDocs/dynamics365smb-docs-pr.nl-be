---
title: Voorraadplanning
description: Bereid een gedetailleerd uitvoerbaar plan en het productieschema van de eindmontage voor verkoop- en productievraag voor.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.for: '291, 292, 293, 295, 517, 9010, 9038'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Planning

De productiebewerkingen die vereist zijn om input om te zetten in gereed product, moeten per dag of per week worden gepland afhankelijk van het volume en de aard van de producten. [!INCLUDE[prod_short](includes/prod_short.md)] bevat functies voor de verwachte en werkelijke vraag van verkoop, montage en productie, en functies voor distributieplanning met SKU's en transfers.

> [!NOTE]
> Dit onderwerp heeft hoofdzakelijk betrekking op de planning voor bedrijven die zich bezighouden met productie- of assemblagebeheer waar resulterende aanvulorders productie-, assemblage-, transfer- en inkooporders zijn. De belangrijkste interface voor dit planningswerk is de pagina **Planningsvoorstel**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt ook voorraadplanning voor de groothandel, waar de resulterende aanvulorders alleen transfer- en inkooporders kunnen zijn. De belangrijkste interface voor dit planningswerk is de pagina **Inkoopvoorstel**, die indirect in dit onderwerp wordt beschreven aangezien de meeste planningsfunctionaliteiten op beide voorstellen van toepassing zijn.

Planning kan worden beschouwd als de voorbereiding van vereiste aanvulorders in de inkoop-, assemblage- of productieafdelingen om te voldoen aan verkoop of vraag naar eindartikelen. Zie voor meer informatie [Inkoop](purchasing-manage-purchasing.md), [Assemblagebeheer](assembly-assemble-items.md) en [Productie](production-manage-manufacturing.md).

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Een korte inleiding krijgen over de wijze waarop het planningssysteem kan worden gebruikt voor het inschatten van de vraag en het maken van een gebalanceerd leveringsplan.|[Informatie over het plannen van functionaliteit](production-about-planning-functionality.md)|
|Begrijpen hoe alle aspecten van het planningssysteem werken en hoe de algoritmen kunnen worden aangepast om te voldoen aan planningsvereisten in verschillende omgevingen.|[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)|
|Leren hoe met de planninglogica onderscheid wordt gemaakt tussen de vraag bij vestigingen volgens de SKU-instellingen en de vraag zonder vestigingscodes.|[Planning met of zonder vestigingen](production-planning-with-without-locations.md)|
|Vraag aan de hand van verwachte verkoop- en productiecomponenten voorspellen.|[Een vraagprognose maken](production-how-to-create-a-forecast.md)|  
|Een-op-een-productieorders of projectproductieorders maken vanuit een verkooporder voor de exacte vraag van die verkooporder.|[Productieorders maken op basis van verkooporders](production-how-to-create-production-orders-from-sales-orders.md)|
|De pagina **Orderplanning** gebruiken om een handmatige planning te maken voor de verkoop- of productievraag, voor één productiestuklijstniveau tegelijk.|[Nieuwe vraag order voor order plannen](production-how-to-plan-for-new-demand.md)|
|De pagina **Planningsvoorstel** gebruiken om de MPS- en MRP-opties uit te voeren om automatisch een leveringsplan op hoog niveau of een gedetailleerd leveringsplan op alle artikelniveaus te maken.|[Volledige planning, MPS of MRP uitvoeren](production-how-to-run-mps-and-mrp.md)|
|Gebruik de pagina **Inkoopvoorstel** om automatisch een gedetailleerd leveringsplan te maken voor artikelen die alleen worden aangevuld door inkopen of transfers.|[Inkoopvoorstel](production-about-planning-functionality.md#requisition-worksheet)|  
|Een productieorder starten of bijwerken als ruw geplande bewerkingen in het hoofdproductieschema.|[Productieorders direct opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md)|
|Afdelings- of bewerkingsplaatsagenda's opnieuw berekenen wegens planningswijzigingen.|[Een afdelingsagenda berekenen](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|De ordervraag (getraceerd aantal), prognose , raamverkooporder of planningparameter (niet-getraceerd aantal) traceren die een planningregel heeft doen stijgen.|[Relaties tussen vraag en aanbod bijhouden](production-how-track-demand-supply.md)|
|De geplande beschikbare voorraad voor een artikel bekijken in verschillende weergaven en nagaan welke brutobehoeften, geplande ontvangsten en andere gebeurtenissen hierop in de loop van de tijd van invloed zijn.|[Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)|  
<!--|Geselecteerde planningsactiviteiten, zoals het wijzigen of toevoegen van planningsvoorstelregels, in een grafische weergave van de toeleveringsketen uitvoeren.|[Planningsuggesties in een grafische weergave wijzigen](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|-->

## Zie ook

[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)  
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
