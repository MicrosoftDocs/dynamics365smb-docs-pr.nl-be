---
title: Aanbevolen procedures voor instellen van algemene planning | Microsoft Docs
description: Het sneltabblad Planning op de pagina Productie-instellingen bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# Aanbevolen procedures instellen: Instellen algemene planning
Het sneltabblad **Planning** op de pagina **Productie-instellingen** bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren.  

 De volgende tabel bevat de aanbevolen procedures voor het instellen van de geselecteerde globale planningparametervelden. Voor meer informatie over een veld, kiest u de koppeling in de kolom **Veld instellen**.  

|Veld instellen|Aanbevolen procedure|Opmerking|  
|-----------------|-------------------|-------------|  
|Prognose op vestigingen gebruiken|Selecteer als u prognoses hebt voor specifieke locaties.||  
|Onderdelen op vestiging|Als artikelen niet als SKU's zijn gedefinieerd, selecteert u de vestigingscode van het hoofdmagazijn.|Dit geldt ook als u alleen het inkoopvoorstel gebruikt.|  
|Blanco-overflowniveau|Selecteer **Standaardberekening toestaan** als u migreert van Microsoft Dynamics NAV 5.0 of eerder.|Alleen gebruiken als u toestaat dat alle of sommige van uw objecten het bestelpunt overschrijden.|  
|Standaard dempingsperiode|Ingesteld tussen 1D en 5D.<br /><br /> Indien planning in [!INCLUDE[prod_short](includes/prod_short.md)] nieuw is voor u stelt u een langere periode in.|Wanneer gebruikers meer vertrouwd zijn met de verschillende redenen voor planningsboodschappen, kort dan de dempingsperiode in om meer wijzigingssuggesties toe te staan.|  
|Demping standaardhoeveelheid %|Tussen 5 en 20 procent van de lotgrootte van het item instellen.||  

## Zie ook  
 [Aanbevolen procedures instellen: Voorraadplanning](setup-best-practices-supply-planning.md)   
 [Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
 [Complexe toepassingsgebieden instellen met aanbevolen procedures](set-up-complex-application-areas-using-best-practices.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]