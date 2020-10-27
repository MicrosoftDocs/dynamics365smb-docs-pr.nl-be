---
title: Financiële rapporten maken met rapportageschema's
description: Beschrijft hoe u rapportageschema's gebruikt om diverse weergaven en lijsten te maken om financiële prestatiegegevens te analyseren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 23a90d6529da231194b80f75e570e106d66a99c6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922204"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Financiële rapportage voorbereiden met rapportageschema's en rekeningcategorieën

Gebruik rapportageschema's om inzicht te krijgen in de financiële gegevens die in uw rekeningschema zijn opgeslagen. Met rapportageschema's worden cijfers geanalyseerd in grootboekrekeningen en worden grootboekposten vergeleken met budgetposten voor het grootboek. De resultaten worden weergegeven in grafieken in uw rolcentrum, zoals het Cashflowdiagram, en in rapporten, zoals de Resultatenrekening en de Balans.

U opent deze twee rapporten, bijvoorbeeld, met de actie **Financiële afschriften** in de rolcentra Bedrijfsmanager en Accountant.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] biedt een aantal voorbeeldrapportageschema's die u direct kunt gebruiken, of u kunt uw eigen rijen en kolommen instellen om de te vergelijken cijfers op te geven. U kunt bijvoorbeeld rapportageschema's maken om winstmarges te berekenen voor dimensies, zoals afdelingen of klantengroepen. U kunt zoveel aangepaste financiële overzichten maken als u wilt.  

Het instellen van rapportageschema's vereist begrip van de financiële gegevens in het rekeningschema. U kunt bijvoorbeeld grootboekposten weergeven als percentages van budgetposten. Hiertoe moeten budgetten worden gemaakt. Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.

## <a name="account-schedules"></a>Rapportageschema's

Rapportageschema's worden gebruikt om rekeningen in het rekeningschema op zo'n manier te ordenen dat dit informatie presenteert over die rekeningen. U kunt verschillende indelingen instellen om de informatie te definiëren die u wilt betrekken uit het rekeningschema. Eén van de belangrijkste functies van rapportageschema's is het bieden van een plek voor berekeningen die niet direct in het rekeningschema kunnen worden gemaakt, zoals het maken van subtotalen voor rekeninggroepen die kunnen worden opgenomen in nieuwe totalen en vervolgens kunnen worden gebruikt in andere totalen. Gebruikers kunnen bijvoorbeeld rapportageschema's maken om winstmarges te berekenen op dimensies zoals afdelingen of klantengroepen. Daarnaast kunnen grootboekposten worden en budgetposten van grootboeken worden gefilterd, op bijvoorbeeld nettowijzigingen of debetbedragen.

U kunt ook twee of meer rapportageschema's en kolomindelingen vergelijken met formules. Met dit soort vergelijkingen kunt u:

* Aangepaste financiële rapporten maken
* Zo veel rapportageschema's maken als u nodig hebt, elk met een eigen naam.
* Verschillende rapportindelingen instellen en de rapporten afdrukken met de huidige cijfers.

## <a name="gl-account-categories"></a>GB-rekeningcategorieën

U kunt GB-rekeningcategorieën gebruiken om de indeling te wijzigen van uw financiële overzichten. Nadat u de rekeningcategorieën hebt ingesteld op de pagina **GB-rekeningcategorieën** en u kiest de actie **Rapportageschema's genereren** , worden de onderliggende rapportageschema's voor de financiële kernrapporten bijgewerkt. De volgende keer dat u een van deze rapporten uitvoert, zoals het rapport **Balans** , worden nieuwe totalen en subposten toegevoegd op basis van uw wijzigingen.

> [!NOTE]
> De accountcategorieën op het hoogste niveau, zoals het knooppunt **Passiva** zijn opgelost en u kunt uw eigen knooppunt niet toevoegen. U kunt rekeningcategorieën echter op lagere niveaus verwijderen en toevoegen en hun structuur wijzigen om te definiëren hoe het gerelateerde rapportageschema in rapporten wordt weergegeven.
>
> Het wordt aanbevolen om uw eigen categorieën van grootboekrekeningen op lager niveau helemaal zelf te maken en te structureren, indien nodig in een hiërarchie, in plaats van te proberen de bestaande categorieën te herschikken. U kunt bijvoorbeeld het knooppunt **Passiva** herstructureren met een nieuw knooppunt **Eigen vermogen** , gevolgd door de knooppunten **Vlottende verplichtingen** en **LT-verplichtingen** .

## <a name="to-create-a-new-account-schedule"></a>Een nieuw rapportageschema maken

U kunt rekeningstelsels gebruiken om de cijfers in grootboekrekeningen te analyseren, of om grootboekposten te vergelijken met grootboekbegrotingsposten. U kunt bijvoorbeeld de grootboekposten weergeven als percentages van de begrotingsposten.

De rapportageschema's in de standaardversie van [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn de basis van de financiële standaardrapporten, die mogelijk niet overeenkomen met de wensen van uw bedrijf. Als u snel uw eigen financiële rapporten wilt maken, kunt u beginnen met een bestaand rapportageschema te kopiëren. Zie stap 3 hieronder.

Op de pagina **Rapportageschemaoverzicht** bekijkt u een voorbeeld van het financiële rapport dat het rapportageschema definieert. In het volgende is het belangrijk te weten dat wat u instelt als rijen en kolommen van het rapportageschema, alleen kan worden gezien en gevalideerd op de pagina **Rapportageschemaoverzicht** , die u kunt openen vanuit een rapportageschema door de actie **Overzicht** te kiezen. De pagina **Rapportageschema** zelf is alleen een instellingengebied.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema's** in en kies de desbetreffende koppeling.  
2. Kies op de pagina **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een rekeningschema te maken.
3. Of kies de actie **Rapportageschema kopiëren** , vul de twee velden in en kies de knop **OK** .
4. Vul de benodigde velden in. Selecteer in het veld **Std. kolomindeling** een bestaande indeling. U kunt het later desgewenst wijzigen.

    U gebruikt kolomindelingen om kolommen te definiëren voor verschillende parameters waarmee de financiële gegevens in de rijen worden weergegeven. U kunt bijvoorbeeld een kolomindeling maken om mutatie en saldo te vergelijken voor dezelfde periode dit jaar en vorig jaar, met vier kolommen. Zie voor meer informatie [Een kolomindeling bewerken](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Kies de actie **Rapportageschema bewerken** .
6. Maak een rij voor financieel elk element dat u in de lijst wilt weergeven, zoals een regel voor vlottende activa en een andere regel voor vaste activa. Zie voor inspiratie bestaande rapportageschema's in het CRONUS-demonstratiebedrijf.
7. Kies de actie **Overzicht** om het resulterende financiële rapport te bekijken.
8. Selecteer op de pagina **Rapportageschemaoverzicht** in het veld **Kolomindelingnaam** een andere kolomindeling om de financiële gegevens door andere parameters te bekijken.
9. Kies de knop **OK** .

U hebt nu de basis van het rapportageschema gedefinieerd, de rijen van financiële gegevens die moeten worden weergegeven, en een bestaande kolomindeling om de gegevens in de rijen per verschillende parameters weer te geven. Als de standaardkolomindeling die u in stap 4 hebt geselecteerd niet met uw doel overeenkomt, volgt u de onderstaande procedure.

### <a name="to-edit-a-column-layout"></a>Een kolomindeling bewerken

U gebruikt kolomindelingen om te definiëren welke kolommen u in het resulterende rapport wilt opnemen. U kunt bijvoorbeeld een indeling maken om mutatie en saldo te vergelijken voor dezelfde periode dit jaar en vorig jaar.

> [!NOTE]
> Een afgedrukte/opgeslagen of voorbeeldversie van een rapportageschema kan maximaal vijf kolommen weergegeven. Als het rapportageschema alleen voor analyse op de pagina **Rapportageschemaoverzicht** is bedoeld, kunt u zoveel kolommen maken als u wilt.

1. Op de pagina **Rapportageschema's** selecteert u het relevante rapportageschema en kiest u vervolgens de actie **Instellingen kolomindeling bewerken** .
2. Op de pagina **Kolomindelingen** maakt u een regel voor elke kolom waarmee financiële gegevens in het financiële rapport worden weergegeven. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kies de knop **OK** .
4. Open van tijd tot tijd de pagina **Rapportageschemaoverzicht** om te controleren of de nieuwe kolomindeling werkt zoals bedoeld.

> [!NOTE]
> De kolommen die u voor elke rij definieert, vertegenwoordigen kolom 3 en hoger op de pagina **Rapportageschemaoverzicht** . De eerste twee kolommen, **Rijnr.** en **Omschrijving** zijn vast.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Een kolom maken die percentages berekent

U wilt mogelijk soms een kolom opnemen in een rekeningschema om percentages van een totaal te berekenen. U hebt bijvoorbeeld een aantal rijen die zijn onderverdeeld op dimensie, en u wilt wellicht een kolom maken om het percentage aan te geven van de totale verkoop van elke rij.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema's** in en kies de desbetreffende koppeling.
2. Selecteer een rapportageschema op de pagina **Rapportageschema's** .  
3. Kies de actie **Rapportageschema bewerken** om een rapportageschemarij te definiëren die de totalen moet berekenen waarop de percentages worden gebaseerd.  
4. Voeg een regel in rechtstreeks boven de eerste rij waarvoor u een percentage wilt weergeven.  
5. Vul de velden als volgt op de regel in: voer in het veld **Samentellingssoort** **Basis voor percentage** in. Voer in het veld **Samentelling** een formule in voor het totaal waarop het percentage wordt gebaseerd. Als bijvoorbeeld rij 11 de totale omzet bevat, voert u **11** in.  
6. Kies de actie **Instellingen kolomindeling bewerken** om een kolom in te stellen.  
7. Vul de velden als volgt op de regel in: selecteer in het veld **Kolomsoort** **Formule** . Voer in het veld **Formule** een formule in voor het bedrag waarvoor u een percentage wilt berekenen, gevolgd door %. Bijvoorbeeld, als kolomnummer N de mutatie bevat, voert u **N%** in.  
8. Herhaal stap 4 tot en met 7 voor elke groep rijen die u wilt uitsplitsen op percentage.

## <a name="to-set-up-account-schedules-with-overviews"></a>Rekeningstelsels met overzichten instellen

U kunt een rekeningstelsel gebruiken om een rekeningoverzicht te maken waarin grootboekcijfers en begrotingscijfers van grootboeken worden vergeleken.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema's** in en kies de desbetreffende koppeling.
2. Selecteer een rapportageschema op de pagina **Rapportageschema's** .  
3. Kies de actie **Rapportageschema bewerken**  
4. Selecteer op de pagina **Rapportageschema** in het veld **Naam** de naam van het standaardrapportageschema.
5. Kies de actie **Rekeningen invoegen** .  
6. Selecteer de rekeningen die u wilt opnemen in uw overzicht en klik vervolgens op **OK** .

    De rekeningen worden nu opgenomen in het rapportageschema. Indien gewenst kunt u ook de kolomindeling wijzigen.  
7. Kies de actie **Overzicht** .  
8. Stel op de pagina **Rapportageschemaoverzicht** op het sneltabblad **Dimensiefilters** het budgetfilter in op de gewenste filternaam.  
9. Kies de knop **Ok** .  

Nu kunt u het budgetoverzicht kopiëren en in een spreadsheet plakken.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Boekingsperioden vergelijken met behulp van periodeformules

Uw rapportageschema kan de resultaten vergelijken van verschillende boekingsperioden, zoals deze maand vergeleken met dezelfde maand vorig jaar. Open hiervoor de pagina **Kolomindeling** en personaliseer deze door het veld **Periodevergelijkingsformule** als een kolom toe te voegen. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie. U kunt dat veld vervolgens instellen op een periodeformule.  

Een boekhoudperiode hoeft niet gelijk te zijn aan een agendaperiode, maar ieder boekjaar moet hetzelfde aantal boekhoudperioden hebben, zelfs wanneer de boekhoudperioden onderling in lengte verschillen.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt de periodeformule om het bedrag uit de vergelijkingsperiode te berekenen in verhouding tot de periode die wordt voorgesteld door het datumfilter in de rapportaanvraag. De vergelijkingsperiode is gebaseerd op de begindatum van het datumfilter. Dit zijn de afkortingen voor periodenpecificaties:

| Afkorting | Omschrijving                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode                                                                                |
| LP           | Laatste periode van een boekjaar, half jaar of kwartaal.                                   |
| HP           | Huidige periode van een boekjaar, half jaar of kwartaal. Gebruik HP in formules om de periode in te stellen waarmee de formule begint of eindigt. Bijvoorbeeld BJ\[1..HP\] geeft de tijd aan vanaf het begin van het huidige boekjaar tot de huidige periode.|
| BJ           | Boekjaar. Met BJ\[1..3\] wordt bijvoorbeeld het eerste kwartaal van het huidige boekjaar aangeduid |

Voorbeelden van formules:

| Formule         | Omschrijving                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Huidige periode                                                                                  |
| \-1P            | Vorige periode                                                                                 |
| \-1BJ\[1..LP\]  | Volledig vorig boekjaar                                                                     |
| \-1BJ           | Huidige periode in vorig boekjaar                                                          |
| \-1BJ\[1..3\]   | Eerste kwartaal van vorig boekjaar                                                           |
| \-1BJ\[1..HP\]  | Van het begin van het vorige boekjaar tot en met de huidige periode in het vorige boekjaar, inclusief beide perioden |
| \-1BJ\[HP..LP\] | Van het begin van het vorige boekjaar tot en met de laatste periode in het vorige boekjaar, inclusief beide perioden   |

Als u de berekening volgens normale tijdsperioden wilt uitvoeren, moet u in plaats daarvan een formule in het veld **Datumvergelijkingsformule** invoeren. Als het veld bijvoorbeeld de waarde -1J heeft, wordt in [!INCLUDE [prodshort](includes/prodshort.md)] met dezelfde periode 1 jaar eerder vergeleken.

> [!NOTE]
> Het is niet altijd transparant welke perioden u vergelijkt omdat u een datumfilter op een rapport kunt instellen dat andere datums omvat dan de boekingsperioden die worden gereflecteerd in de gegevens in het rekeningschema. U maakt bijvoorbeeld een rapportageschema waarin u deze periode wilt vergelijken met dezelfde periode vorig jaar, dus u stelt het veld **Datumvergelijkingsformule** in op *-1BJ* . Vervolgens voert u het rapport uit op 28 februari en stelt u het datumfilter in op januari en februari. Daardoor vergelijkt het rapportageschema januari en februari dit jaar met januari vorig jaar, wat de enige voltooide boekingsperiode van de twee voor vorig jaar is.  

Zie voor meer informatie over datumformules [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
