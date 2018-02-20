---
title: "Een OHW-methode definiëren en projectvoortgang controleren| Microsoft Docs"
descrition: Describes how you can create a work in process (WIP) method and calculate WIP to estimate the financial value of jobs while they are ongoing.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 22dc57e01941927dfc2077eb1e48645cfc7b56de
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="monitor-job-progress-and-performance"></a>Voortgang en prestaties van projecten bewaken
Naarmate een project vordert, worden materialen, resources en overige zaken verbruikt en moeten hiervoor boekingen plaatsvinden op het project. Onderhanden werk (OHW) is een functie waarmee u de financiële waarde van projecten in het grootboek kunt schatten gedurende de projecten. In veel gevallen kunt u kosten voor een project boeken voordat u het project factureert. Wanneer alleen kosten zijn geboekt, klopt het financiële afschrift niet. Zie [OHW-methoden](projects-understanding-wip.md) voor meer informatie.

Als u de waarde in het grootboek wilt volgen, kunt u het OHW-bedrag berekenen en de waarde boeken in het grootboek.

U kunt het OHW-bedrag berekenen op basis van de volgende zaken:

* Kostprijs
* Verkoopprijs
* Kostprijs van omzet
* Percentage voltooid
* Contract voltooid

Als u het resultaat met een andere methode wilt bekijken, kunt u de methode wijzigen en het OHW-bedrag nogmaals berekenen. U kunt net zo vaak het OHW-bedrag berekenen als u wilt. Het OHW-bedrag wordt alleen berekend en wordt niet geboekt in het grootboek. Na het berekenen van het OHW-bedrag, kunt u het OHW-bedrag boeken in het grootboek.

## <a name="to-create-a-job-wip-method"></a>Een OHW-methode voor een project maken
U kunt een OHW-methode voor een project maken die de behoeften van uw organisatie weerspiegelt. Nadat u deze methode hebt gemaakt, kunt u deze instellen als standaard OHW-berekeningsmethode voor een project die wordt gebruikt in uw organisatie.  

> [!NOTE]
> Nadat u uw nieuwe methode hebt gebruikt om OHW-posten te maken, kunt u de methode niet meer verwijderen of wijzigen.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **OHW-methoden taak** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sluit het venster.   
4. Als u van deze nieuwe methode de standaard wilt maken, kiest u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Projectinstellingen** in en kiest u vervolgens de gerelateerde koppeling.  
5. Kies in het veld **Standaard OHW-methode** de methode uit de lijst.

## <a name="to-define-a-wip-method-for-a-job"></a>Een OHW-methode voor een project definiëren
Wanneer u een nieuw project maakt, moet u opgeven welke OHW-methode voor het project van toepassing is. In sommige gevallen is de OHW-methode voor het project die u kunt gebruiken standaard voor u ingesteld.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Nieuw**. Zie voor meer informatie [Projecten maken](projects-how-create-jobs.md).  
3. Selecteer in het venster **Projectkaart** in het veld **OHW-methode** een OHW-methode uit de lijst. Als een standaardmethode is gedefinieerd, kunt u indien nodig een andere optie selecteren.  

## <a name="to-calculate-wip"></a>OHW berekenen
U kunt het OHW-bedrag bepalen dat moet worden geboekt naar balansrekeningen voor eindrapportage van een periode. U gebruikt hiervoor de batchverwerking **OHW voor project berekenen**.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **OHW voor project berekenen** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **OHW berekenen**.
3. Vul in het venster **OHW voor project berekenen** indien nodig de velden in.
4. Kies de knop **OK**.  

> [!NOTE]  
>   De batchverwerking berekent alleen het OHW. Het wordt niet geboekt in het grootboek. Hiervoor moet u de batchverwerking **OHW naar GB boeken** uitvoeren wanneer u het onderhanden werk hebt berekend. Zie de volgende procedure voor meer informatie.

## <a name="to-post-wip"></a>OHW boeken
Wanneer u OHW hebt berekend, kunt u het boeken naar balansrekeningen voor de einddatumrapportage. Hiervoor gebruikt u de batchverwerking **Project-OHW naar GB boeken**.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Project-OHW naar GB boeken** in en klik vervolgens op de gerelateerde koppeling.  
2. Vul in het venster **Project-OHW naar GB boeken** indien nodig de velden in.  
3. Kies de knop **Ok**.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Projectgebruikschattingen weergeven en updates boeken
U kunt in één stap het projectgebruik tot aan de voltooiing van een project bekijken. Hiervoor gebruikt u de batchverwerking **Project - Resterend gebruik berekenen** voor alle taken tot en met het einde van een project.  

Op deze manier kunt u uw oorspronkelijke schattingen volgen en vergelijken met de werkelijke resultaten en zo nodig wijzigingen aanbrengen of nieuwe posten maken. U hebt bijvoorbeeld mogelijk geschat dat een project 10 uur vereist en tot op heden zijn er al 15 uur aan besteed. U kunt de extra vijf uur aan de bestaande dagboekregel toevoegen of een nieuwe dagboekregel maken om deze vijf uur als overuren te rapporteren. Dit is een ander werksoort. De juiste kosten en prijzen worden berekend die vervolgens naar het dagboek kunnen worden geboekt.  

> [!NOTE]  
>   Artikelposten maken artikeljournaalposten en verkleinen de voorraadhoeveelheid. De batchverwerking **Voorraadwaarde boeken** brengt de kosten van de voorraad over naar het grootboek. Resourceposten maken resourceposten.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer een relevant projectdagboek en kies vervolgens de actie **Resterend gebruik berekenen**.  
3. Voer in het venster **Project - Resterend gebruik berekenen** het documentnummer en de boekingsdatum in die in het dagboek moeten worden ingevoegd, en kies vervolgens de knop **OK**.  
4. Werk het dagboek bij met eventuele wijzigingen die nodig zijn.  
5. Kies de actie **Boeken**.

## <a name="to-view-job-ledger-entries"></a>Projectposten bekijken
Alle posten met betrekking tot een project worden in projectjournalen opgeslagen en sequentieel genummerd, te beginnen met 1. Vanuit het projectjournaal hebt u een overzicht van alle projectposten.    

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectjournalen** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer een relevant journaal en kies vervolgens de actie **Projectposten**.

Het venster **Projectposten** wordt geopend, waarin u de posten die zijn gekoppeld aan een project, kunt bekijken.  

## <a name="see-also"></a>Zie ook
[Projecten beheren](projects-manage-projects.md)
[Voorraadkosten beheren](finance-manage-inventory-costs.md)   
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)         
[Verkoop](sales-manage-sales.md)      
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

