---
title: Werkelijke bedragen analyseren in vergelijking met budgetbedragen
description: In dit onderwerp wordt beschreven hoe u werkelijke bedragen kunt analyseren ten opzichte van gebudgetteerde bedragen om uw bedrijfsgegevens te verzamelen, analyseren en delen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 120, 121, 422
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: df267dab7bc0d292bcd90a3e8b1063a5e87e7e61
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335096"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Werkelijke bedragen analyseren in vergelijking met budgetbedragen
Als onderdeel van het verzamelen, analyseren en delen van uw bedrijfsgegevens bekijkt u werkelijke bedragen in vergelijking met gebudgetteerde bedragen voor alle rekeningen en voor meerdere perioden.

Als u gebudgetteerde bedragen wilt analyseren, moet u eerst grootboekbudgetten maken. Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.

## <a name="to-view-a-gl-budget"></a>Grootboekbudget bekijken
In een begroting met dimensies kunt u de posten filteren en zo bepaalde begrotingen bekijken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekbudgetten** in en kies vervolgens de gerelateerde koppeling.
2. Open het budget dat u wilt weergeven op de pagina **Grootboekbudgetten**.  
3. Vul boven aan de pagina de benodigde velden in om te definiëren wat wordt weergegeven. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Als u **Periode** hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven**, moet u het veld **Weergeven per** invullen. Als u **Periode** niet hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven** voert u de juiste periode in het veld **Datumfilter** in.  

> [!NOTE]  
>   Alleen posten uit de grootboekbegroting met de filtercodes die u op het sneltabblad **Filters** hebt ingevoerd, worden in de berekening opgenomen. Budgetposten met andere filtercodes of zonder filtercodes worden niet opgenomen. Zolang het filter op de pagina is ingesteld, worden in het budget alleen de budgetposten met deze filtercodes weergegeven.  

> [!TIP]  
>   Als u de begroting wilt aanpassen, kunt u de begrotingsposten aanpassen. Kies een bedrag om de onderliggende grootboekbudgetposten weer te geven.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Werkelijke en gebudgetteerde bedragen bekijken voor de rekeningen  
U kunt grootboekbudgetten bekijken en ze vergelijken met werkelijke cijfers in verschillende onderdelen van [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Kies op de pagina **Rekeningschema** de actie **Saldo/Budget (Grootboek)**.
3. Vul boven aan de pagina de benodigde velden in om te definiëren wat wordt weergegeven.  
4. Als u een specificatie wilt bekijken die deel uitmaakt van een weergegeven bedrag, moet u het veld kiezen.  

> [!NOTE]  
>   De filters die u instelt in de paginakop, worden toegepast op grootboekposten en budgetposten.

Het rekeningschema wordt weergegeven in de kolommen aan de linkerzijde. In de eerste vier van de vijf kolommen aan de rechterzijde worden de werkelijke en gebudgetteerde debet- en creditbedragen voor elke rekening weergegeven. De vijfde kolom geeft de verhouding weer tussen de werkelijke en gebudgetteerde bedragen op de grootboekrekening.  

> [!TIP]  
>   Met het veld **Weergeven per** op de pagina **Saldo/Budget (Grootboek)** kunt u de periodelengte selecteren. Gebruik het veld **Weergeven als** om te selecteren hoe bedragen worden berekend, **Mutatie** of **Saldo t/m datum**. Kies de actie **Vorige periode** of **Volgende periode** om de periode te wijzigen.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Werkelijke en gebudgetteerde bedragen bekijken voor verschillende perioden  
In plaats van de werkelijke en de gebudgetteerde bedragen in een bepaalde periode te bekijken voor alle rekeningen, kunt u een aantal perioden voor een afzonderlijke rekening bekijken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Selecteer op de pagina **Rekeningschema** de betreffende grootboekrekening en kies de actie **Rekeningsaldo/Budget**.  
3. Vul boven aan de pagina de benodigde velden in om te definiëren wat wordt weergegeven.   
4. Als u een specificatie voor een weergegeven bedrag wilt bekijken, moet u het veld kiezen.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Werken met rekeningschema's](bi-how-work-account-schedule.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]