---
title: Gegevens uit meerdere bedrijven consolideren
description: In dit onderwerp wordt uitgelegd hoe u de grootboekposten van twee of meer aparte bedrijven (dochterbedrijven) consolideert tot één geconsolideerd bedrijf.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 06/16/2021
ms.author: edupont
---

# Financiële gegevens uit meerdere bedrijven consolideren

Sommige organisaties gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in meerdere bedrijfsunits of rechtspersonen. Andere gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in dochterondernemingen die moeten rapporteren aan moederorganisaties. In beide gevallen gebruiken de accountants ingebouwde tools om de financiële gegevens te helpen consolideren.  

U kunt de grootboekposten van twee of meer aparte bedrijven (dochterbedrijven) consolideren in één geconsolideerd bedrijf. Elk afzonderlijk bedrijf dat betrokken is bij een consolidatie, wordt een bedrijfsunit genoemd. Het gecombineerde bedrijf wordt het geconsolideerde bedrijf genoemd.  

U kunt gegevens in het geconsolideerde bedrijf importeren vanuit andere bedrijven in dezelfde [!INCLUDE [prod_short](includes/prod_short.md)]-tenant of vanuit bestanden.  

Als de financiële overzichten van een bedrijfsunit in een andere valuta zijn dan die van het geconsolideerde bedrijf, moet u wisselkoersen instellen voor de consolidatie.  

U kunt consolideren:  

* Gegevens van bedrijven met verschillende rekeningschema's.  
* Gegevens van bedrijven die met verschillende boekjaren en verschillende valuta's werken.  
* Het volledige bedrag of een percentage van de financiële gegevens van een bedrijf
* Verschillende wisselkoersen in afzonderlijke grootboekrekeningen gebruiken
* Bedrijven in andere boekhoudkundige en bedrijfsbeheerprogramma's

U stelt het geconsolideerde bedrijf in op dezelfde manier als waarop u andere bedrijven instelt. Het rekeningschema is onafhankelijk van de rekeningschema's in de andere bedrijfsunits en de rekeningschema's van de aparte bedrijfsunits wijken mogelijk van elkaar af. U stelt een lijst met te consolideren bedrijven in, controleert de boekhoudgegevens vóór de consolidatie, importeert uit bestanden of databases en genereert consolidatierapporten. Zie [Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md) voor meer informatie.  

> [!TIP]
> Consolideren van financiële gegevens kan vooral relevant zijn in verband met IC-processen. Raadpleeg [IC-transacties beheren](intercompany-manage.md) voor meer informatie.

## Proefbalans

Als u meerdere bedrijven in [!INCLUDE[prod_short](includes/prod_short.md)] hebt, kan het rapport **Consolidatie - Proefbalans** u inzicht bieden in de algehele financiële status van uw bedrijf.  

Het rapport combineert de grootboekposten van al uw bedrijven in een nieuw bedrijf dat u maakt om de geconsolideerde gegevens in op te nemen. Dit bedrijf wordt doorgaans het geconsolideerde bedrijf genoemd. Het geconsolideerde bedrijf is slechts een container voor de geconsolideerde gegevens en bevat geen live bedrijfsgegevens. De bedrijven die u in het geconsolideerde bedrijf opneemt, worden in het rapport **bedrijfsunits**. Zie [Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md) voor meer informatie.  

## Gegevens consolideren

Het proces van overdracht van de cijfers van de bedrijfsunits naar de geconsolideerde onderneming is de feitelijke *consolidatie*. Voordat u dit doet, doet u er goed aan te controleren of er verschillen zijn tussen de basisgegevens in de bedrijfsunits en het geconsolideerde bedrijf. Er zijn twee rapporten die u kunt gebruiken om de database en het bestand te testen.

### De gegevens testen vóór consolidatie

U kunt uw gegevens testen voordat u deze naar het geconsolideerde bedrijf overbrengt. [!INCLUDE[prod_short](includes/prod_short.md)] zoekt naar verschillen in de gegevens in de bedrijfsunits en in het geconsolideerde bedrijf. Er wordt bijvoorbeeld gecontroleerd of rekeningnummers of dimensiecodes afwijken. U moet fouten corrigeren voordat u het rapport kunt uitvoeren. U kunt de database testen, als u gegevens uit een XML-bestand importeert, of het bestand testen.  

1. Open het geconsolideerde bedrijf.  
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
3. Ga op een van de volgende manieren te werk:  

    * Als u een bestand wilt testen, kiest u de actie **Bestand testen**, voert u de naam van het bestand in en kiest u **Afdrukken**.  
    * Als u de database wilt testen, kiest u **Database testen**.  

### De consolidatie uitvoeren

Wanneer u de gegevens hebt getest, kunt deze naar het geconsolideerde bedrijf overbrengen.  

1. Meld u aan bij het geconsolideerde bedrijf.  
2. Kies in **Rolcentrum Accountant** de actie **Consolidatie uitvoeren**.  
3. Vul de vereiste velden in.  
4. Stel in de sectie Filter een filter in voor de relevante bedrijfsunit of bedrijfsnaam.  
5. Plan desgewenst de uitvoering van het rapport op een geschikte tijd.  

## Herhaalde transacties verwijderen

Nadat u alle bedrijven hebt geconsolideerd, moet u transacties zoeken die meer dan eens zijn vastgelegd in bedrijven en vervolgens verwijderposten boeken om ze te verwijderen.

Consolidatieverwijderingen boeken is een handmatig proces.  

Als u herhaalde transacties wilt verwijderen:

1. Zoek transacties die mogelijk moeten worden aangepast en voer dagboekregels in om ze te verwijderen.
2. Voer het rapport **Consolidatie - Eliminaties** uit om u te helpen de invloed van de dagboekregels te bepalen voorafgaand aan boeking.
3. Boek de aanpassingstransacties.

Het rapport **Consolidatie - Eliminaties** bevat een voorlopige proefbalans, waar u de gevolgen kunt simuleren van het verwijderen van posten door het vergelijken van de posten in het geconsolideerde bedrijf met de eliminaties die zijn ingevoerd in het algemene dagboek.

Als u een bedrijfsunit wilt opnemen in de lijst, moet u deze instellen op de pagina **Bedrijfsunits** en moet het veld **Consolideren** zijn ingeschakeld.

Elke account wordt afzonderlijk op een regel weergegeven, volgens de structuur van het rekeningschema. Een rekening wordt niet weergegeven als alle bedragen op de regel 0 zijn. De volgende gegevens worden voor elke rekening weergegeven:

* Rekeningnummer
* Rekeningnaam.
* Als u een of meer bedrijfsunitcodes hebt geselecteerd in het veld **Bedrijfsunit** op de aanvraagpagina, wordt een totaal weergegeven voor het geconsolideerde bedrijf zonder de geselecteerde bedrijfsunits en eliminaties. Hebt u het veld **Bedrijfsunit** niet ingevuld, dan wordt een totaal weergegeven voor het geconsolideerde bedrijf zonder de eliminaties.
* Als u een bedrijfsunitcode hebt geselecteerd in het veld **Bedrijfsunit** op de aanvraagpagina, wordt een totaal weergegeven voor de geïmporteerde posten uit de bedrijfsunit. Hebt u het veld **Bedrijfsunit** niet ingevuld, dan wordt een totaal weergegeven voor de geboekte eliminaties in het geconsolideerde bedrijf.
* Het totaal voor het geconsolideerde bedrijf met alle bedrijfsunits en geboekte eliminaties.
* De eliminaties in het geconsolideerde bedrijf, dat wil zeggen de posten in het dagboek dat is geselecteerd op de aanvraagpagina.
* De boekingstekst, gekopieerd uit het dagboek.
* Het totaal voor het geconsolideerde bedrijf na de eliminaties, als deze zijn geboekt.

## Geconsolideerde gegevens exporteren en importeren tussen databases

Als gegevens voor een bedrijfsunit zich in een andere database bevinden, moet u de gegevens naar een bestand exporteren voordat u deze kunt opnemen in de consolidatie. Elk bedrijf moet afzonderlijk worden geëxporteerd. Voor dit doel gebruikt u de batchverwerking **Consolidatie - Export**.  

> [!TIP]
> Gebruik hetzelfde proces om geconsolideerde gegevens te exporteren die moeten worden ingediend bij Dynamics 365 Finance, bijvoorbeeld als de huidige bedrijfsunit een dochteronderneming is en de moedermaatschappij Dynamics 365 Finance gebruikt.

Nadat u de batchtaak hebt uitgevoerd, worden alle posten in grootboekrekeningen verwerkt. Voor elke combinatie van geselecteerde dimensies en datum wordt de inhoud van het veld **Bedrag** van de posten opgeteld en geëxporteerd. De volgende combinatie van geselecteerde dimensies en datum met hetzelfde rekeningnummer wordt verwerkt, gevolgd door de combinaties voor het volgende rekeningnummer, enzovoorts.  

De geëxporteerde posten bevatten de volgende velden: **Bankrekeningnr.**, **Boekingsdatum** en **Bedrag**. Als tevens de dimensiegegevens zijn geëxporteerd, worden ook dimensiecodes en -waarden opgenomen.  

1. Voor elke geëxporteerde regel geldt dat als het totaal in de velden **Bedrag** een debetbedrag is, het rekeningnummer dat is ingesteld in het veld **Consolidatie debetrekening** van het bedrijf, naar de regel wordt geëxporteerd. Als het totaal een creditbedrag is, wordt het overeenkomstige getal in het veld **Consolidatie creditrekening** naar de regel geëxporteerd.  
2. De datum die wordt gebruikt voor elke geëxporteerde regel is de einddatum van de periode, of als de overdracht elke dag plaatsvindt, de exacte datum van de berekening.  
3. De dimensiewaarde die voor de boeking wordt geëxporteerd, is de geconsolideerde bedrijfsdimensiewaarde die is ingesteld in het veld **Consolidatiecode** voor die dimensiewaarde. Als u geen dimensiewaarde voor het geconsolideerde bedrijf hebt opgegeven in het veld **Geconsolideerde code** voor die dimensiewaarde, wordt de dimensiewaarde zelf naar de regel geëxporteerd.  
4. Bovendien bevatten de XML-bestanden ook de valutawisselkoersen binnen de consolidatieperiode. Deze koersen worden in een apart gedeelte aan het begin van het bestand opgenomen.  

## Zie ook

[Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md)  
[Intercompany-transacties beheren](intercompany-manage.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]