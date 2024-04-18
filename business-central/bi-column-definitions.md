---
title: Kolomdefinities in financiële rapportage
description: Beschrijft hoe kolomdefinities in financiële rapportage werken.
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

# Kolomdefinities in financiële rapportage

Gebruik kolomdefinities om op te geven welke kolommen in een rapport moeten worden opgenomen. U kunt bijvoorbeeld een rapportindeling maken om mutatie en saldo te vergelijken voor dezelfde periode dit jaar en vorig jaar. U kunt maximaal 15 kolommen in een kolomdefinitie hebben. Meerdere kolommen zijn bijvoorbeeld handig voor het weergeven van budgetten voor 12 maanden met een kolom die het totaal laat zien.

## Een kolomdefinitie maken of bewerken

Volg deze stappen om een kolomdefinitie te maken of te bewerken.

> [!NOTE]
> Een afgedrukte/opgeslagen of voorbeeldversie van een financieel rapport kan maximaal vijf kolommen weergegeven. Als een financieel rapport daarentegen alleen bedoeld is voor analyse op de pagina **Financieel rapport**, kunt u zoveel kolommen maken als u wilt.

1. Selecteer op de pagina **Financiële rapporten** het betreffende financiële rapport en kies vervolgens de actie **Kolomdefinitie bewerken**.
1. Maak op de pagina **Kolomdefinitie** een rij voor elke kolom met financiële gegevens die in het financiële rapport wordt weergegeven. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Klik op **OK**.
1. Open van tijd tot tijd de pagina **Financieel rapport** om te controleren of de nieuwe kolomdefinitie werkt zoals bedoeld.

## Ingebouwde kolomdefinities

[!INCLUDE[prod_short](includes/prod_short.md)] biedt voorbeeldkolomdefinities waarmee u snel aan de slag kunt gaan met het opstellen van financiële rapporten die aan uw behoeften voldoen.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## Voorbeeld: een kolomdefinitie maken om percentages te berekenen

U wilt misschien een kolom opnemen in een financieel rapport om percentages van een totaal te berekenen. U hebt bijvoorbeeld een aantal rijen die zijn onderverdeeld op dimensie, en u wilt wellicht een kolom maken om het percentage aan te geven van de totale verkoop van elke rij.

1. Kies het pictogram ![Lampje dat de functie Vertel me 2 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.
1. Selecteer op de pagina **Financiële rapporten** een financieel rapport.  
1. Kies de actie **Financieel rapport bewerken** om een rij in een financieel rapport in te stellen waarmee de totalen moeten worden berekend waarop de percentages zijn gebaseerd.  
1. Voeg een regel toe direct boven de eerste rij waarvoor u een percentage wilt weergeven.  
1. Vul de velden als volgt op de regel in: 
    1. Voer in het veld **Samentellingssoort** **Basis voor percentage instellen** in. 
    1. Voer in het veld **Samentelling** een formule in voor het totaal waarop het percentage wordt gebaseerd. Als bijvoorbeeld rij 11 de totale omzet bevat, voert u **11** in.  
1. Kies de actie **Kolomdefinitie bewerken** om een kolom in te stellen.  
1. Vul de velden als volgt op de regel in. 
    1. Kies in het veld **Kolomsoort** de **Formule**. 
    1. Voer in het veld **Formule** een formule in voor het bedrag waarvoor u een percentage wilt berekenen, gevolgd door het percentageteken (%). Dus als kolomnummer N de mutatie bevat, voert u **N%** in.  
1. Herhaal stap 4 tot en met 7 voor elke groep rijen die u wilt uitsplitsen op percentage.

## Boekingsperioden vergelijken met behulp van periodeformules

Uw financiële rapport kan de resultaten vergelijken van verschillende boekingsperioden, zoals de afgelopen maand vergeleken met dezelfde maand vorig jaar. Open hiervoor de pagina **Kolomdefinitie** en personaliseer deze door het veld **Periodevergelijkingsformule** als een kolom toe te voegen. Zie voor meer informatie [Uw werkruimte personaliseren](ui-personalization-user.md). U kunt dat veld vervolgens instellen op een periodeformule.  

Een boekingsperiode hoeft niet overeen te komen met de kalender. Elk boekjaar moet echter hetzelfde aantal boekhoudperioden hebben, ook al kan elke periode een andere lengte hebben.  

[!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de periodeformule om de duur van de vergelijkingsperiode te berekenen in verhouding tot de periode die wordt voorgesteld door het datumfilter in het rapport. De vergelijkingsperiode is gebaseerd op de begindatum van het datumfilter. De volgende tabel toont de afkortingen voor periodespecificaties.

| Afkorting | Omschrijving                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| LP           | Laatste periode van een boekjaar, half jaar of kwartaal.                                   |
| CP           | Huidige periode van een boekjaar, half jaar of kwartaal. Gebruik HP in formules om de periode in te stellen waarmee de formule begint of eindigt. Bijvoorbeeld BJ\[1..HP\] geeft de tijd aan vanaf het begin van het huidige boekjaar tot de huidige periode.|
| BJ           | Boekjaar. Met BJ\[1..3\] wordt bijvoorbeeld het eerste kwartaal van het huidige boekjaar aangeduid. |

Voorbeelden van formules:

| Formule | Omschrijving |
|-----|-----|
| \<Blank\>       | Huidige periode. |
| \-1P            | Vorige periode.            |
| \-1BJ\[1..LP\]  | Volledig vorig boekjaar.                  |
| \-1BJ           | Huidige periode in vorig boekjaar.       |
| \-1BJ\[1..3\]   | Eerste kwartaal van vorig boekjaar.        |
| \-1BJ\[1..HP\]  | Van het begin van het vorige boekjaar tot en met de huidige periode in het vorige boekjaar, inclusief beide perioden. |
| \-1BJ\[HP..LP\] | Van de huidige periode in het vorige boekjaar tot de laatste periode van het vorige boekjaar, inclusief beide perioden.   |

Als u de berekening volgens normale tijdsperioden wilt uitvoeren, moet u in plaats daarvan een formule in het veld **Datumvergelijkingsformule** invoeren. Als het veld bijvoorbeeld de waarde -1J heeft, wordt in [!INCLUDE [prod_short](includes/prod_short.md)] met dezelfde periode één jaar eerder vergeleken.

> [!NOTE]
> Het is niet altijd duidelijk welke perioden u vergelijkt omdat u een datumfilter op een rapport kunt instellen dat andere datums omvat dan de boekingsperioden die worden gereflecteerd in het rekeningschema. Als u dus een financieel rapport maakt waarin u deze periode wilt vergelijken met dezelfde periode vorig jaar, stelt u het veld **Datumvergelijkingsformule** in op **-1BJ**. Vervolgens voert u het rapport uit op **28 februari** en stelt u het datumfilter in op **januari en februari**. Daardoor vergelijkt het financiële rapport januari en februari van dit jaar met januari vorig jaar, wat de enige voltooide boekingsperiode van de twee voor vorig jaar is.  

Zie voor meer informatie [Werken met kalenderdatums en tijden](ui-enter-date-ranges.md).

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## Kolomdefinities van financiële rapporten importeren of exporteren

Vanaf releasewave 1 van 2024 (versie 24.1) kunt u kolomdefinities voor financiële rapporten importeren en exporteren als RapidStart -configuratiepakketten. Configuratiepakketten zijn bijvoorbeeld handig om informatie te delen met andere bedrijven. Het pakket wordt gemaakt vanuit een .rapidstart-bestand, dat de inhoud comprimeert.

> [!NOTE]
> Wanneer u financiële rapporten/kolomdefinities importeert, worden bestaande records met dezelfde naam als de records die u importeert vervangen door de nieuwe definities. Het configuratiepakket voor een rapportdefinitie overschrijft geen bestaande rij- of kolomdefinities die in de rapportdefinitie worden gebruikt.

Volg deze stappen om kolomdefinities van financiële rapporten te importeren of exporteren:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 4.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kolomdefinities** in en kies vervolgens de gerelateerde koppeling.
1. Kies de rijdefinitie en kies vervolgens de actie **Kolomdefinitie importeren** of **Kolomdefinitie exporteren**, afhankelijk van wat u wilt doen.

## Zie ook

[Rijdefinities in financiële rapportage](bi-row-definitions.md)  
[Financiële rapportage voorbereiden](bi-how-work-account-schedule.md)  
[Financiële Business Intelligence](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
