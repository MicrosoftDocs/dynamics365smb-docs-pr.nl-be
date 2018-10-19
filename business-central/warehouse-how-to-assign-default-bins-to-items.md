---
title: Standaardopslaglocaties aan artikelen toewijzen | Microsoft Docs
description: Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken. Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e6c6c8a54ae638fa90bca94e43a38d120b5fd3f6
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="assign-default-bins-to-items"></a>Standaardopslaglocaties aan artikelen toewijzen
Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken. Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld. Standaardopslaglocaties worden gedefinieerd in het venster **Opslaglocatie-inhoud**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Een standaardopslaglocatie toewijzen aan een artikel
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorstel opslaglocatie-inhoudaanmaak** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul de opslaglocatiecode en het artikel in voor elke opslaglocatie die u wilt instellen als standaardwaarde voor een artikel. Selecteer het veld **Standaard**.  
3.  Kies de actie **Opslaglocatie-inhoud maken**. Er worden nu standaardopslaglocaties voor uw artikel toegewezen.  

> [!NOTE]  
>  Wanneer een artikel wordt opgeslagen terwijl er voor het artikel geen standaardopslaglocatie is toegewezen, wordt de locatie waar het artikel wordt opgeslagen toegewezen als de standaardopslaglocatie.  

## <a name="to-change-the-default-bin-for-an-item"></a>De standaardopslaglocatie voor een artikel wijzigen  
Soms moet u de standaardtoewijzing van de opslaglocatie voor een bepaald artikel wijzigen of een standaardopslaglocatie toewijzen aan een nieuw artikel.    
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslaglocatie-inhoud** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de juiste vestiging in het veld **Vestigingsfilter**.  
3.  Zoek naar de huidige inhoudspost van de standaardopslaglocatie voor het artikel en schakel het selectievakje **Standaardopslaglocatie** uit.  
4.  Zoek naar de regel Opslaglocatie-inhoud van de opslaglocatie die u wilt instellen als de nieuwe standaardopslaglocatie. Schakel het selectievakje **Standaardopslaglocatie** in.  

> [!NOTE]  
>  Wanneer een artikel voor het eerst wordt opgeslagen terwijl er geen standaardopslaglocatie is toegewezen aan het artikel, wordt de locatie waar het artikel wordt opgeslagen ingesteld als de standaardopslaglocatie voor het artikel.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

