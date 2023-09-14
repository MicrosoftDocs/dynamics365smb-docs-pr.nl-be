---
title: Werkelijke bedragen analyseren in vergelijking met budgetbedragen
description: 'In dit artikel wordt beschreven hoe u werkelijke bedragen kunt analyseren ten opzichte van gebudgetteerde bedragen om uw bedrijfsgegevens te verzamelen, analyseren en delen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '120, 121, 422'
ms.date: 09/14/2022
ms.author: bholtorf
---
# Werkelijke bedragen analyseren in vergelijking met budgetbedragen

Als onderdeel van het verzamelen, analyseren en delen van uw bedrijfsgegevens bekijkt u werkelijke bedragen in vergelijking met gebudgetteerde bedragen voor alle rekeningen en voor meerdere perioden.

Als u gebudgetteerde bedragen wilt analyseren, moet u eerst grootboekbudgetten (GB) maken. Zie voor meer informatie [GB-budgetten maken](finance-how-create-budgets.md).

## Een grootboekbudget bekijken

In een begroting met dimensies kunt u de posten filteren en zo bepaalde begrotingen bekijken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekbudgetten** in en kies vervolgens de gerelateerde koppeling.
2. Open het budget dat u wilt weergeven op de pagina **Grootboekbudgetten**.  
3. Vul boven aan de pagina de benodigde velden in om te definiëren wat wordt weergegeven. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Als u **Periode** hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven**, moet u het veld **Weergeven per** invullen. Als u **Periode** niet hebt geselecteerd in een van de velden voert u de juiste periode in het veld **Datumfilter** in.  

> [!NOTE]  
> Alleen posten uit de grootboekbegroting met de filtercodes die u op het sneltabblad **Filters** hebt ingevoerd, worden in de berekening opgenomen. Budgetposten met andere filtercodes of zonder filtercodes worden niet opgenomen. Zolang het filter op de pagina is ingesteld, worden in het budget alleen posten met die filtercodes weergegeven.  

> [!TIP]  
> Gebruik de actie **Budget bewerken** om het budget te wijzigen. Kies op de pagina Budget een bedrag om de onderliggende grootboekbudgetposten weer te geven.

## Werkelijke en gebudgetteerde bedragen bekijken voor alle rekeningen

U kunt grootboekbudgetten bekijken en ze vergelijken met werkelijke cijfers in verschillende onderdelen van [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Kies op de pagina **Rekeningschema** de actie **Saldo/Budget (Grootboek)**.
3. Vul op het sneltabblad **Opties** de benodigde velden in om te definiëren wat in de tabel wordt weergegeven.  
4. Plaats de muisaanwijzer op een veld in de tabel om een korte beschrijving van het weergegeven bedrag te lezen.

> [!NOTE]  
> De filters die u instelt in de paginakop, worden toegepast op zowel grootboekposten als budgetposten.

Het rekeningschema wordt weergegeven in de kolommen aan de linkerzijde. In de eerste vier van de vijf kolommen aan de rechterzijde worden de werkelijke en gebudgetteerde debet- en creditbedragen voor elke rekening weergegeven. De vijfde kolom geeft de verhouding weer tussen de werkelijke en gebudgetteerde bedragen op de grootboekrekening.  

> [!TIP]  
> Met het veld **Weergeven per** op de pagina **Saldo/Budget (Grootboek)** kunt u de periodelengte selecteren. Gebruik het veld **Weergeven als** om te selecteren hoe bedragen worden berekend, **Mutatie** of **Saldo t/m datum**. Kies de actie **Vorige periode** of **Volgende periode** om de periode te wijzigen.  

## Werkelijke en gebudgetteerde bedragen bekijken voor verschillende perioden  

In plaats van de werkelijke en de gebudgetteerde bedragen in een bepaalde periode te bekijken voor alle rekeningen, kunt u een aantal perioden voor een afzonderlijke rekening bekijken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Selecteer op de pagina **Rekeningschema** de betreffende grootboekrekening en kies vervolgens de actie **Rekeningsaldo/Budget**.  
3. Vul op het sneltabblad **Opties** de benodigde velden in om te definiëren wat in de tabel wordt weergegeven.  
4. Ga op het sneltabblad **Regels** met de muisaanwijzer op een veld in de tabel staan om een korte beschrijving van het weergegeven bedrag te lezen.  

## Zie gerelateerde training op [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index).

## Zie ook

[Financiële bedrijfsinformatie](bi.md)  
[Werken met financiële rapporten](bi-how-work-account-schedule.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
