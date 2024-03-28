---
title: Gebruikersaccounts instellen voor integratie met Microsoft Dataverse | Microsoft Docs
description: 'Leer hoe u gebruikersaccounts instelt die de apps gebruiken om gegevens uit te wisselen, en die personen gebruiken om toegang te krijgen tot gegevens in de apps en deze te synchroniseren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: null
ms.date: 01/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Gebruikersaccounts instellen voor integratie met Microsoft Dataverse via gegevenssynchronisatie

Dit artikel geeft een overzicht van hoe u de gebruikersaccounts instelt die vereist zijn om [!INCLUDE[prod_short](includes/cds_long_md.md)] te integreren met [!INCLUDE[prod_short](includes/prod_short.md)].

## Het beheerdersaccount instellen

Om de verbinding tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)] tot stand te brengen, moet u inloggen op [!INCLUDE[prod_short](includes/prod_short.md)] met een gebruikersaccount dat is toegewezen aan de [!INCLUDE[prod_short](includes/prod_short.md)] Essential- of [!INCLUDE[prod_short](includes/prod_short.md)] Premium-licentie. We zullen dit account eenmalig gebruiken om enkele vereiste componenten te installeren en configureren.

> [!IMPORTANT]
> Tijdens de installatie wordt u gevraagd om inloggegevens voor de [!INCLUDE[prod_short](includes/cds_long_md.md)] omgeving op te geven. Geef de inloggegevens op van een account dat een gebruiker met licentie is en dat is toegewezen aan de beveiligingsrol **Systeembeheerder** in de [!INCLUDE[prod_short](includes/cds_long_md.md)]-omgeving en aan globale beheerder op de tenant waartoe de omgeving behoort. Dit account heeft geen licentie nodig voor [!INCLUDE[prod_short](includes/prod_short.md)], omdat het alleen wordt gebruikt om instellingstaken uit te voeren in de [!INCLUDE[prod_short](includes/cds_long_md.md)]-omgeving.
>
> Nadat de verbinding is ingesteld, kunt u deze [!INCLUDE[prod_short](includes/cds_long_md.md)]-gebruiker verwijderen. De integratie blijft het gebruikersaccount gebruiken dat automatisch specifiek voor de integratie wordt gemaakt.

## Machtigingen en beveiligingsrollen voor gebruikersaccounts in [!INCLUDE[prod_short](includes/cds_long_md.md)]

Met de basisintegratieoplossing wordt de volgende rol in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] voor de integratie gemaakt:

* **Business Central Dataverse-integratie**: biedt u de mogelijkheid de verbinding te beheren tussen [!INCLUDE [prod_short](includes/prod_short.md)] en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Meestal is dit alleen toegewezen aan het automatisch gemaakte gebruikersaccount voor synchronisatie.

> [!NOTE]
> Alleen de toepassingsgebruiker die de integratie uitvoert, moet de rol **Business Central Dataverse Integratie** hebben. Aan de toepassingsgebruiker hoeft niet de [!INCLUDE [prod_short](includes/prod_short.md)]- of [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-licentie te zijn toegewezen.

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

## Zie ook

[Integreren met Microsoft Dataverse](admin-common-data-service.md)  
[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
