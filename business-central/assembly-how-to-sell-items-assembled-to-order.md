---
title: Assembleren voor order-artikelen verkopen
description: Leer hoe u een artikel verkoopt dat is geassembleerd voor een order.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="sell-items-assembled-to-order"></a><a name="sell-items-assembled-to-order"></a>Assembleren voor order-artikelen verkopen

Artikelen die zijn ingesteld voor op-order-assembleren, worden niet op voorraad verwacht en worden geassembleerd wanneer ze worden opgenomen in een verkooporder. Een artikel is ingesteld voor op order assembleren als het veld **Assemblagebeleid** op de artikelkaart **Op order assembleren bevat**. Wanneer u het artikel invoert op een verkooporderregel, wordt automatisch een assemblageorder gemaakt en gekoppeld aan de verkooporder.  

> [!NOTE]  
> Als sommige op-order-assembleren-artikelen al in voorraad zijn, kunt u die hoeveelheid aftrekken van de assemblageorder en reserveren uit de voorraad. Zie voor meer informatie [Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)  

In deze procedure kunt u de verkoop van een artikel verwerken dat wordt samengesteld volgens de specificaties die zijn aangevraagd door de klant. De stappen omvatten: 

* Een verkooporderregel maken.
* Het assemblageartikel aanpassen door de componenten en resources ervan te bewerken.
* Beschikbaarheid controleren om een leverdatum vast te stellen.
* De verkooporder vrijgeven om te assembleren en onmiddellijk te verzenden.  

> [!NOTE]  
> De volgende procedure bevat niet de stappen voor het maken van een standaardverkooporder die plaatsvinden vóór de stap waarin u het op-order-assembleren artikel invoert op een verkooporderregel. Lees meer over het maken van verkooporders op [Producten verkopen met een klantverkooporder](sales-how-sell-products.md).  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a><a name="to-sell-an-item-that-is-assembled-to-order"></a>Een artikel verkopen dat is samengesteld voor een order

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Een verkooporder maken. 
3. In het veld **Nr.** een artikel in dat is ingesteld om op order te worden geassembleerd.  
4. Definieer vanuit welke vestiging het artikel moet worden verkocht in het veld **Vestiging**. Het assemblageproces wordt uitgevoerd in die vestiging.  
5. Voer het aantal te verkopen artikelen in in het veld **Hoeveelheid**.  

    > [!NOTE]  
    >  Als een of meer componenten van het aantal aangevraagde assemblageartikelen niet beschikbaar is, verschijnt een pagina met een beschikbaarheidswaarschuwing. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    Een assemblageorder wordt gemaakt en gekoppeld aan de verkooporderregel. De vervaldatum van de assemblageorder is de verzenddatum van de verkooporderregel.  

    Het te verkopen aantal wordt gekopieerd naar het veld **Aantal voor op order assembleren**. Dat geeft aan dat de artikelinstellingen verwachten dat u het volledige aantal op de verkoopregel assembleert op order. U kunt een kleinere hoeveelheid op order assembleren, bijvoorbeeld als u weet dat sommige artikelen al beschikbaar zijn. Zie voor meer informatie [Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)  

6. Als de klant nog een artikel in een kit wil, kiest u op het sneltabblad **Regels** de actie **Regel**, kiest u de actie **Op order assembleren** en kiest u vervolgens de actie **Op orderregels assembleren** om de standaard assemblagecomponenten weer te geven en te wijzigen. U kunt ook het veld **Aantal voor op order assembleren** kiezen.  
7. Maak op de pagina **Op orderregels assembleren** een nieuwe regel van het type **Artikel** voor de aanvullende assemblagecomponent.  

    U kunt de volgorde ook aanpassen door de hoeveelheid van één standaardartikel in de kit te verhogen. U kunt dit doen door de waarde in het veld **Aantal per** op de specifieke assemblageorderregel te verhogen.  

    > [!NOTE]  
    >  De pagina **Op orderregels assembleren** bevat alleen de basisvelden om de componentenlijst aan te passen, artikeltraceringsnummers toe te voegen of problemen met de beschikbaarheid op te lossen. Als u meer informatie over de assemblageorder wilt toevoegen, zoals de begindatum van de assemblageorder, kiest u de actie **Documenten weergeven**. Hiermee opent u een volledige weergave van de assemblageorder die is gekoppeld aan de verkooporderregel. U kunt de inhoud van de meeste velden in de assemblageorderkop niet wijzigen en u kunt er geen assemblage-uitvoer vanuit boeken. U moet de verzending van de verkooporderregel boeken.  
    >
    >  Op de gekoppelde assemblageorders kan alleen het veld **Begindatum** worden gewijzigd. Door de begindatum te wijzigen kunnen assemblagemedewerkers aangeven dat ze eerder met de assemblage beginnen dan de vervaldatum. Alle velden op de regels van de gekoppelde assemblageorder kunnen worden gewijzigd, zodat magazijnmedewerkers verbruikcijfers kunnen invoeren tijdens het proces.  

8. Op problemen met de beschikbaarheid componenten of controleren. Selecteer bijvoorbeeld een vervangend artikel.  
9. Sluit de pagina **Op orderregels assembleren**. De gekoppelde assemblageorder is nu klaar en medewerkers kunnen beginnen de aangepaste artikelen te assembleren.  
10. Kies in de verkooporder de actie **Vrijgeven** om de assemblageafdeling te informeren dat het assemblageproces kan worden gestart. Zie voor meer informatie [Artikelen samenstellen](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Artikelvervangingen leiden er niet automatisch toe dat een artikel wordt vervangen door een ander artikel, bijvoorbeeld bij het maken van een verkooporder of in een stuklijst. In plaats daarvan wordt u erop gewezen dat er een vervanging beschikbaar is.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
