---
title: Voorraadartikelen in assembleren-op-order-stromen verkopen
description: Op-order-assembleren-artikelen worden voor verkooporders geassembleerd via een assemblageorder.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# Voorraadartikelen in assembleren-op-order-stromen verkopen

Als het veld **Assemblagebeleid** op de artikelkaart van een assemblageartikel **Op order assembleren** bevat, neemt het standaardproces voor de verkooporder aan dat het item niet in voorraad is en voor verkooporders geassembleerd moet worden. Wanneer u het artikel toevoegt aan een verkooporderregel, maakt [!INCLUDE [prod_short](includes/prod_short.md)] automatisch een assemblageorder die is gekoppeld aan de verkooporder. Ga voor meer informatie over het verkopen van assembleren-op-order artikelen naar [Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md). Echter als een deel van de hoeveelheid van de verkooporder al beschikbaar in voorraad is, kunt u de assemblageorder verkleinen door het veld **Aantal voor op order assembleren** op de verkooporderregel te veranderen.  

Het komt relatief zelden voor dat bedrijven voorraadartikelen verkopen als op order te assembleren artikelen. Op order assembleren-artikelen zijn meestal niet standaard. Ze zijn aangepast om te voldoen aan specifieke eisen van de klant. Het is echter mogelijk dat u hoeveelheden van op bestelling te assembleren artikelen in voorraad hebt als gevolg van retourzendingen of annuleringen van orders. Die hoeveelheden moeten worden gepickt en verkocht voordat er nieuwe worden geassembleerd.  

> [!NOTE]  
> Gebruik het feitenblok **Verkoopregeldetails** op de verkooporder om te controleren of op-order-assembleren-artikelen al beschikbaar zijn voor assemblageorders.  

U kunt soortgelijke dingen doen wanneer u component uit voorraad verkoopt en een deel of de gehele hoeveelheid niet beschikbaar is. U kunt de ontbrekende hoeveelheid leveren via een assemblageorder. Zie voor meer informatie over het verkopen van voorraad- en op-order-assembleren artikelen [Op-order-assembleren-artikelen en voorraadartikelen samen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Bepaalde regels zijn van toepassing op het veld **Te verzenden aantal** op verkooporderregels die een combinatie van op-order-assembleren-aantallen en voorraadaantallen bevatten. Ga voor meer informatie over de regels naar [Combinatiescenario's](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Vervang in deze procedure de aantallen voor assembleren op basis van orders met de voorraadaantallen op een verkooporderregel. De volgende stappen geven een overzicht:

1. Beschikbaarheid bepalen.
2. Die hoeveelheid verminderen van de gekoppelde assemblageorder.
3. De voorraadhoeveelheid reserveren om ervoor te zorgen dat deze wordt gepickt en verzonden voor de order.  

## Voorraadartikelen in assembleren-op-order-stromen verkopen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Een verkooporder maken. Ga voor meer informatie over het maken van verkooporders naar [Producten verkopen](sales-how-sell-products.md).  
3. Voer op een verkooporderregel die een op-order-assembleren-artikel bevat in het veld **Aantal** het aantal in.  
4. Bepaal in het feitenblok **Verkoopregeldetails** of de hoeveelheid geheel of gedeeltelijk beschikbaar is.  
5. In het veld **Aantal voor op order assembleren** trekt u de beschikbare hoeveelheid af zodat alleen niet-beschikbare hoeveelheid op de order wordt geassembleerd. Het veld **Gereserveerde hoeveelheid** wordt dienovereenkomstig verlaagd om aan te geven dat de order-naar-order-koppeling of reservering alleen van toepassing is op de te assembleren hoeveelheid.  
6. Op het sneltabblad **Regels** kiest u **Functies** en vervolgens kiest u de actie **Reserveren**.  
7. Selecteer op de pagina **Reservering** de artikelpostregel of -regels die de beschikbare hoeveelheden bevatten, kies de actie **Vanuit huidige regel reserveren** en kies vervolgens de knop **OK**.  

    Op de pagina **Verkooporder** toont het veld **Gereserveerd aantal** nu dat het gehele aantal op de orderregel is gereserveerd. Het veld **Op order te assembleren aantal** weerspiegelt nog steeds de hoeveelheid die moet worden geassembleerd.  

8. Geef de verkooporder vrij om de artikelen beschikbaar te maken voor picken en voor assemblage van de niet-beschikbare artikelen. Ga voor meer informatie over het assembleren van artikelen naar [Artikelen assembleren](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Het veld **Opslaglocatie** in de verkooporder kan de waarde bevatten uit het veld **Opslaglocatiecode assembleren-op-order verzending** of **Opslagloc.code Vanuit-assembl.** op de locatiekaart. In dat geval is het veld **Opslaglocatie** op de verkooporderregel mogelijk onjuist voor deze combinatie van hoeveelheden van assembleren-naar-order en assembleren-naar-voorraad. Het is verstandig om het veld **Opslaglocatie** te bekijken en te controleren of de opslaglocatie voor alle hoeveelheden werkt. U kunt ook twee verschillende hoeveelheden invoeren op aparte verkooporderregels.  

## Zie ook

[Assemblage](assembly-assemble-items.md)  
[Artikelen reserveren](inventory-how-to-reserve-items.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
