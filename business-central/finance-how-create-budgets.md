---
title: Grootboekbudgetten maken
description: Hier wordt beschreven hoe u grootboekbudgetten maakt om verschillende financiële activiteiten te prognosticeren en dimensies toewijst voor bedrijfsinformatiedoeleinden.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="create-gl-budgets"></a>Grootboekbudgetten maken

U kunt budgetten met aparte namen maken als u meerdere budgetten wilt gebruiken voor dezelfde perioden. Eerst stelt u de begrotingsnaam in en voert u de begrotingscijfers in. De begrotingsnaam wordt vervolgens opgenomen op alle begrotingsposten die u maakt.  

Wanneer u een budget maakt, kunt u voor elk budget vier budgetspecifieke dimensies toewijzen, budgetdimensies genoemd. U kunt budgetdimensies gebruiken om filters in te stellen op een budget en dimensiegegevens aan budgetposten toe te voegen. Zie [Werken met dimensies](finance-dimensions.md) voor meer informatie.

Budgetten spelen een belangrijke rol bij bedrijfsinformatie. Voorbeelden zijn een financieel overzicht op basis van financiële rapporten die budgetposten bevatten of wanneer gebudgetteerde en werkelijke bedragen in het rekeningschema worden geanalyseerd. Meer informatie vindt u op [Bedrijfsinformatie](bi.md).

In kostenadministratie werkt u met kostenbudgetten op een soortgelijke manier. Zie voor meer informatie [Kostenbudgetten maken](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Een nieuw grootboekbudget maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekbudgetten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Lijst bewerken** en vul vervolgens indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Kies de actie **Budget bewerken**.
4. Vul boven aan de pagina **Budget** de benodigde velden in om te definiëren wat wordt weergegeven.  

   De pagina toont alleen posten met de budgetnaam die u hebt ingevoerd in het veld **Budgetnaam**. Aangezien u de budgetnaam net hebt gemaakt, zijn er geen posten die overeenkomen met het filter. Daarom is de pagina leeg.  
5. Voer een bedrag in door op de betreffende cel in de matrix te klikken. De pagina **Grootboekbudgetposten** verschijnt.  
6. Maak een nieuwe regel en vul het veld **Bedrag** in. Sluit de pagina **Grootboekbudgetposten**.  
7. Herhaal stap 5 en 6 voor alle bedragen in het budget.  

> [!NOTE]  
> Op het sneltabblad **Filters** kunt u de budgetinformatie filteren op de budgetdimensies die u hebt ingesteld onder de budgetnaam.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Grootboekbudgetten exporteren en importeren met Excel

Zoals bij vrijwel alle overige pagina's kunt u gegevens op budgetpagina's naar Microsoft Excel exporteren voor verdere verwerking of analyse. Voor meer informatie: [Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md).

> [!NOTE]
> Het rekeningschema waarop de grootboekbudgetten zijn gebaseerd, bevat regels van het rekeningtype Kop. Deze regels bevatten het totaal van de regels eronder. Wanneer u een grootboekbudget exporteert, exporteert u gegevens op alle regels, ongeacht het rekeningtype. U kunt echter alleen gegevens importeren op regels van het rekeningtype Boeking.

Wanneer u dus een grootboekbudget importeert, worden eventuele waarden op kopregels ook verwijderd. Ze worden verwijderd om onjuiste totalen te voorkomen nadat u gegevens importeert die in Excel zijn gemaakt of bewerkt.

### <a name="scenario"></a>Scenario

U weet dat de nieuwe gebudgetteerde salarissenkosten 1.200.000 lokale valuta (LV) zullen zijn. U wilt de afdeling Salarissen laten budgetteren voor drie specifieke regels (van het rekeningtype Boeking) voor fulltime werknemers, parttime werknemers en invalkrachten. De drie regels worden gegroepeerd onder de kopregel Salarissen.

U voert 1.200.000 in op de kopregel, exporteert het budget naar Excel en stuurt het vervolgens naar de afdeling Salarissen, waarbij u hen aangeeft de LV 1.200.000 te distribueren.

De afdeling Salarissen distribueert het bedrag over de drie boekingsrekeningen. Wanneer u terug importeert in het grootboekbudget, worden de drie rekeningen ingevuld met de nieuwe Excel-gegevens, tot een totaal van 1.200.000, en is de kopregel leeg.

## <a name="see-also"></a>Zie ook

[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)  
[Financiën](finance.md)  
[Bedrijfsinformatie](bi.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
