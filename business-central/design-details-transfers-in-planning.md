---
title: 'Ontwerpdetails: Transfers in planning'
description: Leer hoe u transferorders als bron van aanbod gebruikt bij het plannen van voorraadniveaus.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
---
# <a name="design-details-transfers-in-planning" />Ontwerpdetails: Transfers in planning

Transferorders zijn ook een voorzieningenbron bij het werken op SKU-niveau. Als meerdere vestigingen (magazijnen) worden gebruikt, kan de SKU-aanvullingsmethode worden ingesteld op Transfer, wat aangeeft dat de vestiging wordt aangevuld door goederen van een andere vestiging over te brengen. In een situatie met meer magazijnen hebt u mogelijk een keten van transfers. Aanbod naar GROENE vestiging wordt overgezet van GEEL, aanbod naar GEEL wordt overgezet van ROOD, enzovoort. Aan het begin van de keten is er een aanvullingssysteem **Prod.-order** of **Inkoop**.  

![Voorbeeld van overdrachtsstroom.](media/nav_app_supply_planning_7_transfers1.png "Voorbeeld van overdrachtsstroom")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Als u de volgende situaties vergelijkt, is het duidelijk dat de planningstaak in de laatste complex kan worden:

* Een aanvulorder staat rechtstreeks tegenover een vraagorder
* Een verkooporder wordt geleverd via een keten van SKU-transfers

Als de vraag verandert, kan dit een rimpeleffect door de keten veroorzaken. Alle transferorders, plus de inkoop- en productieorder aan de andere kant van de keten, zullen moeten worden bijgewerkt om vraag en aanbod weer in evenwicht te brengen.  

![Voorbeeld van evenwicht tussen vraag en aanbod bij overdrachten.](media/nav_app_supply_planning_7_transfers2.png "Voorbeeld van evenwicht tussen vraag en aanbod bij overdrachten")  

## <a name="why-is-a-transfer-a-special-case" />Waarom is een transfer een speciaal geval?

Transferorders zijn vergelijkbaar met andere orders, zoals inkoop- en productieorders. Achter de schermen ligt het echter heel anders.  

Een verschil is dat een transferregel zowel vraag als aanbod vertegenwoordigt. Het uitgaande deel dat wordt verzonden, is vraag. Het inkomende deel, dat moet worden ontvangen bij de nieuwe vestiging, is aanbod op die vestiging.  

![Inhoud van de pagina Transferorder.](media/nav_app_supply_planning_7_transfers3.png "Inhoud van de transferorderpagina")  

Dit betekent dat wanneer [!INCLUDE [prod_short](includes/prod_short.md)] de aanbodzijde van de transfer wijzigt, een vergelijkbare wijziging aan de vraagkant moet worden gemaakt.  

## <a name="transfers-are-dependent-demand" />Transfers zijn afhankelijke vraag

De relatie tussen vraag en aanbod is vergelijkbaar met materiaal op productieorderregels. Het verschil is dat materiaal op productieorderregels zich op het volgende planningsniveau bevindt en een ander artikel heeft. De twee delen van de transfer bevinden zich op hetzelfde niveau voor hetzelfde artikel.  

Een belangrijke overeenkomst is dat materiaal en transfers afhankelijk zijn van vraag. De vraag van een transferregel wordt bepaald door de aanbodzijde van de transfer. Als het aanbod verandert, heeft dat direct invloed op de vraag.

Tenzij de planningsflexibiliteit Geen is, moet een transferregel nooit worden verwerkt als onafhankelijke vraag in de planning.  

In de planningsprocedure moet alleen met transfervraag rekening worden gehouden nadat de aanbodzijde is verwerkt door het planningssysteem. Voordat die verwerking plaatsvindt, is de daadwerkelijke vraag niet bekend. De volgorde van wijzigingen is belangrijk voor transferopdrachten.  

## <a name="planning-sequence" />Planningsvolgorde

De volgende afbeelding toont een voorbeeld van deze reeks transfers.  

![Voorbeeld van een eenvoudige overdrachtsstroom.](media/nav_app_supply_planning_7_transfers4.png "Voorbeeld van een eenvoudige overdrachtsstroom")  

In dit voorbeeld bestelt een klant het artikel op vestiging GROEN. Vestiging GROEN wordt voorzien via transfer uit het centrale magazijn ROOD. Het centrale magazijn ROOD wordt bevoorraad door transfer uit productie op vestiging BLAUW.  

In dit voorbeeld start het planningssysteem met de klantvraag en wordt achterwaarts door de keten gewerkt. De vragen en voorzieningen worden per vestiging verwerkt.  

![Leveringsplanning met overdrachten.](media/nav_app_supply_planning_7_transfers5.png "Leveringsplanning met overdrachten")  

## <a name="transfer-level-code" />Transferniveaucode

De transferniveaucode van de SKU bepaalt de volgorde waarin het planningssysteem vestigingen verwerkt.  

De transferniveaucode is een intern veld. Het veld wordt berekend en opgeslagen in de SKU wanneer u de SKU maakt of wijzigt. De berekening wordt uitgevoerd voor alle SKU's voor een bepaalde combinatie van artikel en artikelvariant. De berekening gebruikt de locatiecode en de transfer van-code om de te gebruiken route voor de SKU's te bepalen. De berekening zorgt ervoor dat alle aanvragen verwerkt worden.  

De transferniveaucode is 0 voor SKU's met de aanvullingsmethode Inkoop of Productieorder, -1 voor het eerste transferniveau, -2 voor het tweede, enzovoort. In het in de vorige sectie beschreven voorbeeld zouden de niveaus daarom zijn -1 voor ROOD en -2 voor GROEN, zoals aangegeven in de volgende illustratie.  

![Inhoud van pagina SKU-kaart.](media/nav_app_supply_planning_7_transfers6.gif "Inhoud van pagina SKU-kaart")  

Bij het bijwerken van een SKU detecteert het planningssysteem of aanvullingssystemen voor SKU's kringverwijzingen hebben.  

## <a name="planning-transfers-without-sku" />Planningstransfers zonder SKU

Voor minder geavanceerde magazijnconfiguraties kunt u locaties gebruiken en handmatige overboekingen tussen locaties uitvoeren, zelfs als u geen SKU's gebruikt. De transfer kan bijvoorbeeld betrekking hebben op een verkooporder op die vestiging. Het planningssysteem reageert op veranderingen in de vraag.  

Voor handmatige transfers analyseert het planningssysteem transferorders en plant vervolgens de volgorde waarin de vestigingen moeten worden verwerkt. Intern zal het planningssysteem tijdelijke SKU's met transferniveaucodes gebruiken.  

![Transferniveaucode.](media/nav_app_supply_planning_7_transfers7.png "Transferniveaucode")  

Als op een vestiging meerdere transfers bestaan, definieert de eerste transferorder de planningsrichting. Transfers die in de tegengestelde richting lopen, worden geannuleerd.  

## <a name="changing-quantity-with-reservations" />Aantal met reserveringen wijzigen

Bij het wijzigen van hoeveelheden in een aanbod houdt het planningssysteem rekening met reserveringen. De gereserveerde hoeveelheid vertegenwoordigt de ondergrens voor hoeveel het aanbod moet worden verminderd.  

Houd bij het wijzigen van de hoeveelheid op een transferorderregel rekening met de ondergrens. De ondergrens is de hoogste gereserveerde hoeveelheid van de uitgaande en inkomende transferregels.

Een transferorderregel van 117 stuks is bijvoorbeeld gereserveerd voor de volgende regels:

* Een verkoopregel van 46
* Een inkoopregel van 24

Ook al heeft de inkomende zijde mogelijk een overaanbod, u kunt de transferregel niet verlagen tot onder de 46.  

![Reserveringen bij transferplanning.](media/nav_app_supply_planning_7_transfers8.png "Reserveringen bij transferplanning")  

## <a name="changing-quantity-in-a-transfer-chain" />Aantal in een transferketen wijzigen

Hier is een voorbeeld van wat er gebeurt als u een hoeveelheid wijzigt in een transferwijziging.

Uitgangspunt is een evenwichtige situatie met een transferketen die een verkooporder van 27 aanbiedt op vestiging ROOD. Er is een overeenkomstige inkooporder op vestiging BLAUW. Beide transfers gaan via vestiging ROZE. Er zijn twee transferopdrachten, BLAUW-ROZE en ROZE-ROOD.  

![De hoeveelheid in de transferplanning wijzigen 1.](media/nav_app_supply_planning_7_transfers9.png "De hoeveelheid in de transferplanning wijzigen 1")  

Nu maakt de planner op de ROZE vestiging een reservering voor de inkoop.  

![De hoeveelheid in de transferplanning wijzigen 2.](media/nav_app_supply_planning_7_transfers10.png "De hoeveelheid in de transferplanning wijzigen 2")  

De reservering betekent doorgaans dat het planningssysteem de inkooporder en de transfervraag negeert. Zolang er saldo is, is er geen probleem. Maar wat gebeurt er als de vestiging ROOD de order verandert van 27 in 22?  

![De hoeveelheid in de transferplanning wijzigen 3.](media/nav_app_supply_planning_7_transfers11.png "De hoeveelheid in de transferplanning wijzigen 3")  

Wanneer het planningssysteem opnieuw wordt uitgevoerd, moeten overtollige voorzieningen worden gewist. De reservering vergrendelt echter de inkoop en de transfer op een aantal van 27.  

![De hoeveelheid in de transferplanning wijzigen 4.](media/nav_app_supply_planning_7_transfers12.png "De hoeveelheid in de transferplanning wijzigen 4")  

De ROZE-RODE transfer is gereduceerd tot 22. Het inkomende deel van de BLAUW-ROZE transfer is niet gereserveerd, maar het uitgaande deel wel. De reservering betekent dat u de hoeveelheid niet kunt verminderen tot minder dan 27.  

## <a name="lead-time-calculation" />Berekening van levertermijn

Bij de berekening van de vervaldatum van een transferorder wordt rekening gehouden met verschillende soorten levertermijn.  

De volgende doorlooptijden zijn actief bij het plannen van een transferorder:  

* Uitgaande magazijnverwerkingstijd  
* Verzendtijd  
* Inkomende magazijnverwerkingstijd  

Op de planningsregel worden de volgende velden gebruikt om informatie over de berekening te geven:  

* Transferverzenddatum  
* Begindatum  
* Einddatum  
* Vervaldatum  

De verzenddatum van de transferregel wordt weergegeven in het veld **Transferverzenddatum**. De ontvangstdatum van de transferregel wordt weergegeven in het veld **Vervaldatum**.  

De begin- en einddatum worden gebruikt om de werkelijke vervoersperiode te omschrijven.  

De volgende afbeelding toont de interpretatie van de begindatum/-tijd en einddatum/-tijd op planningsregels voor transferorders.  

![Centrale datum-tijden in overdrachtsplanning.](media/nav_app_supply_planning_7_transfers13.png "Centrale datum-tijden in overdrachtsplanning")  

Het voorbeeld toont de volgende berekeningen:  

* Verzenddatum + Uitgaande verwerking = Begindatum  
* Begindatum + Verzendtijd = Einddatum  
* Einddatum + Inslagtijd = Ontvangstdatum  

## <a name="safety-lead-time" />Veiligheidstijd

Het veld **Std. veiligheidstijd** op de pagina **Productie-instellingen** en het gerelateerde veld **Veiligheidstijd** op de pagina **Artikel** worden niet meegenomen in berekeningen van transferorders. Wel heeft de veiligheidstijd invloed op het totale plan. De veiligheidstijd is van invloed op de aanvullingsopdracht (aankoop of productie) aan het begin van de transferketen. Dat is het punt waar de artikelen zijn geplaatst op de locatie van waaruit ze worden overgebracht.  

![Elementen van de vervaldatum van de overdracht.](media/nav_app_supply_planning_7_transfers14.png "Elementen van de vervaldatum van de overdracht")  

Op de productieorderregel: Einddatum + Veiligheidstijd + Inkomende magazijnverwerkingstijd = Vervaldatum.  

Op de inkooporderregel: Geplande ontvangstdatum + Veiligheidstijd + Inkomende magazijnverwerkingstijd = Verwachte ontvangstdatum.  

## <a name="reschedule" />Herplannen

Bij het opnieuw plannen van een bestaande transferregel zoekt het planningssysteem het uitgaande deel en wijzigt het de datum-tijd.

> [!NOTE]
> Als er een veiligheidstijd is gedefinieerd, ontstaat er een gat tussen de verzending en de ontvangst. De veiligheidstijd kan bestaan uit meer elementen, zoals de transporttijd en de magazijnverwerkingstijd. Op een tijdpad zal het planningssysteem terug in de tijd gaan terwijl de elementen worden afgestemd.  

![De vervaldatum in de transferplanning wijzigen.](media/nav_app_supply_planning_7_transfers15.png "De vervaldatum in de transferplanning wijzigen")  

Wanneer u de vervaldatum op een transferregel wijzigt, moet daarom de veiligheidstijd worden berekend om de uitgaande kant van de transfer bij te werken.  

## <a name="serial-and-lot-numbers-in-transfer-chains" />Serie- en lotnummers in transferketens

Als de vraag serie- of lotnummers gebruikt en u de planningsengine uitvoert, worden transferorders gemaakt. Voor meer informatie over dit concept raadpleegt u Artikelkenmerken. Als echter serie- of lotnummers worden verwijderd uit de vraag, gebruiken de transferorders nog steeds serie- of lotnummers en worden ze dus genegeerd door de planning (niet verwijderd).  

## <a name="order-to-order-links" />Order-naar-order koppelingen

In dit voorbeeld is de SKU BLAUW ingesteld met een bestelbeleid **Order**. De SKU's ROZE en ROOD hebben het bestelbeleid **Lot-voor-Lot**. Het maken van een verkooporder voor 27 op locatie ROOD leidt tot een keten van transfers. De laatste transfer is op locatie BLAUW en is gereserveerd met binding. In dit voorbeeld zijn de reserveringen geen harde reserveringen die door de planner zijn gemaakt op locatie ROZE. Het planningssysteem maakt de bindingen. Het belangrijkste verschil is dat het planningssysteem laatstgenoemde kan wijzigen.  

![Order-naar-order koppelingen in transferplanning.](media/nav_app_supply_planning_7_transfers16.png "Order-naar-order koppelingen in transferplanning")  

Als de vraag van 27 verandert in 22, verlaagt het planningssysteem het aantal automatisch in de keten. Ook de bindende reservering wordt verkleind.  

## <a name="see-also" />Zie ook

[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
[Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md)   
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
[Ontwerpdetails: Planning met of zonder vestigingen](production-planning-with-without-locations.md)   
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
