---
title: Picken en verzenden in standaardmagazijnconfiguraties | Microsoft Docs
description: In Business Central kunnen uitgaande processen voor picken en verzending op vier manieren worden uitgevoerd met verschillende functionaliteiten afhankelijk van het complexiteitsniveau van het magazijn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3815e0e928041ca9fcef09b1c7410e45ebb57a1
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035768"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Procedure: picken en verzenden in standaardmagazijnconfiguraties

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

In [!INCLUDE[prod_short](includes/prod_short.md)] kunnen uitgaande processen voor picken en verzending op vier manieren worden uitgevoerd met verschillende functionaliteiten afhankelijk van het complexiteitsniveau van het magazijn.  

|Methode|Inkomend proces|Opslaglocaties|Magazijnpicks|Verzendingen|Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Picken en verzending van de orderregel boeken|X|||2|  
|B|Picken en verzending van een voorraadpickdocument boeken||X||3|  
|L|Picken en verzending van een magazijnverzendingdocument boeken|||X|5-4-6|  
|D|Picken van een magazijnpickdocument en verzending van een magazijnverzendingdocument boeken||X|X|5-4-6|  

Zie voor meer informatie [Ontwerpdetails: Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md).  

De volgende procedure geeft methode B in de vorige tabel weer.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="about-this-walkthrough"></a>Informatie over deze procedure

In standaardmagazijnconfiguraties waarbij voor uw vestiging wel een pickverwerking vereist is, maar geen verzendingsverwerking, gebruikt u de pagina **Voorraadpick** om pick- en verzendingsinformatie voor de uitgaande brondocumenten te verzamelen en boeken. Het uitgaand brondocument kan een verkooporder zijn, maar ook een inkoopretourorder, een uitgaande transferorder of een productieorder met daarop de materiaalbehoefte.  

In deze procedure worden de volgende taken gedemonstreerd:  

- Locatie ZILVER instellen voor voorraadpicks.  
- Maak een verkooporder voor klant 10000 voor 30 luidsprekers.  
- De verkooporder vrijgeven voor magazijnverwerking.  
- Een voorraadpick maken op basis van een vrijgegeven brondocument.  
- De magazijnverplaatsing van het magazijn vastleggen en tegelijkertijd de verkoopverzending voor de bronverkooporder boeken.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Rollen

In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:  

- Magazijnbeheerder  
- Orderverwerker  
- Magazijnmedewerker  

## <a name="prerequisites"></a>Vereisten

U moet het volgende doen om deze procedure uit te voeren:  

- Voor [!INCLUDE[prod_short](includes/prod_short.md)] online, een bedrijf gebaseerd op de optie **Geavanceerde evaluatie - volledige voorbeeldgegevens** in een sandboxomgeving. Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS International Ltd. geïnstalleerd.  
- Maak van uzelf een magazijnwerknemer bij de vestiging ZILVER door de volgende stappen uit te voeren:  

  1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies de gerelateerde koppeling.  
  2. Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Gebruikers**.  
  3. Voer ZILVER in het veld **Vestiging** in.  
  4. Selecteer het veld **Standaard**.  

- Maak artikel LS-81 beschikbaar op locatie ZILVER door deze stappen te volgen:  

  1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboeken** in en kies de gerelateerde koppeling.  
  2. Open het standaarddagboek en maak twee artikeldagboekregels met de volgende informatie over de werkdatum (23 januari).  

        |Boekingssoort|Artikelnummer|Vestiging|Opslaglocatie|Aantal|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Pos. correctie|LS-81|ZILVER|S-01-0001|20|  
        |Pos. correctie|LS-81|ZILVER|S-01-0002|20|  

  3. Kies de actie **Boeken** en selecteer de knop **Ja**.  

## <a name="story"></a>Scenario

Ellen, de magazijnmanager bij CRONUS, stelt magazijn ZILVER in voor basispickverwerking waarbij magazijnmedewerkers uitgaande orders afzonderlijk verwerken. De orderverwerker Suzanne maakt een verkooporder voor 30 eenheden van het artikel LS-81 om aan klant 10000 vanuit het ZILVER Magazijn te worden verzonden. De magazijnmedewerker John zorgt ervoor dat de verzending wordt voorbereid en aan de klant geleverd. John beheert alle betrokken taken op de pagina **Voorraadpick**, dat automatisch wijst naar de opslaglocaties waar LS-81 is opgeslagen.  

## <a name="setting-up-the-location"></a>De locatie instellen

De instellingen van de pagina **Vestiging** definiëren de magazijnstromen van het bedrijf.  

### <a name="to-set-up-the-location"></a>De vestiging instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vestigingen** in en kies de desbetreffende koppeling.  
2. Open de vestigingskaart ZILVER.  
3. Schakel op het sneltabblad **Magazijn** het selectievakje **Pick vereist** in.  

## <a name="creating-the-sales-order"></a>De verkooporder maken

Verkooporders zijn de meest gebruikte soort uitgaand brondocument.  

### <a name="to-create-the-sales-order"></a>De verkooporder maken

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Maak een verkooporder voor klant 10000 op 23 januari (werkdatum) met de volgende verkooporderregel.  

    |Artikel|Vestiging|Aantal|  
    |----|-------------|--------|  
    |LS_81|ZILVER|30|  

     Ga door om het magazijn te informeren dat de verkooporder klaar is voor magazijnverwerking.  

4. Kies de actie **Vrijgeven**.  

    John gaat door met het picken en verzenden van de verkochte artikelen.  

## <a name="picking-and-shipping-items"></a>Artikelen picken en verzenden

Op de pagina **Voorraadpick** kunt u alle uitgaande magazijnactiviteiten voor een bepaald brondocument, zoals een verkooporder, beheren. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>U kunt als volgt artikels picken en verzenden

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadpicks** in en kies de desbetreffende koppeling.  
2. Kies de actie **Nieuw**.  

    Zorg ervoor dat het veld **Nee.** op het sneltabblad **Algemeen** is ingevuld.
3. Selecteer het veld **Brondocument** en selecteer vervolgens **Verkooporder**.  
4. Selecteer het veld **Bronnr.**, selecteer de regel voor de verkoop aan klant 10000, en kies vervolgens de knop **OK**.  

    U kunt ook de actie **Brondocument ophalen** kiezen en de verkooporder kiezen.  
5. Kies de actie **Te verwerken aantal autom. invullen**.  

    Of voer in het veld **Te verwerken aantal** respectievelijk 10 en 20 in op de twee voorraadpickregels.  
6. Kies de actie **Boeken**, selecteer **Verzenden** en kies de knop **OK**.  

    Nu zijn de 30 luidsprekers geregistreerd als gepickt uit de opslaglocaties S-01-0001 en S-01-0002, en een negatieve artikelpost is gemaakt om de geboekte verkoopverzending te weerspiegelen.  

## <a name="see-also"></a>Zie ook

[Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Standaardmagazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md)  
[Artikelen ad hoc verplaatsen in standaardmagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Ontwerpdetails: Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md)  
[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
