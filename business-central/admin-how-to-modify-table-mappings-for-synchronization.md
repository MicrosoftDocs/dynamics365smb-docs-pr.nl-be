---
title: Tabeltoewijzingen wijzigen voor synchronisatie | Microsoft Docs
description: Leer hoe u de tabeltoewijzingen wijzigt die worden gebruikt wanneer gegevens worden gesynchroniseerd tussen Business Central en Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 505c1427c63a0a6f9e68980ea0ff05c93918ea60
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308095"
---
# <a name="modify-table-mappings-for-synchronization"></a>Tabeltoewijzingen wijzigen voor synchronisatie
Een integratietabeltoewijzing koppelt een tabel in [!INCLUDE[d365fin](includes/d365fin_md.md)] aan een integratietabel voor de [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit. Voor elke entiteit in [!INCLUDE[crm_md](includes/crm_md.md)] die u wilt synchroniseren met bijbehorende gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet er een bijbehorende integratietabeltoewijzing zijn. Een integratietabeltoewijzing bevat verschillende instellingen om te bepalen hoe records in een [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en een [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit worden gesynchroniseerd door de bijbehorende integratiesynchronisatietaken.  

## <a name="filtering-records"></a>Records filteren  
 Als u niet alle records voor een bepaalde [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit of [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel wilt synchroniseren, kunt u filters instellen om de records te beperken die worden gesynchroniseerd. U stelt filters in op de pagina **Toewijzingen van integratietabellen**.  

#### <a name="to-filter-records-for-synchronization"></a>Records filteren voor synchronisatie  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.

2.  Als u de [!INCLUDE[d365fin](includes/d365fin_md.md)]-records wilt filteren, stelt u het veld **Tabelfilter** in.  

3.  Als u de [!INCLUDE[crm_md](includes/crm_md.md)]-records wilt filteren, stelt u het veld **Filter integratietabel** in.  

## <a name="creating-new-records"></a>Nieuwe records maken  
 Standaard worden alleen records in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] die zijn gekoppeld, door de integratiesynchronisatietaken gesynchroniseerd. U kunt tabeltoewijzingen zo instellen dat nieuwe records worden gemaakt op de bestemming (bijvoorbeeld [!INCLUDE[d365fin](includes/d365fin_md.md)]) voor elke record in de bron (bijvoorbeeld [!INCLUDE[crm_md](includes/crm_md.md)]) die nog niet is gekoppeld.  

 De Dynamics 365 Sales-synchronisatietaak gebruikt bijvoorbeeld de tabeltoewijzing VERKOPERS. De synchronisatietaak kopieert gegevens uit gebruikersrecords in [!INCLUDE[crm_md](includes/crm_md.md)] naar verkopersrecords in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als u de tabeltoewijzing instelt om nieuwe records te maken, wordt voor elke gebruiker in [!INCLUDE[crm_md](includes/crm_md.md)] die niet al is gekoppeld aan een verkoper in [!INCLUDE[d365fin](includes/d365fin_md.md)], een nieuwe verkopersrecord gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Nieuwe records maken tijdens synchronisatie  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.

2.  Wis in het tabeltoewijzingsitem in de lijst het veld **Alleen gekoppelde records synchr.**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Configuratiesjablonen gebruiken met tabeltoewijzingen
U kunt configuratiesjablonen aan tabeltoewijzingen toewijzen om te gebruiken voor nieuwe records die worden gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)] of [!INCLUDE[crm_md](includes/crm_md.md)]. Voor elke tabeltoewijzing kunt u een configuratiesjabloon opgeven voor nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-records en een andere sjabloon om nieuwe [!INCLUDE[crm_md](includes/crm_md.md)]-records te gebruiken.  

Als u de standaardsynchronisatie-instelling installeert, worden meestal automatisch twee configuratiesjablonen gemaakt en gebruikt voor de tabeltoewijzing voor [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten en [!INCLUDE[crm_md](includes/crm_md.md)]-accounts: **CRMCUST** en **CRMACCOUNT**.  

-   **CRMCUST** wordt gebruikt om nieuwe klanten te maken en te synchroniseren in [!INCLUDE[d365fin](includes/d365fin_md.md)], op basis van een account in [!INCLUDE[crm_md](includes/crm_md.md)].  

     Deze sjabloon wordt gemaakt door een bestaande configuratiesjabloon te kopiëren voor klanten in de toepassing. **CRMCUST** wordt alleen gemaakt als er een bestaande configuratiesjabloon is en het veld **Valutacode** in de sjabloon leeg is. Als een veld in de configuratiesjabloon een waarde bevat, wordt die waarde gebruikt in plaats van de waarde in het toegewezen veld in het [!INCLUDE[crm_md](includes/crm_md.md)]-account. Bijvoorbeeld als het veld **Land/regio** in een [!INCLUDE[crm_md](includes/crm_md.md)]-account *VS* is en het veld **Land/regio** in de configuratiesjabloon *GB* is, wordt *GB* gebruikt als **Land/regio** voor de klant in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** maakt en synchroniseert nieuwe accounts in [!INCLUDE[crm_md](includes/crm_md.md)] op basis van een account in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Configuratiesjablonen opgeven voor een tabeltoewijzing  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.

2.  Kies in de tabeltoewijzingspost in de lijst in het veld **Sjablooncode voor tabelconfiguratie** de configuratiesjabloon die moet worden gebruikt voor nieuwe records in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Stel het veld **Sjablooncode voor int. tabelconfig.** in op de configuratiesjabloon die moet worden gebruikt voor nieuwe records in [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Zie ook  
[Over integratie van Dynamics 365 Business Central met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Business Central en Dynamics 365 Sales synchroniseren](admin-synchronizing-business-central-and-sales.md)   
[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
