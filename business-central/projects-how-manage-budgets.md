---
title: Een budget instellen en beheren voor een project
description: Beschrijft hoe u resources plant en de kosten van een project voorspelt en beheert door een budget voor elk project in te stellen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="manage-job-budgets"></a>Projectbudgetten maken

Voor elk project kunt u een budget instellen. Het budget wordt gebruikt om de resources te plannen die.u aan een project toewijst. Dit kan een algemeen budget zijn met weinig posten of een budget met veel posten die in activiteitsniveaus zijn onderverdeeld. U kunt vervolgens de gebudgetteerde bedragen vergelijken met het werkelijke gebruik zoals vastgelegd in het projectdagboek. Door verschillen tussen werkelijk en gebudgetteerd gebruik te controleren kunt u een lopend project controleren en de kwaliteit van toekomstige projecten verbeteren doordat kosten minder snel worden onderschat.

In de volgende procedure wordt beschreven hoe u gebudgetteerde kosten inschat tijdens een planning. Voor informatie over het vastleggen van gebudgetteerde versus werkelijke projectprijzen en -kosten raadpleegt u [Gebruik voor projecten vastleggen](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="JobBudgetCosts"></a>De gebudgetteerde kosten voor een project schatten
Wanneer een klant de prijs wil weten van een project dat op basis van gebruik wordt gefactureerd, moet u de gebudgetteerde kosten voor het project bepalen. U gebruikt hiervoor de pagina **Projecttaakregels**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Open een relevant project.
3. Selecteer een taakregel van het soort Boeking en kies vervolgens de actie **Projectplanningsregels**.
4. Vul op een nieuwe regel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Raadpleeg voor het veld **Regelsoort** de volgende informatie.  

| Regelsoort | Omschrijving |
| --- | --- |
| **Budget en factureerbaar** |De kosten en prijzen die zijn ingevoerd op de planningsregel, zijn de gebudgetteerde kosten voor de betreffende planningsregel. Het prijsbedrag wordt gefactureerd. |
| **Budget** |Er worden geen gebruikstoeslagen doorberekend aan de klant. Gebruik kan nooit worden overgebracht naar een factuur, maar wordt wel nog gebruikt bij de OHW-berekening. |
| **Factureerbaar** |Er worden gebruikstoeslagen doorberekend aan de klant. Het gebruik wordt naar de factuur overgebracht en wordt gebaseerd op het aantal dat is opgegeven in het veld Te factureren aantal. |

> [!NOTE]  
> Het veld **Geplande leverdatum** voor de planningsregel bevat de datum waarop gebruik dat gerelateerd is aan de planningsregel, naar verwachting is voltooid. Het is ook de datum waarop de planningsregel kan worden overgebracht naar een verkoopfactuur en geboekt. <br /><br /> Op de onderliggende projecttaak op de pagina **Project** bevatten de velden **Begindatum** en **Einddatum** respectievelijk de waarde van het veld **Geplande leverdatum** op de vroegste en laatste projectplanningsregels op de gerelateerde pagina **Projectplanningsregels**.

> [!NOTE]  
>   Wanneer u het veld **Aantal** invult, wordt alle informatie over de totale verkoopprijs en de totale kostprijs berekend en ingevuld voor die planningsregel. U kunt dit op elk gewenst moment wijzigen.

Op de pagina **Projectkaart** kunt u nu een overzicht zien van de totale gebudgetteerde kosten, gebudgetteerde prijs, factureerbare kosten en factureerbare prijs voor elke taak.

Voor informatie over het vastleggen van gebudgetteerde versus werkelijke projectprijzen en -kosten raadpleegt u [Gebruik voor projecten vastleggen](projects-how-record-job-usage.md).

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/set-up-job-planning-lines/)

## <a name="see-also"></a>Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
