---
title: Inleiding tot Contoso Coffee
description: Overzicht van scenario's voor hoe demogegevens voor Contoso Coffee u kunnen helpen bij het leren gebruiken van de magazijnbeheermogelijkheden in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Inleiding tot Contoso Coffee-magazijnbeheer

Contoso Coffee is een fictief bedrijf dat koffiezetapparaten voor consumenten en bedrijven maakt. De apps **Contoso Coffee** voor Business Central voegen demogegevens toe die u kunt gebruiken om te leren hoe u de magazijnbeheermogelijkheden in Business Central kunt benutten. U kunt magazijnbeheerfuncties op verschillende manieren configureren, zie [Overzicht van verschillende configuratieopties](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

De app biedt vier producten die zijn geoptimaliseerd voor verschillende scenario's:

- **ZILVER**  

  Deze locatie is geconfigureerd om opslaglocaties te gebruiken. Het kan eenvoudig worden geconfigureerd om basis of geavanceerd te ondersteunen. 

- **GEEL**  

  Deze locatie gebruikt de geavanceerde magazijnconfiguratie, maar geen opslaglocaties. Het kan opnieuw worden geconfigureerd om basisconfiguraties te ondersteunen.

- **WIT**  

  Deze locatie maakt gebruik van de geavanceerde magazijnconfiguratie met gestuurde opslag en picks, waardoor meer geavanceerde regels mogelijk zijn voor de manier waarop artikelen door het magazijn worden verplaatst.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Gegevens voor Contoso Coffee-magazijnbeheer instellen

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Zodra de relevante apps zijn geïnstalleerd, gaat u naar de pagina [Demohulpmiddel van Contoso](https://businesscentral.dynamics.com/?page=5194) in [!INCLUDE [prod_short](../../includes/prod_short.md)], selecteert u de regel *Magazijnmodule* en gebruikt u de actie **Configureren** om de modules voor te bereiden. In de volgende tabellen worden de instellingen beschreven:  

|Veld  |Omschrijving  |
|---------|---------|
|**Opslaglocatie van vestiging**  |De locatie die moet worden gebruikt voor de basislocatiescenario's.|
|**Vestiging geavanceerd**  |De locatie om te gebruiken voor de eenvoudige logistieke scenario's.|
|**Locatiegerichte opslag en pick**  |De locatie om te gebruiken voor geavanceerde logistieke scenario's.|
|**Locatie in transit**  |De locatie die moet worden gebruikt voor de transitlocatie in overstapscenario's.|
|**Klantnr.**  |De klant die moet worden gebruikt voor de basisscenario's en eenvoudige scenario's in verkoopactiviteiten.|
|**Leveranciersnr.**  |De leverancier die moet worden gebruikt voor alle scenario's bij inkoopactiviteiten.|
|**Nr. voor artikel 1**  |Het hoofdartikel dat voor alle scenario's moet worden gebruikt.|
|**Nr. voor artikel 2**  |Het extra artikel dat voor alle scenario's moet worden gebruikt.|
|**Nr. voor artikel 3**  |Het artikel met tracering.|

Als u gereed bent, kiest u de actie **Demogegevens maken**. Het duurt een paar minuten om de gegevens aan de onderliggende database toe te voegen, maar dan bent u klaar om de verschillende scenario's uit te voeren.  

> [!IMPORTANT]
> Als u de scenario's uitvoert, wilt u mogelijk controleren of uw gebruiker is toegevoegd zoals voor geselecteerde locaties. Zie voor meer informatie [Magazijnmedewerkers instellen](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Scenario's

De magazijndemogegevens voor Contoso Coffee ondersteunen momenteel de volgende magazijnscenario's voor testen en trainen:

1.  [Doorlopen van de inkomende en uitgaande stroom in basismagazijnconfiguraties](warehouse-basic-flow-putaway-pick.md)
2.  [Overzicht van inkomende en uitgaande stroom in gemengde magazijnconfiguraties](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Doorloop van de inkomende en uitgaande stroom in geavanceerde magazijnconfiguratie met gestuurde opslag en pick](warehouse-directed-flow.md)

Lees de stappen voor elk scenario in het desbetreffende artikel.  

## <a name="see-also"></a>Zie ook

[Voorraad instellen](../../inventory-setup-inventory.md) 
[Procedure: vestigingen instellen](../../inventory-how-setup-locations.md) 
[Magazijnbeheer](../../warehouse-manage-warehouse.md) 
[Ontwerpdetails](../../design-details-warehouse-overview.md) 
