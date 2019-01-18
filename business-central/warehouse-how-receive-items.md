---
title: Artikelen ontvangen | Microsoft Docs
description: Bij ontvangst van artikelen in een magazijn waarvoor magazijnontvangstverwerking is ingesteld, moet u de regels ophalen van het vrijgegeven brondocument waaruit de ontvangst voortkomt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: e56105cbd2410befea964c5445d8227021058d4f
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="receive-items"></a>Artikelen ontvangen
Bij ontvangst van artikelen in een magazijn waarvoor magazijnontvangstverwerking niet is ingesteld, registreert u de ontvangst in het gerelateerde bedrijfsdocument, zoals een inkooporder, verkoopretourorder of inkomende transferorder.

Bij ontvangst van artikelen in een magazijn waarvoor magazijnontvangstverwerking is ingesteld, moet u de regels ophalen van het vrijgegeven brondocument waaruit de ontvangst voortkomt. Als u met opslaglocaties werkt, kunt u de voorgestelde standaardopslaglocatie accepteren of, als het artikel nog niet in het magazijn is gebruikt, een andere opslaglocatie voor het artikel invullen. Vervolgens moet u de aantallen van de ontvangen artikelen invullen en de ontvangst boeken.  

## <a name="to-receive-items-with-a-purchase-order"></a>Artikelen ontvangen met een inkooporder
Hieronder wordt beschreven hoe u artikelen ontvangt met een inkooporder. De stappen zijn vergelijkbaar voor verkoopretourorders en transferorders.  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Open een bestaande inkooporder of maak een nieuwe. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).
3. Voer in het veld **Te ontvangen aantal** het aantal in dat u hebt ontvangen.

    De waarde in het veld **Ontvangen aantal** wordt dienovereenkomstig bijgewerkt. Als het een gedeeltelijke ontvangst is, is de waarde lager dan de waarde in het veld **Aantal**.
4. Kies de actie **Boeken**.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Artikelen ontvangen met een magazijnontvangst
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnontvangsten** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  

    Vul de velden op het sneltabblad **Algemeen** in. Bij het ophalen van brondocumentregels worden bepaalde gegevens automatisch naar elke regel gekopieerd.  

    Voor magazijnconfiguraties met gestuurde opslag en pick: als de vestiging een standaardzone en -opslaglocatie voor ontvangsten heeft, worden de velden **Zone** en **Opslaglocatie** automatisch ingevuld. U kunt deze waarden desgewenst wijzigen.  

    > [!NOTE]  
    >  Als u artikelen wilt ontvangen met andere magazijnklassen dan de magazijnklasse van de opslaglocatie in het veld **Opslaglocatie** op de documentkop, moet u de inhoud van het veld **Opslaglocatie** op de kop verwijderen voordat u de brondocumentregels voor de artikelen ophaalt.  
3.  Kies de actie **Brondocumenten ophalen**. De pagina **Brondocumenten** verschijnt.

    U kunt vanuit een nieuwe of geopende magazijnontvangst de pagina **Filters om brondoc. op te halen** gebruiken voor het ophalen van de vrijgegeven brondocumentregels die bepalen welke artikelen moeten worden ontvangen of verzonden.

    1. Kies de actie **Filters om brondoc. op te halen gebruiken**.  
    2. U stelt een nieuw filter in door een omschrijvende code in te voeren in het veld **Code** en vervolgens de actie **Wijzigen** te kiezen.  
    3. Definieer het soort brondocumentregels dat u wilt ophalen door de relevante filtervelden in te vullen.  
    4. Kies de actie **Uitvoeren**.  

    Alle vrijgegeven brondocumentregels die voldoen aan de filtercriteria worden nu ingevoegd op de pagina **Magazijnontvangst** van waaruit u de filterfunctie hebt geactiveerd.  

    De filtercombinaties die u definieert, worden opgeslagen op de pagina **Filters om brondoc. op te halen** tot de volgende keer dat u deze nodig hebt. U kunt een onbeperkt aantal filtercombinaties maken. U kunt de criteria op elk moment wijzigen door de actie **Wijzigen** te kiezen.

4.  Selecteer de brondocumenten waarvoor u artikelen wilt ontvangen en klik op **OK**.  

    De regels van de brondocumenten verschijnen op de pagina **Magazijnontvangst**. Het veld **Te ontvangen aantal** is ingevuld met de openstaande hoeveelheid voor elke regel, maar u kunt het aantal wijzigen indien nodig. Als u de inhoud van het veld **Opslaglocatie** op het sneltabblad **Algemeen** verwijdert voordat u de regels ophaalt, moet u op elke ontvangstregel een opslaglocatie invullen.  

    > [!NOTE]  
    >  Kies de actie **Te ontvangen aantal verwijderen** als u op alle regels nul wilt invullen in het veld **Te ontvangen aantal**. Om het veld nogmaals in te vullen met het openstaande aantal, kiest u de actie **Te ontvangen aantal automatisch invullen**.  

    > [!NOTE]  
    >  U kunt niet meer artikelen ontvangen dan het aantal in het veld **Openstaand aantal** op de brondocumentregel. Om meer artikelen te ontvangen, haalt u een ander brondocument op dat een regel bevat voor het item met behulp van de filterfunctie om brondocumenten met het artikel op te halen.  

5.  Boek de magazijnontvangst. De velden met aantallen in de brondocumenten worden bijgewerkt en de artikelen worden bij de bedrijfsvoorraad gevoegd.  

Als u met magazijnopslag werkt, worden de ontvangstregels naar de magazijnopslagfunctie verzonden. Artikelen die al zijn ontvangen, kunnen pas na opslag worden gepickt. De ontvangen artikelen worden geïdentificeerd als beschikbare voorraad nadat de opslag is geregistreerd.  

Als u niet met magazijnopslag, maar met opslaglocaties werkt, wordt de opslag van de artikelen geregistreerd in de opslaglocatie die is opgegeven op de brondocumentregel.  

> [!NOTE]  
>  Met de functie **Boeken en afdrukken** kunt u zowel de ontvangst boeken als opslaginstructies afdrukken waarin wordt aangegeven waar de artikelen moeten worden opgeslagen.  
>   
>  Als uw locatie met gestuurde opslag en pick werkt, wordt de beste opslaglocatie voor de artikelen bepaald aan de hand van de opslagsjablonen. De opslaglocatie wordt vervolgens op de opslaginstructie afgedrukt.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

