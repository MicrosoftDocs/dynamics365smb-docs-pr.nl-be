---
title: 'Ontwerpdetails: Vraag en aanbod | Microsoft Docs'
description: In dit onderwerp worden de concepten van vraag beschreven, de verzamelterm voor elk soort brutovraag, zoals een verkooporder en materiaalbehoefte van een productieorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cbafba8d012244b10c142912b357188a1f7eece4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386961"
---
# <a name="design-details-demand-at-blank-location"></a>Ontwerpdetails: Vraag op lege vestiging
Wanneer een gebruiker een vraaggebeurtenis maakt, zoals een verkooporderregel, kan de gebruiker soms een vestigingscode toevoegen, maar soms ook niet. In dat geval wordt een lege vestiging gebruikt.

Voor vraag met of zonder vestigingscodes werkt het planningssysteem eenvoudig en duidelijk wanneer:

- Vraagregels altijd vestigingscodes bevatten en het systeem SKU's gebruikt, inclusief de relevante vestigingsinstellingen.
- Vraagregels bevatten nooit vestigingscodes en het systeem gebruikt geen SKU's of andere vestigingsinstellingen (zie het laatste scenario in het volgende gedeelte).

Als vraaggebeurtenissen echter de ene keer wel vestigingscodes bevatten en de andere keer niet, volgt het planningssysteem bepaalde regels, afhankelijk van de instellingen.

## <a name="demand-at-location"></a>Vraag op vestiging
Wanneer het planningssysteem ontdekt dat er op een bepaalde vestiging vraag is, reageert het systeem op verschillende manieren, afhankelijk van drie essentiële instellingen. Tijdens de uitvoering van een planning controleert het systeem een voor een de waarden van de drie instellingen en plant aan de hand van die waarden.

1. Is het selectievakje **Vestiging verplicht** ingeschakeld?

    Als dit het geval is dan:

2. Bestaat de SKU voor het artikel?

    Als dit het geval is dan:

    Het artikel is gepland aan de hand van de planningsparameters op de SKU-kaart.

    Als dit niet het geval is dan:

3. Bevat het veld Onderdelen op vestiging de vereiste vestigingscode?

  Als dit het geval is dan:

  Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.

  Als dit niet het geval is dan:

  Het artikel wordt gepland aan de hand van: Bestelbeleid = Lot-voor-lot, Inclusief voorraad = Ja, alle andere planningsparameters = Leeg, artikelen die gebruikmaken van bestelbeleid = Order blijven zowel Order als de andere instellingen gebruiken.

> [!NOTE]
> De uitzonderlijke planningsinstelling die wordt uitgevoerd als laatste reactie in stap 3 hierboven, wordt in het volgende "minimaal alternatief" genoemd. Deze planningsinstellingen dekken alleen de exacte vraag en alle andere planningsparameters worden genegeerd.

Voor informatie over variaties van deze planningslogica raadpleegt u het gedeelte Scenario's hieronder.

## <a name="demand-at-blank-location"></a>Vraag op lege vestiging
Zelfs als het veld **Vestiging verplicht** is geselecteerd, kan het programma vraagregels zonder een vestigingscode maken, ook wel lege vestiging genoemd. Dit is een afwijking voor het systeem omdat verschillende instellingswaarden zijn afgestemd op gebruik van vestigingen (zie boven). De planningsengine maakt hierdoor geen planningsregel voor een dergelijke vraagregel.

Als het veld **Vestiging verplicht** niet is geselecteerd maar een van de vestigingsinstellingwaarden bestaat, wordt dit ook beschouwd als een afwijking, en wordt door het planningssysteem gereageerd met het "minimale alternatief": het artikel wordt gepland volgens: bestelbeleid = lot-voor-lot (order blijft order), inclusief voorraad = Ja, alle andere planningsparameters = Leeg.

## <a name="scenarios"></a>Scenario's
In de volgende scenario's worden varianten van de vraag op een lege vestiging omschreven en hoe het planningssysteem wordt ingesteld op het "minimale alternatief".

### <a name="setup-1"></a>Instelling 1:
Vestiging verplicht = Ja

SKU is ingesteld voor ROOD

Onderdelen op vestiging = BLAUW

#### <a name="case-11-demand-is-at-red-location"></a>Case 1.1: vraag is op RODE vestiging
Het artikel is gepland aan de hand van de planningsparameters op de SKU-kaart.

#### <a name="case-12-demand-is-at-blue-location"></a>Case 1.2: vraag is op BLAUWE vestiging
Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.

#### <a name="case-13-demand-is-at-green-location"></a>Case 1.3: vraag is op GROENE vestiging
Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.

#### <a name="case-14-demand-is-at-blank-location"></a>Case 1.4: vraag is op LEGE vestiging
Het artikel is niet gepland omdat er geen vestiging is gedefinieerd op de vraagregel.

### <a name="setup-2"></a>Instelling 2:
Vestiging verplicht = Ja

Er bestaat geen SKU

Onderdelen op vestiging = BLAUW

#### <a name="case-21-demand-is-at-red-location"></a>Case 2.1: vraag is op RODE vestiging
Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.

#### <a name="case-22-demand-is-at-blue-location"></a>Case 2.2: vraag is op BLAUWE vestiging
Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.

### <a name="setup-3"></a>Instelling 3:
Vestiging verplicht = Nee

Er bestaat geen SKU

Onderdelen op vestiging = BLAUW

#### <a name="case-31-demand-is-at-red-location"></a>Case 3.1: vraag is op RODE vestiging
Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.

#### <a name="case-32-demand-is-at-blue-location"></a>Case 3.2: vraag is op BLAUWE vestiging
Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.

#### <a name="case-33-demand-is-at-blank-location"></a>Case 3.3: vraag is op LEGE vestiging
Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.

### <a name="setup-4"></a>Instelling 4:
Vestiging verplicht = Nee

Er bestaat geen SKU

Onderdelen op vestiging = LEEG

#### <a name="case-41-demand-is-at-blue-location"></a>Case 4.1: vraag is op BLAUWE vestiging
Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.

#### <a name="case-42-demand-is-at-blank-location"></a>Case 4.2: vraag is op LEGE vestiging
Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.

Zoals in het laatste scenario wordt getoond, kunt u alleen een correct resultaat krijgen voor een vraagregel zonder vestigingscode door alle instellingswaarden uit te schakelen die naar vestigingen verwijzen. Zo krijgt u ook alleen stabiele planningsresultaten voor vraag op vestigingen als u SKU's gebruikt. Als bedrijven dus vaak plannen voor vraag op vestigingen, wordt hun sterk aangeraden de granule voor SKU's te gebruiken.

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]