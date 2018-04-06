---
title: SEPA-betalingen activeren
description: Als u leveranciersbetalingen elektronisch wilt verzenden in de betalingsindeling SEPA (Single Euro Payments Area) ISO 20022, moet u eerst de vereiste instellingen aanbrengen voor het activeren van SEPA-betalingen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9d87cea4036d86ca418bc3e9ac0c042cee3eca74
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

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
3.  Selecteer in het veld **Land-/regiocode** van het sneltabblad **Algemeen** de gewenste code.  

    > [!NOTE]  
    >  De opgegeven land-/regiocode moet zijn geactiveerd voor SEPA, zoals is beschreven in de vorige procedure.  

4.  Geef een waarde op in het veld **Minimumsaldo**.  
5.  Geef in het veld **SWIFT-code** van het sneltabblad **Transfer** een code op.  
6.  Kies de knop **OK**.  

## <a name="to-set-up-vendor-bank-accounts-for-sepa"></a>Bankrekeningen van leveranciers instellen voor SEPA  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de betreffende leverancier en kies vervolgens de actie **Bankrekeningen**.  
3.  Selecteer de bankrekening van een leverancier die u wilt instellen voor SEPA, en kies vervolgens **Bewerken**.  
4.  Geef in de velden **IBAN** en **SWIFT-code** van het sneltabblad **Transfer** de internationale bankidentificatiecode op van de bank waarbij de leverancier de rekening heeft.  
5.  Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
 [SEPA-betalingen](sepa-payments.md)   
 [SEPA-betalingen indienen](how-to-file-sepa-payments.md)   
 [SEPA-betalingen in andere valuta's dan de euro indienen](how-to-file-non-euro-sepa-payments.md)   
 [Exportprotocollen instellen](how-to-set-up-export-protocols.md)

