---
title: "Procedure: Betalingen reconciliëren die niet automatisch kunnen worden vereffend | Microsoft Docs"
description: "Procedure: Betalingen reconciliëren die niet automatisch kunnen worden vereffend"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7b4c109ebda260ee86e2b955a17389b54493de65
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-payments-that-cannot-be-applied-automatically"></a>Procedure: Betalingen reconciliëren die niet automatisch kunnen worden vereffend
U moet soms betalingen op uw bankrekening verwerken die niet kunnen worden vereffend met een gerelateerde openstaande klant-, leveranciers- of bankrekeningpost. Redenen kunnen zijn dat er geen document bestaat in [!INCLUDE[d365fin](includes/d365fin_md.md)] waarmee de betaling kan worden vereffend of dat het gerelateerde document in [!INCLUDE[d365fin](includes/d365fin_md.md)] een ander bedrag dan het transactiebedrag heeft, bijvoorbeeld vanwege de valutawisselkoers. In het venster **Dagboek betalingsreconciliatie** worden alle transactiebedragen voor betalingen die nog niet zijn vereffend, weergegeven in het veld **Verschil**, inclusief bedragen die niet kunnen worden vereffend om redenen zoals de bovengenoemde.

Betalingen die niet kunnen worden vereffend, kunnen op de volgende verschillende manieren op de dagboekregels van de betalingsreconciliatie worden weergegeven:

* De waarde in het veld **Verschil** is gelijk aan de waarde in het veld **Transactiebedrag**, waarmee wordt aangegeven dat er geen gedeelte van de betaling kan worden vereffend met een gerelateerde openstaande klant-, leveranciers- of bankrekeningpost.
* De waarde in het veld **Verschil** is lager dan de waarde in het veld **Transactiebedrag**, waarmee wordt aangegeven dat een gedeelte van de betaling kan worden vereffend met een gerelateerde openstaande klant-, leveranciers- of bankrekeningpost. Het resterende deel van de betaling kan niet worden vereffend en moet handmatig worden gereconcilieerd of moet rechtstreeks naar een rekening worden geboekt.

Als u dergelijke betalingen wilt reconciliëren, kunt u de knop Verschil overboeken naar rekening kiezen en vervolgens opgeven naar welke rekening het bedrag in het veld Verschil wordt geboekt wanneer u het dagboek van de betalingsreconciliatie boekt.

**Opmerking**: er bestaat een vergelijkbare functionaliteit om automatische reconciliatie van terugkerende betalingen in te stellen die niet kunnen worden vereffend met gerelateerde openstaande klant-, leveranciers- of bankrekeningposten. Zie [Procedure: Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliëren](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) voor meer informatie.

## <a name="to-reconcile-payments-that-cannot-be-applied"></a>Betalingen reconciliëren die niet kunnen worden vereffend
1. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Betalingsreconciliatiedagboeken** in en klik op de gerelateerde koppeling.
2. Open een betalingreconciliatiedagboek. Zie voor meer informatie [Procedure: Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).
3. Kies **Verschil overboeken naar rekening**. Het venster **Verschil overboeken naar rekening** wordt geopend.
4. Geef in het veld **Rekeningsoort** het soort rekening op waarnaar het betalingsbedrag wordt geboekt.
5. Selecteer in het veld **Rekeningnr.** geeft u de rekening op waarnaar het betalingsbedrag wordt geboekt.
6. Geef in het veld **Omschrijving** de tekst op waarmee deze directe betalingsboeking wordt omschreven. Standaard wordt de tekst in het veld **Transactietekst** op de dagboekregel van de betalingsreconciliatie ingevoegd.
7. Kies de knop **Ok**.

Als de waarde in het veld **Verschil** gelijk is aan de waarde in het veld **Transactiebedrag** als u het dagboek van de betalingsreconciliatie boekt, wordt de volledige betaling op de dagboekregel rechtstreeks naar de opgegeven tegenrekening geboekt.

Als de waarde in het veld **Verschil** lager is dan de waarde in het **Transactiebedrag**, wordt een extra dagboekregel gemaakt met dezelfde tekst en datum en met het verschil ingevoegd in het veld **Transactiebedrag**. Op de oorspronkelijke dagboekregel wordt het verschil afgetrokken van de waarde van het veld **Transactiebedrag** en blijft de betaling vereffend met de gerelateerde klant-, leveranciers- of bankrekeningpost. Wanneer u het dagboek van de betalingsreconciliatie boekt, wordt één deel van de betaling als een vereffende betaling geboekt. Het andere gedeelte van de betaling wordt direct naar de opgegeven rekening geboekt.

## <a name="see-also"></a>Zie ook
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

