---
title: SEPA-betalingen activeren
description: Als u leveranciersbetalingen elektronisch wilt verzenden in de betalingsindeling SEPA (Single Euro Payments Area) ISO 20022, moet u eerst de vereiste instellingen aanbrengen voor het activeren van SEPA-betalingen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e7e1219c644e7115047af14c6550d41f7d613566
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300275"
---
# <a name="activate-sepa-payments"></a>SEPA-betalingen activeren
Als u leveranciersbetalingen elektronisch wilt verzenden in de betalingsindeling SEPA (Single Euro Payments Area) ISO 20022, moet u eerst de vereiste instellingen aanbrengen voor het activeren van SEPA-betalingen.  

In de volgende procedures wordt beschreven hoe u SEPA-betaling inschakelt en leveranciersbankrekeningen inschakelt.  

## <a name="to-enable-countriesregions-for-sepa"></a>Landen/regio's activeren voor SEPA  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Landen/regio's** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Lijst bewerken**.  
3.  Schakel het selectievakje **SEPA toegestaan** in voor elk land of elke regio dat/die u wilt activeren voor SEPA.  
4.  Kies de knop **OK**.  

## <a name="to-enable-bank-accounts-for-sepa"></a>Bankrekeningen activeren voor SEPA  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de bankrekening die u wilt activeren voor SEPA en kies vervolgens de actie **Bewerken**.  
3.  Kies de juiste redencode in het veld **Land-/regiocode**.  

    > [!NOTE]  
    >  De opgegeven land-/regiocode moet zijn geactiveerd voor SEPA, zoals is beschreven in de vorige procedure.  

4.  Geef een waarde op in het veld **Minimumsaldo**.  
5.  Voer in het veld **SWIFT-code** een code in.  
6.  Kies de knop **Ok**.  

## <a name="to-set-up-vendor-bank-accounts-for-sepa"></a>Bankrekeningen van leveranciers instellen voor SEPA  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de betreffende leverancier en kies vervolgens de actie **Bankrekeningen**.  
3.  Selecteer de bankrekening van de leverancier die u wilt instellen voor SEPA, en kies vervolgens de actie **Bewerken**.  
4.  Voer in de velden **IBAN** en **SWIFT-code** van het sneltabblad Transfer de internationale bankidentificatiecode in van de bank waarbij de leverancier de rekening heeft.  
5.  Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
 [SEPA-betalingen](sepa-payments.md)   
 [SEPA-betalingen indienen](how-to-file-sepa-payments.md)   
 [SEPA-betalingen in andere valuta's dan de euro indienen](how-to-file-non-euro-sepa-payments.md)   
 [Exportprotocollen instellen](how-to-set-up-export-protocols.md)
