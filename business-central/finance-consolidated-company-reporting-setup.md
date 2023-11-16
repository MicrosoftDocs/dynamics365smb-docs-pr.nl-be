---
title: Een bedrijfsconsolidatie instellen
description: Lees hoe u kunt configureren hoe gegevens van verschillende bedrijven in Business Central worden gerapporteerd aan een consolidatiebedrijf.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
---

# <a name="set-up-company-consolidation"></a>Een bedrijfsconsolidatie instellen

Voordat u de grootboekposten van twee of meer bedrijven (dochterondernemingen) in een geconsolideerd bedrijf kunt consolideren, moet u de rekeningschema's en het consolidatiebedrijf voorbereiden.  

Afhankelijk van de complexiteit van uw bedrijven kunt u consolidatie op twee manieren instellen:

* Als u geen geavanceerde instellingen nodig hebt, bijvoorbeeld om een bedrijf waarvan u slechts deels de eigenaar bent op te nemen, kunt u de instellingsguide **Bedrijfsconsolidatie** gebruiken om snel een consolidatie in te stellen. Hierbij wordt u door de basisstappen geleid.
* Als u meer geavanceerde instellingen nodig hebt, kunt u het geconsolideerde bedrijf en de bedrijfsunits zelf instellen.
  * Specificeer de grootboekrekeningen die van elke bedrijfsunit moeten worden opgenomen in de consolidatie en geef de consolidatievertaalmethode voor elke rekening op.
  * Stel in het geconsolideerde bedrijf een bedrijfsunitkaart in voor elk bedrijf dat moet worden opgenomen in de consolidatie. De bedrijfsunitkaart bevat informatie zoals de datums van het boekjaar van de bedrijfsunit en het percentage van elke rekening die moet worden opgenomen in de consolidatie.

## <a name="simple-consolidation-setup"></a>Eenvoudige consolidatie instellen

Als de consolidatie ongecompliceerd is, bijvoorbeeld omdat u de enige eigenaar van de te consolideren bedrijfsunits bent, wordt u door de guide **Bedrijfconsolidatie** door de volgende stappen geleid:

* Maak een nieuw geconsolideerd bedrijf of consolideer een bedrijf dat u al heeft gemaakt. Het bedrijf moet geen transacties bevatten.
* Bekijk de resultaten. [!INCLUDE[prod_short](includes/prod_short.md)] verifieert of u de hoofdgegevens en transacties naar het geconsolideerde bedrijf kunt overbrengen.

Ga als volgt te werk om de begeleide instelling te gebruiken:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Begeleide instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Consolidaties verwerken** en voltooi elke stap in de begeleide instelling Bedrijfsconsolidatie.

## <a name="advanced-consolidation-setup"></a>Geavanceerde consolidatie instellen

Als u meer geavanceerde instellingen voor de consolidatie nodig hebt, kunt u de consolidatie handmatig instellen. U kunt dit bijvoorbeeld doen als u bedrijven hebt die deels uw eigendom zijn of die u niet wilt opnemen.  

### <a name="set-up-the-consolidated-company"></a>Stel het geconsolideerde bedrijf in

U moet eerst het geconsolideerde bedrijf instellen. U stelt het geconsolideerde bedrijf in op dezelfde manier als waarop u andere bedrijven instelt. Ga voor meer informatie over het opzetten van een bedrijf naar [Voorbereid zijn om zaken te doen](ui-get-ready-business.md).  

De volgende lijst illustreert de belangrijkste aspecten van het geconsolideerde bedrijf.

1. Stel het rekeningschema in.

    Voor meer informatie over het instellen van een rekeningschema gaat u naar [De rekeningschema's instellen of wijzigen](finance-setup-chart-accounts.md).  

    De rekeningschema's kunnen identiek zijn voor een bedrijfsunit en het geconsolideerde bedrijf, of het geconsolideerde bedrijf kan een ander rekeningschema hebben. Als het rekeningschema van een bedrijfsunit verschilt van dat van het geconsolideerde bedrijf, moet u de rekeningen toewijzen aan de rekeningen in de bedrijfsunit. Ga voor meer informatie naar de sectie [Grootboekrekeningen voorbereiden voor consolidatie](#glacc).

2. Voeg bedrijfsunits toe.

    Als u gegevens van verschillende bedrijven wilt consolideren, moet u de dochterondernemingen instellen als bedrijfseenheden en opgeven hoeveel van hun saldi u wilt opnemen. Voor meer informatie over bedrijfseenheden gaat u naar de sectie [Bedrijfseenheden toevoegen](#busunit).

3. Geef indien nodig wisselkoersen op.

    Geef wisselkoersen op als u gegevens consolideert voor bedrijfsunits die verschillende valuta's gebruiken. De drie wisselkoersen die u kunt gebruiken, zijn **Gemiddelde koers (handmatig)**, **Wisselkoers** en **Laatste wisselkoers**. Voor meer informatie over wisselkoersen gaat u naar de sectie [Wisselkoersen opgeven voor consolidaties](#exchrates).

4. Consolideer dimensiegegevens en grootboekrekeningen.

    Ga voor meer informatie naar de sectie [Dimensies opnemen of uitsluiten](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Bedrijfsunits toevoegen

Stel in het geconsolideerde bedrijf elk bedrijf waaruit u gegevens wilt consolideren, in als een bedrijfsunit. Voordat u een consolidatie uitvoert en uw consolidatierapport genereert, is het een goed idee om de financiële gegevens in elke bedrijfsunit te verifiëren.

Een groot deel van het opzetten van de bedrijfsunit bestaat uit het specificeren hoe de unit zijn financiële gegevens met het geconsolideerde bedrijf zal delen. Er zijn handmatige en automatische opties.

* Om een handmatig proces te gebruiken, voor [!INCLUDE [prod_short](includes/prod_short.md)] online en on-premises, kunt u een XML-bestand exporteren dat de grootboekposten van de bedrijfsunit bevat. Importeer het bestand vervolgens in het geconsolideerde bedrijf.
* Om de gegevensuitwisseling te automatiseren, voor [!INCLUDE [prod_short](includes/prod_short.md)] online, kunt u een API gebruiken die [!INCLUDE [prod_short](includes/prod_short.md)] biedt, om gegevens te delen tussen omgevingen. Als uw bedrijven zich in dezelfde omgeving bevinden, kunt u de optie **Database** gebruiken.

> [!NOTE]
> Met de API-optie kunt u ook grootboekposten delen uit andere [!INCLUDE [prod_short](includes/prod_short.md)]-omgevingen. Om de API-optie te kunnen gebruiken moet de gebruiker die de consolidatie configureert, toestemming hebben voor toegang tot grootboekposten. De machtigingensets D365 Basis en D365 Lezen bieden bijvoorbeeld toegang.

1. Meld u aan bij het geconsolideerde bedrijf.
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
3. Kies **Nieuw** en vul vervolgens de verplichte velden in op de sneltabbladen **Algemeen** en **Grootboekrekeningen**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Wanneer u de velden **Begindatum** en **Einddatum** invult, moet u ervoor zorgen dat u GAAP-regels betreffende de boekhoudperioden van de bedrijfsunit versus het hoofdbedrijf naleeft.
4. Op het sneltabblad **Gegevens importeren** geeft u in het veld **Standaardmethode voor gegevensimport** op hoe u grootboekposten deelt met het geconsolideerde bedrijf:

   * Kies voor het delen van gegevens tussen bedrijven in dezelfde omgeving **Database**.
   * Kies voor het delen van gegevens tussen bedrijven in verschillende omgevingen **API** en vul vervolgens het veld **API-eindpunt** in.
        
        Om de eindpunt-URL op te halen opent u in de [!INCLUDE [prod_short](includes/prod_short.md)] van de bedrijfsunit de pagina **Bedrijfsunitkaart** en kiest u de actie **Instellingen**. 
   * Als u een .xml-bestand wilt exporteren en handmatig wilt delen, kiest u **Bestandsindeling**.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Grootboekrekeningen voor consolidatie voorbereiden

Het rekeningschema van een bedrijf dat geconsolideerd wordt, moet u rekeningen voor de consolidatie specificeren. Voor elke boekingsgrootboekrekening in elk bedrijf moet u de grootboekrekening in het geconsolideerde bedrijf opgeven waarnaar de balans moet worden overgebracht. Met deze toewijzing kunt u bedrijven consolideren die verschillende rekeningschema's hebben.

Als het rekeningschema van de bedrijfsunit afwijkt van dat van het geconsolideerde bedrijf, moet u grootboekrekeningen voorbereiden voor consolidatie. U kunt de rekeningen voor het boeken van debet- en creditbedragen opgeven en instellen welke methode moet worden gebruikt voor de vertaling van valuta in het geconsolideerde bedrijf.

1. Kies in elke bedrijfsunit [!INCLUDE [prod_short](includes/prod_short.md)], kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Open de kaart voor de rekening en vul de velden op het sneltabblad **Consolidatie** in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Wisselkoersen opgeven voor consolidaties

Als een bedrijfsunit een andere valuta dan het geconsolideerde bedrijf gebruikt, moet u wisselkoersmethoden voor elke rekening opgeven voordat u de consolidatie uitvoert. Voor elke rekening bepaalt de inhoud van het veld **Consol.-vertaalmethode** de wisselkoers. Op elke bedrijfsunitkaart specificeert u in het veld **Wisselkoerstabel** of de consolidatie de wisselkoersen van de bedrijfsunit of van het geconsolideerde bedrijf moet gebruiken. Als u de wisselkoersen van het geconsolideerde bedrijf gebruikt, kunt u de wisselkoersen wijzigen voor een bedrijfseenheid. Als het veld **Wisselkoerstabel** op de bedrijfsunitkaart de waarde **Lokaal** bevat, kunt u de wisselkoers van de bedrijfsunitkaart wijzigen. De wisselkoersen worden overgenomen uit de tabel **Valutawisselkoers**, maar u kunt ze vóór de consolidatie wijzigen.

In de volgende tabel worden de wisselkoersmethoden beschreven die u voor rekeningen kunt gebruiken.

|Wisselkoers | Normaal gebruik |
|---|---|
|Gemiddelde koers (Handmatig) | U berekent de gemiddelde koers voor de te consolideren periode. Bereken het gemiddelde als rekenkundig gemiddelde of als schatting en geef het resultaat op voor elke bedrijfsunit. Wordt gebruikt voor resultatenrekeningen.|
|Wisselkoers (Balans) | Wordt gebruikt voor balansrekeningen.|
|Laatste wisselkoers (Balans) | De koers die gold op de vreemde-valutamarkt op de datum waarvoor de balans- of resultatenrekening wordt voorbereid. U geeft deze koers op voor elke bedrijfsunit. Wordt gebruikt voor balansrekeningen.|
|Historische wisselkoers | De wisselkoers die gold toen de transactie plaatsvond.|
|Samengestelde koers | De bedragen van de huidige periode worden vertaald tegen de gemiddelde koers en worden toegevoegd aan de eerder geregistreerde balans in het geconsolideerde bedrijf. Normaal gesproken gebruikt u deze methode voor ingehouden winstrekeningen. Deze rekeningen bevatten bedragen uit verschillende perioden en bevatten dus bedragen die zijn omgerekend met verschillende wisselkoersen.|
|Aandelenkoers | Deze optie lijkt op **Samengestelde koers**. Verschillen worden geboekt naar verschillende grootboekrekeningen.|

Ga als volgt te werk om wisselkoersen voor bedrijfsunits op te geven:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsunits** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Overzicht bedrijfsunits** de bedrijfsunit en kies vervolgens de actie **Gemiddelde koers (Handmatig)**.  
3. Op de pagina **Wisselkoers wijzigen** is de inhoud van het veld **Gerel. wisselkoers** gekopieerd uit de tabel **Valutawisselkoers**, maar u kunt deze wijzigen. Sluit de pagina.  
4. Kies de actie **Wisselkoers (Balans)**.  
5. Voer in het veld **Gerel. wisselkoersbedrag** de wisselkoers in.

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Dimensies opnemen of uitsluiten

U kunt dimensiegegevens en grootboekrekeningen consolideren.

* Geef in de dimensies het veld **Consolidatiecode** op of laat het leeg.
  * Als u een dimensie in de consolidatie wilt uitsluiten, laat u het veld **Consolidatiecode** leeg voor de dimensie en kiest u geen dimensies in de **Dimensies kopiëren**-velden in consolidatiefuncties of rapporten.
  * Als u dimensie-informatie in de consolidatie wilt opnemen, laat u het veld **Consolidatiecode** leeg. De consolidatie werkt echter alleen als de dimensiewaarden in de bedrijfsunit hetzelfde zijn als die van het geconsolideerde bedrijf.
  * Als u de dimensiewaardecode in de bedrijfsunit wilt consolideren met een andere dimensiewaardecode in het geconsolideerde bedrijf, vult u het veld **Consolidatiecode** voor de dimensies in.  
* Voeg de dimensies toe aan de grootboekrekeningen.

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Een bedrijf uitsluiten van consolidatie

Als u een bedrijfsunit niet wilt opnemen in de consolidatie, kunt u deze uitsluiten. Hiervoor gaat u naar de bedrijfsunitkaart en schakelt u het selectievakje **Consolideren** uit.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Een bedrijf dat deels eigendom is, opnemen in een consolidatie

Als u slechts een deel van een bedrijf bezit, kunt u een percentage van elke transactie opnemen dat overeenkomt met het percentage dat in uw bezit is. Als u voor 70% eigenaar van het bedrijf bent, bevat de consolidatie bijvoorbeeld € 70 van een factuur voor € 100. Als u het percentage wilt opgeven dat het bedrijf van u is, gaat u naar de bedrijfsunitkaart en voert u het percentage in het veld **Consolidatie %** in.  

## <a name="see-also"></a>Zie ook

[Financiële gegevens uit meerdere bedrijven consolideren](finance-consolidated-company-reporting.md)  
[Intercompany-transacties beheren](intercompany-manage.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uw bedrijfsgegevens naar Excel exporteren](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
