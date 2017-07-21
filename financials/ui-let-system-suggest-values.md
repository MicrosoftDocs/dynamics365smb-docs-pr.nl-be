---
title: Voorgestelde veldwaarden instellen | Microsoft Docs
description: Als u handmatige berekeningen wilt voorkomen en taken snel en accuraat wilt voltooien, kunt u automatische gegevensinvoer instellen, zodat Financials geselecteerde velden invult.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 99a76141f13efde3c7edb86037d6daaa0dbbb9d4
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="letting-dynamics-365-for-financials-suggest-values"></a>Dynamics 365 voor Financials waarden laten voorstellen
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan u helpen taken sneller en correcter te voltooien door velden vooraf te vullen of regels te vullen met gegevens die u anders zelf moet berekenen en invoeren. Hoewel dergelijke automatische gegevensinvoer altijd correct is, kunt u deze later wijzigen als u wilt.

De functionaliteit waarmee veldwaarden voor u worden ingevoerd, wordt meestal aangeboden voor taken waarin u grote volumes transactiegegevens invoert en fouten wilt voorkomen en tijd wilt besparen. Dit onderwerp bevat een selectie van deze functionaliteit. In toekomstige updates van [!INCLUDE[d365fin](includes/d365fin_md.md)] worden meer secties toegevoegd.

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>Het selectievakje **Salderingsbedrag voorstellen** in het venster **Fin. dagboekbatches**
Wanneer u bijvoorbeeld dagboekregels invoert voor meerdere uitgaven die allemaal naar dezelfde bankrekening moeten worden geboekt, kunt u telkens als u een nieuwe dagboekregel voor een uitgave invoert, het veld **Bedrag** op de bankrekeningregel automatisch laten bijwerken in het bedrag waarmee de uitgaven sluitend worden gemaakt. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie over het werken met diversendagboeken.

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Het veld **Bedrag** op salderingsdagboekregels automatisch laten invullen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Op de regel voor de dagboekbatch van uw voorkeur kiest u het selectievakje **Salderingsbedrag voorstellen**.
3. Open het dagboek en ga door met het registreren en boeken van transacties met de beschreven functie voor automatische invoer van een veldwaarde.       

Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie over het instellen van een persoonlijke dagboekbatch, bijvoorbeeld voor de verwerking van uitgaven.

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Het veld **Ontvangstdatum automatisch invullen** in het venster **Betalingsregistratie**
Het venster **Betalingsregistratie** bevat openstaande inkomende betalingen als regels die geboekte verkoopdocumenten vertegenwoordigen waar een betalingstermijn voor een bedrag is verstreken. Zie [Procedure: Klantbetalingen van een lijst met onbetaalde verkoopdocumenten handmatig reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) voor meer informatie over het vereffenen van klantbetalingen.

Uw hoofdacties in het venster bestaan eruit het selectievakje **Is betaald** en het veld **Ontvangen op** in te vullen. U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] zo instellen dat automatisch een werkdatum in het veld **Ontvangen op** wordt ingevoerd wanneer u het selectievakje **Is betaald** inschakelt.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Het veld **Ontvangen op** in het venster **Betalingsregistratie** automatisch laten invullen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen van betalingsregistratie** in en kies vervolgens de gerelateerde koppeling.
2. Schakel het selectievakje **Ontvangstdatum automatisch invullen** in.
3. Open het venster **Betalingregistratie** en ga door met het verwerken van inkomende klantbetalingen met de beschreven functie voor automatische invoer van een veldwaarde.

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Financiën](Finance.md)


