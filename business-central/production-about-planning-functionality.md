---
title: Informatie over het plannen van functionaliteit | Microsoft Docs
description: Het planningssysteem houdt rekening met alle gegevens over vraag en voorzieningen, berekent het nettoresultaat, en doet suggesties voor het in overeenstemming brengen van de voorzieningen en de vraag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/14/2020
ms.author: sgroespe
ms.openlocfilehash: 2b803e52038d39375aa13dce36f81d429261f985
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577350"
---
# <a name="about-planning-functionality"></a>Informatie over het plannen van functionaliteit

Het planningssysteem houdt rekening met alle gegevens over vraag en aanbod, berekent het nettoresultaat en doet suggesties voor het in overeenstemming brengen van aanbod en vraag.  

Zie [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md) voor gedetailleerde informatie.  

> [!NOTE]  
> Voor alle velden die in dit onderwerp worden genoemd, kunt u de knopinfo lezen om de functie te begrijpen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Vraag en voorzieningen

Planning bestaat uit twee elementen: vraag en voorzieningen. Deze moeten in evenwicht worden gehouden, zodat op tijd en op een kosteneffectieve wijze aan de vraag wordt voldaan.  

- Vraag is een gebruikelijke term voor elke soort brutobehoefte, zoals een verkooporder, serviceorder, materiaalbehoefte vanuit een assemblage- of productieorder, transfer uit, raamcontract of prognose. Daarnaast voorziet de toepassing in enkele andere technische soorten vraag, zoals een negatieve productie- of inkooporder, negatieve voorraad en inkoopretour.  
- Voorzieningen is een gebruikelijke term voor elke soort aanvulling, zoals voorraad, een inkoop-, assemblage- of productieorder, of transfer in. Ter vergelijking kunnen er ook een negatieve verkoop- of serviceorder, negatieve materiaalbehoefte of verkoopretour zijn, die alle op de een of andere wijze ook voorzieningen weergeven.  

Een ander doel van het planningssysteem is ervoor te zorgen dat de voorraad niet onnodig toeneemt. In het geval van een afnemende vraag zal het planningssysteem voorstellen om bestaande aanvullingsorders uit te stellen, in omvang te verkleinen of te annuleren.  

## <a name="planning-calculation"></a>Planningsberekening

Het planningssysteem wordt gestuurd door de verwachte en werkelijke vraag van klanten, alsmede de parameters van de voorraadinkoopvoorstellen. Het uitvoeren van de planningsberekening leidt ertoe dat de toepassing specifieke acties (planningsboodschappen) voorstelt die genomen dienen te worden met betrekking tot mogelijke aanvullingen door leveranciers, transfers tussen magazijnen of productie. Als er al aanvullingsorders zijn, kunnen de voorgestelde acties bestaan uit het vergroten of versnellen van de orders om te voorzien in veranderingen in de vraag.  

De basis van de planningsroutine is gelegen in de bruto-naar-netto-berekening. De nettobehoeften sturen de geplande ordervrijgaven, die worden gepland op basis van de bewerkingsplaninformatie (geproduceerde artikelen) of de artikeldoorlooptijd (ingekochte artikelen). De aantallen van geplande ordervrijgaven zijn gebaseerd op de planningsberekening en worden beïnvloed door de parameters die zijn ingesteld op de afzonderlijke artikelkaarten.  

## <a name="planning-with-manual-transfer-orders"></a>Planning met handmatige transferorders

In het veld **Aanvullingsmethode** op een SKU-kaart kunt u zien dat het planningssysteem zo kan worden ingesteld dat er transferorders worden gemaakt om voorraad en vraag op alle vestigingen in balans te brengen.  

Naast dergelijke automatische transferorders, moet u mogelijk zo nu en dan voorraadhoeveelheden naar een andere vestiging verplaatsen, ongeacht de bestaande vraag. U kunt voor dit doel handmatig een transferorder maken voor de hoeveelheid die moet worden verplaatst. U kunt ervoor zorgen dat het planningssysteem deze handmatige transferorder niet wijzigt door het veld **Planningsflexibiliteit** op de transferregel(s) in te stellen op Geen.  

Daar staat tegenover dat u het veld **Planningsflexibiliteit** moet instellen op de standaardwaarde Ongelimiteerd als u wilt dat het planningssysteem de hoeveelheden van de transferorder en de datums wel wijzigt op basis van de bestaande vraag.

## <a name="planning-parameters"></a>Planningsparameters

De planningsparameters bepalen wanneer, hoeveel en hoe er wordt aangevuld op basis van de verschillende instellingen op de artikelkaart (SKU) en de productie-instellingen.  

De volgende planningsparameters bestaan op de artikel-/SKU-kaart:  

- Dempingsperiode  
- Dempingsaantal  
- Bestelbeleid  
- Bestelpunt
- Maximale voorraad  
- Overflowniveau  
- Tijdsinterval  
- Lotaccumulatieperiode  
- Herplanningsperiode  
- Bestelaantal  
- Veiligheidstijd  
- Veiligheidsvoorraad  
- Assemblagebeleid  
- Productiebeleid  

De volgende orderwijzigingen bestaan op de artikel-/SKU-kaart:  

- Min. bestelaantal  
- Max. bestelaantal  
- Vaste lotgrootte  

Algemene velden voor planningsinstellingen op de pagina **Productie-instellingen** zijn onder andere:  

- Dynamische low-levelcode  
- Huidige vraagprognose  
- Prognose op vestigingen gebruiken  
- Std. veiligheidstijd  
- Blanco-overflowniveau  
- Gecombineerd MPS/MRP berek.
- Onderdelen op vestiging  
- Standaard dempingsperiode  
- Demping standaardhoeveelheid  

Zie [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) voor meer informatie.  

## <a name="other-important-planning-fields"></a>Andere belangrijke planningsvelden

### <a name="planning-flexibility"></a>Planningsflexibiliteit

Voor de meeste aanvulorders, bijvoorbeeld productieorders, kunt u **Ongelimiteerd** of **Geen** instellen voor het veld **Planningsflexibiliteit** op de regels.

Zo geeft u op of het planningssysteem bij de berekening van planningsboodschappen rekening houdt met het aanbod op de productieorderregel.
Als het veld de optie **Ongelimiteerd** bevat, wordt de regel opgenomen in de berekening van planningsboodschappen. Als het veld de optie **Geen** bevat, is de regel vast en onveranderbaar, en wordt deze regel niet door het planningssysteem meegenomen bij de berekening van planningsboodschappen.

### <a name="warning"></a>Waarschuwing

Het informatieveld **Waarschuwing** op de pagina **Planningsvoorstel** biedt u informatie over elke planningsregel die voor een uitzonderlijke situatie met tekst is gemaakt. De gebruiker kan er dan voor kiezen om aanvullende informatie te lezen. De volgende waarschuwingstypen zijn mogelijk:

- Noodgeval
- Uitzondering
- Opmerking
- Noodgeval

De waarschuwing Noodgeval wordt in twee gevallen weergegeven:

- De voorraad is negatief op de geplande begindatum.
- Er bestaan geantedateerde voorziening- of vraaggebeurtenissen.

Als de voorraad van een artikel negatief is op de geplande begindatum, wordt er door het planningssysteem een noodorder voor een voorziening voorgesteld die wordt aangevoerd op de geplande begindatum. De waarschuwing vermeldt de begindatum en de hoeveelheid van de order voor een noodvoorziening.

Alle documentregels met vervaldatums voor de geplande begindatum worden samengevoegd tot één noodorder voor een voorziening voor het artikel die wordt aangevoerd op de geplande startdatum.

### <a name="exception"></a>Uitzondering

De uitzonderingswaarschuwing wordt weergegeven als de verwachte beschikbare voorraad onder de veiligheidsvoorraad daalt.

Het planningssysteem stelt een order voor een voorziening voor om aan de vraag op de vervaldatum te kunnen voldoen. De waarschuwing vermeldt de veiligheidsvoorraad van het artikel en de datum waarop de voorraad daaronder daalt.

Als de beschikbare voorraad kleiner is dan de veiligheidsvoorraad, wordt dit als een uitzondering beschouwd omdat dit normaliter niet gebeurt als het bestelpunt op de juiste manier is ingesteld.

> [!NOTE]
> Voorzieningen op planningsregels met uitzonderingswaarschuwingen worden gewoonlijk niet gewijzigd volgens planningsparameters. In plaats daarvan stelt het planningssysteem alleen een voorziening ter dekking van de hoeveelheid van de exacte vraag voor. U kunt echter de uitvoering van de planning zo instellen dat bepaalde planningsparameters voor planningsregels met bepaalde waarschuwingen worden gerespecteerd. Zie voor meer informatie de beschrijving van het veld **Planningsparameters voor uitzonderingswaarschuwingen respecteren** in het artikel [Volledige planning, MPS of MRP uitvoeren](production-how-to-run-mps-and-mrp.md).

### <a name="attention"></a>Opmerking

De waarschuwing Attentie wordt in twee gevallen weergegeven:

- De geplande begindatum is eerder dan de werkdatum.
- Op de planningsregel wordt voorgesteld een vrijgegeven inkoop- of productieorder te wijzigen.

> [!NOTE]
> bij het plannen van regels met waarschuwingen wordt het veld **Planningsboodschap accepteren** niet geselecteerd, omdat de planner naar verwachting de regels verder gaat bekijken voordat de planning wordt uitgevoerd.

## <a name="planning-worksheets-and-requisition-worksheets"></a>Planningsvoorstellen en inkoopvoorstellen

Zoals beschreven in [Planning](production-planning.md) kunt u voor de meeste planningsactiviteiten kiezen tussen twee voorstellen, het planningsvoorstel en het inkoopvoorstel. De meeste processen worden beschreven op basis van het planningsvoorstel, maar er is een aantal scenario's waarin het inkoopvoorstel de voorkeur heeft.

### <a name="requisition-worksheet"></a>Inkoopvoorstel

De pagina **Inkoopvoorstel** vermeldt artikelen die u wilt bestellen. U kunt op de volgende manieren artikelen op het voorstel invoeren:

- Voer de artikelen handmatig in op het voorstel en vul de relevante velden in.

- Gebruik de batchverwerking **Planning berekenen**. Hiermee wordt een aanvullingsplan berekend voor artikelen en SKU's waarvoor de aanvullingsmethode **Inkoop** of **Transfer** is ingesteld. Wanneer u deze batchverwerking gebruikt, wordt het veld **Planningsboodschap** automatisch ingevuld met een aanvullingsvoorstel voor het artikel. Hierdoor kan het aantal artikelen op een bestaande order worden vergroot of er kan bijvoorbeeld een nieuwe order worden gemaakt.

- Als u vanaf de pagina **Planningsvoorstel** de batchverwerking **Planning berekenen** hebt geselecteerd, kunt u de batchverwerking **Planningsboodschap uitvoeren** gebruiken om inkoop- en transferordervoorstellen te kopiëren van het planningsvoorstel naar het inkoopvoorstel. Dit is praktisch wanneer voor de verwerking van productieorders en inkoop-/transferorders aparte gebruikers verantwoordelijk zijn.

- U kunt de actie **Doorverzending** gebruiken om de inkoopvoorstelregels in te vullen. Hierbij wordt gebruikgemaakt van de batchverwerking **Verkooporders ophalen**, zodat u kunt bepalen welke verkooporderregels voor een doorverzending zijn bestemd.

- U kunt de actie **Doorverzending** gebruiken om de inkoopvoorstelregels in te vullen. Hierbij wordt gebruikgemaakt van de batchverwerking **Verkooporders ophalen**, zodat u kunt bepalen welke verkooporderregels voor een aparte opdracht zijn bestemd.

Inkoopvoorstelregels bevatten gedetailleerde informatie over de artikelen die moeten worden besteld. U kunt de regels van het aanvullingsplan bewerken en verwijderen en vervolgens met de batchverwerking **Planningsboodschap uitvoeren** verwerken.

Zie voor details over het plannen met locaties en transfers [Planning met of zonder locaties](production-planning-with-without-locations.md).

## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)  
[Gepland](production-planning.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
