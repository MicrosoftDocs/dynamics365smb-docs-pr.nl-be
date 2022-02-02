---
title: Ontvangsten combineren op één factuur
description: Als u meer dan één inkoopontvangst tegelijk wilt factureren, kunt u de functie Ontvangsten combineren gebruiken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 136, 145, 146
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f9a9307ed6774064262f5d0e0fcf57027be3794d
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953278"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Ontvangsten combineren op één factuur

Als u meer dan één inkoopontvangst tegelijk wilt factureren, kunt u de functie **Ontvangsten combineren** gebruiken.  

Een gecombineerde inkoopontvangst kan pas worden gemaakt wanneer meer inkoopontvangsten van dezelfde leverancier in dezelfde valuta zijn geboekt. U moet dus twee of meer inkooporders hebben ingevuld en deze hebben geboekt als ontvangen, maar niet als gefactureerd.  

Wanneer inkoopontvangsten zijn gecombineerd op een factuur en zijn geboekt, wordt een geboekte inkoopfactuur gemaakt voor de gefactureerde regels. Het veld **Gefactureerd aantal** op de oorspronkelijke inkooporder of het oorspronkelijke inkoopraamcontract wordt bijgewerkt op basis van het gefactureerde aantal. Dit oorspronkelijke inkoopdocument wordt echter niet verwijderd, zelfs als dit volledig is ontvangen en gefactureerd en daarom moet u het inkoopdocument zelf verwijderen.  

> [!NOTE]
> De resulterende inkoopfactuur kan later niet worden gecorrigeerd of geannuleerd. Als u een inkoopfactuur wilt wijzigen die op deze manier is gemaakt, moet u inkoopcreditnota's gebruiken. Zie voor meer informatie [Onbetaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>Ontvangsten combineren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).  
3. Op het sneltabblad **Regels** selecteert u de actie **Ontvangstregels ophalen**.  
4. Selecteer meerdere ontvangstregels die u wilt opnemen in de factuur.  

    Als een onjuiste ontvangstregel is geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de inkoopfactuur gewoon verwijderen en vervolgens de functie **Ontvangstregels ophalen** opnieuw gebruiken.  
5. Kies de actie **Boeken** om de factuur te boeken.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Open inkooporders verwijderen na gecombineerde ontvangstboeking

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gefactureerde inkooporders verwijderen** in en kies vervolgens de gerelateerde koppeling  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Kies de knop **OK**.  

U kunt de afzonderlijke orders ook handmatig verwijderen.

Herhaal stap 1 t/m 3 voor alle andere betrokken documenten, zoals inkoopraamcontracten.

## <a name="see-also"></a>Zie ook

[Inkoop](purchasing-manage-purchasing.md)  
[Niet-betaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]