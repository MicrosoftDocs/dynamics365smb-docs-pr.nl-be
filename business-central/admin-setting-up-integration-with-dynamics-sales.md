---
title: Gebruikersaccounts instellen voor integratie met Microsoft Dataverse | Microsoft Docs
description: Leer hoe u gebruikersaccounts instelt die de apps gebruiken om gegevens uit te wisselen, en die personen gebruiken om toegang te krijgen tot gegevens in de apps en deze te synchroniseren.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 7683c301131fa5729d74e1c6ef70880db7f3327d
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607350"
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse"></a>Gebruikersaccounts instellen voor integratie met Microsoft Dataverse

Dit artikel geeft een overzicht van hoe u de gebruikersaccounts instelt die vereist zijn om [!INCLUDE[prod_short](includes/cds_long_md.md)] te integreren met [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-administrator-user-account"></a>Het beheerdersaccount instellen

U moet uw beheerdersaccount toevoegen voor [!INCLUDE[prod_short](includes/prod_short.md)] als gebruiker in [!INCLUDE[cds_long](includes/cds_long_md.md)]. Bij het instellen van de verbinding tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)] wordt dit account één keer gebruikt om enkele vereiste onderdelen te installeren en configureren.

> [!IMPORTANT]
> Het beheerdersaccount moet een gelicentieerde gebruiker zijn met de beveiligingsrol **Systeembeheerder** in de [!INCLUDE[prod_short](includes/cds_long_md.md)]-omgeving en globale beheerder op de tenant waartoe de omgeving behoort. Dit account heeft geen licentie nodig voor [!INCLUDE[prod_short](includes/prod_short.md)], omdat het alleen wordt gebruikt om de service te leveren in de [!INCLUDE[prod_short](includes/cds_long_md.md)]-tenant en om instellingstaken uit te voeren.
>
> Nadat de verbinding is ingesteld, kan deze [!INCLUDE[prod_short](includes/cds_long_md.md)]-gebruiker worden verwijderd. De integratie blijft het gebruikersaccount gebruiken dat automatisch specifiek voor de integratie wordt gemaakt.

## <a name="permissions-and-security-roles-for-user-accounts-in-prod_short"></a>Machtigingen en beveiligingsrollen voor gebruikersaccounts in [!INCLUDE[prod_short](includes/cds_long_md.md)]

Met de basisintegratieoplossing worden de volgende rollen in [!INCLUDE[cds_long](includes/cds_long_md.md)] voor de integratie gemaakt:

* **Integratiebeheerder**: biedt gebruikers de mogelijkheid de verbinding te beheren tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[cds_long](includes/cds_long_md.md)]. Meestal is dit alleen toegewezen aan het automatisch gemaakte gebruikersaccount voor synchronisatie.
* **Integratiegebruiker**: geeft gebruikers toegang tot gesynchroniseerde gegevens. Meestal is dit toegewezen aan het automatisch gemaakte gebruikersaccount voor synchronisatie en andere gebruikers die de gesynchroniseerde gegevens moeten kunnen bekijken of openen.

> [!NOTE]
>
> De rollen **Integratiebeheerder** en **Integratiegebruiker** mogen alleen worden gebruikt door de toepassingsgebruiker die de integratie uitvoert. Aan de toepassingsgebruiker hoeft niet de [!INCLUDE[prod_short](includes/prod_short.md)]- of [!INCLUDE[cds_long](includes/cds_long_md.md)]-licentie te zijn toegewezen.

Als u de basisintegratieoplossing installeert, worden de machtigingen voor het integratiegebruikersaccount geconfigureerd. Als deze machtigingen handmatig worden gewijzigd, kunt u deze opnieuw instellen. Kies **Integratieoplossing opnieuw implementeren** op de pagina **Dataverse-verbinding instellen** om de basisintegratieoplossing opnieuw te installeren. Met deze stap wordt de beveiligingsrol van Business Central CDS-integratie geïmplementeerd.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also"></a>Zie ook

[Integreren met Microsoft Dataverse](admin-common-data-service.md)  
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
