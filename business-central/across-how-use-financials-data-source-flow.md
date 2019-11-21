---
title: Uw gegevens verbinden met Flow| Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een geautomatiseerde werkstroom te maken.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: a46692503b19ddad57c4a68d0f29b588d84f5c9e
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775463"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in een geautomatiseerde werkstroom
U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als onderdeel van een werkstroom in Microsoft Flow gebruiken.

> [!NOTE]
> Naast Microsoft Flow kunt u de werkstroomfunctionaliteit binnen [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken. Het zijn twee aparte werkstroomsystemen, maar elke Flow-sjabloon die u maakt met Microsoft Flow, wordt toegevoegd aan de lijst met werkstromen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

> [!NOTE]  
> U moet een geldige account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Flow hebben.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in Flow toevoegen
1. Navigeer in uw browser naar [flow.microsoft.com](https://flow.microsoft.com/en-us/) en meld u aan.
2. Kies **Mijn Flows** vanuit het lint boven aan de pagina.
3. Er zijn 3 manieren om een Flow te maken; **Beginnen met sjabloon**, **Geheel nieuw maken** en **Beginnen met een connector**. Een sjabloon is een vooraf gedefinieerde stroom die voor u is gemaakt. Als u een sjabloon wilt gebruiken, selecteert u deze en maakt u een verbinding voor elke service die de sjabloon gebruikt. Met de opties **Geheel nieuw maken** en **Beginnen met een connector** kunt u een volledig nieuwe Flow maken.
4. Als u een geheel nieuwe stroom wilt maken, kiest u op de pagina **Mijn flows** de opties **Geheel nieuw maken** en **Geautomatiseerde stroom**.
5. Zoek **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-connector.
6. Definieer een naam en kies de trigger die u voor uw Flow wilt gebruiken.
7. Selecteer in de lijst met beschikbare triggers een van de beschikbare [!INCLUDE[d365fin](includes/d365fin_md.md)]-triggers:  
    
    *Wanneer goedkeuring van een leverancier wordt aangevraagd*.    
    *Wanneer goedkeuring van een dagboekregel wordt aangevraagd*,    
    *Wanneer een record wordt verwijderd*.    
    *Wanneer een record wordt gewijzigd*.    
    *Wanneer een record wordt gemaakt*.    
    *Wanneer een record wordt aangepast*.    
    *Wanneer goedkeuring van een dagboekbatch wordt aangevraagd*,   
    *Wanneer een klantgoedkeuring wordt aangevraagd*,   
    *Wanneer goedkeuring van een artikel wordt aangevraagd*,    
    *Wanneer goedkeuring van een inkoopdocument wordt aangevraagd* of     
     *Wanneer goedkeuring van een verkoopdocument wordt aangevraagd*.
     
8. Flow vraagt u een omgeving en bedrijf in uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-tenant te selecteren, plus eventuele voorwaarden in uw gegevens te selecteren waarop u moet letten.

> [!NOTE]  
>   De [!INCLUDE[d365fin](includes/d365fin_md.md)]-connector voor Microsoft Flow ondersteunt meerdere productie- en sandboxomgevingen. Als u niet meerdere productie- of sandboxomgevingen hebt gemaakt, is **Productie** de enige beschikbare optie die u kunt kiezen. 

Nu hebt u met succes een verbinding gemaakt met uw Business Central-gegevens en kunt u uw stroom gaan maken.

9. Als u een flow van een sjabloon wilt maken, kiest u de optie **Beginnen met sjabloon**.
10. Zoek **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-sjablonen.
11. Selecteer een van de sjablonen in de lijst met beschikbare sjablonen en kies vervolgens **Maken**.  

    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-verkooporder*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-verkoopofferte*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-verkoopfactuur*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-verkoopcreditnota*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-klant*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inkooporder*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inkoopfactuur*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inkoopcreditnota*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-artikel*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-leverancier*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dagboekbatch* of    
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dagboekregels*.  
12. Flow geeft een lijst met services weer die in de Flow-sjabloon worden gebruikt en probeert automatisch verbinding te maken met die services. Als u nog niet eerder verbinding hebt gemaakt met een service, wordt u gevraagd zich aan te melden bij elke service waarmee u verbinding wilt maken. Een groen vinkje verschijnt naast elke service zodra een verbinding tot stand is gebracht. Selecteer **Doorgaan**.
13. Flow vraagt u een omgeving en bedrijf in uw [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-tenant te selecteren. Aangezien elke stap in de stroom onafhankelijk is van de volgende, moet u de omgeving en het bedrijf mogelijk meerdere malen definiëren wanneer u een [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Flow-sjabloon gebruikt.

Zie de [Flow-documentatie](/flow/getting-started) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Aan de slag](product-get-started.md)  
[Werkstroom](across-workflow.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)   
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-werkstromen beheren](across-use-workflows.md)  
[Gebruikersinstellingen voor goedkeuring](across-how-to-set-up-approval-users.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  
