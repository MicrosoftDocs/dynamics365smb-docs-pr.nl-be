---
title: Een integratie met Dynamics 365 Sales upgraden | Microsoft Docs
description: Leren hoe u Dynamics 365 Business Central voorbereidt op integratie met Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 2a5f58ac904ea05f4410ac9e1b804df1cb01c609
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410680"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Een integratie met Dynamics 365 Sales upgraden
[!INCLUDE[d365fin](includes/d365fin_md.md)] integreert ook met [!INCLUDE[d365fin](includes/cds_long_md.md)], waardoor het eenvoudig is om gegevens te verbinden en te synchroniseren met andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)], of zelfs apps die u zelf bouwt. Als u voor de eerste keer integreert, raden we u aan dit te doen via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Zie voor meer informatie [Integratie met Common Data Service](admin-common-data-service.md).

Als u al [!INCLUDE[crm_md](includes/crm_md.md)] hebt geïntegreerd met [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u gegevens blijven synchroniseren met uw setup. Als u echter een upgrade op [!INCLUDE[d365fin](includes/d365fin_md.md)] uitvoert of uw [!INCLUDE[crm_md](includes/crm_md.md)]-integratie uitschakelt, moet u om het weer in te schakelen verbinding maken via [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

> [!NOTE]
> Opnieuw verbinding maken via [!INCLUDE[d365fin](includes/cds_long_md.md)] past standaard synchronisatie-instellingen toe en overschrijft alle configuraties die u hebt. Zo worden de standaardtabeltoewijzingen toegepast.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Uw verbinding upgraden om Common Data Service te gebruiken
1. Open de pagina **Microsoft Dynamics 365-verbinding instellen**, kies de schakelaar **Inschakelen** om uw bestaande verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] uit te schakelen.
2. Open de pagina **Common Data Service-verbinding instellen** en kies de schakelaar **Inschakelen** om de verbinding in te schakelen.
  
   Nadat u de CDS-verbinding hebt ingeschakeld, wordt de Business Central CDS-basisintegratieoplossing geïmplementeerd naar Common Data Service.
3. Verwijder de Microsoft Dynamics 365 Business Central Integratie-oplossing uit uw Dynamics 365 Sales volgens [Een oplossingsonderwerp de-installeren of verwijderen](/powerapps/developer/common-data-service/uninstall-delete-solution) 

4. Kies op de pagina Microsoft Dynamics 365-verbinding instellen de schakelaar Inschakelen om de verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] in te schakelen.
  
   Nadat u de Sales-verbinding hebt ingeschakeld, wordt de Business Central-integratieoplossing geïmplementeerd naar Sales. Dit maakt integratie mogelijk met entiteiten die specifiek zijn voor [!INCLUDE[crm_md](includes/crm_md.md)], zoals verkooporders, offertes en facturen.
5. Kies **Integratieoplossing opnieuw implementeren** om de bijgewerkte Business Central-integratieoplossing te installeren en configureren.
6. Kies op de pagina **Sales-verbinding instellen** **Standaardsynchronisatie-instellingen** om de integratietabeltoewijzingen te initialiseren voor [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Zie ook
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integreren met Common Data Service](admin-common-data-service.md)
