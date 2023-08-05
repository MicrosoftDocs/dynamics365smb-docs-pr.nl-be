---
title: 'Ontwerpdetails: Magazijninstelling'
description: 'Magazijnfunctionaliteit bevat verschillende niveaus van complexiteit, die grotendeels worden bepaald door de opslaglocatie op locatiekaarten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Ontwerpdetails: Magazijninstelling

De magazijnfunctionaliteit in [!INCLUDE[prod_short](includes/prod_short.md)] bevat verschillende niveaus van complexiteit, zoals bepaald door licentiemachtigingen in de aangeboden granules. Het niveau van complexiteit in een magazijnoplossing wordt grotendeels bepaald door de instelling van de opslaglocatie op vestigingskaarten, die zelf wordt bepaald door de licentie. Toegang tot de instellingsvelden voor de opslaglocatie wordt dus gedefinieerd door de licentie. Bovendien bepalen de toepassingsobjecten in de licentie welke UI-documenten moeten worden gebruikt voor de ondersteunde magazijnactiviteiten.  
<!--
The following warehouse-related granules exist:  

- Basic Inventory (4010)  
- Bin (4170)  
- Put Away (4180)  
- Warehouse Receipt (4190)  
- Pick (4200)  
- Warehouse Shipment (4210)  
- Warehouse Management Systems (4620)  
- Internal Picks and Put-aways (4630)  
- Automated Data Capture System (4640)
- Bin Setup (4660)  

For more information about each granule, see [[!INCLUDE[prod_short](includes/prod_short.md)] Price Sheets](https://go.microsoft.com/fwlink/?LinkId=238341) (requires PartnerSource account). -->

In de volgende tabel wordt getoond welke granules vereist zijn om de verschillende niveaus van magazijncomplexiteit te definiëren, welke UI-documenten elk niveau ondersteunen en welke vestigingscode deze niveaus aanduiden in de [!INCLUDE[prod_short](includes/prod_short.md)]-demonstratiedatabase.  

[!INCLUDE [locations-cronus](includes/locations-cronus.md)]

|Complexiteitniveau|Omschrijving|UI-document|Voorbeeldlocatie|Minimale granulevereiste|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|Geen specifieke magazijnactiviteit.<br /><br /> Boekingen vanuit orders ontvangen/verzenden.|Order|BLAUW|Basisvoorraad|  
|2|Geen specifieke magazijnactiviteit.<br /><br /> Boekingen vanuit orders ontvangen/verzenden.<br /><br /> Opslaglocatie is vereist.|Order met opslaglocatiecode|ZILVER|Basisvoorraad/opslaglocatie|  
|3 <br /><br /> **OPMERKING**: hoewel de instellingen **Pick vereist** en **Opslag vereist** worden genoemd, kunt u nog wel ontvangsten en verzendingen rechtstreeks vanuit de bronbedrijfsdocumenten boeken voor vestigingen waarvoor u deze selectievakjes inschakelt.|Elementaire magazijnactiviteit, order-voor-order.<br /><br /> Boeking uit voorraadopslag/pickdocumenten ontvangen/verzenden. <br /><br /> Opslaglocatie is vereist.|Voorraadopslag/Voorraadverplaatsing/Voorraadpick. met opslaglocatiecode|(ZILVER + opslag vereist of opslag vereist)|Basisvoorraad/Opslaglocatie/Opslag/Pick|  
|4|Geavanceerde magazijnactiviteit, voor meerdere orders.<br /><br /> Geconsolideerde ontvangst/verzendboeking op basis van registraties van magazijnopslag/-pick.|Magazijnontvangst/Magazijnopslag/Magazijnpick/Magazijnverzending/Pickvoorstel|GROEN|Basisvoorraad/Magazijnontvangst/Opslag/Pick/Magazijnverzending|  
|5|Geavanceerde magazijnactiviteit, voor meerdere orders.<br /><br /> Geconsolideerde ontvangst/verzendboeking op basis van registraties van magazijnopslag/-pick.<br /><br /> Opslaglocatie is vereist.|Magazijnontvangst/Magazijnopslag/Magazijnpick/Magazijnverzending/Pickvoorstel/Opslagvoorstel met opslaglocatiecode|(GROEN + opslaglocatie verplicht)|Basisvoorraad/Opslaglocatie/Magazijnontvangst/Opslag/Pick/Magazijnverzending|  
|6 <br /><br /> **Opmerking**: dit niveau wordt 'WMS' genoemd, omdat het de meest geavanceerde granule vereist: Warehouse Management Systems.|Geavanceerde magazijnactiviteit, voor meerdere orders<br /><br /> Geconsolideerde ontvangst/verzendboeking op basis van registraties van magazijnopslag/-pick.<br /><br /> Opslaglocatie is vereist.<br /><br /> De zone-/klassecode is optioneel.<br /><br /> Magazijnmedewerkers geleid door werkstroom<br /><br /> Planning aanvulling opslaglocatie<br /><br /> Opslaglocatievolgorde<br /><br /> Instelling opslaglocatie op capaciteit<br /><br /> Plaatsen  <!-- Hand-held device integration -->|Magazijnontvangst/Magazijnopslag/Magazijnpick/Magazijnverzending/Magazijnverplaatsing/Pickvoorstel/Opslagvoorstel/Interne mag.- pick/Interne magazijnopslag met opslaglocatie/klasse/zonecode<br /><br /> Diverse voorstellen voor opslaglocatiebeheer<br /><br /> ADCS-schermen|WIT|Basisvoorraad/Opslaglocatie/Opslag/Magazijnontvangst/Pick/Magazijnverzending/Magazijnbeheersystemen/Interne picks en opslag/Opslaglocatie-instelling/<!-- Automated Data Capture System/ -->Instelling opslaglocatie|  

Zie voor voorbeelden van hoe UI-documenten worden gebruikt per niveau van magazijncomplexiteit [Ontwerpdetails: Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md).  

## Opslaglocatie en inhoud

Een opslaglocatie is een opslagapparaat dat is ontworpen om afzonderlijke onderdelen te bevatten. Het is de kleinste containereenheid in [!INCLUDE[prod_short](includes/prod_short.md)]. Artikelaantallen in opslaglocaties worden opslaglocatie-inhoud genoemd. Een opzoekactie vanuit het veld **Artikel** of het veld **Opslaglocatie** op een magazijngerelateerde documentregel geeft de berekende beschikbaarheid van het artikel op de opslaglocatie weer.  

Aan een opslaglocatie-inhoud kan de eigenschap Vast, Speciaal of Standaard worden gegeven om te definiëren hoe de opslaglocatie-inhoud kan worden gebruikt. Opslaglocaties die geen van deze eigenschappen hebben, worden vrije opslaglocaties genoemd.  

Een vaste opslaglocatie bevat artikelen die aan de desbetreffende opslaglocatiecode zijn toegewezen. De eigenschap Vaste opslaglocatie zorgt dat zelfs als de opslaglocatie-inhoud tijdelijk wordt leeggemaakt, de opslaglocatie-inhoud niet verdwijnt. De opslaglocatie wordt daarom opnieuw geselecteerd zodra het is aangevuld.  

Een toegewezen opslaglocatie bevat opslaglocatie-inhoud die alleen kan worden gepickt voor de specifieke resource, zoals een bewerkingsplaats waar deze opslaglocatie wordt gebruikt. Andere niet-pickinhoud, zoals uitgaande aantallen in een verzendingsboeking, kunnen nog steeds worden verbruikt vanuit een speciale opslaglocatie. Alleen opslaglocatie-inhoud waar door het algoritme **Pick maken** rekening mee wordt gehouden, wordt beschermd in een speciale opslaglocatie.  

De eigenschap Standaardopslaglocatie wordt door het systeem gebruikt om opslaglocaties voor magazijnactiviteiten voor te stellen. Bij WMS-vestigingen wordt de eigenschap Standaardopslaglocatie niet gebruikt. Bij vestigingen waar opslaglocaties vereist zijn, wordt de eigenschap in inkomende stromen gebruikt om op te geven waar artikelen moeten worden geplaatst. In uitgaande stromen wordt de eigenschap gebruikt om op te geven waar artikelen vandaan moeten worden gehaald.  

> [!NOTE]  
>  Als de uitgaande artikelen in verschillende opslaglocaties worden geplaatst, worden artikelen eerst uit de niet-standaardopslaglocaties gehaald, om die te legen, en vervolgens worden de resterende artikelen uit de standaardopslaglocatie gehaald.  

Er kan slechts één standaardopslaglocatie per artikel per vestiging zijn.  

## Opslaglocatiesoort

In WMS-installaties kunt u de magazijnactiviteiten die voor een opslaglocatie toegestaan zijn, beperken door er een opslaglocatiesoort aan toe te wijzen. De volgende typen opslaglocaties bestaan:  

|Opslaglocatiesoort|Omschrijving|  
|------------------|---------------------------------------|  
|ONTVANGST|Artikelen worden geboekt als ontvangen, maar worden nog niet opgeslagen.|  
|VERZENDEN|Artikelen die zijn gepickt voor magazijnverzendregels, maar die nog niet zijn geboekt als verzonden.|  
|OPSLAG|Meestal items die in grote eenheden worden opgeslagen, maar die u niet wilt picken. Aangezien deze opslaglocaties niet worden gebruikt voor het picken, hetzij voor productieorders of verzendingen, is het gebruik van een opslaglocatie voor opslag mogelijk beperkt, maar deze opslaglocatiesoort kan nuttig zijn indien u een grote hoeveelheid items hebt aangeschaft. Dit soort opslaglocaties moeten altijd een lage rangschikking van opslaglocaties hebben, zodat wanneer ontvangen artikelen opgeslagen zijn, andere opslaglocaties van het type OPSLAGPICK- met een hogere rangschikking- die bij het item horen eerder opgeslagen worden. Indien u dit type opslaglocatie gebruikt, moet u regelmatig een opslaglocatieaanvulling uitvoeren, zodat de items in deze opslaglocaties ook beschikbaar zijn in de opslaglocaties van het type OPSLAGPICK of PICK.|  
|PICK|Artikelen die alleen voor picken moeten worden gebruikt. De aanvulling van deze opslaglocaties kan alleen worden gemaakt via verplaatsing, niet via opslag.|  
|OPSL-PICK|Artikelen in opslaglocaties die worden voorgesteld voor de opslag- en pickfuncties. Opslaglocaties van dit soort beschikken waarschijnlijk over verschillende zonevolgordes. U kunt locaties voor bulkopslag bijvoorbeeld instellen als een laaggeclassificeerde versie van dit soort, in tegenstelling tot de normale pickopslaglocaties of een pickopslaggebied.|  
|QC|Deze opslaglocatie wordt gebruikt voor voorraadaanpassing indien u deze opslaglocatie opgeeft in het veld **Code aanpassing opslaglocatie** op de locatiekaart. U kunt dit soort locaties ook instellen voor defecte artikelen en artikelen die worden geïnspecteerd. Als u bepaalde artikelen ontoegankelijk wilt maken voor de normale artikelenstroom, kunt u de artikelen eveneens verplaatsen naar dit soort opslaglocatie. **OPMERKING:**  in tegenstelling tot alle andere soorten opslaglocaties is bij de opslaglocatie van het type **QC** geen enkel selectievakje voor de verwerking van artikelen standaard ingeschakeld. Dit geeft aan dat alle inhoud die u in een opslaglocatie van QC plaatst uitgesloten is van de stroom van artikelen.|  

Voor alle opslaglocatiesoorten, behalve PICK, OPSL-PICK en OPSLAG, is geen andere activiteit voor de opslaglocatie toegestaan dan wat is gedefinieerd voor de opslaglocatiesoort. Een opslaglocatie van de soort **Ontvangen** kan bijvoorbeeld alleen worden gebruikt om artikelen te ontvangen of artikelen uit te picken.  

> [!NOTE]  
> Alleen verplaatsing kan worden uitgevoerd naar opslaglocaties van de soort ONTVANGT en QC. Zo kunnen ook alleen verplaatsingen tussen opslaglocaties van het type VERZENDING en QC worden gemaakt.  

## Opslaglocatievolgorde

In geavanceerde magazijnomgevingen kunt u automatiseren en optimaliseren hoe artikelen in opslag en pickvoorstellen worden verzameld door opslaglocaties een rangorde te geven zodat artikelen worden voorgesteld, gebruikt of geplaatst op basis van rangordecriteria, zodat magazijnruimte optimaal wordt gebruikt.  

Opslagprocessen worden geoptimaliseerd op rangorde van opslaglocaties doordat opslaglocaties met een hogere rangorde worden voorgesteld vóór opslaglocaties met een lagere rangorde. Zo worden pickprocessen ook geoptimaliseerd doordat eerst artikelen worden voorgesteld uit opslaglocaties met een hoge rangorde. Bovendien worden aanvullingen van opslaglocaties voorgesteld van opslaglocaties met een lagere rangorde naar opslaglocaties met een hogere rangorde.  

De opslaglocatievolgorde en de inhoudsinformatie over de opslaglocatie zijn de basiseigenschappen waarmee gebruikers artikelen in het magazijn kunnen plaatsen.  

## Instelling opslaglocatie  
Bij geavanceerde magazijnen kunnen opslaglocaties worden ingesteld met capaciteitswaarden, zoals aantal, totale kubieke inhoud en gewicht, om te bepalen welke artikelen op welke manier worden opgeslagen in de opslaglocatie.  

Op elke artikelkaart kunt u een eenheid (UOM) voor het artikel toewijzen, bijvoorbeeld stuks, pallets, liters, grammen of dozen. U kunt ook een basiseenheid voor een artikel hebben en grotere UOM's opgeven die hierop zijn gebaseerd. U kunt bijvoorbeeld een pallet van 16 stuks definiëren. Stuks is de basiseenheid.  

Als u het maximale aantal van een bepaald artikel wilt instellen dat in een bepaalde opslaglocatie moet worden opgeslagen, en het artikel meerdere eenheden heeft, moet u het maximale aantal instellen voor elke eenheid die voorkomt op de artikelkaart. Als een artikel is ingesteld om te worden verwerkt in stuks en pallets, moet het veld **Max. aantal** op de pagina **Opslaglocatie-inhoud** voor dat artikel tevens in pallets en stuks zijn. Anders wordt het toegestane aantal voor die opslaglocatie niet correct berekend.  

Voordat u capaciteitsbeperkingen instelt voor inhoud van een opslaglocatie, moet u eerst zorgen dat de eenheid en de dimensies van het artikel zijn ingesteld op de artikelkaart.  

> [!NOTE]  
> Er kan alleen met meerdere eenheden worden gewerkt in WMS-installaties. In alle andere configuraties kan opslaglocatie-inhoud alleen worden uitgedrukt in de basiseenheid. In alle transacties met een hogere maateenheid dan de basismaateenheid van het artikel wordt het aantal geconverteerd naar de basismaateenheid.  

## Regio

In geavanceerde magazijnomgevingen kunnen opslaglocaties in zones worden gegroepeerd om te beheren hoe de werkstroom van magazijnactiviteiten wordt gedirigeerd.  

Een zone kan een ontvangstzone of een bevoorradingszone zijn en elke zone kan uit een of meer opslaglocaties bestaan.  

De meeste eigenschappen die zijn toegewezen aan een zone, worden standaard toegewezen aan de opslaglocatie die vanuit die zone wordt gemaakt.  

## Klasse  
In geavanceerde magazijnomgevingen kunt u codes van magazijnklassen toewijzen aan artikelen, opslaglocaties en zones om te bepalen waar verschillende klassen artikelen worden opgeslagen, zoals bevroren goederen. U kunt een zone in verschillende magazijnklassen verdelen. Artikelen in de ontvangstzone kunnen bijvoorbeeld worden opgeslagen als vast, gevaarlijk of een andere klasse.  

Als u magazijnklassen en een standaardopslaglocatie voor ontvangst/verzending gebruikt, moet u de gewenste opslaglocaties in de ontvangst- en verzendingsregels voor het magazijn handmatig invullen.  

In inkomende stromen wordt de klassecode alleen gemarkeerd op inkomende regels waar de artikelklassecode niet overeenkomt met de standaardopslaglocatie. Als de juiste standaardopslaglocaties niet zijn toegewezen, kan het aantal niet worden ontvangen.  

## Vestiging

Een locatie is een fysieke structuur of plaats waar de voorraad wordt ontvangen, opgeslagen en verzonden, en mogelijk in opslaglocaties wordt geordend. Een locatie kan een magazijn, serviceauto, toonzaal, fabriek of een gebied in een fabriek zijn.  

## First-Expired-First-Out (Eerst-vervallen-eerst-uit)

Als u het selectievakje **Picken volgens FEFO** inschakelt op het sneltabblad **Opslaglocatiebeleid** op de vestigingskaart, worden artikelgetraceerde artikelen gepickt op basis van de vervaldatum. De artikelen met de vroegste vervaldatums worden eerst gepickt.  

Magazijnactiviteiten in alle pick- en verplaatsingsdocumenten worden gesorteerd volgens FEFO, tenzij aan de desbetreffende artikelen al serie-/lotnummers zijn toegewezen. Als aan slechts een gedeelte van het aantal op de regel al serie/lot-nummers zijn toegewezen, wordt het resterende te picken aantal gesorteerd op basis van FEFO.  

Bij picken volgens FEFO worden beschikbare artikelen eerst verzameld in een tijdelijke artikeltraceringslijst op basis van de vervaldatum. Als twee artikelen dezelfde vervaldatum hebben, wordt het artikel met het laagste lot- of serienummer het eerste gepickt. Als de lot- of serienummers gelijk zijn, wordt het artikel dat als eerste is geregistreerd, als eerste geselecteerd. Standaardcriteria voor het selecteren van artikelen in pickopslaglocaties, zoals opslaglocatievolgorde en splitsen van bulkgoederen, worden toegepast op deze tijdelijke FEFO-artikeltraceringslijst.  

## Opslagsjabloon

De opslagsjabloon kan worden toegewezen aan een artikel en aan een vestiging. De opslagsjabloon geeft een set prioriteitsregels op die moeten worden aangehouden bij het maken van opslagactiviteiten. Een opslagsjabloon kan bijvoorbeeld vereisen dat het artikel wordt geplaatst in een opslaglocatie met opslaglocatie-inhoud die overeenkomt met de maateenheid en als geen soortgelijke opslaglocatie met voldoende capaciteit kan worden gevonden, moet het artikel in een lege opslaglocatie worden geplaatst.  

## Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Ontwerpdetails: Beschikbaarheid in het magazijn](design-details-availability-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]