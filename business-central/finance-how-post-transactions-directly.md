---
title: Kosten of inkomsten rechtstreeks in grootboek registreren| Microsoft Docs
description: Voor zakelijke activiteiten die niet door een document worden vertegenwoordigd, zoals kleinere ontvangsten of kasontvangsten, kunt u de gerelateerde transacties maken door dagboekregels te boeken op de pagina Diversendagboek.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 54f2cf573d12c50ba26c26fd4c11ad20a1d52db3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241131"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a>Transacties direct naar het grootboek boeken

Met diversendagboeken kunt u financiële transacties direct naar grootboekrekeningen en andere rekeningen boeken, zoals bank-, klant-, leveranciers- en werknemersrekeningen.  

Een veelvoorkomend gebruik van het dagboek is uitgaven van werknemers van eigen geld tijdens zakelijke activiteiten te boeken, voor latere terugbetaling. Zie voor meer informatie [Uitgaven van werknemers vastleggen en terugbetalen](finance-how-record-reimburse-employee-expenses.md).

Dagboeken boeken financiële transacties direct naar grootboekrekeningen en andere rekeningen zoals bank-, klant-, leveranciers- en werknemersrekeningen. Door te boeken met een dagboek worden er altijd posten gemaakt in grootboekrekeningen. Dit geldt zelfs ook als u bijvoorbeeld een dagboekregel naar een klantrekening boekt, omdat een post via een boekingsgroep is geboekt naar een rekening met vorderingen in het grootboek. U kunt uw versie van een dagboek aanpassen door een dagboekbatch of -sjabloon in te stellen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.

In tegenstelling tot posten die zijn geboekt met documenten, die een creditnotaproces vereisen, kunt posten correct tegenboeken die met het diversendagboek zijn geboekt. Zie voor meer informatie [Boekingen tegenboeken](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Een transactie direct naar het grootboek boeken

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open de relevante dagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul op een nieuwe dagboekregel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Herhaal stap 3 voor alle afzonderlijke transacties die u wilt boeken.

    > [!TIP]  
    > Als u meerdere transactieregels boven één tegenrekeningsregel wilt invoeren, bijvoorbeeld, voor één bankrekening, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch op de pagina **Fin. dagboekbatches**. Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de transacties in balans te brengen.
5. Kies de actie **Boeken** om de transacties op de betreffende grootboekrekeningen te registreren.

## <a name="see-also"></a>Zie ook

[Werken met diversendagboeken](ui-work-general-journals.md)  
[Kosten van werknemers registreren en terugbetalen](finance-how-record-reimburse-employee-expenses.md)  
[Boekingen tegenboeken](finance-how-reverse-journal-posting.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
