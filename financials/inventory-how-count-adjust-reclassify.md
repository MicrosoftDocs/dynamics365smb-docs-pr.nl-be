---
title: Voorraad tellen, corrigeren en herindelen| Microsoft Docs
description: Beschrijft hoe u inventarisaties uitvoert, negatieve of positieve correcties uitvoert, en gegevens wijzigt, zoals locatie of lotnummer, in artikelposten of magazijnposten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Procedure: Voorraad tellen, corrigeren en herindelen
Minstens eenmaal per jaar moet u inventariseren, dat wil zeggen, alle artikelen tellen die op voorraad zijn, om te controleren of de geregistreerde hoeveelheid in de database gelijk is aan de werkelijke hoeveelheid in de magazijnen. Wanneer de werkelijke hoeveelheid niet bekend is, moet dit in het grootboek worden geboekt in het kader van een voorraadwaardering aan het einde van een boekingsperiode.

Hoewel alle artikelen in het magazijn minimaal een keer per jaar worden geteld, wilt u sommige artikelen misschien vaker tellen omdat ze waardevoller zijn of snel worden omgezet en belangrijk zijn voor het bedrijf. U kunt tellingsperioden instellen en toewijzen aan magazijnartikelen. Voor dit doel kunt u speciale telperioden aan die artikelen toewijzen. Zie voor meer informatie de sectie 'Clustertellingen uitvoeren'.

Als u vastgelegde voorraadhoeveelheden moet aanpassen, in verband met de inventarisatie of om andere redenen, kunt u een artikeldagboek gebruiken om het voorraadgrootboek direct te wijzigen zonder zakelijke transacties te hoeven boeken. U kunt ook een correctie voor één artikel uitvoeren op de artikelkaart.

Als u kenmerken én hoeveelheden van posten in het artikelgrootboek én wilt wijzigen, kunt u daarvoor het artikelherindelingsdagboek gebruiken. Typische kenmerken voor herindeling zijn serie-/lotnummers, vervaldatums en dimensies.

## <a name="to-perform-a-physical-inventory"></a>Een inventarisatie uitvoeren
Aan het einde van het boekjaar, zo niet vaker, moet u de inventaris opmaken (de beschikbare artikelen tellen) om te controleren of het geregistreerde aantal gelijk is aan het aantal in voorraad. Als er verschillen zijn, moet u deze naar de artikelrekeningen boeken voordat u de voorraadwaardering uitvoert.

Afgezien van de fysieke tellingstaak omvat het volledige proces de volgende drie taken:

- De verwachte voorraad berekenen.
- Het rapport dat bij het tellen moet worden gebruikt afdrukken.
- Invoeren en boeken van de werkelijk getelde voorraad.

### <a name="to-calculate-the-expected-inventory"></a>De verwachte voorraad berekenen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inventarisatiedagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Voorraad berekenen**.
3. Specificeer in het venster **Voorraad berekenen** de voorwaarden die moeten worden gebruikt om de dagboekregels te maken, zoals of artikelen die niet op voorraad zijn al dan niet moeten worden opgenomen.
4. Stel alleen filters in als u de voorraad voor bepaalde artikelen, opslaglocaties, vestigingen of dimensies wilt berekenen.
5. Kies de knop **Ok**.

> [!NOTE]  
>   De artikelposten worden verwerkt volgens de informatie die u hebt opgegeven en de regels in het inventarisatiedagboek worden gemaakt. U ziet dat het veld **Aantal (inventaris)** automatisch wordt ingevuld met hetzelfde aantal als het veld **Aantal (Berekend)**. Met deze functie hoeft u de getelde voorraad niet handmatig in te voeren voor artikelen die overeenkomen met de berekende hoeveelheid. Als het aantal echter afwijkt van wat is ingevoerd in het veld **aantal (Berekend)**, moet u deze overschrijven met de hoeveelheid die daadwerkelijk is geteld.

### <a name="to-print-the-report-used-when-counting"></a>Het bij het tellen gebruikte rapport afdrukken
1. Klik in het venster **Inventarisatiedagboek** met de berekende verwachte voorraad op de actie **Afdrukken**.
2. Specificeer in het veld **Inventarisatielijst** of het rapport het berekende aantal moet tonen en of het rapport voorraadartikelen op serie-/lotnummers moet tonen.
3. Stel filters in als u het rapport alleen wilt afdrukken voor bepaalde artikelen, opslaglocaties, vestigingen of dimensies.
4. Klik op **Afdrukken**.

Medewerkers kunnen nu verder met het tellen van de voorraad en eventuele afwijkingen in het afgedrukte rapport vastleggen.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Invoeren en boeken van de werkelijk getelde voorraad
1. Voer op elke regel in het venster **Inventarisatiedagboek** waar de werkelijk beschikbare voorraad, zoals bepaald door de telling, afwijkt van de berekende hoeveelheid, de werkelijk beschikbare voorraad handmatig in het veld **Aantal (Inventarisatie)** in.

    De gerelateerde velden worden dienovereenkomstig bijgewerkt.

    > [!NOTE]  
>   Als de verschillen in de telling worden veroorzaakt door artikelen die met de verkeerde vestigingscode zijn geboekt, moet u de verschillen niet invoeren in het inventarisatiedagboek. Gebruik in plaats daarvan het herindelingsdagboek of een transferorder om items om te leiden naar de juiste vestigingen. Zie Art.-herindelingsdagboek of 'Procedure: Transferorders maken' voor meer informatie.

2. Als de berekende aantallen wilt aanpassen aan de feitelijk getelde aantallen, kiest u de actie **Boeken**.

    Zowel de artikelposten als de inventarisatieposten worden gemaakt. Open de artikelkaart om de resulterende inventarisatieposten te bekijken.

3. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
4. Als u de inventarisatie wilt controleren, opent u de betreffende artikelkaart en kiest u de actie **Inventarisatieposten**.

# <a name="to-perform-cycle-counting"></a>Clustertelling uitvoeren
Hoewel alle artikelen in het magazijn minimaal een keer per jaar worden geteld, wilt u sommige artikelen misschien vaker tellen omdat ze waardevoller zijn of snel worden omgezet en belangrijk zijn voor het bedrijf. U kunt tellingsperioden instellen en toewijzen aan magazijnartikelen. Voor dit doel kunt u speciale telperioden aan die artikelen toewijzen.

> [!NOTE]  
>   Als uw locatie is ingesteld voor gestuurde opslag en pick, gebruikt u eerst het venster **Mag. inventarisatiedagboek** en vervolgens gebruikt u de functie **Magazijnherwaardering berekenen** in het venster **Artikeldagboek**.

## <a name="to-set-up-counting-periods"></a>U kunt als volgt tellingsperioden instellen
Een inventarisatie wordt gewoonlijk periodiek uitgevoerd, bijvoorbeeld maandelijks, per kwartaal of jaarlijks. U kunt elke gewenste periode instellen.

U stelt de inventarisatieperioden in die u wilt gebruiken en wijst er vervolgens één toe aan elk artikel. Wanneer u een inventarisatie uitvoert en **Tellingsperiode berekenen** in het inventarisatiedagboek gebruikt, worden de regels voor de artikelen automatisch gemaakt.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Voorraadtellingsperioden** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Een tellingsperiode toewijzen aan een artikel  
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het artikel waaraan u een tellingsperiode wilt toewijzen.  
3. Selecteer in het veld **Voorraadtellingsperiode** de gewenste tellingsperiode.  
4. Kies de knop **Ja** om de code te wijzigen en de eerste tellingsperiode voor het artikel te berekenen. De volgende keer dat u een tellingsperiode in het magazijninventarisatiedagboek berekent, wordt het item als een regel in het venster **Inventarisatieartikelselectie** weergegeven. U kunt vervolgens beginnen met tellen van het item op een periodieke basis.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Een telling starten op basis van tellingsperioden
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inventarisatiedagboek** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Tellingsperiode berekenen**.

    Het venster **Inventarisatieartikelselectie** wordt geopend en bevat de artikelen waaraan tellingsperioden zijn toegewezen en die op basis daarvan moeten worden geteld.
3. Voer de inventarisatie uit. Zie voor meer informatie de sectie 'Een magazijninventarisatie uitvoeren'.

## <a name="to-adjust-the-inventory-of-one-item"></a>De voorraad van één artikel aanpassen
Nadat u een fysieke telling hebt uitgevoerd van een artikel in uw voorraadgebied, kunt u de functie **Voorraad wijzigen** gebruiken om het werkelijke voorraadaantal vast te leggen.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het artikel waarvoor u voorraad wilt aanpassen, en kies vervolgens de actie **Voorraad wijzigen**.
3. Voer in het veld **Nieuwe voorraad** het voorraadaantal in dat u voor het artikel wilt vastleggen.
4. Kies de knop **Ok**.

De voorraad van het artikel is nu aangepast. Het nieuwe aantal wordt weergegeven in het veld **Huidige voorraad** in het venster **Voorraad wijzigen** en in het veld **Voorraad** in het venster **Artikelkaart** .

U kunt ook de functie **Voorraad wijzigen** gebruiken als eenvoudige manier om gekochte artikelen op voorraad te plaatsen als u geen inkoopfacturen of orders gebruikt om uw inkopen te registreren. Zie voor meer informatie [Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Als u voorraad hebt aangepast, moet u deze bijwerken met de huidige, berekende waarde. Zie [Procedure: Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Het voorraadaantal van een of meer artikelen aanpassen
In het venster **Artikeldagboek** kunt u rechtstreeks artikeltransacties boeken om uw voorraad aan te passen in verband met inkopen, verkopen en positieve of negatieve mutaties, zonder documenten te gebruiken.

Als u het artikeldagboek vaak gebruikt om dezelfde of vergelijkbare dagboekregels te boeken, bijvoorbeeld met betrekking tot materiële consumptie, kunt u het venster **Standaardartikeldagboek** gebruiken om deze terugkerende taak gemakkelijker te maken. Zie de sectie 'Standaarddagboeken' in [Werken met dagboeken](ui-work-general-journals.md) voor meer informatie.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kies de actie **Boeken** om de voorraadherwaarderingen te maken.

> [!NOTE]  
>   Als u voorraad hebt aangepast, moet u deze bijwerken met de huidige, berekende waarde. Zie [Procedure: Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.

## <a name="to-reclassify-an-items-lot-number"></a>Het lotnummer van een artikel herindelen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelherindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul in het venster **Artikelherindelingsdagboeken** indien nodig de velden in.
3. Voer in het veld **Lotnr.** het huidige lotnummer van het artikel in.
4. Voer in het veld **Nieuw lotnr.** het nieuwe lotnummer van het artikel in.
5. Kies de actie **Boeken**.

## <a name="see-also"></a>Zie ook
[Voorraad](inventory-manage-inventory.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

