---
title: Urenstaten en de goedkeuring ervan instellen| Microsoft Docs
description: U stelt urenstaten in om de tijd te traceren die in projecten en resources wordt gebruikt, wat u helpt bij projectbeheer, personeelsbezetting en capaciteit
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a5b2027649e2adddfd3e59b4376303059f575a99
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-time-sheets"></a>Urenstaten instellen
Urenstaten in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwerken tijdsregistraties in wekelijkse termijnen van zeven dagen. U gebruikt ze om de tijd te volgen die aan projecten wordt besteed en u kunt ze gebruiken om eenvoudige registratie van resourcetijd vast te leggen. Voordat u urenstaten kunt gebruiken, moet u opgeven hoe u wilt dat ze worden ingesteld en geconfigureerd.

Nadat u hebt ingesteld hoe uw organisatie urenstaten gaat gebruiken, kunt u opgeven of en hoe urenstaten worden goedgekeurd. Afhankelijk van de wensen van uw organisatie kunt u het volgende aangeven:

* Een of meer gebruikers als urenstatenbeheerders en fiatteurs voor alle urenstaten.
* Een urenstaatgoedkeurder voor elke resource.

Wanneer u urenstaten hebt ingesteld, kunt u urenstaten maken voor resources, ze toewijzen een projectplanningsregels en urenstaatregels boeken. Zie [Urenstaten gebruiken](projects-how-use-time-sheets.md) voor meer informatie.

## <a name="to-set-up-general-information-for-time-sheets"></a>Algemene informatie instellen voor urenstaten
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png ""pictogram Zoeken naar pagina of rapport"), voer **Resource-instellingen** in en klik vervolgens op de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Selecteer voor het veld **Urenstaat op taakgoedkeuring** een van de volgende opties.

| Optie | Omschrijving |
| --- | --- |
| **Nooit** |De gebruiker in het veld **Gebruikers-id van fiatteur van urenstaat** op de resourcekaart keurt de urenstaat goed. |
| **Altijd** |De gebruiker in het veld **Verantwoordelijke** op de projectkaart keurt de urenstaat goed. |
| **Alleen machine** |Als de urenstaat van een machine is gekoppeld aan een project, keurt de gebruiker in het veld **Verantwoordelijke** op de projectkaart de urenstaat goed. Als de urenstaat van een machine is gekoppeld aan een resource, keurt de gebruiker in het veld **Gebruikers-id van fiatteur van urenstaat** op de resourcekaart de urenstaat goed. |

## <a name="to-assign-a-time-sheet-administrator"></a>Een beheerder van urenstaten toewijzen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikersinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
2. Voeg een nieuwe gebruiker toe als de lijst met gebruikers niet de persoon bevat die de beheerder van urenstaten moet zijn. Zie [Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.
3. Selecteer een gebruiker als beheerder van urenstaten en schakel vervolgens het selectievakje **Urenstaat-admin** in.  

> [!TIP]  
>   Het is raadzaam dat u slechts één gebruiker als beheerder van urenstaten van een bedrijf aanwijst. In de volgende procedure stelt u een urenstaateigenaar en fiatteur in waarbij de urenstaatfiatteur voor elke resource wordt toegewezen.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Een urenstaateigenaar en -fiatteur toewijzen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Resources** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de resource waarvoor u de mogelijkheid wilt instellen om urenstaten te gebruiken, en schakel vervolgens het selectievakje **Urenstaat gebruiken** in.  
3. Voer in het veld **Gebruikers-id van eigenaar van urenstaat** de id in van de eigenaar van de urenstaat. De eigenaar kan tijdsgebruik op een urenstaat invoeren en indienen voor goedkeuring. Als de resource een persoon, is die persoon in het algemeen ook de eigenaar.  
4. Voer in het veld **Gebruikers-id van fiatteur van urenstaat** de id in van de fiatteur van de urenstaat. De goedkeurder kan goedkeuren, weigeren of een urenstaat opnieuw openen.  

> [!NOTE]  
>   U kunt de ID van de urenstaatgoedkeurder niet wijzigen als er urenstaten zijn die nog niet zijn verwerkt en die de status **Ingediend** of **Open** hebben.

## <a name="see-also"></a>Zie ook
[Projectbeheer instellen](projects-setup-projects.md)  
[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)         
[Verkoop](sales-manage-sales.md)      
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

