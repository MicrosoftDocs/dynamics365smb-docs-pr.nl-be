---
title: Afroepassemblyorders maken
description: Maak verkoopraamcontracten voor aangepaste assembly-items voordat u periodiek de feitelijke verkooporders maakt volgens de raamcontractovereenkomst.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-blanket-assembly-orders"></a>Afroepassemblyorders maken

U kunt assemblagebeheer gebruiken om een assemblageartikel op verzoek van een klant aan te passen tijdens het verkoopproces. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).  

 Net zoals bij andere artikelen, kunt u ook verkoopraamcontracten maken voor aangepaste assemblageartikelen alvorens u periodiek de werkelijke verkooporders maakt volgens de raamcontractovereenkomst. Dit proces omvat verschillende extra stappen wanneer u het vergelijkt met het maken van een normaal raamcontract, en gebruikt assemblageraamcontracten, een variatie van een gekoppelde assemblageorder.

> [!NOTE]  
>  Net als alle raamcontracten zijn hoeveelheden op assemblageraamcontracten alleen prognoses en niet operationeel totdat ze worden geconverteerd naar werkelijke assemblage orders. Orderfunctionaliteit, zoals beschikbaarheidsberekening, reservering en artikeltracering is dan ook niet actief op assemblageraamcontracten.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Een afroepassemblyorder maken voor een voor-order-assembleren-artikel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopraamcontracten** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuw verkoopraamcontract met één regel voor een assemblageartikel. Zie [Verkoopraamcontracten maken](sales-how-to-create-blanket-sales-orders.md) voor meer informatie.  
3. Voer het volledige aantal in het veld **Aant. op order assembleren** in op de afroepassemblageorderregel.

    > [!NOTE]  
    >  Maak geen raamcontractovereenkomsten voor een gedeeltelijke hoeveelheid. Daarom moet u dezelfde hoeveelheid invoeren die u hebt ingevoerd in het veld **Hoeveelheid** op de verkoopraamcontractregel.  

4. Kies de actie **Op order assembleren** en kies vervolgens de actie **Op orderregels assembleren**. Of kies het veld **Aant. op order assembleren** op de regel.  
5. Bekijk of wijzig de assemblageorderregels volgens de raamcontractovereenkomst die u met de klant hebt gemaakt op de pagina **Op orderregels assembleren**. Als u meer informatie wilt, kiest u de actie **Document weergeven** om de volledige afroepassemblyorder te openen. U kunt de inhoud van de meeste velden niet wijzigen en u kunt niet boeken.  
6. Wanneer u de assemblageorderregels hebt bijgewerkt volgens de raamcontractovereenkomst, sluit u de pagina **Op orderregels assembleren** om terug te keren naar de pagina **Verkoopraamcontract**.  
7. Wanneer de klant vraagt om een verkooporder op basis van het overeengekomen verkoopraamcontract te maken, maakt u een verkooporder voor het overeengekomen assemblageartikel of de artikelen. Zie [Verkoopraamcontracten maken](sales-how-to-create-blanket-sales-orders.md) voor meer informatie.

Het gekoppelde assemblageraamcontract en eventuele aanpassingen zijn gekoppeld aan die nieuwe verkooporder, als voorbereiding op de assemblage van het artikel of de artikelen die verkocht worden.  

## <a name="see-also"></a>Zie ook

[Verkoopraamcontracten maken](sales-how-to-create-blanket-sales-orders.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
