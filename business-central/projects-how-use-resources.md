---
title: Resourcegebruik en prijzen vastleggen en aanpassen
description: 'Beschrijft hoe u het resourcegebruik of -verbruik kunt vastleggen dat is gekoppeld aan een project, om kosten, prijzen en werksoorten bij te houden en te beheren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '201,206, 207, 271, 493'
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="use-resources-for-jobs"></a>Resources gebruiken voor projecten

U legt het gebruik van resources vast in het projectdagboek om kosten, prijzen en de werksoorten bij te houden die zijn gekoppeld aan projecten. Zie voor meer informatie [Gebruik vastleggen voor projecten](projects-how-record-job-usage.md).

> [!NOTE]
> U kunt ook externe resources aanschaffen, bijvoorbeeld om een leverancier te factureren voor het geleverde werk. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).

U kunt ook het verbruik van een resource boeken in een resourcedagboek. Posten die in een resourcedagboek zijn geboekt, werken niet door in het grootboek.

## <a name="to-assign-resources-to-jobs"></a>Resources toewijzen aan projecten

U wijst resources aan projecten toe door projectplanningsregels voor het project te maken. Zie voor meer informatie [Projecten maken](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Resourceverbruik voor een project vastleggen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projectjournalen** in en kies vervolgens de gerelateerde koppeling.
2. Open een relevante projectdagboekbatch en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wanneer het dagboek compleet is, kiest u de actie **Boeken**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-adjust-resource-prices"></a>Resourceprijzen aanpassen

Als u kost- of verkoopprijzen wilt wijzigen voor een groot aantal resources, kunt u een batchverwerking gebruiken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resourceprijzen herwaarderen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de overige velden op een regel desgewenst in en kies de knop **OK**.

> [!NOTE]  
> Met deze batchverwerking worden geen alternatieve kosten of prijzen voor resources gemaakt of aangepast. Dit verandert alleen de inhoud van het veld op de resourcekaart voor het veld **Aan te passen prijs** dat u hebt geselecteerd in de batchtaak. De aanpassing werkt onmiddellijk door voor de resources. Controleer daarom uw herwaarderingsfactoren zorgvuldig voordat u de batchverwerking uitvoert.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Suggesties voor wijzigingen van resourceprijzen krijgen op basis van bestaande alternatieve prijzen

Als u al alternatieve resourceprijzen hebt ingesteld voor bepaalde resources, kunt u een batchverwerking gebruiken om meerdere alternatieve resourceprijzen in te stellen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resourceprijswijzigingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Res.prijsvoorstellen (Prijs)** en vul indien nodig de velden in.
3. Kies de knop **OK**.  
4. Nadat de batchverwerking is voltooid, bevat de pagina **Resourceprijswijzigingen** de resultaten van de batchverwerking.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Resourceprijsvoorstellen ophalen op basis van standaardverkoopprijzen

Als u meerdere alternatieve resourceprijzen wilt instellen op basis van de standaardverkoopprijzen op de resourcekaarten, kunt u een batchverwerking gebruiken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resourceprijswijzigingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Res.prijsvoorstellen (Res.)** en vul indien nodig de velden in.  
3. Kies de knop **Ok**.  
4. Nadat de batchverwerking is voltooid, opent u de pagina **Resourceprijswijzigingen** om de resultaten van de batchverwerking te bekijken.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Suggesties voor wijzigingen van resourceprijzen krijgen op basis van alternatieve prijzen

Als u al alternatieve resourceprijzen hebt ingesteld voor bepaalde resources, kunt u een batchverwerking gebruiken om meerdere alternatieve resourceprijzen in te stellen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Res.prijsvoorstellen (Prijs)** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in.
3. Kies de knop **Ok**.  
4. Nadat de batchverwerking is voltooid, opent u de pagina **Resourceprijswijzigingen** om de resultaten van de batchverwerking te bekijken.

## <a name="see-also"></a>Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)         
[Verkoop](sales-manage-sales.md)     
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
