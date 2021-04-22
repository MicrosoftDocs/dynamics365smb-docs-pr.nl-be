---
title: Procedure - cashflowprognoses maken met behulp van rapportageschema's
description: Leer hoe u rapportageschema's gebruikt om cashflowprognoses te maken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 48a176c4c363c4a33ae336d754be71c9f7dd0aeb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772116"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Procedure: cashflow met behulp van rapportageschema's maken

In dit scenario wordt beschreven hoe u rapportageschema's kunt maken maken van cashflowprognoses. Rapportageschema's voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd. In de rapportageschema's kunt u subtotalen voor cashflowontvangsten en -betalingen instellen. Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure

In deze procedure worden de volgende taken omschreven:  

- Een nieuwe naam voor een cashflowrekening instellen.  
- Nieuwe rapportageschemaregels instellen.  
- Een nieuwe kolomindeling instellen.  
- Een kolomindeling toewijzen aan een rapportageschema.  
- De cashflowprognose weergeven en afdrukken.  

### <a name="prerequisites"></a>Vereisten

U moet het volgende doen om deze procedure uit te voeren:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- De cashflowvoorstelregels worden geregistreerd  

## <a name="roles"></a>Rollen

In dit overzicht worden taken gedemonstreerd die worden uitgevoerd door de volgende gebruikersrol:  

- Controller  

## <a name="story"></a>Scenario

Ken is controller bij CRONUS die de maandelijkse cashflowprognoses maakt. Hij neemt financiële gegevens, verkoop, inkoop en vaste activa op in de prognose en vervolgens presenteert hij deze aan CFO Sara voor het zakelijk perspectief.  

## <a name="setting-up-a-new-account-schedule-name"></a>Een nieuwe naam voor een rapportschema instellen.

Een rapportageschema bestaat uit een cashflowrekening met een reeks regels en een kolomindeling.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Een nieuwe naam voor een rekeningstelsel instellen  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema's** in en kies de desbetreffende koppeling.  
2. Kies op de pagina **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een cashflowrekening te maken.  
3. Voer in het veld **Naam** de tekst **Prognose** in.  
4. Voer in het veld **Omschrijving** **Cashflowprognose** in.  
5. Laat de velden **Std. kolomindeling** en **Analyseweergavenaam** leeg.  

## <a name="setting-up-account-schedule-lines"></a>Nieuwe rapportageschemaregels instellen.

Nadat een naam voor het rapportageschema is ingesteld, definieert Ken elke regel die in de cashflowrekening wordt weergegeven. Ken definieert de regels die kunnen worden weergegeven in rapporten en daarnaast extra regels die alleen voor het maken van berekeningen dienen.  

### <a name="to-set-up-account-schedule-lines"></a>Nieuwe rapportageschemaregels instellen  

1. Selecteer op de pagina **Rapportageschema's** de naam van het nieuwe rapportageschema **Prognose** dat u hebt gemaakt en kies vervolgens de actie **Rapportageschema bewerken**.  
2. Voer op de pagina **Rapportageschema** elke regel in zoals deze in de volgende tabel wordt weergegeven.  

    > [!TIP]  
    >  Met de functie **CF rekeningen invoegen** kunt u snel de cashflowrekeningen in het schema met cashflowrekeningen markeren en deze naar rapportageschemaregels kopiëren.  

    | Rijnr. | Omschrijving              | Samentellingssoort            | Samentelling | Rijsoort   | Bedragsoort | Weergeven |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Open verkooporders        | Cashflowpostrekeningen | 20       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Verhuur                  | Cashflowpostrekeningen | 30       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Financiële activa         | Cashflowpostrekeningen | 40       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Buitengebruikstelling vaste activa    | Cashflowpostrekeningen | 50       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Privé-investeringen      | Cashflowpostrekeningen | 60       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Diverse ontvangsten   | Cashflowpostrekeningen | 70       |Mutatie | Nettobedrag  | Ja  |
    | R10     | Open serviceorders      | Cashflowpostrekeningen | 80       |Mutatie | Nettobedrag  | Ja  |
    | R20     | Totale kasontvangsten      | Formule                  | R10      |Mutatie | Nettobedrag  | Ja  |
    | R20     | Totale kasontvangsten      | Formule                  | R10      |Mutatie | Nettobedrag  | Ja  |
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

## <a name="setting-up-a-new-column-layout"></a>Een nieuwe kolomindeling instellen

Voordat Ken de cashflowprognose kan afdrukken, moet hij de kolomindeling voor de numerieke gegevens maken. In de kolommen bepaalt hij welke informatie van de regels hij wil gebruiken.

- De eerste kolom heeft nummer *C10* met de titel **Bedrag** en bevat de mutatie.  
- De tweede kolom heeft nummer *C20* en de titel **Saldo t/m datum** en bevat de transacties voor de periode.  
- De derde kolom heeft nummer *C30* en de titel **Volledig jaar** en bevat de mutatie in de saldi voor het gehele boekjaar.  
- Ten slotte wijst hij de kolomindeling toe als de standaardkolomindeling voor het rapportageschema **Prognose**.  

## <a name="to-set-up-a-new-column-layout"></a>Een nieuwe kolomindeling instellen

1. Selecteer in het venster **Rapportageschema's** de nieuwe naam voor het rapportageschema **Prognose** dat u hebt gemaakt. Kies op het tabblad **Start** in de groep **Verwerken** de optie **Instellingen kolomindeling bewerken**.

    > [!TIP]
    > U vindt dezelfde actie op de pagina **Rapportageschema** als u nog steeds bezig bent met het bewerken van het rapportageschema **Voorspelling** daar.

2. Maak een nieuwe kolomindeling met de naam **Cashflow**.

3. Kies de knop Ok.

4. Voer elke regel in zoals in de volgende tabel wordt weergegeven.

    |Kolomnr.|Kolomkop|Kolomsoort|Boekingssoort|Bedragsoort|Weergeven|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |K10|Bedrag|Mutatie|Posten|Nettobedrag|Altijd|  
    |K20|Bedrag tot datum|Saldo t/m datum|Posten|Nettobedrag|Altijd|  
    |K30|Volledig boekjaar|Volledig boekjaar|Posten|Nettobedrag|Altijd|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>De kolomindeling toewijzen aan de naam van het rekeningstelsel

Ken kan nu de kolomindeling toewijzen aan de naam van het rapportageschema.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>De kolomindeling toewijzen aan de naam van het rekeningstelsel  

1. Kies op de pagina **Rapportageschema** waar u werkt met het rapportageschema **Prognose** de actie **Instellingen kolomindeling bewerken**.  
2. Kies in het veld **Kolomindelingnaam** de kolomindeling **Cashflow** om deze toe te wijzen als de standaardkolomindeling.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>De cashflowprognose weergeven en afdrukken

1. Kies op de pagina **Rapportageschema's** de actie **Overzicht** om de cashflowprognose weer te geven.  
2. Op de pagina **Rapportageschemaoverzicht** kunt u een bedrag selecteren en vervolgens de cashflowprognoseposten weergeven waaruit het bedrag bestaat. Bovendien kunt u de formule weergegeven die voor het berekenen van het bedrag wordt gebruikt. U kunt de bedragen ook filteren op datum en dimensie.  
3. Kies de actie **Afdrukken** om de cashflowprognose af te drukken.  

## <a name="see-also"></a>Zie ook

[Werken met rekeningschema's](bi-how-work-account-schedule.md)  
[Cashflow in uw bedrijf analyseren](finance-analyze-cash-flow.md)  
[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]