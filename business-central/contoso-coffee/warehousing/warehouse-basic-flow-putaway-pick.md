---
title: 'Ontvangen, opslaan, picken en verzenden in standaardmagazijnconfiguratie'
description: 'In Business Central kunnen de inkomende en uitgaande processen op verschillende manieren worden uitgevoerd, afhankelijk van het complexiteitsniveau van het magazijn.'
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

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a>Procedure van de inkomende en uitgaande stroom in standaardmagazijnconfiguraties

Deze procedure laat zien hoe inkomende en uitgaande stromen worden voltooid in de configuratie Basis: order voor order. Zie voor meer informatie [Overzicht van verschillende configuratieopties](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Vereisten
Om deze procedure te voltooien moet u een magazijnmedewerker maken op de vestiging *ZILVER* door deze stappen te volgen:  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies vervolgens de gerelateerde koppeling.  
2. Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Gebruikers**.  
3. Voer in het veld **Vestiging** *ZILVER* in.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Inkomende stroom: ontvangen en opslaan in standaardmagazijnconfiguraties

In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunnen de inkomende processen voor ontvangst en opslag op vier manieren worden uitgevoerd met verschillende functionaliteiten, afhankelijk van het complexiteitsniveau van het magazijn.  

|Methode|Inkomend proces|Opslaglocaties|Ontvangsten|Magazijnopslag|Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Ontvangst en opslag van de orderregel boeken|X|||2|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken|||X|3|  
|L|Ontvangst en opslag van een magazijnontvangstdocument boeken||X||5-4-6|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken||X|X|5-4-6|  

Zie voor meer informatie [Ontwerpdetails: Inkomende magazijnstroom](../../design-details-inbound-warehouse-flow.md).  

De volgende procedure geeft methode B in de vorige tabel weer.  

### <a name="scenario"></a>Scenario
Alicia, de inkoopagent, maakt een inkooporder voor verschillende geroosterde bonen. Wanneer de levering in het magazijn aankomt, zet John, de magazijnmedewerker, de artikelen in geschikte opslaglocaties. Wanneer John de opslag boekt, worden de artikelen als ontvangen in de voorraad geboekt en beschikbaar voor verkoop of andere vraag.  

### <a name="steps"></a>Stappen
1. Stel de pagina **Vestiging** in om de inkomende magazijnstromen van het bedrijf te definiëren.  

    1.  Kies het pictogram ![Lampje dat de functie Vertel me opent 2.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
    2.  Open de vestigingskaart *ZILVER*.  
    3.  Selecteer het selectievakje **Opslag vereist**.  

2. Definieer een standaardopslaglocatie voor het artikel om te bepalen waar het wordt opgeslagen

    1.  Kies de actie **Opslaglocaties** op de **Locatiekaart**
    2.  Selecteer de eerste rij voor opslaglocatie *S-1-01* en kies vervolgens de actie **Inhoud**.  
    3.  Kies de actie **Nieuw**.  
    4.  Selecteer de velden **Vast** en **Standaard**.  
    5.  Voer in het veld **Artikelnummer** de waarde *WRB-1000* in.  

3. Maak de inkooporder, wat de meest gebruikte soort inkomend brondocument is.  

    1.  Kies het pictogram ![Lampje dat de functie Vertel me opent 3.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
    2.  Kies de actie **Nieuw**.  
    3.  Maak een inkooporder voor leverancier 10000 met de volgende inkooporderregels. Gebruik de personalisatietools als het veld **Opslaglocatie** niet zichtbaar is. Zie [Uw werkruimte personaliseren](../../ui-personalization-user.md) voor meer informatie. 

    |Artikel|Vestiging|Opslaglocatie|Aantal|  
    |----------|----------|---------|--------------|  
    |WRB-1000|ZILVER|S-1-01|20|  
    |WRB-1001|ZILVER||30|

    De opslaglocatiecode in de eerste is ingevuld volgens de instelling. De opslaglocatiecode voor het tweede artikel is leeg omdat het geen standaardwaarden heeft. Houd het zo.  

    4.  Kies de actie **Vrijgeven** om het magazijn te informeren dat de inkooporder klaar is voor magazijnverwerking wanneer de levering aankomt.  

4. Maak **voorraadopslag** om de geleverde artikelen te ontvangen en op te slaan  

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 4.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadopslag** in en kies vervolgens de gerelateerde koppeling.  
    2. Kies de actie **Nieuw**. 
    3. Selecteer *ZILVER* in het veld **Vestiging**.
    4. Selecteer het veld **Brondocument** en selecteer vervolgens **Inkooporder**.  
    5. Selecteer het veld **Bronnr.**, selecteer de regel voor de inkoop bij leverancier 10000 en kies vervolgens de knop **OK** om de opslagregels te vullen volgens het geselecteerde brondocument.

        U kunt ook de actie **Brondocument ophalen** kiezen en de inkooporder kiezen.  

5. Wijzig de voorraadopslag op basis van daadwerkelijke plaatsing van artikelen en boek het document

    Bij het plaatsen van artikelen in opslaglocaties, merkte John dat de standaardopslaglocatie al enkele artikelen bevat, dus besloot hij een andere opslaglocatie te gebruiken. John plaatst ook andere artikelen in de volgende opslaglocaties, omdat de ontvangen hoeveelheid niet binnen de capaciteit past.

    1. Wijzig op de eerste regel **Opslaglocatie** van *S-1-01*, wat uit de inkooporder is gekopieerd, in *S-1-02*. 
    2.  Voer 20 in het veld **Te verwerken aantal** in op de voorraadopslagregel met artikel WBR-1000.  
    3. Voer op de tweede regel 20 in het veld **Te verwerken aantal** in en kies de actie **Regel splitsen** . Er verschijnt een nieuwe regel. Dit is een kopie van de oorspronkelijke regel, met uitzondering van het veld **Te verwerken aantal**, dat het aantal bevat dat u uit de oorspronkelijke regel hebt verwijderd. 
    4. Vul opslaglocatiecodes in voor artikel WBR-1001:

    |Artikel|Opslaglocatie|Aantal|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Kies de actie **Boeken**, selecteer de actie **Ontvangen** en kies vervolgens de knop **OK**.  

### <a name="results"></a>Resultaten
 - De geroosterde bonen staan nu geregistreerd als opgeslagen in gespecificeerde opslaglocaties
 - de **Geboekte voorraadopslag** wordt gemaakt
 - de **geboekte inkoopontvangst** wordt gemaakt
 - de inkooporder heeft het **Ontvangen aantal** bijgewerkt voor de ontvangen regels
 - de artikel**voorraad** wordt verhoogd met de gekozen hoeveelheid
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a>Uitgaande stroom: picken en verzenden in standaardmagazijnconfiguraties

In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunnen uitgaande processen voor picken en verzending op vier manieren worden uitgevoerd met verschillende functionaliteiten afhankelijk van het complexiteitsniveau van het magazijn.  

|Methode|Inkomend proces|Opslaglocaties|Magazijnpicks|Verzendingen|Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Picken en verzending van de orderregel boeken|X|||2|  
|B|Picken en verzending van een voorraadpickdocument boeken||X||3|  
|L|Picken en verzending van een magazijnverzendingdocument boeken|||X|5-4-6|  
|D|Picken van een magazijnpickdocument en verzending van een magazijnverzendingdocument boeken||X|X|5-4-6|  

Zie voor meer informatie [Ontwerpdetails: Uitgaande magazijnstroom](../../design-details-outbound-warehouse-flow.md).  

De volgende procedure geeft methode B in de vorige tabel weer.

### <a name="scenario-1"></a>Scenario
Susan, de orderverwerker, maakt een verkooporder voor verschillende geroosterde bonen en geeft deze door aan het magazijn. De magazijnmedewerker John zorgt ervoor dat de verzending wordt voorbereid en aan de klant geleverd. John beheert alle betrokken taken op de pagina **Voorraadpick**, die automatisch verwijst naar de opslaglocaties waar geroosterde bonen zijn opgeslagen.

### <a name="steps-1"></a>Stappen
Dit is een voortzetting van [Inkomende stroom: ontvangen en opslaan in standaardmagazijnconfiguraties](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Stel de pagina **Vestiging** in om de inkomende magazijnstromen van het bedrijf te definiëren.  

    1.  Kies het pictogram ![Lampje dat de functie Vertel me opent 5.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
    2.  Open de vestigingskaart *ZILVER*.  
    3.  Selecteer het selectievakje **Pick vereist**.  

2. Maak de verkooporder, wat de meest gebruikte soort uitgaand brondocument is.  

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 6.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
    2. Kies de actie **Nieuw**.  
    3. Maak een verkooporder voor klant 10000 met de volgende verkooporderregel.  

    |Artikel|Vestiging|Aantal|  
    |----|-------------|--------|  
    |WRB-1000|ZILVER|20|  
    |WRB-1001|ZILVER|30|  

    De opslaglocatiecodes worden automatisch ingevuld met standaardopslaglocaties.

    4. Kies de actie **Voorraadopslag/-pick-verplaatsing maken**.
    5. Schakel het selectievakje **Voorraadpick maken** in.  
    6. Kies de knop **Ok**. Er wordt een nieuwe voorraadpick gemaakt.

3. Artikelen picken en verzenden

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 7.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadpicks** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer de voorraadpick voor de verkoop aan klant 10000
    
    De gemaakte voorraadpick negeerde de opslaglocatie die is gedefinieerd voor het artikel *WRB-1000*, omdat deze geen voorraad bevat en gebruikte een andere opslaglocatie. De tweede regels, met artikel *WRB-1001* zijn automatisch gesplitst om uit meerdere opslaglocaties te picken.
    
4. Kies de actie **Te verwerken aantal autom. invullen**.  

5. Kies de actie **Boeken**, selecteer **Verzenden** en kies de knop **OK**.  

### <a name="results-1"></a>Resultaten
 - de geroosterde bonen staan nu geregistreerd als gepickt uit gespecificeerde opslaglocaties
 - de **Geboekte voorraadpick** wordt gemaakt
 - de **geboekte verkoopverzending** wordt gemaakt
 - de verkooporder heeft het **verzonden aantal** bijgewerkt voor de verzonden regels
 - de artikel**voorraad** wordt verlaagd met de gekozen hoeveelheid


## <a name="see-also"></a>Zie ook
[Artikelen opslaan met voorraadopslag](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Standaardmagazijnen met bewerkingsgebieden instellen](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Ontwerpdetails: Inkomende magazijnstroom](../../design-details-inbound-warehouse-flow.md) 
[Artikelen picken met een voorraadpick](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Ontwerpdetails: Uitgaande magazijnstroom](../../design-details-outbound-warehouse-flow.md) 
[Beschikbaarheid van artikelen weergeven](../../inventory-how-availability-overview.md) 
