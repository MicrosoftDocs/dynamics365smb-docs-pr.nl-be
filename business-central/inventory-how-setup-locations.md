---
title: Een vestigingskaart instellen en transferroutes definiëren (bevat video)
description: 'Als u artikelen op meer dan één plaats koopt, opslaat of verkoopt, kunt u elke plaats als een locatie instellen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 03/25/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-locations"></a>Vestigingen instellen

Vestigingen zijn plaatsen zoals magazijnen waar u artikelen koopt, opslaat of verkoopt. [!INCLUDE [prod_short](includes/prod_short.md)] gebruikt vestigingen om de voorraad bij te houden in zowel eenvoudige als complexere magazijnprocessen.

U kunt vervolgens documentregels voor een bepaalde vestiging maken, beschikbaarheid per locatie weergeven en voorraad tussen locaties overbrengen. Ga voor meer informatie naar [Voorraad beheren](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Vestigingskaarten

U geeft informatie over een vestiging, zoals een magazijn of een distributiecentrum, op de pagina **Vestiging** op. U wijst aan elke vestiging een naam toe en een code die de vestiging vertegenwoordigt. U kunt de vestigingscode in andere delen van het programma invoeren om transacties voor een bepaalde vestiging vast te leggen.  

U kunt informatie invoeren over opslaglocaties en magazijnbeleid voor elke vestiging. Op basis van uw magazijnbeleid kunt u de opties op het sneltabblad **Opslaglocaties** gebruiken om de opslaglocaties op te geven die standaard voor transacties moeten worden gebruikt. Als u gestuurde opslag en pick gebruikt, kunt u met de opties op het sneltabblad **Opslaglocatiebeleid** definiëren hoe u geavanceerde magazijnfuncties wilt gebruiken.  

Sommige optievelden zijn afhankelijk van instellingen op de pagina **Vestiging** om niet-ondersteunde combinaties te beperken.  

Kies de actie **Zones** of **Opslaglocaties** voor informatie over zones en opslaglocaties die zijn gedefinieerd voor de vestiging.

### <a name="to-set-up-a-location"></a>Een vestiging instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op de pagina **Vestiging** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Herhaal stap 2 en 3 voor elke locatie waar u voorraad wilt houden.

> [!NOTE]  
> Veel velden op de pagina Vestigingskaart verwijzen naar de verwerking van artikelen in inkomende en uitgaande magazijnprocessen. Deze velden zijn niet relevant voor bedrijven die de meer complexe magazijnfunctionaliteit niet nodig hebben. Ga voor informatie naar [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

U kunt de configuratie van een locatie wijzigen zolang deze geen artikelposten heeft.  

Als u meerdere vestigingen heeft, kunt u vervolgens transferroutes tussen vestigingen definiëren. Ga voor meer informatie over overstaproutes naar [Een transferroute maken](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route"></a>Een transferroute maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferroutes** in en kies vervolgens de gerelateerde koppeling
2. Kies de actie **Nieuw**.
4. Vul indien nodig de velden op de pagina **Vestiging** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

U kunt nu voorraadartikelen tussen twee vestigingen overbrengen. Ga voor meer informatie over transfers naar [Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md).

## <a name="bins"></a>Opslaglocaties

Opslaglocaties vertegenwoordigen de basismagazijnstructuur en kunnen voorstellen voor het plaatsen van artikelen bevatten. Uw opslaglocaties kunnen inhoud hebben of vrije opslaglocaties zijn zonder specifieke inhoud.

Als u de opslaglocatiefunctionaliteit op een locatie wilt gebruiken, schakelt u op de pagina **Vestiging**, op het sneltabblad **Magazijn**, de schakeloptie **Opslaglocatie verplicht** in. U kunt de artikelstroom op de locatie ontwerpen door opslaglocatiecodes op te geven in de velden voor de magazijnprocessen op de sneltabbladen **Opslaglocaties** en **Opslaglocatiebeleid**.

> [!NOTE]
> Voordat u opslaglocatiecodes voor een vestiging kunt opgeven, moet u opslaglocatiecodes maken. Ga voor meer informatie over opslaglocaties naar [Opslaglocaties maken](warehouse-how-to-create-individual-bins.md) en [Opslaglocatiesoorten instellen](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zones

Als u uw opslaglocaties onder zones wilt structureren, kunt u dat doen op de pagina **Zones**. Wanneer u een zone toewijst aan opslaglocaties, kopieert [!INCLUDE [prod_short](includes/prod_short.md)] informatie van de zone naar de opslaglocaties. U kunt er ook voor kiezen om één zone in te stellen en alleen opslaglocaties te gebruiken om uw magazijn te organiseren. Ga voor informatie over zones naar [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Standaardafmetingen voor locaties

Dimensies zijn waarden die items categoriseren, zodat u ze kunt volgen en analyseren met behulp van verschillende rapportagetools. Dimensies kunnen bijvoorbeeld aangeven van welke afdeling of project een boeking afkomstig is. Het hebben van standaardafmetingen helpt mensen om fouten te voorkomen en de afmetingen handmatig op transactieniveau in te voeren als alle goederen afkomstig zijn van één locatie en afdeling.

U stelt standaardafmetingen in voor een locatie op de pagina **Locatiekaart** door **Dimensies** te kiezen. Daarna worden de standaardafmetingen van de locatie toegewezen aan de volgende documenten wanneer u de locatie op een regel kiest.

* Transferorders
* Inventarisatieorders
* Voorraadverzendingen
* Voorraadontvangsten
* Artikeldagboeken

Indien nodig kunt u de dimensie op de regel verwijderen of wijzigen. U kunt in het veld **Waardeboeking** vereisen dat mensen dimensies opgeven voor specifieke locaties voordat ze een post kunnen boeken. Als u wilt dat mensen alleen bepaalde dimensiewaarden kunnen kiezen, kunt u de waarden opgeven in het veld **Filter op toegestane waarden**. U kunt ook locatiedimensiewaarden opnemen op de pagina **Standaarddimensieprioriteiten** en voor combinaties van prioriteit- en dimensieregels op de pagina **Dimensiecombinaties**.

Omdat documenten voor transferorderopdrachten en herindelingsjournalen betrekking hebben op meer dan één locatie, is de volgorde waarin u gegevens invoert belangrijk. Standaardafmetingen worden gekopieerd uit het laatste locatieveld (de transitvestiging wordt genegeerd).

### <a name="example-of-default-dimensions-on-locations"></a>Voorbeeld van standaardafmetingen voor locaties

De volgende voorbeelden illustreren hoe de standaarddimensie wordt gebruikt.

U hebt de volgende dimensie-instellingen:

* Locatie OOST. Afdelingsdimensie is ADM
* Locatie WEST. Afdelingsdimensie is PROD

U geeft de locatie op een transferorder als volgt op:

1. Van locatie = OOST
2. Naar locatie = WEST

De PROD-dimensie wordt gekopieerd van locatie WEST.

U vult de velden als volgt in omgekeerde volgorde in:

1. Naar locatie = WEST
2. Van locatie = OOST

De ADM-dimensie wordt gekopieerd van locatie OOST.

## <a name="see-also"></a>Zie ook

[Voorraad beheren](inventory-manage-inventory.md)  
[Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)  
[Opslaglocaties maken](warehouse-how-to-create-individual-bins.md)  
[Opslaglocatiesoorten instellen](warehouse-how-to-set-up-bin-types.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
