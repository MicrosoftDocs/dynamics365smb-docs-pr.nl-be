---
title: 'Procedure: ontvangen en opslaan in basismagazijnconfiguraties'
description: Lees meer over de verschillende manieren om inkomende processen voor ontvangst en opslag af te handelen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
---
# Procedure: ontvangen en opslaan in standaardmagazijnconfiguraties

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Inkomend proces|Ontvangst vereist|Opslag vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Ontvangst en opslag van de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken||Ingeschakeld|Basis: Order voor order|  
|H|Ontvangst en opslag van een magazijnontvangstdocument boeken|Ingeschakeld||Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Lees meer op [Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md).

De volgende procedure geeft methode B in de vorige tabel weer.  

## Informatie over deze procedure  

In standaardmagazijnconfiguraties waarbij voor uw vestiging de verwerking van opslag, maar niet van ontvangst vereist is, gebruikt u de pagina **Voorraadopslag** om opslag- en ontvangstinformatie voor de inkomende brondocumenten te verzamelen en boeken. De volgende documenten zijn inkomende brondocumenten:

* Inkooporder
* Verkoopretourorder
* Inkomende transferorder
* Productieorder met uitvoer die klaar is om weggezet te worden

> [!NOTE]
> Hoewel de instellingen **Pick vereist** en **Opslag vereist** worden genoemd, kunt u nog wel ontvangsten en verzendingen rechtstreeks vanuit de bronbedrijfsdocumenten boeken voor vestigingen waarvoor u deze selectievakjes inschakelt.  

In deze procedure worden de volgende taken gedemonstreerd:  

* Locatie ZILVER instellen voor voorraadopslag.  
* Locatie ZILVER instellen voor opslaglocatieverwerking.  
* Een standaardopslaglocatie voor artikel LS-81 definiëren. (LS-75 is al ingesteld in CRONUS.)  
* Een inkooporder voor leverancier 10000 voor 40 luidsprekers maken.  
* Controleren of de opslaglocaties vooringesteld zijn.  
* De inkooporder vrijgeven voor magazijnverwerking.  
* Een voorraadopslag maken op basis van een vrijgegeven brondocument.  
* Verifiëren dat de opslaglocaties worden overgenomen van de inkooporder.  
* De magazijnverplaatsing in het magazijn vastleggen en de inkoopontvangst voor de broninkooporder boeken.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Rollen  

De volgende gebruikerstaken voeren de taken uit die door dit overzicht worden gedemonstreerd:  

* Magazijnbeheerder  
* Inkoper  
* Magazijnmedewerker  

## Vereisten  

Voor deze procedure is het volgende nodig:  

* CRONUS International Ltd. gegevens  
* Magazijnmedewerker zijn op locatie ZILVER. Volg deze stappen om uzelf in te stellen:  

    1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies vervolgens de gerelateerde koppeling.  
    2. Kies het veld **Gebruikers-ID** en selecteer uw gebruikersaccount op de pagina **Gebruikers**.  
    3. Kies in het veld **Vestiging** de optie **ZILVER**.  
    4. Schakel het selectievakje **Standaard** in.  

## Scenario  

Ellen, de magazijnmanager bij CRONUS International Ltd., maakt een inkooporder voor 10 eenheden van artikel LS-75 en 30 eenheden van artikel LS-81 van leverancier 10000 om te worden afgeleverd bij magazijn ZILVER. Wanneer de bezorging in het magazijn aankomt, zet de magazijnmedewerker Johanna de artikelen in de standaardopslaglocaties die voor de artikelen zijn gedefinieerd. Wanneer Johanna de voorraadopslag boekt, worden de artikelen als ontvangen en beschikbaar voor verkoop of andere oproepen in de voorraad.  

## De vestiging instellen  

De instellingen van de pagina **Vestiging** definiëren de magazijnstromen van het bedrijf.  

### De vestiging instellen  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
2. Open de vestigingskaart ZILVER.  
3. Zet de schakelaar **Opslag vereist** aan.  

    Stel een standaardopslaglocatie in voor de twee artikelnummers om te bepalen waar deze worden opgeslagen.  

4. Kies de actie **Opslaglocaties**.  
5. Selecteer de eerste rij voor opslaglocatie **S-01-0001** en kies vervolgens de actie **Inhoud**.  

    U ziet op de pagina **Opslaglocatie-inhoud** dat artikel **LS-75** al is ingesteld als inhoud in opslaglocatie S-01-0001.  

6. Kies de actie **Nieuw**.  
7. Selecteer de velden **Vast** en **Standaard**.  
8. Voer in het veld **Artikelnummer** de waarde **LS-81** in.  

## De inkooporder maken  

Inkooporders zijn de meest gebruikte soort inkomend brondocument.  

### De inkooporder maken  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
2. Kies de actie **Nieuw**.  
3. Maak een inkooporder voor leverancier 10000 op 23 januari (werkdatum) met de volgende inkooporderregels.  

    |Artikel|Vestiging|Opslaglocatie|Aantal|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|ZILVER|S-01-0001|10|  
    |LS-81|ZILVER|S-01-0001|30|  

    > [!NOTE]  
    > De opslaglocatiecode wordt automatisch ingevoerd op basis van de instellingen die u in de sectie [De locatie instellen](#setting-up-the-location) hebt gemaakt.  

    Informeer vervolgens het magazijn dat de inkooporder klaar is voor de magazijnverwerking wanneer de bezorging aankomt.  

4. Kies de actie **Vrijgeven**.  

    Het leveren van luidsprekers van leverancier 10000 is aangekomen op magazijn SILVER en Jan bergt ze op.  

## De artikelen ontvangen en opslaan  

Op de pagina **Voorraadopslag** kunt u alle inkomende magazijnactiviteiten voor een bepaald brondocument beheren, zoals een inkooporder.  

### De artikelen ontvangen en opslaan  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadopslag** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Selecteer het veld **Brondocument** en selecteer vervolgens **Inkooporder**.  
4. Selecteer het veld **Bronnr.**, selecteer de regel voor de inkoop van leverancier 10000, en kies vervolgens de knop **OK**.  

    U kunt ook de actie **Brondocument ophalen** kiezen en de inkooporder kiezen.  

5. Kies de actie **Te verwerken aantal autom. invullen**.  

    Of voer in het veld **Te verwerken aantal** respectievelijk 10 en 30 in op de twee voorraadopslagregels.  

6. Kies de actie **Boeken**, selecteer de actie **Ontvangen** en kies vervolgens de knop **OK**.  

    Nu zijn de 40 luidsprekers geregistreerd als opgeslagen in opslaglocatie S-01-0001 en een positieve artikelpost is gemaakt om de geboekte inkoopontvangst te weerspiegelen.  

## Zie ook  

[Artikelen opslaan met voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Standaardmagazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md)  
[Artikelen ad hoc verplaatsen in standaardmagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Ontwerpdetails: Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md)  
[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]