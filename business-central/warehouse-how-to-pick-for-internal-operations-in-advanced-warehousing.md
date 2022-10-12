---
title: Picken voor interne bewerkingen in geavanceerde magazijnconfiguraties
description: Als uw locaties picking en verzending gebruiken, pickt u componenten voor assemblage- en taakactiviteiten op de pagina Magazijnpick.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607567"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Picken voor productie, assemblage of taken in geavanceerde magazijnconfiguraties

In geavanceerde magazijnconfiguraties waarbij de locatie is ingesteld voor het gebruik van picken en verzending, kunt u componenten voor productie- en assemblageactiviteiten kiezen op de pagina **Magazijnpick**.  

U kunt tevens de pagina **Verplaatsingsvoorstel** gebruiken voor spontane verplaatsing van artikelen tussen opslaglocaties, dat wil zeggen, zonder verwijzing naar een brondocument. Zie [Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md) voor meer informatie.  

Zie [Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) voor informatie over het picken van artikelen in standaardmagazijnvestigingen die alleen zijn ingesteld voor picken.  

> [!NOTE]
> U kunt een magazijn-pickdocument niet van het begin af maken, omdat een pick-activiteit altijd onderdeel is van een werkstroom, zowel bij een pull- als bij een push-scenario.  

Bij een push-scenario kan een magazijn-pickdocument gemaakt worden door **Mag. Pick maken** in het brondocument te selecteren, zoals een vrijgegeven assemblageorder of een verzending uit het magazijn. Zie voor meer informatie [Artikelen picken met een magazijnpick](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

U kunt ook een magazijnpickdocument op een pull-manier maken met behulp van de pagina **Pickvoorstel** om pickverzoeken te detecteren. Deze methode is handig voor verzending en interne operaties. Vervolgens kunt u de benodigde magazijnpickdocumenten maken.  

De volgende procedure beschrijft een pull-scenario, waarbij u onderdelen voor een vrijgegeven productieorder pickt met behulp van de pagina **Werkblad Pick**. De procedure geldt ook voor een assemblageorder.  

Als u een pick-verzoek wilt maken, bij zowel een pull- als een push-scenario, moeten de betreffende brondocumenten vrijgegeven worden. Voor interne doeleinden kunnen brondocumenten op de volgende manieren vrijgegeven worden.  

|Brondocument|Vrijgavemethode|  
|---------------------|--------------------|  
|Productieorder|Wijzig de ordersoort in vrijgegeven productieorder.|  
|Assemblageorder|Status wijzigen in Vrijgegeven.|
|Projecten | Status wijzigen in Open.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Onderdelen picken op basis van het pickvoorstel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pickvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Magazijndocumenten ophalen** en selecteer vervolgens de onderdeelregels van de vrijgegeven productieorder.  
3. Sorteer de regels om efficiënt te picken. Misschien wilt u regels combineren om werknemers tijd te besparen.  
4. Kies de actie **Pick maken**.  
5. Bepaal hoe de magazijn-pickdocumenten gemaakt moeten worden en hoe de pickregels gesorteerd moeten worden door de velden op de pagina **Pick maken** in te vullen.  
6. Kies de knop **OK**. Magazijn-pickdocumenten worden gemaakt met een pickregel voor ieder onderdeel dat voor de interne activiteit benodigd is.  

Bedrijfsruimten zoals productiewerkplaatsen hebben mogelijk een standaardbak voor de componenten die ze nodig hebben. Als dit het geval is, wordt de standaardmagazijncode toegevoegd aan het magazijnpickdocument om aan te geven waar de artikelen moeten worden geplaatst. Zie voor meer informatie de knopinfo voor het veld **Code verbruikslocatie** of **Opslaglocatie Naar-assemblage**.

## <a name="filling-the-consumption-bin"></a>De verbruiksopslaglocatie vullen

In dit stroomdiagram wordt weergegeven hoe het veld **Opslaglocatie** op de productieordercomponentregels wordt ingevuld op basis van uw vestigingsinstellingen.

![Stroomdiagram Opslaglocatie.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Zie ook

[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
