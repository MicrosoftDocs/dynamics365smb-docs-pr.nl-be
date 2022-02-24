---
title: Ontvangst combineren | Microsoft Docs
description: Als u meer dan één inkoopontvangst tegelijk wilt factureren, kunt u de functie Ontvangsten combineren gebruiken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/17/2018
ms.author: sgroespe
ms.openlocfilehash: 08a0bb315916ab2a5d344519b680e48bcf6d95fa
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2911227"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Ontvangsten combineren op één factuur
Als u meer dan één inkoopontvangst tegelijk wilt factureren, kunt u de functie **Ontvangsten combineren** gebruiken.  

Een gecombineerde inkoopontvangst kan pas worden gemaakt wanneer meer inkoopontvangsten van dezelfde leverancier in dezelfde valuta zijn geboekt. U moet dus twee of meer inkooporders hebben ingevuld en deze hebben geboekt als ontvangen, maar niet als gefactureerd.  

Wanneer inkoopontvangsten zijn gecombineerd op een factuur en zijn geboekt, wordt een geboekte inkoopfactuur gemaakt voor de gefactureerde regels. Het veld **Gefactureerd aantal** op de oorspronkelijke inkooporder of het oorspronkelijke inkoopraamcontract wordt bijgewerkt op basis van het gefactureerde aantal. Dit oorspronkelijke inkoopdocument wordt echter niet verwijderd, zelfs als dit volledig is ontvangen en gefactureerd en daarom moet u het inkoopdocument zelf verwijderen.  

## <a name="to-combine-receipts"></a>Ontvangsten combineren  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).  
3. Op het sneltabblad **Regels** selecteert u de actie **Ontvangstregels ophalen**.  
4. Selecteer meerdere ontvangstregels die u wilt opnemen in de factuur.  

    Als een onjuiste ontvangstregel is geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de inkoopfactuur gewoon verwijderen en vervolgens de functie **Ontvangstregels ophalen** opnieuw gebruiken.  
5. Kies de actie **Boeken** om de factuur te boeken.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Open inkooporders verwijderen na gecombineerde ontvangstboeking  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gefactureerde inkooporders verwijderen** in en selecteer de desbetreffende koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Kies de knop **OK**.  

U kunt de afzonderlijke orders ook handmatig verwijderen.

Herhaal stap 1 t/m 3 voor alle andere betrokken documenten, zoals inkoopraamcontracten.

## <a name="see-also"></a>Zie ook  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
