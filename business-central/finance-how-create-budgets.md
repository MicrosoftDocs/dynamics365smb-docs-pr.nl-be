---
title: Grootboekbudgetten maken | Microsoft Docs
description: Hier wordt beschreven hoe u grootboekbudgetten maakt om verschillende financiële activiteiten te prognosticeren en dimensies toewijst voor bedrijfsinformatiedoeleinden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6018edd9d7d324c827c6c338ec700492b39bf56d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747028"
---
# <a name="create-gl-budgets"></a>Grootboekbudgetten maken
U kunt budgetten met aparte namen maken als u meerdere budgetten wilt gebruiken voor dezelfde perioden. Eerst stelt u de begrotingsnaam in en voert u de begrotingscijfers in. De begrotingsnaam wordt vervolgens opgenomen op alle begrotingsposten die u maakt.  

Wanneer u een budget maakt, kunt u vier dimensies voor elk budget opgeven. Deze budgetspecifieke dimensies worden budgetdimensies genoemd. U selecteert de budgetdimensies voor elk budget uit de ingestelde dimensies. Met budgetdimensies kunnen budgetfilters worden ingesteld en dimensiegegevens aan budgetposten worden toegevoegd. Zie voor meer informatie [Werken met dimensies](finance-dimensions.md).

Budgetten spelen een belangrijke rol in bedrijfsinformatie, zoals in financiële overzichten gebaseerd op rapportageschema's die budgetposten bevatten, of wanneer gebudgetteerde en werkelijke bedragen in het rekeningschema worden geanalyseerd. Zie voor meer informatie [Bedrijfsinformatie](bi.md).

In kostenadministratie werkt u met kostenbudgetten op een soortgelijke manier. Zie [Procedure: Kostenbudgetten maken](finance-create-cost-budgets.md) voor meer informatie.    

## <a name="to-create-a-new-gl-budget"></a>Een nieuw grootboekbudget maken  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekbudgetten** in en kies de desbetreffende koppeling.  
2. Kies de actie **Lijst bewerken** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Kies de actie **Budget bewerken**.
4. Vul boven aan de pagina **Budget** de benodigde velden in om te definiëren wat wordt weergegeven.  

    Alleen posten met de budgetnaam die u hebt ingevoerd in het veld **Budgetnaam** worden weergegeven. Aangezien de begrotingsnaam net is gemaakt, zijn er geen posten die overeenkomen met het filter. Daarom is de pagina leeg.  
5. Voer een bedrag in door op de betreffende cel in de matrix te klikken. De pagina **Grootboekbudgetposten** verschijnt.  
6. Maak een nieuwe regel en vul het veld **Bedrag** in. Sluit de pagina **Grootboekbudgetposten**.  
7. Herhaal stap 5 tot en met 6 totdat u alle budgetbedragen hebt ingevoerd.  

> [!NOTE]  
>  Op het sneltabblad **Filters** kunt u de budgetinformatie filteren op budgetdimensies die u hebt ingesteld onder de budgetnaam.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Grootboekbudgetten exporteren en importeren met Excel
Zoals bij vrijwel alle overige pagina's kunt u gegevens op budgetpagina's naar Excel exporteren voor verdere verwerking of analyse. Zie voor meer informatie [Uw bedrijfsgegevens exporteren naar Excel](about-export-data.md).

> [!NOTE]
> Het rekeningschema, waarop grootboekbudgetten zijn gebaseerd, bevat regels van het rekeningtype Kop die het totaal bevatten van de regels eronder. Wanneer u een grootboekbudget exporteert, worden gegevens op alle regels geëxporteerd, ongeacht het rekeningtype. Alleen gegevens van het rekeningtype Boeking kunnen echter terug worden geïmporteerd. Zodoende: <br /><br /> **Wanneer u een grootboekbudget importeert, worden eventuele waarden op kopregels verwijderd.** <br /><br /> Hierdoor worden verkeerde totalen voorkomen nadat gegevens zijn geïmporteerd die zijn gemaakt of bewerkt in Excel.<br /><br /> **Scenario**: u weet dat de nieuwe gebudgetteerde salarissenkosten LV 1.200.000 zullen zijn. U wilt de afdeling Salarissen laten budgetteren voor drie specifieke regels (van het rekeningtype Boeking) voor fulltime werknemers, parttime werknemers en invalkrachten. De drie regels worden gegroepeerd onder de kopregel Salarissen.<br /><br />U voert 1.200.000 op de kopregel in, exporteert het budget naar Excel en stuurt het vervolgens naar de afdeling Salarissen, waarbij u hen aangeeft de LV 1.200.000 te distribueren.<br /><br /> De afdeling Salarissen distribueert het bedrag over de drie boekingsrekeningen. Wanneer u terug importeert in het grootboekbudget, worden de drie rekeningen ingevuld met de nieuwe Excel-gegevens, tot een totaal van 1.200.000, en is de kopregel leeg.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)  
[Financiën](finance.md)  
[Bedrijfsinformatie](bi.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]