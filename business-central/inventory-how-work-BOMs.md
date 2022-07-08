---
title: Werken met stuklijsten om onderdelen te beheren
description: U maakt een assemblagestuklijst om de onderdelen of resources op te geven die vereist zijn om het artikel samen te stellen dat de assemblagestuklijst vertegenwoordigt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.forms: 36, 5872, 5870, 5874, 911, 917, 912
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d538ea3e1bb00772a3a3183c09c2220893380058
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079570"
---
# <a name="work-with-bills-of-material"></a>Werken met stuklijsten

U gebruikt stuklijsten om bovenliggende artikelen te structureren die door resources of bewerkingsplaatsen moeten worden geassembleerd of geproduceerd van onderdelen. Er kan ook een assemblagestuklijst worden gebruikt om een hoofdartikel als pakketten bestaande uit de onderdelen te verkopen.

## <a name="assembly-boms-or-production-boms"></a>Assemblagestuklijsten of productiestuklijsten

U gebruikt assemblageorders voor het maken van eindartikelen van onderdelen in een eenvoudig proces dat kan worden uitgevoerd door een of meer standaardbronnen die geen bewerkingsplaatsen of -afdelingen betreffen of waarbij geen bronnen gebruikt worden. Een assemblageproces kan bijvoorbeeld zijn het picken van twee flessen wijn en één pak koffie en deze als een cadeau-item verpakken.  

Een assemblagestuklijst betreft de hoofdgegevens die bepalen welke onderdelen gebruikt worden in een samengesteld eindartikel en welke bronnen gebruikt worden voor het samenstellen van het assemblageartikel. Wanneer u een assemblageartikel en een aantal in een nieuwe assemblageorderkop invoert, worden de assemblageorderregels automatisch op basis van de assemblagestuklijst gevuld met één assemblageorderregel per onderdeel of bron. Zie voor meer informatie [Assemblagebeheer](assembly-assemble-items.md).

Assemblagestuklijsten worden in dit onderwerp beschreven.

U gebruikt productieorders voor het maken van eindartikelen van onderdelen in een complex proces, waarvoor een productiebewerkingsplan en bewerkingsplaatsen of -afdelingen nodig zijn die productiecapaciteit vertegenwoordigen. Een productieproces kan bijvoorbeeld zijn het knippen van stalen platen in één bewerking, deze lassen in een volgende bewerking en het eindartikel verfen in de laatste bewerking. Zie [Productie](production-manage-manufacturing.md) voor meer informatie.  

Een productiestuklijst is de stamgegevens die een productieartikel en de componenten erin definieert. voor componenten moet de productiestuklijst worden gecertificeerd en toegewezen aan het productieartikel voordat het in een productieorder kan worden gebruikt. Wanneer u het productieartikel op een productieorderregel handmatig of door het vernieuwen van de order invoert, wordt de inhoud van de productiestuklijst omgezet in de onderdelen van de productieorder . Zie voor meer informatie [Productiestuklijsten maken](production-how-to-create-production-boms.md).  

Het concept van bronnen in de productie is veel geavanceerder dan in de assemblage. Werkplaatsen en machinecentra fungeren als bronnen en productiestappen worden vertegenwoordigd door bewerkingen die zijn toegewezen aan bronnen in productiebewerkingsplannen. Zie voor meer informatie [Bewerkingsplannen maken](production-how-to-create-routings.md).

Zowel assemblage- als productieorders kunnen rechtstreeks aan verkooporders worden gekoppeld. U kunt echter alleen assemblageorders gebruiken om het eindartikel rechtstreeks voor een klantverzoek aan de verkooporder te koppelen.

## <a name="to-create-an-assembly-bom"></a>Een assemblagestuklijst maken

Als u een bovenliggend artikel wilt definiëren dat bestaat uit andere artikelen, en mogelijk uit resources die nodig zijn om het bovenliggende artikel samen te stellen, moet u een assemblagestuklijst maken.  

Assemblagestuklijsten bevatten gewoonlijk artikelen, maar kunnen ook een of meer resources bevatten die het assemblageartikel samenstellen.

Assemblagestuklijsten kunnen meerdere niveaus bevatten, wat betekent dat een onderdeel op de assemblagestuklijst zelf ook een assemblageartikel kan zijn. In dat geval bevat het veld **Assemblagestuklijst** op de assemblagestuklijstregel **Ja**.

Er gelden speciale vereisten voor artikelen op assemblagestuklijsten met betrekking tot beschikbaarheid. Zie voor meer informatie [De beschikbaarheid van een artikel bekijken op basis van het gebruik ervan in assemblagestuklijsten](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Het maken van een assemblagestuklijst bestaat uit twee delen:
- Een nieuw artikel instellen
- De stuklijststructuur van het assemblageartikel definiëren.

1. Stel een nieuw artikel in. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

    Ga verder om onderdelen of resources in de assemblagestuklijst in te voeren.  
2. Kies op de pagina **Artikel** voor een assemblageartikel de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.
3. Vul indien nodig de velden op de pagina **Assemblagestuklijst** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-edit-assembly-boms"></a>Assemblagestuklijsten bewerken

U kunt de regels op een assemblagestuklijst op elk gewenst moment bewerken. Maar houd er rekening mee dat de stuklijst in gebruik kan zijn bij lopende verkopen of assemblages van het hoofdartikel, dat door de wijziging kan worden beïnvloed. Kies de actie **Waar gebruikt** om te zien in welke artikelen het wordt gebruikt en vervolgens of verkoop- of assemblageorders kunnen worden beïnvloed.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de waarde **Ja** in de kolom **Assemblagestuklijst**.
3. Kies op de pagina **Assemblagestuklijst** de actie **Lijst bewerken** en wijzig vervolgens een willekeurig veld.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Onderdelen en resources ingesprongen volgens de stuklijststructuur weergeven

Vanuit de pagina **Assemblagestuklijst** kunt u een afzonderlijke pagina openen die de onderdelen en resources bevat die zijn ingesprongen op basis van hun stuklijstpositie onder het assemblageartikel.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een assemblageartikel. (Het veld **Assemblagestuklijst** op de pagina **Artikelen** bevat **Ja**.)
3. Kies op de pagina **Artikel** de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.
4. Kies op de pagina **Assemblagestuklijst** de actie **Stuklijst weergeven**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Het assemblageartikel in documentregels vervangen door de samenstellende onderdelen

Vanuit ieder in- of verkoopdocument dat een assemblageartikel bevat, kunt u de regel voor dit artikel door middel van een speciale functie vervangen door nieuwe regels voor de samenstellende onderdelen ervan. Deze functie bijvoorbeeld nuttig als u de onderdelen wilt verkopen als een kit die samen het assemblageartikel vertegenwoordigen.

De actie **Stuklijst weergeven** is ook beschikbaar op de pagina **Assemblagestuklijst** als een methode om subassemblageartikelen in een assemblagestuklijst te bekijken.

> [!CAUTION]  
>  Wanneer u de functie **Stuklijst weergeven** hebt gebruikt, kunt u dit niet gemakkelijk ongedaan maken. U moet dan de verkooporderregels die de onderdelen vertegenwoordigen verwijderen, en vervolgens opnieuw een verkooporderregel voor het assemblageartikel invoeren.

De volgende procedure is gebaseerd op een verkoopfactuur. Dezelfde stappen zijn van toepassing op andere verkoopdocumenten en op alle inkoopdocumenten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Open een verkoopfactuur die een regel voor een assemblageartikel bevat.
3. Selecteer de regel een assemblageartikel en klik vervolgens op de regelactie **Stuklijst weergeven**.

Alle velden op de verkoopfactuurregel voor het assemblageartikel worden worden gewist, behalve de velden **Artikel** en **Beschrijving**. Volledige verkoopfactuurregels worden ingevoegd voor de onderdelen en mogelijke resources, waaruit het assemblageartikel is opgebouwd.

> [!NOTE]
> Het rapport **Picklijst per order** wordt ook gewijzigd om alleen de componenten weer te geven. Dit betekent dat een magazijnmedewerker die het bovenliggende artikel, het assemblageartikel, pickt, het niet zal zien in de picklijst. Zie voor meer informatie [De picklijst afdrukken](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>De vaste verrekenprijs van een assemblageartikel berekenen

U berekent de kostprijs van een assemblageartikel door de kostprijs van elk onderdeel en elke resource in de assemblagestuklijst bij elkaar op te tellen.

U kunt de vaste verrekenprijs voor een of meerdere artikelen ook berekenen en bijwerken op de pagina **Vaste-verrekenprijsvoorstel**. Zie [Vaste verrekenprijzen aanpassen](finance-how-to-update-standard-costs.md) voor meer informatie.  

De kostprijs van een assemblagestuklijst is altijd gelijk aan het totaal van de kostprijzen van de verschillende componenten, inclusief overige assemblagestuklijsten, en eventuele resources.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.
2. Open de kaart voor een assemblageartikel. (Het veld **Assemblagestuklijst** op de pagina **Artikelen** bevat **Ja**.)
3. Kies op de pagina **Artikel** de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.
4. Kies op de pagina **Assemblagestuklijst** de actie **Vaste verrekenprijs berekenen**.
5. Selecteer een van de volgende opties en kies de knop **OK**.

|Optie |Description |
|-------|------------|
|**Hoogste niveau**|Berekent de vaste verrekenprijs van het assemblageartikel als de totale kosten van alle gekochte of geassembleerde artikelen op die assemblagestuklijst, ongeacht eventuele onderliggende assemblagestuklijsten.|
|**Alle niveaus**|Berekent de vaste verrekenprijs voor het assemblageartikel als de som van: 1) De berekende kosten van alle onderliggende assemblagestuklijsten op de assemblagestuklijst. 2) De kosten van alle ingekochte artikelen op de assemblagestuklijst.|



De kosten van de artikelen waaruit de assemblagestuklijst bestaat, worden gekopieerd van artikelkaarten van de componenten. De kosten van elk artikel worden vermenigvuldigd met het aantal, en de totale kostprijs wordt weergegeven in het venster **Kostprijs** op de artikelkaart.

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/modules/set-up-assembly-items-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]