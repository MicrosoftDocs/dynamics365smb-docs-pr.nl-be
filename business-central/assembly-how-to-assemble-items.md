---
title: artikelen samenstellen
description: Meer informatie over de processen assembleren op order en assembleren op voorraad in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# artikelen samenstellen

Als het veld **Aanvullingsmethode** op de artikelkaart **Assemblage** bevat, is de standaardbevoorradingsmethode van het artikel het assembleren volgens een assemblagestuklijst en mogelijk door een specifieke bron. Meer informatie op [Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md). Zie voor meer informatie over hoe u een assemblageartikel instelt [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).

U kunt assemblageartikelen voor twee verschillende assemblageprocessen instellen.

|Proces  |Omschrijving  |
|---------|---------|
|Assembleren voor voorraad     | Artikelen die u assembleert en opslaat voor toekomstige verkoop. Bijvoorbeeld kits voor een aanstaande verkoopcampagne. De artikelen zijn niet gerelateerd aan een verkooporder, althans nog niet. Meestal worden deze artikelen niet aangepast voor verzoeken van klanten.        |
|Assembleren voor order     | Artikelen die u niet op voorraad wilt hebben. Bijvoorbeeld omdat ze zijn aangepast op basis van klantorders of om de kosten van voorhanden voorraad te verlagen. |
  
Dit artikel beschrijft de standaardinstellingen voor assembleren op voorraad. Er zijn misschien andere manieren die geschikter zijn voor uw bedrijf. Zie voor meer informatie [Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) en [Op-order-assembleren-artikelen en voorraadartikelen samen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Assemblycomponenten worden op een speciale manier verwerkt in standaardmagazijnconfiguraties. Zie voor meer informatie [Op-order-assembleren-artikelen met voorraadpicks afhandelen](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## Een artikel assembleren op voorraad

Volg de stappen in deze procedure om een artikel op voorraad te assembleren. Ga voor meer informatie over assembleren op order naar [Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Assemblageorders** in en kies vervolgens de gerelateerde koppeling  
2. Kies de actie **Nieuw**. De pagina **Nieuwe assemblageorder** wordt geopend.  
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Selecteer in het veld **Artikelnr.** het artikel dat u wilt assembleren. U kunt artikelen selecteren die zijn ingesteld voor assemblage en een assemblagestuklijst hebben, of artikelen zonder assemblagestuklijst. Dit laatste is handig voor ongeplande assemblages of scenario's wanneer u artikelherindeling wilt gebruiken en kosten wilt bijhouden.  
5. Voer in het veld **Aantal** het aantal eenheden in dat u van het artikel wilt assembleren.  

    > [!NOTE]  
    >  Als een of meer componenten niet beschikbaar zijn om op de vervaldatum aan de hoeveelheid te voldoen, wordt de pagina **Beschikbaarheid assemblage** geopend. De pagina laat zien hoeveel assemblageartikelen kunnen worden geassembleerd op basis van de beschikbaarheid van componenten. Zie voor meer informatie [Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md). Wanneer u de pagina sluit, wordt de assemblageorder met waarschuwingen omtrent de beschikbaarheid op de regels van de betrokken componenten gemaakt.  

    De regels bevatten de inhoud van de assemblagestuklijst en de opgegeven hoeveelheden.  

    > [!NOTE]  
    >  Als de pagina **Beschikbaarheid assemblage** werd geopend toen u de assemblageorderkop invulde, staat bij iedere betrokken orderregel van de assemblage **Ja** in het veld **Beschikb.waarschuwing** met een koppeling naar gedetailleerde beschikbaarheidsinformatie. <!--check whether this field help is useful For more information, see Check Availability.--> U kunt een probleem met de beschikbaarheid van componenten oplossen door:

    > * Uitstel van de startdatum.
    > * De component vervangen door een ander artikel.
    > * Een beschikbare vervanging selecteren als er een is gedefinieerd.  

6. Geef in het veld **Te assembleren aantal** op hoeveel eenheden van het assemblageartikel u als uitvoer wilt boeken, de volgende keer dat u de assemblageorder boekt. Dit aantal mag lager zijn dan de waarde in het veld **Aantal** om het gedeeltelijk boeken van uitvoer aan te geven.  

    > [!NOTE]  
    >  Om ervoor te zorgen dat het boeken van het verbruik van onderdelen overeenkomt met het boeken van de output van het assemblageartikel, worden de velden met aantallen in de orderregels van de assemblageorder automatisch aangepast aan de waarde die u in het veld **Te assembleren aantal** invoert.  
7. Geef op orderregels van assemblageorders van het type **Item** of **Bron**, in het veld **Te verbruiken aantal**, het aantal eenheden op dat u als verbruikt wilt boeken, de volgende keer dat u de assemblageorder boekt.
8. Wanneer u gereed bent om gedeeltelijk of volledig te boeken, kiest u de actie **Boeken**.  

    > [!NOTE]  
    >  Als er op de regels van de assemblageorder nog steeds waarschuwingen aanwezig zijn, kunt u de order niet boeken. Er verschijnt een bericht over de component of componenten die niet in voorraad zijn.  

Nadat het boeken is voltooid, wordt het assemblageartikel als uitvoer geboekt naar de vestigingscode en mogelijke opslaglocatiecode die op de assemblageorder zijn gedefinieerd. De locatie voor handmatig gemaakte assemblageorders kan worden gekopieerd van de instelling **Standaard locatie voor Orders**. Voor assembleren-op-order kan de vestigingscode van de verkooporderregel worden gekopieerd.  

## Zie ook

[Assemblage](assembly-assemble-items.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
