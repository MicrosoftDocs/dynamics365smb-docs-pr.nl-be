---
title: Gegevens analyseren per dimensie| Microsoft Docs
description: Beschrijft hoe u diverse bedrijfsgegevens analyseert per dimensie.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/13/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: aebeb7a0e3a5fa83ba329bf222c50492f9cb003a
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
#  <a name="how-to-analyze-data-by-dimensions"></a>Procedure: Gegevens analyseren per dimensie
In financiële analyses is een dimensie informatie die u kunt toevoegen aan een post als een soort kenteken. Deze informatie wordt gebruikt om posten met vergelijkbare kenmerken te groeperen, zoals klanten, regio's, producten en verkopers, en om deze groepen eenvoudig op te kunnen roepen voor analyse. Dimensies kunnen worden gebruikt op posten in dagboeken, documenten en budgetten. De term dimensie beschrijft hoe analyse plaatsvindt. Een tweedimensionale analyse is bijvoorbeeld verkoop per gebied. Door echter meer dan twee dimensies te gebruiken bij het maken van een post, kunt u complexere analyses uitvoeren, zoals verkoop per verkoopcampagne per klantengroep per gebied. Zie voor meer informatie [Werken met dimensies](finance-dimensions.md).

Door gegevens met dimensies te analyseren krijgt u een beter inzicht in uw bedrijf, zodat u informatie kunt evalueren, zoals hoe goed uw bedrijf draait, waar de zaken floreren en waar juist niet en waar meer resources moeten worden ingezet.

> [!TIP]
> Als snelle manier om transactiegegevens te analyseren per dimensie kunt u totalen in het rekeningschema en posten in de vensters **Posten** filteren op dimensie. Zoek de actie **Dimensiefilter instellen**.

> [!NOTE]  
>   Deze functionaliteit vereist dat uw ervaring is ingesteld op **Suite**. Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).

## <a name="to-set-up-an-analysis-view"></a>Een analyseweergave instellen  
Met een analyse op basis van dimensies geeft u een geselecteerde combinatie van dimensies weer. U kunt elke ingestelde analyse opslaan en ophalen. De gegevens voor het instellen van een analyse worden op een **Analyseweergave**kaart opgeslagen om analyse in de toekomst te vereenvoudigen.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Analyseweergaven** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **Analyseweergaveoverzicht** de actie **Nieuw**.
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Als u andere dimensiecodes wilt toevoegen naast de vier op het sneltabblad **Dimensies**, kiest u de actie **Filteren**, vult u de velden in en kiest u de knop **OK**.  
5. Als u de weergave wilt bijwerken, kiest u de actie **Bijwerken**.

## <a name="to-analyze-by-dimensions"></a>Analyseren per dimensie
U kunt de matrix **Analyse per dimensie** gebruiken om de bedragen in uw grootboek te bekijken met de analyseweergaven die u al hebt ingesteld. U vult het venster **Analyse per dimensie** in om te bepalen wat wordt weergegeven in de matrix en kiest vervolgens de actie **Matrix weergeven** om de matrix weer te geven..  

- De kolommen aan de verre linkerzijde bevatten gegevens op basis van de selectie in het veld **Als regels weergeven** in de kop.  
- De kolommen aan de verre rechterzijde bevatten gegevens op basis van de selectie in het veld **Als kolommen weergeven** in de kop.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Analyse per dimensie** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer de relevante analyseweergave en kies vervolgens de actie **Analyseweergave bewerken**.
3. Vul boven in het venster **Analyse per dimensie** de velden in om te definiëren wat wordt weergegeven.
4. 5. Als u wilt weten uit welke bedragen een bedrag in de matrix bestaat, selecteert u het bedrag.  

> [!IMPORTANT]  
>   U kunt geen periode selecteren die korter is dan de opgegeven periode voor datumcompressie op de **Analyseweergave**-kaart. De opdrachten **Volgende set** en **Vorige set** zijn niet ingeschakeld als u **Periode** hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven**.  

> [!NOTE]  
>   Met de lijst **Dimensies - detail** kunt u een gedetailleerde classificatie weergeven van de wijze waarop dimensies zijn gebruikt voor posten gedurende een geselecteerde periode. Met de lijst **Dimensies - totaal** kunt u alleen de totale bedragen weergeven.  

> [!TIP]  
>   U kunt de weergave ook wijzigen door de inhoud van het veld **Als regels weergeven** en het veld **Als kolommen weergeven** te veranderen. Als u een weergave-instelling wilt omkeren, kiest u de actie **Regels en kolommen omkeren**.

## <a name="to-update-an-analysis-view"></a>Analyseweergave bijwerken  
Met de bedragen die worden weergegeven in het venster **Analyse per dimensies**, krijgt u een overzicht van de status van het bedrijf die gold op het moment dat u voor het laatst hebt bijgewerkt. Als u de huidige status wilt weten, moet u de analyseweergave bijwerken.

Met de volgende procedure kunt u een analyseweergave bijwerken vanuit het venster **Analyse per dimensies**. De stappen zijn vergelijkbaar vanuit het venster **Analyseweergave** en **Analyseweergaveoverzicht**.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Analyse per dimensie** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **Analyse per dimensie** het veld **Analyseweergavecode**.  
3. Selecteer de regel met de gewenste analyseweergave.  
4. Kies de actie **Bijwerken**.  

> [!TIP]  
>   Als u het selectievakje **Bijwerken bij boeking** op een analyseweergavekaart selecteert, wordt de weergave automatisch bijgewerkt wanneer een desbetreffende transactie wordt geboekt.

> [!NOTE]  
>   Als u bepaalde of alle analyseweergaven tegelijk wilt bijwerken, moet u de batchverwerking **Analyseweergaven bijwerken** gebruiken.  

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met dimensies](finance-dimensions.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

