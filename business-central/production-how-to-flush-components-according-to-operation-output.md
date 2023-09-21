---
title: Onderdelen afboeken op basis van de uitvoer van een bewerking
description: In dit onderwerp wordt beschreven hoe u componenten moet afboeken op basis van de bewerkingsoutput en andere betrokken afboekingsmethoden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="flush-components-according-to-operation-output"></a>Onderdelen afboeken op basis van de uitvoer van een bewerking
U kunt verschillende afboekingsstrategieën definiëren om de registratie van het verbruik van componenten te automatiseren. 

Deze functionaliteit is handig om de volgende redenen:  

- **Voorraadwaardering**

    Waardeposten voor uitvoer en verbruik worden parallel geproduceerd naarmate de productieorder vordert. Zonder bewerkingsplankoppelingen neemt de voorraadwaarde toe als uitvoer wordt geboekt en vervolgens op een later tijdstip weer af wanneer de waarde van het materiaalverbruik wordt geboekt samen met de gereedgemelde productieorder.  
- **Beschikbaarheid van voorraad**

    Bij geleidelijke verbruiksboeking is de beschikbaarheid van artikelonderdelen meer actueel, hetgeen belangrijk is voor het handhaven van het interne evenwicht tussen vraag en aanbod. Zonder bewerkingsplankoppelingen kan bij andere vraag naar het materiaal de misvatting ontstaan dat het materiaal beschikbaar is zolang een vertraagde verbruiksboeking uitstaat.  
- **Just In Time**

    Via de mogelijkheid om producten aan te passen aan de vraag van de klant kunt u verspilling tot een minimum beperken door ervoor te zorgen dat werk en systeemwijzigingen alleen optreden wanneer het nodig is.  

- **Gegevensinvoer verminderen**

    Met de mogelijkheid om een bewerking automatisch af te boeken, kan het hele verbruik- en outputregistratieproces worden geautomatiseerd. Het nadeel van automatisch afboeken is dat u mogelijk dat u uitval niet nauwkeurig registreert, of zelfs niet eens opmerkt.

## <a name="automatic-consumption-posting-flushing-methods"></a>Methoden voor automatisch verbruik boeken (afboeken)

- De hele order voorwaarts afboeken  
- Voorwaarts afboeken per bewerking  
- Achterwaarts afboeken per bewerking  
- De hele order achterwaarts afboeken  

### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automatische rapportage - de hele order voorwaarts afboeken
Als u de productieorder voorwaarts afboekt bij het begin van het project, werkt de toepassing op vergelijkbare wijze als bij handmatig verbruik. Het belangrijkste verschil is dat het verbruik automatisch plaatsvindt.  

- De volledige inhoud van de productiestuklijst wordt verbruikt en afgetrokken van de voorraad op het moment waarop de vrijgegeven productieorder wordt bijgewerkt.  
- Het verbruikte aantal is het aantal per montage zoals vermeld op de productiestuklijst, vermenigvuldigd met het aantal hoofdartikelen dat u maakt.  
- U hoeft geen informatie vast te leggen in het verbruiksdagboek als alle artikelen moeten worden afgeboekt.  
- Wanneer artikelen vanuit de voorraad worden verbruikt, maakt het niet uit wanneer outputdagboekposten worden aangemaakt, want het outputdagboek heeft geen effect op deze manier van verbruikboeking.  
- Er kunnen geen bewerkingsplankoppelingen worden ingesteld.  

Het voorwaarts afboeken van een hele order is nuttig in productieomgevingen met:  

-   Een klein aantal beschadigde artikelen  
-   Een klein aantal bewerkingen  
-   Hoog materiaalverbruik in eerste bewerkingen  

### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automatische rapportage - voorwaarts afboeken per bewerking
Bij afboeken per bewerking kunt u voorraad aftrekken tijdens een specifieke bewerking in het bewerkingsplan van het hoofdartikel. Materiaal wordt gekoppeld aan het bewerkingsplan met behulp van bewerkingsplankoppelingen, die overeenkomen met de bewerkingsplankoppelingen die worden toegepast op onderdelen in de productiestuklijst.  

De afboeking vindt plaats wanneer de bewerking die dezelfde bewerkingsplankoppeling heeft, wordt gestart. Gestart betekent dat enige activiteit is geregistreerd in het outputdagboek voor die bewerking. En die activiteit kan ook bestaan uit het invoeren van een insteltijd.  

Het bedrag van de afboeking is voor het aantal per montage dat vermeld staat op de productiestuklijst, vermenigvuldigd met het aantal hoofdartikelen dat wordt gemaakt (verwachte aantal).  

Deze techniek kan het beste worden toegepast wanneer er veel bewerkingen zijn en bepaalde onderdelen pas later in de montagevolgorde nodig zijn. In feite kan het bij een Just-in-Time (JIT)-omgeving zelfs zo zijn dat de artikelen niet eens voorhanden zijn wanneer de RPO van start gaat.  

Materiaal kan tijdens bewerkingen worden verbruikt met behulp van bewerkingsplankoppelingen. Sommige onderdelen worden mogelijk pas gebruikt bij de eindmontage en mogen pas op dat moment aan de voorraad worden onttrokken.  

### <a name="automatic-reporting---back-flushing-by-operation"></a>Automatische rapportage - achterwaarts afboeken per bewerking
Bij achterwaarts afboeken per bewerking wordt het verbruik geregistreerd nadat de bewerking in het outputdagboek is geboekt.  

Het voordeel van deze methode is dat het aantal hoofdonderdelen dat is gereedgemeld in de bewerking bekend is.  

Het materiaal in de productiestuklijst wordt gekoppeld aan de bewerkingsplanrecords met behulp van bewerkingsplankoppelingen. Het achterwaarts afboeken vindt plaats wanneer een bewerking met een bepaalde bewerkingsplankoppeling wordt geboekt met een gereedgemeld aantal.  

Het bedrag van de afboeking is voor het aantal per montage dat vermeld staat op de productiestuklijst, vermenigvuldigd met het aantal hoofdartikelen dat is geboekt als outputaantal bij die bewerking. Dit kan afwijken van het verwachte aantal.  

### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automatische rapportage - de hele order achterwaarts afboeken
Bij deze rapportagemethode wordt geen rekening gehouden met bewerkingsplankoppelingen.  

Er worden geen onderdelen gepickt totdat de status van de vrijgegeven productieorder is gewijzigd in *Gereedgemeld*. Het bedrag van de afboeking is het aantal per montage dat vermeld staat op de productiestuklijst, vermenigvuldigd met het aantal hoofdartikelen dat is gereedgemeld en in voorraad is geplaatst.  

Voor achterwaarts afboeken van de hele productieorder moeten dezelfde instellingen worden gebruikt als bij voorwaarts afboeken: de rapportagemethode moet worden ingesteld op achterwaarts bij elk artikel voor alle artikelen in de hoofdstuklijst waarvoor de rapportage is bedoeld. Bovendien moeten alle bewerkingsplankoppelingen zijn verwijderd uit de productiestuklijst. 



Als bijvoorbeeld een productieorder voor het vervaardigen van 800 meter 8 kg van een component vereist, worden als u 200 meter als uitvoer boekt automatisch 2 kg als verbruik geboekt. U kunt dat bereiken door de achterwaartse afboekingsmethode te combineren met codes van bewerkingsplankoppelingen, zodat het aantal dat per bewerking wordt afgeboekt, in verhouding staat tot de werkelijke uitvoer van de voltooide bewerking. Voor artikelen die zijn ingesteld met de achterwaartse afboekingsmethode wordt standaard het verbruik van onderdelen berekend en geboekt wanneer u de status van een vrijgegeven productieorder wijzigt in **Voltooid**. Als u ook bewerkingsplankoppelingen definieert, vinden berekening en boeking plaats wanneer elke bewerking is voltooid en wordt de hoeveelheid geboekt die daadwerkelijk is verbruikt in de bewerking. Zie voor meer informatie [Bewerkingsplannen maken](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Onderdelen afboeken op basis van de uitvoer van een bewerking

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Bewerken**.  
3.  Selecteer op het sneltabblad **Aanvulling** in het veld **Afboekingsmethode** de optie **Achterwaarts**.  

    > [!NOTE]  
    >  Selecteer **Pick + Achterwaarts** als het onderdeel wordt gebruikt op een locatie die is ingesteld voor gestuurde opslag en pick.  

4.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bewerkingsplannen** in en kies vervolgens de gerelateerde koppeling.  
5.  Definieer bewerkingsplankoppelingen voor elke bewerking waarbij het onderdeel wordt verbruikt. Zie voor meer informatie [Bewerkingsplannen maken](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Gebruik niet dezelfde routeringskoppeling voor verschillende bewerkingen in de routering, aangezien dit zal leiden tot registratie van het verbruik van een component voor elke gekoppelde bewerking.  
6.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productiestuklijst** in en kies vervolgens de gerelateerde koppeling.  
7.  Definieer bewerkingsplankoppelingen op basis van elk exemplaar van de component voor de bewerking waarbij de component wordt verbruikt.

Het verbruik wordt automatisch geboekt wanneer u output registreert. Zie voor meer informatie [Output en bewerkingstijden in batches boeken](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Afboekingsmethoden

De volgende tabel beschrijft de beschikbare afboekingsmethodeopties die u kunt specificeren op **artikel**kaarten en **SKU**-kaarten.

|Optie|Omschrijving|
|------------|-------------|  
|Handmatig|Hierbij moet u handmatig het verbruik boeken en invoeren in het verbruiksdagboek.|
|Voorwaarts|Boekt automatisch het verbruik op basis van productieordermateriaalregels. <br><br>Het boeken van materiaalverbruik treedt standaard op wanneer u de status van een productieorder wijzigt in **Vrijgegeven**. Als u echter het veld **Bewerkingsplankoppeling** op de productieordermateriaalregels gebruikt, vinden boekingen per bewerking plaats wanneer de bewerking wordt gestart. Zie [Procedure: Bewerkingsplankoppelingen maken](production-how-to-create-routings.md#to-create-routing-links) voor meer informatie. <br><br> **Opmerking**<br>Bij voorwaarts afboeken is de boeking van een specifieke bewerking die u met bewerkingsplankoppelingen verkrijgt, gebaseerd op het verwachte aantal dat gedefinieerd is op de materiaalregel. Zie de beschrijving van **Achterwaarts** in dit onderwerp voor informatie over het afboeken van specifieke bewerkingen gebaseerd op de werkelijke output.<br><br>Als de vestiging of de resources waar dit onderdeel wordt verbruikt, is ingesteld met een standaardopslaglocatiestructuur, wordt het artikel verbruikt vanuit de **Code grijpvoorraadlocatie**. Zie [Procedure: standaard magazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) voor meer informatie. <br><br> **Belangrijk** <br>Voorwaarts afboeken vindt ook plaats wanneer u **Vernieuwen** kiest bij een geheel nieuw vrijgegeven productieorder. U kunt bij deze rechtstreeks vrijgegeven productieorders geen informatie over de opslaglocatie wijzigen omdat de productieordermateriaalregels gegenereerd worden wanneer u de order ververst, waarbij tegelijkertijd de onderdelen voorwaarts afgeboekt worden. Als u dus informatie over de opslaglocatie van een productieorder wilt wijzigen voordat voorwaartse afboeking plaats vindt, moet die order worden gemaakt met de *Geplande* of *Vast geplande* status.|
|Achterwaarts|Berekent en boekt automatisch verbruik op basis van de productieordermateriaalregels.<br><br> De berekening en boeking van materiaalverbruik vindt standaard plaats wanneer u de status van een vrijgegeven productieorder wijzigt in **Gereedgemeld**. Als u echter het veld **Bewerkingsplankoppeling** op de productieordermateriaalregels gebruikt, vinden de berekening en boeking plaats wanneer elke bewerking is voltooid.<br><br> **Opmerking** <br>Achterwaarts afboeken en bewerkingsplankoppelingen kunnen worden gecombineerd zodat het aantal dat per bewerking leeggemaakt wordt, in verhouding staat tot de werkelijke output van die bewerking. Zie voor meer informatie [Procedure: materialen afboeken op basis van de uitvoer van een bewerking](#to-flush-components-according-to-operation-output).<br><br> Als de vestiging of de bewerkingsplaats waar dit onderdeel wordt verbruikt, is ingesteld met een standaardopslaglocatiestructuur, wordt het artikel verbruikt vanuit de **Code grijpvoorraadlocatie**.|
|Picken + voorwaarts|Hetzelfde als voor Voorwaarts afboeken-methode, behalve dat het alleen werkt voor locaties die gebruikmaken van een geavanceerde magazijnconfiguratie of een basismagazijnconfiguratie met verplichte opslaglocaties.<br><br> Verbruik wordt berekend en geboekt op basis van de opslaglocatie die gedefinieerd is in het veld **Code opslaglocatie voor productie** op de vestiging of bewerkingsplaats nadat het onderdeel uit het magazijn is gepickt.<br><br> **Opmerking** <br>Als een onderdeel is ingesteld met de Pick + Voorwaartse afboekingsmethode, kan het geen bewerkingsplankoppeling hebben met een bewerking die ingesteld is met de voorwaartse afboekingsmethode. Het onderdeel zou vervolgens automatisch worden leeggemaakt wanneer de bewerking wordt gestart, waardoor het onmogelijk is om de pickactiviteit aan te vragen.|
|Picken + achterwaarts|Hetzelfde als voor Achterwaarts afboeken-methode, behalve dat het alleen werkt voor locaties die gebruikmaken van een geavanceerde magazijnconfiguratie of een basismagazijnconfiguratie met verplichte opslaglocaties.<br><br> Verbruik wordt berekend en geboekt op basis van de opslaglocatie die gedefinieerd is in het veld **Code opslaglocatie voor productie** op de vestiging of bewerkingsplaats nadat het onderdeel uit het magazijn is gepickt.|

## <a name="see-also"></a>Zie ook

[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
