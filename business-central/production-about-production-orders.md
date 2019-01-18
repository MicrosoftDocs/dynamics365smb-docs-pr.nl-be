---
title: Informatie over productieorders | Microsoft Docs
description: Productieorders worden gebruikt voor het beheren van de conversie van ingekochte materialen naar geproduceerde artikelen. Productieorders (project- of werkorders) leiden het werk door verschillende faciliteiten (afdelingen of bewerkingsplaatsen) op de shopfloor.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 1c534f16c1e69840912e42c30bbcae2d6496b373
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="about-production-orders"></a>Informatie over productieorders
Productieorders worden gebruikt voor het beheren van de conversie van ingekochte materialen naar geproduceerde artikelen. Productieorders leiden het werk door verschillende afdelingen of bewerkingsplaatsen op de shopfloor.  

Voordat wordt doorgegaan met de productie, voeren de meeste bedrijven een voorraadplanning uit, doorgaans een keer in de week, om te berekenen hoeveel productieorders en inkooporders moeten worden uitgevoerd om te voldoen aan de verkoopvraag van die week. Inkooporders vullen de componenten aan die volgens de productiestuklijst vereist zijn om de eindartikelen te produceren.

Productieorders vormen de centrale onderdelen van de productiefunctionaliteit van het programma en bevatten de volgende informatie:  

-   Producten die zijn gepland voor productie  
-   Materialen die nodig zijn voor de geplande productieorders  
-   Producten die zojuist zijn geproduceerd  
-   Materialen die al zijn geselecteerd  
-   Producten die in het verleden zijn geproduceerd  
-   Materialen die in eerdere productiebewerkingen zijn gebruikt  

Productieorders vormen het beginpunt voor:  

-   Plannen van toekomstige productie  
-   Sturen van de huidige productie  
-   Traceren van gereedgemelde productie  

## <a name="production-order-creation"></a>Productieorders opstellen  
Productieorders kunnen handmatig worden opgesteld op basis van order voor order vanuit de pagina **Productieorder** of kunnen worden gegenereerd vanuit de pagina **Verkooporderplanning** of **Orderplanning**. Meerdere orders worden opgesteld vanuit de pagina **Planningsvoorstel**.  

Productieorders worden opgesteld met informatie uit:  

- Artikelen  
- Productiestuklijsten
- Bewerkingsplannen  
- Bewerkingsplaatsen  
- Afdelingen  

## <a name="limitations-on-production-order-creation"></a>Beperkingen aangaande het opstellen van productieorders  
Productieorders worden automatisch gereserveerd en getraceerd naar de bron wanneer:  

-   Opgesteld vanuit het **Planningsvoorstel**  
-   Gemaakt met behulp van de orderfunctie op de pagina **Verkooporderplanning**  
-   Gemaakt vanuit de pagina **Orderplanning**  
-   Met behulp van de functie **Herplannen** in productieorders  

Zie [Relatie tussen vraag en voorzieningen bijhouden](production-how-track-demand-supply.md) voor meer informatie.

Productieorders die op een andere manier tot stand komen, worden niet automatisch gereserveerd en getraceerd.   

## <a name="production-order-status"></a>Productieorderstatus  
De productieorderstatus bepaalt hoe de productieorder wordt behandeld in het programma. De vorm en inhoud van de productie worden bepaald door de status van de order. Afhankelijk van de status worden de productieorders op verschillende pagina's weergegeven. U kunt de status van een productieorder niet handmatig wijzigen; dit gebeurt met de functie **Status wijzigen**.  

### <a name="simulated-production-order"></a>Gesimuleerde productieorder  
Een gesimuleerde productieorder is uniek vanwege de volgende kenmerken:  

- Zoals de naam al aangeeft, is het een simulatie en wordt deze vooral gebruikt voor het maken van offertes en waarderingen, bijvoorbeeld wanneer de afdeling Onderzoek en Ontwikkeling een kostenschatting wil hebben voor een voorgesteld artikel. Een gesimuleerde productieorder dient als voorbeeld voor een productieorder.  
- Deze order heeft geen invloed op het plannen van orders. Planning (MPS en MRP) houdt geen rekening met en wordt ook niet beïnvloed door gesimuleerde productieorders. Een gesimuleerde productieorder kan ook niet worden gebruikt als sjabloon, omdat deze verdwijnt zodra u de status wijzigt.  

### <a name="planned-production-order"></a>Geplande productieorder  
Een geplande productieorder is uniek vanwege de volgende kenmerken:  

- U kunt een geplande productieorder automatisch opstellen op basis van een verkooporder.  
- Geplande productieorders lijken op vrijgegeven productieorders en leveren input voor de capaciteitsplanning door de totale capaciteitsvereisten weer te geven per afdeling of bewerkingsplaats.  
- Een geplande productieorder geeft de best schatting van de toekomstige werklast van de afdeling of bewerkingsplaats weer, op basis van de beschikbare informatie. Ze worden normaliter gegenereerd vanuit de planning, maar kunnen ook handmatig worden opgesteld. Omdat ze tijdens de volgende planningsstadia worden gewist, is handmatig opstellen niet praktisch.  
- Het genereren ervan tijdens de planning resulteert in een voorgestelde "geplande ordervrijgave" die het aantal, de vrijgavedatum en de vervaldatum omvat. De logica van het planningssysteem is gebaseerd op de aanvullingsmethode, het bestelbeleid en orderwijzigingen die het systeem tegenkomt tijdens het plannen van de nettobehoefte.  
- Als u de invloed ervan wilt bekijken, kijkt u naar de werklast voor elke afdeling of bewerkingsplaats in het bewerkingsplan van de geplande productieorder.  

### <a name="firm-planned-production-order"></a>Vast geplande productieorder  
Een vast geplande productieorder is uniek vanwege de volgende kenmerken:  

- U kunt een vast geplande productieorder automatisch opstellen op basis van een verkooporder.  
- Een vast geplande productieorder kan dienstdoen als tijdelijke aanduiding in het planningsschema voor een toekomstig project dat wordt vrijgegeven aan de shopfloor.  
- Een vast geplande productieorder kan worden gegenereerd vanuit de planning of kan handmatig of vanuit verkooporders worden opgesteld. Ze worden tijdens de volgende planning niet gewist.  
- Het genereren ervan tijdens de planning resulteert in een voorgestelde "geplande ordervrijgave" die het aantal, de vrijgavedatum en de vervaldatum omvat. De logica van het planningssysteem is gebaseerd op de aanvullingsmethode, het bestelbeleid en orderwijzigingen die het systeem tegenkomt tijdens het plannen van de nettobehoefte.  
- Als u de invloed ervan wilt bekijken, kijkt u naar de werklast voor elke afdeling of bewerkingsplaats in het bewerkingsplan van de vast geplande productieorder.  

### <a name="released-production-order"></a>Vrijgegeven productieorder  
Een vrijgegeven productieorder is uniek vanwege de volgende kenmerken:  

- U kunt een vrijgegeven productieorder automatisch opstellen op basis van een verkooporder.  
- Wanneer een productieorder is vrijgegeven, betekent dit niet noodzakelijkerwijs dat er materialen zijn gepickt of dat het project fysiek naar de eerste bewerking is gegaan.  
- In een MTO (Make-to-Order)-omgeving, is het niet ongebruikelijk om onmiddellijk na het invoeren van de verkooporder een vrijgegeven productieorder op te stellen.  
- Het werkelijke materiaalverbruik en de productoutput kunnen handmatig worden vastgelegd met een vrijgegeven productieorder. Daarnaast vindt automatische afboeking van verbruik en productoutput alleen plaats voor vrijgegeven productieorders.  

### <a name="finished-production-order"></a>Gereedgemelde productieorder  
Een gereedgemelde productieorder is uniek vanwege de volgende kenmerken:  

- Een gereedgemelde productieorder is normaliter een productieorder die is geproduceerd.  
- Het gereedmelden van de productieorder is een belangrijke taak in het voltooien van de levenscyclus van de waardering van het artikel dat wordt geproduceerd. Door een productieorder gereed te melden, kan de waardering worden bijgewerkt en gereconcilieerd.  
- Gereedgemelde productieorders worden gebruikt voor statistische rapportage en ter ondersteuning van de mogelijkheid om terug te traceren naar andere orders (bijvoorbeeld verkoop-, productie- en inkooporders). Met de mogelijkheid om terug te traceren naar een gereedgemelde productieorder kunt u de gedetailleerde historie bekijken.  
- Gereedgemelde productieorders kunnen nooit worden gewijzigd.  

## <a name="production-order-execution"></a>Uitvoering van productieorders  
Wanneer een productieorder is opgesteld en gepland, moet deze worden vrijgegeven aan de shopfloor om te worden uitgevoerd. Tijdens het uitvoeren van de order wordt het volgende vastgelegd:  

- Materialen die zijn gepickt of verbruikt  
- Hoeveel tijd er is besteed aan het werken aan de order  
- Het aantal hoofdartikelen dat is geproduceerd  

Deze informatie kan handmatig worden vastgelegd of via automatische rapportage, volgens de instelling van de artikelen in het veld Afboekingsmethode.  

### <a name="material-consumption"></a>Materiaalverbruik  
Het programma biedt diverse opties voor de manier waarop een productiebedrijf mogelijk materiaalverbruik wil vastleggen. Het materiaalverbruik kan bijvoorbeeld handmatig worden geregistreerd. Dit is bijvoorbeeld wenselijk wanneer er vaak onderdelen moeten worden vervangen of er een hoger uitvalpercentage is dan verwacht.  

Het materiaalverbruik kan worden verwerkt via het verbruiksdagboek, maar kan ook automatisch worden geregistreerd door het programma. Dit wordt automatische rapportage genoemd. De rapportagemethoden zijn als volgt: De rapportagemethoden zijn:  

-   Handmatig  
-   Voorwaarts  
-   Achterwaarts  

Bij handmatige verbruiksrapportage wordt gebruikgemaakt van het verbruiksdagboek om het picken van materiaal te specificeren.  

Bij voorwaartse verbruiksrapportage wordt ervan uitgegaan dat de verwachte aantallen van alle materialen van de hele order automatisch worden verbruikt bij de vrijgave van een productieorder, tenzij gebruik wordt gemaakt van bewerkingsplankoppelingen. Wanneer bewerkingsplankoppelingen worden gebruikt, wordt het materiaal dat wordt verbruikt bij het begin van de bewerkingsstap geregistreerd in het Outputdagboek. Om de hele productieorder voorwaarts af te boeken, moet u twee dingen doen:  

- Voor alle artikelen in de productiestuklijst op het hoogste niveau moet voorwaarts afboeken worden geselecteerd op de betreffende artikelkaart.  
- Alle bewerkingsplankoppelingen op de productiestuklijst moeten worden verwijderd.  

Bij achterwaartse verbruiksrapportage worden de werkelijke aantallen geregistreerd van alle materialen die zijn gepickt of verbruikt wanneer de status van een productieorder wordt gewijzigd in *Gereedgemeld*, tenzij bewerkingsplankoppelingen worden gebruikt. Wanneer bewerkingsplankoppelingen worden gebruikt, wordt het materiaal verbruikt nadat een aantal van de hoofdartikelen wordt geregistreerd voor de bewerkingsstap in het Outputdagboek.  

Wanneer de productieorder wordt bijgewerkt, wordt de afboekingsmethode gekopieerd van de artikelkaart. Omdat de afboekingsmethode voor elk onderdeel van de productieorder bepaalt hoe en wanneer het verbruik wordt geregistreerd, is het belangrijk te weten dat u de afboekingsmethode voor specifieke artikelen direct kunt wijzigen in de productieorder.  

#### <a name="automatic-consumption-posting-flushing"></a>Automatisch verbruik boeken (afboeken)  
Het voordeel van automatisch afboeken is dat de invoer van gegevens sterk wordt beperkt. Met de mogelijkheid om een bewerking automatisch af te boeken, kan het hele verbruik- en outputregistratieproces worden geautomatiseerd. Het nadeel van automatisch afboeken is dat u mogelijk dat u uitval niet nauwkeurig registreert, of zelfs niet eens opmerkt. De automatische rapportagemethoden zijn als volgt:  

- De hele order voorwaarts afboeken  
- Voorwaarts afboeken per bewerking  
- Achterwaarts afboeken per bewerking  
- De hele order achterwaarts afboeken  

#### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automatische rapportage - de hele order voorwaarts afboeken  
Als u de productieorder voorwaarts afboekt bij het begin van het project, werkt het programma op vergelijkbare wijze als bij handmatig verbruik. Het belangrijkste verschil is dat het verbruik automatisch plaatsvindt.  

- De volledige inhoud van de productiestuklijst wordt verbruikt en afgetrokken van de voorraad op het moment waarop de vrijgegeven productieorder wordt bijgewerkt.  
- Het verbruikte aantal is het aantal per montage zoals vermeld op de productiestuklijst, vermenigvuldigd met het aantal hoofdartikelen dat u maakt.  
- U hoeft geen informatie vast te leggen in het verbruiksdagboek als alle artikelen moeten worden afgeboekt.  
- Wanneer artikelen vanuit de voorraad worden verbruikt, maakt het niet uit wanneer outputdagboekposten worden aangemaakt, want het outputdagboek heeft geen effect op deze manier van verbruikboeking.  
- Er kunnen geen bewerkingsplankoppelingen worden ingesteld.  

Het voorwaarts afboeken van een hele order is nuttig in productieomgevingen met:  

-   Een klein aantal beschadigde artikelen  
-   Een klein aantal bewerkingen  
-   Hoog materiaalverbruik in eerste bewerkingen  

#### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automatische rapportage - voorwaarts afboeken per bewerking  
Bij afboeken per bewerking kunt u voorraad aftrekken tijdens een specifieke bewerking in het bewerkingsplan van het hoofdartikel. Materiaal wordt gekoppeld aan het bewerkingsplan met behulp van bewerkingsplankoppelingen, die overeenkomen met de bewerkingsplankoppelingen die worden toegepast op onderdelen in de productiestuklijst.  

De afboeking vindt plaats wanneer de bewerking die dezelfde bewerkingsplankoppeling heeft, wordt gestart. Gestart betekent dat enige activiteit is geregistreerd in het outputdagboek voor die bewerking. En die activiteit kan ook bestaan uit het invoeren van een insteltijd.  

Het bedrag van de afboeking is voor het aantal per montage dat vermeld staat op de productiestuklijst, vermenigvuldigd met het aantal hoofdartikelen dat wordt gemaakt (verwachte aantal).  

Deze techniek kan het beste worden toegepast wanneer er veel bewerkingen zijn en bepaalde onderdelen pas later in de montagevolgorde nodig zijn. In feite kan het bij een Just-in-Time (JIT)-omgeving zelfs zo zijn dat de artikelen niet eens voorhanden zijn wanneer de RPO van start gaat.  

Materiaal kan tijdens bewerkingen worden verbruikt met behulp van bewerkingsplankoppelingen. Sommige onderdelen worden mogelijk pas gebruikt bij de eindmontage en mogen pas op dat moment aan de voorraad worden onttrokken.  

#### <a name="automatic-reporting---back-flushing-by-operation"></a>Automatische rapportage - achterwaarts afboeken per bewerking  
Bij achterwaarts afboeken per bewerking wordt het verbruik geregistreerd nadat de bewerking in het outputdagboek is geboekt.  

Het voordeel van deze methode is dat het aantal hoofdonderdelen dat is gereedgemeld in de bewerking bekend is.  

Het materiaal in de productiestuklijst wordt gekoppeld aan de bewerkingsplanrecords met behulp van bewerkingsplankoppelingen. Het achterwaarts afboeken vindt plaats wanneer een bewerking met een bepaalde bewerkingsplankoppeling wordt geboekt met een gereedgemeld aantal.  

Het bedrag van de afboeking is voor het aantal per montage dat vermeld staat op de productiestuklijst, vermenigvuldigd met het aantal hoofdartikelen dat is geboekt als outputaantal bij die bewerking. Dit kan afwijken van het verwachte aantal.  

#### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automatische rapportage - de hele order achterwaarts afboeken  
Bij deze rapportagemethode wordt geen rekening gehouden met bewerkingsplankoppelingen.  

Er worden geen onderdelen gepickt totdat de status van de vrijgegeven productieorder is gewijzigd in *Gereedgemeld*. Het bedrag van de afboeking is het aantal per montage dat vermeld staat op de productiestuklijst, vermenigvuldigd met het aantal hoofdartikelen dat is gereedgemeld en in voorraad is geplaatst.  

Voor achterwaarts afboeken van de hele productieorder moeten dezelfde instellingen worden gebruikt als bij voorwaarts afboeken: de rapportagemethode moet worden ingesteld op achterwaarts bij elk artikel voor alle artikelen in de hoofdstuklijst waarvoor de rapportage is bedoeld. Bovendien moeten alle bewerkingsplankoppelingen zijn verwijderd uit de productiestuklijst.  

### <a name="production-output"></a>Productieoutput  
Het programma biedt u de mogelijkheid om te traceren hoeveel werktijd wordt besteed aan een productieorder, naast het registreren van het aantal dat is geproduceerd. Met behulp van deze informatie kunt u de productiekosten nauwkeuriger bepalen. Daarnaast willen producenten die gebruikmaken van een standaard waarderingssysteem misschien de werkelijke informatie registreren om daarmee betere standaarden te kunnen ontwikkelen.  

De output kan worden verwerkt via het outputdagboek, maar kan ook automatisch worden geregistreerd door het programma. Het programma kopieert bij het bijwerken de afboekingsmethode van de bewerkingsplaats of de afdeling naar het productieorderbewerkingsplan. Net als bij het materiaalverbruik zijn er drie rapportagemethoden voor output:  

- Handmatig  
- Voorwaarts  
- Achterwaarts  

Bij de handmatige methode wordt gebruikgemaakt van het outputdagboek om de verbruikte tijd en het geproduceerde aantal te specificeren.  

Bij de voorwaartse methode wordt de verwachte output (en tijd) geregistreerd, die automatisch wordt vastgelegd bij de vrijgave van een productieorder. Bewerkingsplankoppelingen zijn geen factor bij het voorwaarts afboeken van de output.  

Bij de achterwaartse methode wordt de verwachte output (en tijd) geregistreerd, die automatisch wordt vastgelegd bij de gereedmelding van een productieorder. Bewerkingsplankoppelingen zijn geen factor bij het achterwaarts afboeken van de output.  

### <a name="posting-consumption-and-output"></a>Verbruik en output boeken  
U kunt elke combinatie van automatische afboeking en handmatig geregistreerde informatie gebruiken voor zowel verbruik als output. U kunt bijvoorbeeld onderdelen automatisch voorwaarts afboeken, maar toch nog gebruikmaken van het verbruiksdagboek om uitval te registreren. Of wellicht wilt u de output automatisch registreren, maar het outputdagboek gebruiken voor de registratie van uitval van het hoofdartikel of de extra tijd die aan de order is besteed.  

Tot slot is het zo dat als u het verbruik en de output handmatig invoert, u moet bepalen in welke volgorde u deze informatie wilt vastleggen. U kunt eerst het verbruik registreren en met behulp van een snelkoppelingsmethode de informatie invoeren die is gebaseerd op het verwachte aantal van de output. Of u kunt eerst de output invoeren, met behulp van de functie **Bewerkingsplan weergeven**. U registreert dan het verbruik op basis van het werkelijke aantal van de output.  

### <a name="production-journal"></a>Productiedagboek  
Het productiedagboek combineert de functies van het verbruiksdagboek en outputdagboeken in één dagboek, dat direct toegankelijk is vanuit de vrijgegeven productieorder.  

Het doel van het productiedagboek is het bieden van één interface waarin u het verbruik en de output van een productieorder kunt registreren.  

Het productiedagboek heeft een eenvoudige weergave en biedt u de volgende mogelijkheden:  

- Op eenvoudige wijze de output en het verbruik met betrekking tot een productieorder registreren  
- De onderdelen koppelen aan bewerkingen  
- De werkelijke bewerkingsgegevens koppelen aan de standaardschattingen op het productieorderbewerkingsplan en de onderdeelregels  
- Een overzicht boeken en afdrukken van geregistreerde bewerkingsgegevens voor de productieorder  

Met het productiedagboek worden veel van de functies uitgevoerd die ook met het verbruiks- en outputdagboek worden uitgevoerd. Dimensies, artikeltracering en opslaglocatie-inhoud worden op dezelfde manier afgehandeld als in het verbruiks- en het outputdagboek.  

Het productiedagboek verschilt echter als volgt van het verbruiks- en outputdagboek:  

- Het dagboek wordt direct vanuit een vrijgegeven productieorder geopend. De gegevens van die order worden automatisch ingesteld in het dagboek.  
- U kunt aangeven welke soorten materialen worden verwerkt op basis van een afboekingsmethodefilter in het dagboek.  
- Aantallen en tijden die al voor de order zijn geboekt, worden onder in het dagboek als werkelijke posten weergegeven.  
- Velden waarvoor gegevensinvoer niet relevant is, zijn leeg en kunnen niet worden bewerkt.  
- U kunt aangeven hoe outputaantallen vooraf worden ingesteld in het dagboek, bijvoorbeeld dat de laatste bewerking nul als outputaantal moet hebben.  
- Als u het dagboek afsluit zonder uw wijzigingen te boeken, verschijnt er een bericht met de vraag of u het dagboek werkelijk wilt sluiten. Zo kunt u toch in het dagboek blijven.  
- Het dagboek biedt een overzicht van het productieproces, met een logische structuur waarin bewerkingen en materialen overzichtelijk worden weergegeven.  

In het productiedagboek worden verbruiksaantallen geboekt als negatieve artikelposten, outputaantallen worden geboekt als positieve artikelposten en bestede tijd wordt geboekt als capaciteitspost.  

## <a name="see-also"></a>Zie ook
[Productie](production-manage-manufacturing.md)    
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

