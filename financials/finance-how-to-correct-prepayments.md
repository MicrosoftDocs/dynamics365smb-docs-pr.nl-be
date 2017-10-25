---
title: Vooruitbetalingen corrigeren | Microsoft Docs
description: Nadat u een vooruitbetalingsfactuur voor de order hebt geboekt, kunt u een correctie aanbrengen op een order. U kunt nieuwe regels toevoegen aan een order na het verzenden van een vooruitbetaling en vervolgens kunt u een andere vooruitbetalingsfactuur boeken, maar u kunt een regel niet uit een order verwijderen nadat een vooruitbetaling voor de regel is gefactureerd.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b51fba1ee8c9a040836ac24c51f39a036f3c0e23
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-prepayments"></a>Procedure: Vooruitbetalingen storneren
Nadat u een vooruitbetalingsfactuur voor de order hebt geboekt, kunt u een correctie aanbrengen op een order. U kunt nieuwe regels toevoegen aan een order na het verzenden van een vooruitbetaling en vervolgens kunt u een andere vooruitbetalingsfactuur boeken, maar u kunt een regel niet uit een order verwijderen nadat een vooruitbetaling voor de regel is gefactureerd.  

## <a name="to-correct-a-prepayment"></a>Een vooruitbetalingen storneren
De volgende procedure toont hoe u een vooruitbetalingscreditnota verzendt om alle gefactureerde vooruitbetalingen voor een verkooporder te annuleren.  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.  
2. Open de betreffende verkooporder.
3. Kies de actie **Vooruitbetaling** en kies vervolgens de actie **Vooruitbetalingscreditnota boeken** of **Vooruitbetalingscreditnota boeken en afdrukken**.  
4. Corrigeer in het venster **Verkoopcreditnota** de relevante posten, zoals voor elke verkoopcreditnota. Zie [Procedure: Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.     

    > [!NOTE]  
    > Als u het bedrag in het veld **Regelbedrag** wilt verminderen, moet u eerst het vooruitbetalingspercentage op de regel verhogen zodat de waarde in het veld **Regelbedrag vooruitbetaling** niet tot onder de waarde in het veld **Gefactureerde vooruitbetaling** wordt verlaagd.

5. Als u een vooruitbetalingsfactuur wilt maken voor nieuwe regels in de verkoopcreditnota, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Vooruitbetalingsfactuur boeken** of **Vooruitbetalingsfactuur boeken en afdrukken**.  
6. Als u een extra vooruitbetalingsfactuur wilt verzenden, verhoogt u het vooruitbetalingsbedrag op een of meer regels en past u de vooruitbetalingsfactuur aan. Er wordt een nieuwe factuur gemaakt voor het verschil tussen de tot nu toe gefactureerde vooruitbetalingsbedragen en de nieuwe vooruitbetalingsbedragen.  

## <a name="see-also"></a>Zie ook  
[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Procedure: Vooruitbetalingen verkoop instellen en factureren](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

