---
title: "Procedure: Cashflowprognoses maken met behulp van rapportageschema's | Microsoft Docs"
description: In dit scenario wordt beschreven hoe u rapportageschema's kunt maken maken van cashflowprognoses. Rapportageschema's voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd. In de rapportageschema's kunt u subtotalen voor cashflowontvangsten en -betalingen instellen. Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a210792a187bde0217917659f118c58a6a135df2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756553"
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

- [!INCLUDE[prod_short](includes/prod_short.md)] installeren.  
- De cashflowvoorstelregels worden geregistreerd.  

## <a name="roles"></a>Rollen  
In dit overzicht worden taken gedemonstreerd die worden uitgevoerd door de volgende gebruikersrol:  

- Controller  

## <a name="story"></a>Scenario  
Ken is controller bij CRONUS die de maandelijkse cashflowprognoses maakt. Hij neemt financiële gegevens, verkoop, inkoop en vaste activa op in de prognose en vervolgens presenteert hij deze aan CFO Sara voor het zakelijk perspectief.  

## <a name="setting-up-a-new-account-schedule-name"></a>Een nieuwe naam voor een rapportschema instellen.  
Een rapportageschema bestaat uit een cashflowrekening met een reeks regels en een kolomindeling.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Een nieuwe naam voor een rekeningstelsel instellen  

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema's** in en kies de desbetreffende koppeling.  
2.  Kies op de pagina **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een cashflowrekening te maken.  
3.  Voer in het veld **Naam** de tekst **Prognose** in.  
4.  Voer in het veld **Omschrijving** **Cashflowprognose** in.  
5.  Laat de velden **Std. kolomindeling** en **Analyseweergavenaam** leeg.  

## <a name="setting-up-account-schedule-lines"></a>Nieuwe rapportageschemaregels instellen.  
Nadat een naam voor het rapportageschema is ingesteld, definieert Ken elke regel die in de cashflowrekening wordt weergegeven. Ken definieert de regels die kunnen worden weergegeven in rapporten en daarnaast extra regels die alleen voor het maken van berekeningen dienen.  

### <a name="to-set-up-account-schedule-lines"></a>Nieuwe rapportageschemaregels instellen  

1.  Selecteer op de pagina **Rapportageschema's** de naam van het nieuwe rapportageschema **Prognose** dat u hebt gemaakt en kies vervolgens de actie **Rapportageschema bewerken**.  
2.  Voer op de pagina **Rapportageschema** elke regel in zoals deze in de volgende tabel wordt weergegeven.  

    > [!NOTE]  
    >  Met de functie **CF rekeningen invoegen** kunt u snel de cashflowrekeningen in het schema met cashflowrekeningen markeren en deze naar rapportageschemaregels kopiëren.  

    |Rijnr.|Omschrijving|Samentellingssoort|Samentelling|Rijsoort|Bedragsoort|Weergeven|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |K10|Bedrag|Mutatie|Posten|Nettobedrag|Altijd|  
    |K20|Bedrag tot datum|Saldo t/m datum|Posten|Nettobedrag|Altijd|  
    |K30|Volledig boekjaar|Volledig boekjaar|Posten|Nettobedrag|Altijd|  

4.  Kies de knop **Ok**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>De kolomindeling toewijzen aan de naam van het rekeningstelsel  
Ken kan nu de kolomindeling toewijzen aan de naam van het rapportageschema.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>De kolomindeling toewijzen aan de naam van het rekeningstelsel  

1.  Selecteer op de pagina **Rapportageschema's** in het veld **Naam** **Prognose**.  
2.  Kies in het veld **Std. kolomindeling** de kolomindeling **Cashflow** om deze toe te wijzen als de standaardkolomindeling.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>De cashflowprognose weergeven en afdrukken  
1.  Kies op de pagina **Rapportageschema's** de actie **Overzicht** om de cashflowprognose weer te geven.  
2.  Op de pagina **Rapportageschemaoverzicht** kunt u een bedrag selecteren en vervolgens de cashflowprognoseposten weergeven waaruit het bedrag bestaat. Bovendien kunt u de formule weergegeven die voor het berekenen van het bedrag wordt gebruikt. U kunt de bedragen ook filteren op datum en dimensie.  
3.  Kies de actie **Afdrukken** om de cashflowprognose af te drukken.  

## <a name="see-also"></a>Zie ook  
 [Werken met rekeningschema's](bi-how-work-account-schedule.md)   
 [Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]