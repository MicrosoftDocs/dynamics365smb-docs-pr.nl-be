---
title: Nieuwe vraag order voor order plannen
description: 'Deze planningstaak kan worden uitgevoerd op de pagina Orderplanning, waarin alle nieuwe vraag samen met beschikbaarheidsinformatie en suggesties voor levering worden weergegeven, inclusief artikelvervanging.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5522, 5524, 5526'
ms.date: 07/29/2021
ms.author: bholtorf
---
# Nieuwe vraag order voor order plannen

Deze planningstaak kan worden uitgevoerd op de pagina **Orderplanning**, waarin alle nieuwe vraag samen met beschikbaarheidsinformatie en suggesties voor levering worden weergegeven. Zo beschikt u over een helder hulpmiddel om op effectieve wijze op basis van verkoop- en onderdeelregels te plannen voor de vraag. Vervolgens maakt u direct verschillende soorten orders voor voorzieningen aan.  

U kunt de pagina **Orderplanning** op twee manieren openen, afhankelijk van uw doel: vanuit een order waarvoor u specifiek wilt plannen of in de batchmodus omdat u voor alles en eventuele nieuwe vraag wilt plannen.  


## Een nieuwe productieordervraag plannen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geplande productieorders** in en kies vervolgens de gerelateerde koppeling. U kunt deze stappen uitvoeren voor geplande, vast geplande of vrijgegeven productieorders.
2. Open de productieorder waarvoor u wilt plannen en kies de actie **Planning**.  
3. Kies op de pagina **Orderplanning** de actie **Plan berekenen**.  

Op de pagina worden planningsregels weergegeven volgens het weergavefilter **Productievraag**. Dit zijn niet-gerealiseerde materiaalregels van alle bestaande productieorders. Vraag voor slechts één productieorder wordt niet weergegeven omdat het nodig is om één productieorder te plannen met een overzicht van de vraag voor mogelijk eerdere materiaalregels. Planningsregels voor de productieorder in context worden uitgevouwen.  

## Eventuele nieuwe vraag plannen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Orderplanning** in en kies vervolgens de gerelateerde koppeling  
2. Kies op de pagina **Orderplanning** de actie **Plan berekenen**.
3. Kies de knop **Uitvouwen (+)** in het veld **Benodigde datum** als u de onderliggende planningsregels wilt bekijken, die vraagregels met onvoldoende beschikbaarheid vertegenwoordigen.  
4. Voor elke uitgevouwen planningsregel, oftewel vraagregel, kunt u de waarden weergeven in gegevensvelden onder op de pagina.  

    |Optie|Description|  
    |----------------------------------|---------------------------------------|  
    |**Aantal op andere locaties**|Wordt weergegeven als het artikel op een andere locatie bestaat. U kunt dit artikel opzoeken en selecteren.|  
    |**Vervangingsartikel bestaat**|Geeft aan of er voor dit artikel een vervangingsartikel is gemaakt. U kunt dit artikel opzoeken en selecteren. Deze functie geldt alleen voor materialen, dat wil zeggen voor vraagregels van het soort **Productie**.|  
    |**Beschikbaar aantal**|Geeft het aantal weer dat in totaal van dit artikel, dat wil zeggen de geplande voorraad, beschikbaar is.|  
    |**Vroegst beschikbare datum**|Bevat de aankomstdatum van een inkomende order voor voorzieningen die het benodigde aantal kan dekken op een datum die later valt dan de benodigde datum.|  

5. In het veld **Aanvullingsmethode** selecteert u het soort order dat moet worden gemaakt.  

    De standaardwaarde is de waarde van de artikelkaart, of SKU-kaart, maar u kunt deze wijzigen in een van de drie volgende opties:  

    |Optie|Description|  
    |----------------------------------|---------------------------------------|  
    |**Inkoop**|Er wordt een inkooporder gemaakt.|  
    |**Transfer**|Er wordt een transferorder gemaakt.|  
    |**Prod.-order**|Er wordt een productieorder gemaakt.|  

    In het veld **Aanleveren van** moet u een waarde selecteren op basis van de geselecteerde aanvullingsmethode.  

    > [!NOTE]  
    >  Als het veld niet is ingevuld, wordt er door het systeem een foutbericht weergegeven wanneer u de functie **Orders voor voorzieningen maken** gebruikt. Er wordt dan geen voorzieningsorder gemaakt voor de betreffende planningsregel. Dit is echter niet het geval wanneer de aanvullingsmethode **Prod.-order** is.  

6. In het veld **Aanleveren van** kunt u in de relevante lijst opzoeken en selecteren waar de voorziening vandaan moet komen:  

    - Als de aanvullingsmethode **Inkoop** is, wordt met de opzoekknop in dit veld gezocht op de pagina **Artikelleveranciers**.  
    - Als de aanvullingsmethode **Transfer** is, wordt met de opzoekknop in dit veld gezocht op de pagina **Vestigingsoverzicht**.  

    In het geval dat het artikel in een andere vestiging voorhanden is, wordt er een waarde weergegeven in het veld **Aantal op andere locaties** onder in het venster. U kunt vervolgens de vestiging zoeken en selecteren waaruit het artikel moet worden geleverd wanneer u de transferorder maakt.  

    In het geval dat er voor het gevraagde artikel een vervangingsartikel voorhanden is, bevat het veld **Vervangingsartikel bestaat** de waarde **Ja**. U kunt vervolgens het vervangingsartikel opzoeken en selecteren op de pagina **Artikelvervangingsposten**.  

    > [!NOTE]  
    > Houd er rekening mee dat artikelvervangingen er niet automatisch toe leiden dat een artikel wordt vervangen door een ander artikel, bijvoorbeeld bij het maken van een verkooporder of in een stuklijst. In plaats daarvan wordt u erop gewezen dat er een vervanging voor u beschikbaar is.

7. Schakel het selectievakje **Reserveren** in wanneer u een reservering wilt maken tussen de order voor voorzieningen die u aan het maken bent en de vraagregel waarvoor deze wordt gemaakt. De optie is standaard uitgeschakeld.  

    > [!NOTE]  
    >  Het vakje kan alleen worden ingeschakeld wanneer op de artikelkaart van het artikel de waarde **Optioneel** of **Altijd** is ingevuld in het veld **Reservering**.  

8. In het veld **Te bestellen aantal** kunt u het aantal opgeven dat u wilt bestellen op de order die u aan het maken bent.   
    De standaardwaarde is hetzelfde aantal als in het veld **Benodigd aantal**. Maar u kunt besluiten om meer of minder dan dit aantal te bestellen op basis van uw kennis van de vraagsituatie. Als u bijvoorbeeld op de pagina **Orderplanning** ziet dat er verschillende onafhankelijke vraagregels zijn voor hetzelfde aangeschafte artikel en deze rond dezelfde datum vervallen, kunt u deze regels samenvoegen door het totale benodigde aantal in te vullen in het veld **Te bestellen aantal** van één regel en vervolgens de andere, verouderde planningsregels voor dat artikel verwijderen.  

9. In de velden **Vervaldatum** en **Orderdatum** kunt u de datums voor gemaakte voorzieningenorders invoeren.  

    Deze twee velden zijn met elkaar verbonden op basis van het veld **Std. veiligheidstijd**, dat te vinden is op de pagina **Productie-instellingen**. Standaard is de vervaldatum hetzelfde als de benodigde datum, maar dit kunt u eventueel wijzigen.  

> [!NOTE]  
>  Als u een datum later dan de benodigde datum invoert, ontvangt u een waarschuwingsbericht.  

## Orders voor voorzieningen maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geplande productieorders** in en kies vervolgens de gerelateerde koppeling. U kunt deze stappen uitvoeren voor een geplande, vast gepland of vrijgegeven productieorder.  
2. Open de productieorder waarvoor u wilt plannen en kies de actie **Planning**.  
3. Plaats de cursor op een relevante planningsregel en kies de actie **Orders maken**.  
4. Selecteer een van de volgende opties op de pagina **Orders voor voorzieningen maken** op het sneltabblad **Orderplanning**, in de groep **Orders maken voor**.  

    |Optie|Description|  
    |----------------------------------|---------------------------------------|  
    |**De Actieve regel**|Maak alleen een order voor voorzieningen voor de regel waarop de cursor is geplaatst.|  
    |**De Actieve order**|Maak orders voor voorzieningen voor alle regels in de order waarop de cursor is geplaatst.|  
    |**Alle regels**|Maak voorzieningenorders voor alle regels op de pagina **Orderplanning**.|  

5. Op het sneltabblad **Opties** definieert u wat voor soort voorzieningenorders of inkoopvoorstelregels er moeten worden gemaakt.  

    > [!NOTE]  
    >  de laatste instellingen die u hebt gemaakt op de pagina **Aanvulorders maken** worden opgeslagen onder uw gebruikers-id, zodat deze nog hetzelfde zijn zodra u de pagina weer opent.  

6. Kies de knop **OK** om de voorgestelde voorzieningenorders of inkoopvoorstelregels te maken.  

U hebt nu een planning gemaakt voor de openstaande vraag door middel van het maken van voorzieningenorders voor die vraag. Hoe specifieke processen bij gebruik van de pagina **Orderplanning** verder verlopen, is afhankelijk van het interne beleid van een bedrijf.  

Wanneer u klaar bent met de planning op de pagina **Orderplanning** (als u bijvoorbeeld een alternatieve leveringswijze voor de order hebt gedefinieerd), kunt u doorgaan met het maken van voorzieningenorders voor een of meer van de planningregels.  

> [!NOTE]  
> Door de voorzieningenorders die u maakt kan weer nieuwe afhankelijke vraag ontstaan, bijvoorbeeld naar onderliggende productieorders. Kies daarom altijd **Planning berekenen**, zodat u deze productieorders kunt bekijken en afhandelen voordat u verdergaat vanuit het overzicht.  

## Zie ook

<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
[Gepland](production-planning.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)  
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
