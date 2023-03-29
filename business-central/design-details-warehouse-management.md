---
title: Magazijnactiviteiten beheren
description: Naast ontvangsten en verzendingen ondersteunt Business Central een reeks interne magazijnactiviteiten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/05/2022
ms.custom: bap-template
---

# Overzicht van magazijnbeheer

Er zijn twee dingen die belangrijk zijn voor alle bedrijven die goederen fysiek in en uit hun magazijn verplaatsen:

* Ze hebben een overzicht van voorraadniveaus en artikelplaatsing in het magazijn.
* Ze kunnen artikelen snel en nauwkeurig ontvangen, picken en verzenden.

Om bedrijven te helpen deze dingen te bereiken, voegen magazijnfuncties in [!INCLUDE[prod_short](includes/prod_short.md)] de volgende mogelijkheden toe aan voorraadbeheer:

* Opslaglocaties
* Magazijnverzendingen
* Voorraadpicks
* Verplaatsingswerkblad

Implementeer deze functies in verschillende combinaties om uw magazijnprocessen af te stemmen op uw bedrijf. Houd rekening met toenemende complexiteit naarmate uw bedrijf groeit en uw processen veranderen.

## Overzicht van verschillende configuratieopties

U kunt magazijnfuncties op verschillende manieren configureren. Het is belangrijk dat de opties die u kiest uw processen verbeteren zonder overhead te veroorzaken. De volgende tabel geeft een overzicht van typische configuraties die worden gebruikt bij het omgaan met fysieke goederen.

|Complexiteitniveau|Omschrijving|Instellingen|Opslaglocatie|Voorbeeld van inkomende stroom|Voorbeeld van uitgaande stroom|Voorbeeld van interne stroom|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Geen specifieke magazijnactiviteit.|Boeken van orders en dagboeken.||Optioneel. Bepaald door de instelling **Opslaglocatiecode is verplicht**.|Inkooporder|Verkooporder| Productieorder -> Verbruiksdagboek|  
|Basis|Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|**Ontvangst vereist**<br>**Verzending vereist**|Optioneel. Bepaald door de instelling Opslaglocatiecode is verplicht|Inkooporder(s) -> Magazijnontvangst|Verkooporder -> Magazijnverzending|Hetzelfde als hierboven.|
|Basis|Order-voor-order.|Opslag vereisen of pick vereisen. </br><br/> **OPMERKING**: hoewel de instellingen **Pick vereist** en **Opslag vereist** heten, kunt u nog wel ontvangsten en verzendingen rechtstreeks vanuit de brondocumenten boeken op vestigingen waarvoor u deze selectievakjes inschakelt.|Optioneel. Bepaald door de instelling **Opslaglocatiecode is verplicht**.|Inkooporder - Voorraadopslag|Verkooporder -> Voorraadpick|Productieorder - Voorraadpick|
|Geavanceerd|Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.<br /><br />Geconsolideerde pick-/opslagactiviteiten voor meerdere brondocumenten.|Ontvangst vereist + Opslag vereist,</br> Verzending vereist + Pick vereist|Optioneel. Bepaald door de instelling Opslaglocatiecode is verplicht|Inkooporder(s) -> Magazijnontvangst -> Magazijnopslag|Verkooporder(s) -> Magazijnzending(en) -> Pickvoorstel -> Magazijnpick(s)| Productieorder -> Pickvoorstel -> Magazijnpick(s) -> Verbruiksdagboek|
|Geavanceerd|Hetzelfde als hierboven + gerichte pick-/opslagactiviteiten|Gerichte pick en opslag (afhankelijke schakelaars worden automatisch ingeschakeld)|Verplicht|Hetzelfde als hierboven.|Hetzelfde als hierboven.| Productieorder -> Pickvoorstel -> Magazijnpick(s) -> Verbruiksdagboek|

De complexiteit neemt toe met de grootte van uw organisatie en het aantal afdelingen en mensen dat erbij betrokken is. Een proces kan bijvoorbeeld eenvoudig zijn wanneer dezelfde persoon een verkoopdocument maakt en boekt. Processen kunnen ook complexer zijn en meerdere stappen en mensen omvatten. De volgende stappen zijn een voorbeeld van een complexer proces:

1. Een orderverwerker maakt een verkooporder.
1. Een magazijnbeheerder maakt pickinstructies.
1. Een magazijnmedewerker beëindigt de stroom door de magazijnverzending te boeken.

De mate van complexiteit wordt ook beïnvloed door de soorten documenten die u gebruikt in uw magazijnactiviteiten. U kunt bijvoorbeeld magazijnontvangst- en magazijnopslagdocumenten gebruiken voor uw inkomende stroom, maar voorraadpickdocumenten voor uw uitgaande stroom.

Een andere factor die de complexiteit beïnvloedt, is hoe uw fysieke magazijn wordt weergegeven in [!INCLUDE[prod_short](includes/prod_short.md)]. Ga voor meer informatie naar [Het fysieke magazijn modelleren](#modeling-the-physical-warehouse).

## Het fysieke magazijn modelleren

U hebt verschillende opties om de real-world setup van uw magazijn weer te geven in [!INCLUDE[prod_short](includes/prod_short.md)]. Uw keuzes bepalen hoe u met magazijnfuncties werkt.

De plaatsing van artikelen kan schappen, vestigingen of opslaglocaties zijn en er zijn voor- en nadelen voor elke optie.

### Vestigingen en opslaglocaties

Om fysieke goederen af te handelen, moet u ten minste één vestiging hebben. U kunt meerdere vestigingen gebruiken of opslaglocaties gebruiken om uw magazijn en organisatiestructuur te modelleren.

Vestigingen zijn doorgaans de voorkeursmanier om operaties te organiseren die over geografische gebieden zijn verspreid. In sommige gevallen wilt u misschien meerdere vestigingen maken die zich op dezelfde plek bevinden. Het gebruik van vestigingen heeft de volgende voordelen:

* Verleen toegang via de pagina's **Magazijnmedewerker** en **Divisies** .
* Definieer agenda's, bewerkingsplannen en inkomende en uitgaande verwerkingstijden voor datumberekening en planning. [Over het plannen van functionaliteit](production-about-planning-functionality.md)
* Geef standaarddimensies op en gebruik verschillende instellingen voor voorraadboeking.
* Stel planningsparameters in. Zie voor meer informatie [Planningsparameters](production-about-planning-functionality.md#planning-parameters).  
* Gebruik verschillende magazijnfuncties voor elke vestiging.

### Schappen en opslaglocaties

Als u een artikel altijd op dezelfde plek bewaart, kunt u het veld **Schapnummer** gebruiken op de pagina's **Artikel** of **SKU**. Het veld kan worden gebruikt als een handmatig basisopslagsysteem in omgevingen zonder opslaglocaties. Het wordt gekopieerd van de artikelkaart naar lijsten en documentregels, maar is niet te wijzigen. De waarde wordt niet gebruikt in magazijnactiviteiten of beschikbaarheidsberekeningen.

Opslaglocaties vertegenwoordigen de standaardmagazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen:

* Een of meer vaste opslaglocaties voor een artikel.
* Opslaglocaties voor specifieke bewerkingen, zoals een verzendopslaglocatie of een productie-uitvoeropslaglocatie.
* Opslaglocatiecapaciteit en gewichtsbeperkingen (alleen voor gerichte opslag en pick).
* Opslaglocatiebeoordeling (alleen voor gestuurde opslag en pick).

## Typische magazijnwerkstroom

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.

|**Functie**|**Zie**|  
|------------|-------------|  
|Gebruik in een basisstroom per order een voorraadopslag om de ontvangst van artikelen op vestigingen vast te leggen, inclusief eventuele overontvangst. Of gebruik een magazijnontvangst als u meerdere orders consolideert in de ontvangst.|[Inkomende stroom](design-details-inbound-warehouse-flow.md)|
|Registreer de verzending van artikelen vanuit magazijnvestigingen. Gebruik op een order-per-order basis een voorraadpick. Of gebruik een magazijnontvangst als u meerdere orders consolideert in de verzending.|[Uitgaande stroom](design-details-outbound-warehouse-flow.md)|
|Behandel artikelen binnen de magazijnvestiging. Bijvoorbeeld wanneer u componenten naar productie verplaatst of een fysieke inventarisatie uitvoert.|[Interne stroom](design-details-internal-warehouse-flows.md)|

Stel de magazijnprocessen in die geschikt zijn voor uw bedrijf. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

## Terminologie gerelateerd aan magazijnbeheer

### Complexiteitsniveaus

We gebruiken de termen "basis" en "geavanceerd" om onderscheid te maken tussen niveaus van complexiteit. Deze eenvoudige differentiatie dekt verschillende niveaus van complexiteit in vestigingsinstellingen, elk ondersteund door verschillende magazijndocumenten. Het meest geavanceerde niveau van magazijnbeheer wordt "Gerichte opslag en pick" genoemd. Om gerichte opslag en pick voor een vestiging te gebruiken schakelt u **gerichte opslag en pick** in op de pagina **Vestiging**.

### Magazijnstromen

* Inkomende stroom: artikelen verplaatsen naar de magazijnvestiging en ze beschikbaar maken, zoals aankopen en inkomende transfers.
* Uitgaande stroom: artikelen picken en verzenden naar klanten of andere vestigingen.
* Interne stroom: artikelen verwerken binnen een vestiging. Bijvoorbeeld wanneer u componenten naar productie verplaatst of een fysieke inventarisatie uitvoert.

### Basisdocumenten  

De volgende documenten worden gebruikt in basismagazijnstromen.

* Voorraadopslag
* Voorraadpick
* Voorraadverplaatsing
* Artikeldagboek
* Artikelherindelingsdagboek

### Geavanceerde documenten  

De volgende documenten worden gebruikt in geavanceerde magazijnstromen.

* Magazijnontvangst
* Opslagvoorstel
* Magazijnopslag
* Pickvoorstel
* Magazijnpick
* Verplaatsingsvoorstel
* Magazijnverplaatsing
* Interne magazijnpick
* Interne magazijnopslag
* Voorstel opslaglocatieaanmaak
* Voorstel opslaglocatie-inhoudaanmaak
* Magazijnartikeldagboek
* Dagboek voor magazijnartikelherindeling

### Pagina's en instellingen

In dit gedeelte worden de concepten achter de belangrijkste pagina's en instellingen voor magazijnbeheer beschreven.

#### Opslaglocaties en inhoud ervan

Een opslaglocatie is een opslagapparaat dat is ontworpen om afzonderlijke onderdelen te bevatten. Het is de kleinste containereenheid in [!INCLUDE[prod_short](includes/prod_short.md)]. Artikelaantallen in opslaglocaties worden *opslaglocatie-inhoud* genoemd. Een opzoekactie vanuit het veld **Artikel** of het veld **Opslaglocatie** op een magazijngerelateerde documentregel geeft de berekende beschikbaarheid van het artikel op de opslaglocatie weer.  

Opslaglocatie-inhoud kan **Vast**, **Speciaal** of **Standaard** zijn om te definiëren hoe de opslaglocatie-inhoud moet worden gebruikt. Opslaglocaties die geen van deze eigenschappen hebben, worden *vrije* opslaglocaties genoemd.  

Een vaste opslaglocatie bevat artikelen die aan de opslaglocatiecode zijn toegewezen. De eigenschap vaste opslaglocatie zorgt ervoor dat zelfs als de opslaglocatie wordt geleegd, de inhoud van de opslaglocatie niet verdwijnt. U kunt de opslaglocatie weer selecteren zodra de inhoud is aangevuld.  

Een toegewezen opslaglocatie bevat opslaglocatie-inhoud die alleen kan worden gepickt voor de specifieke resource die de opslaglocatie gebruikt. Bijvoorbeeld een bewerkingsplaats. Andere niet-pickinhoud, zoals uitgaande aantallen in een verzendingsboeking, kunnen nog steeds worden verbruikt vanuit een speciale opslaglocatie. Alleen opslaglocatie-inhoud waar door het algoritme **Pick maken** rekening mee wordt gehouden, wordt beschermd in een speciale opslaglocatie.  

De opslaglocatie-eigenschap **Standaard** wordt door [!INCLUDE [prod_short](includes/prod_short.md)] gebruikt om opslaglocaties voor magazijnactiviteiten voor te stellen. Op locaties die gerichte opslag en pick gebruiken, wordt de opslaglocatie-eigenschap Standaard niet gebruikt. Bij vestigingen waar opslaglocaties vereist zijn, geeft de eigenschap op waar artikelen in inkomende stromen moeten worden geplaatst. In uitgaande stromen geeft de eigenschap op waar artikelen vandaan moeten worden gehaald.  

> [!NOTE]  
> Als uitgaande artikelen in verschillende opslaglocaties worden geplaatst, worden artikelen eerst uit de niet-standaardopslaglocaties gehaald om die te legen, en vervolgens worden de resterende artikelen uit de standaardopslaglocatie gehaald.  

U kunt slechts één standaardopslaglocatie per artikel per vestiging hebben.  

#### Opslaglocatiesoort

Vestigingen die gerichte opslag en pick gebruiken, kunnen opslaglocatietypes gebruiken. Opslaglocatietypes bepalen de activiteiten die u toestaat voor een opslaglocatie. De volgende typen opslaglocaties zijn beschikbaar:  

|Opslaglocatiesoort|Omschrijving|  
|------------------|---------------------------------------|  
|ONTVANGST|Artikelen die zijn ontvangen maar niet zijn opgeslagen.|  
|VERZENDING|Artikelen die zijn gepickt voor magazijnverzendregels, maar die niet zijn geboekt als verzonden.|  
|OPSLAG|Meestal artikelen die in grote maateenheden worden opgeslagen, maar waartoe u geen toegang wilt om te picken. Deze opslaglocaties worden niet gebruikt voor picken, noch voor productieorders, noch voor verzendingen, dus het gebruik ervan kan beperkt zijn. Dit type opslaglocatie is handig wanneer u een grote hoeveelheid artikelen inkoopt. De opslaglocaties moeten altijd een lage opslaglocatierang hebben, zodat artikelen met een hogere OPSLPICK-opslaglocatie als eerste worden opgeslagen. Vul dit type opslaglocatie regelmatig bij, zodat de artikelen ervan beschikbaar zijn in opslaglocaties van het type OPSLPICK of PICK.|  
|PICK|Artikelen die alleen voor picken moeten worden gebruikt. U kunt verplaatsingen alleen gebruiken voor aanvulling van deze opslaglocaties, niet voor opslag.|  
|OPSL-PICK|Artikelen in opslaglocaties die worden voorgesteld voor zowel opslag als pick. Opslaglocaties van dit soort beschikken waarschijnlijk over verschillende zonevolgordes. Stel uw opslaglocaties in met lagere opslaglocatierangen dan normale pickopslaglocaties of opslaglocaties in uw voorwaartse pickgebied.|  
|QC|Deze opslaglocatie wordt gebruikt voor voorraadaanpassing indien u deze opslaglocatie opgeeft in het veld **Code aanpassing opslaglocatie** op de locatiekaart. U kunt dit soort locaties ook instellen voor defecte artikelen en artikelen die worden geïnspecteerd. Als u bepaalde artikelen ontoegankelijk wilt maken voor de normale artikelenstroom, kunt u de artikelen eveneens verplaatsen naar dit soort opslaglocatie. **OPMERKING:** in tegenstelling tot alle andere soorten opslaglocaties is bij de opslaglocatie van het type **QC** geen enkel selectievakje voor de verwerking van artikelen standaard ingeschakeld. Inhoud die u in een QC-opslaglocatie plaatst, wordt uitgesloten van artikelstromen.|  

Met uitzondering van de opslaglocaties van het type PICK, OPSLPICK en OPSLAG definieert het type opslaglocatie de toegestane activiteit voor een opslaglocatie. U kunt een opslaglocatie van het type ONTVANGEN bijvoorbeeld alleen gebruiken om artikelen te ontvangen of artikelen uit te picken.  

> [!NOTE]  
> U moet verplaatsingen gebruiken om artikelen naar ONTVANGEN- en QC-opslaglocaties te verplaatsen en verplaatsingen gebruiken om artikelen uit VERZENDEN- en QC-opslaglocaties te verplaatsen.  

#### Volgorde van opslaglocatie

In geavanceerd magazijnbeheer kunt u het verzamelen van artikelen in opslag- en pickwerkbladen automatiseren en optimaliseren door opslaglocaties te rangschikken. Artikelen worden voorgesteld voor picken en opslaan op basis van de opslaglocatierangen.

Opslagprocessen worden geoptimaliseerd op rangorde van opslaglocaties doordat opslaglocaties met een hogere rang worden voorgesteld vóór opslaglocaties met een lagere rang. Pickprocessen stellen artikelen met de hoogste opslaglocatierang uit opslaglocatie-inhoud het eerst voor. Opslaglocatieaanvulling stelt opslaglocaties met een lagere rang eerder voor dan opslaglocaties met een hogere rang.  

Opslaglocatierangen en opslaglocatie-inhoud zijn de basiseigenschappen die magazijnmedewerkers in het magazijn leiden.  

#### Instelling opslaglocatie

In geavanceerd magazijnbeheer kunt u de volgende capaciteitswaarden opgeven om te bepalen hoe en in welke opslaglocaties u artikelen opslaat:

* Aantal
* Totale kubieke inhoud
* Gewicht  

U kunt een basismaateenheid toewijzen aan artikelen. Een basismaateenheid kan bestaan uit stuks, pallets, liters, grammen of dozen. U kunt ook grotere maateenheden maken op basis van uw basismaateenheid. Als stuks bijvoorbeeld uw basiseenheid zijn, kan een pallet gelijk zijn aan 16 stuks.  

Als een artikel meer dan één maateenheid heeft, stelt u de maximale hoeveelheid in voor elke maateenheid op de artikelkaart. Als een artikel is ingesteld om te worden verwerkt in stuks en pallets, moet het veld **Max. aantal** op de pagina **Opslaglocatie-inhoud** voor dat artikel tevens in pallets en stuks zijn. Anders wordt het toegestane aantal voor die opslaglocatie niet correct berekend.  

Voordat u capaciteitsbeperkingen instelt voor inhoud van een opslaglocatie, moet u eerst zorgen dat de eenheid en de dimensies van het artikel zijn ingesteld voor het artikel.  

> [!NOTE]  
> U kunt alleen meerdere maateenheden gebruiken op locaties die gerichte opslag en pick gebruiken. In alle andere configuraties kan opslaglocatie-inhoud alleen worden uitgedrukt in de basismaateenheid. In alle transacties met een grotere maateenheid dan de basismaateenheid van het artikel wordt het aantal geconverteerd naar de basismaateenheid.  

#### Regio

In geavanceerde magazijnomgevingen kunnen opslaglocaties in zones worden gegroepeerd om te beheren hoe de werkstroom van magazijnactiviteiten wordt gedirigeerd voor vestigingen.  

Een zone kan een ontvangstzone of een bevoorradingszone zijn en elke zone kan uit een of meer opslaglocaties bestaan.  

De meeste eigenschappen die zijn toegewezen aan een zone, worden toegewezen aan de opslaglocatie die voor de zone wordt gemaakt.  

#### Magazijnklasse

In geavanceerd magazijnbeheer kunt u magazijnklassecodes toewijzen aan de volgende entiteiten: 

* Artikelen
* Opslaglocaties
* Zones

Magazijnklassen bepalen waar artikelen worden opgeslagen. U kunt een zone in verschillende magazijnklassen verdelen. Artikelen die u opslaat in de ontvangstzone, kunnen bijvoorbeeld worden opgeslagen als vast, gevaarlijk of een andere klasse.

Als u magazijnklassen en een standaardopslaglocatie voor ontvangst/verzending gebruikt, moet u de gewenste opslaglocaties in de ontvangst- en verzendingsregels voor het magazijn handmatig kiezen.  

In inkomende stromen wordt de klassecode alleen gemarkeerd op inkomende regels waar de artikelklassecode niet overeenkomt met de standaardopslaglocatie. Als de juiste standaardopslaglocaties niet zijn toegewezen, kan het aantal niet worden ontvangen.  

#### Vestiging

Een vestiging is een fysieke structuur of plaats waar inventaris wordt ontvangen, opgeslagen en verzonden. Een vestiging kan een magazijn, servicewagen, showroom, fabriek of een gebied in een fabriek zijn. Voorraad is vaak georganiseerd in opslaglocaties en zones.

#### First-Expired-First-Out (Eerst-vervallen-eerst-uit)

Als u het selectievakje **Picken volgens FEFO** inschakelt op het sneltabblad **Opslaglocatiebeleid** op de **vestigingskaart**, worden artikelgetraceerde artikelen op de vestiging gepickt op basis van de vervaldatum. Artikelen met de vroegste vervaldatums worden eerst gepickt.  

Magazijnactiviteiten in alle pick- en verplaatsingsdocumenten worden gesorteerd volgens FEFO, tenzij aan de artikelen serie-/lotnummers zijn toegewezen. Als aan sommige maar niet alle hoeveelheid op de regel serie- of lot-nummers zijn toegewezen, wordt het resterende aantal gesorteerd op basis van FEFO.  

Bij picken volgens FEFO worden artikelen eerst verzameld in een tijdelijke artikeltraceringslijst op basis van de vervaldatum. Als twee artikelen dezelfde vervaldatum hebben, wordt het artikel met het laagste lot- of serienummer het eerste gepickt. Als de lot- of serienummers gelijk zijn, wordt het artikel dat als eerste is geregistreerd, als eerste geselecteerd. Standaardcriteria voor het selecteren van artikelen in pickopslaglocaties, zoals opslaglocatievolgorde en splitsen van bulkgoederen, worden toegepast op de tijdelijke FEFO-artikeltraceringslijst.  

#### Opslagsjabloon

Opslagsjablonen geven een set prioriteitsregels op die moeten worden aangehouden wanneer u opslagactiviteiten maakt. Een opslagsjabloon kan bijvoorbeeld vereisen dat u artikelen in een opslaglocatie plaatst met opslaglocatie-inhoud die dezelfde maateenheid heeft. Als er geen vergelijkbare opslaglocatie met voldoende capaciteit kan worden gevonden, moet het artikel in een lege opslaglocatie worden geplaatst. U wijst een opslagsjabloon toe aan een artikel en aan een vestiging.  

## Zie gerelateerde [Microsoft-training](/training/modules/get-started-warehouse-management/)

## Zie ook

[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]