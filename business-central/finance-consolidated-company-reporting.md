---
title: Gegevens uit meerdere bedrijven consolideren | Microsoft Docs
description: "Krijg een overzicht van de financiële status van uw bedrijven."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 035eb85050ec6feb9e65ee924ebf4dbd2064e5ba
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Financiële gegevens uit meerdere bedrijven consolideren
Als u meerdere bedrijven in [!INCLUDE[d365fin](includes/d365fin_md.md)] hebt, kan het rapport Consolidatie - Proefbalans in het rolcentrum Accountant u inzicht bieden in de algehele financiële status van uw bedrijf.  

Het rapport combineert de grootboekposten van al uw bedrijven in een nieuw bedrijf dat u maakt om de geconsolideerde gegevens in op te nemen. Dit bedrijf wordt doorgaans het geconsolideerde bedrijf genoemd. Het geconsolideerde bedrijf is slechts een container voor de geconsolideerde gegevens en bevat geen live bedrijfsgegevens. De bedrijven die u in het geconsolideerde bedrijf opneemt, worden in het rapport **bedrijfsunits**.

Consolideren van financiële gegevens kan vooral relevant zijn in verband met IC-processen. Raadpleeg [IC-transacties beheren](intercompany-manage.md) voor meer informatie.

U kunt consolideren:  

* Gegevens van bedrijven met verschillende rekeningschema's.  
* Gegevens van bedrijven die met verschillende boekjaren en verschillende valuta's werken.  
* Het volledige bedrag of een percentage van de financiële gegevens van een bedrijf
* Verschillende wisselkoersen in afzonderlijke grootboekrekeningen gebruiken

Afhankelijk van de complexiteit van uw bedrijven, kunt u het rapport op twee manieren instellen:

* Als u geen geavanceerde instellingen nodig hebt, bijvoorbeeld om een bedrijf waarvan u slechts deels de eigenaar bent op te nemen, kunt u de begeleide instelling **Bedrijfconsolidatie** gebruiken om snel een consolidatie in te stellen. Hierbij wordt u door de basisstappen geleid.
* Als u meer geavanceerde instellingen nodig hebt, kunt u het geconsolideerde bedrijf en de bedrijfsunits zelf instellen.

## <a name="to-do-a-simple-consolidation-setup"></a>Een eenvoudige consolidatie instellen
Als de consolidatie ongecompliceerd is, bijvoorbeeld omdat u de enige eigenaar van de te consolideren bedrijfsunits bent, wordt u door de begeleide instellingen **Bedrijfconsolidatie** door de volgende stappen geleid:

* Geef op of er een nieuw geconsolideerd bedrijf moet worden gemaakt of dat de gegevens moeten worden geconsolideerd in een bedrijf dat u al voor de consolidatie hebt gemaakt. Het bedrijf moet geen transacties bevatten.
* Bekijk de resultaten. [!INCLUDE[d365fin](includes/d365fin_md.md)] verifieert of de hoofdgegevens en transacties naar het geconsolideerde bedrijf kunnen worden overgebracht.

Ga als volgt te werk om de begeleide instelling te gebruiken:

1. Kies in het rolcentrum **Accountant** de actie **Begeleide instelling**.
2. Kies **Consolidatierapportage instellen** en voltooi elke stap in de begeleide instelling.

## <a name="to-do-an-advanced-consolidation-setup"></a>Een geavanceerde consolidatie instellen
Als u meer geavanceerde instellingen voor de consolidatie nodig hebt, kunt u de consolidatie handmatig instellen. U kunt dit bijvoorbeeld doen als u bedrijven hebt die slechts deels uw eigendom zijn of die u niet in de consolidatie wilt opnemen. U stelt het geconsolideerde bedrijf op dezelfde manier in als andere bedrijven. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md).  

Met [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u een lijst met te consolideren bedrijven instellen, de boekhoudgegevens vóór de consolidatie controleren, bestanden importeren en consolidatierapporten genereren.  

1. Meld u aan bij het geconsolideerde bedrijf.
2. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
3. Kies **Nieuw** en vul vervolgens de vereiste velden in.  

Als de bedrijfsunit een vreemde valuta gebruikt, moet u de wisselkoers opgeven die in de consolidatie moet worden gebruikt. U moet ook consolidatiegegevens invoeren over de grootboekrekeningen van de bedrijfsunit. Deze processen worden beschreven in de volgende secties.

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a>Grootboekrekeningen voor consolidatie voorbereiden
Als het rekeningschema van de bedrijfsunit afwijkt van dat van het geconsolideerde bedrijf, moet u grootboekrekeningen voorbereiden voor consolidatie. U kunt de rekeningen voor het boeken van debet- en creditbedragen opgeven en instellen welke methode moet worden gebruikt voor de vertaling van valuta in het geconsolideerde bedrijf. Dit is bijvoorbeeld nuttig als u het rapport vaak uitvoert.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart voor de rekening en vul de velden op het sneltabblad **Consolidatie** in.

### <a name="to-specify-exchange-rates-for-consolidations"></a>Wisselkoersen opgeven voor consolidaties
Als een bedrijfsunit een andere valuta dan het geconsolideerde bedrijf gebruikt, moet u wisselkoersmethoden voor elke rekening opgeven voordat u de consolidatie uitvoert. Voor elke rekening bepaalt de inhoud van het veld **Consol.-vertaalmethode** de wisselkoers. Op elke bedrijfsunitkaart specificeert u in het veld **Wisselkoerstabel** of de consolidatie de wisselkoersen van de bedrijfsunit of van het geconsolideerde bedrijf moet gebruiken. Als u de wisselkoersen van het geconsolideerde bedrijf gebruikt, kunt u de wisselkoersen wijzigen voor een bedrijfseenheid. Als het veld **Wisselkoerstabel** op de bedrijfsunitkaart de waarde **Lokaal** bevat, kunt u de wisselkoers van de bedrijfsunitkaart wijzigen. De wisselkoersen worden overgenomen uit de tabel **Valutawisselkoers**, maar u kunt ze vóór de consolidatie wijzigen.

In de volgende tabel worden de wisselkoersmethoden beschreven die u voor rekeningen kunt gebruiken.

|Wisselkoers | Normaal gebruik |
|---|---|
|Gemiddelde koers (Handmatig) | U berekent de gemiddelde koers voor de te consolideren periode. Bereken het gemiddelde als rekenkundig gemiddelde of als schatting en geef het resultaat op voor elke bedrijfsunit. Wordt gebruikt voor resultatenrekening.|
|Wisselkoers (Balans) | Wordt gebruikt voor balansrekeningen.|
|Laatste wisselkoers (Balans) | De koers die gold op de vreemde-valutamarkt op de datum waarvoor de balans- of resultatenrekening wordt voorbereid. U geeft deze koers op voor elke bedrijfsunit. Wordt gebruikt voor balansrekeningen.|
|Historische wisselkoers | De wisselkoers die gold toen de transactie plaatsvond.|
|Samengestelde koers | De bedragen van de huidige periode worden vertaald tegen de gemiddelde koers en worden toegevoegd aan de eerder geregistreerde balans in het geconsolideerde bedrijf. Deze methode wordt vooral gebruikt voor het resultaat van het lopende boekjaar, omdat hiertoe bedragen uit verschillende perioden behoren en dit dus een samenstelling van bedragen is die zijn vertaald met verschillende wisselkoersen.|
|Aandelenkoers | Dit lijkt op **Samengestelde koers**. Verschillen worden geboekt naar verschillende grootboekrekeningen.|   

Ga als volgt te werk om wisselkoersen voor bedrijfsunits op te geven:

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in het venster **Overzicht bedrijfsunits** de bedrijfsunit en kies vervolgens de actie **Gemiddelde koers (Handmatig)**.   
3. In het venster **Wisselkoers wijzigen** is de inhoud van het veld **Gerel. wisselkoers** gekopieerd uit de tabel **Valutawisselkoers**, maar u kunt deze wijzigen. Sluit de pagina.  
4. Kies de actie **Wisselkoers (Balans)**.  
5. Voer in het veld **Gerel. wisselkoersbedrag** de wisselkoers in.

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a>Een bedrijf uitsluiten van consolidatie
Als u een bedrijfsunit niet wilt opnemen in de consolidatie, kunt u deze uitsluiten. Hiervoor gaat u naar de bedrijfsunitkaart en schakelt u het selectievakje **Consolideren** uit.

### <a name="to-include-a-partially-owned-company-in-consolidation"></a>Een bedrijf in de consolidatie opnemen dat deels uw eigendom is
Als u slechts een deel van een bedrijf bezit, kunt u een percentage van elke transactie opnemen dat overeenkomt met het percentage van het bedrijf dat in uw bezit is. Als u voor 70% eigenaar van het bedrijf bent, bevat de consolidatie bijvoorbeeld € 70 van een factuur voor € 100. Als u het percentage wilt opgeven dat het bedrijf van u is, gaat u naar de bedrijfsunitkaart en voert u het percentage in het veld **Consolidatie %** in.  

### <a name="to-test-the-data-before-you-consolidate"></a>De gegevens testen vóór consolidatie
U kunt uw gegevens testen voordat u deze naar het geconsolideerde bedrijf overbrengt. [!INCLUDE[d365fin](includes/d365fin_md.md)] zoekt naar verschillen in de gegevens in de bedrijfsunits en in het geconsolideerde bedrijf. Er wordt bijvoorbeeld gecontroleerd of rekeningnummers of dimensiecodes afwijken. U moet fouten corrigeren voordat u het rapport kunt uitvoeren. U kunt de database testen, als u gegevens uit een XML-bestand importeert, of het bestand testen.   

1. Open het geconsolideerde bedrijf.  
2. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
3. Ga op een van de volgende manieren te werk:  

    * Als u een bestand wilt testen, kiest u de actie **Bestand testen**, voert u de naam van het bestand in en kiest u **Afdrukken**.  
    * Als u de database wilt testen, kiest u **Database testen**.  

## <a name="to-run-the-consolidation"></a>De consolidatie uitvoeren
Wanneer u de gegevens hebt getest, kunt deze naar het geconsolideerde bedrijf overbrengen.  

1. Meld u aan bij het geconsolideerde bedrijf.  
2. Kies in **Rolcentrum Accountant** de actie **Consolidatie uitvoeren**.  
3. Vul de vereiste velden in.  
4. Kies in het veld **Waar** de optie **Bedrijfsnaam** en kies vervolgens het geconsolideerde bedrijf in het veld **is**.  

## <a name="to-export-and-import-consolidated-data-between-databases"></a>Geconsolideerde gegevens exporteren en importeren tussen databases
Als gegevens voor een bedrijfsunit zich in een andere database bevinden, moet u de gegevens naar een bestand exporteren voordat u deze kunt opnemen in de consolidatie. Elk bedrijf moet afzonderlijk worden geëxporteerd. Voor dit doel gebruikt u de batchverwerking **Consolidatie - Export**.  

Nadat u de batchtaak hebt uitgevoerd, worden alle posten in grootboekrekeningen verwerkt. Voor elke combinatie van geselecteerde dimensies en datum wordt de inhoud van het veld **Bedrag** van de posten opgeteld en geëxporteerd. De volgende combinatie van geselecteerde dimensies en datum met hetzelfde rekeningnummer wordt verwerkt, gevolgd door de combinaties voor het volgende rekeningnummer, enzovoorts.  

De geëxporteerde posten bevatten de volgende velden: **Bankrekeningnr.**, **Boekingsdatum** en **Bedrag**. Als tevens de dimensiegegevens zijn geëxporteerd, worden ook dimensiecodes en -waarden opgenomen.  

1. Voor elke geëxporteerde regel geldt dat als het totaal in de velden **Bedrag** een debetbedrag is, het rekeningnummer dat is ingesteld in het veld **Consolidatie debetrekening** van het bedrijf, naar de regel wordt geëxporteerd. Als het totaal een creditbedrag is, wordt het overeenkomstige getal in het veld **Consolidatie creditrekening** naar de regel geëxporteerd.  
2. De datum die wordt gebruikt voor elke geëxporteerde regel is de einddatum van de periode, of als de overdracht elke dag plaatsvindt, de exacte datum van de berekening.  
3. De dimensiewaarde die voor de boeking wordt geëxporteerd, is de geconsolideerde bedrijfsdimensiewaarde die is ingesteld in het veld **Consolidatiecode** voor die dimensiewaarde. Als u geen dimensiewaarde voor het geconsolideerde bedrijf hebt opgegeven in het veld **Geconsolideerde code** voor die dimensiewaarde, wordt de dimensiewaarde zelf naar de regel geëxporteerd.   
4. Bovendien bevatten de XML-bestanden ook de valutawisselkoersen binnen de consolidatieperiode. Deze koersen worden in een apart gedeelte aan het begin van het bestand opgenomen.

## <a name="see-also"></a>Zie ook
[Intercompany-transacties beheren](intercompany-manage.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)

