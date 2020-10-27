---
title: Uw gegevens verbinden met Power Automate | Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een geautomatiseerde werkstroom te maken.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: bmeier
ms.openlocfilehash: 8f4da5b51b4e0df5cdf6f41f7a78c0a51cf0f083
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924865"
---
# <a name="using-prodshort-in-an-automated-workflow"></a>[!INCLUDE[prodshort](includes/prodshort.md)] gebruiken in een geautomatiseerde werkstroom

U kunt uw [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens als onderdeel van een werkstroom in Microsoft Power Automate gebruiken.

> [!NOTE]
> Naast Power Automate kunt u de werkstroomfunctionaliteit binnen [!INCLUDE[prodshort](includes/prodshort.md)] gebruiken. Het zijn twee aparte werkstroomsystemen, maar elke werkstroomsjabloon die u maakt met Power Automate, wordt toegevoegd aan de lijst met werkstromen in [!INCLUDE[prodshort](includes/prodshort.md)]. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

> [!NOTE]  
> U moet een geldig account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power Automate hebben.  

## <a name="to-add-prodshort-as-a-data-source-in-power-automate"></a>[!INCLUDE[prodshort](includes/prodshort.md)] als gegevensbron toevoegen in Power Automate

1. Navigeer in uw browser naar [flow.microsoft.com](https://flow.microsoft.com) en meld u aan.
2. Kies **Mijn Flows** vanuit het lint boven aan de pagina.
3. Er zijn 3 manieren om een stroom te maken; **Beginnen met sjabloon** , **Geheel nieuw maken** en **Beginnen met een connector** . Een sjabloon is een vooraf gedefinieerde stroom die voor u is gemaakt. Als u een sjabloon wilt gebruiken, selecteert u deze en maakt u een verbinding voor elke service die de sjabloon gebruikt. Met de opties **Geheel nieuw maken** en **Beginnen met een connector** kunt u een volledig nieuwe stroom maken.
4. Als u een geheel nieuwe stroom wilt maken, kiest u op de pagina **Mijn Flows** de opties **Geheel nieuw maken** en **Geautomatiseerde stroom** .
5. Zoek **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]** -connector.
6. Definieer een naam en kies de trigger die u voor uw stroom wilt gebruiken.
7. Selecteer in de lijst met beschikbare triggers een van de beschikbare [!INCLUDE[prodshort](includes/prodshort.md)]-triggers:  

    *Wanneer goedkeuring van een leverancier wordt aangevraagd* .  
    *Wanneer goedkeuring van een dagboekregel wordt aangevraagd* ,  
    *Wanneer een record wordt verwijderd* .  
    *Wanneer een record wordt gewijzigd* .  
    *Wanneer een record wordt gemaakt* .  
    *Wanneer een record wordt aangepast* .  
    *Wanneer goedkeuring van een dagboekbatch wordt aangevraagd* ,  
    *Wanneer een klantgoedkeuring wordt aangevraagd* ,  
    *Wanneer goedkeuring van een artikel wordt aangevraagd* ,  
    *Wanneer goedkeuring van een inkoopdocument wordt aangevraagd* of  
    *Wanneer goedkeuring van een verkoopdocument wordt aangevraagd* .

8. Power Automate vraagt u een omgeving en bedrijf in uw [!INCLUDE[prodshort](includes/prodshort.md)]-tenant te selecteren, plus eventuele voorwaarden in uw gegevens te selecteren waarop u moet letten.

    > [!NOTE]
    > De [!INCLUDE[prodshort](includes/prodshort.md)]-connector voor Power Automate ondersteunt meerdere productie- en sandboxomgevingen. Als u niet meerdere productie- of sandboxomgevingen hebt gemaakt, is **Productie** de enige beschikbare optie die u kunt kiezen.  

    Nu hebt u met succes een verbinding gemaakt met uw Business Central[!INCLUDE[prodshort](includes/prodshort.md)]-gegevens en kunt u uw stroom gaan maken.

9. Als u een flow van een sjabloon wilt maken, kiest u de optie **Beginnen met sjabloon** .
10. Zoek **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]** -sjablonen.
11. Selecteer een van de sjablonen in de lijst met beschikbare sjablonen en kies vervolgens **Maken** .  

    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-verkooporder* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-verkoopofferte* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-verkoopfactuur* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-verkoopcreditnota* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-klant* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inkooporder* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inkoopfactuur* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inkoopcreditnota* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-artikel* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-leverancier* ,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dagboekbatch* of    
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dagboekregels* .  
12. Power Automate geeft een lijst met services weer die in de stroomsjabloon worden gebruikt en probeert automatisch verbinding te maken met die services. Als u nog niet eerder verbinding hebt gemaakt met een service, wordt u gevraagd zich aan te melden bij elke service waarmee u verbinding wilt maken. Een groen vinkje verschijnt naast elke service zodra een verbinding tot stand is gebracht. Selecteer **Doorgaan** .
13. Power Automate vraagt u een omgeving en bedrijf in uw [!INCLUDE[prodshort](includes/prodshort.md)]-tenant te selecteren. Aangezien elke stap in de stroom onafhankelijk is van de volgende, moet u de omgeving en het bedrijf mogelijk meerdere malen definiëren wanneer u een [!INCLUDE[prodshort](includes/prodshort.md)] Power Automate-sjabloon gebruikt.

Zie voor meer informatie de [documentatie van Power Automate](/power-automate/getting-started).

## <a name="see-also"></a>Zie ook

[Aan de slag](product-get-started.md)  
[Werkstroom](across-workflow.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[[!INCLUDE[prodlong](includes/prodlong.md)]-werkstromen beheren](across-use-workflows.md)  
[Gebruikersinstellingen voor goedkeuring](across-how-to-set-up-approval-users.md)  
[Instellen van [!INCLUDE[prodshort](includes/prodshort.md)]](setup.md)  
[Financiën](finance.md)  
