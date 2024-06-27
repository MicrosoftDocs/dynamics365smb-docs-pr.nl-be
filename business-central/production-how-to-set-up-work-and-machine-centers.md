---
title: Afdelingen en bewerkingsplaatsen instellen
description: Op een afdelingskaart staan alle vaste waarden en behoeften van de desbetreffende productieresource bij elkaar. Op die manier wordt de productie-output die op die afdeling wordt uitgevoerd door de kaart bepaald.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Afdelingen en bewerkingsplaatsen instellen

[!INCLUDE [prod_short](includes/prod_short.md)] maakt onderscheid tussen drie soorten capaciteit. Deze zijn hiërarchisch gerangschikt. Elk niveau bestaat uit onderliggende niveaus.  

Het bovenste niveau is de afdelingsgroep. Afdelingen worden toegewezen aan afdelingsgroepen. Iedere afdeling kan slechts aan één afdelingsgroep worden gekoppeld.

U kunt aan afdelingen meerdere bewerkingsplaatsen toewijzen. Een bewerkingsplaats kan slechts aan één afdeling worden gekoppeld.  

De geplande capaciteit van een afdeling bestaat uit de beschikbaarheid van de bijbehorende bewerkingsplaatsen en de geplande beschikbaarheid van de afdeling. De geplande beschikbaarheid van de afdelingsgroep is dus het totaal van de beschikbaarheid van corresponderende bewerkingsplaatsen en afdelingen. Beschikbaarheid wordt opgeslagen in agendaposten.  

> [!IMPORTANT]
> Voordat u afdelingen of bewerkingsplaatsen instelt, kunt u productieagenda's instellen. Zie voor meer informatie [Productieagenda's maken](production-how-to-create-work-center-calendars.md).

## Een afdeling instellen

De volgende stappen beschrijven hoe u een afdeling instelt. De stappen voor het instellen van een bewerkingsplaatsagenda komen overeen, met uitzondering van het sneltabblad **Bewerkingsplaninstelling**.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afdelingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Selecteer in het veld **Afdelingsgroepcode** de hoger gelegen resourcegroep waaronder de afdeling is georganiseerd, indien van toepassing. Kis de actie **Nieuw** in de vervolgkeuzelijst.  
5. Selecteer in het veld **Alt. afdeling** de afdeling die u wilt gebruiken als deze afdeling niet beschikbaar is of wanneer de vraag de capaciteit overschrijdt. De alternatieve afdeling is alleen ter informatie en wordt niet automatisch opgenomen in planningsprocessen.
6. Selecteer het veld **Geblokkeerd** als u wilt voorkomen dat de afdeling wordt gebruikt in de verwerking. Dit betekent dat er geen output kan worden geboekt voor een artikel dat in de afdeling wordt geproduceerd. Zie voor meer informatie [Productie-output boeken](production-how-to-post-output-quantity.md).
7. Voer in het veld **Directe kostprijs** de productiekosten voor deze afdeling in voor één eenheid, zonder daarin andere kostenelementen te betrekken. Deze kosten worden vaak het *tarief directe lonen* genoemd.  
8. In het veld **Indirecte kosten %** voert u de algemene bewerkingskosten van het gebruik van de afdeling als percentage van de directe kostprijs. Voor de berekening van de kostprijs wordt dit percentage bij de directe kosten opgeteld.  
9. In het veld **Overheadtarief** voert u alle niet-bewerkingskosten van de afdeling, zoals onderhoudskosten, als absoluut bedrag in.  

    Het veld **Kostprijs** bevat de berekende kostprijs voor de productie van één eenheid op deze afdeling, met daarin alle andere kostenelementen, als volgt:  

    Kostprijs = Directe kostprijs + (Directe kostprijs x Indirecte kosten %) + Overheadtarief.  

10. Definieer in het veld **Kostprijsberekening** of de berekening van de kostprijs per eenheid moet worden gebaseerd op de gebruikte tijd of op het aantal geproduceerde eenheden.  
11. Schakel het selectievakje **Specifieke kostprijs** in wanneer u de afdelingskostprijs wilt definiëren op de bewerkingsplanregel waarop deze wordt gebruikt. Deze instelling kan relevant zijn voor bewerkingen waarvan de capaciteitskosten verschillen van wat u normaal op de afdeling verwerkt.  
12. Selecteer in het veld **Afboekingsmethode** of output handmatig of automatisch wordt berekend en geboekt op deze afdeling met een van de volgende methoden.

    |Optie|Omschrijving|
    |------|-----------|
    |**Handmatig**| Boek gebruikte tijd, output en uitval handmatig in het outputdagboek of productiedagboek.|
    |**Voorwaarts**|Boek automatisch output wanneer u de productieorder vrijgeeft.|
    |**Achterwaarts**|Boek automatisch output wanneer u de productieorder voltooit.|

    > [!NOTE]
    > Zo nodig kan de afboekingsmethode die hier is geselecteerd, voor afzonderlijke bewerkingen worden overschreven. U doet dit door de instellingen op bewerkingsplanregels te wijzigen

13. Voer in het veld **Code van maateenheid** de tijdseenheid in waarin de kostenberekening en capaciteitsplanning van deze afdeling worden gemaakt.
    Pas wanneer u een methode voor meten hebt ingesteld, kunt u het verbruik voortdurend controleren. De eenheden die u invoert, zijn basiseenheden. De verwerkingstijd wordt bijvoorbeeld gemeten in uren en minuten.

    > [!NOTE]  
    > Als u Dagen gebruikt, moet u er rekening mee houden dat één dag 24 uur duurt en niet een werkdag van acht uur.

14. Definieer in het veld **Capaciteit** of er op de afdeling meer dan één machine of persoon tegelijkertijd aan het werk zijn. Wanneer uw [!INCLUDE[prod_short](includes/prod_short.md)] niet de functionaliteit Bewerkingsplaats bevat, moet de waarde in dit veld **1** zijn.  
15. Voer in het veld **Efficiëntie** het percentage van de verwachte standaardoutput in dat deze afdeling werkelijk oplevert. Wanneer u hier **100** invoert, betekent dit dat de werkelijke output van de afdeling net zo hoog is als de standaardoutput.  
16. Zet de schakelaar **Geconsolideerde agenda** aan als u ook bewerkingsplaatsen gebruikt. Door deze instelling worden agendaposten berekend op basis van bewerkingsplaatsagenda's.  
17. Selecteer een productieagenda in het veld **Productieagendacode**. Zie voor meer informatie [Productieagenda's maken](production-how-to-create-work-center-calendars.md).  
18. In het veld **Wachttijd voor bew.** geeft u op hoeveel tijd er moet verstrijken voordat toegewezen werk op deze afdeling kan beginnen. 

> [!NOTE]
> Gebruik wachttijden om een buffer te bieden tussen het moment waarop een component aankomt op een bewerkingsplaats of afdeling en het moment waarop de bewerking daadwerkelijk begint. Een onderdeel wordt bijvoorbeeld om 10.00 uur afgeleverd bij een bewerkingsplaats, maar het duurt een uur om het op de machine te monteren, zodat de bewerking pas om 11.00 uur begint. Om rekening te houden met dat uur, zou de wachttijd een uur zijn. De waarde van het veld **Wachttijd voor bew.** op een bewerkings- of afdelingskaart, opgeteld bij de waarden in de velden **Insteltijd**, **Bewerkingstijd**, **Wachttijd na bew.** en **Transporttijd** op de bewerkingsplanregel vormen samen de productietijd van het artikel. Dit zorgt voor nauwkeurige totale productietijden.  

## Overwegingen over capaciteit

De capaciteit en efficiëntie die voor afdelingen en bewerkingsplaatsen worden gespecificeerd, hebben niet alleen invloed op de beschikbare capaciteit. De waarden hebben ook invloed op de totale productietijd die bestaat uit de insteltijd en de looptijd, die beide op de routeringsregel zijn gedefinieerd.  

Wanneer u een bewerkingsplanregel aan een afdeling of bewerkingsplaats toewijst, berekent [!INCLUDE [prod_short](includes/prod_short.md)]:

- Hoeveel capaciteit is er nodig.
- Hoe lang het duurt voordat de bewerking is voltooid.  

### Bewerkingstijd

Om de bewerkingstijd te berekenen wijst het systeem de exacte tijd toe die is gedefinieerd in het veld **Bewerkingstijd** van de bewerkingsplanregel. Efficiëntie en capaciteit hebben geen invloed op de toegewezen tijd. Als de bewerkingstijd bijvoorbeeld is gedefinieerd als 2 uur, is de toegewezen tijd 2 uur, ongeacht de waarden in de velden efficiëntie en capaciteit in de afdeling.  

> [!NOTE]
> De capaciteit die in de berekeningen wordt gebruikt, wordt gedefinieerd als de minimale waarde tussen de capaciteit die is gedefinieerd op de afdeling of de bewerkingsplaats, en de gelijktijdige capaciteit die is gedefinieerd voor de bewerkingsplanregel. Als een afdeling een capaciteit van 100 heeft, maar de gelijktijdige capaciteit voor de bewerkingsplanregel is 2, dan wordt *2* gebruikt in de berekeningen.

De *duur* van een bewerking daarentegen houdt rekening met zowel efficiëntie als capaciteit. Duur wordt berekend als *Bewerkingstijd / Efficiëntie / Capaciteit*. De volgende lijst toont enkele voorbeelden van de berekening van de duur voor dezelfde bewerkingstijd, die is gedefinieerd als 2 uur voor de bewerkingsplanregel:

- Efficiency 80% betekent dat u 2,5 uur nodig hebt in plaats van 2 uur  
- Efficiëntie 200% betekent dat u de werkzaamheden in één uur kunt voltooien. U kunt het gat twee keer zo snel graven als u een graafmachine hebt die twee keer zo groot is als de kleinere  

    Hetzelfde resultaat kunt u bereiken als u twee kleinere graafmachines gebruikt in plaats van een grote. Gebruik *2* als de capaciteit en *100%* als de efficiëntie  

Fractionele capaciteit is lastig. We zullen het later in dit artikel bespreken. 

### Insteltijd

Tijdtoewijzing voor de insteltijd is afhankelijk van de capaciteit en wordt berekend als *Insteltijd * Capaciteit*. Als de capaciteit bijvoorbeeld is ingesteld op *2*, wordt uw toegewezen insteltijd verdubbeld, omdat u twee machines moet instellen voor de bewerking.  

*Duur* van de insteltijd is afhankelijk van de efficiëntie en wordt berekend als *Insteltijd / Efficiëntie*. 

- Efficiëntie 80% betekent dat u 2,5 uur nodig hebt in plaats van 2 uur om in te stellen.  
- Efficiëntie 200% betekent dat u de installatie in 1 uur kunt voltooien in plaats van 2 uur, zoals gedefinieerd op de bewerkingsplanregel  

De fractale capaciteit wordt alleen in specifieke gevallen gebruikt.

### Afdeling die meerdere orders tegelijk verwerkt

Laten we als voorbeeld een verfspuitcabine gebruiken. Deze heeft dezelfde instel- en bewerkingstijd voor elke verwerkte partij. Maar elke partij kan meerdere individuele orders bevatten die tegelijkertijd worden geverfd.  

In dit geval beheren de insteltijd en de gelijktijdige capaciteit de kosten die aan orders worden toegewezen. We raden u aan om geen bewerkingstijd te gebruiken in de bewerkingsplanregels.  

De toegewezen insteltijd voor elke individuele order zal in omgekeerde volgorde zijn van het aantal orders (hoeveelheden) dat tegelijkertijd wordt uitgevoerd. Hier zijn nog enkele voorbeelden van de berekening van de insteltijd wanneer die is gedefinieerd als twee uur voor de bewerkingsplanregel:

- Als er twee orders zijn, moet de gelijktijdige capaciteit op de bewerkingsplanregel de routeringsregel worden ingesteld op 0,5.

    Als gevolg hiervan zal de toegewezen capaciteit voor elk één uur zijn, maar de duur voor elke order blijft twee uur.
- Als er twee orders zijn met een hoeveelheid van respectievelijk één en vier, dan is de gelijktijdige capaciteit voor de bewerkingsplanregel van de eerste order 0,2 en 0,8 voor de tweede.  

    Als gevolg hiervan is de toegewezen capaciteit voor de eerste order 24 minuten en voor de tweede 96. De duur voor beide orders blijft twee uur.  

In beide gevallen is de totale toegewezen tijd voor alle orders twee uur.


### Efficiënte resource kan slechts een deel van de werkdatum aan productief werk besteden

> [!NOTE]
> Dit is geen aanbevolen scenario. We raden u aan om in plaats daarvan efficiëntie te gebruiken. 

Een van uw afdelingen vertegenwoordigt een ervaren werknemer die met 100% efficiëntie aan taken werkt. Maar hij of zij kan maar 50% van de werktijd aan taken besteden omdat ze de rest van de tijd administratieve taken oplossen. Hoewel deze werknemer in staat is om een taak van twee uur in precies twee uur te voltooien, moet u gemiddeld nog twee uur wachten terwijl de persoon andere opdrachten afhandelt.  

De toegewezen bewerkingstijd is twee uur en de duur is vier uur.  

Gebruik geen insteltijd voor dergelijke scenario's, omdat [!INCLUDE [prod_short](includes/prod_short.md)] slechts 50% van de tijd toewijst. Als de insteltijd is ingesteld op *2*, dan is de toegewezen insteltijd één uur en de duur twee uur.

### Geconsolideerde agenda

Wanneer het veld **Geconsolideerde agenda** is geselecteerd, heeft de afdeling geen eigen capaciteit. In plaats daarvan is de capaciteit gelijk aan de som van de capaciteiten van alle bewerkingsplaatsen die aan de afdeling zijn toegewezen.  

> [!NOTE]
> De efficiëntie van de bewerkingsplaats wordt omgerekend naar de capaciteit van de afdeling.

Als u bijvoorbeeld twee bewerkingsplaatsen hebt met een efficiëntie van respectievelijk 80 en 70, heeft de geconsolideerde kalenderinvoer het volgende:

- Een efficiëntie van 100
- Een capaciteit van 1,5
- Een totale capaciteit van 12 uur (ploeg van 8 uur * capaciteit 1,5 uur).

> [!NOTE]
> Gebruik het veld **Geconsolideerde agenda** wanneer u uw bewerkingsplannen structureert om productiebewerkingen te plannen op bewerkingsplaatsniveau, niet op afdelingsniveau. Wanneer u de agenda consolideert, worden de pagina en de rapporten **Werklast van afdeling** een overzicht van de totale belasting in alle bewerkingsplaatsen die aan de afdeling zijn toegewezen.

### Voorbeeld: verschillende bewerkingsplaatsen die aan een afdeling zijn toegewezen

Tijdens het instellen van bewerkingsplaatsen en afdelingen is het belangrijk dat u plant waaruit de totale capaciteit zal bestaan.

Als er meerdere bewerkingsplaatsen (bijvoorbeeld 210 Verpakkingsruimte 1, 310 Verfcabine ...) aan een afdeling zijn toegewezen, is het belangrijk dat u rekening houdt met de afzonderlijke capaciteit van de bewerkingsplaatsen, omdat een storing op één bewerkingsplaats het hele proces kan onderbreken. De bewerkingsplaatsen kunnen worden ingevoerd op basis van capaciteit, maar worden niet opgenomen in de planning. Als u de schakelaar **Geconsolideerde agenda** uitzet, wordt alleen de capaciteit van de afdeling toegewezen in de planning. De capaciteit van de machineplaats is uitgesloten.

Wanneer u echter identieke bewerkingsplaatsen (bijvoorbeeld 210 Verpakkingsruimte 1 en 220 Verpakkingsruimte 2) combineert op een afdeling, kan de afdeling worden beschouwd als het totaal van de toegewezen bewerkingsplaatsen. De afdeling zou dan worden weergegeven met een capaciteit van nul. Als u de schakelaar **Geconsolideerde agenda** aanzet, wordt de totale capaciteit toegewezen aan de afdeling.

Als u niet wilt dat de capaciteiten van afdelingen bijdragen aan de totale capaciteit, geef dan **0** op in het veld **Efficiëntie**.

## Een bewerkingsplaats of afdeling met beperkte capaciteit instellen

U kunt een beperkte werklast toewijzen aan productieresources die als kritiek worden beschouwd door deze te markeren, in plaats van de onbeperkte werklast die door andere resources worden geaccepteerd. Een resource met beperkte capaciteit kan een afdeling of bewerkingsplaats zijn die als knelpunt wordt beschouwd en waarvoor u een beperkte, begrensde werklast wilt instellen.

[!INCLUDE[prod_short](includes/prod_short.md)] biedt geen ondersteuning voor gedetailleerd werkvloerbeheer. Het systeem plant een uitvoerbaar gebruik van resources door een ruw schema te leveren, maar het maakt en onderhoudt niet automatisch gedetailleerde schema's op basis van prioriteiten of optimalisatieregels.

Op de pagina **Capaciteitsbegrensde resources** kunt u een instelling maken om te voorkomen dat bronnen overbelast raken. De instelling kan ook zorgen dat capaciteit niet niet-toegewezen blijft als dit de doorlooptijd van een productieorder zou kunnen verlengen. In het veld **Demping (% van totale capaciteit)** kunt u dempingstijd aan resources toevoegen om bewerkingsplitsen te verkleinen. Door deze instelling kan het systeem de belasting plannen op de laatst mogelijke dag door het kritieke belastingpercentage iets te overschrijden. Het overschrijden van het belastingspercentage kan het aantal gesplitste bewerkingen verminderen.

Wanneer u plant met capaciteitsbegrensde resources, zorgt [!INCLUDE [prod_short](includes/prod_short.md)] dat er geen resources boven hun capaciteit (kritieke belasting) worden belast. Elke bewerking wordt toegewezen aan de dichtstbijzijnde beschikbare periode. Als de periode niet groot genoeg is om de hele bewerking uit te voeren, wordt de bewerking in twee of meer delen gesplitst in de dichtstbijgelegen beschikbare perioden.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Capaciteitsbegrensde resources** in en kies de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul de velden in.

> [!NOTE]
> Bewerkingen op afdelingen of bewerkingsplaatsen die zijn ingesteld als beperkte resources, worden altijd in serie gepland. Deze planning betekent dat als een beperkte resource meerdere capaciteiten heeft, deze capaciteiten op volgorde moeten worden gepland. U kunt ze niet parallel plannen, zoals het geval zou zijn als het werk- of bewerkingscentrum niet als een beperkte resource was ingericht. Voor een begrensde resource is het veld **Capaciteit** op de afdeling of bewerkingsplaats groter dan **1**.

> In het geval van gesplitste bewerkingen wordt de insteltijd slechts eenmaal toegewezen omdat ervan wordt uitgegaan dat enige handmatige aanpassing wordt uitgevoerd om de planning te optimaliseren.

## Zie ook

[Productieagenda's maken](production-how-to-create-work-center-calendars.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
