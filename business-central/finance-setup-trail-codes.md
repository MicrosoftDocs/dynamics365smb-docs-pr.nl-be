---
title: Codes instellen voor audittrails
description: Lees meer over de taken om broncodes en redencodes in te stellen die u kunt gebruiken om audittrails bij te houden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Broncodes en redencodes instellen voor audittrails

Aan alle geboekte posten wordt automatisch een broncode toegewezen zodat transacties tot aan hun herkomst kunnen worden getraceerd. Als u aan posten een aanvullende broncode wilt toewijzen, kunt u redencodes gebruiken. Met redencodes wordt aangegeven waarom een post is gemaakt. Wanneer u redencodes instelt, kunt u deze toewijzen aan volledige dagboeksjablonen en -batches en aan afzonderlijke dagboekregels en -documenten.  

Gebruik voor zowel broncodes als redencodes codes die gemakkelijk te onthouden en beschrijvend zijn. De code moet uniek zijn en u kunt zoveel codes instellen als u maar wilt.

## <a name="define-source-codes"></a>Broncodes definiëren

In bepaalde gevallen wilt u nagaan hoe een bepaalde post ontstaan is, bijvoorbeeld of de post afkomstig is van de boeking van een dagboek of een inkoopfactuur. Met een broncode wordt de herkomst van een post aangeduid. Posten worden gemaakt wanneer u dagboeken en facturen boekt en bepaalde batchverwerkingen uitvoert. Elke boekingssoort heeft een bepaalde broncode, die wordt toegewezen wanneer afzonderlijke posten worden gemaakt.  

Bij het boeken van dagboeken, orders, facturen of creditnota's en bij het uitvoeren van de verschillende batchverwerkingen worden posten in de financiële overzichten gemaakt. Het venster **Broncode-instelling** bevat meerdere sneltabbladen, één voor elk toepassingsgebied. Elk sneltabblad bevat de broncode die van toepassing is op dat toepassingsgebied.

Wanneer u een batchverwerking boekt of uitvoert, wordt de juiste broncode automatisch aan de post gekoppeld. Als u bijvoorbeeld boekt vanuit het financieel dagboek, wordt de post gecodeerd als *FINDAGB*. Vervolgens kunt u de pagina **Grootboekposten** filteren om te laten zien welke boekingen bijvoorbeeld vanuit het dagboek of uit verkoopdocumenten zijn geboekt

### <a name="to-define-source-codes"></a>Broncodes definiëren

1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Broncode-instelling** in en kies vervolgens de gerelateerde koppeling.  

2. Geef in het venster **Broncode-instelling** voor elk boekingstype en elke batchtaak de relevante broncode op.  

U kunt de inhoud van een veld later wijzigen en die wijziging heeft dan invloed op toekomstige berichten.

## <a name="change-source-codes"></a>Broncodes wijzigen

U wilt wellicht een broncode wijzigen. U wilt bijvoorbeeld de broncode *DAGBOEK* wijzigen in *DAGB*.

### <a name="to-change-source-codes"></a>Broncodes wijzigen

1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Broncodes** in en kies vervolgens de gerelateerde koppeling.

2. Selecteer op de regel met de te wijzigen code de code in het veld **Code**.

3. Voer de nieuwe code in en kies vervolgens de knop **Ja**. U kunt de inhoud van het veld **Omschrijving** ook wijzigen.

De nieuwe posten die worden geboekt uit het dagboek, hebben de nieuwe broncode.

## <a name="define-reason-codes"></a>Redencodes definiëren

Redencodes vullen de broncodes aan en worden gebruikt om aan te geven waarom een post is gemaakt. U kunt redencodes toewijzen aan afzonderlijke posten en u kunt permanente codes toewijzen aan bepaalde dagboeksjablonen en -batches. Wanneer een redencode aan een dagboekregel of een verkoop- of inkoopkop is gekoppeld, worden alle posten met de redencode gemarkeerd wanneer deze worden geboekt.  

### <a name="to-set-up-reason-codes"></a>Redencodes instellen

1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"),  voer **Redencodes** in en kies vervolgens de gerelateerde koppeling.

2. Voer in het venster **Redencodes** de eerste code in het veld **Code** in. Typ een uitleg in het veld **Omschrijving**.

Herhaal de procedure voor elke code die u wilt gebruiken. U kunt een onbeperkt aantal codes instellen.

De volgende procedure beschrijft hoe u een redencode aan een dagboeksjabloon kunt toevoegen, maar vergelijkbare stappen zijn van toepassing op het toevoegen van een redencode aan een dagboekregel of dagboekbatch.  

### <a name="to-assign-reason-codes-to-journal-templates"></a>Redencodes toewijzen aan dagboeksjablonen

1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"),  voer **Fin. dagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.

2. Geef in het veld **Redencode** op de regel met de geselecteerde dagboeksjabloon de relevante code op.

3. Sluit de dagboeksjabloon.

De geselecteerde redencode wordt gekopieerd naar nieuwe dagboekbatches die met deze dagboeksjabloon worden gemaakt. Op dezelfde manier kunt u redencodes toewijzen aan dagboeksjablonen in andere toepassingsgebieden.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>Redencodes gebruiken voor verkoop- en inkoopdocumenten

1. Open het betreffende verkoop- of inkoopdocument.

2. Voer de code in het veld **Redencode** op de verkoop- of inkoopkop in.

Wanneer de factuur wordt geboekt, wordt de redencode gekopieerd naar elke grootboek-, klant- en leverancierspost. U kunt geen andere redencodes toewijzen aan afzonderlijke inkoop- en verkoopregels, omdat de regels als één post zijn geboekt.

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)  
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Werken met dimensies](finance-dimensions.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Cashflow in uw bedrijf analyseren](finance-analyze-cash-flow.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
