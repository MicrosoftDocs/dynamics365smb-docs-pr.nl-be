---
title: Een integratie met Dynamics 365 Sales upgraden
description: Leer hoe u uw Dynamics 365 Business Central-integratie met Dynamics 365 Sales naar de nieuwste versie overzet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3bb6b26e011afc515fbd4f492f56b3090c56e860
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922379"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Een integratie met Dynamics 365 Sales upgraden
[!INCLUDE[d365fin](includes/d365fin_md.md)] integreert ook met [!INCLUDE[d365fin](includes/cds_long_md.md)], waardoor het eenvoudig is om gegevens te verbinden en te synchroniseren met andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)], of zelfs apps die u zelf bouwt. Als u voor de eerste keer integreert, raden we u aan dit te doen via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Zie voor meer informatie [Integratie met Common Data Service](admin-common-data-service.md).

Als u al [!INCLUDE[crm_md](includes/crm_md.md)] hebt geïntegreerd met [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u gegevens blijven synchroniseren met uw setup. Als u echter een upgrade op [!INCLUDE[d365fin](includes/d365fin_md.md)] uitvoert of uw [!INCLUDE[crm_md](includes/crm_md.md)]-integratie uitschakelt, moet u om het weer in te schakelen verbinding maken via [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

> [!NOTE]
> Opnieuw verbinding maken via [!INCLUDE[d365fin](includes/cds_long_md.md)] past standaard synchronisatie-instellingen toe en overschrijft alle configuraties die u hebt. Zo worden de standaardtabeltoewijzingen toegepast.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Uw verbinding upgraden om Common Data Service te gebruiken
1. Open de pagina **Microsoft Dynamics 365-verbinding instellen** , kies de schakelaar **Inschakelen** om uw bestaande verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] uit te schakelen.
2. Open de pagina **Common Data Service-verbinding instellen** en kies de schakelaar **Inschakelen** om de verbinding in te schakelen.
  
   Nadat u de CDS-verbinding hebt ingeschakeld, wordt de Business Central CDS-basisintegratieoplossing geïmplementeerd naar Common Data Service.
3. Verwijder de Microsoft Dynamics 365 Business Central-integratieoplossing uit Dynamics 365 Sales. Zie [Een oplossing deïnstalleren of verwijderen](/powerapps/developer/common-data-service/uninstall-delete-solution) voor meer informatie. 

4. Ga naar de pagina **Microsoft Dynamics 365-verbinding instellen** en stel de wisselknop **Inschakelen** in op het maken van een verbinding met [!INCLUDE[crm_md](includes/crm_md.md)].
  
   Nadat u de Sales-verbinding hebt ingeschakeld, wordt de Business Central-integratieoplossing geïmplementeerd naar Sales. Dit maakt integratie mogelijk met entiteiten die specifiek zijn voor [!INCLUDE[crm_md](includes/crm_md.md)], zoals verkooporders, offertes en facturen.
5. Kies op de pagina **Sales-verbinding instellen** **Standaardsynchronisatie-instellingen** om de integratietabeltoewijzingen te initialiseren voor [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Zie ook
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integreren met Common Data Service](admin-common-data-service.md)
