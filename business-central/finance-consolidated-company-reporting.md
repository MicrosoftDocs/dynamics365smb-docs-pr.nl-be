---
title: Gegevens uit meerdere bedrijven consolideren
description: In dit artikel wordt uitgelegd hoe u de grootboekposten van twee of meer aparte bedrijven (dochterbedrijven) consolideert tot één geconsolideerd bedrijf.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 09/29/2022
ms.author: bholtorf
---

# <a name="consolidating-financial-data-from-multiple-companies"></a><a name="consolidating-financial-data-from-multiple-companies"></a>Financiële gegevens uit meerdere bedrijven consolideren

Sommige organisaties gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in meerdere bedrijfsunits of rechtspersonen. Andere gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in dochterondernemingen die moeten rapporteren aan moederorganisaties. In beide gevallen gebruiken de accountants ingebouwde tools om de financiële gegevens te helpen consolideren.  

U kunt de grootboekposten van twee of meer aparte bedrijven (dochterbedrijven) consolideren in één geconsolideerd bedrijf. Elk afzonderlijk bedrijf dat betrokken is bij een consolidatie, wordt een bedrijfsunit genoemd. Het gecombineerde bedrijf wordt het geconsolideerde bedrijf genoemd.  

U kunt gegevens in het geconsolideerde bedrijf importeren vanuit andere bedrijven in dezelfde [!INCLUDE [prod_short](includes/prod_short.md)]-tenant of vanuit bestanden.  

Als de financiële overzichten van een bedrijfsunit in een andere valuta zijn dan de valuta die wordt gebruikt in het geconsolideerde bedrijf, moet u wisselkoersen instellen voor consolidatie.  

U kunt consolideren:  

* Gegevens van bedrijven met verschillende rekeningschema's.  
* Gegevens van bedrijven die met verschillende boekjaren en verschillende valuta's werken.  
* Het volledige bedrag of een percentage van de financiële gegevens van een bedrijf
* Verschillende wisselkoersen in afzonderlijke grootboekrekeningen gebruiken
* Bedrijven in andere boekhoudkundige en bedrijfsbeheerprogramma's

U stelt het geconsolideerde bedrijf in op dezelfde manier als waarop u andere bedrijven instelt. Het rekeningschema is onafhankelijk van het rekeningschema in de bedrijfsunits. Het rekeningschema in de bedrijfsunits kan van elkaar verschillen. U stelt een lijst met te consolideren bedrijven in, controleert de boekhoudgegevens vóór de consolidatie, importeert uit bestanden of databases en genereert consolidatierapporten. Zie [Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md) voor meer informatie.  

> [!TIP]
> Consolideren van financiële gegevens kan vooral relevant zijn in verband met IC-processen. Raadpleeg [IC-transacties beheren](intercompany-manage.md) voor meer informatie.

## <a name="use-the-consolidated-trial-balance-report"></a><a name="use-the-consolidated-trial-balance-report"></a>Gebruik het rapport Consolidatie - Proef- en saldibalans uitvoeren

Het rapport **Consolidatie - Proefbalans** kan u een overzicht geven van de algehele financiële gezondheid van uw bedrijf. Het rapport combineert grootboekposten van elk van uw bedrijven in een nieuw bedrijf dat u hebt gemaakt voor de geconsolideerde gegevens. Dit bedrijf wordt doorgaans het *geconsolideerde bedrijf* genoemd. Het geconsolideerde bedrijf is slechts een container voor de geconsolideerde gegevens en bevat geen live bedrijfsgegevens. De bedrijven die u in het geconsolideerde bedrijf opneemt, worden in het rapport **bedrijfsunits**. Zie [Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md) voor meer informatie. Heeft u vier of minder bedrijfsonderdelen, dan kunt u ook gebruik maken van het rapport **Consolidatie - Proefbalans (4)**.  

Het rapport toont een regel voor elke rekening en volgt de structuur van het rekeningschema. Een rekening wordt niet weergegeven als alle bedragen op de regel 0 zijn. Het rapport toont de volgende informatie voor elk account:

* Het rekeningnummer en de naam van de rekening.
* De totalen voor het geconsolideerde bedrijf en voor elke bedrijfsunit. Totalen kunnen worden weergegeven als een nettowijziging of als het saldo tot en met datum.
* De eliminaties die in het geconsolideerde bedrijf zijn gemaakt. Eliminaties worden altijd weergegeven voor een periode die overeenkomt met het boekjaar van het geconsolideerde bedrijf.
* Het totaal voor het geconsolideerde bedrijf na de eliminaties, weergegeven als mutatie of als saldo tot en met datum.

## <a name="consolidate-data"></a><a name="consolidate-data"></a>Gegevens consolideren

De overdracht van de cijfers van de bedrijfsunits naar de geconsolideerde onderneming is de feitelijke *consolidatie*. Voordat u de consolidatie uitvoert, doet u er goed aan te controleren of er verschillen zijn tussen de basisgegevens in de bedrijfsunits en het geconsolideerde bedrijf. Er zijn twee rapporten die u kunt gebruiken om de database en het bestand te testen.

### <a name="to-test-the-data-before-you-consolidate"></a><a name="to-test-the-data-before-you-consolidate"></a>De gegevens testen vóór consolidatie

Test uw gegevens testen voordat u deze naar het geconsolideerde bedrijf overbrengt. [!INCLUDE[prod_short](includes/prod_short.md)] zoekt naar verschillen in de gegevens in de bedrijfsunits en in het geconsolideerde bedrijf. Er wordt bijvoorbeeld gecontroleerd of rekeningnummers of dimensiecodes afwijken. U moet fouten corrigeren voordat u het rapport kunt uitvoeren. U kunt de database testen, als u gegevens uit een XML-bestand importeert, of het bestand testen.  

1. Open het geconsolideerde bedrijf.  
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
3. Test het bestand en de database als volgt:  

    * Als u een bestand wilt testen, kiest u de actie **Bestand testen**, voert u de naam van het bestand in en kiest u **Afdrukken**.  
    * Als u de database wilt testen, kiest u **Database testen**.  

### <a name="run-the-consolidation"></a><a name="run-the-consolidation"></a>De consolidatie uitvoeren

Wanneer u de gegevens hebt getest, kunt deze naar het geconsolideerde bedrijf overbrengen.  

1. Meld u aan bij het geconsolideerde bedrijf.  
2. Kies in **Rolcentrum Accountant** de actie **Consolidatie uitvoeren**.  
3. Vul de vereiste velden in.  
4. Stel in de sectie Filter een filter in voor de relevante bedrijfsunit of bedrijfsnaam.  
5. Plan desgewenst de uitvoering van het rapport op een geschikte tijd.  

## <a name="eliminate-repeated-transactions"></a><a name="eliminate-repeated-transactions"></a>Herhaalde transacties verwijderen

Nadat u de bedrijven hebt geconsolideerd, moet u alle transacties vinden en elimineren die meer dan eens in bedrijven zijn geregistreerd. Consolidatieverwijderingen boeken is een handmatig proces.  

Als u herhaalde transacties wilt verwijderen:

1. Zoek transacties die mogelijk moeten worden aangepast en voer algemene dagboekregels in om ze te verwijderen.
2. Voer het rapport **Consolidatie - Eliminaties** uit om u te helpen de invloed van de dagboekregels te bepalen voorafgaand aan boeking.
3. Boek de aanpassingstransacties.

Het rapport **Consolidatie - Eliminaties** geeft een voorlopige proefbalans weer waarin u de gevolgen van het elimineren van boekingen kunt simuleren. Het rapport vergelijkt de boekingen in het geconsolideerde bedrijf met de eliminaties die in het dagboek zijn ingevoerd.

Voordat een bedrijfsunit in het rapport kan worden opgenomen, moet u de unit instellen op de pagina **Bedrijfsunits**. Het veld **Consolideren** moet zijn geselecteerd.

Voor elke rekening wordt een regel aangemaakt volgens de structuur van het rekeningschema. Een rekening wordt niet weergegeven als alle bedragen op de regel 0 zijn. De volgende gegevens worden voor elke rekening weergegeven:

* Rekeningnummer.
* Rekeningnaam.
* Als u een of meer bedrijfsunitcodes hebt geselecteerd in het veld **Bedrijfsunit** op de aanvraagpagina, wordt een totaal weergegeven voor het geconsolideerde bedrijf zonder de geselecteerde bedrijfsunits en eliminaties. Hebt u het veld **Bedrijfsunit** niet ingevuld, dan wordt het totaal weergegeven voor het geconsolideerde bedrijf, zonder de eliminaties.
* Als u een bedrijfsunitcode hebt geselecteerd in het veld **Bedrijfsunit** op de aanvraagpagina, wordt een totaal weergegeven voor de geïmporteerde posten uit de bedrijfsunit. Hebt u het veld **Bedrijfsunit** niet hebt ingevuld, dan wordt een totaal weergegeven voor de geboekte eliminaties in het geconsolideerde bedrijf.
* Het totaal voor het geconsolideerde bedrijf met alle bedrijfsunits en geboekte eliminaties.
* De te maken eliminaties in het geconsolideerde bedrijf. Dat wil zeggen de boekingen in het dagboek die op de aanvraagpagina zijn geselecteerd.
* De boekingstekst, gekopieerd uit het dagboek.
* Het totaal voor het geconsolideerde bedrijf na de eliminaties, als deze zijn geboekt.

## <a name="export-and-import-consolidated-data-between-databases"></a><a name="export-and-import-consolidated-data-between-databases"></a>Geconsolideerde gegevens exporteren en importeren tussen databases

Als gegevens voor een bedrijfsunit zich in een andere database bevinden, moet u de gegevens naar een bestand exporteren voordat u deze kunt opnemen in de consolidatie. Elk bedrijf moet afzonderlijk worden geëxporteerd. Voor dit doel gebruikt u de batchverwerking **Consolidatie - Export**.  

> [!TIP]
> Gebruik hetzelfde proces om geconsolideerde gegevens te exporteren die moeten worden ingediend bij Dynamics 365 Finance, bijvoorbeeld als de huidige bedrijfsunit een dochteronderneming is en de moedermaatschappij Dynamics 365 Finance gebruikt.

Nadat u de batchtaak hebt uitgevoerd, worden alle posten in grootboekrekeningen verwerkt. Voor elke combinatie van geselecteerde dimensies en datum wordt de inhoud van het veld **Bedrag** van de posten opgeteld en geëxporteerd. De volgende combinatie van de geselecteerde dimensies en datum met hetzelfde rekeningnummer wordt verwerkt. Vervolgens worden de combinaties in het volgende rekeningnummer verwerkt, enzovoort.  

De geëxporteerde posten bevatten de volgende velden: **Bankrekeningnr.**, **Boekingsdatum** en **Bedrag**. Als tevens de dimensiegegevens zijn geëxporteerd, worden ook dimensiecodes en -waarden opgenomen.  

1. Voor elke geëxporteerde regel geldt dat als het totaal in de velden **Bedrag** een debetbedrag is, het rekeningnummer dat is ingesteld in het veld **Consolidatie debetrekening** van het bedrijf, naar de regel wordt geëxporteerd. Als het totaal een creditbedrag is, wordt het overeenkomstige getal in het veld **Consolidatie creditrekening** naar de regel geëxporteerd.  
2. De datum die wordt gebruikt voor elke geëxporteerde regel is de einddatum van de periode, of als de overdracht elke dag plaatsvindt, de exacte datum van de berekening.  
3. De dimensiewaarde die voor de boeking wordt geëxporteerd, is de geconsolideerde bedrijfsdimensiewaarde die is gespecificeerd in het veld **Consolidatiecode** voor die dimensiewaarde. Als er geen dimensiewaarde voor het geconsolideerde bedrijf is opgegeven in het veld **Geconsolideerde code** voor de dimensiewaarde, wordt de dimensiewaarde zelf naar de regel geëxporteerd.  
4. Bovendien bevatten de XML-bestanden ook de valutawisselkoersen binnen de consolidatieperiode. Deze koersen worden in een apart gedeelte aan het begin van het bestand opgenomen.  

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md)  
[Intercompany-transacties beheren](intercompany-manage.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
