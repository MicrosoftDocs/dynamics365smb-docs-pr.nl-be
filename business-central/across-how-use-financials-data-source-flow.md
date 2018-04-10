---
title: Uw gegevens verbinden met Flow| Microsoft Docs
description: U kunt uw Financials-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een geautomatiseerde werkstroom te maken.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/21/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5d7fa359ee99cd177a445e025ddf8d156c6e2421
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in een geautomatiseerde werkstroom
U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als onderdeel van een werkstroom in Microsoft Flow gebruiken.  

> [!NOTE]  
>   U moet een geldige account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Flow hebben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in Flow toevoegen
1. Navigeer in uw browser naar [flow.microsoft.com](https://flow.microsoft.com/en-us/) en meld u aan.
2. Kies **Mijn Flows** vanuit het lint boven aan de pagina.
3. Er zijn twee manieren om een stroom te maken: **Maken van sjabloon** en **Geheel nieuw maken**. Een sjabloon is een vooraf gedefinieerde stroom die voor u is gemaakt.  Als u een sjabloon wilt gebruiken, selecteert u deze en maakt u een verbinding voor elke service die de sjabloon gebruikt. Met een lege sjabloon kunt u een helemaal nieuwe stroom maken. 
4. Als u een nieuwe stroom wilt maken, kiest u in het venster **Mijn flows** de optie **Geheel nieuw maken**.
5. Zoek **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-connector.
6. Selecteer in de lijst met beschikbare triggers een van de beschikbare [!INCLUDE[d365fin](includes/d365fin_md.md)]-triggers:  
    *Wanneer een klantgoedkeuring wordt aangevraagd*,  
    *Wanneer goedkeuring van een dagboekbatch wordt aangevraagd*,  
    *Wanneer goedkeuring van een dagboekregel wordt aangevraagd*,  
    *Wanneer goedkeuring van een artikel wordt aangevraagd*,  
    *Wanneer goedkeuring van een inkoopdocument wordt aangevraagd*,  
    *Wanneer goedkeuring van een verkoopdocument wordt aangevraagd*, of  
    *Wanneer goedkeuring van een leverancier wordt aangevraagd*.
7. Flow vraagt u een bedrijf in uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-tenant te selecteren, plus eventuele voorwaarden in uw gegevens te selecteren waarop u moet letten. 

Nu hebt u met succes een verbinding gemaakt met uw Business Central-gegevens en kunt u uw stroom gaan maken. 

8. Als u een flow van een sjabloon wilt maken, kiest u de optie **Maken van sjabloon**.
9. Zoek **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-sjablonen. 
10. Selecteer een van de sjablonen in de lijst met beschikbare sjablonen.  
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
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dagboekbatch*,  
    *Goedkeuring aanvragen voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dagboekregels*.  
11. Flow vraagt u een bedrijf in uw [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-tenant te selecteren. Aangezien elke stap in Flow onafhankelijk is van de volgende, moet u het bedrijf mogelijk meerdere malen definiëren wanneer u een [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-sjabloon gebruikt.
12. De Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-sjabloon is geïntegreerd met de kernwerkstroomengine in Microsoft[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Dat betekent dat telkens wanneer u een van deze sjablonen gebruikt om een flow te maken, een corresponderende workflow wordt gemaakt in Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Raadpleeg de werkstroomdocumentatie voor Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

Zie de [Flow-documentatie](https://docs.microsoft.com/en-us/flow/getting-started) voor meer informatie.

Zie voor het oplossen van problemen met Microsoft Flow [Problemen oplossen met integratie met Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Zie ook
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)   
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-werkstromen beheren](across-use-workflows.md)  
[Gebruikersinstellingen voor goedkeuring](across-how-to-set-up-approval-users.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  

