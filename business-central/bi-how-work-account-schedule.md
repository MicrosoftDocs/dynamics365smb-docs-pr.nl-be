---
title: Financiële rapportages samenstellen met financiële gegevens en accountcategorieën
description: Beschrijft hoe u financiële rapportages gebruikt om diverse weergaven en rapporten te maken om financiële prestatiegegevens te analyseren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Financiële rapportage voorbereiden met financiële gegevens en accountcategorieën

Financiële rapporten geven u inzicht in de financiële gegevens die in uw rekeningschema (COA) zijn opgeslagen. met financiële rapportages worden cijfers in grootboekrekeningen (G/L) geanalyseerd en worden grootboekposten vergeleken met budgetposten. De resultaten worden weergegeven in grafieken en rapporten in uw Rolcentrum, zoals het Cashflowdiagram, en de rapporten resultatenrekening en balans.

U opent deze twee rapporten, bijvoorbeeld, met de actie **Financiële afschriften** in de rolcentra bedrijfsmanager en accountant.  

[!INCLUDE[prod_short](includes/prod_short.md)] biedt voorbeelden van financiële rapportages die u meteen kunt gebruiken. U kunt ook uw eigen rijen en kolommen instellen om de te vergelijken cijfers op te geven. U kunt bijvoorbeeld financiële rapportages maken om winstmarges te berekenen met behulp van dimensies zoals afdelingen of klantengroepen. Het aantal op maat gemaakte financiële overzichten dat u kunt maken is onbeperkt.  

Het instellen van financiële rapportages vereist begrip van de financiële gegevens in het rekeningschema. U kunt bijvoorbeeld grootboekposten weergeven als percentages van budgetposten, maar daarvoor moet u wel budgetten hebben gemaakt. Zie voor meer informatie [GB-budgetten maken](finance-how-create-budgets.md).

## <a name="financial-reports"></a>Financiële rapporten

Financiële rapporten rangschikken rekeningen uit uw rekeningschema op een manier die het gemakkelijker maakt om gegevens te presenteren. U kunt verschillende indelingen instellen om de informatie te definiëren die u wilt betrekken uit het rekeningschema. In financiële rapporten kunnen berekeningen worden uitgevoerd die niet rechtstreeks in het rekeningschema kunnen worden uitgevoerd. U kunt bijvoorbeeld subtotalen maken voor groepen rekeningen en dat totaal vervolgens opnemen in andere totalen. Een ander voorbeeld is winstmarges te berekenen op dimensies zoals afdelingen of klantengroepen. Daarnaast kunt u grootboekposten en budgetposten filteren, op bijvoorbeeld mutatie of debetbedragen.

U kunt ook twee of meer financiële rapporten en kolomdefinities vergelijken met formules, zodat u de volgende dingen kunt doen:

* Aangepaste financiële rapporten maken
* Zo veel financiële rapporten maken als u nodig hebt, elk met een eigen naam.
* Verschillende rapportindelingen instellen en de rapporten afdrukken met de huidige cijfers.

## <a name="gl-account-categories"></a>GB-rekeningcategorieën

U kunt GB-rekeningcategorieën gebruiken om de indeling te wijzigen van uw financiële overzichten. Nadat u de rekeningcategorieën hebt ingesteld op de pagina **GB-rekeningcategorieën** kunt u, bijvoorbeeld, de actie **Financiële rapporten genereren** kiezen en de onderliggende financiële rapporten voor de financiële kernrapporten bijwerken. De volgende keer dat u dan een van deze rapporten uitvoert, zoals het rapport **Balans**, worden nieuwe totalen en subposten toegevoegd.

> [!NOTE]
> De accountcategorieën op het hoogste niveau, zoals het knooppunt **Passiva** zijn opgelost en u kunt uw eigen knooppunt niet toevoegen. U kunt rekeningcategorieën echter op lagere niveaus verwijderen en toevoegen en definiëren hoe het gerelateerde financiële rapport in rapporten wordt weergegeven.
>
> U moet uw eigen categorieën van grootboekrekeningen op lager niveau helemaal zelf maken en structureren, indien nodig in een hiërarchie, in plaats van te proberen de bestaande categorieën te herschikken. U kunt bijvoorbeeld het knooppunt **Passiva** herstructureren met een nieuw knooppunt **Eigen vermogen**, gevolgd door de knooppunten **Vlottende verplichtingen** en **LT-verplichtingen**.

## <a name="create-a-new-financial-report"></a>Een nieuw financieel rapport maken

U gebruikt financiële rapporten voor het analyseren van grootboekrekeningen of om grootboekposten te vergelijken met budgetposten. U kunt bijvoorbeeld de grootboekposten weergeven als percentages van de begrotingsposten.

De financiële rapporten in de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] past mogelijk niet bij uw zakelijke behoeften. Als u snel uw eigen financiële rapporten wilt maken, kunt u beginnen met een bestaand rapport, zoals hieronder is beschreven in stap drie.

> [!TIP]
> Nadat u een financieel rapport hebt gemaakt, kunt u de pagina **Financieel rapport** gebruiken om een voorbeeld van uw nieuw gedefinieerde financiële rapport te bekijken en te valideren. Kies de actie **Financieel rapport bewerken** om de pagina te openen.  

> [!NOTE]
> Wanneer u een financieel rapport opent in de weergave- of bewerkingsmodus, is het filtervenster beschikbaar. Gebruik het deelvenster echter niet om filters in te stellen voor de gegevens in uw rapport. De filters kunnen fouten veroorzaken of filteren de gegevens mogelijk niet daadwerkelijk. Gebruik in plaats daarvan de filtervelden op de sneltabbladen **Opties** en **Dimensies**.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Financiële rapporten** de actie **Nieuw** om een nieuwe naam voor een financieel rapport te maken.
3. Als alternatief kunt u, als u instellingen uit een bestaand financieel rapport opnieuw wilt gebruiken, de actie **Financieel rapport kopiëren** kiezen.
4. Vul de vereiste velden in. Selecteer in het veld **Kolomdefinitie** een bestaande definitie, die u later kunt bewerken als u dat wilt.

    Kolomdefinities specificeren de parameters waarmee de financiële gegevens in de rijen worden weergegeven. Een kolomdefinitie kan bijvoorbeeld vier kolommen bevatten waarmee u mutatie en saldo kunt vergelijken voor dezelfde periode dit jaar en vorig jaar. Meer informatie vindt u in de sectie [Een kolomdefinitie bewerken](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Kies de actie **Rijdefinitie bewerken**.
6. Kies de acties **Grootboekrekeningen invoegen**, **CF-accounts invoegen** en **Kostensoorten invoegen** om een rij te maken voor elk financieel element dat u wilt analyseren. U hebt bijvoorbeeld één rij voor vlottende activa en een andere rij voor vaste activa. Bekijk voor inspiratie de bestaande financiële rapporten in het voorbeeldbedrijf CRONUS.

    > [!NOTE]
    > Het veld **Rijnr.** toont de eerste tien tekens van een identificatie, zoals een rekeningnummer. Als u elementen toevoegt met identifiers die beginnen met dezelfde 10 tekens, krijgt u duplicaten in het veld **Rijnr.**   Indien nodig kunt u de id's handmatig bewerken nadat u de elementen hebt ingevoegd. De volledige identifiers worden weergegeven in het veld **Samentelling**.

7. Kies op de pagina **Financiële rapporten** de actie **Financieel rapport bewerken** om het resulterende financiële rapport te bekijken.
8. Selecteer op de pagina **Financieel rapport** in het veld **Kolomdefinitie** een andere kolomdefinitie om de financiële gegevens op basis van andere parameters te bekijken.
9. Klik op **OK**.

U hebt nu de basis van het financiële rapport gedefinieerd, de rijen van financiële gegevens die moeten worden weergegeven en een bestaande kolomindeling om de gegevens in de rijen weer te geven met behulp van aangepaste parameters. Als de standaardkolomdefinitie die u in stap 4 hebt geselecteerd, niet met uw doel overeenkomt, volgt u de stappen in [Een kolomdefinitie bewerken](#edit-a-column-definition).

### <a name="edit-a-column-definition"></a>Een kolomdefinitie bewerken

Gebruik kolomdefinities om op te geven welke kolommen u in het rapport wilt opnemen. U kunt bijvoorbeeld een indeling maken om mutatie en saldo te vergelijken voor dezelfde periode dit jaar en vorig jaar. U kunt maximaal 15 kolommen hebben, wat bijvoorbeeld handig is voor, bijvoorbeeld, het bekijken van budgetten voor 12 maanden met een kolom die het totaal laat zien.

> [!NOTE]
> Een afgedrukte/opgeslagen of voorbeeldversie van een financieel rapport kan maximaal vijf kolommen weergegeven. Als een financieel rapport daarentegen alleen bedoeld is voor analyse op de pagina **Financieel rapport**, kunt u zoveel kolommen maken als u wilt.

1. Selecteer op de pagina **Financiële rapporten** het betreffende financiële rapport en kies vervolgens de actie **Kolomdefinitie bewerken**.
2. Maak op de pagina **Kolomdefinitie** een rij voor elke kolom met financiële gegevens die in het financiële rapport wordt weergegeven. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Klik op **OK**.
4. Open van tijd tot tijd de pagina **Financieel rapport** om te controleren of de nieuwe kolomdefinitie werkt zoals bedoeld.

> [!NOTE]
> De kolommen die u voor elke rij definieert, vertegenwoordigen kolom drie en hoger op de pagina **Financieel rapport**. De eerste twee kolommen, **Rijnr.** en **Omschrijving** zijn vast.  

### <a name="create-a-column-that-calculates-percentages"></a>Een kolom maken die percentages berekent

Soms wilt u misschien een kolom opnemen in een financieel rapport om percentages van een totaal te berekenen. U hebt bijvoorbeeld een aantal rijen die zijn onderverdeeld op dimensie, en u wilt wellicht een kolom maken om het percentage aan te geven van de totale verkoop van elke rij.

1. Kies het pictogram ![Lampje dat de functie Vertel me 2 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Financiële rapporten** een financieel rapport.  
3. Kies de actie **Financieel rapport bewerken** om een rij in een financieel rapport in te stellen die de totalen moet berekenen waarop de percentages worden gebaseerd.  
4. Voeg een regel in rechtstreeks boven de eerste rij waarvoor u een percentage wilt weergeven.  
5. Vul de velden als volgt op de regel in: voer in het veld **Samentellingssoort** **Basis voor percentage** in. Voer in het veld **Samentelling** een formule in voor het totaal waarop het percentage wordt gebaseerd. Als bijvoorbeeld rij 11 de totale omzet bevat, voert u **11** in.  
6. Kies de actie **Kolomdefinitie bewerken** om een kolom in te stellen.  
7. Vul de velden als volgt op de regel in: selecteer in het veld **Kolomsoort** **Formule**. Voer in het veld **Formule** een formule in voor het bedrag waarvoor u een percentage wilt berekenen, gevolgd door het percentageteken (%). Dus als kolomnummer N de mutatie bevat, voert u **N%** in.  
8. Herhaal stap 4 tot en met 7 voor elke groep rijen die u wilt uitsplitsen op percentage.

## <a name="set-up-financial-reports-with-overviews"></a>Financiële rapporten met overzichten instellen

U kunt een financieel rapport gebruiken om een rekeningoverzicht te maken waarin grootboekcijfers en begrotingscijfers worden vergeleken.

1. Kies het pictogram ![Lampje dat de functie Vertel me 3 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Financiële rapporten** een financieel rapport.  
3. Kies de actie **Rijdefinitie bewerken**  
4. Selecteer op de pagina **Rijdefinitie** in het veld **Naam** de naam van het standaard financiële rapport.
5. Kies de actie **Grootboekrekeningen invoegen**.  
6. Selecteer de rekeningen die u in het rekeningoverzicht wilt opnemen en kies dan **OK**.

    De rekeningen worden nu opgenomen in uw financieel rapport. Indien gewenst kunt u ook de kolomdefinitie wijzigen.  
7. Kies de actie **Financieel rapport bewerken**.  
8. Stel op de pagina **Financieel rapport** op het sneltabblad **Dimensies** het budgetfilter in op de filternaam die u wilt gebruiken.  
9. Klik op **OK**.  

Nu kunt u het budgetoverzicht kopiëren en in een spreadsheet plakken.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Boekingsperioden vergelijken met behulp van periodeformules

Uw financiële rapport kan de resultaten vergelijken van verschillende boekingsperioden, zoals de afgelopen maand vergeleken met dezelfde maand vorig jaar. Open hiervoor de pagina **Kolomdefinitie** en personaliseer deze door het veld **Periodevergelijkingsformule** als een kolom toe te voegen. Zie voor meer informatie [Uw werkruimte personaliseren](ui-personalization-user.md). U kunt dat veld vervolgens instellen op een periodeformule.  

Een boekingsperiode hoeft niet overeen te komen met de kalender. Elk boekjaar moet echter hetzelfde aantal boekhoudperioden hebben, ook al kan elke periode een andere lengte hebben.  

[!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de periodeformule om de duur van de vergelijkingsperiode te berekenen in verhouding tot de periode die wordt voorgesteld door het datumfilter in het rapport. De vergelijkingsperiode is gebaseerd op de begindatum van het datumfilter. Dit zijn de afkortingen voor periodenpecificaties:

| Afkorting | Omschrijving                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| LP           | Laatste periode van een boekjaar, half jaar of kwartaal.                                   |
| CP           | Huidige periode van een boekjaar, half jaar of kwartaal. Gebruik HP in formules om de periode in te stellen waarmee de formule begint of eindigt. Bijvoorbeeld BJ\[1..HP\] geeft de tijd aan vanaf het begin van het huidige boekjaar tot de huidige periode.|
| BJ           | Boekjaar. Met BJ\[1..3\] wordt bijvoorbeeld het eerste kwartaal van het huidige boekjaar aangeduid. |

Voorbeelden van formules:

| Formule         | Omschrijving                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Huidige periode.                                                                                  |
| \-1P            | Vorige periode.                                                                                 |
| \-1BJ\[1..LP\]  | Volledig vorig boekjaar.                                                                     |
| \-1BJ           | Huidige periode in vorig boekjaar.                                                          |
| \-1BJ\[1..3\]   | Eerste kwartaal van vorig boekjaar.                                                           |
| \-1BJ\[1..HP\]  | Van het begin van het vorige boekjaar tot en met de huidige periode in het vorige boekjaar, inclusief beide perioden. |
| \-1BJ\[HP..LP\] | Van de huidige periode in het vorige boekjaar tot de laatste periode van het vorige boekjaar, inclusief beide perioden.   |

Als u de berekening volgens normale tijdsperioden wilt uitvoeren, moet u in plaats daarvan een formule in het veld **Datumvergelijkingsformule** invoeren. Als het veld bijvoorbeeld de waarde -1J heeft, wordt in [!INCLUDE [prod_short](includes/prod_short.md)] met dezelfde periode één jaar eerder vergeleken.

> [!NOTE]
> Het is niet altijd transparant welke perioden u vergelijkt omdat u een datumfilter op een rapport kunt instellen dat andere datums omvat dan de boekingsperioden die worden gereflecteerd in het rekeningschema. Als u dus een financieel rapport maakt waarin u deze periode wilt vergelijken met dezelfde periode vorig jaar, stelt u het veld **Datumvergelijkingsformule** in op *-1BJ*. Vervolgens voert u het rapport uit op 28 februari en stelt u het datumfilter in op januari en februari. Daardoor vergelijkt het financiële rapport januari en februari van dit jaar met januari vorig jaar, wat de enige voltooide boekingsperiode van de twee voor vorig jaar is.  

Zie voor meer informatie [Werken met kalenderdatums en tijden](ui-enter-date-ranges.md).

## <a name="print-and-save-financial-reports"></a>Financiële rapporten afdrukken en opslaan

U kunt financiële rapporten afdrukken met de afdrukservices van uw apparaat. [!INCLUDE[prod_short](includes/prod_short.md)] biedt ook de mogelijkheid om rapporten op te slaan als Microsoft Excel-werkmappen, Microsoft Word-documenten, pdf- en XML-bestanden.

1. Kies het pictogram ![Lampje dat de functie Vertel me 4 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Financiële rapporten** het rapport dat u wilt afdrukken en kies vervolgens de actie **Afdrukken**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Selecteer in het veld **Printer** het apparaat waarnaar het rapport wordt verzonden.
    1. De optie **(Afgehandeld door de browser)** geeft aan dat er geen aangewezen printer is voor het rapport. In dit geval zal de browser de afdruk afhandelen en de standaardafdrukstappen weergeven, waarbij u een lokale printer kunt kiezen die op uw apparaat is aangesloten. **(Afgehandeld door de browser)** is niet beschikbaar in de mobiele [!INCLUDE[prod_short](includes/prod_short.md)]-app of de app voor Microsoft Teams.
5. Kies de actie **Afdrukken**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Plan een financieel rapport of sla het op als pdf-, Word- of Excel-document

Een financieel rapport kan als bestand worden opgeslagen in verschillende indelingen, zoals pdf, XML, Word of Excel. Als alternatief kan [!INCLUDE[prod_short](includes/prod_short.md)] worden ingesteld om terugkerende financiële rapporten te genereren:

1. Kies het pictogram ![Lampje dat de functie Vertel me 4 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Financiële rapporten** de actie **Afdrukken**.
3. Stel het rapport dienovereenkomstig in en kies vervolgens de actie **Verzenden naar**.
4. Selecteer de bestandsindeling of de actie **Schema** en kies **OK**.
5. Vul de velden in om een gepland of terugkerend financieel rapport te genereren. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * Stel voor terugkerende financiële rapporten de velden **Vroegste begindatum/-tijd** en **Vervaldatum/-tijd** met respectievelijk de eerste en laatste datum om het financiële rapport te genereren. Selecteer ook op welke dagen het rapport wordt gegenereerd door het veld **Formule voor volgende uitvoeringsdatum** in te stellen conform de indeling uitgelegd in de sectie [Datumformules gebruiken](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-reports"></a>Financiële rapporten importeren of exporteren

U kunt financiële rapporten importeren en exporteren als RapidStart-configuratiepakketten, die handig zijn om de informatie bijvoorbeeld met andere bedrijven te delen. Het pakket wordt gemaakt vanuit een .rapidstart-bestand, dat de inhoud comprimeert.

### <a name="import-and-export-financial-reports"></a>Financiële rapporten importeren en exporteren

1. Kies het pictogram ![Lampje dat de functie Vertel me 4 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële rapporten** in en kies vervolgens de gerelateerde koppeling.
2. Kies het financiële rapport en kies vervolgens de actie **Financieel rapport importeren** of **Financieel rapport exporteren**, afhankelijk van wat u wilt doen.

> [!NOTE]
> Wanneer u financiële rapporten importeert, worden bestaande records met dezelfde naam als de records die u importeert verwijderd.

## <a name="see-also"></a>Zie ook

[Rapporten uitvoeren en afdrukken](ui-work-report.md)  
[Financiële Business Intelligence](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
