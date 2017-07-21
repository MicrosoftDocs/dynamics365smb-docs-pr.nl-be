---
title: Artikelkaarten maken voor goederen of services| Microsoft Docs
description: U maakt artikelkaarten voor services die u als uren en voor fysieke producten verkoopt, zoals componenten, gereedgemelde goederen, onderdelen of grondstoffen, die u uit uw voorraad verkoopt.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 719e11f2c8fee3d7e5dd3736754700b68f57379c
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-register-new-items"></a>Procedure: Nieuwe artikelen registreren
Artikelen vormen met andere producten de basis van uw bedrijf, de goederen of services waarin u handelt. Elk artikelproduct moet worden geregistreerd als een artikelkaart.

Artikelkaarten bevatten de informatie die is vereist om artikelen te kopen, op te slaan, te verkopen, te leveren en te verantwoorden.

De artikelkaart kan van het type **Voorraad** of **Service** zijn, om aan te geven of het artikel een fysieke eenheid is of arbeidstijd. Behalve enkele velden die over de materiële aspecten van een artikel gaan, functioneren alle velden op een artikelkaart op dezelfde manier voor voorraadartikelen en services. Zie voor meer informatie over het verkopen van een artikel [Procedure: Producten verkopen](sales-how-sell-products.md) of [Procedure: Verkoop factureren](sales-how-invoice-sales.md).

Een artikel kan als bovenliggend artikel met onderliggende artikelen in een stuklijst worden gestructureerd. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt naar een stuklijst verwezen als een assemblagestuklijst. U gebruikt assemblagestuklijsten om bovenliggende artikelen te structureren die u verkoopt als kits bestaande uit de onderdelen van de bovenliggende artikelen, of die u voor orders of voor voorraad assembleert. Zie [Procedure: Werken met stuklijsten](inventory-how-work-BOMs.md) voor meer informatie.

> [!NOTE]  
>   Als klantsjablonen voor verschillende klantsoorten bestaan, wordt een venster automatisch weergegeven wanneer u een nieuwe artikelkaart maakt van waaruit u een geschikte sjabloon kunt selecteren. Als er slechts één artikelsjabloon bestaat, gebruiken nieuwe artikelkaarten altijd deze sjabloon.

## <a name="to-create-a-new-item-card"></a>Een nieuwe artikelkaart maken
1. Kies op de startpagina de actie **Artikelen** om de lijst met bestaande artikelen te openen.  
2. Kies in het venster **Artikelen** de actie **Nieuw**.

    Als er slechts één artikelsjabloon bestaat, wordt vervolgens een nieuwe artikelkaart geopend waarin enkele velden zijn ingevuld met informatie van de sjabloon.
3. Kies in het venster **Selecteer een sjabloon voor een nieuw artikel** de sjabloon die u wilt gebruiken voor de nieuwe artikelkaart.
4. Kies de knop **Ok**. Een nieuwe artikelkaart wordt geopend met enkele velden met informatie uit de sjabloon.
5. Ga door met velden op de artikelkaart in te vullen of te wijzigen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Op het sneltabblad **Prijs en boeken** kunt u speciale prijzen of kortingen weergeven die u voor het artikel verleent als aan bepaalde criteria wordt voldaan, zoals klant, minimaal orderaantal of einddatum. Elke rij vertegenwoordigt een speciale prijs of regelkorting. Elke kolom vertegenwoordigt een criterium dat moet worden toegepast om de speciale prijs te garanderen die u invoert in het veld **Eenheidsprijs** of de regelkorting die u invoert in het veld **Regelkorting %**. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).

Het artikel is nu geregistreerd en de artikelkaart is klaar om voor inkoop- en verkoopdocumenten te worden gebruikt.

Als u deze artikelkaart als sjabloon wilt gebruiken wanneer u nieuwe artikelkaarten maakt, kunt u deze opslaan als een sjabloon. Zie de volgende onderwerpen voor meer informatie.

## <a name="to-save-the-item-card-as-a-template"></a>De artikelkaart als sjabloon opslaan
1. Kies in het venster **Artikelkaart** de actie **Opslaan als sjabloon**. Het venster **Artikelsjabloon** opent de weergave van de artikelkaart als sjabloon.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**. Het venster **Dimensiesjablonen** geeft alle dimensiecodes weer die voor het item zijn ingesteld.
4. Bewerk of typ dimensiecodes die van toepassing zijn op nieuwe artikelkaarten die worden gemaakt met de sjabloon.
5. Wanneer u de nieuwe artikelsjabloon hebt voltooid, kiest u de knop **OK**.

De artikelsjabloon wordt toegevoegd aan de lijst met artikelsjablonen, zodat u deze kunt gebruiken om nieuwe artikelkaarten te maken.

## <a name="see-also"></a>Zie ook
  [Voorraad](inventory-manage-inventory.md)  
  [Inkoop](purchasing-manage-purchasing.md)  
  [Verkoop](sales-manage-sales.md)  
  [Werken met [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
