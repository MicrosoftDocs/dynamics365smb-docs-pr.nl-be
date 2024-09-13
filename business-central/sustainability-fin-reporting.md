---
title: Duurzaamheid financiële rapportage
description: Beschrijft hoe u financiële rapporten kunt gebruiken om verschillende weergaven en rapporten te maken voor het analyseren van gegevens over duurzaamheidsprestaties.
author: altotovi
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: '104, 108, 490'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Analyseren van duurzaamheidsposten met financiële rapporten 

Met de functie  *Financiële rapporten*  krijgt u inzicht in de financiële gegevens die in uw rekeningschema (COA) worden weergegeven. U kunt financiële rapporten instellen om cijfers in grootboekrekeningen (GB) te analyseren en grootboekposten te vergelijken met budgetposten. Maar u kunt met dezelfde functie ook statistische en duurzaamheidsgegevens analyseren en zelfs alle drie de soorten gegevens combineren.  

## Vereisten voor financiële rapportage  

Om financiële rapporten op te stellen, moet u inzicht hebben in de structuur van de gegevens die u wilt analyseren. Er zijn een aantal belangrijke concepten waar u waarschijnlijk op moet letten voordat u uw financiële rapporten opstelt: 

1. Gerelateerd aan het rekeningschema: 
   1. Wijs grootboekboekingsrekeningen toe aan grootboekrekeningcategorieën. 
   2. Ontwerp hoe u dimensies gebruikt.
   3. Stel grootboekbudgetten in.  
2. Gerelateerd aan Duurzaamheid:   
   1. Stel uw duurzaamheidsaccounts in. 
   2. Stel uw CO2- en CO2e-heffingen in via de **Emissieheffingen**.
   3. Ontwerp hoe u dimensies gebruikt.  
3. Gerelateerd aan de statistische rekeningen: 
   1. Stel uw statistische accounts in. 
   2. Ontwerp hoe u dimensies gebruikt.  

> [!NOTE]
> Financiële rapporten hebben geen directe invloed op CO2-, CH4- of N2O-uitstoot. In plaats daarvan wordt het CO2-equivalentmodel gebruikt. Dat betekent dat u eerst  **CO2e** (koolstofdioxide-equivalent) moet configureren op de pagina  **Emissieheffingen** .  

> [!NOTE]
> Meer informatie over het gebruik van financiële rapporten met financiële gegevens en rekeningschema's vindt u hier [Financiële rapporten maken met behulp van financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md).   

## Een nieuw financieel rapport maken  

Als u snel uw eigen financiële rapporten wilt maken, kunt u beginnen met een bestaand rapport te kopiëren, zoals hieronder is beschreven in stap drie. 

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Financiële rapporten** de actie **Nieuw** om een nieuwe naam voor een financieel rapport te maken.  
3. Vul de korte naam van het rapport in het veld  **Naam** (u kunt de naam later niet meer wijzigen) in en voer  **Beschrijving** in.  
4. Kies een rijdefinitie en een kolomdefinitie.   
5. Kies de actie  **rapportdefinitie bewerken** om toegang te krijgen tot meer eigenschappen in het financiële rapport.  
6. Op het sneltabblad **Opties** kunt u de rapportbeschrijving bewerken, de rij- en kolomdefinities wijzigen en definiëren hoe datums worden weergegeven. Voor datums kan een hiërarchie van dag, week, maand, kwartaal, jaar worden gebruikt of er kunnen boekhoudperioden worden gebruikt. Ga voor meer informatie naar [Boekingsperioden vergelijken met behulp van periodeformules](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas). 
7. Op het sneltabblad **Dimensies** kunt u dimensiefilters voor het rapport definiëren.  
8. U kunt een voorbeeld van het rapport bekijken in het gebied onder het sneltabblad **Dimensies**.   

Als u uw duurzaamheids- of statistische gegevens wilt analyseren, kunt u dit doen door de  **rijdefinitie** in te stellen.  

Om een rijdefinitie, volgen te maken of te bewerken, volgt u deze stappen:

1. Selecteer op de pagina **Financiële rapporten** het betreffende financiële rapport en kies vervolgens de actie **Rijdefinitie bewerken**. 
2. Stel rijen in zoals in de volgende stappen.  

> [!NOTE]
> Het veld **Rijnr.** toont de eerste tien tekens van een identificatie, zoals een rekeningnummer. Als u elementen toevoegt met identifiers die beginnen met dezelfde 10 tekens, krijgt u duplicaten in het veld **Rijnr.** . Indien nodig kunt u de id's handmatig bewerken nadat u de elementen hebt ingevoegd. De volledige identifiers worden weergegeven in het veld **Samentelling**.

> [!NOTE]
> U kunt alle **Totaaltypen** combineren, d.W.z. boekingsrekeningen, onderhoudsrekeningen. Rekeningen, statistische rekening.

> [!NOTE]
> Er is geen versiebeheer voor rijdefinities. Wanneer u rijdefinitie wijzigt, wordt de oude versie vervangen en worden uw wijzigingen opgeslagen in de database. 

### Analyseren van duurzaamheidsgegevens  

1. Voer het **rijnummer in.** Om uw ruwe gegevens te identificeren en **Beschrijving** toe te voegen als tekst die op de regel van het financiële rapport zal verschijnen. 
2. Selecteer in de kolom Totaaltype de optie  **Onderhoudsrekeningen** .   
3. Selecteer in het veld Totaliseren een of meer duurzaamheidsrekeningen met behulp van alle toepasselijke filters. 
4. Kies in het  **bedragstype** een van de opties:   
   1. **CO2e** als u de CO2-equivalentwaarde wilt rapporteren vanuit het veld **CO2e-emissie** in de **Duurzaamheidsposten**. 
   2. **Koolstofheffing** als u het financiële equivalent (koolstofheffing) wilt rapporteren vanuit het veld **Koolstofheffing** in de **Duurzaamheidsposten**. 
5. Als u  **Formule** als **Totaaltype** kiest, kunt u wiskundige formules gebruiken in de **Totaalkolom** .  

### Statistische gegevens analyseren

1. Voer het **rijnummer in.** Om uw rij te identificeren en  **Beschrijving** toe te voegen als een tekst die op de regel van het financiële rapport zal verschijnen. 
2. Selecteer in de kolom  **Totaaltype** de optie  **Statistische rekeningen** .   
3. Selecteer in het veld  **Totaal** een of meer duurzaamheidsrekeningen met behulp van alle toepasselijke filters. 
4. Als u  **Formule** als **Totaaltype** kiest, kunt u wiskundige formules gebruiken in de kolom **Totaal** .  

## Zie ook

[Overzicht Duurzaamheidsmanagement](finance-manage-sustainability.md)    
[Duurzaamheidsrapporten en analyses in Business Central](sustainability-reports.md)   
[Duurzaamheid-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Bereid financiële rapportage voor](bi-how-work-account-schedule.md)    
[rijdefinitie en financiële rapportage](bi-row-definitions.md)    
[kolomdefinitie in de financiële rapportage](bi-column-definitions.md)    
[Financiën](finance.md)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
