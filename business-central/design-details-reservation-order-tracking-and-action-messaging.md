---
title: 'Ontwerpdetails: Reservering, ordertracering en planningsboodschappen | Microsoft Docs'
description: Het reserveringssysteem is uitgebreid en omvat de met elkaar verbonden en parallelle functies van ordertracering en planningsboodschappen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: edupont
---
# Ontwerpdetails: Reservering, ordertracering en planningsboodschappen
Het reserveringssysteem is uitgebreid en omvat de met elkaar verbonden en parallelle functies van ordertracering en planningsboodschappen.  

 De kern van het reserveringssysteem bestaat uit de koppeling van een vraagpost en een bijbehorende voorzieningspost, door reservering of ordertracering. Een reservering is een door de gebruiker gegenereerde koppeling en een ordertraceringsrecord is een door het systeem gegenereerde koppeling. Een artikelaantal dat in het reserveringsysteem wordt ingevoerd, wordt gereserveerd of op order getraceerd, maar niet beide tegelijk. Hoe de systemen een artikel verwerken hangt af van hoe het artikel is ingesteld.  

 Het reserveringssysteem communiceert met het planningssysteem door planningsboodschappen op planningsregels te maken tijdens uitgevoerde planningen. Een planningsboodschap kan als een aanhangsel van een ordertraceringsrecord worden beschouwd. Planningsboodschappen, hetzij dynamisch gemaakt in ordertracering of tijdens de planning, bieden een handig hulpmiddel voor efficiënte voorraadplanning.  

> [!NOTE]  
>  Gereserveerde aantallen worden genegeerd door het planningsysteem. Dit betekent dat de vaste koppeling tussen voorziening en vraag niet kan worden gewijzigd via de planning.  

 Het reserveringssysteem vormt ook de structurele basis voor het artikeltraceringsysteem. Zie [Ontwerpdetails: artikeltracering](design-details-item-tracking.md) voor meer informatie.  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Reservering  
 Een reservering is een vaste koppeling die bepaalde vraag en een bepaald aanbod aan elkaar koppelt. Deze koppeling heeft rechtstreeks invloed op de verdere voorraadtransactie en zorgt voor de juiste vereffening van artikelposten voor waarderingsdoeleinden. Een reservering overschrijft de standaardwaarderingsmethode van een artikel. Zie [Ontwerpdetails: artikeltracering](design-details-item-tracking.md) voor meer informatie.  

 De pagina **Reservering** is toegankelijk vanaf alle orderregels van zowel soorten vraag als voorziening. Op deze pagina kan de gebruiker opgeven met welke vraag- of aanbodpost een reserveringskoppeling moet worden gemaakt. De reservering bestaat uit een paar records dat hetzelfde volgnummer deelt. Eén record heeft een negatief teken en verwijst naar de vraag. De andere record heeft een positief teken en wijst naar de voorziening. Deze records worden opgeslagen in de tabel **Reserveringspost** met statuswaarde **Reservering**. De gebruiker kan alle reserveringen bekijken op de pagina **Reserveringsposten**.  

### Compenseren in reserveringen  
 Reserveringen worden gemaakt op basis van beschikbare artikelaantallen. Artikelbeschikbaarheid wordt in het kort als volgt berekend:  

 beschikbaar aantal = voorraad + geplande ontvangsten - brutobehoefte  

 De volgende tabel toont de gegevens van de ordernetwerkentiteiten die deel uitmaken van de beschikbaarheidsberekening.  

||Veld in T27|Brontabel|Tabelfilter|Bronveld|  
|-|------------------|------------------|------------------|------------------|  
|**Voorraad**|Voorraad|Artikelpost|N.v.t.|Aantal|  
|**Geplande ontvangsten**|Vast gepl. orderontv. (Aantal)|Prod.-orderregel|=Vast gepland|Resterend aantal (Basis)|  
|**Geplande ontvangsten**|Vrijgeg. orderontv. (Aantal)|Prod.-orderregel|=Vrijgegeven|Resterend aantal (Basis)|  
|**Geplande ontvangsten**|Aant. op assemblageorder|Assemblagekop|=Volgorde|Resterend aantal (Basis)|  
|**Geplande ontvangsten**|Aantal in inkooporders|Inkoopregel|=Volgorde|Openstaand aantal (Basis)|  
|**Geplande ontvangsten**|Transferorderontv. (Aantal)|Transferregel|N.v.t.|Openstaand aantal|  
|**Brutobehoeften**|Aantal in verkooporders|Verkoopregel|=Volgorde|Openstaand aantal (Basis)|  
|**Brutobehoeften**|Geplande behoefte (Aantal)|Materiaalregel|<>Simulatie|Resterend aantal (Basis)|  
|**Brutobehoeften**|Aant. op assemblagecomponent|Assemblagelijn|=Volgorde|Resterend aantal (Basis)|  
|**Brutobehoeften**|Transferorderverz. (Aantal)|Transferregel|N.v.t.|Openstaand aantal|  

 Zie voor meer informatie [Ontwerpdetails: Beschikbaarheid in het magazijn](design-details-availability-in-the-warehouse.md).  

### Handmatige reservering  
 Wanneer een gebruiker opzettelijk een reservering maakt, verkrijgt de gebruiker volledig eigendom van en verantwoordelijkheid voor deze artikelen. Dit betekent dat de gebruiker een reservering ook handmatig moet wijzigen of annuleren. Door dergelijke handmatige wijzigingen kan automatische aanpassing van de betrokken reserveringen worden veroorzaakt.  

 De volgende tabel toont wanneer en welke wijzigingen kunnen optreden:  

|Gebruikersactie|Systeemreactie|  
|-----------------|---------------------|  
|Het gereserveerde aantal verlagen|De gerelateerde aantalvelden worden bijgewerkt.|  
|Datumvelden wijzigen|De gerelateerde datumvelden worden bijgewerkt.<br /><br /> **Opmerking:** als de vervaldatum van een vraag wordt veranderd en vóór de verzenddatum of de vervaldatum van de voorziening komt te liggen, wordt de reservering geannuleerd.|  
|De order verwijderen|De reservering is geannuleerd.|  
|Vestiging, opslaglocatie, variant, serienummer of lotnummer wijzigen|De reservering is geannuleerd.|  

> [!NOTE]  
>  Met de functie voor late binding kunnen ook reserveringen worden gewijzigd zonder de gebruiker te informeren, door niet-specifieke reserveringen van serie- of lotnummers te wisselen. Zie voor meer informatie 'Ontwerpdetails: Artikeltracering en reservering'.  

### Automatische reserveringen  
 De artikelkaart kan worden ingesteld om altijd automatisch te worden gereserveerd uit vraag, zoals verkooporders. In dat geval wordt de reservering gedaan op basis van voorraad, inkooporders, assemblageorders en productieorders. Er wordt een waarschuwing gegeven als het aanbod ontoereikend is.  

 Bovendien worden artikelen automatisch gereserveerd door verschillende planningsfuncties om vraag gekoppeld te houden aan specifiek aanbod. De ordertraceringsposten voor dergelijke planningskoppelingen bevatten **Reservering** in het veld **Status reservering** in de tabel **Reserveringspost**. Automatische reserveringen worden gemaakt in de volgende situaties:  

-   Een productieorder met meerdere niveaus waarvoor het veld **Productiebeleid** van het bovenliggende artikel en de onderliggende artikelen is ingesteld op **Op order produceren**. Het planningssysteem maakt reserveringen tussen de bovenliggende productieorder en de onderliggende productieorders om te zorgen dat ze samen worden verwerkt. Een dergelijke reserveringsbinding negeert de standaardwaarderings- en vereffeningsmethode voor het artikel.  

-   Een productie, assemblage of inkooporder waarvoor het veld **Bestelbeleid** van het betreffende artikel is ingesteld op **Order**. Het planningssysteem maakt reserveringen tussen de vraag en de geplande voorziening om te zorgen dat de specifieke voorziening wordt gemaakt. Zie voor meer informatie [Order](design-details-handling-reordering-policies.md#order).  

-   Er wordt een productieorder gemaakt van een verkooporder met de functie **Verkooporderplanning** en met een automatische reservering aan de verkooporder gekoppeld.  

-   Een assemblageorder die automatisch voor een verkooporderregel wordt gemaakt om aan het aantal in het veld **($ T_37_900 Qty. to Assemble to Order $)** te voldoen. Deze automatische reservering koppelt de verkoopvraag en de assemblagevoorziening, zodat de verkooporderverwerkers de component rechtstreeks kunnen aanpassen en aan de klant kunnen toezeggen. Bovendien koppelt de reservering de assemblage-uitvoer aan de verkooporderregel door middel van de verzendactiviteit die voldoet aan de order van de klant.  

 In het geval van voorzieningen of vraag die niet is toegewezen, wijst het planningssysteem automatisch een reserveringsstatus van de soort **Overschot** toe. Dit kan resulteren uit vraag die het gevolg is van voorspelde aantallen of door de gebruiker ingevoerde planningsparameters. Dit is legitiem overschot, dat door het systeem wordt herkend en geen planningsboodschappen tot gevolg heeft. Overschot moet ook werkelijke, overtollige voorzieningen of vraag zijn die niet-getraceerd blijft. Dit is een aanduiding om aan te geven dat het ordernetwerk niet in evenwicht is, waardoor het systeem planningsboodschappen verzendt. Een planningsboodschap die een wijziging van aantal voorstelt, verwijst altijd naar de soort **Overschot**. Zie voor meer informatie het gedeelte 'Voorbeeld: Ordertracering in verkoop, productie en transfers' in dit onderwerp.  

 Automatische reserveringen die worden gemaakt tijdens de planning, worden verwerkt op de volgende manieren:  

-   Deze zijn vereffend met artikelaantallen die deel uitmaken van de beschikbaarheidsberekening, zoals de handmatige reserveringen. Zie het onderdeel "Verschuiven in reserveringen" in dit onderwerp voor meer informatie.  

-   Ze worden opgenomen en mogelijk gewijzigd in opeenvolgende uitgevoerde planningen, in tegenstelling tot handmatig gereserveerde artikelen.  

## Ordertracering  
 Ordertracering helpt de planner een geldig leveringsplan te onderhouden door een overzicht te geven van de compensatie tussen vraag en aanbod in het ordernetwerk. De ordertraceringsrecords dienen als basis voor het maken van dynamische planningsboodschappen en planningsregelvoorstellen tijdens uitgevoerde planningen.  

> [!NOTE]  
>  Het ordertraceringssysteem compenseert beschikbare voorraad wanneer orders in het ordernetwerk worden ingevoerd. Dit geeft aan dat het systeem geen prioriteit geeft aan orders die mogelijk urgenter zijn op basis van de vervaldatum. Het is daarom aan de logica van het planningssysteem of de wijsheid van de planner om deze prioriteiten op een zinnige manier te ordenen.  

> [!NOTE]  
>  Ordertraceringsmethode en de functie Planningsboodschappen ophalen zijn niet geïntegreerd met Projecten. Dit betekent dat de vraag met betrekking tot een taak niet automatisch wordt getraceerd. Omdat het niet wordt getraceerd, kan hierdoor het gebruik van een bestaande aanvulling met projectinformatie worden getraceerd naar een andere vraag, bijvoorbeeld een verkooporder. Daarom kan de situatie optreden dat de gegevens over beschikbare voorraad niet zijn gesynchroniseerd.  

### Het ordernetwerk  
 Het ordertraceringssysteem is gebaseerd op het principe dat het ordernetwerk altijd in evenwicht moet zijn, waarbij elke vraag die wordt ingevoerd in het systeem wordt gecompenseerd door een overeenkomende voorziening, en vice versa. Het systeem verzorgt dit door logische koppelingen tussen alle vraag- en voorzieningsposten in het ordernetwerk te identificeren.  

 Dit principe geeft aan dat een wijziging in de vraagresultaten ertoe leidt dat de voorzieningenzijde van het ordernetwerk niet meer in evenwicht is. Andersom leidt een wijziging in voorzieningenresultaten tot een corresponderende onbalans aan de vraagzijde van het ordernetwerk. In werkelijkheid bevindt het ordernetwerk zich in een constante stroom terwijl gebruikers orders invoeren, wijzigen en verwijderen. Tijdens ordertracering worden orders dynamisch verwerkt, in reactie op elke wijziging op het moment dat deze het systeem binnenkomt en onderdeel wordt van het ordernetwerk. Zodra nieuwe ordertraceringsrecords worden gemaakt, is het ordernetwerk in balans, maar slechts tot de volgende wijziging zich voordoet.  

 Om de transparantie te verhogen van berekeningen in het planningssysteem, worden op de pagina **Niet-getraceerde planningselementen** niet-getraceerde aantallen weergegeven, die het verschil in aantal aangeven tussen bekende vraag en voorgestelde voorziening. Elke regel op de pagina verwijst naar de oorzaak van het bovenmatige aantal, bijvoorbeeld **Raamcontract**, **Veiligheidsvoorraadniveau**, **Vast bestelaantal**, **Min. bestelaantal**, **Afronding** of **Demping**.  

### Compenseren in ordertracering  
 In tegenstelling tot reserveringen, die alleen kunnen worden gedaan op basis van beschikbare artikelaantallen, is ordertracering mogelijk op basis van alle ordernetwerkentiteiten die deel uitmaken van de berekening van nettovereisten van het planningssysteem. De nettobehoeften worden als volgt berekend:  

 nettobehoeften = brutobehoeften + bestelpunt - geplande ontvangsten - geplande ontvangsten - voorspelde beschikbare voorraad  

> [!NOTE]  
>  Vraag die is gerelateerd aan prognoses of planningsparameters is niet ordergetraceerd.  

### Voorbeeld: Ordertracering in verkoop, productie en transfers  
 In het volgende scenario wordt aangegeven welke ordertraceringsposten worden gemaakt in de tabel **Reserveringspost** als gevolg van verschillende ordernetwerkwijzigingen.  

 Stel dat er de volgende gegevens zijn voor twee artikelen die zijn ingesteld voor ordertracering.  

|Artikel 1|Name|"Component"|
|-|-|-|
||Beschikbaarheid|100 eenheden op WEST-vestiging<br /><br />- 30 eenheden van LOTA<br />- 70 eenheden van LOTB|  
|Artikel 2|Name|“Gefabriceerd artikel”|
||Productiestuklijst|aant. 1 per "Component"|  
||Vraag|Verkoop voor 100 eenheden op OOST-vestiging|  
||Voorraad|Vrijgegeven productieorder (gegenereerd met de functie **Verkooporderplanning** voor de verkoop van 100 eenheden)|  

Op de pagina **Productie-instellingen** wordt het veld **Onderdelen op vestiging** ingesteld op **ROOD**.

 Er bestaan de volgende ordertraceringsposten in de tabel **Reserveringspost** op basis van de gegevens in de tabel.  

 ![Eerste voorbeeld van ordertraceringsposten in de tabel Reserveringspost.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### Volgnummers 8 en 9  
 Voor de onderdelenlijst voor respectievelijk LOTA en LOTB worden ordertraceringskoppelingen gemaakt van de vraag in tabel 5407, **Materiaalregel**, naar het aanbod in tabel 32, **Artikelpost**. Het veld **Status reservering** bevat **Tracering** om aan te geven dat deze posten dynamische ordertraceringkoppelingen tussen voorzieningen en vraag.  

> [!NOTE]  
>  Het veld **Lotnr.** is leeg op de vraagregels, omdat de lotnummers niet zijn opgegeven op de materiaalregels van de vrijgegeven productieorder.  

### Volgnummers 10  
 Vanuit de verkoopvraag in tabel 37, **Verkoopregel**, wordt een ordertraceringskoppeling gemaakt naar het aanbod in tabel 5406, **Prod.-orderregel**. Het veld **Status reservering** bevat **Reservering** en het veld **Binding** bevat het veld **Order-naar-order**. Dit komt doordat de vrijgegeven productieorder specifiek voor de verkooporder is gegenereerd en gekoppeld moet blijven, in tegenstelling tot ordertraceringskoppelingen met de reserveringstatus **Tracering**, die dynamisch worden gemaakt en gewijzigd. Zie het onderdeel “Automatische reserveringen” in dit onderwerp voor meer informatie.  

 Op dit punt in het scenario worden de 100 eenheden van LOTA en LOTB overgebracht naar de OOST-vestiging met een transferorder.  

> [!NOTE]  
>  Alleen de transferorderverzending wordt op dit moment geboekt, niet de ontvangst.  

 Nu bevat de tabel **Reserveringspost** de volgende ordertraceringsposten.  

 ![Tweede voorbeeld van ordertraceringsposten in de tabel Reserveringspost.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### Volgnummers 8 en 9  
 De reserveringsstatus van ordertraceringsposten voor de twee lots van het onderdeel die vraag reflecteren in tabel 5407, verandert van **Tracering** in **Overschot**. De reden is dat de goederen waaraan ze eerder zijn gekoppeld, in tabel 32, zijn gebruikt door de verzending van de transferorder.  

 Werkelijk overschot, zoals in dit geval, is een reflectie van bovenmatig aanbod of vraag die niet-getraceerd blijft. Het is een indicatie van onbalans in het ordernetwerk, waardoor het planningssysteem een planningsboodschap genereert, tenzij het dynamisch wordt opgelost.  

### Volgnummers 12 tot 16  
 Omdat de twee lots van het materiaal op de transferorder worden geboekt als verzonden maar niet ontvangen, zijn alle gerelateerde positieve ordertraceringsposten van het reserveringsoort **Overschot**, wat aangeeft dat deze niet worden toegewezen aan vraag. Voor elk lotnummer heeft één post betrekking op tabel 5741, **Transferregel**, en één post op de artikelpost bij de in-transit vestiging.  

 Op dit punt in het scenario wordt de transferorder van de onderdelen van de OOST-vestiging naar de WEST-vestiging geboekt als ontvangen.  

 Nu bevat de tabel **Reserveringspost** de volgende ordertraceringsposten.  

 ![Derde voorbeeld van ordertraceringsposten in de tabel Reserveringspost.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

 De ordertraceringsposten zijn nu gelijk aan het eerste punt in het eerste scenario voordat de transferorder werd geboekt als alleen-verzenden, behalve dat posten voor het onderdeel nu de reserveringstatus **Overschot** hebben. Dit komt doordat er nog materiaalbehoefte is op de WEST-vestiging, wat aangeeft dat het veld **Vestiging** op de materiaalregel op de productieorder **WEST** bevat, zoals ingesteld in het venster **Onderdelen op vestiging**. De voorziening die eerder is toegewezen voor deze vraag, is overgebracht naar de OOST-vestiging en kan nu niet volledig worden getraceerd tenzij de materiaalbehoefte op de productieorderregel wordt veranderd in de OOST-vestiging.  

 Op dit punt in het scenario wordt het veld **Vestiging** op de productieorderregel ingesteld op **OOST**. Bovendien worden op de pagina **Artikeltraceringsregels** de 30 eenheden van LOTA en 70 eenheden van LOTB toegewezen aan de productieorderregel.  

 Nu bevat de tabel **Reserveringspost** de volgende ordertraceringsposten.  

 ![Vierde voorbeeld van ordertraceringsposten in de tabel Reserveringspost.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### Volgnummers 21 en 22  
 Aangezien de materiaalbehoefte is gewijzigd naar de OOST-vestiging en de voorziening beschikbaar is als artikelposten op de OOST-vestiging, worden alle ordertraceringsposten voor de twee lotnummers nu volledig getraceerd, wat wordt aangegeven door de reserveringstatus **Tracering**.  

 Het veld **Lotnr.** wordt nu gevuld in de ordertraceringspost voor tabel 5407, omdat de lotnummers zijn toegewezen aan de productieordermateriaalregels.  

 Voor meer voorbeelden van ordertraceringsposten in de tabel **Reserveringspost** raadpleegt u de whitepaper "Tabel Reserveringspost" op [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348) (vereist aanmelding).

## Planningsboodschap  
 Wanneer het ordertraceringssysteem detecteert dat het ordernetwerk niet in evenwicht is, wordt automatisch een planningsboodschap gemaakt om de gebruiker te waarschuwen. Planningsboodschappen worden door het systeem geproduceerd voor gebruikersacties die de details van de onbalans opgeven en de suggesties over hoe de balans in het ordernetwerk kan worden hersteld. Ze worden weergegeven als planningsregels op de pagina **Planningsvoorstel** wanneer u **Planningsboodschappen ophalen** kiest. Bovendien worden de planningsboodschappen weergegeven op planningsregels die door de planning worden gegenereerd in overeenstemming met de suggesties van het planningssysteem over hoe de balans in het ordernetwerk kan worden hersteld. In beide gevallen worden de voorstellen in het ordernetwerk uitgevoerd wanneer u **Planningsboodschap uitvoeren** kiest.  

 Een planningsboodschap betreft één stuklijstniveau tegelijk. Als de gebruiker de planningsboodschap accepteert, kan dit leiden tot meer planningsboodschappen op het volgende stuklijstniveau.  

 De volgende tabel toont de planningsboodschappen die bestaan.  

|Planningsboodschap|Description|  
|--------------------|---------------------------------------|  
|**Aantal wijzigen**|Wijzigt het aantal op een bestaande voorzieningenorder om te voldoen aan gewijzigde of nieuwe vraag.|  
|**Herplannen**|Herplant de vervaldatum op een bestaande order.|  
|**Herplannen en aantal wijzigen**|Herplant de vervaldatum en wijzigt het aantal op een bestaande order.|  
|**Nieuw**|Maakt een nieuwe order als niet aan de vraag kan worden voldaan door een van de eerdere planningsboodschappen.|  
|**Annuleren**|Hiermee annuleert u een bestaande order.|  

 Het ordertraceringssysteem probeert altijd om een verstoord evenwicht in het bestaande ordernetwerk op te lossen. Als dit niet mogelijk is, wordt er een planningsboodschap gegenereerd om een nieuwe order te maken. Hierna volgt de prioriteitlijst die het ordertraceringssysteem gebruikt om te bepalen hoe het evenwicht wordt hersteld. Als er aanvullende vraag in het ordernetwerk wordt ingevoerd, probeert het systeem ordertracering uit te voeren door de volgende controles:  

1.  Controleer op bovenmatige voorziening in de bestaande ordertraceringsrecord voor deze vraag.  
2.  Controleer op geplande ontvangsten op volgorde van ontvangstdatum. De laatst mogelijke datum wordt geselecteerd.  
3.  Controleer op beschikbare voorraad.  
4.  Controleer of er een voorzieningenorder bestaat in de huidige ordertraceringsrecord. In dat geval geeft het systeem een planningsboodschap van het type **Wijzigen** om de order te verhogen.  
5.  Controleer of er geen voorzieningenorder bestaat in de huidige ordertraceringsrecord. In dat geval geeft het systeem een planningsboodschap van het type **Nieuw** om een nieuwe order te maken.  

 Openstaande vraag doorloopt de lijst en compenseert op elk punt de beschikbare voorraad. Eventuele resterende vraag wordt altijd gedekt door controle 4 of controle 5.  

 Als er een afname van vraag optreedt, probeert het ordertraceringssysteem de onbalans op te lossen door de vorige controles in omgekeerde volgorde uit te voeren. Dit betekent dat de bestaande planningsboodschappen kunnen worden gewijzigd of zelfs worden verwijderd, indien nodig. Het ordertraceringssysteem geeft altijd het nettoresultaat van berekeningen weer aan de gebruiker.  

## Ordertracering en planning  
 Wanneer het planningssysteem wordt uitgevoerd, worden alle bestaande ordertraceringsrecords en planningsboodschapposten verwijderd en opnieuw gemaakt als planningsregelvoorstellen volgens vraag-voorzieningcombinaties en prioriteiten. Wanneer de planningsprocedure is voltooid, is het ordernetwerk in evenwicht.  

### Planningssysteem versus ordertracering en planningsboodschappen  
 In de volgende vergelijking worden de verschillen getoond tussen de methoden die door het planningssysteem worden gebruikt om planningsregelvoorstellen te maken, en de methoden die door het ordertraceringssysteem worden gebruikt om ordertraceringsrecords en planningsboodschappen te maken.  

-   Het planningssysteem verwerkt het volledige vraag-voorzieningpatroon van een bepaald artikel, terwijl ordertracering de order verwerkt waardoor deze is geactiveerd.  

-   Het planningssysteem verwerkt alle niveaus van de stuklijsthiërarchie, terwijl ordertracering één stuklijstniveau per keer verwerkt.  

-   Het planningssysteem legt koppelingen tussen vraag en voorzieningen op basis van de prioriteitsvervaldatum. Ordertracering creëert koppelingen tussen vraag en aanbod op basis van de orderinvoervolgorde.  

-   Het planningssysteem houdt rekening met planningsparameters, terwijl ordertracering dit niet doet.  

-   Het planningssysteem maakt koppelingen in een door de gebruiker geactiveerde batchmodus wanneer vraag en voorziening worden vereffend, terwijl bij ordertracering de koppelingen automatisch en dynamisch worden gemaakt wanneer de gebruiker orders invoert.  

## Zie ook  
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
