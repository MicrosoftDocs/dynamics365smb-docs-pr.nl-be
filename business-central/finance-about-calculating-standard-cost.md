---
title: Informatie over het berekenen van vaste verrekenprijzen
description: In een vaste-verrekenprijssysteem wordt de voorraadkostprijs bepaald op basis van redelijkerwijs te verwachten of historische kosten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: bholtorf
---
# Informatie over het berekenen van vaste verrekenprijzen

Veel productiebedrijven kiezen een waarderingsbasis voor de vaste verrekenprijs. Dit geldt ook voor bedrijven die lichte productie zoals assemblage en kitting uitvoeren. In een vaste-verrekenprijssysteem wordt de voorraadkostprijs bepaald op basis van redelijkerwijs te verwachten of historische kosten. Onderzoek van in het verleden gebruikte en voor de toekomst geschatte kosten vormen de basis voor de vaste verrekenprijs. Deze prijs ligt vast totdat wordt besloten deze prijs te wijzigen. Het is mogelijk dat de feitelijke productiekosten van een product afwijken van de geschatte vaste verrekenprijs. Vanuit managementoverwegingen wordt de feitelijke prijs voor een bepaald artikel vergeleken met de vaste verrekenprijs en worden eventuele *verschillen* geïdentificeerd en geanalyseerd.  

Vaste verrekenprijzen kunnen worden gehanteerd voor artikelen die worden aangevuld via inkoop, assemblage en productie. Voor elke aanvullingsmethode kunnen vaste verrekenprijzen uit de volgende elementen bestaan.  

|Aanvullingsmethode|Standaardkostenelementen|  
|--------------------------|----------------------------|  
|**Inkoop**|Directe materiaalkosten en overhead-materiaalkosten indien nodig.|  
|**Assemblage**|Directe materiaalkosten, directe of vaste arbeidskosten en overheadkosten.|  
|**Prod.-order**|Directe materiaalkosten, arbeidskosten, uitbestedingskosten en overheadkosten.|  

## Vaste verrekenprijzen instellen

Aangezien de vaste verrekenprijs van een geproduceerd of geassembleerd artikel uit meerdere kostenelementen bestaat, zoals materiaal-, capaciteits- en uitbestedingskosten (directe kosten en overheadkosten), moet de vaste verrekenprijs worden vastgelegd voor al deze elementen.  

Een productiebedrijf dat vaste verrekenprijzen gebruikt, dient twee accountingtaken uit te voeren:  

- Een vaste verrekenprijs schatten voor een voltooid artikel en deze prijs instellen op de artikelkaart.  
- De feitelijke kosten van de belangrijke kostenelementen vastleggen en toewijzen, en een verantwoording afleggen voor verschillen  

De kosten van alle onderdelen moeten bij elkaar worden opgeteld om de directe kosten van een voltooid artikel te kunnen bepalen. Een geassembleerd of geproduceerd artikel kan halffabricaten bevatten, die ook uit meerdere onderdelen bestaan.  

De volgende belangrijke kostenelementen vormen samen de totale directe kosten van een afgewerkt artikel:  

- Materiaalkosten.  
- Capaciteitskosten.  
- Kosten voor uitbesteden van enkel geproduceerde artikelen.  

### Materiaalkosten

Onder materiaalkosten worden de kosten verstaan die te maken hebben met de subassemblages en de aangeschafte grondstoffen. Materiaalkosten kunnen bestaan uit directe en indirecte kostenelementen.  

- Directe materiaalkosten worden gevormd door een gefactureerd bedrag voor aangeschafte grondstoffen of de verwerkingskosten van een subassemblage.  
- Indirecte materiaalkosten (ofwel *overheads*) kunnen bijvoorbeeld bestaan uit de opslagkosten voor voltooide artikelen nadat deze zijn geproduceerd.  

De instelling van de materiaalkosten voor aangeschafte artikelen die invloed hebben op directe en indirecte kosten wordt bepaald door de waarderingsmethode die is geselecteerd voor het opgeven artikel. U stelt kostengegevens in voor beide waarderingsmethoden op de artikelkaart. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

Ook uitvalkosten (alleen productie) vormen een bijkomende factor die moet worden meegewogen bij de berekening van de totale materiaalkosten. Het uitvallen van een bepaalde hoeveelheid grondstoffen tijdens het assembleren of produceren van artikelen zorgt vaak voor een toename van het aantal onderdelen dat nodig is om het artikel te produceren. Dit leidt tot een toename van de materiaalkosten van de onderdelen die worden gebruikt tijdens het produceren van een hoofdartikel. U kunt uitvalkosten voor materialen instellen in de productiestuklijst of in het bewerkingsplan.  

De materiaalkosten van een geproduceerd artikel kunnen worden weergegeven op twee manieren die overeenkomen met de volgende methoden voor het berekenen van de vaste verrekenprijs.  

|Kostenberekeningsbasis|Berekening van materiaalkosten|  
|----------------------------|-------------------------------|  
|Eén niveau|Geproduceerd artikel is gelijk aan de totale kosten van alle ingekochte of via subassemblage verkregen artikelen op de productiestuklijst van dat artikel.|  
|Alle niveaus of meerdere niveaus|Geproduceerd artikel is de som van de materiaalkosten voor alle subassemblages op de stuklijst van dat artikel en de kosten van alle ingekochte artikelen op de productiestuklijst van dat artikel.|  

### Capaciteitskosten

Capaciteitskosten zijn de kosten die te maken hebben met interne kosten voor arbeid en apparatuur. U moet deze kosten voor elke resource (in assemblagebeheer) en werk- of bewerkingsplaats in het bewerkingsplan (in productie) instellen. Net als bij materiaalkosten kunt u directe en indirecte elementen van capaciteitskosten identificeren. De directe kosten van een afdeling kunnen bijvoorbeeld worden gevormd door het vastgestelde tarief voor het uitvoeren van een bepaalde functie. De indirecte kosten van een afdeling kunnen algemene fabrieksonkosten omvatten, zoals verwarming, verlichting e.d. Net als bij de materiaalkosten kunt u capaciteitoverhead uitdrukken als een indirect kostenpercentage of als een vast overheadtarief.  

De instelling van de capaciteitskosten van geassembleerde artikelen bestaat uit de volgende elementen:  

- Directe en indirecte kostprijs van de resource.  
- Soorten vast of direct resourcegebruik.  

De instelling van de capaciteitskosten van geproduceerde artikelen bestaat uit de volgende elementen:  

- Directe en indirecte kostprijs van de bewerkingsplaats of afdeling.  
- Instelling van tijd en lotgrootte.  

Teneinde de standaardcapaciteitskosten te berekenen, moet u de standaardtijdtarieven vaststellen die nodig zijn om bewerkingen uit te voeren in afdelingen en bewerkingsplaatsen. De totale tijd voor het uitvoeren van een bewerking omvat naast de insteltijd en de bewerkingstijd meestal ook de wachttijd na bewerking en de transporttijd.  

U stelt de tarieven voor al deze tijdtypen voor iedere afdeling of bewerkingsplaats in op een afzonderlijke stuklijst.  

> [!NOTE]  
>  Hoewel er tarieven voor de bewerkingstijd worden toegepast per geproduceerd artikel, worden de insteltijdtarieven per lot toegepast. Daarom moet u de insteltijd voor iedere bewerking in de stuklijst evenredig verdelen ten opzichte van de lotgrootte. U geeft de lotgrootte op in het overeenkomstige veld op het sneltabblad **Aanvulling** van de pagina **Artikelkaart**.  

Om insteltijd op het bewerkingsplan aan te geven voor de planning maar deze onkosten niet op te nemen in de berekening van de vaste verrekenprijs, wist u het veld **Kosten inclusief instelling** op de pagina **Productie-instelling**.  

Als van één niveau wordt uitgegaan, zijn dit de arbeidskosten die nodig zijn om het afgewerkte productieartikel te produceren en wordt dit aangegeven op het bewerkingsplan van het productieartikel. Als van meerdere niveaus wordt uitgegaan, zijn dit de capaciteitskosten die voor elk afzonderlijk geproduceerd artikel dat is opgenomen in de stuklijst van het hoofdartikel zijn opgegeven.  

### Uitbestedingskosten

Onder uitbestedingskosten worden de kosten verstaan die betrekking hebben op services die worden geleverd door externe leveranciers of toeleveranciers van een bedrijf. Net als in het geval van de materiaal- en capaciteitskosten kunnen uitbestedingskosten zowel uit directe kosten als uit overheadkosten bestaan. Directe uitbestedingskosten verwijzen naar de feitelijke tarieven voor elke verschafte service. Overheaduitbestedingskosten kunnen bijvoorbeeld transport- of verwerkingskosten zijn die verband houden met een taak die is uitbesteed.  

Aangezien uitbesteding in feite een externe capaciteit is, stelt u de kosten voor uitbestede services (zowel directe als indirecte kosten) in op de afdelingskaart voor de uitbestedingsbewerking.  

## De vaste verrekenprijzen aanpassen

Om de vaste verrekenprijs van assemblageartikelen bij te werken of te berekenen, gebruikt u de functie van de artikelkaart.  

Het proces van bijwerken of berekenen van vaste verrekenprijzen bestaat gewoonlijk uit de volgende taken:  

1.  Kosten bijwerken op het niveau van onderdeel en capaciteit. Zie voor meer informatie de batchverwerkingen **Vaste verrekenprijs artikel voorstellen** en **Vaste verrekenprijs capaciteit voorstellen**.  
2.  Het consolideren en berekenen van de materiaal- en capaciteitskosten om de totale assemblage- of productiekosten van de artikelen te berekenen. Zie voor meer informatie [De vaste verrekenprijs van een assemblageartikel berekenen](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  De vaste verrekenprijzen implementeren die worden ingevoerd wanneer u de vorige batchverwerkingen uitvoert. De vaste verrekenprijzen worden pas van kracht nadat ze zijn geïmplementeerd. Gebruik de batchverwerking **Vaste verrekenprijswijzigingen doorvoeren**, die de wijzigingen in de standaardkosten voor artikelen bijwerkt met die in de tabel Standaardkostenwerkblad.  
4.  De wijzigingen implementeren om het veld **Kostprijs** op de artikelkaart bij te werken en voorraadherwaardering uit te voeren. Zie [Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.

## Zie ook

[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)  
[Vaste verrekenprijs bijwerken](finance-how-to-update-standard-costs.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Werken met stuklijsten](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
