---
title: 'Procedure: Bankfondsen overboeken| Microsoft Docs'
description: 'Procedure: Bankfondsen overboeken'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 03/32/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e2e3642d08428367fac1dd5845013e14627fe6ed
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-bank-funds"></a>Procedure: Bankfondsen overboeken
Soms moet u een transfer van een bedrag van de ene naar de andere bankrekening boeken. Als u dit wilt doen, moet u een transactie boeken in het dagboek. De taak verschilt afhankelijk van of de bankrekeningen dezelfde valuta gebruiken of niet.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Een transfer boeken tussen bankrekeningen met dezelfde valutacode
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Diversendagboek** in en kies vervolgens de gerelateerde koppeling.
2. Vul op een dagboekregel de velden **Boekingsdatum** en **Documentnr.** in.
3. Selecteer in het veld **Rekeningsoort** de optie **Bankrekening**.
4. Selecteer in het veld **Rekeningnr.** de bank waarvan u de fondsen wilt overbrengen.
5. Voer in het veld **Bedrag** het bedrag in dat u wilt overbrengen.
6. Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.
7. Selecteer in het veld **Tegenrekeningtype** de bankrekening waarvan u de fondsen wilt overbrengen.
8. Boek het dagboek.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Transfers boeken tussen bankrekeningen met verschillende valutacodes
Als u gelden wilt overbrengen tussen bankrekeningen die verschillende valuta's gebruiken, moet u twee dagboekregels boeken.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Diversendagboek** in en kies vervolgens de gerelateerde koppeling.
2. Maak twee dagboekregels en vul de **Boekingsdatum** en **Documentnr.** in.
3. Selecteer op de eerste dagboekregel **Bankrekening** in het veld **Soort**.
4. Selecteer in het veld **Rekeningnr.** selecteer de bankrekening waarvan u de fondsen wilt overbrengen.
5. Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in. Voer creditbedragen met een minteken in. Voer debetbedragen zonder een minteken in.
6. Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.
7. Selecteer in het veld **Tegenrekeningtype** de bankrekening waarvan u de fondsen wilt overbrengen.
8. Selecteer op de tweede dagboekregel **Bankrekening** in het veld **Soort**.
9. Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.
10. Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in. Voer creditbedragen met een minteken in. Voer debetbedragen zonder een minteken in.
11. Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.  
12. Selecteer in het veld **Tegenrekeningtype** selecteer de bankrekening waarvan u de fondsen wilt overbrengen.

    **Opmerking**: als de gebruikte wisselkoersen in het dagboek verschillen van de wisselkoersen in het venster **Valutawisselkoersen**, voert u een derde regel in voor de wisselkoerswinsten of -verliezen. Geef **Grootboekrekening** op in het veld **Rekeningsoort**. Voer in het veld **Rekeningnr.** het grootboekrekeningnummer voor wisselkoerswinst of -verlies in. Voer de wisselkoerswinst of - verlies in het veld **Bedrag** in met of zonder een minteken voor respectievelijk debet- en creditbedragen.
13. Boek het dagboek.

## <a name="see-also"></a>Zie ook
[Bankrekeningen beheren](bank-manage-bank-accounts.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

