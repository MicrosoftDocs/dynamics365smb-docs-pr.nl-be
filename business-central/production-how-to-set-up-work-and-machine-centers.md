---
title: Afdelingen en bewerkingsplaatsen instellen
description: Op een afdelingskaart staan alle vaste waarden en behoeften van de desbetreffende productieresource bij elkaar. Op die manier wordt de productie-output die op die afdeling wordt uitgevoerd door de kaart bepaald.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-work-centers-and-machine-centers"></a><a name="set-up-work-centers-and-machine-centers"></a>Afdelingen en bewerkingsplaatsen instellen

Er wordt onderscheid gemaakt tussen drie soorten capaciteit. Deze zijn hiërarchisch gerangschikt. Elk niveau bestaat uit onderliggende niveaus.  

Het bovenste niveau is de afdelingsgroep. Aan de afdelingsgroepen worden afdelingen toegewezen. Iedere afdeling kan slechts aan één afdelingsgroep worden gekoppeld.

U kunt aan iedere afdeling meerdere bewerkingsplaatsen toewijzen. Een bewerkingsplaats kan slechts aan één afdeling worden gekoppeld.  

De geplande capaciteit van een afdeling bestaat uit de beschikbaarheid van de bijbehorende bewerkingsplaatsen en de extra geplande beschikbaarheid van de afdeling. De geplande beschikbaarheid van de afdelingsgroep is dus het totaal van de beschikbaarheid van corresponderende bewerkingsplaatsen en afdelingen.  

De beschikbaarheid wordt opgeslagen in agendaposten.  

> [!IMPORTANT]
> Voordat u afdelingen of bewerkingsplaatsen instelt, kunt u productieagenda's instellen. Zie voor meer informatie [Productieagenda's maken](production-how-to-create-work-center-calendars.md).

## <a name="to-set-up-a-work-center"></a><a name="to-set-up-a-work-center"></a>Een afdeling instellen

Hier wordt voornamelijk beschreven hoe u een afdeling instelt. De stappen voor het instellen van een bewerkingsplaatsagenda komen overeen, met uitzondering van het sneltabblad **Bewerkingsplaninstelling**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Afdelingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Selecteer in het veld **Afdelingsgroep** de hoger gelegen resourcegroep waaronder de afdeling is georganiseerd, indien van toepassing. Kis de actie **Nieuw** in de vervolgkeuzelijst.  
5. Selecteer in het veld **Alt. afdeling** de afdeling die u wilt gebruiken als deze afdeling niet beschikbaar is of wanneer de vraag de capaciteit overschrijdt. De alternatieve afdeling is alleen ter informatie en wordt niet automatisch opgenomen in planningsprocessen.
6. Selecteer het veld **Geblokkeerd** als u wilt voorkomen dat de afdeling wordt gebruikt in de verwerking. Dit betekent dat er geen output kan worden geboekt voor een artikel dat in de afdeling wordt geproduceerd. Zie voor meer informatie [Productie-output boeken](production-how-to-post-output-quantity.md).
7. Voer in het veld **Directe kostprijs** de productiekosten voor deze afdeling in voor één eenheid, zonder daarin andere kostenelementen te betrekken. Deze kosten worden vaak het *tarief directe lonen* genoemd.  
8. In het veld **Indirecte kosten %** voert u de algemene bewerkingskosten van het gebruik van de afdeling als percentage van de directe kostprijs. Voor de berekening van de kostprijs wordt dit percentage bij de directe kosten opgeteld.  
9. In het veld **Overheadtarief** voert u alle niet-bewerkingskosten van de afdeling, zoals onderhoudskosten, als absoluut bedrag in.  

    Het veld **Kostprijs** bevat de berekende kostprijs voor de productie van één eenheid op deze afdeling, met daarin alle andere kostenelementen, als volgt:  

    Kostprijs = Directe kostprijs + (Directe kostprijs x Indirecte kosten %) + Overheadtarief.  

10. Definieer in het veld **Kostprijsberekening** of de bovenstaande berekening moet worden gebaseerd op de gebruikte tijd: **Tijd** of op het aantal geproduceerde eenheden: **Eenheden**.  
11. Schakel het selectievakje **Specifieke kostprijs** in wanneer u de afdelingskostprijs wilt definiëren op de bewerkingsplanregel waarop deze wordt gebruikt. Dit kan nodig zijn voor bewerkingen waarvan de capaciteitskosten enorm verschillen met die van bewerkingen die normaal op de afdeling worden uitgevoerd.  
12. Selecteer in het veld **Afboekingsmethode** of de outputboeking op deze afdeling handmatig moet worden berekend en geboekt of dat dit automatisch moet gebeuren op een van de volgende wijzen.

    |Optie|Omschrijving|
    |------|-----------|
    |**Handmatig**| Gebruikte tijd, output en uitval worden handmatig geboekt in het outputdagboek of productiedagboek.|
    |**Voorwaarts**|Output wordt automatisch geboekt wanneer de productieorder wordt vrijgegeven.|
    |**Achterwaarts**|Output wordt automatisch geboekt wanneer de productieorder wordt voltooid.|

    > [!NOTE]
    > Zo nodig kan de afboekingsmethode die hier is geselecteerd, voor afzonderlijke bewerkingen worden overschreven. U doet dit door de instellingen op bewerkingsplanregels te wijzigen

13. Voer in het veld **Code van maateenheid** de tijdseenheid in waarin de kostenberekening en capaciteitsplanning van deze afdeling worden gemaakt.
    Pas wanneer u een methode voor meten hebt ingesteld, kunt u het verbruik voortdurend controleren. De eenheden die u invoert, zijn basiseenheden. De verwerkingstijd wordt bijvoorbeeld gemeten in uren en minuten.

    > [!NOTE]  
    > Als u kiest voor het gebruik van dagen, moet u eraan denken dat 1 dag bestaat uit 24 uur en niet uit 8 (werkuren).

14. Definieer in het veld **Capaciteit** of er op de afdeling meer dan één machine of persoon tegelijkertijd aan het werk zijn. Wanneer in [!INCLUDE[prod_short](includes/prod_short.md)] niet de module Bewerkingsplaats is geïnstalleerd, moet de waarde in dit veld **1** zijn.  
15. Voer in het veld **Efficiëntie** het percentage van de verwachte standaardoutput in dat deze afdeling werkelijk oplevert. Wanneer u hier **100** invoert, betekent dit dat de werkelijke output van de afdeling net zo hoog is als de standaardoutput.  
16. Schakel het selectievakje **Geconsolideerde agenda** in als u ook bewerkingsplaatsen gebruikt. Hierdoor worden agendaposten berekend op basis van bewerkingsplaatsagenda's.  
17. Selecteer een productieagenda in het veld **Productieagendacode**. Zie voor meer informatie [Productieagenda's maken](production-how-to-create-work-center-calendars.md).  
18. In het veld **Wachttijd voor bew.** geeft u op hoeveel tijd er moet verstrijken voordat toegewezen werk op deze afdeling kan beginnen. 

> [!NOTE]
> Gebruik wachttijden om een buffer te bieden tussen het moment waarop een component aankomt op een bewerkingsplaats of afdeling en het moment waarop de bewerking daadwerkelijk begint. Een onderdeel wordt bijvoorbeeld om 10.00 uur afgeleverd bij een bewerkingsplaats, maar het duurt een uur om het op de machine te monteren, zodat de bewerking pas om 11.00 uur begint. Om rekening te houden met dat uur, zou de wachttijd een uur zijn. De waarde van het veld **Wachttijd voor bew.** op een bewerkings- of afdelingskaart, opgeteld bij de waarden in de velden **Insteltijd**, **Bewerkingstijd**, **Wachttijd na bew.** en **Transporttijd** op de bewerkingsplanregel vormen samen de productietijd van het artikel. Dit zorgt voor nauwkeurige totale productietijden.  

## <a name="considerations-about-capacity"></a><a name="considerations-about-capacity"></a>Overwegingen over capaciteit

De capaciteit en efficiëntie die voor een afdeling en bewerkingsplaats worden gespecificeerd, hebben niet alleen invloed op de beschikbare capaciteit. Ze hebben ook invloed op de totale productietijd die bestaat uit de insteltijd en de looptijd, die beide op de routeringsregel zijn gedefinieerd.  

Wanneer een specifieke bewerkingsplanregel wordt toegewezen aan een afdeling of bewerkingsplaats, berekent het systeem hoeveel capaciteit nodig is en hoe lang het duurt om de bewerking te voltooien.  

### <a name="run-time"></a><a name="run-time"></a>Bewerkingstijd

Om de bewerkingstijd te berekenen wijst het systeem de exacte tijd toe die is gedefinieerd in het veld **Bewerkingstijd** van de bewerkingsplanregel. Noch efficiëntie, noch capaciteit hebben invloed op de toegewezen tijd. Als de bewerkingstijd bijvoorbeeld is gedefinieerd als 2 uur, is de toegewezen tijd 2 uur, ongeacht de waarden in de velden efficiëntie en capaciteit in de afdeling.  

> [!NOTE]
> De capaciteit die in de berekeningen wordt gebruikt, wordt gedefinieerd als de minimale waarde tussen de capaciteit die is gedefinieerd op de afdeling of de bewerkingsplaats, en de gelijktijdige capaciteit die is gedefinieerd voor de bewerkingsplanregel. Als een afdeling een capaciteit van 100 heeft, maar de gelijktijdige capaciteit voor de bewerkingsplanregel is 2, dan wordt *2* gebruikt in de berekeningen.

De *duur* van een bewerking daarentegen houdt rekening met zowel efficiëntie als capaciteit. Duur wordt berekend als *Bewerkingstijd / Efficiëntie / Capaciteit*. De volgende lijst toont enkele voorbeelden van de berekening van de duur voor dezelfde bewerkingstijd, die is gedefinieerd als 2 uur voor de bewerkingsplanregel:

- Efficiency 80% betekent dat u 2,5 uur nodig hebt in plaats van 2 uur  
- Efficiëntie 200% betekent dat u het werk in één uur kunt voltooien. U kunt het gat twee keer zo snel graven als u een graafmachine heeft die twee keer zo groot is als de kleinere  

    U kunt hetzelfde resultaat bereiken als u twee kleinere graafmachines gebruikt in plaats van een grote; gebruik *2* als de capaciteit en *100%* als de efficiëntie  

De fractionele capaciteit is lastig en we zullen het later bespreken. 

### <a name="setup-time"></a><a name="setup-time"></a>Insteltijd

Tijdtoewijzing voor de insteltijd is afhankelijk van de capaciteit en wordt berekend als *Insteltijd* Capaciteit*. Als de capaciteit bijvoorbeeld is ingesteld op *2*, wordt uw toegewezen insteltijd verdubbeld, omdat u twee machines moet instellen voor de bewerking.  

*Duur* van de insteltijd is afhankelijk van de efficiëntie en wordt berekend als *Insteltijd / Efficiëntie*. 

- Efficiency 80% betekent dat u 2,5 uur nodig hebt in plaats van 2 uur om in te stellen  
- Efficiëntie 200% betekent dat u de installatie in 1 uur kunt voltooien in plaats van 2 uur, zoals gedefinieerd op de bewerkingsplanregel  

De fractale capaciteit is niet gemakkelijk en wordt in zeer specifieke gevallen gebruikt.

### <a name="work-center-processing-multiple-orders-simultaneously"></a><a name="work-center-processing-multiple-orders-simultaneously"></a>Afdeling die meerdere orders tegelijk verwerkt

Laten we als voorbeeld een verfspuitcabine gebruiken. Deze heeft dezelfde instel- en bewerkingstijd voor elke verwerkte partij. Maar elke partij kan meerdere individuele orders bevatten die tegelijkertijd worden geverfd.  

In dit geval worden de tijd en kosten die aan orders worden toegewezen, beheerd door de insteltijd en de gelijktijdige capaciteit. We raden u aan om geen bewerkingstijd te gebruiken in de bewerkingsplanregels.  

De toegewezen insteltijd voor elke individuele order zal in omgekeerde volgorde zijn van het aantal orders (hoeveelheden) dat tegelijkertijd wordt uitgevoerd. Hier zijn nog enkele voorbeelden van de berekening van de insteltijd wanneer die is gedefinieerd als twee uur voor de bewerkingsplanregel:

- Als er twee orders zijn, moet de gelijktijdige capaciteit op de bewerkingsplanregel de routeringsregel worden ingesteld op 0,5.

    Als gevolg hiervan zal de toegewezen capaciteit voor elk één uur zijn, maar de duur voor elke order blijft twee uur.
- Als er twee orders zijn met een hoeveelheid van respectievelijk één en vier, dan is de gelijktijdige capaciteit voor de bewerkingsplanregel van de eerste order 0,2 en 0,8 voor de tweede.  

    Als gevolg hiervan is de toegewezen capaciteit voor de eerste order 24 minuten en voor de tweede 96. De duur voor beide orders blijft twee uur.  

In beide gevallen is de totale toegewezen tijd voor alle orders twee uur.


### <a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a><a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a>Efficiënte resource kan slechts een deel van de werkdatum aan productief werk besteden

> [!NOTE]
> Dit is geen aanbevolen scenario. We raden u aan om in plaats daarvan efficiëntie te gebruiken. 

Een van uw afdelingen vertegenwoordigt een ervaren werknemer die met 100% efficiëntie aan taken werkt. Maar hij of zij kan maar 50% van de werktijd aan taken besteden omdat ze de rest van de tijd administratieve taken oplossen. Hoewel deze werknemer in staat is om een taak van twee uur in precies twee uur te voltooien, moet u gemiddeld nog twee uur wachten terwijl de persoon andere opdrachten afhandelt.  

De toegewezen bewerkingstijd is twee uur en de duur is vier uur.  

Gebruik geen insteltijd voor dergelijke scenario's, aangezien het systeem slechts 50% van de tijd zal toewijzen. Als de insteltijd is ingesteld op *2*, dan is de toegewezen insteltijd één uur en de duur twee uur.

### <a name="consolidated-calendar"></a><a name="consolidated-calendar"></a>Geconsolideerde agenda

Wanneer het veld **Geconsolideerde agenda** is geselecteerd, heeft de afdeling geen eigen capaciteit. In plaats daarvan is de capaciteit gelijk aan de som van de capaciteiten van alle bewerkingsplaatsen die aan de afdeling zijn toegewezen.  

> [!NOTE]
>  De efficiëntie van de bewerkingsplaats wordt omgerekend naar de capaciteit van de afdeling.

Als u bijvoorbeeld twee bewerkingsplaatsen heeft met een efficiëntie van respectievelijk 80 en 70, heeft het geconsolideerde agenda-item een efficiëntie van 100, een capaciteit van 1,5 en een totale capaciteit van 12 uur (ploeg van 8 uur * 1,5 capaciteit). 

> [!NOTE]
>  Gebruik het veld **Geconsolideerde agenda** wanneer u uw bewerkingsplannen structureert om productiebewerkingen te plannen op bewerkingsplaatsniveau, niet op afdelingsniveau. Wanneer u de agenda consolideert, worden de pagina en de rapporten **Werklast van afdeling** een overzicht van de totale belasting in alle bewerkingsplaatsen die aan de afdeling zijn toegewezen.

### <a name="example---different-machine-centers-assigned-to-a-work-center"></a><a name="example---different-machine-centers-assigned-to-a-work-center"></a>Voorbeeld - Verschillende bewerkingsplaatsen die aan een afdeling zijn toegewezen

Tijdens het instellen van bewerkingsplaatsen en afdelingen is het belangrijk dat u plant waaruit de totale capaciteit zal bestaan.

Als er meerdere bewerkingsplaatsen (bijvoorbeeld 210 Verpakkingsruimte 1, 310 Verfcabine ...) aan een afdeling zijn toegewezen, is het belangrijk dat u rekening houdt met de afzonderlijke capaciteit van de bewerkingsplaatsen, omdat storingen op één bewerkingsplaats het hele proces kunnen onderbreken. De bewerkingsplaatsen kunnen worden ingevoerd op basis van capaciteit, maar worden mogelijk niet opgenomen in de planning. Als u het veld **Geconsolideerde agenda** uitschakelt, wordt alleen de afdelingscapaciteit toegewezen in de planning, niet de capaciteit van de afzonderlijke bewerkingsplaatsen.

Wanneer echter identieke bewerkingsplaatsen (bijvoorbeeld 210 Verpakkingsruimte 1 en 220 Verpakkingsruimte 2) worden gecombineerd op een afdeling, kan de afdeling worden beschouwd als het totaal van de toegewezen bewerkingsplaatsen. De afdeling zou dan worden weergegeven met een capaciteit van nul. Als u het veld **Geconsolideerde agenda** inschakelt, wordt de totale capaciteit toegewezen aan de afdeling.

Als de capaciteit van afdelingen niet moet bijdragen aan de totale capaciteit, kunt u dit instellen met efficiëntie = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a><a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Een bewerkingsplaats of afdeling met beperkte capaciteit instellen

U kunt een beperkte werklast toewijzen aan productieresources die als kritiek worden beschouwd door deze te markeren, in plaats van de onbeperkte werklast die door andere resources worden geaccepteerd. Een resource met beperkte capaciteit kan een afdeling of bewerkingsplaats zijn die als knelpunt wordt beschouwd en waarvoor u een beperkte (begrensde) werklast wilt instellen.

[!INCLUDE[prod_short](includes/prod_short.md)] biedt geen ondersteuning voor gedetailleerd werkvloerbeheer. Het systeem plant een uitvoerbaar gebruik van resources door een ruw schema te leveren, maar het maakt en onderhoudt niet automatisch gedetailleerde schema's op basis van prioriteiten of optimalisatieregels.

Op de pagina **Capaciteitsbegrensde resource** kunt u instellingen configureren waarmee overbelasting van specifieke resources kan worden voorkomen, en kunt u ervoor zorgen dat alle capaciteit wordt toegewezen als dit de omlooptijd van een productieorder kan verhogen. In het veld **Demping (% van totale capaciteit)** kunt u dempingstijd aan resources toevoegen om bewerkingsplitsen te verkleinen. Hiermee kan het systeem de werklast op de laatst mogelijke dag plannen door het kritieke werklastpercentage iets te overschrijden als dit het aantal bewerkingen kan verminderen die worden gesplitst.

Bij het plannen met capaciteitsbegrensde resources zorgt het systeem dat er geen resources boven de gedefinieerde capaciteit (kritieke werklastpercentage) worden geladen. Dit gebeurt door elke bewerking toe te wijzen aan de dichtstbijzijnde beschikbare periode. Als de periode niet groot genoeg is om de hele bewerking uit te voeren, wordt de bewerking in twee of meer delen gesplitst in de dichtstbijgelegen perioden.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Capaciteitsbegrensde resources** in en kies de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul de velden in.

> [!NOTE]
> Bewerkingen op afdelingen of bewerkingsplaatsen die zijn ingesteld als beperkte resources, worden altijd in serie gepland. Dit betekent dat als een beperkte bron meerdere capaciteiten heeft, die capaciteiten alleen in volgorde kunnen worden gepland. Dit kan niet parallel, zoals het geval zou zijn als de afdelings- of bewerkingsplaats niet is ingesteld als beperkte resource. In een begrensde resource, is het veld Capaciteit op de afdeling of bewerkingsplaats groter is dan 1.

> In het geval van gesplitste bewerkingen wordt de insteltijd slechts eenmaal toegewezen omdat ervan wordt uitgegaan dat enige handmatige aanpassing wordt uitgevoerd om de planning te optimaliseren.

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Productieagenda's maken](production-how-to-create-work-center-calendars.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
