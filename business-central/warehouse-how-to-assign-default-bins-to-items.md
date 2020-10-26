---
title: Standaardopslaglocaties aan artikelen toewijzen | Microsoft Docs
description: Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken. Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8c8cca84e7ace9eb25f3e1366a5beefa954edbc4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911908"
---
# <a name="assign-default-bins-to-items"></a>Standaardopslaglocaties aan artikelen toewijzen
Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken. Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld. Standaardopslaglocaties worden gedefinieerd op de pagina **Opslaglocatie-inhoud** .  

## <a name="to-assign-a-default-bin-to-an-item"></a>Een standaardopslaglocatie toewijzen aan een artikel
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorstel opslaglocatie-inhoudaanmaak** in en kies vervolgens de desbetreffende koppeling.  
2.  Vul de opslaglocatiecode en het artikel in voor elke opslaglocatie die u wilt instellen als standaardwaarde voor een artikel. Selecteer het veld **Standaard** .  
3.  Kies de actie **Opslaglocatie-inhoud maken** . Er worden nu standaardopslaglocaties voor uw artikel toegewezen.  

> [!NOTE]  
>  Wanneer een artikel wordt opgeslagen terwijl er voor het artikel geen standaardopslaglocatie is toegewezen, wordt de locatie waar het artikel wordt opgeslagen toegewezen als de standaardopslaglocatie.  

## <a name="to-change-the-default-bin-for-an-item"></a>De standaardopslaglocatie voor een artikel wijzigen  
Soms moet u de standaardtoewijzing van de opslaglocatie voor een bepaald artikel wijzigen of een standaardopslaglocatie toewijzen aan een nieuw artikel.    
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslaglocatie-inhoud** in en kies de gerelateerde koppeling.  
2.  Selecteer de juiste vestiging in het veld **Vestigingsfilter** .  
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
