---
title: Ordertoezeggingsdatums berekenen
description: Met de functie Ordertoezegging wordt de vroegst mogelijke datum berekend waarop een artikel beschikbaar is voor verzending of levering.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/29/2021
ms.author: edupont
---
# Ordertoezeggingsdatums berekenen

Een bedrijf moet de klanten op de hoogte kunnen stellen van leverdatums van orders. Met de pagina **Ordertoezeggingsregels** kunt u dit doen vanuit een verkooporder.  

Op basis van de bekende en verwachte beschikbaarheidsdatums van een item berekent [!INCLUDE[prod_short](includes/prod_short.md)] verzend- en leverdatums die u aan klanten kunt toezeggen.  

Als u een aangevraagde leverdatum op een verkooporderregel plaatst, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen:  

- verzochte leverdatum - verzendtijd = geplande verzenddatum  
- geplande verzenddatum - verwerkingstijd uitgaand magazijn = verzenddatum  

Als de artikelen op de verzenddatum kunnen worden gepickt, kan het verkoopproces worden voortgezet. Als de artikelen niet op de verzenddatum kunnen worden gepickt, wordt een voorraadwaarschuwing gegeven.  

Als u geen aangevraagde leverdatum op een verkooporderregel hebt opgegeven of als u niet aan de aangevraagde leverdatum kunt voldoen, wordt gezocht naar de vroegste datum waarop de artikelen beschikbaar zijn. Vervolgens wordt deze datum ingevuld op de regel in het veld **Verzenddatum** waarna de volgende formules worden gebruikt om te bepalen op welke datum de artikelen volgens planning worden verzonden en geleverd aan de klant:  

- verzenddatum + verwerkingstijd uitgaand magazijn = geplande verzenddatum  
- Geplande verzenddatum + Verzendtijd = Geplande leverdatum  

## Informatie over ordertoezeggingen

Met de functionaliteit Ordertoezegging kunt u orders toezeggen, die op een bepaalde datum moeten worden verzonden of geleverd. De datum voor ATP (Available To Promise) of CTP (Capable To Promise) van een artikel wordt berekend en er worden orderregels gemaakt voor de datums die u accepteert. Met deze functionaliteit wordt de vroegst mogelijke datum berekend waarop een artikel beschikbaar is voor verzending of levering. De functie maakt ook aanvraagregels, voor het geval dat de artikelen eerst moeten worden ingekocht of geproduceerd, voor de datums die u accepteert.

[!INCLUDE[prod_short](includes/prod_short.md)] maakt gebruik van twee fundamentele begrippen:  

- Available to Promise (ATP)  
- Capable to promise (CTP)  

### Available to Promise

Available to promise (ATP, ook wel aangeduid als 'Beschikbare voorraad') berekent datums op basis van het reserveringssysteem. Het voert een beschikbaarheidscontrole uit van de niet-gereserveerde aantallen in voorraad met betrekking tot de geplande productie, inkoop, transfers en verkoopretouren. Op basis van deze informatie berekent [!INCLUDE[prod_short](includes/prod_short.md)] de leverdatum van de order van de klant, omdat de artikelen beschikbaar zijn in voorraad of na geplande ontvangsten.  

### Capable to Promise

Capable to promise (CTP) gaat uit van een 'wat als'-scenario, dat uitsluitend van toepassing is op artikelaantallen die niet in voorraad zijn of op geplande orders staan. Op basis van dit scenario berekent [!INCLUDE[prod_short](includes/prod_short.md)] de vroegste datum waarop het artikel beschikbaar wordt als het wordt geproduceerd, gekocht of overgebracht.

#### Opmerking

Als er een order voor 10 stuks is en 6 stuks in de voorraad of in geplande orders beschikbaar zijn, wordt de CTP-berekening gebaseerd op 4 stuks.

### Berekeningen

Wanneer [!INCLUDE[prod_short](includes/prod_short.md)] de leverdatum van de klant berekent, worden twee taken uitgevoerd:  

- Berekent de vroegste leverdatum wanneer de klant niet om een specifieke leverdatum heeft verzocht.  
- Controleert of de door de klant gevraagde of toegezegde leverdatum reaistisch is.  

Als de klant niet om een specifieke leverdatum vraagt, wordt de verzenddatum gelijk aan de werkdatum, en wordt de beschikbaarheid vervolgens gebaseerd op deze datum. Als het artikel in voorraad is, berekent [!INCLUDE[prod_short](includes/prod_short.md)] vooruit in tijd om te bepalen wanneer de order kan worden afgeleverd. Dit gebeurt aan de hand van de volgende formules:  

- Geplande verzenddatum + Uitgaande magazijnverwerkingstijd = Geplande verzenddatum  
- Geplande verzenddatum + Verzendtijd = Geplande leverdatum  

[!INCLUDE[prod_short](includes/prod_short.md)] controleert vervolgens of de berekende leverdatum realistisch is door terug in tijd te rekenen om te bepalen wanneer het item beschikbaar moet zijn om te voldoen aan de toegezegde datum. Dit gebeurt aan de hand van de volgende formules:  

- Geplande leverdatum - Verzendtijd = Geplande verzenddatum  
- Geplande verzenddatum - Uitgaande magazijnverwerking = Verzenddatum  

De verzenddatum wordt gebruikt om de beschikbaarheidscontrole uit te voeren. Als het item op deze datum beschikbaar is, bevestigt [!INCLUDE[prod_short](includes/prod_short.md)] dat aan de aangevraagde/toegezegde levering kan worden voldaan door de geplande leverdatum gelijk te stellen aan de aangevraagde/toegezegde leverdatum. Als het item niet beschikbaar is, verschijnt er een lege datum en kan de orderverwerker vervolgens de CTP-functionaliteit gebruiken.  

Op basis van de nieuwe datums en tijden, worden alle gerelateerde datums berekend volgens de formules die eerder in deze sectie zijn weergegeven. De CTP-berekening duurt langer, maar geeft een nauwkeurige datum voor wanneer de klant het artikel kan verwachten. De datums die worden berekend vanuit CTP, worden weergegeven in de velden **Geplande leverdatum** en **Eerste verzenddatum** op de pagina **Ordertoezeggingsregels**.  

De orderverwerker voltooit het CTP-proces door de datums te accepteren. Dit betekent dat een planningsregel en een reserveringspost voor het artikel worden gemaakt vóór de berekende datum om ervoor te zorgen dat aan de order kan worden voldaan.  

Naast de externe ordertoezegging die u kunt uitvoeren op de pagina **Ordertoezeggingsregels**, kunt u ook interne of externe leverdatums voor stuklijstartikelen beloven. Zie voor meer informatie [Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md).

## Ordertoezegging instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Ordertoezeggingsinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Voer in het veld **Uitsteltijd** een nummer en tijdseenheidscode in. Selecteer een van de volgende codes.  

    |Code|Omschrijving|  
    |----------|-----------------|  
    |**d**|Agendadag|  
    |**w**|Week|  
    |**m**|Maand|  
    |**k**|Kwartaal|  
    |**j**|jaar|  

    "3w" geeft bijvoorbeeld aan dat de uitsteltijd drie weken is. Gebruik voor alle codes "h" als voorvoegsel om de huidige tijdseenheid aan te geven. Voer bijvoorbeeld **hm** in als de uitsteltijd de huidige maand moet zijn.  
3. Voer in het veld **Ordertoezeggingsnrs.** een nummerreeks in door een regel te selecteren in het overzicht op de pagina **Nr.-reeks**.  
4. Voer in het veld **Ordertoezeggingssjabloon** een ordertoezeggingsjabloon in door een regel te selecteren in het overzicht op de pagina **Overzicht ink.-voorstelsjabl.**  
5. Voer in het veld **Ordertoezeggingsvoorstel** een inkoopvoorstel in door een regel te selecteren in het overzicht op de pagina **Inkoopvoorstelbatches**.

### In- en uitslagtijden in ordertoezeggingen

Als u een inslagtijd wilt instellen voor de berekening van de ordertoezegging op de inkoopregel, kunt u op de pagina **Voorraadinstellingen** een standaardverwerkingstijd voor gebruik in verkoop- en inkoopdocumenten opgeven. Op de pagina **Locatiekaart** kunt u ook specifieke tijden invoeren voor elk van uw locaties. 

#### Standaardinslagtijd en -uitslagtijd invoeren voor verkoop- en inkoopdocumenten

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Voer in de velden **Inslagtijd** en **Uitslagtijd** op het sneltabblad **Algemeen** het aantal dagen in dat u wilt opnemen in de berekening van de ordertoezeggingsberekeningen.  

#### In- en uitslagtijden invoeren voor locaties

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locatie** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de relevante vestigingskaart.  
3.  Voer in de velden **Inslagtijd** en **Uitslagtijd** op het sneltabblad **Magazijn** het aantal dagen in dat u wilt opnemen in de berekening van de ordertoezeggingsberekeningen.  

> [!NOTE]  
>  Wanneer u een inkooporder maakt en **Locatie** in het veld **Verzenden naar** op het sneltabblad **Verzending en betaling** kiest en vervolgens een locatie in het veld **Locatiecode** kiest, gebruiken de velden **Uitslagtijd** en **Inslagtijd** de verwerkingstijd die is opgegeven voor de locatie. Voor verkooporders geldt hetzelfde als u een locatie kiest in het veld **Locatiecode**. Als er voor de locatie geen verwerkingstijd is opgegeven, zijn de velden **Uitslagtijd** en **Inslagtijd** leeg. Als u het veld **Locatiecode** leeg laat in verkoop- en inkoopdocumenten, wordt voor de berekening de verwerkingstijd op de pagina **Voorraadinstellingen** gebruikt.

## Artikelen als kritiek aanmerken

Voordat u een artikel in de ordertoezeggingsberekening kunt opnemen, moet het zijn gemarkeerd als kritiek. Deze instellingen zorgen dat de niet-kritieke artikelen niet leiden tot irrelevante ordertoezeggingsberekeningen   
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de relevante artikelkaart.  
3.  Selecteer op het sneltabblad **Planning** het veld **Kritisch**.  

## Een ordertoezeggingsdatum berekenen

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporder** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de betreffende verkooporder en selecteer de verkooporderregels die moeten worden berekend.  
3.  Kies de actie **Ordertoezegging** en kies daarna de actie **Ordertoezeggingsregels**.  
4.  Selecteer een regel en selecteer vervolgens een van de volgende opties:  

    - Selecteer **ATP** als de vroegste datum moet worden berekend waarop het artikel beschikbaar is met betrekking tot de voorraad, de geplande ontvangsten en de brutobehoeften.  
    - Selecteer **CTP** als u weet dat het artikel momenteel niet in voorraad is en de vroegste datum moet worden berekend waarop het artikel beschikbaar wordt door nieuwe aanvullende behoefteregels te maken.  
5.  Kies de knop **Accepteren** om de vroegst beschikbare verzenddatum te accepteren.  

## Zie gerelateerde [Microsoft-training](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/)

## Zie ook

[Verkoop](sales-manage-sales.md)  
[Datumberekening voor inkoop](purchasing-date-calculation-for-purchases.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
