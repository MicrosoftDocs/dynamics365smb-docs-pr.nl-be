---
title: Een rekeningschema instellen (bevat video)
description: Het rekeningschema bevat de grootboekrekeningen die uw financiële gegevens bevatten. U kunt de standaardrekeningen wijzigen in het rekeningschema en u kunt nieuwe rekeningen toevoegen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.search.form: 16, 17, 18, 118, 386, 391
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: f2ef4432d91d9f647a4bea58febbdfd5513a4350
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520294"
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>De rekeningschema's instellen of wijzigen

Het rekeningschema bevat de grootboekrekeningen die uw financiële gegevens bevatten. [!INCLUDE[prod_short](includes/prod_short.md)] bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.
Echter, kunt u de standaardrekeningen wijzigen en u kunt nieuwe rekeningen toevoegen.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Rekeningen toevoegen of wijzigen

Vanuit het rekeningschema kunt u elke grootboekrekening openen en instellingen toevoegen of wijzigen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Desgewenst kunt u meerdere regels gebruiken voor de naam van een grootboekrekening. Kies op de pagina **Grootboekrekening** de groep **Rekening**, kies **Uitgebreide teksten** en vul vervolgens een of meer regels in met de te kopiëren tekst en de accountnaam.  

Voor rekeningen van het rekeningsoort **Totaal** moet u het veld **Samentelling** invullen. Voor rekeningen met het soort **Eindtotaal** wordt dit veld automatisch ingevuld met de inspringfunctie. Nadat u alle accounts heeft ingesteld, kiest u de actie **Verwerken** en vervolgens **Rekeningschema inspringen**.  

> [!IMPORTANT]
> Als u vóór het uitvoeren van de inspringfunctie definities hebt ingevoerd in de velden **Samentelling** voor rekeningen van het type **Eindtotaal**, moet u deze daarna nogmaals invoeren, omdat de functie de waarden in alle **Eindtotaal**-velden overschrijft.

## <a name="delete-accounts"></a>Rekeningen verwijderen

U kunt een grootboekrekening verwijderen. Echter, voordat u deze verwijdert, moet het volgende waar zijn:  

* Het saldo op de rekening moet nul zijn.  
* Het veld **Grootboekrek.-verwijdering toestaan voor** moet zijn ingesteld op de pagina **Grootboekinstelling** en de rekening mag geen grootboekposten op of na die datum hebben.  
* Als het veld **Grootboekrek.-gebruik controleren** op de pagina **Grootboekinstellingen** is geselecteerd, mag de rekening niet worden gebruikt in boekingsgroepen of boekingsinstellingen.  

[!INCLUDE[prod_short](includes/prod_short.md)] voorkomt dat u een grootboekrekening verwijdert die gegevens bevat die nodig zijn in het rekeningschema.  

## <a name="block-deletion-of-gl-accounts"></a>Verwijderen van grootboekrekeningen blokkeren

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

In releasewave 2 van 2022 wordt een extra beveiliging tegen het per ongeluk verwijderen van grootboekrekeningen geïntroduceerd, zelfs in de scenario's waarin aan de criteria wordt voldaan.  

Een nieuw veld, **Blok grootboekrekeningen verwijderen**, wordt toegevoegd aan de pagina **Grootboekinstellingen**. Het veld fungeert als extra validatie wanneer een gebruiker probeert een rekening te verwijderen waarvan er grootboekboekingen zijn na de datum die is opgegeven in het veld **Verwijdering van grootboekrek. controleren na**.

Als het veld **Blok grootboekrekeningen verwijderen** is ingesteld op *Ja*, kunt u geen grootboekrekeningen verwijderen die posten hebben na de datum in het veld **Verwijdering van grootboekrek. controleren na**. Als een een gebruiker met toegang tot de pagina **Grootboekinstellingen** een dergelijke rekening wil verwijderen, moet hij of zij dit veld eerst instellen op *Nee*. Vervolgens kan de rekening worden verwijderd.  

We raden aan om het veld **Blok grootboekrekeningen verwijderen** in te stellen op *Ja*. We raden u ook aan om altijd een datum vast te leggen in het veld **Verwijdering van grootboekrek. controleren na**, zoals de tijd die u nodig hebt om uw financiële gegevens op te slaan.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Werken met dimensies](finance-dimensions.md)  
[Gegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Werken met rekeningschema's](bi-how-work-account-schedule.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Resultatenrekeningen sluiten in de Franse versie](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Resultatenrekeningen afdrukken in de Australische versie](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Resultatenrekeningen afdrukken in de Nieuw-Zeelandse versie](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Saldi op de resultatenrekening instellen en afsluiten in de Spaanse versie](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Het rekeningschema inspringen en valideren in de Spaanse versie](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]