---
title: Vooruitbetalingen corrigeren | Microsoft Docs
description: Nadat u een vooruitbetalingsfactuur voor de order hebt geboekt, kunt u een correctie aanbrengen op een order. U kunt nieuwe regels toevoegen aan een order na het verzenden van een vooruitbetaling en vervolgens kunt u een andere vooruitbetalingsfactuur boeken, maar u kunt een regel niet uit een order verwijderen nadat een vooruitbetaling voor de regel is gefactureerd.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0934cfedb7fa2e387e7d1bdcfbabb3ad45b2133e
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882746"
---
# <a name="correct-prepayments"></a>Vooruitbetalingen storneren
Nadat u een vooruitbetalingsfactuur voor de order hebt geboekt, kunt u een correctie aanbrengen op een order. U kunt nieuwe regels toevoegen aan een order na het verzenden van een vooruitbetaling en vervolgens kunt u een andere vooruitbetalingsfactuur boeken, maar u kunt een regel niet uit een order verwijderen nadat een vooruitbetaling voor de regel is gefactureerd.  

## <a name="to-correct-a-prepayment"></a>Een vooruitbetalingen storneren
De volgende procedure toont hoe u een vooruitbetalingscreditnota verzendt om alle gefactureerde vooruitbetalingen voor een verkooporder te annuleren.  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.  
2. Open de betreffende verkooporder.
3. Kies de actie **Vooruitbetaling** en kies vervolgens de actie **Vooruitbetalingscreditnota boeken** of **Vooruitbetalingscreditnota boeken en afdrukken**.  
4. Corrigeer op de pagina **Verkoopcreditnota** de relevante posten, zoals voor elke verkoopcreditnota. Zie [Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.     

    > [!NOTE]  
    > Als u het bedrag in het veld **Regelbedrag** wilt verminderen, moet u eerst het vooruitbetalingspercentage op de regel verhogen zodat de waarde in het veld **Regelbedrag vooruitbetaling** niet tot onder de waarde in het veld **Gefactureerde vooruitbetaling** wordt verlaagd.

5. Als u een vooruitbetalingsfactuur wilt maken voor nieuwe regels in de verkoopcreditnota, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Vooruitbetalingsfactuur boeken** of **Vooruitbetalingsfactuur boeken en afdrukken**.  
6. Als u een extra vooruitbetalingsfactuur wilt verzenden, verhoogt u het vooruitbetalingsbedrag op een of meer regels en past u de vooruitbetalingsfactuur aan. Er wordt een nieuwe factuur gemaakt voor het verschil tussen de tot nu toe gefactureerde vooruitbetalingsbedragen en de nieuwe vooruitbetalingsbedragen.  

## <a name="see-also"></a>Zie ook  
[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Procedure: Vooruitbetalingen verkoop instellen en factureren](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
