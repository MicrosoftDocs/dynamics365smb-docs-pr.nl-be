---
title: Order voor order plannen | Microsoft Docs
description: Deze planningstaak kan worden uitgevoerd in het venster **Orderplanning**, waarin alle nieuwe vraag samen met beschikbaarheidsinformatie en suggesties voor levering worden weergegeven. Zo beschikt u over een helder hulpmiddel om op effectieve wijze op basis van verkoop- en onderdeelregels te plannen voor de vraag. Vervolgens maakt u direct verschillende soorten orders voor voorzieningen aan.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a7266eddba4293807a1e7e2a187c5002be771499
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="plan-for-new-demand-order-by-order"></a>Nieuwe vraag order voor order plannen
Deze planningstaak kan worden uitgevoerd in het venster **Orderplanning**, waarin alle nieuwe vraag samen met beschikbaarheidsinformatie en suggesties voor levering worden weergegeven. Zo beschikt u over een helder hulpmiddel om op effectieve wijze op basis van verkoop- en onderdeelregels te plannen voor de vraag. Vervolgens maakt u direct verschillende soorten orders voor voorzieningen aan.  

U kunt het venster **Orderplanning** op twee manieren openen, afhankelijk van uw doel: vanuit een order waarvoor u specifiek wilt plannen of in de batchmodus omdat u voor alles en eventuele nieuwe vraag wilt plannen.  


## <a name="to-plan-for-new-production-order-demand"></a>Een nieuwe productieordervraag plannen  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Geplande productieorders** in en klik op de gerelateerde koppeling. U kunt deze stappen uitvoeren voor geplande, vast geplande of vrijgegeven productieorders.
2.  Open de productieorder waarvoor u wilt plannen en kies de actie **Planning**.  
3.  Kies in het venster **Orderplanning** de actie **Plan berekenen**.  

In het venster worden planningsregels weergegeven volgens het weergavefilter **Productievraag**. Dit zijn niet-gerealiseerde materiaalregels van alle bestaande productieorders. Vraag voor slechts één productieorder wordt niet weergegeven omdat het nodig is om één productieorder te plannen met een overzicht van de vraag voor mogelijk eerdere materiaalregels. Planningsregels voor de productieorder in context worden uitgevouwen.  

## <a name="to-plan-for-any-new-demand"></a>Eventuele nieuwe vraag plannen  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Orderplanning** in en klik op de gerelateerde koppeling.  
2.  Kies in het venster **Orderplanning** de actie **Plan berekenen**.
3.  Kies de knop **Uitvouwen (+)** in het veld **Benodigde datum** als u de onderliggende planningsregels wilt bekijken, die vraagregels met onvoldoende beschikbaarheid vertegenwoordigen.  
4.  Voor elke uitgevouwen planningsregel, oftewel vraagregel, kunt u de waarden weergeven in gegevensvelden onder in het venster.  

    |Optie|Description|  
    |----------------------------------|---------------------------------------|  
    |**Aantal op andere locaties**|Wordt weergegeven als het artikel op een andere locatie bestaat. U kunt dit artikel opzoeken en selecteren.|  
    |**Vervangingsartikel bestaat**|Geeft aan of er voor dit artikel een vervangingsartikel is gemaakt. U kunt dit artikel opzoeken en selecteren. Deze functie geldt alleen voor materialen, dat wil zeggen voor vraagregels van het soort **Productie**.|  
    |**Beschikbaar aantal**|Geeft het aantal weer dat in totaal van dit artikel, dat wil zeggen de geplande voorraad, beschikbaar is.|  
    |**Vroegst beschikbare datum**|Bevat de aankomstdatum van een inkomende order voor voorzieningen die het benodigde aantal kan dekken op een datum die later valt dan de benodigde datum.|  

5.  In het veld **Aanvullingsmethode** selecteert u het soort order dat moet worden gemaakt.  

    De standaardwaarde is de waarde van de artikelkaart, of SKU-kaart, maar u kunt deze wijzigen in een van de drie volgende opties:  

    |Optie|Description|  
    |----------------------------------|---------------------------------------|  
    |**Inkoop**|Er wordt een inkooporder gemaakt.|  
    |**Transfer**|Er wordt een transferorder gemaakt.|  
    |**Prod.-order**|Er wordt een productieorder gemaakt.|  

    In het veld **Aanleveren van** moet u een waarde selecteren op basis van de geselecteerde aanvullingsmethode.  

    > [!NOTE]  
    >  Als het veld niet is ingevuld, wordt er door het systeem een foutbericht weergegeven wanneer u de functie **Orders voor voorzieningen maken** gebruikt. Er wordt dan geen voorzieningsorder gemaakt voor de betreffende planningsregel. Dit is echter niet het geval wanneer de aanvullingsmethode **Prod.-order** is.  

6.  In het veld **Aanleveren van** kunt u in de relevante lijst opzoeken en selecteren waar de voorziening vandaan moet komen:  

    - Als de aanvullingsmethode **Inkoop** is, wordt met de opzoekknop in dit veld gezocht in het venster **Artikelleveranciers**.  
    - Als de aanvullingsmethode **Transfer** is, wordt met de opzoekknop in dit veld gezocht in het venster **Vestigingsoverzicht**.  

    In het geval dat het artikel in een andere vestiging voorhanden is, wordt er een waarde weergegeven in het veld **Aantal op andere locaties** onder in het venster. U kunt vervolgens de vestiging zoeken en selecteren waaruit het artikel moet worden geleverd wanneer u de transferorder maakt.  

    In het geval dat er voor het gevraagde artikel een vervangingsartikel voorhanden is, bevat het veld **Vervangingsartikel bestaat** de waarde **Ja**. U kunt vervolgens het vervangingsartikel opzoeken en selecteren in het venster **Artikelvervangingsposten**.  

7.  Schakel het selectievakje **Reserveren** in wanneer u een reservering wilt maken tussen de order voor voorzieningen die u aan het maken bent en de vraagregel waarvoor deze wordt gemaakt. De optie is standaard uitgeschakeld.  

    > [!NOTE]  
    >  Het vakje kan alleen worden ingeschakeld wanneer op de artikelkaart van het artikel de waarde **Optioneel** of **Altijd** is ingevuld in het veld **Reservering**.  

8.  In het veld **Te bestellen aantal** kunt u het aantal opgeven dat u wilt bestellen op de order die u aan het maken bent.   
    De standaardwaarde is hetzelfde aantal als in het veld **Benodigd aantal**. Maar u kunt besluiten om meer of minder dan dit aantal te bestellen op basis van uw kennis van de vraagsituatie. Als u bijvoorbeeld in het venster **Orderplanning** ziet dat er verschillende onafhankelijke vraagregels zijn voor hetzelfde aangeschafte artikel en deze rond dezelfde datum vervallen, kunt u deze regels samenvoegen door het totale benodigde aantal in te vullen in het veld **Te bestellen aantal** van één regel en vervolgens de andere, verouderde planningsregels voor dat artikel verwijderen.  

9.  In de velden **Vervaldatum** en **Orderdatum** kunt u de datums voor gemaakte voorzieningenorders invoeren.  

    Deze twee velden zijn met elkaar verbonden op basis van het veld **Std. veiligheidstijd**, dat te vinden is in het venster **Productie-instellingen**. Standaard is de vervaldatum hetzelfde als de benodigde datum, maar dit kunt u eventueel wijzigen.  

> [!NOTE]  
>   Als u een datum later dan de benodigde datum invoert, ontvangt u een waarschuwingsbericht.  

## <a name="to-make-supply-orders"></a>Orders voor voorzieningen maken  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Geplande productieorders** in en klik op de gerelateerde koppeling. U kunt deze stappen uitvoeren voor een geplande, vast gepland of vrijgegeven productieorder.  
2.  Open de productieorder waarvoor u wilt plannen en kies de actie **Planning**.  
3.  Plaats de cursor op een relevante planningsregel en kies de actie **Orders maken**.  
4.  Selecteer een van de volgende opties in het venster **Orders voor voorzieningen maken** op het sneltabblad **Orderplanning**, in de groep **Orders maken voor**.  

    |Optie|Description|  
    |----------------------------------|---------------------------------------|  
    |**De Actieve regel**|Maak alleen een order voor voorzieningen voor de regel waarop de cursor is geplaatst.|  
    |**De Actieve order**|Maak orders voor voorzieningen voor alle regels in de order waarop de cursor is geplaatst.|  
    |**Alle regels**|Maak voorzieningenorders voor alle regels in het venster **Orderplanning**.|  

5.  Op het sneltabblad **Opties** definieert u wat voor soort voorzieningenorders of inkoopvoorstelregels er moeten worden gemaakt.  

    > [!NOTE]  
    >  De laatste instellingen die u hebt gemaakt in het venster **Orders voor voorzieningen maken** worden opgeslagen onder uw gebruikers-id, zodat deze nog hetzelfde zijn zodra u het venster weer opent.  

6.  Kies de knop **OK** om de voorgestelde voorzieningenorders of inkoopvoorstelregels te maken.  

U hebt nu een planning gemaakt voor de openstaande vraag door middel van het maken van voorzieningenorders voor die vraag. Hoe specifieke processen bij gebruik van het venster **Orderplanning** verder verlopen, is afhankelijk van het interne beleid van een bedrijf.  

Wanneer u klaar bent met de planning in het venster **Orderplanning** (als u bijvoorbeeld een alternatieve leveringswijze voor de order hebt gedefinieerd), kunt u doorgaan met het maken van voorzieningenorders voor een of meer van de planningregels.  

> [!NOTE]  
>  Door de voorzieningenorders die u maakt kan weer nieuwe afhankelijke vraag ontstaan, bijvoorbeeld naar onderliggende productieorders. Kies daarom altijd **Planning berekenen**, zodat u deze productieorders kunt bekijken en afhandelen voordat u verdergaat vanuit het overzicht.  

## <a name="see-also"></a>Zie ook  
[Gepland](production-planning.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

