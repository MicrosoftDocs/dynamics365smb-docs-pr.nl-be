---
title: Een integratie met Dynamics 365 Sales upgraden
description: Leer hoe u uw Dynamics 365 Business Central-integratie met Dynamics 365 Sales naar de nieuwste versie overzet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 69ffe6cea05cc28d1950481a07b064a3365f404e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386711"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Een integratie met Dynamics 365 Sales upgraden
[!INCLUDE[prod_short](includes/prod_short.md)] integreert ook met [!INCLUDE[prod_short](includes/cds_long_md.md)], waardoor het eenvoudig is om gegevens te verbinden en te synchroniseren met andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)], of zelfs apps die u zelf bouwt. Als u voor de eerste keer integreert, raden we u aan dit te doen via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor meer informatie [Integratie met Dataverse](admin-common-data-service.md).

Als u al [!INCLUDE[crm_md](includes/crm_md.md)] hebt geïntegreerd met [!INCLUDE[prod_short](includes/prod_short.md)], kunt u gegevens blijven synchroniseren met uw setup. Als u echter een upgrade op [!INCLUDE[prod_short](includes/prod_short.md)] uitvoert of uw [!INCLUDE[crm_md](includes/crm_md.md)]-integratie uitschakelt, moet u om het weer in te schakelen verbinding maken via [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

> [!NOTE]
> Opnieuw verbinding maken via [!INCLUDE[prod_short](includes/cds_long_md.md)] past standaard synchronisatie-instellingen toe en overschrijft alle configuraties die u hebt. Zo worden de standaardtabeltoewijzingen toegepast.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Uw verbinding upgraden om Dataverse te gebruiken
1. Open de pagina **Microsoft Dynamics 365-verbinding instellen** en zet de schakelaar **Ingeschakeld** uit om de verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] te verbreken.
2. Open de pagina **Dataverse-verbinding instellen** en kies de schakelaar **Ingeschakeld** om de verbinding met [!INCLUDE[prod_short](includes/cds_long_md.md)] in te schakelen.
  
   > [!NOTE]
   > Nadat u de verbinding hebt ingeschakeld, wordt de Business Central-integratieoplossing geïmplementeerd naar Dataverse.
3. Kies **Integratieoplossing opnieuw implementeren** om de Business Central-integratieoplossing opnieuw te installeren.
4. Ga naar de pagina **Microsoft Dynamics 365-verbinding instellen** en zet de schakelaar **Ingeschakeld** aan om weer verbinding te maken met [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > Nadat u de verbinding hebt ingeschakeld, wordt de Business Central-integratieoplossing geïmplementeerd naar [!INCLUDE[prod_short](includes/prod_short.md)]. Dit maakt integratie mogelijk met tabellen die specifiek zijn voor [!INCLUDE[crm_md](includes/crm_md.md)], zoals verkooporders, offertes en facturen.
5. Kies **Integratieoplossing opnieuw implementeren** om de Business Central-integratieoplossing opnieuw te installeren.
6. Kies op de pagina **Sales-verbinding instellen** **Standaardsynchronisatie-instellingen** om de integratietabeltoewijzingen te initialiseren voor [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Zie ook
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integreren met Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]