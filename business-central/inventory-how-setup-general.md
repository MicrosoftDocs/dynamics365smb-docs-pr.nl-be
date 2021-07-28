---
title: Algemene voorraadinstellingen definiëren
description: Beschrijft hoe u de algemene voorraadinstellingen definieert, zodat u uw magazijn en voorraad kunt beheren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a99de8575891e15712e221f28bbf3f4a46f2f771
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435634"
---
# <a name="set-up-general-inventory-information"></a>Algemene voorraadgegevens instellen

U geeft uw algemene voorraadinstellingen op de pagina **Voorraadinstelling** op.

## <a name="to-set-up-general-inventory-information"></a>Algemene voorraadgegevens instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul op de pagina **Voorraadinstelling** de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voor gedetailleerde informatie over de kostprijsvelden **Autom. voorraadwaarde boeken**, **Verw. kostprijs naar GB boeken** en **Standaardwaarderingsmethode** raadpleegt u [Voorraadkosten afstemmen op grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md) en [Ontwerpdetails: Verwachte kostenboeking](design-details-expected-cost-posting.md). Zie voor meer informatie over kostprijsberekening in het algemeen [Voorraadkosten beheren](finance-manage-inventory-costs.md).  

Als u een inslagtijd wilt instellen voor de berekening van de ordertoezegging op de inkoopregel, kunt u deze instellen als standaardwaarde voor de voorraad, op de pagina **Voorraadinstellingen**, en de vestiging. Zie voor meer informatie [Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> De schakelaar **Automatische kostenaanpassing** is standaard ingeschakeld om ervoor te zorgen dat voorraadwaarden altijd correct zijn in het grootboek, waardoor uw verkoop- en winststatistieken up-to-date blijven. Kostenwijzigingen vanuit inkomende posten, zoals voor inkopen of productie-output, worden toegewezen aan de bijbehorende uitgaande posten, zoals verkopen of transfers. Dit is handig voor nieuwe [!INCLUDE[prod_short](includes/prod_short.md)]-klanten en kleine bedrijven met relatief lage voorraadtransactieniveaus. Als een bedrijf echter groeit en de voorraadniveaus toenemen, kan dit de systeemprestaties vertragen. Om verminderde prestaties tijdens het boeken te minimaliseren, selecteert u een tijdoptie om te definiëren hoe ver terug in de tijd vanaf de werkdatum een inkomende transactie kan plaatsvinden om mogelijk een aanpassing van gerelateerde uitgaande waardeposten te activeren. Als alternatief kunt u de kosten met regelmatige tussenpozen handmatig aanpassen met de batchverwerking Kostprijs herwaarderen - Artikelposten.

## <a name="see-also"></a>Zie ook
[Voorraad instellen](inventory-setup-inventory.md)  
[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)    
[Voorraad beheren](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]