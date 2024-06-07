---
title: Rijdefinities in financiële rapportage
description: Beschrijft hoe rijdefinities in financiële rapportage werken.
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Rijdefinities in financiële rapportage

Rijdefinities in financiële rapporten bieden een plaats voor berekeningen die niet rechtstreeks in het rekeningschema kunnen worden uitgevoerd. U kunt bijvoorbeeld subtotalen maken voor groepen rekeningen en dat totaal vervolgens opnemen in andere totalen. Ook kunt u tussenstappen berekenen die niet in het eindrapport staan.

## Een rijdefinitie maken of bewerken

Volg deze stappen om een rijdefinitie te maken of te bewerken:

1. Selecteer op de pagina **Financiële rapporten** het betreffende financiële rapport en kies vervolgens de actie **Rijdefinitie bewerken**.
1. Kies de acties **Grootboekrekeningen invoegen**, **CF-accounts invoegen** en **Kostensoorten invoegen** om een rij te maken voor elk financieel element dat u wilt analyseren. U hebt bijvoorbeeld één rij voor vlottende activa en een andere rij voor vaste activa. Verken voor inspiratie de financiële rapporten in het voorbeeldbedrijf CRONUS.

    > [!NOTE]
    > Het veld **Rijnr.** toont de eerste tien tekens van een identificatie, zoals een rekeningnummer. Als u elementen toevoegt met identifiers die beginnen met dezelfde 10 tekens, krijgt u duplicaten in het veld **Rijnr.** . Indien nodig kunt u de id's handmatig bewerken nadat u de elementen hebt ingevoegd. De volledige identifiers worden weergegeven in het veld **Samentelling**.

> [!NOTE]
> De kolommen die u voor elke regel in de rijdefinitie definieert, vertegenwoordigen kolom drie en hoger op de pagina **Financieel rapport**. De eerste twee kolommen, **Rijnr.** en **Omschrijving** zijn vast.  

## Ingebouwde rijdefinities

[!INCLUDE[prod_short](includes/prod_short.md)] biedt voorbeeldrijdefinities waarmee u snel aan de slag kunt gaan met het opstellen van financiële rapporten die aan uw behoeften voldoen.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> De voorbeeldfinancieringsrapporten in [!INCLUDE[prod_short](includes/prod_short.md)] zijn niet kant-en-klaar voor gebruik. Afhankelijk van de manier waarop u uw grootboekrekeningen, dimensies, grootboekrekeningcategorieën en budgetten instelt, moet u de voorbeeldrij- en kolomdefinities en de financiële rapporten die er gebruik van maken, aanpassen aan uw instellingen.

## GB-rekeningcategorieën gebruiken om de indeling van uw financiële overzichten te wijzigen

U kunt GB-rekeningcategorieën gebruiken om de indeling te wijzigen van uw financiële overzichten. Nadat u de rekeningcategorieën hebt ingesteld op de pagina **GB-rekeningcategorieën** kunt u bijvoorbeeld de actie **Financiële rapporten genereren** kiezen en de onderliggende financiële rapporten voor de financiële kernrapporten bijwerken. De volgende keer dat u een van deze rapporten uitvoert, zoals het rapport **Balans**, worden nieuwe totalen en subposten toegevoegd.

Een ander voordeel van het gebruik van grootboekrekeningcategorieën ten opzichte van de ruwe grootboekrekeningen in uw rijdefinities is dat een wijziging in de structuur van uw rekeningschema geen invloed heeft op uw financiële rapporten.

> [!NOTE]
> De rekeningcategorieën op het hoogste niveau, zoals het knooppunt **Passiva** zijn vast en u kunt geen eigen categorie toevoegen. U kunt rekeningcategorieën echter op lagere niveaus verwijderen en toevoegen en definiëren hoe het gerelateerde financiële rapport in rapporten wordt weergegeven.
>
> U moet uw eigen categorieën van grootboekrekeningen op lager niveau helemaal zelf maken en structureren, indien nodig in een hiërarchie, in plaats van te proberen de bestaande categorieën te herschikken. U kunt bijvoorbeeld het knooppunt **Passiva** herstructureren met een nieuw knooppunt **Eigen vermogen**, gevolgd door de knooppunten **Vlottende verplichtingen** en **LT-verplichtingen**. Meer informatie is te vinden bij [Grootboekrekeningen toewijzen aan rekeningcategorieën](finance-general-ledger.md#account-categories).

## Best practices voor het werken met rijdefinities

Er is geen versiebeheer voor rijdefinities. Wanneer u een rijdefinitie wijzigt, wordt de oude versie vervangen wanneer uw wijziging in de database wordt opgeslagen. De volgende lijst bevat enkele best practices voor het werken met rijdefinities:

- Als u rijdefinities toevoegt, kiest u een goede code en vult u het beschrijvingsveld in met een betekenisvolle tekst, terwijl u nog weet waarvoor u de rijdefinitie gebruikt. Deze informatie helpt uw ​​collega's (en uzelf in de toekomst) om met financiële rapportage te werken en eventueel de rijdefinitie te wijzigen.
- Voordat u een rijdefinitie wijzigt, kunt u overwegen er een kopie van te maken als back-up, voor het geval uw wijziging niet werkt zoals verwacht. U kunt de definitie gewoon kopiëren (geef deze een goede naam) of exporteren. Als u meer wilt weten, gaat u naar [Rijdefinities importeren of exporteren](#import-or-export-financial-reporting-row-definitions).
- Als u een nieuwe kopie nodig heeft van een definitie die [!INCLUDE[prod_short](includes/prod_short.md)] voorziet, kunt u er eenvoudig een krijgen door een nieuw bedrijf op te richten dat alleen instellingsgegevens bevat. Exporteer vervolgens de definitie en importeer deze in het bedrijf waar de definitie moet worden vernieuwd.

## Rijdefinities van financiële rapporten importeren of exporteren

U kunt rijdefinities importeren en exporteren als RapidStart-configuratiepakketten. Configuratiepakketten zijn bijvoorbeeld handig om informatie te delen met andere bedrijven. Het pakket wordt gemaakt vanuit een .rapidstart-bestand, dat de inhoud comprimeert.

> [!NOTE]
> Wanneer u rijdefinities van financiële rapportage importeert, worden bestaande records met dezelfde naam als de records die u importeert, vervangen door de nieuwe definities. Het configuratiepakket voor een rapportdefinitie overschrijft geen bestaande rij- of kolomdefinities die in de rapportdefinitie worden gebruikt.

Volg deze stappen om rijdefinities van financiële rapporten te importeren of exporteren:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 4.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rijdefinities** in en kies vervolgens de gerelateerde koppeling.
1. Kies de rijdefinitie en kies vervolgens de actie **Rijdefinitie importeren** of **Rijdefinitie exporteren**, afhankelijk van wat u wilt doen.

## Zie ook

[Kolomdefinities in financiële rapportage](bi-column-definitions.md)  
[Financiële rapportage voorbereiden](bi-how-work-account-schedule.md)  
[Financiële Business Intelligence](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
