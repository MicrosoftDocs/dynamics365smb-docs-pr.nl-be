---
title: Cashflowprognoses maken met behulp van financiële rapporten
description: In dit scenario wordt beschreven hoe u financiële rapporten kunt maken van cashflowprognoses in Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: edupont
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports" />Overzicht: Cashflowprognoses maken met behulp van financiële rapporten

In dit scenario wordt beschreven hoe u de functie voor financiële rapporten kunt gebruiken om cashflowprognoses te maken in Business Central. Financiële rapporten voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd. In de financiële rapporten kunt u subtotalen voor cashflowontvangsten en -betalingen instellen. Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.  

## <a name="about-this-walkthrough" />Informatie over deze procedure

In deze procedure worden de volgende taken omschreven:  

- Een nieuwe naam voor een financieel cashflowrapport instellen.  
- Financiële rapportregels instellen.  
- Een nieuwe kolomindeling instellen.  
- Een kolomdefinitie toewijzen aan een financieel rapport.  
- De cashflowprognose weergeven en afdrukken.  

### <a name="prerequisites" />Vereisten

U moet het volgende doen om deze procedure uit te voeren:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Een cashflowvoorstel met geregistreerde regels  

## <a name="roles" />Rollen

In dit overzicht worden taken gedemonstreerd die worden uitgevoerd door de volgende gebruikersrol:  

- Controller  

## <a name="story" />Scenario

Ken is controller bij CRONUS die de maandelijkse cashflowprognoses maakt. Ken neemt financiële gegevens, verkoop, inkoop en vaste activa op in de prognoses, die hij presenteert aan CFO Sara voor het zakelijk perspectief.  

## <a name="setting-up-a-new-financial-report-name" />Een nieuwe naam voor een financieel rapport instellen

De naam van het financiële rapport is de naam die u aan de cashflowprognose geeft die een reeks gedefinieerde regels en een kolomdefinitie bevat.  

### <a name="set-up-a-new-financial-report-name" />Een nieuwe naam voor een financieel rapport instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Financiële rapporten** **Nieuw** om een nieuwe naam voor het financiële cashflowrapport te maken.  
3. Voer in het veld **Naam** de tekst **Prognose** in.  
4. Voer in het veld **Omschrijving** **Cashflowprognose** in.  
5. Laat de velden **Rijdefinitie** en **Kolomdefinitie** leeg.

## <a name="setting-up-row-definition-lines" />Rijdefinitieregels instellen

Nadat de naam van een financieel rapport is ingesteld, definieert Ken elke regel in het financiële cashflowrapport. Ken definieert de regels die moeten worden weergegeven in rapporten en daarnaast extra regels die alleen voor het maken van berekeningen dienen.  

### <a name="set-up-row-definition-lines" />Rijdefinitieregels instellen

1. Selecteer op de pagina **Financiële rapporten** het nieuwe financiële rapport **Prognose** dat u hebt gemaakt, en kies vervolgens de actie **Rijdefinitie bewerken**.  
2. Voer op de pagina **Rijdefinitie** elke regel in zoals deze in de volgende tabel wordt weergegeven.  

    > [!TIP]  
    > Met de functie **CF rekeningen invoegen** kunt u snel de gewenste cashflowrekeningen in het schema met cashflowrekeningen markeren en deze naar rijdefinitieregels kopiëren.  

    | Rubriek | Omschrijving              | Samentellingssoort            | Samentelling | Rijsoort   | Bedragtype | Weergeven |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | B10     | Tegoeden              | Cashflowpostrekeningen | 10       |Mutatie | Nettobedrag  | Ja  |
    | B10     | Open verkooporders        | Cashflowpostrekeningen | 20       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Verhuur                  | Cashflowpostrekeningen | 30       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Financiële activa         | Cashflowpostrekeningen | 40       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Buitengebruikstelling vaste activa    | Cashflowpostrekeningen | 50       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Privé-investeringen      | Cashflowpostrekeningen | 60       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Diverse ontvangsten   | Cashflowpostrekeningen | 70       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Open serviceorders      | Cashflowpostrekeningen | 80       |Mutatie | Nettobedrag  | Ja  |
    | R20     | Totale kasontvangsten      | Formule                  | B10      |Mutatie | Nettobedrag  | Ja  |
    | R30     | Schulden                 | Cashflowpostrekeningen | 1010     |Mutatie | Nettobedrag  | Ja  |
    | R30     | Openstaande inkooporders     | Cashflowpostrekeningen | 1020     |Mutatie | Nettobedrag  | Ja  |
    | R30     | Personeelskosten          | Cashflowpostrekeningen | 1030     |Mutatie | Nettobedrag  | Ja  |
    | R30     | Bedrijfskosten            | Cashflowpostrekeningen | 1040     |Mutatie | Nettobedrag  | Ja  |
    | R30     | Financiële kosten            | Cashflowpostrekeningen | 1050     |Mutatie | Nettobedrag  | Ja  |
    | R30     | Investeringen              | Cashflowpostrekeningen | 1070     |Mutatie | Nettobedrag  | Ja  |
    | R30     | Privéverbruik     | Cashflowpostrekeningen | 1090     |Mutatie | Nettobedrag  | Ja  |
    | R30     | Te betalen btw                  | Cashflowpostrekeningen | 1100     |Mutatie | Nettobedrag  | Ja  |
    | R30     | Overige kosten           | Cashflowpostrekeningen | 1110     |Mutatie | Nettobedrag  | Ja  |
    | R40     | Totale kasvoorschotten | Formule                  | R30      |Mutatie | Nettobedrag  | Ja  |
    | R50     | Overschot                  | Formule                  | R20+R40  |Mutatie | Nettobedrag  | Ja  |
    | R60     | Cashflowfondsen          | Cashflowpostrekeningen | 2100     |Mutatie | Nettobedrag  | Ja  |
    | R70     | Totale cashflow          | Formule                  | R50+R60  |Mutatie | Nettobedrag  | Ja  |

    > [!NOTE]
    > Het rijnummer R10 wordt gebruikt voor het vastleggen van de rekeningtotalen voor tegoeden. Het rijnummer R20 wordt gebruikt voor het berekenen van de som van alle kasontvangsten. Het rijnummer R30 wordt gebruikt voor het vastleggen van de rekeningtotalen voor schulden. Het rijnummer R40 wordt gebruikt voor het berekenen van de som van alle kasvoorschotten. Het rijnummer R50 wordt gebruikt voor het vastleggen van de som van alle kassurplus. Het rijnummer R60 wordt gebruikt voor het vastleggen van de liquide fondsen. Het rijnummer R70 wordt gebruikt voor het berekenen van de verwachte cashflow.

## <a name="setting-up-a-new-column-definition" />Een nieuwe kolomindeling instellen

Voordat Ken de cashflowprognose kan afdrukken, moet hij de kolomdefinitie voor de numerieke gegevens maken. In de kolommen bepaalt Ken welke informatie hij van de regels wil gebruiken.

- De eerste kolom heeft nummer *C10* met de titel **Bedrag** en bevat de mutatie.  
- De tweede kolom heeft nummer *C20* en de titel **Saldo t/m datum** en bevat de transacties voor de periode.  
- De derde kolom heeft nummer *C30* en de titel **Volledig jaar** en bevat de mutatie in de saldi voor het gehele boekjaar.  
- Ten slotte wijst Ken de kolomdefinitie toe als de standaardoptie voor het financiële rapport **Prognose**.  

### <a name="set-up-a-new-column-definition" />Een nieuwe kolomdefinitie instellen

1. Selecteer op de pagina **Financiële rapporten** de naam van het nieuwe financiële rapport **Prognose** die u hebt gemaakt. Kies op het tabblad **Start** in de groep **Proces** de optie **Kolomdefinitie bewerken**.

2. Maak een nieuwe kolomdefinitie met de naam **Cashflow**.

3. Kies de knop **OK**.

4. Voer elke regel in zoals in de volgende tabel wordt weergegeven.

    |Kolomnr.|Kolomkop|Kolomsoort|Boekingssoort|Bedragsoort|Weergeven|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |K10|Bedrag|Mutatie|Posten|Nettobedrag|Altijd|  
    |K20|Bedrag tot datum|Saldo op datum|Posten|Nettobedrag|Altijd|  
    |K30|Volledig boekjaar|Volledig boekjaar|Posten|Nettobedrag|Altijd|

## <a name="assigning-the-column-definition-to-the-financial-report-name" />De kolomdefinitie toewijzen aan de naam van het financiële rapport

Ken kan nu de kolomdefinitie toewijzen aan de naam van het financiële rapport.  

### <a name="assign-the-column-definition-to-the-financial-report-name" />De kolomdefinitie toewijzen aan de naam van het financiële rapport

1. Selecteer op de pagina **Financiële rapporten** het financiële rapport **Prognose** en kies vervolgens de actie **Kolomdefinitie bewerken**.  
2. Kies in het veld **Naam** de kolomdefinitie **Cashflow** om deze toe te wijzen als de standaardkolomdefinitie.  

## <a name="view-and-print-the-cash-flow-forecast" />De cashflowprognose weergeven en afdrukken

1. Kies op de pagina **Financiële rapporten** het financiële rapport **Prognose** om de cashflowprognose weer te geven.  
2. Op de pagina **Financieel rapport** kunt u een bedrag selecteren en vervolgens de cashflowprognoseposten weergeven waaruit het bedrag bestaat. Bovendien kunt u de formule weergegeven die voor het berekenen van dat bedrag wordt gebruikt. U kunt de bedragen ook filteren op datum en dimensie.  
3. Kies de actie **Afdrukken** om de cashflowprognose af te drukken.  

## <a name="see-related-microsoft-trainingtrainingmodulesforecast-cash-flow-dynamics--business-central" />Zie gerelateerde [Microsoft-training](/training/modules/forecast-cash-flow-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Werken met financiële rapporten](bi-how-work-account-schedule.md)  
[Cashflow in uw bedrijf analyseren](finance-analyze-cash-flow.md)  
[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
