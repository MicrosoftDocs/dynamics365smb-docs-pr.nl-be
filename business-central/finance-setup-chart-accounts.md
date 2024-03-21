---
title: Het rekeningschema instellen of wijzigen (bevat video)
description: Meer informatie over het instellen van uw rekeningschema (COA) om de grootboekrekeningen weer te geven die uw financiële gegevens bevatten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 12/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>De rekeningschema's instellen of wijzigen

Het rekeningschema (COA) bevat de grootboekrekeningen die uw financiële gegevens bevatten. [!INCLUDE[prod_short](includes/prod_short.md)] bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf. U kunt de standaardrekeningen echter wijzigen en u kunt nieuwe rekeningen toevoegen.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Rekeningen toevoegen of wijzigen

Vanuit het rekeningschema kunt u elke grootboekrekening openen en instellingen toevoegen of wijzigen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Desgewenst kunt u meerdere regels gebruiken voor de naam van een grootboekrekening. Kies op de pagina **Grootboekrekening** de groep **Rekening**, kies **Uitgebreide teksten** en vul vervolgens een of meer regels in met de accountnaam en gekopieerde tekst.  

Voor rekeningen van het rekeningsoort **Totaal** moet u het veld **Samentelling** invullen. Voor rekeningen met het soort **Eindtotaal** wordt dit veld automatisch ingevuld met de inspringfunctie. Nadat u alle accounts heeft ingesteld, kiest u de actie **Verwerken** en vervolgens **Rekeningschema inspringen**.  

> [!IMPORTANT]
> Als u vóór het uitvoeren van de inspringfunctie definities hebt ingevoerd in de velden **Samentelling** voor rekeningen van het type **Eindtotaal**, moet u deze daarna nogmaals invoeren, omdat de functie de waarden in alle **Eindtotaal**-velden overschrijft.

## <a name="delete-accounts"></a>Rekeningen verwijderen

U kunt een grootboekrekening verwijderen. Echter, voordat u deze verwijdert, moet het volgende waar zijn:  

* Het saldo op de rekening moet nul zijn.  
* Het veld **Grootboekrek.-verwijdering toestaan voor** moet zijn ingesteld op de pagina **Grootboekinstelling** en de rekening mag geen grootboekposten op of na die datum hebben.  
* Als het veld **Grootboekrek.-gebruik controleren** op de pagina **Grootboekinstellingen** is geselecteerd, mag de rekening niet worden gebruikt in boekingsgroepen of boekingsinstellingen.  

[!INCLUDE[prod_short](includes/prod_short.md)] voorkomt dat u een grootboekrekening verwijdert die gegevens bevat die nodig zijn in het rekeningschema.  

U kunt ook opgeven wanneer mensen rekeningen mogen verwijderen. Op de pagina **Grootboekinstellingen** werkt de schakelaar **Blok grootboekrekeningen verwijderen** samen met de datum in het veld **Verwijdering van grootboekrek. controleren na** om als extra validatie te fungeren. Als u de schakelaar **Blok grootboekrekeningen verwijderen** aanzet, kunt u geen grootboekrekeningen verwijderen die posten hebben na de datum in het veld **Verwijdering van grootboekrek. controleren na**. Om een dergelijke rekening te verwijderen moet iemand met toegang tot de pagina **Grootboekinstellingen** de schakelaar **Blok grootboekrekeningen verwijderen** uitzetten.  

Het veld **Blok grootboekrekeningen verwijderen** inschakelen is meestal een aanbevolen procedure, net als het instellen van de datum in het veld **Verwijdering van grootboekrek. controleren na**, bijvoorbeeld op de datum tot wanneer u financiële gegevens moet bewaren volgens de regelgeving.  

### <a name="video-guidance"></a>Videobegeleiding

In deze video ziet u hoe u kunt opgeven of en wanneer mensen grootboekrekeningen kunnen verwijderen.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## <a name="see-also"></a>Zie ook

[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Werken met dimensies](finance-dimensions.md)  
[Gegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Werken met financiële rapporten](bi-how-work-account-schedule.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Resultatenrekeningen sluiten in de Franse versie](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Resultatenrekeningen afdrukken in de Australische versie](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Resultatenrekeningen afdrukken in de Nieuw-Zeelandse versie](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Saldi op de resultatenrekening instellen en afsluiten in de Spaanse versie](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Het rekeningschema inspringen en valideren in de Spaanse versie](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
