---
title: Gegevens analyseren per dimensie| Microsoft Docs
description: Beschrijft hoe u diverse bedrijfsgegevens analyseert per dimensie.
services: project-madeira
documentationcenter: ''
author: edupont
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4086da516f9a1ecccf5a3a0c2f86d0f42877b637
ms.sourcegitcommit: edac6cbb8b19ac426f8dcbc83f0f9e308fb0d45d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/29/2020
ms.locfileid: "4817091"
---
#  <a name="analyze-data-by-dimensions"></a>Gegevens analyseren per dimensie
In financiële analyses is een dimensie informatie die u kunt toevoegen aan een post als een soort kenteken. Deze informatie wordt gebruikt om posten met vergelijkbare kenmerken te groeperen, zoals klanten, regio's, producten en verkopers, en om deze groepen eenvoudig op te kunnen roepen voor analyse. Dimensies kunnen worden gebruikt op posten in dagboeken, documenten en budgetten. De term dimensie beschrijft hoe analyse plaatsvindt. Een tweedimensionale analyse is bijvoorbeeld verkoop per gebied. Door echter meer dan twee dimensies te gebruiken bij het maken van een post, kunt u complexere analyses uitvoeren, zoals verkoop per verkoopcampagne per klantengroep per gebied. Zie voor meer informatie [Werken met dimensies](finance-dimensions.md).

Door gegevens met dimensies te analyseren krijgt u een beter inzicht in uw bedrijf, zodat u informatie kunt evalueren, zoals hoe goed uw bedrijf draait, waar de zaken floreren en waar juist niet en waar meer resources moeten worden ingezet.

> [!TIP]
> Als snelle manier om transactiegegevens te analyseren per dimensie kunt u totalen in het rekeningschema en posten op de pagina's **Posten** filteren op dimensie. Zoek de actie **Dimensiefilter instellen**.

## <a name="to-set-up-an-analysis-view"></a>Een analyseweergave instellen  
Met een analyse op basis van dimensies geeft u een geselecteerde combinatie van dimensies weer. U kunt elke ingestelde analyse opslaan en ophalen. De gegevens voor het instellen van een analyse worden op een **Analyseweergave** kaart opgeslagen om analyse in de toekomst te vereenvoudigen.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Analyseweergaven** in en kies de desbetreffende koppeling.  
2. Kies op de pagina **Analyseweergaveoverzicht** de actie **Nieuw**.
3. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Als u andere dimensiecodes wilt toevoegen naast de vier op het sneltabblad **Dimensies**, kiest u de actie **Filteren**, vult u de velden in en kiest u de knop **OK**.  
5. Als u de weergave wilt bijwerken, kiest u de actie **Bijwerken**.

## <a name="to-analyze-by-dimensions"></a>Analyseren per dimensie
U kunt de matrix **Analyse per dimensie** gebruiken om de bedragen in uw grootboek te bekijken met de analyseweergaven die u al hebt ingesteld. U vult de pagina **Analyse per dimensie** in om te bepalen wat wordt weergegeven in de matrix en kiest vervolgens de actie **Matrix weergeven** om de matrix weer te geven.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Analyseweergaven** in en kies de desbetreffende koppeling.  
2. Selecteer de relevante analyseweergave en kies vervolgens de actie **Analyse per dimensie**.
3. Vul boven op de pagina **Analyse per dimensie** de velden in om te definiëren wat wordt weergegeven.
4. Kies de actie **Matrix weergeven** om de desbetreffende matrixpagina voor die analyseweergave te openen.
5. Als u wilt weten uit welke bedragen een bedrag op de matrixpagina bestaat, selecteert u het bedrag.  

- De kolommen aan de verre linkerzijde bevatten gegevens op basis van de selectie in het veld **Als regels weergeven** in de kop.  
- De kolommen aan de verre rechterzijde bevatten gegevens op basis van de selectie in het veld **Als kolommen weergeven** in de kop.

> [!IMPORTANT]  
>   U kunt geen periode selecteren die korter is dan de opgegeven periode voor datumcompressie op de **Analyseweergave**-kaart. De opdrachten **Volgende set** en **Vorige set** zijn niet ingeschakeld als u **Periode** hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven**.  

> [!NOTE]  
>   Met de lijst **Dimensies - detail** kunt u een gedetailleerde classificatie weergeven van de wijze waarop dimensies zijn gebruikt voor posten gedurende een geselecteerde periode. Gebruik de lijst **Dimensies - totaal** voor een overzicht van de totale bedragen.  

> [!TIP]  
>   U kunt de weergave ook wijzigen door de inhoud van het veld **Als regels weergeven** en het veld **Als kolommen weergeven** te veranderen. Als u een weergave-instelling wilt omkeren, kiest u de actie **Regels en kolommen omkeren**.

## <a name="to-update-an-analysis-view"></a>Analyseweergave bijwerken  
Met de bedragen die worden weergegeven op de pagina **Analyse per dimensies**, krijgt u een overzicht van de status van het bedrijf die gold op het moment dat u voor het laatst hebt bijgewerkt. Als u de huidige status wilt weten, moet u de analyseweergave bijwerken.

Met de volgende procedure kunt u een analyseweergave bijwerken vanuit de pagina **Analyse per dimensies**. De stappen zijn vergelijkbaar vanuit de pagina's **Analyseweergave** en **Analyseweergaveoverzicht**.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Analyseweergaven** in en kies de desbetreffende koppeling.
2. Selecteer de relevante analyseweergave en kies vervolgens de actie **Analyse per dimensie**.
2. Kies op de pagina **Analyse per dimensie** het veld **Analyseweergavecode**.  
3. Selecteer de regel met de gewenste analyseweergave.  
4. Selecteer op de pagina **Analyseweergaven** de relevante analyseweergave en kies vervolgens de actie **Bijwerken**.  

> [!TIP]  
>   Als u het selectievakje **Bijwerken bij boeking** op een analyseweergavekaart selecteert, wordt de weergave automatisch bijgewerkt wanneer een desbetreffende transactie wordt geboekt.

> [!NOTE]  
>   Als u bepaalde of alle analyseweergaven tegelijk wilt bijwerken, moet u de batchverwerking **Analyseweergaven bijwerken** gebruiken.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met dimensies](finance-dimensions.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]