---
title: Werkelijk versus budget analyseren| Microsoft Docs
description: Beschrijft hoe u werkelijke bedragen analyseert in vergelijking met budgetbedragen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 17a6368e5a25ad12db05825b863ce29cd329cd39
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Werkelijke bedragen analyseren in vergelijking met budgetbedragen
Als onderdeel van het verzamelen, analyseren en delen van uw bedrijfsgegevens bekijkt u werkelijke bedragen in vergelijking met gebudgetteerde bedragen voor alle rekeningen en voor meerdere perioden.

Als u gebudgetteerde bedragen wilt analyseren, moet u eerst grootboekbudgetten maken. Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.

## <a name="to-view-a-gl-budget"></a>Grootboekbudget bekijken
In een begroting met dimensies kunt u de posten filteren en zo bepaalde begrotingen bekijken.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekbudgetten** in en kies vervolgens de gerelateerde koppeling.
2. Open het budget dat u wilt weergeven in het venster **Grootboekbudgetten**.  
3. Vul boven in het venster de benodigde velden in om te definiëren wat wordt weergegeven. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Als u **Periode** hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven**, moet u het veld **Weergeven per** invullen. Als u **Periode** niet hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven** voert u de juiste periode in het veld **Datumfilter** in.  

> [!NOTE]  
>   Alleen posten uit de grootboekbegroting met de filtercodes die u op het sneltabblad **Filters** hebt ingevoerd, worden in de berekening opgenomen. Budgetposten met andere filtercodes of zonder filtercodes worden niet opgenomen. Zolang het filter in het venster is ingesteld, worden in het budget alleen de budgetposten met deze filtercodes weergegeven.  

> [!TIP]  
>   Als u de begroting wilt aanpassen, kunt u de begrotingsposten aanpassen. Kies een bedrag om de onderliggende grootboekbudgetposten weer te geven.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Werkelijke en gebudgetteerde bedragen bekijken voor de rekeningen  
U kunt grootboekbudgetten bekijken en ze vergelijken met werkelijke cijfers in verschillende onderdelen van [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in het venster **Rekeningschema** de actie **Saldo/Budget (Grootboek)**.
3. Vul boven in het venster de benodigde velden in om te definiëren wat wordt weergegeven.  
4. Als u een specificatie wilt bekijken die deel uitmaakt van een weergegeven bedrag, moet u het veld kiezen.  

> [!NOTE]  
>   De filters die u instelt op de vensterkop, worden toegepast op grootboekposten en budgetposten.

Het rekeningschema wordt weergegeven in de kolommen aan de linkerzijde. In de eerste vier van de vijf kolommen aan de rechterzijde worden de werkelijke en gebudgetteerde debet- en creditbedragen voor elke rekening weergegeven. De vijfde kolom geeft de verhouding weer tussen de werkelijke en gebudgetteerde bedragen op de grootboekrekening.  

> [!TIP]  
>   Met het veld **Weergeven per** in het venster **Saldo/Budget (Grootboek)** kunt u de periodelenge selecteren. Gebruik het veld **Weergeven als** om te selecteren hoe bedragen worden berekend, **Mutatie** of **Saldo t/m datum**. Kies de actie **Vorige periode** of **Volgende periode** om de periode te wijzigen.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Werkelijke en gebudgetteerde bedragen bekijken voor verschillende perioden  
In plaats van de werkelijke en de gebudgetteerde bedragen in een bepaalde periode te bekijken voor alle rekeningen, kunt u een aantal perioden voor een afzonderlijke rekening bekijken.  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer in het venster **Rekeningschema** de betreffende grootboekrekening en kies de actie **Rekeningsaldo/Budget**.  
3. Vul boven in het venster de benodigde velden in om te definiëren wat wordt weergegeven.   
4. Als u een specificatie voor een weergegeven bedrag wilt bekijken, moet u het veld kiezen.  

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Werken met rekeningschema's](bi-how-work-account-schedule.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

