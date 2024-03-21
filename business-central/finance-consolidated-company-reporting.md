---
title: Gegevens uit meerdere bedrijven consolideren
description: In dit artikel wordt uitgelegd hoe u de grootboekposten van twee of meer aparte bedrijven (dochterbedrijven) consolideert tot één geconsolideerd bedrijf.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# Financiële gegevens uit meerdere bedrijven consolideren

Sommige organisaties gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in meerdere bedrijfsunits of rechtspersonen. Andere gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in dochterondernemingen die moeten rapporteren aan moederorganisaties. [!INCLUDE [prod_short](includes/prod_short.md)] geeft accountants tools waarmee ze grootboekposten van twee of meer bedrijven (dochterondernemingen) kunnen overbrengen naar een geconsolideerd bedrijf.  

Elk bedrijf dat betrokken is bij een consolidatie, wordt een bedrijfsunit genoemd. Het bedrijf waarin u de gegevens combineert, wordt het geconsolideerde bedrijf genoemd.  

U kunt financiële gegevens van dochterondernemingen naar het geconsolideerde bedrijf overbrengen, zelfs als de dochterondernemingen [!INCLUDE [prod_short](includes/prod_short.md)] in verschillende omgevingen gebruiken. Voor meer informatie over hoe u verbinding kunt maken met andere omgevingen gaat u naar [Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md#busunit).

Als de financiële overzichten van een bedrijfsunit een andere valuta gebruiken dan die van het geconsolideerde bedrijf, moet u wisselkoersen instellen voor de consolidatie. Ga voor meer informatie over wisselkoersen voor consolidaties naar [Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md#exchrates).  

U kunt consolideren:  

* Gegevens van bedrijven met verschillende rekeningschema's.  
* Gegevens van bedrijven die met verschillende boekjaren en verschillende valuta's werken.  
* Het volledige bedrag of een percentage van de financiële gegevens van een bedrijf.
* Verschillende wisselkoersen in afzonderlijke grootboekrekeningen gebruiken.
* Bedrijven in andere boekhoudkunde- en bedrijfsbeheerprogramma's.
* Bedrijven in verschillende [!INCLUDE [prod_short](includes/prod_short.md)]-omgevingen.

U stelt het geconsolideerde bedrijf in op dezelfde manier als waarop u andere bedrijven instelt. Het rekeningschema is onafhankelijk van het rekeningschema in de bedrijfsunits. Het rekeningschema in de bedrijfsunits kan van elkaar verschillen. Ga voor meer informatie over het instellen van een consolidatie naar [Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Consolideren van financiële gegevens kan vooral relevant zijn voor IC-processen. Ga voor meer informatie over IC-functies naar [IC-transacties beheren](intercompany-manage.md).

## Gegevens consolideren

Voordat u gaat consolideren, is het een goed idee om uw gegevens te testen voordat u deze overdraagt naar het geconsolideerde bedrijf. [!INCLUDE[prod_short](includes/prod_short.md)] zoekt naar verschillen in de gegevens in de bedrijfsunits en in het geconsolideerde bedrijf. Er wordt bijvoorbeeld gecontroleerd of rekeningnummers of dimensiecodes afwijken. Corrigeer eventuele fouten die u vindt, voordat u het rapport uitvoert. U kunt de database testen of het bestand als u gegevens uit een XML-bestand importeert.

### De gegevens testen voordat u consolideert

1. Open het geconsolideerde bedrijf.  
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
3. Test het bestand en de database als volgt:  

    * Als u een bestand wilt testen, kiest u de actie **Bestand testen**, voert u de naam van het bestand in en kiest u **Afdrukken**.  
    * Als u de database wilt testen, kiest u **Database testen**.  

### De consolidatie uitvoeren

Wanneer u de gegevens hebt getest, kunt deze naar het geconsolideerde bedrijf overbrengen. Een begeleide instelling helpt u door het proces.

> [!NOTE]
> Wanneer u de consolidatie uitvoert, kunt u de bedrijven kiezen die u wilt opnemen. Als uw geconsolideerde onderneming geen toegang heeft tot een of meer dochterondernemingen, kunt u met de guide toegang daartoe verlenen.

1. Meld u aan bij het geconsolideerde bedrijf.  
2. Kies op de pagina **Bedrijfsunits** de actie **Consolideren**.  
3. Vul de vereiste velden in.  

## Gebruik het rapport Consolidatie - Proef- en saldibalans uitvoeren

Het rapport **Consolidatie - Proefbalans** kan u een overzicht geven van de algehele financiële gezondheid van uw bedrijf. Het rapport combineert grootboekposten van elk van uw bedrijven in een nieuw bedrijf dat u hebt gemaakt voor de geconsolideerde gegevens. Het geconsolideerde bedrijf is slechts een container voor de geconsolideerde gegevens en bevat geen live bedrijfsgegevens. De bedrijven die u in het geconsolideerde bedrijf opneemt, worden in het rapport **bedrijfsunits**. Heeft u vier of minder bedrijfsonderdelen, dan kunt u ook gebruik maken van het rapport **Consolidatie - Proefbalans (4)**.  

Het rapport toont een regel voor elke rekening en volgt de structuur van het rekeningschema. Een rekening wordt niet weergegeven als alle bedragen op de regel 0 zijn. Het rapport toont de volgende informatie voor elk account:

* Het rekeningnummer en de naam van de rekening.
* De totalen voor het geconsolideerde bedrijf en voor elke bedrijfsunit. Totalen kunnen worden weergegeven als een nettowijziging of als het saldo tot en met datum.
* De eliminaties die in het geconsolideerde bedrijf zijn gemaakt. Eliminaties worden altijd weergegeven voor een periode die overeenkomt met het boekjaar van het geconsolideerde bedrijf.
* Het totaal voor het geconsolideerde bedrijf na de eliminaties, weergegeven als mutatie of als saldo tot en met datum.

## Herhaalde transacties verwijderen

Nadat u de bedrijven hebt geconsolideerd, moet u alle transacties vinden en elimineren die meer dan eens in bedrijven zijn geregistreerd. Consolidatieverwijderingen boeken is een handmatig proces.  

Als u herhaalde transacties wilt verwijderen:

1. Zoek transacties die mogelijk moeten worden aangepast en voer algemene dagboekregels in om ze te verwijderen.
2. Voer het rapport **Consolidatie - Eliminaties** uit om u te helpen de invloed van de dagboekregels te bepalen voorafgaand aan boeking.
3. Boek de aanpassingstransacties.

Het rapport **Consolidatie - Eliminaties** geeft een voorlopige proefbalans weer waarin u de gevolgen van het elimineren van boekingen kunt simuleren. Het rapport vergelijkt de boekingen in het geconsolideerde bedrijf met de eliminaties die in het dagboek zijn ingevoerd.

Voordat een bedrijfsunit in het rapport kunt opnemen, moet u de unit instellen op de pagina **Bedrijfsunits**. Zorg ervoor dat u de schakelaar **Consolideren** aanzet.

Voor elke rekening wordt een regel aangemaakt volgens de structuur van het rekeningschema. Een rekening wordt niet weergegeven als alle bedragen op de regel 0 zijn. Het rapport toont de volgende informatie voor elk account:

* Rekeningnummer.
* Rekeningnaam.
* Als u een of meer bedrijfsunitcodes hebt geselecteerd in het veld **Bedrijfsunit** op de aanvraagpagina, wordt een totaal weergegeven voor het geconsolideerde bedrijf zonder de geselecteerde bedrijfsunits en eliminaties. Hebt u het veld **Bedrijfsunit** niet ingevuld, dan wordt het totaal weergegeven voor het geconsolideerde bedrijf, zonder de eliminaties.
* Als u een bedrijfsunitcode hebt geselecteerd in het veld **Bedrijfsunit** op de aanvraagpagina, wordt een totaal weergegeven voor de geïmporteerde posten uit de bedrijfsunit. Hebt u het veld **Bedrijfsunit** niet hebt ingevuld, dan wordt een totaal weergegeven voor de geboekte eliminaties in het geconsolideerde bedrijf.
* Het totaal voor het geconsolideerde bedrijf met alle bedrijfsunits en geboekte eliminaties.
* De te maken eliminaties in het geconsolideerde bedrijf. Dat wil zeggen de boekingen in het dagboek die op de aanvraagpagina zijn geselecteerd.
* De boekingstekst, gekopieerd uit het dagboek.
* Het totaal voor het geconsolideerde bedrijf na de eliminaties, als deze zijn geboekt.

## Geconsolideerde gegevens exporteren en importeren tussen databases

Als gegevens voor een bedrijfsunit zich in een andere database bevinden, kunt u een handmatige bestandsgebaseerde overdracht uitvoeren of het proces automatiseren met behulp van een API. Ga voor meer informatie over de API naar [Onze API gebruiken om automatisch gegevens tussen omgevingen te delen](#use-our-api-to-automatically-share-data-across-environments).

In dit gedeelte wordt het handmatige, op bestanden gebaseerde proces beschreven.

U exporteert de gegevens naar een bestand voordat u deze in de consolidatie opneemt. Exporteer elk bedrijf afzonderlijk met behulp van de batchverwerking **Consolidatie - Export**.  

> [!TIP]
> Gebruik hetzelfde proces om geconsolideerde gegevens te exporteren die u moet indienen bij Dynamics 365 Finance. Als de bedrijfsunit bijvoorbeeld een dochteronderneming is en het moederbedrijf Dynamics 365 Finance gebruikt.

Nadat u de batchtaak hebt uitgevoerd, worden alle posten in grootboekrekeningen verwerkt. Voor elke combinatie van geselecteerde dimensies en datum wordt de inhoud van het veld **Bedrag** van de posten opgeteld en geëxporteerd. De volgende combinatie van de geselecteerde dimensies en datum met hetzelfde rekeningnummer wordt verwerkt. Vervolgens worden de combinaties in het volgende rekeningnummer verwerkt, enzovoort.  

De geëxporteerde posten bevatten de volgende velden: **Bankrekeningnr.**, **Boekingsdatum** en **Bedrag**. Als tevens de dimensiegegevens zijn geëxporteerd, worden ook dimensiecodes en -waarden opgenomen.  

1. Voor elke geëxporteerde regel geldt dat als het totaal in de velden **Bedrag** een debetbedrag is, het rekeningnummer dat is ingesteld in het veld **Consolidatie debetrekening** van het bedrijf, naar de regel wordt geëxporteerd. Als het totaal een creditbedrag is, wordt het overeenkomstige getal in het veld **Consolidatie creditrekening** naar de regel geëxporteerd.  
2. De datum die wordt gebruikt voor elke geëxporteerde regel is de einddatum van de periode, of als de overdracht elke dag plaatsvindt, de exacte datum van de berekening.  
3. De dimensiewaarde die voor de boeking wordt geëxporteerd, is de geconsolideerde bedrijfsdimensiewaarde die is gespecificeerd in het veld **Consolidatiecode** voor die dimensiewaarde. Als er geen dimensiewaarde voor het geconsolideerde bedrijf is opgegeven in het veld **Geconsolideerde code** voor de dimensiewaarde, wordt de dimensiewaarde zelf naar de regel geëxporteerd.  
4. Bovendien bevatten de XML-bestanden ook de valutawisselkoersen binnen de consolidatieperiode. Deze koersen worden in een apart gedeelte aan het begin van het bestand opgenomen.  

## Onze API gebruiken om automatisch gegevens tussen omgevingen te delen

[!INCLUDE [prod_short](includes/prod_short.md)] biedt een API waarmee u het proces van het delen van financiële gegevens van bedrijfsunits naar het geconsolideerde bedrijf kunt automatiseren. De API is gratis te gebruiken en eenvoudig in te stellen. U kunt er zelfs gegevens mee delen tussen [!INCLUDE [prod_short](includes/prod_short.md)]. Het is bijvoorbeeld mogelijk dat u meerdere omgevingen wilt delen wanneer bedrijfsunits zich niet in dezelfde Azure-geografieën bevinden. Ga voor meer informatie over het gebruik van de API om het consolidatieproces te automatiseren naar [Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md#busunit).

## Zie ook

[Bedrijfsconsolidatie instellen](finance-consolidated-company-reporting-setup.md)  
[Intercompany-transacties beheren](intercompany-manage.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]