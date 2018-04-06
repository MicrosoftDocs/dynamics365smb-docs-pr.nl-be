---
title: Werken met rapportageschema's| Microsoft Docs
description: "Beschrijft hoe u rapportageschema's gebruikt om diverse weergaven en lijsten te maken om financiële prestatiegegevens te analyseren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7b28d3ec6f4a52c5229d2e121ff1fe8ed847eeb7
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-account-schedules"></a>Werken met rekeningschema's
Gebruik rapportageschema's om inzicht te krijgen in de financiële gegevens die in uw rekeningschema zijn opgeslagen. Met rapportageschema's worden cijfers geanalyseerd in grootboekrekeningen en worden grootboekposten vergeleken met budgetposten voor het grootboek. De resultaten worden weergegeven in diagrammen in uw rolcentrum, zoals het cashflowdiagram.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] biedt een aantal voorbeeldrapportageschema's die u direct kunt gebruiken, of u kunt uw eigen rijen en kolommen instellen om de te vergelijken cijfers op te geven. U kunt bijvoorbeeld rapportageschema's maken om winstmarges te berekenen voor dimensies, zoals afdelingen of klantengroepen. U kunt zoveel aangepaste financiële overzichten maken als u wilt.  

Het instellen van rapportageschema's vereist begrip van de financiële gegevens in het rekeningschema. U kunt bijvoorbeeld grootboekposten weergeven als percentages van budgetposten. Hiertoe moeten budgetten worden gemaakt. Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.

## <a name="account-categories-and-account-schedules"></a>Rekeningcategorieën en rekeningschema's
U kunt rekeningcategorieën gebruiken om de indeling te wijzigen van uw financiële overzichten. Nadat u de rekeningcategorieën hebt ingesteld in het venster **GB-rekeningcategorieën** en u kiest de actie **Rapportageschema's genereren**, worden de onderliggende rapportageschema's voor de financiële kernrapporten bijgewerkt. De volgende keer dat u een van deze rapporten uitvoert, zoals het saldo-overzicht, worden nieuwe totalen en subposten toegevoegd op basis van uw wijzigingen. Zie voor meer informatie [Het grootboek en het rekeningschema](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Nieuwe rekeningstelsels maken  
 U kunt rekeningstelsels gebruiken om de cijfers in grootboekrekeningen te analyseren, of om grootboekposten te vergelijken met grootboekbegrotingsposten. U kunt bijvoorbeeld de grootboekposten weergeven als percentages van de begrotingsposten.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een rekeningschema te maken.
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de actie **Rapportageschema bewerken**.
5. Vul de benodigde velden in het venster **Rapportageschema** in.  

    Nadat u een nieuw rapportageschema hebt gemaakt en de rijen hebt ingesteld, moet u kolommen instellen. U kunt de kolommen handmatig instellen of een vooraf gedefinieerde kolomindeling toewijzen aan het rapportageschema.
6. Kies de actie **Instellingen kolomindeling bewerken**.
7. Vul indien nodig in het venster **Kolomindeling** de velden in.

> [!NOTE]  
>   Als u geen standaardkolomindeling hebt toegewezen aan het rapportageschema, moet u de kolommen handmatig instellen.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Een kolom maken die percentages berekent  
U wilt mogelijk soms een kolom opnemen in een rekeningschema om percentages van een totaal te berekenen. U hebt bijvoorbeeld een aantal rijen die zijn onderverdeeld op dimensie, en u wilt wellicht een kolom maken om het percentage aan te geven van de totale verkoop van elke rij.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer een rapportageschema in het venster **Rapportageschema's**.  
3. Kies de actie **Rapportageschema bewerken** om een rapportageschemarij te definiëren die de totalen moet berekenen waarop de percentages worden gebaseerd.  
4. Voeg een regel in rechtstreeks boven de eerste rij waarvoor u een percentage wilt weergeven.  
5. Vul de velden als volgt op de regel in: voer in het veld **Samentellingssoort** **Basis voor percentage** in. Voer in het veld **Samentelling** een formule in voor het totaal waarop het percentage wordt gebaseerd. Als bijvoorbeeld rij 11 de totale omzet bevat, voert u **11** in.  
6. Kies de actie **Instellingen kolomindeling bewerken** om een kolom in te stellen.  
7. Vul de velden als volgt op de regel in: selecteer in het veld **Kolomsoort** **Formule**. Voer in het veld **Formule** een formule in voor het bedrag waarvoor u een percentage wilt berekenen, gevolgd door %. Bijvoorbeeld, als kolomnummer N de mutatie bevat, voert u **N%** in.  
8. Herhaal stap 4 tot en met 7 voor elke groep rijen die u wilt uitsplitsen op percentage.

## <a name="to-set-up-account-schedules-with-overviews"></a>Rekeningstelsels met overzichten instellen  
U kunt een rekeningstelsel gebruiken om een rekeningoverzicht te maken waarin grootboekcijfers en begrotingscijfers van grootboeken worden vergeleken.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer een rapportageschema in het venster **Rapportageschema's**.  
3. Kies de actie **Rapportageschema bewerken**  
4. Selecteer in het venster **Rapportageschema** in het veld **Naam** de naam van het standaardrapportageschema.
5. Kies de actie **Rekeningen invoegen**.  
6. Selecteer de rekeningen die u wilt opnemen in uw overzicht en klik vervolgens op **OK**.

    De rekeningen worden nu opgenomen in het rapportageschema. Indien gewenst kunt u ook de kolomindeling wijzigen.  
7. Kies de actie **Overzicht**.  
8. Stel op het sneltabblad **Dimensiefilters** het begrotingsfilter in met de gewenste filternaam.  
9. Kies de knop **Ok**.  

Nu kunt u het budgetoverzicht kopiëren en in een spreadsheet plakken.

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

