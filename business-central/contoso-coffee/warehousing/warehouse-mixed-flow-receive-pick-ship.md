---
title: 'Ontvangen, opslaan, picken en verzenden in gemengde magazijnconfiguratie'
description: 'In Business Central kunnen de inkomende en uitgaande processen op verschillende manieren worden uitgevoerd, afhankelijk van het complexiteitsniveau van het magazijn.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Procedure van inkomende en uitgaande stroom in gemengde magazijnconfiguraties

Deze procedure laat zien hoe inkomende en uitgaande stromen in een gemengde configuratie kunnen worden voltooid, waarbij voor de inkomende stroom het magazijn is geconfigureerd als Basis: Order voor order en voor de uitgaande stroom de geavanceerde configuratie wordt gebruikt. Zie voor meer informatie [Overzicht van verschillende configuratieopties](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Vereisten  
Om deze procedure te voltooien moet u een magazijnmedewerker maken op de vestiging *GEEL* door deze stappen te volgen:  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies vervolgens de gerelateerde koppeling.  
2. Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Gebruikers**.  
3. Voer in het veld **Vestiging** *GEEL* in.  

## Inkomende stroom: ontvangen en opslaan in standaardmagazijnconfiguraties

In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunnen de inkomende processen voor ontvangst en opslag op vier manieren worden uitgevoerd met verschillende functionaliteiten, afhankelijk van het complexiteitsniveau van het magazijn.  

|Methode|Inkomend proces|Opslaglocaties|Ontvangsten|Magazijnopslag|Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Ontvangst en opslag van de orderregel boeken|X|||2|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken|||X|3|  
|L|Ontvangst en opslag van een magazijnontvangstdocument boeken||X||5-4-6|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken||X|X|5-4-6|  

Zie voor meer informatie [Ontwerpdetails: Inkomende magazijnstroom](../../design-details-inbound-warehouse-flow.md).  

De volgende procedure geeft methode C in de vorige tabel weer.  

### Scenario  
Alicia, de inkoopagent, maakt inkooporders voor verschillende geroosterde bonen zodra er vraag naar is. Wanneer een gecombineerde levering in het magazijn aankomt, ontvangt John, de magazijnmedewerker, deze en slaat deze op. Wanneer John de ontvangst boekt, worden de artikelen geboekt als ontvangen in voorraad en beschikbaar voor verkoop of andere vraag.  

### Stappen
1. Stel de pagina **Vestiging** in om de inkomende magazijnstromen van het bedrijf te definiëren.  

    1.  Kies het pictogram ![Lampje dat de functie Vertel me opent 2.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
    2.  Open de vestigingskaart *GEEL*.  
    3.  Zet de schakelaar **Opslag vereist** uit.  

2. Inkooporders vrijgeven naar magazijn.  

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 3.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
    2. Selecteer orders van leverancier 10000 voor de GELE locatie. Leveranciersordernummers zijn *Y-1* en *Y-2*. Gebruik de personalisatietools als het veld **Ordernr. leverancier** niet zichtbaar is. Zie [Uw werkruimte personaliseren](../../ui-personalization-user.md) voor meer informatie.
    3. Kies de actie **Vrijgeven** om het magazijn te informeren dat de geselecteerde inkooporders klaar zijn voor magazijnverwerking wanneer de levering aankomt.  

3. Maak de magazijnontvangst om de geleverde artikelen te ontvangen en op te slaan
    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 4.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnontvangsten** in en kies de gerelateerde koppeling.
    2. Kies de actie **Nieuw**
    3. Druk op de magazijnontvangstpagina op Enter om automatisch een magazijnontvangstnummer te selecteren
    4. Voer in het veld **Vestiging** *GEEL* in.
    5. Kies de actie **Brondocumenten ophalen...**
    6. Selecteer eerder vrijgegeven inkooporders van leverancier 10000 en klik op de knop **OK**.
        De regels bevatten een nieuwe post voor elke inkooporderregel.

4. Hoeveelheid aan ontvangst aanpassen op basis van ontvangen hoeveelheid en document boeken
    1. Selecteer de regel met artikel *WRB-1000*.
    2. Selecteer *MEERONTV10* in het veld **Meerontvangstcode** en wijzig de waarde in het veld **Te ontvangen aantal** van *100* in *110*.
    3. Selecteer de regel met artikel *WRB-1001* en 
    4. Wijzig op de tweede regel de waarde in het veld **Te ontvangen aantal** van *200* in *190*.
    5. Kies de actie **Ontvangst boeken**.

### Resultaten 
 - de geroosterde bonen staan nu geregistreerd als opgeslagen
 - de **geboekte magazijnontvangst** wordt gemaakt
 - de **geboekte inkoopontvangst** wordt gemaakt
 - de inkooporder heeft het **Ontvangen aantal** bijgewerkt voor de ontvangen regels
 - de artikel**voorraad** wordt verhoogd met de gekozen hoeveelheid
    

## Uitgaande stroom: picken en verzenden in geavanceerde magazijnconfiguraties

In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunnen uitgaande processen voor picken en verzending op vier manieren worden uitgevoerd met verschillende functionaliteiten afhankelijk van het complexiteitsniveau van het magazijn.  

|Methode|Inkomend proces|Opslaglocaties|Magazijnpicks|Verzendingen|Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Picken en verzending van de orderregel boeken|X|||2|  
|B|Picken en verzending van een voorraadpickdocument boeken||X||3|  
|L|Picken en verzending van een magazijnverzendingdocument boeken|||X|5-4-6|  
|D|Picken van een magazijnpickdocument en verzending van een magazijnverzendingdocument boeken||X|X|5-4-6|  

Zie voor meer informatie [Ontwerpdetails: Uitgaande magazijnstroom](../../design-details-outbound-warehouse-flow.md).  

De volgende procedure geeft methode D in de vorige tabel weer.

### Scenario  
Susan, de orderverwerker, maakt verkooporders voor verschillende geroosterde bonen en geeft deze door aan het magazijn. Omdat alle orders van dezelfde klant komen, besluit Ellen, de magazijnbeheerder, ze samen te verzenden. De magazijnmedewerker John zorgt ervoor dat de verzending wordt voorbereid en aan de klant geleverd.

### Stappen
Dit is een voortzetting van [Inkomende stroom: ontvangen en opslaan in standaardmagazijnconfiguraties](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Verkooporders vrijgeven naar magazijn.  

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 5.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer orders voor klant 10000 voor de GELE locatie. Externe ordernummers zijn *Y-3*, *Y-4* en *Y-5*.
    3. Kies de actie **Vrijgeven** om het magazijn te informeren dat de geselecteerde verkooporders klaar zijn voor magazijnverwerking.  

2. Artikelen verzenden  
    1. Kies het pictogram ![Lampje dat de functie Vertel me opent 6.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnverzendingen** in en kies vervolgens de gerelateerde koppeling.  
    2. Kies de actie **Nieuw**.  
    3. Voer in het veld **Vestiging** *GEEL* in.  
    4. Kies de actie **Filters om brondoc. op te halen gebruiken**.  
    5. Voer in het veld **Code** **KLANT10000** in.  
    6. Voer in het veld **Beschrijving** **Klant 10000** in.  
    7. Kies de actie **Wijzigen**.  
    8. Voer op het sneltabblad **Verkoop** in het veld **Orderklantnr.-filter** *10000* in.  
    9. Kies de actie **Uitvoeren**. 
    
    De magazijnverzending wordt gevuld met vier regels die verkooporderregels voor de opgegeven klant vertegenwoordigen. Het veld **Te verzenden aantal** is leeg, omdat artikelen eerst moeten worden gepickt.

3. Maak de magazijnpick vanuit de magazijnverzending
    1. Kies op de magazijnverzendingspagina de actie **Pick maken**.
    2. Bevestig de benodigde pickinstellingen. Selecteer bijvoorbeeld *Artikel* in het veld **Sorteringsmethode voor activiteitsregels** om dezelfde artikelen te groeperen. Kies de knop **Ok**.
    3. U ontvangt een bevestigingsbericht met het picknummer. 

4. De magazijnpick openen
    1. Voer met het pictogram ![Lampje dat de functie Vertel me opent 7.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnpicks** in en kies de gerelateerde koppeling.
    2. Zoek de pick die u hebt gemaakt en open deze.
    3. Werk het **Te verwerken aantal** indien nodig bij.
    4. Kies de actie **Pick registreren**.
    5. De magazijnpick wordt gesloten en verwijderd als alle hoeveelheden zijn afgehandeld.

5. De magazijnverzending boeken
   1. Kies het pictogram ![Lampje dat de functie Vertel me opent 8.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnverzendingen** in en kies vervolgens de gerelateerde koppeling.  
   2. Zoek de verzending die u eerder hebt gemaakt en open deze.
    Merk op dat **Te verzenden aantal** is gevuld.
    3. U kunt **Boekingsdatum**, **Extern documentnr.**, **Expediteur**, **Verzendmethode** indien nodig bijwerken. Niet-lege waarden worden doorgegeven aan brondocumenten.
    4. Kies de actie **Verzending boeken**.
    5. Bevestig de **Verzending**-optie.

### Resultaten
 - de geroosterde bonen staan nu geregistreerd als gepickt 
 - de **geregistreerde magazijnpick** wordt gemaakt
 - de **geboekte magazijnverzending** wordt gemaakt
 - de drie **Geboekte verkoopzendingen** worden gemaakt
 - de verkooporder heeft het **verzonden aantal** bijgewerkt voor de verzonden regels
 - de artikel**voorraad** wordt verlaagd met de gekozen hoeveelheid


## Zie ook
[Artikelen ontvangen](../../warehouse-how-receive-items.md)
[Standaardmagazijnen met bewerkingsgebieden instellen](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Ontwerpdetails: Inkomende magazijnstroom](../../design-details-inbound-warehouse-flow.md)
[Artikelen verzenden](../../warehouse-how-ship-items.md)
[Picken van artikelen voor magazijnverzending](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Ontwerpdetails: Uitgaande magazijnstroom](../../design-details-outbound-warehouse-flow.md)
[Beschikbaarheid van artikelen weergeven](../../inventory-how-availability-overview.md)
