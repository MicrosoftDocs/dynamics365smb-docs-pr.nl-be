---
title: 'Ontwerpdetails: Tabel Planningstoewijzing'
description: Dit onderwerp geeft inzicht in wat er gebeurt als een verandering in de vraag- of aanbodpatronen vereist dat u berekent hoe u een artikel plant.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Ontwerpdetails: Tabel Planningstoewijzing
Alle artikelen moeten worden gepland, maar er is geen reden om een planning voor een artikel te berekenen tenzij er een verandering in het vraag- of aanbodpatroon is opgetreden sinds er voor het laatst een planning is berekend.  

Als de gebruiker een nieuwe verkooporder heeft ingevoerd of een bestaande heeft gewijzigd, is er reden om de planning opnieuw te berekenen. Andere redenen omvatten een wijziging in de voorspelde of gewenste veiligheidsvoorraad. Het wijzigen van een stuklijst door een materiaal toe te voegen of te verwijderen duidt waarschijnlijk op een wijziging, maar alleen voor het onderdeelartikel.  

Voor meerdere vestigingen vindt de toewijzing plaats op het niveau van de combinatie artikel per vestiging. Wanneer bijvoorbeeld een verkooporder op slechts één vestiging is gemaakt, wordt het artikel in die specifieke vestiging voor planning toegewezen.  

De reden voor het selecteren van artikelen voor planning heeft te maken met systeemprestaties. Als er geen verschil is opgetreden in het vraag/aanbod-patroon van een artikel, zal het planningssysteem geen uit te voeren acties voorstellen. Zonder de planningstoewijzing moet het systeem de berekeningen voor alle artikelen uitvoeren om te weten waarvoor moet worden gepland, en dat zou de systeembronnen uitputten.  

De tabel **Planningsopdracht** bewaakt vraag- en aanbodgebeurtenissen en wijst de benodigde artikelen toe aan de planning. De volgende gebeurtenissen worden gecontroleerd:  

* Een nieuwe verkooporder, prognose, onderdeel, inkooporder, productieorder, assemblageorder of transferorder.  
* Wijziging van een artikel, aantal, locatie, variant of datum in een verkooporder, prognose, onderdeel, inkooporder, productieorder, assemblageorder of transferorder.  
* Annulering van een verkooporder, prognose, onderdeel, inkooporder, productieorder, assemblageorder of transferorder.  
* Verbruik van andere dan geplande artikelen.  
* Output van andere dan geplande artikelen.  
* Niet-geplande wijzigingen in voorraad.  

Voor deze directe aanbod-vraag verplaatsingen onderhoudt het ordertracerings- en planningsboodschapsysteem de tabel Planningstoewijzing en geeft het een planningsreden als een planningsboodschap.  

De volgende wijzigingen in stamgegevens kunnen ook een verstoord evenwicht in de planning veroorzaken:  

* Wijziging van status in Gecertificeerd in de productiestuklijstkop (voor alle artikelen die de kop gebruiken).  
* Verwijderde regel (onderliggend artikel).  
* Wijziging van status in Gecertificeerd in de bewerkingsplankop (voor alle artikelen die het bewerkingsplan gebruiken).  
* Wijzigingen in de volgende artikelkaartvelden.  
* Veiligheidsvoorraad of veiligheidstijd.  
* Levertermijn.  
* Bestelpunt.  
* Productiestuklijstnr. (en alle onderliggende elementen van oude stuklijstverwijzing).  
* Bew.-plannr.  
* Bestelbeleid.  

In deze gevallen onderhoudt een nieuwe functie, Beheer planningstoewijzing, de tabel en wordt als planningsreden Mutatie vermeld.  

De volgende wijzigingen hebben geen planningsopdracht als gevolg:  

* Agenda's  
* Overige planningsparameters op de artikelkaart  

Bij het berekenen van een MPS of MRP gelden de volgende beperkingen:  

* MPS: Het planningssysteem controleert of het artikel een vraagprognose of een verkooporder heeft. Zo niet, dan wordt het artikel niet opgenomen in de planning.  
* MRP: Wanneer het planningssysteem ontdekt dat het artikel wordt aangevuld door een MPS-planningsregel of een MPS-voorzieningenorder, wordt het artikel uit de planning gelaten. Vraag van relevante onderdelen wordt echter opgenomen.  

## Zie ook  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
[Ontwerpdetails: Transfers in planning](design-details-transfers-in-planning.md)   
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]