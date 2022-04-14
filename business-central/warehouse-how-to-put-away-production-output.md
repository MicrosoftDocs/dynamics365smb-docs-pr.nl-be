---
title: Productieoutput opslaan
description: Hoe u de productieoutput opslaat, is afhankelijk van de vestigingsinstellingen van het magazijn. Voorraadopslag kan op de volgende manieren worden uitgevoerd.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 4b6f6a19787f1fd2630cf3bc3a6882dc17f0d6bb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514321"
---
# <a name="put-away-production-or-assembly-output"></a>Productie- of assemblageoutput opslaan

Hoe u de productieoutput opslaat, is afhankelijk van de vestigingsinstellingen van het magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

In standaardmagazijnconfiguraties waar voor uw vestiging opslagverwerking vereist is, gebruikt u het document **Voorraadopslag** om productieoutput te boeken en de opslag van output vast te leggen.  

> [!NOTE]  
> Voorraadopslag wordt niet ondersteund voor assemblageprocessen. U boekt een assemblageorder om output te registreren. Als u opslaglocaties gebruikt, kunt u artikelen later tussen opslaglocaties verplaatsen. Zie [Artikelen ad hoc verplaatsen in standaardmagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) voor meer informatie.  

In geavanceerde magazijnconfiguraties waar voor de vestiging zowel opslag- als ontvangstverwerking vereist is, kunt u een interne-opslagdocument of een verplaatsingsdocument maken om de output op te slaan.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Productieoutput opslaan met een voorraadopslag

De eerste stap bij het opslaan van output is het maken van het inkomende magazijnverzoek. Deze aanvraag informeert het magazijn dat de output van de productie- of assemblageorder gereed is voor opslag.

### <a name="to-create-the-inbound-warehouse-request"></a>Ink.magazijnontvangst maken  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vrijgegeven productieorder** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies in de productieorder die gereed is voor opslag de actie **Ink. magazijnontvangst maken**.  

> [!NOTE]  
> U kunt de inkomende magazijnaanvraag ook maken door het veld **Inkomend verzoek maken** te kiezen bij het vernieuwen van de productieorder. Zie [Productieorders opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md) voor meer informatie.  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Output opslaan met een voorraadopslag  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadopslag** in en kies vervolgens de gerelateerde koppeling.  
2.  Een nieuwe voorraadopslag maken. Zie voor meer informatie [Artikelen opslaan met een voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Kies de actie **Brondocumenten ophalen** en selecteer de vrijgegeven productieorder om de productieorderoutput te openen.  
4.  Vul de opslagregels in.
5.  Wanneer de regels gereed zijn voor boeken, kiest u de actie **Boeken**. Het boeken leidt tot het maken van de benodigde magazijnposten en tot het boeken van de output van de artikelen.  

Het is ook mogelijk om rechtstreeks vanuit een vrijgegeven productieorder een **Voorraadopslag** te maken. Zie voor meer informatie [Artikelen opslaan met een voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Wanneer u een voorraadopslag boekt, wordt ervan uitgegaan dat alle bewerkingen worden geboekt overeenkomstig het standaardbewerkingsplan, dus dat de outputhoeveelheid wordt geboekt overeenkomstig de laatste bewerking. U kunt het outputdagboek gebruiken om verschillen in de outputhoeveelheid en de instel- en bewerkingstijd te boeken. Als u een gedeeltelijke boeking moet uitvoeren nadat u de voorraadopslag hebt gemaakt, kunt u dit doen voor insteltijden en hoeveelheden voor alle bewerkingen, behalve de laatste. In dat geval wordt de laatste bewerking bestuurd door de voorraadopslag.  

Als u alleen instel- of bewerkingstijd hoeft te boeken voor de laatste bewerking, stelt u de outputhoeveelheid voor de laatste bewerking in op 0. Eventueel kunt u ervoor kiezen om de laatste regel helemaal niet te boeken door deze te verwijderen.  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Assemblage en productieoutput opslaan in geavanceerde magazijnconfiguraties
Wanneer u de output van een productie- of assemblageorder boekt in het magazijn dat is ingesteld om gestuurde opslag en pick te gebruiken, wordt de output in de opslaglocatie geplaatst die is gedefinieerd in de productie- of assemblageorder. 

De volgende tabel beschrijft verschillende manieren om artikelen binnen het magazijn te verplaatsen met geavanceerde configuraties waarbij alle magazijnactiviteiten in een gerichte werkstroom moeten worden uitgevoerd. 

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Artikelen met het magazijnverplaatsingswerkblad verplaatsen.|[Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Maak een interne opslag om geassembleerde artikelen op te slaan in een geavanceerde magazijnconfiguratie.|[Een interne opslag maken](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> In geen van beide procedures kan het brondocumentnummer, zoals Productieordernr. worden ingevoerd in de documenten interne opslag, opslag of verplaatsing.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
