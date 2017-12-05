---
title: Bedrijfsgerelateerde onkosten vastleggen en terugbetalen | Microsoft Docs
description: Boek onkosten van werknemers met het dagboek naar de rekening van de werknemer en boek later een betaling naar de bankrekening van de werknemer om bedrijfgerelateerde onkosten terug te betalen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 0e10011c598678134cb7badbd9a3be97751b4424
ms.contentlocale: nl-be
ms.lasthandoff: 10/17/2017

---
# <a name="how-to-record-and-reimburse-employees-expenses"></a>Procedure: kosten van werknemers registreren en terugbetalen
[!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt transacties voor een werknemer op dezelfde manier als voor leveranciers. Daarom zijn er werknemersboekingsgroepen om te zorgen dat werknemersposten worden geboekt naar de relevante rekeningen in het grootboek.

> [!NOTE]  
> Werknemerstransacties kunnen alleen in de lokale valuta worden geboekt. Terugbetalingen aan werknemers ondersteunen geen kortingen en betalingstoleranties.

Als medewerkers hun eigen geld uitgeven tijdens zakelijke activiteiten, kunt u de kosten boeken naar de rekening van de werknemer. Vervolgens kunt u de werknemer terugbetalen door een betaling te doen naar de bankrekening van de werknemer, net zoals u leveranciers betaalt.

## <a name="to-record-an-employees-expense"></a>Onkosten van een werknemer registreren
U boekt onkosten van een werknemer in het venster **Diversendagboek**.
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Dagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Open de relevante dagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul op een nieuwe dagboekregel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Herhaal stap 3 voor alle kosten die de werknemer heeft betaald.

    > [!TIP]  
    > Als u meerdere onkostenregels boven één tegenrekeningsregel wilt invoeren voor de bankrekening van de werknemer, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch in het venster **Fin. dagboekbatches**. Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de onkosten in balans te brengen.
5. Kies de actie **Boeken** om de kosten op de rekening van de werknemer te registreren.

## <a name="to-reimburse-an-employee"></a>Een werknemer terugbetalen
U betaalt werknemers terug door betalingen te boeken naar hun bankrekening in het venster **Betalingsdagboek**.
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Open de relevante betalingsdagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul indien nodig de velden in. Zie voor meer informatie [Betalingen doen](payables-make-payments.md).
4. Of kies de actie **Werknemersbetalingen voorstellen** om automatisch dagboekregels in te voegen voor werknemersterugbetalingen die in behandeling zijn.
5. Kies de actie **Boeken** om de terugbetaling te registreren.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Terugbetalingen reconciliëren met werknemersposten
U vereffent werknemersbetalingen met de gerelateerde open werknemersposten op dezelfde manier als u dat doet voor leveranciersbetalingen, bijvoorbeeld in het venster **Betalingsreconciliatiedagboek**, op basis van de gerelateerde bankafschriftposten. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md). U kunt ook handmatig vereffenen in het venster **Werknemerposten**. Zie voor meer informatie de gerelateerde [Procedure: Leveranciersbetalingen handmatig reconciliëren](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Zie ook
[Procedure: Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Procedure: boekingen tegenboeken](finance-how-reverse-journal-posting.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

