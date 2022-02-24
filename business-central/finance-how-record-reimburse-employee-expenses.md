---
title: Bedrijfsgerelateerde onkosten vastleggen en terugbetalen | Microsoft Docs
description: Boek onkosten van werknemers met het dagboek naar de rekening van de werknemer en boek later een betaling naar de bankrekening van de werknemer om bedrijfgerelateerde onkosten terug te betalen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 5f943006997e4735d4ec224957442f23e2af1324
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184088"
---
# <a name="record-and-reimburse-employees-expenses"></a>Kosten van werknemers registreren en terugbetalen
[!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt transacties voor een werknemer op dezelfde manier als voor leveranciers. Daarom zijn er werknemersboekingsgroepen om te zorgen dat werknemersposten worden geboekt naar de relevante rekeningen in het grootboek.

> [!NOTE]  
> Werknemerstransacties kunnen alleen in de lokale valuta worden geboekt. Terugbetalingen aan werknemers ondersteunen geen kortingen en betalingstoleranties.

Als medewerkers hun eigen geld uitgeven tijdens zakelijke activiteiten, kunt u de kosten boeken naar de rekening van de werknemer. Vervolgens kunt u de werknemer terugbetalen door een betaling te doen naar de bankrekening van de werknemer, net zoals u leveranciers betaalt.

## <a name="to-record-an-employees-expense"></a>Onkosten van een werknemer registreren
U boekt onkosten van een werknemer op de pagina **Diversendagboek**.
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies de desbetreffende koppeling.
2. Open de relevante dagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul op een nieuwe dagboekregel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Herhaal stap 3 voor alle kosten die de werknemer heeft betaald.

    > [!TIP]  
    > Als u meerdere onkostenregels boven één tegenrekeningsregel wilt invoeren voor de bankrekening van de werknemer, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch op de pagina **Fin. dagboekbatches**. Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de onkosten in balans te brengen.
5. Kies de actie **Boeken** om de kosten op de rekening van de werknemer te registreren.

## <a name="to-reimburse-an-employee"></a>Een werknemer terugbetalen
U betaalt werknemers terug door betalingen te boeken naar hun bankrekening op de pagina **Betalingsdagboek**.
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies de gerelateerde koppeling.
2. Open de relevante betalingsdagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul indien nodig de velden in. Zie voor meer informatie [Betalingen doen](payables-make-payments.md).
4. Of kies de actie **Werknemersbetalingen voorstellen** om automatisch dagboekregels in te voegen voor werknemersterugbetalingen die in behandeling zijn.
5. Kies de actie **Boeken** om de terugbetaling te registreren.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Terugbetalingen reconciliëren met werknemersposten
U vereffent werknemersbetalingen met de gerelateerde open werknemersposten op dezelfde manier als u dat doet voor leveranciersbetalingen, bijvoorbeeld op de pagina **Betalingsreconciliatiedagboek**, op basis van de gerelateerde bankafschriftposten. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md). U kunt ook handmatig vereffenen op de pagina **Werknemerposten**. Zie voor meer informatie het gerelateerde [Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Zie ook
[Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
