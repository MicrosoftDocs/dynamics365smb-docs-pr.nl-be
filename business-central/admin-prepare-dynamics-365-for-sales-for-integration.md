---
title: Integratie met Dynamics 365 for Sales| Microsoft Docs
description: Leren hoe u Dynamics 365 Business Central voorbereidt op integratie met Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 991d8432c24b1963da019e3c8b665f9ad009d077
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247292"
---
# <a name="integrating-with-dynamics-365-for-sales"></a>Integreren met Dynamics 365 for Sales
De functie van verkoper wordt vaak beschouwd als een van de meest naar buiten gerichte taken in een bedrijf. Het kan voor verkopers echter handig zijn in het bedrijf te kunnen kijken en te zien wat er bij de backend gebeurt. Door [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] te integreren kunt u uw verkopers dat inzicht geven door ze informatie in [!INCLUDE[d365fin](includes/d365fin_md.md)] te laten zien terwijl ze werken in [!INCLUDE[crm_md](includes/crm_md.md)]. Bijvoorbeeld, tijdens het voorbereiden van een verkoopofferte kan het handig zijn om te weten of u voldoende voorraad hebt om de order te kunnen vervullen. Zie voor meer informatie [Dynamics 365 for Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md).

> [!Note]
> Deze stappen beschrijven de integratie van online versies van [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)].

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Overzicht van het integratieproces
De volgende stappen geven een overzicht van de stappen om [!INCLUDE[crm_md](includes/crm_md.md)] te integreren met [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Deze taken vereisen de beveiligingsrol **Systeembeheerder** in [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Stel in het Office 365-beheercentrum een gebruikersaccount in voor de verbinding met en synchronisatie van gegevens met [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integratie met Dynamics 365 for Sales instellen](admin-setting-up-integration-with-dynamics-sales.md).

2. Wijs licenties voor [!INCLUDE[crm_md](includes/crm_md.md)] toe aan de [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers die de geïntegreerde apps zullen gebruiken.

3. Een verbinding instellen met [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Een verbinding instellen met Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Optioneel: koppel [!INCLUDE[d365fin](includes/d365fin_md.md)]- en [!INCLUDE[crm_md](includes/crm_md.md)]-records. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md).

5. Gegevens synchroniseren tussen de apps. Zie voor meer informatie [Business Central en Dynamics 365 for Sales synchroniseren](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Over de Business Central-integratieoplossing
Met de oplossing kunnen gebruikers informatie bekijken in [!INCLUDE[d365fin](includes/d365fin_md.md)] terwijl ze werken in [!INCLUDE[crm_md](includes/crm_md.md)]. De oplossing geeft bijvoorbeeld inzicht in klantstatistieken, biedt gebruikers de mogelijkheid records in [!INCLUDE[d365fin](includes/d365fin_md.md)] te koppelen en weer te geven uit [!INCLUDE[crm_md](includes/crm_md.md)] en laat gebruikers zien of producten beschikbaar zijn in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Standaard importeert de begeleide instelling Dynamics 365 for Sales-verbinding instellen de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratieoplossing. De begeleide instelling gebruikt daarvoor een beheerdersaccount. Dit account moet ook een geldige gebruiker in [!INCLUDE[crm_md](includes/crm_md.md)] zijn met de volgende beveiligingsrollen:

* Systeembeheerder  
* Oplossingsaanpasser  

Zie voor meer informatie [Gebruikersaccounts instellen voor integratie met Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md), [Gebruikers maken in Microsoft Dynamics 365 (online) en beveiligingsrollen toewijzen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles.md) en [Gebruikers en machtigingen beheren](ui-how-users-permissions.md).  

Dit account wordt slechts eenmaal gebruikt tijdens het instellen. Nadat de oplossing is geïmporteerd in [!INCLUDE[d365fin](includes/d365fin_md.md)], is het account niet meer nodig. Integratie gaat door met het gebruikersaccount te gebruiken dat specifiek voor de integratie is gemaakt.

Naast het aanpassen van [!INCLUDE[crm_md](includes/crm_md.md)] maakt de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratieoplossing ook de volgende rollen in [!INCLUDE[crm_md](includes/crm_md.md)] voor de integratie:

* **Integratiebeheerder** - Biedt gebruikers de mogelijkheid de verbinding te beheren tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)]. Meestal alleen toegewezen aan het gebruikersaccount voor synchronisatie.  
* **Integratiegebruiker** - Geeft gebruikers toegang tot gesynchroniseerde gegevens. Meestal toegewezen aan het gebruikersaccount voor synchronisatie en een andere gebruiker die de gesynchroniseerde gegevens moet bekijken of openen.
* **Gebruiker van productbeschikbaarheid** - Biedt gebruikers de mogelijkheid productbeschikbaarheid in [!INCLUDE[d365fin](includes/d365fin_md.md)] op te vragen vanuit [!INCLUDE[crm_md](includes/crm_md.md)].

Aan het eind van de begeleide instelling vraagt [!INCLUDE[d365fin](includes/d365fin_md.md)] u verkopers te koppelen aan gebruikers [!INCLUDE[crm_md](includes/crm_md.md)]. Aan records in [!INCLUDE[crm_md](includes/crm_md.md)] wordt gewoonlijk een eigenaar (gebruiker) toegewezen en als er geen koppeling bestaat tussen de gebruiker in [!INCLUDE[crm_md](includes/crm_md.md)] en de verkoper in [!INCLUDE[d365fin](includes/d365fin_md.md)], mislukt de synchronisatie. U kunt dit ook later doen door de actie **Verkopers koppelen** te gebruiken op de pagina **Microsoft Dynamics 365-verbinding instellen**.

## <a name="see-also"></a>Zie ook  
[Gebruikersaccounts instellen voor integratie met Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Een verbinding instellen met Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)
[Business Central en Dynamics 365 for Sales synchroniseren](admin-synchronizing-business-central-and-sales.md)
