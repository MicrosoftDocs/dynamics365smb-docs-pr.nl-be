---
title: Een dagboekboeking ongedaan maken door een tegenboeking te boeken| Microsoft Docs
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
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reverse-journal-posting"></a>Procedure: Dagboekboeking tegenboeken
Om een foutieve dagboekpost ongedaan te maken, selecteert en maakt u een tegenboeking (posten die identiek zijn aan de oorspronkelijke post, maar met een tegenovergesteld teken in het bedragveld) met hetzelfde documentnummer en dezelfde boekingsdatum als de originele post. Nadat een post is tegengeboekt, moet u de juiste post maken.

U kunt alleen posten tegenboeken die zijn geboekt vanaf een algemene dagboekregel. Een post kan slechts één keer worden tegengeboekt.

Voor meer informatie over het boeken vanuit een dagboek zie [Procedure: Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)

U kunt posten vanuit alle **Posten**-vensters tegenboeken. De volgende procedure is gebaseerd op het venster **Grootboekposten**.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>De dagboekboeking van een grootboekpost tegenboeken
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de post die u wilt tegenboeken en kies vervolgens de actie **Transactie tegenboeken**. Het moet afkomstig zijn uit een dagboekboeking.
3. Selecteer in het venster **Transactieposten tegenboeken** de relevante post en kies de actie **Tegenboeken**.
4. Kies de knop **Ja** in het bevestigingsbericht.

## <a name="see-also"></a>Zie ook
[Procedure: Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

