---
title: Een bedrijfsconsolidatie instellen
description: Lees hoe u kunt configureren hoe gegevens van verschillende bedrijven in Business Central worden gerapporteerd aan een consolidatiebedrijf.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-company-consolidation" />Een bedrijfsconsolidatie instellen

Voordat u de grootboekposten van twee of meer afzonderlijke bedrijven (dochterondernemingen) in een geconsolideerd bedrijf kunt consolideren, moet u de rekeningschema's en het consolidatiebedrijf voorbereiden.  

Afhankelijk van de complexiteit van uw bedrijven kunt u consolidatie op twee manieren instellen:

* Als u geen geavanceerde instellingen nodig hebt, bijvoorbeeld om een bedrijf waarvan u slechts deels de eigenaar bent op te nemen, kunt u de begeleide instelling **Bedrijfsconsolidatie** gebruiken om snel een consolidatie in te stellen. Hierbij wordt u door de basisstappen geleid.
* Als u meer geavanceerde instellingen nodig hebt, kunt u het geconsolideerde bedrijf en de bedrijfsunits zelf instellen.
  * Specificeer welke grootboekrekeningen van elke bedrijfsunit moeten worden opgenomen in de consolidatie en geef de consolidatievertaalmethode voor elke rekening op.
  * Stel in het consolidatiebedrijf een bedrijfsunitkaart in voor elk bedrijf dat moet worden opgenomen in de consolidatie. De bedrijfsunitkaart bevat informatie zoals de datums van het boekjaar van de bedrijfsunit en het percentage van elke rekening die moet worden opgenomen in de consolidatie.

## <a name="simple-consolidation-setup" />Eenvoudige consolidatie instellen

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Als de consolidatie ongecompliceerd is, bijvoorbeeld omdat u de enige eigenaar van de te consolideren bedrijfsunits bent, wordt u door de begeleide instellingen **Bedrijfconsolidatie** door de volgende stappen geleid:

* Geef op of er een nieuw geconsolideerd bedrijf moet worden gemaakt of dat de gegevens moeten worden geconsolideerd in een bedrijf dat u al voor de consolidatie hebt gemaakt. Het bedrijf moet geen transacties bevatten.
* Bekijk de resultaten. [!INCLUDE[prod_short](includes/prod_short.md)] verifieert of de hoofdgegevens en transacties naar het geconsolideerde bedrijf kunnen worden overgebracht.

Ga als volgt te werk om de begeleide instelling te gebruiken:

1. Kies in het rolcentrum **Accountant** de actie **Begeleide instelling**.
2. Kies **Consolidatierapportage instellen** en voltooi elke stap in de begeleide instelling.

## <a name="advanced-consolidation-setup" />Geavanceerde consolidatie instellen

Als u meer geavanceerde instellingen voor de consolidatie nodig hebt, kunt u de consolidatie handmatig instellen. U kunt dit bijvoorbeeld doen als u bedrijven hebt die slechts deels uw eigendom zijn of die u niet in de consolidatie wilt opnemen.  

### <a name="set-up-the-consolidated-company" />Het geconsolideerde bedrijf instellen

U moet eerst het geconsolideerde bedrijf instellen. U stelt het geconsolideerde bedrijf in op dezelfde manier als waarop u andere bedrijven instelt. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md).  

De volgende lijst illustreert de belangrijkste aspecten van het geconsolideerde bedrijf.

1. Het rekeningschema instellen

    Voor meer informatie raadpleegt u [Het rekeningschema instellen of wijzigen](finance-setup-chart-accounts.md).  

    De rekeningschema's kunnen identiek zijn voor een bedrijfsunit en het geconsolideerde bedrijf, of het geconsolideerde bedrijf kan een ander rekeningschema hebben. Als het rekeningschema van een bedrijfsunit verschilt van dat van het geconsolideerde bedrijf, moet u de toewijzing tussen rekeningen op de rekeningen in de bedrijfsunit opgeven. Zie voor meer informatie de sectie [Grootboekrekeningen voorbereiden voor consolidatie](#glacc).

2. Bedrijfsunits toevoegen

    Voor het consolideren van de financiële gegevens van meerdere bedrijven in een geconsolideerd bedrijf moet u gegevens opgeven over zowel het dochterbedrijf als de bedrijfsunits die worden opgenomen en over de mate waarin de cijfers ervan worden opgenomen.

    Zie voor meer informatie de sectie [Bedrijfsunits toevoegen](#busunit).
3. U kunt wisselkoersen opgeven wanneer u de financiële overzichten van bedrijfsunits consolideert als de financiële overzichten in een vreemde valuta zijn.

    De drie wisselkoersen die worden gebruikt, zijn **Gemiddelde koers (handmatig)**, **Wisselkoers** en **Laatste wisselkoers**. Zie voor meer informatie de sectie [Wisselkoersen opgeven voor consolidaties](#exchrates).
4. U kunt dimensiegegevens en grootboekrekeningen consolideren.

    Zie voor meer informatie de sectie [Dimensies opnemen of uitsluiten](#dim).

### <a name="add-business-units" /><a name="busunit"></a>Bedrijfsunits toevoegen

Met [!INCLUDE[prod_short](includes/prod_short.md)] kunt u een lijst met te consolideren bedrijfsunits instellen, de boekhoudgegevens vóór de consolidatie controleren, bestanden importeren en consolidatierapporten genereren.  

1. Meld u aan bij het geconsolideerde bedrijf.
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
3. Kies **Nieuw** en vul vervolgens de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Wanneer u de velden **Begindatum** en **Einddatum** invult, moet u ervoor zorgen dat u GAAP-regels betreffende de boekhoudperioden van de bedrijfsunit versus het hoofdbedrijf naleeft.
4. Herhaal stap 3 voor elke extra bedrijfsunit

Als de bedrijfsunit een vreemde valuta gebruikt, moet u de wisselkoers opgeven die in de consolidatie moet worden gebruikt. U moet ook consolidatiegegevens invoeren over de grootboekrekeningen van de bedrijfsunit. Deze processen worden beschreven in de volgende secties.

### <a name="prepare-general-ledger-accounts-for-consolidation" /><a name="glacc"></a>Grootboekrekeningen voor consolidatie voorbereiden

Het rekeningschema van een bedrijf dat wordt geconsolideerd, moet rekeningen voor de consolidatie specificeren. Voor elke boekingsgrootboekrekening in elk bedrijf moet u de grootboekrekening in het geconsolideerde bedrijf opgeven waarnaar de balans wordt overgebracht bij consolidatie. Dit is een toewijzing waarmee bedrijven met een ander rekeningschema samen worden geconsolideerd.

Als het rekeningschema van de bedrijfsunit afwijkt van dat van het geconsolideerde bedrijf, moet u grootboekrekeningen voorbereiden voor consolidatie. U kunt de rekeningen voor het boeken van debet- en creditbedragen opgeven en instellen welke methode moet worden gebruikt voor de vertaling van valuta in het geconsolideerde bedrijf. Dit is bijvoorbeeld nuttig als u het rapport vaak uitvoert.

1. Kies in elke bedrijfsunit [!INCLUDE [prod_short](includes/prod_short.md)], kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Open de kaart voor de rekening en vul de velden op het sneltabblad **Consolidatie** in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations" /><a name="exchrates"></a>Wisselkoersen opgeven voor consolidaties

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

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Overzicht bedrijfsunits** de bedrijfsunit en kies vervolgens de actie **Gemiddelde koers (Handmatig)**.  
3. Op de pagina **Wisselkoers wijzigen** is de inhoud van het veld **Gerel. wisselkoers** gekopieerd uit de tabel **Valutawisselkoers**, maar u kunt deze wijzigen. Sluit de pagina.  
4. Kies de actie **Wisselkoers (Balans)**.  
5. Voer in het veld **Gerel. wisselkoersbedrag** de wisselkoers in.

### <a name="include-or-exclude-dimensions" /><a name="dim"></a>Dimensies opnemen of uitsluiten

U kunt dimensiegegevens en grootboekrekeningen consolideren.

* Geef in de relevante dimensies het veld **Consolidatiecode** op of laat het leeg
  * Als u een dimensie in de consolidatie wilt uitsluiten, laat u het veld **Consolidatiecode** leeg voor de dimensie en kiest u geen dimensies in de **Dimensies kopiëren**-velden in consolidatiefuncties of rapporten.
  * Als u dimensie-informatie in de consolidatie wilt opnemen, laat u het veld **Consolidatiecode** leeg. De consolidatie werkt echter alleen als de dimensiewaarden in de bedrijfsunit hetzelfde zijn als die van het geconsolideerde bedrijf.
  * Als u de dimensiewaardecode in de bedrijfsunit wilt consolideren met een andere dimensiewaardecode in het geconsolideerde bedrijf, vult u het veld **Consolidatiecode** voor de relevante dimensies in.  
* Voeg de relevante dimensies toe aan de relevante grootboekrekeningen

### <a name="exclude-a-company-from-consolidation" /><a name="exclude"></a>Een bedrijf uitsluiten van consolidatie

Als u een bedrijfsunit niet wilt opnemen in de consolidatie, kunt u deze uitsluiten. Hiervoor gaat u naar de bedrijfsunitkaart en schakelt u het selectievakje **Consolideren** uit.

### <a name="include-a-partially-owned-company-in-consolidation" /><a name="include"></a>Een bedrijf dat deels eigendom is, opnemen in een consolidatie

Als u slechts een deel van een bedrijf bezit, kunt u een percentage van elke transactie opnemen dat overeenkomt met het percentage van het bedrijf dat in uw bezit is. Als u voor 70% eigenaar van het bedrijf bent, bevat de consolidatie bijvoorbeeld € 70 van een factuur voor € 100. Als u het percentage wilt opgeven dat het bedrijf van u is, gaat u naar de bedrijfsunitkaart en voert u het percentage in het veld **Consolidatie %** in.  

## <a name="see-also" />Zie ook

[Financiële gegevens uit meerdere bedrijven consolideren](finance-consolidated-company-reporting.md)  
[Intercompany-transacties beheren](intercompany-manage.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
