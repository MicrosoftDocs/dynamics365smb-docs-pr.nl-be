---
title: Bankfondsen overboeken| Microsoft Docs
description: U kunt bedragen overbrengen van de ene naar de andere bankrekening, inclusief andere valuta's, door de transactie in het dagboek te boeken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 934124d419e19c1dc8180f11fcae748cd2afd15d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752367"
---
# <a name="transfer-bank-funds"></a>Bankfondsen overboeken
Soms moet u een bedrag van de ene naar de andere bankrekening overboeken in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u dit wilt doen, moet u een transactie boeken op de pagina **Dagboek**. De taak verschilt afhankelijk van of de bankrekeningen dezelfde valuta gebruiken of niet.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Een transfer boeken tussen bankrekeningen met dezelfde valutacode
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.
2. Vul op een dagboekregel de velden **Boekingsdatum** en **Documentnr.** in.
3. Selecteer in het veld **Rekeningsoort** de optie **Bankrekening**.
4. Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.
5. Voer in het veld **Bedrag** het bedrag in dat u wilt overbrengen.
6. Kies de actie **Meer kolommen weergeven** om alle beschikbare velden te bekijken.
7. Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.
8. Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.
9. Boek het dagboek.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Transfers boeken tussen bankrekeningen met verschillende valutacodes
Als u gelden wilt overbrengen tussen bankrekeningen die verschillende valuta's gebruiken, moet u twee dagboekregels boeken.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.
2. Maak twee dagboekregels en vul de velden **Boekingsdatum** en **Documentnr.** in.
3. Selecteer op de eerste dagboekregel **Bankrekening** in het veld **Soort**.
4. Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.
5. Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in. Voer creditbedragen met een minteken in. Voer debetbedragen zonder een minteken in.
6. Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.
7. Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.
8. Selecteer op de tweede dagboekregel **Bankrekening** in het veld **Soort**.
9. Selecteer in het veld **Rekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.
10. Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in. Voer creditbedragen met een minteken in. Voer debetbedragen zonder een minteken in.
11. Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.  
12. Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.

    > [!NOTE]  
    > Als de gebruikte wisselkoersen in het dagboek verschillen van de wisselkoersen op de pagina **Valutawisselkoersen**, voert u een derde regel in voor de wisselkoerswinsten of -verliezen. Geef **Grootboekrekening** op in het veld **Rekeningsoort**. Voer in het veld **Rekeningnr.** het grootboekrekeningnummer voor wisselkoerswinst of -verlies in. Voer de wisselkoerswinst of - verlies in het veld **Bedrag** in met of zonder een minteken voor respectievelijk debet- en creditbedragen.
13. Boek het dagboek.

## <a name="see-also"></a>Zie ook
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]