---
title: Planning met of zonder vestigingen
description: 'In dit onderwerp leert u over productie en fabricage, inclusief leveringsplanning, in Business Central.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: edupont
---
# <a name="planning-with-or-without-locations" />Planning met of zonder vestigingen

Voordat u de planningsengine gaat gebruiken, raden we u aan om te beslissen of u vestigingen wilt gebruiken. Er zijn twee eenvoudige hoofdmanieren:

* vraagregels altijd vestigingscodes bevatten en het systeem SKU's gebruikt, inclusief de relevante vestigingsinstellingen. Meer informatie op [Vraag op vestiging](#demand-at-location).  
* vraagregels bevatten nooit vestigingscodes en het systeem gebruikt de artikelkaart. Zie de het onderstaande scenario [Vraag op een "lege vestiging"](#demand-at-blank-location).

## <a name="demand-at-location" />Vraag op vestiging

Wanneer het planningssysteem ontdekt dat er op een bepaalde vestiging vraag is (een regel met een vestigingscode), reageert het systeem op verschillende manieren, afhankelijk van 2 essentiële instellingswaarden.  

Tijdens de uitvoering van een planning controleert het systeem een voor een de waarden van de twee instellingen en plant aan de hand van die waarden:  

1. Bestaat er een SKU voor het artikel op de gewenste vestiging?  

    Als dit het geval is dan:  

    Het artikel is gepland aan de hand van de planningsparameters op de SKU-kaart.  

    Als dit niet het geval is dan:  

2. Bevat het veld **Onderdelen op vestiging** op de pagina **Productie-instellingen** de gevraagde vestgingscode?  

    Als dit het geval is dan:  

    Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.  

    Als dit niet het geval is dan:  

    Het artikel wordt gepland volgens het "minimale alternatief" dat de exacte vraag dekt. De planningsparameters worden als volgt ingesteld: Bestelbeleid = *Lot-voor-Lot*, Inclusief voorraad = *Ja*, alle andere planningsparameters = Leeg. (Artikelen die gebruikmaken van het bestelbeleid *Order* blijven *Order* gebruiken en de andere instellingen ook.)

> [!TIP]
> Als u vaak plant voor vraag op verschillende vestigingen, bevelen we aan dat u de SKU-functionaliteit gebruikt en vraag op lege vestigingen voorkomt. Meer informatie op [SKU's instellen](inventory-how-to-set-up-stockkeeping-units.md)

Zie de variaties in de [onderstaande scenario's](#scenarios).

> [!NOTE]
> Het veld **Onderdelen op vestiging** op de pagina **Productie-instellingen** is erg belangrijk om te bepalen hoe het planningssysteem omgaat met productievraagregels.
>
> Met betrekking tot de productievraag gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] dezelfde vestiging voor subassemblage en onderdelen als die welke op de productieorder vermeld staat. Door dit veld in te vullen kunt u echter de subassemblage en onderdelen naar een andere vestiging leiden.
>
> U kunt dit ook voor een specifieke SKU definiëren door de code van een andere vestiging in het veld **Onderdelen op vestiging** op de SKU-kaart te selecteren. Let echter op dat dit nauwelijks zinvol is aangezien de planningslogica vervormd kan zijn wanneer u plant voor de SKU-component.

## <a name="demand-at-blank-location" />Vraag op "lege vestiging"

Wanneer het planningssysteem vraag detecteert op een lege vestiging (een regel zonder vestigingscode), wordt het artikel over het algemeen gepland volgens planningsparameters op de artikelkaart.

Het veld **Vestiging verplicht** op de pagina **Voorraadinstellingen** en het veld **Onderdelen op vestiging** op de pagina **Productie-instellingen** of SKU's zijn erg belangrijk om te bepalen hoe het planningssysteem vraagregels met/zonder vestigingscodes verwerkt. Als een van de volgende beweringen waar is, wordt dit ook beschouwd als een afwijking, en wordt door het planningssysteem gereageerd met het "minimale alternatief": het artikel wordt gepland volgens: bestelbeleid = *Lot-voor-lot* (*Order* blijft *Order*), inclusief Voorraad = *Ja*, alle andere planningsparameters = Leeg.

* Het veld **Onderdelen op vestiging** op de pagina **Productie-instellingen** bevat een waarde.
* Er bestaat een SKU voor het geplande artikel.
* Het veld **Vestiging verplicht** is geselecteerd.

## <a name="scenarios" />Scenario's

Zie de variaties in de onderstaande configuratiescenario's.

### <a name="setup-" />Instelling 1

* Vestiging verplicht = *Ja*  
* SKU is ingesteld voor *WEST*  
* Onderdeel op vestiging = *OOST*  

#### <a name="case--demand-is-at-west-location" />Geval 1.1: Vraag is op vestiging *WEST*

Het artikel is gepland volgens planningsparameters op de SKU-kaart (inclusief mogelijke transfer).

#### <a name="case--demand-is-at-east-location" />Geval 1.2: Vraag is op vestiging *OOST*

Het artikel wordt gepland aan de hand van planningsparameters op de artikelkaart.

#### <a name="case--demand-is-at-north-location" />Geval 1.3: vraag is op vestiging *NOORD*

Het artikel is gepland volgens: Bestelbeleid = *Lot-voor-Lot* (*Order* blijft *Order*), Inclusief voorraad = *Ja*, alle andere planningsparameters = Leeg.

#### <a name="case--demand-is-at-blank-location" />Case 1.4: vraag is op *LEGE* vestiging

Het artikel is gepland volgens: Bestelbeleid = *Lot-voor-Lot* (*Order* blijft *Order*), Inclusief voorraad = *Ja*, alle andere planningsparameters = Leeg.

### <a name="setup-" />Instelling 2

* Vestiging verplicht = *Ja*  
* Er bestaat geen SKU  
* Onderdeel op vestiging = *OOST*  

#### <a name="case--demand-is-at-west-location" />Geval 2.1: Vraag is op vestiging *WEST*

Het artikel is gepland volgens: Bestelbeleid = *Lot-voor-Lot* (*Order* blijft *Order*), Inclusief voorraad = *Ja*, alle andere planningsparameters = Leeg.

#### <a name="case--demand-is-at-east-location" />Geval 2.2: Vraag is op vestiging *OOST*

Het artikel wordt gepland aan de hand van planningsparameters op de artikelkaart.  

### <a name="setup-" />Instelling 3

* Vestiging verplicht = *Nee*  
* Er bestaat geen SKU  
* Onderdeel op vestiging = *OOST*  

#### <a name="case--demand-is-at-west-location" />Geval 3.1: Vraag is op vestiging *WEST*

Het artikel is gepland volgens: Bestelbeleid = *Lot-voor-Lot* (*Order* blijft *Order*), Inclusief voorraad = *Ja*, alle andere planningsparameters = Leeg.

#### <a name="case--demand-is-at-east-location" />Geval 3.2: Vraag is op vestiging *OOST*

Het artikel wordt gepland aan de hand van planningsparameters op de artikelkaart.  

#### <a name="case--demand-is-at-blank-location" />Case 3.3: vraag is op *LEGE* vestiging

Het artikel is gepland volgens: Bestelbeleid = *Lot-voor-Lot* (*Order* blijft *Order*), Inclusief voorraad = *Ja*, alle andere planningsparameters = Leeg.

### <a name="setup-" />Instelling 4

* Vestiging verplicht = *Nee*  
* Er bestaat geen SKU  
* Onderdeel op vestiging = *LEEG*  

#### <a name="case--demand-is-at-east-location" />Geval 4.1: vraag is op vestiging *OOST*

Het artikel is gepland volgens: Bestelbeleid = *Lot-voor-Lot* (*Order* blijft *Order*), Inclusief voorraad = *Ja*, alle andere planningsparameters = Leeg.

#### <a name="case--demand-is-at-blank-location" />Case 4.2: vraag is op *LEGE* vestiging

Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.

Zoals u in het laatste scenario kunt zien, kunt u alleen een correct resultaat krijgen voor een vraagregel zonder vestigingscode door alle instellingswaarden uit te schakelen die naar vestigingen verwijzen. Zo krijgt u ook alleen stabiele planningsresultaten voor vraag op vestigingen als u SKU's gebruikt.  

Als u vaak vraag op vestigingen plant, raden we daarom aan dat u de SKU-functionaliteit gebruikt.

## <a name="see-related-training-at-microsoft-learntrainingpathstrade-get-started-dynamics--business-central" />Zie gerelateerde training op [Microsoft Learn](/training/paths/trade-get-started-dynamics-365-business-central/).

## <a name="see-also" />Zie ook

[Gepland](production-planning.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Voorraad](inventory-manage-inventory.md)  
[SKU's instellen](inventory-how-to-set-up-stockkeeping-units.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)  
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
