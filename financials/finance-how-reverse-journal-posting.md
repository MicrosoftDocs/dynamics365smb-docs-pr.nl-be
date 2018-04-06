---
title: Een boeking ongedaan maken door een tegenboeking te boeken| Microsoft Docs
description: Als u een foutieve boeking in het dagboek hebt gemaakt, kunt u vervolgens de functie Transactie tegenboeken gebruiken om de boeking ongedaan te maken met de juiste audittrail.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 66fcd6282f02d5789b12b79467ec177817422c5c
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-postings"></a>Boekingen tegenboeken
Om een foutieve dagboekpost ongedaan te maken, selecteert en maakt u een tegenboeking (posten die identiek zijn aan de oorspronkelijke post, maar met een tegenovergesteld teken in het bedragveld) met hetzelfde documentnummer en dezelfde boekingsdatum als de originele post. Nadat een post is tegengeboekt, moet u de juiste post maken.

U kunt alleen posten tegenboeken die zijn geboekt vanaf een algemene dagboekregel. Een post kan slechts één keer worden tegengeboekt.

Voor meer informatie over het boeken vanuit een dagboek zie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)

Als u een onjuist negatief aantal hebt geboekt, dat wil zeggen, als u een inkooporder hebt gemaakt met bijvoorbeeld het verkeerde aantal artikelen en deze order hebt geboekt als ontvangen (maar niet gefactureerd), kunt u de boeking ongedaan maken.

Als u een onjuist positief aantal hebt geboekt, dat wil zeggen, als u een inkoopretourorder hebt gemaakt met bijvoorbeeld het verkeerde aantal artikelen en deze order hebt geboekt als verzonden (maar niet gefactureerd), kunt u de boeking ongedaan maken.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>De dagboekboeking van een grootboekpost tegenboeken
U kunt posten vanuit alle **Posten**-vensters tegenboeken. De volgende procedure is gebaseerd op het venster **Grootboekposten**.
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekposten** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de post die u wilt tegenboeken en kies vervolgens de actie **Transactie tegenboeken**. Het moet afkomstig zijn uit een dagboekboeking.
3. Selecteer in het venster **Transactieposten tegenboeken** de relevante post en kies de actie **Tegenboeken**.
4. Kies de knop **Ja** in het bevestigingsbericht.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Een aantalsboeking ongedaan maken op een geboekte inkoopontvangst  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Geboekte inkoopontvangsten** in en klik vervolgens op de gerelateerde koppeling.  
2.  Open de geboekte ontvangst die u ongedaan wilt maken.  
3.  Selecteer de regel(s) die u ongedaan wilt maken.  
4.  Kies de actie **Ontvangst ongedaan maken**.

    Er wordt een correctieregel ingevoegd onder de geselecteerde ontvangstregel.  

    Als de hoeveelheid in een magazijnontvangst is ontvangen, wordt een correctieregel ingevoegd in de geboekte magazijnontvangst.  

    De velden **Ontvangen aantal** en **Niet geboekt aantal** op de bijbehorende inkooporder worden ingesteld op nul.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Een aantalboeking ongedaan maken en opnieuw uitvoeren voor een geboekte retourzending

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Geboekte inkoopontvangsten** in en klik vervolgens op de gerelateerde koppeling.  
2.  Open de geboekte retourzending die u ongedaan wilt maken.
3. Selecteer de regel(s) die u ongedaan wilt maken.  

4.  Kies de actie **Retourverzending ongedaan maken**.  

    In het geboekte document wordt een gecorrigeerde regel ingevoegd. Op de retourorder worden de velden **Retouraantal verzonden** en **Retourverzending niet gefact.** ingesteld op nul.  

    Ga nu terug naar de inkoopretourorder om opnieuw te boeken.  

5.  Let in het venster **Geboekte retourverzending** op het nummer in het **Retourordernr.** veld.  
6.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopretourorders** in en selecteer vervolgens de gerelateerde koppeling.  
7.  Open de retourorder en kies de actie **Opnieuw openen**.  
8.  Corrigeer de post in het veld **Aantal** en boek de inkoopretourorder opnieuw.  

## <a name="to-post-a-negative-entry"></a>Een negatieve post boeken  
U kunt het veld **Storno** gebruiken om een negatief debetbedrag in plaats van een creditbedrag te boeken, of om een negatief creditbedrag in plaats van een debetbedrag op een rekening te boeken. Om aan juridische vereisten te voldoen is dit veld standaard zichtbaar in alle dagboeken. De velden **Debetbedrag** en **Creditbedrag** bevatten beide zowel de oorspronkelijke post als de gecorrigeerde post. Deze velden hebben geen invloed op het rekeningsaldo.  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Dagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer in het veld **Batchnaam** de juiste batchnaam.  
3.  Voer informatie in de relevante velden in.  
4.  Selecteer op de dagboekregel die u wilt activeren voor negatieve posten het selectievakje **Storno**.  
5.  Als u naar het dagboek wilt boeken, kiest u de actie **Boeken** en kiest u vervolgens de knop **Ja**.

## <a name="see-also"></a>Zie ook
[Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

