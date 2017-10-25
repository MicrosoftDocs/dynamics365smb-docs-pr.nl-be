---
title: Een inkoopfactuur maken van een verkoopfactuur om artikelen te kopen voor een verkoop | Microsoft Docs
description: Vanuit een verkoopfactuur kunt u, om producten te kopen, een inkoopfactuur maken voor een leverancier.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a>Procedure: Producten kopen voor een verkoop
Vanuit verkooporders en verkoopfacturen kunt u functie gebruiken om snel inkoopdocumenten te maken voor ontbrekende artikelaantallen die vereist worden door de verkoop. U kunt twee verschillende functies gebruiken, afhankelijk van de documentsoort.
|Functie|Description|
|--------|-----------|
|**Inkooporders maken**|Vanuit een verkooporder maakt deze functie een inkooporder voor elk van de artikelen op de verkooporder. U kunt het inkoopaantal wijzigen voordat u de inkooporders maakt. Alleen niet-beschikbare verkoopaantallen worden voorgesteld.
|**Inkoopfactuur maken**|Vanuit een verkooporder en vanuit een verkoopfactuur maakt deze functie een inkoopfactuur voor een geselecteerde leverancier voor alle regels of geselecteerde regels op het verkoopdocument. Het volledige verkoopaantal wordt voorgesteld.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Een of meerdere inkooporders van een verkooporder maken
Als u een inkooporder wilt maken voor elk niet-beschikbaar artikelaantal op de verkooporder, gebruikt u de functie **Inkooporders maken**. 

> [!NOTE]  
>   Deze functionaliteit vereist dat uw ervaring is ingesteld op **Suite**. Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).

1. Kies op de startpagina de tegel **Doorlopende verkooporders**.
2. Open een verkooporder waarvoor u artikelen wilt inkopen.
3. Kies de actie **Inkooporders maken**.

    Het venster **Inkooporders maken** wordt geopend met een regel voor elk ander artikel op de verkooporder. Regels voor volledig beschikbare verkoopaantallen en niet-beschikbare verkoopaantallen (grijs) worden standaard weergegeven. U kunt de actie **Niet-beschikbare weergeven** kiezen om alleen regels weer te geven voor niet-beschikbare verkoopaantallen.

    Het veld **In te kopen aantal** bevat standaard het niet-beschikbare verkoopaantal.
4. Als u een ander aantal wilt aanschaffen dan het niet-beschikbare verkoopaantal, bewerkt u de waarde in het veld **In te kopen aantal**.

    > [!NOTE]  
>   U kunt ook het veld **In te kopen aantal** wijzigen op grijze regels, ook al vertegenwoordigen deze volledig beschikbare verkoopaantallen.
5. Kies de knop **OK**. 
    
    Een inkooporder wordt gemaakt voor elke leverancier van artikelen op de verkooporder, inclusief aantalwijzigingen die u aanbrengt in het venster **Inkooporders maken**.
7. Ga verder met het verwerken van de inkooporder of -orders, bijvoorbeeld door inkooporderregels te bewerken of toe te voegen. Zie voor meer informatie [Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Een inkoopfactuur van een verkooporder of verkoopfactuur maken
Als u één inkoopfactuur wilt maken voor een of meer regels in een verkoopdocument door eerst te selecteren van welke leverancier wordt gekocht, gebruikt u de functie **Inkoopfactuur maken**. 

> [!NOTE]  
>   Deze functie maakt een inkoopfactuur voor het exacte artikelaantal op het geselecteerde verkoopdocument. Als u het inkoopaantal wilt wijzigen, moet u de inkoopfactuur wijzigen nadat deze is gemaakt.  

1. Kies op de startpagina de tegel **Doorlopende verkoopfacturen**.
2. Open een verkoopfactuur waarvoor u artikelen wilt inkopen.
3. Selecteer een of meer verkoopfactuurregels die u wilt gebruiken op de inkoopfactuur. Als u alle verkoopfactuurregels wilt gebruiken, selecteert u ze allemaal of selecteert u helemaal geen regels.
4. Kies de actie **Inkoopfactuur maken**.
5. Selecteer **Alle regels** of **Geselecteerde regels** en kies de knop **OK**.  
6. Selecteer in de lijst met leveranciers die wordt weergegeven, de leverancier van wie u alle artikelen wilt kopen en kies vervolgens de knop **OK**.

    Er wordt een inkoopfactuur gemaakt die één, meerdere of alle regels op de verkoopfactuur bevat.
7. Ga verder met het verwerken van de inkoopfactuur, bijvoorbeeld door inkoopfactuurregels te bewerken of toe te voegen. Zie voor meer informatie [Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md)  
[Procedure: Verkopen factureren](sales-how-invoice-sales.md)  
[Procedure: Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

