---
title: Inleiding tot de demogegevens voor Contoso Coffee
description: Overzicht van scenario's voor hoe Contoso Coffee-demogegevens u kunnen helpen bij het leren gebruiken van de mogelijkheden in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# Inleiding tot de demogegevens voor Contoso Coffee

Contoso Coffee is een fictief bedrijf dat koffiezetapparaten voor consumenten en bedrijven maakt. De apps **Contoso Coffee** voor Business Central voegen demogegevens toe die u kunt gebruiken om te leren hoe u de productiemogelijkheden in Business Central kunt benutten.  


## Gegevens voor Contoso Coffee instellen

Als u de demogegevens voor Contoso Coffee wilt gebruiken, moet u twee apps in het desbetreffende bedrijf in [!INCLUDE [prod_short](../includes/prod_short.md)] installeren:  

- **Gegevensset voor demo van Contoso Coffee**  

    Deze app levert demogegevens voor de basistoepassing.  
- **Gegevensset voor demo van Contoso Coffee (land-id)**  

    Deze app voegt landspecifieke inhoud toe bovenop de basistoepassing.

Voeg de apps toe aan een leeg bedrijf in een betaald abonnement of als onderdeel van een proefperiode. Maak bijvoorbeeld een nieuw bedrijf zonder voorbeeldgegevens op basis van de begeleide instelling **Nieuw bedrijf maken** die u kunt openen vanuit de lijst **Bedrijven**. Voeg vervolgens de apps toe vanuit de [marktplaats](../ui-extensions-install-uninstall.md#install) als deze nog niet in de lijst op de pagina **Extensiebeheer** voorkomen.  

U moet dan het volgende invullen:
 - De [Productie-instellingen](manufacturing/contoso-coffee-manufacturing-intro.md) ter voorbereiding op het gebruik van de [Productiescenario's](#manufacturing-scenarios)
 - De [Magazijninstellingen](warehousing/contoso-coffee-warehousing-intro.md) ter voorbereiding op het gebruik van de [Magazijnscenario's](#warehousing-scenarios)

## Productiescenario's

De demogegevens voor Contoso Coffee ondersteunen momenteel de volgende productiescenario's voor testen en trainen:

1. [Een nieuwe productiestuklijst en stuklijstversie maken](manufacturing/create-new-production-bom-version.md)  
2. [Een nieuw bewerkingsplan maken](manufacturing/create-new-routing.md)  
3. [Een nieuwe vast geplande productieorder maken en deze wijzigen](manufacturing/create-firm-planned-production-order-change.md)  
4. [Automatisch en handmatig afboeken combineren](manufacturing/combine-automatic-manual-flushing.md)  
5. [Orderplanning gebruiken om voorraad te maken en te reserveren](manufacturing/order-planning-create-reserve-supply.md)  
6. [Een uitbestedingsbewerkinge instellen en verwerken](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Nieuwe capaciteit instellen](manufacturing/set-up-new-capacity.md)  
8. [Vraag voorspellen voor artikelvarianten met verschillende toegewezen stuklijsten](manufacturing/variants.md)  

Lees de stappen voor elk scenario in het desbetreffende artikel.  

> [!IMPORTANT]
> De productieprocedures vereisen dat de gebruikerservaring is ingesteld op *Premium* op de pagina **Bedrijfsgegevens**.

## Magazijnscenario's

De demogegevens voor Contoso Coffee ondersteunen momenteel de volgende magazijnscenario's voor testen en trainen:

1.  Standaardopslaglocaties configureren, ontvangen en wegzetten met voorraadopslag, picken en verzenden met voorraadpicken op order-voor-order-wijze met [Doorlopen van de inkomende en uitgaande stroom in basismagazijnconfiguraties](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Meerdere inkomende bestellingen tegelijk ontvangen en wegzetten met magazijnontvangst, meerdere bestellingen tegelijk verzenden met magazijnverzending, picken met magazijnpicks met [Doorloop van inkomende en uitgaande stroom in gemengde magazijnconfiguraties](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Configureer vaste opslaglocaties voor de maateenheid van artikelen, cross-docking door gebruikers om fysieke verplaatsingen van goederen te verminderen, optimaliseer het plaatsen van goederen met het aanvullen van opslaglocaties, verdeel grote maateenheden in kleinere, verdeel het picken onder magazijnmedewerkers met een pickwerkblad met [Doorloop van inkomende en uitgaande stroom in gemengde magazijnconfiguraties](warehousing/warehouse-directed-flow.md)

Lees de stappen voor elk scenario in het desbetreffende artikel.
   
## Zie ook

[Productie](../production-manage-manufacturing.md)  
[Magazijn](../warehouse-manage-warehouse.md)  

