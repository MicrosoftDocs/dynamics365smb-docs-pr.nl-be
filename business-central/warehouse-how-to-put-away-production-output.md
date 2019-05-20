---
title: Productieoutput opslaan | Microsoft Docs
description: Hoe u de productieoutput opslaat, is afhankelijk van de vestigingsinstellingen van het magazijn.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d7f941c5f0467f65ec3f94f00cacdd9c8fda6dc6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248424"
---
# <a name="put-away-production-or-assembly-output"></a>Productie- of assemblageoutput opslaan
Hoe u de productieoutput opslaat, is afhankelijk van de vestigingsinstellingen van het magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

In standaardmagazijnconfiguraties waar voor uw vestiging opslagverwerking vereist is, maar ontvangstverwerking niet, gebruikt u het document **Voorraadopslag** om de opslag van productieoutput te beheren en vast te leggen.  

In geavanceerde magazijnconfiguraties waar voor de vestiging zowel opslag- als ontvangstverwerking vereist is, kunt u een interne-opslagdocument of een verplaatsingsdocument maken om de output op te slaan.  

De eerste stap bij het opslaan van output is het maken van het inkomende magazijnverzoek. Deze aanvraag informeert het magazijn dat de output van de productie- of assemblageorder gereed is voor opslag.

## <a name="to-create-the-inbound-warehouse-request"></a>Ink.magazijnontvangst maken  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vrijgegeven productieorder** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies in de productieorder die gereed is voor opslag de actie **Ink. magazijnontvangst maken**.  

> [!NOTE]  
>  U kunt de inkomende magazijnaanvraag ook maken door het selectievakje **Inkomend verzoek maken** in te schakelen bij het vernieuwen van de productieorder. Zie [Productieorders opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md) voor meer informatie.  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Output opslaan met een voorraadopslag  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadopslag** in en kies vervolgens de gerelateerde koppeling.  
2.  Een nieuwe voorraadopslag maken. Zie voor meer informatie [Artikelen opslaan met een voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Kies de actie **Brondocumenten ophalen** en selecteer de vrijgegeven productieorder om de productieorderoutput te openen.  
4.  Vul de opslagregels in.
5.  Wanneer de regels gereed zijn voor boeken, kiest u de actie **Boeken**. Het boeken leidt tot het maken van de benodigde magazijnposten en tot het boeken van de output van de artikelen.  

Het is ook mogelijk om rechtstreeks vanuit een vrijgegeven productieorder een **Voorraadopslag** te maken. Zie voor meer informatie [Artikelen opslaan met een voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Wanneer u een voorraadopslag boekt, wordt ervan uitgegaan dat alle bewerkingen worden geboekt overeenkomstig het standaardbewerkingsplan, dus dat de outputhoeveelheid wordt geboekt overeenkomstig de laatste bewerking. U kunt het outputdagboek gebruiken om verschillen in de outputhoeveelheid en de instel- en bewerkingstijd te boeken. Als u een gedeeltelijke boeking moet uitvoeren nadat u de voorraadopslag hebt gemaakt, kunt u dit doen voor insteltijden en hoeveelheden voor alle bewerkingen, behalve de laatste. In dat geval wordt de laatste bewerking bestuurd door de voorraadopslag.  

Als u alleen instel- of bewerkingstijd hoeft te boeken voor de laatste bewerking, stelt u de outputhoeveelheid voor de laatste bewerking in op 0. Eventueel kunt u ervoor kiezen om de laatste regel helemaal niet te boeken door deze te verwijderen.  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Output opslaan via interne magazijnopslag
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Interne mag.-opslag** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul de velden op de kop van een nieuwe interne opslag in. Vermeld in ieder geval de **vestiging**.  
4. Vul voor ieder artikel dat u naar het magazijn wilt verplaatsen een regel in. U hoeft alleen de velden **Artikelnr.** en **Aantal** in te vullen.  

    > [!NOTE]  
    >  Wanneer u het veld **Artikelnr.** selecteert, wordt het **opslaglocatie-inhoudsoverzicht** geopend in plaats van de **artikellijst**. Het artikel dat u wilt opslaan behoort namelijk tot de inhoud van een bepaalde opslaglocatie. Bovendien weet u al uit welke opslaglocatie het artikel moet worden gehaald.  

4.  Kies de actie **Opslaglocatie-inhoud ophalen** om de voorstelregels te vullen met de volledige of gefilterde inhoud van de opslaglocaties in de vestiging.  
5.  Kies de actie **Opslag maken**. De artikelen die u uit het productieproces wilt halen, worden nu opgenomen in opslaginstructies, zodat ze in het magazijn kunnen worden opgeslagen.  

> [!NOTE]  
>  Als voor uw magazijnvestiging gestuurde opslag en pick is ingesteld, wordt het magazijn via de standaardproductieopslaglocaties gekoppeld aan de productieafdeling: de inkomende en uitgaande productieopslaglocaties en de open shopflooropslaglocatie, die u definieert op het sneltabblad **Opslaglocaties** van de vestigingskaart. Wanneer u de output van een productieorder boekt, wordt de output in de **uitgaande productieopslaglocatie** geplaatst. Volg de bovenstaande procedure om de productieoutput op te slaan. Sla de output echter niet direct op in de standaardopslaglocatie van de artikelen, maar verplaats de artikelen van de **Uitgaande productieopslaglocatie** naar de standaardopslaglocatie.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Handmatig een opslaglocatie opgeven voor het opslaan van artikelen uit de productieoutput  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verplaatsingsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul de kop in en maak een regel voor elk artikel dat u naar het magazijn wilt verplaatsen.  
3.  Vul de velden **Van opslaglocatie** en **Naar opslaglocatie** in en geef het aantal artikelen op in het veld **Aantal**.  
4.  Kies de actie **Opslaglocatie-inhoud ophalen** om de voorstelregels te vullen met de volledige of gefilterde inhoud van de opslaglocaties in de vestiging.  
5. Kies de actie **Verplaatsing maken**. Er wordt een verplaatsingsinstructie voor het magazijn gemaakt met Nemen- en Plaatsen-regels die door de magazijnmedewerkers kunnen worden uitgevoerd.  

> [!NOTE]  
>  In geen van beide procedures kan het brondocumentnummer, zoals Productieordernr. worden ingevoerd in de documenten interne opslag, opslag of verplaatsing.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
