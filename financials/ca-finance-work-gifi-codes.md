---
title: GIFI-codes in Canada | Microsoft Docs
Description: In Canada kunt u instellen GIGI-codes (General Index of Financial Information) instellen en deze toewijzen aan boekingsgroepen
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-gifi-codes-in-canada"></a>Procedure: Met GIFI-codes werken in Canada
Fiscale gegevens kunnen grootboekrekeningen, rapporten, resultatenrekeningen, balansen en afschriften van ingehouden winst omvatten. Fiscale gegevens worden ingedeeld met behulp van codes. Het gebruik van codes kan de overheid helpen informatie te verwerken, elektronische aangifte voor te bereiden en elektronische belastinggegevens te valideren. Het gebruik van statistische codes helpt statistische organisaties ook efficiënter werken, aangezien de financiële gegevens beter beschikbaar zijn. Zie voor meer informatie de [website van de Canada Revenue Agency](http://www.cra-arc.gc.ca/).

Het Canada Revenue Agency gebruikt GIFI-codes (General Index of Financial Information) om financiële en belastinggegevens elektronisch te verzamelen, valideren en verwerken. Het is het beste GIFI-codes alleen toe te wijzen aan boekingsrekeningen, zodat alle totalisering wordt uitgevoerd door uw belastingvoorbereidingssoftware.

Wanneer een rekening aan een GIFI-code is gekoppeld, wordt deze onder die code aan het Revenue Agency aangegeven. Meerdere rekeningen kunnen alle dezelfde GIFI-code hebben, maar elke rekening kan slechts één GIFI-code hebben.

U kunt saldo-informatie exporteren per GIFI-code en het geëxporteerde bestand in Excel opslaan, wat handig is om informatie over te brengen naar uw belastingvoorbereidingssoftware.

## <a name="to-set-up-gifi-codes"></a>GIFI-codes instellen
In Dynamics NAV moet u GIFI-codes instellen voor grootboekrekeningen, rapporten, balansen, rapporten, inkomstenoverzichten en afschriften van ingehouden winsten.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **GIGI-codes** in en kies vervolgens de gerelateerde koppeling.
2. Kies in het venster **GIFI-codes** de actie **Nieuw**.
3. Stel GIFI-codes in door velden in te vullen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a>GIFI-codes koppelen aan grootboekrekeningen
Als u financiële gegevens wilt aangeven per GIFI-code, moet elke GIFI-code aan de juiste rekeningen worden gekoppeld in het rekeningschema.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een relevante grootboekrekening en kies vervolgens de actie **Bewerken**.
3. Selecteer op het sneltabblad **Kostprijsboekhouding** in het veld **GIFI-code** een geschikte GIFI-code.

## <a name="to-view-account-balances-using-the-gifi-code-report"></a>Rekeningsaldi weergeven met behulp van het rapport GIFI-code
U kunt uw rekeningsaldi per GIFI-code controleren met het rapport **Rekeningsaldi per GIFI-code**.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningsaldi per GIFI-code** in en kies vervolgens de gerelateerde koppeling.
2. Opgeven wat in de lijst moeten worden opgenomen door de velden te vullen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kies de knop **Afdrukken** of **Voorbeeld**.

## <a name="to-export-balance-information-using-gifi-codes"></a>Saldo-informatie exporteren met GIFI-codes
U kunt saldo-informatie exporteren met GIFI-codes en het geëxporteerde bestand opslaan in Excel. U kunt het bestand wijzigen, opslaan of verwijderen. U kunt het bestand gebruiken om gegevens over te brengen naar uw belastingvoorbereidingssoftware.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **GIFI-gegevens exporteren naar Excel** in en kies vervolgens de gerelateerde koppeling.
2. Geef op wat naar Excel moet worden geëxporteerd door de velden in te vullen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kies de knop **Ok**.

> [!NOTE]  
>   Het Excel-bestand heeft de volgende kenmerken:

* Het saldo wordt afgerond naar het dichtstbijzijnde percentage, maar de celwaarde behoudt hetzelfde percentage als in het grootboek.
* Negatieve getallen worden weergegeven als positieve getallen tussen haakjes. -123 wordt dus weergegeven als (123).

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)   
[Financiën instellen](finance-setup-finance.md)

