---
title: 'Procedure: ontvangen en opslaan in basismagazijnconfiguraties'
description: In Business Central kunnen de inkomende processen voor ontvangst en opslag op vier verschillende manieren worden uitgevoerd, afhankelijk van het complexiteitsniveau van het magazijn.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cca66a1e693e63b1d83b6d37d3f8c2957b3edf46
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144527"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Procedure: ontvangen en opslaan in standaardmagazijnconfiguraties

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

In [!INCLUDE[prod_short](includes/prod_short.md)] kunnen de inkomende processen voor ontvangst en opslag op vier manieren worden uitgevoerd met verschillende functionaliteiten, afhankelijk van het complexiteitsniveau van het magazijn.  

|Methode|Inkomend proces|Opslaglocaties|Ontvangsten|Magazijnopslag|Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Ontvangst en opslag van de orderregel boeken|X|||2|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken|||X|3|  
|L|Ontvangst en opslag van een magazijnontvangstdocument boeken||X||5-4-6|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken||X|X|5-4-6|  

Zie voor meer informatie [Ontwerpdetails: Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md).  

De volgende procedure geeft methode B in de vorige tabel weer.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure  
In standaardmagazijnconfiguraties waarbij voor uw vestiging de verwerking van opslag, maar niet van ontvangst vereist is, gebruikt u de pagina **Voorraadopslag** om opslag- en ontvangstinformatie voor de inkomende brondocumenten te verzamelen en boeken. Het inkomende brondocument kan een inkooporder zijn, maar ook een verkoopretourorder, een inkomende transferorder of een productieorder met output die kan worden opgeslagen.

> [!NOTE]
> Hoewel de instellingen **Pick vereist** en **Opslag vereist** worden genoemd, kunt u nog wel ontvangsten en verzendingen rechtstreeks vanuit de bronbedrijfsdocumenten boeken voor vestigingen waarvoor u deze selectievakjes inschakelt.  

In deze procedure worden de volgende taken gedemonstreerd.  

-   Locatie ZILVER instellen voor voorraadopslag.  
-   Locatie ZILVER instellen voor opslaglocatieverwerking.  
-   Een standaardopslaglocatie voor artikel LS-81 definiëren. (LS-75 is al ingesteld in CRONUS.)  
-   Maak een inkooporder voor leverancier 10000 voor 40 luidsprekers.  
-   Controleren of de opslaglocaties vooringesteld zijn.  
-   De inkooporder vrijgeven voor magazijnverwerking.  
-   Een voorraadopslag maken op basis van een vrijgegeven brondocument.  
-   Verifiëren dat de opslaglocaties worden overgenomen van de inkooporder.  
-   De magazijnverplaatsing in het magazijn vastleggen en tegelijkertijd de inkoopontvangst voor de broninkooporder boeken.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Rollen  
In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:  

-   Magazijnbeheerder  
-   Inkoper  
-   Magazijnmedewerker  

## <a name="prerequisites"></a>Vereisten  
U moet het volgende doen om deze procedure uit te voeren:  

-   CRONUS International Ltd. geïnstalleerd.  
-   Maak van uzelf een magazijnwerknemer bij vestiging ZILVER door de volgende stappen uit te voeren:  

    1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnmedewerkers** in en kies vervolgens de gerelateerde koppeling.  
    2.  Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Gebruikers**.  
    3.  Voer ZILVER in het veld **Vestiging** in.  
    4.  Selecteer het veld **Standaard**.  

## <a name="story"></a>Scenario  
Ellen, de magazijnmanager bij CRONUS International Ltd., maakt een inkooporder voor 10 eenheden van artikel LS-75 en 30 eenheden van artikel LS-81 van leverancier 10000 om te worden afgeleverd bij magazijn ZILVER. Wanneer de bezorging in het magazijn aankomt, zet de magazijnmedewerker Johanna de artikelen in de standaardopslaglocaties die voor de artikelen zijn gedefinieerd. Wanneer Johanna de voorraadopslag boekt, worden de artikelen als ontvangen en beschikbaar voor verkoop of andere oproepen in de voorraad.  

## <a name="setting-up-the-location"></a>De locatie instellen  
 De instellingen van de pagina **Vestiging** definiëren de magazijnstromen van het bedrijf.  

### <a name="to-set-up-the-location"></a>De vestiging instellen  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de vestigingskaart ZILVER.  
3.  Selecteer het selectievakje **Opslag vereist**.  

    Ga door met het instellen van een standaardopslaglocatie voor de twee artikelnummers om te bepalen waar deze worden opgeslagen.  

4.  Kies de actie **Opslaglocaties**.  
5.  Selecteer de eerste rij voor opslaglocatie S-01-0001 en kies vervolgens de actie **Inhoud**.  

    U ziet op de pagina **Opslaglocatie-inhoud** dat artikel LS-75 al is ingesteld als inhoud in opslaglocatie S-01-0001.  

6.  Kies de actie **Nieuw**.  
7.  Selecteer de velden **Vast** en **Standaard**.  
8.  Voer in het veld **Artikelnr.** de waarde LS-81 in.  

## <a name="creating-the-purchase-order"></a>De inkooporder maken  
Inkooporders zijn de meest gebruikte soort inkomend brondocument.  

### <a name="to-create-the-purchase-order"></a>De inkooporder maken  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
2.  Kies de actie **Nieuw**.  
3.  Maak een inkooporder voor leverancier 10000 op 23 januari (werkdatum) met de volgende inkooporderregels.  

    |Artikel|Vestiging|Opslaglocatie|Aantal|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|ZILVER|S-01-0001|10|  
    |LS-81|ZILVER|S-01-0001|30|  

    > [!NOTE]  
    >  De opslaglocatiecode wordt automatisch ingevoerd op basis van de instellingen die u in de sectie 'De locatie instellen' heeft uitgevoerd.  

    Ga door om het magazijn te informeren dat de inkooporder klaar is voor de magazijnverwerking wanneer de bezorging aankomt.  

4.  Kies de actie **Vrijgeven**.  

    Het leveren van luidsprekers van leverancier 10000 is aangekomen op magazijn SILVER en Jan bergt ze op.  

## <a name="receiving-and-putting-the-items-away"></a>De artikelen ontvangen en opslaan  
Op de pagina **Voorraadopslag** kunt u alle inkomende magazijnactiviteiten voor een bepaald brondocument beheren, zoals een inkooporder.  

### <a name="to-receive-and-put-the-items-away"></a>De artikelen ontvangen en opslaan  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadopslag** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Selecteer het veld **Brondocument** en selecteer vervolgens **Inkooporder**.  
4.  Selecteer het veld **Bronnr.**, selecteer de regel voor de inkoop van leverancier 10000, en kies vervolgens de knop **OK**.  

    U kunt ook de actie **Brondocument ophalen** kiezen en de inkooporder kiezen.  

5.  Kies de actie **Te verwerken aantal autom. invullen**.  

    Of voer in het veld **Te verwerken aantal** respectievelijk 10 en 30 in op de twee voorraadopslagregels.  

6.  Kies de actie **Boeken**, selecteer de actie **Ontvangen** en kies vervolgens de knop **OK**.  

    Nu zijn de 40 luidsprekers geregistreerd als opgeslagen in opslaglocatie S-01-0001 en een positieve artikelpost is gemaakt om de geboekte inkoopontvangst te weerspiegelen.  

## <a name="see-also"></a>Zie ook  
 [Artikelen opslaan met voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Standaardmagazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md)   
 [Artikelen ad hoc verplaatsen in standaardmagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Ontwerpdetails: Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md)   
 [Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]