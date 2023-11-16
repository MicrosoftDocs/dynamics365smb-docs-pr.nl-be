---
title: Budgetten voor vaste activa beheren
description: 'U stelt gegevens over toekomstige investeringen, buitengebruikstellingen en afschrijvingen van vaste activa in om te helpen budgetten en prognoses voor te bereiden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.search.form: '5610, 5611'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="manage-budgets-for-fixed-assets"></a>Budgetten voor vaste activa beheren.

U kunt gebudgetteerde vaste activa instellen. Hiermee kunt u bijvoorbeeld verwachte aan- en verkopen opnemen in lijsten.  

Als u de gebudgetteerde resultaten, de gebudgetteerde balans en het kasbudget wilt voorbereiden, hebt u informatie nodig over toekomstige investeringen, buitengebruikstellingen en afschrijvingen van vaste activa. U kunt deze informatie vinden in de lijst **Vast activum - Geschatte waarde**. Voordat u deze lijst afdrukt, moet u het budget voorbereiden.  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>De aanschafkosten van een vast activum budgetteren

U kunt een budget voorbereiden door kaarten in stellen voor de vaste activa die u in de toekomst wilt kopen. De gebudgetteerde vaste activa worden ingesteld als gewone vaste activa instellen, maar deze moeten zo worden ingesteld dat ze niet naar het grootboek worden geboekt.

Wanneer u de aanschafkosten boekt, voert u het nummer van het gebudgetteerde vaste activum in het veld **VA-nr. (Budget)** in. Hierdoor worden de aanschafkosten geboekt met een tegengesteld teken voor het gebudgetteerde activum. Dit betekent dat de totale aanschafkosten voor het gebudgetteerde activum worden gevormd door het verschil tussen de gebudgetteerde en de werkelijke aanschafkosten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Als u een nieuwe VA-kaart wilt maken voor het gebudgetteerde vaste activum, kiest u de actie **Nieuw**.
3. Schakel het selectievakje **Gebudgetteerd activum** in om boekingen naar het grootboek te voorkomen.
4. Vul de overige velden in, wijs een afschrijvingsboek toe en boek vervolgens de eerste aanschafkosten met het gebudgetteerde vaste activum dat in het veld **VA-nr. (budget)** op de dagboekregel is ingevoerd Zie [Vaste activa aanschaffen](fa-how-acquire.md) voor meer informatie.

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>De buitengebruikstelling van een vast activum budgetteren

Als u activa binnen de budgetperiode wilt verkopen, kunt u informatie over verkoopprijzen en -datums opgeven.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum dat buiten gebruik moet worden gesteld en kies vervolgens de actie **Afschrijvingsboeken**.
3. Op de pagina **VA-afschrijvingsboeken** vult u de velden **Verwachte BGS-datum** en **Verwachte opbrengst bij BGS** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>Geschatte buitengebruikstellingswaarden bekijken

Als u de geschatte buitengebruikstellingswaarden wilt bekijken en verlies en winst wilt berekenen, kunt u het rapport **Geschatte waarde VA** gebruiken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geschatte waarde VA** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden in.
3. Kies de knop **Afdrukken** of **Voorbeeld**.

## <a name="to-budget-depreciation"></a>Afschrijvingen budgetteren

U kunt het rapport **Vast activum - Geschatte waarde** gebruiken om toekomstige afschrijving te berekenen. Het rapport laat de boekwaarde en gecumuleerde afschrijving aan het begin van de geselecteerde periode zien, wijzigingen gedurende de periode en de boekwaarde en gecumuleerde afschrijving aan het eind van de geselecteerde periode.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geschatte waarde van vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Vul de velden in.
3. Als u de totale waarden voor alle activa wilt bekijken, schakelt u het selectievakje **Per VA afdrukken** uit.
4. Laat het sneltabblad **Vast activum** leeg, zodat alle activa in de lijst worden opgenomen. Stel het veld **Alleen budget** in op **Nee** om gebudgetteerde activa uit te sluiten, of stel het veld in op **Ja** om alleen gebudgetteerde activa te zien.
5. Kies de knop **Afdrukken** of **Voorbeeld**.

## <a name="see-also"></a>Zie ook

[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Financiën](finance.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
