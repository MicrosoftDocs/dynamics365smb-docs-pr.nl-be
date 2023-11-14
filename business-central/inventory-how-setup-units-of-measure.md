---
title: Artikeleenheden instellen | Microsoft Docs
description: U kunt meerdere maateenheden voor een artikel instellen zodat u maateenheden kunt toewijzen aan het artikel.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2021
ms.author: bholtorf
---
# Maateenheden instellen

Als onderdeel van het opzetten van uw [!INCLUDE [prod_short](includes/prod_short.md)] stelt u algemene maateenheden in op de pagina **Maateenheden**. Wanneer u vervolgens nieuwe artikelen registreert, specificeert u de basismaateenheid op de **artikelkaart**. Maar u kunt later ook maateenheden toevoegen.  

U kunt meerdere eenheden voor een artikel instellen zodat u eenheden kunt toewijzen aan het artikel voor de volgende doeleinden:

- Wijs een basiseenheid op de artikelkaart van het artikel toe om te bepalen hoe het wordt opgeslagen in voorraad en om als conversiebasis te dienen voor alternatieve eenheden.
- Wijs alternatieve eenheden aan inkoop-, productie- of verkoopdocumenten toe om op te geven hoeveel eenheden van de basiseenheid u tegelijk verwerkt in die processen. U kunt het artikel bijvoorbeeld kopen op pallets en alleen afzonderlijke delen in de productie gebruiken.

Als een artikel in één eenheid in voorraad is, maar in een andere eenheid wordt geproduceerd, kan een productieorder worden gemaakt die gebruikmaakt van een productiebatcheenheid voor het berekenen van het juiste aantal onderdelen tijdens de batchverwerking **Productieorder vernieuwen**. Een voorbeeld van een berekening van een productiebatcheenheid is wanneer een geproduceerd artikel als stukgoed in voorraad is maar in tonnen gewicht wordt geproduceerd. Zie voor meer informatie [Werken met productiebatcheenheden](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

Een ander hulpmiddel dat het gemakkelijker maakt om met meerdere maateenheden voor artikelen te werken, is de mogelijkheid om een afrondingsprecisie op te geven voor basismaateenheden. Het specificeren van een afrondingsprecisie geeft richtlijnen over wat iemand moet invoeren voor een bepaald bedrijfsproces en helpt afrondingsproblemen te verminderen. Als u alternatieve maateenheden gebruikt, helpt de waarde in het veld **Aantal in eenheid** bij het berekenen van de hoeveelheid in de basiseenheid, wat kan leiden tot afrondingsproblemen. Stel u bijvoorbeeld voor dat u een doos ontvangt met zes artikelen. Wanneer de doos in uw magazijn aankomt, ontdekt u dat een van de zes artikelen ontbreekt. U besluit niet de ontvangst van één doos te boeken, maar in plaats daarvan de ontvangen hoeveelheid te wijzigen in vijf van zes stuks. Dat zou leiden tot een ontvangst van 4,99998 stukken in plaats van vijf. Op de pagina **Artikeleenheden** kunt u met het veld **Afrondingsprecisie voor aantal** een waarde opgeven waarmee de hoeveelheid wordt geconverteerd naar een getal dat gemakkelijker te begrijpen is. Als we doorgaan met het voorbeeld, zouden we **1** in het veld invoeren om af te ronden op vijf stuks.

## Maateenheden instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Eenheden** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Een nieuwe lege regel wordt ingevoegd.  
3. Vul de velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Als u weet dat uw organisatie artikelen met deze maateenheid zal verkopen aan klanten in andere landen/regio's, kunt u vertalingen toevoegen.  
    1. Selecteer de code waarvoor u vertalingen wilt instellen en kies de actie **Vertalingen**.
    2. Selecteer in het veld **Taal** de pijl-omlaag voor een overzicht van de beschikbare taalcodes. Selecteer de taalcode waarvoor u een vertaling wilt invoeren en kies de knop OK om de code naar het veld te kopiëren.
    3. Voer de gewenste tekst in het veld **Omschrijving** in.
5. Herhaal de vorige stappen voor eventuele extra maateenheden die u wilt toevoegen.  

Wanneer u een nieuw artikel registreert, kunt u de basismaateenheid kiezen uit de lijst met maateenheden die u nu hebt ingesteld. U kunt ook meerdere maateenheden voor een artikel instellen.  

## Meerdere maateenheden voor artikelen instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de artikelkaart waarvoor u alternatieve eenheden wilt instellen.
3. Kies de actie **Eenheden**. De pagina **Artikeleenheden** wordt geopend.
4. Als het veld **Basiseenheid** op de artikelkaart is ingevuld, is die eenheid al ingesteld.
5. Kies de actie **Nieuw**. Een nieuwe lege regel wordt ingevoegd.
6. Voer in het veld **Code** de naam van de eenheid in. Of kies het veld waaruit u de eenheidscodes in de database wilt selecteren.
7. Voer in het veld **Aantal per eenheid** in hoeveel eenheden van de basismaateenheid de nieuwe maateenheid bevat.
8. In de velden **Hoogte**, **Breedte**, **Lengte** en **Gewicht** kunt u de exacte gegevens voor één maateenheid opgeven. Vervolgens kan [!INCLUDE [prod_short](includes/prod_short.md)] berekenen hoeveel er van ieder artikel in een bepaalde opslaglocatie kan worden geplaatst. Het veld **Kubieke inhoud** wordt automatisch berekend op basis van **Hoogte**, **Breedte** en **Lengte**.

    Als een van deze velden een andere waarde dan 0 bevat, wordt die maat gebruikt tijdens alle processen waarbij artikelen in een opslaglocatie worden geplaatst: opslag, verplaatsingen, ontvangsten, zendingen, picks en aanpassingen. [!INCLUDE [prod_short](includes/prod_short.md)] controleert het totaal van elke fysieke maat van de artikelen die worden opgeslagen en de artikelen die al in de opslaglocatie aanwezig zijn, en vergelijkt dit met de maximale grootte of andere maat die in een opslaglocatie past, volgens het capaciteitsbeleid voor de opslaglocatie dat is geselecteerd op de vestigingskaart voor dit artikel. Met andere woorden, u moet voor elke dimensie voor alle artikelmaateenheden dezelfde maateenheid gebruiken - gebruik bijvoorbeeld kilogram of pond voor gewicht, maar wees consistent.
9. Herhaal stap 5 t/m 7 om alle alternatieve eenheden in te stellen die u in verschillende processen voor dit artikel wilt gebruiken.

    In het veld **Basiseenheid** onder in het venster kunt u de basiseenheid van het artikel weergeven of wijzigen. U kunt ook de basiseenheden wijzigen in het veld **Basiseenheid** op de artikelkaart. Op de pagina **Artikeleenheden** moet de basismaateenheid de waarde **1** hebben in het veld **Aantal per maateenheid**.

U kunt nu afwisselende eenheden gebruiken op inkoop-, productie- en verkoopdocumenten. Zie voor meer informatie [Standaardeenheidscodes invoeren voor verkoop- en inkooptransacties](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions).  

## Eenheidsvertalingen instellen

Wanneer u artikelen aan buitenlandse klanten verkoopt, wilt u de eenheid mogelijk opgeven in de taal van de klant. U kunt dat doen door vertalingen voor maateenheden op te geven.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Eenheden** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de code waarvoor u vertalingen wilt instellen en kies de actie **Vertalingen**.
3. Selecteer in het veld **Taal** de pijl-omlaag voor een overzicht van de beschikbare taalcodes. Selecteer de taalcode waarvoor u een vertaling wilt invoeren en kies de knop OK om de code naar het veld te kopiëren.
4. Voer de gewenste tekst in het veld **Omschrijving** in.
5. Herhaal stap 2 tot en met 4 voor de maateenheidscodes en de talen waarvoor u vertalingen wilt invoeren.

## Standaardeenheidscodes invoeren voor verkoop- en inkooptransacties

Als u doorgaans in andere eenheden dan de basiseenheid inkoopt of verkoopt, kunt u verschillende eenheden opgeven voor inkopen en verkopen. U moet hiervoor de maateenheden instellen op de pagina **Artikeleenheden**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de desbetreffende artikelkaart waarvoor u een standaardeenheidscode voor verkopen of inkopen wilt opgeven.
3. Open voor verkopen op het sneltabblad **Factureren** in het veld **Verkoopeenheid** de pagina **Artikeleenheden**.
4. Open voor inkopen op het sneltabblad **Aanvulling** in het veld **Ink.-eenheid** de pagina **Artikeleenheden**.
5. Selecteer de code die u als standaardeenheid voor respectievelijk verkopen of inkopen wilt instellen en kies de knop **OK**.

## Zie ook

[Werken met productiebatcheenheden](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad beheren](inventory-manage-inventory.md)  
[Inkopen beheren](purchasing-manage-purchasing.md)  
[Verkopen beheren](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
