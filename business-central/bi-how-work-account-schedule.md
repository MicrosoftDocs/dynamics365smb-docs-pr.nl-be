---
title: "Financiële rapporten maken met rapportageschema's"
description: "Beschrijft hoe u rapportageschema's gebruikt om diverse weergaven en lijsten te maken om financiële prestatiegegevens te analyseren."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: nl-be
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Financiële rapportage voorbereiden met rapportageschema's en rekeningcategorieën
Gebruik rapportageschema's om inzicht te krijgen in de financiële gegevens die in uw rekeningschema zijn opgeslagen. Met rapportageschema's worden cijfers geanalyseerd in grootboekrekeningen en worden grootboekposten vergeleken met budgetposten voor het grootboek. De resultaten worden weergegeven in grafieken in uw rolcentrum, zoals het Cashflowdiagram, en in rapporten, zoals de Resultatenrekening en de Balans.

U opent deze twee rapporten, bijvoorbeeld, met de actie **Financiële afschriften** in de rolcentra Bedrijfsmanager en Accountant.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] biedt een aantal voorbeeldrapportageschema's die u direct kunt gebruiken, of u kunt uw eigen rijen en kolommen instellen om de te vergelijken cijfers op te geven. U kunt bijvoorbeeld rapportageschema's maken om winstmarges te berekenen voor dimensies, zoals afdelingen of klantengroepen. U kunt zoveel aangepaste financiële overzichten maken als u wilt.  

Het instellen van rapportageschema's vereist begrip van de financiële gegevens in het rekeningschema. U kunt bijvoorbeeld grootboekposten weergeven als percentages van budgetposten. Hiertoe moeten budgetten worden gemaakt. Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.

## <a name="account-categories-and-account-schedules"></a>Rekeningcategorieën en rekeningschema's
U kunt rekeningcategorieën gebruiken om de indeling te wijzigen van uw financiële overzichten. Nadat u de rekeningcategorieën hebt ingesteld in het venster **GB-rekeningcategorieën** en u kiest de actie **Rapportageschema's genereren**, worden de onderliggende rapportageschema's voor de financiële kernrapporten bijgewerkt. De volgende keer dat u een van deze rapporten uitvoert, zoals het rapport Balans, worden nieuwe totalen en subposten toegevoegd op basis van uw wijzigingen. Zie voor meer informatie het gedeelte "Rekeningcategorieën" in [Het grootboek en COA begrijpen](finance-general-ledger.md).  

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
> Als u geen standaardkolomindeling hebt toegewezen aan het rapportageschema, moet u de kolommen handmatig instellen.

### <a name="to-copy-an-existing-account-schedule"></a>Een bestaand rekeningschema kopiëren
De rapportageschema's in de standaardversie van [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn de basis van de financiële standaardrapporten, die mogelijk niet overeenkomen met de wensen van uw bedrijf. Als u snel uw eigen financiële rapporten wilt maken, kunt u beginnen met een bestaand rapportageschema te kopiëren.
1. Selecteer in het venster **Rapportageschema** een rapportageschema en kies vervolgens de actie **Rapportageschema kopiëren**.
2. Vul in het venster **Rapportageschema kopiëren** de benodigde velden in en kies vervolgens de knop **OK**.

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

## <a name="comparing-accounting-periods-using-period-formulas"></a>Boekingsperioden vergelijken met behulp van periodeformules
Uw rapportageschema kan de resultaten vergelijken van verschillende boekingsperioden, zoals deze maand vergeleken met dezelfde maand vorig jaar. Daarvoor voegt u een kolom met het veld **Periodevergelijkingsformule** toe en stelt u dat veld in op een periodeformule.  

Een boekhoudperiode hoeft niet gelijk te zijn aan een agendaperiode, maar ieder boekjaar moet hetzelfde aantal boekhoudperioden hebben, zelfs wanneer de boekhoudperioden onderling in lengte verschillen.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt de periodeformule om het bedrag uit de vergelijkingsperiode te berekenen in verhouding tot de periode die wordt voorgesteld door het datumfilter in de rapportaanvraag. De vergelijkingsperiode is gebaseerd op de begindatum van het datumfilter. Dit zijn de afkortingen voor periodenpecificaties:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Afkorting</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Periode</p></td>
</tr>
<tr class="even">
<td><p>LP</p></td>
<td><p>Laatste periode van een boekjaar, half jaar of kwartaal.</p></td>
</tr>
<tr class="odd">
<td><p>HP</p></td>
<td><p>Huidige periode van een boekjaar, half jaar of kwartaal.</p></td>
</tr>
<tr class="even">
<td><p>BJ</p></td>
<td><p>Boekjaar. Met BJ[1..3] wordt bijvoorbeeld het eerste kwartaal van het huidige boekjaar aangeduid.</p></td>
</tr>
</tbody>
</table>

Voorbeelden van formules:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Formule</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Leeg&gt;</p></td>
<td><p>Huidige periode</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Vorige periode</p></td>
</tr>
<tr class="odd">
<td><p>-1BJ[1..LP]</p></td>
<td><p>Volledig vorig boekjaar</p></td>
</tr>
<tr class="even">
<td><p>-1BJ</p></td>
<td><p>Huidige periode in vorig boekjaar</p></td>
</tr>
<tr class="odd">
<td><p>-1BJ[1..3]</p></td>
<td><p>Eerste kwartaal van vorig boekjaar</p></td>
</tr>
<tr class="even">
<td><p>-1BJ[1..HP]</p></td>
<td><p>Van het begin van het vorige boekjaar tot en met de huidige periode in het vorige boekjaar</p></td>
</tr>
<tr class="odd">
<td><p>-1BJ[HP..LP]</p></td>
<td><p>Van de huidige periode in het vorige boekjaar tot en met de laatste periode van het vorige boekjaar</p></td>
</tr>
</tbody>
</table>

Als u de berekening volgens normale tijdsperioden wilt uitvoeren, moet u in plaats daarvan een formule in het veld **Datumvergelijkingsformule** invoeren.

> [!NOTE]
> Het is niet altijd transparant welke perioden u vergelijkt omdat u een datumfilter op een rapport kunt instellen dat andere datums omvat dan de boekingsperioden die worden gereflecteerd in de gegevens in het rekeningschema. U maakt bijvoorbeeld een rapportageschema waarin u deze periode wilt vergelijken met dezelfde periode vorig jaar, dus u stelt het veld **Filter van vergelijkingsdatumperiode** in op *-1BJ*. Vervolgens voert u het rapport uit op 28 februari en stelt u het datumfilter in op januari en februari. Daardoor vergelijkt het rapportageschema januari en februari dit jaar met januari vorig jaar, wat de enige voltooide boekingsperiode van de twee voor vorig jaar is.  


## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

