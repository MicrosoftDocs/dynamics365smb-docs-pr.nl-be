---
title: Inleiding tot Contoso Coffee
description: Overzicht van scenario's voor hoe demogegevens voor Contoso Coffee u kunnen helpen bij het leren gebruiken van de magazijnbeheermogelijkheden in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-warehousing" />Inleiding tot Contoso Coffee-magazijnbeheer

Contoso Coffee is een fictief bedrijf dat koffiezetapparaten voor consumenten en bedrijven maakt. De apps **Contoso Coffee** voor Business Central voegen demogegevens toe die u kunt gebruiken om te leren hoe u de magazijnbeheermogelijkheden in Business Central kunt benutten. U kunt magazijnbeheerfuncties op verschillende manieren configureren, zie [Overzicht van verschillende configuratieopties](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

De app biedt vier producten die zijn geoptimaliseerd voor verschillende scenario's:

- **ZILVER**  

  Deze locatie is geconfigureerd om opslaglocaties te gebruiken. Het kan eenvoudig worden geconfigureerd om basis of geavanceerd te ondersteunen. 

- **GEEL**  

  Deze locatie gebruikt de geavanceerde magazijnconfiguratie, maar geen opslaglocaties. Het kan opnieuw worden geconfigureerd om basisconfiguraties te ondersteunen.

- **WIT**  

  Deze locatie maakt gebruik van de geavanceerde magazijnconfiguratie met gestuurde opslag en picks, waardoor meer geavanceerde regels mogelijk zijn voor de manier waarop artikelen door het magazijn worden verplaatst.

## <a name="set-up-contoso-coffee-warehousing-data" />Gegevens voor Contoso Coffee-magazijnbeheer instellen

Als u de demogegevens voor Contoso Coffee-magazijnbeheer wilt gebruiken, moet u twee apps in het desbetreffende bedrijf in [!INCLUDE [prod_short](../../includes/prod_short.md)] installeren:  

- **Gegevensset voor demo van Contoso Coffee**  

    Deze app levert demogegevens voor de basistoepassing.  
- **Gegevensset voor demo van Contoso Coffee (land-id)**  

    Deze app voegt landspecifieke inhoud toe bovenop de basistoepassing.

Voeg de apps toe aan een leeg bedrijf in een betaald abonnement of als onderdeel van een proefperiode. Maak bijvoorbeeld een nieuw bedrijf zonder voorbeeldgegevens op basis van de begeleide instelling **Nieuw bedrijf maken** die u kunt openen vanuit de lijst **Bedrijven**. Voeg vervolgens de apps toe vanuit de [marktplaats](../../ui-extensions-install-uninstall.md#install) als deze nog niet in de lijst op de pagina **Extensiebeheer** voorkomen.  

Zodra de relevante apps zijn geïnstalleerd, gaat u naar de pagina [Magazijn-demogegevens voor Contoso Coffee](https://businesscentral.dynamics.com/?page=4761) in [!INCLUDE [prod_short](../../includes/prod_short.md)] en wijzigt u de standaardinstellingen om aan uw wensen te voldoen. De volgende tabel beschrijft de instellingen:  

|Veld  |Omschrijving  |
|---------|---------|
|**Beginjaar** |Hiermee wordt het eerste jaar opgegeven dat u wilt gebruiken voor de demonstratiegegevens van Contoso Coffee. Afhankelijk van de bedrijfsconfiguratie is het jaar een kalenderjaar of een boekjaar.|
|**Opslaglocatie van vestiging**  |De locatie die moet worden gebruikt voor de basislocatiescenario's.|
|**Locatie Geavanc. logistiek**  |De locatie om te gebruiken voor de eenvoudige logistieke scenario's.|
|**Locatiegerichte opslag en pick**  |De locatie om te gebruiken voor geavanceerde logistieke scenario's.|
|**Locatie in transit**  |De locatie die moet worden gebruikt voor de transitlocatie in overstapscenario's.|
|**Klantnr.**  |De klant die moet worden gebruikt voor de basisscenario's en eenvoudige scenario's in verkoopactiviteiten.|
|**Leveranciersnr.**  |De leverancier die moet worden gebruikt voor alle scenario's bij inkoopactiviteiten.|
|**Hoofdartikelnr.**  |Het artikel dat moet worden gebruikt voor alle scenario's in verkoopbewerkingen|
|**Nr. voor artikel 1**  |Het hoofdartikel dat voor alle scenario's moet worden gebruikt.|
|**Nr. voor artikel 2**  |Het extra artikel dat voor alle scenario's moet worden gebruikt.|
|**Klantboekingsgroep**|Specificeert een bedrijfscode voor binnenlandse klanten. De bedrijfscodes worden gebruikt wanneer transacties worden geboekt. |
|**Algemene bedrijfsboekingsgroep**|Specificeert een bedrijfscode voor binnenlandse klanten. De bedrijfscodes worden gebruikt wanneer transacties worden geboekt. |
|**Leveranciersboekingsgroep**|Hiermee wordt een bedrijfscode voor binnenlandse klanten en leveranciers opgegeven. De bedrijfscodes worden gebruikt wanneer transacties worden geboekt. |
|**Leverancier - Algemene bedrijfsboekingsgroep**|Hiermee wordt een bedrijfscode voor binnenlandse klanten en leveranciers opgegeven. De bedrijfscodes worden gebruikt wanneer transacties worden geboekt. |
|**Binnenland - Btw-bedrijfsboekingsgroep**|Specificeert een btw-bedrijfscode voor klanten en leveranciers voor het boeken van btw als btw is ingeschakeld.|
|**Wederverkoop - voorraadboekingsgroep**    |Specificeert een code voor artikelen die moeten worden gebruikt voor het boeken van wederverkoop.|
|**Detailhandel - Algemene productboekingsgroep**    |Specificeert een code voor artikelen die moeten worden gebruikt voor het boeken van detailhandel.|
|**Btw-productboekingsgroep**    |Specificeert een btw-productcode voor artikelen voor het boeken van btw als btw is ingeschakeld.|
|**Prijsfactor**     |Hiermee wordt een factor opgegeven om een prijs om te rekenen van USD/EUR naar de lokale valuta. *1* betekent dat de prijs hetzelfde bedrag is in elke valuta. Er wordt een hoger getal gebruikt om de prijs in de lokale valuta weer te geven. |
|**Afrondingsprecisie**  |Hiermee wordt gedefinieerd hoe berekende verbruiksaantallen worden afgerond wanneer deze worden ingevoerd op de verbruiksdagboekregels. Aantallen van minder dan 0,5 worden naar beneden afgerond. Aantallen gelijk aan of hoger dan 0,5 worden naar boven afgerond.|

Als u gereed bent, kiest u de actie **Demogegevens maken**. Het duurt een paar minuten om de gegevens aan de onderliggende database toe te voegen, maar dan bent u klaar om de verschillende scenario's uit te voeren.  

> [!IMPORTANT]
> Als u de scenario's uitvoert, wilt u mogelijk controleren of uw gebruiker is toegevoegd zoals voor geselecteerde locaties. Zie voor meer informatie [Magazijnmedewerkers instellen](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios" />Scenario's

De magazijndemogegevens voor Contoso Coffee ondersteunen momenteel de volgende magazijnscenario's voor testen en trainen:

1.  [Doorlopen van de inkomende en uitgaande stroom in basismagazijnconfiguraties](warehouse-basic-flow-putaway-pick.md)
2.  [Doorlopen van de inkomende en uitgaande stroom in gemengde magazijnconfiguraties](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Doorloop van de inkomende en uitgaande stroom in geavanceerde magazijnconfiguratie met gestuurde opslag en pick](warehouse-directed-flow.md)

Lees de stappen voor elk scenario in het desbetreffende artikel.  

## <a name="see-also" />Zie ook

[Voorraad instellen](../../inventory-setup-inventory.md) 
[Procedure: vestigingen instellen](../../inventory-how-setup-locations.md) 
[Magazijnbeheer](../../warehouse-manage-warehouse.md) 
[Ontwerpdetails](../../design-details-warehouse-overview.md) 
