---
title: Een boeking ongedaan maken door een tegenboeking te boeken
description: Als u een foutieve boeking in het dagboek hebt gemaakt, kunt u vervolgens de functie Transactie tegenboeken gebruiken om de boeking ongedaan te maken met de juiste audittrail.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 07/22/2021
ms.author: edupont
ms.openlocfilehash: c23dcaed561997b5c0f38b4cd5ad5631b8519706
ms.sourcegitcommit: e904da8dc45e41cdd1434111c15e2a9d9edd3fa2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/23/2021
ms.locfileid: "6660168"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken
Tegenjournaalboekingen worden niet alleen gebruikt voor het corrigeren van fouten, maar kunnen ook worden gebruikt om bijvoorbeeld een oude transitoriaboeking te wissen voordat een nieuwe wordt ingevoerd. U selecteert de post en maakt een tegenpost (posten die identiek zijn aan de oorspronkelijke post, maar met een tegenovergesteld teken in het bedragveld) met hetzelfde documentnummer en dezelfde boekingsdatum als de originele post. Nadat een post is tegengeboekt, moet u de juiste post maken.

U kunt alleen posten tegenboeken die zijn geboekt vanaf een algemene dagboekregel. Een post kan slechts één keer worden tegengeboekt.

Als u een boeking van een ontvangst of verzending ongedaan wilt maken voordat ze als gefactureerd worden geboekt, kunt u de functie **Ongedaan maken** in het geboekte document gebruiken. U kunt hoeveelheden van het type **Artikel** en **Resource** ongedaan maken.

Als u een onjuist negatief aantal hebt geboekt, dat wil zeggen, als u een inkooporder hebt gemaakt met bijvoorbeeld het verkeerde aantal artikelen en deze order hebt geboekt als ontvangen (maar niet gefactureerd), kunt u de boeking ongedaan maken.

Als u een onjuist positief aantal hebt geboekt, dat wil zeggen, als u een verkoopverzending of een inkoopretourzending hebt gemaakt met bijvoorbeeld het verkeerde aantal artikelen en deze hebt geboekt als verzonden (maar niet gefactureerd), kunt u de boeking ongedaan maken.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>De dagboekboeking van een grootboekpost tegenboeken
U kunt posten vanuit alle **Posten**-pagina's tegenboeken. De volgende procedure is gebaseerd op de pagina **Grootboekposten**.
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de post die u wilt tegenboeken en kies vervolgens de actie **Transactie tegenboeken**. Het moet afkomstig zijn uit een dagboekboeking.
3. Kies op de pagina **Transactieposten tegenboeken** de actie **Tegenboeken**.
4. Kies de knop **Ja** in het bevestigingsbericht.

> [!NOTE]
> U kunt geen posten tegenboeken die zijn ingevoerd met informatie uit een taak, of die winsten en verliezen hebben gerealiseerd binnen dezelfde transactie.

## <a name="to-post-a-negative-entry"></a>Een negatieve post boeken  
U kunt het veld **Storno** gebruiken om een negatief debetbedrag in plaats van een creditbedrag te boeken, of om een negatief creditbedrag in plaats van een debetbedrag op een rekening te boeken. Om aan juridische vereisten te voldoen is dit veld standaard zichtbaar in alle dagboeken. De velden **Debetbedrag** en **Creditbedrag** bevatten beide zowel de oorspronkelijke post als de gecorrigeerde post. Deze velden hebben geen invloed op het rekeningsaldo.  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling  
2.  Selecteer in het veld **Batchnaam** de juiste batchnaam.  
3.  Voer informatie in de relevante velden in.  
4.  Selecteer op de dagboekregel die u wilt activeren voor negatieve posten het selectievakje **Storno**.  
5.  Als u naar het dagboek wilt boeken, kiest u de actie **Boeken** en kiest u vervolgens de knop **Ja**.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Een aantalsboeking ongedaan maken op een geboekte inkoopontvangst  
Hieronder wordt beschreven hoe u een geboekte ontvangst van artikelen of resources ongedaan kunt maken. De stappen zijn vergelijkbaar met de stappen voor geboekte verzendingen.

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte inkoopontvangsten** in en kies vervolgens de gerelateerde koppeling  
2.  Open de geboekte ontvangst die u ongedaan wilt maken.  
3.  Selecteer de regel(s) die u ongedaan wilt maken.  
4.  Kies de actie **Ontvangst ongedaan maken**.

Er wordt een correctieregel ingevoegd onder de geselecteerde ontvangstregel. Als de hoeveelheid in een magazijnontvangst is ontvangen, wordt een correctieregel ingevoegd op de geboekte magazijnontvangst.  

De velden **Ontvangen aantal** en **Niet geboekt aantal** op de bijbehorende inkooporder worden ingesteld op nul.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Een aantalboeking ongedaan maken en opnieuw uitvoeren voor een geboekte retourzending
Hieronder wordt beschreven hoe u een geboekte retourzending van artikelen of resources ongedaan kunt maken en vervolgens de inkoopretour opnieuw kunt boeken met een nieuwe hoeveelheid. De stappen zijn vergelijkbaar met de stappen voor geboekte ontvangsten.

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte retourverzendingen** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de geboekte retourzending die u ongedaan wilt maken.
3. Selecteer de regel(s) die u ongedaan wilt maken.  

4.  Kies de actie **Retourverzending ongedaan maken**.  

    In het geboekte document wordt een gecorrigeerde regel ingevoegd. Op de retourorder worden de velden **Retouraantal verzonden** en **Retourverzending niet gefact.** ingesteld op nul.  

    Ga nu terug naar de inkoopretourorder om opnieuw te boeken.  

5.  Let op de pagina **Geboekte retourverzending** op het nummer in het **Retourordernr.** toevoegen.  
6.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopretourorders** in en selecteer vervolgens de gerelateerde koppeling.  
7.  Open de retourorder en kies de actie **Opnieuw openen**.  
8.  Corrigeer de post in het veld **Aantal** en boek de inkoopretourorder opnieuw.  

## <a name="see-also"></a>Zie ook
[Boeken van assemblage ongedaan maken](assembly-how-to-undo-assembly-posting.md)  
[Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]