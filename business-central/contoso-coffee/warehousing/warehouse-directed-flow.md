---
title: 'Ontvangst, opslag, verplaatsing, picken en verzending in geavanceerde magazijnconfiguratie met gerichte pick en opslag'
description: 'Inkomende en uitgaande processen kunnen op verschillende manieren worden uitgevoerd, afhankelijk van het complexiteitsniveau van het magazijn.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# Procedure van inkomende en uitgaande stroom in geavanceerde magazijnconfiguratie met gestuurde opslag en pick

Deze procedure laat zien hoe inkomende en uitgaande stromen worden voltooid in de geavanceerde configuratie van opslag en picken. Zie voor meer informatie [Overzicht van verschillende configuratieopties](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Vereisten  
Om deze procedure te voltooien moet u een magazijnmedewerker maken op de vestiging *WIT* door deze stappen te volgen:  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies vervolgens de gerelateerde koppeling.  
2. Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Gebruikers**.  
3. Voer WIT in het veld **Vestiging** in.  
4. Schakel de schakelaar **Standaard** in.


## Scenario  
Ellen, de magazijnmanager, maakt gebruik van crossdocking en aanvulling van opslaglocaties om de ontvangst- en verzendtijd te verkorten.  

## Stappen

1. Magazijnverzending maken.  

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 2.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer order voor klant 10000 voor de WITTE locatie. Extern ordernummer is *W-1*.
    3. Kies de actie **Magazijnverzending maken** om een magazijnverzending te maken voor de geselecteerde verkooporder.
    4. Kies de actie **Vrijgeven** om het magazijn te informeren dat de verzending klaar is voor magazijnverwerking.  

2. Definieer opslaglocaties voor het artikel om te bepalen waar het wordt opgeslagen 

    1.  Kies het pictogram ![Lampje dat de functie Vertel me opent 3.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
    2.  Selecteer *WRB-1000* en kies vervolgens de actie **Opslaglocatie-inhoud**.  
    3.  Kies de actie **Nieuw**. Voeg twee regels toe.
    
    |Artikel|Vestiging|Code van opslaglocatie|Vast|Maateenheid|
    |----------|----------|---------|---|------|  
    |MAGART-1000|WIT|W-05-0001|Ja|TAS|  
    |WRB-1000|WIT|W-05-0002|Ja|TAS|

3. Maak een magazijnontvangst.  

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 4.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
    2. Selecteer order van leverancier 10000 voor de WITTE locatie. Leveranciersordernummer is *W-2*. Gebruik de personalisatietools als het veld **Ordernr. leverancier** niet zichtbaar is. Zie [Uw werkruimte personaliseren](../../ui-personalization-user.md) voor meer informatie.
    3. Kies de actie **Magazijnontvangst maken** om een magazijnontvangst te maken voor de geselecteerde inkooporder.


4. Controleren of er uitgaande orders zijn die ontvangen artikelen nodig hebben en postontvangst
    1. Kies de actie **Cross-dock berekenen**. Dit vult een kolom genaamd **Te cross-docken aantal**.
    2. Voer 0 in het veld **Te cross-docken aantal** in op de regel met artikel *WRB-1000* omdat u niet van plan bent om opnieuw in te pakken in het ontvangstgebied.
    3. Kies de actie **Ontvangst boeken**.

5. De magazijnopslag registreren
    1. Voer met het pictogram ![Lampje dat de functie Vertel me opent 5.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), **Magazijnopslag** in en kies de gerelateerde koppeling.
    2. Zoek het magazijnopslagdocument dat is gemaakt op basis van uw magazijnontvangst en open het
    3. Bekijk op de pagina **Magazijnopslag** het gedeelte **Regels**

    In dit stadium wordt de logica van de opslagcapaciteit onthuld. De magazijnopslagregels hebben drie regels voor artikel *WRB-1000*:
    - Een Nemen-regel om de ontvangen hoeveelheden uit de ontvangstbak te verplaatsen (W-08-0001)
    - Een Plaatsen-regel die één TAS verplaatst naar een van de geconfigureerde vaste opslaglocaties (W-05-0001)
    - Een Plaatsen-regel die een andere TAS naar een andere vaste opslaglocatie verplaatst (W-05-0002). Dit komt doordat een enkele vaste opslaglocatie niet de volledige ontvangsthoeveelheid kan bevatten.

    Omdat deze opslag crossdock-regels bevat, ziet u drie regels voor artikel *WRB-1001*:
    -  Een Nemen-regel om de ontvangen hoeveelheden uit de ontvangstbak te verplaatsen (W-08-0001)
    -  Een Plaats-regel voor de 2 in de cross-dock opslaglocatie
    -  Een Plaatsen-regel voor de resterende hoeveelheid in de opslaglocatie

    4. Kies de actie **Opslag registreren**.


6. Definieer opslaglocaties voor het artikel om te bepalen waar het wordt gepickt 

    1.  Kies het pictogram ![Lampje dat de functie Vertel me opent 6.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
    2.  Open de *WITTE* vestigingskaart.  
    3.  Kies de actie **Opslaglocaties** op de **Locatiekaart**
    4.  Selecteer opslaglocatie *W-02-0001* en kies vervolgens de actie **Inhoud**.  
    5.  Kies de actie **Nieuw**.  
    6.  Zet de schakelaar **Vast** aan.  
    7.  Voer in het veld **Artikelnummer** de waarde *WRB-1000* in. 
    8.  Voer in het veld **Min. aantal** *2* in. 
    9.  Voer in het veld **Max. aantal** *10* in. 

    Gebruik de personalisatietools als de velden **Min. aantal** en **Max. aantal** niet zichtbaar zijn. Zie [Uw werkruimte personaliseren](../../ui-personalization-user.md) voor meer informatie. 

7. Reorganiseer het magazijn door artikelen van het bulkopslaggebied naar het pickgebied te verplaatsen om de picktijd te optimaliseren.

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 7.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verplaatsingsvoorstellen** in en kies de gerelateerde koppeling
    2. Kies de actie **Opslaglocatieaanvulling berekenen**. 

    Het magazijnvoorstel met het voorstel om artikel *WRB-1000* te verplaatsen van bulkopslag naar pickgebied is gemaakt.

    3. Kies de actie **Verplaatsing maken** en bevestig het maken van het document.
    4.  Kies het pictogram ![Lampje dat de functie Vertel me opent 8.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnverplaatsingen** in en kies de gerelateerde koppeling
    5.  Open de magazijnverplaatsing die u hebt gemaakt en controleer het gedeelte **Regels**

     In dit stadium wordt de breakbulk-functionaliteit onthuld. Er zullen vier regels zijn:
    - Een regel om de ene TAS uit de bulkopslaglocatie te nemen
    - Een regel om de 48 stuks terug in voorraad te plaatsen in dezelfde opslaglocatie. 
    - Een regel om de 10 stuks uit de bulkopslaglocatie te nemen
    - Een regel om de 10 stuks in de opslaglocatie te plaatsen

    6.  Kies de actie **Verplaatsing registreren**.

8. Magazijnpicks maken

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 9.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pickvoorstellen** in en kies vervolgens de gerelateerde koppeling
    2. Kies de actie **Magazijndocumenten ophalen**, selecteer de regel voor de verkooporder voor klant 10000 en kies vervolgens de knop **OK** om de werkbladregels te vullen volgens het geselecteerde document.

    3. Inspecteer het veld **Aantal in cross-dockopslagloc.**. 

    4. Kies de actie **Pick maken**.
    5. Bevestig van de benodigde pick-instellingen, schakel bijvoorbeeld **Per Van zone** in. Kies de knop **Ok**.
    
    U ontvangt een bevestigingsbericht met de picknummers. Er zijn twee picks omdat sommige items zich in de cross-dockzone bevinden, dicht bij het verzendgebied, en het zou logisch zijn om ze afzonderlijk te verwerken.

9.  De magazijnpicks registreren
    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 10.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnpicks** in en kies de gerelateerde koppeling.
    2. Zoek de picks die u hebt gemaakt en open deze.
    3. Kies de actie **Pick registreren**.
    4. Herhaal dit voor de tweede pick

10. De magazijnverzending boeken
    
    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 11.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnverzending** in en kies de gerelateerde koppeling.
    2. Bekijk op de magazijnopslagpagina het gedeelte **Regels**. Nadat de magazijnpick is geregistreerd, wordt de magazijnverzending bijgewerkt met **Te verzenden aantal** ingevuld.
    3. Kies de actie **Verzending boeken**.
    4. Bevestig de **Verzending**-optie.


## Resultaten
- de **geboekte magazijnontvangst** wordt gemaakt
- de **geregistreerde magazijnopslag** wordt gemaakt    
- de **geboekte inkoopontvangst** wordt gemaakt    
- de **Inkooporder** heeft het **Ontvangen aantal** bijgewerkt voor de ontvangen regels
- de **geregistreerde magazijnverplaatsing** wordt gemaakt
- de **geregistreerde magazijnpick** wordt gemaakt
- de **geboekte magazijnverzending** wordt gemaakt
- de **geboekte verkoopverzending** wordt gemaakt
- de **verkooporder** heeft het **verzonden aantal** bijgewerkt voor de verzonden regels
- De artikel**voorraad** wordt verhoogd met de rest die niet is verzonden



## Zie ook
[Artikelen ontvangen](../../warehouse-how-receive-items.md) 
[Ontwerpdetails: Inkomende magazijnstroom](../../design-details-inbound-warehouse-flow.md) 
[Artikelen verzenden](../../warehouse-how-ship-items.md) 
[Artikelen picken voor magazijnverzending](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Ontwerpdetails: Uitgaande magazijnstroom](../../design-details-outbound-warehouse-flow.md) 
[Beschikbaarheid van artikelen weergeven](../../inventory-how-availability-overview.md) 
