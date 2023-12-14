---
title: 'Volledige planning, MPS of MRP uitvoeren'
description: 'Met het planningssysteem kan op verzoek de MPS (Master Production Schedule) of MRP (Material Requirements Planning) worden berekend, of beide tegelijk.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000852, 99000860'
ms.date: 06/22/2021
ms.author: bholtorf
---
# Volledige planning, MPS of MRP uitvoeren

De termen "planningsvoorstel uitvoeren" en "MRP uitvoeren" verwijzen naar het berekenen van het hoofdproductieschema en de benodigde materialen op basis van de werkelijke en de geprognosticeerde behoefte. Met het planningssysteem kan op verzoek de MPS (Master Production Schedule) of MRP (Material Requirements Planning) worden berekend, of beide tegelijk.  

-   MPS is de berekening van een hoofdproductieschema op basis van de werkelijke vraag en de vraagprognose. De MPS-berekening wordt gebruikt voor eindartikelen met een voorspelling of een verkooporderregel. Deze artikelen worden MPS-artikelen genoemd en worden dynamisch geïdentificeerd wanneer de berekening start.  
-   MRP is de berekening van het benodigde materiaal op basis van de werkelijke vraag naar materiaal en de vraagprognose op materiaalniveau. MRP wordt alleen berekend voor artikelen die geen MPS-artikelen zijn. Het uiteindelijke doel van MRP is om in tijd gefaseerde formele plannen te leveren, per artikel, om het juiste artikel op de juiste tijd te kunnen leveren, op de juiste plaats en in de juiste aantallen.  

De planningsalgoritmen die worden gebruikt voor MPS en MRP zijn identiek. De planningsalgoritmen hebben betrekking op de nettoberekening, het hergebruik van bestaande aanvullingsorders en planningsboodschappen. Er wordt door het planningssysteem gekeken naar wat er nodig is of zal zijn (behoefte) en wat er in voorraad is of verwacht wordt (voorziening.) Wanneer deze aantallen tegen elkaar tot een nettowaarde worden teruggebracht, geeft [!INCLUDE[prod_short](includes/prod_short.md)] planningsboodschappen af. Planningsboodschappen zijn suggesties voor het opstellen van een nieuwe order, het wijzigen van een order (aantal of datum), of het annuleren van een order die al is besteld. De term 'order' omvat inkooporders, assemblageorders, productieorders en transferorders.

Koppelingen die door de planningsengine tussen vraag en bijbehorend aanbod worden gemaakt, kunnen worden getraceerd op de pagina **Ordertracering**. Zie [Relatie tussen vraag en voorzieningen bijhouden](production-how-track-demand-supply.md) voor meer informatie.   

De juistheid van de planningsresultaten hangt af van de instellingen in de artikelkaarten, productiestuklijsten en bewerkingsplannen.  

## Methoden voor het genereren van een plan  

-   **Regeneratief plan berekenen:** met deze functie verwerkt of regenereert u het materiaalplan. Dit proces begint met het verwijderen van alle geplande voorzieningenorders die op dat moment geladen zijn. Alle artikelen in de database worden herpland.  
-   **Mutatieplan berekenen**: met deze functie verwerkt u een mutatieplan. Artikelen worden meegenomen in een mutatieplanning van twee soorten wijzigingen:  
    - **Wijzigingen in vraag en aanbod**: deze omvatten wijzigingen in de aantallen op verkooporders, vraagprognoses, assemblageorders, productieorders of inkooporders. Een niet/geplande voorraadwijziging wordt ook beschouwd als een wijziging van het aantal.  
    - **Wijzigingen in de planningsparameters**: deze omvatten wijzigingen in de veiligheidsvoorraad, bestelpunt, bewerkingsplan, stuklijst en wijzigingen in het tijdsinterval of de levertermijn.  
-   **Planningsboodschappen ophalen**: deze functie doet dienst als een planningstool voor de korte termijn, doordat planningsboodschappen worden afgegeven om de gebruiker op de hoogte te stellen van wijzigingen die zijn doorgevoerd sinds het laatste regeneratieve of mutatieplan is berekend.  

Voor elke geplande methode, maakt [!INCLUDE[prod_short](includes/prod_short.md)] voorstelposten, ervan uitgaande dat onbeperkt capaciteit beschikbaar is. Capaciteit van kostenplaatsen en bewerkingsplaatsen worden niet meegenomen als u schema's ontwikkelt.  

> [!IMPORTANT]  
>  De functie Regeneratief plan berekenen is het meest gebruikte proces. De functies Planning berekenen en Planningsboodschappen uitvoeren kunnen echter worden gebruikt voor het uitvoeren van het proces Mutatieplan berekenen.  
>   
>  De functie Planningsboodschappen ophalen kan worden uitgevoerd tussen de uitvoering van mutatieplanberekening en regeneratieve planning om onmiddellijk een overzicht te krijgen van de effecten van wijzigingen in het schema, maar is niet bedoeld als vervanging voor volledige mutatieplanberekening of regeneratieve planning.  

## Een planningsvoorstel berekenen  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planningsvoorstellen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Regeneratief plan berekenen** om de pagina **Planning berekenen** te openen.  
3.  Vul op het sneltabblad **Opties** de velden in, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Selecteer de optie on de berekening van een hoofdproductieschema te initiëren. Artikelen met open verkooporders of vraagprognoses worden meegenomen in deze procedure.|  
    |**MRP**|Selecteer de optie om de berekening van de materiaalbehoefteplanning te initiëren. Artikelen met afhankelijke vraag worden meegenomen in deze procedure. Normaal gesproken worden MPS en MRP gelijktijdig uitgevoerd. Als u MPS en MRP gelijktijdig wilt uitvoeren, moet er een vinkje worden gezet in het veld **Gecombineerd MPS/MRP berek.** op het sneltabblad **Planning** op de pagina **Productie-instellingen**.|  
    |**Begindatum**|Deze datum wordt gebruikt om de beschikbaarheid van voorraad te evalueren. Als van een artikel minder in voorraad is dan vastgelegd voor het bestelpunt, wordt met voorwaartse planning een aanvullingsorder opgesteld vanaf deze datum. Als van een artikel minder is dan de veiligheidsvoorraad (met ingang van de begindatum), wordt met achterwaartse planning een aanvullingsorder opgesteld met de begindatum van de planning als vervaldatum.|  
    |**Einddatum**|Dit is de einddatum van de planningshorizon. Na deze datum wordt noch met vraag noch met voorzieningen rekening gehouden. Als de bestelfrequentie zich uitstrekt voorbij de einddatum, is de effectieve planningshorizon voor dat artikel gelijk aan de orderdatum + bestelfrequentie.<br /><br /> De planningshorizon is de hoeveelheid tijd waarover het plan zich uitstrijkt. Als de horizon te kort is, worden artikelen met een langere doorlooptijd niet op tijd besteld. Als de horizon te kort is, wordt te veel tijd besteed aan het bekijken en verwerken van informatie die waarschijnlijk gewijzigd wordt voordat deze nodig is. Het is mogelijk om één planningshorizon in te stellen voor productie en een langere voor inkoop, maar dit is niet vereist. Er moet een planningshorizon voor inkoop en productie worden ingesteld die de cumulatieve doorlooptijd voor onderdelen bestrijkt.|  
    |**Stoppen en eerste fout tonen**|Selecteer de optie om de de planning te stoppen zodra er een fout wordt aangetroffen. Tegelijkertijd wordt een boodschap weergegeven met informatie over de (eerste) fout. Als er sprake is van een fout, worden alleen de planningsregels die gemaakt zijn voordat de fout werd geconstateerd, in het planningsvoorstel weergegeven. Als u dit veld niet selecteert, gaat de batchverwerking **Planning berekenen** door totdat deze voltooid is en wordt de batchverwerking niet onderbroken door fouten. Als er een of meer fouten zijn, wordt na afloop een bericht weergegeven waarin staat hoeveel artikelen dit betreft. Vervolgens wordt de pagina **Planningfoutenlogboek** geopend met meer informatie over de fout en koppelingen naar de betreffende artikelkaart(en).|  
    |**Prognose gebruiken**|in dit veld selecteert u een prognose die als vraag wordt opgenomen tijdens de batchverwerking voor de planning. De standaardprognose wordt ingesteld op het sneltabblad **Planning** van de pagina **Productie-instellingen**.|  
    |**Prognose uitsluiten voor**|Definieer hoeveel van de geselecteerde prognose u wilt opnemen in de planning die wordt uitgevoerd. U doet dit door een datum in te voeren waarvóór de prognose niet moet worden meegenomen, zodat u oude informatie kunt uitsluiten.|  
    |**Planningsparameters voor uitzonderingswaarschuwingen respecteren**|Standaard is dit selectievakje ingeschakeld.<br /><br /> Voorzieningen op planningsregels met waarschuwingen wordt gewoonlijk niet gewijzigd volgens planningsparameters. In plaats daarvan stelt het planningssysteem alleen een voorziening ter dekking van de hoeveelheid van de exacte vraag voor. U kunt echter bepaalde planningsparameters voor planningsregels definiëren die moeten worden gerespecteerd bij bepaalde waarschuwingen.<br /><br />|  

4.  Op het sneltabblad **Artikel** kunt u filters instellen om de planning uit te voeren op basis van artikel, artikelomschrijving of vestiging.  
5.  Kies de knop **Ok**. De batchverwerking wordt uitgevoerd en vervolgens wordt het planningsvoorstel ingevuld met de planningsregels.  

## Planningsboodschappen uitvoeren  
1.  Kies op de pagina **Planningsvoorstel** de actie **Planningsboodschap uitvoeren**.  
2.  Op het sneltabblad **Opties** moet u opgeven hoe de voorzieningen gemaakt moeten worden. Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Productieorder**|Geef op hoe u productieorders wilt maken. U kunt dit ook rechtstreeks doen vanaf de planningsregelvoorstellen. U kunt geplande of vast geplande productieorders opstellen.|  
    |**Assemblageorder**|Geef op hoe u assemblageorders wilt maken. U kunt dit ook rechtstreeks doen vanaf de planningsregelvoorstellen.|  
    |**Inkooporder**|Geef op hoe u inkoopeorders wilt maken. U kunt dit ook rechtstreeks doen vanaf de planningsregelvoorstellen.<br /><br /> Als u de planningsregelvoorstellen voor inkooporders naar het inkoopvoorstel kopieert, selecteert u de sjabloon en de naam van een werkblad.|  
    |**Transferorder**|Geef op hoe u transferorders wilt maken. U kunt dit ook rechtstreeks doen vanaf de planningsregelvoorstellen.<br /><br /> Als u de planningsregelvoorstellen voor transferorders naar het inkoopvoorstel kopieert, selecteert u de sjabloon en de naam van een werkblad.|  
    |**Transferorders combineren**|Selecteer als u transferorders wilt combineren.|  
    |**Stoppen en eerste fout tonen**|Selecteer als u de batchtaak **Planningsboodschap uitvoeren** wilt stoppen zodra er een fout wordt aangetroffen. Tegelijkertijd wordt een boodschap weergegeven met informatie over de eerste fout. Als er sprake is van een fout, leiden alleen de planningsregels die zijn verwerkt voordat de fout werd geconstateerd tot orders voor voorzieningen.|  

3.  Op het sneltabblad **Planningsregel** kunt u filters instellen om de planningsboodschappen te beperken.  
4.  Kies de knop **Ok**.  

Bij de batchverwerking worden de regels in het planningsvoorstel verwijderd nadat de planningsboodschap is uitgevoerd. De overige regels blijven in het planningsvoorstel staan totdat deze op een latere datum worden geaccepteerd of worden verwijderd. U kunt de regels ook handmatig verwijderen.  

## Planningsboodschappen  
Planningsboodschappen worden afgegeven door het ordertraceringssysteem wanneer geen balans te verkrijgen is binnen het bestaande ordernetwerk. Deze kunnen worden beschouwd als een suggestie aan u om wijzigingen te verwerken die zorgen voor een nieuwe balans tussen voorzieningen en vraag.  

Het genereren van planningsboodschappen gebeurt op één niveau tegelijk, voor de low-levelcode van elk artikel. Op die manier wordt ervoor gezorgd dat rekening wordt gehouden met alle artikelen die te maken hebben of krijgen met wijzigingen in de voorzieningen of vraag.  

Om kleine, overbodige of onbelangrijke planningsberichten te voorkomen, kan de gebruiker dempingen instellen, die ervoor moeten zorgen dat het genereren van planningsboodschappen beperkt blijft tot alleen die wijzigingen die een bepaald aantal of aantal dagen overschrijdt.  

Wanneer u de planningsboodschap hebt bekeken en u hebt bepaald of u enkele of alle van de voorgestelde wijzigingen wilt accepteren, selecteert u het veld **Planningsboodschap accepteren**. Daarna bent u klaar om de schema's overeenkomstig bij te werken.  

> [!NOTE]  
>  Een planningsboodschap is een suggestie om een nieuwe order te maken, een order te annuleren, of het aantal of de datum van een order te wijzigen. Een order is een inkooporder, transferorder of productieorder.  

Als reactie op een gebrek aan evenwichtigheid tussen voorzieningen en vraag worden de volgende planningsboodschappen gegenereerd.  

|Planningsboodschap|Omschrijving|  
|--------------------|---------------------------------------|  
|**Nieuw**|Als in een vraag niet kan worden voorzien door het voorstellen van de planningsboodschappen **Aantal wijzigen**, **Herplannen** of **Herplannen en aantal wijzigen** van bestaande orders, wordt de planningsboodschap **Nieuw** gegenereerd, hetgeen een nieuwe order suggereert. Daarnaast wordt de planningsboodschap **Nieuw** afgegeven als er geen bestaande orders voor voorzieningen zijn binnen de bestelfrequentie van het betreffende artikel. Deze parameter bepaalt het aantal perioden voorwaarts en achterwaarts in het beschikbaarheidsprofiel bij het zoeken naar een order om te herplannen.|  
|**Aantal wijzigen**|Wanneer een vraag die wordt getraceerd naar een of meer orders voor voorzieningen te maken krijgt met een wijziging van het aantal, wordt de planningsboodschap **Aantal wijzigen** afgegeven, waarmee wordt aangegeven dat de betreffende voorziening moet worden gewijzigd met betrekking tot de wijziging in de behoefte. Als zich een nieuwe vraag voordoet, zoekt [!INCLUDE[prod_short](includes/prod_short.md)] binnen de bestelfrequentie naar de dichtstbijzijnde order voor voorzieningen die nog niet gereserveerd is en geeft de planningsboodschap Wijzigen af voor die order.|  
|**Herplannen**|Wanneer een order voor voorzieningen of een vraag te maken krijgt met een datumwijziging waardoor de balans in het ordernetwerk wordt verstoord, wordt de planningsboodschap **Herplannen** gegenereerd. Als er geen een-op-een-relatie is tussen vraag en voorzieningen, wordt een planningsboodschap gegenereerd die voorstelt om de order voor voorzieningen overeenkomstig te verplaatsen. Als de order voor voorzieningen voorziet in de vraag van meer dan één verkooporder, wordt de order voor voorzieningen herplant overeenkomstig de datum van de eerste vraag.|  
|**Herplannen en aantal wijzigen**|Als zowel de datums als de aantallen van een order zijn gewijzigd, moet u plannen met betrekking tot beide omstandigheden te wijzigen. Bij het planningsboodschapproces worden beide acties - **Herplannen en Aantal wijzigen** - in één boodschap samengebracht, om ervoor te zorgen dat het evenwicht in het ordernetwerk wordt hersteld.|  
|**Annuleren**|Als een vraag die wordt gedekt op basis van order-op-order wordt verwijderd, wordt de planningsboodschap gegenereerd om de bijbehorende order(s) voor voorzieningen te annuleren. Als de relatie niet order-op-order is, wordt de planningsboodschap voor wijziging gegenereerd om de voorziening te verminderen. Als door andere factoren, zoals voorraadherwaarderingen, een order voor voorzieningen niet nodig is op het moment waarop de planningsboodschappen worden gegenereerd door de gebruiker, suggereert [!INCLUDE[prod_short](includes/prod_short.md)] de planningsboodschap **Annuleren** in het voorstel.|  

## Zie ook  
[Gepland](production-planning.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]