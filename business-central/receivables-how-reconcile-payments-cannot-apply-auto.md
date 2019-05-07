---
title: De functie Verschil overboeken naar account gebruiken om betalingen te reconciliëren | Microsoft Docs
description: Beschrijft hoe u betalingen verwerkt die niet met een document kunnen worden vereffend, bijvoorbeeld wanneer een wisselkoers ertoe leidt dat bedragen verschillen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d96f46d7c0bd2b8a20294ff934ed645a76298e42
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "926641"
---
# <a name="reconcile-payments-that-cannot-be-applied-automatically"></a>Betalingen reconciliëren die niet automatisch kunnen worden vereffend
U moet soms betalingen op uw bankrekening verwerken die niet kunnen worden vereffend met een gerelateerde openstaande klant-, leveranciers- of bankrekeningpost. Redenen kunnen zijn dat er geen document bestaat in [!INCLUDE[d365fin](includes/d365fin_md.md)] waarmee de betaling kan worden vereffend of dat het gerelateerde document in [!INCLUDE[d365fin](includes/d365fin_md.md)] een ander bedrag dan het transactiebedrag heeft, bijvoorbeeld vanwege de valutawisselkoers. Op de pagina **Dagboek betalingsreconciliatie** worden alle transactiebedragen voor betalingen die nog niet zijn vereffend, weergegeven in het veld **Verschil**, inclusief bedragen die niet kunnen worden vereffend om redenen zoals de bovengenoemde.

Betalingen die niet kunnen worden vereffend, kunnen op de volgende verschillende manieren op de dagboekregels van de betalingsreconciliatie worden weergegeven:

* De waarde in het veld **Verschil** is gelijk aan de waarde in het veld **Transactiebedrag**, waarmee wordt aangegeven dat er geen gedeelte van de betaling kan worden vereffend met een gerelateerde openstaande klant-, leveranciers- of bankrekeningpost.
* De waarde in het veld **Verschil** is lager dan de waarde in het veld **Transactiebedrag**, waarmee wordt aangegeven dat een gedeelte van de betaling kan worden vereffend met een gerelateerde openstaande klant-, leveranciers- of bankrekeningpost. Het resterende deel van de betaling kan niet worden vereffend en moet handmatig worden gereconcilieerd of moet rechtstreeks naar een rekening worden geboekt.

Als u dergelijke betalingen wilt reconciliëren, kunt u de knop **Verschil overboeken naar rekening** kiezen en vervolgens opgeven naar welke rekening het bedrag in het veld **Verschil** wordt geboekt wanneer u het dagboek van de betalingsreconciliatie boekt.

> [!TIP]  
>   Er bestaat een vergelijkbare functionaliteit om automatische reconciliatie van terugkerende betalingen in te stellen die niet kunnen worden vereffend met gerelateerde openstaande klant-, leveranciers- of bankrekeningposten. Zie [Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliëren](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) voor meer informatie.

## <a name="to-reconcile-payments-that-cannot-be-applied-automatically"></a>Betalingen reconciliëren die niet automatisch kunnen worden vereffend
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsreconciliatiedagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open een betalingreconciliatiedagboek. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).
3. Kies **Verschil overboeken naar rekening**. De pagina **Verschil overboeken naar rekening** wordt geopend.
4. Geef in het veld **Rekeningsoort** het soort rekening op waarnaar het betalingsbedrag wordt geboekt.
5. Geef in het veld **Rekeningnr.** de rekening op waarnaar het betalingsbedrag wordt geboekt.
6. Geef in het veld **Omschrijving** de tekst op waarmee deze directe betalingsboeking wordt omschreven. Standaard wordt de tekst in het veld **Transactietekst** op de dagboekregel van de betalingsreconciliatie ingevoegd.
7. Kies de knop **Ok**.

Als de waarde in het veld **Verschil** gelijk is aan de waarde in het veld **Transactiebedrag** als u het dagboek van de betalingsreconciliatie boekt, wordt de volledige betaling op de dagboekregel rechtstreeks naar de opgegeven tegenrekening geboekt.

Als de waarde in het veld **Verschil** lager is dan de waarde in het **Transactiebedrag**, wordt een extra dagboekregel gemaakt met dezelfde tekst en datum en met het verschil ingevoegd in het veld **Transactiebedrag**. Op de oorspronkelijke dagboekregel wordt het verschil afgetrokken van de waarde van het veld **Transactiebedrag** en blijft de betaling vereffend met de gerelateerde klant-, leveranciers- of bankrekeningpost. Wanneer u het dagboek van de betalingsreconciliatie boekt, wordt één deel van de betaling als een vereffende betaling geboekt. Het andere gedeelte van de betaling wordt direct naar de opgegeven rekening geboekt.

## <a name="see-also"></a>Zie ook
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
