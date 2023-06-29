---
title: Artikelen verplaatsen in magazijnen die gebruikmaken van gestuurde opslag en pick
description: In dit artikel wordt uitgelegd hoe u artikelen verplaatst naar locaties die gebruikmaken van gestuurde opslag en pick.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
---

# <a name="move-items-in-advanced-warehouse-configurations-that-use-directed-put-away-and-pick"></a><a name="move-items-in-advanced-warehouse-configurations-that-use-directed-put-away-and-pick"></a>Artikelen verplaatsen in geavanceerde magazijnconfiguraties die gebruikmaken van gestuurde opslag en pick

U kunt artikelen tussen opslaglocaties verplaatsen zonder een vraag van een brondocument. U wilt dat bijvoorbeeld doen als onderdeel van de volgende activiteiten:

* Uw magazijn reorganiseren.
* Artikelen naar een inspectiegebied brengen.
* Artikelen tijdelijk uit de magazijn-opslaglocaties halen om bijvoorbeeld als demonstratiemodel te dienen tijdens een verkooppresentatie.
* Extra artikelen verplaatsen naar het productiegebied voor materialen die zijn geconfigureerd met bepaalde afboekingsmethoden.
* Geproduceerde of geassembleerde artikelen van het productie- of assemblagegebied naar het magazijn verplaatsen.
* Artikelen uit het bulkopslaggebied verplaatsen naar opslaglocaties die u gebruikt voor picken.

Hoe u artikelen verplaatst, is afhankelijk van de vestigingsinstellingen van het magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

In magazijnconfiguraties waar de schakelaar **Gestuurde opslag en pick** is ingeschakeld voor locaties, kunt u ongeplande verplaatsingen registreren op de volgende pagina's:  

* Verplaatsingsvoorstel
* Interne magazijnpick
* Interne magazijnopslag
* Magazijnherindelingsdagboek

De pagina's **Verplaatsingsvoorstel**, **Interne magazijnpick** en **Interne magazijnopslag** werken op dezelfde manier. Gebruik de pagina's om magazijnactiviteiten voor magazijnmedewerkers voor te bereiden. Het verschil zit hem in de geavanceerde functionaliteit die aan elke pagina is gekoppeld, en de verschillende soorten magazijnactiviteiten die waarschijnlijk door verschillende medewerkers worden uitgevoerd:

* Met het verplaatsingsvoorstel kunt u hoog geplaatste pickopslaglocaties vullen met artikelen uit andere opslaglocaties
* Magazijnopslag maakt gebruik van opslagsjablonen
* Picking maakt gebruik van opslaglocatievolgorde en beschikbaarheid

## <a name="warehouse-movement-worksheet"></a><a name="warehouse-movement-worksheet"></a>Magazijnverplaatsingsvoorstel

### <a name="to-move-items-with-the-warehouse-movement-worksheet"></a><a name="to-move-items-with-the-warehouse-movement-worksheet"></a>artikelen met het magazijnverplaatsingswerkblad verplaatsen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verplaatsingsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden op de voorstelregels handmatig in of gebruik een van de volgende acties om de regels automatisch in te vullen:

    * Met **Opslaglocatie-inhoud ophalen** vult u de voorstelregels in met de inhoud van de opslaglocatie(s) die u opgeeft.
    * **Opslaglocatieaanvulling berekenen** functie gebruikt de opslaglocatievolgorde om het bijvullen van opslaglocaties van hoog naar laag voor te stellen.

    > [!NOTE]  
    > Als het artikel voldoet aan de criteria in de onderstaande lijst, zijn de velden **Van zone** en **Van opslaglocatie** leeg. [!INCLUDE [prod_short](includes/prod_short.md)] berekent alleen vanwaar de artikelen moeten worden verplaatst als u de actie **Verplaatsing maken** gebruikt.  
    >  
    > * Het artikel heeft een vervaldatum.  
    > * De schakelaar **Picken volgens FEFO** is ingeschakeld voor de vestiging.  
    > * U gebruikt de functie **Opslaglocatieaanvulling berekenen**.  

3. Kies de actie **Verplaatsing maken** om de verplaatsing te maken. Zodra de verplaatsing klaar is, kunt u deze registreren.  

### <a name="to-register-the-warehouse-movement"></a><a name="to-register-the-warehouse-movement"></a>De magazijnverplaatsing registreren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verplaatsingen** in en kies vervolgens de gerelateerde koppeling.  
2. Open het verplaatsingsdocument om te registreren.  
3. Specificeer regels voor **Plaatsen** waar, welk en vóór wanneer het artikel verplaatst moet worden door waarden te kiezen in de velden **Zone**, **Opslaglocatie**, **Te verwerken aantal** of **Vervaldatum**.  
4. Specificeer op de regels voor **Nemen** in het veld **Te verwerken aantal** het aantal voor de opslaglocatie-inhoud die u wilt verplaatsen. U kunt dit veld alleen bewerken de regels voor **Nemen**. 

    > [!NOTE]
    > Als het nodig is de artikelen voor een regel in meerdere opslaglocaties te picken of te plaatsen, bijvoorbeeld omdat de aangewezen opslaglocatie vol is, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.
 
5. Als u alle voorgestelde aantallen zoals opgegeven in het veld **Aantal** wilt registreren, kiest u de actie **Te verwerken aantal autom. invullen**.  
6. Kies de actie **Registreren**.  

> [!NOTE]  
> Voor vestigingen die gestuurde opslag en pick gebruiken, kunt u artikelen in opslaglocaties van het type **ONTVANGEN** niet handmatig verplaatsen omdat ze nog niet als beschikbare voorraad worden beschouwd. U moet de artikelen in deze opslaglocaties opbergen voordat ze beschikbaar zijn voor verplaatsingen.

## <a name="internal-pick"></a><a name="internal-pick"></a>Interne pick

### <a name="to-create-an-internal-pick"></a><a name="to-create-an-internal-pick"></a>Een interne pick maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Interne mag.-pick** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul het veld **Nr.**, het veld **Vestiging** en het veld **Naar opslaglocatie** in op het sneltabblad **Algemeen**. Het veld **Naar opslaglocatie** geeft aan waar u de gepickte artikelen wilt plaatsen. Voor productiedoeleinden is deze locatie de inkomende productieopslaglocatie of open-shopopslaglocatie. In alle andere gevallen moet u een opslaglocatiecode kiezen van een soort die niet wordt gebruikt voor pickactiviteiten, zoals een opslaglocatie voor staging, verzending of speciale doeleinden.  
4. Selecteer een artikel in het veld **Artikelnr.** en geef het gewenste pickaantal op.  
5. Kies de actie **Pick maken**. De pickinstructie voor het magazijn kan nu worden uitgevoerd door een magazijnmedewerker. Als alternatief kunt u de actie **Vrijgeven** kiezen en magazijnpicks maken met de pagina **Pickvoorstel**. Zie voor meer informatie over pickvoorstellen [Bulksgewijs pickdocumenten maken met het pickvoorstel](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Zodra de pick klaar is, kunt u deze registreren.  

### <a name="to-register-the-warehouse-pick"></a><a name="to-register-the-warehouse-pick"></a>De magazijnpick registreren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Picks** in en kies vervolgens de gerelateerde koppeling.  

    Als u een bepaalde pick wilt bewerken, selecteert u de pick in de lijst. U kunt de lijst ook filteren op de picks die aan u zijn toegewezen.  
2. Als het veld **Toegewezen gebruikers-id** leeg is, voert u uw id in om uzelf te identificeren indien nodig.  
3. Pick de artikelen.  

    Omdat voor het magazijn gestuurde opslag en pick is ingesteld, bepaalt de opslaglocatievolgorde uit welke opslaglocaties gepickt kan worden. De opslaglocaties worden voorgesteld op de pickregels. De instructies bevatten minstens twee afzonderlijke regels voor de acties Nemen en Plaatsen.  

4. Nadat u de pick hebt uitgevoerd en de artikelen op de verzendlocatie hebt geplaatst, kiest u de actie **Pick registreren**.  

## <a name="internal-put-away"></a><a name="internal-put-away"></a>Interne opslag

### <a name="to-create-an-internal-put-away"></a><a name="to-create-an-internal-put-away"></a>Een interne opslag maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Interne magazijnopslag** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul het veld **Nr.**, en het veld **Vestiging** in.
4. Vul voor ieder artikel dat u naar het magazijn wilt verplaatsen een regel in. De velden **Artikelnr.** en **Aantal** zijn verplicht.

    > [!NOTE]  
    > Wanneer u een artikel kiest in het veld **Artikelnr.**, wordt de pagina **Opslaglocatie-inhoud** geopend in plaats van de pagina **Artikelen**. Deze pagina wordt geopend omdat u een artikel opbergt dat is toegewezen aan een bepaalde opslaglocatie - *Opslaglocatie-inhoud* - niet zomaar een artikel, en u weet al uit welke opslaglocatie het artikel moet worden gehaald. Als u het veld **Van opslaglocatie** hebt ingevuld, wordt de inhoud van de opslaglocatie op die waarde gefilterd.

5. Kies de actie **Opslaglocatie-inhoud ophalen** om de regels te vullen met de volledige of gefilterde inhoud van de opslaglocaties in de vestiging.  
6. Kies de actie **Opslag maken**. De opslaginstructie voor het magazijn is nu klaar voor een magazijnmedewerker. Als alternatief kunt u de actie **Vrijgeven** kiezen om magazijnopslag te maken met de pagina **Opslagvoorstel**. Zie voor meer informatie over opslagvoorstellen [Bulksgewijs opslagdocumenten maken met het opslagvoorstel](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Zodra de opslag klaar is, kunt u deze registreren.  

### <a name="to-register-the-warehouse-put-away"></a><a name="to-register-the-warehouse-put-away"></a>De magazijnopslag registreren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnopslag** in en kies vervolgens de gerelateerde koppeling.
2. Open de magazijnopslag die klaar is om te verwerken.  
3. Voer indien nodig uw gebruikers-id in wanneer u aan een opslag begint.  

    Om het opslagproces te optimaliseren, kunt u de opslagregels sorteren op verschillende criteria. Bijvoorbeeld op artikel, schapnummer of vervaldatum.

    * Als de regels voor Nemen en Plaatsen op de ontvangstregels niet opeenvolgend worden weergegeven, kunt u de regels sorteren door **Artikel** te selecteren in het veld **Sorteermethode**.  
    * Als de volgorde van de opslaglocaties de fysieke indeling van het magazijn weerspiegelt, gebruikt u de sorteermethode **Opslaglocatievolgorde** om het werk rond de opslaglocaties te organiseren.  

4. Voer de opslag uit.

    Elke interne opslagregel is in de magazijnopslag omgezet in ten minste twee regels.  

    * De eerste regel met **Nemen** in het veld **actiesoort** geeft aan waar de artikelen zich in het ontvangstgebied bevinden. U kunt de zone en de opslaglocatie op deze regel niet wijzigen.  
    * De volgende regel, met **Plaatsen** in het veld **Actiesoort**, laat zien waar u de artikelen in het magazijn moet plaatsen. Als u een groot aantal artikelen via één ontvangstregel ontvangt, moeten de artikelen mogelijk op verschillende opslaglocaties worden opgeslagen en wordt er een Plaatsen-regel voor elke opslaglocatie weergegeven.  

5. Als u alle artikelen volgens de instructies op de opslaglocaties hebt geplaatst, kiest u de actie **Opslag registreren**.  

## <a name="to-register-a-movement-that-has-already-happened"></a><a name="to-register-a-movement-that-has-already-happened"></a>Een verplaatsing registreren die al heeft plaatsgevonden

Als u moet registreren dat artikelen al naar andere opslaglocaties zijn verplaatst zonder opslag, pick of verplaatsing, kunt u de pagina **Mag. herindelingsdagboek** gebruiken om de verplaatsing te registreren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Mag. herindelingsdagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden **Artikelnr.**, **Van zone**, **Van opslaglocatie**, **Naar zone** en **Naar opslaglocatie** in.  
3. Kies de actie **Registreren**.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
