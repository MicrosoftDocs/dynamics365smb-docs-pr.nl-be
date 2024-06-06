---
title: 'Projectresourcekosten, prijzen en capaciteit instellen'
description: 'Als u resources wilt gebruiken en projectbeheer wilt mogelijk maken, geeft u kosten en prijzen voor afzonderlijke resources of resourcegroepen op en stelt u de resourcecapaciteit in.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-resources-for-projects"></a>Resources instellen voor projecten

Om resourceactiviteiten correct te beheren, moet u resources en de bijbehorende kosten en prijzen instellen. De aan projecten gerelateerde prijzen, kortingen en kostenfactorregels worden ingesteld op de projectkaart. U kunt de kosten en prijzen opgeven voor afzonderlijke resources, resourcegroepen of alle beschikbare resources van het bedrijf.

Wanneer resources worden gebruikt of verkocht voor een project, worden de bijbehorende prijzen en kosten opgehaald uit de informatie die u instelt.

Bij het maken van de resource geeft u het standaardbedrag per uur op. Als u bijvoorbeeld 5 uur lang een specifieke machine gebruikt voor een project, worden de kosten van het project gebaseerd op de kosten per uur.

> [!NOTE]
> U kunt ook externe resources aanschaffen, bijvoorbeeld om een leverancier te factureren voor het geleverde werk. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).<br /><br />
> Voor externe resources is het raadzaam om ze een naam te geven of te groeperen, zodat ze niet worden verward met uw interne resources.
>  
> Als u intercompany-transacties boekt, hoewel u een resource op een regel op een verkooporder kunt plaatsen, wordt de resource niet opgenomen als u de verkooporder omzet in een inkooporder aan de ontvangende zijde. Als u resources wilt gebruiken in intercompany-transacties, gebruikt u het veld **Grootboekrekeningnr. IC-aankoop** op de resourcekaart om de rekening op te geven waarnaar de uitgaven moeten worden geboekt.

## <a name="to-set-up-a-resource"></a>Een resource instellen

Maak een kaart per resource die u wilt gebruiken in projecten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resources** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Een gebruikersgroep instellen

U kunt meerdere resources in één resourcegroep combineren. De capaciteit en budgetten van individuele resources worden bij elkaar opgeteld en vormen de capaciteit en het budget voor de resourcegroep. Het is ook mogelijk om capaciteit op te geven voor de resourcegroepen die los staat van de opgetelde waarden, of een aanvulling hierop vormt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resourcegroepen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden in.

## <a name="to-set-capacity-for-a-resource"></a>Capaciteit voor een resource instellen

Om te berekenen hoeveel tijd een resource aan projecten kan besteden moet de capaciteit ervan eerst worden ingesteld als beschikbare tijd per periode op de werkagenda. Deze instelling wordt gebruikt als u projectplanningsregels invult die de resource bevatten. Zie voor meer informatie [Projecten maken](projects-how-create-jobs.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resources** in en kies vervolgens de gerelateerde koppeling.
2. Open de desbetreffende resourcekaart en kies vervolgens de actie **Resourcecapaciteit**.
3. Geef op de pagina **Resourcecapaciteit** in het veld **Weergeven per** de lengte van de periode op, zoals **Dag**, die wordt weergegeven in kolommen op het sneltabblad **Resourcecapaciteitsmatrix**.
4. Geef voor elke resource op een regel voor elke periode in de kolommen het aantal uren op dat de resource beschikbaar is.
5. Of, als u de wekelijke capaciteit van de resource wilt detailleren met een begin- en een einddatum, kiest u de actie **Capaciteit instellen**.
6. Vul op de pagina **Resourcecapaciteitsinstellingen** indien nodig de velden in.
7. Kies de actie **Capaciteit bijwerken**. De pagina **Resourcecapaciteit** wordt bijgewerkt met de ingevoerde capaciteit.
8. Sluit de pagina.

## <a name="to-set-up-alternate-resource-costs"></a>Alternatieve resourcekosten instellen

Naast de kosten die op de resourcekaart worden opgegeven, kunt u alternatieve kosten voor elke resource instellen. Als een werknemer bijvoorbeeld een hoger uurtarief heeft voor overwerk, kunt u een resourcekostprijs voor het overwerktarief instellen. De alternatieve kostprijs die u voor de resource instelt, vervangt de kostprijs op de resourcekaart wanneer u de resource in het resourcedagboek gebruikt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resources** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de resource waarvoor u een of meerdere alternatieve kosten wilt instellen en kies vervolgens de actie **Kosten**.  
3. Vul op de pagina **Resourcekostprijzen** indien nodig de velden op een regel in.  
4. Herhaal stap 3 voor elke alternatieve resourcekostprijs die u wilt instellen.

**Opmerking**. Als u resourcekostprijzen wilt instellen die gelden voor alle resources en resourcegroepen, opent u de pagina **Resourcekostprijzen** en vult u de velden in.

## <a name="to-set-up-alternate-resource-prices"></a>Alternatieve resourceprijzen instellen

Naast de prijs die op de resourcekaart wordt opgegeven, kunt u alternatieve prijzen voor elke resource instellen. Deze alternatieve prijzen kunnen voorwaardelijk zijn. Ze kunnen afhankelijk zijn van of de resource met een bepaald project of werksoort wordt gebruikt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resources** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de resource waarvoor u een of meerdere alternatieve prijzen wilt instellen, en kies vervolgens de actie **Prijzen**.
3. Vul op de pagina **Resourceprijzen** indien nodig de velden op een regel in.
4. Herhaal stap 3 voor elke alternatieve resourceprijs die u wilt instellen.

## <a name="see-also"></a>Zie ook

[Projectbeheer instellen](projects-setup-projects.md)  
[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
